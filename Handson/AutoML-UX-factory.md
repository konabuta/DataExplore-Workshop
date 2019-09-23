# Automated ML UX による品質管理モデル

製造品の品質を予測する機械学習モデルを構築します。製造工程から取れたIoTデータと製造品の検査結果を学習データにします。

1. データのダウンロード
2. データのアップロード
3. Automated ML UX 事前設定と学習
4. 結果の確認
5. (Option) モデルのデプロイ

## 1. データのダウンロード
[本リポジトリのdataフォルダ](https://github.com/konabuta/DataExplore-Workshop/tree/master/Sample/data)から、**Factory.csv** をローカルPCにダウンロードします。<br/>


## 2. データのアップロード
Azure Machine Learning service のトップ画面 ([URL](https://ml.azure.com/workspaceportal/)) を開きます。 

<img src="../docs/images/aml-top.png">

Workspace の画面の左パネルの **_Datasets_** から、データセットを作成していきます。

<img src="../docs/images/aml-datasets.png" width=200>

<br/>

**_Create dataset_** から **_From local files_** を選択します。

<img src="../docs/images/aml-datasets-from-local.png" width=300>

<br/><br/>

Browse から先ほどダウンロードした **Factory.csv** を選択します。
<img src="../docs/images/aml-datasets-browse.png"><br/>


無事インポートできたことを確認して、次に進みます。名称は Factory にしています。
<img src="../docs/images/aml-datasets-browsed.png"><br/>

プレビュー画面にて問題なくデータがインポートできていることを確認して、次に進みます。
<img src="../docs/images/aml-datasets-preview.png"><br/>

各列の Type(データの形式) が問題ないことを確認して、終了します。
<img src="../docs/images/aml-datasets-schema.png"><br/>

データ(Factory)が無事登録されたことを確認します。
<img src="../docs/images/aml-datasets-registered.png"><br/>

これでデータのアップロード完了です。Azure Machine Learning に Datasets を登録すると、Automated ML や Python SDK から簡単にデータにアクセスすることができます。下記は Python SDK から呼び出すサンプルコードを示しています。

<img src="../docs/images/aml-datasets-sample-usage.png"><br/>


## 3. Automated ML UX 事前設定と学習
では、Automated ML の画面にアクセスします。Create Experiment から設定作業を始めます。

<img src="../docs/images/aml-automl-top.png"><br/>

Experimennt name に **factory-dllab**、計算環境に **cpucluster** を選択します。問題なければ、次に進みます。

<img src="../docs/images/aml-automl-name-compute.png"><br/>

先ほど登録して **Factory** という名称の Datasets を選択します。
<img src="../docs/images/aml-automl-select-datasets.png"><br/>

基本的な設定を行います。
- ID 変数は学習には必要ないので Ignored に変更
- Prediction Task : **Classification**
- Target : **Quality**
<img src="../docs/images/aml-automl-settings.png"><br/>

詳細な設定が必要な場合には、**_Advanced Settings_** で設定します。

<img src="../docs/images/aml-automl-settings-advanced.png"><br/>

設定が完了したら、学習を開始します。

<img src="../docs/images/aml-automl-start-train.png"><br/>

<img src="../docs/images/aml-automl-starting-train.png"><br/>


全学習が終わるまで待機します。

<br/><br/>

## 4. 結果の確認

**Run is Completed** という学習が完了したメッセージが確認します。モデルのパイプライン一覧から精度指標を確認することができます。

<img src="../docs/images/aml-automl-complete.gif"><br/>


## 5. (Option) モデルのデプロイ

**Deploy Best Model**をクリックします。
<img src="../docs/images/aml-automl-start-deploy.png"><br/>

デプロイする推論環境の名称を入力し、Deploy します。

<img src="../docs/images/aml-automl-deploy-model.png"><br/>

推論環境 (Azure Container Instances) へのデプロイが始まります。

<img src="../docs/images/aml-automl-deploy-started.png" width=200>

無事完了したことを確認します。

<img src="../docs/images/aml-automl-deploy-finished.png" width=200><br/>

左パネルの Model 機能にアクセスすると、登録されたモデルを確認できます。また、そのモデルに紐づく Run Id (Experimentを一意に認識するもの) がわかります。

<img src="../docs/images/aml-automl-deployed-model.gif"><br/>

さらに、そのモデルに推論環境 (Azure Container Instances) を確認することができます。

<img src="../docs/images/aml-automl-model-aci.gif"><br/>
