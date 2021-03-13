---
title: 作業指示書のメンテナンス ダウンタイム
description: このトピックでは、作業指示書で選択した資産において、メンテナンス ダウンタイム登録を作成する方法について説明します。
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
ms.openlocfilehash: 53487a0173453ef7a8f5ea818672d999fe71cb65
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020914"
---
# <a name="maintenance-downtime-for-work-orders"></a><span data-ttu-id="c3b62-103">作業指示書のメンテナンス ダウンタイム</span><span class="sxs-lookup"><span data-stu-id="c3b62-103">Maintenance downtime for work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="c3b62-104">作業指示書で選択した資産に対して、メンテナンス ダウンタイム登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-104">You can create maintenance downtime registrations on the asset that is selected on a work order.</span></span> <span data-ttu-id="c3b62-105">この能力は、生産領域の 1 つ以上のマシンにメンテナンス ダウンタイムを登録する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="c3b62-105">This capability is useful if you want to register maintenance downtime on one or more machines in the production area.</span></span> <span data-ttu-id="c3b62-106">まず、使用するメンテナンス ダウンタイムの理由コードを作成します (例えば **故障** や **計画停止** など)。</span><span class="sxs-lookup"><span data-stu-id="c3b62-106">You first create the maintenance downtime reason codes that you want to use, such as **Breakdown** and **Planned stop**.</span></span> <span data-ttu-id="c3b62-107">このステップは、**メンテナンス ダウンタイムの理由コード** ページで実行されます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-107">This step is done on the **Maintenance downtime reason codes** page.</span></span> <span data-ttu-id="c3b62-108">次に、**メンテナンス ダウンタイム** ページでメンテナンス ダウンタイムの登録を作成し、関連するメンテナンス ダウンタイムの理由コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-108">You can then create maintenance downtime registrations on the **Maintenance downtime** page and add the relevant maintenance downtime reason codes.</span></span>

## <a name="create-maintenance-downtime-reason-codes"></a><span data-ttu-id="c3b62-109">メンテナンス ダウンタイムの理由コードの作成</span><span class="sxs-lookup"><span data-stu-id="c3b62-109">Create maintenance downtime reason codes</span></span>

1. <span data-ttu-id="c3b62-110">**資産管理** > **設定** > **作業指示書** > **メンテナンス ダウンタイムの理由コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-110">Select **Asset management** > **Setup** > **Work orders** > **Maintenance downtime reason codes**.</span></span>

2. <span data-ttu-id="c3b62-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-111">Select **New**.</span></span>

3. <span data-ttu-id="c3b62-112">**メンテナンス ダウンタイムの理由コード** フィールドに、メンテナンス ダウンタイムの理由コードの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-112">In the **Maintenance downtime reason code** field, enter an ID for the maintenance downtime reason code.</span></span>

4. <span data-ttu-id="c3b62-113">**名前** フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-113">In the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="c3b62-114">理由コードを資産の主要業績評価指標 (KPI) の計算に含める必要がある場合は、**KPI include** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="c3b62-114">Select the **KPI include** check box if the reason code should be included in calculations of key performance indicators (KPIs) for the asset.</span></span> <span data-ttu-id="c3b62-115">一般に、想定されるパフォーマンスには影響しないため、計画済生産停止は KPI 計算には含めません。</span><span class="sxs-lookup"><span data-stu-id="c3b62-115">In general, planned production stops should not be included in KPI calculations, because they don't affect expected performance.</span></span>

6. <span data-ttu-id="c3b62-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-116">Select **Save**.</span></span>

<span data-ttu-id="c3b62-117">次の図では、**メンテナンス ダウンタイムの理由コード** ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-117">The illustration below shows an example of the **Maintenance downtime reason codes** page.</span></span>

![図 1](media/15-work-orders.png)

<span data-ttu-id="c3b62-119">使用するメンテナンス ダウンタイムの理由コードを作成したら、作業指示書および資産に対してメンテナンス ダウンタイムの登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-119">After you've created the maintenance downtime reason codes that you want to use, you can create maintenance downtime registrations for work orders and assets.</span></span>


