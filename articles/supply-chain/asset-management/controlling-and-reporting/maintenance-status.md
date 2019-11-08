---
title: メンテナンスの状態
description: このトピックでは、資産管理でメンテナンス ステータスを計算する方法について説明します。
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
ms.openlocfilehash: 8f336086838632dd3f464de2870e9a9197746daa
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652129"
---
# <a name="maintenance-status"></a><span data-ttu-id="c8143-103">メンテナンスの状態</span><span class="sxs-lookup"><span data-stu-id="c8143-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c8143-104">資産管理で、新しい、有効な、および完了したメンテナンス要求、作業指示書、およびメンテナンス ダウンタイム アクティビティに関する特定の期間の概要計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="c8143-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="c8143-105">また、同じ期間に完了した条件評価の数を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="c8143-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="c8143-106">この計算を使用して、受信および完了したメンテナンス要求および作業指示書に関するワークロードの概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="c8143-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="c8143-107">メンテナンス ステータスの計算の実行</span><span class="sxs-lookup"><span data-stu-id="c8143-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="c8143-108">**資産管理** > **照会** > **メンテナンス ステータス**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8143-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="c8143-109">**ステータスの計算**ダイアログ内の**開始日**および**終了日**フィールドで、計算を実行する時間範囲を選択します。</span><span class="sxs-lookup"><span data-stu-id="c8143-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="c8143-110">**レベル** フィールドを使用すると、機能の場所に関するメンテナンス明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c8143-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="c8143-111">たとえば、フィールドに「1」の番号を挿入し、複数レベルの機能的な場所構造がある場合、機能的な場所に対するすべてのメンテナンス明細行が最上位レベルに表示されます。したがって明細行のステータスは、下位レベルにある機能的な場所から追加される場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8143-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="c8143-112">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルですべてメンテナンス明細行を示す、詳細な結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8143-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="c8143-113">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="c8143-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="c8143-114">**グループ化**ボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8143-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="c8143-115">選択した**グループ化**ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="c8143-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="c8143-116">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="c8143-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="c8143-117">**グループ化**ボタンを有効化または無効化するか、または新しい期間に対して計算を実行することにより、変更を行うたびに**更新**ボタンをクリックし、計算を更新してください。</span><span class="sxs-lookup"><span data-stu-id="c8143-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="c8143-118">新しいメンテナンス ステータスの計算を作成する場合、**ステータス**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c8143-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="c8143-119">**メンテナンス ステータス**に表示される結果には、実際の開始日時があるメンテナンス要求および作業指示書のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c8143-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="c8143-120">終了日時は空白にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c8143-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="c8143-121">例 1</span><span class="sxs-lookup"><span data-stu-id="c8143-121">Example 1</span></span>

<span data-ttu-id="c8143-122">次のスクリーンショットでは、**年**および**月**ボタンが有効化されています。</span><span class="sxs-lookup"><span data-stu-id="c8143-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="c8143-123">これらの**グループ化**オプションを選択すると、メンテナンス要求と作業指示書に関連する月ごとのワークロードとスループットの一般的な概要を取得します。</span><span class="sxs-lookup"><span data-stu-id="c8143-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![月ごとのワークロードの例](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="c8143-125">例 2</span><span class="sxs-lookup"><span data-stu-id="c8143-125">Example 2</span></span>

<span data-ttu-id="c8143-126">次のスクリーンショットでは、機能の場所に関する情報が追加されています。</span><span class="sxs-lookup"><span data-stu-id="c8143-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="c8143-127">地理的な場所、工場、または作業領域を表す機能の場所間でワークロードおよびスループットを比較することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c8143-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![機能の場所を含む月ごとのワークロードの例](media/14-controlling-and-reporting.png)

