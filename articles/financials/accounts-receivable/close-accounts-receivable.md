---
title: 売掛金勘定の決算
description: 次の見出しに売掛金勘定の決算業務プロセスをサポートしているページの一覧を示します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3563f0f4d7d281a02231c1d3edcfe3ceb4277f5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835265"
---
# <a name="close-accounts-receivable"></a><span data-ttu-id="7bc4a-103">売掛金勘定の決算</span><span class="sxs-lookup"><span data-stu-id="7bc4a-103">Close Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bc4a-104">次の表に売掛金勘定の決算業務プロセスをサポートしているページの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-104">The following table lists the pages that support the close Accounts receivable business process.</span></span>

> [!NOTE] 
> <span data-ttu-id="7bc4a-105">次の表で一部のページを開くには、情報の入力またはパラメーター設定の指定が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-105">To open some of the pages in the table, you must enter information or specify parameter settings.</span></span>

<span data-ttu-id="7bc4a-106">**業務プロセス コンポーネント タスク**</span><span class="sxs-lookup"><span data-stu-id="7bc4a-106">**Business process component task**</span></span>                   

<span data-ttu-id="7bc4a-107">一般会計の期間の閉鎖</span><span class="sxs-lookup"><span data-stu-id="7bc4a-107">Close periods in the general ledger</span></span>

| <span data-ttu-id="7bc4a-108">ページ名</span><span class="sxs-lookup"><span data-stu-id="7bc4a-108">Page name</span></span>                            | <span data-ttu-id="7bc4a-109">用途</span><span class="sxs-lookup"><span data-stu-id="7bc4a-109">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="7bc4a-110">バッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="7bc4a-110">Batch job</span></span>                             | <span data-ttu-id="7bc4a-111">バッチ ジョブを表示または作成します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-111">View or create batch jobs.</span></span> <span data-ttu-id="7bc4a-112">バッチ ジョブを完了できなかった可能性があるため、すべての転記が完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-112">Batch jobs might not be completed, and you want to make sure that all posting is completed.</span></span>                                                                                                               |
|<span data-ttu-id="7bc4a-113">販売注文の確認</span><span class="sxs-lookup"><span data-stu-id="7bc4a-113">Confirm sales order</span></span>                   | <span data-ttu-id="7bc4a-114">販売注文を更新します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-114">Update sales orders.</span></span>                                                                       |
|<span data-ttu-id="7bc4a-115">外貨再評価</span><span class="sxs-lookup"><span data-stu-id="7bc4a-115">Foreign currency revaluation</span></span>          | <span data-ttu-id="7bc4a-116">外貨で転記された未処理の顧客トランザクションの値を更新するトランザクションを生成します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-116">Generate transactions that update the value of open customer transactions in foreign currencies.</span></span>                                                                                                                         |
| <span data-ttu-id="7bc4a-117">仕訳帳</span><span class="sxs-lookup"><span data-stu-id="7bc4a-117">Journal</span></span>                              | <span data-ttu-id="7bc4a-118">請求書、支払、および約束手形を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-118">Post invoices, payments, and promissory notes.</span></span>                                             |
| <span data-ttu-id="7bc4a-119">仕訳伝票</span><span class="sxs-lookup"><span data-stu-id="7bc4a-119">Journal voucher</span></span>                      |<ul><li><span data-ttu-id="7bc4a-120">**支払仕訳帳** : 支払を生成、処理、および転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-120">**Payment journal** – Generate, process, and post payments.</span></span></li><li><span data-ttu-id="7bc4a-121">**為替手形振出仕訳帳** : 為替手形を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-121">**Draw bill of exchange journal** – Post bills of exchange.</span></span></li><li><span data-ttu-id="7bc4a-122">**為替手形受取拒否仕訳帳** : 受取拒否手形を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-122">**Protest bill of exchange journal** – Post protested bills of exchange.</span></span></li><li><span data-ttu-id="7bc4a-123">**為替手形仕訳の振出** : 再振出済為替手形を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-123">**Redraw bill of exchange journal** – Post redrawn bills of exchange.</span></span></li><li><span data-ttu-id="7bc4a-124">**送金仕訳帳** : 送金を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-124">**Remittance journal** – Post remittances.</span></span></li><li><span data-ttu-id="7bc4a-125">**為替手形仕訳帳の決済** : 決済済為替手形を転記します</span><span class="sxs-lookup"><span data-stu-id="7bc4a-125">**Settle bill of exchange journal** – Post settled bills of exchange</span></span></li></ul>                   |
| <span data-ttu-id="7bc4a-126">梱包明細転記</span><span class="sxs-lookup"><span data-stu-id="7bc4a-126">Packing slip posting</span></span>                 | <span data-ttu-id="7bc4a-127">販売注文の梱包明細を更新します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-127">Update packing slips for sales orders.</span></span>                                                     |
| <span data-ttu-id="7bc4a-128">自由書式の請求書の転記</span><span class="sxs-lookup"><span data-stu-id="7bc4a-128">Post free text invoice</span></span>               | <span data-ttu-id="7bc4a-129">自由書式の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-129">Post free text invoices.</span></span>                                                                   |
| <span data-ttu-id="7bc4a-130">請求の転記</span><span class="sxs-lookup"><span data-stu-id="7bc4a-130">Posting invoice</span></span>                      | <span data-ttu-id="7bc4a-131">販売注文の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-131">Post invoices for sales orders.</span></span>                                                            |
| <span data-ttu-id="7bc4a-132">ピッキング リストの転記</span><span class="sxs-lookup"><span data-stu-id="7bc4a-132">Posting picking list</span></span>                 |<span data-ttu-id="7bc4a-133">販売注文のピッキング リストを更新します。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-133">Update picking lists for sales orders.</span></span>                                                      |

<span data-ttu-id="7bc4a-134">**業務プロセス コンポーネント タスク**</span><span class="sxs-lookup"><span data-stu-id="7bc4a-134">**Business process component task**</span></span>   

<span data-ttu-id="7bc4a-135">EU 販売リストの作成および送信</span><span class="sxs-lookup"><span data-stu-id="7bc4a-135">Create and submit the EU sales list</span></span>

| <span data-ttu-id="7bc4a-136">ページ名</span><span class="sxs-lookup"><span data-stu-id="7bc4a-136">Page name</span></span>                            | <span data-ttu-id="7bc4a-137">用途</span><span class="sxs-lookup"><span data-stu-id="7bc4a-137">Usage</span></span>                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|<span data-ttu-id="7bc4a-138">EU 販売リスト</span><span class="sxs-lookup"><span data-stu-id="7bc4a-138">EU sales list</span></span>                         | <span data-ttu-id="7bc4a-139">付加価値税 (VAT) 申告のための売上税所轄官庁への欧州連合 (EU) 販売のレポート。</span><span class="sxs-lookup"><span data-stu-id="7bc4a-139">Report on European Union (EU) sales to the tax authority for value-added tax (VAT) declaration purposes.</span></span>                                                                                                                           |






