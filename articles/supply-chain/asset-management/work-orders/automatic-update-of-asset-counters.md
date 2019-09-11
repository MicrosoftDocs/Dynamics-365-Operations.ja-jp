---
title: 資産カウンターの自動更新
description: このトピックでは、資産管理での資産カウンターの自動更新について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875763"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="fc9ba-103">資産カウンターの自動更新</span><span class="sxs-lookup"><span data-stu-id="fc9ba-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fc9ba-104">前のセクションでは、資産カウンターの手動登録について説明されています。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="fc9ba-105">資産カウンターの設定については、[カウンター](../setup-for-objects/counters.md) で説明されています。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="fc9ba-106">カウンター値は、生産時間または生産数量に基づいて、生産登録から自動的に更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="fc9ba-107">これは、**資産カウンターの更新**で行われます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="fc9ba-108">1 つのパラメーター、**開始日**を挿入することにより、1 つまたは複数の資産を更新できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="fc9ba-109">このパラメーターでは、生産登録の開始日 (生産時間数や生産数量) を指定します。これは、カウンター値を更新する開始日を意味します。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="fc9ba-110">リソースに関連する、*および*生産数量または生産時間数に基づいて更新するように設定されている資産カウンターがあるすべての資産は、自動更新に含まれ、新しいカウンター値が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="fc9ba-111">生産数量に基づくカウンターについては、登録されている良品数量およびエラー数量がカウントに含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="fc9ba-112">生産数量の登録に使用されている単位がカウンターで使用されている単位と異なる場合、数量はカウンター単位に対応するように換算されます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="fc9ba-113">上記に示されたように、自動カウンターは生産登録から更新できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="fc9ba-114">したがって、カウンターを自動的に更新する資産は、リソース (マシン) に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="fc9ba-115">以下で、**資産管理**モジュールにおける資産のカウンターの自動更新の基礎として使用される製造オーダー (**生産管理**モジュール) の設定と処理の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="fc9ba-116">生産数量または生産時間数がリソースに登録されたら、関連付けられている資産カウンターを更新できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="fc9ba-117">**資産管理** > **定期処理** > **資産** > **資産カウンターの更新**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="fc9ba-118">**開始日**フィールドで、自動更新の開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="fc9ba-119">このフィールドの日付は、**工順トランザクション** (**生産管理** > **照会およびレポート** > **生産** > **工順トランザクション** > **現物日付**フィールド) からの "仕掛品" の日付です。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="fc9ba-120">自動更新で特定の資産、資産タイプ、またはリソースを選択する場合は、**対象に含めるレコード** クイックタブで**フィルター**をクリックし、関連する選択を行います。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="fc9ba-121">**バックグラウンドで実行**クイック タブで、必要に応じて自動更新をバッチ ジョブとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![図 1](media/12-work-orders.png)

5. <span data-ttu-id="fc9ba-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-123">Click **OK**.</span></span> <span data-ttu-id="fc9ba-124">資産カウンターの自動更新が完了すると、**資産カウンター** (**資産管理** > **共通** > **資産** > **すべての資産** > 資産を選択 >**カウンター** ボタン) に関連するカウンター登録が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="fc9ba-125">**資産カウンターの合計**では、すべての資産のすべてのカウンター タイプで行われた最新の登録の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="fc9ba-126">**資産管理** > **照会** > **資産** > **資産カウンター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="fc9ba-127">このビューは**資産カウンター**とよく似ていますが、**資産の集計値**で登録を追加または編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="fc9ba-128">概要のみに対するものです。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-128">It is for overview only.</span></span>

![図 2](media/13-work-orders.png)


- <span data-ttu-id="fc9ba-130">自動的に更新されるカウンター タイプについては、依然として手動のカウンター値の登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="fc9ba-131">詳細については、"資産カウンターの手動更新" セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="fc9ba-132">別のカウンターに関連するカウンターを設定できます。つまり、カウンターが更新されると、同時に関連するカウンターが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="fc9ba-133">関連するカウンターの設定については、[カウンター](../setup-for-objects/counters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc9ba-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
