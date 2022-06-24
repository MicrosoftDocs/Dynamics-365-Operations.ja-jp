---
title: Regression Suite Automation Tool のチュートリアル
description: この記事では、Regression Suite Automation Tool (RSAT) の使用方法について説明します。 さまざまな機能について説明し、高度なスクリプトを使用した例を示します。
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 04c7d7081ece4e077881092534ed061fe2d0e999
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854602"
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

2. タスク記録を **開発者の記録** として保存し、Azure DevOps のテスト ケースに関連付けます。
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

![生産 – 開始通知。](./media/use_rsa_tool_05.png)

RSAT を使用してこのメッセージを検証するには、該当する記録の Excel パラメーター ファイルにある **メッセージ検証** タブにメッセージ テキストを入力します。

![メッセージ検証タブ。](./media/use_rsa_tool_06.png)

テスト ケースを実行すると、Excel パラメーター ファイル内のメッセージが、表示されるメッセージと比較されます。 メッセージが一致しない場合、テストケースは失敗します。

> [!NOTE]
> Excel パラメーター ファイルの **メッセージ検証** タブには、複数のメッセージを入力できます。 メッセージは、情報メッセージではなく、エラーまたは警告メッセージである場合もあります。

### <a name="snapshot"></a>スナップショット

この機能は、タスク記録中に実行された手順のスクリーンショットを撮ります。 これは、監査やデバッグの目的で役立ちます。

