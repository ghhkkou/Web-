# Web Technology Learning - Java/Spring Boot版

このリポジトリは、『[改訂新版] プロになるためのWeb技術入門』の Go サンプルコードを、**Java/Spring Boot** で再実装したものです。

## ブランチ構成

- `v1-latest`: 元の Go サンプルコード
- `java-samples`: Java/Spring Boot 版のサンプルコード（本ブランチ）

## Chapter 6: 従来型の Web アプリケーション

### 段階的なサンプル

1. **simple-webserver1** - 文字列を返す基本的な Web アプリケーション
   - Spring Boot REST コントローラーで「Hello, Web application!」を返す

2. **simple-webserver2** - ファイルの内容を返す Web アプリケーション
   - 静的ファイルサーブ機能

3. **tinytodo-01-base** - 固定の ToDo を表示
   - 固定データをテンプレートで表示

4. **tinytodo-02-add** - ToDo を追加できるように
   - フォーム送信で ToDo を追加

5. **tinytodo-03-prg** - Post-Redirect-Get パターン
   - 追加後にリダイレクト

6. **tinytodo-04-session** - セッション管理
   - ユーザーごとに異なる ToDo リストを管理

7. **tinytodo-05-user-final** - ユーザー管理機能
   - アカウント作成、ログイン、ユーザーごとの ToDo 管理

## 技術スタック

- **Java 17**
- **Spring Boot 3.2.0**
- **Spring Data JPA**
- **H2 Database** (開発用埋め込みデータベース)
- **Thymeleaf** (テンプレートエンジン)
- **Maven** (ビルドツール)

## セットアップと実行

### 前提条件
- Java 17 以上
- Maven 3.6 以上

### プロジェクト構造

```
project/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── jp/littleforest/webtech/
│   │   │       ├── Application.java
│   │   │       ├── chapter06/
│   │   │       │   ├── SimpleWebServer1/
│   │   │       │   ├── SimpleWebServer2/
│   │   │       │   ├── TinyTodo01Base/
│   │   │       │   ├── TinyTodo02Add/
│   │   │       │   ├── TinyTodo03Prg/
│   │   │       │   ├── TinyTodo04Session/
│   │   │       │   └── TinyTodo05UserFinal/
│   │   └── resources/
│   │       ├── application.yml
│   │       └── templates/
│   └── test/
└── README.md
```

## ビルドと実行

```bash
# プロジェクトビルド
mvn clean package

# 実行
mvn spring-boot:run
```

アプリケーションは `http://localhost:8080` で起動します。

## 各サンプルの詳細

詳細は各サンプルディレクトリの README.md をご参照ください。

## ライセンス

MIT License
