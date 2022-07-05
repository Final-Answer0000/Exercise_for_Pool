# 課題2（Docker&DB）について
本課題ではDockerコンテナ上でのスクレイピング作業及び取得したデータのMySQLデータベースへの格納を行う。<br>

## 課題2-1
課題2-1では、Dockerのコンテナにより下記を満たす環境を構築する。<br>
Python環境とMySQLは一つのコンテナに同梱させなくてもよいが、複数コンテナで構成する場合はコンテナ間で連携させること。
1. OS : Ubuntu20.04
2. DB : MySQL
3. Python3.8
### 提出するもの
以下の項目が映った状態のスクリーンショット（ファイル名：ex2-1.png）。スクリーンショットの描像は「sample_ex2-1.png」を参照。
- Ubuntuのバージョン
- pythonのバージョン
- MySQLのバージョン

## 課題2-2
課題2-2では、課題1（Webスクレイピング）と同様にスクレイピングによりデータを取得し、csvファイルに出力するのではなくMySQLにテーブルとして格納する。<br>
MySQLへデータを格納する工程もpythonにより実行すること。<br>
### 使用するpythonのライブラリ
1. sqlalchemy
2. pandas
3. re
4. selenium (or requests)

### データベース名
ex2
### テーブル名
ex2_2

### 提出するもの
- ソースコード: 2-2.py
- スクリーンショット
    - SQLコマンドの「select count(URL) from [テーブル名];」の出力。<br>
    ファイル名：ex2-2_count.png
    - SQLコマンドの「show columns from [テーブル名];」の出力<br>
    ファイル名：ex2-2_columns.png
    - SQLコマンドの「select * from [テーブル名] limit 5;」の出力<br>
    ファイル名：ex2-2_table.png


# 本課題を行う上での注意点
1. リクエスト先のサーバーに不可をかけないために、リクエスト前には必ず3秒のアイドリングタイムを入れること。[参考](https://docs.pyq.jp/column/crawler.html)
2. requests及びseleniumを使用する際は、ユーザーエージェントを設定すること。
3. 成果物のフォーマットを守ること。
4. ソースコードの可読性をある程度意識すること。
