---
title: 小売明細書の店舗のコンフィギュレーション
description: この手順では、コマース明細書の作成される影響を及ぼす、転記または店舗のコンフィギュレーションを説明します。
author: jashanno
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: da862af25df241ad42b7e1ade3fdca19f6280278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804116"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="0466d-103">小売明細書の店舗のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0466d-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0466d-104">この手順では、コマース明細書の作成される影響を及ぼす、転記または店舗のコンフィギュレーションを説明します。</span><span class="sxs-lookup"><span data-stu-id="0466d-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="0466d-105">店舗の財務分析コードは別の手順に含まれます。</span><span class="sxs-lookup"><span data-stu-id="0466d-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="0466d-106">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="0466d-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="0466d-107">**ナビゲーション ウィンドウ** で、**モジュール > Retail と Commerce > チャネル > 店舗 > すべての店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0466d-107">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="0466d-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0466d-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0466d-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0466d-110">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0466d-110">Click **Edit**.</span></span>
5. <span data-ttu-id="0466d-111">**明細書/決済** クイック タブの設定は、明細書の作成、検証、店舗の転記に影響します。</span><span class="sxs-lookup"><span data-stu-id="0466d-111">The settings in the **Statement/closing** FastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="0466d-112">**明細書/決済** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="0466d-112">Expand the **Statement/closing** FastTab.</span></span>  
6. <span data-ttu-id="0466d-113">**明細書の方法** フィールドで、明細行のグループ化に使用する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-113">In the **Statement method** field, select the method you want to use to group the statement lines by.</span></span>  
7. <span data-ttu-id="0466d-114">明細書を作成するバッチ ジョブから明細書を作成するとき、1 日あたり 1 つの明細書のみが作成されるようにするには、**1 日に 1 つの明細書** で「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="0466d-115">**支払/入金申告の計算** フィールドは、支払/入金申告を一緒に追加するか、または最後の 1 つを使用するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="0466d-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="0466d-116">**丸め** フィールドで、丸め差額を転記する勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="0466d-117">**最大丸め誤差** フィールドでは、許可されている最大丸め誤差を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="0466d-118">**転記** フィールドでは、明細書で許可される最大転記差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="0466d-119">**シフト** フィールドでは、明細書のシフトの最大差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="0466d-120">**トランザクション** フィールドでは、明細行の最大差額の合計を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="0466d-121">**決済方法** フィールドで、明細書に含まれているトランザクションが終了したシフトの一部であるか、または定義済みの日時範囲内のトランザクションであるかどうかを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="0466d-122">午前 0 時より後に前日に転記される必要のあるトランザクションが発生した場合、**営業日の終了** フィールドに時間を入力できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="0466d-123">午前 0 時より後に、前日に転記される必要のあるトランザクションが発生した場合は、**営業日として転記する** で「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="0466d-124">定義された各明細書の方法で明細書が作成されるようにする場合は、**明細書の方法別分割** で「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0466d-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="0466d-125">このアクションは、並列処理できる小さな明細書が大量に作成されるため、店舗の大量のトランザクションの転記のパフォーマンスを改善する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0466d-125">This action can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="0466d-126">**一般** クイック タブの **既存の顧客** フィールドで、飛び込みの顧客への販売に使用する顧客口座を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0466d-126">In the **General** FastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]