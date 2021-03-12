---
title: クレジット カード処理のコンフィギュレーション
description: この手順は、支払プロバイダの一覧を表示し、売掛金勘定の支払口座を構成する方法を説明しています。
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 611cc49d2373247da141d2fafc149d05f3bd13b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006113"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="2b318-103">クレジット カード処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2b318-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b318-104">この手順は、支払プロバイダの一覧を表示し、売掛金勘定の支払口座を構成する方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="2b318-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="2b318-105">この手順では、デモ データの会社 USRT を使用し、管理者および IT プロフェッショナルを対象としています。</span><span class="sxs-lookup"><span data-stu-id="2b318-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="2b318-106">支払プロバイダーの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="2b318-106">View a list of payment providers</span></span>
1. <span data-ttu-id="2b318-107">[売掛金勘定] > [支払設定] > [支払サービス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b318-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="2b318-108">[使用可能プロバイダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="2b318-109">支払アカウントの構成</span><span class="sxs-lookup"><span data-stu-id="2b318-109">Configure payment account</span></span>
1. <span data-ttu-id="2b318-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-110">Click New.</span></span>
2. <span data-ttu-id="2b318-111">[支払サービス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b318-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="2b318-112">[支払コネクタ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b318-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="2b318-113">[支払サービス アカウント] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2b318-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="2b318-114">[環境] フィールドに「PROD」を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b318-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="2b318-115">[クレジット カード タイプ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-115">Click Credit card types.</span></span>
7. <span data-ttu-id="2b318-116">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2b318-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2b318-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2b318-118">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-118">Click Add.</span></span>
10. <span data-ttu-id="2b318-119">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b318-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="2b318-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2b318-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2b318-121">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2b318-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2b318-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2b318-123">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-123">Click Add.</span></span>
15. <span data-ttu-id="2b318-124">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b318-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="2b318-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2b318-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2b318-126">必要なカード タイプの数だけこれらの手順を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="2b318-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="2b318-127">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2b318-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="2b318-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2b318-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-129">Click Add.</span></span>
20. <span data-ttu-id="2b318-130">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b318-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="2b318-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-131">Click Save.</span></span>
22. <span data-ttu-id="2b318-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2b318-132">Close the page.</span></span>
23. <span data-ttu-id="2b318-133">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-133">Click Validate.</span></span>
24. <span data-ttu-id="2b318-134">[新しいクレジット カードの既定のプロセッサ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2b318-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="2b318-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2b318-135">Click Save.</span></span>

