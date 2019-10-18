---
title: 分析コード階層
description: このトピックでは、分析コード階層について説明します。 分析コード階層を使用して、原価会計のレポート構造、コスト ポリシー、およびセキュリティ設定を定義します。
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54c00718c344b55794fb4a5de9419b81ec82ad47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187938"
---
# <a name="dimension-hierarchy"></a><span data-ttu-id="2bac4-104">分析コード階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-104">Dimension hierarchy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bac4-105">このトピックでは、分析コード階層について説明します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-105">This topic provides information about dimension hierarchies.</span></span> <span data-ttu-id="2bac4-106">分析コード階層を使用して、原価会計のレポート構造、コスト ポリシー、およびセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-106">You use a dimension hierarchy to define the reporting structure, cost policies, and security setup in Cost accounting.</span></span>  

## <a name="overview"></a><span data-ttu-id="2bac4-107">概要</span><span class="sxs-lookup"><span data-stu-id="2bac4-107">Overview</span></span>

<span data-ttu-id="2bac4-108">分析コード階層は、原価会計のさまざまな場所で使用します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-108">Dimension hierarchies are used in various places in Cost accounting.</span></span> <span data-ttu-id="2bac4-109">分析コード階層を使用して、次の情報を定義できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-109">A dimension hierarchy lets you define the following information:</span></span>

-  <span data-ttu-id="2bac4-110">組織の要件に適合するレポート構造</span><span class="sxs-lookup"><span data-stu-id="2bac4-110">The reporting structure that fits into the organization's requirements</span></span>
-  <span data-ttu-id="2bac4-111">コスト ポリシー</span><span class="sxs-lookup"><span data-stu-id="2bac4-111">Cost policies</span></span>
-  <span data-ttu-id="2bac4-112">セキュリティ設定</span><span class="sxs-lookup"><span data-stu-id="2bac4-112">The security setup</span></span>

<span data-ttu-id="2bac4-113">分析コード階層の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-113">Here is an example of a dimension hierarchy.</span></span>

![分析コード階層の例](./media/dimension-hierarchy.png)

<span data-ttu-id="2bac4-115">次のタイプの分析コードに対して分析コード階層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-115">A dimension hierarchy can be created for the following types of dimensions:</span></span>

-  <span data-ttu-id="2bac4-116">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-116">Cost element dimensions</span></span>
-  <span data-ttu-id="2bac4-117">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-117">Cost object dimensions</span></span>
-  <span data-ttu-id="2bac4-118">統計分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-118">Statistical dimensions</span></span>

> [!NOTE]
> - <span data-ttu-id="2bac4-119">異なる分析視点が必要な場合は、同じ分析コードに対して複数の分析コード階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-119">You can create multiple dimension hierarchies for the same dimension if different perspectives are required.</span></span>
> - <span data-ttu-id="2bac4-120">分析コード階層は、1 つの分析コードにのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-120">A dimension hierarchy can be associated with only one dimension.</span></span>
> - <span data-ttu-id="2bac4-121">分析コード階層は構造内に無制限にレベルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-121">A dimension hierarchy can have unlimited levels in its structure.</span></span> <span data-ttu-id="2bac4-122">すべてのレベルは **原価管理** ワークスペースで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-122">All the levels will be available in the **Cost control** workspace.</span></span> <span data-ttu-id="2bac4-123">レポート用に Microsoft Excel または Microsoft Power BI を使用する場合は、分析コード階層の最初の 15 レベルのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-123">When you use Microsoft Excel or Microsoft Power BI for reporting purposes, only the first 15 levels of the dimension hierarchy are exported.</span></span> <span data-ttu-id="2bac4-124">この制限があるのは、Excel も Power BI も固定スキーマを必要とするためです。</span><span class="sxs-lookup"><span data-stu-id="2bac4-124">This limitation exists because both Excel and Power BI require a fixed schema.</span></span>
> - <span data-ttu-id="2bac4-125">分析コード階層は、日付に対して有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-125">A dimension hierarchy isn't date-effective.</span></span> <span data-ttu-id="2bac4-126">このため、分析コード階層への変更は直ちにレコードに保存され、日付前と日付後を比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-126">Therefore, any change to a dimension hierarchy is immediately saved to the record, and you can't compare the before date and after date.</span></span>

## <a name="dimension-hierarchy-type"></a><span data-ttu-id="2bac4-127">分析コード階層タイプ</span><span class="sxs-lookup"><span data-stu-id="2bac4-127">Dimension hierarchy type</span></span>

<span data-ttu-id="2bac4-128">新しい分析コード階層を作成する際には、階層タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-128">When you create a new dimension hierarchy, you must select a hierarchy type.</span></span> <span data-ttu-id="2bac4-129">**原価会計** > **分析コード** > **分析コード階層**に移動します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-129">Go to **Cost accounting** > **Dimensions** > **Dimension hierarchies**.</span></span> <span data-ttu-id="2bac4-130">**新規**をクリックし、分析コード階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-130">Click **New**, and select a dimension hierarchy type.</span></span> <span data-ttu-id="2bac4-131">**分析コード カテゴリ階層**または**分析コード分類階層**のいずれかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-131">You can select either **Dimension categorization hierarchy** or **Dimension classification hierarchy**.</span></span>

### <a name="dimension-categorization-hierarchy"></a><span data-ttu-id="2bac4-132">分析コード カテゴリ階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-132">Dimension categorization hierarchy</span></span>

<span data-ttu-id="2bac4-133">**分析コードカテゴリ階層**タイプはレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-133">The **Dimension categorization hierarchy** type is used for reporting purposes.</span></span> <span data-ttu-id="2bac4-134">コスト要素分析コードのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2bac4-134">It supports only the cost element dimensions.</span></span> <span data-ttu-id="2bac4-135">このタイプを選択する場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-135">When you select this type, the following rules apply:</span></span>

-  <span data-ttu-id="2bac4-136">分析コード メンバーは、階層構造に複数回関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-136">A dimension member can be associated more than one time in the hierarchy structure.</span></span>
-  <span data-ttu-id="2bac4-137">コスト動作をリーフ ノードに割り当てることにより、さまざまなノードにコスト要素分析コード メンバーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-137">You can put a cost element dimension member in different nodes by assigning a cost behavior to the leaf node.</span></span>

### <a name="dimension-classification-hierarchy"></a><span data-ttu-id="2bac4-138">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-138">Dimension classification hierarchy</span></span>

<span data-ttu-id="2bac4-139">**分析コード分類階層**タイプはルールの定義、およびレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-139">The **Dimension classification hierarchy** type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="2bac4-140">コスト オブジェクト、コスト要素、および統計分析コードなどのすべての分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2bac4-140">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span> <span data-ttu-id="2bac4-141">このタイプを選択する場合は、分析コード メンバーは階層構造に 1 回のみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-141">When you select this type, a dimension member can be associated only one time in the hierarchy structure.</span></span>

## <a name="create-and-maintain-a-dimension-hierarchy"></a><span data-ttu-id="2bac4-142">分析コード階層の作成と管理</span><span class="sxs-lookup"><span data-stu-id="2bac4-142">Create and maintain a dimension hierarchy</span></span>

