---
title: 作業指示書の作成
description: このトピックでは、資産管理で作業指示書を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: 6e910b2400106baf9f9dc06f6bc0d3daee8e4a43
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570079"
---
# <a name="creating-work-orders"></a><span data-ttu-id="42c6c-103">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="42c6c-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="42c6c-104">予防的メンテナンス ジョブがスケジュールされている場合は、次の手順でジョブの作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="42c6c-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="42c6c-105">これは、メンテナンス スケジュールのいずれかで行われます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="42c6c-106">メンテナンス スケジュールのスケジュールされたジョブには、異なる参照タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="42c6c-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="42c6c-107">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="42c6c-107">Reference type</span></span> | <span data-ttu-id="42c6c-108">説明</span><span class="sxs-lookup"><span data-stu-id="42c6c-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42c6c-109">メンテナンス計画</span><span class="sxs-lookup"><span data-stu-id="42c6c-109">Maintenance plans</span></span>     | <span data-ttu-id="42c6c-110">予防的メンテナンス ジョブは、メンテナンス計画タイプの "時間" または "カウンター" に基づきます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="42c6c-111">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="42c6c-111">Maintenance rounds</span></span>    | <span data-ttu-id="42c6c-112">予防的メンテナンス ジョブには、同様のタイプのメンテナンスを必要とする複数の資産が含まれます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="42c6c-113">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="42c6c-113">Maintenance request</span></span>   | <span data-ttu-id="42c6c-114">手動で作成された資産のメンテナンスまたは修理に対する要求が、ワークオーダーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="42c6c-115">**資産管理** > **共通** > **すべてのメンテナンス スケジュール**または**未処理のメンテナンス スケジュール行**または**未処理のメンテナンス スケジュール プール**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="42c6c-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="42c6c-116">作業指示書を作成するスケジュール済みメンテナンス ジョブを選択し、**作業指示書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42c6c-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="42c6c-117">**作業指示書の作成**ダイアログで、**メンテナンス予測時間**フィールドには、選択した明細行に対する予測時間の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="42c6c-118">**パラメーター** セクションで、作成する必要がある作業指示の数を選択します。</span><span class="sxs-lookup"><span data-stu-id="42c6c-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="42c6c-119">1つのメンテナンス スケジュール行ごとに 1 つの作業指示書、または **1 つの作業指示書ごと**の選択項目に基づいて複数の作業指示書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="42c6c-120">作成するすべての作業指示書で使用される**作業指示書タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42c6c-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="42c6c-121">次の図は、**作業指示書の作成**ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="42c6c-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![図 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="42c6c-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42c6c-123">Click **OK**.</span></span> <span data-ttu-id="42c6c-124">1 つ以上の作業指示書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="42c6c-124">One or more work orders are created.</span></span>

