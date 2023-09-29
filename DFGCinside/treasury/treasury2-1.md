# Safe Wrapper ツール

運営上、Safeを使い勝手をよくするため、以下のサービスを利用します。

* **Parcel**　TXJPを扱える。TXシェアページがある。ヒストリーのDLができる。
* CoinShift　TXJPトークンが表示されず扱えない
* Utopia　ヒストリーを読み込んでこない

### 選定条件

* 1人向け、複数名向け、CSVでTX作成
* リカーリング支払いワークフローを登録できる
* マルチシグ署名、できればトリガーを投票にする
* TXごとに支出メモを残せて、パブリックに共有可能
* ヒストリーデータをCSVダウンロードできる
* ドル入力でトークン数量を自動計算してくれる（任意）
* 署名者以外がTX作成できる（任意）

## SafeのDeFiサポート

#### DeFi

| Services      | In-app | WalletConnect |
| ------------- | :----: | :-----------: |
| Curve         |    ✅   |       ✅       |
| Compound      |        |       ✅       |
| Convex        |        |       ✅       |
| LlamaAirforce |        |       ✅       |
| Uniswap       |    ✅   |       ✅       |
| Balancer      |    ✅   |       ✅       |
| 1inch         |    ✅   |       ✅       |
| Votium        |        |       ✅       |
| Fuse          |        |       ✅       |
|               |        |               |
|               |        |               |

#### Utility

| Services  | In-app | WalletConnect |
| --------- | :----: | :-----------: |
| Debank    |        |       -       |
| Zapper    |        |       ✅       |
| Zerion    |    ✅   |       ✅       |
| Defisaver |    ✅   |       ✅       |
| Instadapp |    ✅   |       ✅       |
| Etherscan |        |       ✅       |
| Snapshot  |    ✅   |       ✅       |
|           |        |               |

