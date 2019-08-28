---
title: CGの作り方 ～Blenderの基本事項～
date: 2019-08-27 14:28:25
tags:
---

卑弥呼だよ！☆（ゝω・）v ｷｬﾋﾟ

## はじめに

初めまして。こんにちは。**Himiko** と申します。**卑弥呼が大好き** な７４期生
です。趣味は **CG 制作** です。以後お見知りおきを。

さて、今回は初めての部誌ということで、**CG 制作の流れ** を説明しましょう。
幸いなことに(？)CG を作るのを趣味とする者が数研では筆者しかいないようなの で、詳しくお伝えしようと思います。

## CG とは？
省略したい。が、そういうわけにもいかないので。コピペで。

> CG
> コンピュータ を使用して描かれた画像や図形のこと。または、それらを作成する技術のこ と。グラフィックスソフトを使用して、本物そっくりの 2 次元や 3 次元のコンピューターグラ フィックスを作成できる。

出典 ASCII.jp デジタル用語辞典 ASCII.jp デジタル用語辞典について

CG は「**Computer Graphics** 」(コンピューターグラフィックス)の略称です。 「Consul General」でも「Consultative Group」でもありません。お間違いないよ うに。ちなみに本稿で時々現れる３D モデルという言葉は、CG と等しいと思って いてください。

皆さんご存じの通り CG とは、**何らかの立体的な映像や画像をコンピュータで作り出すこと、そして作り出したもの** です。対象が現実に存在すればより写実的に、 存在しない想像上のものであれば現実に存在するかのように立体的にデザインする、 ということが真理だと筆者は思っています。

## ソフトについて
CG はコンピュータで、ダウンロードしたソフトを用いて作ります。筆者が普段 使っているのは、「**Blender**」というものです。このソフトは**無料**ですが、かなり**本格的**に CG を作ることができます。モデリングはもちろんのこと、それを静止画に する「**レンダリング**」や**アニメーション**、**映像のノンリニア編集**や**エフェクト適用**まで、これ１つでできるのです。
このソフトのさらに凄いところは、**様々な質感**や、**光の屈折**を**写実的**に表現できるという点です。ゴムのような柔らかさや、ガラスのような透明感や、コンクリー トのような重さを、幾度かのクリックのみでそこにあるかのように、映し出せるの です。しかも、物理性質に準じた光線の追跡を行いリアルな光の表現も可能です。 **有料の商用ソフト**にも全く劣らないため、初心者からプロまで使用しています。

しかし、操作性について一部のユーザーの間では、初心者には向かない…、無駄 な機能が多くてわかりづらい…と評価されているようです。ですが、アップデート により画面が見やすくなり、操作方法は一貫しているため昔よりかなり使いやすく なっていると感じます。*とにかくこのソフトウェアは無料の割に高性能なので、興 味があれば是非ともダウンロードしてほしいです！*

https://www.blender.org/

