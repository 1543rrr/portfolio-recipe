# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

# users table
|email   |string|not null|投稿者｜
|password|string|not null|投稿タイトル｜
|name    |string|not null|名前|



# comments table
|user      |references|投稿者     |
|post      |references|投稿を格納する場所｜
|content   |text      |投稿内容    |
|star      |integer   |参考になったの数|

# posts table
|user   |references|投稿者|
|content|text  |投稿内容|
|title  |string|投稿タイトル|
|image  |ActiveStorage|投稿写真｜

# likes table
|user_id|integer|null false|
|post_id|integer|null false|