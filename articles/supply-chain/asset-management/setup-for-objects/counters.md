---
title: 資産測定
description: このトピックでは、資産管理で資産測定を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc6b9e944a7ecf6b769a8e3c2f9b1fbafaa60734
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626111"
---
# <a name="counters"></a><span data-ttu-id="76586-103">カウンター</span><span class="sxs-lookup"><span data-stu-id="76586-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76586-104">このトピックでは、資産管理でカウンター タイプを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="76586-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="76586-105">カウンター タイプは、生産時間数や資産で生産される数量など、資産のカウンター登録を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="76586-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="76586-106">資産タイプは、カウンター タイプに関連しています。</span><span class="sxs-lookup"><span data-stu-id="76586-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="76586-107">つまり、資産で使用される資産タイプに対してカウンターが設定されている場合にのみ、カウンターを資産に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="76586-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="76586-108">資産に対してカウンター登録を行う前に、まず**カウンター**で使用するカウンター タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="76586-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="76586-109">次に、**カウンター**の資産に対するカウンター登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="76586-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="76586-110">カウンターは、メンテナンス計画で使用できます。</span><span class="sxs-lookup"><span data-stu-id="76586-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="76586-111">メンテナンス計画明細行は、たとえば、生産時間数や生産数量に関連するタイプ「カウンター」にすることができます。</span><span class="sxs-lookup"><span data-stu-id="76586-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="76586-112">カウンター登録は、生産時間または生産数量に基づいて、手動または自動で更新できます。</span><span class="sxs-lookup"><span data-stu-id="76586-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="76586-113">カウンターは、3 つの更新方法のいずれかを使用するように設定できます (**カウンター**の**更新**フィールドで選択)。</span><span class="sxs-lookup"><span data-stu-id="76586-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="76586-114">手動 - カウンター値を手動で登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76586-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="76586-115">生産時間 - カウンターは生産時間数に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="76586-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="76586-116">生産数量 - カウンターは生産数量に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="76586-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="76586-117">生産数量を使用すると、登録された*すべて*の品目がカウンター登録、良品数量、および不良数量に含まれます。</span><span class="sxs-lookup"><span data-stu-id="76586-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="76586-118">必要に応じて、いつでも手動でカウンター登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="76586-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="76586-119">資産カウンター登録のカウンター タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="76586-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="76586-120">**資産管理** > **設定** > **資産タイプ** > **カウンター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="76586-121">**新規作成**を選択して、新しいカウンター タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="76586-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="76586-122">**カウンター** フィールドに ID を挿入し、**名前**フィールドにカウンター名を挿入します。</span><span class="sxs-lookup"><span data-stu-id="76586-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="76586-123">**一般**クイック タブの**単位**フィールドで、カウンター単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="76586-124">**更新**フィールドで、カウンターに使用する更新方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="76586-125">資産構造の子資産が親資産で行われたカウンター登録を自動的に継承する必要がある場合は、**カウンター値の継承**トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="76586-126">**総計**フィールドで、このカウンター タイプのカウンターに使用する合計方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="76586-127">「合計」は、合計値に登録値を継続的に追加するために使用される標準的な選択です。</span><span class="sxs-lookup"><span data-stu-id="76586-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="76586-128">"平均" は、資産の温度、振動、または資産の摩耗など、しきい値を監視するようにカウンターが設定されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="76586-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="76586-129">**偏差上**フィールドで、手動カウンター登録が予想範囲内にあるかどうかを検証するために、上位レベルをパーセントで挿入します。</span><span class="sxs-lookup"><span data-stu-id="76586-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="76586-130">検証は、既存のカウンター登録の線形増加に基づいています。</span><span class="sxs-lookup"><span data-stu-id="76586-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="76586-131">**偏差下**フィールドで、手動カウンター登録が予想範囲内にあるかどうかを検証するために、下位レベルをパーセントで挿入します。</span><span class="sxs-lookup"><span data-stu-id="76586-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="76586-132">検証は、既存のカウンター登録の線形減少に基づいています。</span><span class="sxs-lookup"><span data-stu-id="76586-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="76586-133">**タイプ** フィールドで、手動でカウンター登録を行うときに、定義された範囲外の偏差が発生した場合に表示するメッセージの種類 (情報、警告、エラー) を選択します。</span><span class="sxs-lookup"><span data-stu-id="76586-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="76586-134">**資産タイプ**クイック タブで、カウンターを使用できるようにする資産タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="76586-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="76586-135">**関連する資産カウンター** クイック タブで、このカウンターの更新時に自動的に更新するカウンターを追加します。</span><span class="sxs-lookup"><span data-stu-id="76586-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="76586-136">関連するカウンターは、カウンターの設定で、関連するカウンターに関連する資産タイプがある場合にのみ、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="76586-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="76586-137">たとえば、"生産時間" のカウンターを設定し、資産タイプ "トラック エンジン" を追加します。</span><span class="sxs-lookup"><span data-stu-id="76586-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="76586-138">そのカウンターが更新されると、関連するカウンター "オイル" も同じカウンター値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="76586-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="76586-139">**カウンター**での設定には、「時間」の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76586-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="76586-140">また、「オイル」カウンターでは、資産タイプの「トラック エンジン」を**資産タイプ** クイック タブに追加して、カウンター関係を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76586-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="76586-141">時間とオイル カウンターの設定の例については、以下のスクリーンショットを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76586-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="76586-142">**カウンター**のカウンター タイプに資産タイプが追加されると、そのカウンターは [資産タイプ](../setup-for-objects/object-types.md) の**カウンター** クイック タブの資産タイプに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="76586-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![図 1](media/071-setup-for-objects.png)

