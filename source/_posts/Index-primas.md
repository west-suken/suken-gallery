---
title: 素数を順番に出力するプログラム
date: 2019-09-15 01:50:21-0700
tags: 
cover_index: https://7u0moq.bn.files.1drv.com/y4mQaqN6QFROz1lMnVUfHjAOr_YoySJ6dyTgFk8Fulb-QI_keHruv4Z_3xSnQZ2aF3JQM_RBV98CEp_c7BLSiMlJ73IRInR61Gg0nEbPdPjjVaqbQAAmoauD2qeQnyF1N9tk1sN-apQtyAt8saxDAKK102wd6cJet94kgBGccs4i_E6S2PZ6-dwRs7Lffwu-btxB5syNNok4UBxCWBQOPndQA?width=1300&height=500&cropmode=none
cover_detail: https://7u0moq.bn.files.1drv.com/y4mQaqN6QFROz1lMnVUfHjAOr_YoySJ6dyTgFk8Fulb-QI_keHruv4Z_3xSnQZ2aF3JQM_RBV98CEp_c7BLSiMlJ73IRInR61Gg0nEbPdPjjVaqbQAAmoauD2qeQnyF1N9tk1sN-apQtyAt8saxDAKK102wd6cJet94kgBGccs4i_E6S2PZ6-dwRs7Lffwu-btxB5syNNok4UBxCWBQOPndQA?width=1300&height=500&cropmode=none
---

by さきちゃん (代筆: T@S)

多分これが一番速いと思います

## お詫び
諸事情により、T@Sによる代筆になっています。

## 紹介
本来はJavaを解説しようと計画していたのですが、あまりにも多忙だったので断念して、素数のリストを作るプログラムをJavaで書いて、それを紹介することにしました。  
早速ですが、紹介と解説に移ります。  
…と言いたいところですが、コードを眺めたほうがわかりやすい方もいると思うので、制作の流れを追って追記していこうと思います。  
最初のバージョンと最終バージョンのソースはPastebinを使用して公開します。  

### バージョン1
  <iframe src="https://pastebin.com/embed_iframe/4yBcNCs2" style="border:none;width:100%"></iframe>  <br/>
このプログラムでは、まず最初に2を自明な素数として与え(11-12行目)、3以上の自然数に対して、今までに素数だと判明した数で割った余りを求め(21-32行目)、どれでも割り切れなかった場合にそれを素数とする(26行目)、という処理を行っています。  
さきちゃんのつぶやきによると、while(true)によるループを、条件によりbreakするところが面白いらしいです。 <s>私は基本的にプログラムを書けないのでよくわかりません。</s>  
これ以降、行数は全てこのバージョンに準拠して表記します。後ろに"(insert)"とあるものはその行に挿入し、ないものはその行を置換しています。いつまでこれを続ける気力が残っているか楽しみですね。

### バージョン2
```java
if(primes.get(i) > isPrime / 2)break;
```

(line: 25)  <br/>
$N$が素数かどうか判定するとき、$\frac{N}{2}$以下の素数で割り切れなければ$N$が素数になるのは明らかなので変更。  
計算時間を約半分に短縮することに成功しました。

### バージョン3
```java
double isPsqrt = Math.pow(10 , Math.ceil(Math.floor(Math.log10(isPrime) + 1) / 2));
```

(line: 22(insert))  
```java
primes.get(i) > isPsqrt
```

(line: 25)  <br/>
ある自然数$N$が合成数であるとき、$N$は必ず$\sqrt{N}$以下の素因数を持つ、という事実と、  
$N>0$の時に、

$$
\begin{align*}
  &10^{k-1}<N<10^k\\
  \Leftrightarrow&\sqrt{10^{k-1}}<\sqrt{N}<\sqrt{x^k}\\
  \Leftrightarrow&x^{\frac{k-1}{2}}<\sqrt{N}<x^{\frac{k}{2}}
\end{align*}
$$

が成立することを利用して、$\sqrt{N}$をかなり粗く上から抑えています。<s>実はこれ、私(T@S)のアイデアです。</s>  
この処理によってそれなりに速くなりました。そして、ついでに1箇所に存在していたtypoも修正しました。

#### バージョン3.5
```java
double isPsqrt = Math.pow(10 , (Math.ceil(Math.log10(isPrime)) / 2))
```

