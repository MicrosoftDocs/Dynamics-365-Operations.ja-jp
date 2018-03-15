---
title: "製品ライフサイクルの状態"
description: "製品ライフサイクルの状態では、リリースされた製品または製品バリアントのライフサイクルの状態をドキュメントします。"
author: cvocph
manager: AnnBe
ms.date: 12/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: conradv
ms.dyn365.ops.version: 7.3
ms.search.validFrom: 2017-12-31
ms.translationtype: HT
ms.sourcegitcommit: 236b0253f20330f09f07dbcfa19257350fb5d37f
ms.openlocfilehash: 8ef72de3f226a3270ac0145a20e4da7dfe64f4ba
ms.contentlocale: ja-jp
ms.lasthandoff: 02/08/2018

---

# <a name="product-lifecycle-state"></a><span data-ttu-id="6409f-103">製品ライフサイクルの状態</span><span class="sxs-lookup"><span data-stu-id="6409f-103">Product lifecycle state</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6409f-104">製品ライフサイクルの状態では、リリースされた製品または製品バリアントのライフサイクルの状態をドキュメントします。</span><span class="sxs-lookup"><span data-stu-id="6409f-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="6409f-105">製品ライフサイクルの状態は、ユーザー、通常は製品マネージャーまたは製品マスター データのマネージャーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="6409f-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="6409f-106">マスター プランなどの特定の業務プロセスは、特定のライフサイクルの状態によって影響を受けることができます。</span><span class="sxs-lookup"><span data-stu-id="6409f-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>   
 
<span data-ttu-id="6409f-107">リリースされた製品または製品バリアントが、特定の製品または現在あるバリアントのライフサイクル状態に記載した製品ライフサイクルの状態を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="6409f-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="6409f-108">都道府県名と説明を割り当てることにより、製品ライフサイクルの状態の番号を定義できます。</span><span class="sxs-lookup"><span data-stu-id="6409f-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="6409f-109">新しいリリース済製品の既定の状態として、1つのライフサイクルの状態を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6409f-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="6409f-110">リリース済製品のバリエーションは、作成時にリリースされた製品マスターから、その製品ライフサイクルの状態を継承します。</span><span class="sxs-lookup"><span data-stu-id="6409f-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="6409f-111">リリース済製品マスターのライフサイクルの状態を変更する際、同じの元の状態にあるすべての既存のバリエーションを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6409f-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="6409f-112">新製品ライフサイクルの状態を作成</span><span class="sxs-lookup"><span data-stu-id="6409f-112">Create a new product lifecycle state</span></span> 
 
