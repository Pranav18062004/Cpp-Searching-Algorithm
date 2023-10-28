# Searching Algorithms: Linear Search and Binary Search

Searching for specific elements within a collection of data is a common task in computer science. Two fundamental searching algorithms are often used: **Linear Search** and **Binary Search**. In this README, we'll explain what these algorithms are and how to implement them in C++.

## Linear Search

**Linear Search** is a straightforward searching algorithm that checks each element in a collection one by one until the target element is found. Here's a brief overview of how to perform a Linear Search in C++:

1. **Loop Through the Data**: Start at the beginning of the data collection and move through it one element at a time, checking each element.

2. **Compare Each Element**: At each step, compare the current element with the target element you're searching for.

3. **Element Found**: If the current element matches the target, the search is successful, and you can return the index of the found element.

4. **Element Not Found**: If the entire collection is traversed without finding the target element, indicate that the element is not present in the collection.

## Binary Search

**Binary Search** is an efficient searching algorithm for sorted data. It repeatedly divides the collection into two halves, eliminating one half in each step until the target element is found. Here's a brief overview of how to perform a Binary Search in C++:

1. **Initialize Pointers**: Set two pointers, one at the beginning (left) and one at the end (right) of the sorted collection.

2. **Find the Middle**: Calculate the middle index between the left and right pointers.

3. **Compare with the Middle Element**: Compare the middle element with the target element.

4. **Adjust Pointers**: Depending on the comparison result, adjust the left or right pointer to focus on the half where the target element might be.

5. **Repeat**: Repeat steps 2-4 until the target element is found or the left pointer is greater than the right pointer, indicating that the element is not in the collection.

## C++ Implementation

In C++, you can implement these searching algorithms as functions. Below are basic code outlines for both Linear Search and Binary Search in C++:

**Linear Search:**

```cpp
int linearSearch(const std::vector<int>& data, int target) {
    for (int i = 0; i < data.size(); i++) {
        if (data[i] == target) {
            return i; // Element found
        }
    }
    return -1; // Element not found
}
