---
title: 分析コード階層
description: このトピックでは、分析コード階層について説明します。 分析コード階層を使用して、原価会計のレポート構造、コスト ポリシー、およびセキュリティ設定を定義します。
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fdf280031e2ad2356a1a2ef3bba75d1f74c8e4de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810177"
---
# <a name="dimension-hierarchy"></a><span data-ttu-id="dd54e-104">分析コード階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-104">Dimension hierarchy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd54e-105">このトピックでは、分析コード階層について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-105">This topic provides information about dimension hierarchies.</span></span> <span data-ttu-id="dd54e-106">分析コード階層を使用して、原価会計のレポート構造、コスト ポリシー、およびセキュリティ設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-106">You use a dimension hierarchy to define the reporting structure, cost policies, and security setup in Cost accounting.</span></span>  

## <a name="overview"></a><span data-ttu-id="dd54e-107">概要</span><span class="sxs-lookup"><span data-stu-id="dd54e-107">Overview</span></span>

<span data-ttu-id="dd54e-108">分析コード階層は、原価会計のさまざまな場所で使用します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-108">Dimension hierarchies are used in various places in Cost accounting.</span></span> <span data-ttu-id="dd54e-109">分析コード階層を使用して、次の情報を定義できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-109">A dimension hierarchy lets you define the following information:</span></span>

-  <span data-ttu-id="dd54e-110">組織の要件に適合するレポート構造</span><span class="sxs-lookup"><span data-stu-id="dd54e-110">The reporting structure that fits into the organization's requirements</span></span>
-  <span data-ttu-id="dd54e-111">コスト ポリシー</span><span class="sxs-lookup"><span data-stu-id="dd54e-111">Cost policies</span></span>
-  <span data-ttu-id="dd54e-112">セキュリティ設定</span><span class="sxs-lookup"><span data-stu-id="dd54e-112">The security setup</span></span>

<span data-ttu-id="dd54e-113">分析コード階層の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-113">Here is an example of a dimension hierarchy.</span></span>

![分析コード階層の例](./media/dimension-hierarchy.png)

<span data-ttu-id="dd54e-115">次のタイプの分析コードに対して分析コード階層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-115">A dimension hierarchy can be created for the following types of dimensions:</span></span>

-  <span data-ttu-id="dd54e-116">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-116">Cost element dimensions</span></span>
-  <span data-ttu-id="dd54e-117">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-117">Cost object dimensions</span></span>
-  <span data-ttu-id="dd54e-118">統計分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-118">Statistical dimensions</span></span>

> [!NOTE]
> - <span data-ttu-id="dd54e-119">異なる分析視点が必要な場合は、同じ分析コードに対して複数の分析コード階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-119">You can create multiple dimension hierarchies for the same dimension if different perspectives are required.</span></span>
> - <span data-ttu-id="dd54e-120">分析コード階層は、1 つの分析コードにのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-120">A dimension hierarchy can be associated with only one dimension.</span></span>
> - <span data-ttu-id="dd54e-121">分析コード階層は構造内に無制限にレベルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-121">A dimension hierarchy can have unlimited levels in its structure.</span></span> <span data-ttu-id="dd54e-122">すべてのレベルは **原価管理** ワークスペースで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-122">All the levels will be available in the **Cost control** workspace.</span></span> <span data-ttu-id="dd54e-123">レポート用に Microsoft Excel または Microsoft Power BI を使用する場合は、分析コード階層の最初の 15 レベルのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-123">When you use Microsoft Excel or Microsoft Power BI for reporting purposes, only the first 15 levels of the dimension hierarchy are exported.</span></span> <span data-ttu-id="dd54e-124">この制限があるのは、Excel も Power BI も固定スキーマを必要とするためです。</span><span class="sxs-lookup"><span data-stu-id="dd54e-124">This limitation exists because both Excel and Power BI require a fixed schema.</span></span>
> - <span data-ttu-id="dd54e-125">分析コード階層は、日付に対して有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-125">A dimension hierarchy isn't date-effective.</span></span> <span data-ttu-id="dd54e-126">このため、分析コード階層への変更は直ちにレコードに保存され、日付前と日付後を比較することはできません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-126">Therefore, any change to a dimension hierarchy is immediately saved to the record, and you can't compare the before date and after date.</span></span>

## <a name="dimension-hierarchy-type"></a><span data-ttu-id="dd54e-127">分析コード階層タイプ</span><span class="sxs-lookup"><span data-stu-id="dd54e-127">Dimension hierarchy type</span></span>

<span data-ttu-id="dd54e-128">新しい分析コード階層を作成する際には、階層タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-128">When you create a new dimension hierarchy, you must select a hierarchy type.</span></span> <span data-ttu-id="dd54e-129">**原価会計** > **分析コード** > **分析コード階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-129">Go to **Cost accounting** > **Dimensions** > **Dimension hierarchies**.</span></span> <span data-ttu-id="dd54e-130">**新規** をクリックし、分析コード階層タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-130">Click **New**, and select a dimension hierarchy type.</span></span> <span data-ttu-id="dd54e-131">**分析コード カテゴリ階層** または **分析コード分類階層** のいずれかを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-131">You can select either **Dimension categorization hierarchy** or **Dimension classification hierarchy**.</span></span>

### <a name="dimension-categorization-hierarchy"></a><span data-ttu-id="dd54e-132">分析コード カテゴリ階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-132">Dimension categorization hierarchy</span></span>

<span data-ttu-id="dd54e-133">**分析コードカテゴリ階層** タイプはレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-133">The **Dimension categorization hierarchy** type is used for reporting purposes.</span></span> <span data-ttu-id="dd54e-134">コスト要素分析コードのみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="dd54e-134">It supports only the cost element dimensions.</span></span> <span data-ttu-id="dd54e-135">このタイプを選択する場合は、次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-135">When you select this type, the following rules apply:</span></span>

-  <span data-ttu-id="dd54e-136">分析コード メンバーは、階層構造に複数回関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-136">A dimension member can be associated more than one time in the hierarchy structure.</span></span>
-  <span data-ttu-id="dd54e-137">コスト動作をリーフ ノードに割り当てることにより、さまざまなノードにコスト要素分析コード メンバーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-137">You can put a cost element dimension member in different nodes by assigning a cost behavior to the leaf node.</span></span>

### <a name="dimension-classification-hierarchy"></a><span data-ttu-id="dd54e-138">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-138">Dimension classification hierarchy</span></span>

<span data-ttu-id="dd54e-139">**分析コード分類階層** タイプはルールの定義、およびレポート用に使用します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-139">The **Dimension classification hierarchy** type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="dd54e-140">コスト オブジェクト、コスト要素、および統計分析コードなどのすべての分析コードをサポートします。</span><span class="sxs-lookup"><span data-stu-id="dd54e-140">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span> <span data-ttu-id="dd54e-141">このタイプを選択する場合は、分析コード メンバーは階層構造に 1 回のみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-141">When you select this type, a dimension member can be associated only one time in the hierarchy structure.</span></span>

## <a name="create-and-maintain-a-dimension-hierarchy"></a><span data-ttu-id="dd54e-142">分析コード階層の作成と管理</span><span class="sxs-lookup"><span data-stu-id="dd54e-142">Create and maintain a dimension hierarchy</span></span>

