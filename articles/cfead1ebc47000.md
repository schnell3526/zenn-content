---
title: "laravel8まとめ"
emoji: "🗂"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [laravel]
published: false
---

# データベース関係

## seederの作成

データベースに初期値を代入したい時はseederを設定する。例として`users`テーブルの初期値挿入を考える。

```bash
php artisan make:seeder FoobarsTableSeeder
```

でseederファイルが`/database/seeders`に作られるので`UsersTableSeeder.php`の中の`run()`に以下を記入する。

```php
DB::table('users')->insert([
            'name' => 'hogehoge',
            'email' => 'hogehoge@fuga.com',
            'password' => bcrypt('password'),
            'created_at' => Carbon::now(),
            'updated_at' => Carbon::now(),
        ]);
```

記入が終わったら、

```bash
composer dump-autoload
php artisan db:seed --class=UsersTableSeeder

# またはこれでテーブル初期化とseed挿入が同時にできるかも
php artisan migrate:fresh --seed
```