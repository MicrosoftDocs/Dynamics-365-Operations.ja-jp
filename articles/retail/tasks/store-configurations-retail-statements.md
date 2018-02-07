--- 
title: "小売明細書の店舗のコンフィギュレーション"
description: "この手順では、小売明細書の作成される影響を及ぼす、転記または小売店舗のコンフィギュレーションを説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="45809-103">小売明細書の店舗のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="45809-103">Store configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="45809-104">この手順では、小売明細書の作成される影響を及ぼす、転記または小売店舗のコンフィギュレーションを説明します。</span><span class="sxs-lookup"><span data-stu-id="45809-104">This procedure walks through configurations for the Retail store that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="45809-105">小売店舗の財務分析コードは別の手順に含まれます。</span><span class="sxs-lookup"><span data-stu-id="45809-105">Financial dimensions on Retail stores are covered in another procedure.</span></span> <span data-ttu-id="45809-106">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="45809-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="45809-107">[小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="45809-107">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="45809-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="45809-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="45809-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="45809-110">[明細書/決済] セクションの設定は、明細書の作成、検証、店舗の転記に影響します。</span><span class="sxs-lookup"><span data-stu-id="45809-110">The settings in the Statement/closing section affect the statement creation, validation, and posting for the store.</span></span>  <span data-ttu-id="45809-111">[明細書/決算] セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="45809-111">Open the Statement/closing section.</span></span>  
    * <span data-ttu-id="45809-112">明細行のグループ化に使用する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-112">Select the method you want to use to group the statement lines by.</span></span>  
    * <span data-ttu-id="45809-113">明細書を作成するバッチ ジョブから明細書を作成するとき、1 日あたり一つの明細書のみが作成されるようにするには、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-113">Select "Yes" if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
    * <span data-ttu-id="45809-114">[支払/入金申告の計算] フィールドは、支払/入金申告を一緒に追加するか、または最後の一つを使用するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="45809-114">The Tender declaration calculation field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
    * <span data-ttu-id="45809-115">丸め差額を転記する [勘定科目] を選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-115">Select the ledger account to post rounding differences into.</span></span>  
    * <span data-ttu-id="45809-116">[最大丸め金額] フィールドでは、許可されている最大丸め誤差を入力できます。</span><span class="sxs-lookup"><span data-stu-id="45809-116">In the Maximum rounding difference field, you can enter the maximum rounding difference allowed.</span></span>  
    * <span data-ttu-id="45809-117">[転記] フィールドでは、明細書で許可される最大転記差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="45809-117">In the Posting field, you can enter the maximum total posting difference allowed for a statement.</span></span>  
    * <span data-ttu-id="45809-118">[シフト] フィールドでは、明細書のシフトの最大差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="45809-118">In the Shift field, you can enter the maximum total difference within a shift in a statement.</span></span>  
    * <span data-ttu-id="45809-119">[トランザクション] フィールドでは、明細行の最大差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="45809-119">In the Transaction field, you can enter the maximum total difference in a statement line.</span></span>  
    * <span data-ttu-id="45809-120">[決済方法] フィールドで、明細書に含まれているトランザクションが終了したシフトの一部であるか、または定義済みの日時範囲内のトランザクションであるかどうかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="45809-120">In the Closing method field, you can define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
    * <span data-ttu-id="45809-121">午前 0 時より後に前日に転記される必要のあるトランザクションが発生した場合、[営業日の終了] フィールドに時間を入力できます。</span><span class="sxs-lookup"><span data-stu-id="45809-121">In the End of business day field, you can enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
    * <span data-ttu-id="45809-122">午前 0 時より後に、前日に転記される必要のあるトランザクションが発生した場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-122">Select "Yes" if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
    * <span data-ttu-id="45809-123">定義された各明細書の方法で明細書が作成されるようにする場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="45809-123">Select "Yes" to get statements created for each statement method defined.</span></span> <span data-ttu-id="45809-124">これは、並列処理できる小さな明細書が大量に作成されるため、店舗の大量のトランザクションの転記のパフォーマンスを改善する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="45809-124">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
    * <span data-ttu-id="45809-125">[既定の顧客] フィールドで、飛び込みの顧客への販売に使用する顧客口座を選択できます。</span><span class="sxs-lookup"><span data-stu-id="45809-125">In the Default customer field, you can select the customer account to use for sales to walk-in customers.</span></span>  


