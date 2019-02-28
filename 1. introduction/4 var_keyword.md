#### type inference

        void main(){
              var i = 1;
              var j = 4.5;
              var w = "hello";
              var b = true;
              var n = null;
              var l = [];
              var m = {};
              print(i.runtimeType);
              print(j.runtimeType);
              print(w.runtimeType);
              print(b.runtimeType);
              print(n.runtimeType);
              print(l.runtimeType);
              print(m.runtimeType);
        }

        int
        double
        String
        bool
        Null
        List<dynamic>
        _InternalLinkedHashMap<dynamic, dynamic>
        
#### dart is typed 


     dart is typed, datatype of variable cannot be changed

        var i = 1;
        i = true;   //error : type of i is fixed
