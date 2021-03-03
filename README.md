#  simplycook
### 料理レシピを投稿ができるアプリケーション

# 概要

### 誰でも料理レシピを投稿することができる。
### レシピに書かれている材料から近くのスーパーで売っている食材を検索することができる。
### 調理で用いた調理器具を紹介することができ、リンクで調理器具の販売をすることができる。

# 利用方法

#### `☆ トップページから新規登録・ログイン`
#### `☆ 一覧画面へ遷移する`
#### `☆ 料理レシピを投稿することができる`
#### `☆ 投稿完了後は一覧画面へ戻る`
#### `☆ 投稿詳細画面へ遷移する`
#### `☆ 投稿者本人であれば投稿の編集・削除が投稿詳細画面から可能になる`
#### `☆ 投稿詳細画面からコメントができる`
#### `☆ 投稿詳細画面かいいねをつけることができる`

# 課題解決

| ユーザーストーリーから考える課題                                                        | 課題解決                                         |
| ------------------------------------------------------------------------------- | ------------------------------------------------- |
| 料理をどう始めればいいのか悩んでいる 　　　　　　　                                        | 手軽な料理レシピを掲載し、料理に対して興味を沸かせる |
| 料理レシピで手元にレシピど通りの食材がないので料理が作れないという課題                           | レシピに掲載してある食材を近くのスーパーにあるか表示させる |
| 調理器具を買い替えようとしているがどこで何がいいのか買ったらいいのかわからない課題                  | 投稿者が使用している調理器具を載せることによって投稿者のおすすめ調理器具を掲載できるようにする |



# 機能一覧

| 機能           | 概要             |
| -------------- | -----------------|
| ユーザー管理機能　| 新規登録・ログイン・ログアウトが可能  |
| 投稿機能 | 画像付きで料理レシピ投稿が可能 |
| 投稿詳細表示機能 | 各投稿詳細が詳細ページで閲覧可能 |
| 投稿編集・削除機能 | 投稿者本人のみ投稿編集・削除が可能 |
| LIKE機能 | 各投稿へ非同期通信でLIKEをつけることが可能　非同期通信でLIKE削除も可能 |
| コメント機能 | 投稿詳細ページから非同期通信でコメントが可能|

# 追加予定機能

## LIKE機能

| 特徴            | 概要             |
| -------------- | -----------------|
| LIKEした数を表示する | 数が多ければランキングの上位にレシピを紹介される |
| 非同期通信活用 | 通信量の削減が可能となり、パフォーマンスの向上 |


## コメント機能
| 特徴            | 概要             |
| -------------- | ---------------- |
| 投稿とコメント欄の位置関係 | レシピ作った感想を載せることができる　|
| 非同期通信活用 | 通信量の削減が可能となり、パフォーマンスの向上 |
 

# ローカルでの動作方法

$ git clone 
</br>
$ cd global-day
</br>
$ bundle install
</br>
$ rails db:create
</br>
$ rails db:migrate
</br>
$ rails s
</br>

# 開発環境

- VScode
- Ruby 2.6.5
- Rails 6.0.3.4
- mysql2 0.5.3
- JavaScript
- gem 3.0.3
- heroku 7.46.0


# DB設計

# テーブル設計

## users テーブル

| Column             | Type   | Options                  |
| -----------------  | ------ | -------------------------|
| nickname	          | string	| null: false unique: true |
| email              | string | null: false unique: true |
| encrypted_password | string | null: false              |
| family_name        | string | null: false              |
| first_name         | string | null: false              |
| birthdate          | date   | null: false              |

### Association
- has_many: items 
- has_many: likes 
- has_many: comments


##  items テーブル

| Column        | Type       | Options                        |
| -----------   | ---------- | ------------------------------ |
| name          | string     | null: false                    |
| explanation   | text       | null: false                    |
| category_id   | integer    | null: false                    |
| time          | integer    | null: false                    |
| cost          | integer    | null: false                    |
| material      | integer    | null: false                    |
| maiking       | integer    | null: false                    |
| point         | integer    | null: false                    |
| user          | references | null: false, foreign_key: true |


### Association

- belongs_to_active_hash :category
- belongs_to_active_hash :time
- belongs_to_active_hash :cost
- belongs_to             :user
- has_many: likes 
- has_many: comments


##  likes テーブル

| Column        | Type       | Options                         |
| -----------   | ---------- | ------------------------------ |
| user          | references | null: false, foreign_key: true |
| items         | references | null: false, foreign_key: true |


### Association
- belongs_to: user
- belongs_to: items


##  comments テーブル

| Column        | Type       | Options                        |
| -----------   | ---------- | ------------------------------ |
| user          | references | null: false, foreign_key: true |
| items         | references | null: false, foreign_key: true |
| comment       | text       | null: false                    |


### Association
- belongs_to: user
- belongs_to: items
