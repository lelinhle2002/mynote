```ads
with GAda.Text_IO ;
with Assert;
with Tour;
with Train;
with Simulation;
with Insa_Air;
with Cartographie;

procedure Mission3 is
   package Txt renames GAda.Text_IO;
procedure Info_Aeroport (code:string) is
Pos : Cartographie.T_coords;
 begin 
      Pos := Cartographie.Coords_Aeroport(Code);
      Txt.Put("Aeroport " & Code & " = " & Cartographie.Nom_Aeroport(Code)) ;
      Txt.Put_Line (" Lattitude = " & Float'Image(Pos.Lat) & " Long = " & Float'Image(Pos.Long));
end Info_Aeroport;
procedure Tester_Carto is
begin
Info_Aeroport ("LFBO") ;
Info_Aeroport ("EGLL") ;
Info_Aeroport ("LFPG") ;
end Tester_Carto ;
function Distance (P1 : Cartographie.T_Coords ; P2 : Cartographie.T_Coords) return Float is
 begin
 return 111.600 * (Cartographie.Sqrt ((P1.Lat - P2.Lat)**2 + (P1.Long - P2.Long)**2)) ;
 end Distance ;
function Cap_Cible (Cible : String) return Float is
   Aero : Cartographie.T_Coords;
   Avion: Cartographie.T_Coords;
begin
     Aero := Cartographie.Coords_Aeroport (Cible) ;
     Avion := Cartographie.Coords_Avion ;
     return Cartographie.Cap_Vecteur (Aero.Long - Avion.Long, Aero.Lat - Avion.Lat);
end Cap_Cible;
procedure Tester_cap_cible is
begin
Txt.Put_Line ( Float'Image (Cap_Cible("EGLL"))) ;
end Tester_cap_cible ;
procedure Naviguer_Vers (Code:String) is
   begin
   while (Distance(P1 : Cartographie.T_Coords,P2: Cartographie.T_Coords))>=100.0 loop
   Txt.Put_Line (Float'Image (Cap_Cible));
   end loop;
   if (Distance(P1,P2))<100.0 then
   Cartographie.Placer_Marque(Point);
   end if;
end Naviguer_Vers ;

procedure DEMO_VOL is
  begin
 Txt.Put_Line(Naviguer_Vers(Code));
end DEMO_VOL;
begin
   Naviguer_Vers(BOD);
end Mission3

```
