#### library/sourcefile private instance variable

#### if instance variable begins with underscore, this variable is specific to library or current source file

#### test.dart

        class Student {
          String _name; //private to current sourcefile/library
        }

        main() {
          var student =Student();
          student._name = "hello";
        }

#### sample.dart

        import 'test.dart';
        main(List<String> args) {
            Student student =Student();
            student.name = "ranjit";    //error
        }
