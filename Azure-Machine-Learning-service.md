# Azure Machine Learning service


### [Azure Machine Learning service](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/)
Azure Machine Learning service は、機械学習/深層学習のプロセスを効率的に回すための、オープンな分析プラットフォームです。

<img src="https://docs.microsoft.com/en-us/azure/machine-learning/service/media/concept-azure-machine-learning-architecture/workflow.png" width = "500">   

[こちらのスライド](Presentation/AzureML概要.pptx)もご参照ください。
<br/><br/>


---

## 自動機械学習 Automated Machine Learning
Azure Machine Learning が提供する Automated Machine Learning は、特徴量エンジニアリング & モデル選択 & パラメータ選択を全自動で行います。

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/service/media/tutorial-auto-train-models/flow2.png" width=400>
<br/><br/>


## Interpretability SDK

Azure Machine Learning service が提供するモデル解釈ライブラリ。機械学習モデルのモデル全体の説明変数の重要度 (グローバル) や個々の予測値に対する説明変数の重要度 (ローカル) を理解することが可能です。

### 基本コンポーネント

<img src="https://docs.microsoft.com/ja-jp/azure/machine-learning/service/media/machine-learning-interpretability-explainability/interpretability-architecture.png" width=600>

今回は Tabulear Data (表形式データ) について説明します。

### Mimic
**Global Surrogate** に対応したモデル解釈に対応する Explainer です。

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
**Permutation Feature Importance** に対応した Explainer です。

```python
from azureml.explain.model.permutation.permutation_importance import PFIExplainer 

# "features" and "classes" fields are optional
explainer = PFIExplainer(model, 
                         features=breast_cancer_data.feature_names, 
                         classes=classes)
```

<br/>

### Tabular Explainer

**SHAP** に対応した Explainer です。
- ツリーベースのモデルの場合は、SHAP TreeExplainer を適用
- DNN モデルの場合は、SHAP DeepExplainer を適用
- BlackBox モデルとして扱い、SHAP KernelExplainer を適用

```python
from azureml.explain.model.tabular_explainer import TabularExplainer
# "features" and "classes" fields are optional
explainer = TabularExplainer(model, 
                             x_train, 
                             features=breast_cancer_data.feature_names, 
                             classes=classes)
```
