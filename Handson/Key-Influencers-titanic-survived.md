# Power BI - Key Influencers による要因探索

タイタニック号の乗船リストデータを利用して、生き残った乗客の属性を探索します。

## 1. データのダウンロード
[Kaggle : Titanic Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data) からタイタニック号の乗船顧客データをPCにダウンロードします。

<img src="../docs/images/kaggle-titanic.png" width = 500><br/><br/>


train.csv をダウンロードします。

<img src="../docs/images/kaggle-data-download.png" width = 500><br/><br/>


## 2. データのアップロード
Power BI Desktop を開いて、CSV データをインポートします。

<!-- <img src=""> -->

無事インポートされていることを確認してください。

<!-- <img src=""> -->


<br/><br/>

## 2. データの変換
Key Influencers が利用できるように、"Surviced" 列のデータ形式を **_バイナリ_** に変更します。

<br/><br/>

## 3. Key Influecers 
レポート作成画面に移動し、右上の視覚化から **主要なインフルエンサ**  ( = Key Influencers) を選択します。変数データを下記のようにドラッグ & ドロップで移動します。

<br/><br/>

## 4. 結果の確認


<br/><br/>

## (Option) 5. ダッシュボードの作成
出来上がった画面にフィルターを追加し、性別毎の特徴など、様々な観点で分析してみます。