#### named constructor : used name of constructor while creating objects

#### instead of using overloaded constructor , use named constructor for extra clarity

#### named constructor replace overloaded constructor 

          Use a named constructor to implement multiple constructors for a class or to provide extra clarity:

      
          class Person {
                String firstName;

                Person.fromJson(Map data) {
                  this.firstName = data['name'];
                }

                Person.fromString(String name){
                  this.firstName = name;
                }
          }

          main() {
                var person = new Person.fromJson({"name":"rajat"});
                print(person.firstName);
                var person_string = new Person.fromString("ajay");
                print(person_string.firstName);
          }
          
#### without overload construcot : error

        class Person {
          String firstName;

           Person(Map data) {
             this.firstName = data['name'];
           }


           Person(String name){   // only one unnamed constructor is supported, which is already defined above
             this.firstName = name;
           }
        }
