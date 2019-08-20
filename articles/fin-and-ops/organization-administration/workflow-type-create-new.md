---
title: 新しいワークフロー タイプの作成
description: このトピックでは、 Microsoft Dynamics 365 for Finance and Operations のアプリケーション エクスプローラーでワークフロー タイプを作成する方法について説明します。
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
ms.openlocfilehash: c17b8410472b1eecbeaf994f8e2bcb7cea8e76d1
ms.sourcegitcommit: 4fd51830be21b95a1398dc80d5429a74bcec73fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2019
ms.locfileid: "1736970"
---
# <a name="create-a-new-workflow-type"></a><span data-ttu-id="c96e4-103">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="c96e4-103">Create a new workflow type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c96e4-104">ワークフロー プロセスをワークフロー ドキュメントで使用できるようにするには、ワークフロー コンフィギュレーション ユーザーインター フェイス (UI) で使用されるワークフロー タイプを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c96e4-104">To make the workflow process available for a workflow document, you must create the workflow types that are used in the workflow configuration user interface (UI).</span></span> <span data-ttu-id="c96e4-105">このトピックでは、アプリケーション エクスプローラーでワークフロー タイプを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-105">This topic describes how to create a workflow type in Application Explorer.</span></span>

<span data-ttu-id="c96e4-106">ワークフロー タイプでは、次の情報を定義します:</span><span class="sxs-lookup"><span data-stu-id="c96e4-106">A workflow type defines the following information:</span></span>

- <span data-ttu-id="c96e4-107">ワークフローが使用されるドキュメント</span><span class="sxs-lookup"><span data-stu-id="c96e4-107">The document that the workflow is used for</span></span>
- <span data-ttu-id="c96e4-108">ワークフロー タイプを特定のモジュールに割り当てるために使用するワークフロー カテゴリ。</span><span class="sxs-lookup"><span data-stu-id="c96e4-108">Workflow categories, which are used to assign a workflow type to a specific module</span></span>
- <span data-ttu-id="c96e4-109">ユーザーが構成できるタスク、自動化タスク、承認、および行項目ワークフロー</span><span class="sxs-lookup"><span data-stu-id="c96e4-109">Tasks, automated tasks, approvals, and line item workflows that the user can configure</span></span>
- <span data-ttu-id="c96e4-110">メニュー項目とイベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="c96e4-110">Menu items and event handlers</span></span>

## <a name="create-a-new-workflow-type"></a><span data-ttu-id="c96e4-111">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="c96e4-111">Create a new workflow type</span></span>

1. <span data-ttu-id="c96e4-112">次のいずれかの手順に従って、 **ワークフロー** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-112">Follow one of these steps to open the **Workflow** wizard.</span></span> <span data-ttu-id="c96e4-113">ウィザードは、新しいワークフロー タイプを作成するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-113">The wizard will help you create a new workflow type.</span></span>

    + <span data-ttu-id="c96e4-114">アプリケーションエクスプローラーで、 **ビジネスプロセスとワークフロー** ノードを右クリックし、次に **アドイン** \> **ワークフロー タイプ ウィザード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-114">In Application Explorer, right-click the **Business Process and Workflow** node, and then select **Add-Ins** \> **Workflow type wizard**.</span></span>
    + <span data-ttu-id="c96e4-115">**プロジェクト** メニューの **新しい項目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-115">On the **Project** menu, select **Add new item**.</span></span> <span data-ttu-id="c96e4-116">**新しい項目の追加** ダイアログ ボックスで、 **ワークフロー タイプ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-116">In the **Add new item** dialog box, select **Workflow type**.</span></span> <span data-ttu-id="c96e4-117">クエリ名を入力し、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-117">Enter a name for the query, and then select **Create**.</span></span>