<span data-ttu-id="2bac4-143">分析コード階層は、ノードとリーフ ノードのリレーションシップを持つツリー構造として作成されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-143">A dimension hierarchy is created as a tree structure that has node and leaf node relationships.</span></span>

-  <span data-ttu-id="2bac4-144">ノードは 1:_n_ サブノードを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-144">A node can have 1:_n_ subnodes.</span></span>
-  <span data-ttu-id="2bac4-145">ノードはサブノードとそれに割り当てられたリーフ ノードの両方を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-145">A node can’t have both subnodes and leaf nodes assigned to it.</span></span>
-  <span data-ttu-id="2bac4-146">リーフ ノードは、階層の最下位レベルでのみ割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-146">A leaf node can be assigned only at the lowest level in the hierarchy.</span></span>

### <a name="example"></a><span data-ttu-id="2bac4-147">例</span><span class="sxs-lookup"><span data-stu-id="2bac4-147">Example</span></span>

<span data-ttu-id="2bac4-148">小規模の会社が次の組織構造を持っています。「財務」および「人事管理」は「管理」の下にある部署、また「組み立て」および「梱包業」は「生産」の下にある部署です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-148">A small company has the following organization structure, where Finance and Human resources are departments under Admin, and Assembly and Packaging are departments under Production.</span></span>

![組織構造の例](./media/dimension-hierarchy-org.png)

<span data-ttu-id="2bac4-150">コスト オブジェクト分析コードは、組織内のすべてのコスト センターを表します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-150">A cost object dimension represents all the cost centers in the organization.</span></span>

- <span data-ttu-id="2bac4-151">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-151">Cost object dimension</span></span>
    - <span data-ttu-id="2bac4-152">コスト センター</span><span class="sxs-lookup"><span data-stu-id="2bac4-152">Cost centers</span></span>

<span data-ttu-id="2bac4-153">すべてのコスト センターを表すコスト オブジェクト分析コードは以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-153">The cost object dimension that represents all the cost centers can be set up as shown here.</span></span>

| <span data-ttu-id="2bac4-154">コスト センター</span><span class="sxs-lookup"><span data-stu-id="2bac4-154">Cost centers</span></span> | <span data-ttu-id="2bac4-155">説明</span><span class="sxs-lookup"><span data-stu-id="2bac4-155">Description</span></span> |
|--------------|-------------|
| <span data-ttu-id="2bac4-156">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-156">CC001</span></span>        | <span data-ttu-id="2bac4-157">HR</span><span class="sxs-lookup"><span data-stu-id="2bac4-157">HR</span></span>          |
| <span data-ttu-id="2bac4-158">CC002</span><span class="sxs-lookup"><span data-stu-id="2bac4-158">CC002</span></span>        | <span data-ttu-id="2bac4-159">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-159">Finance</span></span>     |
| <span data-ttu-id="2bac4-160">CC003</span><span class="sxs-lookup"><span data-stu-id="2bac4-160">CC003</span></span>        | <span data-ttu-id="2bac4-161">税申告</span><span class="sxs-lookup"><span data-stu-id="2bac4-161">Tax</span></span>         |
| <span data-ttu-id="2bac4-162">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-162">CC007</span></span>        | <span data-ttu-id="2bac4-163">AR/AP</span><span class="sxs-lookup"><span data-stu-id="2bac4-163">AR/AP</span></span>       |
| <span data-ttu-id="2bac4-164">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-164">CC005</span></span>        | <span data-ttu-id="2bac4-165">組み立て</span><span class="sxs-lookup"><span data-stu-id="2bac4-165">Assembly</span></span>    |
| <span data-ttu-id="2bac4-166">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-166">CC006</span></span>        | <span data-ttu-id="2bac4-167">梱包業</span><span class="sxs-lookup"><span data-stu-id="2bac4-167">Packaging</span></span>   |

<span data-ttu-id="2bac4-168">コスト要素分析コードは、組織内のすべてのコスト要素を表します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-168">A cost element dimension represents all the cost elements in the organization.</span></span>

- <span data-ttu-id="2bac4-169">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-169">Cost element dimension</span></span>
    - <span data-ttu-id="2bac4-170">コスト要素</span><span class="sxs-lookup"><span data-stu-id="2bac4-170">Cost elements</span></span>

<span data-ttu-id="2bac4-171">すべてのコスト要素を表すコスト要素分析コードは以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-171">The cost element dimension that represents all the cost elements can be set up as shown here.</span></span>

| <span data-ttu-id="2bac4-172">コスト要素</span><span class="sxs-lookup"><span data-stu-id="2bac4-172">Cost elements</span></span> | <span data-ttu-id="2bac4-173">説明</span><span class="sxs-lookup"><span data-stu-id="2bac4-173">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="2bac4-174">10001</span><span class="sxs-lookup"><span data-stu-id="2bac4-174">10001</span></span>         | <span data-ttu-id="2bac4-175">電気</span><span class="sxs-lookup"><span data-stu-id="2bac4-175">Electricity</span></span> |
| <span data-ttu-id="2bac4-176">10010</span><span class="sxs-lookup"><span data-stu-id="2bac4-176">10010</span></span>         | <span data-ttu-id="2bac4-177">クリーニング</span><span class="sxs-lookup"><span data-stu-id="2bac4-177">Cleaning</span></span>    |
| <span data-ttu-id="2bac4-178">10011</span><span class="sxs-lookup"><span data-stu-id="2bac4-178">10011</span></span>         | <span data-ttu-id="2bac4-179">暖房</span><span class="sxs-lookup"><span data-stu-id="2bac4-179">Heating</span></span>     |
| <span data-ttu-id="2bac4-180">40001</span><span class="sxs-lookup"><span data-stu-id="2bac4-180">40001</span></span>         | <span data-ttu-id="2bac4-181">COGS</span><span class="sxs-lookup"><span data-stu-id="2bac4-181">COGS</span></span>        |

<span data-ttu-id="2bac4-182">組織のレポート要件を満たす分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-182">A dimension hierarchy that meets the organizational reporting requirements can be set up as shown here.</span></span>

<span data-ttu-id="2bac4-183">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="2bac4-183">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="2bac4-184">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="2bac4-184">Dimension hierarchy name</span></span> | <span data-ttu-id="2bac4-185">分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-185">Dimension</span></span>    | <span data-ttu-id="2bac4-186">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="2bac4-186">Dimension hierarchy type name</span></span>      | <span data-ttu-id="2bac4-187">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-187">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="2bac4-188">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-188">Organization</span></span>             | <span data-ttu-id="2bac4-189">コスト センター</span><span class="sxs-lookup"><span data-stu-id="2bac4-189">Cost centers</span></span> | <span data-ttu-id="2bac4-190">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-190">Dimension classification hierarchy</span></span> | <span data-ttu-id="2bac4-191">無</span><span class="sxs-lookup"><span data-stu-id="2bac4-191">No</span></span>                    |

<span data-ttu-id="2bac4-192">レポートの分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-192">The dimension hierarchy for reporting can be set up as shown here.</span></span>

