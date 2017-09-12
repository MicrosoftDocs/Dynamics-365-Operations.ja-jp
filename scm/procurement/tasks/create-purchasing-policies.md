--- 
title: "購入ポリシーの作成"
description: "この手順では、購買の業務プロセスに対応する購入ポリシーを作成する方法を説明します。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b3a66443394f5bfbe51b6685513281025d68fd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-purchasing-policies"></a><span data-ttu-id="e087f-103">購入ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="e087f-103">Create purchasing policies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e087f-104">この手順では、購買の業務プロセスに対応する購入ポリシーを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e087f-104">This procedure shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="e087f-105">購買ポリシーを作成する前に、購買ポリシー パラメーターを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e087f-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="e087f-106">購入ポリシーの作成、変更、無効は可能ですが、購入ポリシーの削除はできません。</span><span class="sxs-lookup"><span data-stu-id="e087f-106">It’s possible to create, modify, and retire a purchasing policy, but you can’t delete a purchasing policy.</span></span> <span data-ttu-id="e087f-107">通常、このタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="e087f-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="e087f-108">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="e087f-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="e087f-109">ポリシー パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="e087f-109">Set up policy parameters</span></span>
1. <span data-ttu-id="e087f-110">購入ポリシーを表示します。</span><span class="sxs-lookup"><span data-stu-id="e087f-110">Go to Purchasing policies.</span></span>
2. <span data-ttu-id="e087f-111">[パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e087f-111">Click Parameters.</span></span>
    * <span data-ttu-id="e087f-112">ポリシーの優先順位ルールは、組織内のさまざまなレベルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="e087f-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="e087f-113">表示される組織単位は、組織の階層に対応しており、その階層におけるレベルに応じて調達の内部統制についての目的が割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="e087f-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="e087f-114">たとえば組織内に法人、コスト センター、地域、部門があるかもしれませんが、これらの一部のみが調達の内部統制の階層についての目的を有しています。</span><span class="sxs-lookup"><span data-stu-id="e087f-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="e087f-115">既定として、「会社」タイプの組織が使用できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="e087f-116">[ポリシー ルール タイプ パラメーター] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e087f-116">Click the Policy rule type parameters tab.</span></span>
4. <span data-ttu-id="e087f-117">ツリーで、[購買ポリシー\購買請求コントロール ルール] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e087f-117">In the tree, select 'Purchasing policy\Purchase requisition control rule'.</span></span>
    * <span data-ttu-id="e087f-118">ポリシー レベルでポリシー解決の優先順位を定義します。</span><span class="sxs-lookup"><span data-stu-id="e087f-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="e087f-119">ただし、一部のポリシー タイプについては、個々のポリシー ルール タイプの優先順位を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="e087f-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="e087f-120">たとえば、コスト センター、部門、会社の順序で、購買ポリシーの優先順位を定義できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="e087f-121">カタログ ポリシー ルールでは、優先順位を、部門、コスト センター、会社の順序にされるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="e087f-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="e087f-122">カタログ ポリシー ルールについての優先順位を変更できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="e087f-123">作業者が要求を作成すると、表示されるカタログは、作業者部門と、そしてコスト センター、それから会社と関連付けられるポリシーによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="e087f-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker’s department, then their cost center, and then their company.</span></span>  
    * <span data-ttu-id="e087f-124">複数の組織レベルが一覧表示される場合、上/下方向の矢印を使用して [購買要求] の管理ルールの優先順位を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-124">If there’s more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="e087f-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e087f-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="e087f-126">新しいポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="e087f-126">Create a new policy</span></span>
1. <span data-ttu-id="e087f-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e087f-127">Click New.</span></span>
2. <span data-ttu-id="e087f-128">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e087f-128">In the Name field, type a value.</span></span>
3. <span data-ttu-id="e087f-129">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e087f-129">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e087f-130">1 つの購入ポリシーは、1 つの組織階層にのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="e087f-131">たとえば、「地理」という階層と「部門」という階層を設定できますが、それぞれに対して異なる購買ポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-131">For example, you could have one hierarchy called “Geographic” and one called “Department”, and have a different purchasing policy for each.</span></span>  
    * <span data-ttu-id="e087f-132">ポリシーを適用する組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="e087f-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="e087f-133">矢印をクリックして選択された組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="e087f-133">Click the arrow to add the selected organization.</span></span>
    * <span data-ttu-id="e087f-134">このプロセスを繰り返して、さらに組織を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="e087f-135">ポリシー ルールの追加</span><span class="sxs-lookup"><span data-stu-id="e087f-135">Add a policy rule</span></span>
1. <span data-ttu-id="e087f-136">ポリシー ルール タイプの一覧で、[請求目的のルール] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e087f-136">In the Policy rule type list, select Requisition purpose rule.</span></span>
    * <span data-ttu-id="e087f-137">請求の目的を既定で [消費] に設定しつつ、[補充タイプ] も選択できるようにルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="e087f-137">You’ll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="e087f-138">[ポリシー ルールの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e087f-138">Click Create policy rule.</span></span>
3. <span data-ttu-id="e087f-139">[手動での上書きを許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e087f-139">Select Yes in the Allow manual override field.</span></span>
4. <span data-ttu-id="e087f-140">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e087f-140">Click Close.</span></span>
    * <span data-ttu-id="e087f-141">次に、購入ポリシーの他のポリシー ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e087f-141">Now you can set up other policy rules for the purchasing policy.</span></span>   <span data-ttu-id="e087f-142">ポリシー ルール タイプでは、1 つの調達ポリシー内で同時に有効なルールを重複させることはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e087f-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  
5. <span data-ttu-id="e087f-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e087f-143">Close the page.</span></span>
6. <span data-ttu-id="e087f-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e087f-144">Close the page.</span></span>


