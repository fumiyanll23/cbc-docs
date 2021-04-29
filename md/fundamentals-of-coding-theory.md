<!--
目的: 符号理論の基本的な知識について理解する
キーワード: (線型) 符号、生成行列、パリティ検査行列、双対符号、ハミング距離、ハミング重み
-->

# はじめに - Before You Read

符号理論 (coding theory) は、1948年にC。Shannonによって提唱された論文 "A Mathematical Theory of Communication" (通信の数学的理論) に端を発する。
本記事ではcode-based暗号を理解するうえで最低限必要となる符号理論の基礎知識を紹介する。

# 符号とは? - What Is a Code?

## Def. 符号 (code)

有限体$\mathbb{F}$上の**線型符号** (linear code) または単に**符号** (code) $C$とは、$n$次元線型空間$\mathbb{F}^{n}$の部分空間

$$C \coloneqq \{\mathbf{c}_{1}, \mathbf{c}_{2}, \ldots, \mathbf{c}_{M}\}$$

である。
$C$の元$\mathbf{c}_{i}\ (i = 1, 2, \ldots, M)$を**符号語** (codeword) といい、$n$を**符号長** (code length) という。
特に、$C$が$k$次元部分空間$\mathbb{F}^{k}$である (つまり、$\mathrm{dim}(C) = k$が成り立つ) とき、$C$は$(n, k)$線型符号 (linear code) または$(n, k)$符号であるといい、$k$を符号$C$の**次元** (dimention) とよぶ。

**注**)
以降、線型符号のことを単に符号と記す。

## 符号の性質

有限体$\mathbb{F}$上の符号$C = \{\bf{c}_{1}, \bf{c}_{2}, \ldots, \bf{c}_{M}\}$に対して、以下の性質が成り立つ。どれも容易に示せるので、証明は省略する：

1. 任意の2つの符号語$\mathbf{c}_{1}, \mathbf{c}_{2}$に対して、$\mathbf{c}_{1} + \mathbf{c}_{2}$もまた符号語である、

1. 任意の符号語$\mathbf{c}$とスカラー$\alpha\in\mathbb{F}$に対して、$\alpha\mathbf{c}$もまた符号語である、

1. 零ベクトル$\mathbf{0}$は常に符号語である、

1. $\mid\mathbb{F}\mid = q$のとき、$(n, k)$符号$C$の位数 (符号語の総数) は$M = q^{k}$である。$\Box$

符号を表現する方法として、以下に挙げる生成行列による表現が一般的である。

## Def. 生成行列 (generator matrix)

各行が、有限体$\mathbb{F}$上の$(n, k)$符号$C$の基底 (basis) であるような$k\times n$行列$G$を、符号$C$の**生成行列** (generator matrix) という。

**注**)
符号の基底は一意に定まらないため、生成行列もまた一意に定まらない。
また、符号$C$の生成行列に対して行基本変形を施したものもまた$C$の生成行列となる。

# 双対符号とは? - What Is a Dual Code?

## Def. 双対符号 (dual code)

有限体$\mathbb{F}$上の符号$C$のすべての符号語と直交するような$\mathbb{F}^{n}$上のベクトル全体の集合を**双対符号** (dual code) といい、$C^{\perp}$で表す。
つまり、

$$C^{\perp} \coloneqq \{\bf{x}\in\mathbb{F}^{n} \mid {}^{\forall}\bf{c}\in\mathbb{F}^{n},\ \bf{x}\cdot\bf{c} = 0\}.$$

**注**)
定義から明らかなように、双対符号$C^{\perp}$は元の符号$C$の直交補空間 (orthogonal complement) である。

## Def. パリティ検査行列 (parity check matrix)

# 重みと距離 - Weights and Distances

## Def. ハミング重み (Hamming weight)

## Def. ハミング距離 (Hamming distance)

# 参考文献 - References

1. 植松友彦、代数系と符号理論、オーム社、2010。

1. 齋藤正彦、線型代数入門、東京大学出版、1966。
