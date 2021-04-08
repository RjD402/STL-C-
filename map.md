## Time Complexity
A lookup in map is O(logn)

Insertion is O(logn)

If you are inserting n items(inserting an array into a map) then time complexity will be O(nlogn). For example in the below code snippet will have O(nlogn)
```
void add(int N, std::map<int, int>& map) {
  for (int i = 0; i < N; ++i) {
    map[i] = i;
  }
}
```

## Info

In a map Each element has a key value and a mapped value. No two mapped values can have same key values.

The keys in a map are arranged and saved in a sorted order. 
If you want the keys to be unsorted use **unordered_map**

Inserting values in a map
```
int main()
{

   map<int,int> m;
   m.insert({1,2});
   m.insert({3,4});
   
   //another method of putting in a map
    m.insert(pair<int, int>(1, 40));
    m.insert(pair<int, int>(2, 30));

    //method 1
    for(auto& x: m){
        cout<<x.first<<" "<<x.second<<endl;
    }
    cout<<endl;

   
   
   //method 2
   for(auto it = m.begin();it!=m.end(); it++){
       cout<<it->first<<" "<<it->second<<endl;
   }
   
   return 0;
}

output
1 2
2 30
3 4

1 2
2 30
3 4

```

### find
find(key) is a built-in function in C++ STL which returns an iterator or a constant iterator that refers to the position where the key is present in the map. If the key is not present in the map container, it returns an iterator or a constant iterator which refers to map.end().

The time complexity for find is O(logn) as it is a balanced tree (based on red black tree)

```
{

	// Initialize container
	map<int, int> mp;

	// Insert elements in random order
	mp.insert({ 2, 30 });
	mp.insert({ 1, 40 });
	mp.insert({ 3, 20 });
	mp.insert({ 4, 50 });

	cout << "Elements from position of 3 in the map are : \n";
	cout << "KEY\tELEMENT\n";

	// find() function finds the position
	// at which 3 is present
	for (auto itr = mp.find(3); itr != mp.end(); itr++) {
	
		cout << itr->first << '\t' << itr->second << '\n';
	}

	return 0;
}


OUTPUT

The elements from position 3 in map are : 
KEY    ELEMENT
3    20
4    50

```

### erase
Can be used to remove a key and its value from a map

```
    mp.insert({ 2, 30 });
    mp.insert({ 1, 40 });
    mp.insert({ 3, 60 });
    mp.insert({ 5, 50 });
 
    // function to erase given keys
    mp.erase(1);
    mp.erase(2);

    OUTPUT
     3 60
     5 50

```

Can also be used to remove a key using an iterator which points to the key

```
// C++ program to illustrate
// map::erase(iteratorposition)
#include <bits/stdc++.h>
using namespace std;

int main()
{

	// initialize container
	map<int, int> mp;
	// insert elements in random order
	mp.insert({ 2, 30 });
	mp.insert({ 1, 40 });
	mp.insert({ 3, 60 });
	mp.insert({ 5, 50 });


	// function to erase given position
	auto it = mp.find(2);
	mp.erase(it);

	auto it1 = mp.find(5);
	mp.erase(it1);

	
	for (auto itr = mp.begin(); itr != mp.end(); ++itr) {
		cout << itr->first
			<< '\t' << itr->second << '\n';
	}
	return 0;
}

OUTPUT 
1 40
3 60

```

Can also be used to remove keys between two iterators. 
The first iterator key is removed and for the second iterator upto that is removed.

```
    map<int, int> mp;
    // insert elements in random order
    mp.insert({ 2, 30 });
    mp.insert({ 1, 40 });
    mp.insert({ 3, 60 });
    mp.insert({ 2, 20 });
    mp.insert({ 5, 50 });
 
 
    // function to erase in a given range
    // find() returns the iterator reference to
    // the position where the element is
    auto it1 = mp.find(2);
    auto it2 = mp.find(5);
    mp.erase(it1, it2);
 

    for (auto itr = mp.begin(); itr != mp.end(); ++itr) {
        cout << itr->first
             << '\t' << itr->second << '\n';
    }
    return 0;
}

OUTPUT
1 40 
5 50

```

### count
The map::count() is a built-in function in C++ STL which returns 1 if the element with key K is present in the map container. It returns 0 if the element with key K is not present in the container.

```
    
	// initialize container
	map<int, int> mp;

	// insert elements in random order
	mp.insert({ 2, 30 });
	mp.insert({ 1, 40 });
	mp.insert({ 3, 60 });
	mp.insert({ 4, 20 });
	mp.insert({ 5, 50 });

	// checks if key 1 is present or not
	if (mp.count(1))
		cout << "The key 1 is present\n";
	else
		cout << "The key 1 is not present\n";

	// checks if key 100 is present or not
	if (mp.count(100))
		cout << "The key 100 is present\n";
	else
		cout << "The key 100 is not present\n";

	return 0;
}

OUTPUT

The key 1 is present
The key 100 is not present
```
