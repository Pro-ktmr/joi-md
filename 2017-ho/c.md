配点： $100$ 点

JOIOI 王国は $H$ 行 $W$ 列のマスに区切られた長方形の形をしている．JOIOI 王国では，行政の効率化のため，国全体を $2$ つの地域 JOI と IOI に分けることにした．

地域の分け方が複雑になりすぎるのを防ぐため，以下の条件を満たすように分割を行うことにした：

- 各地域は，$1$ つ以上のマスを含む．
- それぞれのマスは，$2$ つの地域のうちのちょうど $1$ つに属する．
- 地域 JOI に属するどの $2$ つのマスの間も，その地域に属さないマスに入らずに辺で接しているマスへの移動を繰り返すことにより移動できる．地域 IOI についても同様である．
- 各行，各列について，その行または列に属するマス全体を取り出したとき，それぞれの地域のマスはひとつながりになっている．ただし，その行あるいは列のすべてのマスが同じ地域に属していてもよい．

各マスには標高と呼ばれる整数が定まっている．地域への分割を行った後は，各地域内での移動が活発になると想定される．地域内での標高の差があまりに大きいと移動が大変であるため，同じ地域内での標高差ができるだけ小さくなるように分割を行いたい．すなわち，地域 JOI の中での標高の最大値と最小値の差と，地域 IOI の中での標高の最大値と最小値の差のうち，大きい方の値を最小化したい．

### 課題
JOIOI 王国の各マスの標高が与えられたとき，条件を満たすように地域の分割をした際の，地域 JOI の中での標高の最大値と最小値の差と，地域 IOI の中での標高の最大値と最小値の差のうち，大きい方の値の最小値を求めるプログラムを作成せよ．

---

### 入力
標準入力から以下の入力を読み込め．

- $1$ 行目には，$2$ 個の整数 $H, W$ が空白を区切りとして書かれている．これらは，JOIOI 国が $H$ 行 $W$ 列のマスに区切られた長方形の形をしていることを表す．
- 続く $H$ 行のうちの $i$ 行目 ($1 \leqq i \leqq H$) には，$W$ 個の整数 $A_{i, 1}, A_{i, 2}, \ldots, A_{i, W}$ が空白を区切りとして書かれている．これは，JOIOI 王国の上から $i$ 行目，左から $j$ 列目 ($1 \leqq j \leqq W$) の標高が $A_{i, j}$ であることを表す．

### 出力
標準出力に，条件を満たすように地域の分割をした際の，地域 JOI の中での標高の最大値と最小値の差と，地域 IOI の中での標高の最大値と最小値の差のうち，大きい方の値の最小値を $1$ 行で出力せよ．

---

### 制限
すべての入力データは以下の条件を満たす．

- $2 \leqq H \leqq 2\,000$．
- $2 \leqq W \leqq 2\,000$．
- $1 \leqq A_{i, j} \leqq 1\,000\,000\,000$ ($1 \leqq i \leqq H$，$1 \leqq j \leqq W$)．

### 小課題 1 [15 点]
以下の条件を満たす．

- $H \leqq 10$．
- $W \leqq 10$．

### 小課題 2 [45 点]
以下の条件を満たす．

- $H \leqq 200$．
- $W \leqq 200$．

### 小課題 3 [40 点]
追加の制限はない．

---

### 入力例 1
```
4 4
1 12 6 11
11 10 2 14
10 1 9 20
4 17 19 10
```

### 出力例 1
```
11
```

この入力例では，例えば下の図のように地域を分割すればよい．ここで，J は地域 JOI，I は地域 IOI を表す．

```
J J J I
J J J I
J J I I
J I I I
```

ここで，例えば次のような分割は，左から $3$ 列目において地域 IOI がひとつながりになっていないため，条件を満たす分割ではない．

```
J J I I
J J J I
J J J I
J I I I
```

---

### 入力例 2
```
8 6
23 23 10 11 16 21
15 26 19 28 19 20
25 26 28 16 15 11
11 8 19 11 15 24
14 19 15 14 24 11
10 8 11 7 6 14
23 5 19 23 17 17
18 11 21 14 20 16
```

### 出力例 2
```
18
```