---
description: >-
  DeFiGeek Communityにおける各Dapps Tokenの標準的な展開方法（Token Launch
  Standard＝TLS）です。Tokenによって展開方法が変わる可能性はあり、あくまでも標準的な展開方法を定めるものです。
---

# DFGC トークンローンチスタンダード ver1

## 1. 基本アロケーション（基本配分）

<table data-full-width="false"><thead><tr><th width="162" align="center">配分割合（%）</th><th width="289" align="center">配分名目</th><th align="center">備考</th></tr></thead><tbody><tr><td align="center">5%</td><td align="center">開発者報酬</td><td align="center">ー</td></tr><tr><td align="center">5%</td><td align="center"><a href="https://defigeek.xyz/txjp/">TXJP</a>(DFGCガバナンストークン）ホルダーへの配分</td><td align="center">ー</td></tr><tr><td align="center">5%</td><td align="center">DEX LP用</td><td align="center"><p>1％　IAO</p><p>1％　Uniswap v3 対CJPYpool</p><p>1％　Uniswap v3 対TXJPpool</p><p>2％　Curve pool</p></td></tr><tr><td align="center">5%</td><td align="center"><p>コミュニティトレジャリー配分</p><p>（長期開発支援予算）</p></td><td align="center">defigeek.eth</td></tr><tr><td align="center">5%</td><td align="center">初期ユーザーへの配分</td><td align="center">ー</td></tr><tr><td align="center">10%</td><td align="center">CurveLP用リワード</td><td align="center">年次2％べスティング5年間</td></tr><tr><td align="center">10%</td><td align="center">フェーズ2投資家用</td><td align="center">クリフ2年、3年目</td></tr><tr><td align="center">55%</td><td align="center">Dapp長期ユーザーリワード</td><td align="center">初年度5.5% 年次10％逓減</td></tr></tbody></table>

## 2.基本仕様

* 総発行数：10億Token
* 発行規格：ERC-20スタンダード
* その他：veモデルの実装

{% hint style="info" %}
**ve（Vote-Escrowed　ボート・エスクロード）モデルとは**

Tokenを長期間預けることで、より大きな権限と報酬を得られるモデルです。

「Vote（投票）」と「Escrowed（預託）」を組み合わせた言葉で、分散型取引所Curveが初めて導入しました。

例えば、Curveの場合は、CRVトークンを4年間預けると

* 投票力が最大4倍に
* 流動性提供の報酬が最大2.5倍に
* プロトコル（システム）収益の一部を受け取れる

といったインセンティブがあります。

この仕組みにより、短期的な売り圧力を抑えながら、プロジェクトの意思決定に真剣に関わるユーザーを増やすことができます。現在では、多くのDeFiプロジェクトでも採用されるToken経済モデルとなっています。
{% endhint %}

## 3.基本ローンチフロー

{% stepper %}
{% step %}
### Da**ppsユーザーリワード分（55％）以外を発行（**総量の**45%発行）**
{% endstep %}

{% step %}
### IAOの実施（総量の1%）

DFGC開発DappであるIAOプラットフォーム「[Yamawake](https://yamawake.xyz/)」にて実施。

※[Yamawake公式ドキュメント](https://docs.yamawake.xyz/)

{% hint style="info" %}
**IAO（Initial Auction Offering）とは**

IAOは、暗号資産プロジェクトの新しい資金調達方式の1つです。従来のICO（Initial Coin Offering）やIDO（Initial DEX Offering）とは異なり、オークション形式で行われる特徴があります。\
DFGCでは、IAOプラットフォーム「Yamawake」を開発・ローンチしており、Yamawakeを使ってIAOを実施します。
{% endhint %}
{% endstep %}

{% step %}
### DEX LP v1設置(IAO分を除く）（総量の4%）

* Uniswapにて、IAO価格の上に10倍（＄）Token、下に入札ETH分（＄）（CJPY,TXJP）をpool設置
  * 1％　Uniswap v3 CJPYpool
    * CJPYはDFGCトレジャリーから[Yamato](https://app.yamato.fi/#/)及び[punodwoɔ](https://pnd.defigeek.xyz/)を通じて調達
  * 1％　Uniswap v3 TXJPpool
    * TXJPはIAO入札ETHにて市場購入
* 2％　Curve pool
{% endstep %}

{% step %}
### [punodwoɔ](https://pnd.defigeek.xyz/)での担保化

循環供給量の1～5〜10％をサプライキャップ目安に担保化を行います。時価総額が大きいほど1％になり、時価総額が小さいほど10％になります。

IAO後のDEX流動性設置と稼働実績を以ってオラクル取得次第、担保化を実行します。

{% hint style="info" %}
[**punodwoɔ**](https://pnd.defigeek.xyz/)**とは**

管理者（第三者）を介さずユーザー同士で貸し借りができるDFGCが開発したプロトコルです。

ユーザーは、担保資産をプールに預け入れることで、ベース資産を借り入れることが出来、ベース資産を預け入れることで利息を得ることが可能です。

※[punodwoɔ公式ドキュメント](https://app.gitbook.com/o/-MhI8qrzXbwrsBM7wCuy/c/3sR7g0lYDp1Mdk4aM1Oj)
{% endhint %}
{% endstep %}

{% step %}
### 開発者報酬配布（総量の5％）
{% endstep %}

{% step %}
### 各Dapp仕様に合わせた初期ユーザーへの配分開始（総量の5%）

各Dappの初期ユーザーに対する配当です。
{% endstep %}

{% step %}
### [TXJP](https://defigeek.xyz/txjp/)(DFGCガバナンストークン）ホルダーへの配分（総量の5%）

DFGCが開発するマークルディストリビューターツール「Megumi（2024Q4メインネット稼働予定）」を使って配布予定。

ただし、以下のアドレスは配布対象外です（コミュニティトレジャリーアドレス等）

<table><thead><tr><th width="492">除外アドレス</th><th>除外理由</th></tr></thead><tbody><tr><td>0xBA12222222228d8Ba445958a75a0704d566BF2C8</td><td>Balancer</td></tr><tr><td>0x153d9DD730083e53615610A0d2f6F95Ab5A0Bc01</td><td>safe.defigeek.eth</td></tr><tr><td>0x65330f9589d3384C8218374dE93cF48d43927904</td><td>LlamaPay</td></tr><tr><td>0xA9166690c35d900a57D2ec132C58291bC0678944</td><td>UniswapTXJP</td></tr><tr><td>0x4534f4968006Ca9ECA3Bac922022C7eCBa066E9e</td><td>ガバナンス用１</td></tr><tr><td>0xDc94EEeb3260D0b9Bf22849E8f5d236D286CDBa1</td><td>ガバナンス用２</td></tr><tr><td>0x08bfa2Ba3c948A35AD9d9f2746A51Ffaf796A814</td><td>UniswapPNDTXJP</td></tr><tr><td>0x0028A459D6705B30333E98d5bCb34DD1B21e2A89</td><td>FuseリワードTXJP１</td></tr><tr><td>0x485D8c64f33Db5152A1159e0443dAA4b1A620160</td><td>FuseリワードTXJP２</td></tr><tr><td>0x63942E31E98f1833A234077f47880A66136a2D1e</td><td>VotiumBribe</td></tr><tr><td>0x378Ba9B73309bE80BF4C2c027aAD799766a7ED5A</td><td>Votiumスタック</td></tr><tr><td>0x9008D19f58AAbD9eD0D60971565AA8510560ab41</td><td>cowスタック</td></tr><tr><td>0x4a183b7ED67B9E14b3f45Abfb2Cf44ed22c29E54</td><td>Zerionスタック</td></tr><tr><td>0x29e3b0E8dF4Ee3f71a62C34847c34E139fC0b297</td><td>Votiumスタック</td></tr><tr><td>0xce88686553686DA562CE7Cea497CE749DA109f9F</td><td>Balancerスタック</td></tr><tr><td>0x00000000009726632680FB29d3F7A9734E3010E2</td><td>Rainbowスタック</td></tr><tr><td>0x000000fee13a103A10D593b9AE06b3e05F2E7E1c</td><td>ルータースタック</td></tr><tr><td>0xdD9f24EfC84D93deeF3c8745c837ab63E80Abd27</td><td>ルータースタック</td></tr><tr><td>0xeFbF49285c3d3dc16bd2634E2E06b16651Ba0bdb</td><td>旧Votiumスタック</td></tr><tr><td>その他0.01TXJP未満保有アドレス</td><td>0.01TXJP未満保有</td></tr></tbody></table>


{% endstep %}

{% step %}
### Dapp長期ユーザーリワードとして、各Dapp仕様に合わせて適時発行及び配布開始（総量の55%）
{% endstep %}

{% step %}
### DFGCコミュニティチャット（[Discord](https://discord.gg/FQYXqVBEnh)）にてprice info botを設置
{% endstep %}

{% step %}
### トークンリスティング（[CoinGecko](https://www.coingecko.com/ja)等）

CoinGecko等のTokenの市場データ情報プラットフォームにリスティング依頼を行います。
{% endstep %}

{% step %}
### DEX LP v2 （Curve）
{% endstep %}
{% endstepper %}



