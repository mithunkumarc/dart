
          import 'dart:collection';

          void main(){
            //since dart is a typed language, list/set cant have data more than one datatype 

            //ways to create set
            var s = <int>{1,2,3};
            Set s1 = <String>{};
            Set<int> s2 = {1,2,3};
            dynamic s3 = {33,5,6};//s3 can point to any kind of data/value/object in future
            Set set_obj = new Set();

            //set don't allow duplicates
            var set = {1,1,1,1};
            print(set);

            //by default : set is mutable
            var mut_set = {1,2,3};
            mut_set.add(4);
            print(mut_set);


            //immutable set
            const con_set = {1,3,2};
            //con_set.add(5);//cannot change unmodifialbe set
            //con_set = {4,5,6};//const are by default final


            //final set: can be modified
            final fin_set = <int>{1,2,3};
            //fin_set = {4,5,6};//error
            fin_set.add(7);//ok
            print(fin_set);

            //search : 
            print({1,2,3,4,5}.contains(4));

            //remove
            var rem_set = {1,2,3,4,5};
            rem_set.remove(4);
            print(rem_set);//4 removed

            //retain all : retains only mentioned elements 
            var ret_set = {1,2,3,4,5};
            ret_set.retainAll({3,4});
            print(ret_set);//retained 3,4 removesa all other elements


            //list to set, you ll lose duplicates
            print([1,2,3,4,4,4,5].toSet());

            //add more than one elements 
            var addall_set = <String>{};
            addall_set.addAll({'x','y','z'});
            print(addall_set);

            //isEmpty
            s = {};
            print(s.isEmpty);


            //length
            print({3,4,5}.length);//3

            //first 3 elements 
            print(<int>{3,4,5,7,8,9,10}.take(3));

            //all elements which are less than 8, 2 not selected because it appears after condtion fails
            print(<int>{3,4,5,7,8,9,10,2}.takeWhile((n) => n<8));
            //output : (3,4,5,7)

            //common between two sets
            print(<int>{3,4,5,7,8,9,10}.intersection({6,7,8}));

            //is not empty : 
            print(<int>{3,4,5,7,8,9,10}.isNotEmpty);//true

            //returns single element which matches condtion, if there are more matches ,throws error
            print(<int>{3,4,5,7,8,9,10}.singleWhere((n) => n==5));

            //skip as long as condtion is true, then selects all remaining elements both < 7 or > 7
            print(<int>{3,4,5,7,8,9,10}.skipWhile((n) => n<7));

            //any even numbers ? 
            print(<int>{3,4,5,7,8,9,10,2,1}.any((n) => n%2==0));//true

            //expand inner sets into single set
            var new_set = <Set>{<int>{1,2,4},<int>{1,2,3}}.expand((n) => n).toSet();
            print(new_set);//{1,2,4,3}
            print(new_set.runtimeType);


            //import 'dart:collection'; to use hashset , linkedhashset and splaytreeset

            //unordered
            var hashset = new HashSet<dynamic>();
            hashset.add(1);
            hashset.add('one');
            hashset.add(true);
            hashset.add("hello");
            hashset.add([1,2]);

            print(hashset);

            //ordered
            var linkedhashSet = new LinkedHashSet();
            linkedhashSet.add(1);
            linkedhashSet.add('one');
            linkedhashSet.add(true);
            linkedhashSet.add("hello");
            linkedhashSet.add([1,2]);

            print(linkedhashSet);


            //sorted : use splayTreeSet for sorting
            SplayTreeSet<int> st = new SplayTreeSet();
            st.add(10);
            st.add(9);
            st.add(3);
            st.add(-1);
            print(st);

            // splaytreeset cant take diff data, cannot sort
            SplayTreeSet<dynamic> st_dynamic = new SplayTreeSet();
            // st_dynamic.add(10);
            // st_dynamic.add("hello");
            // st_dynamic.add(true);
            // st_dynamic.add(-1);
            // print(st_dynamic); //error

          }
