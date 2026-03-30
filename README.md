# ECショップ (FRONTIER)

## プロジェクト概要

このプロジェクトは、ASP.NET Core MVCを使用して開発されたECショッピングアプリケーションです。
商品の閲覧・購入・カート管理・注文履歴・管理者パネル・決済機能・ユーザー認証機能を提供します。

## 機能

- ユーザー認証（登録、ログイン、ログアウト）
- 商品一覧表示
- 商品詳細表示
- 商品購入機能
- カート機能
- 注文履歴
- 管理者パネル
- 決済機能
- 在庫管理
- エラーハンドリング

## 技術スタック

- ASP.NET Core MVC（.NET 8.0）
- Entity Framework Core 8.0
- SQLite
- Bootstrap
- C#
- BCrypt.Net（パスワードハッシュ化）

## 環境構築

### 前提条件

- .NET SDK 8.0 以上
- Visual Studio または Visual Studio Code

### インストール手順

#### 1. リポジトリをクローン
```bash
git clone https://github.com/SunnyDayService321/frontier-ec-shop.git
cd frontier-ec-shop
```

#### 2. 依存関係のインストール
```bash
dotnet restore
```

#### 3. データベースの初期化
```bash
dotnet ef database update
```

※ 初回起動時にテスト商品データが自動で投入されます。

#### 4. アプリケーションの起動
```bash
dotnet run
```

ブラウザで https://localhost:5001 にアクセスしてください。

## 主な機能詳細

### ユーザー認証

- 新規ユーザー登録
- ログイン / ログアウト
- パスワードの BCrypt ハッシュ化
- Cookie認証
- 入力バリデーション

### 製品管理

- 商品一覧表示
- 商品詳細表示
- 在庫管理
- 論理削除対応

### 注文処理

- カート機能
- 商品購入
- 在庫数自動更新
- 注文履歴ページ
- 決済機能

### 管理者パネル

- 商品の登録・編集・削除
- 在庫管理
- 注文管理

### データベース

- SQLite を使用
- Entity Framework Core によるデータアクセス
- 初回起動時のシードデータ自動投入

## 📁 ディレクトリ構成
```
frontier-ec-shop/
├── Controllers/          # コントローラー（Product, Cart, Account, Admin）
├── Models/               # データモデル（Product, User, Order）
├── Views/                # Razorテンプレート
├── Data/                 # DBコンテキスト（MvcMovieContext）
├── Migrations/           # EFマイグレーションファイル
├── Properties/           # 起動設定
├── wwwroot/              # 静的ファイル（CSS, JS, 画像）
├── Program.cs            # アプリケーションエントリーポイント
├── appsettings.json      # 設定ファイル
├── first_asp_app.csproj  # プロジェクト定義
└── README.md
```
