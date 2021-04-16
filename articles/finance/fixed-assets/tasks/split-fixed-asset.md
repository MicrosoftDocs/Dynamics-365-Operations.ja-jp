---
title: 固定資産の分割
description: このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。
author: saraschi2
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa21d5698275ff691ca83d29abd297a796b652d1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823911"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="debc3-103">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="debc3-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="debc3-104">このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="debc3-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="debc3-105">これは、経理担当ロールと USMF デモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="debc3-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="debc3-106">新しい固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="debc3-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="debc3-107">ナビゲーション ウィンドウで、**モジュール \> 固定資産 \> 固定資産 \> 固定資産** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="debc3-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="debc3-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-108">Select **New**.</span></span>
3. <span data-ttu-id="debc3-109">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="debc3-110">分割処理で使用する固定資産番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="debc3-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="debc3-111">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="debc3-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="debc3-112">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="debc3-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="debc3-113">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="debc3-113">Split a fixed asset</span></span>

<span data-ttu-id="debc3-114">減価償却の対象となる資産を完全に分割する前に、資産帳簿のステータスを手動で **終了** から **オープン** に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="debc3-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="debc3-115">この手順が必要となるのは、資産のトランザクションを転記する必要がある場合 (処分販売など) には、帳簿のステータスを **オープン** にする必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="debc3-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="debc3-116">また、**総勘定元帳パラメーター** ページの **一般** タブで、**1 つの伝票内で複数のトランザクションを許可する** パラメーターもオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="debc3-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="debc3-117">資産帳簿のステータスが変更され、1 つの伝票内の複数のトランザクションが許可された後に、次の手順を実行して資産を分割します。</span><span class="sxs-lookup"><span data-stu-id="debc3-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="debc3-118">一覧で、分割する固定資産のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="debc3-119">**帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-119">Select **Books**.</span></span> <span data-ttu-id="debc3-120">新しい資産に分割する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="debc3-121">**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-121">Select **Functions**.</span></span>
4. <span data-ttu-id="debc3-122">**固定資産の分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="debc3-123">**分割先固定資産** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="debc3-124">**次の帳簿まで** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="debc3-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="debc3-125">**トランザクション日付** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="debc3-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="debc3-126">**割合** フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="debc3-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="debc3-127">**仕訳帳名** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="debc3-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="debc3-129">仕訳帳トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="debc3-129">Post the journal transaction</span></span>

1. <span data-ttu-id="debc3-130">ナビゲーション ウィンドウで、**モジュール \> 固定資産 \> 仕訳帳エントリー \> 固定資産の仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="debc3-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="debc3-131">リストで、分割処理で作成された仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="debc3-132">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-132">Select **Lines**.</span></span>

    - <span data-ttu-id="debc3-133">作成した仕訳帳明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="debc3-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="debc3-134">取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。</span><span class="sxs-lookup"><span data-stu-id="debc3-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="debc3-135">取得トランザクションは、新しい資産に対して同じ金額で作成されます。</span><span class="sxs-lookup"><span data-stu-id="debc3-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="debc3-136">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="debc3-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]