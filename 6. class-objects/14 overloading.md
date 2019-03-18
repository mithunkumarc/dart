#### no overloading method in dart
#### supports optional parameters



          class Game{
            //player1 : positional argumnet
            //player2 and time are optional
            void play(var player1,[var player2, var time]){
              print(player1);
              print(player2);
              print(time);
              print("*"*10);
            }

          }
          main(List<String> args) {
            var game = Game();
            game.play("kumar"); //player2 and time is null
            game.play("kumar","vasu");//time null
            game.play("kumar","sridhar","1.11");
          }
          
          output : 
          
          kumar
          null
          null
          **********
          kumar
          vasu
          null
          **********
          kumar
          sridhar
          1.11
          **********