|                   | <span data-ttu-id="2bac4-193">分析コード メンバーの範囲</span><span class="sxs-lookup"><span data-stu-id="2bac4-193">Dimension member ranges</span></span>   |                         |
|-------------------|---------------------------|-------------------------|
| <span data-ttu-id="2bac4-194">**ノード**</span><span class="sxs-lookup"><span data-stu-id="2bac4-194">**Nodes**</span></span>         | <span data-ttu-id="2bac4-195">**移動元分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-195">**From dimension member**</span></span> | <span data-ttu-id="2bac4-196">**移動先分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-196">**To dimension member**</span></span> |
| <span data-ttu-id="2bac4-197">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-197">Organization</span></span>      |                           |                         |
| <span data-ttu-id="2bac4-198">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-198">&nbsp;&nbsp;Admin</span></span>         |                           |                         |
|<span data-ttu-id="2bac4-199">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-199">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="2bac4-200">CC002</span><span class="sxs-lookup"><span data-stu-id="2bac4-200">CC002</span></span>                     | <span data-ttu-id="2bac4-201">CC003</span><span class="sxs-lookup"><span data-stu-id="2bac4-201">CC003</span></span>                   |
|                   | <span data-ttu-id="2bac4-202">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-202">CC007</span></span>                     | <span data-ttu-id="2bac4-203">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-203">CC007</span></span>                   |
| <span data-ttu-id="2bac4-204">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="2bac4-204">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="2bac4-205">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-205">CC001</span></span>                     | <span data-ttu-id="2bac4-206">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-206">CC001</span></span>                   |
| <span data-ttu-id="2bac4-207">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="2bac4-207">&nbsp;&nbsp;Production</span></span>    |                           |                         |
| <span data-ttu-id="2bac4-208">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="2bac4-208">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="2bac4-209">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-209">CC005</span></span>                     | <span data-ttu-id="2bac4-210">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-210">CC005</span></span>                   |
| <span data-ttu-id="2bac4-211">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="2bac4-211">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="2bac4-212">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-212">CC006</span></span>                     | <span data-ttu-id="2bac4-213">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-213">CC006</span></span>                   |

<span data-ttu-id="2bac4-214">ポリシー要件を満たす分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-214">A dimension hierarchy that meets the policy requirement can be set up as shown here.</span></span>

<span data-ttu-id="2bac4-215">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="2bac4-215">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="2bac4-216">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="2bac4-216">Dimension hierarchy name</span></span> | <span data-ttu-id="2bac4-217">分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-217">Dimension</span></span>     | <span data-ttu-id="2bac4-218">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="2bac4-218">Dimension hierarchy type name</span></span>      |
|--------------------------|---------------|------------------------------------|
| <span data-ttu-id="2bac4-219">原価動作</span><span class="sxs-lookup"><span data-stu-id="2bac4-219">Cost behavior</span></span>            | <span data-ttu-id="2bac4-220">コスト要素</span><span class="sxs-lookup"><span data-stu-id="2bac4-220">Cost elements</span></span> | <span data-ttu-id="2bac4-221">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-221">Dimension classification hierarchy</span></span> |

<span data-ttu-id="2bac4-222">ポリシーの分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-222">The dimension hierarchy for the policy can be set up as shown here.</span></span>

|                   | <span data-ttu-id="2bac4-223">分析コード メンバーの範囲</span><span class="sxs-lookup"><span data-stu-id="2bac4-223">Dimension member ranges</span></span>   |                         |
|-------------------|---------------------------|-------------------------|
| <span data-ttu-id="2bac4-224">**ノード**</span><span class="sxs-lookup"><span data-stu-id="2bac4-224">**Nodes**</span></span>         | <span data-ttu-id="2bac4-225">**移動元分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-225">**From dimension member**</span></span> | <span data-ttu-id="2bac4-226">**移動先分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-226">**To dimension member**</span></span> |
| <span data-ttu-id="2bac4-227">原価動作</span><span class="sxs-lookup"><span data-stu-id="2bac4-227">Cost behavior</span></span>     |                           |                         |
| <span data-ttu-id="2bac4-228">&nbsp;&nbsp;固定費</span><span class="sxs-lookup"><span data-stu-id="2bac4-228">&nbsp;&nbsp;Fixed cost</span></span>    | <span data-ttu-id="2bac4-229">10001</span><span class="sxs-lookup"><span data-stu-id="2bac4-229">10001</span></span>                     | <span data-ttu-id="2bac4-230">10011</span><span class="sxs-lookup"><span data-stu-id="2bac4-230">10011</span></span>                   |
|<span data-ttu-id="2bac4-231">&nbsp;&nbsp;変動費</span><span class="sxs-lookup"><span data-stu-id="2bac4-231">&nbsp;&nbsp;Variable cost</span></span> | <span data-ttu-id="2bac4-232">40001</span><span class="sxs-lookup"><span data-stu-id="2bac4-232">40001</span></span>                     | <span data-ttu-id="2bac4-233">40010</span><span class="sxs-lookup"><span data-stu-id="2bac4-233">40010</span></span>                   |

> [!NOTE]
> <span data-ttu-id="2bac4-234">**分析コード メンバーの範囲**で、ノードは 1:_n_ 分析コード メンバーの範囲を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-234">Under **Dimension member ranges**, a node can contain 1:_n_ dimension member ranges.</span></span> <span data-ttu-id="2bac4-235">分析コード メンバとしてまだ存在していない分析コード メンバー ID を挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-235">You can insert dimension member IDs that don’t yet exist as dimension members.</span></span> <span data-ttu-id="2bac4-236">この方法により、階層が今後弾力性のあるものになります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-236">This approach makes the hierarchy resilient for the future.</span></span>  

### <a name="copy-a-hierarchy"></a><span data-ttu-id="2bac4-237">階層のコピー</span><span class="sxs-lookup"><span data-stu-id="2bac4-237">Copy a hierarchy</span></span>

<span data-ttu-id="2bac4-238">新しい分析コード階層の開始点として、現在の分析コード階層をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-238">You can copy a current dimension hierarchy as the starting point for a new dimension hierarchy.</span></span> <span data-ttu-id="2bac4-239">この方法は、前の分析コード階層を新しい分析コード階層と比較したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-239">This approach can be useful if you want to compare the previous dimension hierarchy to the new dimension hierarchy.</span></span>

### <a name="rearrange-nodes-in-a-hierarchy"></a><span data-ttu-id="2bac4-240">階層内のノードの再配置</span><span class="sxs-lookup"><span data-stu-id="2bac4-240">Rearrange nodes in a hierarchy</span></span>

<span data-ttu-id="2bac4-241">構造内の現在のレベル内でノードを上下に移動できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-241">You can move a node up and down within its current level in the structure.</span></span> <span data-ttu-id="2bac4-242">この方法で、**原価管理** ワークスペースのレポート用のノードの順序を並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-242">In this way, you can rearrange the order of nodes for reporting in the **Cost control** workspace.</span></span>

