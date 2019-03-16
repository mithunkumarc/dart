#### const context 
#### using const to variable is enough, no need to use const to all values of map is not neede
  
          class Point{
            final int x;
            final int y;
            const Point(this.x,this.y);  
          }
        
        
        main(List<String> arguments) {
          
          //creating immutable map ; const keyword used for all values
          const pointLine = {
              'point' : const [const Point(11, 11)],
              'line' : const [const Point(12, 12), const Point(15,15)]
          };

          //const context : using const for variable is enough, no need to use multiple times to create immutable map
          const pointAndLine = {
              'point' : [  Point(11, 11)],
              'line' : [ Point(12, 12), Point(15,15)]
          };

          //trying add new entries to map leads to error
          MapEntry<String,List<Point>> entry1   =MapEntry("triangle" , [Point(100,100)]);
          MapEntry<String,List<Point>> entry2   =MapEntry("triangle" , [Point(100,100)]);
          Iterable<MapEntry<String, List<Point>>> iterable = {entry1,entry2};

          pointLine.addEntries(iterable);//error
          pointAndLine.addEntries(iterable);//error

        }
