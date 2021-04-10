### Custom Comparators
 
 with the built in sort function we can add custom comparator function to change the order of sorting
 With the help of custom comparators we can sort in descending order or even go deeper in a data structure
 
 It comes in handy when we are trying to sort sttuct based on some internal value of a struct
 
 example
 ```
 bool comp(int a, int b){
    return a>b;
}

int main()
{
   int arr[] = {1,2,3,4,5,6,7,8};
   int n = sizeof(arr)/sizeof(arr[0]);
   sort(arr, arr+n, comp);
   
   for(auto& x: arr){
       cout<<x<<" ";
   }
   return 0;
}

OUTPUT
8 7 6 5 4 3 2 1
 
 ```
 
 
 ```
 struct Interval {
    int start, end;
};
  
// Compares two intervals 
// according to staring times.
bool compareInterval(Interval i1, Interval i2)
{
    return (i1.start < i2.start);
}
  
int main()
{
    Interval arr[]
        = { { 6, 8 }, { 1, 9 }, { 2, 4 }, { 4, 7 } };
    int n = sizeof(arr) / sizeof(arr[0]);
  
    // sort the intervals in increasing order of
    // start time
    sort(arr, arr + n, compareInterval);
  
    cout << "Intervals sorted by start time : \n";
    for (int i = 0; i < n; i++)
        cout << "[" << arr[i].start << "," << arr[i].end
             << "] ";
  
    return 0;
}

OUTPUT 
[1,9] [2,4] [4,7] [6,8]
 ```
