# Model-Agnostic Methods

モデルに依存しない汎用的なモデル解釈の主要アルゴリズムの概要を説明します。ニューラルネットワークなど複雑な Black Boxなモデルに適用できます。


<!-- ## Feature Importance
どの説明変数が目的変数に大きく影響し、逆にどの辺があまり影響していないのかを確認します。

- 品質に大きく影響している変数を特定する
- 売り上げに大きく影響している変数を特定する
- モデルの妥当性を確認する
etc

今回は、Permutationn Feature Importance という手法を用います。 -->

### Global Surrogate
グローバルなモデル解釈方法。構築済みの機械学習モデルに対するインプットデータと予測値から、解釈可能なモデルで学習し直して、モデル解釈をするアプローチ方法。


### Permutationn Feature Importance
グローバルなモデル解釈方法。インプットデータを変化させた際の予測値の変化の大きさから、変数の影響度を判断するアプローチ方法。

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

