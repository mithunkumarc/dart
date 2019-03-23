
        const oneSecond = Duration(seconds: 1);

        Future<void> printWithDelay(String message) async {
          await Future.delayed(oneSecond);
          print(message);
        }

        main(List<String> args) {
          printWithDelay("hello dart");
        }
        output : hello world (will be displayed after 1 second)
        
        
        
