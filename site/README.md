# MatomeDrop 公式サイト

既存の `manosukemac/matomedrop-privacy` のGitHub Pagesに追加する静的サイトです。
公開履歴は `main` の `pages build and deployment`。既存のルートPrivacy (`index.html`) とSupport (`support.html`) は変更しません。

- 日本語: https://manosukemac.github.io/matomedrop-privacy/site/
- English: https://manosukemac.github.io/matomedrop-privacy/site/en/

## 更新とプレビュー

リポジトリのルートで `python3 -m http.server 8765 --bind 127.0.0.1` を実行し、`/site/` と `/site/en/` を確認します。ビルド不要です。確認後にmainへ反映すると、既存GitHub Pagesフローが配信します。

App Storeリンクは `site-config.json` と両HTMLの `data-app-store` リンクを揃えて更新します。HTMLのリンクはJavaScript無効でも使えます。公開パスを変更する場合はcanonical、hreflang、OGPも更新します。

## デザインと素材

トップはコピーとApple公式バッジが中心。デバイス紹介は共有前の確認説明の直後に配置し、各プロモーション画像は1回だけ表示します。削除済みの重複画像は戻していません。コピー、画像、配色は維持しています。

`asset-sources.json` に既存素材のSHA-256を記録しています。画像とApple公式バッジは無改変です。

Apple公式バッジ: https://toolbox.marketingtools.apple.com/api/v2/badges/download-on-the-app-store/black/ja-jp （英語はen-us）

## 公開前確認

日英の1440×900、390×844表示、見出し構造、画像alt、FAQのキーボード操作、フォーカス、言語切替、メタ情報、相対パスを確認。外部解析SDK、トラッキング、外部フォントは追加していません。実機全機種・全ブラウザやスクリーンリーダーの網羅試験は含みません。

Marketing URLには言語ごとの上記URLを使用できます。Support URLとPrivacy Policy URLは既存URLを維持します。
