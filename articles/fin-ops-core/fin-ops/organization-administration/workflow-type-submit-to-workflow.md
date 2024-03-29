---
title: SubmitToWorkflow クラスの作成
description: この記事では、SubmitToWorkflow クラスを作成する方法について説明します。
author: josaw1
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.openlocfilehash: b1ad26d1d8cee37567902ea8e3f60dfc5a620697
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267741"
---
# <a name="create-a-submittoworkflow-class"></a>SubmitToWorkflow クラスの作成 

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

ワークフローは、ユーザーがワークフロー ツールバーの **送信** ボタンを選択したときに開始されます。 **送信** ボタンは、ワークフローを有効にするために作成したクラスの **main** メソッドを呼び出すアクション メニュー項目にバインドされます。 この記事では、**SubmitToWorkflow** クラスを作成する方法、およびワークフロー タイプの名前を使用してワークフローを有効にする方法について説明します。

ワークフロー コンフィギュレーション IDまたはワークフローのシーケンス 番号を使用してワークフローを有効にすることもできます。 基本的な手順は同じです。 詳細については、 [ワークフローの有効化](/dynamicsax-2012/developer/activating-a-workflow) を参照してください。

> [!NOTE]
> **ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ウィザードが、ワークフロー送信マネージャー クラスを既に作成しています。 単にコードを追加するだけです。

## <a name="create-a-submittoworkflow-class"></a>SubmitToWorkflow クラスの作成

1. アプリケーション エクスプローラーで、 **クラス** ノードを展開します。
2. **クラス** ノードを右クリックし、 **新しいクラス** を選択します。 クラス グループは、 **クラス** ノードの下に表示されます。
3. 新しい クラスを右クリックし、 **新しいメソッド** を選択します。 **クラス** ノードの下に新しいメソッド ノードが表示されます。
4. 新しいメソッドを右クリックし、 **編集** を選択します。
5. ワークフローを有効化するためにワークフロー タイプの名前を使用する **main** メソッドに次のコードを入力します。

    > [!NOTE]
    > この例は、ワークフローの送信に適用されます。 エンタープライズ ポータルでも機能する例については、 [ワークフロー送信のためのエンタープライズ ポータル サポートの追加](/dynamicsax-2012/developer/adding-enterprise-portal-support-for-workflow-submission) を参照してください。

    ```X++
    public static void main(Args args)
    {
        // Variable declaration.
        recId _recId = args.record().RecId;
        WorkflowCorrelationId _workflowCorrelationId;
        // Hardcoded workflow type name.
        WorkflowTypeName _workflowTypeName = workflowtypestr("MyWorkflowType");
        // Initial note is the information that users enter when they
        // submit the document for workflow.
        WorkflowComment _initialNote = "";
        WorkflowSubmitDialog workflowSubmitDialog;
        // Opens the submit to workflow dialog box for user comments.
        workflowSubmitDialog = WorkflowSubmitDialog::construct(args.caller().getActiveWorkflowConfiguration());
        workflowSubmitDialog.run();
        if (workflowSubmitDialog.parmIsClosedOK())
        {
            _recId = args.record().RecId;
            // Get user comments from the submit to workflow dialog box.
            _initialNote = workflowSubmitDialog.parmWorkflowComment();
            try
            {
                ttsbegin;
                // Activate the workflow from a template.
                _workflowCorrelationId = Workflow::activateFromWorkflowType(_workflowTypeName, _recId, _initialNote, NoYes::No);
                ttscommit;
                // Updates the workflow button to display Actions instead of Submit.
                args.caller().updateWorkflowControls();
            }
            catch(exception::Error)
            {
                // ToDo Insert your error code here.
            }
        }
    }
    ```

6. **エディター** ウィンドウを閉じ、 **はい** を選択して変更を保存します。

    > [!NOTE]
    > このコードを保存すると、 **catch(exception::Error)** ブロックに有効なコードを追加しない限り、 **コンパイラ出力** ウィンドウに "空の複合文" の警告メッセージが表示されます。

## <a name="see-also"></a>参照

[ワークフローの有効化](/dynamicsax-2012/developer/activating-a-workflow)

[新しいワークフロー タイプの作成](workflow-type-create-new.md)

[ワークフロー::activateFromWorkflowType メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg812416(v=ax.60))

[ワークフロー::activateFromWorkflowSequenceNumber メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg812415(v=ax.60))

[ワークフロー::activateFromWorkflowConfigurationId メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg812414(v=ax.60))


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
