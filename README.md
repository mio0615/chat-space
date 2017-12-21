# DB設計

## users table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, unique: true|
|email|string|null: false|
|password|string|null: false|
|name|string|null: false|

### Association


## message table

|Column|Type|Options|
|------|----|-------|
|image|string|null: false|
|body|text|null: false|
|group_id|integer|null: false, unique: true|
|user_id|integer|null: false, unique: true|


## members table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foregin_key, true|
|group_id|integer|null: false, foregin_key, true|

### Association
- belongs_to :group
- belongs_to :user
