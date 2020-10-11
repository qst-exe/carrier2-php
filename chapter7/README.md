# Chapter7

PHPフレームワーク「Laravel」を使ってアプリ開発を行います。

## Laravelのインストール

Laravelインストーラのダウンロード(composerのインストールが必須です)
```
$ composer global require laravel/installer
```

プロジェクトの作成
```
$ composer create-project "laravel/laravel=7.*" todo
```

Laravelサーバの起動
```
$ php artisan serve
```

Laravelで作ったアプリケーションは以下のURLから閲覧できます。

http://localhost:8000/

## GitHubでのリポジトリ作成

今まではForkしてリポジトリを作っていましたが、これからは各個人のアカウントに直接リポジトリを作ってください。

## テーブルの作成

テーブルの作成

```
$ php artisan make:migration create_todos_table
```

マイグレーション

```
$ php artisan migrate
```

## Seederの作成

seederの作成
```
$ php artisan make:seeder TodoTableSeeder
```

seederの実行
```
$ php artisan db:seed
```

## Todo一覧の作成

![Todo一覧の作成](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/36927/aaed0d55-aae9-eb3c-150e-987f30e9b22e.jpeg "Todo一覧の作成")

Todoモデルの作成
```
$ php artisan make:model Todo
```

Todoコントローラーの作成
```
$ php artisan make:controller TodoController --resource 
```

### 各リソースコントローラのアクション

[リソースコントローラ](https://readouble.com/laravel/7.x/ja/controllers.html#resource-controllers)

Todo一覧ページのView

[resources/views/todo/index.blade.php](https://raw.githubusercontent.com/qst-exe/c2-laravel-todo/99f74d4c268371aac47d968b4cca3b170117617d/resources/views/todo/index.blade.php)

## Todo単体ページの作成

![Todo単体ページの作成](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/36927/ce867ccc-a868-3b11-7840-9b2d53ff790f.jpeg "Todo単体ページの作成")

[resources/views/todo/show.php](https://raw.githubusercontent.com/qst-exe/c2-laravel-todo/4bf89ada0e4ac64212c83be0af75a6ca2a672d0f/resources/views/todo/show.blade.php)

## ページネーションの追加

![ページネーションの追加](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/36927/64fa6560-2a36-55d5-27b2-17c8a7192869.jpeg "ページネーションの追加")