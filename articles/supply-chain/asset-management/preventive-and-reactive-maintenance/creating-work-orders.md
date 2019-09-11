---
title: 作業指示書の作成
description: このトピックでは、資産管理で作業指示書を作成する方法について説明します。
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
ms.openlocfilehash: b23ed3251b2f6cf4f34b423ce2f85301d6ab31a1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875751"
---
# <a name="creating-work-orders"></a><span data-ttu-id="70bae-103">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="70bae-103">Creating work orders</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="70bae-104">予防的メンテナンス ジョブがスケジュールされている場合は、次の手順でジョブの作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="70bae-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="70bae-105">これは、メンテナンス スケジュールのいずれかで行われます。</span><span class="sxs-lookup"><span data-stu-id="70bae-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="70bae-106">メンテナンス スケジュールのスケジュールされたジョブには、異なる参照タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="70bae-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="70bae-107">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="70bae-107">Reference type</span></span> | <span data-ttu-id="70bae-108">説明</span><span class="sxs-lookup"><span data-stu-id="70bae-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70bae-109">メンテナンス計画</span><span class="sxs-lookup"><span data-stu-id="70bae-109">Maintenance plans</span></span>     | <span data-ttu-id="70bae-110">予防的メンテナンス ジョブは、メンテナンス計画タイプの "時間" または "カウンター" に基づきます。</span><span class="sxs-lookup"><span data-stu-id="70bae-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="70bae-111">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="70bae-111">Maintenance rounds</span></span>    | <span data-ttu-id="70bae-112">予防的メンテナンス ジョブには、同様のタイプのメンテナンスを必要とする複数の資産が含まれます。</span><span class="sxs-lookup"><span data-stu-id="70bae-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="70bae-113">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="70bae-113">Maintenance request</span></span>   | <span data-ttu-id="70bae-114">手動で作成された資産のメンテナンスまたは修理に対する要求が、ワークオーダーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="70bae-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="70bae-115">**資産管理** > **共通** > **すべてのメンテナンス スケジュール**または**未処理のメンテナンス スケジュール行**または**未処理のメンテナンス スケジュール プール**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="70bae-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="70bae-116">作業指示書を作成するスケジュール済みメンテナンス ジョブを選択し、**作業指示書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70bae-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="70bae-117">**メンテナンス予測時間**フィールドには、選択した明細行に対する予測時間数の合計が表示されます。</span><span class="sxs-lookup"><span data-stu-id="70bae-117">The total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="70bae-118">**パラメーター** セクションで、作成する必要がある作業指示の数を選択します。</span><span class="sxs-lookup"><span data-stu-id="70bae-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="70bae-119">1つのメンテナンス スケジュール行ごとに 1 つの作業指示書、または **1 つの作業指示書ごと**の選択項目に基づいて複数の作業指示書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="70bae-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="70bae-120">作成するすべての作業指示書で使用される**作業指示書タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="70bae-120">Select a **Work order type** that will be used on all the work orders you create.</span></span>

5. <span data-ttu-id="70bae-121">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="70bae-121">Click **OK**.</span></span> <span data-ttu-id="70bae-122">1 つ以上の作業指示書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="70bae-122">One or more work orders are created.</span></span>

![図 1](media/18-preventive-maintenance.png)

