---
title: 原価オブジェクト コントローラーのアクセス権
description: このトピックでは、原価オブジェクト コント ローラーのアクセス権に関する情報を提供します。
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fa8faf0f0f45f901151b3b20a1792b3d8f264fa6
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897627"
---
# <a name="access-rights-for-cost-object-controllers"></a><span data-ttu-id="605ce-103">原価オブジェクト コントローラーのアクセス権</span><span class="sxs-lookup"><span data-stu-id="605ce-103">Access rights for cost object controllers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="605ce-104">**原価管理** ワークスペースは、マネージャーが原価オブジェクトのパフォーマンスを表示できる中心点です。</span><span class="sxs-lookup"><span data-stu-id="605ce-104">The **Cost control** workspace is a central point where managers can view the performance of their cost objects.</span></span> <span data-ttu-id="605ce-105">このワークスペースでは、マネージャーが原価経理担当者でない場合でも原価会計データを使用できます。</span><span class="sxs-lookup"><span data-stu-id="605ce-105">This workspace lets managers consume Cost accounting data even though they aren't cost accountants.</span></span> <span data-ttu-id="605ce-106">セキュリティ上の理由から、マネージャは自分が担当する特定の原価オブジェクトに関連付けられている原価計算データのみの参照が許可されます。</span><span class="sxs-lookup"><span data-stu-id="605ce-106">For security reasons, managers should be allowed to see only the Cost accounting data that is related to the specific cost objects that they are responsible for.</span></span>

<span data-ttu-id="605ce-107">原価計算には、次の 4 つの固有のロールがあります。</span><span class="sxs-lookup"><span data-stu-id="605ce-107">There are four unique roles in Cost accounting.</span></span>

| <span data-ttu-id="605ce-108">ロール名</span><span class="sxs-lookup"><span data-stu-id="605ce-108">Role name</span></span>               | <span data-ttu-id="605ce-109">ライセンス</span><span class="sxs-lookup"><span data-stu-id="605ce-109">License</span></span>      |
|-------------------------|--------------|
| <span data-ttu-id="605ce-110">原価会計マネージャー</span><span class="sxs-lookup"><span data-stu-id="605ce-110">Cost accounting manager</span></span> | <span data-ttu-id="605ce-111">活動</span><span class="sxs-lookup"><span data-stu-id="605ce-111">Activity</span></span>     |
| <span data-ttu-id="605ce-112">原価経理担当</span><span class="sxs-lookup"><span data-stu-id="605ce-112">Cost accountant</span></span>         | <span data-ttu-id="605ce-113">Operations</span><span class="sxs-lookup"><span data-stu-id="605ce-113">Operations</span></span>   |
| <span data-ttu-id="605ce-114">原価経理担当係</span><span class="sxs-lookup"><span data-stu-id="605ce-114">Cost accountant clerk</span></span>   | <span data-ttu-id="605ce-115">Operations</span><span class="sxs-lookup"><span data-stu-id="605ce-115">Operations</span></span>   |
| <span data-ttu-id="605ce-116">原価オブジェクト コントローラー</span><span class="sxs-lookup"><span data-stu-id="605ce-116">Cost object controller</span></span>  | <span data-ttu-id="605ce-117">チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="605ce-117">Team members</span></span> |

<span data-ttu-id="605ce-118">ここでは **原価オブジェクト コントローラー** ロールをマネージャーに割り当てる方法について説明します</span><span class="sxs-lookup"><span data-stu-id="605ce-118">This topic explains how to assign the **Cost object controller** role to a manager.</span></span>

<span data-ttu-id="605ce-119">**原価オブジェクト コントローラー** ロールがマネージャーに割り当てられると、マネージャーは次の作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="605ce-119">When the **Cost object controller** role is assigned to a manager, the manager can perform the following tasks:</span></span>

- <span data-ttu-id="605ce-120">**原価管理** ワークスペースにアクセス (クライアントで)。</span><span class="sxs-lookup"><span data-stu-id="605ce-120">Access the **Cost control** workspace (in the client).</span></span>

    - <span data-ttu-id="605ce-121">ドリルスルー経験をサポートするページへのドリルスルーおよび表示アクセス。</span><span class="sxs-lookup"><span data-stu-id="605ce-121">Drill through and have view access to the pages that support the drill-through experience.</span></span>

- <span data-ttu-id="605ce-122">**原価管理** ワークスペースにアクセス (モバイル アプリケーションで)。</span><span class="sxs-lookup"><span data-stu-id="605ce-122">Access the **Cost control** workspace (in the mobile application).</span></span>

