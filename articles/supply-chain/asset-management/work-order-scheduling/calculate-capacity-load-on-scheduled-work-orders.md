---
title: スケジュール済み作業指示書の最大能力負荷の計算
description: このトピックでは、資産管理でスケジュール済み作業指示書の最大能力負荷を計算する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887162"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="c94ba-103">スケジュール済み作業指示書の最大能力負荷の計算</span><span class="sxs-lookup"><span data-stu-id="c94ba-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c94ba-104">スケジュール済み作業指示書の最大能力負荷を計算して、特定の期間に対するリソースの作業負荷の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="c94ba-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="c94ba-105">メンテナンス作業者、作業者グループ、ツール、および資産に対して計算を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c94ba-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="c94ba-106">**資産管理** > **照会** > **スケジュール** > **最大能力負荷**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c94ba-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="c94ba-107">**最大能力負荷の計算**ダイアログ > **表示**フィールドで、計算する負荷タイプとして "能力"、"引当済"、または "残余" を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: "Capacity", "Reserved", or "Remainder".</span></span>

3. <span data-ttu-id="c94ba-108">ゼロを含む結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで "はい" を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-108">Select "Yes" on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="c94ba-109">該当するトグル ボタンの**作業者**、**メンテナンス作業者グループ**、**ツール**、および**資産**で "はい" を選択して、作業負荷を計算に使用するリソース タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-109">Select the resource types for which you want to calculate capacity load by selecting "Yes" on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="c94ba-110">**開始日**フィールドで、計算の開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="c94ba-111">**間隔のタイプ** フィールドで、計算の間隔として "日"、"週"、"月"、または "四半期" を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-111">In the **Interval type** field, select the interval for the calculation: "Day", "Week", "Month", or "Quarter".</span></span>

7. <span data-ttu-id="c94ba-112">**期間頻度**フィールドに、計算する間隔の数を挿入します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="c94ba-113">たとえば、"日" を間隔タイプとして選択し、このフィールドに数値 "5" を挿入した場合、開始日から 5 日間の計算が行われます。</span><span class="sxs-lookup"><span data-stu-id="c94ba-113">For example, if you have selected "Day" as the interval type, and you insert the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="c94ba-114">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="c94ba-115">次の図は、負荷タイプ "引当済" に対する 3 週間の計算の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="c94ba-115">The figure below shows the result of a calculation covering three weeks for the load type "Reserved".</span></span>

![図 1](media/08-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="c94ba-117">負荷タイプ "能力" または "剰余" を選択した計算では、選択した期間のリソースに対して引当が行われていない場合、同じ結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c94ba-117">If you select the load types "Capacity" or "Remainder" for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="c94ba-118">スケジュール済み作業指示書でなく、メンテナンス スケジュール明細行で最大能力負荷を計算する方法についての詳細は、[最大能力負荷の計算](../capacity-planning/calculate-capacity-load.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c94ba-118">Refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md) for information on how to calculate capacity load on maintenance schedule lines and not scheduled work orders.</span></span>

