# Setup
ハンズオンに必要な環境のセットアップ方法を記載します。

## Table of Content
 - Power BI Desktop
 - Azure Machine Learning service
    - ワークスペース
    - Notebook VM
    - Compute Target

## Power BI Deskop
Power BI Desktop は無料で利用できる可視化ツールです。  

下記リンクより、Microsoft ストアから Windows アプリとしてインストールでできます。
http://aka.ms/pbidesktopstore

※ Widnowsストア経由でインストールされた Power BI Desktop は、自動更新機能が常に最新バージョンをご利用になれます。

<br/>

## Azure Machine Learning service
Azure Machine Learning service は機械学習のモデル学習、デプロイ、運用管理をサポートするクラウドベースの機械学習の統合プラットフォームです。

### ワークスペース

- [Azure Portal](https://portal.azure.com/) へアクセスします。
- 画面左上の**リソースの作成** を選択します。  
<img src="./docs/images/setup-aml-portal1.png" width=400>

- 検索バーにて、**machine learning service workspace** と入力します。  
<img src="./docs/images/setup-aml-portal2.png" width=400> 

- *Machine Learning service workspace* を選択し、**作成** をクリックします。
<img src="./docs/images/setup-aml-portal3.png" width=400> 

- 各種情報を入力します。  
<img src="./docs/images/setup-aml-portal4.png" width=400> 

- **確認および作成** をクリックし、レビュー画面にて **作成** を選択します。
- 無事デプロイが完了したら、**リソースに移動** します。  
<img src="./docs/images/setup-aml-portal5.png" width=400> 

- Azure Machine Learning service ワークスペースの画面が表示されたら完了です。
<img src="./docs/images/ws.png" width=400> 

- また、プレビュー中（2019年9月現在）のワークスペース画面にも、下記リンクからアクセスできることを確認してください。  <br/>    
**New Workspace Experience**  
https://ml.azure.com/workspaceportal   
<img src="./docs/images/new-ws2.0.png" width=400> 

<br/> 


### Compute Target
機械学習のトレーニングを回すための計算環境 (Machine Learning Compute) を設定します。
Workspace の画面の左パネルの **_Compute_** から、計算環境を作成していきます。

<img src="./docs/images/aml-compute.png" width=150> 

**Add** して、新規で計算環境を構築します。

<img src="./docs/images/aml-compute-add.png" ><br/>

**cpucluster** という名称で、Compute Type は **Machine Learning Compute** を選択します。

<img src="./docs/images/aml-compute-add-name-type.png"><br/>

VMの種類やノードの設定を行います。下記画面を参考に選択してください。設定が完了したら、Create を押して環境作成を開始します。

<img src="./docs/images/aml-compute-add-details.png"><br/>

計算環境の作成が無事終わったことを確認します。

<img src="./docs/images/aml-compute-list.png"><br/>

## Azure Machine Learning Python SDK 環境
### Notebook VM


### ローカル PC の Python 環境
