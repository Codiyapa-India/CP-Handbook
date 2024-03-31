
## Introduction to Queues:

A queue is a linear data structure that follows the FIFO (First In First Out) principle. This means that the element which is inserted ﬁrst will be the one to be removed ﬁrst. Think of it like a queue of people waiting for a bus to go to a particular destination, where the person who arrived ﬁrst gets on the bus ﬁrst and the person
who enters at last will exit ﬁrst.



## Properties of Queue:

->FIFO (First In First Out): The element that is added ﬁrst is the one that gets removed ﬁrst.

-> Linear Data Structure: Queue elements are arranged in a linear sequence.

-> Two Ends: A queue has two ends, namely the front and the rear.

-> Elements are added to the rear end and removed from the front end.

-> Dynamic Size: Queues can be of ﬁxed size or dynamic size, depending on the implementation.Types of Queues:

1. Simple Queue: A basic queue where elements are inserted at the rear end and removed from the front end.

2. Circular Queue: A queue where the rear end is connected to the front end, forming a circle. This allows for eﬃcient space utilization in a ﬁxed-size queue.

3. Priority Queue: A queue where elements have associated priorities, and the element with the highest priority is dequeued ﬁrst.

4. Double Ended Queue (Deque): A queue that supports insertion and deletion at both ends.
## Implementation:


**Queue Implementation using STL:**

*In software terms, the queue can be viewed as a set or collection of *elements as shown below. The elements are arranged linearly.**

![Queue](https://media.geeksforgeeks.org/wp-content/uploads/20220805131014/fifo.png)

**We have two ends i.e. “front” and “rear” of the queue. When the queue is empty, then both the pointers are set to -1.**

**The “rear” end pointer is the place from where the elements are inserted in the queue. The operation of adding /inserting elements in the queue is called “enqueue”.**

**The “front” end pointer is the place from where the elements are removed from the queue. The operation to remove/delete elements from the queue is called “dequeue”.**

**When the rear pointer value is size-1, then we say that the queue is full. When the front is null, then the queue is empty.**

Here is the Queue Implementation in STL ,C++
```
// CPP code to illustrate Queue in 
// Standard Template Library (STL)
#include <iostream>
#include <queue>

using namespace std;

// Print the queue
void showq(queue<int> gq)
{
	queue<int> g = gq;
	while (!g.empty()) {
		cout << '\t' << g.front();
		g.pop();
	}
	cout << '\n';
}

// Driver Code
int main()
{
	queue<int> gquiz;
	gquiz.push(10);
	gquiz.push(20);
	gquiz.push(30);

	cout << "The queue gquiz is : ";
	showq(gquiz);

	cout << "\ngquiz.size() : " << gquiz.size();
	cout << "\ngquiz.front() : " << gquiz.front();
	cout << "\ngquiz.back() : " << gquiz.back();

	cout << "\ngquiz.pop() : ";
	gquiz.pop();
	showq(gquiz);

	return 0;
}

```

#### The output will be:
```
The queue gquiz is :     10    20    30

gquiz.size() : 3
gquiz.front() : 10
gquiz.back() : 30
gquiz.pop() :     20    30
```

### Methods of Queues: 

1. queue::empty() -> Returns whether the queue is empty. It return true if the queue is empty otherwise returns false.

2. queue::size() ->	Returns the size of the queue.

3. queue::swap() -> Exchange the contents of two queues but the queues must be of the same data type, although sizes may differ.

4. queue::emplace() -> Insert a new element into the queue container, the new element is added to the end of the queue.

5. queue::front() -> Returns a reference to the first element of the queue.

6. queue::back() -> Returns a reference to the last element of the queue.

7. queue::push(g) -> Adds the element ‘g’ at the end of the queue.

8. queue::pop() -> Deletes the first element of the queue.

Here's the C++ code to demostrate the working of the some more functions/methods: 

```
// CPP code to illustrate Queue operations in STL
// Divyansh Mishra --> divyanshmishra101010
#include <iostream>
#include <queue>

using namespace std;

// Print the queue
void print_queue(queue<int> q)
{
	queue<int> temp = q;
	while (!temp.empty()) {
		cout << temp.front()<<" ";
		temp.pop();
	}
	cout << '\n';
}

// Driver Code
int main()
{
	queue<int> q1;
	q1.push(1);
	q1.push(2);
	q1.push(3);

	cout << "The first queue is : ";
	print_queue(q1);

	queue<int> q2;
	q2.push(4);
	q2.push(5);
	q2.push(6);

	cout << "The second queue is : ";
	print_queue(q2);


	q1.swap(q2);
	
	cout << "After swapping, the first queue is : ";
	print_queue(q1);
	cout << "After swapping the second queue is : ";
	print_queue(q2);

	cout<<q1.empty(); //returns false since q1 is not empty

	return 0;
}

```
**Additional resources:**

**1. [Queue**](https://leetcode.com/tag/queue/)[** ](https://leetcode.com/tag/queue/)[-**](https://leetcode.com/tag/queue/)[** ](https://leetcode.com/tag/queue/)[LeetCode**](https://leetcode.com/tag/queue/)**

**2.[Queue**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[Data**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[Structure**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[-**](https://www.geeksforgeeks.org/queue-data-structure/)[** ](https://www.geeksforgeeks.org/queue-data-structure/)[GeeksforGeeks**](https://www.geeksforgeeks.org/queue-data-structure/)**

**3.[Queue**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Data**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Structure**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[-**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[** ](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)[Tutorialspoint**](https://www.tutorialspoint.com/data_structures_algorithms/dsa_queue.htm)**

**4.[Queues**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[-**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Solve**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Data**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[Structures**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[|**](https://www.hackerrank.com/domains/data-structures/queues)[** ](https://www.hackerrank.com/domains/data-structures/queues)[HackerRank**](https://www.hackerrank.com/domains/data-structures/queues)**

**Practice problems as much as possible in order to**

**get a good command on queue from above**

**mentioned resources….**

**Happy coding…**

