```adb
with GAda.Text_IO ;

procedure mission2s2 is
         type T_Intervalle is record
             Inf: float;
             Sup: float;
         end record;
         function Intervalle_Image (C: T_Intervalle) return String is
              begin
                   return ("[" & integer'image(integer(C.Inf))& integer'image(integer(C.Sup)) & "]");
         end Intervalle_Image;
         function Est_Inclus (A: T_intervalle; B:T_Intervalle) return Boolean is
              begin 
                   If A.Inf > B.Inf and A.Sup < B.Sup then
                       return (2>1) ;
                   end if;
                   
              end Est_Inclus;
         function Disjoints (A: T_intervalle; B:T_Intervalle) return Boolean is 
              begin 
                   if (  A.Inf < B.Inf and A.Sup < B.Inf) or ( A.Inf > B.Sup and A.Sup > B.Sup) then 
                          return (2>1);
                   end if;
                   
              end Disjoints;
         procedure Afficher_Relation (A: T_intervalle; B:T_Intervalle) is
                begin
                 if Est_Inclus(A,B) then
	               GAda.Text_IO.Put("A est inclus dans B");
                else if Est_Inclus (B,A) then
	                 GAda.Text_IO.Put("B est inclus dans A");
                else if Disjoints (A,B) then
	                 GAda.Text_IO.Put("A et B sont disjoints");
                 else 
	                  GAda.Text_IO.Put("A et B ne sont pas disjoints");
               end if;
               end if;
               end if;
            end Afficher_Relation;
         C: T_Intervalle;
   D: T_Intervalle;
   E: T_Intervalle;
begin
    C.Inf:= 5.0;
    C.Sup:=10.0;
     D.Inf:=7.0;
     D.Sup:=8.0;
     E.Inf:=4.0;
     E.Sup:=6.0;
     Afficher_Relation(C,D);
     Afficher_Relation(D,C);
     Afficher_Relation(C,E);
     Afficher_Relation(D,E);
   
         

end mission2s2 ;
```
