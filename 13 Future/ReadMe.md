#### avoid callback : use asyc and await
        
        const oneSecond = Duration(seconds: 1);

        Future<void> printWithDelay(String message) async {
          await Future.delayed(oneSecond);
          print(message);
        }

        main(List<String> args) {
          printWithDelay("hello dart");
        }
        output : hello world (will be displayed after 1 second)
        
        
        
#### above code is equivalent to below code

        const oneSecond = Duration(seconds: 1);
        Future<void> printWithDelay(String message) {
          return Future.delayed(oneSecond).then((_) {
            print(message);
          });
        }
        main(List<String> args) {
          printWithDelay("hello dart");
        }
