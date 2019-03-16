#### Factory constructors : similar to factory class in java

#### java uses , static methods to create instance(immutable/singleton)

#### Note: Factory constructors have no access to this.


          class Logger{
          
          
              final String name;
              
              //factory constructors cannot use this keyword , takes help of named constructor, coz it has 'this' keyword access
              factory Logger(String name){
                  //use map, if there is already a logger with same name, return that 
                  //else create new Logger object using named constructor which has 'this' keyword access
                  
                  final logger = Logger._internal(name);        //calling named constructor
                  
                  return logger;
              }
              
              Logger._internal(this.name);//not visible outside this sourcefile
          
          }


          main(List<String> args) {
            var logger = Logger('debug');

            print(logger.name);  
          }

          output : debug
