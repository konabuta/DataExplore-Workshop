# DataExplore-Workshop
<br/>

<img src="docs/images/dllab.png" width=350>


[Dllab Engineers Days 2019 Handson Day1](https://dllab.connpass.com/event/144595/)   
**自動機械学習 AutoML & 要因探索 ハンズオン(Microsoft)**



# Agenda
### [Setup](./Setup.md)
ワークショップの開発環境の準備

### [Introduction](./Introduction.md)
一般的な自動機械学習やモデル解釈のアプローチ方法

### [Handson](./Handson.md)
ハンズオンのコンテンツ

<br/>

## Sample Code

下記の表には、本リポジトリに含まれるサンプルコードをリストしています。Environment列のリンクからアクセスできます。

| Algorithm | Environment | Interpretability Type | Description | 
| --- | --- | --- | --- |
| Decision Tree | [Azure ML service Python SDK](Sample/Decision-Tree/FactoryQC-azureml-sklearn-DT.ipynb) / [InterpretML](Sample/Decision-Tree/FactoryQC-InterpretML-DT.ipynb)| Interpretable | Decision Tree (決定木) を用いたモデル開発のサンプルコード| 
| Linear Regression | [Excel](Sample/Linear-Regression/linear-regression.xlsx) / [Azure ML service Python SDK](Sample/Linear-Regression/diabetes-azureml-sklearn-LR.ipynb) / [InterpretML](Sample/Linear-Regression/diabetes-InterpretML-LR.ipynb) | Interpretable | Linear Regression (線形回帰) を用いたモデル開発のサンプルコード| 
| Power BI - Key Influencers | [Power BI](Sample/Key-Influencers/titanic-sample.pbix) | Interpretable| KPI 要因探索ビジュアル機能 |
| Azure ML Automated ML + Interpretability SDK | [Azure ML service Python SDK](Sample/Automated-Machine-Learning) | Model-Agnostic | 自動機械学習 + モデル解釈統合フレームワーク| 
| Microsoft InterpretML | [Python - Classification](Sample/Interpret/FactoryQC-InterpretML-classification.ipynb) | Interpretable | Microsoft Interpret ML によるモデル開発のサンプルコード| 
| Global Surrogate | _作成中_<!--[Python](Sample/Global-Surrogate)--> | Model-Agnostic | Global Surrogate を用いたモデル解釈| 
| Permutation Feature Importance |_作成中_<!--[Python](Sample/PFI)--> | Model-Agnostic | PFI を用いたモデル解釈| 
| LIME | _作成中_<!--[Python](Sample/LIME)--> | Model-Agnostic | LIME によるモデル解釈| 
| SHAP | _作成中_<!--[Python](Sample/SHAP)--> | SHAP によるモデル解釈|


<br/>


# 参考
- [Azure AI 概要](https://azure.microsoft.com/ja-jp/overview/ai-platform/#machine-learning)
- [Azure Machine Learning service ドキュメント](https://docs.microsoft.com/ja-JP/azure/machine-learning/)
- [Interpretable Machine Learning - A Guide for Making Black Box Models Explainable](https://christophm.github.io/interpretable-ml-book/)