<span data-ttu-id="2bac4-243">ターゲット ノードを選択して、ノードを階層内の新しい場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-243">You move a node to a new location in the hierarchy by selecting the target node.</span></span> <span data-ttu-id="2bac4-244">ノードを移動する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-244">There are two ways to move a node:</span></span>

- <span data-ttu-id="2bac4-245">**下へ移動** – 階層内の現在の位置から選択したノードを移動し、選択したターゲット ノードの **下に** 挿入します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-245">**Move below** – Move the selected node from its current position in the hierarchy, and insert it **under** the selected target node.</span></span>
- <span data-ttu-id="2bac4-246">**後に移動** – 階層内の現在の位置から選択したノードを移動し、階層内のそのレベルの選択したターゲット ノードの **後に** 挿入します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-246">**Move after** – Move the selected node from its current position in the hierarchy, and insert it **after** the selected target node at its level of the hierarchy.</span></span>

> [!NOTE] 
> <span data-ttu-id="2bac4-247">Excel また Power BI では既定で英数字の並べ替え順序を使用しているため、それらのツールにデータをエクスポートする場合はノードの順序は維持されません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-247">The order of the nodes isn't maintained when you export data to Excel or Power BI, because those tools use an alphanumeric sort order by default.</span></span> <span data-ttu-id="2bac4-248">手動で順序を並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-248">You should manually rearrange the order.</span></span>

## <a name="define-dimension-hierarchies-for-reporting"></a><span data-ttu-id="2bac4-249">レポートの分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="2bac4-249">Define dimension hierarchies for reporting</span></span>

<span data-ttu-id="2bac4-250">分析コード階層はレポートにとって重要です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-250">Dimension hierarchies are important for reporting.</span></span> <span data-ttu-id="2bac4-251">それによって個々の組織に適合する特定の構造を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-251">They let you define the specific structure that fits into the individual organization.</span></span> <span data-ttu-id="2bac4-252">分析コード階層のノード レベルでなされる集約により、組織のどのレベルの利害関係者でも任意のレベルのデータを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-252">The aggregations that are done at the node level of the dimension hierarchy let stakeholders at any level of the organization see data at any level.</span></span>

<span data-ttu-id="2bac4-253">分析コード階層は、次のレポート ツールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-253">Dimension hierarchies are available in the following reporting tools.</span></span> <span data-ttu-id="2bac4-254">この方法は、レポート構造の一貫性を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-254">This approach helps guarantee consistency in the reporting structure.</span></span>

- <span data-ttu-id="2bac4-255">**原価管理** ワークスペース (クライアント):</span><span class="sxs-lookup"><span data-stu-id="2bac4-255">**Cost control** workspace (Client):</span></span>

    - <span data-ttu-id="2bac4-256">コンフィギュレーションによる管理。</span><span class="sxs-lookup"><span data-stu-id="2bac4-256">Controlled by configuration.</span></span>

- <span data-ttu-id="2bac4-257">**原価管理** ワークスペース (モバイル アプリケーション):</span><span class="sxs-lookup"><span data-stu-id="2bac4-257">**Cost control** workspace (Mobile application):</span></span>

    - <span data-ttu-id="2bac4-258">コンフィギュレーションによる管理。</span><span class="sxs-lookup"><span data-stu-id="2bac4-258">Controlled by configuration.</span></span>

- <span data-ttu-id="2bac4-259">Excel</span><span class="sxs-lookup"><span data-stu-id="2bac4-259">Excel</span></span>

    - <span data-ttu-id="2bac4-260">エクスポート定義ごとの特定の分析コード階層を選択するためのオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-260">Provides the option to select specific dimension hierarchies per export definition:</span></span>

        - <span data-ttu-id="2bac4-261">1 つのコスト要素分析コード階層 (必須)</span><span class="sxs-lookup"><span data-stu-id="2bac4-261">One cost element dimension hierarchy (mandatory)</span></span>
        - <span data-ttu-id="2bac4-262">1 つのコスト オブジェクト分析コード階層 (オプション)</span><span class="sxs-lookup"><span data-stu-id="2bac4-262">One cost object dimension hierarchy (optional)</span></span>
        - <span data-ttu-id="2bac4-263">1 つの統計分析コード階層 (オプション)</span><span class="sxs-lookup"><span data-stu-id="2bac4-263">One statistical dimension hierarchy (optional)</span></span>

- <span data-ttu-id="2bac4-264">Power BI:</span><span class="sxs-lookup"><span data-stu-id="2bac4-264">Power BI:</span></span>

    - <span data-ttu-id="2bac4-265">すべての分析コード階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-265">All dimension hierarchies are available.</span></span>
    
<span data-ttu-id="2bac4-266">Excel または Power BI を使用してレポートを作成する場合は、分析コード階層の最初の 15 レベルのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-266">If you create reports by using Excel or Power BI, only the first 15 levels of the dimension hierarchies are exported.</span></span> <span data-ttu-id="2bac4-267">この制限があるのは、Excel も Power BI も固定スキーマを必要とするためです。</span><span class="sxs-lookup"><span data-stu-id="2bac4-267">This limitation exists because a fixed schema is required in Excel and Power BI.</span></span> <span data-ttu-id="2bac4-268">階層に 15 より多いレベルがある場合は、追加のレベルはエクスポートされません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-268">If a hierarchy has more than 15 levels, the additional levels won't be exported.</span></span> <span data-ttu-id="2bac4-269">正規化テーブルには、階層内の各分析コード メンバーのレコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2bac4-269">The normalized table contains a record for each dimension member in the hierarchy.</span></span> <span data-ttu-id="2bac4-270">そのため、自動化集約が行われます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-270">Therefore, automated aggregation occurs.</span></span> <span data-ttu-id="2bac4-271">この動作は、階層内の使用可能な 15 のレベルのいずれの残高も正しいことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-271">This behavior helps guarantee that the balances at any of the 15 available levels in the hierarchy are still correct.</span></span>

<span data-ttu-id="2bac4-272">次の例では、レポート構造における分析コード階層の例を示します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-272">The following example shows what a dimension hierarchy might look like in the reporting structure.</span></span>