<span data-ttu-id="dd54e-143">分析コード階層は、ノードとリーフ ノードのリレーションシップを持つツリー構造として作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-143">A dimension hierarchy is created as a tree structure that has node and leaf node relationships.</span></span>

-  <span data-ttu-id="dd54e-144">ノードは 1:_n_ サブノードを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-144">A node can have 1:_n_ subnodes.</span></span>
-  <span data-ttu-id="dd54e-145">ノードはサブノードとそれに割り当てられたリーフ ノードの両方を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-145">A node can’t have both subnodes and leaf nodes assigned to it.</span></span>
-  <span data-ttu-id="dd54e-146">リーフ ノードは、階層の最下位レベルでのみ割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-146">A leaf node can be assigned only at the lowest level in the hierarchy.</span></span>

### <a name="example"></a><span data-ttu-id="dd54e-147">例</span><span class="sxs-lookup"><span data-stu-id="dd54e-147">Example</span></span>

<span data-ttu-id="dd54e-148">小規模の会社が次の組織構造を持っています。「財務」および「人事管理」は「管理」の下にある部署、また「組み立て」および「梱包業」は「生産」の下にある部署です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-148">A small company has the following organization structure, where Finance and Human resources are departments under Admin, and Assembly and Packaging are departments under Production.</span></span>

![組織構造の例](./media/dimension-hierarchy-org.png)

<span data-ttu-id="dd54e-150">コスト オブジェクト分析コードは、組織内のすべてのコスト センターを表します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-150">A cost object dimension represents all the cost centers in the organization.</span></span>

- <span data-ttu-id="dd54e-151">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-151">Cost object dimension</span></span>
    - <span data-ttu-id="dd54e-152">コスト センター</span><span class="sxs-lookup"><span data-stu-id="dd54e-152">Cost centers</span></span>

<span data-ttu-id="dd54e-153">すべてのコスト センターを表すコスト オブジェクト分析コードは以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-153">The cost object dimension that represents all the cost centers can be set up as shown here.</span></span>

| <span data-ttu-id="dd54e-154">コスト センター</span><span class="sxs-lookup"><span data-stu-id="dd54e-154">Cost centers</span></span> | <span data-ttu-id="dd54e-155">説明</span><span class="sxs-lookup"><span data-stu-id="dd54e-155">Description</span></span> |
|--------------|-------------|
| <span data-ttu-id="dd54e-156">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-156">CC001</span></span>        | <span data-ttu-id="dd54e-157">HR</span><span class="sxs-lookup"><span data-stu-id="dd54e-157">HR</span></span>          |
| <span data-ttu-id="dd54e-158">CC002</span><span class="sxs-lookup"><span data-stu-id="dd54e-158">CC002</span></span>        | <span data-ttu-id="dd54e-159">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-159">Finance</span></span>     |
| <span data-ttu-id="dd54e-160">CC003</span><span class="sxs-lookup"><span data-stu-id="dd54e-160">CC003</span></span>        | <span data-ttu-id="dd54e-161">税申告</span><span class="sxs-lookup"><span data-stu-id="dd54e-161">Tax</span></span>         |
| <span data-ttu-id="dd54e-162">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-162">CC007</span></span>        | <span data-ttu-id="dd54e-163">AR/AP</span><span class="sxs-lookup"><span data-stu-id="dd54e-163">AR/AP</span></span>       |
| <span data-ttu-id="dd54e-164">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-164">CC005</span></span>        | <span data-ttu-id="dd54e-165">組み立て</span><span class="sxs-lookup"><span data-stu-id="dd54e-165">Assembly</span></span>    |
| <span data-ttu-id="dd54e-166">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-166">CC006</span></span>        | <span data-ttu-id="dd54e-167">梱包業</span><span class="sxs-lookup"><span data-stu-id="dd54e-167">Packaging</span></span>   |

<span data-ttu-id="dd54e-168">コスト要素分析コードは、組織内のすべてのコスト要素を表します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-168">A cost element dimension represents all the cost elements in the organization.</span></span>

- <span data-ttu-id="dd54e-169">原価要素分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-169">Cost element dimension</span></span>
    - <span data-ttu-id="dd54e-170">コスト要素</span><span class="sxs-lookup"><span data-stu-id="dd54e-170">Cost elements</span></span>

<span data-ttu-id="dd54e-171">すべてのコスト要素を表すコスト要素分析コードは以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-171">The cost element dimension that represents all the cost elements can be set up as shown here.</span></span>

| <span data-ttu-id="dd54e-172">コスト要素</span><span class="sxs-lookup"><span data-stu-id="dd54e-172">Cost elements</span></span> | <span data-ttu-id="dd54e-173">説明</span><span class="sxs-lookup"><span data-stu-id="dd54e-173">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="dd54e-174">10001</span><span class="sxs-lookup"><span data-stu-id="dd54e-174">10001</span></span>         | <span data-ttu-id="dd54e-175">電気</span><span class="sxs-lookup"><span data-stu-id="dd54e-175">Electricity</span></span> |
| <span data-ttu-id="dd54e-176">10010</span><span class="sxs-lookup"><span data-stu-id="dd54e-176">10010</span></span>         | <span data-ttu-id="dd54e-177">クリーニング</span><span class="sxs-lookup"><span data-stu-id="dd54e-177">Cleaning</span></span>    |
| <span data-ttu-id="dd54e-178">10011</span><span class="sxs-lookup"><span data-stu-id="dd54e-178">10011</span></span>         | <span data-ttu-id="dd54e-179">暖房</span><span class="sxs-lookup"><span data-stu-id="dd54e-179">Heating</span></span>     |
| <span data-ttu-id="dd54e-180">40001</span><span class="sxs-lookup"><span data-stu-id="dd54e-180">40001</span></span>         | <span data-ttu-id="dd54e-181">COGS</span><span class="sxs-lookup"><span data-stu-id="dd54e-181">COGS</span></span>        |

<span data-ttu-id="dd54e-182">組織のレポート要件を満たす分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-182">A dimension hierarchy that meets the organizational reporting requirements can be set up as shown here.</span></span>

<span data-ttu-id="dd54e-183">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="dd54e-183">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="dd54e-184">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="dd54e-184">Dimension hierarchy name</span></span> | <span data-ttu-id="dd54e-185">分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-185">Dimension</span></span>    | <span data-ttu-id="dd54e-186">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="dd54e-186">Dimension hierarchy type name</span></span>      | <span data-ttu-id="dd54e-187">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-187">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="dd54e-188">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-188">Organization</span></span>             | <span data-ttu-id="dd54e-189">コスト センター</span><span class="sxs-lookup"><span data-stu-id="dd54e-189">Cost centers</span></span> | <span data-ttu-id="dd54e-190">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-190">Dimension classification hierarchy</span></span> | <span data-ttu-id="dd54e-191">無</span><span class="sxs-lookup"><span data-stu-id="dd54e-191">No</span></span>                    |

<span data-ttu-id="dd54e-192">レポートの分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-192">The dimension hierarchy for reporting can be set up as shown here.</span></span>

<span data-ttu-id="dd54e-193">**分析コード メンバーの範囲**</span><span class="sxs-lookup"><span data-stu-id="dd54e-193">**Dimension member ranges**</span></span>

