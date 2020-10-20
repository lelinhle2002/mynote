```ads
procedure Info_Aeroport (code:string) is
Pos : Cartographie.T_coords;
 begin 
      Pos := Cartographie.Coords_Aeroport;
      Txt.Put("Aeroport " & Code & " = " & Cartographie.Nom_Aeroport(Code)) ;
      Txt.Put_Line (" Lat. = " & Float'Image(Pos.Lat) & " Long. = " & Float'Image(Pos.Long)) ;
end Info_Aeroport;
procedure Tester_Carto is
begin
Infos_Aeroport ("LFBO") ;
Infos_Aeroport ("EGLL") ;
Infos_Aeroport ("LFPG") ;
end Tester_Carto ;
function Distance (P1 : Cartographie.Des_Coords ; P2 : Cartographie.Des_Coords) return Float is
 begin
 return 111.600 * (Cartographie.Sqrt ((P1.Lat - P2.Lat)**2 + (P1.Long - P2.Long)**2)) ;
 end Distance ;
function Cap_Cible (Cible : String) return Float is
Aero : Cartographie.Des_Coords ;
Avion : Cartographie.Des_Coords ;
begin
     Aero := Cartographie.Coords_Aeroport (Cible) ;
     Avion := Cartographie.Coords_Avion ;
     return Cartographie.Cap_Vecteur (Aero.Long - Avion.Long, Aero.Lat - Avion.Lat));
end Cap_Cible;
procedure Tester_cap_cible is
begin
Txt.Put_Line ("Cap_Cible vers Heathrow : " & Float'Image (Cap_Cible("EGLL"))) ;
end Tester_cap_cible ;
procedure Naviguer_Vers 
```