| <span data-ttu-id="2bac4-273">コスト オブジェクト分析コード階層 - レベル 1</span><span class="sxs-lookup"><span data-stu-id="2bac4-273">Cost object dimension hierarchy – Level 1</span></span> | <span data-ttu-id="2bac4-274">コスト オブジェクト分析コード階層 - レベル 2</span><span class="sxs-lookup"><span data-stu-id="2bac4-274">Cost object dimension hierarchy – Level 2</span></span> | <span data-ttu-id="2bac4-275">コスト オブジェクト分析コード階層 - レベル 3</span><span class="sxs-lookup"><span data-stu-id="2bac4-275">Cost object dimension hierarchy – Level 3</span></span> | <span data-ttu-id="2bac4-276">コスト オブジェクト分析コード階層 - レベル 4</span><span class="sxs-lookup"><span data-stu-id="2bac4-276">Cost object dimension hierarchy – Level 4</span></span> | <span data-ttu-id="2bac4-277">コスト オブジェクト分析コード階層 - レベル 15</span><span class="sxs-lookup"><span data-stu-id="2bac4-277">Cost object dimension hierarchy – Level 15</span></span> |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="2bac4-278">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-278">Organization</span></span>                              | <span data-ttu-id="2bac4-279">管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-279">Admin</span></span>                                     | <span data-ttu-id="2bac4-280">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-280">Finance</span></span>                                   | <span data-ttu-id="2bac4-281">CC002</span><span class="sxs-lookup"><span data-stu-id="2bac4-281">CC002</span></span>                                     |                                            |
| <span data-ttu-id="2bac4-282">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-282">Organization</span></span>                              | <span data-ttu-id="2bac4-283">管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-283">Admin</span></span>                                     | <span data-ttu-id="2bac4-284">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-284">Finance</span></span>                                   | <span data-ttu-id="2bac4-285">CC003</span><span class="sxs-lookup"><span data-stu-id="2bac4-285">CC003</span></span>                                     |                                            |
| <span data-ttu-id="2bac4-286">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-286">Organization</span></span>                              | <span data-ttu-id="2bac4-287">管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-287">Admin</span></span>                                     | <span data-ttu-id="2bac4-288">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-288">Finance</span></span>                                   | <span data-ttu-id="2bac4-289">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-289">CC007</span></span>                                     |                                            |
| <span data-ttu-id="2bac4-290">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-290">Organization</span></span>                              | <span data-ttu-id="2bac4-291">管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-291">Admin</span></span>                                     | <span data-ttu-id="2bac4-292">HR</span><span class="sxs-lookup"><span data-stu-id="2bac4-292">HR</span></span>                                        | <span data-ttu-id="2bac4-293">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-293">CC001</span></span>                                     |                                            |
| <span data-ttu-id="2bac4-294">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-294">Organization</span></span>                              | <span data-ttu-id="2bac4-295">生産</span><span class="sxs-lookup"><span data-stu-id="2bac4-295">Production</span></span>                                | <span data-ttu-id="2bac4-296">梱包業</span><span class="sxs-lookup"><span data-stu-id="2bac4-296">Packaging</span></span>                                 | <span data-ttu-id="2bac4-297">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-297">CC005</span></span>                                     |                                            |
| <span data-ttu-id="2bac4-298">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-298">Organization</span></span>                              | <span data-ttu-id="2bac4-299">生産</span><span class="sxs-lookup"><span data-stu-id="2bac4-299">Production</span></span>                                | <span data-ttu-id="2bac4-300">組み立て</span><span class="sxs-lookup"><span data-stu-id="2bac4-300">Assembly</span></span>                                  | <span data-ttu-id="2bac4-301">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-301">CC006</span></span>                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a><span data-ttu-id="2bac4-302">レポートのために使用される分析コード階層の更新</span><span class="sxs-lookup"><span data-stu-id="2bac4-302">Update the dimension hierarchies that are used for reporting</span></span> 

<span data-ttu-id="2bac4-303">時間と共に、前述のレポート作成ツールで使用されている分析コード階層を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-303">Over time, the dimension hierarchies that are used in the previously mentioned reporting tools will have to be updated.</span></span> <span data-ttu-id="2bac4-304">分析コード階層を更新するには、クライアントを更新します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-304">You can update dimension hierarchies by refreshing the client.</span></span>

- <span data-ttu-id="2bac4-305">**原価管理** ワークスペース (クライアント)</span><span class="sxs-lookup"><span data-stu-id="2bac4-305">**Cost control** workspace (Client)</span></span>
- <span data-ttu-id="2bac4-306">**原価管理** ワークスペース (モバイル アプリケーション)</span><span class="sxs-lookup"><span data-stu-id="2bac4-306">**Cost control** workspace (Mobile application)</span></span>

<span data-ttu-id="2bac4-307">分析コード階層の更新は、事前キャッシュしたジョブで 24 時間ごとに取得します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-307">Updates to dimension hierarchies are picked up every 24 hours by a pre-cached job.</span></span> <span data-ttu-id="2bac4-308">エクスポートしたデータが更新された後は、次のツールで更新済の分析コード階層が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-308">After the exported data is updated, the updated dimension hierarchies are available in the following tools:</span></span>

- <span data-ttu-id="2bac4-309">Excel</span><span class="sxs-lookup"><span data-stu-id="2bac4-309">Excel</span></span>
- <span data-ttu-id="2bac4-310">Power BI</span><span class="sxs-lookup"><span data-stu-id="2bac4-310">Power BI</span></span>

> [!NOTE] 
> <span data-ttu-id="2bac4-311">分析コード階層キャッシュの更新を手動で開始するため、更新する必要のある分析コード階層用に Excel への新しいエクスポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-311">To manually trigger an update of the dimension hierarchy cache, you can create a new export to Excel for the dimension hierarchy or hierarchies that must be updated.</span></span>

## <a name="define-dimension-hierarchies-for-cost-policies"></a><span data-ttu-id="2bac4-312">コスト ポリシーの分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="2bac4-312">Define dimension hierarchies for cost policies</span></span>

<span data-ttu-id="2bac4-313">原価会計は、詳細なルールを定義している複数のポリシーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-313">Cost accounting consists of multiple policies where detailed rules are defined.</span></span> <span data-ttu-id="2bac4-314">次のポリシーのために 1 つまたは複数の分析コード階層を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-314">You must define one or more dimension hierarchies for the following policies:</span></span>

- <span data-ttu-id="2bac4-315">原価動作</span><span class="sxs-lookup"><span data-stu-id="2bac4-315">Cost behavior</span></span>
- <span data-ttu-id="2bac4-316">原価配分</span><span class="sxs-lookup"><span data-stu-id="2bac4-316">Cost distribution</span></span>
- <span data-ttu-id="2bac4-317">原価配賦</span><span class="sxs-lookup"><span data-stu-id="2bac4-317">Cost allocation</span></span>
- <span data-ttu-id="2bac4-318">原価ロールアップ</span><span class="sxs-lookup"><span data-stu-id="2bac4-318">Cost rollup</span></span>

<span data-ttu-id="2bac4-319">分析コード階層によりルールが作成しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-319">Dimension hierarchies make it easy to create rules.</span></span> <span data-ttu-id="2bac4-320">すべての分析コード メンバーのルールを作成しなくてよいように、分析コード階層レベルが提供する分析コード メンバーの集約を利用できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-320">To avoid having to create rules for every dimension member, you can take advantage of the aggregations of dimension members that are provided by dimension hierarchy levels.</span></span> <span data-ttu-id="2bac4-321">重複するルールがある場合、間接費の計算時にシステムが考慮する特定のルールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-321">If you have overlapping rules, you must define specific rules that the system will consider when it does the overhead calculation.</span></span>

### <a name="example-define-a-cost-behavior-policy"></a><span data-ttu-id="2bac4-322">例: コスト動作ポリシーを定義する</span><span class="sxs-lookup"><span data-stu-id="2bac4-322">Example: Define a cost behavior policy</span></span>

<span data-ttu-id="2bac4-323">以下のように、新しいコスト動作ポリシーが作成され、適切な分析コード階層がポリシーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-323">A new cost behavior policy is created, and appropriate dimension hierarchies are assigned to the policy, as shown here.</span></span>

