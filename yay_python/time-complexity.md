# Introduction to Time Complexity

There's a compilation time limit for each programming question. So, we need to design efficient algorithms. Analysing time complexity let's us decide an efficient algorithm to use in a programming problem. 

In a nutshell, time complexity describes how the time it takes to run your algorithm increases as the input size increases. 

For competitive programming, we focus on **Big O Notation**. Big O Notation tells you the *worst* case performance of your algorithm. 
 ## Big O Notation Rules

 - Written as $O(...)$ where $...$ is a function in terms of $n$. $n$ is the number of inputs. For example, if you're algorithm has time complexity of $O(n^2)$, then for $n$ inputs your algorithm will take $n^2$ steps to complete.  

 - The time complexity for single commands is $O(1)$ 
 
 i.e.
 ```
a++;
b--;
int c = a+b;
b = 5;
// this program runs in O(1) time complexity.
// One way to think of it: there are no inputs so the computation 
// time is always the same when you run this program
 ```
 -  A running a single loop is $O(n)$.
 ```
 for (int i = 0; i < n; ++i) {
    // do something here
 }
 // This loop takes n steps to execute. So its time complexity is O(n)
 ```

 Now suppose our algorithm had nested loops (a loop inside a loop)
 ```
 for (int i = 0; i < n; ++i) {
   for (int j = 0; j < n; ++j) {
    // do something here
   }
 }
 ```

 The outer loop runs $n$ times. And in each iteration of the outer loop, the inner loop runs $n$ times as well. In total, it takes the algorithm $n \times n $ or $n^2$ steps to complete. Hence, the time complexity is $O(n^2)$

:::{note}
 **Big O notation only considers the *biggest* factor**
 Suppose we had a following loop

```
 for (int i = 0; i < n; ++i) {
   for (int j = 0; j < n-1; ++j) {
    // do something here
   }
 }
 ```

 This loop takes $n \times (n-1) = n^2-n$ steps to run. Since $n^2$ gets bigger much faster than $n$ as you increase $n$, we ignore the $n$ term in its time complexity. *The time complexity is still $O(n^2)*$
:::

 Now let's analyse a loop inside a loop inside a loop (triple nested loop).

```
 for (int i = 0; i < n; ++i) {
   for (int j = 0; j < n; ++j) {
      for (int k = 0; k < n; ++k) {
         // do something
      }
   }
 }

 ```

 The outmost loop runs $n$ times. The middle loops $n$ times for each iteration of the outer loop. The innermost loop runs $n$ times for each iteration of the middle loop. Therefore, it takes $n \times n \times n = n^3$ steps to run. So the time complexity is $O(n^3)$.



## Summary 
- Time complexity estimates how long a program will take to execute for some given inputs
- Calculating time complexity is useful to find out whether your program will TLE without having to write the program. It helps you explore the fastest solutions
- “Asymptotic upper bound” is used with Big O notation
means the worst possible performance of your algorithm
- Labelled as $O(…)$, where … is some function




There's a lot more to time complexity that we won't touch here! For more info, check out this [video](https://www.youtube.com/watch?v=D6xkbGLQesk&ab_channel=CSDojo)

