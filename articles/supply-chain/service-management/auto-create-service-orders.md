---
title: サービス注文を自動で作成します
description: サービス契約が有効期間にあるサービス契約に基づいてサービス注文を生成できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fb7363ab87fd6a7f3d38406e72b1f542dc2c2a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432142"
---
# <a name="automatically-create-service-orders"></a><span data-ttu-id="85e15-103">サービス注文を自動で作成します</span><span class="sxs-lookup"><span data-stu-id="85e15-103">Automatically create service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="85e15-104">サービス契約が有効期間にあるサービス契約に基づいてサービス注文を生成できます。</span><span class="sxs-lookup"><span data-stu-id="85e15-104">You can generate service orders that are based on a service agreement for the valid period of the service agreement.</span></span>

<span data-ttu-id="85e15-105">サービス契約から生成したサービス注文は、すべてそのサービス契約に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="85e15-105">The service orders that you generate from a service agreement are all attached to the service agreement.</span></span>

<span data-ttu-id="85e15-106">サービス注文は、以下の設定から自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="85e15-106">Service orders are generated automatically from the following settings:</span></span>

  - <span data-ttu-id="85e15-107">サービス契約明細行で設定されたサービス契約期間。</span><span class="sxs-lookup"><span data-stu-id="85e15-107">The service agreement interval that is set up in the service agreement lines.</span></span> <span data-ttu-id="85e15-108">サービス契約期間は、サービス注文明細行が作成される頻度を示します。</span><span class="sxs-lookup"><span data-stu-id="85e15-108">The service agreement interval indicates the frequency that service-order lines are created.</span></span> <span data-ttu-id="85e15-109">詳細については、[サービス期間](service-intervals.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85e15-109">For more information, see [Service intervals](service-intervals.md).</span></span>

  - <span data-ttu-id="85e15-110">サービス期間の定義として **サービス注文の作成** フォームの **開始日** および **終了日** フィールドで指定した期間。</span><span class="sxs-lookup"><span data-stu-id="85e15-110">The period that you specify to define the service period in the **From date** and **To date** fields in the **Create service orders** form.</span></span> <span data-ttu-id="85e15-111">詳細については、[サービス注文の自動作成](create-service-orders-automatically.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85e15-111">For more information, see [Create service orders automatically](create-service-orders-automatically.md).</span></span>

  - <span data-ttu-id="85e15-112">サービス合意ヘッダーの **サービス注文の組み合わせ** オプション。</span><span class="sxs-lookup"><span data-stu-id="85e15-112">The **Combine service orders** option on the service agreement header.</span></span> <span data-ttu-id="85e15-113">このオプションは、サービス契約から生成されたサービス注文明細行が、従業員、サービス タスク、サービス対象、またはサービス契約に応じて、サービス注文を連結するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="85e15-113">This option defines whether service order lines generated from a service agreement, combines service orders according to employee, service task, service object, or service agreement.</span></span> <span data-ttu-id="85e15-114">詳細については、[サービス注文の組み合わせ](combine-service-orders.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85e15-114">For more information, see [Combine service orders](combine-service-orders.md).</span></span>

  - <span data-ttu-id="85e15-115">サービス合意項目の **時間枠** オプション。</span><span class="sxs-lookup"><span data-stu-id="85e15-115">The **Time window** option on the service agreement line.</span></span> <span data-ttu-id="85e15-116">時間枠では、計算日に関連してサービス注文明細行が移動できる範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="85e15-116">The time window defines how far a service order line can move with regard to its calculated date.</span></span> <span data-ttu-id="85e15-117">詳細については、[時間枠](time-windows.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85e15-117">For more information, see [Time windows](time-windows.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="85e15-118">サービス注文に指定された日が<STRONG>サービス管理パラメーター</STRONG>フォームで選択したカレンダーでオープンでない場合、カレンダーに不一致があることをメッセージが示します。</span><span class="sxs-lookup"><span data-stu-id="85e15-118">If the day that is specified for a service order is not open in the calendar that you have selected in the <STRONG>Service management parameters</STRONG> form, a message will indicate that there is a calendar conflict.</span></span> <span data-ttu-id="85e15-119">このメッセージは無視できます。カレンダー上でその日が終了していてもサービス注文は作成されます。</span><span class="sxs-lookup"><span data-stu-id="85e15-119">You can safely ignore the message; the service order will be created, even though the day is closed on the calendar.</span></span></P>

## <a name="example-1"></a><span data-ttu-id="85e15-120">例 1</span><span class="sxs-lookup"><span data-stu-id="85e15-120">Example 1</span></span>

<span data-ttu-id="85e15-121">サービス合意の期間は 2012 年 1 月 1 日～ 2012 年 12 月 31 日です。</span><span class="sxs-lookup"><span data-stu-id="85e15-121">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="85e15-122">**サービス注文の作成** フォームで指定するサービス期間が 2012 年 11 月 1日～ 2013 年 2 月 1 日の場合、サービス注文が 2012 年 11 月 1 日～ 2012年 12 月 31 日で作成されます。</span><span class="sxs-lookup"><span data-stu-id="85e15-122">If the service period that you specify in the **Create service orders** form is from November 1, 2012 until February 1, 2013, service orders are created from November 1, 2012 until December 31, 2012.</span></span>

## <a name="example-2"></a><span data-ttu-id="85e15-123">例 2</span><span class="sxs-lookup"><span data-stu-id="85e15-123">Example 2</span></span>

<span data-ttu-id="85e15-124">サービス合意の期間は 2012 年 1 月 1 日～ 2012 年 12 月 31 日です。</span><span class="sxs-lookup"><span data-stu-id="85e15-124">The service agreement lasts from January 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="85e15-125">このサービス合意に 2 つのサービス合意項目が関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="85e15-125">Two service agreement lines are attached to the service agreement.</span></span> <span data-ttu-id="85e15-126">最初のサービス合意項目は、開始日が 2012 年 1 月 2 日で、終了日が 2012 年 3 月 1 日です。</span><span class="sxs-lookup"><span data-stu-id="85e15-126">The first service agreement line has a starting date on January 2, 2012 and an ending date on March 1, 2012.</span></span> <span data-ttu-id="85e15-127">2 つ目のサービス合意項目は、開始日が 2012 年 4 月 1 日で、終了日が 2012 年 12 月 31 日です。</span><span class="sxs-lookup"><span data-stu-id="85e15-127">The second service agreement line has a starting date on April 1, 2012 and an ending date on December 31, 2012.</span></span> <span data-ttu-id="85e15-128">**サービス注文の作成** フオームで指定する期間は、2012 年 10 月 1 日～ 2012年 12 月 31 日です。</span><span class="sxs-lookup"><span data-stu-id="85e15-128">You specify a period in the **Create service orders** form that is from October 1, 2012 until December 31, 2012.</span></span> <span data-ttu-id="85e15-129">この場合、最初の合意項目の開始日と終了日が、サービス注文に指定した期間よりも前の日付であるため、サービス注文は 2 番目の合意項目に対してのみ生成されます。</span><span class="sxs-lookup"><span data-stu-id="85e15-129">Therefore, service orders are generated only for the second agreement line, because the starting date and ending date of the first agreement line are before the period that you specified for the service order.</span></span>

  


