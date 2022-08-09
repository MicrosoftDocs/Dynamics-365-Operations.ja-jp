---
title: Azure DevOps パイプラインと RSAT を統合する
description: この記事では、検証を自動化するために、Microsoft Azure DevOps パイプラインで Regression suite automation tool (RSAT) を統合する方法について説明します。
author: FrankDahl
ms.date: 04/05/2022
ms.topic: article
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2022-03-29
ms.openlocfilehash: 551db9bbf3c197ff508750da6981cbfebd26990a
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103685"
---
# <a name="integrate-rsat-with-azure-devops-pipelines"></a>Azure DevOps パイプラインと RSAT を統合する

[!include[banner](../../includes/banner.md)]

Microsoft Azure DevOps パイプラインを設定して、 Regression suite automation tool (RSAT) により、テスト スイートのスケジューリングと実行をシームレスに自動化することができます。

Azure DevOps パイプライン ジョブは、RSAT コマンドライン プログラム (Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe、RSAT コンソール アプリとも呼ばれる) を使用して、Windows PowerShell タスクを介して RSAT を実行できます。 また、Visual Studio マーケットプレースで使用できるコンフィギュレーション済み RSAT タスクを Azure DevOps パイプラインに追加することもできます。 この方法で、カスタムの Windows PowerShell のスクリプトを記述せずに、RSAT の複数のテスト スイートをビルドまたは実行できます。

この記事では、Azure DevOps 組織および[パイプライン](/azure/devops/pipelines) の管理に慣れている方を想定しています。 RSAT 機能に慣れている方も想定しています。

## <a name="prerequisite-install-an-azure-devops-self-hosted-windows-agent"></a>前提条件: Azure DevOps の自己ホスト Windows エージェントのインストール

Azure DevOps パイプラインを構成して RSAT タスクを含めるには、RSAT がインストールされているコンピューターで自己ホスト Windows エージェントを構成する必要があります。 このプロセスの詳細については、[Azure Pipelines エージェント](/azure/devops/pipelines/agents/agents?view=vsts) を参照してください。 自己ホスト Windows エージェントの設定方法については、[自己ホスト Windows エージェント](/azure/devops/pipelines/agents/v2-windows) を参照してください。

Azure DevOps エージェントを構成するときは、次のガイドラインに従います。

- 1 つのエージェントを使用する専用のエージェント プールを作成します。 この方法で、パイプライン タスク全体で同じコンピューターが使用されます。 また、機能は無視できます。 64-ビット バージョンのエージェント ソフトウェアを、RSAT クライアント コンピューターにインストールします。
- 各 RSAT クライアント コンピューターで 1 つのエージェントだけを実行します。
- エージェントをローカル Windows 管理者ユーザー アカウントとして実行してください。 ネットワーク サービスを使用してそのサービスを実行することはできません。 RSAT クライアント コンピューターの管理者が使用する場合は、独自のユーザー アカウントを使用することもできます。
- エージェントを対話型で実行するか、Windows サービスとして実行するか決定します。 対話的に実行するエージェントの設定の方が簡単です。 また、この方法により、エージェントの実行時に手動で制御できます。 Windows サービスとして実行するエージェントを設定するには、さらに手順を実行する必要があります。 ただし、この方法によって、エージェントの実行は自動化されます。
- エージェントを Windows サービスとして実行する場合は、次の追加手順に従います。

    > [!IMPORTANT]
    > セットアップ全体で同じ Windows 管理者ユーザー アカウントが使用されている必要があります。

    1. Windows で、コンポーネント サービス アプリを見つけて開きます。

        選択した Windows 管理者ユーザー アカウントでエージェント サービスを実行するには、最初にそのサービスを構成する必要があります。

    2. **サービス (ローカル)** を選択し、エージェント サービスを検索します。 サービスの名前は、次のような形式になります。

        - Azure Pipelines エージェント \<name of your agent\>
        - VSTS エージェント \<name of your agent\>
        - vstsagent.\<organization name\>.\<name of your agent\>

    3. エージェント サービスを選択したまま (または右クリックしてから)、**プロパティ** を選択します。
    4. **ID** タブで、**このユーザー** オプションを選択し、Azure DevOps エージェントを実行するローカル管理者ユーザーを指定します。 *domain\\username* 形式を使用します。 次にパスワードを入力して確認します。

        次に、エージェント サービスのアクセス許可を取得して Microsoft Excel COM オブジェクトにアクセスする必要があります。

    5. コンポーネント サービス アプリで、**コンポーネント サービス**\>**コンピューター**\>**マイ コンピューター** を展開し、**DCOM Config** を選択します。
    6. **Microsoft Excel アプリケーション** を検索します (または **000208D5-0000-0000-C000-000000000046**: この値は、コンピューターにインストールされている Excel のバージョンによって異なる場合があります)。
    7. 選択したまま (または右クリックにしてから)、**プロパティ** を選択します。
    8. **セキュリティ** タブの **起動とアクティベーションのアクセス許可** カテゴリで、**カスタマイズ** オプションを選択します。 次に、**編集** を選択し、ユーザーへの完全なアクセスを提供します。 他の 2 つのアクセス許可カテゴリ (**アクセス許可** と **コンフィギュレーションのアクセス許可**) を繰り返します。

        ![Excel DCOM セキュリティをコンフィギュレーションしています。](media/excel-dcom-security.png)  