|   <span data-ttu-id="dd54e-194">ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-194">Nodes</span></span>           |   <span data-ttu-id="dd54e-195">移動元分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-195">From dimension member</span></span>   |   <span data-ttu-id="dd54e-196">移動先分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-196">To dimension member</span></span>   |
|-------------------|---------------------------|-------------------------|
| <span data-ttu-id="dd54e-197">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-197">Organization</span></span>      |                           |                         |
| <span data-ttu-id="dd54e-198">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-198">&nbsp;&nbsp;Admin</span></span>         |                           |                         |
| <span data-ttu-id="dd54e-199">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-199">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="dd54e-200">CC002</span><span class="sxs-lookup"><span data-stu-id="dd54e-200">CC002</span></span>                     | <span data-ttu-id="dd54e-201">CC003</span><span class="sxs-lookup"><span data-stu-id="dd54e-201">CC003</span></span>                   |
|                   | <span data-ttu-id="dd54e-202">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-202">CC007</span></span>                     | <span data-ttu-id="dd54e-203">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-203">CC007</span></span>                   |
| <span data-ttu-id="dd54e-204">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="dd54e-204">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="dd54e-205">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-205">CC001</span></span>                     | <span data-ttu-id="dd54e-206">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-206">CC001</span></span>                   |
| <span data-ttu-id="dd54e-207">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="dd54e-207">&nbsp;&nbsp;Production</span></span>    |                           |                         |
| <span data-ttu-id="dd54e-208">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="dd54e-208">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="dd54e-209">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-209">CC005</span></span>                     | <span data-ttu-id="dd54e-210">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-210">CC005</span></span>                   |
| <span data-ttu-id="dd54e-211">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="dd54e-211">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="dd54e-212">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-212">CC006</span></span>                     | <span data-ttu-id="dd54e-213">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-213">CC006</span></span>                   |

<span data-ttu-id="dd54e-214">ポリシー要件を満たす分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-214">A dimension hierarchy that meets the policy requirement can be set up as shown here.</span></span>

<span data-ttu-id="dd54e-215">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="dd54e-215">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="dd54e-216">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="dd54e-216">Dimension hierarchy name</span></span> | <span data-ttu-id="dd54e-217">分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-217">Dimension</span></span>     | <span data-ttu-id="dd54e-218">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="dd54e-218">Dimension hierarchy type name</span></span>      |
|--------------------------|---------------|------------------------------------|
| <span data-ttu-id="dd54e-219">原価動作</span><span class="sxs-lookup"><span data-stu-id="dd54e-219">Cost behavior</span></span>            | <span data-ttu-id="dd54e-220">コスト要素</span><span class="sxs-lookup"><span data-stu-id="dd54e-220">Cost elements</span></span> | <span data-ttu-id="dd54e-221">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-221">Dimension classification hierarchy</span></span> |

<span data-ttu-id="dd54e-222">ポリシーの分析コード階層は、以下のように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-222">The dimension hierarchy for the policy can be set up as shown here.</span></span>

<span data-ttu-id="dd54e-223">**分析コード メンバーの範囲**</span><span class="sxs-lookup"><span data-stu-id="dd54e-223">**Dimension member ranges**</span></span>

|   <span data-ttu-id="dd54e-224">ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-224">Nodes</span></span>           |   <span data-ttu-id="dd54e-225">移動元分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-225">From dimension member</span></span>   |   <span data-ttu-id="dd54e-226">移動先分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-226">To dimension member</span></span>   |
|-------------------|---------------------------|-------------------------|
| <span data-ttu-id="dd54e-227">原価動作</span><span class="sxs-lookup"><span data-stu-id="dd54e-227">Cost behavior</span></span>     |                           |                         |
| <span data-ttu-id="dd54e-228">&nbsp;&nbsp;固定費</span><span class="sxs-lookup"><span data-stu-id="dd54e-228">&nbsp;&nbsp;Fixed cost</span></span>    | <span data-ttu-id="dd54e-229">10001</span><span class="sxs-lookup"><span data-stu-id="dd54e-229">10001</span></span>                     | <span data-ttu-id="dd54e-230">10011</span><span class="sxs-lookup"><span data-stu-id="dd54e-230">10011</span></span>                   |
| <span data-ttu-id="dd54e-231">&nbsp;&nbsp;変動費</span><span class="sxs-lookup"><span data-stu-id="dd54e-231">&nbsp;&nbsp;Variable cost</span></span> | <span data-ttu-id="dd54e-232">40001</span><span class="sxs-lookup"><span data-stu-id="dd54e-232">40001</span></span>                     | <span data-ttu-id="dd54e-233">40010</span><span class="sxs-lookup"><span data-stu-id="dd54e-233">40010</span></span>                   |

> [!NOTE]
> <span data-ttu-id="dd54e-234">**分析コード メンバーの範囲** で、ノードは 1:_n_ 分析コード メンバーの範囲を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-234">Under **Dimension member ranges**, a node can contain 1:_n_ dimension member ranges.</span></span> <span data-ttu-id="dd54e-235">分析コード メンバとしてまだ存在していない分析コード メンバー ID を挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-235">You can insert dimension member IDs that don’t yet exist as dimension members.</span></span> <span data-ttu-id="dd54e-236">この方法により、階層が今後弾力性のあるものになります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-236">This approach makes the hierarchy resilient for the future.</span></span>  

### <a name="copy-a-hierarchy"></a><span data-ttu-id="dd54e-237">階層のコピー</span><span class="sxs-lookup"><span data-stu-id="dd54e-237">Copy a hierarchy</span></span>

<span data-ttu-id="dd54e-238">新しい分析コード階層の開始点として、現在の分析コード階層をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-238">You can copy a current dimension hierarchy as the starting point for a new dimension hierarchy.</span></span> <span data-ttu-id="dd54e-239">この方法は、前の分析コード階層を新しい分析コード階層と比較したい場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-239">This approach can be useful if you want to compare the previous dimension hierarchy to the new dimension hierarchy.</span></span>

### <a name="rearrange-nodes-in-a-hierarchy"></a><span data-ttu-id="dd54e-240">階層内のノードの再配置</span><span class="sxs-lookup"><span data-stu-id="dd54e-240">Rearrange nodes in a hierarchy</span></span>

<span data-ttu-id="dd54e-241">構造内の現在のレベル内でノードを上下に移動できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-241">You can move a node up and down within its current level in the structure.</span></span> <span data-ttu-id="dd54e-242">この方法で、**原価管理** ワークスペースのレポート用のノードの順序を並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-242">In this way, you can rearrange the order of nodes for reporting in the **Cost control** workspace.</span></span>

<span data-ttu-id="dd54e-243">ターゲット ノードを選択して、ノードを階層内の新しい場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-243">You move a node to a new location in the hierarchy by selecting the target node.</span></span> <span data-ttu-id="dd54e-244">ノードを移動する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-244">There are two ways to move a node:</span></span>

- <span data-ttu-id="dd54e-245">**下へ移動** – 階層内の現在の位置から選択したノードを移動し、選択したターゲット ノードの **下に** 挿入します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-245">**Move below** – Move the selected node from its current position in the hierarchy, and insert it **under** the selected target node.</span></span>
- <span data-ttu-id="dd54e-246">**後に移動** – 階層内の現在の位置から選択したノードを移動し、階層内のそのレベルの選択したターゲット ノードの **後に** 挿入します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-246">**Move after** – Move the selected node from its current position in the hierarchy, and insert it **after** the selected target node at its level of the hierarchy.</span></span>

