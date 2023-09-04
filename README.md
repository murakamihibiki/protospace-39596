# README

This README would normally document whatever steps are necessary to get the
application up and running.

## users テーブル

| Column             | Type   | Options                              |
| ------------------ | ------ | ------------------------------------ |
| email              | string | null: false, unique constraint: true |
| encrypted_password | string | null: false                          |
| name               | string | null: false                          |
| profile            | text   | null: false                          |
| occupation         | text   | null: false                          |
| position           | text   | null: false                          |

## prototypes テーブル

| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| title              | string     | null: false                    |
| catch_copy         | text       | null: false                    |
| concept            | text       | null: false                    |
| user               | references | null: false, foreign_key: true |

## comments テーブル

| Column             | Type       | Options                        |
| ------------------ | ---------- | ------------------------------ |
| content            | text       | null: false                    |
| prototype          | references | null: false, foreign_key: true |
| user               | references | null: false, foreign_key: true |
