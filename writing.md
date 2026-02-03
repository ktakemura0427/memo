---
layout: page
title: Writing
permalink: /writing/
---

## 一般的論文ルール
- 結論はネガティブにならないように．ネガティブなまとめ方をすると研究不完全　＝>　努力が足りない，卒業に不十分などネガティブなものが連鎖します．
- 概要には，自分の研究をわかりやすく示すような図があるとGood. 読むか読まないかは図の印象が大きく影響します．
- 点と丸は，．を使用．日本語文章の場合，全角のものを使用することに注意．
- 日本語の論文の場合，括弧，ピリオド，カンマなどは全角，算用数字だけ半角で統一しておきましょう．
- 最低限のスペルチェックをすること(WORDに貼り付けるなど. emacs なら ispell)
- 略語を用いる場合は、初出の際にことわること(例：ヘッドマウントディスプレイ (以下，HMD))．
- 図のラベルは`\label{fig:xxx}`とする

## タイトルについて
- 卒論概要では，英語のタイトルは最初だけ大文字．学会発表等はルールが異なる．
- 自分のオリジナルのアイディアが含まれるようなタイトルにすること
- 「の開発」は最悪．「に関する研究」というタイトルは全てを網羅的に研究した人のみに許されるため１０年早い．

## キーワードについて
- アブストラクトに含まれるものから選択

## グラフについて
- 複数ある場合，縦軸，ヨコ軸のフォントサイズは同じくらいに表示されるような調整をすること．
- 図のキャプションは文章の場合，最後にピリオドを書く．文章でない場合はピリオドは不要．
- 図中の説明及びキャプションは，英語とします．
- 図中の英語はTimes New Romanで書くこと．
- 図のフォーマットはPDFとする．必ずベクター情報が含まれること(文字などが編集可能であること)．
- 図のタテヨコ比は原則4:3にする．写真を切り抜く場合は注意．
- 図を並べて`subfloat`を用いて(a),(b)と表示する場合は，英語では`Fig.1a` と文中で表示する．括弧はつけない．日本語では`Fig.1(a)`と括弧がつく．
- 図に含まれる色の種類は，少ない方がベター．白黒でかけることがベスト．
- グラフをPythonで作成するようにしよう
  [tlab-pyplotter](https://bitbucket.org/takemuralab/tlab-pyplotter/src/main/)

## 数式について
- ベクトルと行列は太文字にすること
- 数式はできる限り参照せず文中として記述する．(NEW)
  - (例) 注視点$\bf p$は，

```tex
\begin{equation}
{\bf p} = 
\end{equation}
```

- 数式を文章中で参照するときは，式3と書く．式(3)とは書かない.
- カンマ，ピリオドをつけること(NEW)
- `sin`, `cos`, `tan` は texの記法を用いて記述する．`arcsin`, `arccos`, `arctan`も同様．

## 語句について
- 語句の省略は，必ず正式名称を記載した後，定義して利用する．
  - 例：反射点(以下，グリント）[New]

## 製品名について
- カッコ書きで(型番，会社，会社のロケーション)とする．
- 修論概要，卒論概要については，(型番，会社，国)とする．
- 国はJP,USなどの略称で．

## 参考文献の書き方 (bibtexを用いること)
- [卒論・修論・bib修正用.py](https://scrapbox.io/files/65c620bc948c120025c07509.py) 概要は名前手動変更
- 参考文献は，名前，タイトル，会議名，ページ，年度等が出力される必要があり，bibtexを用いる．
- `\bibliographystyle{ieeetr}`を利用すること(gaiyou.bst)
- 著者は1人，2人の場合はそのままかく
- 著者が3人以上の場合は，第一著者 [/ et al.]とする．
- 日本語の場合は姓のみ．英語の場合は，FirstNameはイニシャルのみ．
- 省略できるものは省略（省略語＋.（ドット）となるように）
  - 例：International→Int. ，Symposium→Symp. ，in Proceeding →in Proc. ，in 2007 11th →in Proc. of the 11th, Association of Computer, Proceeding→ Proc. ,Transaction → Trans. , Association → Assoc. , Conference → Conf.
  - 概要ではこれらも省略？ 例：Biomedical →Biomed. , Engineering→Eng.

### bibtexで表示する内容
#### 論文の場合
```tex
@article{Takemura2014,
  title={Estimation of a focused object using a corneal surface image for eye-based interaction},
  author={Takemura, Kentaro and Yamakawa, Tomohisa and Takamatsu, Jun and Ogasawara, Tsukasa},
  journal={Journal of eye movement research},
  volume={7},
  number={3},
  pages={1--9},
  year={2014}
}
```

#### 国際会議の場合
```tex
@inproceedings{Takemura2010,
  title={Estimating 3D point-of-regard and visualizing gaze trajectories under natural head movements},
  author={Takemura, Kentaro and Kohashi, Yuji and Suenaga, Tsuyoshi and Takamatsu, Jun and Ogasawara, Tsukasa},
  booktitle={Proceedings of the 2010 ACM Symposium on Eye-Tracking Research \& Applications},
  pages={157--160},
  year={2010}
}
```

- 修論，卒論ではフルで書くが，概要ではInt. Conf. などと省略する．
- ACM系のペーパではArticle Noが近年採用されているため，bstを編集してArticle No.の出力する必要がある．-> [Article No. 追加のやりかた](#65cae6f7afaaf7002674e59e)
- doiは，修論，卒論は必要ないが，国際会議や論文誌は，それぞれのルールに合わせて．

```tex
@inproceedings{Abdrabou2019,
  author = {Abdrabou, Yasmeen and Mostafa, Mariam and Khamis, Mohamed and Elmougy, Amr},
  title = {Calibration-Free Text Entry Using Smooth Pursuit Eye Movements},
  year = {2019},
  doi = {10.1145/3314111.3319838},
  booktitle = {Proceedings of the 11th ACM Symposium on Eye Tracking Research \& Applications},
  articleno = {35}
}
```

- ACM系のぺーパー（ETRAなど）は，筆頭著者のlast nameのアルファベット順に引用文献が並べられるのでそのままでOK．
  - 例: (Hiroe et al. 2018; Nagamatsu et al. 2009; Vidal et al. 2013)
- 国内学会のもまれにアルファベット順になっているので，`\bibliographystyle{}`を`jplain`->`junsrt`にすると発表順になる．（直すかどうかは適宜確認）

## 単位について
- [[　]]を付けずに記入．ただし数字と単位の間は半角スペース (例: 1 kHz)

## その他
- 「行う」に送り仮名を統一
- 及びの使い方は，A，B及びC
- 「の為」は使わず，「のため」と平仮名にする．
- 「事」は使わず，「こと」と平仮名にする．[NEW]
- 適用と適応は違うことを理解すること．英語で理解すると簡単．
- 被験者ではなく実験協力者
- 細かな表現についてはできる限りラボで共通化–> [論文用語句](NEW)
- 一組，八の字など単語に含まれるものは漢数字

## 修論・卒論向け
- キャプションは英語で，Fig. Table を採用する．図中の文字も英語．すべての図表で統一すること．
- 商品の図，関連研究の図は掲載しないこと．
- ページ数が限られているわけではないので，十分に例を示すべき．(NEW)
- 各章では，節を記述する前に，この章がどのような内容を記述するものであるか説明を簡単にいれる．[NEW]
  - 例: `$ \chapter{章タイトル} 本章では... \section{セクションタイトル}`