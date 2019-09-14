# Model-Agnostic Methods

## Feature Importance
どの説明変数が目的変数に大きく影響し、逆にどの辺があまり影響していないのかを確認します。

- 品質に大きく影響している変数を特定する
- 売り上げに大きく影響している変数を特定する
- モデルの妥当性を確認する
etc

今回は、Permutationn Feature Importance という手法を用います。

## Partial Dependence Plot
重要度が高い変数と目的変数の関係を可視化する手法。非線形の関係も確認することができる。


## LIME (+SP-LIME)
KDD2016で採択されたモデル解釈のフレームワークです。Localな解釈が可能になる LIME と、Globalな解釈が可能になる SP-LIME の2つがございます。



## SHAP
NIPS 2017 で採択されたモデル解釈フレームワーク。ゲーム理論の shapley value (シャープレイ値) の枠組みをモデル解釈に利用するアプローチを採用。