#### abstract class : similar to java, subclass either maintain abstract or implement abstract method

#### object of abstract class cannot be created


            abstract class Software{
                var version;
                //abstract method
                void install();
            }


            class Windows extends Software{
              void install(){
                print("follow bootable pendrive to install...");
              }
            }

            main(List<String> args) {
              //Software software = Software();//obj cannot be created
              Windows windows =Windows();
              windows.install();
            }   


#### constructor chaining with abstract class

            abstract class Software{
                var version;
                void install();
                Software(this.version){
                  print("sofware constructor");
                }
            }
            
            class Windows extends Software{
              var version;
              
              //super: calling base class constructor
              Windows(this.version): super(version){
                print("windows constructor");
              }
              void install(){
                print("install windows sofware..");
              }
            }
            
            main(List<String> args) {
              //Software software = Software();//obj cannot be created
              
              Windows windows = Windows(1.1);
              windows.install();
            }
            
            ouput : 
            sofware constructor
            windows constructor
            install windows sofware..