- ユーザー インターフェイスを使用して RSAT を実行しているときにこの機能を使用するには、RSAT のインストール ホルダー (例: **C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- CLI (例: Azure DevOps) で RSAT を実行しているときにこの機能を使用するには、RSAT のインストール ホルダー (例: **C:\\Program Files (x86)\\Regression Suite Automation Tool**) にある **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** ファイルを開き、次の要素の値を **False** から **True** に変更します。

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

テスト ケースを実行すると、RSAT は、ステップのスナップショット (画像) を生成し、作業ディレクトリ内のテスト ケースの再生フォルダーに保存します。 再生フォルダーには、**StepSnapshots** という別のサブフォルダーが作成されます。 そのフォルダーには、実行されたテスト ケースのスナップショットが格納されます。

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

![デモ シナリオのフロー。](./media/use_rsa_tool_14.png)

次の図は、LCS ビジネス プロセス モデラーでのこのシナリオの業務プロセスの階層を示しています。

![デモ シナリオの業務プロセス。](./media/use_rsa_tool_15.png)

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

すべてのコマンドを一覧表示するか、特定のコマンドのヘルプを使用可能なパラメーターと共に表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: オプションのパラメーター

`command`: ``[command]`` は上記の一覧のコマンドの 1 つです。

#### <a name="about"></a>情報:

インストールされている RSAT のバージョンを表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

画面をクリアします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>ダウンロード

指定したテスト ケースの添付ファイル (レコード、実行、パラメーター ファイル) を Azure DevOps から出力ディレクトリにダウンロードします。 ``list`` コマンドを使用して、使用可能なすべてのテスト ケースを取得し、最初の列の任意の値を **test_case_id** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、ダウンロード プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。

##### <a name="download-required-parameters"></a>ダウンロード: 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。

##### <a name="download-optional-parameters"></a>download: オプション パラメーター

+ `output_dir`: 出力作業ディレクトリを表します。 このディレクトリが存在している必要があります。 このパラメーターが指定されていない場合は、設定の作業ディレクトリが使用されます。

##### <a name="download-examples"></a>ダウンロード: 例

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

指定したテスト スイートにあるすべてのテスト ケースの添付ファイル (レコード、実行、パラメーター ファイル) を Azure DevOps から出力ディレクトリにダウンロードします。 ``listtestsuitenames`` コマンドを使用して、使用可能なすべてのテスト スイートを取得し、任意の値を **test_suite_name** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、ダウンロード プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/byid`: このスイッチは、目的のテスト スイートが、テスト スイート名ではなく Azure DevOps IDで識別されることを示します。

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: 必須パラメーター

+ `test_suite_name`: テスト スイートの名前を表します。 /byid スイッチが指定されて **いない** 場合、このパラメーターは必須です。 この名前は Azure DevOps テスト スイート名です。
+ `test_suite_id`: テスト スイート ID を表します。 /byid スイッチが指定されて **いる** 場合、このパラメーターは必須です。 この ID はテスト スイート Azure DevOps ID です。

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: オプション パラメーター

+ `output_dir`: 出力作業ディレクトリを表します。 このディレクトリが存在している必要があります。 このパラメーターが指定されていない場合は、設定の作業ディレクトリが使用されます。

##### <a name="downloadsuite-examples"></a>downloadsuite: 例

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>編集

Excel プログラムでパラメーター ファイルを開いて編集できるようにします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>編集: 必須パラメーター

+ `excel_file`: 既存の Excel ファイルへの完全なパスが含まれている必要があります。

##### <a name="edit-examples"></a>編集: 例

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>作成

指定されたテスト ケースのテスト実行およびパラメーター ファイルを出力ディレクトリに生成します。 ``list`` コマンドを使用すると、使用可能なすべてのテスト ケースを取得できます。 最初の列の値を **test_case_id** パラメーターとして使用します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、生成プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/dllonly`: テスト実行ファイルのみ生成します。 Excel パラメーター ファイルを再生成しないでください。
+ `/keepcustomexcel`: 既存のパラメーター ファイルをアップグレードします。 実行ファイルも再生成します。

##### <a name="generate-required-parameters"></a>Generate : 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。

##### <a name="generate-optional-parameters"></a>generate: オプション パラメーター

+ `output_dir`: 出力作業ディレクトリを表します。 このディレクトリが存在している必要があります。 このパラメーターが指定されていない場合は、設定の作業ディレクトリが使用されます。

##### <a name="generate-examples"></a>generate: 例

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

指定したテスト ケースの新しい派生テスト ケース (子テスト ケース) を生成します。 新しいテスト ケースは、指定したテスト スイートにも追加されます。 ``list`` コマンドを使用して、使用可能なすべてのテスト ケースを取得し、最初の列の任意の値を **test_case_id** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、生成プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。

##### <a name="generatederived-required-parameters"></a>generatederived: 必須パラメータ

+ `parent_test_case_id`: 親テスト ケース ID を表します。
+ `test_plan_id`: テスト計画 ID を表します。
+ `test_suite_id`: テスト スイート ID を表します。

##### <a name="generatederived-examples"></a>generatederived: 例

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

指定したテスト ケースのテスト実行ファイルのみを生成します。 Excel パラメーター ファイルは生成されません。 ファイルは、指定した出力ディレクトリに生成されます。 ``list`` コマンドを使用して、使用可能なすべてのテスト ケースを取得し、最初の列の任意の値を **test_case_id** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、生成プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: 必須パラメータ

+ `test_case_id`: テスト ケース ID を表します。

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: オプション パラメーター

+ `output_dir`: 出力作業ディレクトリを表します。 このディレクトリが存在している必要があります。 このパラメーターが指定されていない場合は、設定の作業ディレクトリが使用されます。

##### <a name="generatetestonly-examples"></a>generatetestonly: 例

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

指定したテスト スイートにあるすべてのテスト ケースのテスト自動化ファイルを生成します。 ``listtestsuitenames`` コマンドを使用して、使用可能なすべてのテスト スイートを取得し、任意の値を **test_suite_name** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、生成プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/dllonly`: テスト実行ファイルのみ生成します。 Excel パラメーター ファイルを再生成しないでください。
+ `/keepcustomexcel`: 既存のパラメーター ファイルをアップグレードします。 実行ファイルも再生成します。
+ `/byid`: このスイッチは、目的のテスト スイートが、テスト スイート名ではなく Azure DevOps IDで識別されることを示します。

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: 必須パラメータ

+ `test_suite_name`: テスト スイートの名前を表します。 /byid スイッチが指定されて **いない** 場合、このパラメーターは必須です。 この名前は Azure DevOps テスト スイート名です。
+ `test_suite_id`: テスト スイート ID を表します。 /byid スイッチが指定されて **いる** 場合、このパラメーターは必須です。 この ID はテスト スイート Azure DevOps ID です。

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: オプション パラメーター

+ `output_dir`: 出力作業ディレクトリを表します。 このディレクトリが存在している必要があります。 このパラメーターが指定されていない場合は、設定の作業ディレクトリが使用されます。

##### <a name="generatetestsuite-examples"></a>generatetestsuite: 例

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>ヘルプ

[?](#section) と同一 コマンド。

#### <a name="list"></a>リスト

現在のテスト計画で使用可能なすべてのテスト ケースを一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

使用可能なすべてのテスト計画を一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

指定されたテスト スイートのテスト ケースを一覧表示します。 ``listtestsuitenames`` コマンドを使用して、使用可能なすべてのテスト スイートを取得し、リストの任意の値を **suite_name** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: 必須パラメータ

+ `test_suite_name`: 目的のスイートの名前。

##### <a name="listtestsuite-examples"></a>listtestsuite: 例

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

指定されたテスト スイートのテスト ケースを一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: 必須パラメーター

+ `test_suite_id`: 目的のスイートの ID。

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: 例

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

現在のテスト計画で使用可能なすべてのテスト スイートを一覧表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

指定した Excel パラメーター ファイルに関連付けられたテスト ケースを再生します。 このコマンドは既存のローカル自動化ファイルを使用し、Azure DevOps からファイルをダウンロードしません。 このコマンドは POS コマース テスト ケースではサポートされていません。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、再生プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/comments[="comment"]`: Azure DevOps テスト ケースを実行するための概要ページおよびテスト結果ページの **コメント** フィールドに含めるカスタム情報文字列を指定します。

##### <a name="playback-required-parameters"></a>playback: 必須パラメータ

+ `excel_parameter_file`: Excel パラメーター ファイルの完全なパス。 ファイルが存在する必要があります。

##### <a name="playback-examples"></a>playback: 例

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

同時に複数のテスト ケースを再生します。 テスト ケースは ID で識別されます。 このコマンドは、ファイルを Azure DevOps からダウンロードします。 ``list`` コマンドを使用して、使用可能なすべてのテスト ケースを取得し、最初の列の任意の値を **test_case_id** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、再生プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/comments[="comment"]`: Azure DevOps テスト ケースを実行するための概要ページおよびテスト結果ページの **コメント** フィールドに含めるカスタム情報文字列を指定します。

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: 必須パラメータ

+ `test_case_id1`: 既存のテスト ケースの ID。
+ `test_case_id2`: 既存のテスト ケースの ID。
+ `test_case_idN`: 既存のテスト ケースの ID。

##### <a name="playbackbyid-examples"></a>playbackbyid: 例

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

同時に多数のテスト ケースを再生します。 テスト ケースは Excel パラメーター ファイルで識別されます。 このコマンドは既存のローカル自動化ファイルを使用し、Azure DevOps からファイルをダウンロードしません。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、再生プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/comments[="comment"]`: Azure DevOps テスト ケースを実行するための概要ページおよびテスト結果ページの **コメント** フィールドに含めるカスタム情報文字列を指定します。

##### <a name="playbackmany-required-parameters"></a>playbackmany: 必須パラメータ

+ `excel_parameter_file1`: Excel パラメーター ファイルの完全なパス。 ファイルが存在する必要があります。
+ `excel_parameter_file2`: Excel パラメーター ファイルの完全なパス。 ファイルが存在する必要があります。
+ `excel_parameter_fileN`: Excel パラメーター ファイルの完全なパス。 ファイルが存在する必要があります。

##### <a name="playbackmany-examples"></a>playbackmany: 例

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

1 つ以上の指定したテスト スイートからすべてのテスト ケースを再生します。 /local スイッチが指定されている場合、ローカルの添付ファイルが再生に使用されます。 それ以外の場合、添付ファイルは Azure DevOps からダウンロードされます。 ``listtestsuitenames`` コマンドを使用して、使用可能なすべてのテスト スイートを取得し、最初の列の任意の値を **suite_name** パラメーターとして使用できます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: オプション スイッチ

+ `/updatedriver`: このスイッチが指定されている場合は、再生プロセスが実行される前に、インターネット ブラウザーの webdriver が必要に応じて更新されます。
+ `/local`: このスイッチは、Azure DevOps からファイルをダウンロードする代わりに、ローカル添付ファイルを再生に使用する必要があることを示します。
+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、再生プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/comments[="comment"]`: Azure DevOps テスト ケースを実行するための概要ページおよびテスト結果ページの **コメント** フィールドに含めるカスタム情報文字列を指定します。
+ `/byid`: このスイッチは、目的のテスト スイートが、テスト スイート名ではなく Azure DevOps IDで識別されることを示します。

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: 必須パラメータ

+ `test_suite_name1`: テスト スイートの名前を表します。 /byid スイッチが指定されて **いない** 場合、このパラメーターは必須です。 この名前は Azure DevOps テスト スイート名です。
+ `test_suite_nameN`: テスト スイートの名前を表します。 /byid スイッチが指定されて **いない** 場合、このパラメーターは必須です。 この名前は Azure DevOps テスト スイート名です。
+ `test_suite_id1`: テスト スイート ID を表します。 /byid スイッチが指定されて **いる** 場合、このパラメーターは必須です。 この ID はテスト スイート Azure DevOps ID です。
+ `test_suite_idN`: テスト スイート ID を表します。 /byid スイッチが指定されて **いる** 場合、このパラメーターは必須です。 この ID はテスト スイート Azure DevOps ID です。

##### <a name="playbacksuite-examples"></a>playbacksuite: 例

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

指定した Azure DevOps テスト スイートですべてのテスト ケースを実行します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: オプション スイッチ

+ `/retry[=seconds]`: このスイッチが指定され、ケースのテスト ケースが他の RSAT インスタンスによってブロックされている場合、再生プロセスは指定した秒数待機してから、もう 1 度試行します。 \[seconds\] の既定値は 120 秒です。 このスイッチがないと、テスト ケースがブロックされた場合、プロセスは直ちにキャンセルされます。
+ `/comments[="comment"]`: Azure DevOps テスト ケースを実行するための概要ページおよびテスト結果ページの **コメント** フィールドに含めるカスタム情報文字列を指定します。
+ `/byid`: このスイッチは、目的のテスト スイートが、テスト スイート名ではなく Azure DevOps IDで識別されることを示します。

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: 必須パラメーター

+ `test_suite_id`: Azure DevOps に存在する テスト スイート IDを表します。

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: 例

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

アプリケーションを閉じます。 このコマンドは、アプリケーションが対話モードで実行されている場合にのみ役立ちます。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: 例

`quit`

#### <a name="upload"></a>アップロード

指定したテスト スイートまたはテスト ケースに属する添付ファイル (記録、実行、およびパラメーター ファイル) を Azure DevOps にアップロードします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: 必須パラメータ

+ `test_suite_name`: 指定したテスト スイートに属するすべてのファイルがアップロードされます。
+ `test_case_id1`: アップロードする最初のテスト ケース ID を表します。 このパラメーターは、テスト スイート名が指定されていない場合にのみ使用します。
+ `test_case_idN`: アップロードする最後のテスト ケース ID を表します。 このパラメーターは、テスト スイート名が指定されていない場合にのみ使用します。

##### <a name="upload-examples"></a>upload: 例

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

1 つ以上の指定したテスト ケースに属する記録ファイルのみを Azure DevOps にアップロードします。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: 必須パラメータ

+ `test_case_id1` : Azure DevOps にアップロードする記録の最初のテスト ケース ID を表します。
+ `test_case_idN` : Azure DevOps にアップロードする記録の最後のテスト ケース ID を表します。

##### <a name="uploadrecording-examples"></a>uploadrecording: 例

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>使用

このアプリケーションの 3 つの使用モードを表示します。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

アプリケーションの対話的な実行:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

コマンドを指定してアプリケーションを実行:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

設定ファイルを指定してアプリケーションを実行:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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

```powershell
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