## <a name="create-maintenance-downtime-registrations"></a><span data-ttu-id="c3b62-120">メンテナンス ダウンタイムの登録の作成</span><span class="sxs-lookup"><span data-stu-id="c3b62-120">Create maintenance downtime registrations</span></span>

1. <span data-ttu-id="c3b62-121">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3b62-121">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="c3b62-122">作業指示書を選択してから、**作業指示書** タブ (**資産** グループ内) で、**メンテナンス ダウンタイム** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-122">Select the work order, and then, on the **Work order** tab, in the **Asset** group, select **Maintenance downtime**.</span></span>

3. <span data-ttu-id="c3b62-123">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-123">Select **New**.</span></span>

4. <span data-ttu-id="c3b62-124">**開始** および **終了** フィールドで、メンテナンス ダウンタイムの登録に使用する日付と時間の間隔を定義します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-124">In the **From** and **To** fields, define the date and time interval for the maintenance downtime registration.</span></span>

>[!NOTE]
><span data-ttu-id="c3b62-125">**終了** フィールドを終了すると、期間 (時) が **期間** フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-125">When you leave the **To** field, the duration in hours is automatically inserted in the **Duration** field.</span></span>

5. <span data-ttu-id="c3b62-126">**メンテナンス ダウンタイムの理由コード** フィールドで理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-126">In the **maintenance downtime reason code** field, select a reason code.</span></span>

6. <span data-ttu-id="c3b62-127">ステップ 3 から 5 を繰り返して登録を追加します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-127">Repeat steps 3 through 5 to add more registrations.</span></span>

7. <span data-ttu-id="c3b62-128">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-128">Select **Save**.</span></span>

<span data-ttu-id="c3b62-129">下の図は、メンテナンス ダウンタイム登録の例を示します。</span><span class="sxs-lookup"><span data-stu-id="c3b62-129">The illustration below shows an example of maintenance downtime registration.</span></span>

![図 2](media/16-work-orders.png)

<span data-ttu-id="c3b62-131">メンテナンス ダウンタイムの登録の計算に使用されるカレンダーは、資産とパラメーターの設定での選択によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c3b62-131">The calendar that is used to calculate a maintenance downtime registration depends on your selection in the setup of assets and parameters.</span></span> <span data-ttu-id="c3b62-132">次の図に示すように、**リソース** フィールド (**固定資産** クイック タブ、**すべての資産** ページ) の資産に対してリソースが選択されている場合は、関連付けられているリソース グループに対して設定されているカレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-132">If a resource is selected on an asset in the **Resource** field on the **Fixed asset** FastTab of the **All assets** page, the calendar that is set up for the associated resource group is used, as shown in the following illustration.</span></span>

![図 3](media/17-work-orders.png)

<span data-ttu-id="c3b62-134">資産に対してリソースが選択されていない場合、次の図に示すように、**資産管理パラメーター** ページで選択された標準カレンダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-134">If no resource is selected on the asset, the standard calendar that is selected on the **Asset management parameters** page is used, as shown in the following illustration.</span></span>

![図 4](media/18-work-orders.png)

<span data-ttu-id="c3b62-136">すべてのメンテナンス ダウンタイムの登録の概要を表示するには、**資産管理** > **照会** > **メンテナンス ダウンタイム** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3b62-136">To see an overview of all maintenance downtime registrations, click **Asset management** > **Inquiries** > **Maintenance downtime**.</span></span>

>[!NOTE]
><span data-ttu-id="c3b62-137">**資産管理** モジュールで使用されるすべてのカレンダーは、**組織管理** > **設定** > **カレンダー** > **カレンダー** で設定されます。</span><span class="sxs-lookup"><span data-stu-id="c3b62-137">All calendars that are used in the **Asset Management** module are set up in **Organization administration** > **Setup** > **Calendars** > **Calendars**.</span></span>

