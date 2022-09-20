---
title: $x^{2m}$のフーリエ級数展開に挑む
date: 2022-09-19 22:05:00
tags: 2022年度
cover_index: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
cover_detail: https://dsm04pap001files.storage.live.com/y4mcKDoFg6vOpq1linjJcaFwAtuia_d2Akkli0fKlN-FdZtq3oWmnInncAqSMvO2Xe27yA8uHdfU-os_O_VAo-ndtsaGf3ytPhKhEt7I8pWxI1qzim_gX1WajAiJMOWCETb9-kgDGHdxBIlDeviCz4FLe9uJNaz5GgCzmxjPKNdWmJ4_L_J-L4hsA7Rn3PPdgTz?width=991&height=379&cropmode=none
---

<div style="text-align: right;">76期　椅子屋本号</div>

## はじめに

　まず、お詫びしたいことがある。新歓の数研の部誌で、複素関数の発展的な内容を話そうと宣言したのだが、まだ自分自身の、他の数学の課題が残っているので留数定理の初歩しか扱えていない。そのため、今回は別の話をする。書き始め当初はいろいろな関数をフーリエ級数展開して、三角関数の無限に続く美しい連なりをグラフで表現しようか、と考えていたのだが、色々進めていくうちに、より興味深いテーマを発見したので、題名のように、$x^{2m}$のフーリエ級数展開を行う、ということを最終目標にこの部誌を書き進めていきたい。（他団体の部誌や冊子にも僕の同位体がいくつか紛れ込んでいるので、そちらも是非。）

## フーリエ級数展開の定義

～フーリエ級数展開が可能な条件と、定義（参考書によって若干のズレがあるらしい）～

　$f(x)$が、周期$2L$で、有界変動（絶対可積分）で、$f(x)＝\frac{f(x-0)+f(x+0)}{2}$、区分的になめらかであるとき（わかりやすく言えば、その関数がなめらかであり、飛び飛びの値があった時に、その中点に点があるとき）、
$$
f(x)=\frac{a_0}{2}+\sum_{n=1}^\infty a_n\cos{\frac{n{\pi}x}{L}}+b_n\sin{\frac{n{\pi}x}{L}}
$$ただし、
$$
a_0=\frac{1}{L}\int_{-L}^{L}f(x)dx,$$$$a_n=\frac{1}{L}\int_{-L}^{L}f(x) \cos{\frac{n{\pi}x}{L}}dx,b_n=\frac{1}{L}\int_ {-L}^{L}f(x) \sin{\frac{n{\pi}x}{L}}dx
$$定義だけ突き出すのも不親切だと思うので、フーリエ級数展開におけるフーリエ係数($a_n,b_n$)の値を簡単に導出して、この式の正当性を確かめよう。

## 係数の導出

　導出にあたり、三角関数の直行性について予め認知してほしい。（計算が楽になる）
〜三角関数の直行性〜
$$m,n\in\mathbb{N}$$$$\int_{-L}^{L}\sin{mx}\cos{nx}dx=0$$\begin{align}\int_{-L}^{L}\sin{mx}\sin{nx}dx=\begin{cases}\pi\quad (\text{if}\quad n=m)\newline
0\quad (\text{if}\quad n\neq{m})\end{cases}\end{align}\begin{align}\int_{-L}^{L}\sin{mx}\sin{nx}dx=\begin{cases}\pi\quad (\text{if}\quad n=m)\newline
0\quad (\text{if}\quad n\neq{m})\end{cases}\end{align}積分の基礎的な素養が必要だが計算すればこれらは容易に導き出せる。ちなみに、関数の内積が$\int_{-\pi}^{\pi}f(x)g(x)dx$で定義されているため、これらは内積が$0$になっていることから、「三角関数の直行性」と呼ばれている。さらにちなみに、関数の内積はそれらの関数を無限次元ベクトルの集まりと見なすことで、直感的に理解できる。さて、私たちが求めたいものは、以下の式の$a_n,b_n$の値であった。
$$
f(x)=\frac{a_0}{2}+\sum_{n=1}^{\infty}a_n\cos{n\pi}+b_n\sin{n\pi}…(*)
$$

