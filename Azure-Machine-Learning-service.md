# Azure Machine Learning service

## 概要

Azure Machine Learning service の概要については、[こちらのスライド](Presentation/AzureML概要.pptx)を参照してください。


## Interpretability SDK

Azure Machine Learning service が提供するモデル解釈ライブラリ。機械学習モデルのモデル全体の説明変数の重要度 (グローバル) や個々の予測値に対する説明変数の重要度 (ローカル) を理解することが可能です。

### 基本コンポーネント

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/service/media/machine-learning-interpretability-explainability/interpretability-architecture.png" width=600>

今回は Tabulear Data (表形式データ) について説明します。

### Mimic
Global Surrogate と呼ばれるグローバルなモデル解釈方法。構築済みの機械学習モデルに対するインプットデータと予測値から、解釈可能なモデルで学習し直して、モデル解釈をするアプローチ方法。

Azure Machine Learning では、`LightGBM` `Linear Regression` `SGD` `Decision Tree` が利用できます。

```python
from azureml.explain.model.mimic.mimic_explainer import MimicExplainer

# you can use one of the following four interpretable models as a global surrogate to the black box model
from azureml.explain.model.mimic.models.lightgbm_model import LGBMExplainableModel
from azureml.explain.model.mimic.models.linear_model import LinearExplainableModel
from azureml.explain.model.mimic.models.linear_model import SGDExplainableModel
from azureml.explain.model.mimic.models.tree_model import DecisionTreeExplainableModel

explainer = MimicExplainer(model, 
                           x_train, 
                           LGBMExplainableModel, 
                           augment_data=True, 
                           max_num_of_augmentations=10, 
                           features=breast_cancer_data.feature_names, 
                           classes=classes)
```
### Feature Permutation
Permutation Feature Importance と呼ばれるグローバルなモデル解釈方法。インプットデータを変化させた際の予測値の変化の大きさから、変数の影響度を判断するアプローチ方法。

<br/>

### LIME
KDD 2016で採択されたローカルなモデル解釈手法。ある予測結果について局所的に近似させた解釈可能な機械学習モデルを適用して、そのモデルを解釈するアプローチ方法。

**"Why Should I Trust You?": Explaining the Predictions of Any Classifier**  
https://arxiv.org/abs/1602.04938



<br/>

### SHAP
NIPS 2017で採択されたローカルなモデル解釈手法。ゲーム理論のシャープレイ値の枠組みを利用して、変数の影響度を算出している。

**A Unified Approach to Interpreting Model Predictions**  
https://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions
