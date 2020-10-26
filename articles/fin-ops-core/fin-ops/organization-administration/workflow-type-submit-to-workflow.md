---
title: SubmitToWorkflow クラスの作成
description: このトピックでは、SubmitToWorkflow クラスを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 8a8b75e409392bb7f24a10dbd60f927e53275788
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975354"
---
# <a name="create-a-submittoworkflow-class"></a><span data-ttu-id="c91e1-103">SubmitToWorkflow クラスの作成</span><span class="sxs-lookup"><span data-stu-id="c91e1-103">Create a SubmitToWorkflow class</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c91e1-104">ワークフローは、ユーザーがワークフロー ツールバーの**送信**ボタンを選択したときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-104">A workflow is started when the user selects the **Submit** button on the workflow toolbar.</span></span> <span data-ttu-id="c91e1-105">**送信** ボタンは、ワークフローを有効にするために作成したクラスの **main** メソッドを呼び出すアクション メニュー項目にバインドされます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-105">The **Submit** button is bound to an action menu item that calls the **main** method of a class that you create to activate a workflow.</span></span> <span data-ttu-id="c91e1-106">このトピックでは、 **SubmitToWorkflow** クラスを作成する方法、およびワークフロー タイプの名前を使用してワークフローを有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-106">This topic describes how to create a **SubmitToWorkflow** class and use the name of the workflow type to activate the workflow.</span></span>

<span data-ttu-id="c91e1-107">ワークフロー コンフィギュレーション IDまたはワークフローのシーケンス 番号を使用してワークフローを有効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-107">You can also activate a workflow by using the workflow configuration ID or the workflow sequence number.</span></span> <span data-ttu-id="c91e1-108">基本的な手順は同じです。</span><span class="sxs-lookup"><span data-stu-id="c91e1-108">The basic procedure is the same.</span></span> <span data-ttu-id="c91e1-109">詳細については、 [ワークフローの有効化](https://docs.microsoft.com/dynamicsax-2012/developer/activating-a-workflow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c91e1-109">For more information, see [Activating a workflow](https://docs.microsoft.com/dynamicsax-2012/developer/activating-a-workflow).</span></span>

> [!NOTE]
> <span data-ttu-id="c91e1-110">**ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ウィザードが、ワークフロー送信マネージャー クラスを既に作成しています。</span><span class="sxs-lookup"><span data-stu-id="c91e1-110">If you used the **Workflow** wizard to create the workflow type, the wizard has already created a workflow submission manager class.</span></span> <span data-ttu-id="c91e1-111">単にコードを追加するだけです。</span><span class="sxs-lookup"><span data-stu-id="c91e1-111">You just have to add code to it.</span></span>

## <a name="create-a-submittoworkflow-class"></a><span data-ttu-id="c91e1-112">SubmitToWorkflow クラスの作成</span><span class="sxs-lookup"><span data-stu-id="c91e1-112">Create a SubmitToWorkflow class</span></span>

1. <span data-ttu-id="c91e1-113">アプリケーション エクスプローラーで、 **クラス** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-113">In Application Explorer, expand the **Classes** node.</span></span>
2. <span data-ttu-id="c91e1-114">**クラス** ノードを右クリックし、 **新しいクラス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-114">Right-click the **Classes** node, and then select **New Class**.</span></span> <span data-ttu-id="c91e1-115">クラス グループは、 **クラス** ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-115">A class group appears under the **Classes** node.</span></span>
3. <span data-ttu-id="c91e1-116">新しい クラスを右クリックし、 **新しいメソッド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-116">Right-click the new class, and then select **New Method**.</span></span> <span data-ttu-id="c91e1-117">**クラス** ノードの下に新しいメソッド ノードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-117">A new method node appears under the **Classes** node.</span></span>
4. <span data-ttu-id="c91e1-118">新しいメソッドを右クリックし、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-118">Right-click the new method, and then select **Edit**.</span></span>
5. <span data-ttu-id="c91e1-119">ワークフローを有効化するためにワークフロー タイプの名前を使用する **main** メソッドに次のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-119">Enter the following code for the **main** method to use the name of the workflow type to activate the workflow.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c91e1-120">この例は、ワークフローの送信に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-120">This example applies to workflow submissions.</span></span> <span data-ttu-id="c91e1-121">エンタープライズ ポータルでも機能する例については、 [ワークフロー送信のためのエンタープライズ ポータル サポートの追加](https://docs.microsoft.com/dynamicsax-2012/developer/adding-enterprise-portal-support-for-workflow-submission) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c91e1-121">For an example that also works with Enterprise Portal, see [Adding enterprise portal support for workflow submission](https://docs.microsoft.com/dynamicsax-2012/developer/adding-enterprise-portal-support-for-workflow-submission).</span></span>

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

6. <span data-ttu-id="c91e1-122">**エディター** ウィンドウを閉じ、 **はい** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="c91e1-122">Close the **Editor** window, and select **Yes** to save your changes.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c91e1-123">このコードを保存すると、 **catch(exception::Error)** ブロックに有効なコードを追加しない限り、 **コンパイラ出力** ウィンドウに "空の複合文" の警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c91e1-123">When you save this code, you will receive an "Empty compound statement" warning message in the **Compiler Output** window unless you add valid code in the **catch(exception::Error)** block.</span></span>

## <a name="see-also"></a><span data-ttu-id="c91e1-124">参照</span><span class="sxs-lookup"><span data-stu-id="c91e1-124">See also</span></span>

[<span data-ttu-id="c91e1-125">ワークフローの有効化</span><span class="sxs-lookup"><span data-stu-id="c91e1-125">Activating a workflow</span></span>](https://docs.microsoft.com/dynamicsax-2012/developer/activating-a-workflow)

[<span data-ttu-id="c91e1-126">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="c91e1-126">Create a new workflow type</span></span>](workflow-type-create-new.md)

<span data-ttu-id="c91e1-127">[ワークフロー::activateFromWorkflowType メソッド](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812416(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="c91e1-127">[Workflow::activateFromWorkflowType method](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812416(v=ax.60))</span></span>

<span data-ttu-id="c91e1-128">[ワークフロー::activateFromWorkflowSequenceNumber メソッド](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812415(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="c91e1-128">[Workflow::activateFromWorkflowSequenceNumber method](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812415(v=ax.60))</span></span>

<span data-ttu-id="c91e1-129">[ワークフロー::activateFromWorkflowConfigurationId メソッド](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812414(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="c91e1-129">[Workflow::activateFromWorkflowConfigurationId method](https://docs.microsoft.com/previous-versions/dynamics/ax-2012/application-classes/gg812414(v=ax.60))</span></span>
