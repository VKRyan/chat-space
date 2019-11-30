<!-- groups_usersテーブル -->
 
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

<!-- usersテーブル -->

|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :
- has_many :

<!-- messagesテーブル -->

|Column|Type|Options|
|------|----|-------|
|body|text|null: false|
|image|string|null: false|
|group|references|null: false,foreign_key:true|
|user|references|null: false,foreign_key:true|
### Association
- belongs_to :group
- belongs_to :user

<!-- groupsテーブル -->

|Column|Type|Options|
|------|----|-------|
|groupname|string|null: false,unique:true|
### Association
- has_many :user, through::memebers
- has_many :messages
- has_many :members

<!-- membersテーブル -->

<!-- |Column|Type|Options|
|------|----|-------|
|group_id|references|null: false,foreign_key:true|
|user_id|references|null: false,foreign_key:true|
### Association
- belongs_to :user
- belongs_to :group -->