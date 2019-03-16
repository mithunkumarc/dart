#### default value of instance variables(of all datatypes) is null

                class Point{
                  int x;
                  int y;
                  int z;        
                  Point(this.x,this.y); //z is skipped , so initailized with null

                }
                main(List<String> arguments) {
                  var point = Point(2,4);
                  print(point.x);
                  print(point.y);
                  print(point.z);  //null
                }



#### <ref_var>?.<property> = value,    if ref_var is not null, sets value

        class Point{
          int x,y;
          Point(this.x,this.y);
        }
        main() {
          Point p;//not initialized
          p.x = 5; //error
          p?.x = 5;//no error, if there is an object , then sets value or else skips execution
          print(p.x);//error since there is not object, no field called x
        } 
        


