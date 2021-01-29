```adb
with GAda.Text_IO ;

procedure Mission2 is
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
                       return True;
                   end if;
              end Est_Inclus;
         function Disjoints (A: T_intervalle; B:T_Intervalle) return Boolean is 
              begin 
                   if A.Inf < B.Inf and A.Sup > B.Sup then
                   
         

end Mission2 ;
```
