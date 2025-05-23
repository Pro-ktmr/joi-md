配点： $100$ 点

### 問題文

JOI 街道は東西に伸びる長さ $L$ メートルの道路であり，道路の西端から $l$ メートル ($0 \leqq l \leqq L$) 進んだ場所は地点 $l$ と呼ばれている．

さて，今年は JOI 街道で初めてマラソン大会が開催されることとなった．このマラソン大会は通常のルールとは異なり，次のようなルールに基づいて行われる．

<ul>
<li> 道路上に $N$ 個のボールが置かれており，$i$ 番目 ($1 \leqq i \leqq N$) のボールは地点 $X_i$ に置かれている．複数のボールが同じ地点に置かれていることもある．
<li> 参加者は定められたスタート地点から出発する．
<li> $N$ 個のボールをすべて持った状態で，定められたゴール地点に制限時間内にたどり着くと<b>完走</b>となる．ただし，一度持ったボールを地面に置くと失格となる．
</ul>

この大会のスタート地点，ゴール地点および制限時間はまだ公開されていないが，$Q$ 個のシナリオのいずれかになることは既に公開されている．
$j$ 番目 ($1 \leqq j \leqq Q$) のシナリオでは，スタート地点が地点 $S_j$，ゴール地点が地点 $G_j$，制限時間が $T_j$ 秒である．

マラソン大会の参加者である理恵さんは，ボールを $1$ 個拾うのに $1$ 秒かかり，$x$ 個のボールを持った状態で道路上を $1$ メートル走るのに $x+1$ 秒かかる．

JOI 街道，ボール，シナリオに関する情報が与えられたとき，それぞれのシナリオについて，理恵さんが完走する方法が存在するかを判定するプログラムを作成せよ．

---

### 入力

入力は以下の形式で標準入力から与えられる．

~~~
$N$ $L$
$X_1$ $X_2$ $\cdots$ $X_N$
$Q$
$S_1$ $G_1$ $T_1$
$S_2$ $G_2$ $T_2$
$\vdots$
$S_Q$ $G_Q$ $T_Q$
~~~

### 出力

標準出力に $Q$ 行で出力せよ．
$j$ 行目 ($1 \leqq j \leqq Q$) には，$j$ 番目のシナリオにおいて理恵さんが完走する方法が存在する場合 <code>Yes</code>，そうでない場合 <code>No</code> を出力せよ．

---

### 制約

<ul>
<li> $1 \leqq N \leqq 500\,000$．
<li> $1 \leqq L \leqq 500\,000$．
<li> $0 \leqq X_i \leqq L$ ($1 \leqq i \leqq N$)．
<li> $1 \leqq Q \leqq 500\,000$．
<li> $0 \leqq S_j \leqq L$ ($1 \leqq j \leqq Q$)．
<li> $0 \leqq G_j \leqq L$ ($1 \leqq j \leqq Q$)．
<li> $1 \leqq T_j \leqq 500\,000$ ($1 \leqq j \leqq Q$)．
<li> 入力される値はすべて整数である．
</ul>

### 小課題

<ol>
<li> ($7$ 点) $N \leqq 7$，$Q \leqq 10$，$S_j = 0$，$G_j = 0$ ($1 \leqq j \leqq Q$)．
<li> ($7$ 点) $N \leqq 7$，$Q \leqq 10$．
<li> ($10$ 点) $N \leqq 14$，$Q \leqq 10$．
<li> ($28$ 点) $N \leqq 100$，$Q \leqq 10$．
<li> ($10$ 点) $N \leqq 2\,000$，$Q \leqq 10$．
<li> ($19$ 点) $N \leqq 2\,000$．
<li> ($19$ 点) 追加の制約はない．
</ol>

---

### 入力例 1

~~~
3 100
30 80 30
3
0 100 403
0 100 300
0 100 262
~~~

### 出力例 1

~~~
Yes
Yes
No
~~~

$1$ 番目のシナリオでは，スタート地点は地点 $0$，ゴール地点は地点 $100$，制限時間は $403$ 秒である．以下のようにして，制限時間内の $263$ 秒で完走することができる．よって，$1$ 行目には <code>Yes</code> を出力する．

<style>
.example-01-table th,
.example-01-table td {
    text-align: center;
    border: solid 1px;
    padding: 4px 8px;
}
.example-01-table tr > *:nth-last-child(4) {
    border-right: double 3px;
}
</style>

