---
title: Regression Suite Automation Tool のチュートリアル
description: このトピックでは、Regression Suite Automation Tool (RSAT) の使用方法について説明します。 さまざまな機能について説明し、高度なスクリプトを使用した例を示します。
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a194e14c76827650e6752f331081ebe0c2130a13
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866159"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool のチュートリアル

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> インターネット ブラウザーのツールを使用して、このページを PDF 形式でダウンロードして保存します。

このチュートリアルでは、デモの割り当て、戦略と重要な学習ポイントの説明を含む Regression Suite Automation Tool (RSAT) の高度な機能をいくつかを説明します。

## <a name="notable-features-of-rsat-and-task-recorder"></a>RSAT とタスク レコーダーの注目すべき機能

### <a name="validate-a-field-value"></a>フィールド値を検証する

RSAT を使用すると、予測値を検証するためにテスト ケース内に検証ステップを含めることができます。 この機能の詳細については、[予測値の検証](rsat-validate-expected.md) を参照してください。

次の例は、この機能を使用して、手持在庫が 0 (ゼロ) よりも大きいかどうかを検証する方法を示します。

1. **USMF** 会社のデモデータで、次の手順を含むタスク記録を作成します。

    1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
    2. クイック フィルターを使用して、レコードを見つけます。 たとえば、**1000** という値で **品目番号** フィールドをフィルター処理します。
    3. **手持在庫** を選択します。
    4. クイック フィルターを使用して、レコードを見つけます。 たとえば、**1** という値で **サイト** フィールドをフィルター処理します。
    5. 一覧で、選択された行をマークします。
    6. **引当可能合計数** フィールドの値が、**411.0000000000000000** であることを検証します。

2. タスク記録を **開発者記録** として保存し、Azure Devops のテスト ケースに関連付けます。
3. テスト ケースをテスト計画に追加し、テスト ケースを RSAT に読み込みます。
4. Excel パラメータ ファイルを開き、**TestCaseSteps** タブに移動します。
5. 常に **0** を超える在庫が存在するかどうかを検証するには、**利用できる合計の検証** ステップに移動し、その値を **411** から **0** に変更します。 **演算子** フィールドの値を、(**\>**) よりも大きい等号 (**=** ) に変更します。
6. Excel パラメーター ファイルを保存して閉じます。
7. **アップロード** を選択し、Excel パラメーター ファイルに加えた変更を Azure DevOps に保存します。

これで、指定した在庫品目の **引当可能合計数** フィールド値が0 ( ゼロ ) よりも大きい場合、実際の手持在庫値に関係なくテストが合格となります。

### <a name="saved-variables-and-chaining-of-test-cases"></a>保存された変数とテスト ケースの連鎖

RSAT の主要な機能の 1 つとして、テスト ケースの連鎖、つまり、変数を他のテストに渡すテストの機能、があります。 詳細については、[テスト ケースの連鎖への変数のコピー](rsat-chain-test-cases.md) を参照してください。

### <a name="derived-test-case"></a>派生テスト ケース

RSAT を使用すると、複数のテスト ケースで同じタスク レコードを使用して、タスクを異なるデータ構成で実行できます。 詳細については、[派生テスト ケース](rsat-derived-test-cases.md) を参照してください。

### <a name="validate-notifications-and-messages"></a>通知とメッセージの検証

この機能は、アクションが実行されたかどうかを検証するために使用できます。 たとえば、製造オーダーが作成、見積り、開始された時に、アプリは製造オーダーが開始されたことを通知する "生産 – 開始" メッセージを表示します。

![生産 – 開始通知](./media/use_rsa_tool_05.png)

RSAT を使用してこのメッセージを検証するには、該当する記録の Excel パラメーター ファイルにある **メッセージ検証** タブにメッセージ テキストを入力します。

![メッセージ検証タブ](./media/use_rsa_tool_06.png)

