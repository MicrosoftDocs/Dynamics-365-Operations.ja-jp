---
title: 消費の登録
description: このトピックでは、資産管理で消費を登録する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 174c816c7a6442b07e4722c03045293b94c59153
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024663"
---
# <a name="register-consumption"></a><span data-ttu-id="f8317-103">消費の登録</span><span class="sxs-lookup"><span data-stu-id="f8317-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="f8317-104">ワーク オーダーでメンテナンス作業が完了したら、次のステップで、消費を登録して仕訳帳を転記します。</span><span class="sxs-lookup"><span data-stu-id="f8317-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="f8317-105">時間、品目、および経費のいずれかの消費タイプで登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f8317-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="f8317-106">さまざまな消費タイプが、**ワーク オーダー仕訳帳**ページに登録および転記されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="f8317-107">**資産管理**における仕訳帳の設定は、**プロジェクト管理および会計**モジュールで時間、品目、および経費の、個別の仕訳帳を作成および転記するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="f8317-108">作業指示書の予測明細行を追加または削除できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f8317-108">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="f8317-109">ワーク オーダーのライフサイクル状態の設定、関連するプロジェクト タイプ、およびプロジェクト タイプに関連するステージ ルールにより、仕訳帳明細行を追加または編集できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="f8317-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="f8317-110">ワーク オーダーのライフサイクル状態と、関連するプロジェクト ステージの詳細については、[プロジェクト管理および会計への統合](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8317-110">Read more about work order lifecycle states and related project stages in [Integration to project management and accounting](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="f8317-111">ワーク オーダーのライフサイクル状態での仕訳帳の自動転記を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f8317-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="f8317-112">詳細については、[ワーク オーダーのライフサイクル状態](../setup-for-work-orders/work-order-lifecycle-states.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8317-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="f8317-113">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f8317-114">ワーク オーダーを選択し、**仕訳帳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-114">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f8317-115">**予測からコピー**をクリックして、ワーク オーダーに関連付けられている予測明細行を転送します。</span><span class="sxs-lookup"><span data-stu-id="f8317-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="f8317-116">転送する消費タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8317-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="f8317-117">必要に応じて、**行の追加**をクリックし、明細行にデータを入力することで、関連するクイック タブに消費明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f8317-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="f8317-118">**仕訳帳の検証**をクリックして、転記する前に仕訳帳を検証します。</span><span class="sxs-lookup"><span data-stu-id="f8317-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="f8317-119">**仕訳帳の転記**をクリックし、仕訳帳明細行を転記します。</span><span class="sxs-lookup"><span data-stu-id="f8317-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="f8317-120">消費仕訳帳を転記した後は、ワーク オーダーのライフサイクル状態を更新 (たとえば、「終了」など) して、ワーク オーダーが完了したことを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="f8317-120">After you've posted the consumption journals, you can update the work order lifecycle state, for example to "Ended", to indicate that the work order has been completed.</span></span>

- <span data-ttu-id="f8317-121">**ワーク オーダー仕訳帳**ページの上部にある**表示**フィールドで、表示する仕訳帳明細行を、すべて、未転記、または転記済から選択します。</span><span class="sxs-lookup"><span data-stu-id="f8317-121">In the **Show** field placed at the top of the **Work order journals** page, select which journal lines you want to see: All, Not posted, or Posted.</span></span> <span data-ttu-id="f8317-122">転記済仕訳帳の場合は、**転記済**チェック ボックスがオンになります。</span><span class="sxs-lookup"><span data-stu-id="f8317-122">Posted journals have a check mark in the **Posted** check box.</span></span>  
- <span data-ttu-id="f8317-123">品目明細行がワーク オーダー仕訳帳で作成されると、その品目に関連付けられている製品分析コードと追跡用分析コードが、自動的に仕訳帳明細行に転送されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-123">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="f8317-124">次のスクリーンショットは、**ワーク オーダー仕訳帳**のワーク オーダーにおける時間と品目の登録の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f8317-124">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![図 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="f8317-126">複数のワーク オーダー ジョブを含むワーク オーダーの時間分割</span><span class="sxs-lookup"><span data-stu-id="f8317-126">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="f8317-127">ワーク オーダーに複数のワーク オーダー ジョブが含まれている場合は、**時間分割**機能を使用して作業時間を登録することができます。つまり、1 時間の登録明細行を各ワーク オーダー ジョブに均等に配分することができます。</span><span class="sxs-lookup"><span data-stu-id="f8317-127">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="f8317-128">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-128">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="f8317-129">ワーク オーダーを選択し、**仕訳帳**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-129">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="f8317-130">分割する時間登録明細行を選択し、**時間分割**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-130">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="f8317-131">**ワーク オーダー メンテナンス ジョブ** ダイアログでは、ログインしている作業者の名前が**作業者**フィールドに自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-131">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="f8317-132">必要に応じて、別の作業者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f8317-132">If required, you can select another worker.</span></span>

5. <span data-ttu-id="f8317-133">**カテゴリ** フィールドで、時間登録のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8317-133">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="f8317-134">**時間**フィールドに、分割する作業時間を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f8317-134">Insert number of work hours to be split in the **Hours** field.</span></span>

![図 2](media/02-consumption.png)

7. <span data-ttu-id="f8317-136">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f8317-136">Click **OK**.</span></span>

<span data-ttu-id="f8317-137">*例 :* 下のスクリーンショットには、3 つのワーク オーダー ジョブを含むワーク オーダーの仕訳帳明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-137">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="f8317-138">3 つの作業時間を含む最初の明細行が分割され、各ワーク オーダー ジョブに 1 つの作業時間が登録されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-138">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="f8317-139">3 つの時間登録明細行を作成した後で、元の時間登録明細行 (例の最初の明細行) をどうするか決定します。</span><span class="sxs-lookup"><span data-stu-id="f8317-139">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="f8317-140">そのままにすることも、削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="f8317-140">You can keep it as is or delete it.</span></span> 

![図 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="f8317-142">消費登録の財務分析コード</span><span class="sxs-lookup"><span data-stu-id="f8317-142">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="f8317-143">消費登録を行うと、さまざまな登録タイプに関連する財務分析コードが、特定の順序で登録に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-143">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

<span data-ttu-id="f8317-144">*時間および経費の登録 :* 最初に、仕訳帳ヘッダーの財務分析コードが追加されます (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="f8317-144">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f8317-145">次に、関連するワーク オーダー プロジェクトの財務分析コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-145">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f8317-146">最後に、リソース (作業者) からの財務分析コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-146">Finally, financial dimensions from the resource (worker) are added.</span></span>

<span data-ttu-id="f8317-147">*品目の登録 :* 最初に、仕訳帳ヘッダーの財務分析コードが追加されます (存在する場合)。</span><span class="sxs-lookup"><span data-stu-id="f8317-147">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="f8317-148">そして、関連するワーク オーダー プロジェクトの財務分析コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-148">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="f8317-149">次に、サイトからの財務分析コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-149">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="f8317-150">最後に品目からの財務分析コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="f8317-150">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="f8317-151">3 つの登録タイプすべてについて、財務分析コードの組み合わせが検証され、無効な組み合わせは空白になります。</span><span class="sxs-lookup"><span data-stu-id="f8317-151">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="f8317-152">これは、Finance and Operations における標準設定です。</span><span class="sxs-lookup"><span data-stu-id="f8317-152">This is standard setup in Finance and Operations.</span></span>

