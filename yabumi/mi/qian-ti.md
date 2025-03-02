---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 前提

## SNS ID

Yabumiの設計では、SNSに個別の数字（ID）を割り振って、識別します。

例えばDiscordは1、Twitterは2となります。

ガス代を考慮して数字で識別する工夫を施しています。

## 署名

バックエンドでの署名には、以下の3つの要素を使用します。

* SNS上のUser ID　
  * [ ] 例：123456789
* SNS ID　
  * [ ] 例：1
* ミントしたウォレットアドレス　
  * [ ] 例：0x123456789...（40桁の16進数）

## JointedID

SNS上のUser IDとSNS IDをアンダースコアで結合したものをJointedIDと呼びます。

* [ ] 例：123456789\_1

## ハッシュ化

SNS上のUser IDとSNS ID（JointedID）と、ミントしたウォレットアドレスを結合ハッシュ化して署名メッセージに利用します。
