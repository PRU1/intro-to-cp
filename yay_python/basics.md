# Getting started

We are assuming you know the basics of your chosen programming language. The easiest way to practice problems is through [DMOJ](dmoj.ca). On DMOJ you'll find a bunch of programming questions. You can copy/paste your code into DMOJ, and it will grade it.

Let's learn how DMOJ works with a CCC problem. 

## CCC J1 2023
Every year there are 5 junior and senior problems. Junior and Senior problems are labelled as *J <question #>* and *S <question #>* respectively. So J1 is the first problem in the Junior section of CCC.

---

In the game, Deliv-e-droid, a robot droid has to deliver packages while avoiding obstacles. At the end of the game, the final score is calculated based on the following point system:
- Gain points for every package delivered.
- Lose points for every collision with an obstacle.
- Earn a bonus points if the number of packages delivered is greater than the number of collisions with obstacles.

Your job is to determine the final score at the end of a game.

### Input Specification

The input will consist of two lines. The first line will contain a non-negative integer $P$, representing the number of packages delivered. The second line will contain a non-negative integer $C$, representing the number of collisions with obstacles.

### Output Specification

The output will consist of a single integer, $F$, representing the final score.

### Sample Input 1
```
5
2
```
### Sample Output 1
```
730
```
### Explanation for Sample 1
There are $5$ packages delivered, so $5 \times 50 = 250$
 points are gained. There are $2$ 
 collisions, so $2 \times 10 = 20$
 points are lost. Since $5 > 2$
, a bonus $500$ 
 points are earned. Therefore, the final score is $250 - 20 + 500$
.

*** [Link to Problem](https://dmoj.ca/problem/ccc23j1) *** 

Try coding a solution to this problem. Once you're done, continue reading.

## Submitting Your Solution

We submit a solution to DMOJ so it can be graded.

By "graded", we mean it runs your code and gives it a bunch of inputs. If you code gives a correct output, the grader displays a message, summarized in the table below.

| Message | Meaning |
| --- | ----------- |
| **<span style="color:Green"> AC </span>** | Accepted |
| **<span style="color:Red">WA</span>** | Wrong Answer |
| **<span style="color:Grey">TLE</span>** | Time Limit Exceeded |

If the coder shows **<span style="color:Grey">TLE</span>** it means your program is too slow (there is a compilation time limit!)


To submit the solution to DMOJ, click "Submit Solution" on the right side of the screen. You will need to have opened a DMOJ account to submit a solution.

TODO: add solutions??
