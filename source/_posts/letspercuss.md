---
title: 打楽器練習用アプリを開発してみた
date: 2020-10-3 0:02:25
tags: 2020年度
---

# 打楽器練習用アプリを開発してみた

<div style="text-align: right">74期 ヤート</div>



[TOC]

## 開発のきっかけ

　自分は中学生のとき、吹奏楽部に所属していました。しかし、楽器を吹いたことは一度もありません！　なぜでしょうか？　答えはもうお分かりですね。打楽器パートを担当していたからです。吹奏楽だけでなくオーケストラにも当てはまることですが、一つの楽団の中で打楽器を演奏している人数は管楽器と弦楽器に比べてだいぶ少ないです（まあ多くても困りますが）。それもあってか、市販のメトロノームアプリは管楽器や弦楽器向けのものばかりである、ということに気が付きました。そこで、打楽器奏者が欲している機能だけを詰め込んだオリジナルのウェブアプリをプログラミングしてみました。

## 開発に用いたツール

- コードエディタ：Visual Studio Code
- プログラミング言語：TypeScriptなど
- フレームワーク：Vue.js、Vuetify.js
- バージョン管理システム：Git
- ホスティングサービス：Netlify

## 完成品の紹介

<img src="https://kqdvka.dm.files.1drv.com/y4m2e3ffBOHQGmJr6j6SGTwQ0GrzDB6jAodV2SsUeD5zvaqVykeIsj7Y3of15YTs7mGqbFltSRa1tffXzkqM9kj8U-un3j66Z0vhDmjWy3w7hrTJUS-7M0KOIH4TVpp7i_zElhvF53vGq-sogRvLxH_rlG9N7SChqo36xkoWT4_n63rFqi_CHr1rff6rdQ8yKquajeoDXWJ0VwsWvdKyfDzvA?width=756&height=1650&cropmode=none" style="zoom: 25%;" /><img src="https://iacknq.dm.files.1drv.com/y4ma8edAp6TSfYjDuPJ_WAy-mXp9dj6Jx9xUZNGmldFn6y3YrOUHomg0owM0OjG27rg8dlgi1DDTJ7ovcUxMwtcUk0etmJp74Dn8lCFj81N_C5rS8JjPYY4F-1Yyi8XCea6tmloKmb7L5iJHQu8AWGY3IQoK5IkECQaHO0ssVALHaQ7fZAXqhNaZ5gTbwzH6ZorAyLmU5kvSD08DC89JnZ3mw?width=756&height=1650&cropmode=none" style="zoom:25%;" /><img src="https://kadvka.dm.files.1drv.com/y4mJriYltwEsxEJs1gfM2WEt584Rj5ogCZRZEC_S9K7IVht_zWe5ovmRiUZzLoiSGc-0uZqA4pBIel-ij4ateANqvNQNIDPxEO-ydgGQvuIS8YsZukXRh4drG-F9xxujiUP4grsKhK-QExQFVhnWHOyVqSyvszDv3CRJJn5efE-zdrY77GVohVx8p-OEj3eP8OtVfYIBN5rruEjzUoSBj-hJQ?width=756&height=1650&cropmode=none" style="zoom:25%;" /><img src="https://k6dvka.dm.files.1drv.com/y4mnHbTJiJeHsqfi7kvNAdaxLDGgOYxdlLQPAfL46b3Oa1bdfl6RgLB9EstllzeLPwbEYc2RAoa0ZoBkqh0QOIj2Hwb2g96enR2PwNpm3eHbZsj3QCP0aAkaafwFuybjtD_9JqofAkuIGSrIqoaHJACPbitPChosUHm4xtwp42HWe-ZCFIyxlMnxeVuB58-nGQEjVU5tUqOxelzgSu12ND8og?width=756&height=1650&cropmode=none" style="zoom:25%;" /><img src="https://lqdvka.dm.files.1drv.com/y4msdQ7vBfpmThS-x_u31zI3AeXde-9zrEmz_vDdtb7FW_r4iJXqYRMl3nhXGp0Chccqc90uANixG7G4NVLD7zaZAV9gkAq4k4R5PjCPFbMcwwbJsn0R8QxlQ--UMMMT5H4Tu9RM-tQT4AYOtYPBYYshmYti2Ep4nTbErIpkwwQebzQeUG9OpRJL3NK0T9-12LbQIhJG1VyXXZRnaP7Hdi8Fw?width=756&height=1650&cropmode=none" style="zoom:25%;" /><img src="https://lkdvka.dm.files.1drv.com/y4mTmvuK1SIGECblqe2VGq0dTvMGXPJwEEYY0SLl8vse7B2MzGl4qhfruiPYUFlCj63KkqXxrcK3HV-4eHJw7R-T3XCsOENQNdXCjaXZa7n4JWYg6LXtwYli8RBAxBmJ0FMho9RDIWWl7wPK7b_ysTZMHE1-jVxyBYl_Jk10CR3J9VOoXvF_zQ7sTlr0SW1q1GSwK7lNprvKz-Pt0lXJTNObQ?width=756&height=1650&cropmode=none" style="zoom:25%;" />

