---
title: 作業指示書の作成
description: このトピックでは、資産管理で作業指示書を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206130"
---
# <a name="creating-work-orders"></a><span data-ttu-id="1d077-103">作業指示書の作成</span><span class="sxs-lookup"><span data-stu-id="1d077-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1d077-104">予防的メンテナンス ジョブがスケジュールされている場合は、次の手順でジョブの作業指示書を作成します。</span><span class="sxs-lookup"><span data-stu-id="1d077-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="1d077-105">これは、メンテナンス スケジュールのいずれかで行われます。</span><span class="sxs-lookup"><span data-stu-id="1d077-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="1d077-106">メンテナンス スケジュールのスケジュールされたジョブには、異なる参照タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="1d077-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="1d077-107">参照タイプ</span><span class="sxs-lookup"><span data-stu-id="1d077-107">Reference type</span></span> | <span data-ttu-id="1d077-108">説明</span><span class="sxs-lookup"><span data-stu-id="1d077-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d077-109">メンテナンス計画</span><span class="sxs-lookup"><span data-stu-id="1d077-109">Maintenance plans</span></span>     | <span data-ttu-id="1d077-110">予防的メンテナンス ジョブは、メンテナンス計画タイプの "時間" または "カウンター" に基づきます。</span><span class="sxs-lookup"><span data-stu-id="1d077-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="1d077-111">メンテナンス ラウンド</span><span class="sxs-lookup"><span data-stu-id="1d077-111">Maintenance rounds</span></span>    | <span data-ttu-id="1d077-112">予防的メンテナンス ジョブには、同様のタイプのメンテナンスを必要とする複数の資産が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1d077-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="1d077-113">メンテナンス要求</span><span class="sxs-lookup"><span data-stu-id="1d077-113">Maintenance request</span></span>   | <span data-ttu-id="1d077-114">手動で作成された資産のメンテナンスまたは修理に対する要求が、ワークオーダーに変換されます。</span><span class="sxs-lookup"><span data-stu-id="1d077-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="1d077-115">**資産管理** > **共通** > **すべてのメンテナンス スケジュール**または**未処理のメンテナンス スケジュール行**または**未処理のメンテナンス スケジュール プール**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d077-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="1d077-116">作業指示書を作成するスケジュール済みメンテナンス ジョブを選択し、**作業指示書**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d077-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="1d077-117">**作業指示書の作成**ダイアログで、**メンテナンス予測時間**フィールドには、選択した明細行に対する予測時間の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d077-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="1d077-118">**パラメーター** セクションで、作成する必要がある作業指示の数を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d077-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="1d077-119">1つのメンテナンス スケジュール行ごとに 1 つの作業指示書、または **1 つの作業指示書ごと**の選択項目に基づいて複数の作業指示書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="1d077-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="1d077-120">作成するすべての作業指示書で使用される**作業指示書タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d077-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="1d077-121">次の図は、**作業指示書の作成**ダイアログの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1d077-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![図 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="1d077-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d077-123">Click **OK**.</span></span> <span data-ttu-id="1d077-124">1 つ以上の作業指示書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1d077-124">One or more work orders are created.</span></span>

