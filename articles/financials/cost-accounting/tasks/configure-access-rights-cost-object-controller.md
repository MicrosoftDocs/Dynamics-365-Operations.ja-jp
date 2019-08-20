---
title: 原価オブジェクト コントローラーのアクセス権のコンフィギュレーション
description: この手順を使用して、コスト オブジェクト コントローラーのアクセス権を設定します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b7356706ea80c97fdf5b73faf32134a4aebacbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841444"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="e8c66-103">原価オブジェクト コントローラーのアクセス権のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8c66-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8c66-104">この手順を使用して、コスト オブジェクト コントローラーのアクセス権を設定します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="e8c66-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="e8c66-106">原価オブジェクト コントローラー ロールを割り当て</span><span class="sxs-lookup"><span data-stu-id="e8c66-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="e8c66-107">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e8c66-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="e8c66-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e8c66-109">たとえば、「アリシア」の値で [ユーザー名] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="e8c66-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e8c66-111">[ロールの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-111">Click Assign roles.</span></span>
5. <span data-ttu-id="e8c66-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e8c66-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="e8c66-114">リスト セキュリティのアクセスを有効</span><span class="sxs-lookup"><span data-stu-id="e8c66-114">Enable access list security</span></span>
1. <span data-ttu-id="e8c66-115">[原価会計] > [分析コード] > [分析コード階層] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="e8c66-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e8c66-117">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-117">Select Organization.</span></span>  
3. <span data-ttu-id="e8c66-118">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-118">Click Edit.</span></span>
4. <span data-ttu-id="e8c66-119">[アクセス リスト階層] のフィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="e8c66-120">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="e8c66-121">ユーザーへのアクセス権を割り当て</span><span class="sxs-lookup"><span data-stu-id="e8c66-121">Assign access rights to user</span></span>
1. <span data-ttu-id="e8c66-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-122">Click New.</span></span>
2. <span data-ttu-id="e8c66-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e8c66-124">[ユーザー ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="e8c66-125">[管理者] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-125">Select Admin.</span></span>  
4. <span data-ttu-id="e8c66-126">ツリーで、「組織\CEO\CFO\FIM」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="e8c66-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-127">Click New.</span></span>
6. <span data-ttu-id="e8c66-128">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e8c66-129">[ユーザー ID] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="e8c66-130">[アリシア] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-130">Select Alicia.</span></span>  
8. <span data-ttu-id="e8c66-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="e8c66-132">原価会計のアクセス権を有効化</span><span class="sxs-lookup"><span data-stu-id="e8c66-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="e8c66-133">[原価会計] > [設定] > [パラメーター] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="e8c66-134">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-134">Click the General tab.</span></span>
3. <span data-ttu-id="e8c66-135">原価オブジェクト分析コード メンバー フィールドに対する [表示アクセスの有効化] で、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="e8c66-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-136">Click Save.</span></span>
5. <span data-ttu-id="e8c66-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e8c66-137">Close the page.</span></span>
6. <span data-ttu-id="e8c66-138">[原価会計] > [設定] > [原価管理ワークスペース コンフィギュレーション] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="e8c66-139">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-139">Click Edit.</span></span>
8. <span data-ttu-id="e8c66-140">[公開済] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e8c66-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="e8c66-141">[はい] を選択すると、次の 4 つのロールのいずれかに割り当てられているユーザーは、原価管理ワークスペースでレポートを確認できます: 原価会計マネージャー、原価経理担当、原価経理担当係および原価オブジェクト コントローラー。</span><span class="sxs-lookup"><span data-stu-id="e8c66-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="e8c66-142">[いいえ] を選択すると、次のロールのいずれかに割り当てられているユーザーのみが、レポートを確認できます: 原価会計マネージャー、原価経理担当、および原価経理担当係。</span><span class="sxs-lookup"><span data-stu-id="e8c66-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="e8c66-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e8c66-143">Click Save.</span></span>

