--- 
title: "小売店舗の明細書の作成、計算、および転記"
description: "この手順では、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
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
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="78d60-103">小売店舗の明細書の作成、計算、および転記</span><span class="sxs-lookup"><span data-stu-id="78d60-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="78d60-104">この手順では、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="78d60-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="78d60-105">同じタスクにコンフィギュレーションできるバッチ ジョブもあります。</span><span class="sxs-lookup"><span data-stu-id="78d60-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="78d60-106">他のトピックで、バッチ ジョブをコンフィギュレーションし、実行するための手順を検索できます。</span><span class="sxs-lookup"><span data-stu-id="78d60-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="78d60-107">この手順を完了するには、POS で完了して Dynamics AX で取り出されたトランザクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="78d60-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="78d60-108">この記録では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="78d60-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="78d60-109">この手順は、Microsoft Dynamics AX を参照する場合があります。</span><span class="sxs-lookup"><span data-stu-id="78d60-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="78d60-110">Dynamics AX は現在 Microsoft Dynamics 365 for Operations と呼ばれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="78d60-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="78d60-111">すべてのワークスペース > .. に移動します</span><span class="sxs-lookup"><span data-stu-id="78d60-111">Go to All workspaces > ..</span></span> <span data-ttu-id="78d60-112">> 小売店舗の財務。</span><span class="sxs-lookup"><span data-stu-id="78d60-112">> Retail store financials.</span></span>
2. <span data-ttu-id="78d60-113">[新しい明細書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-113">Click New statement.</span></span>
3. <span data-ttu-id="78d60-114">[店舗番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="78d60-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="78d60-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="78d60-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-116">Click OK.</span></span>
    * <span data-ttu-id="78d60-117">[設定グループ] には、どのトランザクションを明細書に含めるか、どのように明細行にグループ化するかを制御する設定があります。</span><span class="sxs-lookup"><span data-stu-id="78d60-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="78d60-118">[設定グループ] を開き、これらの設定を変更することもできますが、既定値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="78d60-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="78d60-119">[明細書の方法] フィールドで明細行をグループ化する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="78d60-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="78d60-120">特定のスタッフ メンバーまたはレジスターの明細書のみ計算する場合、スタッフ メンバーまたはレジスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="78d60-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="78d60-121">[決済方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="78d60-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="78d60-122">[明細書の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="78d60-123">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-123">Click Yes.</span></span>
    * <span data-ttu-id="78d60-124">明細書を計算した後、各支払方法の合計金額と使用された明細書の方法が記された行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="78d60-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="78d60-125">入力、または更新する必要がある場合、各行に計算済金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="78d60-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="78d60-126">計算済フィールドには、POS で実行した支払/入金申告の金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="78d60-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="78d60-127">[明細書の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-127">Click Post statement.</span></span>
10. <span data-ttu-id="78d60-128">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-128">Click Close.</span></span>
11. <span data-ttu-id="78d60-129">[小売りとコマース] > [チャンネル] > [小売店舗の財務] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="78d60-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="78d60-130">[転記済明細書] のタブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78d60-130">Click the Posted statements tab.</span></span>

