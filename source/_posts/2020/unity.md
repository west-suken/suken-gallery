---
title: Unityによるゲーム制作
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">75期 ［しえーる］</div>

## Unityは便利

　ホッケーゲームを作りました。ホッケーを作るのって入射角とか反射角とか色々とプログラムが大変そう、って思いませんか？　実は制作に１時間かかってないのです。なぜならUnityを使うことで最初からある程度のものが揃っているからです。

　Unityは主にゲーム開発などに利用されます。便利なのが最初からある程度のことができるようになっていることです。どういうことか申しますと、例えば重力などの多くのゲームに共通して使用されているものを数タップで実装可能。Unityには最初からそう言った機能が多く搭載されています。

　プログラミングなど他にも多くの便利な機能があるので本当にUnityは便利です。

　難点といえば、一応プログラミングは不可欠なので少しハードルが高いことと、全て英語で書かれていて少しわかりにくいことですかね。

## 今回やったこと

　先ほど説明した通り、Unityには最初から多くのものが揃っています。そのため、今回のゲームもUnityに最初から搭載されている反射の機能を使うことで、短い時間でゲームを作ることができました。

　今回僕が行ったのは、大まかに言えば

- 最初にホッケーの球を動かす

- 色を付ける

- 反射させるやつを左右に動かすプログラムを組む

　のわずか三つだけ

　Unityを使うことで少ない労力でゲームを作れました。

　一応補足ですが、Unityでちゃんとした素晴らしいゲームを作ることももちろんできますよ。

　需要があるかわかりませんが、プログラミングのコードものせておきます。

```c++
//最初にUnityのプログラムを使うと宣言しています。
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class side : MonoBehaviour
{
    // アップデート内にプログラムを書くと、その内容は1フレームごとに呼び出される
    void Update()
    {
      //もし右矢印が押されたら、z座標に−0.1移動する。
        if(Input.GetKey(KeyCode.RightArrow))
        {
            transform.Translate(0f, 0f, -0.1f);
        }
      //もし左矢印が押されたら、z座標に＋0.1移動する。
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            transform.Translate(0f, 0f, 0.1f);
        }
    }
}
```
　これは反射されるやつのプログラムです。

　他にも最初にたまに力を加えるプログラムもありますが、省きます。

## ゲームの内容紹介

　内容紹介とは言いましたが、ほとんど何も無いゲームなので紹介するものが少ないです。

　皆さんが思い浮かべるホッケーです。反射させるやつは二つあるので、一人で二つ操作して遊んでもいいし、二人で対戦してもいいですね。ゲームの公開方法はよくわからないので調べます。間に合ったら公開しようとは思っていますが、保証はできません。

　操作方法ですが、矢印キーとZ、Xキーを適当に操作してもらえればわかると思います。

　もしかしたら、公開する際に変更を加える可能性もあるので、違ったらすみません。

　では、最後に一応写真を載せておきます。

![](https://dxfyfa.ch.files.1drv.com/y4mg2YfwJQhiy8kLz85VUhNJZbsHuzfy2a6eQpWOJR_ayJEAoykfG1mGbdDtaOs4jIuXegMZkcP1ekGOVVpyh1n60SEG7lfAKwKo58xriiqgFMjwbp_yAgZic_-xvJo8Et_Smd5YYBhEzu84yFxMYUGm5608juFOEfHKWMOs1rYeti70kmFKY5m8WJast3yK1oIsKYLerxJoRnpvdzmttWezg?width=1003&height=551&cropmode=none)