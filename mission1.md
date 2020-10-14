with Simulation ;
procedure MISSION1 is
package S renames Simulation ;

procedure ROULER_KA is
begin

S.Attendre_Autorisation_Roulage ;
S.Rouler_Vers ('L') ;
S.Rouler_Vers ('M') ;
S.Rouler_Vers ('E') ;
S.Rouler_Vers ('A') ;
end ROULER_KA ;

procedure ROULER_DK is
begin
S.Rouler_Vers ('N') ;
S.Rouler_Vers ('P') ;
S.Rouler_Vers ('M') ;
S.Rouler_Vers ('L') ;
S.Rouler_Vers ('K') ;
end ROULER_DK ;


procedure TESTER_ROULAGE is
begin

Rouler_KA ;
S.Attendre_Autorisation_Decollage ;
S.Parcourir_Piste ;
Rouler_DK ;
end TESTER_ROULAGE ;

begin
Tester_Roulage ;
end MISSION1 ;
