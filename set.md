### set

Sets are a type of associative containers in which each element has to be unique because the value of the element identifies it. The value of the element cannot be modified once it is added to the set, though it is possible to remove and add the modified value of that element.   

The elements of the set are sorted in increasing order by default

```
   set<int> s;
   for(int i=5;i>=0;i--){
       s.insert(i);
   }
   //only one 2 and 4 are inserted since values in set are unique
   s.insert(4);
   s.insert(2);
   
   //values are stored in increasing order
   for(auto& x: s){
       cout<<x<<" ";
   }
   cout<<endl;
   
   OUTPUT
   0 1 2 3 4 5
```
