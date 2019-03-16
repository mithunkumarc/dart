#### Default constructor : similar to java

#### constructors are not inherited

      If you don’t declare a constructor, a default constructor is provided for you. 
      The default constructor has no arguments and invokes the no-argument constructor in the superclass.//similar to java



#### when object is created , constructor is called

        class Point{
          int x;
          int y;
          Point(){
            print("constructor called");
          }  
        }
        main(List<String> arguments) {
            Point(); // calls constructor
        }
