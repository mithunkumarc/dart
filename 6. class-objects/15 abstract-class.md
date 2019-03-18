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
