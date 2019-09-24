# DataExplore-Workshop
<br/>

<img src="docs/images/dllab.png" width=350>


[Dllab Engineers Days 2019 Handson Day1](https://dllab.connpass.com/event/144595/)   
**自動機械学習 AutoML & 要因探索 ハンズオン(Microsoft)**



# Agenda
- [事前準備](./Setup.md)

- [Introduction](./Introduction.md)

- [Handson](./Handson.md)

<br/>

## Sample Code

下記の表には、本リポジトリに含まれるサンプルコードをリストしています。Environment列のリンクからアクセスできます。

| Algorithm | Environment | Interpretability Type | Description | 
| --- | --- | --- | --- |
| Decision Tree | [Azure ML service Python SDK](Sample/Decision-Tree/FactoryQC-azureml-sklearn-DT.ipynb) / [InterpretML](Sample/Decision-Tree/FactoryQC-InterpretML-DT.ipynb)| Interpretable | Decision Tree (決定木) を用いたモデル開発のサンプルコード| 
| Linear Regression | [Excel](Sample/Linear-Regression/linear-regression.xlsx) / [Azure ML service Python SDK](Sample/Linear-Regression/diabetes-azureml-sklearn-LR.ipynb) / [InterpretML](Sample/Linear-Regression/diabetes-InterpretML-LR.ipynb) | Interpretable | Linear Regression (線形回帰) を用いたモデル開発のサンプルコード| 
| Global Surrogate | _作成中_<!--[Python](Sample/Global-Surrogate)--> | Model-Agnostic | Decision Tree (決定木) を用いたモデル開発のサンプルコード| 
| Permutation Feature Importance |_作成中_<!--[Python](Sample/PFI)--> | Model-Agnostic | Linear Regression (線形回帰) を用いたモデル開発のサンプルコード| 
| LIME | _作成中_<!--[Python](Sample/LIME)--> | Model-Agnostic | Microsoft Interpret ML によるモデル開発のサンプルコード| 
| SHAP | _作成中_<!--[Python](Sample/SHAP)--> | Model-Agnostic | Microsoft Interpret ML によるモデル開発のサンプルコード|
| Power BI - Key Influencers | [Power BI](Sample/Key-Influencers/titanic-sample.pbix) | Interpretable| KPI 要因探索ビジュアル機能 |
| Azure ML Automated ML + Interpretability SDK | [Azure ML service Python SDK](Sample/Automated-Machine-Learning) | Model-Agnostic | 自動機械学習 + モデル解釈統合フレームワーク| 
| Microsoft InterpretML | _作成中_<!--[Python](Sample/Interpret)--> | Interpretable | Microsoft Interpret ML によるモデル開発のサンプルコード| 

<br/>


# 参考
- [Azure AI 概要](https://azure.microsoft.com/ja-jp/overview/ai-platform/#machine-learning)