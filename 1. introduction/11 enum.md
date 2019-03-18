#### user defined constants : 

          enum colors{ green, red ,blue, mixedcolor}

          main(List<String> args) {
              //var option =colors.green;
              var option =colors.mixedcolor;
              switch(option){
                  case colors.blue : print("i am blue");
                   break;
                  case colors.green : print("i m green");
                  break;
                  case colors.red : print("i am red");
                  break;        
                  default: print("sorry wrong color");
                  break;
              }      
          }


