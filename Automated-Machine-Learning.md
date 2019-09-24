# Automated Machine Learning

自動機械学習（AutoML）のテクノロジーが進歩してきています。
- モデリングの試行錯誤の工数が大幅に削減する
- ビジネスユーザが機械学習モデリングができるようになる
- 機械学習が企業に浸透する

データ探索においても、データの特徴や関係性を理解する際に利用する機械学習モデルを開発する手段として自動機械学習は有効です。

<br/>

# 機械学習のモデル構築プロセス

一般的な自動機械学習が対象にする自動化されるプロセスを下記にて説明します。

## 特徴量エンジニアリング

機械学習に必要なデータを準備するプロセスです。

- 例： 特徴量作成、標準化、正規化、次元削減、欠損値補完 etc

## アルゴリズム選択
機械学習の種類 (Classification, Regresison, Forecasting) に応じて適切なアルゴリズムを選択します。

アルゴリズムの種類の選択方法は、Cheat Sheet も有効です。  <br/>


_[scikit-learn](https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html)_

<img src="https://scikit-learn.org/stable/_static/ml_map.png" width=400><br/>
_[Azure Machine Learning Studio](https://docs.microsoft.com/en-us/azure/machine-learning/studio/algorithm-cheat-sheet)_

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/studio/media/algorithm-cheat-sheet/machine-learning-algorithm-cheat-sheet-small_v_0_6-01.png" width=400><br/>



## ハイパーパラメータ選択
各機械学習アルゴリズムは固有のパラメータを保持しており、ユーザーは学習前にパラメータを調整する必要があります。ハイパーパラメータの値によってモデルのパフォーマンスが変わってくるため、試行錯誤が必要なプロセスです。


<br/>




# AutoML 関連テクノロジー
* [Microsoft - Automated Machine Learing](https://azure.microsoft.com/ja-jp/services/machine-learning-service/)
* [DataRobot](https://www.datarobot.com/jp/)
* [Google - AutoML](https://cloud.google.com/automl/?hl=ja)
* [H2O](https://www.h2o.ai/products/h2o-driverless-ai/)
* [dotData](http://dotdata.jp/)