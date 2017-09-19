--- 
title: "小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション"
description: "この手順は、分析コード値を使用する小売チャンネルの財務分析コードの作成と小売店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 56b586e971cfd4684f3c0b259270cc8b31521ac9
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="cf1b9-103">小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cf1b9-103">Create financial dimensions for Retail channels and configure dimension values on stores</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cf1b9-104">この手順は、分析コード値を使用する小売チャンネルの財務分析コードの作成と小売店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-104">This procedure walks through creating a retail channel financial dimension with dimension values and steps to configure financial dimension values on retail stores.</span></span> <span data-ttu-id="cf1b9-105">このトピックには、分析コード セットおよび勘定構造の作成などの関連手順は含まれません。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="cf1b9-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cf1b9-107">[総勘定元帳] > [勘定科目表] > [分析コード] > [財務分析コード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="cf1b9-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-108">Click New.</span></span>
3. <span data-ttu-id="cf1b9-109">[値の使用元] フィールドで、[小売チャンネル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-109">In the Use values from field, select 'Retail channels'.</span></span>
4. <span data-ttu-id="cf1b9-110">[分析コード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="cf1b9-111">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-111">Click Activate.</span></span>
6. <span data-ttu-id="cf1b9-112">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-112">Click Close.</span></span>
7. <span data-ttu-id="cf1b9-113">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-113">Click Activate.</span></span>
8. <span data-ttu-id="cf1b9-114">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-114">Click Dimension values.</span></span>
9. <span data-ttu-id="cf1b9-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-115">Close the page.</span></span>
10. <span data-ttu-id="cf1b9-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-116">Click Save.</span></span>
11. <span data-ttu-id="cf1b9-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-117">Close the page.</span></span>
12. <span data-ttu-id="cf1b9-118">[小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-118">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
13. <span data-ttu-id="cf1b9-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cf1b9-120">[財務分析コード] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="cf1b9-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-121">Click Edit.</span></span>
16. <span data-ttu-id="cf1b9-122">[Retailchannel] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-122">In the Retailchannel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="cf1b9-123">リストで、更新された店舗の分析コード値を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="cf1b9-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="cf1b9-125">[CostCenter] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="cf1b9-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="cf1b9-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="cf1b9-128">[部門] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="cf1b9-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="cf1b9-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="cf1b9-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf1b9-131">Click Save.</span></span>

