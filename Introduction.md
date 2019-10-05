# Introduction

ビッグデータの時代になり、データ分析のニーズが高まっています。BIツール・Excel による可視化、機械学習による予測モデリングなどデータを扱うための様々なテクノロジーが生まれています。

その中でも **記述的分析・診断的分析** に属するデータ探索 (要因探索、原因分析 ...) はデータ分析に中心的な取り組みです。製造品の不良分析、ローン審査、顧客分析 ... など数多くの活用シーンがあります。

<br/>

<img src="./docs/images/analytics_steps.gif" width = 400><br/>

しかしながら、複雑・大量になっているデータに対する探索は非常に困難です。下記のような理由が挙げられます。

- 直感的に可視化してデータの傾向は理解しているけど、**客観的なデータの関係性** が理解ができない
- 統計解析・機械学習のテクノロジーを導入する **ハードルが高い (コスト、人材、スキル)**
- **機械学習モデルが複雑** で解釈できない、理解できない、信頼されない  
etc

本ワークショップでは、データ探索の中でも **診断的分析** にフォーカスして、**機械学習によって高度なデータ探索を行うアプローチ方法** をご紹介します。

また、Microsoft のテクノロジーを利用することで、上記課題を解決し、効率的・簡単に分析プロセスを進めることを実感いただくことを目的にします。

<br/>

## モデル解釈の重要性

複雑なデータの関係性を理解するために統計解析や機械学習の利用が必要になります。しかしながら、近年はアルゴリズムが複雑化して精度が大幅に向上しましたが、一方で下記のような問題が出てくるようになりました。

- 構築された機械学習モデルは妥当なものか？信頼できるか？
- なぜこの予測値になったのか現場に説明できない
- モデルをどうやって改善すればいいか分からない


そのため、単に精度が高い機械学習モデルを開発するだけでなく、**モデルの解釈可能性** が必要になってきています。

また、予測値の算出というよりも、説明変数と予測対象変数の関係性を分析したいようなデータ探索においても **モデルの解釈可能性** は重要です。

モデル解釈のアプローチ方法は大きく下記の2通りあります。

- 解釈可能なモデルを利用する (Interpretable Algorithms)
- Black Box なモデルを解釈する (Model-Agnostiic Methods)

本ワークショップでは、この機械学習モデルの解釈可能性についても取り上げます。

<br/>

## Technology & Microsoft サービス
利用するテクノロジーと Microsoft サービスについて整理します。詳細についてはリンク先のドキュメントを参照してください。

### Technology
- **[Automated Machine Learning (AutoML)](Automated-Machine-Learning.md)**   
    - 自動機械学習のテクノロジー。特徴量エンジニアリング、アルゴリズム選択、パラメータチューニングのプロセスを自動化。機械学習の民主化を実現し、高速 & 効率的なモデル開発が可能に。
- **[Interpretable Algorithms](Interpretable-Algorithms.md)** 
    - 解釈可能なモデル。構造がシンプルなモデルを利用することで、モデルの構造を理解でき、説明変数と予測対象変数の関係性が解釈可能に。統計解析の手法が使われることが多い。
- **[Model-Agnostic Methods](Model-Agnostic-Methods.md)** 
    - Black Box なモデルを解釈するためアプローチ方法。あらゆるモデルに対応可能な汎用的なモデル解釈フレームワーク。

### Microsoft サービス

- **[Azure Machine Learning service](Azure-Machine-Learning-service.md)** 
    - 機械学習/深層学習のプロセスを効率的に回すための、**オープン & マネージドな分析プラットフォーム**です。**自動機械学習 Automated ML** など効率的に実験的なモデル学習を進める機能や、最先端の **モデル解釈フレームワーク Interpretability SDK** も提供しています。
- **[Power BI](PowerBI.md)**
    - エンタープライズまでスケール可能な **セルフサービス BI** サービスです。膨大なデータに対して、簡単なマウス操作で、傾向を分析＆“見える化”することで、重要な気づきを発掘することができます。Key Influencers や Quick Insight など高度な分析機能も含まれます。
- **[Microsoft Interpret ML](InterpretML.md)**
    - モデル解釈性や精度の両方を追求した機械学習アルゴリズム。Microsoft Research が開発している。

### Mapping Table


|   Category                   |  Microsoft サービス      |
| -----------------------------| ---------------------------|
|  Automated Machine Learning  |  1. Azure Machine Learning service   |
|  Interpretable Algorithms    |  1. Power BI - Key Influencers<br>2. Microsoft Interpret ML<br>3. カスタム Python & R (Azure ML)       |
|  Model Agnostic Methods      |  1. Azure Machine Learning Interpretability SDK<br>2. カスタム Python & R  (Azure ML)             |

<br/>

