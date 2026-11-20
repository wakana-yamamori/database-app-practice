# database-app-practice

## 概要

COACHTECH 教材 Tutorial 9-3「データベース操作ハンズオン演習」で作成した成果物です。
マイグレーション、シーダー、クエリビルダを活用し、商品管理システムの商品一覧表示機能を実装しました。

## 使用技術

- PHP 8.x
- Laravel 10.x
- Laravel Sail / Docker
- MySQL
- マイグレーション、シーダー、クエリビルダ（`DB` ファサード）

## 学んだこと

- マイグレーションファイル（`Schema::create`）を使って、テーブル定義やデフォルト値（`stock` のデフォルト `0` など）をコードで管理する方法
- シーダー（`ProductSeeder`）を作成し、テストデータを一括投入する流れ
- コントローラーでクエリビルダ（`DB::table('products')->get()`）を使ってデータを取得し、Bladeテンプレートへ渡して一覧表示する方法
- スペルミスによるエラーの原因特定
- シーダー重複した時のリセット方法(migrate:freshを使用しました。)

## 動作確認

1. プロジェクトディレクトリに移動し、Sailを起動します。
   ```bash
   ./vendor/bin/sail up -d
   ```
2. http://localhost/productsを開き、「全5件の商品があります。」と表示され、1件ずつ確認できます。
   ![商品一覧画面]<img width="1470" height="956" alt="スクリーンショット 2026-11-20 6 21 07" src="https://github.com/user-attachments/assets/1b8cf1ce-ec78-45fc-b420-efbde0d34934" />
