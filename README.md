# 🌎 GlobalDay
### SNS上の語学学校をイメージとした英語学習に特化したアプリケーション

![toppage](https://user-images.githubusercontent.com/71579504/99182917-86be2100-277b-11eb-8dc9-153ae2103757.PNG)


# 💭　概要

### 日記を書くことは語学の定着に優れているという。
### 英語力の向上を目的としたSNSである。

自身の英語学習のアウトプットを「日記投稿」と言う形で行うことのできるSNS
投稿した日記に対して他者が文法・単語の使い方をコメントし、指摘し合う
指摘されたものはメモを残すことができ復習ができる

# 🌐  App URL
### **https://global-day.herokuapp.com/** 


# 💻  利用方法

#### `☆ トップページから新規登録・ログイン`
#### `☆ 一覧画面へ遷移する`
#### `☆ 新規投稿は右上アバター写真をクリック → 「New diary」を選択`
#### `☆ 投稿完了後は一覧画面へ戻る`<br>
[![Image from Gyazo](https://i.gyazo.com/b50633706f144ad8e9edee35bdead0c1.gif)](https://gyazo.com/b50633706f144ad8e9edee35bdead0c1)
[![Image from Gyazo](https://i.gyazo.com/98224025cb5b2527589230d42d653c76.gif)](https://gyazo.com/98224025cb5b2527589230d42d653c76)
  <br>
#### `☆ 一覧画面から１つの投稿を選択 → 投稿詳細画面へ遷移する`
#### `☆ 投稿者本人であれば投稿の編集・削除が投稿詳細画面から可能になる`<br>
 [![Image from Gyazo](https://i.gyazo.com/47f972d7dea97e1bb4d1397d280dba27.gif)](https://gyazo.com/47f972d7dea97e1bb4d1397d280dba27)
<br>
  
#### `☆ 投稿詳細画面からコメントができる`
#### `（コメントは投稿に対しての英語の使い方を指摘するものが望ましいが、交流のために使っても良い）`<br>
  [![Image from Gyazo](https://i.gyazo.com/8e43f278a15fdf4b1d25ccce1e533c58.gif)](https://gyazo.com/8e43f278a15fdf4b1d25ccce1e533c58)
<br>

#### `☆ コメントから得た学びや他者の投稿から得た学びを「My memo」へコピペして管理することができる`
#### `☆ 右上アバター写真をクリック → 「My memo」を選択`
#### `☆ Memoした履歴のタイトルをクリックするとメモ内容が表示される仕組みとなっている。`
#### `(タイトルにはわかりやすい記述がおすすめである)`<br>
  [![Image from Gyazo](https://i.gyazo.com/3272392fdd0ffa386c28e4520b9d56a6.gif)](https://gyazo.com/3272392fdd0ffa386c28e4520b9d56a6)
  [![Image from Gyazo](https://i.gyazo.com/8610c38cf24535a15c0be1ad81c0aa22.gif)](https://gyazo.com/8610c38cf24535a15c0be1ad81c0aa22)
 

# ✅ 課題解決
| ユーザーストーリーから考える課題                                                        | 課題解決                                         |
| ------------------------------------------------------------------------------- | ------------------------------------------------- |
| 自身文法があっているのかわからないという日常の課題                                          | コメント機能をつけ各自のアウトプットのため投稿へ助言ができるようにする |
| 単語の使い方が合っているのかわからないという課題                                            | 自分の苦手箇所や単語の使い方を復習できるよう個人のメモ機能をマイページとして使用できるようにする |
| 従来のSNSを利用しても目的の一致した人と関わりづらいという課題                                  | 語学を学ぶことに特化するSNSとすることで同じ目的の人同士が関わることができるようにする |
| 語学勉強のためのアプリケーションは他もあるが、有料のものが多い                                  | 同じ目的を持つ人たちによる勉強型SNSにすることで無料のアプリケーションとすることができる |
| アウトプットの仕方がわからないという課題                                                    | 日記は語学のアウトプットに良いとされているため、SNSの仕組みで気軽に投稿できるものとする |



# 📦  機能一覧
| 機能           | 概要             |
| -------------- | -----------------|
| ユーザー管理機能　| 新規登録・ログイン・ログアウトが可能  |
| 投稿機能 | 画像付きで日記投稿が可能 |
| 投稿詳細表示機能 | 各投稿詳細が詳細ページで閲覧可能 |
| 投稿編集・削除機能 | 投稿者本人のみ投稿編集・削除が可能 |
| ユーザー詳細表示機能 | 各ユーザーのプロフィール・投稿一覧が閲覧可能 |
| ユーザー情報編集機能 | ログイン中のユーザーでアカウント本人であればプロフィール編集が可能 |
| メモ機能 | 利用者本人のみが投稿・閲覧可能なメモ機能 |
| LIKE機能 | 各投稿へ非同期通信でLIKEをつけることが可能　非同期通信でLIKE削除も可能 |
| コメント機能 | 投稿詳細ページから非同期通信でコメントが可能|




## 📝 メモ機能
| 特徴            | 概要             |
| -------------- | -----------------|
| SNSにメモ機能　| 従来のSNSにはない機能。学習に特化したSNSのためメモを活用して自身だけの「辞書」のような役割を果たすことが可能である。　|
| 非同期通信を活用 | 通信量の削減が可能となり、パフォーマンスの向上 |
| アコーディオン形式を使ってのメモ表示 | メモを見やすく管理する為、タイトルをクリックするとメモ内容が見れる仕組みとなっている |

## 💜 LIKE機能

| 特徴            | 概要             |
| -------------- | -----------------|
| LIKEした数ではなくユーザーの名前表示 | 数に意識されず利用者がより自分を表現しやすいようにする為　数値での評価は避ける為 |
| 非同期通信を活用 | 通信量の削減が可能となり、パフォーマンスの向上、そしてアイコンが即座に変わる使用にする為 |

## 💬 コメント機能
| 特徴            | 概要             |
| -------------- | ---------------- |
| 投稿とコメント欄の位置関係 | 投稿とコメントブラウザ半々の表示にすることで、投稿内容に対してのコメント（助言）がスムーズに行えるようにした |
| 非同期通信活用 | 通信量の削減が可能となり、パフォーマンスの向上 |
| ユーザーアイコンの表示とリンク | コメントしたユーザー情報がわかることで、交流にもつなげていける仕様とする為 |



# 🔨 追加予定機能

- メモ機能へ検索機能追加予定

# 📎  ローカルでの動作方法

$ git clone https://github.com/liz539z/global-day.git
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
👉 http://localhost:3000

# 🚜 開発環境

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
| nickname	         | string	| null: false unique: true |
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
