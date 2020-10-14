```ads
with Avion_Sol ;
with Tour ;

procedure MISSION2A is

package AS renames Avion_Sol ;

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
end ROULER_DK ;

procedure TESTER_ROULAGE is
begin
Rouler_KA ;
Tour.Attendre_Autorisation_Decollage ;
AS.Parcourir_Piste ;
Rouler_DK ;
end TESTER_ROULAGE ;

begin
Tester_Roulage ;
end MISSION2A ;
```
