---
title: ワークフロー カテゴリの作成
description: このトピックでは、ワークフロー カテゴリの作成方法を説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 84d8780261e5dde83582f46c148365dd5ff19604
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747135"
---
# <a name="create-a-workflow-category"></a><span data-ttu-id="3fc36-103">ワークフロー カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="3fc36-103">Create a workflow category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fc36-104">ワークフロー タイプを作成する際には、ワークフロー タイプをその質問に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fc36-104">When you create a workflow type, you must assign it to a workflow category.</span></span> <span data-ttu-id="3fc36-105">ワークフロー カテゴリによって、特定のモジュールでワークフロー タイプを使用できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="3fc36-105">The workflow category determines whether the workflow type is available in a specific module.</span></span> <span data-ttu-id="3fc36-106">適切なワークフロー カテゴリがまだ存在していない場合は、作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3fc36-106">If an appropriate workflow category doesn't already exist, you must create it.</span></span>

<span data-ttu-id="3fc36-107">たとえば、顧客請求書のワークフロー タイプは、 **マスター プラン** モジュールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="3fc36-107">For example, a workflow type for a customer invoice should not be available in the **Master planning** module.</span></span> <span data-ttu-id="3fc36-108">ワークフロー タイプを **顧客** モジュールでのみ使用できるようにするには、ワークフロー カテゴリの作成時に **顧客** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-108">To make the workflow type available only in the **Customer** module, select the **Customer** module when you create a workflow category.</span></span>

<span data-ttu-id="3fc36-109">このトピックでは、ワークフロー カテゴリの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-109">This topic describes how to create a workflow category.</span></span>

## <a name="create-a-workflow-category"></a><span data-ttu-id="3fc36-110">ワークフロー カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="3fc36-110">Create a workflow category</span></span>

1. <span data-ttu-id="3fc36-111">アプリケーション エクスプローラーで、 **ビジネス プロセスとワークフロー** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-111">In Application Explorer, expand the **Business Process and Workflow** node.</span></span>
2. <span data-ttu-id="3fc36-112">次のいずれかの手順に従って、ワークフロー カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-112">Follow one of these steps to create the workflow category:</span></span>

    + <span data-ttu-id="3fc36-113">**ワークフロー カテゴリ** ノードを右クリックし、 **新しいワークフロー カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-113">Right-click the **Workflow Categories** node, and then select **New Workflow Category**.</span></span> <span data-ttu-id="3fc36-114">新しいワークフロー カテゴリ グループが **ワークフロー カテゴリ** ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3fc36-114">A new workflow category group appears under the **Workflow Categories** node.</span></span> <span data-ttu-id="3fc36-115">新しいワークフロー カテゴリを右クリックし、 **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-115">Right-click the new workflow category, and then select **Properties**.</span></span>
    + <span data-ttu-id="3fc36-116">**プロジェクト** メニューの **新しい項目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-116">On the **Project** menu, select **Add new item**.</span></span> <span data-ttu-id="3fc36-117">**新しい項目の追加** ダイアログ ボックスで、 **ワークフロー カテゴリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-117">In the **Add new item** dialog box, select **Workflow category**.</span></span> <span data-ttu-id="3fc36-118">新しいカテゴリ名を入力し、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-118">Enter a name for the category, and then select **Create**.</span></span>

3. <span data-ttu-id="3fc36-119">**プロパティ** シートで、必要に応じて次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-119">On the **Properties** sheet, set the following properties, as required.</span></span>

    | <span data-ttu-id="3fc36-120">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3fc36-120">Property</span></span> | <span data-ttu-id="3fc36-121">金額</span><span class="sxs-lookup"><span data-stu-id="3fc36-121">Value</span></span> |
    |---|---|
    | <span data-ttu-id="3fc36-122">氏名</span><span class="sxs-lookup"><span data-stu-id="3fc36-122">Name</span></span> | <span data-ttu-id="3fc36-123">ワークフロー カテゴリを参照するために使用される名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-123">Specify the name that is used to reference the workflow category.</span></span> |
    | <span data-ttu-id="3fc36-124">ラベル</span><span class="sxs-lookup"><span data-stu-id="3fc36-124">Label</span></span> | <span data-ttu-id="3fc36-125">ユーザー インターフェイス (UI) でワークフロー カテゴリに使用されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-125">Specify the label that is used for the workflow category in the user interface (UI).</span></span> |
    | <span data-ttu-id="3fc36-126">ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="3fc36-126">Help Text</span></span> | <span data-ttu-id="3fc36-127">ワークフロー コンフィギュレーション UI でワークフロー カテゴリに表示される説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-127">Specify the description that is shown for the workflow category in the workflow configuration UI.</span></span> |
    | <span data-ttu-id="3fc36-128">モジュール</span><span class="sxs-lookup"><span data-stu-id="3fc36-128">Module</span></span> | <span data-ttu-id="3fc36-129">ワークフローが使用できるモジュールを指定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-129">Specify the module that the workflow will be available in.</span></span> <span data-ttu-id="3fc36-130">既定のモジュールは **元帳** です。</span><span class="sxs-lookup"><span data-stu-id="3fc36-130">The default module is **Ledger**.</span></span> |

<span data-ttu-id="3fc36-131">ワークフローカテゴリを作成した後、ワークフロー タイプをバインドすることができます。</span><span class="sxs-lookup"><span data-stu-id="3fc36-131">After you create a workflow category, a workflow type can be bound to it.</span></span> <span data-ttu-id="3fc36-132">通常は、 **ワークフロー** ウィザードでこの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-132">Typically, the **Workflow** wizard completes this step.</span></span> <span data-ttu-id="3fc36-133">ただし、次の手順では、ワークフロー タイプをワークフロー カテゴリに手動でバインドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-133">However, the following procedure explains how to manually bind a workflow type to a workflow category.</span></span>

## <a name="bind-a-workflow-type-to-a-workflow-category"></a><span data-ttu-id="3fc36-134">ワークフロー タイプをワークフロー カテゴリにバインドする</span><span class="sxs-lookup"><span data-stu-id="3fc36-134">Bind a workflow type to a workflow category</span></span>

1. <span data-ttu-id="3fc36-135">アプリケーションエクスプローラーで、 **ビジネスプロセスとワークフロー** ノードを展開し、次に **ワークフロー タイプ** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-135">In Application Explorer, expand the **Business Process and Workflow** node, and then expand the **Workflow Types** node.</span></span>
2. <span data-ttu-id="3fc36-136">ワークフロー カテゴリにバインドするワークフロー タイプを右クリックし、 **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-136">Right-click the workflow type that you want to bind to a workflow category, and then select **Properties**.</span></span>
3. <span data-ttu-id="3fc36-137">**プロパティ** シートで、 **カテゴリ** プロパティを前の手順で作成したワークフロー カテゴリに設定します。</span><span class="sxs-lookup"><span data-stu-id="3fc36-137">On the **Properties** sheet, set the **Category** property to the workflow category that you created in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fc36-138">参照</span><span class="sxs-lookup"><span data-stu-id="3fc36-138">See also</span></span>

[<span data-ttu-id="3fc36-139">ワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="3fc36-139">Create a workflow type</span></span>](workflow-type-create.md)

[<span data-ttu-id="3fc36-140">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="3fc36-140">Create a new workflow type</span></span>](workflow-type-create-new.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]