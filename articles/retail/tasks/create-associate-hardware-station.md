---
title: ハードウェア ステーションの作成と関連付け
description: この手順では、新しいハードウェア ステーションを作成する方法を説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80df4fa663d208e28f5c9b031b6610d29286171c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548396"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="a7477-103">ハードウェア ステーションの作成と関連付け</span><span class="sxs-lookup"><span data-stu-id="a7477-103">Create and associate a hardware station</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a7477-104">この手順では、新しいハードウェア ステーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a7477-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="a7477-105">新しいハードウェア プロファイルは、あらかじめ定義された店舗 (チャンネル) に新しいハードウェア ステーションを追加するために作成および使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7477-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="a7477-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="a7477-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="a7477-107">Commerce エッセンシャル > チャンネル >.. に移動します</span><span class="sxs-lookup"><span data-stu-id="a7477-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="a7477-108">> ..</span><span class="sxs-lookup"><span data-stu-id="a7477-108">> ..</span></span> <span data-ttu-id="a7477-109">> ..</span><span class="sxs-lookup"><span data-stu-id="a7477-109">> ..</span></span> <span data-ttu-id="a7477-110">> ハードウェア ステーションのプロファイル。</span><span class="sxs-lookup"><span data-stu-id="a7477-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="a7477-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-111">Click New.</span></span>
3. <span data-ttu-id="a7477-112">[ハードウェア ステーション ID] フィールドで、「TestHWProfile」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7477-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="a7477-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7477-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a7477-114">[ポート番号] フィールドに数を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7477-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="a7477-115">[ハードウェア プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7477-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a7477-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a7477-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a7477-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a7477-118">[パッケージ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7477-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="a7477-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7477-120">これは新しい環境が含まれる標準パッケージです。</span><span class="sxs-lookup"><span data-stu-id="a7477-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="a7477-121">バージョン番号が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7477-121">The version number may vary.</span></span>  
11. <span data-ttu-id="a7477-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-122">Click Save.</span></span>
12. <span data-ttu-id="a7477-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a7477-123">Close the page.</span></span>
13. <span data-ttu-id="a7477-124">[小売りとコマース] > [チャンネル] > [すべての小売店舗] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a7477-124">Go to Retail and commerce > Channels > All retail stores.</span></span>
14. <span data-ttu-id="a7477-125">一覧で行 17 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7477-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="a7477-126">デモ データの会社 USRT を使用している場合、ヒューストン店となります。</span><span class="sxs-lookup"><span data-stu-id="a7477-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="a7477-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a7477-128">[ハードウェア ステーション] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a7477-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="a7477-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-129">Click Add.</span></span>
18. <span data-ttu-id="a7477-130">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a7477-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="a7477-131">[プロファイル ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7477-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="a7477-132">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a7477-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a7477-133">これは、前の手順で作成した新しいハードウェア ステーションのプロファイルである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7477-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="a7477-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="a7477-135">[ホスト名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7477-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="a7477-136">[EFT ターミナル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7477-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="a7477-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7477-137">Click Save.</span></span>

