
# Vectors
 Vectors are the same as dynamic arrays with the ability to resize themselves automatically when an element is inserted or deleted, with their storage being handled automatically by the container. 

 It is defined inside the <vector> header file.

### Syntax to declare vector in c++

 `std::vector<dataType> vectorName;`
 where the data type is the type of data of each element of the vector. You can remove the std:: if you have already used the std namespace.





## Iterators in Vectors:
 1. begin()– Returns an iterator pointing to the first element in the vector.  

2. end()– Returns an iterator pointing to the theoretical element that follows the last element in the vector.

 3. rbegin()– Returns a reverse iterator pointing to the last    element in the vector (reverse beginning). It moves from last to first element.

 4. rend()– Returns a reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end).

 5. cbegin()– Returns a constant iterator pointing to the first element in the vector.

 6. cend()– Returns a constant iterator pointing to the theoretical element that follows the last element in the vector.

 7. crbegin()– Returns a constant reverse iterator pointing to the last element in the vector (reverse beginning). It moves from last to first element.

 8. crend()– Returns a constant reverse iterator pointing to the theoretical element preceding the first element in the vector (considered as reverse end).

 ## Member Functions in Vectors in C++

1. push_back(): Adds an element in the vector at the last.

Syntax:  
`vt.push_back(element)`
element will be added to the vector vt.

2. pop_back():  Removes the last element from the vector.

Syntax:  
```
vt[] ={1,2,3,4,5};
int x = vt.pop_back();
```
x will contain 5.

3. size() :     Returns the number of elements in the vector. 

Syntax:  
```
vt[] = {1,2,3,4,5}
int len = vt.size();
```
len will contain size of vector = 5.

4. resize():    Changes the size of the vector.

5. capacity() : Returns the size of the storage space currently allocated to the vector.

6. empty() :   Checks if the vector is empty.

7. front() :  Accesses the first element of the vector.

8. back() :   Accesses the last element of the vector. 

## 2D vector in C++

A 2D vector is a vector of vector. Like 2D arrays , we can declare and assign values to a 2D vector.

Syntax to define a 2D vector: 
`vector<vector<int>>vt;`

Code implementation to assign values in c++: 

```
for(int i= 0;i<n;i++){
    for(int j = 0;j<n;j++){
        cin>>vt[i][j];
    }
}
```
In a 2D vector , every element is a vector.

## Advantage of Vector over Array

1.  Vector is template class and is C++ only construct whereas arrays are built-in language construct and present in both C and C++.

2.  Vector are implemented as dynamic arrays with list interface whereas arrays can be implemented as statically or dynamically with primitive data type interface.