<span data-ttu-id="2bac4-324">**コスト動作ポリシー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-324">**Cost behavior policy**</span></span>

| <span data-ttu-id="2bac4-325">ポリシー名</span><span class="sxs-lookup"><span data-stu-id="2bac4-325">Policy name</span></span>   | <span data-ttu-id="2bac4-326">原価要素分析コード階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-326">Cost element dimension hierarchy</span></span> | <span data-ttu-id="2bac4-327">原価オブジェクト分析コード階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-327">Cost object dimension hierarchy</span></span> | <span data-ttu-id="2bac4-328">会計通貨</span><span class="sxs-lookup"><span data-stu-id="2bac4-328">Accounting currency</span></span> |
|---------------|----------------------------------|---------------------------------|---------------------|
| <span data-ttu-id="2bac4-329">原価動作</span><span class="sxs-lookup"><span data-stu-id="2bac4-329">Cost behavior</span></span> | <span data-ttu-id="2bac4-330">原価動作</span><span class="sxs-lookup"><span data-stu-id="2bac4-330">Cost behavior</span></span>                    | <span data-ttu-id="2bac4-331">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-331">Organization</span></span>                    | <span data-ttu-id="2bac4-332">USD</span><span class="sxs-lookup"><span data-stu-id="2bac4-332">USD</span></span>                 |

<span data-ttu-id="2bac4-333">**ルール**</span><span class="sxs-lookup"><span data-stu-id="2bac4-333">**Rules**</span></span>

| <span data-ttu-id="2bac4-334">原価要素分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="2bac4-334">Cost element dimension hierarchy node</span></span> | <span data-ttu-id="2bac4-335">原価オブジェクト分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="2bac4-335">Cost object dimension hierarchy node</span></span> | <span data-ttu-id="2bac4-336">固定割合</span><span class="sxs-lookup"><span data-stu-id="2bac4-336">Fixed percentage</span></span> | <span data-ttu-id="2bac4-337">固定金額</span><span class="sxs-lookup"><span data-stu-id="2bac4-337">Fixed amount</span></span> | <span data-ttu-id="2bac4-338">発効日</span><span class="sxs-lookup"><span data-stu-id="2bac4-338">Valid from</span></span> | <span data-ttu-id="2bac4-339">失効日</span><span class="sxs-lookup"><span data-stu-id="2bac4-339">Valid to</span></span> |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| <span data-ttu-id="2bac4-340">固定費</span><span class="sxs-lookup"><span data-stu-id="2bac4-340">Fixed cost</span></span>                            | <span data-ttu-id="2bac4-341">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-341">Organization</span></span>                         | <span data-ttu-id="2bac4-342">100.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-342">100.00</span></span>           | <span data-ttu-id="2bac4-343">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-343">0.00</span></span>         | <span data-ttu-id="2bac4-344">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-344">1/1/2017</span></span>   | <span data-ttu-id="2bac4-345">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-345">Never</span></span>    |
| <span data-ttu-id="2bac4-346">10001</span><span class="sxs-lookup"><span data-stu-id="2bac4-346">10001</span></span>                                 | <span data-ttu-id="2bac4-347">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-347">Organization</span></span>                         | <span data-ttu-id="2bac4-348">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-348">0.00</span></span>             | <span data-ttu-id="2bac4-349">150.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-349">150.00</span></span>       | <span data-ttu-id="2bac4-350">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-350">1/1/2017</span></span>   | <span data-ttu-id="2bac4-351">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-351">Never</span></span>    |
| <span data-ttu-id="2bac4-352">10001 (\*)</span><span class="sxs-lookup"><span data-stu-id="2bac4-352">10001 (\*)</span></span>                             | <span data-ttu-id="2bac4-353">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-353">Finance</span></span>                              |                  | <span data-ttu-id="2bac4-354">50.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-354">50.00</span></span>        | <span data-ttu-id="2bac4-355">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-355">1/1/2017</span></span>   | <span data-ttu-id="2bac4-356">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-356">Never</span></span>    |
| <span data-ttu-id="2bac4-357">コスト動作や変動費 (\*\*)</span><span class="sxs-lookup"><span data-stu-id="2bac4-357">Cost behavior or Variable cost (\*\*)</span></span>   | <span data-ttu-id="2bac4-358">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-358">Organization</span></span>                         | <span data-ttu-id="2bac4-359">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-359">0.00</span></span>             | <span data-ttu-id="2bac4-360">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-360">0.00</span></span>         | <span data-ttu-id="2bac4-361">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-361">1/1/2017</span></span>   | <span data-ttu-id="2bac4-362">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-362">Never</span></span>    |

<span data-ttu-id="2bac4-363">\* 変動費ノードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-363">\* The variable cost node isn't required.</span></span> <span data-ttu-id="2bac4-364">コストが固定費に分類されていない場合は、変動費になります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-364">If a cost isn't classified as a fixed cost, it must be a variable cost.</span></span>

<span data-ttu-id="2bac4-365">\*\* コスト要素メンバー 10001 と財務階層レベル (CC002、CC003、CC007) の下で集約されるすべてのコスト オブジェクト メンバーの組み合わせに対して詳細なルールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-365">\*\* A detailed rule is created for the combination of cost element member 10001 and all cost object members that are aggregated under the Finance hierarchy level (CC002, CC003, CC007).</span></span>

<span data-ttu-id="2bac4-366">前述のルールは分析コード階層が提供する柔軟性を示します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-366">The preceding rules show the flexibility that dimension hierarchies provide.</span></span> <span data-ttu-id="2bac4-367">高レベルのルールを定義することで、メンテナンスを最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-367">By defining high-level rules, you can help minimize maintenance.</span></span> <span data-ttu-id="2bac4-368">特定の業務目標に適合する詳細なルールを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-368">You can then define detailed rules to fit into a specific business objective.</span></span>

<span data-ttu-id="2bac4-369">ルール内で使用する分析コード階層が更新される場合、システムが自動的に更新を進めます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-369">If the dimension hierarchies that are used in rules are updated, the system automatically brings the updates forward.</span></span>

<span data-ttu-id="2bac4-370">ルール内の粒度のレベルが必要なくなった場合、そのルールを失効にできます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-370">If a level of granularity in the rules is no longer required, the rule can be expired.</span></span>

<span data-ttu-id="2bac4-371">たとえば、財務コスト オブジェクトの分析コード階層ノードの特定のコスト動作ルールが必要でなくなりました。</span><span class="sxs-lookup"><span data-stu-id="2bac4-371">For example, a specific cost behavior rule for the Finance cost object dimension hierarchy node is no longer required.</span></span> <span data-ttu-id="2bac4-372">この場合は、**ルールを失効にする**をクリックしてルールを失効させます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-372">In this case, click **Expire rule** to expire the rule.</span></span>

