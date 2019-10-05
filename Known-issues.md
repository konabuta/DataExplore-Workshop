# Known Issues
- Microsoft が把握している既知の問題
    - [Azure Machine Learning の既知の問題とトラブルシューティニング](https://docs.microsoft.com/ja-JP/azure/machine-learning/service/resource-known-issues) 
- Automated ML UX の画面がでてこない
    - ブラウザの新しいタブで再度アクセスを試みてください。
- Jupyter Notebook で Azure Machine Learning services の SDK が動作しない
    - 現在の Azure Machine Learning services の SDKは、 Python 3.6 以上で動作します。Kernel で Pythonのバージョンを確認してください。
- GPU クラスターの作成に失敗する
    - 無料アカウントの場合、GPU インスタンスのクォータ (利用可能CPU数) が不足しています。0 になっています。もし GPU インスタンスを利用したいという場合は、従量課金のアカウントへ切り替えてください。
    - 有償のアカウントの場合、GPUのコア数が不足している場合があります。サポートチケットを作成して、GPUコア数の引き上げのリクエストをしてください。即座に実施できるわけではなく、数営業日かかる場合もあります。
- New Workspace Experience に自分のサブスクリプション・ワークスペースが表示されない
    - 画面の右上の設定画面から適切なディレクトリを選択します。
- Microsoft Interpret ML がクラウド上で動作しない
    - Plotlyのサーバが関連する問題と思われます。showメソッドではなく、preserveメソッドを利用してください。<br/>
    
    
    ```python
    from interpret import preserve

    hist = ClassHistogram().explain_data(X_train, y_train, name = 'Train Data')
    preserve(hist, file_name = 'hist.html')

    ebm_global = ebm.explain_global(name='EBM')
    preserve(ebm_global)
    preserve(ebm_global,'ProcessA-Pressure')
    ```