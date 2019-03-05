#### is operator, check var is pointing to specific type or not


        void main(List<String> args) {
          var emp = new Person();
          print(emp is Person);

        }
        class Person{

        }


#### as operator : Use the as operator to cast an object to a particular type. : similar to instanceof in java

        
        void main(List<String> args) {
          var emp = new Person();
          (emp as Person).firstName = "ranjit";
          print(emp.firstName);
        }
        
        class Person{
          String firstName;
        }
        
        example 2 : 

        void main(List<String> args) {
          var emp = new Person();
          print(emp as Person);
        }
        class Person{

        }

        output : 
        Instance of 'Person'