> [!NOTE] 
> <span data-ttu-id="dd54e-247">Excel また Power BI では既定で英数字の並べ替え順序を使用しているため、それらのツールにデータをエクスポートする場合はノードの順序は維持されません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-247">The order of the nodes isn't maintained when you export data to Excel or Power BI, because those tools use an alphanumeric sort order by default.</span></span> <span data-ttu-id="dd54e-248">手動で順序を並べ替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-248">You should manually rearrange the order.</span></span>

## <a name="define-dimension-hierarchies-for-reporting"></a><span data-ttu-id="dd54e-249">レポートの分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="dd54e-249">Define dimension hierarchies for reporting</span></span>

<span data-ttu-id="dd54e-250">分析コード階層はレポートにとって重要です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-250">Dimension hierarchies are important for reporting.</span></span> <span data-ttu-id="dd54e-251">それによって個々の組織に適合する特定の構造を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-251">They let you define the specific structure that fits into the individual organization.</span></span> <span data-ttu-id="dd54e-252">分析コード階層のノード レベルでなされる集約により、組織のどのレベルの利害関係者でも任意のレベルのデータを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-252">The aggregations that are done at the node level of the dimension hierarchy let stakeholders at any level of the organization see data at any level.</span></span>

<span data-ttu-id="dd54e-253">分析コード階層は、次のレポート ツールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-253">Dimension hierarchies are available in the following reporting tools.</span></span> <span data-ttu-id="dd54e-254">この方法は、レポート構造の一貫性を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-254">This approach helps guarantee consistency in the reporting structure.</span></span>

- <span data-ttu-id="dd54e-255">**原価管理** ワークスペース (クライアント):</span><span class="sxs-lookup"><span data-stu-id="dd54e-255">**Cost control** workspace (Client):</span></span>

    - <span data-ttu-id="dd54e-256">コンフィギュレーションによる管理。</span><span class="sxs-lookup"><span data-stu-id="dd54e-256">Controlled by configuration.</span></span>

- <span data-ttu-id="dd54e-257">**原価管理** ワークスペース (モバイル アプリケーション):</span><span class="sxs-lookup"><span data-stu-id="dd54e-257">**Cost control** workspace (Mobile application):</span></span>

    - <span data-ttu-id="dd54e-258">コンフィギュレーションによる管理。</span><span class="sxs-lookup"><span data-stu-id="dd54e-258">Controlled by configuration.</span></span>

- <span data-ttu-id="dd54e-259">Excel</span><span class="sxs-lookup"><span data-stu-id="dd54e-259">Excel</span></span>

    - <span data-ttu-id="dd54e-260">エクスポート定義ごとの特定の分析コード階層を選択するためのオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-260">Provides the option to select specific dimension hierarchies per export definition:</span></span>

        - <span data-ttu-id="dd54e-261">1 つのコスト要素分析コード階層 (必須)</span><span class="sxs-lookup"><span data-stu-id="dd54e-261">One cost element dimension hierarchy (mandatory)</span></span>
        - <span data-ttu-id="dd54e-262">1 つのコスト オブジェクト分析コード階層 (オプション)</span><span class="sxs-lookup"><span data-stu-id="dd54e-262">One cost object dimension hierarchy (optional)</span></span>
        - <span data-ttu-id="dd54e-263">1 つの統計分析コード階層 (オプション)</span><span class="sxs-lookup"><span data-stu-id="dd54e-263">One statistical dimension hierarchy (optional)</span></span>

- <span data-ttu-id="dd54e-264">Power BI:</span><span class="sxs-lookup"><span data-stu-id="dd54e-264">Power BI:</span></span>

    - <span data-ttu-id="dd54e-265">すべての分析コード階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-265">All dimension hierarchies are available.</span></span>
    
<span data-ttu-id="dd54e-266">Excel または Power BI を使用してレポートを作成する場合は、分析コード階層の最初の 15 レベルのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-266">If you create reports by using Excel or Power BI, only the first 15 levels of the dimension hierarchies are exported.</span></span> <span data-ttu-id="dd54e-267">この制限があるのは、Excel も Power BI も固定スキーマを必要とするためです。</span><span class="sxs-lookup"><span data-stu-id="dd54e-267">This limitation exists because a fixed schema is required in Excel and Power BI.</span></span> <span data-ttu-id="dd54e-268">階層に 15 より多いレベルがある場合は、追加のレベルはエクスポートされません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-268">If a hierarchy has more than 15 levels, the additional levels won't be exported.</span></span> <span data-ttu-id="dd54e-269">正規化テーブルには、階層内の各分析コード メンバーのレコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dd54e-269">The normalized table contains a record for each dimension member in the hierarchy.</span></span> <span data-ttu-id="dd54e-270">そのため、自動化集約が行われます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-270">Therefore, automated aggregation occurs.</span></span> <span data-ttu-id="dd54e-271">この動作は、階層内の使用可能な 15 のレベルのいずれの残高も正しいことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-271">This behavior helps guarantee that the balances at any of the 15 available levels in the hierarchy are still correct.</span></span>

<span data-ttu-id="dd54e-272">次の例では、レポート構造における分析コード階層の例を示します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-272">The following example shows what a dimension hierarchy might look like in the reporting structure.</span></span>

| <span data-ttu-id="dd54e-273">コスト オブジェクト分析コード階層 - レベル 1</span><span class="sxs-lookup"><span data-stu-id="dd54e-273">Cost object dimension hierarchy – Level 1</span></span> | <span data-ttu-id="dd54e-274">コスト オブジェクト分析コード階層 - レベル 2</span><span class="sxs-lookup"><span data-stu-id="dd54e-274">Cost object dimension hierarchy – Level 2</span></span> | <span data-ttu-id="dd54e-275">コスト オブジェクト分析コード階層 - レベル 3</span><span class="sxs-lookup"><span data-stu-id="dd54e-275">Cost object dimension hierarchy – Level 3</span></span> | <span data-ttu-id="dd54e-276">コスト オブジェクト分析コード階層 - レベル 4</span><span class="sxs-lookup"><span data-stu-id="dd54e-276">Cost object dimension hierarchy – Level 4</span></span> | <span data-ttu-id="dd54e-277">コスト オブジェクト分析コード階層 - レベル 15</span><span class="sxs-lookup"><span data-stu-id="dd54e-277">Cost object dimension hierarchy – Level 15</span></span> |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| <span data-ttu-id="dd54e-278">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-278">Organization</span></span>                              | <span data-ttu-id="dd54e-279">管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-279">Admin</span></span>                                     | <span data-ttu-id="dd54e-280">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-280">Finance</span></span>                                   | <span data-ttu-id="dd54e-281">CC002</span><span class="sxs-lookup"><span data-stu-id="dd54e-281">CC002</span></span>                                     |                                            |
| <span data-ttu-id="dd54e-282">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-282">Organization</span></span>                              | <span data-ttu-id="dd54e-283">管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-283">Admin</span></span>                                     | <span data-ttu-id="dd54e-284">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-284">Finance</span></span>                                   | <span data-ttu-id="dd54e-285">CC003</span><span class="sxs-lookup"><span data-stu-id="dd54e-285">CC003</span></span>                                     |                                            |
| <span data-ttu-id="dd54e-286">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-286">Organization</span></span>                              | <span data-ttu-id="dd54e-287">管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-287">Admin</span></span>                                     | <span data-ttu-id="dd54e-288">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-288">Finance</span></span>                                   | <span data-ttu-id="dd54e-289">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-289">CC007</span></span>                                     |                                            |
| <span data-ttu-id="dd54e-290">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-290">Organization</span></span>                              | <span data-ttu-id="dd54e-291">管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-291">Admin</span></span>                                     | <span data-ttu-id="dd54e-292">HR</span><span class="sxs-lookup"><span data-stu-id="dd54e-292">HR</span></span>                                        | <span data-ttu-id="dd54e-293">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-293">CC001</span></span>                                     |                                            |
| <span data-ttu-id="dd54e-294">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-294">Organization</span></span>                              | <span data-ttu-id="dd54e-295">生産</span><span class="sxs-lookup"><span data-stu-id="dd54e-295">Production</span></span>                                | <span data-ttu-id="dd54e-296">梱包業</span><span class="sxs-lookup"><span data-stu-id="dd54e-296">Packaging</span></span>                                 | <span data-ttu-id="dd54e-297">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-297">CC005</span></span>                                     |                                            |
| <span data-ttu-id="dd54e-298">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-298">Organization</span></span>                              | <span data-ttu-id="dd54e-299">生産</span><span class="sxs-lookup"><span data-stu-id="dd54e-299">Production</span></span>                                | <span data-ttu-id="dd54e-300">組み立て</span><span class="sxs-lookup"><span data-stu-id="dd54e-300">Assembly</span></span>                                  | <span data-ttu-id="dd54e-301">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-301">CC006</span></span>                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a><span data-ttu-id="dd54e-302">レポートのために使用される分析コード階層の更新</span><span class="sxs-lookup"><span data-stu-id="dd54e-302">Update the dimension hierarchies that are used for reporting</span></span> 

