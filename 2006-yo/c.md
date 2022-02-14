配点： $100$ 点

### 問題

サイコロが以下の図のような向きで置かれている．

ここで使用するサイコロは，この図のように，上側に $1$，南側に $2$ があるときは，東側に $3$ があるものとする．サイコロの向かいあう面の和は必ず $7$ なので，見えない面はそれぞれ北側 $5$，西側 $4$，下側 $6$ になっている．

![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_base.png)

この初期配置の状態から指示に従ってサイコロを動かしていく．ただし，指示は以下の $6$ 通りの操作を何回か行うものである．

![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_east.png)
![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_left.png)
![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_north.png)
![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_right.png)
![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_south.png)
![](https://img.atcoder.jp/joi2006yo/2006-yo-t3-fig_west.png)

North，East，South，West の各操作は指示された方向へサイコロを $90$ 度回転させる．
Right，Left の $2$ つの操作は上下の面はそのままで水平方向に $90$ 度回転させる．（回転させる向きに要注意．）

初期配置で上の面に出ている目 $1$ を初期値とし，$1$ 回の操作が終わるたびに，上の面に出ている目の数を加算していき，指示にしたがってすべての操作を終えたときの合計値を出力するプログラムを作成しなさい.

入力の $1$ 行目には総指示回数 $n$ が書かれていて，続く $n$ 行の各行には 「North，East，South，West，Right，Left」 のいずれか $1$ つの指示が書かれているものとする．ただし，$n \leqq 10\,000$ とする．

出力においては，出力（合計値）の後に改行を入れること．

---

### 入力例 1

~~~
5
North
North
East
South
West
~~~

### 出力例 1

~~~
21
~~~

---

### 入力例 2

~~~
8
West
North
Left
South
Right
North
Left
East
~~~

### 出力例 2

~~~
34
~~~
