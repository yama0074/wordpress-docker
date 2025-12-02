# WordPress Docker Environment

Docker Compose を使って WordPress の開発環境を構築しました。  
公式 WordPress Docker イメージ（wordpress:latest）を使用しており、内部的には Apache サーバが動作しています。  
DB は MariaDB、管理画面用に phpMyAdmin も立てています。  

---

## 技術スタック
- Docker
- Docker Compose
- WordPress (PHP-Apache)
- MariaDB
- phpMyAdmin

---

## サービス構成
- **wordpress**: WordPress 本体、Apache サーバ  
- **db**: MariaDB データベース  
- **phpmyadmin**: DB 管理用 Web インターフェース

---

## 起動方法

1. プロジェクトフォルダに移動
```powershell
cd "C:\Users\namel\wordpress-docker"
```
2. Docker Compose でコンテナを起動
```powershell
docker-compose up -d
```
3. ブラウザでアクセス

- WordPress: http://localhost:8000
- phpMyAdmin: http://localhost:8080

（ユーザー: root / パスワード: rootpass）
## ディレクトリ構造

wordpress-docker/
 ├─ docker-compose.yml
 ├─ wp-data/          ← WordPress のデータ（テーマ・プラグイン）
 ├─ db_data/          ← DB データ（GitHub には含めない）
 └─ README.md

## 学んだこと

- マルチコンテナ構成の理解
- Docker Compose による環境定義
- Web サーバ (Apache) と DB (MariaDB) の連携
- 開発環境をコードで管理する重要性
- phpMyAdmin を使った DB 管理方法
