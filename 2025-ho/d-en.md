Score: $100$ points

### Problem Statement

Just Odd Inventions Co., Ltd. is a company renowned for doing "just odd inventions."
Here we just call it JOI Company.

To celebrate the 5th anniversary of their flagship product, "Just Long Neckties," JOI Company has invented a new product: "Just Stretchable Neckties."
As its name suggests, this new necktie has the unique feature of being able to extend its length indefinitely.

JOI Company has decided to hold a showcase event to promote the new necktie, and you have been selected as the host of the event.
At the event, several models wearing the new neckties will appear on stage.
Initially, the <b>length</b> of every necktie worn by the models is set to $1$.

After that, you will carry out a total of $N$ <b>performances</b> to demonstrate the necktie's stretchable feature to the audience.
Each performance is conducted as follows:

<ol>

<li> First, you ask the audience to call out a number of their choice.
Let this number be $x$.

<li> Next, you decide whether to respond or ignore it.

<ul>

<li> If you choose to respond to it, you must select one of the models on stage whose necktie length is currently <b>less than or equal to</b> $x$ and set the length of that model's necktie to exactly $x$.
(Note that you may select a model whose necktie length is already $x$.)
However, if no model can be selected, the showcase event will fail.

<li> If you choose to ignore it, you do nothing.
</ul>
</ol>

However, if you ignore the audience's number two or more times in a row, the audience will get angry, and the showcase event will fail.

The number of models on stage, denoted as $k$ ($k\geq 1$), has not yet been determined.
Since hiring models costs considerable money, it is desirable to keep $k$ as small as possible.
The minimum value of $k$ required to prevent the showcase event from failing depends on the numbers called out by the audience during the performances.
Fortunately, you possess precognitive abilities and have foreseen that the number called out by the audience during the $i$-th performance ($1\leq i\leq N$) will be $A_i$.

Write a program which, given the numbers called out by the audience during the showcase event, calculates the minimum number of models $k$ required to prevent the showcase event from failing.

---

### Input

Read the following data from the standard input.
~~~
$N$
$A_1$ $A_2$ $\cdots$ $A_N$
~~~

### Output

Write one line to the standard output.
The output should contain the minimum number of models $k$ required to prevent the showcase event from failing.

---

### Constraints

<ul>
<li> $2 \leq N \leq 5\,000\,000$.
<li> $1\leq A_i \leq 21$ ($1 \leq i \leq N$).
<li> Given values are all integers.
</ul>

### Subtasks

<ol>
<li> ($10$ points) $N\leq 15$.
<li> ($6$ points) $N\leq 500$, $A_i \leq 2$ ($1 \leq i \leq N$).
<li> ($12$ points) $N\leq 500$, $A_i \leq 5$ ($1 \leq i \leq N$).
<li> ($18$ points) $N\leq 500$, $A_i \leq 15$ ($1 \leq i \leq N$).
<li> ($26$ points) $N\leq 500\,000$, $A_i \leq 15$ ($1 \leq i \leq N$).
<li> ($10$ points) $N\leq 500\,000$.
<li> ($18$ points) No additional constraints.
</ol>

---

### Sample Input 1

~~~
5
5 3 4 2 1
~~~

### Sample Output 1

~~~
2
~~~

When $k=2$, the showcase event can be conducted as follows, for example:

<ul>

<li> First, two models wearing the new neckties appear on stage. Initially, the length of each model's necktie is $1$.

<li> During the 1st performance, the audience calls out $5$. You ignore this.

<li> During the 2nd performance, the audience calls out $3$. You respond to this by selecting the first model and setting their necktie length to $3$. The necktie lengths of the two models are now $3$ and $1$, respectively.

<li> During the 3rd performance, the audience calls out $4$. You respond to this by selecting the first model and setting their necktie length to $4$. The necktie lengths of the two models are now $4$ and $1$, respectively.

<li> During the 4th performance, the audience calls out $2$. You respond to this by selecting the second model and setting their necktie length to $2$. The necktie lengths of the two models are now $4$ and $2$, respectively.

<li> During the 5th performance, the audience calls out $1$. You ignore this.
</ul>

When $k=1$, the showcase event will always fail.
For example, if you respond to the audience's numbers during the 2nd, 3rd, and 4th performances as described above, the only model's necktie length becomes $4$ after the 3rd performance.
Then, at the 4th performance, you cannot select a model whose necktie length is less than or equal to $2$, so the showcase event fails.

Hence, the minimum number of models $k$ required to prevent the showcase event from failing is $2$, and the output should be $2$.

This sample input satisfies the constraints of Subtasks $1,3,4,5,6,$ and $7$.

---

### Sample Input 2

~~~
6
2 1 1 2 2 1
~~~

### Sample Output 2

~~~
1
~~~

When $k=1$, the showcase event can be conducted as follows, for example:

<ul>

<li> First, a model wearing the new necktie appear on stage. Initially, the length of the model's necktie is $1$.

<li> During the 1st performance, the audience calls out $2$. You ignore this.

<li> During the 2nd performance, the audience calls out $1$. You respond to this by selecting the only model on stage and setting their necktie length to $1$.

<li> During the 3rd performance, the audience calls out $1$. You respond to this by selecting the only model on stage and setting their necktie length to $1$.

<li> During the 4th performance, the audience calls out $2$. You respond to this by selecting the only model on stage and setting their necktie length to $2$.

<li> During the 5th performance, the audience calls out $2$. You respond to this by selecting the only model on stage and setting their necktie length to $2$.

<li> During the 6th performance, the audience calls out $1$. You ignore this.
</ul>

Note that in the example above, during the 2nd and 3rd performances, a model whose necktie length is already $1$ is selected, and their necktie length is set to $1$ again.
Such a choice, where the necktie length does not change, is also allowed.

Hence, the minimum number of models $k$ required to prevent the showcase event from failing is $1$, and the output should be $1$.

This sample input satisfies the constraints of all the subtasks.

\newline

---

### Sample Input 3

~~~
10
2 4 6 7 4 5 5 3 4 1
~~~

### Sample Output 3

~~~
3
~~~

This sample input satisfies the constraints of Subtasks $1,4,5,6,$ and $7$.