<span data-ttu-id="dd54e-303">時間と共に、前述のレポート作成ツールで使用されている分析コード階層を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-303">Over time, the dimension hierarchies that are used in the previously mentioned reporting tools will have to be updated.</span></span> <span data-ttu-id="dd54e-304">分析コード階層を更新するには、クライアントを更新します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-304">You can update dimension hierarchies by refreshing the client.</span></span>

- <span data-ttu-id="dd54e-305">**原価管理** ワークスペース (クライアント)</span><span class="sxs-lookup"><span data-stu-id="dd54e-305">**Cost control** workspace (Client)</span></span>
- <span data-ttu-id="dd54e-306">**原価管理** ワークスペース (モバイル アプリケーション)</span><span class="sxs-lookup"><span data-stu-id="dd54e-306">**Cost control** workspace (Mobile application)</span></span>

<span data-ttu-id="dd54e-307">分析コード階層の更新は、事前キャッシュしたジョブで 24 時間ごとに取得します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-307">Updates to dimension hierarchies are picked up every 24 hours by a pre-cached job.</span></span> <span data-ttu-id="dd54e-308">エクスポートしたデータが更新された後は、次のツールで更新済の分析コード階層が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-308">After the exported data is updated, the updated dimension hierarchies are available in the following tools:</span></span>

- <span data-ttu-id="dd54e-309">Excel</span><span class="sxs-lookup"><span data-stu-id="dd54e-309">Excel</span></span>
- <span data-ttu-id="dd54e-310">Power BI</span><span class="sxs-lookup"><span data-stu-id="dd54e-310">Power BI</span></span>

> [!NOTE] 
> <span data-ttu-id="dd54e-311">分析コード階層キャッシュの更新を手動で開始するため、更新する必要のある分析コード階層用に Excel への新しいエクスポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-311">To manually trigger an update of the dimension hierarchy cache, you can create a new export to Excel for the dimension hierarchy or hierarchies that must be updated.</span></span>

## <a name="define-dimension-hierarchies-for-cost-policies"></a><span data-ttu-id="dd54e-312">コスト ポリシーの分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="dd54e-312">Define dimension hierarchies for cost policies</span></span>

<span data-ttu-id="dd54e-313">原価会計は、詳細なルールを定義している複数のポリシーで構成されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-313">Cost accounting consists of multiple policies where detailed rules are defined.</span></span> <span data-ttu-id="dd54e-314">次のポリシーのために 1 つまたは複数の分析コード階層を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-314">You must define one or more dimension hierarchies for the following policies:</span></span>

- <span data-ttu-id="dd54e-315">原価動作</span><span class="sxs-lookup"><span data-stu-id="dd54e-315">Cost behavior</span></span>
- <span data-ttu-id="dd54e-316">原価配分</span><span class="sxs-lookup"><span data-stu-id="dd54e-316">Cost distribution</span></span>
- <span data-ttu-id="dd54e-317">原価配賦</span><span class="sxs-lookup"><span data-stu-id="dd54e-317">Cost allocation</span></span>
- <span data-ttu-id="dd54e-318">原価ロールアップ</span><span class="sxs-lookup"><span data-stu-id="dd54e-318">Cost rollup</span></span>

<span data-ttu-id="dd54e-319">分析コード階層によりルールが作成しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-319">Dimension hierarchies make it easy to create rules.</span></span> <span data-ttu-id="dd54e-320">すべての分析コード メンバーのルールを作成しなくてよいように、分析コード階層レベルが提供する分析コード メンバーの集約を利用できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-320">To avoid having to create rules for every dimension member, you can take advantage of the aggregations of dimension members that are provided by dimension hierarchy levels.</span></span> <span data-ttu-id="dd54e-321">重複するルールがある場合、間接費の計算時にシステムが考慮する特定のルールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-321">If you have overlapping rules, you must define specific rules that the system will consider when it does the overhead calculation.</span></span>

### <a name="example-define-a-cost-behavior-policy"></a><span data-ttu-id="dd54e-322">例: コスト動作ポリシーを定義する</span><span class="sxs-lookup"><span data-stu-id="dd54e-322">Example: Define a cost behavior policy</span></span>

<span data-ttu-id="dd54e-323">以下のように、新しいコスト動作ポリシーが作成され、適切な分析コード階層がポリシーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-323">A new cost behavior policy is created, and appropriate dimension hierarchies are assigned to the policy, as shown here.</span></span>

<span data-ttu-id="dd54e-324">**コスト動作ポリシー**</span><span class="sxs-lookup"><span data-stu-id="dd54e-324">**Cost behavior policy**</span></span>

| <span data-ttu-id="dd54e-325">ポリシー名</span><span class="sxs-lookup"><span data-stu-id="dd54e-325">Policy name</span></span>   | <span data-ttu-id="dd54e-326">原価要素分析コード階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-326">Cost element dimension hierarchy</span></span> | <span data-ttu-id="dd54e-327">原価オブジェクト分析コード階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-327">Cost object dimension hierarchy</span></span> | <span data-ttu-id="dd54e-328">会計通貨</span><span class="sxs-lookup"><span data-stu-id="dd54e-328">Accounting currency</span></span> |
|---------------|----------------------------------|---------------------------------|---------------------|
| <span data-ttu-id="dd54e-329">原価動作</span><span class="sxs-lookup"><span data-stu-id="dd54e-329">Cost behavior</span></span> | <span data-ttu-id="dd54e-330">原価動作</span><span class="sxs-lookup"><span data-stu-id="dd54e-330">Cost behavior</span></span>                    | <span data-ttu-id="dd54e-331">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-331">Organization</span></span>                    | <span data-ttu-id="dd54e-332">USD</span><span class="sxs-lookup"><span data-stu-id="dd54e-332">USD</span></span>                 |

