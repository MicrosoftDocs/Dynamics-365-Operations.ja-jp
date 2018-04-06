---
title: "倉庫作業ポリシー"
description: "倉庫作業ポリシーは、ワーク オーダーのタイプ、在庫場所、および製品に基づいて、製造の倉庫プロセスのために倉庫作業が作成されるかどうかをコントロールします。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: a0c900dc208736f1823be50e8522061406c9f126
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="88f25-103">倉庫作業ポリシー</span><span class="sxs-lookup"><span data-stu-id="88f25-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="88f25-104">Microsoft Dynamics 365 for Finance and Operations で倉庫作業ポリシーは、ワーク オーダーのタイプ、在庫場所、および製品に基づいて、製造の倉庫プロセスのために倉庫作業が作成されるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="88f25-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="88f25-105">この作業ポリシーは、製造の倉庫プロセスのために倉庫作業が作成されるかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="88f25-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="88f25-106">**作業オーダー タイプ**、**在庫場所**、および**製品**の組み合わせを使用して作業ポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="88f25-107">たとえば、製品 L0101 は、出荷場所 001 に完了済として報告されます。</span><span class="sxs-lookup"><span data-stu-id="88f25-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="88f25-108">完成品は、後に出荷場所 001 で別の製造オーダーに消費されます。</span><span class="sxs-lookup"><span data-stu-id="88f25-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="88f25-109">この場合、出荷場所 001 に完了済として L0101 製品の報告の際に、作成から完成品のプット アウェイの作業を回避するために作業ポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="88f25-110">作業ポリシーは次の情報を表すことができる個々のエンティティです:</span><span class="sxs-lookup"><span data-stu-id="88f25-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="88f25-111">**作業ポリシー名** (作業ポリシーの固有の ID)</span><span class="sxs-lookup"><span data-stu-id="88f25-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="88f25-112">**ワーク オーダー タイプ** と **作業作成方法**</span><span class="sxs-lookup"><span data-stu-id="88f25-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="88f25-113">**在庫場所**</span><span class="sxs-lookup"><span data-stu-id="88f25-113">**Inventory locations**</span></span>
-   <span data-ttu-id="88f25-114">**製品**</span><span class="sxs-lookup"><span data-stu-id="88f25-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="88f25-115">ワーク オーダー タイプ</span><span class="sxs-lookup"><span data-stu-id="88f25-115">Work order types</span></span>
<span data-ttu-id="88f25-116">次のワーク オーダー タイプから選択できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="88f25-117">完成品のプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="88f25-117">Finished goods put away</span></span>
-   <span data-ttu-id="88f25-118">連産物と副産物のプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="88f25-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="88f25-119">原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="88f25-119">Raw material picking</span></span>

