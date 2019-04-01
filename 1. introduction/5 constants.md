#### const : cannot be reinitialized (implicitly final)

      void main(){
          const i = 10;
          const b = true;
          const d = 35.5;
          const l = [];
          const m = {};
          i =  15;    //error
          b = false;  //error
          d = 454.65; //error
          l = [];     //error
          m = {};     //error
      }

#### const : var must be initialised
      
      const i;//error : const var must be initialized
      
      
####      
