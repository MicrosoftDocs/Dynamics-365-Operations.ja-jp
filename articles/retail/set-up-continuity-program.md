---
title: "コール センターの連続プログラムの設定"
description: "この記事では、コール センターの連続プログラムの設定方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 369856f33c6da49b6c6b3f51f42c99a8f07fe777
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="set-up-continuity-programs-for-call-centers"></a><span data-ttu-id="aad52-103">コール センターの連続プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="aad52-103">Set up continuity programs for call centers</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aad52-104">この記事では、コール センターの連続プログラムの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aad52-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="aad52-105">繰返し注文プログラムとも呼ばれる連続プログラムでは、事前定義スケジュールに応じて、顧客は通常の製品出荷を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="aad52-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="aad52-106">月例図書推薦会の場合のように、各出荷に異なる製品を含めたり、同じ製品を繰り返し送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="aad52-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="aad52-107">連続プログラムを設定するには、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad52-107">To set up a continuity program, you must complete the following tasks.</span></span>

1. <span data-ttu-id="aad52-108">**コール センター パラメーター** ページで連続パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="aad52-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2. <span data-ttu-id="aad52-109">支払スケジュール、出荷のタイミング、先行請求であるか、などの詳細を指定する連続プログラムを作成します。</span><span class="sxs-lookup"><span data-stu-id="aad52-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="aad52-110">また、連続プログラムに含まれる製品の一覧を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad52-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="aad52-111">各製品は 1 で始まる、連続して割り当てられるイベント ID 番号を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="aad52-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="aad52-112">イベント ID により、製品が送信される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="aad52-112">The event IDs determine the order that products are sent in.</span></span>

    - <span data-ttu-id="aad52-113">顧客が各出荷で別の製品を受け取る場合、製品はイベント ID に応じて、現在のイベントから順番に送信されます。</span><span class="sxs-lookup"><span data-stu-id="aad52-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    - <span data-ttu-id="aad52-114">顧客が各出荷で同じ製品を受け取る場合、一覧には 1 つのイベント ID を持つ 1 つのイベントのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="aad52-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="aad52-115">同じイベントが繰り返し発生します。</span><span class="sxs-lookup"><span data-stu-id="aad52-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="aad52-116">各イベントが繰り返される回数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="aad52-116">You can specify how many times each event is repeated.</span></span>

3. <span data-ttu-id="aad52-117">手順 2 で作成した連続プログラムを表す親製品を作成します。</span><span class="sxs-lookup"><span data-stu-id="aad52-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="aad52-118">販売注文にこの製品を追加すると、**連続性** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="aad52-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="aad52-119">その後、このページを使用して実際の連続注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="aad52-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="aad52-120">親製品は、顧客が各出荷で受け取る個々の製品を指定しません。</span><span class="sxs-lookup"><span data-stu-id="aad52-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="aad52-121">上記で説明されている連続プログラムを設定すると、顧客の連続注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="aad52-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="aad52-122">次の追加のメンテナンス作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="aad52-122">You might also have to perform the following additional maintenance tasks.</span></span>

- <span data-ttu-id="aad52-123">**現在の連続イベント期間の更新** – 現在のイベント期間をシステムに知らせるバッチ ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="aad52-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
- <span data-ttu-id="aad52-124">**連続の子注文の作成** – 親の連続注文から子注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="aad52-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
- <span data-ttu-id="aad52-125">**連続支払の処理** – 連続販売注文に関連付けられた支払の請求と通知を処理します。</span><span class="sxs-lookup"><span data-stu-id="aad52-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
- <span data-ttu-id="aad52-126">**連続行数の拡張** (必要な場合) – 連続イベントを繰り返す回数を拡張します。</span><span class="sxs-lookup"><span data-stu-id="aad52-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="aad52-127">これにより出荷の繰り返しは、コール センター パラメーターの **連続繰り返しのしきい値** フィールドで設定されている制限を超えて拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="aad52-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
- <span data-ttu-id="aad52-128">**連続更新の実行** (必要な場合) – 連続プログラムと親連続販売注文の間の差を同期します。</span><span class="sxs-lookup"><span data-stu-id="aad52-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
- <span data-ttu-id="aad52-129">**連続の親明細行と注文を閉じる** – 連続注文を閉じます。</span><span class="sxs-lookup"><span data-stu-id="aad52-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>

