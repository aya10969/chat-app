# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |

### Association

- has_many :room_users
- has_many :rooms, thro



## attend(出席) テーブル 


| Column        | Type       | Options                        |
| -------       | ---------- | ------------------------------ |
| guest         | string     | null: false                    |
| gender        | string     | null: false                    |
| relationship  | string     | null: false                    |
| address       | integer    | null: false                    |
| transportation| string     | null: false                    |
| second party  | string     | null: false                    |
| user          | references | null: false, foreign_key: true |

### Association


- belongs_to :user