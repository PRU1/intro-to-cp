# Math tips
**You probably don't need this**. In my experience, I have never used these tips that I picked up from a book competitive programming. Nevertheless, in the slim chance these are helpful, or if you just like math, here's some math : D.

## Arithmetic series

An arithmetic series is when the difference between any 2 consecutive terms is the same. For example, $\{1,2,3,4,5,6,7\}$ and  $\{-5, -3, -1, 1, 3, 5, 7 … \}$  are arithmetic series because they have a common difference between terms. 

<aside>
💡 $S_n$  represents the sum of a series with $n$ terms
$a$ represents the first term in a series
$d$ represents the common difference in an arithmetic series
$r$ represents the ratio between any two terms in a geometric series
$t_n$ represents $n^{th}$ term in a series

</aside>

> Sum of arithmetic series: $S_n = \frac{n}{2} \cdot (a + a + (n-1)(d))$ or $S_n=\frac{n}{2} \cdot (t_1+t_n)$
> 

> $t_n = a + (n-1)(d)$
> 

If you need to find the sum numbers like 1+2+3+4+5…., don’t use a `for` loop. Apply the formula or alternatively use the formula $\displaystyle\sum_{t=0}^{n}1+2+3+ ... +n = \frac{1}{2}\cdot (n)(n+1)$

```cpp
// Don't do this:
int sum{}; int n = 100;
for (int i = 0; i < n; ++i){
sum += i;
}
// Do this, it's faster
int sum{}; int n = 100;
sum = n*(n+1)/2
```

## Geometric series

To get the next term, you multiply by the same number each time. A geometric series is when the ratio between two consecutive terms is the same.

> Sum of a geometric series: $\displaystyle \frac{a(r^n-1)}{r-1}$
> 

> $t_n = ar^{(n-1)}$
> 

## Set theory

A set is a collection of objects (objects can be numbers, strings, etc.). For example, $X=\{1,2,3,4,5\}$ is an example of a set. Note **sets are unordered and each object is distinct.**  

- [ ]  Add use in competitive programming

### Set operations

- **Intersection** $A \cap B$: The elements two sets have in common. i.e. if $A=\{2,4,6,8\}$ and $B=\{4,8\}$, then $A \cap B = \{4,8\}$
- **Union** $A \cup B$: Combine elements of $A$ and $B$ into one set
- **Complement** $\bar{A}$: Every element NOT in $A$. Depends on a *universal set*, which tells every possible element that could be in a set. So if a universal set was $\{1,2,3,4,5,6,7,8,9,10\}$ and $A = \{1,2,3\}$, then $\bar{A}=\{4,5,6,7,8,9,10\}$
- **Difference** $A \setminus B$**:** Every element in $A$ but not in $B$, like $A$ minus $B$. See this [website](https://www.math-only-math.com/difference-of-sets-using-Venn-diagram.html):

 


### Set notation

|  Symbol | Meaning |
| --- | --- |
| $\mid A \mid$ | The size of a set (the number of elements). Also called cardinality |
| $A \subset B$ | $A$ is a subset of $B$: each element of A is also in B |
| $\emptyset$ | Means set is empty |
| $4 \in \mathbb{R}$  |  4 is in the real number set |
| $4 \notin \mathbb{R}$ | 4 is NOT in the real number set |
| $\mathfrak{P}(A)$ or $P(A)$ |  Refers to all subsets of a set (in this case, a set called $A$). There are $2^{|A|}$ subsets if you include the original set and an empty set as a subset |