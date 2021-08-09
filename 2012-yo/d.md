配点： $100$ 点

### 問題
あなたはパスタが大好物であり，毎日，晩御飯にパスタを作って食べている．あなたはトマトソース，クリームソース，バジルソースの $3$ 種類のパスタを作ることができる．

$N$ 日間の晩御飯の予定を考えることにした．それぞれの日に $3$ 種類のパスタから $1$ 種類を選ぶ．ただし，同じパスタが続くと飽きてしまうので，$3$ 日以上連続して同じパスタを選んではいけない．また，$N$ 日のうちの $K$ 日分のパスタはすでに決めてある．

入力として $N$ の値と，$K$ 日分のパスタの情報が与えられたとき，条件をみたす予定が何通りあるかを $10\,000$ で割った余りを求めるプログラムを作成せよ．

---

### 入力
入力は $K + 1$ 行からなる．

$1$ 行目には $2$ つの整数 $N, K$ ($3 \leqq N \leqq 100$，$1 \leqq K \leqq N$) が空白を区切りとして書かれている．

$1 + i$ 行目 ($1 \leqq i \leqq K$) には $2$ つの整数 $A_i, B_i$ ($1 \leqq A_i \leqq N$，$1 \leqq B_i \leqq 3$) が空白を区切りとして書かれている．これは，$A_i$ 日目のパスタはすでに決まっており，$B_i = 1$ のときはトマトソースであり，$B_i = 2$ のときはクリームソースであり，$B_i = 3$ のときはバジルソースであることを表す．$A_i$ ($1 \leqq i \leqq K$) は全て異なる．与えられる入力データにおいて，条件をみたす予定は $1$ 通り以上あることが保証されている．

### 出力
条件をみたす予定が何通りあるかを $10\,000$ で割った余りを $1$ 行で出力せよ．

---

### 入力例 1
~~~
5 3
3 1
1 1
4 2
~~~

### 出力例 1
~~~
6
~~~

入出力例 $1$ において，あなたは $5$ 日間の予定を考える．$1$ 日目と $3$ 日目はトマトソースであり，$4$ 日目はクリームソースである．また，$3$ 日以上連続して同じパスタを選んではいけない．これらの条件をみたす予定は $6$ 通りある．

![](https://img.atcoder.jp/joi2012yo/2012-yo-t4-fig01.png)

この表では，$1$ はトマトソースを，$2$ はクリームソースを，$3$ はバジルソースを表す．

---

### 入力例 2
~~~
20 5
10 2
4 3
12 1
13 2
9 1
~~~

### 出力例 2
~~~
2640
~~~

入出力例 $2$ において，条件をみたす予定は全部で $4\,112\,640$ 通りある．それを $10\,000$ で割った余りである $2\,640$ を出力する．