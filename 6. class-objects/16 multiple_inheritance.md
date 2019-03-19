

#### dart supports multiple inheritance through mixins

        //mixin 
        class recordable{
          //this is mixin, don't include constructor
          record(){

          }
        }
        //mixin
        class dth{
          //this is mixin, don't include constructor
          recharge(){
          }
        }
        class Electronics{}
        class TV with recordable,dth{

        }

#### mixins are similar to class but without constructors

#### mixin dont use constructors, to avoid child parent constructor complications 

        class recordable{
          //this is mixin, don't include constructor
          record(){

          }
        }




#### mixins can be declared using class or mixin keyword, but without constructors


      //mixin with class keyword 
      class recordable{
        //this is mixin, don't include constructor
        record(){

        }
      }

      //mixin with mixin keyword
      mixin dth{
        //this is mixin, don't include constructor
        recharge(){
        }
      }





#### a class can extends one class and use multiple mixins

#### use extends for inheritance and use with keyword for mixins

            //mixin 
            class recordable{
              //this is mixin, don't include constructor
              record(){

              }
            }
            //mixin
            mixin dth{
              //this is mixin, don't include constructor
              recharge(){
              }
            }
            class Electronics{}
            class TV extends Electronics with recordable,dth{

            }     
