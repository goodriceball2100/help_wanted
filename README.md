# help_wanted DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false|
### Association
- has_many :images

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|introduction|text|null: false,|
|employment_status|string|ull: false,|
|email|string|null: false|
|phone_number|string|null: false|
|wage|string|null: false|
### Association
- belongs_to : user
- belongs_to : category
- had_many: item_imgs, dependent::destroy

## imageテーブルテーブル
|column|Type|Option|
|------|----|------|
|url|string|null:false|
|item|reference|null:false,foregin_key:true|
### Association
- belongs_to : item