配点： $20$ 点

###

あなたは以下のルールでダーツゲームをすることになった．

> あなたは，矢を的（まと）に向かって $4$ 本まで投げることができる．必ずしも $4$ 本全てを投げる必要はなく，$1$ 本も投げなくてもかまわない．的は $N$ 個の部分に区切られていて，各々の部分に点数 $P_1,\ldots,P_N$ が書かれている．矢が刺さった場所の点数の合計 $S$ があなたの得点の基礎となる．$S$ があらかじめ決められたある点数 $M$ 以下の場合は $S$ がそのまま
あなたの得点となる．しかし，$S$ が $M$ を超えた場合はあなたの得点は $0$ 点となる．

的に書かれている点数と $M$ の値が与えられたとき，あなたが得ることのできる点数の最大値を求めるプログラムを作成せよ．

---

### 入力

入力ファイルのファイル名は `input.txt` である．

$1$ 行目には，整数 $N$ ($1\leqq N\leqq 1000$) と $M$ ($1\leqq M\leqq 200000000=2\times 10^8$) がこの順に空白区切りで書かれている．$2$ 行目以降の第 $1 + i$ 行目 ($1\leqq i\leqq N$) には， $P_i$ ($1 \leqq P_i\leqq 100000000=10^8$) が書かれている．

採点用データのうち, 配点の $20$ %分は $N \leqq 100$ を満たし，配点の $50$ %分は $N \leqq 300$ を満たす．

### 出力

出力ファイルのファイル名は `output.txt` である．

`output.txt` は 1 行だけからなり，あなたが得ることのできる点数の最大値を含む．

---

### 入力例 1

~~~
4 50
3
14
15
9
~~~

### 出力例 1

~~~
48
~~~

この例では，$15$ 点の部分に $3$ 本，$3$ 点の部分に $1$ 本の矢が刺さった場合にあなたの得点は最大になり，その得点は $48$ 点である．

---

### 入力例 2

~~~
3 21
16
11
2
~~~

### 出力例 2

~~~
20
~~~

この例では，$16$ 点の場所に $1$ 本，$2$ 点の場所に $2$ 本の矢が刺さった場合にあなたの得点は最大になり，その得点は $20$ 点である．
