# ER図1
【フィードバック】
[add]→付け加えなければいけないところ
[fix]→修正が必要なところ
[comment]→その他コメント
それぞれ、フィードバックを付け加えましたので、参考にしながら再提出をお願いします。
また、再提出のする際はフィードバックを消さないようにお願いします。

## 全体
- ActiveRecordでデフォルトで作られる登録日、更新日の記述がどのテーブルにもない。
[add]→複数住所をしまうための、配送先テーブルが存在しない
[add]→受注詳細テーブルがない

## エンドユーザー
- エンドユーザーが退会したかどうかなどのステータスがわからない

## カート
- アーティスト名、ジャケット画像、シングル/アルバム名を商品テーブルから引っ張っていることを考慮していない。
- 決済テーブルとリレーションの関係になっていて決済の情報を持ち続けてしまう。
[add]→エンドユーザとのリレーションがない
[add]→主キーがテーブル名と一致していない
[add]→合計金額カラムは必要か？
[add]→カート内商品テーブルではないでしょうか？テーブル名命名要確認。

## 商品
- レーベル、ジャンルに該当するカラムは複数のデータを入れる可能性があるが商品テーブルで管理されている
[add]→アーティストカラムが存在している
[add]→曲名カラムが存在している
[add]→商品の論理削除は考慮されているか
[add]→ステータスカラムの用途は何ですか？
[add]→在庫数は（入荷数）ー（販売数）から計算される数字。基本的にデータベースの中に計算処理後の値は入れないようにするべき。（計算処理命令が同時に来た時エラーが起きることがあるため）

## 購入履歴
- PKの記載がない
[fix]そもそもこのテーブルは必要だろうか？

## 購入履歴
[add]→テーブル名と機能が異なっている
[add]→購入日カラムを持っている。
[add]→送料カラムがない。合計金額カラムがない
[add]→カートとのリレーションがある。
[add]→送付先住所カラムがあるが、宛名と郵便番号がない。

## 管理者
-エンドユーザーと商品テーブルにリレーションをかけている


# 注意
* マークダウン形式で記入してください。
* 全体を通しての指摘事項の場合、テーブル名の部分を「全体」「共通」などとしてください。