まず(*)の両辺に$\cos mx$をかけて$-\pi$から$\pi$まで積分すると、三角関数の直行性より、$m≠n$の時右側の級数は全て$0$になる。$m=n$の時は$\cos$だけが残り、その積分値は$π$。$a_0$の部分も明らかに$0$。よって
\begin{align}
\int_{-\pi}^{\pi}f(x)\cos{nx}dx=a_n\pi\newline
(\text{結局}n=m\text{の時を考えるので、左辺の}\cos\text{はこれで良い})\newline
\therefore a_n=\frac{1}{\pi} \int_{-\pi}^{\pi}f(x)\cos{nx}dx
\end{align}

次に(*)の両辺に$\sin{mx}$をかけて$-\pi$から$\pi$まで積分すると、上と同様、
$$
\int_{-\pi}^{\pi}f(x)\sin{nx}dx=b_n\pi$$$$\therefore b_n=\frac{1}{\pi} \int_{-\pi}^{\pi}f(x)\sin{nx}dx$$最後に、両辺を$-\pi$から$\pi$まで積分すると、
$$
\int_{-\pi}^{\pi}f(x)dx＝\pi a_0
$$$$\therefore a_0=\frac{1}{\pi} \int_{-\pi}^{\pi}f(x)dx$$これは見事に$a_n$における$n＝0$の値である（見事というか、そうだから初めから$a_0$とおいていた。）

　ここで出た$a_n,b_n$の値は周期が$2\pi$の周期関数におけるフーリエ係数である。よって、周期$2L$の周期関数においても適用できるように、$\pi$を$L$に置き換え、三角関数の周期を$\frac{L}{\pi}$倍するため、引数（中身）を$\frac{\pi}{L}$倍すると、一番初めに提示した式が出てくる。さあ、いよいよフーリエ級数展開を実行してみよう。

## 具体例

### のこぎり波

　まず、始めに、有名な、「のこぎり波」というグラフをフーリエ級数展開してみよう。

　のこぎり波というのは、このような関数である。（$x＝0$を挟んだ$-\pi <x<\pi$の範囲のみ示す。実際は無限にこれを繰り返す。）
\begin{align}
f(x)=\begin{cases}x\quad (\text{if}\quad -\pi<{x}<\pi)\newline
0\quad (\text{if}\quad x=\pm \pi)
\end{cases}
\end{align}この関数は周期$2\pi$であるので、
\begin{align}
a_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x\cos{x}dx\newline
&=\frac{1}{\pi}\left\lbrace\frac{1}{n}[x\sin{nx}]^\pi_{-\pi}-\frac{1}{n}\int_{-\pi}^{\pi}\sin{nx}dx\right\rbrace\newline
&=0
\end{align}\begin{align}
b_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x\sin{x}dx\newline
&=\frac{1}{\pi}\left\lbrace\frac{1}{n}[-x\cos{nx}]^\pi_{-\pi}-\frac{1}{n}\int_{-\pi}^{\pi}-\cos{nx}dx\right\rbrace\newline
&=\frac{1}{n\pi}\left\lbrace-\pi(-1)^n-\pi(-1)^n+\frac{1}{n^2}[\sin{nx}]^\pi_{-\pi}\right\rbrace\newline
&=\frac{2(-1)^{n+1}}{n}
\end{align}$$
f(x)=\sum_{n=1}^{\infty} \frac{2(-1)^{n+1}}{n}\sin{nx}=2\sin x-\sin{2x}+\frac{2}{3}\sin3x\cdots
$$では、フーリエ級数展開がもとまったところで、この展開の、元のグラフに対する近付き方をみてみよう。

