# Nuclear Fusion Power Generation Stocks Landing Page

核融合発電関連銘柄の投資情報を提供するランディングページです。

## 機能

- 🇯🇵 **IP地域制限**: 日本国内からのアクセスのみ許可
- 📊 **銘柄情報**: 核融合発電関連銘柄10選の詳細データ
- 📱 **レスポンシブデザイン**: モバイル・デスクトップ対応
- 🎨 **多色タイトル**: 視覚的に魅力的なデザイン
- 📈 **Google Analytics**: コンバージョン追跡機能
- 🔗 **LINE連携**: 自動リダイレクト機能

## 技術スタック

- HTML5
- CSS3 (Flexbox, Grid, Animations)
- JavaScript (ES6+)
- jQuery
- Vercel (デプロイメント)

## ファイル構成

```
vercel1/
├── index.html          # メインページ
├── contact.html        # リダイレクトページ
├── assets/            # 静的リソース
│   ├── tubiao@2x.png  # LINEアイコン
│   ├── jquery-3.5.1.min.js.下载
│   └── js             # Google Analytics
├── vercel.json        # Vercel設定
├── package.json       # プロジェクト設定
└── README.md          # このファイル
```

## デプロイメント

### Vercelでのデプロイ

1. GitHubリポジトリにプッシュ
2. Vercelでリポジトリをインポート
3. 自動デプロイ完了

### ローカル開発

```bash
npm install
npm run dev
```

## 環境変数

以下の環境変数を設定してください：

- `ANALYTICS_TRACKING_ID`: Google Analytics追跡ID

## ライセンス

MIT License

## 連絡先

- サイト: ねこじの株式投資
- LINE: プロフィール欄のリンクからアクセス
