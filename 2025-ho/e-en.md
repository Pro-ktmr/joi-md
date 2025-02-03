Score: $100$ points

### Problem Statement

In the JOI country, there are $N$ post offices, numbered from $1$ to $N$.  
Each post office has an assigned "destination," and the destination of post office $i$ is post office $P_i$. Note that it is possible for $P_i = i$.  
If a package is sent from post office $i$ at time $t$, it will arrive at post office $P_i$ at time $t + 1$. However, a post office cannot send another package while it is in the process of sending a package.  
Each post office can store an unlimited number of packages at any given time.  

Now, $M$ packages need to be delivered in the JOI country.  
The $j$-th package arrives at post office $A_j$ at time $0$, and it must eventually be delivered to the assigned post office $B_j$.  
Given the information about the post offices and the packages, write a program to determine whether it is possible to deliver all the packages to their assigned post offices, and if so, find the smallest possible time at which the last package arrives at its assigned post office.

---

### Input

Read the following data from the standard input.

~~~
$N$
$P_1$ $P_2$ $\cdots$ $P_N$
$M$
$A_1$ $B_1$
$A_2$ $B_2$
$\vdots$
$A_M$ $B_M$
~~~

### Output

Output a single line to the standard output.
If it is possible to deliver all the packages to their assigned post offices, output the smallest possible time at which the last package arrives at its assigned post office.
Otherwise, output <code>-1</code> instead.

---

### Constraints

<ul>
<li> $2 \leqq N \leqq 200 \, 000$.
<li> $1 \leqq M \leqq 200 \, 000$.
<li> $1 \leqq P_i \leqq N$ ($1 \leqq i \leqq N$).
<li> $1 \leqq A_j, B_j \leqq N$ ($1 \leqq j \leqq M$).
<li> $A_j \neq B_j$ ($1 \leqq j \leqq M$).
<li> Given values are all integers.
</ul>

### Subtasks

<ol>
<li> ($3$ points) $N \leqq 3 \, 000$， $M = 1$.
<li> ($9$ points) $N \leqq 3 \, 000$， $M \leqq 3 \,000$.
<li> ($13$ points) $P = (1, 1, 2, \cdots, N-1)$, and $\max(B_1, B_2, \dots, B_M) < \min(A_1, A_2, \dots, A_M)$.
<li> ($25$ points) $P = (1, 1, 2, \cdots, N-1)$.
<li> ($11$ points) $P = (N, 1, 2, \cdots, N-1)$.
<li> ($25$ points) $P_1 = 1$, $P_i < i$ ($2 \leqq i \leqq N$).
<li> ($14$ points) No additional constraints.
</ol>

---

### Sample Input 1

~~~
5
1 1 2 3 4
3
3 2
3 1
3 1
~~~

### Sample Output 1

~~~
3
~~~

For example, by sending the packages in the following way, all the packages can be delivered to their assigned post offices by time $3$:

<ul> <li> At time $0$, packages $1$, $2$, and $3$ are at post office $3$. Send package $2$ to post office $2$. <li> At time $1$, package $2$ is at post office $2$, and packages $1$ and $3$ are at post office $3$. From post office $2$, send package $2$ to post office $1$, and from post office $3$, send package $3$ to post office $2$. <li> At time $2$, package $2$ is at post office $1$, package $3$ is at post office $2$, and package $1$ is at post office $3$. From post office $2$, send package $3$ to post office $1$, and from post office $3$, send package $1$ to post office $2$. <li> At time $3$, packages $2$ and $3$ are at post office $1$, and package $1$ is at post office $2$. At this point, all the packages have reached their destinations. </ul>

Since it is not possible to deliver all the packages to their assigned post offices by time $2$, output $3$.

This sample input satisfies the constraints of Subtasks $2, 3, 4, 6, 7$.

---

### Sample Input 2

~~~
3
2 1 3
1
1 3
~~~

### Sample Output 2

~~~
-1
~~~

No matter how the packages are sent, it is impossible to deliver a package from post office $1$ to post office $3$, so output <code>-1</code>.

This sample input satisfies the constraints of Subtasks $1, 2, 7$.

---

### Sample Input 3

~~~
7
1 1 2 3 4 5 6
6
4 2
5 1
5 3
6 2
7 3
7 6
~~~

### Sample Output 3

~~~
5
~~~

This sample input satisfies the constraints of Subtasks $2, 4, 6, 7$.

---

### Sample Input 4

~~~
4
4 1 2 3
4
4 1
4 1
2 3
2 3
~~~

### Sample Output 4

~~~
4
~~~

This sample input satisfies the constraints of Subtasks $2, 5, 7$.

---

### Sample Input 5

~~~
7
1 1 1 3 3 4 4
5
6 1
6 3
7 1
5 1
5 1
~~~

### Sample Output 5

~~~
5
~~~

This sample input satisfies the constraints of Subtasks $2, 6, 7$.

---

### Sample Input 6

~~~
11
3 1 2 5 6 7 8 4 4 5 10
6
2 1
9 8
11 8
10 4
5 6
5 7
~~~

### Sample Output 6

~~~
6
~~~

This sample input satisfies the constraints of Subtasks $2, 7$.