2. <span data-ttu-id="c96e4-118">ウィザードに、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-118">Set the following values for the wizard.</span></span>

    | <span data-ttu-id="c96e4-119">金額</span><span class="sxs-lookup"><span data-stu-id="c96e4-119">Value</span></span> | <span data-ttu-id="c96e4-120">説明</span><span class="sxs-lookup"><span data-stu-id="c96e4-120">Description</span></span> |
    |---|---|
    | <span data-ttu-id="c96e4-121">氏名</span><span class="sxs-lookup"><span data-stu-id="c96e4-121">Name</span></span> | <span data-ttu-id="c96e4-122">ワークフロー タイプに使用される名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-122">Specify the name that will be used for the workflow type.</span></span> |
    | <span data-ttu-id="c96e4-123">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="c96e4-123">Category</span></span> | <span data-ttu-id="c96e4-124">ワークフロー タイプに使用されるワークフロー カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-124">Select the workflow category that will be used for the workflow type.</span></span> <span data-ttu-id="c96e4-125">カテゴリにより、ワークフロー タイプを使用できるモジュールが決まります。</span><span class="sxs-lookup"><span data-stu-id="c96e4-125">The category determines the module that the workflow type is available in.</span></span> <span data-ttu-id="c96e4-126">既存のカテゴリまたは作成した新しいカテゴリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-126">You can use an existing category or a new category that you create.</span></span> <span data-ttu-id="c96e4-127">詳細については、 [新しいワークフロー カテゴリの作成](workflow-type-category.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c96e4-127">For more information, see [Create a workflow category](workflow-type-category.md).</span></span> |
    | <span data-ttu-id="c96e4-128">クエリ</span><span class="sxs-lookup"><span data-stu-id="c96e4-128">Query</span></span> | <span data-ttu-id="c96e4-129">ワークフロー ドキュメントのテーブル フィールドにアクセスするクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-129">Select the query that will access the table fields for the workflow document.</span></span> <span data-ttu-id="c96e4-130">詳細については、 [ワークフロー タイプのクエリの作成](workflow-type-query.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c96e4-130">For more information, see [Create a query for a workflow type](workflow-type-query.md).</span></span> |
    | <span data-ttu-id="c96e4-131">ドキュメント メニュー項目</span><span class="sxs-lookup"><span data-stu-id="c96e4-131">Document menu item</span></span> | <span data-ttu-id="c96e4-132">ワークフロータイプを作成しているドキュメントを表示するメインページを指すメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-132">Select the menu item that points to the main page that shows the document that you're creating the workflow type for.</span></span> |
    | <span data-ttu-id="c96e4-133">ドキュメント Web メニュー項目</span><span class="sxs-lookup"><span data-stu-id="c96e4-133">Document web menu item</span></span> | <span data-ttu-id="c96e4-134">ワークフロータイプを作成しているドキュメントを表示するエンタープライズ ポータル ページを指すWebメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-134">Select the web menu item that points to the Enterprise Portal page that shows the document that you're creating the workflow type for.</span></span> |

3. <span data-ttu-id="c96e4-135">作成するメニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-135">Specify the types of menu items that you want to create.</span></span> <span data-ttu-id="c96e4-136">Microsoft Dynamics 365 for Finance and Operations クライアント、エンタープライズ ポータルの web メニュー項目、またはクライアントとエンタープライズ ポータルの両方の項目について、メニュー項目を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-136">You can create menu items for the Microsoft Dynamics 365 for Finance and Operations client, web menu items for Enterprise Portal, or items for both the client and Enterprise Portal.</span></span>
4. <span data-ttu-id="c96e4-137">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-137">Select **Next**.</span></span> <span data-ttu-id="c96e4-138">ワークフロータイプに対して作成されるすべてのリソースの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-138">A list of all the resources that will be created for the workflow type is shown.</span></span>
5. <span data-ttu-id="c96e4-139">**完了** を選択すると、リソースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-139">Select **Finish** to create the resources.</span></span> <span data-ttu-id="c96e4-140">ウィザードによって、クラス、メニュー項目、web メニュー項目、ワークフロー タイプ、およびすべての項目を含むプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-140">The wizard creates classes, menu items, web menu items, the workflow type, and a project that contains all the items.</span></span>
6. <span data-ttu-id="c96e4-141">ステータスを示すダイアログ ボックスが表示されたら、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-141">When dialog box appears that indicates the status, select **OK**.</span></span> <span data-ttu-id="c96e4-142">ワークフロータイプのリソースを含むプロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c96e4-142">The project that contains the workflow type resources is shown.</span></span>

<span data-ttu-id="c96e4-143">ワークフロー タイプを作成したら、次のステップとして、ワークフロー ドキュメント クラスを作成して、条件のドキュメント データを公開します。</span><span class="sxs-lookup"><span data-stu-id="c96e4-143">After you create a workflow type, the next step is to create a workflow document class to expose document data for conditions.</span></span> <span data-ttu-id="c96e4-144">詳細については、 [新しいワークフロー ドキュメント クラスの作成](workflow-type-document-create.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c96e4-144">For more information, see [Create a workflow document class](workflow-type-document-create.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c96e4-145">参照</span><span class="sxs-lookup"><span data-stu-id="c96e4-145">See also</span></span>

[<span data-ttu-id="c96e4-146">ワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="c96e4-146">Creating a workflow type</span></span>](workflow-type-create.md)

[<span data-ttu-id="c96e4-147">ワークフロー カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="c96e4-147">Create a workflow category</span></span>](workflow-type-category.md)
