---
title: ワークフロー ビジネス イベント
description: ワークフロー ビジネス イベントは、ワークフローの処理のさまざまなポイントで生成されます。
author: ChrisGarty
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d85d16297cc3c0706e5bea26ea68cd79ba169787
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068301"
---
# <a name="workflow-business-events"></a>ワークフロー ビジネス イベント
[!include[banner](../includes/banner.md)]

ワークフロー ビジネス イベントは、ワークフローの処理のさまざまなポイントで生成されます。   

## <a name="workflow-construction"></a>ワークフローの構築

ワークフローを構築するため、開発者は Visual Studio ツール内のメタデータ及びコードでワークフロー コンポーネントを定義することができます。

管理者は Web クライアントでワークフローを作成してから、ワークフロー デザイナーでそれらをデザインすることができます。 詳細については、[ワークフローの作成](../../fin-ops/organization-administration/create-workflow.md)を参照してください。

### <a name="workflow-components"></a>ワークフローのコンポーネント
ワークフロー コンポーネントはメタデータで以下のように定義されます。
- **ワークフロー タイプ** - テンプレートとしても知られるワークフロー タイプは、ワークフローで許容される要素を定義します。 管理者はワークフローのデザインを作成するときに実際に使用される要素を決定します。 
     - アプリケーション エクスプローラーで、**AOT > ビジネス プロセスおよびワークフロー > ワークフロー タイプ** の順に移動します。
- **ワークフロー要素** - ワークフロー要素はワークフローを構成する実行可能要素です。 詳細については、[ワークフロー要素](../../fin-ops/organization-administration/workflow-elements.md)を参照してください。
     - タスク (または手動タスク) - **AOT > ビジネス プロセスおよびワークフロー > ワークフロー タスク** の順に移動します。
     - 承認 - **AOT > ビジネス プロセスおよびワークフロー > ワークフローの承認** の順に移動します。
     - 自動化タスク - **AOT > ビジネス プロセスおよびワークフロー > ワークフロー自動化タスク** の順に移動します。

