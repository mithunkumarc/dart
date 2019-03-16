#### helps to create immutable object : 
#### mark constructor as constant and instance variables as final to create immutable object

        class ImmutablePoint{
          final int x;
          final int y;
          const ImmutablePoint(this.x, this.y);  
         static final ImmutablePoint origin =  const ImmutablePoint(0, 0);  
        }

        main(List<String> arguments) {
          //immutable object
          var immutalbepoint = ImmutablePoint.origin;
        }
