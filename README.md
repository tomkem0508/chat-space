# chat-space


## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|text|null: false, foreign_key: true|
|member_id|integer|null: false, foreign_key: true|

### Association
- has_many : members

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|text|null: false, foreign_key: true|
|member_id|integer|null: false, foreign_key: true|

### Association
- has_many :members

## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
- has_many :messages

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|body|text||
|image|string||
|member_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :member
