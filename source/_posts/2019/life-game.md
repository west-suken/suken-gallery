---
title: ライフ・ゲーム
date: 2019-08-29 21:51:31
tags: 2019年度
cover_index: https://pe0foq.bn.files.1drv.com/y4mi1siwIzefpZbFTo7fkECjD9rd8KRHQH-G_7IgpmAFLQFGAbAP49HRszj65Th5DIROsPmFvFcUoeDNU0gpKqVJlqCMijG5rOAAjELDyEr_Mt_970nPjLg_-I8-YTQ7a2u_f0FLXy0Ds9_Q5HWpu6OtptJEIQateGKBIxpN5JDAjkky8WcjmlpJPeeEEq2OHDrOVKCIOvQ_YshsDYzH9WCxg?width=660&height=254&cropmode=none
cover_detail: https://pe0foq.bn.files.1drv.com/y4mi1siwIzefpZbFTo7fkECjD9rd8KRHQH-G_7IgpmAFLQFGAbAP49HRszj65Th5DIROsPmFvFcUoeDNU0gpKqVJlqCMijG5rOAAjELDyEr_Mt_970nPjLg_-I8-YTQ7a2u_f0FLXy0Ds9_Q5HWpu6OtptJEIQateGKBIxpN5JDAjkky8WcjmlpJPeeEEq2OHDrOVKCIOvQ_YshsDYzH9WCxg?width=1300&height=500&cropmode=none
---

ライフゲームは１９６０年代にケンブリッジ大学でジョン・ホートン・コンウェーによって作られた。
コンウェーはとても単純なルールで無限の結果を生み出す、そんな仕組みを作りたかったようだ。

![](https://7p36qg.bn.files.1drv.com/y4mtNaEPubJEFKiAmAUNaQmqgg6WdKzmvgvOP3yDVj1abt7f9gP7a7TZzUKlUaZ5XqnJDlBjhzUyrnHlBPBp4z1jpA-1Jmewsi4iTuiSCCsC1cM5w-4tqU8BDcu-csGHrTTaKfYRAdKV3fNbUIwoQOle23DAbBajo6JJWogv2U0xhu2gGAgwdboSEkt7kXi4aGMLcY7FqfZJDx7PjGPw2xMZQ?width=600&height=600&cropmode=none)

上の画像は筆者が実際にプログラミングで作ってみたライフゲームのモデルの画像である。
チェスの盤面のように四角形のマス目が３００×３００の９００マス並んでいる。
マス目をセルと呼ぶ。一つ一つのセルには二つの状態がある。
生（緑）と死（灰色）だ。ライフゲームは一つ一つのセルの状態が変化していく。
セルは自分の周りの８つのセル（近傍）を見てその中に生であるセルが何個ある
のか、
そして今自分が生なのか死なのか、この二つの情報をもとにして、
次に自分がどの状態であるかを決める。

## 自分が生の場合

- 近傍の中で２つまたは３つのセルが生なら生のまま
- 近郷の中で４つ以上のセルが生なら死になる
- 近傍の中で１つ以下のセルが生なら死になる

## 自分が死の場合

- 近傍の中に３つのセルが生なら生に変わる
- 上以外なら死のまま

上記したルールのみでライフゲームのセルは状態（色）を次々と変えていく。
ここには動画は載せられないが、その様子は見ていて飽きず、不思議なものだ。

筆者が作ったモデルの場合初期状態（０世代）はランダムに決まる。
その後、生は徐々に数を減らすが、一瞬で爆発的に増えたりもして、
減ったり増えたりを繰り返す。最終的には一定の形（動き）に落ち着く。

ここで感動的なのは初期状態が決まった時点でその後の動きも最後の形も決まっていると言うことだ。
しかし、その過程はあまりにも複雑で盤が一定の大きさ以上になると人間の手に負えなくなってしまう。
このことはどこか宇宙に通ずるものを感じる、法則に従っている物質がゴッツンゴッツンぶつかったり、くっついたり、
離れたりしている間に何んとも複雑な生き物やらなんやら（我々のような）が出てくる。ラプラスの悪魔的な、ね。

もともと、初期の時代はライフ・ゲームの計算を石とかを並べて手計算でやっていたらしいが、今はコンピューター上でやるのが一般的だ。

ところで、ライフゲームには「グライダー」と呼ばれるものが時たま出てくる。
グライダーは４世代（それぞれのセルが一つ状態を変えるごとに世代が１増えると考える、初期は０世代）で元の形に戻る一つの型（一定の動きをするセルの集まり、ある意味ライフ）だ。
これは他のセルに触れない限り無限に一つの方向に進んでいく。

![](https://7p37qg.bn.files.1drv.com/y4mpTtbnxxY4qUAYDd_DqmNaSc23DfwRrA4JRzF-7UPBGCh2wol_MWGPxIi67CCCB_vgEZhsx-ohcOR2iDNhAlVHY9ajjC5KeFTe05h91RvVdTj1H8DXwX-GCPvMtT36yz5BxKuiPSa9rOXrveTIFGM0KG-RbLXAEJwvWDYOzppk1RbDjMLrBZ21fGxjLc2KOrzHjfHmmGdWwepNI25SeWO2g?width=60&height=59&cropmode=none)
![](https://7p30qg.bn.files.1drv.com/y4mbr5TFJCAoB9DovwNmA8SRwPwMeAaD5H9dYX9pY72HgZbq_ANt-4PMgSShqMxh_a6ViEcUgYF7kD42u4RIskvkDEG0R9F-J5fTnf3cgSK7c8uIsP8aOYcAFVlWQJ4FrPydBk78NWQIwFhqrzqOpVE5m_waIdxfRhxL-XOGwQAFwFgtFaLpCp8B8IUIathzPsFxLNWQEEwazVQcxlslDHoGw?width=64&height=67&cropmode=none)

グライダーの第１世代（上）第２世代（下）
暇な人は動かして見てね。

９００のセルの中からでもこんな単純ではあるが規則を持った存在が出てくる。
もし、セルの盤を太陽系くらいの大きさにしたら、銀河系くらいの大きさにしたら、
一体どんなものが生まれてくるだろうか。
これを読んでいる方のほとんどはグライダーをライフとは認めないだろう。
しかし、太陽系くらいの大きさの盤からはライフと認めざるを得ないような、
繁殖し、進化するような型が出て来るかもしれない。

PARCO
