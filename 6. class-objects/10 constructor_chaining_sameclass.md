#### achieved through redirecting constructor, which cannot have field initializers

            class Software{
                var version;
                Software(this.version);
                //this is a redirecting constructor , but cannot have field initializer.
                Software.setVersion(this.version):this(ver);            //error: can't initialize this.version
            }

            main(List<String> args) {
              Software s =Software(1.11);  
            }

            solution : 

            class Software{
                var version;
                Software(this.version);
                //ver helping variable to initialize version
                Software.setVersion(var ver):this(ver);
            }

            main(List<String> args) {
              Software s =Software(1.11);  
            }


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


#### using this and super together

            abstract class Software{
                var version;
                Software(this.version);
                Software.setVersion(var ver):this(ver);
            }
            class Windows extends Software{
              var version;
              Windows(this.version): super.setVersion(version){
                print("windows constructor");
              }

            }
            main(List<String> args) {

            }
            
####             
