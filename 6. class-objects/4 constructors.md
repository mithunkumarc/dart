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
