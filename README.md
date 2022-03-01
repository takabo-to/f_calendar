# README

## ペルソナ
自分と家族

## 背景
普段のシフト共有手段がLINEのため、シフト表を送り、それぞれがスマホや手帳などに記載し管理している。
この方法だと、予定が変わる度にそれぞれがスケジュールを書き直す必要があるため面倒。

## 課題解決策
Web上にカレンダーを一つ作り、そこに各々がシフトを入力することでスケジュール管理が楽になるのではないかと考えた。

## usersテーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |

### Association
- has_many :blogs

## blogsテーブル

| Column    | Type       | Options      |
| ----------| ---------- | -------------|
| title     | string     | null: false  |
| content   | text       | null: false  |
| start_time| datetime   | null: false  |

## Association
- belongs_to :user