<span data-ttu-id="dd54e-333">**ルール**</span><span class="sxs-lookup"><span data-stu-id="dd54e-333">**Rules**</span></span>

| <span data-ttu-id="dd54e-334">原価要素分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-334">Cost element dimension hierarchy node</span></span> | <span data-ttu-id="dd54e-335">原価オブジェクト分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-335">Cost object dimension hierarchy node</span></span> | <span data-ttu-id="dd54e-336">固定割合</span><span class="sxs-lookup"><span data-stu-id="dd54e-336">Fixed percentage</span></span> | <span data-ttu-id="dd54e-337">固定金額</span><span class="sxs-lookup"><span data-stu-id="dd54e-337">Fixed amount</span></span> | <span data-ttu-id="dd54e-338">発効日</span><span class="sxs-lookup"><span data-stu-id="dd54e-338">Valid from</span></span> | <span data-ttu-id="dd54e-339">失効日</span><span class="sxs-lookup"><span data-stu-id="dd54e-339">Valid to</span></span> |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| <span data-ttu-id="dd54e-340">固定費</span><span class="sxs-lookup"><span data-stu-id="dd54e-340">Fixed cost</span></span>                            | <span data-ttu-id="dd54e-341">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-341">Organization</span></span>                         | <span data-ttu-id="dd54e-342">100.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-342">100.00</span></span>           | <span data-ttu-id="dd54e-343">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-343">0.00</span></span>         | <span data-ttu-id="dd54e-344">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-344">1/1/2017</span></span>   | <span data-ttu-id="dd54e-345">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-345">Never</span></span>    |
| <span data-ttu-id="dd54e-346">10001</span><span class="sxs-lookup"><span data-stu-id="dd54e-346">10001</span></span>                                 | <span data-ttu-id="dd54e-347">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-347">Organization</span></span>                         | <span data-ttu-id="dd54e-348">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-348">0.00</span></span>             | <span data-ttu-id="dd54e-349">150.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-349">150.00</span></span>       | <span data-ttu-id="dd54e-350">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-350">1/1/2017</span></span>   | <span data-ttu-id="dd54e-351">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-351">Never</span></span>    |
| <span data-ttu-id="dd54e-352">10001 (\*)</span><span class="sxs-lookup"><span data-stu-id="dd54e-352">10001 (\*)</span></span>                             | <span data-ttu-id="dd54e-353">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-353">Finance</span></span>                              |                  | <span data-ttu-id="dd54e-354">50.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-354">50.00</span></span>        | <span data-ttu-id="dd54e-355">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-355">1/1/2017</span></span>   | <span data-ttu-id="dd54e-356">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-356">Never</span></span>    |
| <span data-ttu-id="dd54e-357">コスト動作や変動費 (\*\*)</span><span class="sxs-lookup"><span data-stu-id="dd54e-357">Cost behavior or Variable cost (\*\*)</span></span>   | <span data-ttu-id="dd54e-358">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-358">Organization</span></span>                         | <span data-ttu-id="dd54e-359">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-359">0.00</span></span>             | <span data-ttu-id="dd54e-360">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-360">0.00</span></span>         | <span data-ttu-id="dd54e-361">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-361">1/1/2017</span></span>   | <span data-ttu-id="dd54e-362">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-362">Never</span></span>    |

<span data-ttu-id="dd54e-363">\* 変動費ノードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-363">\* The variable cost node isn't required.</span></span> <span data-ttu-id="dd54e-364">コストが固定費に分類されていない場合は、変動費になります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-364">If a cost isn't classified as a fixed cost, it must be a variable cost.</span></span>

<span data-ttu-id="dd54e-365">\*\* コスト要素メンバー 10001 と財務階層レベル (CC002、CC003、CC007) の下で集約されるすべてのコスト オブジェクト メンバーの組み合わせに対して詳細なルールが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-365">\*\* A detailed rule is created for the combination of cost element member 10001 and all cost object members that are aggregated under the Finance hierarchy level (CC002, CC003, CC007).</span></span>

<span data-ttu-id="dd54e-366">前述のルールは分析コード階層が提供する柔軟性を示します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-366">The preceding rules show the flexibility that dimension hierarchies provide.</span></span> <span data-ttu-id="dd54e-367">高レベルのルールを定義することで、メンテナンスを最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-367">By defining high-level rules, you can help minimize maintenance.</span></span> <span data-ttu-id="dd54e-368">特定の業務目標に適合する詳細なルールを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-368">You can then define detailed rules to fit into a specific business objective.</span></span>

<span data-ttu-id="dd54e-369">ルール内で使用する分析コード階層が更新される場合、システムが自動的に更新を進めます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-369">If the dimension hierarchies that are used in rules are updated, the system automatically brings the updates forward.</span></span>

<span data-ttu-id="dd54e-370">ルール内の粒度のレベルが必要なくなった場合、そのルールを失効にできます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-370">If a level of granularity in the rules is no longer required, the rule can be expired.</span></span>

<span data-ttu-id="dd54e-371">たとえば、財務コスト オブジェクトの分析コード階層ノードの特定のコスト動作ルールが必要でなくなりました。</span><span class="sxs-lookup"><span data-stu-id="dd54e-371">For example, a specific cost behavior rule for the Finance cost object dimension hierarchy node is no longer required.</span></span> <span data-ttu-id="dd54e-372">この場合は、**ルールを失効にする** をクリックしてルールを失効させます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-372">In this case, click **Expire rule** to expire the rule.</span></span>

| <span data-ttu-id="dd54e-373">原価要素分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-373">Cost element dimension hierarchy node</span></span> | <span data-ttu-id="dd54e-374">原価オブジェクト分析コード階層ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-374">Cost object dimension hierarchy node</span></span> | <span data-ttu-id="dd54e-375">固定割合</span><span class="sxs-lookup"><span data-stu-id="dd54e-375">Fixed percentage</span></span> | <span data-ttu-id="dd54e-376">固定金額</span><span class="sxs-lookup"><span data-stu-id="dd54e-376">Fixed amount</span></span> | <span data-ttu-id="dd54e-377">発効日</span><span class="sxs-lookup"><span data-stu-id="dd54e-377">Valid from</span></span> | <span data-ttu-id="dd54e-378">失効日</span><span class="sxs-lookup"><span data-stu-id="dd54e-378">Valid to</span></span>  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| <span data-ttu-id="dd54e-379">固定費</span><span class="sxs-lookup"><span data-stu-id="dd54e-379">Fixed cost</span></span>                            | <span data-ttu-id="dd54e-380">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-380">Organization</span></span>                         | <span data-ttu-id="dd54e-381">100,00</span><span class="sxs-lookup"><span data-stu-id="dd54e-381">100,00</span></span>           | <span data-ttu-id="dd54e-382">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-382">0,00</span></span>         | <span data-ttu-id="dd54e-383">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-383">1/1/2017</span></span>   | <span data-ttu-id="dd54e-384">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-384">Never</span></span>     |
| <span data-ttu-id="dd54e-385">10001</span><span class="sxs-lookup"><span data-stu-id="dd54e-385">10001</span></span>                                 | <span data-ttu-id="dd54e-386">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-386">Organization</span></span>                         | <span data-ttu-id="dd54e-387">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-387">0,00</span></span>             | <span data-ttu-id="dd54e-388">150,00</span><span class="sxs-lookup"><span data-stu-id="dd54e-388">150,00</span></span>       | <span data-ttu-id="dd54e-389">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-389">1/1/2017</span></span>   | <span data-ttu-id="dd54e-390">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-390">Never</span></span>     |
| <span data-ttu-id="dd54e-391">10001</span><span class="sxs-lookup"><span data-stu-id="dd54e-391">10001</span></span>                                 | <span data-ttu-id="dd54e-392">財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-392">Finance</span></span>                              |                  | <span data-ttu-id="dd54e-393">50,00</span><span class="sxs-lookup"><span data-stu-id="dd54e-393">50,00</span></span>        | <span data-ttu-id="dd54e-394">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-394">1/1/2017</span></span>   | <span data-ttu-id="dd54e-395">20/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-395">20/1/2017</span></span> |
| <span data-ttu-id="dd54e-396">コスト動作または変動費</span><span class="sxs-lookup"><span data-stu-id="dd54e-396">Cost behavior or Variable cost</span></span>        | <span data-ttu-id="dd54e-397">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-397">Organization</span></span>                         | <span data-ttu-id="dd54e-398">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-398">0,00</span></span>             | <span data-ttu-id="dd54e-399">0.00</span><span class="sxs-lookup"><span data-stu-id="dd54e-399">0,00</span></span>         | <span data-ttu-id="dd54e-400">1/1/2017</span><span class="sxs-lookup"><span data-stu-id="dd54e-400">1/1/2017</span></span>   | <span data-ttu-id="dd54e-401">許可しない</span><span class="sxs-lookup"><span data-stu-id="dd54e-401">Never</span></span>     |

