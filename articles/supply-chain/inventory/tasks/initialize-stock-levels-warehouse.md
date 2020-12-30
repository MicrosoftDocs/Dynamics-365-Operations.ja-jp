---
title: 倉庫の在庫レベルの初期化
description: この手順では、在庫移動仕訳帳を使用して手持在庫を手動で更新する方法を示します。
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03481ddc5bd12b3459b69d65b1cfaeb23c60dfd4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432225"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="14d22-103">倉庫の在庫レベルの初期化</span><span class="sxs-lookup"><span data-stu-id="14d22-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14d22-104">この手順では、在庫移動仕訳帳を使用して手持在庫を手動で更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="14d22-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="14d22-105">(データ エンティティのトランザクションをインポートして手持在庫を更新することもできます。) 仕訳帳名、品目の設定、転記プロファイル、勘定などのすべての前提条件が揃っているデモ データの会社 USMF でこのガイドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="14d22-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="14d22-106">このガイドでは、使用する品目および分析コードに対して特定の値が提示されます。</span><span class="sxs-lookup"><span data-stu-id="14d22-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="14d22-107">別の品目を選択する場合は、別の分析コードの値を入力する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="14d22-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="14d22-108">[在庫管理] > [仕訳入力] > [品目] > [移動] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="14d22-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="14d22-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-109">Click New.</span></span>
3. <span data-ttu-id="14d22-110">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="14d22-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="14d22-111">[IMov] を選択します。</span><span class="sxs-lookup"><span data-stu-id="14d22-111">Select IMov.</span></span>
    * <span data-ttu-id="14d22-112">異なる事業目的ごとに異なる仕訳帳名のテンプレートを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="14d22-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="14d22-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="14d22-114">[相手勘定] フィールドに値「140200」を指定します。</span><span class="sxs-lookup"><span data-stu-id="14d22-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="14d22-115">これは、仕訳帳明細行で既定の勘定となる相手勘定です。</span><span class="sxs-lookup"><span data-stu-id="14d22-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="14d22-116">既定値を上書きして、行ごとに異なる相殺勘定を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="14d22-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="14d22-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-117">Click OK.</span></span>
8. <span data-ttu-id="14d22-118">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-118">Click New.</span></span>
9. <span data-ttu-id="14d22-119">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="14d22-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="14d22-120">品目 A0001 を選択します。</span><span class="sxs-lookup"><span data-stu-id="14d22-120">Select item A0001.</span></span>
11. <span data-ttu-id="14d22-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="14d22-122">[在庫分析コード] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="14d22-123">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="14d22-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="14d22-124">サイト 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="14d22-124">Select site 1.</span></span>
15. <span data-ttu-id="14d22-125">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="14d22-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="14d22-126">倉庫 13 を選択します。</span><span class="sxs-lookup"><span data-stu-id="14d22-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="14d22-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="14d22-128">[場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="14d22-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="14d22-129">場所 13 を選択します。</span><span class="sxs-lookup"><span data-stu-id="14d22-129">Select location 13.</span></span>
20. <span data-ttu-id="14d22-130">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14d22-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="14d22-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-131">Click Save.</span></span>
22. <span data-ttu-id="14d22-132">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-132">Click Post.</span></span>
23. <span data-ttu-id="14d22-133">[すべての転記エラーを新しい仕訳帳に転送] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="14d22-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="14d22-134">このオプションを有効にすると、転記が失敗する明細行は新しい仕訳帳にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="14d22-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="14d22-135">ログにある情報を使用して問題を修正してから明細行を再転記できます。</span><span class="sxs-lookup"><span data-stu-id="14d22-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="14d22-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14d22-136">Click OK.</span></span>
25. <span data-ttu-id="14d22-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="14d22-137">Close the page.</span></span>
26. <span data-ttu-id="14d22-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="14d22-138">Close the page.</span></span>

