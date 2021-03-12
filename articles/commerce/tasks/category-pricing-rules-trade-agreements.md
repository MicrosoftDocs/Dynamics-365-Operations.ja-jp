---
title: 売買契約を作成するためのカテゴリの価格決定ルール
description: この手順は、カテゴリ価格決定ルールを使用して販売価格の売買契約を作成する方法を示します。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPricingDiscountCategoryPriceRule, RetailCategoryPriceRule, EcoResCategorySingleLookup, RetailCategoryPriceWizard, PriceDiscAdm, PriceDiscAdmTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a945a0f49df92731175c1624da98831bbc5bb741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006088"
---
# <a name="category-pricing-rules-to-create-trade-agreements"></a><span data-ttu-id="5e11d-103">売買契約を作成するためのカテゴリの価格決定ルール</span><span class="sxs-lookup"><span data-stu-id="5e11d-103">Category pricing rules to create trade agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e11d-104">この手順は、カテゴリ価格決定ルールを使用して販売価格の売買契約を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-104">This procedure demonstrates how to create sales price trade agreements using a category pricing rule.</span></span> <span data-ttu-id="5e11d-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="5e11d-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5e11d-106">このタスクは、Commerce 販売促進マネージャー ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="5e11d-106">This task is intended for the Commerce merchandising manager role.</span></span>

1. <span data-ttu-id="5e11d-107">[価格設定および割引の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="5e11d-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-108">Click New.</span></span>
3. <span data-ttu-id="5e11d-109">[カテゴリ価格ルール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-109">Click Category price rule.</span></span>
4. <span data-ttu-id="5e11d-110">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-110">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="5e11d-111">[会計コード] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-111">In the Account code field, select an option.</span></span>
    * <span data-ttu-id="5e11d-112">「グループ」タイプのアカウント コードは [チャンネル]、[ロイヤルティ プログラム]、[カタログ] および [所属] 固有の販売価格の売買契約を設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e11d-112">A "Group" type account code is used to set up sales price trade agreements that are specific for Channels, Loyalty programs, Catalogs, and Affiliations.</span></span>  
6. <span data-ttu-id="5e11d-113">[勘定の選択] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-113">In the Account selection field, enter or select a value.</span></span>
7. <span data-ttu-id="5e11d-114">[カテゴリ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-114">In the Category field, enter or select a value.</span></span>
8. <span data-ttu-id="5e11d-115">[金額 / パーセンテージ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-115">In the Amount/Percent field, enter a number.</span></span>
9. <span data-ttu-id="5e11d-116">[丸めバージョン] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-116">In the Rounding version field, enter or select a value.</span></span>
10. <span data-ttu-id="5e11d-117">[売買契約の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-117">Click Generate trade agreements.</span></span>
11. <span data-ttu-id="5e11d-118">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-118">Click Next.</span></span>
12. <span data-ttu-id="5e11d-119">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-119">In the From date field, enter a date.</span></span>
13. <span data-ttu-id="5e11d-120">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-120">In the To date field, enter a date.</span></span>
14. <span data-ttu-id="5e11d-121">[次を検索] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-121">Select Yes in the Find next field.</span></span>
15. <span data-ttu-id="5e11d-122">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-122">Click Next.</span></span>
16. <span data-ttu-id="5e11d-123">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-123">Click Finish.</span></span>
    * <span data-ttu-id="5e11d-124">これにより [売買契約仕訳帳] が作成され、確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5e11d-124">This creates a Trade agreement journal and opens it for your review.</span></span>  
17. <span data-ttu-id="5e11d-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5e11d-126">[カテゴリ価格決定ルール] から作成された売買契約仕訳帳は転記されません。</span><span class="sxs-lookup"><span data-stu-id="5e11d-126">The trade agreement journals created from the Category pricing rules aren't posted.</span></span> <span data-ttu-id="5e11d-127">それらを転記する前に生成される価格を確認および編集できます。</span><span class="sxs-lookup"><span data-stu-id="5e11d-127">You can  review and edit the prices generated before posting them.</span></span>  
18. <span data-ttu-id="5e11d-128">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-128">Click Edit.</span></span>
19. <span data-ttu-id="5e11d-129">[通貨金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e11d-129">In the Amount in currency field, enter a number.</span></span>
20. <span data-ttu-id="5e11d-130">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-130">Click Post.</span></span>
21. <span data-ttu-id="5e11d-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-131">Click OK.</span></span>
22. <span data-ttu-id="5e11d-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e11d-132">Close the page.</span></span>
23. <span data-ttu-id="5e11d-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e11d-133">Close the page.</span></span>
24. <span data-ttu-id="5e11d-134">[カテゴリ価格のルール] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e11d-134">Click the Category price rules tab.</span></span>
    * <span data-ttu-id="5e11d-135">チャンネルの特定の [カテゴリ価格決定ルール] はこのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e11d-135">Channel specific Category pricing rules will show in this list.</span></span>  

