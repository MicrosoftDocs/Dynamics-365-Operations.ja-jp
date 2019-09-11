---
title: メンテナンス ダウンタイム
description: このトピックでは資産管理のメンテナンス ダウンタイムについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918247"
---
# <a name="maintenance-downtime"></a><span data-ttu-id="afd57-103">メンテナンス ダウンタイム</span><span class="sxs-lookup"><span data-stu-id="afd57-103">Maintenance downtime</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="afd57-104">作業指示書で選択した資産に対して、メンテナンス ダウンタイム登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="afd57-104">You can create maintenance downtime registrations on the asset selected on a work order.</span></span> <span data-ttu-id="afd57-105">これは、生産領域の 1 つ以上のマシンにメンテナンス ダウンタイムを登録する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="afd57-105">This is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="afd57-106">まず、使用するメンテナンス ダウンタイムの理由コードを作成します (例えば故障や計画停止など)。</span><span class="sxs-lookup"><span data-stu-id="afd57-106">First, you create the maintenance downtime reason codes that you want to use, for example, breakdown and planned stop.</span></span> <span data-ttu-id="afd57-107">これは、**メンテナンス ダウンタイムの理由コード**で実行されます。</span><span class="sxs-lookup"><span data-stu-id="afd57-107">This is done in **Maintenance downtime reason codes**.</span></span> <span data-ttu-id="afd57-108">次に、**メンテナンス ダウンタイム**でメンテナンス ダウンタイムの登録を作成し、関連する理由コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="afd57-108">Next, you can create maintenance downtime registrations in **Maintenance downtime** and add the relevant reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="afd57-109">メンテナンス ダウンタイムの理由コードの作成</span><span class="sxs-lookup"><span data-stu-id="afd57-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="afd57-110">**資産管理** > **設定** > **作業指示書** > **メンテナンス ダウンタイムの理由コード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-110">Click **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="afd57-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-111">Click **New**.</span></span>

3. <span data-ttu-id="afd57-112">**メンテナンス ダウンタイムの理由コード** フィールドに ID を挿入します。</span><span class="sxs-lookup"><span data-stu-id="afd57-112">Insert an ID in the **Maintenance downtime reason code** field.</span></span>

4. <span data-ttu-id="afd57-113">**名前**フィールドに、理由コードの名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="afd57-113">Insert a name for the reason code in the **Name** field.</span></span>

5. <span data-ttu-id="afd57-114">理由コードを資産 KPI の計算に含める必要がある場合は、**KPI include** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd57-114">Select the **KPI include** check box if the reason code should be included in asset KPI calculations.</span></span> <span data-ttu-id="afd57-115">一般に、想定されるパフォーマンスには影響しないため、計画済生産停止は KPI 計算には含めません。</span><span class="sxs-lookup"><span data-stu-id="afd57-115">Generally, planned production stops should not be included in KPI calculations as they do not impact expected performance.</span></span>

6. <span data-ttu-id="afd57-116">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-116">Click **Save**.</span></span>

![図 1](media/15-work-orders.png)


<span data-ttu-id="afd57-118">使用するメンテナンス ダウンタイムの理由コードを作成した場合は、作業指示書および資産に対してメンテナンス ダウンタイムの登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="afd57-118">When you have created the maintenance downtime reason codes you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="afd57-119">メンテナンス ダウンタイムの登録の作成</span><span class="sxs-lookup"><span data-stu-id="afd57-119">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="afd57-120">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-120">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="afd57-121">作業指示書を選択し、**メンテナンス ダウンタイム**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-121">Select the work order and click **Maintenance downtime**.</span></span>

3. <span data-ttu-id="afd57-122">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-122">Click **New**.</span></span>

4. <span data-ttu-id="afd57-123">**開始**および**終了**フィールドに、メンテナンス ダウンタイムの登録に使用する日付と時間の間隔を挿入します。</span><span class="sxs-lookup"><span data-stu-id="afd57-123">Insert date and time interval for the maintenance downtime registration in the **From** and **To** fields.</span></span>

5. <span data-ttu-id="afd57-124">**終了**フィールドを終了すると、期間 (時) が**期間**フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="afd57-124">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

6. <span data-ttu-id="afd57-125">**メンテナンス ダウンタイムの理由コード** フィールドで理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd57-125">Select a reason code in the **maintenance downtime reason code** field.</span></span>

7. <span data-ttu-id="afd57-126">登録をさらに追加する場合は、ステップ 3 から 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="afd57-126">Repeat steps 3-6 if you want to add more registrations.</span></span>

8. <span data-ttu-id="afd57-127">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="afd57-127">Click **Save**.</span></span>


![図 2](media/16-work-orders.png)


<span data-ttu-id="afd57-129">メンテナンス ダウンタイムの登録の計算に使用されるカレンダーは、資産とパラメーターの設定での選択によって異なります。</span><span class="sxs-lookup"><span data-stu-id="afd57-129">The calendar used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="afd57-130">次の図に示すように、**すべての資産** > **固定資産**クイック タブ > **リソース** フィールドの資産に対してリソースが選択されている場合は、関連付けられているリソース グループに対して設定されているカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="afd57-130">If a resource is selected on an asset in **All assets** > **Fixed asset** FastTab > **Resource** field, the calendar set up for the associated resource group is used, as shown in the following figure.</span></span>

![図 3](media/17-work-orders.png)


<span data-ttu-id="afd57-132">資産に対してリソースが選択されていない場合、次の図に示すように、**資産管理パラメーター**で選択された標準カレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="afd57-132">If no resource is selected on the asset, the standard calendar selected in **Asset management parameters** is used, as shown in the following figure.</span></span>

![図 4](media/18-work-orders.png)


<span data-ttu-id="afd57-134">**エンタープライズ資産管理** > **照会** > **メンテナンス ダウンタイム**をクリックして、すべてのメンテナンス ダウンタイムの登録の概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="afd57-134">Click **Enterprise asset management** > **Inquiries** > **Maintenance downtime** to see an overview of all maintenance downtime registrations.</span></span>

>[!NOTE]
><span data-ttu-id="afd57-135">**資産管理**モジュールで使用されるすべてのカレンダーは、**組織管理** > **設定** > **カレンダー** > **カレンダー**で設定されます。</span><span class="sxs-lookup"><span data-stu-id="afd57-135">All calendars used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

