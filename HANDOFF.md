# 引き継ぎメモ

## プロジェクト概要

推し活グッズ BtoB ECサイトの要件定義書・画面遷移図・画面設計書・ワイヤーフレームを作成中。

## リポジトリ

- GitHub: https://github.com/Yusuke-holospace/ec-docs (public)
- GitHub Pages: https://yusuke-holospace.github.io/ec-docs/
- ローカル: `/Users/yusukeoniyanagi/Claude Code/ec-docs`

## ファイル構成

```
ec-docs/
├── requirements.md          # 要件定義書
├── screen-flow.md            # 画面遷移図
├── screen-design/            # 画面設計書
│   ├── c-01-top.md
│   ├── c-02-product-list.md
│   ├── c-03-product-detail.md
│   ├── c-04-cart.md
│   ├── c-05-upload.md
│   ├── c-06-confirm.md
│   ├── c-07-complete.md
│   ├── c-08-login.md
│   ├── c-09-register.md
│   ├── c-10-mypage.md
│   ├── c-11-profile.md
│   ├── c-12-orders.md
│   ├── c-13-order-detail.md
│   ├── c-14-contact.md
│   ├── c-15-faq.md
│   ├── c-16-guide.md
│   ├── c-17-19-legal.md
│   └── c-20-404.md
└── wireframes/               # ワイヤーフレーム（HTML）
    ├── c-01-top.html / -sp.html
    ├── c-02-product-list.html / -sp.html
    ├── c-03-product-detail.html / -sp.html
    ├── c-04-cart.html / -sp.html
    ├── c-05-upload.html / -sp.html
    ├── c-06-confirm.html / -sp.html
    ├── c-07-complete.html / -sp.html
    ├── c-08-login.html（PC/SP共通）
    ├── c-09-register.html（PC/SP共通）
    ├── c-10-mypage.html / -sp.html
    ├── c-11-profile.html / -sp.html
    ├── c-12-orders.html / -sp.html
    ├── c-13-order-detail.html / -sp.html
    ├── c-14-contact.html / -sp.html
    ├── c-15-faq.html / -sp.html
    ├── c-16-guide.html / -sp.html
    ├── c-17-terms.html / -sp.html
    ├── c-18-privacy.html / -sp.html
    ├── c-19-legal.html / -sp.html
    └── c-20-404.html / -sp.html
```

## 完了状況

### 購入者向け画面（C-01〜C-20）

| 画面 | PC | SP | 設計書 | 状態 |
|------|----|----|--------|------|
| C-01 トップページ | done | done | done | 完了 |
| C-02 商品一覧ページ | done | done | done | 完了 |
| C-03 商品詳細 | done | done | done | 完了 |
| C-04 カート | done | done | done | 完了 |
| C-05 入稿 | done | done | done | 完了 |
| C-06 注文確認 | done | done | done | 完了 |
| C-07 注文完了 | done | done | done | 完了 |
| C-08 ログイン | done | 共通 | done | 完了 |
| C-09 会員登録 | done | 共通 | done | 完了 |
| C-10 マイページ | done | done | done | 完了 |
| C-11 会員情報 | done | done | done | 完了 |
| C-12 注文履歴 | done | done | done | 完了 |
| C-13 注文詳細 | done | done | done | 完了 |
| C-14 問い合わせ | done | done | done | 完了 |
| C-15 FAQ | done | done | done | 完了 |
| C-16 ご利用ガイド | done | done | done | 完了 |
| C-17 利用規約 | done | done | done | 完了 |
| C-18 プラポリ | done | done | done | 完了 |
| C-19 特商法 | done | done | done | 完了 |
| C-20 404 | done | done | done | 完了 |

### 管理者向け画面（A-01〜A-10）

全て**未着手**。画面遷移図（screen-flow.md）に画面一覧と遷移詳細は定義済み。

## 次のタスク

1. **C-01 トップページ** — PC/SP版ワイヤーフレーム＋画面設計書
2. **C-02 商品一覧ページ** — PC/SP版ワイヤーフレーム＋画面設計書
3. **管理者画面（A-01〜A-10）** — ワイヤーフレーム＋画面設計書

## 重要な設計ルール

### PCワイヤーフレーム
- ヘッダー2段構成: 1段目（ロゴ・検索・ユーティリティリンク・カートアイコン）、2段目（カテゴリナビ・ホバーでドロップダウン）
- パンくずリスト: ヘッダー下＋フッター直上（隙間なし）
- ログイン/マイページ: 未ログイン「ログイン」、ログイン済み「マイページ」に切替
- カートアイコン: プレースホルダー（iconテキスト）＋バッジ
- フッター: 商品カテゴリ・サポート・法的情報の3カラム

### SPワイヤーフレーム
- max-width: 390px
- ヘッダー: ロゴ＋ログイン/カート/メニュー（アイコン＋テキスト）＋検索バー
- パンくずなし
- タップ領域: 全要素44px以上
- ドラッグ&ドロップなし（ファイル選択ボタンのみ）
- タブ → アコーディオン
- 関連商品: グリッド → 横スクロール
- 絵文字使用禁止

### 共通
- アイコンはプレースホルダー（「icon」テキスト）
- 価格は税込表示
- 送料は商品ごとに設定、カートで合算、N円以上で無料
- カートに追加はログイン不要、入稿・注文確定時にログイン必要
- 会社情報登録はスキップ可能、入稿・注文確定時に未登録ならC-11に遷移
- サンプル制作: 1式（10個）、式数変更可能
- 入稿スロット: 1スロット=1ファイル、オプション連動で表示/非表示
- ライセンス同意: C-06（注文確認ページ）で1回のみ
- 支払い方法: クレカ（Stripe）、銀行振込、請求書払い。C-06で選択
- 決済はこの時点では発生しない旨を複数箇所に明記

## 参考サイト
- Casetify（カスタム商品EC）
- 無印良品（シンプルなデザイン）
- Amazon（UXの基準）
- 販促スタイル（同業種のBtoB EC）
