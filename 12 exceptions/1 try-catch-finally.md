
          class OutOfLamaException implements Exception{
            String message;
            OutOfLamaException(this.message);
          }

          breeMoreLamas(){
            throw OutOfLamaException("out of lama");
          }

          main(List<String> args) {
            try{
              breeMoreLamas();
            }on OutOfLamaException{
              print("some plan to generate more lama");
            }on Exception catch (e){
              print("some unknown exception occured "+e.toString());
            }
          }