開くとこんな感じ↓
![](https://pe32qg.bn.files.1drv.com/y4mAUPlAsLhgV0qo6zZxwbCYs-e0ue8ueT3oFfun13HIC8RAqptt0uParfyYPCpsUVIViUqM5aWLfM3asYkar9rdc_JQwFe3uSW_H7DGHo9ow3WICjqfb4xCDdXGDVDSSEpQ364AYyJSJLwsBuro9tKca4TNGxA301egabkw_128OhJpUStZBAfX4UnEM9WiBx6qul-2HDjFGc7Yp3jVlw0jg?width=1024&height=632&cropmode=none)

## CG 制作の流れ
それでは早速本題に入っていきましょう。CG 制作の工程は大まかに以下のような感じです。

1. デザイン…アイデアを考える
2. モデリング…形を作る
3. マテリアル…色や質感を設定する
4. カメラ…構図を決める
5. ライティング…光源を設置
6. レンダリング…コンピュータに計算させ仕上げる
7. 保存…完成

と、言われても意味がわからないと思うのでスクリーンショットを使ってお伝えし ましょう。

### ①デザイン

まず、アイデアを頭の中に思い浮かべます。紙に描きだしてもいいです。

### ②モデリング

早速形を作っていきます。Blender で始めにすることは、簡単な図形を画面に出 すことです。正方形や球体、錐体等の簡単な形を組み合わせたり、面に凹凸をつけ たりして複雑な形が生み出せるのです。
![](https://pe33qg.bn.files.1drv.com/y4mFTp0uB6Mk2QFTu_Z0XizpXtt-qhdXlCShwMff8jJntfoXAgl2zQlLZe1YpfaWeqXB1KK3e62rABKnGH9rNWXgt8X3jO_qfz22Gik4n1mslZkUOfoE0tM5_0mFIWVDZ8ox6MRjsoT4U2DXf7gM0nb37_yQa4qE3vOiGrmRhA4Bdqw5iwx6iKnSV5OobZMw-qQNqO7Xo5qxQjlIXQNnG7zYg?width=919&height=609&cropmode=none)
そのもととなる単純な形も色々な種類があります。上の図は主に使用するもので、１は立方体、 ２は円柱、３は平面 の円、４はトーラス (トポロジーの研究 やドーナツ作りに よく使われる)、５は 球体、６は正二十面 体、７は円錐、８は 平面の正方形ですが、9 番はこの中で異彩を放つ…サルです。いや、Blender の公 式キャラクター、サルのスザンヌといいます(名前もついています)。これは、サル をモデリングしたい、サルの CG を作りたい人はもちろん、どんなキャラクターを 作るか迷う制作者たちがとりあえず使ったり、練習に使ったりするものです。この スザンヌを改造(髪を生やしたり胴体をつけて猿人を作ったり)して遊ぶ人もいます。

**まとめると、簡単な形を組み合わせて変形させることで、CG は作られるのです。**

### ③マテリアル

マテリアルとは、英語で material、材質のこと。主にどんな材質を表現できるか、 先ほど紹介した中の球体を使って説明しましょう。 質感にも色々ありますが、特によく使うのは以下の 3 つです。

#### １、ディフューズ BSDF

![](https://pe3wqg.bn.files.1drv.com/y4mc-qSdP6LNMEL9qFAGq7t02ZfQPRlnA4kPrFQclAJ0Xg-TEBzO5ycW9S4ruhGnDUDuruJtgntbBUwylKOq_fosaM416wHJwPlE2_MYRiOZ-ai9EIlqhpJbD1m69L1BProG7fJW6SNZviOoapdv_boLalcfP4t0IrXPMeHYZedU4SHnUDn1y7hiOvjXzwWpW46JesJtdTIu70Q1iuEh7L9Pw?width=660&height=371&cropmode=none)

→表面の粗い、つやのな いマテリアル

#### ２、光沢 BSDF 

![](https://pe3xqg.bn.files.1drv.com/y4mJ7LGObEJY9UhMvAbm14CuSONWf4owosU4IujqcufvrjX9_6Rdseq1PQxEjD55mRyJQzVmyI7JEgblFio8XUD_F60Copw_luqlfVQPxxTVIBieQCDhraR5mD0iEKVzY2ZtPkreB1W-oW3enxoKY3NrmK0U2zO2t_6JEnn3DCrIQ-VTNPzt2uqLIvXJywszn6iNL0VTPcR3vMLH-yATOVxpQ?width=660&height=371&cropmode=none)

→金属反射 

#### ３、グラス BSDF 

![](https://7u34qg.bn.files.1drv.com/y4mAajzQr-TKZt-Is20VqoVm91bf7kSwMskYcnstdWkEPN93EzuVAPW8jyk5hRQs4RdYdY-pq78xqUpkZacPzM8MEhpg6rTlGxD-iLWoiTcKXmSEdg4D0a3irxImeGeF2tou969MMPFCHkCXeUcPHzA6KpzI-pL70N7Zm8ZRbhiVPGe-VHiX6pSwTRpBh8nfI6EUURbZyb8jqVh3MIu4TG1Sw?width=660&height=371&cropmode=none)

→ガラスや水、ダイヤモンドを表現する透明マ テリアル 

他にも、起毛素材の独特な質感を出す「ベルベット BSDF」や、牛乳や陶器、人 の肌などの半透明感を出す「サブサーフェイス・スキャタリング」というマテリア ルもあります。

### ④カメラ

カメラの位置を決めるということはつまり、モデリングしたものをどこから映すかを決めるということです。

![](https://7u35qg.bn.files.1drv.com/y4mus13ASTrAcsvnq51lJpLw8RJ2fXye_Ek_ps_3enRvjVXW3E7IdIa2dYFU7dG7frm5vH4v4SWWHUkjd0LtmWl5FIwyVc18MJHg27V4wtbygJljpvMSI6vpfmpqJ3hocZ5_9kTwV5LBGOSMeSn_PxwH8kv1ozel0kpE32e6d7iZ9NYLT40mjFWWOgQfdfdBKSgjTaU_LhtnUFHc2H-I0Q9vg?width=660&height=401&cropmode=none)

→オレンジ色になっているのがカメラのオブジェクト。
→上の画像のよう な見方を 3D ビュ ーというのに対し、 下の画像のような 見方をカメラビュ ーといいます。 カメラビューの、オ レンジの枠内が、 最終的に映し出さ れる部分です。

![](https://7u36qg.bn.files.1drv.com/y4mHpXmiG2gmTIpoXstlC0tlS3CR0gI5xNZ_tBeOE7e67kIWWUek3lCfr1C5R3Gj1jsWH3iVq3eJrTHcbgGm8hu3V1hyr_aCTEo6pf8HFks3SyxtCzF2QaaY-qiVjLt8liN_xfxjxqLZxHlnL0x91bj6GpanCvaE6zG5a1pHJ9DT5UI7oe4E-By-LnnJHLYnDateu68hw4fAa5sYUBWTTv-UQ?width=660&height=443&cropmode=none)

カメラビューを見ながら、オブジェクトの配置を決めます。

### ⑤ライティング

writing ではなく lighting ですよ。光の種類や当て方を決める工程です。 CG 制作において、光源は必要不可欠なものです。もし光源が無かったら。。。

![](https://7u37qg.bn.files.1drv.com/y4mkbaSkJCyOxIORAgFNSQ68wrNdLAqF3NeubTc0uzcyIWmnAIqGI1UT-Ij6Vf0ZtMpdkobyZYqqZ7jcZHh_Nzp6BmSIQTv4K-g46HD-Ut1_e033Ix0Xho4ROZ5BfqZD2yXv_Z_5h0iI5CUiAa6cqZtPCZ-0I73qLimoJivh03zw2M0syU0DmlWaK90hZI9leR4fqqQzrN9_gYBePUSdHYe8A?width=256&height=144&cropmode=none)

上のように暗くなってしまいます。だから光を当てなければなりません。ライト (Blender ではランプと呼ぶ)にも、マテリアルと同様にいくつか種類があります。 よく使うのは、以下の 3 つです。

#### １、ポイント

![](https://7u30qg.bn.files.1drv.com/y4m2ywy88PmMLQBRIwdOL8n9ZCqORZ-YZ-mcpNPoASOX6KllnGFLRlKhubRJgcVvdNYEg1qeRiAKRgK_l63jds3FIcMWS7AQngmKpzgPkqPhX-zn4F1zETSXonOFZ3QsVIZP9PbQqM3PjBcTonOPcvTq6KTltTrZSUqcnDL4EV9QyV9fBRSgaJ1sU1VsaTtpPXzSGhrpKXhxZ2SlKGkzl-nSA?width=256&height=143&cropmode=none)

→光源の位置から全体に広がるように照らす。

#### ２、サン

![](https://7u31qg.bn.files.1drv.com/y4msxg0NI6ncGaDju26QnRLIYTUAB8PSLPo6r8phzcBjVqRjoOrw88hkDRdH2-EoIyOA-qJiwhDqB6M23TRCJirJOcpnlIlO6DgdTWpKwB9WmVmk_Dn5w_f-p1kIQpTbZBTDcMY7kOcRTOE97P_CTbgQVW_sD6NH8TPfHCO9SrixU1Qc_C9Hp3Neew4GxFviGNFIdcuBCIdUGU_R6_38OZ7Ww?width=256&height=144&cropmode=none)

→平行に照らす、太陽光。

#### ３、スポットライト

![](https://7u32qg.bn.files.1drv.com/y4mcYff8tA6MyrniSE7yVR2QfCS0HPcCgSlGCGEp-4rkKvSlZXxVvhn-xdkBNQQ3FxBCb8EGcAdsVXpWfFJKkGcWWH94wHJ-n-Lec1MLX4I6Zbdy2ynBqf03hHbjqcm4oYds351y5lZCFB1KB4dqgg45sxP1dx8oGAOYaOiBIY7Ki3BHW_S9vWIJXxq8P0eMkbv-fMo9AWN79QSqBJsfojUTg?width=256&height=143&cropmode=none)

→スポットライトの光を再現で きる。光に色を付けることも可能。

他にも、オブジェクト(物体自体)を光源にすることもできます。

### ⑥レンダリング

![](https://7u33qg.bn.files.1drv.com/y4m2wwQRMKXgp7ILPt5rwY0c-qEmVCCfgJPrHeLipIl4lMCLkThOSOO3uKdexvbHE8cjw4GyW5MZN_C1XyJFteX24eCCRJQ8aMrnc1RLGTwQqDn8dFrO5Sqh9iIAR2Ej9CbRUdi77l-AV_iX_ZgSKufCt-kJHn8vEfoLt4OUrMorWnJf0g8lCayFM3kq0aH4f4yBHujGKbBc2aG8g4rfMLmwA?width=660&height=410&cropmode=none)

設定どおりに画像を出力するのがこの工程です。
→解像度を高く設定するほど、レンダリングに時間がかかります。

３Dアニメーションを制作する時は、1コマずつレンダリングするのでさらに時間 がかかります。

### ⑦保存

保存したら完成です。PNG 形式、JPEG 形式、BMP 形式などで画像として保存 できます。 ここまでで、モデリングからレンダリングまでの基本的な流れや、Blender の機 能を紹介しました。
作ったCG は、SNSのアイコンや印刷してステッカーなどにすることができます。 また、 Blender 愛好者の掲示板サイトなどに作ったものを投稿することもできます。

## さいごに

最後まで読んでいただきありがとうございました。本稿についてお気づきの点や質問がございましたら、作成者・Himiko まで。では、Blenderを使用して作られたものを載せておきます。

３Dアーティスト・Pierrick Picaut 氏の作品

![](https://7u3wqg.bn.files.1drv.com/y4mXyJtkOsG4nhcPqAdEs5Whc6-pNVF7ZEu__KGJHGevVyefOaIm4qNOIqGsgVYoCW7i-9_brUIpouLqVTCF8jvHOErnt3QAKm80w3jzgFq4aN0Gc51zvXJctejwa73300FcXT8zpz_ff6iwiuW1H46RAs1TQEUOdPrtno0DFQfIaBAkoCGVs3HD8uBBy7dOCCU5YCmSJY2Mf8I4xdy3BCTig?width=448&height=660&cropmode=none)

![](https://7u3xqg.bn.files.1drv.com/y4mlzmrnN65stXwPiKIe0aJY3xJang3u1J8IBTmGt3vhCicmov_vRLx7z1XLp8wjuymJSbZeXi357Fk-ZlcyGOQh43Jag7H8I4GYvdE-G-e46j2xuYzNCTbesMAifEnS-7BG3n0ZCk8MjGVjqWFBx519XQcvCI7J9r-9I8TW2GdcvVyveVaUWIdl3br0P3LJMC1BH6SjSdiPeZqPgFbc7uXyw?width=604&height=604&cropmode=none)
