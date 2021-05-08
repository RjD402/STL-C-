### set

The time complexity for inserting an item in a set is O(logn)

Sets are a type of associative containers in which each element has to be unique because the value of the element identifies it. The value of the element cannot be modified once it is added to the set, though it is possible to remove and add the modified value of that element.   

The elements of the set are sorted in increasing order by default

The time complexity for set count is O(logn)

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

### unordered_set

Time complexity for inserting an item in a set is O(1). 
Time complexity for checking if unordered_set contians a value is O(1). Unordered_set.contains
