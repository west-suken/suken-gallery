---
title: 参照関係を可視化して美しいコードを
date: 2019-09-19 09:52:03
tags: 2019年度
---

Decolony by shundroid

## 概要

　何も考えずにコードを書いていると、スパゲッティが出来上がることはよくあります。コードがどれくらいスパゲッティになっているかを視覚的に表現することで、設計にどれほど忠実になっているか、また外部のライブラリを使う際はその構造などをよく理解することができるはずです。

## デモ

![](https://9e2mla.bn.files.1drv.com/y4mwjwPLBmAF3ZS8LmylAhiWlPJ8l2-ED4E3cH1x3CbfJFHAVRHkfIncLAp8XabElz0LcGBdwhrpCrO0mBJkcHKfHwOM-WVHNd5lTlXS9DjjZ0P3cT_HN1cPNfJ9nt7UhbdNP4r7Xm5vAG7NGBs-14ApuB9fq-K9oBwYtCLIMZbQ-apkNZE5sDMVV1XjqGjAI1ZjirULVXGGm-UT__y254iPw?width=434&height=380&cropmode=none)

　参照関係は見えにくいですが矢印で示されています。包含関係は円の大きさと距離で示されています。参照・被参照関係の多い２つのスコープ間の距離は近くなります。

## コードの説明（ざっくり）

![](https://pu2mla.bn.files.1drv.com/y4m6izWmruwpuD5BHwl2jaPd1lxVxnW_KiySVIPVMnrxe15O86MMpqcf8KApXAkHS3tz84PfvYTRcTLoIq8afpyJvUA4nulKGvnhLePtaK73RBZQeLMDQjZ-V6cIQIllytGXkLSFWgY_JSWN1ZFM6fBh8pjPFUeBZcemCR5S7r4ZRGCuth-GXNh6QZjF2ulUMtsTZNMeSxBa8QPvRnUPJRKRQ?width=526&height=163&cropmode=none)

　コードをデータに変換するのには恥ずかしながらacornというライブラリを使っています。（自作した先輩もいます）そこから参照・定義を抽出し、その後それらを結びつけるためIDを振っていきます。そうして出来上がったJSONをUnityに渡して物理演算させてはい終わり。

## 実用化に向けて

　現在は「参照関係を抽出するコード」自身の参照関係を抽出して、描画しています。すごい対角線論法されそう(小並)。ほかのコードは何で抽出しないのかというとエラーが出るのが怖いのです。なのでまずはそれをやりたい。そのあとは外部ライブラリのrequireの対応や、ES6 importの対応、VueなどaltJSによるファイルとの参照関係に対応させていきたいです。

## バグったけどきれいだったやつ

![](https://9e2ola.bn.files.1drv.com/y4mYJl9N_E7GfkjBN_UJUF_uoG0Kd8mkVnMltb7XnP1kbwpJiajPHC1lk1x3OGfi26gfiTNgmaW2U0XqWVUl1y56xiyLjNi11RecCyjpGvFwElbArx25IVLpsw2IVJ__BdVeQGH02lEdGw4kdsZo-Yg145zMyEdsAtuyhe8tSlCVydDQ3jCrNqyxZbUU1VL7RUejRRiBIYv_DOx-RE0dEfcdw?width=229&height=243&cropmode=none)

