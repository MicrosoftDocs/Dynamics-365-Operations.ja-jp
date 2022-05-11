---
title: Dynamics 365 Translation Service Azure DevOps 拡張機能のチュートリアル (パブリック プレビュー)
description: このチュートリアルでは、Dynamics 365 Translation Service DevOps 拡張機能を Azure DevOps ワークフローに統合する方法を説明します。
author: joshsantana
ms.date: 04/14/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: joshsantana
ms.search.validFrom: 03-28-2022
ms.openlocfilehash: c566ae5dab70f3a455e2b557cf8a436a7f271adf
ms.sourcegitcommit: 11986a459c54555c434279ac97bf9c9ca96ec889
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2022
ms.locfileid: "8602565"
---
# <a name="dynamics-365-translation-service-azure-devops-extension-tutorial-public-preview"></a>Dynamics 365 Translation Service Azure DevOps 拡張機能のチュートリアル (パブリック プレビュー)

[!include[banner](../includes/banner.md)]
[!include[preview banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Translation Service (DTS) Azure DevOps 拡張機能は、パイプライン統合のための複数のタスクを提供します。 この拡張機能を使用して、Dynamics 365 ソリューションを Azure DevOps から効率的に翻訳します。

## <a name="learning-objectives"></a>学習目標

このチュートリアルでは、次の目標を達成します。

- DTS Azure DevOps 拡張機能の特徴と機能について説明します。
- Azure DevOps パイプラインを介して翻訳要求を送信します。
- 翻訳を修正し、再生成します。
- アライメント要求を送信して、以前に翻訳されたファイルから翻訳メモリを作成します。

## <a name="prerequisites"></a>必要条件

- Azure DevOps の一般情報
- Microsoft Dynamics Lifecycle Services (LCS) に関する一般的な理解

## <a name="install-and-configure-the-dts-azure-devops-extension"></a>DTS Azure DevOps 拡張機能の構成とインストール

### <a name="before-you-begin"></a>準備

この練習を行うには、Azure DevOps プロジェクトにアクセスできる必要があります。 パイプラインを実行できるリポジトリ (repo) も必要です。 さらに、LCS にアクセスできる必要があります。

この練習では、次のタスクを完了します。

- Azure DevOps 組織内に DTS 拡張機能をインストールします。
- LCS アプリケーション プログラミング インターフェイス (API) で使用出来るように、アプリケーションを登録します。
- LCS サービス接続を作成します。

### <a name="install-the-dts-azure-devops-extension"></a>DTS Azure DevOps 拡張機能をインストールする

1. Web ブラウザーで、[Visual Studio マーケットプレース](https://marketplace.visualstudio.com/)に移動します。
1. **Azure DevOps** タブで、**Dynamics 365 Translation Service** を検索します。
1. 検索結果から、**Dynamics Translation Service Tasks** 拡張機能を見つけ、開きます。
1. 拡張機能ページで、**無料で利用** を選択します。

    ![Dynamics Translation Service Tasks 拡張機能のページ。](media/dts-ado-tutorial-image2.png)

1. インストール ページで、拡張機能を Azure DevOps 組織にインストールするか、サーバー インストール用に VSIX パッケージをダウンロードするか選択します。 

拡張機能をインストールすると、組織内のどのパイプラインからでも利用できます。

### <a name="register-an-application"></a>アプリケーションを登録する

DTS API を利用するには、拡張機能が Microsoft ID プラットフォームからアクセス トークンを取得する必要があります。 LCS へのサービス接続は、拡張機能が API アクセス許可を取得するために必要な構成を提供します。 このサービス接続では、LCS アクセス許可で構成する登録済みアプリケーションを使用します。

1. 勤務先または学校アカウント、または個人の Microsoft アカウントを使用して、Azure ポータルにサインインします。
1. 検索バーに **アプリの登録** と入力を始めて、結果が表示されたらそれを選択します。
1. **アプリの登録** ページで、**新しい登録** を選択します。
1. **アプリケーションの登録** ページで、アプリケーションの登録に関する次の情報を入力します。

    - **名前** – 意味のある名前を入力します。
    - **サポートされるアカウント タイプ** – アプリがサポートする必要があるアカウントの種類を選択します。
    - **リダイレクト URL** - このフィールドはオプションです。 現在のユース ケースでは必要ありません。

1. 左側のナビゲーション ウィンドウの **管理** で、**API アクセス許可** を選択します。
1. **API アクセス許可** ページで、**アクセス許可の追加** を選択します。

    ![API アクセス許可ページに、アクセス許可ボタンを追加します。](media/dts-ado-tutorial-image5.png)

1. **組織が使用する API** タブで **LCS** を検索します。
1. **API アクセス許可の要求** ダイアログ ボックスで **user\_impersonation** 許可のチェックボックスを選択し、アプリケーションに LCS API へのアクセスを許可します。
1. **アクセス許可の追加** を選択します。

    ![API のアクセス許可の要求ダイアログ ボックスで選択された user_impersonation アクセス許可のチェック ボックス。](media/dts-ado-tutorial-image6.png)

1. 左側のナビゲーション ウィンドウの **管理** で、**認証** を選択します。
1. **認証** ページの **詳細設定** で、**パブリック クライアントのフローを許可** オプションを **はい** に設定します。

    ![認証ページでパブリック クライアント フローを許可するオプションを有効にします。](media/dts-ado-tutorial-image7.png)

1. **保存** を選択します。
1. 左側のナビゲーション ウィンドウで、**概要** を選択します。
1. 次のタスクで入力する必要があるため、アプリの登録概要ページでクライアント ID をメモしておきます。
1. **エンドポイント** を選択し、一覧で **OAuth 2.0 トークン エンドポイント** を見つけます。 このエンドポイントは、拡張機能サービス接続で使用される認証エンドポイントです。 次のタスクで入力する必要があるため、値をメモしておいてください。

    ![エンドポイント一覧の OAuth 2.0 トークン エンドポイント。](media/dts-ado-tutorial-image9.png)

### <a name="create-an-lcs-connection"></a>LCS 接続を作成する

LCS API 接続に登録されるアプリができたので、次に LCS サービス接続を作成できます。 このサービス接続により、拡張機能は登録済みのアプリケーションを介して、LCS のアクセス許可を取得できるようになります。

> [!NOTE]
> LCS 認証では、多要素認証がオフになっていて、フェデレーション サインイン によってサポートされていない Azure Active Directory (Azure AD) アカウントが必要です。サービス接続には、アクセス許可が制限された別のアカウントを使用することをお勧めします。

1. Azure DevOps プロジェクトの、左メニューの下にある **プロジェクト設定** ボタン (ギア記号) を選択します。
1. **プロジェクト設定** ウィンドウの **パイプライン** で、**サービスの接続** を選択します。 次に、**サービス接続を作成** を選択します。

    ![サービス接続ボタンを作成します。](media/dts-ado-tutorial-image10.png)

1. **新しいサービス接続** ダイアログ ボックスで、**Dynamics Lifecycle Services** サービス接続タイプを見つけ選択し、**次へ** を選択します。

    ![新しいサービス接続ダイアログ ボックスで選択された Dynamics Lifecycle Services サービス接続タイプ。](media/dts-ado-tutorial-image11.png)

1. サービス接続の情報を入力します。 アプリの登録時にメモしたクライアント ID と認証エンドポイントを使用します。 このサービスに対して選択した名前は、DTS DevOps 拡張タスクの入力として使用されます。 **Lifecycle Services AP エンドポイント** のフィールドには、既定値が入力されます。 欧州連合 (EU) 内ですべてのデータを処理する必要がある場合は、代わりに ``https://lcsapi.eu.lcs.dynamics.com`` を使用してください。

    ![新しいサービス接続の情報を入力します。](media/dts-ado-tutorial-image12.png)

### <a name="conclusion"></a>まとめ

この練習では、Azure DevOps 組織内の DTS 拡張機能を設定します。 これで、自動翻訳、再生成、および配置タスクのための新しいパイプラインを作成する準備が整いました。

## <a name="create-a-translation-pipeline"></a>翻訳パイプラインを作成する

DTS 拡張機能は、開発プロセスの一部として DTS 翻訳要求を自動化するタスクを提供します。 リソース ファイルを収集し、ローカライズのために、それらをに DTS にアップロードするように、翻訳タスクを構成できます。 その後、ローカライズされたファイルや翻訳メモリを確認し、必要に応じて調整できます。

### <a name="before-you-begin"></a>準備

この練習では、DTS 拡張機能がインストールされ、LCS サービス接続が構成されている Azure DevOps 組織にアクセスできる必要があります。 詳細については、[Azure DevOps 拡張機能のインストールと構成](dts-ado-tutorial.md#install-and-configure-the-dts-azure-devops-extension)セクションを参照してください。

この練習では、次のタスクを完了します。

- Azure DevOps プロジェクトで、翻訳要求のパイプラインを定義します。
- 翻訳パイプラインを実行します。
- 翻訳されたファイルを取得し、多言語エディタを使用して翻訳メモリを確認します。
- Azure DevOps プロジェクトで、再生成タスクのパイプラインを定義します。
- 再生成パイプラインを実行します。

### <a name="set-up-a-sample-repo-for-translation-jobs"></a>翻訳ジョブのサンプル レポジトリの設定

1. Azure DevOps プロジェクトを開き、レポジトリに移動します。
1. レポジトリのルートに、**res.label.txt** という名前で、次の内容のファイルを作成します。

    ```text
    Greeting=Hello

    Farewell=Goodbye

    InvalidFileHelpText=The specified file is invalid. Please try again.
    ```

1. 新しいファイルをレポジトリにコミットします。

### <a name="define-a-translation-pipeline"></a>翻訳パイプラインを定義する

1. 左側のメニューで、**パイプライン** を選択します。 **新しいパイプライン** を選択します。
1. ウィザードに従ってリポジトリを選択し、スターター パイプラインを作成します。
1. エディターで、**アシスタントを表示** メニュー項目を展開し、**DTS 翻訳** タスクを検索します。
1. **DTS 翻訳** タスクを構成する:

    1. **LCS サービス接続** フィールドで、先ほど作成したサービス接続を選択します。
    1. 任意の要求名を入力します。
    1. 製品として **財務と運用** を選択します。
    1. ソース言語として **英語** を選択します。
    1. ターゲット言語 (翻訳先の言語) を選択します。
    1. 翻訳タイプとして **ユーザー インターフェイス** を選択します。
    1. 前に作成したリソース ファイルのパス: **$(Build.SourcesDirectory)/\*.label.txt** を入力します。
    1. 出力パスとして **$(Build.ArtifactStagingDirectory)** を入力します。

1. **追加** を選択し、パイプラインにタスクを追加します。
1. **アシスタントを表示** メニュー項目を展開し、**パイプライン アーティファクトを発行** タスクを検索します。
1. **パイプライン アーティファクトを発行** タスクを構成する:

    1. **ファイルまたはディレクトリ パス** フィールドを **$(Build.ArtifactStagingDirectory)** に設定します。
    1. 任意のコンポーネント名を入力し、発行場所を **Azure Pipelines** に設定したままのままにします。

1. **追加** を選択し、パイプラインにタスクを追加します。
1. パイプラインを保存します。

### <a name="run-the-translation-pipeline"></a>翻訳パイプラインを実行する

パイプラインを保存した後に、自動実行をトリガーする必要があります。 パイプラインが自動実行されない場合、手動で実行できます。 **パイプライン** ページで、パイプラインの縦の省略記号 (3 つのドット) を選択し、**パイプラインの実行** を選択します。

![パイプライン ページでパイプラインを手動で実行します。](media/dts-ado-tutorial-image17.png)

### <a name="review-the-translation-pipeline-output"></a>翻訳パイプラインの出力を確認する

パイプラインが実行された後、パイプラインの概要ページにリダイレクトされます。

1. **ジョブ** リストからジョブを選択します。 **キューに追加済み** または **実行中** である必要があります。
1. **ジョブ出力** ウィンドウに、DTS 翻訳タスクが表示されます。 それを選択し、出力を表示します。
1. 出力で、翻訳 ID がジョブを識別します。 これは、LCS の DTS ダッシュボードにある ID に対応しています。 後で翻訳を再生成する時に値を入力する必要があるため、値をメモしておきます。

    ![ジョブ出力ウィンドウにある DTS 翻訳タスクの出力。](media/dts-ado-tutorial-image18.png)

    **パイプライン アーティファクトの発行** タスクを使って、パイプラインの概要ページから翻訳出力をダウンロードできます。

1. **戻る** ボタン (左矢印) を選択し、概要ページに戻ります。 
1. **関連** 列で、**1 発行済み** を選択します。

    ![パイプラインの概要ページの関連列にある 1 発行済み。](media/dts-ado-tutorial-image20.png)

1. **翻訳の確認** フォルダを開き、.xlf ファイルをダウンロードします。

### <a name="review-and-edit-the-translations"></a>翻訳を確認および編集

翻訳をダウンロードした後、それを確認し必要な変更を加えることができます。 任意の XLIFF エディターを使用できます。 ただし、無料の[多言語エディター](/windows/apps/design/globalizing/multilingual-app-toolkit-editor-downloads)を使用することをお勧めします。 このツールは、XLIFF ファイルに不要な変更が加えられるのを防ぐのに役立ちます。 次の例は、多言語エディターの使用方法を示しています。

1. 多言語エディターで .xlf ファイルを開きます。 エラーが発生した場合は、そのメッセージを無視します。
1. ウィンドウの左下隅にある **文字列** タブを選択します。
1. 翻訳を確認するために、**要確認** 状態にある文字列にフィルターを適用できます。 これにより、機械翻訳されたか、異なるリソース ID を持つ文字列からリサイクルされた翻訳のみを表示できます。
1. 翻訳を確認、編集し、期待通りの品質であることを確信したら、将来行われる要求に使用できるように、**翻訳済み**、 **最終**、または **サインオフ済み** としてマークしてください。
1. 文字列に任意の変更を加えてから、ファイルを保存します。 次のタスクでは、ファイルを使用してリソース ファイルを再生成します。

![多言語エディターでの翻訳文字列の確認と編集。](media/dts-ado-tutorial-image23.png)

### <a name="regenerate-the-translation"></a>翻訳を再生成する

XLIFF ファイルの翻訳の確認と編集が完了したら、翻訳されたネイティブ形式を再生成する必要があります。 DTS 拡張機能は、再生成プロセスを自動化するタスクを提供します。

1. 編集した .xlf ファイルをレポジトリにアップロードします。
1. [翻訳パイプラインの定義](#define-a-translation-pipeline)セクションで行ったように、**パイプライン** ページからリポジトリの新しいスターター パイプラインを作成します。
1. エディターで、**アシスタントを表示** メニュー項目を展開し、**DTS 再生成** タスクを検索します。
1. **DTS 再生成** タスクを構成する:

    1. **LCS サービス接続** フィールドで、先ほど作成したサービス接続を選択します。
    1. **再生成ファイル** フィールドに、編集した .xlf ファイルのパスを入力します。 そのファイルをレポジトリのルートに配置すると、パスは **$(Build.SourcesDirectory)/res.fr.label.txt.xlf** になります。
    1. **DTS 翻訳 ID** フィールドを、翻訳パイプラインの出力を確認したときにメモした翻訳 ID に設定します。
    1. **出力パス** フィールドを **$(Build.ArtifactStagingDirectory)** に設定します。

    ![構成された DTS 再生成タスク。](media/dts-ado-tutorial-image24.png)

1. パイプラインにのタスクを追加します。
1. **アシスタントを表示** メニュー項目を展開し、**パイプライン アーティファクトを発行** タスクを検索します。
1. **パイプライン アーティファクトを発行** タスクを構成する:

    1. **ファイルまたはディレクトリ パス** フィールドを **$(Build.ArtifactStagingDirectory)** に設定します。
    1. 任意のコンポーネント名を入力し、発行場所を **Azure Pipelines** に設定したままのままにします。

1. パイプラインにのタスクを追加します。
1. パイプラインを保存します。

### <a name="run-the-regeneration-pipeline"></a>再生成パイプラインを実行する

パイプラインを保存した後に、自動実行をトリガーする必要があります。 パイプラインが自動的に実行されない場合は、[翻訳パイプラインを実行](#run-the-translation-pipeline)セクションで行ったように、**パイプライン** ページから手動で実行できます。

### <a name="review-the-regeneration-pipeline-output"></a>再生成パイプラインの出力を確認する

パイプラインが実行された後、パイプラインの概要ページにリダイレクトされます。

1. **ジョブ** リストからジョブを選択します。 **キューに追加済み** または **実行中** である必要があります。
1. ジョブの実行が完了したら、**関連** 列で **1 発行済み** を選択して、再生成されたリソース ファイルと翻訳メモリを表示およびダウンロードします。

新しいリソース ファイルには、.xlf 翻訳メモリに対して確認中に行った編集が反映されている必要があります。

### <a name="optional-save-changes-it-git"></a>(オプション) Git に変更を保存する

翻訳完了後、ローカライズされたファイルをプロジェクトの Git リポジトリに保存するかもしれません。 Git コマンドを実行する前に、バージョン管理アクセス許可をパイプライン エージェントに付与する必要があります。

### <a name="grant-permissions"></a>アクセス許可を付与する

1. **組織の設定\> 一般 \> プロジェクト** に移動します。
1. 編集するプロジェクトを選択します。
1. **プロジェクト設定** ウィンドウの **Repos** で、**リポジトリ** を選択します。
1. この練習では、使用しているリポジトリを選択します。
1. **セキュリティ** タブを選択し、セキュリティ設定を編集します。
1. **Project Collection Build Service** ユーザーを検索し、実行する Git コマンドに必要なアクセス許可を付与します。 通常、次のアクセス許可が必要です。

    - 寄稿者
    - ブランチの作成
    - 既読

    ![Project Collection Build Service ユーザーにアクセス許可を付与します。](media/dts-ado-tutorial-image27.png)

### <a name="add-git-scripts-to-a-pipeline"></a>パイプラインへの Git スクリプトの追加

Git コマンドを実行する前に、スクリプトがシステム トークンにアクセスできるようにする必要があります。 **persistCredentials** パラメーターが **true** に設定されている **チェックアウト** ステップを追加することで、このタスクを完了することができます。

Windows PowerShell または bash スクリプト タスクの一部として、Git コマンドを追加できます。 次の例は、翻訳タスクの出力をコミットしてプッシュする bash スクリプトを示しています。 このスクリプトでは、**git config** コマンドを最初に 2 回呼び出して、ユーザーのメールアドレスと名前を設定します。 次に、**git checkout** コマンドを使用して新しいブランチを作成します。 次に、**git add** コマンドを使用して、**$(Build.SourcesDirectory)** のすべての変更をステージします。 次に、**git commit** コマンドを使用して、変更をローカルに保存します。 最後に、**git push** でローカルの変更をリモート リポジトリにアップロードします。

```YAML
- checkout: self

persistCredentials: true

- task: Bash@3

  inputs:

    targetType: 'inline'

    script: |

      # Write your commands here

      git config --global user.email "user@microsoft.com"

      git config --global user.name "User Name"

      git checkout -b localized

      git add $(Build.SourcesDirectory)

      git commit -m "Committing translations from pipeline"

      git push --set-upstream origin localized

    workingDirectory: '$(Build.SourcesDirectory)'

```

## <a name="create-a-translation-memory-from-previously-translated-files"></a>以前に翻訳されたファイルから翻訳メモリを作成する

DTS 配置タスクを使用して翻訳メモリ ファイルを作成できます。 以前に翻訳したファイルとそれに対応するソース ファイルがある場合、配置タスクを使用して XLIFF ファイルを生成できます。

### <a name="before-you-begin"></a>準備

この練習では、DTS 拡張機能がインストールされ、LCS サービス接続が構成されている Azure DevOps 組織にアクセスできる必要があります。 詳細については、[Azure DevOps 拡張機能のインストールと構成](dts-ado-tutorial.md#install-and-configure-the-dts-azure-devops-extension)セクションを参照してください。

この練習では、次のタスクを完了します。

- 配置タスクで使用できるパイプラインを定義します。
- パイプラインを実行し、結果を検査します。

### <a name="set-up-a-sample-repository-for-alignment-jobs"></a>配置ジョブのサンプル レポジトリを設定する

1. Azure DevOps プロジェクトを開き、レポジトリに移動します。
1. レポジトリのルートに、**res.label.txt** という名前で、次の内容のファイルを作成します。

    ```text
    Greeting=Hello

    Farewell=Goodbye

    InvalidFileHelpText=The specified file is invalid. Please try again.
    ```

1. **res.label.fr.txt** という名前で、次の内容のファイルを作成します。

    ```text
    Greeting=Bonjour

    Farewell=Au revoir

    InvalidFileHelpText=Le fichier spécifié n'est pas valide. Veuillez réessayer.
    ```

1. 両方のファイルをレポジトリにコミットします。

### <a name="define-an-alignment-pipeline"></a>配置パイプラインを定義する

1. 左側のメニューで、**パイプライン** を選択します。
1. 新しいスターター パイプラインを作成します。
1. エディターで、**アシスタントを表示** メニュー項目を展開し、**DTS 配置** タスクを検索します。
1. **DTS 配置** タスクを構成する:

    1. **LCS サービス接続** フィールドで、先ほど作成したサービス接続を選択します。
    1. 製品として **財務と運用** を選択します。
    1. ソース言語として **英語** を選択します。
    1. ターゲット言語として **フランス語** を選択します。
    1. 翻訳タイプとして **ユーザー インターフェイス** を選択します。
    1. **ソース ファイル** フィールドで、前に作成したリソース ファイルのパス: **$(Build.SourcesDirectory)/res.label.txt** を入力します。
    1. **ターゲット ファイル** フィールドに、**$(Build.SourcesDirectory)/res.label.fr.txt** と入力します。
    1. **出力パス** フィールドに、**$(Build.ArtifactStagingDirectory)** と入力します。

    ![パイプラインにのタスクを追加します。](media/dts-ado-tutorial-image29.png)

1. パイプラインにのタスクを追加します。
1. **アシスタントを表示** メニュー項目を展開し、**パイプライン アーティファクトを発行** タスクを検索します。
1. **パイプライン アーティファクトを発行** タスクを構成する:

    1. **ファイルまたはディレクトリ パス** フィールドを **$(Build.ArtifactStagingDirectory)** に設定します。
    1. 任意のコンポーネント名を入力し、発行場所を **Azure Pipelines** に設定したままのままにします。

1. パイプラインにのタスクを追加します。
1. パイプラインを保存します。

### <a name="run-the-alignment-pipeline"></a>配置パイプラインを実行する

パイプラインを保存した後に、自動実行をトリガーする必要があります。 パイプラインが自動実行されない場合、**Pipelines** ページから手動で実行できます。

### <a name="review-the-alignment-pipeline-output"></a>配置パイプラインの出力を確認する

パイプラインが実行された後、パイプラインの概要ページにリダイレクトされます。

1. **ジョブ** リストからジョブを選択します。 **キューに追加済み** または **実行中** である必要があります。
1. ジョブの実行が完了した後、発行されたコンポーネントを選択して、XLIFF ファイルを表示およびダウンロードできます。
1. [翻訳の確認と編集](#review-and-edit-the-translations)セクションで説明されているように、多言語エディターでファイルにさらに変更を加えるか、XLIFF ファイルを今後の翻訳要求のために翻訳メモリとして使用できます。

## <a name="summary"></a>要約

このチュートリアルでは、DTS Azure DevOps 拡張機能が提供する機能と特徴について学びました。 翻訳要求を自動化するパイプラインを作成する方法を学びました。 さらに、編集内容に基づいて、翻訳を編集し、それらを再生成する方法も学びました。 そして最後に、配置タスクを使用して XLIFF 翻訳メモリを作成する方法を学びました。
