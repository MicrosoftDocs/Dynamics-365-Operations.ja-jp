---
title: サービス注文の開始時刻と期間の表示
description: サービス注文の作業が開始された時刻や、サービス注文の完了予定時刻を表示できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2891e0cb5b65f22c3cb444db4352f8e7767c900b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206384"
---
# <a name="view-the-start-time-and-duration-of-a-service-order"></a><span data-ttu-id="32c4b-103">サービス注文の開始時刻と期間の表示</span><span class="sxs-lookup"><span data-stu-id="32c4b-103">View the start time and duration of a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="32c4b-104">サービス注文の作業が開始された時刻や、サービス注文の完了予定時刻を表示できます。</span><span class="sxs-lookup"><span data-stu-id="32c4b-104">You can view when the work on the service order was started and when the service order is going to be completed.</span></span>

<span data-ttu-id="32c4b-105">また、サービス注文の時刻記録がいつ開始および停止されたかも表示できます。</span><span class="sxs-lookup"><span data-stu-id="32c4b-105">You can also view when the time recording for a service order was started and stopped.</span></span> <span data-ttu-id="32c4b-106">サービス注文が停止されると、サービス注文の完了期限の時刻は繰り下げられます。</span><span class="sxs-lookup"><span data-stu-id="32c4b-106">When a service order is stopped, the time at which the service order must be completed is postponed.</span></span>

## <a name="view-the-start-time-for-a-service-order"></a><span data-ttu-id="32c4b-107">サービス注文の開始時刻の表示</span><span class="sxs-lookup"><span data-stu-id="32c4b-107">View the start time for a service order</span></span>

1.  <span data-ttu-id="32c4b-108">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-108">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="32c4b-109">詳細フォームを開く対象の注文を選択し、ダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-109">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="32c4b-110">**一般**タブの**開始時刻**フィールドで、サービス注文の作業が開始された時刻を表示します。</span><span class="sxs-lookup"><span data-stu-id="32c4b-110">On the **General** tab, view the time that the work was started for a service order in the **Start time** field.</span></span>

## <a name="view-the-time-remaining-to-complete-a-service-order"></a><span data-ttu-id="32c4b-111">サービス注文の完了期限までの残り時間の表示</span><span class="sxs-lookup"><span data-stu-id="32c4b-111">View the time remaining to complete a service order</span></span>

1.  <span data-ttu-id="32c4b-112">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="32c4b-113">詳細フォームを開く対象の注文を選択し、ダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-113">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="32c4b-114">**一般**タブの**最新の完了時刻**フィールドで、サービス注文の完了期限までの残り時間を表示します。</span><span class="sxs-lookup"><span data-stu-id="32c4b-114">On the **General** tab, view the time remaining to complete a service order in the **Latest completion time** field.</span></span>

## <a name="view-the-start-time-and-stop-time-recording-entries-for-a-service-order"></a><span data-ttu-id="32c4b-115">サービス注文の開始時刻および停止時刻記録エントリの表示</span><span class="sxs-lookup"><span data-stu-id="32c4b-115">View the start time and stop time recording entries for a service order</span></span>

1.  <span data-ttu-id="32c4b-116">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-116">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="32c4b-117">詳細フォームを開く対象の注文を選択し、ダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="32c4b-117">Select and double-click an order to open the details form.</span></span>

2.  <span data-ttu-id="32c4b-118">**アクション ウィンドウ**で、**出荷** タブ \> **時刻記録**の順にクリックし、**SLA 時刻記録**フォームを開き、サービス注文の時刻記録エントリを表示します。</span><span class="sxs-lookup"><span data-stu-id="32c4b-118">On the **Action Pane**, click the **Dispatch** tab \> **Time recording** to open the **SLA time recording** form and view the time recording entries for the service order.</span></span>

## <a name="see-also"></a><span data-ttu-id="32c4b-119">参照</span><span class="sxs-lookup"><span data-stu-id="32c4b-119">See also</span></span>

<span data-ttu-id="32c4b-120">[サービス注文 (フォーム)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="32c4b-120">[Service orders (form)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))</span></span>

  


