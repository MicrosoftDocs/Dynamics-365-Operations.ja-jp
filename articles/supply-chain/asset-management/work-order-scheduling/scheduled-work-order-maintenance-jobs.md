---
title: スケジュールされた作業指示書メンテナンス作業
description: このトピックでは、資産管理におけるスケジュール済みワーク オーダー メンテナンス作業について説明します。
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
ms.openlocfilehash: 4b3cc32d6ff263967c1ee843702c28968219ac33
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887185"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="fbbbb-103">スケジュールされた作業指示書メンテナンス作業</span><span class="sxs-lookup"><span data-stu-id="fbbbb-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fbbbb-104">**スケジュール済みワーク オーダーのメンテナンス作業**ページは、リソースに割り当てられたワーク オーダーの概要を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-104">The **Scheduled work order maintenance jobs** page is used to get an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="fbbbb-105">リソースタイプ「人事管理」、「ツール」、および 「機械」を使用するワーク オーダーが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown in the list.</span></span> <span data-ttu-id="fbbbb-106">この一覧を使用して、特定のリソースに割り当てられているワーク オーダーの概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-106">The list can be used to get an overview of work orders allocated to a specific resource.</span></span> <span data-ttu-id="fbbbb-107">これを使用して、たとえば今朝病気になったメンテナンス作業者に割り当てられたワーク オーダーをすばやく見つけ、別のメンテナンス作業者をジョブに割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-107">You can also use it to quickly find a work order allocated to a maintenance worker who, for example, called in sick this morning, and then quickly allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="fbbbb-108">スケジュール済みワーク オーダーのメンテナンス作業の表示</span><span class="sxs-lookup"><span data-stu-id="fbbbb-108">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="fbbbb-109">**資産管理** > **共通** > **ワーク オーダー** > **スケジュール済のワーク オーダー メンテナンス作業**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-109">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="fbbbb-110">ワーク オーダーのライフサイクル状態が「スケジュール済」または「処理中」に設定されているすべてのワーク オーダーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-110">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="fbbbb-111">一覧は、メンテナンス作業者などで並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-111">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="fbbbb-112">また、フィルターを使用して一覧を制限し、特定のリソースまたはメンテナンス作業者に割り当てられたワーク オーダーを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-112">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="fbbbb-113">リストでワーク オーダーのジョブを選択し、**メモ**をクリックして、ワーク オーダーのメモを表示し、必要に応じて新しいメモを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-113">You can see notes on the work order and, if required, add new notes by selecting the work order job in the list and clicking **Notes**.</span></span>

4. <span data-ttu-id="fbbbb-114">1 人のメンテナンス作業者をワーク オーダーに割り当てる場合は、リストでワーク オーダーを選択し、**ワーク オーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-114">If you want to allocate one maintenance worker to a work order, select the work order in the list, and click **Work order**.</span></span>

5. <span data-ttu-id="fbbbb-115">**ワーク オーダー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-115">The **Work order** page opens.</span></span> <span data-ttu-id="fbbbb-116">**派遣**をクリックし、特定のメンテナンス作業者にワーク オーダーをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-116">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="fbbbb-117">複数のワーク オーダーまたは 1 つのワーク オーダーのスケジューリングについては、[ワーク オーダーのスケジュール](../work-order-scheduling/schedule-work-orders.md)および[派遣のワーク オーダー](../work-order-scheduling/dispatch-work-order.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-117">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="fbbbb-118">次の図は、**スケジュール済みワーク オーダーのメンテナンス作業**ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="fbbbb-118">The figure below shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![図 1](media/07-work-order-scheduling.png)

