---
title: 倉庫管理による CW 製品の処理
description: このトピックでは、作業テンプレートと場所ディレクティブを使用して作業が倉庫のどこでどのように実行されるかを決定する方法を説明します。
author: perlynne
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: ed588ea28bec3e734f9648c1fbd7551ab0b3cdda
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836120"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="3e8fc-103">倉庫管理による CW 製品の処理</span><span class="sxs-lookup"><span data-stu-id="3e8fc-103">Catch weight product processing with warehouse management</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]


## <a name="feature-exposure"></a><span data-ttu-id="3e8fc-104">エクスポージャ機能</span><span class="sxs-lookup"><span data-stu-id="3e8fc-104">Feature exposure</span></span>

<span data-ttu-id="3e8fc-105">CW 製品を処理する倉庫管理を使用するには、ライセンス コンフィギュレーション キーを使用して、機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-105">To use warehouse management to process catch weight products, you must use a license configuration key to turn on the functionality.</span></span> <span data-ttu-id="3e8fc-106">(**システム管理\>設定\>ライセンス コンフィギュレーション**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-106">(Go to **System administration \> Setup \> License configuration**.</span></span> <span data-ttu-id="3e8fc-107">その後、**コンフィギュレーション キー**タブで**取引\>倉庫および配送の管理**を展開し、**倉庫用 CW** のチェック ボックスを選択します)。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-107">Then, on the **Configuration keys** tab, expand **Trade \> Warehouse and Transportation management**, and select the check box for **Catch weight for warehouse**).</span></span>

> [!NOTE]
> <span data-ttu-id="3e8fc-108">**倉庫および配送の管理**ライセンス コンフィギュレーション キーおよび**流通処理 \> CW** ライセンス コンフィギュレーション キーの両方をオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-108">Both the **Warehouse and Transportation management** license configuration key and the **Process distribution \> Catch weight** license configuration keys must also be turned on.</span></span>

<span data-ttu-id="3e8fc-109">ラインセンス コンフィギュレーション キーをオンにした後、リリースされた製品を作成する場合は、**CW** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-109">After the license configuration key is turned on, when you create a released product, you can select **Catch weight**.</span></span> <span data-ttu-id="3e8fc-110">**倉庫管理プロセスを使用**パラメーターが選択されている保管分析コードのグループで、リリースされた製品を関連付けることも可能です。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-110">You can also associate the released product with a storage dimension group that the **Use warehouse management processes** parameter is selected for.</span></span>

<span data-ttu-id="3e8fc-111">倉庫管理で製品を使う前に、CW のいくつかの基本的な製品固有設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-111">Before you can use the product in Warehouse management, you must do some basic product-specific setup for catch weight:</span></span>

- <span data-ttu-id="3e8fc-112">変換定義の一部として、CW 単位 (ボックス) と在庫単位 (キログラム\[kg\]) の間で公称重量換算を定義します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-112">Define the nominal weight conversion between the catch weight unit (box) and the inventory unit (kilogram \[kg\]) as part of a unit conversion definition.</span></span>
- <span data-ttu-id="3e8fc-113">CW 単位の設定の一部として、最小および最大の重量の許容範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-113">Define the minimum and maximum weight tolerances as part of the catch weight unit setup.</span></span>
- <span data-ttu-id="3e8fc-114">CW 単位が最小在庫単位 (SKU) として定義されている順序グループの単位を設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-114">Set up a unit sequence group where the catch weight unit is defined as the lowest stock keeping unit (SKU).</span></span>
- <span data-ttu-id="3e8fc-115">CW 品目の取り扱いに関するポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-115">Set up a catch weight item handling policy.</span></span>