## <a name="configure-azure-devops-pipelines-to-run-rsat-tasks"></a>Azure DevOps パイプラインを構成して、RSAT タスクを実行する

Azure DevOps パイプラインを構成して RSAT タスクを実行する場合、次の 2 つのオプションがあります。

- [Visual Studio マーケットプレース](https://marketplace.visualstudio.com/azuredevops/) で使用できる Azure DevOps RSAT 拡張機能を使用します。 この拡張機能には、簡単に構成されたタスクが含まれており、このタスクを使用してカスタムの Windows PowerShell スクリプトを記述することなく RSAT テスト スイートを構築し、実行できます。
- カスタム Windows PowerShell タスクを使用して、RSAT コンソール アプリを使用する独自のスクリプトを作成します。 このオプションによって最大の柔軟性が提供されますが、より専門的な知識が必要になります。

## <a name="install-the-azure-devops-rsat-extension"></a>Azure DevOps RSAT 拡張機能をインストールする

Azure DevOps RSAT 拡張機能は、RSAT テスト スイートをビルドし実行する RSAT タスクを含む Visual Studio マーケットプレース パッケージです。 既成の RSAT タスクを使用するには、この拡張機能をインストールする必要があります。 RSAT バージョン 2.4.11480.52 またはそれ以降が必要です。

### <a name="install-the-extension"></a>拡張機能をインストール

1. Azure DevOps で、組織の設定を開きます。
2. **拡張機能** タブを選択してから、ページの右側にある **マーケットプレースを参照** を選択します。
3. 「RSAT」を検索し、**Regression Suite Automation Tool** という名前の拡張機能を探します。 Azure DevOps 組織の管理者または所有者である場合は、拡張機能を選択し、次に **無料で利用** を選択してインストールします。

Azure DevOps 組織に拡張機能をインストールした後 、拡張機能によって提供される RSAT タスクを使用するパイプラインを作成できます。 RSAT タスクを作成する新しいパイプラインに、または編集する既成のパイプラインに追加できます。 

## <a name="create-a-pipeline"></a>パイプラインを作成する

Azure Dev Ops エージェントを設定した後は、次の手順に従ってパイプラインを作成します。

1. Azure DevOps で、パイプラインをホストするプロジェクトを選択します。 次に、**パイプライン** に移動し、 右上隅の **新しいパイプライン** を選択します。

    パイプラインは YAML を使用して設計できます。 この方法は強力ですが、習得するにはある程度の経験が必要です。 この記事はパイプラインの設計について詳細な情報を提供することではなく、開始を助けることを目的としているので、この手順は YAML を使用せずに基本的なパイプラインを構築する方法を示しています。

2. **クラシック エディターを使用する** リンクを選択して、YAML を使用せずにパイプラインを作成します。

    ![クラシック エディターのリンクを使用します。](media/pipeline-connect.png)

3. リポジトリ ソースを選択し、次に **続行** を選択します。

    ![リポジトリを選択しています。](media/pipeline-repos.png)

4. 次のページで、**空のジョブ** リンクを選択して、タスクのない空のパイプラインを作成します。

    ![空のジョブ リンク。](media/pipeline-new-job.png)

5. パイプライン項目を選択します。 パイプラインの名前を入力し、前に作成したエージェント プールを指定します。

    ![パイプライン項目を構成します。](media/pipeline-pipeline-edit.png)

6. エージェント ジョブ項目を選択します。 ジョブの表示名を入力します。 パイプライン全体で同じエージェント プールを使用するには、**エージェント プール** フィールド セットを **\<inherit from pipeline\>** に設定したままにします。 **並列処理** フィールド グループで、**なし** のオプションを選択したままにします。

    ![エージェント ジョブ項目を構成します。](media/pipeline-job-edit.png)

## <a name="add-rsat-tasks-to-a-pipeline"></a>パイプラインへの RSAT タスクの追加

この手順では、既存のパイプライン ジョブに RSAT タスクを追加する方法を示します。 RSAT タスクは、Visual Studio マーケットプレースで使用できる Azure DevOps RSAT 拡張機能の一部です。 これらのタスクは簡単に構成でき、カスタム スクリプトを記述することなく、RSAT テスト スイートをビルトして実行できます。

1. Azure DevOps で、パイプラインをホストするプロジェクトを選択します。 次に **パイプライン** に移動します。
2. 新しいタスクを追加するジョブ項目のプラス記号 (**+**) を選択します。

    ![ジョブ項目へタスクを追加しています。](media/pipeline-new-task.png)

3. 「RSAT」を検索し、**Regression Suite Automation Tool** タスクを探し、**追加** を選択します。

    ![新しい Regression Suite Automation Tool タスクを追加しています。](media/pipeline-new-rsat-task.png)

    RSAT タスクは 2 つのモードで実行できます。

    - **ビルド**- 1 つ以上の RSAT テスト スイートに対してテスト自動化ファイルを生成します。 記録を変更したり、新しいバージョンの RSAT をインストールした後でビルド タスクを実行する必要があります。
    - **実行**- 1 つ以上の RSAT テスト スイートを実行します。

    ビルド タスクと実行タスクの両方を含むパイプラインでは、タスクを実行する前にビルド タスクを使用して実行ファイルを準備します。

4. 次のいずれかの手順を使用して、RSAT タスクをビルド タスクまたは実行タスクとして構成します。

### <a name="option-1-build-test-suites"></a>オプション 1: テスト スイートをビルドする

1. タスクの表示名を入力します。
2. **コマンド** フィールド グループで、**テスト ケースのビルド** オプションを選択して、テスト スイートをビルドするタスクを作成します。 このタスクによって、テスト実行ファイルが生成され、Azure DevOps テスト ケースにアップロードされます。 記録を変更したり、新しいバージョンの RSAT をインストールした後でこのタスクを実行する必要があります。
3. **RSAT の場所** で、RSAT インストール フォルダーを再確認します。
4. RSAT 設定ファイルの場所を入力する 設定ファイルは、RSAT 設定ダイアログ ボックスから保存できます。 テスト計画の場所、財務と運用テスト環境の URL、優先ブラウザーなどの情報が含まれます。
5. 既存の Excel パラメーターを再生成または上書きしない場合、**テスト実行ファイルのみを生成する** チェックボックスをオンにします。 このシナリオが最も一般的であり、チェックボックスは既定でオンになっています。
6. **テスト スイートを使用する** フィールド グループで、テスト スイートを名前または ID で指定するかどうかを選択します。
7. ビルドするテスト スイートの名前または ID を入力します。 複数のテスト スイートを指定するには、コンマを使用して値を区切ります。
8. タスクの実行時にテスト ケースが使用されている状況を管理するには、**テスト ケースがブロックされている場合に再試行する** チェックボックスを選択し、**再試行の一時停止** フィールドに秒数を入力します。 その後、ビルド タスクは指定した秒の間一時停止してから再開できます。

![新しい RSAT ビルド タスクを構成しています。](media/pipeline-rsat-build-task.png)

### <a name="option-2-run-test-suites"></a>オプション 2: テスト スイートの実行

1. タスクの表示名を入力します。
2. **コマンド** フィールド グループで、**テスト ケースの実行** オプションを選択して、既に実行しているテスト スイートを実行するタスクを作成します。
3. **RSAT の場所** で、RSAT インストール フォルダーを再確認します。
4. RSAT 設定ファイルの場所を入力する 設定ファイルは、RSAT 設定ダイアログ ボックスから保存できます。 テスト計画の場所、財務と運用テスト環境の URL、優先ブラウザーなどの情報が含まれます。
5. 実行を開始する前に、Azure DevOps テスト ケースから添付ファイル (テスト実行およびパラメーター ファイル) をダウンロードする場合は、**ダウンロード** チェックボックスを選択します。 ファイルを以前のビルド タスクからダウンロードした場合は、このチェックボックスをオフにします。 この場合、作業ディレクトリの現在のファイルが使用されます。
6. **テスト スイートを使用する** フィールド グループで、テスト スイートを名前または ID で指定するかどうかを選択します。
7. 実行するテスト スイートの名前または ID を入力します。  複数のテスト スイートを指定するには、コンマを使用して値を区切ります。
8. オプション: **コメント** フィールドに、テキストを入力します。 Azure DevOps 変数を含めることができます。 このテキストは、後日参照用としてテスト実行の集計結果およびテスト ケース結果に記録されます。

![新しい RSAT 実行タスクを構成しています。](media/pipeline-rsat-execute-task.png)

## <a name="add-a-custom-windows-powershell-task"></a>カスタム Windows PowerShell タスクを追加する

独自のカスタム スクリプトを使用する場合は、RSAT タスクを使用する代わりにパイプライン ジョブに Windows PowerShell タスクを追加できます。 独自のスクリプトを作成する予定がある場合は、RSAT Azure DevOps 拡張機能は必要ありません。

1. Azure DevOps で、パイプラインをホストするプロジェクトを選択します。 次に **パイプライン** に移動します。
2. 新しいタスクを追加するジョブ項目のプラス記号 (**+**) を選択します。
3. 「PowerShell」を検索し、**PowerShell** タスクを探して、**追加** を選択します。

    ![新しい PowerShell タスクを追加しています。](media/pipeline-new-powershell-task.png)

4. PowerShell スクリプト タスクを選択します。 **タイプ** フィールド グループで、**インライン** オプションを選択し、次に RSAT コンソール アプリ (Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe) を使用してスクリプトを作成します。 または、**ファイル パス** オプションを選択し、次に Windows PowerShell スクリプトのパスを入力します。

    ![PowerShell スクリプト タスクを構築しています。](media/pipeline-powershell-task.png)

## <a name="schedule-a-pipeline"></a>パイプラインのスケジュール設定

Azure DevOps パイプラインを作成した後、パイプラインを手動でトリガー、スケジュール、または事前に定義された繰り返しスケジュールで実行するように構成できます。

![パイプラインの実行をスケジュールしています。](media/pipeline-schedule.png)

## <a name="using-the-rsat-console-app"></a>RSAT コンソール アプリの使用

RSAT コンソール アプリ (Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe) を使用すると、RSAT Windows アプリを通じて使用できる RSAT 機能をプログラムを使用して実行できます。 このファイルは、メインの RSAT インストール フォルダー (既定では C: \\Program Files (x86)\\Regression Suite Automation Tool\\) にあります。 対話モードまたはコマンド モードで使用できます。

RSAT コマンドの詳細については、[Regression suite automation tool (RSAT) - 高度なスクリプト](rsat-tutorial.md#advanced-scripting) を参照してください。

### <a name="interactive-mode-and-help"></a>対話型モードとヘルプ

対話モードで RSAT コンソール アプリを使用するには、コマンド プロンプト ウィンドウまたは Windows PowerShell を使用して Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe を実行します。 対話型モードは、コマンドをテストする場合やヘルプを表示する場合に便利です。

1. コマンド プロンプト ウィンドウまたは Windows PowerShell を管理者として開きます。
2. RSAT インストール フォルダーに移動します。
3. `Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe` を実行し、対話型モードでアプリを開きます。

    ![対話型モードでの RSAT コンソール アプリ](media/rsatconsole-interactive.png)

4. `help` コマンドを使用して、使用可能な任意の RSAT コマンドについてヘルプを表示します。 次にいくつか例を挙げます。

    - `help playbacksuite`

        ![plaubacksuite RSAT コマンドのヘルプ。](media/rsatconsole-help-1.png)

    - `help generatetestsuite`

        ![generatetestsuite コマンドのヘルプ。](media/rsatconsole-help-2.png)

### <a name="command-mode"></a>コマンド モード

コマンド モードは、1 つのコマンドを実行する場合や、カスタムの Windows PowerShell スクリプトで RSAT コマンドを使用する場合に便利です。

次にいくつか例を挙げます。

- `.\Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playbacksuite /byid 47`
- `.\Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe listtestsuitenames`

### <a name="run-the-console-app-with-a-specific-settings-file"></a>特定の設定ファイルを使用したコンソール アプリの実行

既定では、コンソール アプリは、RSAT ユーザー インターフェイスを通してユーザー アカウントによって構成された設定を使用します。 別の設定ファイルを指定するには、次の例に示すように、`settings` パラメーターを使用します。

`.\Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Users\rob\Documents\RSAT\SettingFiles\Canaryenv.settings" playbacksuite "Acceptance Test Suite 1"`