<span data-ttu-id="dd54e-402">2017 年 1 月 20 日以降に実行される間接費計算は、このルールを考慮しなくなります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-402">Any overhead calculation that is run after January 20, 2017, no longer considers this rule.</span></span>

> [!NOTE] 
> <span data-ttu-id="dd54e-403">**発効日** および **失効日** フィールドは日付と時刻に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-403">The **Valid from** and **Valid to** fields are date-effective and time-effective.</span></span> <span data-ttu-id="dd54e-404">同じ日にルールの失効と新しい間接費の計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-404">You can expire the rule and run a new overhead calculation on the same day.</span></span>

## <a name="define-dimension-hierarchies-for-security-setup"></a><span data-ttu-id="dd54e-405">セキュリティ設定の分析コード階層の定義</span><span class="sxs-lookup"><span data-stu-id="dd54e-405">Define dimension hierarchies for security setup</span></span>

<span data-ttu-id="dd54e-406">原価会計のデータは、レポート単位を担当するすべてのマネージャーに使用可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-406">Cost accounting data should be made available to all managers who are responsible for a reporting unit.</span></span> <span data-ttu-id="dd54e-407">原価会計用語では、レポート単位は、コスト オブジェクトまたは一連のコスト オブジェクトとして表されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-407">In Cost accounting terminology, a reporting unit is represented as a cost object or a set of cost objects.</span></span>

<span data-ttu-id="dd54e-408">すべてのマネージャーは、収益や利益幅といった機密性の高いビジネス データにアクセスできるようになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-408">Potentially, all managers will be able to access highly sensitive business data, such revenues and margins.</span></span> <span data-ttu-id="dd54e-409">そのため、マネージャーが自分に関連のあるデータのみを参照するよう、セキュリティを設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-409">Therefore, it's important that you set up security, so that managers see only the data that is relevant to them.</span></span> <span data-ttu-id="dd54e-410">データ セキュリティを管理するために、分析コード階層を定義します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-410">To help control data security, you define dimension hierarchies.</span></span>

- <span data-ttu-id="dd54e-411">分析コード階層の使用は、分析コード階層参照で選択されている分析コード値がコスト オブジェクト分析コードである場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-411">The use of dimension hierarchies applies only when the dimension value that is selected in the dimension hierarchy reference is a cost object dimension.</span></span>
- <span data-ttu-id="dd54e-412">アクセス リスト階層内のコスト オブジェクト分析コードごとに 1 つの分析コード階層のみを有効にできます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-412">Only one dimension hierarchy can be enabled per cost object dimension in the access list hierarchy.</span></span>

<span data-ttu-id="dd54e-413">**分析コード階層の詳細**</span><span class="sxs-lookup"><span data-stu-id="dd54e-413">**Dimension hierarchy details**</span></span>

| <span data-ttu-id="dd54e-414">分析コード階層名</span><span class="sxs-lookup"><span data-stu-id="dd54e-414">Dimension hierarchy name</span></span> | <span data-ttu-id="dd54e-415">分析コード</span><span class="sxs-lookup"><span data-stu-id="dd54e-415">Dimension</span></span>    | <span data-ttu-id="dd54e-416">分析コード階層タイプ名</span><span class="sxs-lookup"><span data-stu-id="dd54e-416">Dimension hierarchy type name</span></span>      | <span data-ttu-id="dd54e-417">アクセス リスト階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-417">Access list hierarchy</span></span> |
|--------------------------|--------------|------------------------------------|-----------------------|
| <span data-ttu-id="dd54e-418">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-418">Organization</span></span>             | <span data-ttu-id="dd54e-419">コスト センター</span><span class="sxs-lookup"><span data-stu-id="dd54e-419">Cost centers</span></span> | <span data-ttu-id="dd54e-420">分析コード分類階層</span><span class="sxs-lookup"><span data-stu-id="dd54e-420">Dimension classification hierarchy</span></span> | <span data-ttu-id="dd54e-421">**有**</span><span class="sxs-lookup"><span data-stu-id="dd54e-421">**Yes**</span></span>               |

<span data-ttu-id="dd54e-422">新しい **ユーザー** クイック タブは階層デザイナーで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="dd54e-422">A new **Users** FastTab is available in the hierarchy designer.</span></span> <span data-ttu-id="dd54e-423">ここでは、階層内の各ノードに 1 つまたは複数のユーザー ID を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-423">Here, you can insert one or more user IDs at each node in the hierarchy.</span></span>

<span data-ttu-id="dd54e-424">**ユーザーおよびディメンション メンバー範囲**</span><span class="sxs-lookup"><span data-stu-id="dd54e-424">**Users and dimension member ranges**</span></span>

