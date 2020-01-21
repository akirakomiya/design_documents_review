# アプリケーション詳細設計
## 全体
- 管理者のみがみる画面のURLがadminになっていない
- 商品に関するテーブルがない
- deviseコントローラーの記載がない
- トップページがない
- アーティスト、ジャンル、レーベルについてのCRUDがない

## users
- 論理削除を行うため、users#destroyは不要。
- ユーザー退会に関するアクションが明記されていない

## cds
-  論理削除を行うため、users#destroyは不要。

## orders
- newのurlが/ordersになっている

## order_details
- 購入履歴画面がない
- order_detailsは一回の注文に含まれる注文商品を参照するものであるので、orders#showが同じ役割を果たすため、不要
- order#createで注文商品の保存を行うのでorder_details#createは不要。

## admin
- editのURLが/admins/idになっている

## gem
- 論理削除を考慮したgemがない
- ペジネーション機能のgemがない
- クレカ決済用のgemがない

# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。


# フィードバック　一回目（フィードバックは消さないようにしましょう）
[add]→付け加えなければいけないところ
[fix]→修正が必要なところ
[comment]→その他コメント（修正ではないけど、確認して欲しいポイントです）


## 全体
[add]→トップページが存在していない
[add]→アーティスト、ジャンル、レーベルについてのCRUDが存在していない（CRUDについてわからなければ、調べてみてください！）
[add]→ユーザー退会に関するアクションが明記されていない
[add]→deviseで作成されるコントローラーに関しての記述がない

## order_details
- 購入履歴画面がない
[fix]→order_detailsは一回の注文に含まれる注文商品を参照するものであるので、orders#showが同じ役割を果たすため、不要
[add]→同様にorder#createで注文商品の保存も行うのでorder_details#createについても不要。

## admin
[fix]→admins
- editのURLが/admins/idになっている

## users[add]
[add]→論理削除を行うため、users#destroyは不要。

## cds[add]
[add]→論理削除を行うため、cds#destroyは不要。
