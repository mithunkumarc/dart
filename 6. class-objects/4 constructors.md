#### constructor : initialize properties

         class Point{
          int x,y;
          Point(var x,var y){
            this.x = x;
            this.y = y;
          }
          @override
          String toString() {
            return "x : "+ this.x.toString() + ", " +" y : " + this.y.toString();
          }
        }

        main() {
          Point p = new Point(10,45);
          print(p);
        } 
        
        
#### another simple way to write constructor

        class Point{
          int x,y;
          
          Point(this.x,this.y);
          
          @override
          String toString() {
            return "x : "+ this.x.toString() + ", " +" y : " + this.y.toString();
          }
        }        


#### overloaded constructor: named constructors can be used to achieve constructor overloading

         class Software{
           var version;
           Software.asString(this.version);
           Software.asNumber(this.version);    

         }

         main(List<String> args) {
           Software s1 = new Software.asString("1.11");
           Software s2 = new Software.asNumber(1.11);
           print('asString ${s1.version}');
           print('asNumber ${s2.version}');
         }
         
         version : 
         asString 1.11
         asNumber 1.11
