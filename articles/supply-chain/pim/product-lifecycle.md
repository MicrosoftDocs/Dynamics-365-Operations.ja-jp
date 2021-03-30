---
title: 製品ライフサイクル状態の概要
description: 製品ライフサイクルの状態は、リリースされた製品または製品バリアントのライフサイクルの状態を付記します。
author: cvocph
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: aaa3747dd13d56726251b150a8e0a3ec2dced614
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247841"
---
# <a name="product-lifecycle-state-overview"></a><span data-ttu-id="24ec1-103">製品ライフサイクル状態の概要</span><span class="sxs-lookup"><span data-stu-id="24ec1-103">Product lifecycle state overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24ec1-104">製品ライフサイクルの状態は、リリースされた製品または製品バリアントのライフサイクルの状態を付記します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-104">A product lifecycle state documents the lifecycle state of a released product or product variant.</span></span> <span data-ttu-id="24ec1-105">製品ライフサイクルの状態は、ユーザー、通常は製品マネージャーまたは製品マスター データのマネージャーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-105">Product lifecycle states are defined by the user, typically a product manager or a product master data manager.</span></span> <span data-ttu-id="24ec1-106">マスター プランなどの特定の業務プロセスは、特定のライフサイクルの状態によって影響を受けることができます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-106">Specific business processes, such as master planning, can be affected by a specific lifecycle state.</span></span>

<span data-ttu-id="24ec1-107">リリースされた製品または製品バリアントが、特定の製品または現在あるバリアントのライフサイクル状態に記載した製品ライフサイクルの状態を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-107">A released product or product variant can be associated with a product lifecycle state that documents in which lifecycle state a specific product or variant is currently in.</span></span> <span data-ttu-id="24ec1-108">都道府県名と説明を割り当てることにより、製品ライフサイクルの状態の番号を定義できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-108">You can define any number of product lifecycle states by assigning a state name and description.</span></span> <span data-ttu-id="24ec1-109">新しいリリース済製品の既定の状態として、1つのライフサイクルの状態を選択できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-109">You can select one lifecycle state as the default state for new released products.</span></span> <span data-ttu-id="24ec1-110">リリース済製品のバリエーションは、作成時にリリースされた製品マスターから、その製品ライフサイクルの状態を継承します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-110">Released product variants inherit their product lifecycle state from their released product master on creation.</span></span> <span data-ttu-id="24ec1-111">リリース済製品マスターのライフサイクルの状態を変更する際、同じの元の状態にあるすべての既存のバリエーションを更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-111">When changing the lifecycle state on a released product master, you can choose to update all existing variants that have the same original state.</span></span>  

## <a name="create-a-new-product-lifecycle-state"></a><span data-ttu-id="24ec1-112">新しい製品ライフサイクル状態の作成</span><span class="sxs-lookup"><span data-stu-id="24ec1-112">Create a new product lifecycle state</span></span>