テスト ケースを実行すると、Excel パラメーター ファイル内のメッセージが、表示されるメッセージと比較されます。 メッセージが一致しない場合、テストケースは失敗します。

> [!NOTE]
> Excel パラメーター ファイルの **メッセージ検証** タブには、複数のメッセージを入力できます。 メッセージは、情報メッセージではなく、エラーまたは警告メッセージである場合もあります。

### <a name="snapshot"></a>スナップショット

この機能は、タスク記録中に実行された手順のスクリーンショットを撮ります。 これは、監査やデバッグの目的で役立ちます。

- この機能を使用するには、RSAT のインストール フォルダー (たとえば、**C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

テスト ケースを実行すると、RSAT は、作業ディレクトリ内のテスト ケースの再生フォルダにあるステップのスナップショット (画像) を生成します。 古いバージョンの RSAT を使用している場合、画像は **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** に保存され、実行される各テスト ケースに対して個別のフォルダが作成されます。

## <a name="assignment"></a>割り当て

### <a name="scenario"></a>シナリオ

1. 製品デザイナーが新しくリリースされた製品を作成します。
2. 生産マネージャは、在庫レベルを 2 個にするために製造オーダーを開始します。
3. 製造は、製造オーダーを開始および終了し、手持在庫数量が 2 個であることを確認します。
4. 販売チームは、新しい製品 4 個 の注文を受けます。 したがって、販売チームは動的計画を使って正味必要量を更新します。 追加の利用可能容量がないので、既定の注文ポリシーは "作成ではなく購入" に設定されます。 したがって、計画発注書が作成されます。
5. 購入者は、仕入先を追加し、計画発注書を確定してから、発注書を確認します。
6. 購入した商品が店舗に到着すると、店舗オペレーターが関連する発注書を検索して商品を受け取ります。 注文が完了したため、販売注文に対して商品をピッキングおよび梱包することができます。
7. 財務は、仕入請求書および売上請求書に転記します。

次の図は、このシナリオのフローを示しています。

![デモ シナリオのフロー](./media/use_rsa_tool_14.png)

次の図は、LCS ビジネス プロセス モデラーでのこのシナリオの業務プロセスの階層を示しています。

![デモ シナリオの業務プロセス](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>戦略 – キー学習

### <a name="data"></a>データ

- 代表的なデータボリューム (生産のコピー/高品質の構成データと移行されたデータ) があることを確認してください。
- タスク レコーダーを介して新しいデータを生成する場合は、既存の名前と競合しないテスト名 (例えば、**RSATxxx** などの接頭語を使用するなど) を作成します。
- Azure ポイントインタイム復元を使用して、第 1 層環境以外でテストを再実行します。
- Excel 関数の **RANDOM** や **NOW** を使用して、独自の組み合わせを生成することはできますが、その作業量は大幅に多くなります。 次に例を示します。

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>タスク レコーダー

- 記録を開始する前にシナリオを定義します。 適切に管理されたプロジェクトには、事前定義済みのテスト シナリオがあります。 テスト ケースを構築するには、それらのテスト シナリオの結果がどの程度予測可能かを考慮します。
- 異なるロールによって実行される場合、または待機時間がある場合、または次のステップの前に外部イベントがある場合に、記録を分割します。
- リストから値を選択することは避けてください。 代わりに、**FIFO**、**AudioRM**、**SiteWH** などのテキスト形式を使用します。 リスト内で選択した場合は、値自体ではなく、リスト内の値の位置が記録されます。 このリストに品目を追加すると、値の位置が変わる場合があります。 したがって、記録では別のパラメーターが使用され、その他のシナリオが影響を受ける可能性があります。
- マルチ ユーザーの動作について考えてみましょう。 たとえば、新しく作成された販売注文が常に自動的に選択されるとは限りません。 代わりに、常にフィルターを使用して正しい注文を見つけます。
- 連鎖したテスト ケースで使用できるように、タスク レコーダーのコピー機能を使用して、新しく作成された製品の名前を保存します。
- タスク レコーダーの検証機能を使用して、ステップが正常に実行されたことを確認するチェックポイントを設定します。

### <a name="rsat"></a>RSAT

- 別の会社でテストを実行するには、Excel パラメーター ファイルの **一般** タブで会社を変更します。 設定およびデータが、新しく選択した会社で使用可能であることを確認してください。
- テスト ユーザーは、Excel パラメーター ファイルの **一般** タブで変更できます。 テスト ケースを実行するユーザーの電子メール ID を指定します。 この方法で、指定したユーザーのセキュリティ アクセス許可を使用し、テスト ケースを実行できます。
- テストが開始されるまで待機するには、Excel パラメーター ファイルの **一般** タブで一時停止を定義します。 この一時停止は、バッチ ジョブで使用できます (たとえば、次のステップを実行する前にワークフローを実行する必要がある場合など)。

## <a name="advanced-scripting"></a>高度なスクリプト

### <a name="cli"></a>CLI

RSAT は、**コマンド プロンプト** または **PowerShell** ウィンドウから呼び出すことができます。

> [!NOTE]
> **TestRoot** 環境変数が RSAT インストール パスに設定されていることを確認します。 (Microsoft Windows の **コントロール パネル** を開き、**システムとセキュリティ\>システム\>高度なシステム設定** を選択し、**環境変数** を選択します。)

1. **コマンド プロンプト** または **PowerShell** ウィンドウを管理者として開きます。
2. RSAT インストール ディレクトリに移動します。

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. すべてのコマンドのリスト

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

使用可能なすべてのコマンドとそのパラメーターに関するヘルプを表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: オプションのパラメーター

`command`: ここでは、``[command]`` は以下で指定されたコマンドの 1 つです。

#### <a name="about"></a>情報:

現在のバージョンを表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

画面をクリアします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>ダウンロード

指定したテスト ケースの添付ファイルを出力ディレクトリにダウンロードします。
``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>ダウンロード: 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。
+ `output_dir`: 出力ディレクトリを表します。 このディレクトリが存在している必要があります。

##### <a name="download-examples"></a>ダウンロード: 例

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>編集

Excel プログラムでパラメーター ファイルを開いて編集できるようにします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>編集: 必須パラメーター

+ `excel_file`: 既存の Excel ファイルへの完全なパスが含まれている必要があります。

##### <a name="edit-examples"></a>編集: 例

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>作成

指定されたテスト ケースのテスト実行およびパラメーター ファイルを出力ディレクトリに生成します。 ``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>Generate : 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。
+ `output_dir`: 出力ディレクトリを表します。 このディレクトリが存在している必要があります。

##### <a name="generate-examples"></a>generate: 例

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

指定されたテスト ケースから派生する新しいテスト ケースを生成します。 ``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: 必須パラメータ

+ `parent_test_case_id`: 親テスト ケース ID を表します。
+ `test_plan_id`: テスト計画 ID を表します。
+ `test_suite_id`: テスト スイート ID を表します。

##### <a name="generatederived-examples"></a>generatederived: 例

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

指定されたテスト ケースのテスト実行ファイルのみを出力ディレクトリに生成します。 ``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。
+ `output_dir`: 出力ディレクトリを表します。 このディレクトリが存在している必要があります。

##### <a name="generatetestonly-examples"></a>generatetestonly: 例

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

指定されたスイートのすべてのテスト ケースを出力ディレクトリに生成します。 ``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。 最初の列の値を **test_suite_name** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: 必須パラメータ

+ `test_suite_name`: テスト スイートの名前を表します。
+ `output_dir`: 出力ディレクトリを表します。 このディレクトリが存在している必要があります。

##### <a name="generatetestsuite-examples"></a>generatetestsuite: 例

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>ヘルプ

[?](#section) と同一 コマンド。

#### <a name="list"></a>リスト

使用可能なすべてのテスト ケースを一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

使用可能なすべてのテスト計画を一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

指定されたテスト スイートのテスト ケースを一覧表示します。 ``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。 最初の列の値を **suite_name** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: 必須パラメータ

+ `suite_name`: 目的のスイートの名前。

##### <a name="listtestsuite-examples"></a>listtestsuite: 例

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

使用可能なすべてのテスト スイートを一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Excel ファイルを使用してテスト ケースを再生します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: 必須パラメータ

+ `excel_file`: Excel ファイルへの完全なパス。 ファイルが存在する必要があります。

##### <a name="playback-examples"></a>playback: 例

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

同時に複数のテスト ケースを再生します。 ``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: 必須パラメータ

+ `test_case_id1`: 既存のテスト ケースの ID。
+ `test_case_id2`: 既存のテスト ケースの ID。
+ `test_case_idN`: 既存のテスト ケースの ID。

##### <a name="playbackbyid-examples"></a>playbackbyid: 例

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Excel ファイルを使用して、同時に多数のテスト ケースを再生します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: 必須パラメータ

+ `excel_file1`: Excel ファイルへの完全なパス。 ファイルが存在する必要があります。
+ `excel_file2`: Excel ファイルへの完全なパス。 ファイルが存在する必要があります。
+ `excel_fileN`: Excel ファイルへの完全なパス。 ファイルが存在する必要があります。

##### <a name="playbackmany-examples"></a>playbackmany: 例

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

指定されたテスト スイートからすべてのテスト ケースを再生します。
``listtestsuitenames`` コマンドを使用すると、使用可能なすべてのテスト スイートを取得できます。 最初の列の値を **suite_name** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: 必須パラメータ

+ `suite_name`: 目的のスイートの名前。

##### <a name="playbacksuite-examples"></a>playbacksuite: 例

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

アプリケーションを閉じます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>アップロード

指定されたテスト スイートまたはテスト ケースに属するすべてのファイルをアップロードします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: 必須パラメータ

+ `suite_name`: 指定されたテスト スイートに属するすべてのファイルがアップロードされます。
+ `testcase_id`: 指定されたテスト ケースに属するすべてのファイルがアップロードされます。

##### <a name="upload-examples"></a>upload: 例

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

指定されたテスト ケースに属する記録ファイルのみをアップロードします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: 必須パラメータ

+ `testcase_id`: 指定されたテスト ケースに属する記録ファイルがアップロードされます。

##### <a name="uploadrecording-examples"></a>uploadrecording: 例

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>使用

このアプリケーションを呼び出す 2 つの方法を示します。1 つは既定の設定ファイルを使用する方法、もう 1 つは設定ファイルを提供する方法です。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell の例

#### <a name="run-a-test-case-in-a-loop"></a>ループでのテスト ケースの実行

新しい顧客を作成するテスト スクリプトがあります。 このテスト ケースは、スクリプトを使用し、各繰り返しを実行する前に次のデータをランダム化することによってループで実行できます。

- 顧客 ID
- 顧客名
- 顧客の住所

顧客 ID は、*ATCUS\<number\>* の形式で、\<number\>は **000000001** と **999999999** の間の値にします。

次の例は、1 つのパラメーター、**開始** を使用して、使用される最初の番号を定義します。 2 番目のパラメーター **nr** を使用して、作成する必要がある顧客数を定義します。 繰り返しごとに、Excel パラメーター ファイル内のパラメーターが UpdateCustomer 関数を使用して変更されます。 次に、RSAT コマンドラインは RunTestCase 関数内で呼び出されます。

管理者モードで Microsoft Windows PowerShell Integrated Scripting Environment (ISE) を開き、**Untitled1.ps1** という名前のウィンドウに次のコードを貼り付けます。

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Microsoft Dynamics 365 のデータに依存するスクリプトを実行する

次の例は、オープン データ プロトコル (OData) 呼び出しを使用して、発注書のオーダー状態を検索します。 ステータスが **請求済** ではない場合、たとえば、請求書を転記する RSAT のテスト ケースを呼び出すことができます。

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]