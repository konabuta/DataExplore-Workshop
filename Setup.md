# Setup
ハンズオンに必要な環境のセットアップ方法を記載します。

## Table of Content
 - [Power BI Desktop](#power-bi-deskop)
 - [Azure Machine Learning service](#azure-machine-learning-service)
    1. [ワークスペース](#1-ワークスペース)
    2. [Compute Target](#2-compute-target)
    3. [Python SDK 環境](#3-python-sdk-環境)
    4. [コードのインポート](#4-コードのインポート)

## Power BI Deskop
Power BI Desktop は無料で利用できる可視化ツールです。  

下記リンクより、Microsoft ストアから Windows アプリとしてインストールでできます。  
http://aka.ms/pbidesktopstore

※ Widnowsストア経由でインストールされた Power BI Desktop は、自動更新機能によって常に最新バージョンをご利用になれます。

<br/>

## Azure Machine Learning service
Azure Machine Learning service は機械学習のモデル学習、デプロイ、運用管理をサポートするクラウドベースの機械学習の統合プラットフォームです。

### 1. ワークスペース

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


### 2. Compute Target
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

### 3. Python SDK 環境
#### A. Notebook VM

Notebook VM は、 Azure Machine Learning service が提供するマネージドな Jupyter Notebook / Jupyter Lab 環境です。

自分の Notebook VM を作成する際は、左パネルの **Notebook VM**機能にアクセスし、**New**をクリックします。
<img src="./docs/images/aml-nvm-list.png"><br/>

任意の名称とVMのスペックを選択して、作成を開始します。
<img src="./docs/images/aml-nvm-create.png"><br/>

Status が **Running** になっていることを確認し、**Jupyter** をクリックして、Jupyter Notebook にアクセスできることが確認できれば完了です。

<img src="./docs/images/aml-nvm-created.png"><br/>

<br/>

#### B. ローカル PC の Python 環境

1. [Miniconda](https://docs.conda.io/en/latest/miniconda.html) もしくは [Anaconda](https://www.anaconda.com/distribution/) をインストールします。

2. Anaconda Prompt を開いて、Pythonの myenv という名前の環境を作成します。

```bash
# New Conda
conda create -n myenv Python=3.6
# Activate 
conda activate myenv
```

3. Azure Machine Learning service Python SDK をインストールします。
```bash
# Package Install
pip install --upgrade azureml-sdk[notebooks,automl,explain,contrib] azureml-dataprep
```

4. Jupyter Notebook をインストールし、カーネルを有効化します。
```bash
# Install Jupyer Notebook
conda install notebook ipykernel
```

```bash
# Jupyter Kernel Attach
python -m ipykernel install --user --name myenv --display-name myenv
```
```bash
# Start Jupyter Notebook
jupyter notebook
```

次の Python プログラムで正常に Azure Machine Learning service Python SDK がインポートできたか確認できれば完了です。

```python
import azureml.core
azureml.core.VERSION
```

### 4. コードのインポート
#### A. Notebook VM

Notebook VM には Git がインストール済みのため、その Git コマンドからインポートする方法です。

Jupyter Notebook の Terminal を開きます。自分の個人フォルダーに移動し、本リポジトリをクローンします。

```bash
cd <個人フォルダ>
git clone https://github.com/konabuta/DataExplore-Workshop
```
<br/>

#### B. ローカル PC の Python 環境

下記のいずれかの方法でローカルPCにインポートします。

A. ローカルPCの作業フォルダにて、本リポジトリをクローン
```bash
git clone https://github.com/konabuta/DataExplore-Workshop
```
B. 本リポジトリの [Zip ファイル](https://github.com/konabuta/DataExplore-Workshop/archive/master.zip) をダウンロードし、ローカルPCの作業フォルダで解凍する　
