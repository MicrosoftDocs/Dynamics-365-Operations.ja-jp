---
title: ワークフロー タイプ チェックリスト
description: このトピックでは、新しいワークフロー タイプを作成するために必要な手順について説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 389f80e432605db3a67977bb5f3e11ccf01998ce
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065565"
---
# <a name="workflow-type-checklist"></a>ワークフロー タイプ チェックリスト

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

このトピックでは、新しいワークフロー タイプを作成するために必要な手順について説明します。 ワークフロー タイプは、 ワークフローの構成を作成するために使用されます。

## <a name="workflow-type-checklist"></a>ワークフロー タイプのチェックリスト

1. 既存のカテゴリが適切ではない場合は、ワークフロー タイプに使用する新しいワークフロー カテゴリを作成します。 詳細については、 [新しいワークフロー カテゴリの作成](workflow-type-category.md) を参照してください。
2. 新しいワークフロー タイプが作成されるドキュメントにアクセスするクエリを作成します。 詳細については、 [ワークフロー タイプのクエリの作成](workflow-type-query.md) を参照してください。
3. アプリケーション エクスプローラーでワークフロー タイプを作成します。 通常、 **ワークフロー** ウィザードを使用してこの手順を完了します。 詳細については、 [新しいワークフロー タイプの作成](workflow-type-create-new.md) を参照してください。

ワークフロー タイプを作成するために、 **ワークフロー** ウィザードを使用することをお勧めします。 ウィザードでは次のタスクを実行します。 場合によっては、ワークフロー タイプに対してさらにコードを追加する必要があります。 ウィザードによって実行されるアクションの詳細、およびワークフロー タイプを完了するために実行する必要がある追加手順を確認できるように、リンクが提供されています。

1. ワークフロー ドキュメント クラスを作成し、ワークフローに使用するクエリをクラスにバインドします。 詳細については、 [新しいワークフロー ドキュメント クラスの作成](workflow-type-document-create.md) を参照してください。
2. ワークフロー ドキュメント クラスをワークフロー タイプにバインドします。 詳細については、 [ワークフロー ドキュメント クラスとワークフロー タイプの関連付け](workflow-type-associate-document.md) を参照してください。
3. 開始、完了、コンフィギュレーションの変更、およびキャンセルされたイベントのワークフロー イベント ハンドラーを作成し、イベント ハンドラーをワークフロー タイプにバインドします。 詳細については、 [新しいワークフロー イベント ハンドラーの作成](/dynamicsax-2012/developer/how-to-create-a-workflow-event-handler) を参照してください。
4. **SubmitToWorkflowMenuItem** のクラスを作成します。 必要に応じて、 **CancelMenuItem** のクラスを作成します。 次のステップで作成するアクション メニュー項目にクラスをバインドします。 詳細については、[クラスおよびメソッド](../../dev-itpro/dev-ref/xpp-classes-methods.md) を参照してください。
5. **SubmitToWorkflowMenuItem** ワークフロー プロパティのアクション メニュー項目を作成します。 必要に応じて、 **CancelMenuItem** プロパティのアクション メニュー項目を作成します。 アクションをワークフロー タイプにバインドします。 詳細については、 [新しいワークフロー タイプの作成](workflow-type-create-new.md) を参照してください。

## <a name="next-steps"></a>次のステップ

ワークフロー タイプを作成した後、タスク、自動化されたタスク、および承認を追加できます。

## <a name="see-also"></a>参照

[ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md)

[ワークフローでの手動タスクのコンフィギュレーション](configure-manual-task-workflow.md)

[ワークフローでの自動化タスクのコンフィギュレーション](configure-automated-task-workflow.md)

[ワークフローでの承認プロセスのコンフィギュレーション](configure-approval-process-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]