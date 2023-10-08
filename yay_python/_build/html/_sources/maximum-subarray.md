# Maximum Subarray Sum Problem
*practising finding the O(n) solution*

Say you have an array of $n$ elements.

```
    int arr[] = {-1,3,-2,5,3,-5,2,2}

```

Your goal is to find the subarray with the maximum sum.

`````{admonition} What's a subarray
:class: tip
A subarray is a **contiguous** part of your original array. Contiguous means a subarray consists of elements that are side-by-side.

so if `arr[] = {1,2,-4,3}`, then `{1,2,-4}` and `{-4}` are examples of subarrays but `{1,2,3}` is NOT. 
`````

One way to approach this problem is to find the sum of all possible subarrays. Then, store the maximum subarray sum. This is called a **brute force** solution, since we find all possible subarrays.

## The brute force solution: O($n^2$)
A systematic way of finding all subarrays is to find all subarrays starting at each index of the array. So, for

```
    int arr[] = {-1,3,-2,5,3,-5,2,2}

```

Have a variable, `index` to keep track of what array index you start listing subarrays from. When `index = 0`, you form these subarrays. 
```
{-1}
{-1,3}
{-1,3,-2}
{-1,3,-2,5}
{-1,3,-2,5,3}
{-1,3,-2,5,3,-5}
{-1,3,-2,5,3,-5,2}
{-1,3,-2,5,3,-5,2,2}

```
Then, increment `index`. At `index = 1`, you form the following subarrays:
```
{3}
{3,-2}
{3,-2,5}
{3,-2,5,3}
{3,-2,5,3,-5}
{3,-2,5,3,-5,2}
{3,-2,5,3,-5,2,2}
```

Continue incrementing `index` until `index = n-1` (in our case, `index = 8-1`).
```
{2}
``` 

Keep a variable `max_sum` that you update for each subarray sum you calculate. 
Try coding out an O($n^2$) solution! Double check your solution with solution provided below:
```
// This is a C++ solution

#include <iostream>
#include <vector>
using namespace std;

int main()
{
    vector<int> arr = {-1,3,-2,5,3,-5,2,2};
    int n = 8; // size of input
    int maxSum = 0;
    
    // brute force solution
    // O(n^2) time
    
    for (int index = 0; index < n; ++index) { // starting index
        int currentSum = 0;
        for (int j = index; j < n; ++j) {
            currentSum += arr[j];
            maxSum = max(maxSum, currentSum); // keep track of largest subarray sum
        }
        
    }
    cout << maxSum;
    return 0;
}
```
The solution is O($n^2$) since we have a nested loop.

`````{warning}

 **A reminder about time complexity**

Starting at index 0, there are $n$ subarrays. Starting at index 1, there are $n-1$ subarrays. And at index $n-1, there's only one 1 subarray.

The number of steps to find all subarrays is $n + (n-1) + (n-2) + ... + 1$.
Hence,
$n + (n-1) + (n-2) + ... + 1 = \frac{n(n-1)}{2} = \frac{(n^2-n)}{2}$
it takes $(n^2-n)/2$ steps to find all subarrays. BUT, the time complexity is still $O(n^2)$ since we only consider the biggest factor (which is $n^2$) in time complexity.
`````


+++

NOT DONE PART

+++

- brute force solution
- O(n^2)
- how many arrays possible starting at each index
- takes n*(n-1)/2 steps, which has time complexity O(n^2) (because we ignore small factors)
- this solution is slow if we had time limit on grader
- give example of CSES problem set

- we need a better solution
- we can solve this in O(n)
- iterate through the array
- store the maximum subarray sum that ends at each index
- called Kadane's algorithm?????

## The O(n) solution

