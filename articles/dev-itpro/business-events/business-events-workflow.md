---
title: ワークフロー ビジネス イベント
description: ワークフロー ビジネス イベントは、ワークフローの処理のさまざまなポイントで生成されます。
author: ChrisGarty
manager: AnnBe
ms.date: 02/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 190bcf9aca5ad140a0df9ecbb640139cb2481a47
ms.sourcegitcommit: ea17d2e35c24a141c20ab429897eebf9fa186f61
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "768846"
---
# <a name="workflow-business-events"></a>ワークフロー ビジネス イベント
[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

ワークフロー ビジネス イベントは、ワークフローの処理のさまざまなポイントで生成されます。   

## <a name="workflow-construction"></a>ワークフローの構築

ワークフローを構築するため、開発者は Visual Studio ツール内のメタデータ及びコードでワークフロー コンポーネントを定義することができます。

管理者は Web クライアントでワークフローを作成してから、ワークフロー デザイナーでそれらをデザインすることができます。 詳細については、[ワークフローの作成](../../fin-and-ops/organization-administration/create-workflow.md)を参照してください。

### <a name="workflow-components"></a>ワークフローのコンポーネント
ワークフロー コンポーネントはメタデータで以下のように定義されます。
- **ワークフロー タイプ** - テンプレートとしても知られるワークフロー タイプは、ワークフローで許容される要素を定義します。 管理者はワークフローのデザインを作成するときに実際に使用される要素を決定します。 
     - アプリケーション エクスプローラーで、**AOT > ビジネス プロセスおよびワークフロー > ワークフロー タイプ** の順に移動します。
- **ワークフロー要素** - ワークフロー要素はワークフローを構成する実行可能要素です。 詳細については、[ワークフロー要素](../../fin-and-ops/organization-administration/workflow-elements.md)を参照してください。
     - タスク (または手動タスク) - **AOT > ビジネス プロセスおよびワークフロー > ワークフロー タスク** の順に移動します。
     - 承認 - **AOT > ビジネス プロセスおよびワークフロー > ワークフローの承認** の順に移動します。
     - 自動化タスク - **AOT > ビジネス プロセスおよびワークフロー > ワークフロー自動化タスク** の順に移動します。

## <a name="workflow-runtime"></a>ワークフロー ランタイム
ユーザーがワークフローを送信すると、ワークフローはキューに追加され、**ワークフロー メッセージ処理** バッチ ジョブを使用して実行されます。 ワークフローの実行時、終了に達するまですべての [接続されたワークフロー要素](../../fin-and-ops/organization-administration/create-workflow.md#connect-the-elements)を経て進行します。 ワークフロー ランタイムが[手動タスク要素](../../fin-and-ops/organization-administration/workflow-elements.md#manual-task)に遭遇すると、[タスクに割り当てわれたユーザー](../../fin-and-ops/organization-administration/configure-manual-task-workflow.md#assign-the-task)に対して作業項目が作成されます。 ワークフロー ランタイムが[承認要素](../../fin-and-ops/organization-administration/workflow-elements.md#approval-processes)に遭遇すると、[各承認ステップに割り当てわれたユーザー](../../fin-and-ops/organization-administration/configure-approval-step-workflow.md#assign-the-approval-step)ごとに作業項目が作成されます。

## <a name="workflow-business-event-categories"></a>ワークフロー ビジネス イベントのカテゴリ

ワークフロー ビジネス イベントには 5 つの異なるカテゴリがあります。 カテゴリが Microsoft Flow に表示され、イベントを選択できます。

![Microsoft Flow のビジネス イベント カテゴリ](media/Business-event-category.png  "Microsoft Flow のビジネス イベント カテゴリ")
- **カテゴリ: ワークフロー タイプ** 
     - これらのイベントは、開始および完了などのワークフロー イベントで発生します。 すべてのワークフロー インスタンスはこのカテゴリに相当します。
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID、たとえば、"Workflow_BudgetPlanReview_000002"
     - **名前の形式** - ワークフロー ラベル + " (" + ワークフロー インスタンス ID ")"、たとえば、"Prepare department budget (000002)"
- **カテゴリ: 開始されたワークフロー要素**
     - これらのイベントはワークフロー要素が開始されたときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロー要素はこのカテゴリに相当します。 
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_Started"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_Started"
     - **名前の形式** - ワークフロー ラベル + " (" + ワークフロー インスタンス ID ") - " + ワークフロー要素ラベル、たとえば、"Prepare department budget (000002) - Activate associated budget plan"
- **カテゴリ: ワークフロー要素**
     - これらのイベントは、完了などの、開始以外のワークフロー要素イベントで発生します。 ワークフロー インスタンス内のすべての有効なワークフロー要素はこのカテゴリに相当します。 
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild"
     - **名前の形式** - ワークフロー ラベル + " (" + ワークフロー インスタンス ID ") - " + ワークフロー要素ラベル、たとえば、"Prepare department budget (000002) - Activate associated budget plan"
- **カテゴリ: ワークフローの外部タスク** 
     - これらのイベントはワークフロー自動化タスク要素が開始されたときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロー自動化タスク要素はこのカテゴリに相当します。 
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_ExternalTask"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_ExternalTask"
     - **名前の形式** - ワークフロー ラベル + " (" + ワークフロー インスタンス ID ") - " + ワークフロー要素ラベル、たとえば、"Prepare department budget (000002) - Activate associated budget plan"
- **カテゴリ: ワークフロー作業項目**
     - これらのイベントはユーザーに対してワークフロー作業項目が作成されるときに発生します。 ワークフロー インスタンス内のすべての有効なワークフロータスクおよびワークフロー承認はこのカテゴリに相当します。 
     - **ID の形式** - "Workflow_" + ワークフロー名 + ワークフロー インスタンス ID + "_" + ワークフロー要素名 + "_WorkItem"、たとえば、"Workflow_BudgetPlanReview_000002_BudgetActivateBudgetPlanChild_WorkItem"
     - **名前の形式** - ワークフロー ラベル + " (" + ワークフロー インスタンス ID ") - " + ワークフロー要素ラベル、たとえば、"Prepare department budget (000002) - Activate associated budget plan"
