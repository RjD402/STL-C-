### substr()
This function takes two values pos and len as an argument and returns a newly constructed string object with its value initialized to a copy of a sub-string of this object. Copying of string start from pos and done till pos+len means [pos, pos+len).

```
    string s1 = "Geeks";
  
    // Copy three characters of s1 (starting 
    // from position 1 and of length 3(i.e [1,4))
    string r = s1.substr(1, 3);
  
    // prints the result
    cout << "String is: " << r;

    OUTPUT
    String is: eek

        string s = "dog:cat";
  
    // Find position of ':' using find()
    int pos = s.find(":");
  
    // Copy substring after pos
    string sub = s.substr(pos + 1);
  
    // prints the result
    cout << "String is: " << sub;

    OUTPUT
    String is : cat
```

### find()
Finds the element in the given range of numbers. Returns an iterator to the first element in the range [first,last) that compares equal to val. If no such element is found, the function returns last.

```
    int ser = 30;
      
    // std::find function call
    it = std::find (vec.begin(), vec.end(), ser);
    if (it != vec.end())
    {
        std::cout << "Element " << ser <<" found at position : " ;
        std::cout << it - vec.begin() << " (counting from zero) \n" ;
    }

    OUTPUT
    Original vector : 10 20 30 40
Element 30 found at position : 2 (counting from zero)
```

### stringstream



### vector

#### rbegin() and rend()
rbegin() – Returns a reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element
rend() – Returns a reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end)

```
for a vector {1,2,3,4,5}
 for (auto ir = g1.rbegin(); ir != g1.rend(); ++ir)
        cout << *ir << " ";

OUTPUT
5 4 3 2 1
```

#### resize()
vectorname.resize(int n)

1.If the given value of n is less than the size at present then extra elements are demolished.

2.If n is more than current size of container then upcoming elements are appended at the end of the vector. - The appended elements have a default value of 0 each. If you want new elements to have another default value write vectorname.resize(int n, int val) and all the new elements will have val default value

#### insert()
[insert](https://www.geeksforgeeks.org/vector-insert-function-in-c-stl/)

#### clear()
clear() function is used to remove all the elements of the vector container, thus making it size 0. 

Time complexity of clear is O(N)

vectorname.clear()

```
    vector<int> nums = {1,2,3};
    cout<<nums.size()<<endl;
    nums.clear();
    cout<<nums.size()<<endl;

    OUTPUT:
    3
    0
```
#### erase()

Can be used to erase an element at an iterator position as well as delete elements between two iterators


```
    vector<int> myvector{ 1, 2, 3, 4, 5 };
    vector<int>::iterator it;
 
    it = myvector.begin();
    myvector.erase(it);

    OUTPUT
    2 3 4 5

    vector<int> myvector{ 1, 2, 3, 4, 5 };
    vector<int>::iterator it1, it2;
 
    it1 = myvector.begin();
    it2 = myvector.end();
    it2--;
    it2--;
 
    myvector.erase(it1, it2);
    
    OUTPUT
    4 5
```
