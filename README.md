# README


## アプリケーション名
warikan.com


## アプリケーション概要
一律ではない額を割り前勘定（以下、割り勘）する際、一人ひとりの支払額を表示することができます。

## URL
https://warikan-com.herokuapp.com/

## テスト用アカウント
テストID（１）：test@test  
テストPASS（１）：test1234

テストID（２）：test2@test  
テストPASS（２）：test1234

## 利用方法

1. まず、割り勘計算を行う上での総支払額と総人数を入力します
1. 続いて、グループ2以降に人数と、比率or一人当たりの支払額を入力します
1. それらの数値をもとに計算を行い、グループ1を含め、全員の一人当たり支払う金額が出力されます

## 課題解決

主に飲み会の幹事向けアプリです。

例えば男女やお酒が飲めるか否かで支払額を分ける際、手軽に計算できるようこのアプリを作りました。  
データ保存機能を実装しているため、履歴を後から確認でき、お金のトラブル解決にも役立てられます。

## 要件定義

* **機能**  
全員同額でない割り勘をする際の計算機能と、その経歴を保存する機能。

* **目的**  
一律ではない額の割り勘計算を手軽に行うこと。  
また、その計算の履歴を残しておくことで、金銭面のトラブル解決に役立てること。

* **詳細**  
1. 計算機能：立場、役割ごとに支払額か比率を入力して、割り勘計算ができる機能  
1. ユーザー管理機能：新規登録、ログイン、ログアウト  
1. 飲み会履歴保存機能（ログイン中のユーザーに限り）：計算結果、グループ名、日時など

## テーブル

![ER図](https://user-images.githubusercontent.com/70509887/95564074-3b687280-0a59-11eb-871a-3606ce9daf35.png)

## 実装した機能
* **計算機能**  
立場、役割ごとに支払額か比率を入力して、割り勘計算ができる機能  
1. 総額・総支払額を入力する  
1. グループ２以降から人数と一人当たりの支払額or比率を入力していく
1. 全員の一人当たりの支払額と、あまりが表示される

![計算機能](https://user-images.githubusercontent.com/70509887/97251586-83eea100-184b-11eb-8f7e-6504391c520a.gif)


* **ユーザー管理機能**  
新規登録・ログイン・ログアウト機能

![ユーザー管理機能](https://user-images.githubusercontent.com/70509887/97251598-881abe80-184b-11eb-9fb2-a68c2edf0b72.gif)


* **計算保存機能**  
割り勘計算の結果を保存し、一覧表示や削除ができる機能（ログイン中のユーザーのみ利用可）

![計算保存機能](https://user-images.githubusercontent.com/70509887/97251632-98329e00-184b-11eb-8a46-1579481ab3d6.gif)


* **レスポンシブWebデザイン**  
スマートフォン・タブレット画面に対応

![レスポンシブWebデザイン](https://user-images.githubusercontent.com/70509887/97251639-99fc6180-184b-11eb-800e-03462b93044e.gif)


## ローカルでの動作方法

以下の順でターミナルに入力してください。

```
git clone https://github.com/kohki-kimura/warikan-com.git #アプリをclone

% cd #ホームディレクトリに移動
% cd warikan-com #warikan-comディレクトリに移動

bundle install #Gemを有効にする
rails db:create #データベースを作成する
rails db:migrate #データベースを有効にする
```

## 開発環境
* ruby 2.6.5p114 (2019-10-01 revision 67812) [x86_64-darwin19]
* Rails 6.0.3.3
* mysql  Ver 14.14 Distrib 5.6.47, for osx10.15 (x86_64) using  EditLine wrapper
* Mac OS Catalina version 10.15.6
