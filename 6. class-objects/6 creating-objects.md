#### objects can be created with or without using new keyword
#### when obj is created , mem is allocated, 

        class Point{
          int x;
          int y;
          Point(this.x,this.y);
        }
        main(List<String> arguments) {
          var point = Point(2,4);
          var point1 = new Point(4, 5);
          print(point is Point);//true
          print(point1 is Point);//true  
        }
