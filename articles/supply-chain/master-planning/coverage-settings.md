---
title: 補充設定
description: このトピックでは、在庫品目要求の計算にマスター スケジューリングが使用する補充設定について説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1134f734f1025151a56b2a72266a6baa5763ba4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982723"
---
# <a name="coverage-settings"></a><span data-ttu-id="3b1d9-103">補充設定</span><span class="sxs-lookup"><span data-stu-id="3b1d9-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b1d9-104">マスタ スケジューリングでは補充設定を使用して在庫品目要求を計算します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="3b1d9-105">補充設定は次のように複数の方法で指定できます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="3b1d9-106">補充グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="3b1d9-107">リンク先のすべての製品の設定を含む補充グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="3b1d9-108">補充グループを作成するには、**マスター プラン &gt; 設定 &gt; 補充 &gt; 補充グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="3b1d9-109">補充グループは製品にリンクできます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="3b1d9-110">サイト、倉庫、製品分析コードに固有のリンクの場合、**品目の補充**ページで**補充グループ**のフィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="3b1d9-111">一般のリンクの場合は、製品分析コードに関係なく**製品の詳細**ページの**計画**クイック タブの**補充グループ** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="3b1d9-112">既定では、補充グループを製品にリンクしない場合は、マスター プランでは**マスター プランのパラメーター**で指定された一般補充グループが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="3b1d9-113">製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="3b1d9-114">特定の製品の補充設定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="3b1d9-115">**製品管理情報 &gt; 製品 &gt; リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3b1d9-116">製品を選択し、アクション ペイン、**計画**タブ、**補充**グループで、**品目補充**を選択し、**品目補充**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="3b1d9-117">製品が補充グループにすでにリンクされている場合、**上書き**フィールドで設定した補充グループの設定は無視できます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="3b1d9-118">**品目の補充**ページの補充設定は、**補充グループ** ページの設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="3b1d9-119">ウィザードで製品の補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="3b1d9-120">ウィザードでは、主要な品目補充パラメータを設定する手順を順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="3b1d9-121">**品目の補充**ページのアクション ペインで**ウィザード**を選択して**品目補充ウィザード**を開きます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="3b1d9-122">分析コード グループの補充設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="3b1d9-123">**製品管理情報 &gt; 製品 &gt; リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="3b1d9-124">**管理**セクションの、**一般**クイック タブにおける、**リリース済製品の詳細**ページで、**保管分析コード グループ** フィールドのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="3b1d9-125">**保管分析コード グループ** ページで**分析コード別補充計画**チェック ボックスを選択して、保管分析コード グループの分析コードについて補充設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="3b1d9-126">コンフィギュレーション、色、サイズ、スタイルなどすべての製品分析コードで、**分析コード別補充計画**フィールドを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="3b1d9-127">補充コード</span><span class="sxs-lookup"><span data-stu-id="3b1d9-127">Coverage codes</span></span>

<span data-ttu-id="3b1d9-128">さまざまな補充方法を使用するようにマスター プランをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="3b1d9-129">補充方法またはロットサイズ変更方法は、購入した品目または生産された品目のバッチサイズを決定するためにシステムで使用される技術です。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="3b1d9-130">各補充方法には、次のいずれかの補充コードが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="3b1d9-131">**手動** - システムが品目に対して、購入、移動、または製造オーダーを提案しないロットサイズ変更方法。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="3b1d9-132">品目のプランナーは、品目の補充に必要な注文の作成を担当します。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="3b1d9-133">**要求ごと**: システムが品目の要求ごとに計画購買、移動、または製造オーダーが作成されるロットサイズ変更方法。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="3b1d9-134">これは一般に、断続的な需要がある高価な品目に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="3b1d9-135">**期間ごと**: 品目に対する期間のすべての需要を品目の 1 つの注文にまとめるロットサイズ変更方法。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="3b1d9-136">この注文は、期間の初日に対して計画され、その数量が設定された期間における正味必要量となります。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="3b1d9-137">この期間は、品目の最初の需要から始まり、定義された期間を対象としています。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="3b1d9-138">次の期間は、品目の次の要件から開始されます。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="3b1d9-139">**最小/最大**: 予測手持在庫がしきい値を下回った場合に、特定のレベルまでの在庫の補充を含むロットサイズ変更方法です。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="3b1d9-140">補充数量は、最大レベルと予測手持在庫レベルの差額になります。</span><span class="sxs-lookup"><span data-stu-id="3b1d9-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="3b1d9-141">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3b1d9-141">Additional resources</span></span>

[<span data-ttu-id="3b1d9-142">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="3b1d9-142">Master plans overview</span></span>](master-plans.md)
