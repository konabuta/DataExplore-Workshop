# DataExplore-Workshop
<br/>

<img src="docs/images/dllab.png" width=350>


[Dllab Engineers Days 2019 Handson Day1](https://dllab.connpass.com/event/144595/)

### 自動機械学習 AutoML & 要因探索 ハンズオン

機械学習を使って色んな問題を解きたいけど、人材やスキル不足が課題でなかなか前に進まない…そんな状況から脱出しませんか？ Azureは機械学習の民主化を実現するプラットフォームを提供しています。本ハンズオンでは、マウス操作による簡単な要因探索、また自動機械学習を利用して高速にプロトタイプを構築するプロセスをご体感頂きます。今回は Azure Machine Learning service の自動機械学習 (Automated Machine Learning) や PowerBI の要因探索機能 (Key Influencers) を中心に利用します。Azure Machine Learning service によるモデルの解釈方法についても言及します。



# Agenda
### [Setup](./Setup.md)
- 本ワークショップの開発環境の構築作業

### [Introduction](./Introduction.md)
- 一般的な自動機械学習やモデル解釈のアプローチ方法
- 関連する Microsoft のサービス

### [Handson](./Handson.md)
- ハンズオンのコンテンツ

<br/>

## Sample Code

下記の表には、本リポジトリに含まれるサンプルコードのリストです。Environment 列のリンクからアクセスできます。

| Algorithm | Environment | Interpretability Type | Description | 
| --- | --- | --- | --- |
| Decision Tree | [Azure ML service Python SDK](Sample/Decision-Tree/FactoryQC-azureml-sklearn-DT.ipynb) / [InterpretML](Sample/Decision-Tree/FactoryQC-InterpretML-DT.ipynb)| Interpretable | Decision Tree (決定木) を用いたモデル開発のサンプルコード| 
| Linear Regression | [Excel](Sample/Linear-Regression/linear-regression.xlsx) / [Azure ML service Python SDK](Sample/Linear-Regression/diabetes-azureml-sklearn-LR.ipynb) / [InterpretML](Sample/Linear-Regression/diabetes-InterpretML-LR.ipynb) | Interpretable | Linear Regression (線形回帰) を用いたモデル開発のサンプルコード| 
| Decision Tree & Linear Regressionn | [Power BI -  Key Influencers](Sample/Key-Influencers/titanic-sample.pbix) | Interpretable| KPI 要因探索ビジュアル機能 |
| AutoML + Model Interpretability | [Azure ML service Python SDK (Automated ML + Interpretabiliy SDK)](Sample/Automated-Machine-Learning) | Model-Agnostic | 自動機械学習 + モデル解釈統合フレームワーク| 
| Microsoft InterpretML | [Python - Classification](Sample/Interpret/FactoryQC-InterpretML-classification.ipynb) | Interpretable | Microsoft Interpret ML によるモデル開発のサンプルコード| 
| Global Surrogate | _n/a_<!--[Python](Sample/Global-Surrogate)--> | Model-Agnostic | Global Surrogate を用いたモデル解釈| 
| Permutation Feature Importance |_n/a_<!--[Python](Sample/PFI)--> | Model-Agnostic | PFI を用いたモデル解釈| 
| LIME | _[external site](https://github.com/marcotcr/lime)_<!--[Python](Sample/LIME)--> | Model-Agnostic | LIME によるモデル解釈| 
| SHAP | _[external site](https://github.com/slundberg/shap)_| Model-Agnostic | SHAP によるモデル解釈|


<br/>



# Known Issues
うまくいかない時は、[こちらのドキュメント](Known-issues.md) を参照してください。<br/>



# 参考
- [Azure AI 概要](https://azure.microsoft.com/ja-jp/overview/ai-platform/#machine-learning)
- [Azure Machine Learning service ドキュメント](https://docs.microsoft.com/ja-JP/azure/machine-learning/)
- [Azure Machine Learning service Sample Code](https://github.com/Azure/MachineLearningNotebooks)
- [Interpretable Machine Learning - A Guide for Making Black Box Models Explainable](https://christophm.github.io/interpretable-ml-book/)