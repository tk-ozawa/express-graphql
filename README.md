# express + graphql アプリ

## 利用方法

### (初回のみ)

1. 本リポジトリを`git clone`する
1. `cd express-graphql`, `npm install`を実行
1. `cp .env.example .env`を実行
1. MongoDBのWeb版でSchema作成。必要な情報をコピーして`.env`に記述

### (初回 + 初回以降のデバッグ時)

`nodemon app`でアプリ起動  
(router/index.js内のコメントアウトを外してapp.jsのapp.use内のミドルウェアをnullにして、
localhost:4000/graphql でGraphiQL起動)

## なぜ作った？

テーマ「手っ取り早くGraphQLすげええええってなりたい」

- APIサーバを気軽に作りたい → Expresss.js
- そのままだと使いづらい → MVC化
- RESTfulだとURI設計めんどくさい → GraphQL
- RDBMSだと設計から実装までがめんどくさい → NoSQL(MongoDB)

#### +α

- 認証API実装  
GraphQLのエンドポイントを認証ガード下に置いて実運用にも耐えられるようにしてみた

## 利用技術

package.jsonを参照
