---
title: ユーザー受け入れテストの作成と自動化
description: このトピックでは、タスク ガイドと BPM を 使用して承認テスト スイートを作成および実行することに関する情報を提供します。
author: kfend
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 4df1fd3f83c141b277156cd4334dee55d3d8bb2d
ms.sourcegitcommit: f79f2249d7557e578d7d3c4d6ea83682df7362d5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/14/2019
ms.locfileid: "1874821"
---
# <a name="create-and-automate-user-acceptance-tests"></a>ユーザー受け入れテストの作成と自動化

[!include [banner](../includes/banner.md)]

タスク レコーダーおよびビジネス プロセス モデラー (BPM) を使用して、ユーザー承認テスト ライブラリを作成することができます。 タスク レコーダーは、テスト ケースを記録し、BPM を使用して業務プロセス別に整理する強力なツールです。 Microsoft パートナーは、BPM を使用して LCS および LCS ソリューション経由で顧客にテスト ライブラリを配布することができます。 顧客の場合、BPM を使用し、さまざまなプロジェクトおよびチーム間でテスト ライブラリを作成して配布します。
BPM は Azure DevOps (旧 Visual Studio Team Services) と同期することができるので、Azure DevOps プロジェクトでテスト ケース (テスト ステップを含む) を自動的に作成できます。 その後、Azure DevOps は、対象となるテスト計画およびテスト スイートを作成して、テストの実行を管理し、結果を調査できるテスト構成およびテスト管理ツールとして動作できます。  

このトピックでは、手動テストまたは自動テストに使用する承認テスト スイートを作成および実行するプロセスについて説明します。







## <a name="create-a-scenario-acceptance-testing-bpm-library"></a>シナリオ承認テスト BPM ライブラリの作成
BPM は、業務プロセスおよびユーザー タスクの階層を記述する優れた LCS ツールです。 LCS では Microsoft パートナーおよび顧客がアセット ライブラリ経由で LCS プロジェクト間の BPM ライブラリを作成し配布することもできます。 このセクションでは、承認テスト ライブラリを定義する BPM を活用する方法を説明します。

### <a name="create-a-bpm-library"></a>BPM ライブラリの作成
ビジネス プロセス モデラー (BPM) ライブラリを作成するにはいくつかの方法があります。 BPM でライブラリを作成する方法の詳細については、[BPM ライブラリの作成、編集、および参照](creating-editing-browsing.md) を参照してください。

説明目的で、このトピックでは、経費精算書の作成および注文要求の承認などの一般的な業務プロセスを含むライブラリを使用します。 Excel インポート機能を使用してライブラリを作成しました。  

![Excel からインポート](./media/import-from-excel.PNG "Excel からインポート")

### <a name="record-test-cases-and-save-to-bpm"></a>テスト ケースを記録して BPM に保存 

BPMライブラリを作成した後は、タスク レコーダーを使用してテスト ケースを作成し、それから BPM にそのケースをアップロードする必要があります。 これを行うにはいくつかの方法があります。 

既に必要なタスク記録 (テスト ケース) が付属されている BPM ライブラリを使用している場合、この手順を省略できます。 それ以外の場合、新しいタスク記録を作成するには、次の手順に従います。

#### <a name="create-and-save-a-new-task-recording"></a>新しいタスク記録を作成して保存する
1. クライアントを開いて、サインインします。 
2. 記録中に使用する会社を選択します。
3. **設定** > **タスク レコーダー**に移動します。

![タスク レコーダーの選択](./media/select_task_recorder.PNG "タスク レコーダーの選択")

4. **新しい記録の作成**をクリックします。
5. コンフィギュレーション名を入力し、**開始**をクリックします。 記録は、**開始** をクリックすると開始されます。
6. 記録が完了したら、タスク レコーダー ウィンドウで、**停止** をクリックします。
7. 添付された BPM にタスク記録を保存するには、**Lifecycle Services に保存** をクリックします。

![タスク レコーダー オプション](./media/task_recorder_options.PNG "タスク レコーダー オプション")

8. 記録を保存するライブラリを選択し、**保存** をクリックします。 それ以外の場合、**ディスクに保存** を選択し、次のセクション「BPM に AXTR ファイルをアップロードする」の手順に従います。

 >[!NOTE]
 > 自動化ツールを使用して、テストの有効な実行を有効にするには、タスク記録がすべて Dynamics 365 for Finance and Operations の主要なダッシュボードで開始することを確認します。
 > 複数のユーザーによって実行されるエンド ツー エンド プロセスの場合、ユーザー固有のタスクにタスク記録を分割することをお勧めします。 これにより、テスト ケースの保守作業を簡素化され、セキュリティ ロールのコンテキストでテスト ケースを実行することができます。これはベスト プラクティスです。 

#### <a name="upload-an-axtr-file-to-bpm"></a>BPM に AXTR ファイルをアップロード
ディスクに記録 (AXTR ファイル) を保存した場合、以下の手順に従って BPM にアップロードします。

