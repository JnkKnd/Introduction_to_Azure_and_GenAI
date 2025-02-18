# Introduction to Azure and Generative AI
プログラム「生成AIと Azure の基礎」でデモを行うための手順やコードをまとめています。

## 参考リンク集
#### Demo①：Azure OpenAI をチャットプレイグラウンドで簡単に試す
→画面共有しつつデモをしました\
https://learn.microsoft.com/ja-jp/azure/ai-studio/quickstarts/hear-speak-playground

#### Demo②：API で Azure OpenAI モデルを使う
→ python コードなどでつくったものを見せていました\
[Azure OpenAI Service の REST API リファレンス - Azure OpenAI | Microsoft Learn](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/reference)

#### Demo③：Personal Voice で自分の音声モデル作成
→ これはボランティアを募ってその場で自分の合成音声を作っていただきました。本人の合意があること、デモのみに使用し終了後は速やかに削除することを明示した上で行っています。\
https://learn.microsoft.com/ja-jp/azure/ai-services/speech-service/personal-voice-overview#how-to-create-a-personal-voice

#### Demo④：Add your data 機能で RAG を構築する
→簡単なファイルをアップロードさせて回答させました。\
https://learn.microsoft.com/ja-jp/azure/ai-services/openai/use-your-data-quickstart?tabs=command-line%2Ctypescript%2Cpython-new&pivots=programming-language-studio#add-your-data-using-azure-openai-studio

#### Demo⑤：Prompt Flow で RAG を構築する
→パワポに貼ってある動画の通りです。\
[プロンプト フローのビルド方法 - Azure AI Studio | Microsoft Learn](https://learn.microsoft.com/ja-jp/azure/ai-studio/how-to/flow-develop)

#### Demo⑥：Python SDK で RAG を構築する
→jupyter notebookでのpythonコードを作っており、ぽちぽちハンズオンが可能ですが、まだ Githubには挙げていないです…。新人向けとしては急にハードル高くなるので、雰囲気を見てもらう感じで紹介していました。\
[RAG と生成 AI - Azure AI Search | Microsoft Learn](https://learn.microsoft.com/ja-jp/azure/search/retrieval-augmented-generation-overview)

## 事前準備
1. Azure OpenAI リソースから gpt-4o のデプロイ
2. .env ファイルへの入力
2 

### リポジトリのクローン
- demo を分かりやすくするために、キーとエンドポイントを直打ちする場合がありますので、ローカルにクローンした上でご利用ください

### python 仮想環境の構築と有効化
今回は python 3.12 で行いました。
``` sh
python -m pip install --upgrade pip
python -m venv .venv
./.venv/Scripts/activate
```

### 必要なライブラリのインストール
``` sh
pip install -r .\requirements.txt
```

### Azure AI Foundry でのモデルデプロイ
Azure Portal から Azure OpenAI リソースを作成後、Azure AI Foundry でプロジェクトを作成し、 gpt-4o-mini をデプロイしてください。


### 環境変数の設定
.env-sample のファイル名を .env に変更し、プロジェクトの接続文字列を設定

## Demo 1 Azure Portal の画面

