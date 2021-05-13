---
title: ワークフロー ドキュメント クラスの作成
description: このトピックでは、ワークフロー ドキュメント クラスを作成する方法について説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 202694
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: d700cc17edc378f3022c90ef0b95ef50f78fec21
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890345"
---
# <a name="create-a-workflow-document-class"></a><span data-ttu-id="ef47a-103">ワークフロー ドキュメント クラスの作成</span><span class="sxs-lookup"><span data-stu-id="ef47a-103">Create a workflow document class</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef47a-104">クエリでテーブルフィールドを定義して、ワークフロー条件を作成します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-104">You define table fields in a query to create workflow conditions.</span></span> <span data-ttu-id="ef47a-105">一般的なシナリオでは、計算済フィールドはワークフローの動作を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-105">In a typical scenario, calculated fields are used to determine the behavior of a workflow.</span></span> <span data-ttu-id="ef47a-106">たとえば、テーブル内のすべてのレコードの動的な販売合計をワークフロー条件として使用し、ステップを使用するかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-106">For example, a dynamic sales total of all records in a table can be used as a workflow condition to determine whether the step should be used.</span></span> <span data-ttu-id="ef47a-107">ただし、クエリの制限としては、クエリ自体に計算済フィールドを定義できないことが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-107">However, a limitation of queries is that you can't define calculated fields in the queries themselves.</span></span> <span data-ttu-id="ef47a-108">このクエリ制限を克服するには、ワークフロー ドキュメント クラスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-108">To overcome this query limitation, you must use a workflow document class.</span></span> <span data-ttu-id="ef47a-109">このトピックでは、ワークフロー ドキュメント クラスを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-109">This topic describes how to create a workflow document class.</span></span>

<span data-ttu-id="ef47a-110">作成するワークフロー ドキュメント クラスは、アプリケーション エクスプローラーのクエリとパラメータ メソッドという 2 つの方法で、条件のテーブル フィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-110">The workflow document class that you create defines table fields for conditions in two ways: the Application Explorer query and parameter methods.</span></span> <span data-ttu-id="ef47a-111">クエリの名前を返すには、 [WorkflowDocument クラス](/previous-versions/dynamics/ax-2012/application-classes/gg798542(v=ax.60)) の **getQueryName** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-111">You must override the **getQueryName** method of the [WorkflowDocument class](/previous-versions/dynamics/ax-2012/application-classes/gg798542(v=ax.60)) to return the name of the query.</span></span> <span data-ttu-id="ef47a-112">必要に応じて、クラスの特定の署名を持つパラメータ メソッドを追加して、計算済フィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-112">You can optionally add calculated fields by adding parameter methods that have a specific signature on the class.</span></span> <span data-ttu-id="ef47a-113">ワークフロー条件の詳細については、 [ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md) と [ワークフローでの条件付き意思決定のコンフィギュレーション](configure-conditional-decision-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef47a-113">For more information about workflow conditions, see [Configure workflow properties](configure-workflow-properties.md) and [Configure conditional decisions in a workflow](configure-conditional-decision-workflow.md).</span></span>