1. Lifecycle Services (LCS) で、プロジェクトの**業務プロセス ライブラリ** ページで、タスク記録をアップロードするライブラリを選択します。
2. **作成と編集**をクリックして、明細行内で、タスク記録をアップロードするプロセスを特定し選択します。
3. 右ウィンドウで**アップロード**をクリックします。 

![AXTR 1 のアップロード](./media/upload_axtr_1.PNG "AXTR 1 のアップロード")

4. **参照**をクリックして、アップロードするファイルを検索して選択し、次に**アップロード**をクリックします。

![AXTR 2 のアップロード](./media/upload_axtr_2.PNG "AXTR 2 のアップロード")

#### <a name="save-an-existing-task-recording-to-bpm"></a>既存のタスク記録を BPM を保存
1. 既存のタスクの記録を添付するには、クライアントにサインインします。
2. **設定** > **タスク レコーダー**に移動します。
3. **タスクの記録を編集** を選択し、LCS に直接を保存するか、AXTR にダウンロードしてから BPM にアップグレードすることによって、そのファイルを添付します。

### <a name="guidelines-for-recording-test-cases"></a>テスト ケースを記録するためのガイドライン

テスト ケースを作成して記録するとき、特にテストの実行を自動化する予定がある場合は、次のガイドラインに従います。
ここで説明されているプロセスおよびツールは、業務プロセスの受け入れテストに適用されます。 通常の開発者によって所有されているコンポーネントおよび単体テストを交換するためではありません。

- 組み合わせるとエンド ツー エンド プロセス全体をカバーする限られた数のテスト ケースを作成します。
- カスタマイズされている業務プロセスに焦点を当てててください。
- 個々のテスト ケース (記録) は、通常は 1 人のユーザーによって実行される、1 つか 2 つの業務のみを対象としてください。 これにより、タスク記録メンテナンスが簡略化されます。 1 つの大きなタスクの記録に「調達から支払」や「注文から現金」などの包括的なエンド ツー エンド ビジネス プロセスを組み合わせることはしないでください。 たとえば、RFQ > 発注書 > 製品受領書 > 仕入先請求書 > 仕入先支払を 1 つのテスト ケースとするのではなく、3 つか 4 つのテスト ケースにプロセスを分割します。 これらのテストを後で順序指定テスト スイートに組み合わせることができます。
- テスト ケースでは、少なくとも 1 つの検証が必要です。 その他のフィールドの影響をカバーする重要なフィールドを検証するには、このようにしてください。 例: 売上または発注書の合計が単位価格/数量/割引/税金をカバーするかの検証など。
- テスト ケースのレポートを印刷しないようにします。 テスト ケースでレポートを印刷する必要がある場合は、画面で選択してください。
- テスト ケースの 80% 以上は、トランザクションや元伝票にしてください。 マスタ データは、テスト ケースの最大 20% に限定する必要があります。

## <a name="synchronize-and-configure-your-test-plan-in-azure-devops"></a>Azure DevOps でテスト計画の同期およびコンフィギュレーション

引受テスト ライブラリは、開始点です。 通常、業務プロセス別に分類されている特定のアプリケーションのすべてのテスト ケース (タスク記録) が含まれています。 特定のテスト パスの間、通常はすべてのテスト ケースを実行する必要があるわけではありません。 選択したテスト ケースが実装のフェーズまたは更新の性質に依存している場合、実稼働環境に適用するよう計画します。 Azure DevOps を使用すると、テスト計画およびテスト スイートでテスト ケースを整理できます。 テスト計画には、1 つまたは複数のテストスイート (テスト ライブラリのサブセット) が含まれています。テスト ケースは、1 つ以上のテスト スイートに属することができます。

承認テスト BPM ライブラリを一度選択すると、Azure DevOps と同期してテスト計画およびテスト スイートを作成します。

