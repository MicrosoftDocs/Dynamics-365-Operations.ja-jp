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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75ff895c252bfd4f70f8bcc4c4adece585d9a22
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "320400"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="bc9d1-103">クレジット カード処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bc9d1-103">Configure credit card processing</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="bc9d1-104">この手順は、支払プロバイダの一覧を表示し、売掛金勘定の支払口座を構成する方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="bc9d1-105">この手順では、デモ データの会社 USRT を使用し、管理者および IT プロフェッショナルを対象としています。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="bc9d1-106">支払プロバイダーの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-106">View a list of payment providers</span></span>
1. <span data-ttu-id="bc9d1-107">[売掛金勘定] > [支払設定] > [支払サービス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="bc9d1-108">[使用可能プロバイダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="bc9d1-109">支払アカウントの構成</span><span class="sxs-lookup"><span data-stu-id="bc9d1-109">Configure payment account</span></span>
1. <span data-ttu-id="bc9d1-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-110">Click New.</span></span>
2. <span data-ttu-id="bc9d1-111">[支払サービス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="bc9d1-112">[支払コネクタ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="bc9d1-113">[支払サービス アカウント] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="bc9d1-114">[環境] フィールドに「PROD」を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="bc9d1-115">[クレジット カード タイプ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-115">Click Credit card types.</span></span>
7. <span data-ttu-id="bc9d1-116">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bc9d1-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bc9d1-118">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-118">Click Add.</span></span>
10. <span data-ttu-id="bc9d1-119">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="bc9d1-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="bc9d1-121">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bc9d1-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bc9d1-123">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-123">Click Add.</span></span>
15. <span data-ttu-id="bc9d1-124">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="bc9d1-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bc9d1-126">必要なカード タイプの数だけこれらの手順を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="bc9d1-127">[支払仕訳帳] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="bc9d1-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="bc9d1-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-129">Click Add.</span></span>
20. <span data-ttu-id="bc9d1-130">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="bc9d1-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-131">Click Save.</span></span>
22. <span data-ttu-id="bc9d1-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-132">Close the page.</span></span>
23. <span data-ttu-id="bc9d1-133">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-133">Click Validate.</span></span>
24. <span data-ttu-id="bc9d1-134">[新しいクレジット カードの既定のプロセッサ] チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="bc9d1-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bc9d1-135">Click Save.</span></span>

