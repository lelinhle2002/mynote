```ads
with Assert ;
with Gada.Text_IO ;
with Avion_Sol, INSA_Air ;
with Train, Tour ;

procedure Mission2b is
package TXT renames GAda.Text_IO ;
package IA renames INSA_Air ;
package AS renames Avion_Sol ;

function DELTA_CAP (Cap_Actuel : Float ; Cap_Voulu : Float) return Float is
Resultat : Float ;

begin
Resultat := Cap_Voulu - Cap_Actuel ;
if Resultat > 180.0 then Resultat := Resultat - 360.0 ;
elsif Resultat < -180.0 then Resultat := Resultat + 360.0 ;
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

procedure ORIENTER_AU_SOL (Cap : Float) is
begin
Assert.Failif (Cap < 0.0 or Cap > 360.0, "Cap_Vers : cap incorrect = " & Float'Image(Cap)) ;
IA.Regler_Reacteur (1) ;
while not (Caps_Egaux (Cible, IA.Cap)) loop
if Delta_Cap (IA.Cap, Cible) < 0.0 then Train.A_Gauche ;
else
Train.A_Droite ;
end if ;
end loop ;
Train.A_Zero ;
AS.Freiner ;
end ORIENTER_AU_SOL ;

begin
Tour.Attendre_Autorisation_Roulage ;
AS.Rouler_Vers ('L') ;
AS.Rouler_Vers ('M') ;
AS.Freiner ;
ORIENTER_AU_SOL(0.0) ;
AS.Attendre_Entree ;
ORIENTER_AU_SOL(90.0) ;
AS.Attendre_Entree ;
ORIENTER_AU_SOL(270.0) ;
AS.Attendre_Entree ;
ORIENTER_AU_SOL( 180.0) ;
AS.Attendre_Entree ;
AS.Rouler_Vers ('M') ;
AS.Rouler_Vers ('L') ;
AS.Rouler_Vers ('K') ;
end TESTER_CAP ;

begin
Tester_Delta_Cap (0.0, 45.0) ;
Tester_Delta_Cap (45.0, 0.0) ;
Tester_Delta_Cap (350.0, 10.0) ;
Tester_Delta_Cap (10.0, 350.0) ;
Tester_Delta_Cap (30.0, 285.0) ;
Tester_Caps_Egaux (0.0, 10.0) ;
Tester_Caps_Egaux (-10.0, 0.0) ;
Tester_Caps_Egaux (358.0, 2.0) ;
Tester_Cap ;
end Mission2b ;
```
