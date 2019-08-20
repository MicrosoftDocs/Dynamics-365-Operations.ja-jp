---
title: 資産測定
description: このトピックでは、資産管理で資産測定を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783413"
---
# <a name="asset-measures"></a><span data-ttu-id="53d7c-103">資産測定</span><span class="sxs-lookup"><span data-stu-id="53d7c-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="53d7c-104">このトピックでは、資産管理で資産測定を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="53d7c-105">資産測定タイプは、生産時間数や資産で生産される数量など、資産の測定登録を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="53d7c-106">資産タイプは、資産測定タイプに関連しています。</span><span class="sxs-lookup"><span data-stu-id="53d7c-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="53d7c-107">つまり、資産で使用される資産タイプに対して資産測定が設定されている場合にのみ、資産測定を資産に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="53d7c-108">資産に対して測定登録を行う前に、まず**カウンター**で使用する資産測定タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="53d7c-109">次に、**資産測定**の資産に対する測定登録を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="53d7c-110">資産測定は、メンテナンス計画で使用できます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="53d7c-111">メンテナンス計画明細行は、たとえば、生産時間数や生産数量に関連するタイプ「カウンター」にすることができます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="53d7c-112">資産測定登録は、生産時間または生産数量に基づいて、手動または自動で更新できます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="53d7c-113">資産測定は、3 つの更新方法のいずれかを使用するように設定できます (**カウンター**の**更新**フィールドで選択)。</span><span class="sxs-lookup"><span data-stu-id="53d7c-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="53d7c-114">手動 - 資産測定値を手動で登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d7c-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="53d7c-115">生産時間 - カウンターは生産時間数に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="53d7c-116">生産数量 - カウンターは生産数量に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="53d7c-117">生産数量を使用すると、登録された*すべて*の品目が測定登録、良品数量、および不良数量に含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="53d7c-118">必要に応じて、いつでも手動で資産測定登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="53d7c-119">資産カウンター登録のカウンター タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="53d7c-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="53d7c-120">**資産管理** > **設定** > **資産タイプ** > **カウンター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="53d7c-121">**新規**を選択して、新しい資産測定タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="53d7c-122">**カウンター** フィールドに ID を挿入し、**名前**フィールドにカウンター名を挿入します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="53d7c-123">**一般**クイック タブの**単位**フィールドで、測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="53d7c-124">**更新**フィールドで、資産測定に使用する更新方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="53d7c-125">資産構造の子資産が親資産で行われた資産測定登録を自動的に継承する必要がある場合は、**カウンター値の継承**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="53d7c-126">**総計**フィールドで、この資産測定タイプの資産測定に使用する合計方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="53d7c-127">「合計」は、合計値に登録値を継続的に追加するために使用される標準的な選択です。</span><span class="sxs-lookup"><span data-stu-id="53d7c-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="53d7c-128">「平均」は、資産の温度、振動、または資産の摩耗など、しきい値を監視するように資産測定が設定されている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="53d7c-129">**偏差上**フィールドで、手動資産測定登録が予想範囲内にあるかどうかを検証するために、上位レベルをパーセントで挿入します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="53d7c-130">検証は、既存の資産測定登録の線形増加に基づいています。</span><span class="sxs-lookup"><span data-stu-id="53d7c-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="53d7c-131">**偏差下**フィールドで、手動資産測定登録が予想範囲内にあるかどうかを検証するために、下位レベルをパーセントで挿入します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="53d7c-132">検証は、既存の資産測定登録の線形減少に基づいています。</span><span class="sxs-lookup"><span data-stu-id="53d7c-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="53d7c-133">**タイプ** フィールドで、手動で資産測定登録を行うときに、定義された範囲外の偏差が発生した場合に表示するメッセージの種類 (情報、警告、エラー) を選択します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="53d7c-134">**資産タイプ**クイック タブで、資産測定を使用できるようにする資産タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="53d7c-135">**関連する資産メジャー**クイック タブで、この資産測定の更新時に自動的に更新する資産測定を追加します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="53d7c-136">関連する資産測定は、資産測定の設定で、関連する資産測定に関連する資産タイプがある場合にのみ、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="53d7c-137">たとえば、「生産時間」の資産測定を設定し、資産タイプ「トラック エンジン」を追加します。</span><span class="sxs-lookup"><span data-stu-id="53d7c-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="53d7c-138">その資産測定が更新されると、関連するカウンター「オイル」も同じ資産測定値で更新されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="53d7c-139">**カウンター**での設定には、「時間」の設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="53d7c-140">また、「オイル」資産測定では、資産タイプの「トラック エンジン」を**資産タイプ** クイック タブに追加して、資産測定関係を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d7c-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="53d7c-141">時間とオイル資産測定の設定の例については、以下のスクリーンショットを参照してください。</span><span class="sxs-lookup"><span data-stu-id="53d7c-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="53d7c-142">**カウンター**の資産測定タイプに資産タイプが追加されると、その資産測定は[資産タイプ](../setup-for-objects/object-types.md) の**カウンター** クイック タブの資産タイプに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="53d7c-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![図 1](media/071-setup-for-objects.png)


