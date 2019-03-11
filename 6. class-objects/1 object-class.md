
* Dart is an object-oriented language with classes and mixin-based inheritance. 

* Every object is an instance of a class, and all classes descend from Object. 

* Mixin-based inheritance means that although every class (except for Object) has exactly one superclass, a class body can be reused in multiple class hierarchies.


###  Object class

        The base class for all Dart objects.

        Because Object is the root of the Dart class hierarchy, every other Dart class is a subclass of Object.

        When you define a class, you should override toString to return a string describing an instance of that class. 

        You might also need to define hashCode and operator ==, 
        as described in the Implementing map keys section of the library tour.



#### Properties

        hashCode → int
            The hash code for this object. [...]
            read-only
        runtimeType → Type
            A representation of the runtime type of the object.
            read-only

#### Methods

        noSuchMethod(Invocation invocation) → dynamic
            Invoked when a non-existent method or property is accessed. [...] 

        toString() → String
            Returns a string representation of this object. 


#### example for nosuchmethod

      nosuchmethod will be called when object calls a method on itself with method name which doesn't exists

      class A { 
        noSuchMethod(Invocation i) {
          return "there is no such method";
        } 
      }

      main() {
        Object o = new Object();
        //print((new A()).foo()); error
        //fool compiler , use dynamic
        print((new A() as dynamic).foo());  
      } 
      
      
