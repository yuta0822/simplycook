# テーブル設計

## users テーブル

| Column             | Type   | Options                  |
| -----------------  | ------ | -------------------------|
| nickname	         | string	| null: false unique: true |
| email              | string | null: false unique: true |
| encrypted_password | string | null: false              |
| family_name        | string | null: false              |
| first_name         | string | null: false              |
| family_name_kana   | string | null: false              |
| first_name_kana    | string | null: false              |
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