### <a name="sync-with-azure-devops"></a>Azure DevOps との同期
Azure DevOps プロジェクトと BPM ライブラリを同期します。 詳細については、「[LCS プロジェクトのコンフィギュレーションおよび LCS に接続](synchronize-bpm-vsts.md#configure-your-lcs-project-to-connect-to-azure-devops)」を参照してください。 

コンフィギュレーションが完了した後、Azure DevOps プロジェクトと BPM ライブラリを同期します。
1. **業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**Azure DevOps 同期**を選択します。

![VSTS Sync1](./media/vsts_sync_1.png "VSTS Sync1")

また、BPM ライブラリ内のツールバーから Azure DevOps 同期を開始することができます。 省略記号ボタン (...) を選択し、**Azure DevOps の同期** を選択します。

![VSTS Sync2](./media/vsts_sync_2.png "VSTS Sync2")

2. Azure DevOps の同期が完了した後、省略記号ボタン (…) を選択し、**テスト ケースの同期**を選択します。

![テスト ケースの同期](./media/sync_test_case.PNG "テスト ケースの同期")

3. このステップが完了したら、タスク記録は Azure DevOps のテスト ケースになり、**要件** タブの下にリンクが表示されます。 

![テスト ケースの表示](./media/view_test_case.PNG "テスト ケースの表示")


テスト ステップに加えて、タスクを記録する XML ファイルが Azure DevOps テスト ケースに付属します。 テストの実行を自動化する場合、このファイルを必要とします。 

### <a name="create-a-test-suite-in-azure-devops"></a>Azure DevOps でテスト スイートを作成する
次に、Azure DevOps でテスト計画とスイートを作成する必要があります。 これにより、テスト ケースの順序指定テストを実行できるので、結果の管理、調査、追跡が容易になります。 

1. Azure DevOps にログインし、テストするプロジェクトとテスト計画を選択します。 
2. ツール バーで、**テスト** > **テスト計画** を選択します。
3. 左ウィンドウで、**+** を選択してから、**静的スイート**を選択します。 
4. スイート名を入力します。
5. **既存の追加**をクリックし、**LCS:Test Cases** タグを照会します。
6. **実行** > **テスト ケースの追加**の順にクリックします。

![テスト ケースの追加](./media/add_test_cases.PNG "テスト ケースの追加")
 
7. 詳細と関連付けられている XML ファイルを表示するには、テスト ケースを選択します。   

![テスト ケースの詳細](./media/test_case_details.PNG "テスト ケースの詳細")

 >[!NOTE]
 > この例は、すべてのテスト ケースが追加された 1 つの包括的受入れテスト スイートを作成する方法を示しています。 代わりに、同じテスト計画下にさまざまなテスト スイートを作成し、カスタム クエリを使用してテスト スイートに特定のテスト ケースを追加する必要があります。 テスト ケースは、1 つ以上のテスト スイートに属することができます。

## <a name="execute-your-tests"></a>テストを実行します。

### <a name="run-manual-test-cases"></a>手動テスト ケースを実行
テスト スイートがある場合、サンドボックスおよびテスト環境で Dynamics 365 for Finance and Operations アプリケーションが更新された後、回帰テストを使用する準備ができるようになります。 テスト スイートで手動でテスト ケースを実行、またはテスト スイートの一部であるタスク記録を再生し、Azure DevOps を使用してテスト ケースを成功または失敗としてマークすることができます。

![マーク済み VSTS テスト](./media/vsts_test_marked.png "マーク済み VSTS テスト")

Azure DevOps は、**テスト ランナー** というツールを提供して、手動テスト ケースの実行も管理します。 テスト ランナーの使用の詳細については、[手動テストの実行](https://docs.microsoft.com/vsts/manual-test/getting-started/run-manual-tests) を参照してください。

Azure DevOps はテストだけでなく、結果の管理と軽減策のための豊富な管理機能セットを提供するので、VSTS の活用をお勧めします。

### <a name="run-automated-test-cases"></a>自動テスト ケースを実行

Dynamics 365 Unified Operations プラットフォームは、タスク記録に基づいてテスト ケースを作成し、Azure DevOps を使用してそれらのテスト ケースの自動実行を管理するためのツールを開発者を提供します。 

開発者は、**ビルドおよびテスト**環境のビルドおよびテスト自動化機能を使用できます。 詳細については、[継続的な配信ホーム ページ](../dev-tools/continuous-delivery-home-page.md) を参照してください。

機能パワー ユーザーは、**Regression Suite Automation Tool** を使ってテスト ケースの実行を自動化できます。 詳細については、[ツールをダウンロードする](https://www.microsoft.com/download/details.aspx?id=57357) および [Regression Suite Automation Tool](../perf-test/rsat/rsat-overview.md) を参照してください。

Regression Suite Automation Toolの詳細については、次の情報を参照してください。

- [- 第 1 部: Regression Suite Automation Tool -- 背景と設定](https://infopedia.eventbuilder.com/event?eventid=j5m3w4&source=Dynamics_365_for_Operations_-_FastTrack_Tech_Talks)
- [- 第 2 部: Regression Suite Automation Tool -- ライフサイクル デモのテスト](https://infopedia.eventbuilder.com/event?eventid=r5j6c1&source=Dynamics_365_for_Operations_-_FastTrack_Tech_Talks)
-  [Regression Suite Automation Tool ドキュメント](../perf-test/rsat/rsat-overview.md)
 
実習で使用する手順については、次のトピックを参照してください。

- [Regression Suite Automation Toolの設定およびインストール](../../fin-and-ops/get-started/hol-set-up-regression-suite-automation-tool.md)
- [Regression Suite Automation Toolの使用](../../fin-and-ops/get-started/hol-use-regression-suite-automation-tool.md)

#### <a name="investigate-test-runs"></a>テストの実行を調査します
自動実行が完了したら、Azure DevOps ツール バーで**テスト > 実行** (または **テスト計画 > 実行**) を選択し、テストの実行を調査すします。 テスト ケース失敗およびエラーを調査するために必要なテスト実行を選択します。 Azure DevOps のテスト スイートにアクセスして、テスト ケースに関連する最新の結果を確認することもできます。
Azure DevOps のテストおよびテスト管理の詳細については、[Azure DevOps ドキュメント](https://docs.microsoft.com/azure/devops)を参照してください。

