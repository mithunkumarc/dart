

        import 'dart:convert';


        // this is cool , variables , can be declared outside class and functions ,just like python
        // This string is JSON, not Dart.
        var jsonString = '''
          [
            {"score": 40},
            {"score": 80}
          ]
        ''';

        var scores = jsonDecode(jsonString);

        var firstScore = scores[0];

        main(List<String> args) {
          print(firstScore);
        } 
