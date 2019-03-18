#### inheritance: 

        class Animal{
          var __name,age;
          //__name : private to current file
        }
        class Dog extends Animal{

        }
        main(List<String> args) {
          var d = new Dog();
          d.__name = "tex";
          d.age = 2;
          print(d.__name);//animal
          print(d.age);//2
        }
        
        output : 
          tex
          2
  
#### instance var value decided by reference type and method by object

            class Animal{
              var name = "animal name";
              var weight = "weight name";
              void eat(){
                print("animal eat");
              }
            }
            class Dog extends Animal{
              void eat(){
                print('dog eat');
              }
            }
            main(List<String> args) {
              var d= new Dog();
              d.name = "dog name";

              Animal a = new Dog();
              print(d.runtimeType); //Dog
              print(a.runtimeType); //Dog

              // value of instance variable decided by type of reference variable
              print(d.name);//dog name
              print(a.name);//animal name

              //method called depends on type of object on which they called
              d.eat();//dat eat, obj is dog
              a.eat();//dat eat, obj is dog

            }
           
