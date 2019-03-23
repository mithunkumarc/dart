private var cannot be accessed outside file

helloword.dart

      int i = 100;
      int j = 200;
      int _k = 300;//private variable


sample.dart

        import 'helloword.dart';
        main(List<String> args) {  
          print(i);
          print(j);
          print(k);//error : k is private
        }




#### calculator.dart

      add(){
        print("add");
      }

      sub(){
        print("sub");
      }
      
      

#### import 'calculator.dart' as calci;

      import 'calculator.dart' as calci;
      //import 'package:electronics/tv.dart';
      main(List<String> args) {
        calci.add();
        calci.sub();
      }