(line: 22(insert))  <br/>
切り捨てて1を加える操作を切り上げる操作に変更し、指数部分を切り上げないように変更しました。誤差だと言い切れるほどの速度向上ができました。

### バージョン4
(removed inserted line: 22 from 3.5)
```java
if(primes.get(i) > Math.sqrt(isPrime))break;
```

(line: 25)  <br/>
変なことをせずに素直に`Math.sqrt()`を使って平方根を求めたほうが高速に処理できることが判明しました。  
このあたりから処理時間を計測するようなコードを追加していますが、ここでは割愛します。  
ちなみに、この時点でT@SのPC(そのへんの家電量販店で購入したただのデスクトップPC)では1,000,000個の出力に30分程度かかっています。

### バージョン5
```java
if(isPrime % primes.get(i) == 0){
	flag = false;
	break;
```

(line: 26)  <br/>
どういうわけか小さい数で割り切れても余りを求め続けていたので、T@Sが強引に変更しました。  
微妙に高速化出来ました。

#### バージョン5.5
出力方式をテキスト形式に変更しました。

### バージョン6 (最終)
```java
String message = Arrays.toString(primes.toArray());
message = message.substring(1,message.length()-1);
```

(lines: 34-37)  <br/>
リストを出力する時にやたらと時間がかかっていることが判明したので、素数を格納しているリストをそのまま文字列に変換し、先頭の"["と末尾の"]"を削除するようにしました。  
その結果、T@SのPCでは<strong>10,000,000個</strong>のリストの出力にかかる時間が<strong><font color=crimson>1分弱</font></strong>まで削減されました。  
<s>文字列処理にどんだけ時間食ってんだよ……</s>  

#### 最終版ソースコード
<iframe src="https://pastebin.com/embed_iframe/rhmTHrPx" style="border:none;height:256;width:100%"></iframe>  <br/>

## その後
最終版コードを元に、新しい素数が見つかり次第テキストファイルに追記していくようなプログラムを書いてT@SのPCで放置してみたところ、$2^{31}-1\ {}_{\footnotesize{(=2147483647)}$以下の105,097,565個の素数を全て出力するのにもわずか4時間程度しかかかりませんでした。ただ、こちらはファイルサイズが1GBを超えてしまっているので公開はしません。

## おわりに
このプログラム、実質T@Sとさきちゃんの共同制作物なんですよね。そのおかげで、私もさほど苦労せずにこの記事を(一から)代筆することが出来ました。  
また、せっかくソースコードを公開しているので、どうせなら皆さんにもっと改良していただきたいなぁ、とT@Sが勝手に思っています。改良しても連絡などは不要です。……というより、連絡先を公開するのは流石に気が引けます。  
本当は、各バージョンでの処理時間の比較などもしてみたかったのですが、ちょっと忙しすぎるので割愛させてください。  
ここまで読んでくださり、ありがとうございました。

------

#### 追記
さきちゃんが1年前にとある企画のために作った、N以下の素数をリスト化するJavaのプログラムが奇跡的に残っていたので、それにも処理時間計測コードを仕込んで計算させてみました。  
そちらもバージョンが2つあったので、古い方をα、新しい方をβとして、今回の方からはバージョン2と6を使って、100,000以下の9592個の素数を出力させました。  
かなり雑に計測していたり、1回ずつしか計測していなかったり、色々とツッコミどころはありますが、目安程度にどうぞ。 

|バージョン|α|β|2|6|
|-------|-|-|-|-|
|処理時間(ms)|9561|943|1113|18|

……  
バージョン2がβに負けてますね……  
<s>見なかったことにしておきましょう。</s>  
バージョン6の処理速度が爆速すぎてびっくりです。わずか10,000個程度でもここまで差が出るとは思いませんよね。  
ちなみに、$316<\sqrt{100000}<317$なので、結局316以下の65個の素数しか使っていません。このように、出力する個数を増やせば増やすほど、このプログラムは有利になっていきます。  
例えば、先程のように$2^{31}-1$以下の素数を求めたければ、46,341以下の4,792個の素数を使えば良いことがわかります。  
長くなってきたので追記を終了します。ここまで読んでくださって、本当にありがとうございました。