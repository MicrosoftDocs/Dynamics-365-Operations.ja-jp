---
title: 固定資産の分割
description: このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000296"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="24f4c-103">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="24f4c-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24f4c-104">このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="24f4c-105">これは、経理担当ロールと USMF デモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="24f4c-106">新しい固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="24f4c-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="24f4c-107">ナビゲーション ウィンドウで、 **モジュール \> 固定資産 \> 固定資産 \> 固定資産** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="24f4c-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-108">Select **New**.</span></span>
3. <span data-ttu-id="24f4c-109">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="24f4c-110">分割処理で使用する固定資産番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="24f4c-111">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="24f4c-112">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="24f4c-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="24f4c-113">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="24f4c-113">Split a fixed asset</span></span>

<span data-ttu-id="24f4c-114">減価償却の対象となる資産を完全に分割する前に、資産帳簿のステータスを手動で **終了** から **オープン** に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24f4c-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="24f4c-115">この手順が必要となるのは、資産のトランザクションを転記する必要がある場合 (処分販売など) には、帳簿のステータスを **オープン** にする必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="24f4c-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="24f4c-116">資産帳簿のステータスが変更されたら、次の手順に従って資産を分割します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="24f4c-117">一覧で、分割する固定資産のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="24f4c-118">**帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-118">Select **Books**.</span></span> <span data-ttu-id="24f4c-119">新しい資産に分割する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="24f4c-120">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-120">Select **Functions**.</span></span>
4. <span data-ttu-id="24f4c-121">**固定資産の分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="24f4c-122">**分割先固定資産** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="24f4c-123">**次の帳簿まで** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="24f4c-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="24f4c-124">**トランザクション日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="24f4c-125">**割合** フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="24f4c-126">**仕訳帳名** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="24f4c-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="24f4c-128">仕訳帳トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="24f4c-128">Post the journal transaction</span></span>

1. <span data-ttu-id="24f4c-129">ナビゲーション ウィンドウで、 **モジュール \> 固定資産 \> 仕訳帳エントリー \> 固定資産の仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="24f4c-130">リストで、分割処理で作成された仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="24f4c-131">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-131">Select **Lines**.</span></span>

    - <span data-ttu-id="24f4c-132">作成した仕訳帳明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="24f4c-133">取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。</span><span class="sxs-lookup"><span data-stu-id="24f4c-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="24f4c-134">取得トランザクションは、新しい資産に対して同じ金額で作成されます。</span><span class="sxs-lookup"><span data-stu-id="24f4c-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="24f4c-135">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24f4c-135">Select **Post**.</span></span>
