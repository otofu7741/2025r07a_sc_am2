---
marp: true
theme: default
paginate: true
html: true
style: |
  :root {
    --main:    #0041C0;
    --dark:    #001A4D;
    --mid:     #1C68D4;
    --light:   #4A8FE8;
    --pale:    #EBF2FF;
    --accent:  #00AECE;
    --correct: #1A7A48;
    --wrong:   #B83232;
    --gold:    #D4820A;
    --gray:    #F0F4FF;
    --white:   #FFFFFF;
  }

  /* ===== Base ===== */
  section {
    background: var(--white);
    color: #1A1A2E;
    font-family: 'Noto Sans JP', 'Hiragino Kaku Gothic ProN', sans-serif;
    padding: 36px 52px;
    font-size: 18px;
    line-height: 1.55;
  }

  section::after {
    color: var(--main);
    font-weight: 700;
    font-size: 0.7em;
  }

  h1 {
    color: var(--main);
    font-size: 1.55em;
    border-bottom: 3px solid var(--main);
    padding-bottom: 6px;
    margin-bottom: 16px;
  }

  h2 {
    color: var(--main);
    font-size: 1.25em;
    border-left: 5px solid var(--main);
    padding-left: 12px;
    margin: 16px 0 10px;
  }

  h3 {
    color: var(--mid);
    font-size: 1.05em;
    margin: 12px 0 6px;
  }

  strong { color: var(--dark); }
  em     { color: var(--mid); font-style: normal; font-weight: 600; }

  ul, ol { padding-left: 1.4em; margin: 6px 0; }
  li     { margin: 3px 0; font-size: 0.92em; }

  blockquote {
    border-left: 4px solid var(--accent);
    background: var(--pale);
    margin: 8px 0;
    padding: 6px 14px;
    border-radius: 0 6px 6px 0;
    font-size: 0.88em;
  }

  code {
    background: var(--pale);
    color: var(--main);
    padding: 1px 5px;
    border-radius: 3px;
    font-size: 0.85em;
  }

  /* ===== Tables ===== */
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.82em;
    margin: 10px 0;
  }
  th {
    background: var(--main);
    color: white;
    padding: 7px 10px;
    text-align: left;
  }
  td { padding: 5px 10px; border-bottom: 1px solid #ccd8f0; }
  tr:nth-child(even) td { background: var(--pale); }

  /* ===== Special Layouts ===== */
  section.title {
    background: linear-gradient(145deg, var(--dark) 0%, var(--main) 55%, #2A68D4 100%);
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.title h1 {
    color: white;
    border-bottom: 2px solid rgba(255,255,255,0.35);
    font-size: 2em;
    margin-bottom: 12px;
  }
  section.title h2, section.title p {
    color: rgba(255,255,255,0.88);
    border: none;
    font-size: 1.1em;
  }
  section.title .subtitle {
    font-size: 0.95em;
    color: rgba(255,255,255,0.7);
    margin-top: 18px;
    padding: 6px 20px;
    border: 1px solid rgba(255,255,255,0.3);
    border-radius: 20px;
  }

  section.sec-header {
    background: linear-gradient(135deg, var(--dark) 0%, var(--main) 100%);
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.sec-header h1, section.sec-header h2 {
    color: white;
    border: none;
    font-size: 2em;
  }
  section.sec-header p {
    color: rgba(255,255,255,0.8);
    font-size: 1em;
  }
  section.sec-header .qs {
    font-size: 0.85em;
    background: rgba(255,255,255,0.15);
    padding: 4px 16px;
    border-radius: 20px;
    margin-top: 10px;
    color: rgba(255,255,255,0.9);
  }

  /* ===== Badges ===== */
  .badge {
    display: inline-block;
    color: white;
    padding: 2px 11px;
    border-radius: 20px;
    font-size: 0.72em;
    font-weight: 700;
    margin-right: 6px;
    vertical-align: middle;
    letter-spacing: 0.03em;
  }
  .badge.crypto  { background: #0041C0; }
  .badge.attack  { background: #B83232; }
  .badge.auth    { background: #6B3FAA; }
  .badge.web     { background: #0C7B5E; }
  .badge.mgmt    { background: #A65C00; }
  .badge.net     { background: #1A6B9E; }
  .badge.webtech { background: #2262A0; }
  .badge.system  { background: #4A5568; }
  .badge.law     { background: #7D5A0E; }
  .badge.calc    { background: #2E7D32; }
  .badge.audit   { background: #37474F; }
  .badge.diff-easy  { background: #2E7D32; }
  .badge.diff-std   { background: #1565C0; }
  .badge.diff-hard  { background: #B83232; }

  /* ===== Answer & Trend Boxes ===== */
  .answer-box {
    background: #EAF7EF;
    border-left: 4px solid var(--correct);
    padding: 7px 14px;
    margin: 8px 0;
    border-radius: 0 6px 6px 0;
    font-size: 0.9em;
  }
  .answer-box .ans-label {
    font-weight: 700;
    color: var(--correct);
    font-size: 0.85em;
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }

  .trend-box {
    background: #FFF8E6;
    border-left: 4px solid var(--gold);
    padding: 7px 14px;
    margin: 8px 0;
    border-radius: 0 6px 6px 0;
    font-size: 0.82em;
    line-height: 1.5;
  }
  .trend-box .trend-label {
    font-weight: 700;
    color: var(--gold);
    font-size: 0.85em;
    letter-spacing: 0.03em;
  }

  .info-box {
    background: var(--pale);
    border-left: 4px solid var(--main);
    padding: 7px 14px;
    margin: 8px 0;
    border-radius: 0 6px 6px 0;
    font-size: 0.88em;
  }

  .correct-mark { color: var(--correct); font-weight: 700; }
  .wrong-mark   { color: var(--wrong);   font-weight: 700; }

  /* ===== Two-column layout ===== */
  .cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-top: 10px;
  }
  .cols3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 12px;
    margin-top: 10px;
  }
  .col-box {
    background: var(--pale);
    border-radius: 8px;
    padding: 10px 14px;
    font-size: 0.85em;
  }
  .col-box h4 {
    color: var(--main);
    font-size: 0.92em;
    margin: 0 0 6px;
    border-bottom: 1px solid #ccd8f0;
    padding-bottom: 4px;
  }

  /* ===== Priority stars ===== */
  .star-high   { color: #D4820A; font-size: 1.1em; }
  .star-mid    { color: #1565C0; font-size: 1.1em; }
  .star-low    { color: #4A5568; font-size: 1.1em; }

  /* ===== Keyword chips ===== */
  .chip {
    display: inline-block;
    background: var(--pale);
    color: var(--main);
    border: 1px solid #9BB8F0;
    border-radius: 16px;
    padding: 2px 10px;
    font-size: 0.78em;
    margin: 2px;
    font-weight: 600;
  }

  /* ===== Footer bar ===== */
  section.has-footer::before {
    content: '令和7年度 秋期 情報処理安全確保支援士試験 午前Ⅱ 分析';
    position: absolute;
    bottom: 18px;
    left: 52px;
    font-size: 0.65em;
    color: #8A9BBD;
    letter-spacing: 0.02em;
  }
---

<!-- _class: title -->

# 令和7年度 秋期<br>情報処理安全確保支援士試験<br>午前Ⅱ 分析

## 問1〜問25 全問解説 ＋ 情報分野の情勢

<div class="subtitle">試験時間 10:50〜11:30（40分）／全25問必須解答</div>

---

<!-- _class: has-footer -->

# 試験全体の概要

<div class="cols">
<div>

**出題構成**

全25問 ／ 択一4択 ／ 40分

- セキュリティ系：**16問（64%）**
- 基礎IT系：**9問（36%）**

**合格ライン目安：60点（15問）以上**

</div>
<div>

**今回の特徴**

1. 🔬 AI・量子（PQC）が正面出題
2. ☁️ クラウドセキュリティ2問
3. ⚠️ 攻撃手法4問（多様化）
4. 📋 フレームワーク・組織4問以上
5. 🔧 基礎技術は例年どおり9問

</div>
</div>

---

<!-- _class: has-footer -->

# 出題カテゴリ分布

| カテゴリ                                    | 問題番号               | 問数  | 比率  |
| ------------------------------------------- | ---------------------- | :---: | :---: |
| 暗号技術                                    | 問1, 問3, 問9          |   3   |  12%  |
| 攻撃手法                                    | 問2, 問5, 問7, 問8     |   4   |  16%  |
| 認証・PKI                                   | 問4, 問10, 問11        |   3   |  12%  |
| Webセキュリティ                             | 問6, 問16              |   2   |  8%   |
| セキュリティ管理・組織                      | 問12, 問13, 問14, 問15 |   4   |  16%  |
| ネットワーク                                | 問17, 問19, 問20       |   3   |  12%  |
| Web技術 / システム・DB / 法律 / 計算 / 監査 | 問18, 問21〜25         |   6   |  24%  |

> **セキュリティ関連合計：16問（64%）　　基礎IT：9問（36%）**

---

<!-- _class: has-footer -->

# 問題難易度の概観

| 難易度                                      | 問題番号                                                      | 備考                         |
| ------------------------------------------- | ------------------------------------------------------------- | ---------------------------- |
| <span class="badge diff-easy">易</span>     | 問2, 問9, 問12, 問18, 問20                                    | 定義・用語の直接問いかけ     |
| <span class="badge diff-std">標準</span>    | 問1, 問4, 問6, 問11, 問13, 問14, 問15, 問17, 問19, 問23, 問25 | 正確な理解が必要             |
| <span class="badge diff-hard">やや難</span> | 問3, 問5, 問7, 問8, 問10, 問16, 問21, 問22                    | 紛らわしい選択肢あり         |
| 計算                                        | 問24                                                          | 落ち着いて計算すれば正解可能 |

<div class="info-box">
易問（5問）は確実に取り、標準問題（11問）で合否が決まる。やや難問でも最低4〜5問は正解したい。
</div>

---

<!-- _class: sec-header -->

# 暗号技術

<p>問1・問3・問9</p>
<div class="qs">CRYPTREC暗号リスト ／ PQC ／ 情報理論的安全性</div>

---

<!-- _class: has-footer -->

# 問1　CRYPTREC暗号リスト

<span class="badge crypto">暗号技術</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：ウ</div>
推奨候補暗号リスト＝安全性・実装性能が確認され、今後推奨リストに掲載される可能性がある暗号技術
</div>

**CRYPTREC暗号リストの3区分**

| リスト名                                                      | 位置付け                       |
| ------------------------------------------------------------- | ------------------------------ |
| **電子政府推奨暗号リスト**                                    | 政府システムで推奨。現役・主力 |
| **推奨候補暗号リスト** <span class="correct-mark">← ウ</span> | 将来の推奨候補。今後昇格予定   |
| **運用監視暗号リスト**                                        | 新規利用不可。互換維持のみ許容 |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
2024年にNISTがPQC標準（ML-KEM/ML-DSA等）を正式公開。CRYPTRECもデジタル庁主導で耐量子暗号への移行計画を策定中。推奨候補リストは量子コンピュータ時代への橋渡しとして重要性が増大。
</div>

---

<!-- _class: has-footer -->

# 問3　PQC（Post-Quantum Cryptography）

<span class="badge crypto">暗号技術</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：エ</div>
量子コンピュータを使った攻撃に対しても、<strong>従来のコンピュータを使って</strong>安全性を確保できる暗号技術
</div>

**重要な誤解ポイント**

> PQCは「量子コンピュータで動作する暗号」ではなく、「量子攻撃に耐える暗号」

- 対象脅威：**Shorのアルゴリズム**（RSA/ECC破壊）、**Groverのアルゴリズム**（対称鍵攻撃）
- 候補技術：格子暗号・符号暗号・多変数多項式暗号

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
2024年8月、NISTがML-KEM（FIPS 203）・ML-DSA（FIPS 204）・SLH-DSA（FIPS 205）を正式公開。NSA CNSA 2.0は2030〜2033年の移行期限を明示。「Harvest Now, Decrypt Later」攻撃に備え早急な移行が必要。TLS/SSH/VPNへの組み込みが進行中。
</div>

---

<!-- _class: has-footer -->

# 問9　情報理論的安全性に基づく暗号技術

<span class="badge crypto">暗号技術</span> <span class="badge diff-easy">易</span>

<div class="answer-box">
<div class="ans-label">正解：エ　ワンタイムパッド（OTP）</div>
鍵長≧平文長 ＋ 真乱数 ＋ 使い捨て の3条件を満たすと、無限の計算能力を持つ攻撃者にも解読不可能
</div>

**安全性の分類**

| 種別                 | 前提                     | 例                    |
| -------------------- | ------------------------ | --------------------- |
| **情報理論的安全性** | 計算能力に依存しない     | **ワンタイムパッド**  |
| 計算量的安全性       | 現実的な計算量で解読不可 | RSA・DH・楕円曲線暗号 |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
量子鍵配送（QKD）はOTPの原理で完全秘匿通信を実現しようとする技術。東芝・NECが実証実験を推進、政府・金融機関での試験導入が進行中。秘密分散（Secret Sharing）・安全なMPC（マルチパーティ計算）にも応用されている。
</div>

---

<!-- _class: sec-header -->

# 攻撃手法

<p>問2・問5・問7・問8</p>
<div class="qs">Pass the Hash ／ モデルインバージョン ／ SYN反射型DDoS ／ ドメインフロンティング</div>

---

<!-- _class: has-footer -->

# 問2　Pass the Hash攻撃

<span class="badge attack">攻撃手法</span> <span class="badge diff-easy">易</span>

<div class="answer-box">
<div class="ans-label">正解：イ</div>
パスワードのハッシュ値だけでログインできる仕組みを悪用し、ハッシュ値そのものを認証トークンとして使用
</div>

**攻撃フロー**

1. SAMデータベース・LSASSメモリからNTLMハッシュを窃取
2. 平文パスワードを復元**せずに**、そのまま別システムへの認証に使用
3. **ラテラルムーブメント**（横断的侵害）に悪用

**誤りの選択肢**：ア＝パスワードクラック、ウ＝リバースブルートフォース、エ＝平文漏洩

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
ランサムウェアグループ・APTによる横断的侵害で依然多用。Microsoft はWindows 11でCredential Guard をデフォルト有効化。CISAのKEVカタログに関連手法が頻繁に登録されており被害増加傾向。
</div>

---

<!-- _class: has-footer -->

# 問5　AIに対するモデルインバージョン攻撃

<span class="badge attack">攻撃手法</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
AIモデルへの入力を調整しながら出力を繰り返し取得・解析し、<strong>学習に用いた元のデータを推測</strong>する
</div>

**AIへの主要攻撃手法の整理**

| 攻撃名                                                          | 概要                                               |
| --------------------------------------------------------------- | -------------------------------------------------- |
| **モデルインバージョン** <span class="correct-mark">← ア</span> | 出力から学習データを逆算・復元（プライバシー侵害） |
| モデル抽出攻撃                                                  | 入出力観察によりモデルを複製                       |
| ポイズニング攻撃                                                | 学習データ汚染で意図的誤動作                       |
| 敵対的サンプル攻撃                                              | 微小摂動で誤分類を引き起こす                       |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
LLM（ChatGPT/Claude等）の急普及でAIセキュリティへの関心が急騰。EU AI Act（2024年発効）はリスク分類とセキュリティ要件を規定。MITREがATLAS（AI攻撃戦術フレームワーク）を公開。日本でもAIガバナンス議論が加速。
</div>

---

<!-- _class: has-footer -->

# 問7　SYN/ACKパケット大量観測時の攻撃推定

<span class="badge attack">攻撃手法</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
IPアドレスAを<strong>攻撃先（被害者）</strong>とするサービス妨害攻撃
</div>

**SYN反射型DDoS攻撃のメカニズム**

```
攻撃者 ──[送信元IP=A に偽装したSYNパケット]──▶ 多数のホスト
                                                     │
多数のホスト ──[SYN/ACK をIPアドレスAに返送]──────▶ A（被害者・大量の不要SYN/ACKで過負荷）
```

- 宛先IPが「未使用」→ そのホストはSYNを送ってないから届いたSYN/ACKは偽物（AがSYNを偽装して見せかけている証拠）
- 送信元ポート80 → 正規Webサーバに見せかける偽装

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
2023〜2024年に数Tbps超の記録的DDoS攻撃が多発（Cloudflare・Akamai報告）。DNS/NTP/QUICを悪用した反射型増幅攻撃の亜種が登場。ISPでのBCP38（送信元アドレス検証）適用が国際的に求められている。
</div>

---

<!-- _class: has-footer -->

# 問8　ドメインフロンティングを悪用した攻撃

<span class="badge attack">攻撃手法</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
マルウェアがCDNの機能を悪用し、<strong>実際の通信先を隠蔽</strong>して攻撃者のサーバに接続する
</div>

**ドメインフロンティングの仕組み**

| レイヤ                               | 指定するドメイン             |
| ------------------------------------ | ---------------------------- |
| TLS SNI（外側・監視に見える）        | `cdn.example.com`（正規CDN） |
| HTTP Host ヘッダ（内側・実際の宛先） | `attacker.evil.com`          |

- ネットワーク監視はSNIしか見えない → 正規CDNへの通信に偽装成功
- **C2通信の隠蔽**に悪用される

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
ロシア・北朝鮮·イランの国家支援型APTが多用。AWS CloudFront・Googleは対策を実施済みだが「ドメイン隠蔽」「クラウドトンネリング」など派生手法が続出。TLS Inspection（SSL復号検査）の重要性が増大。Cobalt Strike等への組み込みも確認。
</div>

---

<!-- _class: sec-header -->

# 認証・PKI

<p>問4・問10・問11</p>
<div class="qs">PKIのRA ／ 認証デバイス ／ NIST SP 800-63-3</div>

---

<!-- _class: has-footer -->

# 問4　PKIのRA（Registration Authority）の役割

<span class="badge auth">認証・PKI</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：エ</div>
本人確認を行い、デジタル証明書の発行申請の<strong>承認または却下</strong>を行う
</div>

**PKIの主要コンポーネント**

| コンポーネント                                                          | 役割                             |
| ----------------------------------------------------------------------- | -------------------------------- |
| **CA**（Certificate Authority）                                         | 証明書の発行・署名・失効         |
| **RA**（Registration Authority） <span class="correct-mark">← エ</span> | 申請者の本人確認・審査、CAへ通知 |
| **VA**（Validation Authority）                                          | 証明書の有効性確認（OCSP）       |
| **AA**（Attribute Authority）                                           | 属性証明書の発行                 |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
IoT・コンテナ普及でマシンアイデンティティの発行件数が急増。Let's Encryptを筆頭にACMEプロトコルが普及し証明書の短命化（47日化を業界が議論）が進行。CAB Forum規則強化でRAの本人確認プロセスにも厳格化の圧力。
</div>

---

<!-- _class: has-footer -->

# 問10　認証デバイスに関する記述

<span class="badge auth">認証・PKI</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：イ</div>
虹彩認証では、認証デバイスで用いる虹彩パターンの<strong>更新がほとんど不要</strong>である
</div>

**各選択肢の誤り**

| 選択肢                                 | 誤りのポイント                                                      |
| -------------------------------------- | ------------------------------------------------------------------- |
| ア                                     | USBトークン証明書に接続先PCのMACアドレスは不要                      |
| <span class="correct-mark">イ ○</span> | 虹彩は加齢でほぼ変化しない → 更新不要・FAR極めて低い                |
| ウ                                     | LED照明の影響を受けるのは**光学式**（静電容量式は電気的特性を検出） |
| エ                                     | コイル誘導起電力を使うのは**非接触型**（接触型は物理接点）          |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
パスキー（Passkey）・FIDO2/WebAuthn普及でパスワードレス認証が急拡大。Apple/Google/Microsoftがサポート。マイナンバーカードのスマホ搭載（2023年〜）も進行。ディープフェイクによる顔認証バイパスへの懸念でLiveness Detection技術が重要化。
</div>

---

<!-- _class: has-footer -->

# 問11　NIST SP 800-63-3 の Identity Proofing

<span class="badge auth">認証・PKI</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
システムに利用者を登録する際に、利用者本人と<strong>写真付き身分証とを照合し確認</strong>する
</div>

**NIST SP 800-63-3 の3要素**

| 要素                  | 内容                           | 正解との関係                           |
| --------------------- | ------------------------------ | -------------------------------------- |
| **Identity Proofing** | 登録時の本人確認（身分証照合） | <span class="correct-mark">ア ○</span> |
| Authentication        | ログイン時の本人確認           | エが相当                               |
| Federation            | システム間ID連携               | —                                      |

IAL（Identity Assurance Level）1〜3で厳格さを段階規定

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
NISTはSP 800-63-4を策定中（リモートでのオンラインIdentity Proofing強化）。マイナンバーカードを使ったeKYC（JPKI）が金融・行政で急普及。ディープフェイクを使ったKYCバイパス事例も報告され、業界横断的な課題となっている。
</div>

---

<!-- _class: sec-header -->

# Webセキュリティ

<p>問6・問16</p>
<div class="qs">XMLデジタル署名 ／ CSRF攻撃対策</div>

---

<!-- _class: has-footer -->

# 問6　XMLデジタル署名の特徴

<span class="badge web">Webセキュリティ</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：イ</div>
XML文書中のエレメントに対するデタッチ署名を作成し、<strong>同じXML文書に含める</strong>ことができる
</div>

**XMLデジタル署名の3形式**

| 形式                                                    | 説明                                                  |
| ------------------------------------------------------- | ----------------------------------------------------- |
| エンベロープ署名                                        | 署名対象のXML内部に署名を埋め込む                     |
| エンベロービング署名                                    | 署名要素の内部に署名対象を含める                      |
| **デタッチ署名** <span class="correct-mark">← イ</span> | 署名対象と署名が分離。同一XML文書内に含めることも可能 |

- CMSはPKCS#7/S/MIMEで使用。ASN.1はCMS側の記述言語。XMLデジタル署名はW3C XMLSig準拠。

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
電子政府・B2B EDIでXML署名が継続使用。APIエコノミーではJWT/JWSが主流。クラウドサイン等の電子契約急拡大に伴い、eIDAS規則・電子署名法への理解が重要化。
</div>

---

<!-- _class: has-footer -->

# 問16　CSRF攻撃の対策として**効果がない**もの

<span class="badge web">Webセキュリティ</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：エ（効果なし）</div>
特殊文字（&lt; &gt;等）をHTMLエスケープする → これは<strong>XSS対策</strong>であり、CSRF対策としては無効
</div>

**有効なCSRF対策**

| 対策                                       | 選択肢          |
| ------------------------------------------ | --------------- |
| CSRFトークン（セッション連動乱数値を検証） | イ ✓            |
| パスワード再入力（重要操作時の追加認証）   | ア ✓            |
| Refererチェック（補助的）                  | ウ ✓            |
| SameSite Cookie属性（Lax/Strict）          | —（選択肢なし） |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
主要ブラウザがSameSite=Laxをデフォルト化し、従来型CSRF攻撃リスクは大幅低減。ただしOWASP Top 10から単独外れただけで脅威は継続。SPA（React/Vue.js）フレームワークでの自動保護への依存度が高まっている。
</div>

---

<!-- _class: sec-header -->

# セキュリティ管理・組織

<p>問12・問13・問14・問15</p>
<div class="qs">MITRE ／ PSIRT ／ UEBA ／ CSPM</div>

---

<!-- _class: has-footer -->

# 問12　MITREの役割

<span class="badge mgmt">セキュリティ管理</span> <span class="badge diff-easy">易</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
CVEの事務局であり、サイバー攻撃のプロセスを記述したナレッジベース（<strong>ATT&CK</strong>）を公開する
</div>

**主要セキュリティ機関の整理**

| 機関                                             | 役割                                                           |
| ------------------------------------------------ | -------------------------------------------------------------- |
| **MITRE** <span class="correct-mark">← ア</span> | CVE管理・ATT&CK・CWE（米国非営利）                             |
| NIST                                             | サイバーセキュリティFW・ガイドライン発行（米国標準技術研究所） |
| ENISA                                            | EU加盟国のサイバーセキュリティ支援（欧州）                     |
| JPCERT/CC                                        | 日本国内インシデント受付・対応支援                             |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
MITRE ATT&CK v15（2024年）でGenAIを悪用した攻撃戦術が追加。SIEM/XDR/脅威ハンティングツールへの統合が標準化。CVEの年間発行件数は増加の一途で、JVN・IPAとの連携も強化されている。
</div>

---

<!-- _class: has-footer -->

# 問13　自社製品の脆弱性に起因するリスクへの対応

<span class="badge mgmt">セキュリティ管理</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：イ　PSIRT</div>
Product Security Incident Response Team ＝ 自社製品・サービスの脆弱性に関するリスク対応
</div>

**セキュリティ組織の役割比較**

| 組織                                             | 対象範囲                                       |
| ------------------------------------------------ | ---------------------------------------------- |
| CSIRT                                            | 自組織が**受ける**サイバー攻撃・インシデント   |
| **PSIRT** <span class="correct-mark">← イ</span> | 自社**製品**の脆弱性（収集・分析・修正・公開） |
| SOC                                              | 自組織ネットワークの監視・検知・分析           |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
IoT・コネクテッドカー・ICS/OTへのサイバー攻撃が急増し、製造業でのPSIRT設立が急務。欧州CRA（Cyber Resilience Act）や米国大統領令で製品セキュリティ要件・脆弱性開示が義務化方向。JPCERTがPSIRT支援ガイドライン・トレーニングを提供。
</div>

---

<!-- _class: has-footer -->

# 問14　UEBAの機能

<span class="badge mgmt">セキュリティ管理</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：エ</div>
利用者や機器の<strong>異常な振る舞いを検知</strong>する（User and Entity Behavior Analytics）
</div>

**UEBAの特徴**

- ユーザ・エンティティの行動パターンを**機械学習**で分析
- 内部不正・アカウント乗っ取り・ラテラルムーブメントの検知に有効
- UBA（User Behavior Analytics）が進化し、エンティティ（サーバ・デバイス等）分析を追加したもの

**他の選択肢との違い**：ア＝生体認証、イ＝アクセス制御、ウ＝DLP/暗号化

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
XDRへの統合でSIEM/EDR/NDRと連携したプラットフォームが主流に。AIによる異常検知精度が向上しSOCアナリストのアラート疲れを軽減。日本の重要インフラ・金融機関で内部不正対策として導入が加速。
</div>

---

<!-- _class: has-footer -->

# 問15　CSPMの機能

<span class="badge mgmt">セキュリティ管理</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：イ</div>
クラウドサービスの設定を継続的に監視し、<strong>不適切な設定（misconfiguration）を検知</strong>する
</div>

**クラウドセキュリティツールの整理**

| ツール                                          | 主な機能                                  |
| ----------------------------------------------- | ----------------------------------------- |
| **CSPM** <span class="correct-mark">← イ</span> | クラウドインフラ設定ミスの検出・修正      |
| CWPP                                            | クラウドワークロード（VM・コンテナ）保護  |
| CASB                                            | クラウドアクセスの可視化・制御            |
| CNAPP                                           | CSPM + CWPP + CIEM の統合プラットフォーム |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
Gartnerは「クラウドセキュリティ失敗の99%は顧客の設定ミス」と指摘。S3バケット・Blobコンテナの設定ミスによる大規模漏洩が多発。CSPMはCNAPPへ統合進化しており、マルチクラウド・ハイブリッドクラウドの一元管理が重要課題に。
</div>

---

<!-- _class: sec-header -->

# ネットワーク・Web技術

<p>問17・問18・問19・問20</p>
<div class="qs">IEEE 802.1X ／ Ajax ／ OSPF ／ HTTPステータスコード</div>

---

<!-- _class: has-footer -->

# 問17　IEEE 802.1Xが規定するもの

<span class="badge net">ネットワーク</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：ア</div>
アクセスポイントが<strong>EAPを使用して</strong>、クライアントを認証する枠組み
</div>

**IEEE 802.1Xの3者構成**

| 役割                      | 機器                     |
| ------------------------- | ------------------------ |
| Supplicant（認証依頼者）  | クライアントPC・デバイス |
| Authenticator（認証装置） | APやスイッチ             |
| Authentication Server     | **RADIUS**サーバ         |

- **EAP（Extensible Authentication Protocol）** で認証
- 企業無線LAN（WPA2/WPA3 Enterprise）で広く採用

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
ゼロトラストで「接続＝信頼」の前提が崩れ、802.1Xの重要性が再評価。WPA3-Enterpriseは802.1Xを強制。IoT機器の急増で802.1X非対応デバイスの管理（NACとの組み合わせ）が課題。SD-WANやSSEとの統合も進行中。
</div>

---

<!-- _class: has-footer -->

# 問18　Ajaxの説明

<span class="badge webtech">Web技術</span> <span class="badge diff-easy">易</span>

<div class="answer-box">
<div class="ans-label">正解：ア　Ajax</div>
JavaScriptを使ったブラウザ内蔵の<strong>非同期通信機能</strong>を利用する技術。ページ全体を再読み込みせずにサーバとデータ交換
</div>

**選択肢の整理**

| 選択肢                                          | 正体                                          |
| ----------------------------------------------- | --------------------------------------------- |
| **Ajax** <span class="correct-mark">← ア</span> | 非同期通信技術（XMLHttpRequest / Fetch API）  |
| CSS                                             | スタイルシート言語                            |
| DOM                                             | ドキュメントオブジェクトモデル（構造操作API） |
| SAX                                             | XMLパーサAPIの方式                            |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
現在はFetch API・WebSocket・SSEが後継として整備。React/Vue.js/AngularなどSPAフレームワーク内に吸収・自動化。セキュリティ観点ではCORS（Cross-Origin Resource Sharing）の誤設定が情報漏洩リスクとして継続。
</div>

---

<!-- _class: has-footer -->

# 問19　OSPFだけに当てはまる特徴

<span class="badge net">ネットワーク</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：イ</div>
<strong>リンク状態のデータベース（LSDB）を使用</strong>する ← RIP-2にはない
</div>

**RIP-2 vs OSPF 比較**

| 比較項目         | RIP-2              | OSPF                         |
| ---------------- | ------------------ | ---------------------------- |
| アルゴリズム     | ディスタンスベクタ | **リンクステート**           |
| メトリック       | ホップ数（最大15） | コスト（帯域幅ベース）       |
| VLSM対応         | ○                  | ○（共通なのでア×）           |
| 更新方式         | 定期（30秒）       | 変化時のみ（LSA）            |
| マルチキャスト   | 224.0.0.9          | 224.0.0.5/6（共通なのでウ×） |
| **リンク状態DB** | **なし**           | **あり（LSDB）← イ○**        |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
SD-WAN台頭後もOSPF/BGPはエンタープライズ・DCのコアプロトコルとして健在。AWS Direct Connect・Azure ExpressRoute等ではBGPが重要。OSPFの認証機能（MD5/SHA）設定がルートインジェクション攻撃対策として重要。
</div>

---

<!-- _class: has-footer -->

# 問20　HTTPステータスコードの説明

<span class="badge net">ネットワーク</span> <span class="badge diff-easy">易</span>

<div class="answer-box">
<div class="ans-label">正解：ウ</div>
300番台は、完了するために<strong>リダイレクトなど更なる動作が必要</strong>なことを意味する
</div>

**HTTPステータスコードの分類**

| コード                                         | 意味                             | 代表例              |
| ---------------------------------------------- | -------------------------------- | ------------------- |
| 1xx                                            | 情報（処理継続中）               | 100 Continue        |
| 2xx                                            | 成功                             | 200 OK, 201 Created |
| **3xx** <span class="correct-mark">← ウ</span> | **リダイレクト（追加動作必要）** | 301, 302 Found      |
| 4xx                                            | クライアントエラー               | 400, 401, 403, 404  |
| 5xx                                            | サーバエラー                     | 500, 503            |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
HTTP/3（QUIC over UDP）がCloudflare・Google等で普及中。RESTful API設計でステータスコードの正確な利用（401 vs 403の使い分け）が必要。エラーレスポンスによる情報漏洩抑制もOWASP API Security Top 10の重要項目。
</div>

---

<!-- _class: sec-header -->

# システム・DB／法律・計算・監査

<p>問21〜問25</p>
<div class="qs">トランザクション ／ 結合テスト ／ 著作権 ／ 可用性計算 ／ システム監査</div>

---

<!-- _class: has-footer -->

# 問21　DBMSがトランザクションのコミット処理を完了するタイミング

<span class="badge system">システム・DB</span> <span class="badge diff-hard">やや難</span>

<div class="answer-box">
<div class="ans-label">正解：エ</div>
<strong>ログファイルへのコミット情報書込み完了時点</strong>（ログバッファへの書込みでは不十分）
</div>

**WAL（Write-Ahead Logging）の処理順序**

```
① アプリが更新命令発行
② バッファプール（メモリ）に反映
③ ログバッファにコミット情報を書き込む
④ ログファイル（永続ストレージ）に書き出す ← ★コミット完了
⑤ バッファプールの内容をデータファイルに書き出す（チェックポイント）
```

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
PostgreSQL/MySQL/SQLiteで広く採用。クラウドマネージドDB（RDS/Azure SQL）でも同原則が適用され、自動フェイルオーバー・PITRの基盤となる。NewSQL（CockroachDB/TiDB/Spanner）ではWAL＋Raft/Paxosで分散耐障害性を実現。
</div>

---

<!-- _class: has-footer -->

# 問22　ソフトウェア結合テスト方式

<span class="badge system">システム・DB</span> <span class="badge diff-hard">やや難</span>

**状況**：アプリ層・ミドルウェア層の単体テスト完了、デバイスドライバ層が**未完了**

<div class="answer-box">
<div class="ans-label">正解：イ　トップダウンテスト</div>
上位層から順に結合。未完成の下位層の代わりに<strong>スタブ（stub）</strong>を使用
</div>

**結合テスト方式の比較**

| 方式                                                    | 進行方向     | 代替物   | 本問への適否                    |
| ------------------------------------------------------- | ------------ | -------- | ------------------------------- |
| **トップダウン** <span class="correct-mark">← イ</span> | 上→下        | スタブ   | **○**（ドライバ層をスタブ代替） |
| ボトムアップ                                            | 下→上        | ドライバ | ×（下位が未完成のため不可）     |
| サンドイッチ                                            | 中間から両方 | 両方     | ×（複雑）                       |
| ビッグバン                                              | 一度に全部   | —        | ×（規模が大きい場合不適）       |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
CI/CDパイプラインでテスト自動化が標準化。DevSecOpsではSAST/DAST/SCAをテストパイプラインに組み込むことが必須。AIを活用した自動テスト生成（GitHub Copilot等）も登場。
</div>

---

<!-- _class: has-footer -->

# 問23　著作権の帰属先

<span class="badge law">法律・著作権</span> <span class="badge diff-std">標準</span>

**状況**：開発請負契約書に著作権帰属の取り決めが**ない**場合

<div class="answer-box">
<div class="ans-label">正解：ウ　請負人に帰属する</div>
著作権法第17条：著作権は<strong>著作物を創作した者（著作者）</strong>に原始帰属する
</div>

**ポイント**

- 契約に定めがない → 実際に開発した**請負人に帰属**
- 注文者に帰属させたいなら **「著作権の譲渡条項」** を契約書に明記
- 従業員が業務で作成した場合 → 法人著作（職務著作）として**使用者（会社）**に帰属する可能性

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
GitHub Copilot等のAIが生成したコードの著作権帰属が新たな法的論点に。各国でAI生成物への著作権立法論議が継続中。SBOMの普及でOSSライセンス管理（GPL/MIT等）の重要性も増大。
</div>

---

<!-- _class: has-footer -->

# 問24　サービス可用性の計算

<span class="badge calc">計算問題</span>

**条件：4月1日〜6月30日 ／ バージョンアップ停止（84時間）はサービス提供時間に含めない**

<div class="answer-box">
<div class="ans-label">正解：ウ　99.52%</div>
</div>

**計算過程**

| 項目                         | 計算                     | 結果          |
| ---------------------------- | ------------------------ | ------------- |
| 期間の総時間                 | (30＋31＋30) 日 × 24時間 | **2,184時間** |
| バージョンアップ停止（除外） | —                        | −84時間       |
| **サービス提供時間（分母）** | 2,184 − 84               | **2,100時間** |
| ハードウェア故障停止         | —                        | −10時間       |
| **サービス稼働時間（分子）** | 2,100 − 10               | **2,090時間** |
| **可用性**                   | 2,090 ÷ 2,100 × 100      | **99.52%**    |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
クラウドSLAでは99.9〜99.99%（スリー〜フォーナイン）が標準。ファイブナイン（99.999%、年間約5分のダウンタイム）が求められるシステムも増加。マルチリージョン・アクティブ-アクティブ構成（HA）がクラウドアーキテクチャの標準に。
</div>

---

<!-- _class: has-footer -->

# 問25　システム監査基準（令和5年）のリスク評価に基づく監査計画

<span class="badge audit">監査</span> <span class="badge diff-std">標準</span>

<div class="answer-box">
<div class="ans-label">正解：エ</div>
組織体内外の<strong>環境変化によってリスクが相当程度変化した</strong>場合には、監査計画の見直しを検討し、必要に応じて変更する
</div>

**選択肢の誤りポイント**

| 選択肢 | 誤りの理由                                             |
| ------ | ------------------------------------------------------ |
| ア     | 監査リスクを「完全に回避」は不可能。許容水準を設定する |
| イ     | リスク・アプローチは均等配分ではなく**重点配分**       |
| ウ     | 監査リスクの三要素は「固有・統制・発見」               |

<div class="trend-box">
<div class="trend-label">情報分野の情勢</div>
令和5年基準改訂ではAI・クラウド・サプライチェーンリスクへの対応が強化。ISO/IEC 27001・SOC2・ISAE3402との整合性も求められる。クラウド設定監査・ペネトレーションテスト結果活用・インシデント対応能力評価が現代的な監査テーマに。
</div>

---

<!-- _class: sec-header -->

# 出題傾向まとめと学習指針

---

<!-- _class: has-footer -->

# 重点学習分野

<div class="cols">
<div>

| 優先度                             | 分野                         |
| ---------------------------------- | ---------------------------- |
| <span class="star-high">★★★</span> | 攻撃手法（最新含む）         |
| <span class="star-high">★★★</span> | セキュリティ管理ツール・組織 |
| <span class="star-high">★★★</span> | 暗号技術（PQC含む）          |
| <span class="star-mid">★★☆</span>  | 認証・PKI                    |
| <span class="star-mid">★★☆</span>  | Webセキュリティ              |
| <span class="star-mid">★★☆</span>  | ネットワーク基礎             |
| <span class="star-low">★☆☆</span>  | 計算・法律・監査             |

</div>
<div>

**優先学習の根拠**

- 攻撃手法：毎回4問前後、最新手法まで出題
- 管理ツール：UEBA・CSPM等クラウド系が近年急増
- 暗号：PQCは今後も継続出題が確実視
- 認証：毎回コンスタントに3問前後
- 基礎技術：36%を占め無視できない

> 計算・法律・監査は各1問。基礎を確認し確実に取る。

</div>
</div>

---

<!-- _class: has-footer -->

# 近年の新傾向キーワード

今後も出題が予想される新興トピック：

<div class="cols">
<div>

**AI/MLセキュリティ**
<span class="chip">モデルインバージョン</span>
<span class="chip">ポイズニング攻撃</span>
<span class="chip">モデル抽出攻撃</span>
<span class="chip">敵対的サンプル</span>
<span class="chip">MITRE ATLAS</span>

**耐量子暗号（PQC）**
<span class="chip">ML-KEM (FIPS 203)</span>
<span class="chip">ML-DSA (FIPS 204)</span>
<span class="chip">格子暗号</span>
<span class="chip">CNSA 2.0</span>

**クラウドセキュリティ**
<span class="chip">CSPM</span>
<span class="chip">CWPP</span>
<span class="chip">CASB</span>
<span class="chip">CNAPP</span>
<span class="chip">CIEM</span>

</div>
<div>

**ゼロトラスト**
<span class="chip">SDP</span>
<span class="chip">IAP</span>
<span class="chip">マイクロセグメンテーション</span>
<span class="chip">SSE</span>

**サプライチェーンセキュリティ**
<span class="chip">SBOM</span>
<span class="chip">ソフトウェアサプライチェーン</span>
<span class="chip">Coordinated Vulnerability Disclosure</span>

**脅威インテリジェンス**
<span class="chip">MITRE ATT&CK</span>
<span class="chip">STIX/TAXII</span>
<span class="chip">XDR</span>
<span class="chip">脅威ハンティング</span>

</div>
</div>

---

<!-- _class: has-footer -->

# 参照規格・ドキュメント　＋　正解一覧

<div class="cols">
<div>

**主要参照規格**

| 規格/文書                    | 関連問 |
| ---------------------------- | ------ |
| CRYPTREC暗号リスト           | 問1    |
| NIST PQC（FIPS 203/204/205） | 問3    |
| NIST SP 800-63-3             | 問11   |
| MITRE ATT&CK                 | 問12   |
| IEEE 802.1X                  | 問17   |
| システム監査基準（令和5年）  | 問25   |

</div>
<div>

**正解一覧**

|  問   |   正   |  問   |   正   |  問   |   正   |
| :---: | :----: | :---: | :----: | :---: | :----: |
|   1   | **ウ** |  10   | **イ** |  19   | **イ** |
|   2   | **イ** |  11   | **ア** |  20   | **ウ** |
|   3   | **エ** |  12   | **ア** |  21   | **エ** |
|   4   | **エ** |  13   | **イ** |  22   | **イ** |
|   5   | **ア** |  14   | **エ** |  23   | **ウ** |
|   6   | **イ** |  15   | **イ** |  24   | **ウ** |
|   7   | **ア** |  16   | **エ** |  25   | **エ** |
|   8   | **ア** |  17   | **ア** |       |        |
|   9   | **エ** |  18   | **ア** |       |        |

</div>
</div>

---

<!-- _class: title -->

# 合格を目指して

## 試験の傾向を押さえ、着実に得点を積み重ねよう

<div class="subtitle">令和7年度 秋期 情報処理安全確保支援士試験 午前Ⅱ 分析資料</div>
