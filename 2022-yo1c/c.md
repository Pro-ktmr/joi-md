配点： $100$ 点

### 問題文
JOI 高校には $N$ 人の生徒がおり，$1$ から $N$ までの出席番号が付けられている．

来月 JOI 高校では運動会が開催され，$N$ 人の生徒全員がこれに参加する．生徒のうち $K$ 人が赤組に，残りの $N - K$ 人が白組に属している．

出席番号 $N$ 番の葵は，自分がどちらの組に属しているかを忘れてしまった．そこで，自分以外の生徒 $N - 1$ 人それぞれがどちらの組に属しているかを聞いてまわることで，自分がどちらの組に属しているかを判断することにした．

葵以外の $N-1$ 人の組み分けの情報は，長さ $N - 1$ の文字列 $S$ で表される．$S$ の各文字は `R`，`W` のいずれかであり，その意味は次の通りである．

- $S$ の $i$ 文字目 ($1 \leqq i \leqq N - 1$) が `R` の場合は，出席番号 $i$ 番の生徒が赤組に属していることを表す．
- $S$ の $i$ 文字目 ($1 \leqq i \leqq N - 1$) が `W` の場合は，出席番号 $i$ 番の生徒が白組に属していることを表す．

葵が赤組に属しているならば `R` と，白組に属しているならば `W` と出力せよ．

### 制約
- $2 \leqq N \leqq 2\,000$．
- $1 \leqq K \leqq N-1$．
- $S$ は長さ $N - 1$ の文字列である．
- $S$ の各文字は `R`，`W` のいずれかである．
- $S$ に含まれる `R` の個数は $K-1$ 個または $K$ 個である．
- $N, K$ は整数である．

---

### 入力
入力は以下の形式で標準入力から与えられる．

~~~
$N$
$K$
$S$
~~~

### 出力
葵が赤組に属しているならば `R` と，白組に属しているならば `W` と出力せよ．

---

### 入力例 1
~~~
7
3
RWWRWW
~~~

### 出力例 1
~~~
R
~~~

出席番号 $1, 2, 3, 4, 5, 6$ 番の生徒はそれぞれ赤組，白組，白組，赤組，白組，白組に属している．

葵を除いた生徒について，赤組に属している生徒は $2$ 人，白組に属している生徒は $4$ 人である．全生徒のうち $3$ 人が赤組に，残りの $4$ 人が白組に属しているため，葵は赤組に属しているとわかる．したがって，`R` と出力する．

---

### 入力例 2
~~~
5
3
RWRR
~~~

### 出力例 2
~~~
W
~~~

出席番号 $1, 2, 3, 4$ 番の生徒はそれぞれ赤組，白組，赤組，赤組に属している．

葵を除いた生徒について，赤組に属している生徒は $3$ 人，白組に属している生徒は $1$ 人である．全生徒のうち $3$ 人が赤組に，残りの $2$ 人が白組に属しているため，葵は白組に属しているとわかる．したがって，`W` と出力する．

---

### 入力例 3
~~~
70
1
WWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWW
~~~

### 出力例 3
~~~
R
~~~