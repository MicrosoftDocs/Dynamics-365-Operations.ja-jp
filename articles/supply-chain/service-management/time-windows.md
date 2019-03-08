---
title: 時間枠
description: サービス注文明細行のスケジューリングを最適化するために時間枠を使用できます。
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f748268f6cb85ff835919485da2828689eee23c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "347218"
---
# <a name="time-windows"></a><span data-ttu-id="14e1b-103">時間枠</span><span class="sxs-lookup"><span data-stu-id="14e1b-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14e1b-104">サービス注文明細行のスケジューリングを最適化するために時間枠を使用できます。</span><span class="sxs-lookup"><span data-stu-id="14e1b-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="14e1b-105">サービス注文を自動的に作成するようにシステムを設定できます。</span><span class="sxs-lookup"><span data-stu-id="14e1b-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="14e1b-106">時間枠で指定された条件に基づき、できる限り少ないのサービス注文として、できるだけ多くのサービス注文明細行を接続できます。</span><span class="sxs-lookup"><span data-stu-id="14e1b-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="14e1b-107">時間枠では、計算日からサービス注文明細行が移動できる範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="14e1b-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="14e1b-108">計算日は、サービス注文明細行が実施される予定の日付です。</span><span class="sxs-lookup"><span data-stu-id="14e1b-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="14e1b-109">**サービス注文の作成** ページで定義したサービス期間と間隔の設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="14e1b-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="14e1b-110">時間枠を定義するには、次の表の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="14e1b-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="14e1b-111">方法</span><span class="sxs-lookup"><span data-stu-id="14e1b-111">Method</span></span> | <span data-ttu-id="14e1b-112">説明</span><span class="sxs-lookup"><span data-stu-id="14e1b-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14e1b-113">週</span><span class="sxs-lookup"><span data-stu-id="14e1b-113">Week</span></span>   | <span data-ttu-id="14e1b-114">サービス注文明細行が初期計算日と同じ週の任意のオープン日に移動できる日付。</span><span class="sxs-lookup"><span data-stu-id="14e1b-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="14e1b-115">月</span><span class="sxs-lookup"><span data-stu-id="14e1b-115">Month</span></span>  | <span data-ttu-id="14e1b-116">サービス注文明細行を初期計算日と同じ月の任意のオープン日に移動できる日付。</span><span class="sxs-lookup"><span data-stu-id="14e1b-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="14e1b-117">たとえば、サービス注文明細行の計算日は、2017 年 2 月 15 日です。</span><span class="sxs-lookup"><span data-stu-id="14e1b-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="14e1b-118">サービス注文明細行は、2017 年 2 月 1 日から 2 月 28 日の間で任意の平日をスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="14e1b-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="14e1b-119">マニュアル</span><span class="sxs-lookup"><span data-stu-id="14e1b-119">Manual</span></span> | <span data-ttu-id="14e1b-120">初期計算日の前後にサービス注文明細行を移動できる最大日数を定義します。</span><span class="sxs-lookup"><span data-stu-id="14e1b-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="14e1b-121">サービス契約項目の時間枠を指定しない場合、そのサービス契約から派生したサービス注文明細行は、元々スケジュール設定された日付に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14e1b-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14e1b-122">関連トピック</span><span class="sxs-lookup"><span data-stu-id="14e1b-122">Related topics</span></span>

[<span data-ttu-id="14e1b-123">時間枠の作成</span><span class="sxs-lookup"><span data-stu-id="14e1b-123">Create time windows</span></span>](create-time-windows.md)

