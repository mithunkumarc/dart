#### LIST also knows as arrays

              void main(){
              //lists are mutable
              //use const keyword to make list immutable
              List<int> list = [1,2,3];
              var vlist = [1,2,3]; //equavalent to List<int>
              final flist = [1,2,3];//flist cannot point to any other list
              const clist = [1,2,3];//immutable list, closed for changes
              dynamic dlist = [1,2,3];//if you want a dynamic var point to list

              print([1].single);//returns single element if iterable/list has one element else error
              print(list.length);//size

              //index base
              print(list[1]);//output : 2

              //sublist : slicing in python
              //difference : first element not selected so first position must be start - 1
              //by default : end will be assumed as last element
              //mandatory input is start point ,which must be startposition - 1 
              print(list.sublist(1));//creates sublist : output : [2,3]

              //asMap : list to map , elements/values gets position as keys
              print(list.asMap());

              //iterate using foreach elements
              list.forEach((f) => print(f));


              //iterate using iterator
              print("*" * 30);
              Iterator<int> ilist = list.iterator;
              while(ilist.moveNext()){
                print(ilist.current);
              }

              //joins all elements using seperator
              print(list.join("*"));//1*2*3

              //prints last element
              print(list.last);
              //prints first element
              print(list.first);


              //print elements using for loop
              for(var n in list){
                print(n * n);
              }

              //skips frist three elements
              print([1,2,3,4,5,6,7,8].skip(3));

              //takes first three elements 
              print([1,2,3,4,5,6,7,8].take(3));


              //take as long as condition satisfies
              print([1,2,3,4,5,6,7,8].takeWhile((n) => n < 5));//output : (1, 2, 3, 4)


              //map : support functional prog
              //filter : use foreach
              print([1,2,3,4,5,6,7,8].map((f) => f*f));


              //reduce
              print([1,2,3,4,5,6,7,8].reduce((x,y) => x+y));


              //search
              print([1,2,3,4,5,6,7,8].contains(7));//true
              print([1,2,3,4,5,6,7,8].contains(77));//false


              var remlist = [1,2,3,4,5,6,7,8]; 
              remlist.remove(2);
              print(remlist);//removed 2

              remlist.removeLast();//removed 8
              print(remlist);


              remlist.removeAt(0);//removed base on position
              print(remlist);//removed 1



              //clear
              list.insert(0, 111);
              print(list);//adds 111 at position 0

              //set range : replacing elements
              var srl = [1,2,3,4,5,6];
              srl.setRange(2, 5, [87,77,67]);
              print(srl);

              //remove range




              }





              1
              3
              2
              [2, 3]
              {0: 1, 1: 2, 2: 3}
              1
              2
              3
              ******************************
              1
              2
              3
              1*2*3
              3
              1
              1
              4
              9
              (4, 5, 6, 7, 8)
              (1, 2, 3)
              (1, 2, 3, 4)
              (1, 4, 9, 16, 25, 36, 49, 64)
              36
              true
              false
              [1, 3, 4, 5, 6, 7, 8]
              [1, 3, 4, 5, 6, 7]
              [3, 4, 5, 6, 7]
              [111, 1, 2, 3]
              [1, 2, 87, 77, 67, 6]
              
              
#### lists are mutable but can be made immutable using const

          const list = [1,2,3] // immutable


        //lists are mutable
          var a = [1,2,3];
          print(a.hashCode);
          a.add(4);
          print(a.hashCode);
          print(a);

        const list : immutable
