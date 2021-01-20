```adb
http://wwwperso.insa-toulouse.fr/~lebotlan/Y/Ada-S2/exo-traces.html
with GAda.Text_IO ;
with Rois;
procedure Mission1 is
         procedure Tracer_Rectangle ( Largeur : integer; Hauteur: integer) is
                 a: character:='#';
                 b: string:=" ";
                  begin
                  for x in 1..hauteur loop 
                     if x=1 or x= hauteur then
                      for i in 1..largeur loop
                            GAda.Text_IO.put(a);
                      end loop;

                                GAda.Text_IO.new_line;
                     else 
                       for i in 1..largeur loop
                         if i=1 or i= largeur then
                            GAda.Text_IO.put(a);
                         else GAda.Text_IO.put(b);
                         end if;
                      end loop;
                      GAda.Text_IO.new_line;
                      end if;
                   end loop;
         end Tracer_Rectangle;
        begin
                   Tracer_Rectangle(5,5);
                    Tracer_Rectangle(6,5);
                    Tracer_Rectangle(10,20);
         

end Mission1 ;
```
2.
```adb
with GAda.Text_IO ;
with Rois;
procedure Mission1 is
         procedure Tracer_Quadrillage ( Largeur : integer; Hauteur: integer) is
                 a: character:='#';
                 b: string:=" ";
                  begin
                  for x in 1..hauteur loop 
                     if x mod 2 /= 0  then
                      for i in 1..largeur loop
                            GAda.Text_IO.put(a);
                      end loop;

                                GAda.Text_IO.new_line;
                     else 
                       for i in 1..largeur loop
                         if i mod 2=0  then
                            GAda.Text_IO.put(b);
                         else GAda.Text_IO.put(a);
                         end if;
                      end loop;
                      GAda.Text_IO.new_line;
                      end if;
                   end loop;
         end Tracer_Quadrillage;
        begin
                   Tracer_Quadrillage(5,5);
                   --Tracer_Quadrillage(6,5);
                   --Tracer_Quadrillage(14,2);
         

end Mission1 ;
```