- <span data-ttu-id="24ec1-113">新製品ライフサイクルの状態を作成するには、[新製品ライフサイクルの状態を作成](tasks/new-product-lifecycle-state.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-113">To create a new product lifecycle state, see [Create a new product lifecycle state](tasks/new-product-lifecycle-state.md).</span></span>

- <span data-ttu-id="24ec1-114">既定の製品ライフサイクルの状態を作成するには、[既定の製品ライフサイクルの状態を作成](tasks/default-product-lifecycle-state.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-114">To create a default product lifecycle state, see [Create a default product lifecycle state](tasks/default-product-lifecycle-state.md).</span></span>

## <a name="associate-product-lifecycle-states-to-released-products"></a><span data-ttu-id="24ec1-115">製品ライフサイクルの状態をリリースされた製品に関連付け</span><span class="sxs-lookup"><span data-stu-id="24ec1-115">Associate product lifecycle states to released products</span></span>  

<span data-ttu-id="24ec1-116">製品ライフサイクルの状態を、リリースされた製品または製品バリアントに関連付けための複数の方法があります。</span><span class="sxs-lookup"><span data-stu-id="24ec1-116">There are multiple ways to associate a product lifecycle state to released products or product variants.</span></span>

- <span data-ttu-id="24ec1-117">新しいリリース済製品の作成時に、既定の **製品ライフサイクルの状態** は自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-117">On creation of a new released product, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="24ec1-118">法人の製品のリリース時に、既定の **製品ライフサイクルの状態** は自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-118">On release of a product to a legal entity, the default **Product lifecycle state** is automatically assigned.</span></span>
- <span data-ttu-id="24ec1-119">製品バリアントから法人のリリース時、法人のリリース済製品マスターに関連付けされた **製品ライフサイクルの状態** は、新しいバリアントに自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-119">On release of a product variant to a legal entity, the **Product lifecycle state** associated to the released product master in this legal entity is automatically assigned to the new variant.</span></span>

<span data-ttu-id="24ec1-120">以下の事項を使用して、製品ライフサイクルの状態を手動で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-120">You can manually update the product lifecycle state by using:</span></span>

- <span data-ttu-id="24ec1-121">**リリース済製品** のリスト ページ、または **詳細ビュー**。</span><span class="sxs-lookup"><span data-stu-id="24ec1-121">The **Released products** list page or **Details view**.</span></span>
- <span data-ttu-id="24ec1-122">**リリース済製品バリアント** のリスト ページ、または **詳細ビュー**。</span><span class="sxs-lookup"><span data-stu-id="24ec1-122">The **Released product variants** list page or **Details view**.</span></span>
- <span data-ttu-id="24ec1-123">古い形式の製品または需要に基づいた製品バリアントを検索し、ライフサイクルの状態に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-123">Find the obsolete products or product variants based on demand and associate a lifecycle state.</span></span>  

<span data-ttu-id="24ec1-124">詳細情報:</span><span class="sxs-lookup"><span data-stu-id="24ec1-124">For more information:</span></span>

- <span data-ttu-id="24ec1-125">製品ライフサイクルの状態をリリース済製品マスターに関連付けるには、[製品ライフサイクルの状態をリリース済製品マスターに割り当てる](tasks/product-lifecycle-state-released-product-master.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-125">To associate a product lifecycle state to a released product master, see [Assign a product lifecycle state to a released product master](tasks/product-lifecycle-state-released-product-master.md).</span></span>

- <span data-ttu-id="24ec1-126">製品ライフサイクルの状態をリリース済製品に関連付けるには、[製品ライフサイクルの状態をリリース済製品に割り当てる](tasks/product-lifecycle-state-released-product.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-126">To associate a product lifecycle state to a release product, see [Assign a product lifecycle state to a released product](tasks/product-lifecycle-state-released-product.md).</span></span>

## <a name="impact-on-master-planning"></a><span data-ttu-id="24ec1-127">マスター プランへの影響</span><span class="sxs-lookup"><span data-stu-id="24ec1-127">Impact on master planning</span></span>

<span data-ttu-id="24ec1-128">製品ライフサイクルの状態では、1 つの制御フラグ **計画に対して有効** のみです。</span><span class="sxs-lookup"><span data-stu-id="24ec1-128">The product lifecycle state has only one control flag: **Is active for planning**.</span></span> <span data-ttu-id="24ec1-129">既定では、全ての作成済製品ライフサイクルの状態では **はい** と設定されていますが、**いいえ** にも変更可能です。</span><span class="sxs-lookup"><span data-stu-id="24ec1-129">By default, this is set to **Yes** for all created product lifecycle states, but it can be changed to **No**.</span></span> <span data-ttu-id="24ec1-130">**いいえ** と設定する際、関連付けられているリリース済製品またはリリース済製品バリアントは以下のようになります。</span><span class="sxs-lookup"><span data-stu-id="24ec1-130">When set to **No**, the associated released products or released product variants are:</span></span>

- <span data-ttu-id="24ec1-131">マスター プランから除外されます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-131">Excluded from master planning.</span></span>
- <span data-ttu-id="24ec1-132">BOM レベルの計算から除外されます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-132">Excluded from BOM-level calculation.</span></span>

<span data-ttu-id="24ec1-133">製品ライフサイクルの状態を使用して、製品をマスター プランおよび BOM レベルの計算から製品を除外する方法の詳細については、[マスター プランから製品を除外する製品ライフサイクルの状態を作成](tasks/exclude-products-master-planning.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="24ec1-133">For detailed information about how to use product lifecycle state to exclude products from master planning and BOM-level calculation, see [Create a product lifecycle state to exclude products from Master planning](tasks/exclude-products-master-planning.md)</span></span>

> [!NOTE]
> <span data-ttu-id="24ec1-134">パフォーマンス上の理由から、全ての古い形式のリリース済製品または製品バリアントを、特に再使用不可能な製品コンフィギュレーション バリアントを操作する際、マスタープランに対して無効な製品ライフサイクルの状態に関連付けることを強くお勧めます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-134">For performance reasons, it is highly recommended to associate all obsolete released products or product variants, especially when working with non-reusable product configuration variants, with a product lifecycle state that is deactivated for master planning.</span></span>  

## <a name="default-migration-import-and-export"></a><span data-ttu-id="24ec1-135">既定の移行、インポートおよびエクスポート</span><span class="sxs-lookup"><span data-stu-id="24ec1-135">Default migration, import, and export</span></span>

<span data-ttu-id="24ec1-136">製品ライフサイクルの状態はデータ エンティティによってサポートされており、ライフサイクルの状態はリリース済製品のデータ エンティティまたはリリース済みバリアント データ エンティティのいずれかを介して、変動状態に設定できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-136">The product lifecycle states are supported by data entities, and the lifecycle state can be set to a variable state through either the released product data entity or the released variant data entity.</span></span>

## <a name="find-obsolete-products-and-products-variants"></a><span data-ttu-id="24ec1-137">古い形式の製品および製品バリアントを検索</span><span class="sxs-lookup"><span data-stu-id="24ec1-137">Find obsolete products and products variants</span></span>

<span data-ttu-id="24ec1-138">古い形式のリリース済製品または製品バリアントを検索してシミュレーション分析が実行でき、製品ライフサイクルの状態を更新できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-138">You can run a simulation analysis to find the obsolete released products or product variants and then update their product lifecycle status.</span></span> <span data-ttu-id="24ec1-139">古い形式の製品を検索するには、[古い形式の製品バリアントを見つけ、製品ライフサイクルの状態を割り当てる](tasks/obsolete-product-variants.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-139">To find obsolete products, see [Find obsolete product variants and assign a product lifecycle state](tasks/obsolete-product-variants.md).</span></span> <span data-ttu-id="24ec1-140">このトピックでは、古い形式のリリース済製品または製品バリアントを検索する方法と、古い形式の製品に製品ライフサイクルの状態を関連付ける方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-140">This topic shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="24ec1-141">また、シミュレーション結果の表示方法と、シミュレーション無しで更新が実行中に、いくつの製品と製品バリアントが新しい製品ライフサイクルの状態に関連付けられるのか説明します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-141">It also shows hot to view the simulation results and assess how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

<span data-ttu-id="24ec1-142">シミュレーション モードで分析を実行すると、古い形式として識別された製品と製品バリアントは、簡単に確認できる特定のフォームに表示されます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-142">By running the analysis in a simulation mode, the products and product variants identified as obsolete are displayed in a specific form, where they can easily be reviewed.</span></span> <span data-ttu-id="24ec1-143">分析では、特定期間内で需要がなく、需要につながるマスター プランもない製品を識別するトランザクションと特定のマスター データを検索します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-143">The analysis searches for transactions and specific master data to identify products that have no demand within a variable period and no master data that can result in demand.</span></span> <span data-ttu-id="24ec1-144">変動期間内の新しいリリース済製品は、分析から除外できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-144">New released products within a variable period can be excluded from the analysis.</span></span> <span data-ttu-id="24ec1-145">分析のシミュレーションに期待される結果が返される際、ユーザーは分析を実行し、分析によって古い形式として識別されるすべての製品に新しい製品ライフサイクルの状態を設定できます。</span><span class="sxs-lookup"><span data-stu-id="24ec1-145">When the analysis simulation returns the expected result, the user can run the analysis and set a new product lifecycle state to all products identified as obsolete by the analysis.</span></span>  

> [!NOTE]
> <span data-ttu-id="24ec1-146">すべての分析および更新プログラムを同じ法人内で行う必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="24ec1-146">Note that all analysis and updates must be done within the same legal entity.</span></span>  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a><span data-ttu-id="24ec1-147">リリース済製品または製品バリアントを、選択および更新するための基準</span><span class="sxs-lookup"><span data-stu-id="24ec1-147">Criteria to select and update released products or product variants</span></span>

<span data-ttu-id="24ec1-148">リリース済製品と製品バリアントを選択および更新するには、以下の基準を使用します。</span><span class="sxs-lookup"><span data-stu-id="24ec1-148">Use the following criteria to select and update the released products and product variants:</span></span>

- <span data-ttu-id="24ec1-149">製品または製品バリアントの製品ライフサイクルの状態は、新しい適切な状態とは別にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="24ec1-149">The product lifecycle state of the product or product variant must be different from the new desired state.</span></span>
- <span data-ttu-id="24ec1-150">製品または製品バリアントは、数日前に選択ダイアログ ボックスに入力した日数に基づいて作成されました。</span><span class="sxs-lookup"><span data-stu-id="24ec1-150">The product or product variant was created some days ago based on the number of days that you enter in the selection dialog box.</span></span>
- <span data-ttu-id="24ec1-151">製品または製品バリアントの開いている製造オーダーが存在しません (= ステータス < 終了)。</span><span class="sxs-lookup"><span data-stu-id="24ec1-151">There are no open production orders (= status < ended) for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-152">製品または製品バリアントの未処理の在庫トランザクションが存在しません (= 払出ステータス ReservPhysical から QuotationIssue または 受入ステータス Registrered から QuotationReceipt)。</span><span class="sxs-lookup"><span data-stu-id="24ec1-152">There are no open inventory transactions (= status issue ReservPhysical to QuotationIssue or status receipt Registrered to QuotationReceipt) for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-153">製品または製品バリアントの最終日数内では、在庫トランザクションは存在しません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-153">There are no inventory transactions within the last number of days for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-154">製品または製品バリアントの将来の需要や供給予測は存在しません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-154">There is no future demand or supply forecast for the product or product variant.</span></span>  
- <span data-ttu-id="24ec1-155">製品または製品バリアントの品目補充では、最小在庫レベルが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-155">No minimum stock level has been set in item coverage for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-156">製品または製品バリアントの有効な固定数量かんばんルールが存在しません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-156">No active fixed quantity kanban rule for the product or product variant.</span></span>  
- <span data-ttu-id="24ec1-157">製品または製品バリアントのサービス注文明細行は存在しません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-157">No service order line for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-158">製品または製品バリアントの有効で将来の販売または購買契約明細行は、存在しません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-158">No active or future sales or purchase agreement lines for the product or product variant.</span></span>
- <span data-ttu-id="24ec1-159">製品または製品バリアントは、有効期限が切れていない承認済 BOM バージョンを、製品または計画に対して有効なバリアントに関連付けられている BOM では使用されません。</span><span class="sxs-lookup"><span data-stu-id="24ec1-159">The product or product variant is not used in a BOM that is associated with a non-expired approved BOM version for a product or variant that is active for planning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24ec1-160">関連トピック</span><span class="sxs-lookup"><span data-stu-id="24ec1-160">Related topics</span></span>

- [<span data-ttu-id="24ec1-161">新しい製品ライフサイクル状態の作成</span><span class="sxs-lookup"><span data-stu-id="24ec1-161">Create a new product lifecycle state</span></span>](tasks/new-product-lifecycle-state.md)
- [<span data-ttu-id="24ec1-162">既定の製品ライフサイクル状態の作成</span><span class="sxs-lookup"><span data-stu-id="24ec1-162">Create a default product lifecycle state</span></span>](tasks/default-product-lifecycle-state.md)
- [<span data-ttu-id="24ec1-163">リリース済製品マスターに製品ライフサイクル状態を割り当てる</span><span class="sxs-lookup"><span data-stu-id="24ec1-163">Assign a product lifecycle state to a released product master</span></span>](tasks/product-lifecycle-state-released-product-master.md)
- [<span data-ttu-id="24ec1-164">リリース済製品に製品ライフサイクル状態を割り当てる</span><span class="sxs-lookup"><span data-stu-id="24ec1-164">Assign a product lifecycle state to a released product</span></span>](tasks/product-lifecycle-state-released-product.md)
- [<span data-ttu-id="24ec1-165">古い形式の製品バリアントを検索して、製品ライフサイクルの状態を割り当てる</span><span class="sxs-lookup"><span data-stu-id="24ec1-165">Find obsolete product variants and assign a product lifecycle state</span></span>](tasks/obsolete-product-variants.md)
- [<span data-ttu-id="24ec1-166">マスター プランから製品を除外する場合は、製品ライフサイクルの状態を作成</span><span class="sxs-lookup"><span data-stu-id="24ec1-166">Create a product lifecycle state to exclude products from Master planning</span></span>](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]