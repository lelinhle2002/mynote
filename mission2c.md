```ads
with Assert ;
with Gada.Text_IO ;
with Avion_Sol, INSA_Air ;
with Train, Tour, Pilote_Automatique, Carburant ;

procedure Mission2c is
package TXT renames GAda.Text_IO ;
package IA renames INSA_Air ;
package AS renames Avion_Sol ;
package PA renames Pilote_Automatique ;

procedure ROULER_KA is
begin
Tour.Attendre_Autorisation_Roulage ;
AS.Rouler_Vers ('L') ;
AS.Rouler_Vers ('M') ;
AS.Rouler_Vers ('E') ;
AS.Rouler_Vers ('A') ;
end ROULER_KA ;

procedure ROULER_DK is
begin
AS.Rouler_Vers ('N') ;
AS.Rouler_Vers ('P') ;
AS.Rouler_Vers ('M') ;
AS.Rouler_Vers ('L') ;
AS.Rouler_Vers ('K') ;
AS.Freiner ;
end ROULER_DK ;
Angle_Tour : constant Float := 360.0 ;
Demi_Tour : constant Float := Angle_Tour / 2.0 ;

function DELTA_CAP (Cap_Actuel : Float ; Cap_Voulu : Float) return Float is
Resultat : Float ;
begin
Resultat := Cap_Voulu - Cap_Actuel ;
if Resultat > Demi_Tour then Resultat := Resultat - Angle_Tour ;
elsif Resultat < - Demi_Tour then Resultat := Resultat + Angle_Tour ;
end if ;
return Resultat ;
end DELTA_CAP ;
procedure TESTER_DELTA_CAP (CapA : Float ; CapV : Float) is
begin
Txt.Put_Line ("Delta_Cap " & Float'Image(CapA) & ", " &
Float'Image(CapV) & " = " &
Float'Image(Delta_Cap(CapA, CapV))) ;
end TESTER_DELTA_CAP ;

function CAPS_EGAUX (Cap1 : Float ; Cap2 : Float) return Boolean is
Tolerance : constant Float := 5.0 ;
begin
return abs (Delta_Cap (Cap1, Cap2)) < Tolerance ;
end CAPS_EGAUX ;

procedure TESTER_CAPS_EGAUX (Cap1, Cap2 : Float) is
begin
Txt.Put ("Les caps " & Float'Image(Cap1) & " et " &
Float'Image(Cap2) & " ") ;
if Caps_Egaux(Cap1, Cap2) then
Txt.Put_Line (" sont égaux (à 5 degrés près).") ;
else
Txt.Put_Line (" ne sont pas égaux (à 5 degrés près).") ;
end if ;
end TESTER_CAPS_EGAUX ;

begin
Assert.Failif (Cible < 0.0 or Cible > Angle_Tour, "Cap_Vers : cap incorrect = " & Float'Image(Cible)) ;
while not (Caps_Egaux (Cible, IA.Cap)) loop
if Delta_Cap (IA.Cap, Cible) < 0.0 then INSA_Air.Gouverne_A_Gauche ;
else
INSA_Air.Gouverne_A_Droite ;
end if ;
end loop ;
INSA_Air.Gouverne_A_Zero ;
end CAP_VOL_VERS ;

procedure VOL_DEMO is
Cap_Aller : constant Float := 295.0 ;
Cap_Retour : constant Float := 115.0 ;
Temps_Aller : constant Float := 20.0 * 60.0 ;
Temps_Retour : constant Float := 15.0 * 60.0 ;
Reacteur_Decollage : constant Integer := 8 ;
Reacteur_Vol_Croisiere : constant Integer := 6 ;
Reacteur_Atterrissage : constant Integer := 3 ;

begin
Carburant.Faire_Le_Plein ;
IA.Nom_Compagnie("Kako-Air") ;
Rouler_KA ;
Tour.Attendre_Autorisation_Decollage ;
IA.Regler_Reacteur (Reacteur_Decollage) ;
PA.Decoller ;
IA.Regler_Reacteur (Reacteur_Vol_Croisiere) ;
Train.Mouvement_Train (False) ;
Cap_Vol_Vers (Cap_Aller) ;
IA.Attendre(Temps_aller) ;
Cap_Vol_Vers (Cap_Retour) ;
IA.Attendre(Temps_Retour) ;
IA.Regler_Reacteur (Reacteur_Atterrissage) ;
Train.Mouvement_Train (True) ;
Tour.Attendre_Autorisation_Atterrissage ;
PA.Atterrir ;
Rouler_DK ;
end VOL_DEMO ;

begin
Vol_Demo ;
end MISSION2C ;
```
