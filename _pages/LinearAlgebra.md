---
mayout: single
author_profile: true
title:  "Guidance"
date:   2026-02-04 23:04:30 +0900
categories: LinearAlgebra

---
<!-- _class: title -->
<!-- _paginate: false -->
<!-- _header: "" -->

# Linear Algebra (線形代数)

##### Prof. Kentaro Takemura, Ph.D (takemura@tokai.ac.jp)
Department of Applied Computer Engineering
School of Information Science and Engineering 
Tokai University

<!-- paginate: true -->
---
<!-- _class: chapter -->
# ガイダンス
線形代数は，理工系大学生に必須の初等数学です．理系において学ばないという選択肢はないです．必ず，1年次に履修してください．

- 内容
  1. 教科書・参考書
  2. 学習目標
  3. 評価方法
  4. Python開発環境
  5. スケジュール

---
# 教科書・参考書
<!-- _class: split -->
<div class=ldiv>

日本語版
- **ストラング：教養の線形代数**
  *Gilbert Strang著，松崎公紀，訳*  
  近代科学社，6,160円+税

補足
- スライドを配布する予定だが，理解を深めるため，購入を強く推奨．
- **「線形代数は理工系大学生に必須の初等数学」**，教科書を手元に置くことは無駄ではない！
- 難易度高めの教科書ですが，将来的に役に立ちます．
</div>
<div class=rdiv>

![](https://m.media-amazon.com/images/I/71YhOj4qblL._SY522_.jpg)<span class ="img-caption">図1 : 教科書</span>
</div>



---
# 学習目標
### リベラルアーツコース(他学科向け)では
1. **行列の基本的な計算**  
   - 逆行列，固有値・固有ベクトル，行列式が計算できる。
2. **行列を用いた工学的応用**  
   - 最小二乗法，主成分分析が理解できる。
### コンピュータサイエンスコース(DA向け)では
1. **リベラルアーツコースの内容**に加え
2. **Pythonを用いたプログラミング**  
   - 行列演算をプログラムで実装できることを目指す。  

---
# 評価方法
**100点満点**
- **:レポート50%**
  - **遅延は一切認めません**
  - **指定の用紙を使用すること**
  - ソフトウェアを使用して**A4用紙に整形されたPDFファイル**をOpenLMSに提出．
  - 直接PDFに記入してもOK．但し，OpenLMS上で，解答が見えるか確認すること．
- **試験50%**
  - 中間試験 25%
  - 期末試験 25%

---
# Pythonの開発環境
- Python3(バージョン３系)，venvで仮想環境の構築を推奨
- 必要なモジュール(numpy, matplotlib)はpipで管理
- エディタ, 統合開発環境
なんでも良いが，PyCharm，VSCodeが主流
- 環境構築が難しい場合(非推奨)
• Google Colaboratory(https://colab.research.google.com)

---
# スケジュール
<!-- _class: split -->

<div class=ldiv>


**前半**
• 4/14：ガイダンス
• 4/21：ベクトルと行列
• 4/28：線形方程式
• 5/12：逆行列
• 5/19：ベクトル空間
• 5/26：階数 【オンデマンド】
• 6/02：線形写像
• 6/09：中間試験 (試験範囲は前半部分)
</div>

<div class=rdiv>

**後半**
• 6/16：直交性
• 6/23：射影 直交化法
• 6/30：行列式
• 7/07：固有値，固有ベクトル
• 7/14：特異値分解，主成分分析，線形変換
• 7/21：期末試験 (試験範囲は全範囲)
</div>

---
<!-- _class: chapter -->
# ベクトルと行列
- 授業テーマ：ベクトルと行列
- キーワード：ベクトル，行列
- 参考書範囲：pp.1--44
- 事前学習(100分)：高校数学のベクトルについて復習
- 授業概要：ベクトルの線形結合と行列について学ぶ
- 授業学習目標：ベクトルの線形結合，内積，ノルム，行列について理解する
- 事後学習(60分)：Python環境の構築
- 宿題(40分)：レポートNo.1に取り組む
- 留意事項：

---
# ベクトルの線形結合
**列ベクトルと転置ベクトル**
$$\mathbf{v} = \begin{bmatrix} v_1 \\ v_2 \end{bmatrix}=\begin{bmatrix} v_1 & v_2 \end{bmatrix}^\top,  \quad 
    \mathbf{w} = \begin{bmatrix} w_1 \\ w_2 \end{bmatrix}=\begin{bmatrix} w_1 & w_2 \end{bmatrix}^\top$$

Note: $\top$は，転置を意味する

**和，差，零，スカラー積は線形結合**
- **ベクトルの和：** $\mathbf{v} + \mathbf{w} = \begin{bmatrix} \quad & \quad \\  \quad & \quad \end{bmatrix}$
- **和，スカラー積：**
$2\mathbf{v}=\begin{bmatrix}\quad\\\quad\end{bmatrix}$, $-\mathbf{v}=\begin{bmatrix}\quad\\\quad\end{bmatrix}$, $c\mathbf{v}=\begin{bmatrix}\quad\\\quad\end{bmatrix}$
- **線形結合：** $a\mathbf{v} + b\mathbf{w} = \begin{bmatrix} \qquad\qquad \\ \qquad \end{bmatrix}$

</div>
