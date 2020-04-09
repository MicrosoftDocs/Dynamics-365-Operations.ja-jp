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
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138118"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="9de2a-103">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="9de2a-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9de2a-104">このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="9de2a-105">これは、経理担当ロールと USMF デモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="9de2a-106">新しい固定資産の作成</span><span class="sxs-lookup"><span data-stu-id="9de2a-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="9de2a-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 固定資産 > 固定資産**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="9de2a-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-108">Select **New**.</span></span>
3. <span data-ttu-id="9de2a-109">**固定資産グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="9de2a-110">分割処理で使用する固定資産番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="9de2a-111">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9de2a-112">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9de2a-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="9de2a-113">固定資産の分割</span><span class="sxs-lookup"><span data-stu-id="9de2a-113">Split a fixed asset</span></span>
1. <span data-ttu-id="9de2a-114">一覧で、分割する固定資産のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="9de2a-115">**帳簿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-115">Select **Books**.</span></span> <span data-ttu-id="9de2a-116">新しい資産に分割する帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="9de2a-117">**機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-117">Select **Functions**.</span></span>
4. <span data-ttu-id="9de2a-118">**固定資産の分割**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="9de2a-119">**分割先固定資産**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="9de2a-120">**次の帳簿まで**フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9de2a-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9de2a-121">**トランザクション日付**フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="9de2a-122">**割合**フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="9de2a-123">**仕訳帳名**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="9de2a-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="9de2a-125">仕訳帳トランザクションの転記</span><span class="sxs-lookup"><span data-stu-id="9de2a-125">Post the journal transaction</span></span>
1. <span data-ttu-id="9de2a-126">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="9de2a-127">リストで、分割処理で作成された仕訳帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="9de2a-128">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-128">Select **Lines**.</span></span>

    - <span data-ttu-id="9de2a-129">作成した仕訳帳明細行を確認します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="9de2a-130">取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。</span><span class="sxs-lookup"><span data-stu-id="9de2a-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="9de2a-131">取得トランザクションは、新しい資産に対して同じ金額で作成されます。</span><span class="sxs-lookup"><span data-stu-id="9de2a-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="9de2a-132">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de2a-132">Select **Post**.</span></span>

