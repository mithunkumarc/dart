== and identical : both checks whether two references pointing to same object or not


#### without overrding == operator

        class Point{
          int x,y;
          Point(this.x,this.y);

        }
        main() {
          var p1 = new Point(10, 10);
          var p2 = new Point(10, 10);
          print(p1 == p2);           
        } 

        output : false , two references pointing to two diff objects even though content is same
        
        
#### overriding == operator , checks content

        overrding double equal == operator checks the content of two references/object are same or not

        class Point{
          int x,y;
          Point(this.x,this.y);
            //similar to overriding equals in java
            //operator overloading
             bool operator == (other){
               return other.x == x && other.y == y;
        }


          }
        main() {
          var p1 = new Point(10, 10);
          var p2 = new Point(10, 10);
          print(p1 == p2);//without == operator overloading
        } 


        # ouput : true
        
        
        




#### identical checks whether two references points to same object

        class Point{
          int x,y;
          Point(this.x,this.y);
        }
        
        main() {
          var p1 = new Point(10, 10);
          var p2 = new Point(10, 10);

          //identical : checks whether two reference points to same object  
          print(identical(p1, p2));   //false , points to two diff objectts
          
          var p3 = p1
          print(identical(p1, p3));   //true , points to same objectts
          
        } 

        output : false
                  true









#### identical : 
