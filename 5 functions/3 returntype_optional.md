#### return type is optional

#### if a function returns another function, you can use Function as type to store function.

        //no return type , return type is optional
        tell_me_something(){
          return "hello , how are you";
        }
        
        
        add(var i,var j){
          return i + j;
        }

        get_square_logic(){
          //return type Function
          return (number) => number * number;
        }

        main(List<String> arguments) {
          print(tell_me_something());
          print(add(4,5));
          Function square =get_square_logic();  //Function is a type
          print(square(10));
        }