## <a name="workflow-runtime"></a>ワークフロー ランタイム
ユーザーがワークフローを送信すると、ワークフローはキューに追加され、**ワークフロー メッセージ処理** バッチ ジョブを使用して実行されます。 ワークフローの実行時、終了に達するまですべての [接続されたワークフロー要素](../../fin-ops/organization-administration/create-workflow.md#connect-the-elements)を経て進行します。 ワークフロー ランタイムが[手動タスク要素](../../fin-ops/organization-administration/workflow-elements.md#manual-task)に遭遇すると、[タスクに割り当てわれたユーザー](../../fin-ops/organization-administration/configure-manual-task-workflow.md#assign-the-task)に対して作業項目が作成されます。 ワークフロー ランタイムが[承認要素](../../fin-ops/organization-administration/workflow-elements.md#approval-processes)に遭遇すると、[各承認ステップに割り当てわれたユーザー](../../fin-ops/organization-administration/configure-approval-step-workflow.md#assign-the-approval-step)ごとに作業項目が作成されます。

## <a name="workflow-business-event-categories"></a>ワークフロー ビジネス イベントのカテゴリ

ワークフロー ビジネス イベントには 5 つの異なるカテゴリがあります。 カテゴリが Microsoft Power Automate に表示され、イベントを選択できます。

![Microsoft Power Automate でのビジネス イベント カテゴリ。](media/Business-event-category.png  "Microsoft Power Automate でのビジネス イベント カテゴリ")
- **カテゴリ: ワークフロー タイプ** 
     - これらのイベントは、開始および完了などのワークフロー イベントで発生します。 すべてのワークフロー インスタンスはこのカテゴリに相当します。
     - 例: 購買要求承認ワークフローの開始
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID、たとえば、"Workflow_BudgetPlanReview_000002"
- **カテゴリ: 開始されたワークフロー要素**
     - これらのイベントはワークフロー要素が開始されたときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロー要素はこのカテゴリに相当します。 
     - 例: 購買要求の自動承認の開始
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_Started"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_Started"
- **カテゴリ: ワークフロー要素**
     - これらのイベントは、完了などの、開始以外のワークフロー要素イベントで発生します。 ワークフロー インスタンス内のすべての有効なワークフロー要素はこのカテゴリに相当します。 
     - 例: 購買要求の自動承認の完了
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild"
- **カテゴリ: ワークフローの外部タスク** 
     - これらのイベントはワークフロー自動化タスク要素が開始されたときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロー自動化タスク要素はこのカテゴリに相当します。 
     - 例: 購買要求の自動承認の開始
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_ExternalTask"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_ExternalTask"
- **カテゴリ: ワークフロー作業項目**
     - これらのイベントはユーザーに対してワークフロー作業項目が作成されるときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロータスクおよびワークフロー承認はこのカテゴリに相当します。 
     - 例: Bob に対して作成された購買要求の手動承認作業項目
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_WorkItem"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_WorkItem"

## <a name="completion-of-a-work-item-in-power-automate"></a>Power Automate で作業項目を完了する
ワークフロー ビジネス イベント は承認フローのトリガーに優れたターゲットです。 **ワークフロー作業項目** イベントは、OData アクションの検証と完了と組み合わせて使用することで、Power Automate の作業項目完了を容易にすることができます。

承認やタスク作業項目は、次の手順を使用して Power Automate で完了することができます:
- 適切な **ワークフロー作業項目** イベントを対象にした **ビジネス イベントが発生した場合** のトリガーを使用して、Power Automate をトリガーします。
- **ワークフロー作業項目** に有効な一連の情報が含まれていることを検証し、**WorkflowWorkItems** エンティティで **検証** メソッドを呼び出して完了できるようにします。 
- 作業項目に完了する準備ができていない場合は、割り当てられたユーザーに通知を送信して、注意が必要な作業項目があることを知らせます。
- 作業項目を完了する準備ができたら、使用可能な回答オプションをユーザーに送信して、割り当てられたユーザーに回答を要求します。
- 回答が提供されたら、**WorkflowWorkItems** エンティティの **完了** メソッドを呼び出して、その回答で作業項目を完了します。 

作業項目の外部完了を可能にするには、作業項目のアクション マネージャー クラスは、IValidateWorkflowWorkItemAction インターフェイスを実装する必要があります。 標準の WorkflowWorkItemActionManager クラスはこのインターフェイスを実装しています。 プラットフォーム更新 32 では、IValidateWorkflowWorkItemAction インターフェイスの実装をおこなうために TrvWorkflowWorkItemActionManager クラスが更新されます。 例として、既存の IValidateWorkflowWorkItemAction 実装を使用して、その他の WorkflowWorkItemActionManager クラスについての更新を通知します。

Microsoft Power Automate で作業項目完了を設定する詳細なガイドは [ワークフロー承認ビジネス イベントを消費する](how-to/how-to-flow.md) を参照してください。

## <a name="templates-for-work-item-completion-in-power-automate"></a>Power Automate での作業項目完了のテンプレート

Power Automate での作業項目完了に関する次のテンプレートが使用できます。
- [財務と運用のワークフローの作業項目を完了する (PU26)](https://flow.microsoft.com/galleries/public/templates/efb564143834442283c41e19cdc2a6bb/complete-dynamics-365-for-finance-and-operations-workflow-work-items-pu26/)
- [財務と運用のワークフローの作業項目を完了する (PU29)](https://flow.microsoft.com/galleries/public/templates/ebeccaa6f7aa40899828d8d01151d268/complete-dynamics-365-for-finance-and-operations-workflow-work-items-pu29/)

プラットフォーム更新プログラム 29 バージョンは、ビジネス イベント ペイロードから完了オプションを取得します。 これらのオプションはプラットフォーム更新プログラム 29 で追加され、承認アクションによりユーザーに表示されます。 

## <a name="troubleshooting-workflow-business-events"></a>ワークフロー ビジネスイベントのトラブルシューティング

### <a name="troubleshooting-workflow-issues"></a>ワークフローの問題に関するトラブルシューティング ###
ワークフローが正常に稼働し、期待通りに作業項目を作成できることを確認します。 ワークフローがアプリケーション内で動作せず、状態の変化が発生した場合、イベントは発生しません。 必要に応じてワークフローの設定を調整します。 この調整を行うには、 **ワークフローの履歴** フォームの詳細を確認してください。

### <a name="troubleshooting-power-automate-issues"></a>Power Automate の問題に関するトラブルシューティング ###
Power Automate サブスクリプションが、**アクティブ イベント** タブの **システム管理 > 設定 > ビジネス イベント > ビジネス イベント カタログ** で利用可能なことを確認します。Power Automateサブスクリプションがそこにない場合は、Power Automate をチェックして、必要に応じて再作成します。

### <a name="troubleshooting-business-events-issues"></a>ビジネス イベントの問題に関するトラブルシューティング ###
Power Automate を作成することでその他のビジネス イベントが正常に発生し、他のビジネスイベントがトリガーから外されることを確認します。 たとえば、フリー テキストのインボイス転記済イベントは、単一行のフリー テキスト インボイスを作成して転記することでトリガーできます。 詳細については [ビジネス イベントのトラブルシューティング](troubleshooting.md) を参照してください。

### <a name="troubleshooting-work-item-approval-via-power-automate"></a>Power Automate を介して作業項目承認のトラブルシューティング ### 
フローが作業項目の承認を対処しようとしているが、起動しない場合は、次のステップを検証します。
- 作業項目が作成され、それにより適用されるユーザーは Web クライアントで承認を待機していることを見ることができますか？
 - フローからのイベント サブスクリプションは、ビジネス イベント フォームで見ることができますか？
- ワークフロー構成とフローからのイベント サブスクリプションは、正しい法的エンティティ (企業) 向けになっていますか？



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

