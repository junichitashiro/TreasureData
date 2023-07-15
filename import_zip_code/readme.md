# 郵便番号データをインポートするワークフロー

## 概要

* 日本郵政で公開している郵便番号のCSVファイルをS3からインポートする

## digファイル

* import_zip_code.dig
* ワークフローの設計書となるファイル

## ymlファイル

* load_zip_code.yml
* CSVファイルの入出力設定を記載するファイル
* configディレクトリ配下に配置する

## CSVファイル

* AWSのS3バケット配下に配置
* 取得元
  * https://www.post.japanpost.jp/zipcode/dl/oogaki-zip.html
  * **全国一括** のデータを使用
  * 取得時はzip形式なので展開してから **KEN_ALL.CSV** のファイル名で配置する

## 補足

* time列がないのでインポート時に追加する設定をymlファイルに記載する
