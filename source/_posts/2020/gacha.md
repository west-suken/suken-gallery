---
title: 推しを迎え入れるにはガチャを何回引けば良いか
date: 2020-10-3 0:02:25
tags: 2020年度
---

<div style="text-align: right">74期 だーれかさん</div>

## はじめに

みなさん、こんばんは。あなたの心の赤の他人。だーれかさんです。

私は数弱で、プログラミングも初心者なので、簡単で理解しやすいものを書きたいと思います。

私は数学の中で比較的、場合の数が得意だった（場合の数がメインの定期考査で数Aクラス内一位。その時の数Iはクラス内下から二位でした）ので、場合の数について書きたいと思い、このテーマ、推しを迎え入れるにはガチャを何回引けば良いか、にしました。

## 方法について

サイコロをn回振って、最低一回は1が出る確率を求める式は、全ての確率から1が一回も出ない確率を引くことで求められます。つまり、
$$
1-(5/6)^n
$$
これをガチャの推しが出る確率に置き換えれば、推しが一回でも出てきてくれる確率を求められるわけです。しかし、手で計算するのはあまりにも面倒だし、電卓でもnの値を1ずつ変えるのは面倒です。そこで、自動で計算してくれるプログラムを書いてみたいと思いました。

## プログラミングしてみた

はじめにで書いた通り、私はプログラミング初心者です。なので、とりあえずどういう処理が必要かをまとめてみることにしました。フローチャートにまとめると、以下のようになります。

![](https://qf2ahq.dm.files.1drv.com/y4mLGygXiP6134uhopGfERYXAokj_uvtWJMFkPcTAhPGIKPCYFS3Z65nllU2QjLIdLf2zETdexfK75cX2NZJeqh8Bo53y9_pIQPqlY6Oqd_wWeIAoqVU_gKe-BPRBg9zGPyZ-VY-UHZULaR18pyBdnjYQJxEXRlcqE7ZQ0Ijza_JET_PcGf0_B5IKG09D-GBBR69dm2tkP3n6X6e6RZ3_4jTA?width=1674&height=1483&cropmode=none)

![](https://qp2ahq.dm.files.1drv.com/y4mcHxDGAPORGxM6CPIU7E4df7vDLA0wZ1Ku2Hw-5OYKt53QJFYbI5NSYDROd5fdehXbMY5OdKquystsCz9cMCyJCkjzDL1ml-y_fYOXscjen6-yiPL53CZ7vc-7uXj9KaXTJpWXwhzRMAGieLDFIU-mY63zEwoO55pxhfzSV1vhqRgXQPP68Tut-43eeaRgGEgEQSzCydC5dnZ6J_wdbz6ww?width=1639&height=524&cropmode=none)

一番重要なのは、条件付きのループだと思いました。調べてみると、今回使うJavaScriptでは、whileを使うとうまくいくことがわかりました。他にも入力した数値を取り出す方法なども同時に調べました。

そして完成したプログラムが以下の通りです。

```javascript
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>ガチャ</title>
</head>
<body>
    <form>
        <label for="textForm">確率: </label>
        <input type="number" id="textForm"> 

        <button id="button">計算</button> 
    </form>

    <label for="resultForm">計算結果: </label>
    <input type="text" id="resultForm">

    <label for="resultForm2">回数: </label>
    <input type="text" id="resultForm2">

</body>

<script>
    var button = document.getElementById("button");
    button.addEventListener("click", function(e){
        e.preventDefault();

        let count = 0;

        let textForm = document.getElementById("textForm").value;

        let form = 100 - parseFloat(textForm, 10);
        form = form / 100;
        let hit = form;
        while (hit > 0.5 ){
            hit = hit * form;
            count++; 
        }
        let resultForm = document.getElementById("resultForm");
        resultForm.value = ( 1 - hit ) * 100;
        let resultForm2 = document.getElementById("resultForm2");
        resultForm2.value = count;
    });
</script>
</html>
```

 

説明すると、上半分は、排出率を入力する場所と、結果を表示する場所を作っていて、
下半分は入力した排出率を取り出して、計算させています。
ちなみにかかった時間は、調べる時間も含めて約3時間でした。

## 結果

ちょうどこれを執筆するときに推しの供給がきたので、ガチャを引いてみることにしました。
排出率は、ピックアップで0.501%　このプログラムで計算してみると、

![](https://oimpog.bn.files.1drv.com/y4m4EBsEnQgMBRhKn5Mwt6RzEAkTOHJuo0Nu-WWp3Y1-vJS06TMZKEUOE6C61oq7TX2ASHNdYo1nPbt43m_TEKQNQlFg9oD-X6e1U2u9zJTB_YsuUoiHi0WGTxelUhDKcIGR39lMCgx9FKd26zNO34oM4GY5wX_mgb_xPNaoLr0XxZRM6jCNlaeytqdZ4mLnOxJePVbApFQNrll8gLgW0GU5w?width=880&height=132&cropmode=none)

138回引けば約50.25%で迎え入れることができるみたいです。
しかし、微課金勢の私は、無料石をかき集めても107回しか引くことができず（課金分0回）、推しを迎え入れることができませんでした。部誌のために課金するのも変なので許してください。
ちなみに107回のガチャで推しを迎え入れることができる確率は、whileの（）の中を少し書き換えて、計算すると、

![](https://oipefg.bn.files.1drv.com/y4mJy0etsWCvlWDgTEilGuZQvgQ5XTGRutJodcopYRjJ7cG9W2tIltfcv3MxMVH00UOnjvOZgadrp4ak9FSlrxpyKntQGmD7YqDSFVna1LT0TJFa7L2OTSQuQlpyGJp4bGvt_JVTgr0wxmSUnqANCodM6Mbb7RsrR-y8qNQq9YM6Yrm7QzVFG0XyjaiDrJ0ZFlySv9ox26Xs8E8cWZLe2xQqA?width=866&height=122&cropmode=none)

約41.87%でした。

「◯◯回引いたのに推しが出なかった！　運が悪い！」というためには思ったより回数を引く必要があるみたいです。

最後まで読んでいただきありがとうございました。みなさんも簡単なプログラミングを学んで、問題を解決してみてください。