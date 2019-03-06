helloworld.dart

        Function get_me_logic(){
          var square = (number) => number * number;
          return square;
        }
        main(List<String> args) {

        }
        
sample.dart imports get_me_logic() from helloworld.dart

        import 'helloword.dart';
        main(List<String> args) {
          Function t = get_me_logic();
          print(t(5));  
        }
