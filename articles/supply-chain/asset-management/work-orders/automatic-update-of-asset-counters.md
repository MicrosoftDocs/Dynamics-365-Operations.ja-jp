---
title: 資産カウンターの自動更新
description: このトピックでは、資産管理での資産カウンターの自動更新について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3e8619439545cf3ea42f84a6dd7ee6ffdf1026e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021933"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="c6e88-103">資産カウンターの自動更新</span><span class="sxs-lookup"><span data-stu-id="c6e88-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6e88-104">資産カウンターの手動登録については、[資産カウンターの手動登録](../work-orders/manual-update-of-asset-counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6e88-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="c6e88-105">資産カウンターの設定方法の詳細については[カウンター](../setup-for-objects/counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6e88-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="c6e88-106">カウンター値は、生産時間または生産数量 (つまり、生産された数量) に基づいて、生産登録から自動的に更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="c6e88-107">この更新は、**資産カウンターの更新** ページで行われます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="c6e88-108">1 つのパラメーター、**開始日** を設定することにより、1 つまたは複数の資産を更新できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="c6e88-109">このパラメーターは、生産登録の開始日 (生産時間または生産数量) を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="c6e88-110">つまり、カウンターの値を更新する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="c6e88-111">リソースに関連する、*および* 生産時間または生産数量に基づいて更新するように設定されている資産カウンターがあるすべての資産は、自動更新に含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="c6e88-112">新しいカウンター値が作成されます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-112">New counter values will be created.</span></span>

<span data-ttu-id="c6e88-113">生産数量に基づくカウンターについては、良品数量と登録されている不良数量の両方がカウントされます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="c6e88-114">生産数量の登録に使用されている単位がカウンターで使用されている単位と異なる場合、数量はカウンター単位に対応するように換算されます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="c6e88-115">上記に示されたように、自動カウンターは生産登録から更新できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="c6e88-116">したがって、カウンターを自動的に更新する資産は、リソース (マシン) に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6e88-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="c6e88-117">生産数量または生産時間数がリソースに登録されたら、関連付けられている資産カウンターを更新できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="c6e88-118">**資産管理** > **定期処理** > **資産** > **資産カウンターの更新** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="c6e88-119">**開始日** フィールドで、自動更新の開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="c6e88-120">このフィールドの日付は、**工順トランザクション** (**生産管理** > **照会およびレポート** > **生産** > **工順トランザクション** > **現物日付** フィールド) からの "仕掛品" の日付です。</span><span class="sxs-lookup"><span data-stu-id="c6e88-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="c6e88-121">**対象に含めるレコード** クイック タブでは、自動更新のための特定の資産、資産タイプ、またはリソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="c6e88-122">**フィルター** を選択して、関連する選択を行います。</span><span class="sxs-lookup"><span data-stu-id="c6e88-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="c6e88-123">**バックグラウンドで実行** クイック タブでは、必要に応じて自動更新をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="c6e88-124">次の図は、**資産カウンターの更新** ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c6e88-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![図 1](media/12-work-orders.png)

5. <span data-ttu-id="c6e88-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-126">Select **OK**.</span></span> 

<span data-ttu-id="c6e88-127">資産カウンターの自動更新が終了すると、**資産カウンター** ページの資産に関連するカウンターの登録を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="c6e88-128">**資産管理** > **共通** > **資産** > **全資産** の順に選択して、資産を選択してからアクション ウィンドウの **資産** タブの、**予防的** グループで、**カウンター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="c6e88-129">**資産の集計値** ページでは、すべての資産のすべてのカウンター タイプで行われた最新の登録の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="c6e88-130">**資産管理** > **照会** > **資産** > **資産の集計値** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="c6e88-131">このページは **資産カウンター** ページに似ていますが、登録を追加または編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="c6e88-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="c6e88-132">概要のみに対するものです。</span><span class="sxs-lookup"><span data-stu-id="c6e88-132">It's for overview only.</span></span>

<span data-ttu-id="c6e88-133">次の図は、**資産の集計値** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c6e88-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![図 2](media/13-work-orders.png)

<span data-ttu-id="c6e88-135">次のポイントに注意します。</span><span class="sxs-lookup"><span data-stu-id="c6e88-135">Note the following points:</span></span>

- <span data-ttu-id="c6e88-136">自動的に更新されるカウンター タイプには、手動のカウンター値の登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="c6e88-137">詳細については、[資産カウンターの手動更新](../work-orders/manual-update-of-asset-counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6e88-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="c6e88-138">別のカウンターに関連するカウンターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="c6e88-139">この場合、カウンターが更新されると、関連するカウンターが同時に自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c6e88-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="c6e88-140">関連するカウンターの設定方法の詳細については、[カウンター](../setup-for-objects/counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6e88-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

