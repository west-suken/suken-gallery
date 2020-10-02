---
title: 美しく自然なサイトを目指して
date: 2019-09-19 09:54:59
tags: 2019年度
---

https://kinensai.netlify.com

by shundroid, 記念祭サイト制作有志, T@S

## 概要

　今年度は宣伝のために生徒で記念祭のサイトを作りました。公開までは技術面・制度面様々な苦労がありましたが、公開後は1日最大2000PV（ページビュー）を達成するなど成果を上げています。

## スクリーンショット

![](https://9e2ila.bn.files.1drv.com/y4mm92JGXYYm4YguPqmtbpCgX8KRI8RdebAT_EcfsrFSlQiQjva5UwLOy1aGbKA2VOXye6g164QK7HzA_124qcv4UPOuW5du0V2JY_pTXwcXA5fk4fhAnp2XtNsEtJvG9yqnwc6JAr9ptO927el-udYrlIVeHPhdVE7yhARbQfMmdp1yD5NrZOyCT3NpdphT-MvvCd93D1RjhyiQzqVREm6Ww?width=494&height=249&cropmode=none)

記念祭テーマの「　」をイメージしたデザインとなっています。

![](https://9e2jla.bn.files.1drv.com/y4mB-wPQ7t4E_3GjRrsEB3ypyapexmROI7CXdictouIvzQZBGY9DmUL_Ol1qPcAeqIDIMWSBIalsmwjbPT_iypABkesaPaaAR-fLicLxgu7dxozlAOcMOuhDbq-Itv6vo_A72HwRIzRGlmKC5gphmoLNYhmKuSOkWPw0_QCO8ZrfZdiDU0JPfGfGuHrwERqDmxqD01Ktp-ZaZ7iAF2DRXfGOQ?width=255&height=155&cropmode=none)

Theme のところでは「」のデザインが変化していきます。

![](https://9e2kla.bn.files.1drv.com/y4mFfLzoSL6_sKbDYlWDe7lmg8PSmgl2KD03ugBm-d10eosz-QulSPKD2ob_CnVHUw72hZGVPq5LsfFkFszDFNhEz7FomgQB_o0ls4ZEP9a8SJKMHzZRPoTqpdYfyfhtgVQh7yZPdylaHmogT2BSv2u65APm9dhdMbmRsr5UnSKKSarp3d8Ly0jTArNHHI2HwoBXD42B0rgXKdNFbTpM-EoEA?width=132&height=172&cropmode=none)

メインポスターはツイートに対応！

![](https://9e2lla.bn.files.1drv.com/y4m3TxmsX3834jU67oPQBzBBc5UeoKqYmxma5fOw-O_UEhY1zDd0dWbUguLCEeHKrxGBbmIDHfQZg4BOG0Z7Gl1zf6KqcHButHMI3MSafRutnobWEyQOboJ2lm37bCJkvQ7-74ijPXTo8ScXONZB31pu_RM8lsuDp-OszxvQwRLYGxhcRwFwMwJ1YpvySRB6KLpaT4jdA5Il5-KFoIZ8i-hkw?width=512&height=257&cropmode=none)

404エラーページでは実はゲームができます！

## 美しさ・自然さを実現する技術

### Transitionの活用によりノイズを除去し自然なユーザーエクスペリエンスを実現

SPA(=Single Page Application)を採用しているため、ページ遷移時にも実は物理的にページは移動しておらず、滑らかなアニメーションが実現されています。

### 高度に抽象化されたModelによるリストレンダリングで効率化とともにデザイン上のズレをなくす

MVVMにおけるM(Model)はプラトン哲学でいうイデアにあたると考えます。
その存在を端的で本質として管理することでMVVMの良さを生かし、無駄がなく~現実世界のように~自然なリストレンダリングを可能としています。

例
- Newsにおける各項目
- Programの内容(jsonで端的に保存、待ち時間管理のところで再利用されている)

### 待ち時間表示などにより記念祭そのものに自然に溶け込めるサイト設計

この非公式記念祭サイトは各団体の待ち時間の表示という役割を通して記念祭をサポートします。

## 待ち時間表示システムの構造

![](https://pu2nla.bn.files.1drv.com/y4mKM0dBJQAnNfIvpF7T6xp7_TAZ6dfNvY6V3TCtEkP6X53MU31oVX4oWqMD_5akZy1bRa-6GlwLZlkHn4Hxm9vAo8kRjy_1fFkN_oXEeMJS0A14l2xuZorH_Qsao50zUjEd9_kXdjI1af0vd6I_Ev4DN3Zeu5HFMLnErajhilGR39Rb8Soh35BkVPoERh_5WqF2TF4MSnrPLaALEG2lSyYWQ?width=542&height=201&cropmode=none)

（ほんとはHerokuサーバーとGASを統一したかったが時間がなかった）

## 共同開発

　デザインや広報担当の生徒とのやり取りは、LINEやPowerPointの共同編集を利用して行われました。これは「テキストボックス会話」の一部です。

![](https://9e2fla.bn.files.1drv.com/y4m3thA7dBIuXJnPo9fKumMXWPKAjBNpWrdiOgzKB820Osts_FQ69RiVlMz3y9u0mLhXx1z51zDsOSvaDbWAUf43rBd6nJy-GYCQhI6X_Ow1b_0z89OdsxTZglCxKPMjex7l1ogkBCzUJtXU_cmM5tUtb48sdDqDb91RUu5PgYsvhAv5QPKuVR3UiPs2s42KTfjOlOd6Ao75KTMCwee9_9IYQ?width=285&height=321&cropmode=none)

　数研のT@S氏には、GASでツイートするシステムの制作経験があったので、彼のノウハウをそのまま転用させてもらいました。このような協力ができるのは数研の大きな魅力です。

## 後輩へ

　記念祭サイトの制作は今後の代も続けていってほしいです。まあただ作るだけではなくて、サイトがどうみんなをハッピーにするか、が大事なのだとは思いますが。
　技術的な面で言うと、Vue は推せます。Web サービスでなくただ単にサイトとしてもかなり便利で効率化できます。正直一からやるなら生html/css/jsよりもこっちに詳しくなったほうがいいと思う…
　なかなか「公式」の称号をもらうのは難しいと思いますが、SEO対策や宣伝力を駆使してどんどんサイトを広める力も非常に大事だと感じました。頑張ってください。
