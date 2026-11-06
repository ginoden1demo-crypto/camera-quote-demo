# 防犯カメラ WEB自動見積｜共有テスト版

カメラ台数・解像度・配線距離・工事条件を選ぶと、概算見積もりが即時に変化する、ブラウザだけで動く静的HTMLです。

> **公開試験版**：掲載価格は検証用の仮単価であり、見積依頼や写真・個人情報は一切サーバーへ送信されません。現場写真、実名、実際のメールアドレスなどは入力しないでください。

## GitHub Pages 公開手順

1. GitHubにログインして **New repository** をクリック。
2. リポジトリ名は `camera-quote-demo` などを入力。無料のGitHubアカウントでは **Public** にします。 `Add a README file` は選ばず作成します（READMEもアップロードします）。
3. リポジトリで **Add file → Upload files** を選び、このフォルダ内の `index.html`、`.nojekyll`、`README.md`、`TEST_GUIDE.md` をアップロードします。`.nojekyll` は隠しファイルです。最低限 `index.html` だけでも動きます。
4. **Commit changes** で `main` ブランチへ保存。
5. リポジトリの **Settings → Pages → Build and deployment** で、**Source: Deploy from a branch**、**Branch: main / (root)** にして **Save**。
6. Pages画面の **Visit site** から公開URLを確認し、テスターへ共有します。URLの形式は通常 `https://<ユーザー名>.github.io/camera-quote-demo/` です（ユーザー名や最終URLはGitHub側で確認してください）。

GitHub公式手順： https://docs.github.com/ja/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## テスト範囲

- 住宅・店舗・アパート・駐車場の切り替え
- カメラ画質、台数、録画方法
- 配線距離、RC、屋外、高所などの工事条件
- 見積明細、税込額、月額オプション
- 写真の端末内プレビュー（外部送信なし）
- 見積コピー、印刷/PDF、デモ送信（外部送信なし）
- 端末や不具合コメントを含むテスト結果のコピー

## 注意事項

- 公開ページは誰でも閲覧可能です。**パスワード制限・管理者認証はありません**。管理者風の価格編集画面もデモ機能で、誰でもローカル表示中の単価を変更できますが、他の閲覧者には反映されません。
- 顧客情報の保存、写真アップロード、問い合わせメール送信、共有データベース、テスター別ログ収集などは未実装です。
- テスターからのフィードバックは「見積条件＋操作結果をコピー」から、別途メールやチャットに貼り付けて回収してください。
- GitHub Pagesは静的サイトのホスティングです。顧客情報の本番受付には、サーバー側の実装・認証・安全管理が必要です。
- 検索エンジンへの掲載を抑える `noindex` メタ情報を指定していますが、公開ページへのアクセス制限にはなりません。