<table class="example-01-table">
<thead>
<tr>
<th>順番</th>
<th>行動</th>
<th>消費時間</th>
<th>累計時間</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>地点 <var>0</var> から出発し，地点 <var>30</var> に移動する．</td>
<td><var>30</var> 秒</td>
<td><var>30</var> 秒</td>
</tr>
<tr>
<td>2</td>
<td><var>1</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>31</var> 秒</td>
</tr>
<tr>
<td>3</td>
<td><var>3</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>32</var> 秒</td>
</tr>
<tr>
<td>4</td>
<td>地点 <var>30</var> から地点 <var>80</var> に移動する．</td>
<td><var>150</var> 秒</td>
<td><var>182</var> 秒</td>
</tr>
<tr>
<td>5</td>
<td><var>2</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>183</var> 秒</td>
</tr>
<tr>
<td>6</td>
<td>地点 <var>80</var> から地点 <var>100</var> に移動し，完走する．</td>
<td><var>80</var> 秒</td>
<td><var>263</var> 秒</td>
</tr>
</tbody>
</table>

$2$ 番目のシナリオでは，スタート地点とゴール地点は $1$ 番目のシナリオと同じであるが，制限時間は $300$ 秒となっている．前と同じ方法で，制限時間内の $263$ 秒で完走することができる．よって，$2$ 行目には <code>Yes</code> を出力する．

$3$ 番目のシナリオでは，スタート地点とゴール地点は $1, 2$ 番目のシナリオと同じであるが，制限時間は $262$ 秒となっている．制限時間内に完走する方法は存在しない．よって，$3$ 行目には <code>No</code> を出力する．

この入力例は小課題 $2, 3, 4, 5, 6, 7$ の制約を満たす．

---

### 入力例 2

~~~
3 100
30 80 30
3
0 0 403
0 0 300
0 0 262
~~~

### 出力例 2

~~~
Yes
No
No
~~~

$1$ 番目のシナリオでは，スタート地点は地点 $0$，ゴール地点は地点 $0$，制限時間は $403$ 秒である．以下のようにして，制限時間内の $403$ 秒で完走することができる．よって，$1$ 行目には <code>Yes</code> を出力する．

<table class="example-01-table">
<thead>
<tr>
<th>順番</th>
<th>行動</th>
<th>消費時間</th>
<th>累計時間</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>地点 <var>0</var> から出発し，地点 <var>30</var> に移動する．</td>
<td><var>30</var> 秒</td>
<td><var>30</var> 秒</td>
</tr>
<tr>
<td>2</td>
<td><var>1</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>31</var> 秒</td>
</tr>
<tr>
<td>3</td>
<td>地点 <var>30</var> から地点 <var>80</var> に移動する．</td>
<td><var>100</var> 秒</td>
<td><var>131</var> 秒</td>
</tr>
<tr>
<td>4</td>
<td><var>2</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>132</var> 秒</td>
</tr>
<tr>
<td>5</td>
<td>地点 <var>80</var> から地点 <var>30</var> に移動する．</td>
<td><var>150</var> 秒</td>
<td><var>282</var> 秒</td>
</tr>
<tr>
<td>6</td>
<td><var>3</var> 番目のボールを拾う．</td>
<td><var>1</var> 秒</td>
<td><var>283</var> 秒</td>
</tr>
<tr>
<td>7</td>
<td>地点 <var>30</var> から地点 <var>0</var> に移動し，完走する．</td>
<td><var>120</var> 秒</td>
<td><var>403</var> 秒</td>
</tr>
</tbody>
</table>

$2, 3$ 番目のシナリオでは，スタート地点とゴール地点は $1$ 番目のシナリオと同じであるが，制限時間はそれぞれ $300$ 秒，$262$ 秒となっている．どちらについても，制限時間内に完走する方法は存在しない．よって，$2$ 行目には <code>No</code> を，$3$ 行目には <code>No</code> を出力する．

この入力例は小課題 $1, 2, 3, 4, 5, 6, 7$ の制約を満たす．

---

### 入力例 3

~~~
6 100
0 50 100 0 50 100
4
20 70 600
70 20 600
10 40 600
40 10 600
~~~

### 出力例 3

~~~
No
Yes
No
Yes
~~~

この入力例は小課題 $2, 3, 4, 5, 6, 7$ の制約を満たす．


