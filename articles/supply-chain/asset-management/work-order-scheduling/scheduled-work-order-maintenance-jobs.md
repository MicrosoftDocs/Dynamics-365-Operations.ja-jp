---
title: スケジュールされた作業指示書メンテナンス作業
description: このトピックでは、資産管理におけるスケジュール済みワーク オーダー メンテナンス作業について説明します。
author: josaw1
manager: tfehr
ms.date: 08/19/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c8cea81d27f1671b54c4947b05bbc387667247c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263809"
---
# <a name="scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="23e2d-103">スケジュールされた作業指示書メンテナンス作業</span><span class="sxs-lookup"><span data-stu-id="23e2d-103">Scheduled work order maintenance jobs</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="23e2d-104">**スケジュール済みワーク オーダーのメンテナンス作業** ページには、リソースに割り当てられたワーク オーダーの概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-104">The **Scheduled work order maintenance jobs** page shows an overview of the work orders allocated to a resource.</span></span> <span data-ttu-id="23e2d-105">リソースタイプ「人事管理」、「ツール」、および 「機械」を使用するワーク オーダーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-105">Work orders using resource types "Human resources", "Tool", and "Machine" are shown.</span></span> <span data-ttu-id="23e2d-106">たとえば、メンテナンス作業者が病気になった場合、このページを使用して作業者に割り当てられたワーク オーダーをすばやく見つけ、別のメンテナンス作業者をジョブに割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-106">For example, if a maintenance worker calls in sick, you can use this page to quickly find work orders allocated to the worker, and then allocate another maintenance worker to the job.</span></span>

## <a name="view-scheduled-work-order-maintenance-jobs"></a><span data-ttu-id="23e2d-107">スケジュール済みワーク オーダーのメンテナンス作業の表示</span><span class="sxs-lookup"><span data-stu-id="23e2d-107">View scheduled work order maintenance jobs</span></span>

1. <span data-ttu-id="23e2d-108">**資産管理** > **共通** > **ワーク オーダー** > **スケジュール済のワーク オーダー メンテナンス作業** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23e2d-108">Click **Asset management** > **Common** > **Work orders** > **Scheduled work order maintenance jobs**.</span></span> <span data-ttu-id="23e2d-109">ワーク オーダーのライフサイクル状態が「スケジュール済」または「処理中」に設定されているすべてのワーク オーダーの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-109">You see a list of all work orders set to work order lifecycle state "Scheduled" or "In progress".</span></span>

2. <span data-ttu-id="23e2d-110">一覧は、メンテナンス作業者などで並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-110">You can sort the list, for example, by maintenance worker.</span></span> <span data-ttu-id="23e2d-111">また、フィルターを使用して一覧を制限し、特定のリソースまたはメンテナンス作業者に割り当てられたワーク オーダーを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-111">You can also use the filter to limit the list to display work orders allocated to a specific resource or maintenance worker.</span></span>

3. <span data-ttu-id="23e2d-112">ワーク オーダーのメモを表示し、必要に応じてワーク オーダーのジョブを選択することにより新しいメモを追加し、**メモ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23e2d-112">You can see notes on the work order and, if required, add new notes by selecting the work order job, and then click **Notes**.</span></span>

4. <span data-ttu-id="23e2d-113">1 人のメンテナンス作業者をワーク オーダーに割り当てる場合は、ワーク オーダーを選択し、**ワーク オーダー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23e2d-113">If you want to allocate one maintenance worker to a work order, select the work order, and then click **Work order**.</span></span>

5. <span data-ttu-id="23e2d-114">**ワーク オーダー** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23e2d-114">The **Work order** page opens.</span></span> <span data-ttu-id="23e2d-115">**派遣** をクリックし、特定のメンテナンス作業者にワーク オーダーをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="23e2d-115">Click **Dispatch** to schedule the work order to a specific maintenance worker.</span></span>

>[!NOTE]
><span data-ttu-id="23e2d-116">複数のワーク オーダーまたは 1 つのワーク オーダーのスケジューリングについては、[ワーク オーダーのスケジュール](../work-order-scheduling/schedule-work-orders.md)および[派遣のワーク オーダー](../work-order-scheduling/dispatch-work-order.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23e2d-116">Read more about scheduling several work orders or one work order in [Schedule work orders](../work-order-scheduling/schedule-work-orders.md) and [Dispatch work order](../work-order-scheduling/dispatch-work-order.md).</span></span>

<span data-ttu-id="23e2d-117">次のスクリーンショットは、**スケジュール済みワーク オーダーのメンテナンス作業** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="23e2d-117">The following screenshot shows an example of the **Scheduled work order maintenance jobs** page.</span></span>

![図 1](media/07-work-order-scheduling.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]