|   <span data-ttu-id="dd54e-425">ノード</span><span class="sxs-lookup"><span data-stu-id="dd54e-425">Nodes</span></span>         |   <span data-ttu-id="dd54e-426">ユーザー ID</span><span class="sxs-lookup"><span data-stu-id="dd54e-426">User ID</span></span>        |   <span data-ttu-id="dd54e-427">移動元分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-427">From dimension member</span></span>   |   <span data-ttu-id="dd54e-428">移動先分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="dd54e-428">To dimension member</span></span>   |
|-----------------|------------------|---------------------------|-------------------------|
| <span data-ttu-id="dd54e-429">組織</span><span class="sxs-lookup"><span data-stu-id="dd54e-429">Organization</span></span>    | <span data-ttu-id="dd54e-430">ベンジャミン、クレア</span><span class="sxs-lookup"><span data-stu-id="dd54e-430">Benjamin, Claire</span></span> |                           |                         |
| <span data-ttu-id="dd54e-431">&nbsp;&nbsp;管理者</span><span class="sxs-lookup"><span data-stu-id="dd54e-431">&nbsp;&nbsp;Admin</span></span>         | <span data-ttu-id="dd54e-432">4 月</span><span class="sxs-lookup"><span data-stu-id="dd54e-432">April</span></span>            |                           |                         |
| <span data-ttu-id="dd54e-433">&nbsp;&nbsp;&nbsp;&nbsp;財務</span><span class="sxs-lookup"><span data-stu-id="dd54e-433">&nbsp;&nbsp;&nbsp;&nbsp;Finance</span></span>   | <span data-ttu-id="dd54e-434">アリシア</span><span class="sxs-lookup"><span data-stu-id="dd54e-434">Alicia</span></span>           | <span data-ttu-id="dd54e-435">CC002</span><span class="sxs-lookup"><span data-stu-id="dd54e-435">CC002</span></span>                     | <span data-ttu-id="dd54e-436">CC003</span><span class="sxs-lookup"><span data-stu-id="dd54e-436">CC003</span></span>                   |
|                 |                  | <span data-ttu-id="dd54e-437">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-437">CC007</span></span>                     | <span data-ttu-id="dd54e-438">CC007</span><span class="sxs-lookup"><span data-stu-id="dd54e-438">CC007</span></span>                   |
| <span data-ttu-id="dd54e-439">&nbsp;&nbsp;&nbsp;&nbsp;HR</span><span class="sxs-lookup"><span data-stu-id="dd54e-439">&nbsp;&nbsp;&nbsp;&nbsp;HR</span></span>        | <span data-ttu-id="dd54e-440">アーニー</span><span class="sxs-lookup"><span data-stu-id="dd54e-440">Arnie</span></span>            | <span data-ttu-id="dd54e-441">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-441">CC001</span></span>                     | <span data-ttu-id="dd54e-442">CC001</span><span class="sxs-lookup"><span data-stu-id="dd54e-442">CC001</span></span>                   |
| <span data-ttu-id="dd54e-443">&nbsp;&nbsp;生産</span><span class="sxs-lookup"><span data-stu-id="dd54e-443">&nbsp;&nbsp;Production</span></span>    | <span data-ttu-id="dd54e-444">デビッド</span><span class="sxs-lookup"><span data-stu-id="dd54e-444">David</span></span>            |                           |                         |
| <span data-ttu-id="dd54e-445">&nbsp;&nbsp;&nbsp;&nbsp;梱包業</span><span class="sxs-lookup"><span data-stu-id="dd54e-445">&nbsp;&nbsp;&nbsp;&nbsp;Packaging</span></span> | <span data-ttu-id="dd54e-446">エレン</span><span class="sxs-lookup"><span data-stu-id="dd54e-446">Ellen</span></span>            | <span data-ttu-id="dd54e-447">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-447">CC005</span></span>                     | <span data-ttu-id="dd54e-448">CC005</span><span class="sxs-lookup"><span data-stu-id="dd54e-448">CC005</span></span>                   |
| <span data-ttu-id="dd54e-449">&nbsp;&nbsp;&nbsp;&nbsp;組み立て</span><span class="sxs-lookup"><span data-stu-id="dd54e-449">&nbsp;&nbsp;&nbsp;&nbsp;Assembly</span></span>  | <span data-ttu-id="dd54e-450">クリス</span><span class="sxs-lookup"><span data-stu-id="dd54e-450">Chris</span></span>            | <span data-ttu-id="dd54e-451">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-451">CC006</span></span>                     | <span data-ttu-id="dd54e-452">CC006</span><span class="sxs-lookup"><span data-stu-id="dd54e-452">CC006</span></span>                   |

> [!NOTE] 
> <span data-ttu-id="dd54e-453">原価計算のすべてのエントリを表示できるように、原価経理担当者は階層の最上部に割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-453">Cost accountants should be assigned to the top level of the hierarchy, so that they can see all entries in Cost accounting.</span></span>

<span data-ttu-id="dd54e-454">アクセス リスト階層とそのセキュリティ設定を有効にするには、**原価会計** > **設定** > **パラメーター** > **一般** に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-454">To enable the access list hierarchy and its security settings, go to **Cost accounting** > **Setup** > **Parameters** > **General**.</span></span> <span data-ttu-id="dd54e-455">**コスト オブジェクト分析コード メンバーに対する表示アクセスの有効化** パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-455">Select the **Enable view access for cost object dimension members** parameter.</span></span>

<span data-ttu-id="dd54e-456">アクセス リスト階層の設定は、次の領域に表示されるデータを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="dd54e-456">The settings for the access list hierarchy are used to control the data that is shown in the following areas:</span></span>

- <span data-ttu-id="dd54e-457">**原価管理** ワークスペース (クライアント):</span><span class="sxs-lookup"><span data-stu-id="dd54e-457">**Cost control** workspace (Client):</span></span>

    - <span data-ttu-id="dd54e-458">シナリオをドリルスルーするために使用されるフォーム内のデータ</span><span class="sxs-lookup"><span data-stu-id="dd54e-458">Data in forms that are used to drill through scenarios</span></span>

- <span data-ttu-id="dd54e-459">**原価管理** ワークスペース (モバイル アプリケーション):</span><span class="sxs-lookup"><span data-stu-id="dd54e-459">**Cost control** workspace (Mobile application):</span></span>

    - <span data-ttu-id="dd54e-460">カードの残高</span><span class="sxs-lookup"><span data-stu-id="dd54e-460">Balances in cards</span></span>

- <span data-ttu-id="dd54e-461">Power BI:</span><span class="sxs-lookup"><span data-stu-id="dd54e-461">Power BI:</span></span>

    - <span data-ttu-id="dd54e-462">Power BI ビジュアル化に表示されるデータ</span><span class="sxs-lookup"><span data-stu-id="dd54e-462">Data that is shown in Power BI visualizations</span></span>
    - <span data-ttu-id="dd54e-463">Dynamics 365 Finance クライアントに埋め込まれた Power BI ビジュアル化データ</span><span class="sxs-lookup"><span data-stu-id="dd54e-463">Data Power BI visualizations that are embedded in the Dynamics 365 Finance client</span></span>

> [!NOTE] 
> - <span data-ttu-id="dd54e-464">アクセス リスト階層が Power BI のデータに影響を及ぼす前に、アクセス リスト階層と Power BI の行レベルのセキュリティがペアリングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd54e-464">Before the access list hierarchy can affect data in Power BI, access list hierarchy and row-level security in Power BI must be paired.</span></span> <span data-ttu-id="dd54e-465">詳細については、「[原価会計コンテンツ パックのセキュリティ設定](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd54e-465">For more information, see [Set up security for Cost accounting content pack](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).</span></span>
> - <span data-ttu-id="dd54e-466">アクセス リスト階層は、Excel へのデータのエクスポートの保護には役立ちません。</span><span class="sxs-lookup"><span data-stu-id="dd54e-466">The access list hierarchy doesn't help secure the export of data to Excel.</span></span> <span data-ttu-id="dd54e-467">したがって、そのレポート ツールは、データの表示に完全なアクセス権を持つ必要があるコスト経理担当者およびマネージャーのみが使用します。</span><span class="sxs-lookup"><span data-stu-id="dd54e-467">Therefore, that reporting tool should be used only by cost accountants and managers who must have full access to view the data.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]