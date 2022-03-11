---
title: Dynamics 365 Translation Service Azure DevOps の拡張機能
description: このトピックでは、Dynamics 365 Translation Service DevOps 拡張機能を Azure DevOps ワークフローに統合する方法を説明します。
author: joshsantana
ms.date: 02/09/2022
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: joshsantana
ms.search.validFrom: 2021-11-19
ms.openlocfilehash: 5f5b561b3d10661cb7d9eea2b978911391a5da2e
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109847"
---
# <a name="dynamics-365-translation-service-azure-devops-extension-public-preview"></a>Dynamics 365 Translation Service Azure DevOps 拡張機能 (パブリック プレビュー)

[!include[banner](../includes/banner.md)]

Azure DevOps の Microsoft Dynamics 365 Translation Service (DTS) 拡張機能では、DTS のアクションを実行できるよういくつかのパイプライン タスクが用意されています。 たとえば、ユーザー インターフェイス (UI) ファイルの変換、変換要求の再生成、および変換メモリ (TM) ファイルの作成を行うことができます。

DTS パイプライン タスクの使用を開始するには、組織に拡張機能をインストールし、Translation Service に接続する必要があります。 詳細については、このトピックで後述する[拡張機能の設定](#setting-up-the-extension) セクションを参照してください。

このトピックは、[Azure Pipelines](/azure/devops/pipelines/create-first-pipeline) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> Azure DevOps の DTS 拡張機能は、パブリック プレビューとしてのみ使用できます。 DTS は現在米国でのみ展開されているため、データは地域の境界外で処理および保管されることがあります。

## <a name="running-a-task"></a>タスクの実行

新しい変換、再生成、または要求の位置合わせを作成するには、パイプライン用の YAML で新しいタスクを追加します。

次の例では、新しい変換タスクの定義を示します。

```yaml
- task: DTSTranslation@0
    inputs:
        LCSConnection: 'DTS connection'
        requestName: 'My Request'
        productType: '2'
        productVersion: '5'
        sourceLanguage: 'en-US'
        targetLanguage: 'es'
        translationType: 'ui'
        sourceFile: '$(Build.SourcesDirectory)/resources/en-US/*.label.txt'
        translationOutputPath: '$(Build.ArtifactStagingDirectory)'
```

![Azure Pipelines UI での新しい変換タスクの定義。](media/dts-ado-pipeline-sample.PNG)

既定では、要求の出力は Build.ArtifactStagingDirectory ステージング フォルダに準備されます。 変換出力をダウンロードする方法については、[Azure Pipelines でコンポーネントの発行とダウンロード](/azure/devops/pipelines/artifacts/pipeline-artifacts) を参照してください。 変換出力をリポジトリにプッシュし返す場合は、[変換出力をリポジトリにコミット](#commit-translation-output-to-your-repository) を参照してください。

## <a name="overview-of-task-inputs"></a>タスク インプットの概要

### <a name="dts-translation-task"></a>DTS 変換タスク

変換タスクを使用すると、ユーザーが DTS を介して新しい変換要求を送信できます。

| 入力 | 必須 | Description |
|-------|----------|-------------|
| Dynamics Lifecycle Services のサービス コネクション | あり | LCS による認証で使用される Microsoft Dynamics Lifecycle Services (LCS) のサービス コネクション。 詳細については、トピックの後述の[サービス コネクションを作成](#create-a-service-connection) セクションを参照してください。 |
| 要求名 | あり | 要求名を入力します。 |
| 製品名 | あり | 製品名を選択します。 |
| 製品バージョン | あり | 製品バージョンを選択します。 |
| ソース言語 | あり | 変換される言語。 |
| ターゲット言語 | いいえ\* | 変換する言語。 |
| 複数のターゲット言語 | いいえ\* | <p>ターゲット言語コードのコンマ区切りの一覧。</p><p>この入力は、複数のターゲット言語の要求を送信するために使用されます。 設定されている場合、**ターゲット言語** 入力を上書きします。 次に例を示します: **ja、pt-BR、fr**。</p> |
| 換算タイプ | あり | <p>ファイル タイプを選択します。</p><p>**ユーザー インターフェイス** ファイルのみが現在サポートされています。 詳細については、[サポートされている製品とファイル タイプ](translation-service-overview.md#supported-products) を参照してください。</p> |
| リソース ファイルをパス | あり | <p>変換するファイルのパス。</p><p>パスのワイルド カードを使用できます。 サブフォルダーの再帰がサポートされます。 次に 2 つの例を挙げます。</p><p>`$(Build.SourcesDirectory)/**/*.label.txt`</p><p>`$(Build.SourcesDirectory)/resources`</p> |
| 変換メモリ ファイルにパス | いいえ | <p>TM ファイルのパス。</p><p>ワイルドカード文字がサポートされています。</p> |
| 出力パス | あり | 変換出力を保存するパス。 このパスはパイプラインを基準にしています。 詳細については、[Azure Pipelines のコンポーネント](/azure/devops/pipelines/artifacts/build-artifacts) を参照してください。 |

\*単一のターゲット言語を選択するか、または要求の一部として複数のターゲット言語を指定するか、どちらかが必要となります。

### <a name="dts-alignment-task"></a>DTS配置タスク

以前変換したファイルおよび対応するソース ファイルがある場合、配置ツールを使用すると XML ローカライズ変換ファイル形式 (XLIFF) で TM を作成できます。

| 入力 | 必須 | Description |
|-------|----------|-------------|
| Dynamics Lifecycle Services のサービス コネクション | あり | LCS 認証に使用される資格情報。 詳細については、トピックの後述の[サービス コネクションを作成](#create-a-service-connection) セクションを参照してください。 |
| 製品名 | あり | リソース ファイルを変換する製品。 |
| 製品バージョン | あり | 製品バージョンを選択します。 |
| ソース言語 | あり | 変換される言語。 |
| ターゲット言語 | あり | 変換する言語。 |
| ソース ファイル | あり | ソース ファイルのパス。 |
| ターゲット ファイル | あり | ラーゲット ファイルのパス。 |
| 出力パス | あり | 配置出力を保存するパス。 このパスはパイプラインを基準にしています。 詳細については、[Azure Pipelines のコンポーネント](/azure/devops/pipelines/artifacts/build-artifacts) を参照してください。 |

### <a name="dts-regeneration-task"></a>DTS 再生成タスク

再生成タスクを使用すると、ユーザーが DTS を介して新しい再生成要求を送信できます。

| 入力 | 必須 | Description |
|-------|----------|-------------|
| Dynamics Lifecycle Services のサービス コネクション | あり | LCS 認証に使用される資格情報。 詳細については、トピックの後述の[サービス コネクションを作成](#create-a-service-connection) セクションを参照してください。 |
| ファイルの再生成 | あり | 編集した TM ファイルのパス。 |
| DTS 変換 ID | あり | <p>元のトランザクションの ID。</p><p>[変換タスク](#dts-translation-task) から再生成している場合、変換 ID はタスク出力にあります。</p> |
| 出力パス | あり | 変換出力を保存するパス。 このパスはパイプラインを基準にしています。 詳細については、[Azure Pipelines のコンポーネント](/azure/devops/pipelines/artifacts/build-artifacts) を参照してください。 |

## <a name="setting-up-the-extension"></a>拡張機能の設定

### <a name="install-the-extension"></a>拡張機能をインストール

Azure DevOps 組織に拡張機能をインストールする場合は、次の手順に従います。

1. [Visual Studio Marketplace](https://marketplace.visualstudio.com/) を開きます。
2. **Azure DevOps** タブで、「Dynamics 365 Translation Service」を検索します。
3. **Dynamics Translation Service Tasks** 拡張機能をを検索して開きます。
4. 拡張機能ページで、**無料で利用** を選択します。

    ![Visual Studio Marketplace の Dynamics Translation Service Tasks 拡張機能。](media/dts-ado-task-marketplace.PNG)

5. インストール ページで、拡張機能をインストールする Azure DevOps組織を選択するか、またはサーバー インストールの VSIX パッケージをダウンロードするか選択できます。

拡張機能がインストールされた後、DTS タスクは Azure DevOps 組織のパイプラインで表示されます。

### <a name="register-an-application"></a>アプリケーションを登録する

DTSで認証するために LCS サービス接続を作成するには、まず適切な LCS アクセス許可を持つアプリを登録する必要があります。 次の手順は、アプリ登録プロセスについて説明しています。 また、LCSサービス接続を設定するために必要なクライアント ID と Azure Open Authorization (OAuth) エンドポイントを取得する方法も示しています。

1. LCS アプリ プログラミング インターフェイス (API) との通信に使用されるユーザーとして、[Azure ポータル](https://portal.azure.com/) にログインします。
2. **Azure サービス** で、**アプリの登録** を選択します。 
3. **アプリの登録** ページで、**新しい登録** を選択します。
4. **アプリの登録** ページの **名前** フィールドで、アプリ名を入力します。
5. **サポートされているアカウント タイプ** で、サポートするアカウントを指定するオプションを選択します。
6. **登録** を選択します。
7. 新しいアプリ登録ページの左ナビゲーション ウィンドウで、**管理** から **アプリのアクセス許可** を選択します。
8. **API アクセス許可** ページで、**アクセス許可の追加** を選択します。
9. **組織が使用する API** タブで、**Dynamics Lifecycle Services** API を見つけて選択します。
10. **user\_impersonation** スコープを所有する API アクセス許可のチェックボックスを選び、**アクセス許可の追加** を選択します。
11. アクセス許可に対する管理者の同意を許可する場合は、このボタンをクリックします。 アクションの確認を求められたら、**はい** を選択します。
12. 左側のナビゲーション ウィンドウの **管理** で、**認証** を選択します。
13. **認証** ページの **詳細設定** で、**パブリック クライアントのフローを許可** オプションを **はい** に設定します。
14. 左側のナビゲーション ウィンドウで、**概要** を選択します。
15. アプリ登録の概要ページには、クライアント ID が表示されます。 認証エンドポイントを検索するには、**エンドポイント** を選択します。 OAuth 2.0 トークン エンドポイントを使用します。

    ![Azure ポータルのエンドポイントの一覧にある OAuth 2.0 トークン エンドポイント。](./media/dts-ado-endpoint-list-app-registration.png)

### <a name="create-a-service-connection"></a>サービス接続の作成

これで LCS API 接続に登録されるアプリ作成されたので、次に LCS で認証を行うサービス接続を作成する必要があります。

> [!NOTE]
> LCS 認証では、多要素認証 (MFA) がオフで連合したサインインに支えられていない Azure Active Directory (Azure AD) アカウントが必要です。Microsoft では、API を有効にするための新しい認証機能と、作業がこれらのタイプの設定で認証されるオプションを検討しています。

サービス接続は次の手順に従います。

| 入力 | 必須 | Description |
|-------|----------|-------------|
| 認証エンドポイント | 有効 | アプリに使用するエンドポイント。 詳細については、[アプリの登録](#register-an-application) セクションを参照してください。 |
| Lifecycle Services API エンドポイント | 有効 | LCS API エンドポイント。  既定値は [https://lcsapi.lcs.dynamics.com] です。 すべての処理済みデータを欧州連合 (EU) 内で取得する必要がある場合は、https://lcsapi.eu.lcs.dynamics.com を使用します。
| ユーザー名 | 有効 | <p>DTS を使用して要求を送信するユーザー。</p><p><strong>注:</strong> MFA は無効にする必要があります。</p> |
| パスワード | あり | ユーザーのパスワード。 |
| クライアント ID | あり | 登録済アプリのクライアント ID。 詳細については、このトピックの前述の[アプリの登録](#register-an-application) セクションを参照してください。 |


1. Azure DevOps プリジェクトの左メニューの下部で、**プロジェクトの設定** を選択します。
2. **プロジェクト設定** ウィンドウの **パイプライン** で、**サービスの接続** を選択します。 次に、**サービス接続を作成** を選択します。
3. **新しいサービス接続** ダイアログ ボックスで、**Dynamics Lifecycle Services** サービス接続タイプを見つけ選択します。 その後、**次へ** を選択します。
4. サービス接続の情報を入力します。 登録されたアプリのクライアント ID と認証エンドポイントを使用します。 このサービスに対して選択した名前は、DTS Azure DevOps 拡張タスクの入力として使用されます。

    ![新しい Dynamics Lifecycle Services サービス接続のダイアログ ボックス。](./media/dts-ado-service-connection-populate.png)

## <a name="commit-translation-output-to-your-repository"></a>リポジトリに変換出力をコミット

変換が完了すると、ローカライズされたファイルをプロジェクトのリポジトリに自動的にプッシュすることに関心を持つかもしれません。 Git コマンドを実行する前に、バージョン管理アクセス許可をパイプライン エージェントに付与する必要があります。

1. **組織の設定\> 一般 \> プロジェクト** に移動します。
2. プロジェクト設定ページで、正しいプロジェクトを選択し編集します。
3. **プロジェクト設定** ウィンドウの **Repos** で、**リポジトリ** を選択します。 次に、このトピックで使用しているリポジトリを選択します。
4. **セキュリティ** タブを選択し、セキュリティ設定を編集します。
5. **Project Collection Build Service** ユーザーを検索します。
6. 実行したい Git コマンドに必要なアクセス許可を付与します。 通常、次のアクセス許可が必要です。

    - 寄稿者
    - ブランチの作成
    - 既読

    ![Azure DevOps のリポジトリ セキュリティ アクセス許可ページ。](./media/dts-ado-repo-perms.PNG)

### <a name="add-git-scripts-to-a-pipeline"></a>パイプラインへの Git スクリプトの追加

Git コマンドを実行する前に、スクリプトがシステム トークンにアクセスできるよう許可する必要があります。 この設定を完了するには、`persistCredentials` が *true* に設定されている `checkout` ステップを追加します。

PowerShell または bash スクリプト タスクの一部として、Git コマンドを追加できます。 次の bash スクリプトの例では、変換タスクの出力をコミットし、**ローカライズされた** という名のブランチをプッシュします。

```bash
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
