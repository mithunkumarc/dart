#### function can be defined inside a function : 

          main(List<String> args) {
              int add(a,b){     //its ok not to write type for parameters
                return a+b;
              }
              print(add(4,5));    
          }
          
          output : 9
          
          

#### if function returns a function use return type as Function

          Function get_me_logic(){
            var square = (number) => number * number;
            return square;
          }

          main(List<String> args) {
              //var also works
              //final also works
              //const won't works, it needs a const value
              //dynamic works
              Function my_square = get_me_logic();
              print(my_square(10)); //output : 100
          }



#### function can return logic


        main(List<String> args) {

          Function add_logic(){   //Function : keyword is optinal
            return (a,b) => a+b;
          }

          var logic = add_logic();
          print(logic(4,5)); //ouput : 9
        }


