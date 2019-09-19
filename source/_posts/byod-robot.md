---
title: BYODネットワークを活用したロボット遠隔操作
date: 2019-09-19 10:12:15
tags:
---

by shiro-alba, shundroid

## 概要

　都立西高校では昨年夏からWi-Fiが使えるようになりました。数研ではこのネットワークの普及を目指したプロジェクトを行いました。高校の広い範囲でつながることのメリットを生かしたロボットを作りました。

## イメージ

![](https://pu2pla.bn.files.1drv.com/y4mKNRrw-rvwvUxCLrz7RUHBTh86XV9DA5jyJzsYEFoxG69qLMTeQQhS0iQWg8KGgq_3nItX4vjl_w3pj57i1ywLGYCUtJFF3Z15FYxjPHS4HmMoN48pRO61_WKuvL2UEDdVfg8nsYiwplwUXa2uO5BWiY04XjJhYgkdo4FA_Ec2Afsb45Kt0oA68sj0l6qmq_y7buKfRDpO_NuDAuNT09hUg?width=476&height=268&cropmode=none)

　管理棟（職員室、物理室など）側など教室の外は残念ながらネットワークにつながりません。これはどうしてできているかって？それは簡単、これはネットワークを使用していない手動操縦だからです(ひどい)

## 構造

![](https://pu2ila.bn.files.1drv.com/y4m03qeASZEpW8EJrAxJ6dA8xBRAq83B0rL0gtBoPBOM7C5ASL6yzYCcYOWSRgetGldvJrpFK_Y8NSPfQHm-YjqRBb9w7w9OCfdCxAQN4I9t5Wzx0fi2M8ser50_ifC-RbVV1-b-EX3GB6Mm9rt4kW3BPTKh7vvF6tZ1-uZtcDAINg2oXjnHLwGCciTAHjZdCvlgaOH3OiRgba-YxjJ9UGD2w?width=537&height=133&cropmode=none)

## 共同開発

　このプロジェクトの共同開発は他と比べて簡単でした。というのも2人の担当がそれぞれハード・ソフトでくっきりと分かれていたからです。境目はGPIOの信号の送信部分くらいです。互いの仕事がわからないのはちょっと不安ではありましたが…

## 課題

　ハード面・ソフト面ともに課題は残っています。ハード面ではサーボの傾きが左右でちょっと違うことや、前進リクエストを１秒間隔位で送り続けているとだんだん動きが遅くなっていって停止してしまうことがあります。ソフト面では操作の簡略化や、映像をWebRTCで送ることなどです。

## 画像認識を利用したライントレース

　このプロジェクトでもう１つやろうとしていることがあります。それはライントレースです。OpenCVを利用して画像認識をさせてやっているそうです。ただ前日の段階でshiro-albaが相当沼にハマっていたので本番どうなるんでしょう。ドキドキです。こちらも今後は、SSD(Single Shot Multibox Detector)を利用して標識感知をしたりと、自動運転っぽく発展させていきたいそうです。
