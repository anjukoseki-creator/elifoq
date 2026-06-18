<p align="center">
  <img src="icon-512.png" width="100" alt="Elifoq アイコン" />
</p>

<h1 align="center">Elifoq（エリフォク）</h1>

<p align="center">
  <b>Everyday Life Is Full Of Questions</b><br>
  日常の「なぜ？」に答えると、AIが正解判定をせずに視点を広げてくれる思考力トレーニングアプリ
</p>

<p align="center">
  <a href="https://anjukoseki-creator.github.io/elifoq/">
    <img src="https://img.shields.io/badge/%E2%96%B6%20Live%20demo-online-2E6DB4?style=for-the-badge" alt="Live demo" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/AI-Gemini%202.5%20Flash-4285F4?logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/Host-GitHub%20Pages-222?logo=github" />
  <img src="https://img.shields.io/badge/backend-none%20(BYOK)-2E9E5B" />
  <img src="https://img.shields.io/badge/license-MIT-green" />
</p>

---

## ▶ 触ってみる

**[https://anjukoseki-creator.github.io/elifoq/](https://anjukoseki-creator.github.io/elifoq/)**

設定画面で自分の Gemini APIキー（無料）を登録すると、実際に AI が採点・フィードバックを返します。インストール不要、スマホでもPCでもそのまま動きます。

## 📱 画面

<p align="center">
  <img src="preview-home.png" width="270" alt="ホーム：ジャンル別の問題集" />
  &nbsp;&nbsp;&nbsp;
  <img src="preview-feedback.png" width="270" alt="AIフィードバック：8項目の採点と模範回答" />
</p>

<p align="center"><sub>左：ジャンルから問題を選ぶ　／　右：8項目の採点・別視点・模範回答・発展質問</sub></p>

## 🎯 コンセプト

身近な「なぜ？」に自分なりの答えを書くと、AIが **正解判定をせず** に視点を広げて返してくれる。
クイズアプリが「正解を覚える」のに対し、Elifoqは「**考え方を学ぶ**」ことに特化しています。

| | 一般的なクイズアプリ | **Elifoq** |
|---|---|---|
| ゴール | 正解を覚える | 考え方の幅を増やす |
| AIの役割 | 採点して終わり | 視点を広げるコーチ |
| 体験 | ○×が出る | 別の切り口・模範回答・発展質問が返る |

就活のケース面接対策・ロジカルシンキングの習慣化を主なターゲットにしています。

## ✨ 主な機能

- **ジャンル別 問題集（全48問）** — マーケ / IT・SIer / 経営 / 心理学 / 社会 / 身近な謎。好きな問題に何問でも挑戦できる。
- **8項目の思考採点（10点満点）** — 問題定義力・論理性・多角性・具体性・問題分解力・仮説を立てる力・数字感覚・創造力を、それぞれスコアと講評で可視化。
- **模範回答例** — 筋の良い回答例を提示。
- **発展質問に連続回答** — 返ってきた問いにそのまま答えて、思考をさらに深掘りできる。
- **思考履歴** — 過去の回答とフィードバックを端末に保存して振り返り。
- **BYOK（Bring Your Own Key）** — ユーザー自身の Gemini APIキーで動作。鍵はブラウザ内にのみ保存し、外部サーバーには一切送らない。

## 🏗 仕組み

```
ブラウザ（Elifoq / 単一HTML）
   ├─ APIキーは localStorage に保存（外部送信なし）
   └─ ユーザーのキーで Gemini API を直接呼ぶ → 構造化JSONのフィードバック
```

- **バックエンドなし** — GitHub Pages 上の静的な単一HTMLだけで完結。サーバー費ゼロ。
- **無料で動く** — Gemini の Flash 系は無料枠（カード登録不要）。この用途なら実質0円。
- **安全** — 共有キーを埋め込まないため「鍵流出で高額請求」のリスクがない。鍵は各ユーザー自身のもの。

## 🧰 技術スタック

| 項目 | 採用 |
|---|---|
| フロント | Vanilla JavaScript（単一 `index.html`、依存ライブラリなし） |
| AI | Google Gemini API（`gemini-2.5-flash`、`responseSchema` でJSON固定） |
| 鍵・履歴の保存 | localStorage |
| ホスティング | GitHub Pages |
| PWA | manifest + アイコン（ホーム画面に追加可能） |

## 🚀 ローカルで動かす

```bash
git clone https://github.com/anjukoseki-creator/elifoq.git
cd elifoq
# index.html をブラウザで開くだけ。ビルド不要。
```

起動後、設定画面で [Google AI Studio](https://aistudio.google.com/app/apikey) のキー（無料）を登録してください。

## 🗺 ロードマップ

- [x] ジャンル別問題集（48問）
- [x] 8項目の思考採点・模範回答・発展質問への連続回答
- [x] 思考履歴 / BYOK / アプリアイコン
- [ ] 視点コレクション（使った視点を図鑑のように収集）
- [ ] 思考レーダーチャート（ジャンル別の傾向を可視化）
- [ ] みんなの回答（匿名公開）

## 📄 ライセンス

MIT License — [LICENSE](LICENSE)

---

<p align="center"><sub>個人開発のポートフォリオ作品です。</sub></p>