> [!NOTE]
> <span data-ttu-id="605ce-123">**原価オブジェクト コントローラー** ロールは、ユーザーがどの原価オブジェクトへのアクセスや表示ができるかを制御しません。</span><span class="sxs-lookup"><span data-stu-id="605ce-123">The **Cost object controller** role doesn't control which cost objects the user can access and view data for.</span></span> <span data-ttu-id="605ce-124">行レベル セキュリティは、分析コード階層とアクセス リスト階層によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="605ce-124">Row-level security is provided via dimension hierarchies and the Access list hierarchy.</span></span>

## <a name="grant-access-rights"></a><span data-ttu-id="605ce-125">アクセス権の付与</span><span class="sxs-lookup"><span data-stu-id="605ce-125">Grant access rights</span></span>
<span data-ttu-id="605ce-126">次の例は、分析コード階層がどのように見えるかを示します。</span><span class="sxs-lookup"><span data-stu-id="605ce-126">The following example shows what a dimension hierarchy can look like.</span></span>

<span data-ttu-id="605ce-127">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="605ce-127">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="605ce-128">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="605ce-128">Dimension hierarchy name</span></span> | <span data-ttu-id="605ce-129">分析コード</span><span class="sxs-lookup"><span data-stu-id="605ce-129">Dimension</span></span>    | <span data-ttu-id="605ce-130">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="605ce-130">Dimension hierarchy type name</span></span>      | <span data-ttu-id="605ce-131">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="605ce-131">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="605ce-132">組織</span><span class="sxs-lookup"><span data-stu-id="605ce-132">Organization</span></span>             | <span data-ttu-id="605ce-133">コスト センター</span><span class="sxs-lookup"><span data-stu-id="605ce-133">Cost centers</span></span> | <span data-ttu-id="605ce-134">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="605ce-134">Dimension classification hierarchy</span></span> | <span data-ttu-id="605ce-135">**有**</span><span class="sxs-lookup"><span data-stu-id="605ce-135">**Yes**</span></span>               |

<span data-ttu-id="605ce-136">階層デザイナーの **ユーザー** クイック タブで、各ノードに 1 つまたは複数のユーザー ID を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="605ce-136">You can use the **Users** FastTab in the hierarchy designer to insert one or more user IDs on each node.</span></span>

|             <span data-ttu-id="605ce-137">ノード</span><span class="sxs-lookup"><span data-stu-id="605ce-137">Nodes</span></span>                 | <span data-ttu-id="605ce-138">ユーザー</span><span class="sxs-lookup"><span data-stu-id="605ce-138">Users</span></span>            | <span data-ttu-id="605ce-139">移動元分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="605ce-139">From dimension member</span></span>     |   <span data-ttu-id="605ce-140">移動先分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="605ce-140">To dimension member</span></span>   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="605ce-141">組織</span><span class="sxs-lookup"><span data-stu-id="605ce-141">Organization</span></span>                      | <span data-ttu-id="605ce-142">ベンジャミン、クレア</span><span class="sxs-lookup"><span data-stu-id="605ce-142">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="605ce-143">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="605ce-143">&nbsp;&nbsp;Admin</span></span>                 | <span data-ttu-id="605ce-144">4 月</span><span class="sxs-lookup"><span data-stu-id="605ce-144">April</span></span>            |                           |                         |
| <span data-ttu-id="605ce-145">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="605ce-145">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="605ce-146">アリシア</span><span class="sxs-lookup"><span data-stu-id="605ce-146">Alicia</span></span>           | <span data-ttu-id="605ce-147">CC002</span><span class="sxs-lookup"><span data-stu-id="605ce-147">CC002</span></span>                     | <span data-ttu-id="605ce-148">CC003</span><span class="sxs-lookup"><span data-stu-id="605ce-148">CC003</span></span>                   |
|                                   |                  | <span data-ttu-id="605ce-149">CC007</span><span class="sxs-lookup"><span data-stu-id="605ce-149">CC007</span></span>                     | <span data-ttu-id="605ce-150">CC007</span><span class="sxs-lookup"><span data-stu-id="605ce-150">CC007</span></span>                   |
| <span data-ttu-id="605ce-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="605ce-151">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="605ce-152">アーニー</span><span class="sxs-lookup"><span data-stu-id="605ce-152">Arnie</span></span>            | <span data-ttu-id="605ce-153">CC001</span><span class="sxs-lookup"><span data-stu-id="605ce-153">CC001</span></span>                     | <span data-ttu-id="605ce-154">CC001</span><span class="sxs-lookup"><span data-stu-id="605ce-154">CC001</span></span>                   |
| <span data-ttu-id="605ce-155">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="605ce-155">&nbsp;&nbsp;Production</span></span>            | <span data-ttu-id="605ce-156">デビッド</span><span class="sxs-lookup"><span data-stu-id="605ce-156">David</span></span>            |                           |                         |
| <span data-ttu-id="605ce-157">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="605ce-157">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="605ce-158">エレン</span><span class="sxs-lookup"><span data-stu-id="605ce-158">Ellen</span></span>            | <span data-ttu-id="605ce-159">CC005</span><span class="sxs-lookup"><span data-stu-id="605ce-159">CC005</span></span>                     | <span data-ttu-id="605ce-160">CC005</span><span class="sxs-lookup"><span data-stu-id="605ce-160">CC005</span></span>                   |
| <span data-ttu-id="605ce-161">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="605ce-161">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="605ce-162">クリス</span><span class="sxs-lookup"><span data-stu-id="605ce-162">Chris</span></span>            | <span data-ttu-id="605ce-163">CC006</span><span class="sxs-lookup"><span data-stu-id="605ce-163">CC006</span></span>                     | <span data-ttu-id="605ce-164">CC006</span><span class="sxs-lookup"><span data-stu-id="605ce-164">CC006</span></span>                   |