| <span data-ttu-id="2bac4-373">原価要素分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="2bac4-373">Cost element dimension hierarchy node</span></span> | <span data-ttu-id="2bac4-374">原価オブジェクト分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="2bac4-374">Cost object dimension hierarchy node</span></span> | <span data-ttu-id="2bac4-375">固定割合</span><span class="sxs-lookup"><span data-stu-id="2bac4-375">Fixed percentage</span></span> | <span data-ttu-id="2bac4-376">固定金額</span><span class="sxs-lookup"><span data-stu-id="2bac4-376">Fixed amount</span></span> | <span data-ttu-id="2bac4-377">発効日</span><span class="sxs-lookup"><span data-stu-id="2bac4-377">Valid from</span></span> | <span data-ttu-id="2bac4-378">失効日</span><span class="sxs-lookup"><span data-stu-id="2bac4-378">Valid to</span></span>  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| <span data-ttu-id="2bac4-379">固定費</span><span class="sxs-lookup"><span data-stu-id="2bac4-379">Fixed cost</span></span>                            | <span data-ttu-id="2bac4-380">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-380">Organization</span></span>                         | <span data-ttu-id="2bac4-381">100,00</span><span class="sxs-lookup"><span data-stu-id="2bac4-381">100,00</span></span>           | <span data-ttu-id="2bac4-382">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-382">0,00</span></span>         | <span data-ttu-id="2bac4-383">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-383">1/1/2017</span></span>   | <span data-ttu-id="2bac4-384">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-384">Never</span></span>     |
| <span data-ttu-id="2bac4-385">10001</span><span class="sxs-lookup"><span data-stu-id="2bac4-385">10001</span></span>                                 | <span data-ttu-id="2bac4-386">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-386">Organization</span></span>                         | <span data-ttu-id="2bac4-387">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-387">0,00</span></span>             | <span data-ttu-id="2bac4-388">150,00</span><span class="sxs-lookup"><span data-stu-id="2bac4-388">150,00</span></span>       | <span data-ttu-id="2bac4-389">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-389">1/1/2017</span></span>   | <span data-ttu-id="2bac4-390">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-390">Never</span></span>     |
| <span data-ttu-id="2bac4-391">10001</span><span class="sxs-lookup"><span data-stu-id="2bac4-391">10001</span></span>                                 | <span data-ttu-id="2bac4-392">財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-392">Finance</span></span>                              |                  | <span data-ttu-id="2bac4-393">50,00</span><span class="sxs-lookup"><span data-stu-id="2bac4-393">50,00</span></span>        | <span data-ttu-id="2bac4-394">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-394">1/1/2017</span></span>   | <span data-ttu-id="2bac4-395">20/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-395">20/1/2017</span></span> |
| <span data-ttu-id="2bac4-396">コスト動作または変動費</span><span class="sxs-lookup"><span data-stu-id="2bac4-396">Cost behavior or Variable cost</span></span>        | <span data-ttu-id="2bac4-397">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-397">Organization</span></span>                         | <span data-ttu-id="2bac4-398">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-398">0,00</span></span>             | <span data-ttu-id="2bac4-399">0.00</span><span class="sxs-lookup"><span data-stu-id="2bac4-399">0,00</span></span>         | <span data-ttu-id="2bac4-400">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="2bac4-400">1/1/2017</span></span>   | <span data-ttu-id="2bac4-401">許可しない</span><span class="sxs-lookup"><span data-stu-id="2bac4-401">Never</span></span>     |

<span data-ttu-id="2bac4-402">2017 年 1 月 20 日以降に実行される間接費計算は、このルールを考慮しなくなります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-402">Any overhead calculation that is run after January 20, 2017, no longer considers this rule.</span></span>

> [!NOTE] 
> <span data-ttu-id="2bac4-403">**発効日**および**失効日**フィールドは日付と時刻に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-403">The **Valid from** and **Valid to** fields are date-effective and time-effective.</span></span> <span data-ttu-id="2bac4-404">同じ日にルールの失効と新しい間接費の計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-404">You can expire the rule and run a new overhead calculation on the same day.</span></span>

## <a name="define-dimension-hierarchies-for-security-setup"></a><span data-ttu-id="2bac4-405">セキュリティ設定の分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="2bac4-405">Define dimension hierarchies for security setup</span></span>

<span data-ttu-id="2bac4-406">原価会計のデータは、レポート単位を担当するすべてのマネージャーに使用可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-406">Cost accounting data should be made available to all managers who are responsible for a reporting unit.</span></span> <span data-ttu-id="2bac4-407">原価会計用語では、レポート単位は、コスト オブジェクトまたは一連のコスト オブジェクトとして表されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-407">In Cost accounting terminology, a reporting unit is represented as a cost object or a set of cost objects.</span></span>

<span data-ttu-id="2bac4-408">すべてのマネージャーは、収益や利益幅といった機密性の高いビジネス データにアクセスできるようになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-408">Potentially, all managers will be able to access highly sensitive business data, such revenues and margins.</span></span> <span data-ttu-id="2bac4-409">そのため、マネージャーが自分に関連のあるデータのみを参照するよう、セキュリティを設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-409">Therefore, it's important that you set up security, so that managers see only the data that is relevant to them.</span></span> <span data-ttu-id="2bac4-410">データ セキュリティを管理するために、分析コード階層を定義します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-410">To help control data security, you define dimension hierarchies.</span></span>

- <span data-ttu-id="2bac4-411">分析コード階層の使用は、分析コード階層参照で選択されている分析コード値がコスト オブジェクト分析コードである場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-411">The use of dimension hierarchies applies only when the dimension value that is selected in the dimension hierarchy reference is a cost object dimension.</span></span>
- <span data-ttu-id="2bac4-412">アクセス リスト階層内のコスト オブジェクト分析コードごとに 1 つの分析コード階層のみを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-412">Only one dimension hierarchy can be enabled per cost object dimension in the access list hierarchy.</span></span>

<span data-ttu-id="2bac4-413">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="2bac4-413">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="2bac4-414">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="2bac4-414">Dimension hierarchy name</span></span> | <span data-ttu-id="2bac4-415">分析コード</span><span class="sxs-lookup"><span data-stu-id="2bac4-415">Dimension</span></span>    | <span data-ttu-id="2bac4-416">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="2bac4-416">Dimension hierarchy type name</span></span>      | <span data-ttu-id="2bac4-417">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-417">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="2bac4-418">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-418">Organization</span></span>             | <span data-ttu-id="2bac4-419">コスト センター</span><span class="sxs-lookup"><span data-stu-id="2bac4-419">Cost centers</span></span> | <span data-ttu-id="2bac4-420">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="2bac4-420">Dimension classification hierarchy</span></span> | <span data-ttu-id="2bac4-421">**有**</span><span class="sxs-lookup"><span data-stu-id="2bac4-421">**Yes**</span></span>               |

<span data-ttu-id="2bac4-422">新しい**ユーザー**クイック タブは階層デザイナーで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="2bac4-422">A new **Users** FastTab is available in the hierarchy designer.</span></span> <span data-ttu-id="2bac4-423">ここでは、階層内の各ノードに 1 つまたは複数のユーザー ID を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-423">Here, you can insert one or more user IDs at each node in the hierarchy.</span></span>

