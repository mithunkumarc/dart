
            import 'dart:collection';
            void main(){
                  var gifts = {
                    // Key:    Value
                    'first': 'partridge',
                    'second': 'turtledoves',
                    'fifth': 'golden rings'

                  };


                 var nobleGases = {
                    2: 'helium',
                    10: 'neon',
                    18: 'argon',
                  }; 


                 print(gifts.runtimeType);//_InternalLinkedHashMap<String,String>
                  print(nobleGases.runtimeType);//_InternalLinkedHashMap<int,String>



                  //map rejects duplicate keys
                  Map<int,String> student  = {1:"rajat",2:"anil",3:"vinay",3:"vinay"};
                  print(student);
                  student[3] = 'trupti';//update
                  print(student);

                  //search : key
                  print(student.containsKey(2));//true

                  //length
                  print(student.length);//3

                  //list of values
                  print(student.values);//runtimetype : _CompactIterable<String>
                  //student.values.forEach((f) => print(f));

                  //iterable keys
                  print(student.keys);

                  //display view of map  
                  print(student.cast());//{1: rajat, 2: anil, 3: trupti}

                  //search value
                  print(student.containsValue("anil"));//true

                  //removed
                  student.remove(2);
                  print(student.cast());//anil removed

                  //add new entry
                  student[5] = "kumar";//easy update
                  print(student.cast());
                  student.update(5,(String val) => "Mr." +val );
                  print(student);
                  //or replace old value
                  student.update(5,(String val) => "Mr.krishna kumar" );
                  print(student.cast());


                  //add : can be added single or multiple pairs
                  student.addAll({100:"vishnu"});
                  student.addAll({101:"ranjit",102:"gopal"});
                  print(student);


                  //iterate
                  student.entries.forEach((f) => print(f));

                  //filter : removes from original map
                  student.removeWhere((k,v) => k%2 == 0);
                  print(student);

                  //map : functional
                  student.map((k,v) => map_student(k,v)).forEach((k,v) => print(v));



              }

              MapEntry<int,String> map_student(var k,var v){
                  return new MapEntry(k, "hi : "+v);

              }