> [!NOTE]
> <span data-ttu-id="605ce-165">原価計算のすべてのエントリを表示できるように、原価経理担当者は階層の最上部に割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="605ce-165">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="605ce-166">アクセス リスト階層およびセキュリティ設定を適用する前に、**原価会計パラメーター** ページの **一般** タブにある **原価オブジェクト分析コード メンバーに対する表示アクセスの有効化** オプションを **はい** に設定する必要があります (**原価会計** > **設定** > **パラメータ**)。</span><span class="sxs-lookup"><span data-stu-id="605ce-166">Before the Access list hierarchy and its security settings can be applied, the **Enable view access for cost object dimension members** option must be set to **Yes** on the **General** tab of the **Cost accounting parameters** page (**Cost accounting** > **Setup** > **Parameters**).</span></span>

<span data-ttu-id="605ce-167">アクセス リスト階層の設定は、次の領域に表示されるデータを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="605ce-167">The settings for the Access list hierarchy are used to control the data that is shown in following areas:</span></span>

- <span data-ttu-id="605ce-168">**原価管理** ワークスペース (クライアント内):</span><span class="sxs-lookup"><span data-stu-id="605ce-168">**Cost control** workspace (in the client):</span></span>

    - <span data-ttu-id="605ce-169">ドリルスルーに使用されるページのデータ</span><span class="sxs-lookup"><span data-stu-id="605ce-169">Data on the pages that are used for drill-through</span></span>

- <span data-ttu-id="605ce-170">**原価管理** ワークスペース (モバイル アプリケーション内):</span><span class="sxs-lookup"><span data-stu-id="605ce-170">**Cost control** workspace (in the mobile application):</span></span>

    - <span data-ttu-id="605ce-171">カードの残高</span><span class="sxs-lookup"><span data-stu-id="605ce-171">Balances in cards</span></span>

- <span data-ttu-id="605ce-172">Microsoft Power BI:</span><span class="sxs-lookup"><span data-stu-id="605ce-172">Microsoft Power BI:</span></span>

    - <span data-ttu-id="605ce-173">Power BI ビジュアル化に表示されるデータ</span><span class="sxs-lookup"><span data-stu-id="605ce-173">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="605ce-174">Dynamics 365 Finance クライアントに埋め込まれた Power BI ビジュアル化データ</span><span class="sxs-lookup"><span data-stu-id="605ce-174">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="605ce-175">アクセス リスト階層が Power BI のデータに影響を及ぼす前に、アクセス リスト階層と Power BI の行レベルのセキュリティがペアリングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="605ce-175">Before the Access list hierarchy can affect data in Power BI, the Access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="605ce-176">詳細については、「[原価会計コンテンツ パックのセキュリティ設定](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="605ce-176">For more information, see [Set up security for Cost accounting content pack](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="605ce-177">このトピックでは、**原価管理** ワークスペースを使用するための前提条件を説明します。</span><span class="sxs-lookup"><span data-stu-id="605ce-177">This topic shows the prerequisites that must be in place before you can use the **Cost control** workspace.</span></span>

<span data-ttu-id="605ce-178">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="605ce-178">Additional resources</span></span>

- [<span data-ttu-id="605ce-179">原価管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="605ce-179">Cost control workspace</span></span>](cost-control-workspace.md)
- [<span data-ttu-id="605ce-180">分析コード階層</span><span class="sxs-lookup"><span data-stu-id="605ce-180">Dimension hierarchy</span></span>](dimension-hierarchy.md)
- [<span data-ttu-id="605ce-181">原価会計コンテンツ パックのセキュリティ設定</span><span class="sxs-lookup"><span data-stu-id="605ce-181">Set up security for Cost accounting content pack</span></span>](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