|                 | <span data-ttu-id="2bac4-424">ユーザー</span><span class="sxs-lookup"><span data-stu-id="2bac4-424">Users</span></span>            | <span data-ttu-id="2bac4-425">分析コード メンバーの範囲</span><span class="sxs-lookup"><span data-stu-id="2bac4-425">Dimension member ranges</span></span>   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="2bac4-426">**ノード**</span><span class="sxs-lookup"><span data-stu-id="2bac4-426">**Nodes**</span></span>       | <span data-ttu-id="2bac4-427">**ユーザー ID**</span><span class="sxs-lookup"><span data-stu-id="2bac4-427">**User ID**</span></span>      | <span data-ttu-id="2bac4-428">**移動元分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-428">**From dimension member**</span></span> | <span data-ttu-id="2bac4-429">**移動先分析コード メンバー**</span><span class="sxs-lookup"><span data-stu-id="2bac4-429">**To dimension member**</span></span> |
| <span data-ttu-id="2bac4-430">組織</span><span class="sxs-lookup"><span data-stu-id="2bac4-430">Organization</span></span>    | <span data-ttu-id="2bac4-431">ベンジャミン、クレア</span><span class="sxs-lookup"><span data-stu-id="2bac4-431">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="2bac4-432">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="2bac4-432">&nbsp;&nbsp;Admin</span></span>         | <span data-ttu-id="2bac4-433">4 月</span><span class="sxs-lookup"><span data-stu-id="2bac4-433">April</span></span>            |                           |                         |
| <span data-ttu-id="2bac4-434">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="2bac4-434">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="2bac4-435">アリシア</span><span class="sxs-lookup"><span data-stu-id="2bac4-435">Alicia</span></span>           | <span data-ttu-id="2bac4-436">CC002</span><span class="sxs-lookup"><span data-stu-id="2bac4-436">CC002</span></span>                     | <span data-ttu-id="2bac4-437">CC003</span><span class="sxs-lookup"><span data-stu-id="2bac4-437">CC003</span></span>                   |
|                 |                  | <span data-ttu-id="2bac4-438">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-438">CC007</span></span>                     | <span data-ttu-id="2bac4-439">CC007</span><span class="sxs-lookup"><span data-stu-id="2bac4-439">CC007</span></span>                   |
| <span data-ttu-id="2bac4-440">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="2bac4-440">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="2bac4-441">アーニー</span><span class="sxs-lookup"><span data-stu-id="2bac4-441">Arnie</span></span>            | <span data-ttu-id="2bac4-442">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-442">CC001</span></span>                     | <span data-ttu-id="2bac4-443">CC001</span><span class="sxs-lookup"><span data-stu-id="2bac4-443">CC001</span></span>                   |
| <span data-ttu-id="2bac4-444">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="2bac4-444">&nbsp;&nbsp;Production</span></span>    | <span data-ttu-id="2bac4-445">デビッド</span><span class="sxs-lookup"><span data-stu-id="2bac4-445">David</span></span>            |                           |                         |
| <span data-ttu-id="2bac4-446">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="2bac4-446">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="2bac4-447">エレン</span><span class="sxs-lookup"><span data-stu-id="2bac4-447">Ellen</span></span>            | <span data-ttu-id="2bac4-448">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-448">CC005</span></span>                     | <span data-ttu-id="2bac4-449">CC005</span><span class="sxs-lookup"><span data-stu-id="2bac4-449">CC005</span></span>                   |
| <span data-ttu-id="2bac4-450">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="2bac4-450">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="2bac4-451">クリス</span><span class="sxs-lookup"><span data-stu-id="2bac4-451">Chris</span></span>            | <span data-ttu-id="2bac4-452">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-452">CC006</span></span>                     | <span data-ttu-id="2bac4-453">CC006</span><span class="sxs-lookup"><span data-stu-id="2bac4-453">CC006</span></span>                   |

> [!NOTE] 
> <span data-ttu-id="2bac4-454">原価計算のすべてのエントリを表示できるように、原価経理担当者は階層の最上部に割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-454">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="2bac4-455">アクセス リスト階層とそのセキュリティ設定を有効にするには、**原価会計** > **設定** > **パラメーター** > **一般**に移動します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-455">To enable the access list hierarchy and its security settings, go to **Cost accounting** > **Setup** > **Parameters** > **General**.</span></span> <span data-ttu-id="2bac4-456">**コスト オブジェクト分析コード メンバーに対する表示アクセスの有効化**パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-456">Select the **Enable view access for cost object dimension members** parameter.</span></span>

<span data-ttu-id="2bac4-457">アクセス リスト階層の設定は、次の領域に表示されるデータを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2bac4-457">The settings for the access list hierarchy are used to control the data that is shown in the following areas:</span></span>

- <span data-ttu-id="2bac4-458">**原価管理** ワークスペース (クライアント):</span><span class="sxs-lookup"><span data-stu-id="2bac4-458">**Cost control** workspace (Client):</span></span>

    - <span data-ttu-id="2bac4-459">シナリオをドリルスルーするために使用されるフォーム内のデータ</span><span class="sxs-lookup"><span data-stu-id="2bac4-459">Data in forms that are used to drill through scenarios</span></span>

- <span data-ttu-id="2bac4-460">**原価管理** ワークスペース (モバイル アプリケーション):</span><span class="sxs-lookup"><span data-stu-id="2bac4-460">**Cost control** workspace (Mobile application):</span></span>

    - <span data-ttu-id="2bac4-461">カードの残高</span><span class="sxs-lookup"><span data-stu-id="2bac4-461">Balances in cards</span></span>

- <span data-ttu-id="2bac4-462">Power BI:</span><span class="sxs-lookup"><span data-stu-id="2bac4-462">Power BI:</span></span>

    - <span data-ttu-id="2bac4-463">Power BI ビジュアル化に表示されるデータ</span><span class="sxs-lookup"><span data-stu-id="2bac4-463">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="2bac4-464">Dynamics 365 Finance クライアントに埋め込まれた Power BI ビジュアル化データ</span><span class="sxs-lookup"><span data-stu-id="2bac4-464">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!NOTE] 
> - <span data-ttu-id="2bac4-465">アクセス リスト階層が Power BI のデータに影響を及ぼす前に、アクセス リスト階層と Power BI の行レベルのセキュリティがペアリングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2bac4-465">Before the access list hierarchy can affect data in Power BI, access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="2bac4-466">詳細については、「[原価会計コンテンツ パックのセキュリティ設定](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2bac4-466">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="2bac4-467">アクセス リスト階層は、Excel へのデータのエクスポートの保護には役立ちません。</span><span class="sxs-lookup"><span data-stu-id="2bac4-467">The access list hierarchy doesn't help secure the export of data to Excel.</span></span> <span data-ttu-id="2bac4-468">したがって、そのレポート ツールは、データの表示に完全なアクセス権を持つ必要があるコスト経理担当者およびマネージャーのみが使用します。</span><span class="sxs-lookup"><span data-stu-id="2bac4-468">Therefore, that reporting tool should be used only by cost accountants and managers who must have full access to view the data.</span></span>
