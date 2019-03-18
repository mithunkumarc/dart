class Animal{
  var name;
  var weight;
}
class Dog extends Animal{
  
}
main(List<String> args) {
  var d= new Dog();
  print(d.runtimeType);//type dog, type inference : depends on object
  
}
