---
title: 原価オブジェクト コントローラーのアクセス権の定義
description: このトピックでは、原価オブジェクト コント ローラーのアクセス権に関する情報を提供します。
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 290b16eeb99ac7ddb9b552b289215c99a0451660
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565912"
---
# <a name="access-rights-of-a-cost-object-controller"></a><span data-ttu-id="04d9c-103">原価オブジェクト コントローラーのアクセス権</span><span class="sxs-lookup"><span data-stu-id="04d9c-103">Access rights of a cost object controller</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04d9c-104">**原価管理**ワークスペースは、マネージャーが原価オブジェクトのパフォーマンスを表示できる中心点です。</span><span class="sxs-lookup"><span data-stu-id="04d9c-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="04d9c-105">このワークスペースでは、マネージャーが原価経理担当者でない場合でも原価会計データを使用できます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="04d9c-106">セキュリティ上の理由から、マネージャは自分が担当する特定の原価オブジェクトに関連付けられている原価計算データのみの参照が許可されます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="04d9c-107">原価計算には、次の 4 つの固有のロールがあります。</span><span class="sxs-lookup"><span data-stu-id="04d9c-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="04d9c-108">ロール名</span><span class="sxs-lookup"><span data-stu-id="04d9c-108">Role name</span></span>               | <span data-ttu-id="04d9c-109">ライセンス</span><span class="sxs-lookup"><span data-stu-id="04d9c-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="04d9c-110">原価会計マネージャー</span><span class="sxs-lookup"><span data-stu-id="04d9c-110">Cost accounting manager</span></span> | <span data-ttu-id="04d9c-111">活動</span><span class="sxs-lookup"><span data-stu-id="04d9c-111">Activity</span></span>     |
| <span data-ttu-id="04d9c-112">原価経理担当</span><span class="sxs-lookup"><span data-stu-id="04d9c-112">Cost accountant</span></span>         | <span data-ttu-id="04d9c-113">Operations</span><span class="sxs-lookup"><span data-stu-id="04d9c-113">Operations</span></span>   |
| <span data-ttu-id="04d9c-114">原価経理担当係</span><span class="sxs-lookup"><span data-stu-id="04d9c-114">Cost accountant clerk</span></span>   | <span data-ttu-id="04d9c-115">Operations</span><span class="sxs-lookup"><span data-stu-id="04d9c-115">Operations</span></span>   |
| <span data-ttu-id="04d9c-116">原価オブジェクト コントローラー</span><span class="sxs-lookup"><span data-stu-id="04d9c-116">Cost object controller</span></span>  | <span data-ttu-id="04d9c-117">チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="04d9c-117">Team members</span></span> |

<span data-ttu-id="04d9c-118">ここでは**原価オブジェクト コントローラー** ロールをマネージャーに割り当てる方法について説明します</span><span class="sxs-lookup"><span data-stu-id="04d9c-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="04d9c-119">**原価オブジェクト コントローラー** ロールがマネージャーに割り当てられると、マネージャーは次の作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="04d9c-120">**原価管理**ワークスペースにアクセス (クライアントで)。</span><span class="sxs-lookup"><span data-stu-id="04d9c-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="04d9c-121">ドリルスルー経験をサポートするページへのドリルスルーおよび表示アクセス。</span><span class="sxs-lookup"><span data-stu-id="04d9c-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="04d9c-122">**原価管理**ワークスペースにアクセス (モバイル アプリケーションで)。</span><span class="sxs-lookup"><span data-stu-id="04d9c-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="04d9c-123">**原価オブジェクト コントローラー**ロールは、ユーザーがどの原価オブジェクトへのアクセスや表示ができるかを制御しません。</span><span class="sxs-lookup"><span data-stu-id="04d9c-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="04d9c-124">行レベル セキュリティは、分析コード階層とアクセス リスト階層によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="04d9c-125">アクセス権の付与</span><span class="sxs-lookup"><span data-stu-id="04d9c-125">Grant access rights</span></span>
<span data-ttu-id="04d9c-126">次の例は、分析コード階層がどのように見えるかを示します。</span><span class="sxs-lookup"><span data-stu-id="04d9c-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="04d9c-127">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="04d9c-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="04d9c-128">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="04d9c-128">Dimension hierarchy name</span></span> | <span data-ttu-id="04d9c-129">分析コード</span><span class="sxs-lookup"><span data-stu-id="04d9c-129">Dimension</span></span>    | <span data-ttu-id="04d9c-130">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="04d9c-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="04d9c-131">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="04d9c-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="04d9c-132">組織</span><span class="sxs-lookup"><span data-stu-id="04d9c-132">Organization</span></span>             | <span data-ttu-id="04d9c-133">コスト センター</span><span class="sxs-lookup"><span data-stu-id="04d9c-133">Cost centers</span></span> | <span data-ttu-id="04d9c-134">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="04d9c-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="04d9c-135">**有**</span><span class="sxs-lookup"><span data-stu-id="04d9c-135">**Yes**</span></span>               |

