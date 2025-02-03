Score: $100$ points

### Problem Statement

President K is designing a pattern represented by a grid with $N$ rows and $N$ columns. To achieve this, he has decided to paint each cell with a color represented by an integer number. Let us refer to the cell in the $i$-th row ($1 \leq i \leq N$) and $j$-th column ($1 \leq j \leq N$) as cell $(i,j)$.

Currently, the cells in the first column and first row are already painted. Specifically, cell $(i,1)$ ($1 \leq i \leq N$) is painted with color $A_i$ and cell $(1,j)$ ($1 \leq j \leq N$) is painted with color $B_j$. Note that $A_1 = B_1$.

For the remaining unpainted cells, President K is going to paint them by the following procedure:

<ul>
<li> For each $i=2,3,\dots,N$ in order, paint the cells in the $i$-th row as follows:
<ul>
<li> For each $j=2,3,\dots,N$ in order, paint cell $(i,j)$ with the color that has the larger number between:
<ul>
<li> The color of cell $(i-1,j)$, and 
<li> The color of cell $(i,j-1)$.
</ul>
If both colors have the same number, paint the cell with that color.
</ul>
</ul>

President K would like to determine the color that is painted on the largest number of cells after all $N^2$ cells have been painted, as well as the number of cells painted with that color.

Write a program that, given the size of the grid and the color information for the first column and first row, determines the color number painted on the largest number of cells and the number of cells painted with that color. If multiple colors are painted on the largest number of cells, output the <b>largest color number</b> among them.

---

### Input

Read the following data from the standard input.

~~~
$N$
$A_1$ $A_2$ $\cdots$ $A_N$
$B_1$ $B_2$ $\cdots$ $B_N$
~~~

### Output

Write one line to the standard output containing two integers separated by a space:

<ol>
<li> The color number that is painted on the largest number of cells, and
<li> The number of cells painted with that color.
</ol>

If multiple colors are painted on the largest number of cells, output the largest color number among them.

---

### Constraints

<ul>
<li> $2 \leq N \leq 200\,000$.
<li> $1 \leq A_i \leq 10^9$ ($1 \leq i \leq N$).
<li> $1 \leq B_j \leq 10^9$ ($1 \leq j \leq N$).
<li> $A_1 = B_1$.
<li> Given values are all integers.
</ul>

### Subtasks

<ol>
<li> ($15$ points) $N \leq 500$, $A_i \leq 100\,000$ ($1 \leq i \leq N$), $B_j \leq 100\,000$ ($1 \leq j \leq N$).
<li> ($10$ points) $N \leq 500$.
<li> ($20$ points) $A_i \leq 2$ ($1 \leq i \leq N$), $B_j \leq 2$ ($1 \leq j \leq N$).
<li> ($25$ points) $A_i < A_{i+1}$ ($1 \leq i \leq N-1$), $B_j < B_{j+1}$ ($1 \leq j \leq N-1$).
<li> ($30$ points) No additional constraints.
</ol>

---

### Sample Input 1

~~~
3
5 2 5
5 3 1
~~~

### Sample Output 1

~~~
5 4
~~~

In this sample, the color of each cell in the grid will be as follows:

<style>
.table-bordered {
    text-align: center;
    width: 120px;
    height: 120px;
    max-width: 100%;
}
</style>

<p>
<table class="table-bordered">
    <tr>
        <td>5</td>
        <td>3</td>
        <td>1</td>
    </tr>
    <tr>
        <td>2</td>
        <td>3</td>
        <td>3</td>
    </tr>
    <tr>
        <td>5</td>
        <td>5</td>
        <td>5</td>
    </tr>
</table>
</p>

The color number painted on the largest number of cells is $5$, which appears on $4$ cells. Thus, print $5$ and $4$ in this order, separated by a space.

This sample input satisfies the constraints of Subtasks $1$, $2$, and $5$.

---

### Sample Input 2

~~~
3
1 7 8
1 3 5
~~~

### Sample Output 2

~~~
8 3
~~~

In this sample, the color of each cell in the grid will be as follows:

<p>
<table class="table-bordered">
    <tr>
        <td>1</td>
        <td>3</td>
        <td>5</td>
    </tr>
    <tr>
        <td>7</td>
        <td>7</td>
        <td>7</td>
    </tr>
    <tr>
        <td>8</td>
        <td>8</td>
        <td>8</td>
    </tr>
</table>
</p>

The color numbers painted on the largest number of cells are $7$ and $8$, each painted on $3$ cells. In this case, output the larger color number, $8$, followed by the number of cells, $3$, separated by a space.

This sample input satisfies the constraints of Subtasks $1$, $2$, $4$, and $5$.

---

### Sample Input 3

~~~
4
2 1 2 1
2 1 1 2
~~~

### Sample Output 3

~~~
2 10
~~~

This sample input satisfies the constraints of Subtasks $1$, $2$, $3$, and $5$.
