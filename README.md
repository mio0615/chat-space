# DB設計

## users table

|Column|Type|Options|
|------|----|-------|
|email|string|null: false  unique: true|
|password|string|null: false, unique: true|
|name|string|null: false, unique: true|

### Association
- has_many: messages
- has_many: members
- has_many: groups


## messages table

|Column|Type|Options|
|------|----|-------|
|image|string||
|body|text||
|group_id|integer|foregin_key: true|
|user_id|integer|foregin_key: true|

### Association
- belongs_to :user
- belongs_to :group

## members table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|foregin_key: true|
|group_id|integer|foregin_key: true|

### Association
- belongs_to :user
- belongs_to :group

## groups table

|Column|Type|Options|
|------|----|-------|
|group_id|integer|foregin_key: true|
|name|string||

### Association
- has_many :messages
- has_many :members
- has_many :users
