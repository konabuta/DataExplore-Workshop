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

- また、プレビュー中（2019年9月現在）のワークスペース画面にも、下記リンクからアクセスできることを確認してください。    
<br/>

**New Workspace Experience**  
https://ml.azure.com/workspaceportal 
<img src="./docs/images/new-ws2.0.png" width=400> 

<br/> 

### Notebook VM