![](https://dsm04pap001files.storage.live.com/y4mY3e0pDVMVc65PxDUeLIr6v9LKujyX5MgEHc6Cq3lGzoQmYNVknbOQcEXUApjs1j6GwcVxudaDjFAjIbpCw8vohaF-m5TKtpJ_ACwH0v1xKg0XdM1lga_DPI5W6Qs0D9JJtKk2IEgxGeICBw03zUQnDn_3Iu7I3lo58yT1k217ujo64Qg4qo3AzIUXgK-ASKo?width=1024&height=563&cropmode=none)

こんな感じ。美しくない？

　ちなみに私は一定期間この画像をLINEのアイコンにしていた。（多分結構の人にひかれた)

## $x^2$とあの有名問題

　次に、先ほどのこぎり波の応用として、$x^2$の関数をフーリエ級数展開してみることにした。これはただの興味からで、この結果が驚くべきものになろうとは、計算を始めた時は知る由もなかった。
\begin{align}
a_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x^2\cos{nx}dx\newline
&=\frac{1}{n\pi}\left\lbrace[x^2\sin{nx}]^\pi_{-\pi}-\int_{-\pi}^{\pi}2\sin{nx}dx\right\rbrace\newline
&=-\frac{1}{n^2\pi}\left\lbrace[2x(-\cos{nx})]^\pi_{-\pi}+2\int_{-\pi}^{\pi}\cos{nx}dx\right\rbrace\newline
&=-\frac{1}{n^2\pi}\left\lbrace2\pi(-(-1)^n)+ 2\pi(-(-1)^n)+\frac{2}{n}[\sin{nx}]^\pi_{-\pi}\right\rbrace\newline
&=\frac{4}{n^2}(-1)^n
\end{align}$$
a_0=\frac{1}{\pi}\int_{-\pi}^{\pi}x^2dx=\frac{2}{3}{\pi}^2
$$\begin{align}
b_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x^2\sin{nx}dx\newline
&=\frac{1}{n\pi}\left\lbrace[x^2(-\cos{nx})]^\pi_{-\pi}-\int_{\pi}^{\pi}2x(-\cos{nx}dx)\right\rbrace\newline
&=\frac{1}{n\pi}\left[{\pi}^2(1(-1)^n)-(-\pi)^2(-(-1)^n)-\left\lbrace\frac{1}{n}[2x(-\sin{nx})]^\pi_{-\pi}-2\int_{-\pi}^{\pi}(-\sin{nx})dx\right\rbrace\right]\newline
&=\frac{2}{n^2\pi}[\cos{nx}]^\pi_{-\pi}\newline
&=0
\end{align}以上より
$$
f(x)=\frac{1}{2}\frac{2}{3}{\pi}^2+\sum_{n=1}^{\infty}\frac{4}{n^2}(-1)^n\cos{nx}=\frac{1}{3}{n^2}+4\sum_{n=a}^{\infty}\frac{1}{n^2}(-1)^n\cos{nx}
$$　さあ、これで$x^2$のフーリエ級数展開がもとまった。何か感じるものはないだろうか。この式に、$x=\pi$を代入してみよう。$f(x)$の定義より、
\begin{align}
\pi^2&=\frac{1}{3} {\pi}^2+4\sum_{n=1}^{\infty}\frac{1}{n^2}(-1)^n\cos{n\pi}\newline
&=\frac{1}{3} {\pi}^2+4\sum_{n=1}^{\infty}\frac{1}{n^2}(-1)^n(-1)^n\newline
&=\frac{1}{3}{\pi}^2+4\sum_{n=1}^{\infty}\frac{1}{n^2}
\end{align}　もう気づく人が多いだろう。そう、$x^2$のフーリエ級数展開はバーゼル問題につながっていたのだ。
上の式を整理して、
$$
\sum_{n=1}^{\infty}\frac{1}{n^2}=\frac{\pi^2}{6}
$$　自分でこの値を出すことができた瞬間はもはや感動もの。