<span data-ttu-id="3e8fc-116">詳細については、[設定および CW 品目の管理](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-116">For more information, see [Setting up and maintaining catch weight items](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).</span></span>

## <a name="transaction-adjustments"></a><span data-ttu-id="3e8fc-117">取引の調整</span><span class="sxs-lookup"><span data-stu-id="3e8fc-117">Transaction adjustments</span></span>

<span data-ttu-id="3e8fc-118">在庫の重量は倉庫に入ると、出庫されるときの重量とは異なる場合があるので、CW 製品の処理は在庫調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-118">Because the weight of inventory when it comes into a warehouse can differ from the weight when the inventory is issued out of the warehouse, the catch weight product processing must adjust the inventory.</span></span>

<span data-ttu-id="3e8fc-119">**例 1**</span><span class="sxs-lookup"><span data-stu-id="3e8fc-119">**Example 1**</span></span>

<span data-ttu-id="3e8fc-120">**完了レポート**の生産処理中に、CW 製品の 8 つのボックスを含むライセンス プレートのインバウンド重量は 80.1 kg として記録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-120">During a **Report as finished** production process, the inbound weight of a license plate that contains eight boxes of a catch weight product is captured as 80.1 kg.</span></span> <span data-ttu-id="3e8fc-121">ライセンス プレートは完成品エリアで格納され、保管期間中に、いくつかの重量が失われます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-121">The license plate is then stored away in the finished goods area, and during the storage period, some weight is lost into the air.</span></span>

<span data-ttu-id="3e8fc-122">その後、ピッキング プロセスの販売注文の一部として、同じライセンス プレートの重量は 79.8 kg として記録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-122">Later, as part of a sales order picking process, the weight of the same license plate is captured as 79.8 kg.</span></span> <span data-ttu-id="3e8fc-123">そのため、システムでは現物分析コードの一部として重量差があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-123">Therefore, in the system, you now have a weight difference as part of the physical dimension set.</span></span>

<span data-ttu-id="3e8fc-124">この場合、システムでは自動的に不足している 0.3 kg に対して取引を転記して差異を調整します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-124">In this case, the system automatically adjusts the difference by posting a transaction for the missing 0.3 kg.</span></span>

<span data-ttu-id="3e8fc-125">**例 2**</span><span class="sxs-lookup"><span data-stu-id="3e8fc-125">**Example 2**</span></span>

<span data-ttu-id="3e8fc-126">その定義では、製品を**ボックス** CW 単位の 8 kg の最小重量および 12 kg の最大重量を許容するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-126">In its definition, a product is set up to tolerate a minimum weight of 8 kg and a maximum weight of 12 kg for the **Box** catch weight unit.</span></span>

<span data-ttu-id="3e8fc-127">製品 2 箱を所有し、16 kg の登録済重量があるとします。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-127">You have two boxes of the product, and they have a registered weight of 16 kg.</span></span> <span data-ttu-id="3e8fc-128">倉庫作業者が箱 1 つの重さを量り、その重量が 9 kg と記録された場合、残りの箱は7 kg になります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-128">If a warehouse worker picks and weighs one of the boxes, and the weight is captured as 9 kg, the remaining box will weigh 7 kg.</span></span> <span data-ttu-id="3e8fc-129">ただし、7 kg が最小重量を下回っているので、システムでは手持在庫の重さが 1 kg 増えるよう自動的に調整します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-129">However, because 7 kg is below the minimum weight, the system does an automatic adjustment to increase the weight of the on-hand inventory by 1 kg.</span></span>

<span data-ttu-id="3e8fc-130">これらの調整に転記される勘定を設定するには、**原価管理\>元帳統合ポリシー設定\>転記**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-130">To set up the accounts that these adjustments are posted to, go to **Cost management \> Ledger integration policies setup \> Posting**.</span></span> <span data-ttu-id="3e8fc-131">その後、**在庫**タブで次の勘定を定義します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-131">Then, on the **Inventory** tab, define the following accounts:</span></span>

- <span data-ttu-id="3e8fc-132">CW 損失勘定</span><span class="sxs-lookup"><span data-stu-id="3e8fc-132">Catch weight loss account</span></span>
- <span data-ttu-id="3e8fc-133">CW 利益勘定</span><span class="sxs-lookup"><span data-stu-id="3e8fc-133">Catch weight profit account</span></span>

## <a name="catch-weight-item-handling-policy"></a><span data-ttu-id="3e8fc-134">CW 品目の取り扱いに関するポリシー</span><span class="sxs-lookup"><span data-stu-id="3e8fc-134">Catch weight item handling policy</span></span>

<span data-ttu-id="3e8fc-135">CW 品目の取り扱いポリシーは、いつ品目重量が取得され、どのように記録されるかという 2 つの品目プライマリの倉庫管理フローを定義します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-135">The catch weight item handling policy defines two primary warehouse management flows for the items: when the weight of the items is captured, and how it's captured.</span></span>

<span data-ttu-id="3e8fc-136">いつ重量が販売と注文処理の移動を記録されたかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-136">You can define when the weight is captured for sales and transfer order processing.</span></span> <span data-ttu-id="3e8fc-137">重量は、次のプロセスのいずれかの過程で自動的に記録することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-137">The weight can be captured during either of the following processes:</span></span>

- <span data-ttu-id="3e8fc-138">**ピッキング** – 重量は、注文作業の初期ピック作業明細行の過程で記録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-138">**Picking** – The weight is captured during the initial pick work lines of order work.</span></span>
- <span data-ttu-id="3e8fc-139">**梱包** – 重量は、手動梱包中に記録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-139">**Packing** – The weight is captured during manual packing.</span></span> <span data-ttu-id="3e8fc-140">(品目は梱包ステーションに送信する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="3e8fc-140">(You must send the items to a packing station.)</span></span>

<span data-ttu-id="3e8fc-141">実際の重量がコンテナーの梱包プロセス中に梱包ステーションで記録された場合、倉庫作業員はピッキング中に重量を記録するように促されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-141">If the actual weight is captured at the packing station during the container packing processes, warehouse workers won't be prompted to capture the weight during picking work.</span></span> <span data-ttu-id="3e8fc-142">代わりに、現物在庫の平均重量を梱包エリアに移動するピッキング済の在庫重量として使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-142">Instead, the average weight of the physical inventory will be used as the weight of the picked inventory that goes to the packing area.</span></span>

<span data-ttu-id="3e8fc-143">棚卸および修正の調整などの内部倉庫管理のプロセスは、重量が記録されるかどうかを定義することが可能です。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-143">For internal warehouse management processes like counting and adjustment corrections it is possible to define if the weight should be captured or not.</span></span> <span data-ttu-id="3e8fc-144">記録されない場合は、公称重量が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-144">If not captured the nominal weight will be used.</span></span>

<span data-ttu-id="3e8fc-145">重量の記録方法を定義することも可能です。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-145">You can also define how the weight is captured.</span></span> <span data-ttu-id="3e8fc-146">2 つの主要なフローの 1 つに、CW タグが追跡され、重量を記録るために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-146">In one of the two main flows, catch weight tags are tracked and used to capture the weight.</span></span> <span data-ttu-id="3e8fc-147">その他のフローでは、CW タグの履歴が記録されません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-147">In the other flow, catch weight tags aren't tracked.</span></span>

- <span data-ttu-id="3e8fc-148">**はい** – 品目は CW タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-148">**Yes** – The item uses catch weight tags.</span></span> <span data-ttu-id="3e8fc-149">各タグ番号は 1 つの CW 単位 (ボックス) を表し、重量と他の情報はタグに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-149">Each tag number represents one catch weight unit (box), and a weight and other information are associated with the tag.</span></span> <span data-ttu-id="3e8fc-150">発信プロセスの場合、タグに関連付けられている重量が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-150">For outbound processes, the weight that is associated with the tag is used.</span></span>
- <span data-ttu-id="3e8fc-151">**いいえ** – 品目は CW タグを使用していません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-151">**No** – The item doesn't use catch weight tags.</span></span> <span data-ttu-id="3e8fc-152">入庫と出庫の重量計量プロセスは、各プロセス中に記録された実際の重量に基づいています。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-152">The inbound and outbound weighing processes are based on the actual weight that is captured during each process.</span></span>

<span data-ttu-id="3e8fc-153">追跡 CW タグのプロセスは、記憶域期間中に重量を変更しない品目に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-153">The process of tracking catch weight tags can be used for items that won't change weight during the storage period.</span></span> <span data-ttu-id="3e8fc-154">重量は、入庫倉庫の処理中にのみ記録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-154">The weight will be captured only during the inbound warehouse process.</span></span> <span data-ttu-id="3e8fc-155">出庫プロセス中に CW タグはただスキャンされ、タグに関連付けられた重量は出庫トランザクションの処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-155">During the outbound process, the catch weight tags will just be scanned, and the weights that are associated with the tags will be used for the outbound transactional processing.</span></span>

### <a name="how-to-capture-catch-weight"></a><span data-ttu-id="3e8fc-156">CW の記録方法</span><span class="sxs-lookup"><span data-stu-id="3e8fc-156">How to capture catch weight</span></span>

<span data-ttu-id="3e8fc-157">CW タグの追跡が使用されると、タグは常に受信されたすべての CW 単位に対して作成する必要があり、全てのタグは常に重量と関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-157">When catch weight tag tracking is used, a tag must always be created for every catch weigh unit that is received, and every tag must always be associated with a weight.</span></span>

<span data-ttu-id="3e8fc-158">たとえば、**ボックス**は CW 単位で、8 つのボックスのうち 1 つのパレットを受信します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-158">For example, **Box** is the catch weight unit, and you receive one pallet of eight boxes.</span></span> <span data-ttu-id="3e8fc-159">この場合、8 つの固有 CW タグを作成し、重量は各タグを関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-159">In this case, eight unique catch weight tags must be created, and a weight must be associated with each tag.</span></span> <span data-ttu-id="3e8fc-160">入庫 CW タグによっては、8 つすべてのボックスが記録される、各ボックスに配る、または固有重量を各ボックスに記録するのどちらかが可能です。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-160">Depending on the inbound catch weight tag, either the weight of all eight boxes can be captured, and the average weight can then be distributed to each box, or a unique weight can be captured for each box.</span></span>

<span data-ttu-id="3e8fc-161">CW タグの追跡が使用されていない場合は、各分析コードの設定 (たとえば、それぞれのライセンス プレートと追跡用分析コードごとに) の重量を取得できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-161">When catch weight tag tracking isn't used, the weight can be captured for each dimension set (for example, for each license plate and tracking dimension).</span></span> <span data-ttu-id="3e8fc-162">または、5 つのライセンス プレート (パレット) などの統合されたレベルに基づく重量を記録することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-162">Alternatively, the weight can be captured based on an aggregated level, such as five license plates (pallets).</span></span>

<span data-ttu-id="3e8fc-163">出庫重量を記録するための方法は、各 CW 単位 (つまりボックス 1 つあたり) の重量が処理されるか、または重量がピッキングされる数量に基づき記録されるか定義できます (たとえば 3 つのボックス)。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-163">For the methods for capturing outbound weight, you can define whether the weighing is done for each catch weight unit (that is, per box), or whether the weight is captured based on the quantity that will be picked (for example, three boxes).</span></span> <span data-ttu-id="3e8fc-164">実稼働ラインのピッキングと内部の移動プロセスについては、**取得されない**オプションが使用される場合、平均加重は使用されません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-164">Note that for the production line picking and internal movement processes, the average weight will be used if the **Not captured** option is used.</span></span>

<span data-ttu-id="3e8fc-165">倉庫管理のピッキング プロセスをキャプチャする重量から制限して CW/損益調整するには、出庫重量の差異メソッドの使用が可能です。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-165">To restrict the warehouse management picking processes from capturing weights resulting in catch weight profit/loss adjustments, the Outbound weight variance method can be used.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="3e8fc-166">サポートされているシナリオ</span><span class="sxs-lookup"><span data-stu-id="3e8fc-166">Supported scenarios</span></span>

<span data-ttu-id="3e8fc-167">すべての作業員が倉庫管理による CW 製品の処理を行っているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-167">Not all workflows support catch weight product processing with warehouse management.</span></span> <span data-ttu-id="3e8fc-168">現在以下の制限があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-168">The following restrictions currently apply.</span></span>
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a><span data-ttu-id="3e8fc-169">倉庫管理による CW 製品のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3e8fc-169">Configuring catch weight products for warehouse management processes</span></span>

- <span data-ttu-id="3e8fc-170">CW 製品では、品目の保管分析コード グループを変更できません (倉庫管理プロセスが使用できるように)。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-170">For catch weight products, the storage dimension group for items can't be changed (so that warehouse management processes can be used for them).</span></span>
- <span data-ttu-id="3e8fc-171">フォーミュラの処理のみが CW 製品でサポートされています (部品表ではない)。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-171">Only formula processing is supported for catch weight products (not bill of materials).</span></span>
- <span data-ttu-id="3e8fc-172">CW 製品は、所有者分析コードを使用して追跡用の分析コード グループに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-172">Catch weight products can't be associated with a tracking dimension group by using the Owner dimension.</span></span>
- <span data-ttu-id="3e8fc-173">CW 製品をサービスとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-173">Catch weight products can't be used as services.</span></span>
- <span data-ttu-id="3e8fc-174">CW 製品は、品目モデル グループの一部としてのみ「在庫製品」として使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-174">Catch weight products can be used as "stocked products" only as part the item model group.</span></span>
- <span data-ttu-id="3e8fc-175">CW 製品は、「販売プロセスで有効」を追跡するための機能と一緒に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-175">Catch weight products can't be used together with the functionality for tracking "Active in sales process."</span></span>
- <span data-ttu-id="3e8fc-176">CW 製品は、シリアル番号を記録するための機能と一緒に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-176">Catch weight products can't be used together with the functionality for capturing serial numbers.</span></span> <span data-ttu-id="3e8fc-177">したがって、製品はピッキング/梱包プロセスの一部として「空白」からシリアル番号に転送できません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-177">Therefore, products can't be transferred from a "blank" to a serial number as part of the picking/packing process.</span></span>
- <span data-ttu-id="3e8fc-178">CW 製品は、消費前のシリアルを登録するための機能と一緒に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-178">Catch weight products can't be used together with the functionality for registering serials before consumption.</span></span>
- <span data-ttu-id="3e8fc-179">バリアントが有効な CW 製品は、バリアント数量単位を変換するための機能と組み合わせて使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-179">Catch weight products that are variant-enabled can't be used together with the functionality for converting variant units of measure.</span></span>
- <span data-ttu-id="3e8fc-180">CW 製品は、小売の「製品キット」としてマークすることはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-180">Catch weight products can't be marked as a retail "product kit."</span></span>
- <span data-ttu-id="3e8fc-181">CW 製品は、CW の材料取り扱い単位を所有し、最下位のシーケンスとして CW 単位を所有する順序グループとのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-181">Catch weight products can be used only with a unit sequence group that has catch weight handling units, and that has the catch weight unit as the lowest sequence.</span></span>
- <span data-ttu-id="3e8fc-182">CW 製品では、変換が 1 以上の名目数量を生成する場合にのみ、在庫単位を CW 単位に変換できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-182">For catch weight products, the inventory unit can be converted to the catch weight unit only if the conversion produces a nominal quantity that is more than 1.</span></span>
- <span data-ttu-id="3e8fc-183">CW 製品のバーコード設定には、変動重量の設定をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-183">The setup of bar codes for catch weight products doesn't support a variable weight setup.</span></span>
 
### <a name="order-processing"></a><span data-ttu-id="3e8fc-184">注文処理</span><span class="sxs-lookup"><span data-stu-id="3e8fc-184">Order processing</span></span>

- <span data-ttu-id="3e8fc-185">事前出荷明細通知 (ASN/梱包構造) の作成には、重量情報をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-185">The creation of advance ship notice (ASN/packing structures) doesn't support weight information.</span></span>
- <span data-ttu-id="3e8fc-186">注文数量は CW 単位に基づいて維持される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-186">The order quantity must be maintained based on the catch weight unit.</span></span>
 
### <a name="inbound-warehouse-processing"></a><span data-ttu-id="3e8fc-187">入庫の倉庫処理</span><span class="sxs-lookup"><span data-stu-id="3e8fc-187">Inbound warehouse processing</span></span>

- <span data-ttu-id="3e8fc-188">重量情報が事前出荷明細通知の一部としてサポートされていないため、ライセンス プレートは重量が登録中に割り当てられることを要求します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-188">Receiving license plates requires that weights be assigned during registration, because weight information isn't supported as part of the advance ship notice.</span></span> <span data-ttu-id="3e8fc-189">CW タグのプロセスを使用する場合、タグ番号は CW 単位ごとに手動で割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-189">When catch weight tag processes are used, the tag number must be manually assigned per catch weight unit.</span></span>
 
### <a name="inventory-and-warehouse-operations"></a><span data-ttu-id="3e8fc-190">在庫および倉庫の操作</span><span class="sxs-lookup"><span data-stu-id="3e8fc-190">Inventory and warehouse operations</span></span>

- <span data-ttu-id="3e8fc-191">検査指示の手動作成では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-191">Manual creation of quarantine orders isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-192">作業に関連付けしている在庫の手動による移動では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-192">Manual movement of inventory that is related to work isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-193">ライセンス プレートの連結では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-193">Consolidation of license plates isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-194">倉庫の在庫を初期化するためのライセンス プレートの読み込みでは、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-194">License plate loading to initialize warehouse stock isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-195">バッチ バランシングのプロセスでは、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-195">Batch balancing processes aren't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-196">マイナスの現物在庫の処理では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-196">Handling of negative physical inventory isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-197">CW 製品には、在庫のマーキングを使用できません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-197">Inventory marking can't be used for catch weight products.</span></span>
 
### <a name="outbound-warehouse-processing"></a><span data-ttu-id="3e8fc-198">出庫の倉庫処理</span><span class="sxs-lookup"><span data-stu-id="3e8fc-198">Outbound warehouse processing</span></span>

- <span data-ttu-id="3e8fc-199">クラスター ピッキングの機能では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-199">The functionality for cluster picking isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-200">ピッキングと梱包の倉庫の処理では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-200">Pick and pack warehouse processing isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-201">CW 製品では、作業テンプレートで定義されている作業を自動的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-201">For catch weight products, work that is defined in a work template can be run automatically.</span></span>
- <span data-ttu-id="3e8fc-202">逆仕訳作業の機能では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-202">The functionality for reversing work isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-203">CW 製品では、コンテナーが終了した後に、作業が作成される手作業の梱包ステーションの処理はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-203">For catch weight products, manual packing station processing where work is created after containers are closed isn't supported.</span></span>
- <span data-ttu-id="3e8fc-204">個ごとのスキャン機能では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-204">The functionality for pcs-by-pcs scanning isn't supported for catch weight products.</span></span>
 
### <a name="production-processing"></a><span data-ttu-id="3e8fc-205">生産プロセス</span><span class="sxs-lookup"><span data-stu-id="3e8fc-205">Production processing</span></span>

- <span data-ttu-id="3e8fc-206">CW 製品では、フォーミュラ製品のバッチ オーダーのみサポートします。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-206">For catch weight products, only batch orders for formula products are supported.</span></span>
- <span data-ttu-id="3e8fc-207">かんばんの機能では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-207">Kanban functionality isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-208">CW 製品では、シリアル番号を消費する前に登録することはできません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-208">For catch weight products, serial numbers can't be registered before consumption.</span></span>
- <span data-ttu-id="3e8fc-209">逆仕訳ライセンス プレートの機能では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-209">The functionality for reversing license plates isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-210">CW 製品では、完了報告はシリアル番号で登録できません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-210">For catch weight products, reporting as finished cannot be registered by serial number.</span></span>

### <a name="transportation-management-processing"></a><span data-ttu-id="3e8fc-211">輸送管理プロセス</span><span class="sxs-lookup"><span data-stu-id="3e8fc-211">Transportation management processing</span></span>

- <span data-ttu-id="3e8fc-212">積荷構築のワークベンチ処理では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-212">Load building workbench processing isn't supported for catch weight products.</span></span>
- <span data-ttu-id="3e8fc-213">配送要求の明細行では、CW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-213">Transport request lines aren't supported for catch weight products.</span></span>
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="3e8fc-214">倉庫管理による CW 製品のプロセス用その他制限および動作</span><span class="sxs-lookup"><span data-stu-id="3e8fc-214">Other restrictions and behaviors for catch weight product processing with warehouse management</span></span>

- <span data-ttu-id="3e8fc-215">ユーザーが追跡用分析コードを識別するよう求められないピッキング処理の間に、重量の割り当ては平均重量に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-215">During picking processes where the user isn't prompted to identify tracking dimensions, the weight assignment is done based on the average weight.</span></span> <span data-ttu-id="3e8fc-216">たとえば、追跡用分析コードの組み合わせが同じ場所で使用されたときや、ユーザー処理のピッキング後に追跡用分析コード値は 1 つだけその場所に残っているときに、この現象が発生します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-216">This behavior occurs when, for example, a combination of tracking dimensions is used in the same location and, after a user processes picking, only one tracking dimension value is left in the location.</span></span>
- <span data-ttu-id="3e8fc-217">在庫が倉庫管理プロセスで構成されている CW 製品用に予約された場合、たとえ手持ち最後の数量であっても、予約は定義されている最小重量に基づいて処理されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-217">When inventory is reserved for a catch weight product that is configured for warehouse management processes, the reservation is done based on the minimum weight that is defined, even if this quantity is the on-hand last handling quantity.</span></span> <span data-ttu-id="3e8fc-218">この動作は、倉庫管理プロセスに対して設定されていない品目の動作と異なります。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-218">This behavior differs from the behavior for items that aren't configured for warehouse management processes.</span></span>
- <span data-ttu-id="3e8fc-219">キャパシティの計算 (ウェーブのしきい値、ワーク最大改行、コンテナーの最大値、場所の負荷能力など) の一部として重量を使用する処理は、在庫の実重量を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-219">Processes that use the weight as part of capacity calculations (wave thresholds, work maximum breaks, container maximums, location load capacities, and so on) don't use the actual weight of the inventory.</span></span> <span data-ttu-id="3e8fc-220">代わりに、処理は製品に対して定義されている現物処理重量に基づいています。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-220">Instead, the processes are based on the physical handling weight that is defined for the product.</span></span>
- <span data-ttu-id="3e8fc-221">一般に、小売機能ではCW 製品はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-221">In general, Retail functionality isn't supported for catch weight products.</span></span>
 
### <a name="catch-weight-tags"></a><span data-ttu-id="3e8fc-222">CW タグ</span><span class="sxs-lookup"><span data-stu-id="3e8fc-222">Catch weight tags</span></span>

<span data-ttu-id="3e8fc-223">現時点では、CW タグの機能は次のシナリオの一部としてのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-223">Currently, the functionality for catch weight tags is supported only as part of the following scenarios:</span></span>

- <span data-ttu-id="3e8fc-224">発注書の倉庫アプリケーション受信処理をしたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-224">When processing purchase order warehouse app receiving.</span></span>
- <span data-ttu-id="3e8fc-225">倉庫アプリケーション経由で読み込み受信の処理をしたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-225">When processing load receiving via warehouse app.</span></span>
- <span data-ttu-id="3e8fc-226">発注書の読み取りに関連付けられるライセンス プレートの受信では、入庫プロセス時に重量の割り当てが要求されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-226">For license plate receiving that is related to a purchase order load, weight assignment is requested during the receiving process.</span></span> <span data-ttu-id="3e8fc-227">これに対し、移動オーダー入庫では、移動オーダーの出荷データから重量が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-227">By contrast, for transfer order receiving, the weight from the shipment data for the transfer order is used.</span></span>
- <span data-ttu-id="3e8fc-228">移動オーダーの品目および非倉庫管理からの明細行の入荷は、倉庫を処理します。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-228">For transfer order item and line receiving that comes from a non-warehouse management process warehouse.</span></span>
- <span data-ttu-id="3e8fc-229">販売の返品注文の入荷処理は CW タグを記録できますが、もともと特定の販売注文の明細行に出荷された同じタグの場合、処理は検証されません。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-229">The processing of sales return order receiving can record catch weight tags, but the processing won't be validated if the tags are the same tags that were originally shipped for a particular sales order line.</span></span>
- <span data-ttu-id="3e8fc-230">在庫ステータスが倉庫アプリケーションを使用して変更処理されたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-230">When processing a inventory status changed by using the warehouse app.</span></span>
- <span data-ttu-id="3e8fc-231">倉庫アプリケーションを使用して倉庫移動が行われたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-231">When a warehouse transfer is done by using the warehouse app.</span></span>
- <span data-ttu-id="3e8fc-232">倉庫アプリケーション経由で調整を出し入れしたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-232">When processing adjustment in and out via the warehouse app.</span></span>
- <span data-ttu-id="3e8fc-233">ピッキング作業が販売と在庫移動の作業に対して処理されたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-233">When picking work is processed for sales and transfer orders.</span></span> <span data-ttu-id="3e8fc-234">(CW タグは、製造コンポーネントのピッキングに記録されません。)</span><span class="sxs-lookup"><span data-stu-id="3e8fc-234">(Note that catch weight tags can't be recorded for production component picking.)</span></span>
- <span data-ttu-id="3e8fc-235">コンテナーが使用されているかどうかにかかわらず、ピッキング済数量が積荷明細行から減らされたとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-235">When picked quantities are reduced from load lines, regardless of whether containers are used.</span></span>
- <span data-ttu-id="3e8fc-236">製品が梱包ステーションでコンテナーに梱包されるとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-236">When products are packed into containers at a packing station.</span></span>
- <span data-ttu-id="3e8fc-237">コンテナーが再度開くとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-237">When containers are reopened.</span></span>
- <span data-ttu-id="3e8fc-238">フォーミュラの製品が倉庫アプリケーションを使用して終了報告があるとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-238">When formula products are reported as finished by using the warehouse app.</span></span>
- <span data-ttu-id="3e8fc-239">配送負荷が倉庫のアプリケーションを使用して処理されるとき。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-239">When transport loads are processed by using the warehouse app.</span></span>

<span data-ttu-id="3e8fc-240">CW タグは、フォームで手動作成したアプリケーション プロセスの倉庫管理を使うか、またはデータ エンティティのプロセスを使って作成できます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-240">A catch weight tag can either be created using a warehousing app process, manually created in the form, or creating using a data entity process.</span></span> <span data-ttu-id="3e8fc-241">CW タグが、購買注文明細行などの元伝票明細行に関連付けられている場合、タグは登録されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-241">If a catch weight tag gets associated with an inbound source document line, such as purchase order line, the tag will be registered.</span></span> <span data-ttu-id="3e8fc-242">明細行が発信処理のために使用される場合。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-242">If the line is used for outbound processing.</span></span> <span data-ttu-id="3e8fc-243">タグは出荷時に更新されます。</span><span class="sxs-lookup"><span data-stu-id="3e8fc-243">The tag will be updated as shipped.</span></span>
