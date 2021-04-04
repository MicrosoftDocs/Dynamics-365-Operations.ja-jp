---
title: ウェーブ中の作業作成のスケジュール
description: このトピックでは、作業作成のスケジュールのウェーブ処理メソッドを設定および使用する方法について説明します。
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501225"
---
# <a name="schedule-work-creation-during-wave"></a>ウェーブ中の作業作成のスケジュール

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

ウェーブ プロセスの一部として *作業作成のスケジュール* 機能を使用すると、並行処理を使用してシステムに作業を作成させることにより、ウェーブ処理のスループットを向上させることができます。

この機能を有効にすると、計画作業が自動的に作成され、最終的にシステムが実際の作業の作成を処理します。 ウェーブ積荷の数が所定のしきい値に達すると、システムは並列の非同期処理を適用することで、より迅速に実際の作業を作成します。

## <a name="enable-the-schedule-work-creation-feature"></a>作業作成のスケジュール機能を有効にする

### <a name="enable-the-feature-in-feature-management"></a>機能管理で機能を有効にする

*作業作成のスケジュール* 機能を使用するには、システム上で有効にする必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。 この機能は、次のようにして表示されます。

- **モジュール:** *倉庫管理*
- **機能名:** *作業作成のスケジュール*

> [!NOTE]
> *組織全体の作業のブロック* 機能は、*作業作成のスケジュール* を有効にする前に、有効にする必要があります。

### <a name="manually-enable-batch-processing-of-waves"></a>ウェーブのバッチ処理を手動で有効にする

並列非同期メソッドを利用して倉庫作業を作成するには、ウェーブ プロセスをバッチで実行する必要があります。 これを設定するには:

1.  **倉庫管理 \> 設定 \> 倉庫管理パラメーター** の順に移動します。

1. **全般** タブで **ウェーブのバッチ処理** を *はい* に設定します。 必要に応じて、専用の **ウェーブを処理するバッチ グループ** を選択して、バッチ キューの処理が他のプロセスと同時に実行されないようにすることもできます。

1. システムが複数のウェーブを同時に処理する場合に適用される、**ロック待機 (ミリ秒) 時間** を設定します。 大規模なウェーブ プロセスの場合は、値を *60000* にすることをお勧めします。

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>既存のウェーブ テンプレートに対して新しいウェーブ ステップ メソッドを手動で有効にする

最初に、新しいウェーブ ステップ メソッドを作成し、並列非同期タスク処理を有効にします。

1.  **倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。

1.  **メソッドの再生成** を選択して、*WHSScheduleWorkCreationWaveStepMethod* が出荷ウェーブ テンプレートで使用できるウェーブ プロセス メソッドの一覧に追加されていることに注意してください。

1. **メソッド名** *WHSScheduleWorkCreationWaveStepMethod* を含むレコードを選択し、**タスク構成** を選択します。

1. グリッドに新しい行を追加するには、アクション ウィンドウで **新規** を選択して、次の設定を使用します:

    - **倉庫** - 作業作成処理をスケジュールするために使用する倉庫を選択します。

    - **バッチ タスクの最大数** - バッチ タスクの最大数を指定します。 ほとんどの場合、この値は 8-16 の範囲にする必要がありますが、シナリオに基づいて最適な設定を試することをお勧めします。

    - **ウェーブを処理するバッチ グループ** - 専用のウェーブを処理するバッチ グループを選択して、バッチ キュー処理を最適化します。

これで、既存のウェーブ テンプレートを更新 (または新しいテンプレートを作成) して、*作業作成のスケジュール* ウェーブ処理メソッドを使用する準備が整いました。

1.  **倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。

1. アクション ペインで **編集** を選択します。

1. リスト ペインで、更新するウェーブ テンプレートを選択します (デモ データを使用してテストを行っている場合は、*24 出荷の既定* を使用できます)。

1. **メソッド** クイック タブを展開し、**残りのメソッド** グリッドで **名前** *作業作成のスケジュール* の行を選択します。

1. **選択されたメソッド** 列を指す矢印を選択して、選択した行をその列に移動します。 (*WHSScheduleWorkCreationWaveStepMethod* または *createWork* を使用するメソッドは、一度に 1 つしか選択できないため、**メソッド名** *createWork* を持つ既存の行は、自動的に **残りのメソッド** グリッドに移動されます。)

## <a name="set-wave-task-processing-threshold-data"></a>ウェーブ タスク処理のしきい値データの設定

システムは、タスク ベースの処理を使用してウェーブ プロセスを初めて実行するときに、既定のウェーブ タスク処理のしきい値データを作成します。 データは、ウェーブ処理を非同期に実行し、タスク ベースにするタイミングを制御するために使用されます。これにより、ウェーブ処理を並行して処理し、作業を作成できます。

既定のデータでは、最初に、最小積荷明細行数 (MINIMUMWAVELOADLINES) に対してしきい値 15 が使用されます。 つまり、システムが、15 より多い積荷明細行を含むウェーブを処理すると、非同期タスク処理を使用します。 このデータは、テスト環境の **WHSWaveTaskProcessingThresholdParameters** テーブルに手動で挿入または更新できますが、運用環境でこの設定を変更する必要がある場合は、Microsoft サポートに連絡して、更新を依頼する必要があります。

## <a name="work-with-the-feature"></a>機能の使用

*作業作成のスケジュール* 機能を有効にすると、ウェーブ処理は計画作業を作成し、最終的には新しい作業作成プロセスで使用されます。 作業の作成中は、*組織全体の作業のブロック* 機能を使用して作業がブロックされます。

次のフローチャートは、ウェーブ処理中に計画作業がどのように作成されるかを示しています。

![作業作成のスケジュール](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>計画作業

**計画作業の詳細** ページ (**倉庫管理 \> 作業 \> 計画作業の詳細**) には、ウェーブ処理中に最初に作成された計画作業に関する情報が表示されます。 以下の **プロセス状態** 値を使用できます:

- **キューに設定** - 計画作業は、作業の作成に使用されるまで待機しています。
- **完了** - 計画作業が作業の作成に使用されました。
- **失敗** – ウェーブ処理が失敗しました。 計画作業は、関連する実際の作業の有無にかかわらず、**失敗** した状態になることがあります。 実際の作業作成プロセスが失敗すると、実際の作業は *キャンセル済* 状態のままになります。

### <a name="batch-job-for-the-work-creation-process"></a>作業作成プロセスのバッチ ジョブ

ウェーブを処理するバッチ ジョブを表示するには、**すべてのウェーブ** ページのアクション ペインで **バッチ ジョブ** を選択 します。

ここから、各バッチ ジョブ ID のすべてのバッチ タスクの詳細を表示できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]