# Microsoft Learn AI Fundamentals Labs

本リポジトリは[MicrosoftDocs/ai-fundamentals](https://github.com/MicrosoftDocs/ai-fundamentals)の非公式日本語化です。収録されているサンプルコードは、[Microsoft Azure AI Fundamentals](https://docs.microsoft.com/learn/certifications/azure-ai-fundamentals)資格の各関連ラーニングパスの演習に使われるように設計されています。


## 環境セットアップ

演習を完了するには、次のものが必要です。

- Microsoft Azure のサブスクリプション。お持ちでない場合は、<a href ='https://azure.microsoft.com/ja-jp/free/' target='_blank'>https://azure.microsoft.com/ja-jp/free/</a>で無料お試し版にサインアップ出来ます（方法については本Readmeで述べません）。Azure Passなどをお持ちの場合は、手持ちのものを使って下さい。
- Azure Machine Learning ワークスペース環境。この環境の中で、演習用のノートブックを実行します。まだお持ちでない場合、以下に従って準備して下さい：

### 1. Azure Machine Learning ワークスペースの作成

 - Azure portal (portal.azure.com) にサインインします。
   - **+ リソースの作成** を選択し、Machine Learning を検索し、次の設定を使用して新しい Machine Learning リソースを作成します。
   - **ワークスペース名**: 一意の名前を入力します（例：ai900-lab-workspace）
   - **サブスクリプション**: _お使いの Azure サブスクリプション_
   - **リソース グループ**: ユニークの名前で新しいリソース グループを作成します（例：ai900-lab-rg）
   - **場所**: 利用可能な場所を選択します（例：米国東部）
   - ワークスペース が作成されるまで待ちます (数分かかる場合があります)。 
 - 作成が終わったら **リソースに移動する** ボタンでPortal上のワークスペースページへ移動し、 **概要** ページで　**スタジオWeb URL**をクリックし、 Azure Machine Learning Studio を起動します。

### 2. コンピューティング インスタンスの作成

ノートブックを実行するのにコンピューティング インスタンスが必要です。既にある場合、次のステップに進んでください。ない場合は、次の手順に従って作成します。

 - Azure Machine Learning Studio で、左上にある ☰ アイコンをクリックし、**コンピューティング** ページ (**管理** の下にある) を表示します。
 - **Compute Instances**(コンピューティング インスタンス) タブで、下までスクロールし **+新規** ボタンをクリック、次の設定を使用して新しいコンピューティング インスタンスを作成します。
    - **コンピューティング名**: 一意の名前を入力します（例：ai900-instance）
    - **仮想マシンのタイプ**: CPU
    - **仮想マシンのサイズ**: Standard_DS11_v2(すべてのオプションから選択に切り替えて)
 - コンピューティング インスタンスが開始するまで、数分ほどかかる場合があります。その間に次のステップを開始して下さい。

### 3. 演習用ファイルのダウンロード

 - 左上にある ☰ アイコンをクリックし、**ノートブック** ページを表示します (**作成者** の下にあります) 。
 - **ファイル**の下にある4つボタンのうち、二番目の **+** ボタンをクリックし、新しいファイルを作成します。
    - **ファイルの場所**: Users/"自分のユーザー名"
    - **ファイル名**:　デフォルト設定のまま（「.ipynb」部分を削らないように気をつけて下さい）
    - **ファイルの種類**: ノートブック
    - **Overwrite if already exists**(既に存在する場合は上書きする): オン
 - 新しいノートブックが作成されたら、前に作成したコンピューティング インスタンスが **コンピューティング** ボックスで選択されていて、かつ状態が **実行中** であることを確認します。 次に、ノートブックに作成された四角形のセルに、次のコードを貼り付けます。

<a name="gitclone"></a>
```
!git clone https://github.com/wentingd/ai-fundamentals
```

 - セルの横にある **▷** ボタンを使ってコードを実行します。 これにより、GitHub から演習ファイルがクローンされます。
 - ファイルのダウンロードが完了したら、**ファイル** の右下にある ↻ ボタン（更新ボタン）をクリックし、ai-fundamentals という名前のフォルダーが作成されていて中にファイルがダウンロードされていることを確認します。

### 4. 演習をする

ai-fundamentals フォルダーの中にあるそれぞれの演習に該当するノートブック（.ipynbで終わるファイル）を開きます。 
トレーナー付き演習を実施している場合、トレーナーへ現在実行すべきノートブックについて確認して下さい。
ノートブックで書かれている情報をよく読み、指示に従ってAzure Portalでリソースを作成したり、それに含まれているコード セルを順番に実行してください。
(**≪** ボタンを使用してエクスプローラー ペインを折りたたむとスペースが広がるので、ノートブック タブに集中できます。)

### 5. クリーンアップ

演習が終わったら、Azure クレジットを不必要に使用することがないように、コンピューティング インスタンスを停止する必要があります。
 - Azure Machine Learning Studio で、**コンピューティング** ページ (**管理** の下) を表示します。
 - **Compute Instances**(コンピューティング インスタンス) タブで、ご自分のコンピューティング インスタンスを選択してから、**停止** ボタンを使用してそれを停止します。

## Contributing

現時点では、このリポジトリへの投稿は受け付けていません。演習で問題が発生した場合は、[report it](https://docs.microsoft.com/learn/support/troubleshooting#report-feedback)をお願いします。