## $x^{2m}$とあの関数

　さあ、私はここから無謀にも、$x^p$のフーリエ級数展開に試みた。しかし、$p$が正偶数の時に限る。というのも、$x^2$のフーリエ級数展開から、$p$を正の偶数とするとある関数とつながるという、僕の直感と、計算結果との整合性に因る。
$$
a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}x^p\cos{nx}dx=\frac{2}{\pi}\int_{0}^{\pi}x^p\cos{nx}dx
$$ここで、$I_k= \int_{0}^{\pi}x^{p-k}\cos{nx}dx $と置く。
\begin{align}
I_0&=\frac{1}{n}\left\lbrace[x^p\sin{nx}]^\pi_0-\int_0^\pi px^{p-1}\sin{nx}dx\right\rbrace\newline
&=-\frac{p}{n}\int_0^\pi x^{p-1}\sin{nx}dx\newline
&=-\frac{p}{n^2}\left\lbrace[x^{p-1}(-\cos{nx})]^\pi_0+\int_0^\pi (p-1)x^{p-2}\cos{nx}dx\right\rbrace\newline
&=-\frac{p}{n^2}\left\lbrace-(\pi)^{p-1}(-1)^n+\int_0^\pi (p-1)x^{p-2}\cos{nx}dx\right\rbrace\newline
&=\frac{p}{n^2}{\pi}^{p-1}(-1)^n-\frac{p(p-1)}{n^2} \int_0^\pi x^{p-2}\cos{nx}dx(=I_2)
\end{align}
ここで、$I_n$の形が再び現れていることに気づく。$\int_{0}^{\pi}x^p\cos{nx}dx $と$\int_{0}^{\pi} x^{p-2}\cos{nx}dx $を見比べてほしい。$p$が$pー2$に変わっているだけだ。以後同様の操作をすれば、この形が繰り返し現れてくることが帰納的に判明する。すなわち、
$$
I_2=\frac{p-2}{n^2}{\pi}^{p-3}(-1)^n-\frac{(p-2)(p-3)}{n^2}I_4
$$これを繰り返し、次々に代入していくと次のような級数が現れる。（この時pは十分大きな偶数であるとする。）
$$
I_0=\frac{p}{n^2}{\pi}^{p-1}(-1)^n-\frac{p(p-1)(p-2)}{n^4}{\pi}^{p-3}(-1)^n+\frac{p(p-1)(p-2)(p-3)(p-4)}{n^6}{\pi}^{p-5}(-1)^n-\cdots
$$しかし、実際は、$p$が正の偶数であることから、この級数は有限(なぜなら、部分積分がいつか途切れるから)。ゆえに、$k=p$の時、すなわち$I_p$の値を計算する必要がある。
$$
I_p=\int_0^\pi\cos{nx}dx=\frac{1}{n}[\sin{nx}]^\pi_0=0
$$よって、計算するのは$I_{p-2}$までで良い。

　すると、先ほどの級数をこのようにまとめることができる。（なんでこうなるんだよ！っていう人は、代入して展開してみてください）
$$
I_0=\sum_{k=0}^{\frac{p-2}{2}}\frac{p!(\pi)^{p-2k-1}(-1)^k(-1)^n}{(p-2k-1)!n^{2k+2}}
$$また、
$$
a_0=\int_{-\pi}^{\pi}x^pdx=\frac{2}{p+1}{\pi}^{p+1}
$$これと、上記の、$a_n$の式に$I_0$を代入した、
$$
a_n=\frac{2}{\pi} \sum_{k=0}^{\frac{p-2}{2}}\frac{p!(\pi)^{p-2k-1}(-1)^k(-1)^n}{(p-2k-1)!n^{2k+2}}
$$さらに$f(x)$は偶関数であることから、$b_n$は$0$であるので、
$$
f(x)=x^p(-\pi \leqq x \leqq \pi)=\frac{\pi^p}{p+1}+\frac{2}{\pi}\sum_{n=1}^{\infty}\sum_{k=0}^{\frac{p-2}{2}}\frac{p!(\pi)^{p-2k-1}(-1)^k(-1)^n}{(p-2k-1)!n^{2k+2}}\cos{nx}
$$を得る。