- <span data-ttu-id="6409f-113">新製品ライフサイクルの状態を作成するには、再生またはタスク ガイドを [**新製品ライフサイクルの状態を作成**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-113">To create a new product lifecycle state, play or read the task guide **Create a new product lifecycle state**.</span></span> 

-  <span data-ttu-id="6409f-114">既定製品ライフサイクルの状態を作成するには、再生またはタスク ガイドを [**既定製品ライフサイクルの状態を作成**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-114">To create a default product lifecycle state, play or read the task guide **Create a default product lifecycle state**.</span></span>   

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="6409f-115">製品ライフサイクルの状態をリリースされた製品に関連付け</span><span class="sxs-lookup"><span data-stu-id="6409f-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="6409f-116">製品ライフサイクルの状態を、リリースされた製品または製品バリアントに関連付けための複数の方法があります。</span><span class="sxs-lookup"><span data-stu-id="6409f-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

-  <span data-ttu-id="6409f-117">新しいリリース済製品の作成時に、既定の [**製品ライフサイクルの状態**] は自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6409f-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="6409f-118">法人の製品のリリース時に、既定の [**製品ライフサイクルの状態**] は自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6409f-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span> 
-  <span data-ttu-id="6409f-119">製品バリアントから法人のリリース時、法人のリリース済製品マスターに関連付けされた [**製品ライフサイクルの状態**] は、新しいバリアントに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6409f-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span> 

<span data-ttu-id="6409f-120">以下の事項を使用して、製品ライフサイクルの状態を手動で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="6409f-120">You can manually update the product lifecycle state by using:</span></span> 

-    <span data-ttu-id="6409f-121">[**リリース済製品**] のリスト ページ、または [**詳細ビュー**]。</span><span class="sxs-lookup"><span data-stu-id="6409f-121">The **Released products** list page or **Details view**.</span></span> 
-  <span data-ttu-id="6409f-122">[**リリース済製品バリアント**] のリスト ページ、または [**詳細ビュー**]。</span><span class="sxs-lookup"><span data-stu-id="6409f-122">The **Released product variants** list page or **Details view**.</span></span> 
-  <span data-ttu-id="6409f-123">古い形式の製品または需要に基づいた製品バリアントを検索し、ライフサイクルの状態に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="6409f-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="6409f-124">製品ライフサイクルの状態を関連付ける方法の詳細については、再生または次の 2 つのタスク ガイドを参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-124">For detailed information about how to associate product lifecycle states, play or read the following two task guides.</span></span>

-  <span data-ttu-id="6409f-125">製品ライフサイクルの状態をリリース済製品マスターに関連付けるには、再生またはタスク ガイド [**製品ライフサイクルの状態をリリース済製品マスターに割り当てる**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-125">To associate a product lifecycle state to a released product master, play or read the task guide **Assign a product lifecycle state to a released product master**.</span></span> 

-  <span data-ttu-id="6409f-126">製品ライフサイクルの状態をリリース製品に関連付けるには、再生またはタスク ガイド [**製品ライフサイクルの状態をリリース済製品に割り当てる**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-126">To associate a product lifecycle state to a release product, play or read the task guide **Assign a product lifecycle state to a released product**.</span></span> 

## <a name="impact-on-master-planning"></a><span data-ttu-id="6409f-127">マスター プランへの影響</span><span class="sxs-lookup"><span data-stu-id="6409f-127">Impact on master planning</span></span> 

<span data-ttu-id="6409f-128">製品ライフサイクルの状態では、1 つの制御フラグ [**計画に対して有効**] のみです。</span><span class="sxs-lookup"><span data-stu-id="6409f-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="6409f-129">既定では、全ての作成済製品ライフサイクルの状態では [**はい**] と設定されていますが、[**いいえ**] にも変更可能です。</span><span class="sxs-lookup"><span data-stu-id="6409f-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="6409f-130">[**いいえ**] と設定する際、関連付けられているリリース済製品またはリリース済製品バリアントは以下のようになります。</span><span class="sxs-lookup"><span data-stu-id="6409f-130">When set to **No**, the associated released products or released product variants are:</span></span> 

-  <span data-ttu-id="6409f-131">マスター プランから除外されます。</span><span class="sxs-lookup"><span data-stu-id="6409f-131">Excluded from master planning.</span></span> 
-  <span data-ttu-id="6409f-132">BOM レベルの計算から除外されます。</span><span class="sxs-lookup"><span data-stu-id="6409f-132">Excluded from BOM-level calculation.</span></span> 

<span data-ttu-id="6409f-133">製品ライフサイクルの状態を使用して、製品をマスター プランおよび BOM レベルの計算から製品を除外する方法の詳細については、再生またはタスク ガイド [**マスター プランから製品を除外する製品ライフサイクルの状態を作成**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, play or read the task guide **Create a product lifecycle state to exclude products from Master planning**.</span></span>

> [!NOTE]
> <span data-ttu-id="6409f-134">パフォーマンス上の理由から、全ての古い形式のリリース済製品または製品バリアントを、特に再使用不可能な製品コンフィギュレーション バリアントを操作する際、マスタープランに対して無効な製品ライフサイクルの状態に関連付けることを強くお勧めます。</span><span class="sxs-lookup"><span data-stu-id="6409f-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  
 
## <a name="default-migration-import-and-export"></a><span data-ttu-id="6409f-135">既定の移行、インポートおよびエクスポート</span><span class="sxs-lookup"><span data-stu-id="6409f-135">Default migration, import, and export</span></span> 

<span data-ttu-id="6409f-136">製品ライフサイクルの状態がデータ エンティティでサポートされていないと、ライフサイクルの状態はリリース済製品のデータ エンティティを通じて、変動状態に設定できません。</span><span class="sxs-lookup"><span data-stu-id="6409f-136">The product lifecycle states are not supported by data entities, and the lifecycle state cannot be set to a variable state through the released product data entities.</span></span>

-  <span data-ttu-id="6409f-137">以前のリリースから移行において、すべての製品および製品バリアントのライフサイクルの状態は空白になります。</span><span class="sxs-lookup"><span data-stu-id="6409f-137">On migration from previous releases, the lifecycle state of all products and product variants will be blank.</span></span>  
-  <span data-ttu-id="6409f-138">データ エンティティを通じてリリース済製品インポートする際、既定のライフサイクルの状態は作成時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6409f-138">When importing released products through a data entity, the default lifecycle state will be applied on creation.</span></span>  
-  <span data-ttu-id="6409f-139">データ エンティティを通じてリリース済製品バリアントをインポートする際、リリース済製品マスターの製品ライフサイクルの状態がインポートされます。</span><span class="sxs-lookup"><span data-stu-id="6409f-139">When importing released product variants through a data entity, the product lifecycle state of the released product master will be imported.</span></span>   
 
## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="6409f-140">古い形式の製品および製品バリアントを検索</span><span class="sxs-lookup"><span data-stu-id="6409f-140">Find obsolete products and products variants</span></span> 
 
<span data-ttu-id="6409f-141">古い形式のリリース済製品または製品バリアントを検索してシミュレーション分析が実行でき、製品ライフサイクルの状態を更新できます。</span><span class="sxs-lookup"><span data-stu-id="6409f-141">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="6409f-142">古い形式の製品を検索する際、再生およびタスク ガイドの [**古い形式の製品バリアントを見つけ、製品ライフサイクルの状態を割り当てる**] を参照します。</span><span class="sxs-lookup"><span data-stu-id="6409f-142">To find obsolete products, play and read the task guide **Find obsolete product variants and assign a product lifecycle state**.</span></span> <span data-ttu-id="6409f-143">このタスク ガイドでは、古い形式のリリース済製品または製品バリアントを検索する方法と、古い形式の製品に製品ライフサイクルの状態を関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6409f-143">This task guide shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="6409f-144">また、シミュレーション結果の表示方法と、シミュレーション無しで更新が実行中に、いくつの製品と製品バリアントが新しい製品ライフサイクルの状態に関連付けられるのか説明します。</span><span class="sxs-lookup"><span data-stu-id="6409f-144">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  
 
<span data-ttu-id="6409f-145">シミュレーション モードで分析を実行すると、古い形式として識別された製品と製品バリアントは、簡単に確認できる特定のフォームに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6409f-145">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="6409f-146">分析では、特定期間内で需要がなく、需要につながるマスター プランもない製品を識別するトランザクションと特定のマスター データを検索します。</span><span class="sxs-lookup"><span data-stu-id="6409f-146">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="6409f-147">変動期間内の新しいリリース済製品は、分析から除外できます。</span><span class="sxs-lookup"><span data-stu-id="6409f-147">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="6409f-148">分析のシミュレーションに期待される結果が返される際、ユーザーは分析を実行し、分析によって古い形式として識別されるすべての製品に新しい製品ライフサイクルの状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6409f-148">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  
 
> [!NOTE]
> <span data-ttu-id="6409f-149">すべての分析および更新プログラムを同じ法人内で行う必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6409f-149">Note that all analysis and updates must be done within the same legal entity.</span></span>  
 
## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="6409f-150">リリース済製品または製品バリアントを、選択および更新するための基準</span><span class="sxs-lookup"><span data-stu-id="6409f-150">Criteria to select and update released products or product variants</span></span> 
 
<span data-ttu-id="6409f-151">リリース済製品と製品バリアントを選択および更新するには、以下の基準を使用します。</span><span class="sxs-lookup"><span data-stu-id="6409f-151">Use the following criteria to select and update the released products and product variants:</span></span> 

-    <span data-ttu-id="6409f-152">製品または製品バリアントの製品ライフサイクルの状態は、新しい適切な状態とは別にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6409f-152">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span> 
-  <span data-ttu-id="6409f-153">製品または製品バリアントは、数日前に選択ダイアログ ボックスに入力した日数に基づいて作成されました。</span><span class="sxs-lookup"><span data-stu-id="6409f-153">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span> 
-  <span data-ttu-id="6409f-154">製品または製品バリアントの開いている製造オーダーが存在しません (= ステータス < 終了)。</span><span class="sxs-lookup"><span data-stu-id="6409f-154">There are no open production orders (= status < ended) for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-155">製品または製品バリアントの未処理の在庫トランザクションが存在しません (= 払出ステータス ReservPhysical から QuotationIssue または 受入ステータス Registrered から QuotationReceipt)。</span><span class="sxs-lookup"><span data-stu-id="6409f-155">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-156">製品または製品バリアントの最終日数内では、在庫トランザクションは存在しません。</span><span class="sxs-lookup"><span data-stu-id="6409f-156">There are no inventory transactions within the last number of days for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-157">製品または製品バリアントの将来の需要や供給予測は存在しません。</span><span class="sxs-lookup"><span data-stu-id="6409f-157">There is no future demand or supply forecast for the product or product variant.</span></span>  
-  <span data-ttu-id="6409f-158">製品または製品バリアントの品目補充では、最小在庫レベルが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="6409f-158">No minimum stock level has been set in item coverage for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-159">製品または製品バリアントの有効な固定数量かんばんルールが存在しません。</span><span class="sxs-lookup"><span data-stu-id="6409f-159">No active fixed quantity kanban rule for the product or product variant.</span></span>  
-  <span data-ttu-id="6409f-160">製品または製品バリアントのサービス注文明細行は存在しません。</span><span class="sxs-lookup"><span data-stu-id="6409f-160">No service order line for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-161">製品または製品バリアントの有効で将来の販売または購買契約明細行は、存在しません。</span><span class="sxs-lookup"><span data-stu-id="6409f-161">No active or future sales or purchase agreement lines for the product or product variant.</span></span> 
-  <span data-ttu-id="6409f-162">製品または製品バリアントは、有効期限が切れていない承認済 BOM バージョンを、製品または計画に対して有効なバリアントに関連付けられている BOM では使用されません。</span><span class="sxs-lookup"><span data-stu-id="6409f-162">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6409f-163">関連トピック</span><span class="sxs-lookup"><span data-stu-id="6409f-163">Related topics</span></span>

-  [<span data-ttu-id="6409f-164">新製品のライフサイクル状態の作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-164">Create a new product lifecycle state (Task guide)</span></span>](tasks/new-product-lifecycle-state.md)
-  [<span data-ttu-id="6409f-165">既定の製品のライフサイクル状態の作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-165">Create a default product lifecycle state (Task guide)</span></span>](tasks/default-product-lifecycle-state.md)
-  [<span data-ttu-id="6409f-166">リリース済製品マスターに製品ライフサイクル状態を割り当てる (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-166">Assign a product lifecycle state to a released product master (Task guide)</span></span>](tasks/product-lifecycle-state-released-product-master.md)
-  [<span data-ttu-id="6409f-167">リリース済製品に製品ライフサイクル状態を割り当てる (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-167">Assign a product lifecycle state to a released product (Task guide)</span></span>](tasks/product-lifecycle-state-released-product.md)
-  [<span data-ttu-id="6409f-168">古い形式の製品バリアントを検索し、製品ライフサイクルの状態を割り当てる (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-168">Find obsolete product variants and assign a product lifecycle state (Task guide)</span></span>](tasks/obsolete-product-variants.md)
-  [<span data-ttu-id="6409f-169">マスター プランから製品を除外するよう製品ライフサイクルの状態を作成 (タスク ガイド)</span><span class="sxs-lookup"><span data-stu-id="6409f-169">Create a product lifecycle state to exclude products from Master planning (Task guide)</span></span>](tasks/exclude-products-master-planning.md)