<span data-ttu-id="88f25-120">[**作業作成方法**] のフィールドは、値が**なし**になります。</span><span class="sxs-lookup"><span data-stu-id="88f25-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="88f25-121">この値は、作業ポリシーが選択したワーク オーダー タイプのために作成された倉庫作業を防ぐことを示します。</span><span class="sxs-lookup"><span data-stu-id="88f25-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="88f25-122">在庫場所</span><span class="sxs-lookup"><span data-stu-id="88f25-122">Inventory locations</span></span>
<span data-ttu-id="88f25-123">作業ポリシーが適用される場所を選択できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="88f25-124">場所は作業ポリシーに関連付けられなければ、作業ポリシーはプロセスに適用されません。</span><span class="sxs-lookup"><span data-stu-id="88f25-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="88f25-125">[**場所**] ページで、特定の場所の作業ポリシーの選択を選択するか、またはキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="88f25-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="88f25-126">製品</span><span class="sxs-lookup"><span data-stu-id="88f25-126">Products</span></span>
<span data-ttu-id="88f25-127">作業ポリシーが適用される製品を選択できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="88f25-128">すべての製品または選択した製品に作業ポリシーを適用できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="88f25-129">例</span><span class="sxs-lookup"><span data-stu-id="88f25-129">Example</span></span>
<span data-ttu-id="88f25-130">次の例では、2 つの製造オーダー、PRD-001 と PRD-00*2* があります。</span><span class="sxs-lookup"><span data-stu-id="88f25-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="88f25-131">製品オーダー PRD-001 は、製品 SC1 が場所 O1 に完了済として報告される**組み立て**として名付けられた工程があります。</span><span class="sxs-lookup"><span data-stu-id="88f25-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="88f25-132">製造オーダー PRD-002 には、**塗装**と名付けられた、および場所 O1 から製品 SC1 の消費の工程があります。</span><span class="sxs-lookup"><span data-stu-id="88f25-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="88f25-133">製造オーダー PRD-002 は、場所 O1 からの原材料消費 RM1 も消費します。</span><span class="sxs-lookup"><span data-stu-id="88f25-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="88f25-134">RM1 は、倉庫の場所 BULK-001 に保存され、原材料のピッキングの倉庫作業によって場所 O1 がピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="88f25-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="88f25-135">ピッキング作業は、生産 PRD-002 がリリースされるときに生成されます。</span><span class="sxs-lookup"><span data-stu-id="88f25-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="88f25-136">[![倉庫作業ポリシー](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="88f25-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="88f25-137">このシナリオの倉庫作業ポリシーをコンフィギュレーションする計画の場合、次の情報を考慮する必要があります:</span><span class="sxs-lookup"><span data-stu-id="88f25-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="88f25-138">完成品のプット アウェイの倉庫作業は、製造オーダー PRD-001 から場所 O1 に完成済として 製品 SC1 を報告するときに必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="88f25-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="88f25-139">これは、製造オーダー PRD-002 の**塗装**工程が同じ場所で SC1 を消費するためです。</span><span class="sxs-lookup"><span data-stu-id="88f25-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="88f25-140">原材料ピッキングの倉庫作業は、倉庫の場所 BULK-001 から場所 O1 へ原材料 RM1 を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88f25-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="88f25-141">次の例では、これらの考慮事項に基づいて、設定できる作業ポリシーついて示しています。</span><span class="sxs-lookup"><span data-stu-id="88f25-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="88f25-142">**作業ポリシー名**</span><span class="sxs-lookup"><span data-stu-id="88f25-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="88f25-143">**ワーク オーダー タイプ**</span><span class="sxs-lookup"><span data-stu-id="88f25-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="88f25-144">プット アウェイ 01 なし     \`</span><span class="sxs-lookup"><span data-stu-id="88f25-144">No put away 01     \`</span></span>                    |<span data-ttu-id="88f25-145">- 完成品のプット アウェイ</span><span class="sxs-lookup"><span data-stu-id="88f25-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="88f25-146">**場所**</span><span class="sxs-lookup"><span data-stu-id="88f25-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="88f25-147">- O1</span><span class="sxs-lookup"><span data-stu-id="88f25-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="88f25-148">**製品**</span><span class="sxs-lookup"><span data-stu-id="88f25-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="88f25-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="88f25-149">- SC1</span></span>                                                  |

<span data-ttu-id="88f25-150">次の手順は、このシナリオの倉庫作業ポリシーを設定する方法の手順を示します。</span><span class="sxs-lookup"><span data-stu-id="88f25-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="88f25-151">サンプルはセットアップを示し、ライセンス プレート制御ではない場所に完了済として製造オーダーをレポートする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="88f25-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="88f25-152">倉庫作業ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="88f25-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="88f25-153">倉庫のプロセスは倉庫作業を常に含みません。</span><span class="sxs-lookup"><span data-stu-id="88f25-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="88f25-154">作業ポリシーを定義して、原材料のピッキングの作業の作成、および特定の場所での一連の製品に対する完成品のプット アウェイを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="88f25-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="88f25-155">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="88f25-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="88f25-156">ステップ (21)</span><span class="sxs-lookup"><span data-stu-id="88f25-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="88f25-157">1.</span><span class="sxs-lookup"><span data-stu-id="88f25-157">1.</span></span>  | <span data-ttu-id="88f25-158">[倉庫管理] &gt; [設定] &gt; [作業] &gt; [作業ポリシー] に移動します。</span><span class="sxs-lookup"><span data-stu-id="88f25-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="88f25-159">2.</span><span class="sxs-lookup"><span data-stu-id="88f25-159">2.</span></span>  | <span data-ttu-id="88f25-160">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="88f25-161">3.</span><span class="sxs-lookup"><span data-stu-id="88f25-161">3.</span></span>  | <span data-ttu-id="88f25-162">[作業ポリシー名] フィールドに、「プット アウェイ作業なし」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88f25-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="88f25-163">4.</span><span class="sxs-lookup"><span data-stu-id="88f25-163">4.</span></span>  | <span data-ttu-id="88f25-164">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="88f25-165">5.</span><span class="sxs-lookup"><span data-stu-id="88f25-165">5.</span></span>  | <span data-ttu-id="88f25-166">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="88f25-167">6.</span><span class="sxs-lookup"><span data-stu-id="88f25-167">6.</span></span>  | <span data-ttu-id="88f25-168">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88f25-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="88f25-169">7.</span><span class="sxs-lookup"><span data-stu-id="88f25-169">7.</span></span>  | <span data-ttu-id="88f25-170">[ワーク オーダー タイプ] フィールドで、[完成品のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="88f25-171">8.</span><span class="sxs-lookup"><span data-stu-id="88f25-171">8.</span></span>  | <span data-ttu-id="88f25-172">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="88f25-173">9.</span><span class="sxs-lookup"><span data-stu-id="88f25-173">9.</span></span>  | <span data-ttu-id="88f25-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88f25-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="88f25-175">10。</span><span class="sxs-lookup"><span data-stu-id="88f25-175">10.</span></span> | <span data-ttu-id="88f25-176">[ワーク オーダー タイプ] フィールドで、[連産物と副産物のプット アウェイ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="88f25-177">11。</span><span class="sxs-lookup"><span data-stu-id="88f25-177">11.</span></span> | <span data-ttu-id="88f25-178">[在庫場所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="88f25-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="88f25-179">12。</span><span class="sxs-lookup"><span data-stu-id="88f25-179">12.</span></span> | <span data-ttu-id="88f25-180">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="88f25-181">13</span><span class="sxs-lookup"><span data-stu-id="88f25-181">13.</span></span> | <span data-ttu-id="88f25-182">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88f25-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="88f25-183">14。</span><span class="sxs-lookup"><span data-stu-id="88f25-183">14.</span></span> | <span data-ttu-id="88f25-184">倉庫の一覧で、「51」を入力します。</span><span class="sxs-lookup"><span data-stu-id="88f25-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="88f25-185">15.</span><span class="sxs-lookup"><span data-stu-id="88f25-185">15.</span></span> | <span data-ttu-id="88f25-186">[場所] フィールドで「001」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="88f25-187">16.</span><span class="sxs-lookup"><span data-stu-id="88f25-187">16.</span></span> | <span data-ttu-id="88f25-188">[製品] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="88f25-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="88f25-189">17.</span><span class="sxs-lookup"><span data-stu-id="88f25-189">17.</span></span> | <span data-ttu-id="88f25-190">[製品の選択] フィールドで、[選択済] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="88f25-191">18.</span><span class="sxs-lookup"><span data-stu-id="88f25-191">18.</span></span> | <span data-ttu-id="88f25-192">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="88f25-193">19.</span><span class="sxs-lookup"><span data-stu-id="88f25-193">19.</span></span> | <span data-ttu-id="88f25-194">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="88f25-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="88f25-195">20.</span><span class="sxs-lookup"><span data-stu-id="88f25-195">20.</span></span> | <span data-ttu-id="88f25-196">[品目番号] フィールドで、「L0101」を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="88f25-197">21.</span><span class="sxs-lookup"><span data-stu-id="88f25-197">21.</span></span> | <span data-ttu-id="88f25-198">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="88f25-199">ライセンス プレートにより制御されていない場所に完了済として製造オーダーを報告します。</span><span class="sxs-lookup"><span data-stu-id="88f25-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="88f25-200">この手順では、ライセンス プレートにより制御されていない場所への完了報告の例を示します。</span><span class="sxs-lookup"><span data-stu-id="88f25-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="88f25-201">適用できる作業ポリシーは、このタスクの前提条件です。</span><span class="sxs-lookup"><span data-stu-id="88f25-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="88f25-202">前の手順では、作業ポリシーの設定を示します。</span><span class="sxs-lookup"><span data-stu-id="88f25-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="88f25-203">ステップ (25)</span><span class="sxs-lookup"><span data-stu-id="88f25-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="88f25-204"><strong>下位タスク: 出荷場所を設定します。</strong></span><span class="sxs-lookup"><span data-stu-id="88f25-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="88f25-205">[組織管理] &gt; [リソース] &gt; [リソース グループ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="88f25-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="88f25-206">一覧で、リソース グループ「5102」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="88f25-207">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="88f25-208">[出荷倉庫] フィールドに、「51」を入力します。</span><span class="sxs-lookup"><span data-stu-id="88f25-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="88f25-209">[出荷場所] フィールドに、「001」を入力します。</span><span class="sxs-lookup"><span data-stu-id="88f25-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="88f25-210">場所 001 はライセンス プレートにより制御される場所ではありません。</span><span class="sxs-lookup"><span data-stu-id="88f25-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="88f25-211">場所に適用できる作業ポリシーが存在する場合にのみ、ライセンス プレートのない出荷場所を設定できます。</span><span class="sxs-lookup"><span data-stu-id="88f25-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="88f25-212"><strong>下位タスク: 製造オーダーを作成して完了済として報告します。</strong></span><span class="sxs-lookup"><span data-stu-id="88f25-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="88f25-213">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88f25-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="88f25-214">[生産管理] &gt; [製造オーダー] &gt; [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88f25-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="88f25-215">[新しい製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="88f25-216">[品目番号] フィールドに、「L0101」を入力します。</span><span class="sxs-lookup"><span data-stu-id="88f25-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="88f25-217">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="88f25-218">アクション ペインで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="88f25-219">[見積] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="88f25-220">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="88f25-221">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="88f25-222">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="88f25-223">[自動 BOM 消費] フィールドで、「なし」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="88f25-224">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="88f25-225">［完了レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="88f25-226">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="88f25-227">[エラー適用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="88f25-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="88f25-228">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="88f25-229">アクション ペインで [倉庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="88f25-230">[作業の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88f25-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="88f25-231">製造オーダーが完了と報告されたときに、作業はプット アウェイに生成されませんでした。</span><span class="sxs-lookup"><span data-stu-id="88f25-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="88f25-232">これは、製品 L0101 が場所 001 に完了として報告されるときに作業が生成されないように作業ポリシーを定義しているために発生します。</span><span class="sxs-lookup"><span data-stu-id="88f25-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




