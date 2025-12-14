# ポートフォリオLP（公開用）

制作会社さま向けの1ページLP。Figmaデザインをもとに、HTML5＋SCSSで静的に構築し、GA4＋GTMで計測できる状態を前提にしています。

## サイト概要
- LP目的：LPコーディング＋GA4/GTM実装の外部パートナー紹介
- 技術：HTML5 / SCSS / npm scripts / BrowserSync（静的ホスティング想定）
- アクセシビリティ：alt・aria属性を付与、3段階レスポンシブ対応

## 計測まわり（GA4＋GTM）
- GTMスニペットは `GTM-XXXXXXX` をプレースホルダーとして設置（実運用IDは環境変数や配信側で差し込み）
- 主要イベント：cta_click / nav_click / scroll_50 / scroll_90 / form_start / form_submit / tel_click / email_click
- data-attributeベースで計測IDを整理済み（`data-gtm-event`、`data-gtm-section` など）

## libecityからのトラフィック実績
- 副業コミュニティ「libecity」経由の紹介流入が継続的に発生
- リファラ経由での相談・DMが多く、ポートフォリオ経由のリード獲得に寄与
- 計測はGA4でドメイン横断せず、GTMイベントで遷移後のCTA動きを把握

## セットアップ
1. 依存インストール（ロックファイルあり）
   - `npm install`
2. 開発サーバー（Sass監視＋BrowserSync）
   - `npm run dev`
3. ビルド（SCSS→CSS）
   - `npm run build`

## 公開チェックリスト（自分確認用）
- [x] .env / 秘匿情報を含むファイルは同梱していない
- [x] GTM・GA4のIDはプレースホルダーに差し替え
- [x] クライアント案件や取引先固有のデータを含むディレクトリは除外
- [x] node_modules など生成物は .gitignore で除外
- [x] 公開に不要な旧バージョン（oldディレクトリなど）は含めていない