<span data-ttu-id="ef47a-114">次の手順では、計算済フィールドのパラメータ メソッドを含むワークフロー ドキュメント クラスを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-114">The following procedures explain how to create a workflow document class that includes a parameter method for a calculated field.</span></span> <span data-ttu-id="ef47a-115">開始する前に、アクセスするデータを指定するクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-115">Before you begin, you must create a query that specifies the data that will be accessed.</span></span> <span data-ttu-id="ef47a-116">ワークフロー クエリの詳細については、 [ワークフロー タイプのクエリの作成](workflow-type-query.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef47a-116">For more information about workflow queries, see [Create a query for a workflow type](workflow-type-query.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ef47a-117">**ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ウィザードはワークフロー ドキュメント クラスを既に作成しています。</span><span class="sxs-lookup"><span data-stu-id="ef47a-117">If you used the **Workflow** wizard to create the workflow type, the wizard has already created the workflow document class.</span></span>

## <a name="create-a-workflow-document-class"></a><span data-ttu-id="ef47a-118">ワークフロー ドキュメント クラスの作成</span><span class="sxs-lookup"><span data-stu-id="ef47a-118">Create a workflow document class</span></span>

1. <span data-ttu-id="ef47a-119">新しいクエリを作成するには、次のいずれかのステップを実行します</span><span class="sxs-lookup"><span data-stu-id="ef47a-119">Follow one of these steps to create a new query:</span></span>

    + <span data-ttu-id="ef47a-120">アプリケーション エクスプローラーで、 **クラス** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-120">In Application Explorer, expand the **Classes** node.</span></span> <span data-ttu-id="ef47a-121">**クラス** ノードを右クリックし、 **新しいクラス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-121">Right-click the **Classes** node, and then select **New Class**.</span></span> <span data-ttu-id="ef47a-122">クラス グループは、 **クラス** ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-122">A class group appears under the **Classes** node.</span></span> <span data-ttu-id="ef47a-123">新しいクラスを右クリックし、 **名前変更** を選択して、ワークフロー ドキュメント クラスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-123">Right-click the new class, select **Rename**, and then enter a name for the workflow document class.</span></span>
    + <span data-ttu-id="ef47a-124">**プロジェクト** メニューの **新しい項目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-124">On the **Project** menu, select **Add new item**.</span></span> <span data-ttu-id="ef47a-125">**新しい項目の追加** ダイアログ ボックスで、 **クラス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-125">In the **Add new item** dialog box, select **Class**.</span></span> <span data-ttu-id="ef47a-126">クラス名を入力し、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-126">Enter a name for the class, and then select **Create**.</span></span>

2. <span data-ttu-id="ef47a-127">新しいクラスを展開し、 **classDeclaration** を選択し、クラス宣言を右クリックして、次に **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-127">Expand the new class, select **classDeclaration**, right-click the class declaration, and then select **Edit**.</span></span>
3. <span data-ttu-id="ef47a-128">クラス宣言に次のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-128">Enter the following code in the class declaration.</span></span>

    ```X++
    class <MyWorkflowDocumentClassName> extends WorkflowDocument
    {
    }
    ```

4. <span data-ttu-id="ef47a-129">**エディター** ウィンドウを閉じ、 **はい** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-129">Close the **Editor** window, and select **Yes** to save your changes.</span></span>
5. <span data-ttu-id="ef47a-130">新しいクラスを右クリックし、 **オーバーライド メソッド** をポイントして、次に **getQueryName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-130">Right-click the new class, point to **Override Method**, and then select **getQueryName**.</span></span> <span data-ttu-id="ef47a-131">**GetQueryName** という名前のメソッド ノードがワークフロー ドキュメント クラス ノードの下に表示され、 **エディター** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-131">A method node that is named **getQueryName** appears under the workflow document class node, and the **Editor** window appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef47a-132">オーバーライドする方法として **getQueryName** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="ef47a-132">Be sure to select **getQueryName** as the method to override.</span></span> <span data-ttu-id="ef47a-133">[WorkflowDocument.getQuery メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg798533(v=ax.60)) は、 [WorkflowDocument.getQueryName メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg798541(v=ax.60)) によって返される文字列に基づいて、実際のクエリを取得するために内部的にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-133">The [WorkflowDocument.getQuery method](/previous-versions/dynamics/ax-2012/application-classes/gg798533(v=ax.60)) is used only internally to retrieve the actual query, based on the string that is returned by the [WorkflowDocument.getQueryName method](/previous-versions/dynamics/ax-2012/application-classes/gg798541(v=ax.60)).</span></span>

6. <span data-ttu-id="ef47a-134">**エディター** ウィンドウで、次のコードをクエリ メソッドに入力します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-134">In the **Editor** window, enter the following code for the query method.</span></span>

    ```X++
    QueryName getQueryName()
    {
        return querystr(<MyWorkflowDocumentQueryName>);
    }
    ```

<span data-ttu-id="ef47a-135">ワークフロー ドキュメント クラスを作成した後、それをワークフロー タイプにバインドできます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-135">After you create the workflow document class, you can bind it to the workflow type.</span></span> <span data-ttu-id="ef47a-136">詳細については、 [ワークフロー ドキュメント クラスとワークフロー タイプの関連付け](workflow-type-associate-document.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef47a-136">For more information, see [Associate a workflow document class with a workflow type](workflow-type-associate-document.md).</span></span>

<span data-ttu-id="ef47a-137">ワークフロー ドキュメント クラスに計算済フィールドを追加できるのは、次の条件を満たしている場合だけです。</span><span class="sxs-lookup"><span data-stu-id="ef47a-137">You can add a calculated field to the workflow document class only if it meets these conditions:</span></span>

- <span data-ttu-id="ef47a-138">**parm \<name\>** という名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-138">It must be named **parm \<name\>**.</span></span>
- <span data-ttu-id="ef47a-139">**CompanyId**、 **TableId**、および **RecId** の各パラメータを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-139">It must define the **CompanyId**, **TableId**, and **RecId** parameters.</span></span>
- <span data-ttu-id="ef47a-140">条件または通知メッセージを定義するフィールドの一覧に含まれる拡張データ型 (EDT) を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-140">It must return an extended data type (EDT) that will be included in the list of fields that define conditions or notification messages.</span></span> <span data-ttu-id="ef47a-141">EDTのラベルは、値を一意に識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef47a-141">The label for the EDT must uniquely identify the value.</span></span>

## <a name="add-a-calculated-field-to-the-workflow-document-class"></a><span data-ttu-id="ef47a-142">ワークフロー ドキュメント クラスへの計算済フィールドの追加</span><span class="sxs-lookup"><span data-stu-id="ef47a-142">Add a calculated field to the workflow document class</span></span>

1. <span data-ttu-id="ef47a-143">計算済フィールドを追加するワークフロー ドキュメント クラスで、クラスを右クリックして、 **新しいメソッド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-143">In the workflow document class that you want to add a calculated field to, right-click the class, and then select **New Method**.</span></span> <span data-ttu-id="ef47a-144">**クラス** ノードの下に新しいメソッド ノードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef47a-144">A new method node appears under the **Classes** node.</span></span>
2. <span data-ttu-id="ef47a-145">新しいメソッド ノードを右クリックし、 **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-145">Right-click the new method node, and then select **Edit**.</span></span>
3. <span data-ttu-id="ef47a-146">次の例に示す形式でコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-146">Enter code in the format that is shown in the following example.</span></span> <span data-ttu-id="ef47a-147">この例では、計算済フィールドを追加して仕訳帳の貸方金額の合計を決定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ef47a-147">This example shows how to add a calculated field to determine the total credit amount for a journal.</span></span>

    ```X++
    public TotalJournalCreditAmount parmTotalJournalCreditAmount(CompanyId _companyId, TableId _tableId, RecId _recId)
    {
        // The calculateAmounts method contains business and validation logic
        this.calculateAmounts(_companyId, _tableId, _recId);
        return totalJournalCreditAmount;
    }
    ```

## <a name="see-also"></a><span data-ttu-id="ef47a-148">参照</span><span class="sxs-lookup"><span data-stu-id="ef47a-148">See also</span></span>

[<span data-ttu-id="ef47a-149">ワークフロー ドキュメント クラスとワークフロー タイプの関連付け</span><span class="sxs-lookup"><span data-stu-id="ef47a-149">Associate a workflow document class with a workflow type</span></span>](workflow-type-associate-document.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]