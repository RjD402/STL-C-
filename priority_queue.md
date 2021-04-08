### Info
A STL method to implement heap data structure

By default a priority queue is a max heap - that means pq.top() will give the maximum element present in the heap.
```
priority_queue<int> pq;
```

To crate a min heap - use the following syntax

```
priority_queue<int, vector<int>, greater<int>> pq;
```

### size()
pq.size() - gives the number of elements present in the priority queue

### top()

pq.top() - gives the element present at the top, in case of max heap its the maximum element and vice versa for min heap

### pop()

pq.pop() - removes the top element from the heap

### push()

pq.push() - used to put in elements in a heap . eg:

```
     priority_queue<int, vector<int>,  
                       greater<int> > gquiz;
    gquiz.push(10);
    gquiz.push(30);
    gquiz.push(20);
    gquiz.push(5);
    gquiz.push(1);

    cout << "\ngquiz.size() : " << gquiz.size();
    cout << "\ngquiz.top() : " << gquiz.top();

    OUTPUT
    gquiz.size() : 5
    gquiz.top() : 1
```

### empty()

To check if a priority is empty or not

### priority queue of pair

```
  //creating a min heap of pair. The first part of pair will be frequency
  // In this the priority_queue will be sorted according to the first part of the pair
  priority_queue<pair<int, int>,vector<pair<int, int>>, greater<pair<int, int>>> pq;
```
