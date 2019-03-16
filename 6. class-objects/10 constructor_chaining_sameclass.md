#### also called redirecting constructor

#### constructor calling similar to c++ and csharp, this and super used along with constructor declaration



            class Student {
              String name;
              int age;

              //user provided default constructor
              Student(this.name,this.age);

              //redirecting constructor, this constructor call default construcotor
              Student.fromMap(Map data) : this(data['name'],data['age']);

            }

            main() {
              var student =Student('ranjit',25);
              print(student.name);//ranjit
              print(student.age);//25
            }