　左の画像から1〜6とします。

1. トップ画面
   - URLからアクセスできます。
   - PWAに対応しているため、スマホのブラウザのメニューからホーム画面に追加をすると普通のアプリのように振る舞います。
   - 『Let's! パーカス』というアプリ名は、さあ打楽器を練習しようという気持ちを表した「Let's」と、打楽器すなわちパーカッションの愛称「パーカス」を組み合わせたものです。
2. メトロノーム（シンプルモード）
   - 指定したテンポでクリック音が鳴ります。
   - アナログメトロノームの針の動きを再現しました（説明は後述）。聴覚だけでなく視覚でテンポを把握できます。
   - 「＋」や「ー」のボタンを押すと、テンポを上げたり下げたりできます。普通のメトロノームアプリでは増分が1であるところ、このアプリではアナログメトロノームの一目盛りにしました。これは、打楽器奏者が基礎練習を毎日一目盛りずつテンポを上げて行うからです。
   - 画面上部のメニューをクリックすると、基礎練メニューを選択/追加/削除できます。基礎練ごとにテンポが保存されるので、翌日も同じテンポで練習することができて便利です。
3. メトロノーム（ミラーモード）
   - 普通のメトロノームアプリではこの位置にチューナーモードが内蔵されているものですが、打楽器はチューナーなんてほとんど使わないので機能に入れませんでした。代わりにこのミラーモードを内蔵しています。
   - 鏡になっているので、基礎練習を確認しながら自分のフォームを確認することができます。
   - 赤線は両手のスティック（いわゆるバチ）を同じ高さに上げるための目安にできます。画面をタップすると上下させられます。右手と左手のスティックを振り上げる高さを合わせることは、打楽器入門者が最初にぶつかる壁です...。
4. リズムでフラッシュ
   - リズムの有名な語呂合わせをフラッシュカード式で覚えられるミニゲームです。
   - 楽譜に出てくるリズムはだいたいこの7パターンなので、これらを覚えれば初見の楽譜をすらすら読めます。
5. テンポ当てゲーム
   - 音で流れるテンポを当てるミニゲームです。
   - 出題されるテンポはランダムで全5問。
   - 自分で言うのもなんですが、これなかなか楽しいです。

GitHubリポジトリはこちら。
https://github.com/OTRAY271/lets-percuss

## メトロノームの針の数式

　アナログメトロノームの針の動きは、自作の数式で再現してみました。物理学的に合っているのかは知りませんが、それっぽく見えます。

　時間を$t$(秒)、テンポを$a$(拍/分)とすると、針を動径として鉛直上向きに始線をとったときの一般角$\theta$は定数$k$を使って
$$
\theta = ksin(\frac{a}{60}\pi t)\ \ \ \ \ \ (-k \leqq \theta \leqq k) \
$$
　と表せます。要は周期$\frac{120}{a}$、振幅$k$の正弦波です。三角関数便利〜。