<span data-ttu-id="04d9c-136">階層デザイナーの**ユーザー**クイック タブで、各ノードに 1 つまたは複数のユーザー ID を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|                                   | <span data-ttu-id="04d9c-137">ユーザー</span><span class="sxs-lookup"><span data-stu-id="04d9c-137">Users</span></span>            | <span data-ttu-id="04d9c-138">分析コード メンバーの範囲</span><span class="sxs-lookup"><span data-stu-id="04d9c-138">Dimension member ranges</span></span>   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="04d9c-139">**ノード**</span><span class="sxs-lookup"><span data-stu-id="04d9c-139">**Nodes**</span></span>                         | <span data-ttu-id="04d9c-140">**ユーザー ID**</span><span class="sxs-lookup"><span data-stu-id="04d9c-140">**User ID**</span></span>      | <span data-ttu-id="04d9c-141">**移動元分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="04d9c-141">**From dimension member**</span></span> | <span data-ttu-id="04d9c-142">**移動先分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="04d9c-142">**To dimension member**</span></span> |
| <span data-ttu-id="04d9c-143">組織</span><span class="sxs-lookup"><span data-stu-id="04d9c-143">Organization</span></span>                      | <span data-ttu-id="04d9c-144">ベンジャミン、クレア</span><span class="sxs-lookup"><span data-stu-id="04d9c-144">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="04d9c-145">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="04d9c-145">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="04d9c-146">4 月</span><span class="sxs-lookup"><span data-stu-id="04d9c-146">April</span></span>            |                           |                         |
| <span data-ttu-id="04d9c-147">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="04d9c-147">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="04d9c-148">アリシア</span><span class="sxs-lookup"><span data-stu-id="04d9c-148">Alicia</span></span>           | <span data-ttu-id="04d9c-149">CC002</span><span class="sxs-lookup"><span data-stu-id="04d9c-149">CC002</span></span>                     | <span data-ttu-id="04d9c-150">CC003</span><span class="sxs-lookup"><span data-stu-id="04d9c-150">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="04d9c-151">CC007</span><span class="sxs-lookup"><span data-stu-id="04d9c-151">CC007</span></span>                     | <span data-ttu-id="04d9c-152">CC007</span><span class="sxs-lookup"><span data-stu-id="04d9c-152">CC007</span></span>                   |
| <span data-ttu-id="04d9c-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="04d9c-153">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="04d9c-154">アーニー</span><span class="sxs-lookup"><span data-stu-id="04d9c-154">Arnie</span></span>            | <span data-ttu-id="04d9c-155">CC001</span><span class="sxs-lookup"><span data-stu-id="04d9c-155">CC001</span></span>                     | <span data-ttu-id="04d9c-156">CC001</span><span class="sxs-lookup"><span data-stu-id="04d9c-156">CC001</span></span>                   |
| <span data-ttu-id="04d9c-157">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="04d9c-157">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="04d9c-158">デビッド</span><span class="sxs-lookup"><span data-stu-id="04d9c-158">David</span></span>            |                           |                         |
| <span data-ttu-id="04d9c-159">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="04d9c-159">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="04d9c-160">エレン</span><span class="sxs-lookup"><span data-stu-id="04d9c-160">Ellen</span></span>            | <span data-ttu-id="04d9c-161">CC005</span><span class="sxs-lookup"><span data-stu-id="04d9c-161">CC005</span></span>                     | <span data-ttu-id="04d9c-162">CC005</span><span class="sxs-lookup"><span data-stu-id="04d9c-162">CC005</span></span>                   |
| <span data-ttu-id="04d9c-163">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="04d9c-163">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="04d9c-164">クリス</span><span class="sxs-lookup"><span data-stu-id="04d9c-164">Chris</span></span>            | <span data-ttu-id="04d9c-165">CC006</span><span class="sxs-lookup"><span data-stu-id="04d9c-165">CC006</span></span>                     | <span data-ttu-id="04d9c-166">CC006</span><span class="sxs-lookup"><span data-stu-id="04d9c-166">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="04d9c-167">原価計算のすべてのエントリを表示できるように、原価経理担当者は階層の最上部に割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="04d9c-167">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="04d9c-168">アクセス リスト階層およびセキュリティ設定を適用する前に、**原価会計パラメーター**ページの**一般**タブにある**原価オブジェクト分析コード メンバーに対する表示アクセスの有効化**オプションを**はい**に設定する必要があります (**原価会計** > **設定** > **パラメータ**)。</span><span class="sxs-lookup"><span data-stu-id="04d9c-168">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="04d9c-169">アクセス リスト階層の設定は、次の領域に表示されるデータを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="04d9c-169">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="04d9c-170">**原価管理**ワークスペース (クライアント内):</span><span class="sxs-lookup"><span data-stu-id="04d9c-170">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="04d9c-171">ドリルスルーに使用されるページのデータ</span><span class="sxs-lookup"><span data-stu-id="04d9c-171">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="04d9c-172">**原価管理**ワークスペース (モバイル アプリケーション内):</span><span class="sxs-lookup"><span data-stu-id="04d9c-172">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="04d9c-173">カードの残高</span><span class="sxs-lookup"><span data-stu-id="04d9c-173">Balances in cards</span></span>

