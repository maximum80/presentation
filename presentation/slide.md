# はじめてのHTML①
株式会社ギブリー IT研修  
新田章太



### この研修の対象
- 非エンジニア
- 簡単なプログラミングに触れてみたい人


## この研修の最終的なゴール


簡単なWebページをつくれるようになろう


[Web名刺](mycard/index.html)




## 今日学習すること
- 1.HTMLとは?（基本概念）
- 2.実際にみてみよう
- 3.HTMLを書いてみよう



## 1. HTMLとは?


### 1-1. HTMLとは？
HTMLとは、Hyper Text Markup Language（ハイパーテキスト・マークアップ・ランゲージ）


Webページを作るための最も基本的なマークアップ言語のひとつです。


### 1-2. ハイパーテキストって？
ハイパーテキスト（HyperText）とは、ハイパーリンクを埋め込むことができる高機能なテキストです。


ハイパーテキストでは、ウェブページから別のウェブページにリンクをはったり、 ウェブページ内に画像・動画・音声などのデータファイルをリンクで埋め込むことができます。


 つまり、「テキストをハイパーにした」ということです。普通のテキストデータを拡張して色々埋め込めるようにしただけです。


![](http://www.htmq.com/htmlkihon/images/001_01.png)


### 1-3. マークアップって？
「マークアップ」とは、人間語が認識出来ない機械でも文書の構造が認識出来るように、文書の各要素に目印（Markup）を与えて行く事です。


例えば、見出し・段落・表・リストなど、文書の中で各部分が果たしている役割が分かるように目印をつけます。


こうした見出し・段落・表・リストなどの文書内の各部分を **要素（element）** と呼びます。


![](http://www.htmq.com/htmlkihon/images/001_02.png)



## 2. 実際にHTMLの中身をみてみよう
[このリンクを開いてください](mycard/index.html)




# HTMLを書いてみよう



## 1. HTMLの基本構造を作ろう


```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>title</title>
  </head>
  <body>
  </body>
</html>
```



### 1-1. htmlファイルを作る
- 専用のフォルダを作成
- index.htmlというファイルを作成
- 好きなテキストエディタでファイルを開いてください



### 1-2. 宣言

```
<!DOCTYPE html>
<html lang="ja">
</html>
```


#### DOCTYPE宣言
`<!DOCTYPE html>` は、文書がHTML5で作成されたものであることを宣言しており、これは要素ではありません。HTMLはバージョンごとに使用できる要素や属性が厳密に定義されております。


細かいことは覚えず、`<!DOCTYPE html>`はHTML文書を召喚する呪文だと思ってください。


#### html要素
HTML文書のルートを表します。全ての要素はhtml要素の中に記述する必要があります。


#### lang属性
lang属性は要素内で使用されている言語(英語、日本語など)を指定します。「ja」は日本語を意味する値で、html要素内で使われている言語が日本語という意味になります。



### 1-3. HTMLの基本要素の設定


```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>title</title>
  </head>
  <body>
  </body>
</html>
```


#### head要素
HTML文書自体の情報(ヘッダ)を表し、html要素の最初の要素として使用します。


例えばhead要素の中にtitle要素を記述することで、HTML文章のタイトルを設定できます。その他にmeta要素などをヘッダ情報として記載でき、詳細は次に説明します。


head要素は普段はユーザが直接目にすることは少なく、機械(Googleのクローラ)とかが見るうえで必要な要素が多いです。（SEO対策やOGP等）


#### meta要素
文章に関する情報(メタデータ)を表します。メタデータとは「情報についての情報」で、例えば文章のタイトルもメタデータの1つです。


#### title要素
HTML文書の表題を表します。head要素の中でしか使用できず、HTML文書の中に1つしか入れてはいけません。
title要素の内容は、ブラウザのタイトルバーに表示されます。


![](https://s3-ap-northeast-1.amazonaws.com/mash-jp/staging/uploads/3401/8528868d085074d2d1fee5a720343246672dccf5.3498.original.png?1488165254)


#### body要素
文章の内容を記述する領域を表します。body要素の中は、見出し・段落・ハイパーリンクなど、文章の中身を記述します。


![](http://liskul.com/wp-content/uploads/2015/06/e87f5c306eaa3f729d2a5c7362b3e3ac.png)



### 1-4. ドキュメントツリー


#### ドキュメントツリーとは


```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>title</title>
</head>
<body>
</body>
</html>
```


```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>title</title>
  </head>
  <body>
  </body>
</html>
```


HTMLは要素の **入れ子** によって構成されており、これをツリー状に表したものが **ドキュメントツリー** です。


#### 親要素と子要素


![](https://s3-ap-northeast-1.amazonaws.com/mash-jp/staging/uploads/3501/4a2c3f3c7fbefcfdec7ee7e4ae5482c203b3ac01.3501.original.png?1488165258)


ある要素の上位にある要素を**親要素**<br>
下位にある要素を**子要素**と呼びます。


この空白挿入による字下げのことを**インデント**と呼びます。<br>
適切にインデントを利用し、**人に見やすく書くこと**を今後心掛けましょう。


![](https://s3-ap-northeast-1.amazonaws.com/mash-jp/staging/uploads/3501/65609286cc04ece831a844984a6bc9eb80450cf7.3500.original.png?1488165257)


#### TIPS
- 機械は **半角英数字** しかHTMLとして認識できません。
- 全角スペースは機械にとって**ゴキブリ**です。
- 殲滅してください



### 1-5. HTML基本構造　まとめ

#### DOCTYPE宣言
HTMLのバージョン情報を宣言する。
#### html要素
HTML文書のルートを表す。全ての要素はhtml要素の中に記述する。


#### head要素
HTML文書自体の情報(ヘッダ)を表す。html要素の最初の要素として記述する。


#### meta要素
文章に関する情報(メタデータ)を表す。
#### title要素
HTML文書の表題を表す。ブラウザのタイトルバーに要素の内容が表示される。


#### body要素
文章の内容を記述する領域を表す。
