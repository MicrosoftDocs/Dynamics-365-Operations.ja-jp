---
title: 国立モーター貨物の分類 (NMFC) コード
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management で国立モーター貨物の分類 (NMFC) コードの使用方法について説明します
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941885"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="243e9-103">国立モーター貨物の分類 (NMFC) コード</span><span class="sxs-lookup"><span data-stu-id="243e9-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="243e9-104">国立モーター貨物の分類 (NMFC) コードを使用すると、出荷可能な品目を分類できます。</span><span class="sxs-lookup"><span data-stu-id="243e9-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="243e9-105">NMFC コードは、商品をグループ化するために使用される指定です。</span><span class="sxs-lookup"><span data-stu-id="243e9-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="243e9-106">これにより、配送会社はトラックの適合性、積載の問題、問題の処理、および傷みやすさなどの考慮事項に基づいて品目を分類することで、出荷の商品を評価できます。</span><span class="sxs-lookup"><span data-stu-id="243e9-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="243e9-107">商品は、50 ～ 500 の範囲内の番号を使用して、18 貨物クラスのいずれかにグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="243e9-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="243e9-108">商品がグループ化されるクラスは、密度、収納性、取り扱い、および責任の 4 つの輸送特性に対する評価に基づいています。</span><span class="sxs-lookup"><span data-stu-id="243e9-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="243e9-109">これらの特性の組み合わせで、商品の輸送性が確立されます。</span><span class="sxs-lookup"><span data-stu-id="243e9-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="243e9-110">NMFCコードは、トラックの負荷より小さい (LTL) すべての出荷品目に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="243e9-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="243e9-111">たとえば、ラップトップには 2.5 に分類される NMFC が割り当てられ、電気コードには 65 に分類される NMFC が割り当てられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="243e9-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="243e9-112">この機能を使用すると、作業者が NMFC コードを使用して LTL 出荷品目を分類しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="243e9-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="243e9-113">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="243e9-113">Here are some examples:</span></span>

- <span data-ttu-id="243e9-114">会社が船荷証券 (BOL) に貨物の説明を含めている場合、配送業者は貨物が何であるかをある程度知っています。</span><span class="sxs-lookup"><span data-stu-id="243e9-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="243e9-115">配送業者の多くは、出荷する貨物の種類に基づいてビジネス モデル全体を構築しているため、貨物の分類は重要です。</span><span class="sxs-lookup"><span data-stu-id="243e9-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="243e9-116">この分類は特定の積荷の原価を決定するのに使用されるため、会社にとって不可欠な場合があります。</span><span class="sxs-lookup"><span data-stu-id="243e9-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="243e9-117">会社は、LTL 物流および輸送会社の収益性を特定できます。</span><span class="sxs-lookup"><span data-stu-id="243e9-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="243e9-118">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での NMFC コードの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="243e9-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="243e9-119">必要条件</span><span class="sxs-lookup"><span data-stu-id="243e9-119">Prerequisites</span></span>

<span data-ttu-id="243e9-120">NMFC コードを作成する前に、そのコードにマップする必要があるすべての LTL 貨物クラスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="243e9-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="243e9-121">LTL 貨物クラスは品目のカテゴリを表しますが、NMFC コードは 18 の各貨物クラスの特定の商品に関連しています。</span><span class="sxs-lookup"><span data-stu-id="243e9-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="243e9-122">LTL クラスの使用方法の詳細については、[トラックの負荷より小さい (LTL) クラス](ltl-class.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="243e9-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="243e9-123">NMFC コードの作成</span><span class="sxs-lookup"><span data-stu-id="243e9-123">Create an NMFC code</span></span>

<span data-ttu-id="243e9-124">NMFC コードを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="243e9-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="243e9-125">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="243e9-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="243e9-126">**倉庫管理 \> 設定 \> 在庫 \> NMFC コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="243e9-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="243e9-127">**輸送管理 \> 設定 \> 輸送標準 \> NMFC コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="243e9-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="243e9-128">**新規** を選択して、NMFC コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="243e9-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="243e9-129">その後、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="243e9-129">Then set the following fields:</span></span>

    - <span data-ttu-id="243e9-130">**NMFC コード** – 商品タイプの NMFC コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="243e9-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="243e9-131">**名前** – NMFC コードの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="243e9-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="243e9-132">**LTL クラス** – NMFC コードに関連付けられている LTL クラスを選択します。</span><span class="sxs-lookup"><span data-stu-id="243e9-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="243e9-133">**BOL 材料取り扱い単位** – 出荷の既定の処理タイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="243e9-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="243e9-134">例: NMFC コードの設定</span><span class="sxs-lookup"><span data-stu-id="243e9-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="243e9-135">次の例は、異なる製品で使用できる 2 つの異なる NMFC コードの設定方法を示します。</span><span class="sxs-lookup"><span data-stu-id="243e9-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="243e9-136">**倉庫管理 \> 設定 \> 在庫 \> NMFC コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="243e9-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="243e9-137">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="243e9-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="243e9-138">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="243e9-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="243e9-139">**NMFC コード:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="243e9-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="243e9-140">**名前:** *コンピューター*</span><span class="sxs-lookup"><span data-stu-id="243e9-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="243e9-141">**LTL クラス:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="243e9-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="243e9-142">**BOL 材料取り扱い単位:** *単位*</span><span class="sxs-lookup"><span data-stu-id="243e9-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="243e9-143">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="243e9-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="243e9-144">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="243e9-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="243e9-145">新しい明細行で、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="243e9-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="243e9-146">**NMFC コード:** *125*</span><span class="sxs-lookup"><span data-stu-id="243e9-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="243e9-147">**名前:** *電話*</span><span class="sxs-lookup"><span data-stu-id="243e9-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="243e9-148">**LTL クラス:** *125*</span><span class="sxs-lookup"><span data-stu-id="243e9-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="243e9-149">**BOL 材料取り扱い単位:** *単位*</span><span class="sxs-lookup"><span data-stu-id="243e9-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="243e9-150">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="243e9-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="243e9-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="243e9-151">Additional resources</span></span>

- [<span data-ttu-id="243e9-152">トラックの負荷より小さい (LTL) クラス</span><span class="sxs-lookup"><span data-stu-id="243e9-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="243e9-153">船荷証券の作成</span><span class="sxs-lookup"><span data-stu-id="243e9-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
