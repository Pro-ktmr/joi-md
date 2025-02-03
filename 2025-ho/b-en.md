Score: $100$ points

### Problem Statement

Bitaro, the brave hero, has set out on an adventure to defeat monsters.

Bitaro has a strength value, denoted as $x$, which starts at an initial value. There are $N$ monsters, each labeled with a number from $1$ to $N$. To defeat the $i$-th monster ($1 \leq i \leq N$), Bitaro must have a strength of at least $A_i$. Defeating the $i$-th monster increases Bitaro's strength by $B_i$.

Bitaro wants to defeat all the monsters using the following strategy:
<ol>
<li> Start with a specific monster $j$ ($1 \leq j \leq N$) and defeat the monsters in order: $j, j + 1, \ldots, N$.
<li> If $j \geq 2$, go back and defeat the monsters $1, 2, \ldots, j-1$ in sequence.
</ol>

Given the information about the monsters, write a program to determine the minimum initial strength $x$ required for Bitaro to defeat all the monsters.

---

### Input

Read the following data from the standard input.

~~~
$N$
$A_1$ $A_2$ $\dots$ $A_N$
$B_1$ $B_2$ $\dots$ $B_N$
~~~

### Output

Output a single integer, the minimum initial strength $x$ required for Bitaro to defeat all the monsters.

---

### Constraints

<ul>
<li> $2 \leq N \leq 500\,000$.
<li> $0 \leq A_i \leq 10^9$ ($1 \leq i \leq N$).
<li> $0 \leq B_i \leq 10^9$ ($1 \leq i \leq N$).
<li> Given values are all integers.

</ul>

### Subtasks

<ol>
<li> ($10$ points) $N \leq 2\,000$, and the minimum initial strength $x$ is $10$ or less.
<li> ($21$ points) $N \leq 2\,000$.
<li> ($19$ points) The minimum initial strength $x$ is $10$ or less.
<li> ($22$ points) $B_i = 1$ ($1 \leq i \leq N$).
<li> ($28$ points) No additional constraints.
</ol>

---

### Sample Input 1

~~~
5
1 3 2 8 6
4 3 1 1 2
~~~

### Sample Output 1

~~~
1
~~~

<ul>
<li> Start with an initial strength of $1$.
<li> Defeat monsters in the following order:
<ol>
<li> Defeat monster $1$. Strength increases by $4$ to $5$.
<li> Defeat monster $2$. Strength increases by $3$ to $8$.
<li> Defeat monster $3$. Strength increases by $1$ to $9$.
<li> Defeat monster $4$. Strength increases by $1$ to $10$.
<li> Defeat monster $5$. Strength increases by $2$ to $12$.
</ol>
</ul>

This sample input satisfies the constraints of Subtasks $1,2,3$ and $5$.

---

### Sample Input 2

~~~
5
1 6 3 3 2
1 2 1 0 1
~~~

### Sample Output 2

~~~
3
~~~

<ul>
<li> Start with an initial strength of $3$.
<li> Defeat monsters in the following order:
<ol>
<li> Defeat monster $3$. Strength increases by $1$ to $4$.
<li> Defeat monster $4$. Strength increases by $0$ to $4$.
<li> Defeat monster $5$. Strength increases by $1$ to $5$.
<li> Defeat monster $1$. Strength increases by $1$ to $6$.
<li> Defeat monster $2$. Strength increases by $2$ to $8$.
</ol>
</ul>

This sample input satisfies the constraints of Subtasks $1,2,3$ and $5$.

---

### Sample Input 3

~~~
10
11 9 8 12 7 7 8 12 9 10
1 1 1 1 1 1 1 1 1 1
~~~

### Sample Output 3

~~~
9
~~~

This sample input satisfies the constraints of all the subtasks.

---

### Sample Input 4

~~~
7
1125 638 0 37 737 820 1202
23 984 558 350 52 345 580
~~~

### Sample Output 4

~~~
0
~~~

This sample input satisfies the constraints of Subtasks $1,2,3$ and $5$.


