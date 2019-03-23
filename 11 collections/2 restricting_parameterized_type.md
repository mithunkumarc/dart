When implementing a generic type, you might want to limit the types of its parameters. You can do this using extends.


            class Animal{
              void eat(){
                print("animal eat");
              }
            }
            class Dog extends Animal{
              void eat(){
                print("dog eat");
              }
            }

            class Cat extends Animal{
              void eat(){
                print("cat eat");
              }
            }


            class Pigeon {
              void eat(){

              }
            }

            class DisplayAnimals<T extends Animal>{     //T must be subclass of animal

               void printInfo(List<T> list){
                  for (dynamic item in list) {
                      item.eat();
                  }
              }
            }

            main(List<String> args) {
              List<Dog> dogList = [Dog(),Dog(),Dog(),Dog()];
              new DisplayAnimals().printInfo(dogList);
              List<Animal> animalList = [Cat(),Dog(),Cat(),Dog()];
              new DisplayAnimals().printInfo(animalList);
              
              //error
              List<Pigeon> pigeonList = [Pigeon(),Pigeon()];
              new DisplayAnimals().printInfo(pigeonList);   //error
            }
            
            
            dog eat
            dog eat
            dog eat
            dog eat
            cat eat
            dog eat
            cat eat
            dog eat
