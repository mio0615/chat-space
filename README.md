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