- <span data-ttu-id="04d9c-174">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="04d9c-174">Microsoft Power BI:</span></span>

    - <span data-ttu-id="04d9c-175">Power BI ビジュアル化に表示されるデータ</span><span class="sxs-lookup"><span data-stu-id="04d9c-175">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="04d9c-176">Microsoft Dynamics 365 for Finance and Operations クライアントに埋め込まれた Power BI ビジュアル化データ</span><span class="sxs-lookup"><span data-stu-id="04d9c-176">Data Power BI visualizations that are embedded in the Microsoft Dynamics 365 for Finance and Operations, client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="04d9c-177">アクセス リスト階層が Power BI のデータに影響を及ぼす前に、アクセス リスト階層と Power BI の行レベルのセキュリティがペアリングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="04d9c-177">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="04d9c-178">詳細については、「[原価会計コンテンツ パックのセキュリティ設定](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04d9c-178">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="04d9c-179">このトピックでは、**原価管理**ワークスペースを使用するための前提条件を説明します。</span><span class="sxs-lookup"><span data-stu-id="04d9c-179">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="04d9c-180">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="04d9c-180">Additional resources</span></span>

- [<span data-ttu-id="04d9c-181">原価管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="04d9c-181">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="04d9c-182">分析コード階層</span><span class="sxs-lookup"><span data-stu-id="04d9c-182">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="04d9c-183">原価会計コンテンツ パックのセキュリティ設定</span><span class="sxs-lookup"><span data-stu-id="04d9c-183">Set up security for Cost accounting content pack</span></span>](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)
