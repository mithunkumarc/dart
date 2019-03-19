#### static : same as java

#### accessed through class name, cannot use this.

#### use double underscore in the beginning for static private (for current file) variable/method

#### static method can also be created, cannot access properties of object

#### static method are not inherited


          class Student{
            //private static variable
            static var __library = "books";
            //public static variable
            static var number = 0;
            //static/class method
            static int getCount() => number;

            var name;
            Student.asName(this.name){
              number++;
            }

          }
          main(List<String> args) {
            var student1 = Student.asName("rajat");
            var student2 = Student.asName("vinay");
            var student3 = Student.asName("vikram");
            var student4 = Student.asName("anin");
            var student5 = Student.asName("arun");

            print(Student.number);//5
            print(Student.getCount());//5
            print(Student.__library);//books
          }