　さあ、もう少しこの数式の嵐に耐えて私に付き合ってほしい。この式に$\pi$を代入すると、$\cos{n\pi}=(-1)^n$より、
$$
\pi^p=\frac{\pi^p}{p+1}+\frac{2}{\pi}\sum_{n=1}^{\infty}\sum_{k=0}^{\frac{p-2}{2}}\frac{p!(\pi)^{p-2k-1}(-1)^k}{(p-2k-1)!n^{2k+2}}
$$美しく見せるために、$p=2m$（$m\in\mathbb{N} $）と置換し、
$$
\pi^{2m}=\frac{\pi^{2m}}{2m+1}+ \frac{2}{\pi}\sum_{n=1}^{\infty} \sum_{k=0}^{m-1}\frac{(2m)!(\pi)^{2m-2k-1}(-1)^k}{(2m-2k-1)!n^{2k+2}}
$$　さらに、リーマンゼータ関数を用いて、$n$を消去することができる。（リーマン予想に関わる重要な関数です。素数に興味がある中学生はリーマン予想について調べてみてね、いやというかここまで読んだ中学生すごすぎ）
〜リーマンゼータ関数とは（定義だけ）〜 $s\in\mathbb{C}$の時、
$$
\zeta(s)=\sum_{n=1}^{\infty}\frac{1}{n^s}
$$よって、
$$
\pi^{2m}=\frac{2m+1}{m\pi} \sum_{k=0}^{m-1}\frac{(2m)!(\pi)^{2m-2k-1}(-1)^k}{(2m-2k+1)!}\zeta(2k+2)
$$　なぜリーマンゼータ関数を用いて表したのかというと、この式を用いれば、（計算量はされど）次々に$\zeta(2m)$の値が求まるからである。具体的に、$m=1$を代入すれば、上記の値になるし、それを用いれば$m=2$の値も求まる。最も、ベルヌーイ数というとても強力な武器を今の数学は有しているのだが。（語るな、という声が外野から飛んできているのが聞こえます）

## 終わりに

　まず。この問題の相談にのってくれた数学科K先生、協力して考えてくれた友人のH君、私のこの部誌の苦労話を興味津々で聞いてくれた友人のT君、そしていつも数研を支えてくれている会長と会計担当者、顧問の先生、その他この問題を解くにあたって僕を支えてくれた人たちにこの場を借りて感謝申し上げたい。

　私にとっては、今まで取り組んだ問題の中で最も計算量が多い問題だったため、色々なことをこなしながら、何週間も計算ミスをし、それを修正し、という作業を繰り返した。途中自分の能力のなさに呆然とし、諦めかけたが、幸運にも目標の結論を導くことができ、検算によってある程度の有効性を確かめることができた。答えが出た時は、叫び出しそうになったが、すんでのところで理性がそれを制御した。本当は有識者に校正を頼みたいのだが、今（9月6日）は実力テストの直後で、数学の先生方も忙しいようなので、頼むことも申し訳ないし、この話題を理解をもって共有できる友人は数人しかいないので、中々難しく、厳密性に欠けた文章及び論理展開になってしまったことはご了承願いたい。何せ今の時刻が11時なので、とても眠いので、まだまだ語りたいところだが、期限も迫っており自分で誤字等を修正する必要があるので、この辺で失礼したい。それではまた、いつかどこかで。

※なんかうちの部誌で名言集を載せてた友人がいたので僕も1つ。

$$
\textbf{整数は神が作った。それ以外は、人間が作った。　〜クロネッカー〜}
$$