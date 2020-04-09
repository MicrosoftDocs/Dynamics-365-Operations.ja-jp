---
title: 小売店舗の明細書の作成、計算、および転記
description: このトピックでは、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f1b0a34205e192957405bc9d298c45c8bb4d25
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141017"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="84368-103">小売店舗の明細書の作成、計算、および転記</span><span class="sxs-lookup"><span data-stu-id="84368-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84368-104">このトピックでは、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="84368-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="84368-105">同じタスクにコンフィギュレーションできるバッチ ジョブもあります。</span><span class="sxs-lookup"><span data-stu-id="84368-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="84368-106">他のトピックで、バッチ ジョブをコンフィギュレーションし、実行するための手順を検索できます。</span><span class="sxs-lookup"><span data-stu-id="84368-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="84368-107">この手順を完了するには、POS で完了して Dynamics 365 Commerce で取り出されたトランザクションが必要です。</span><span class="sxs-lookup"><span data-stu-id="84368-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="84368-108">この記録では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="84368-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="84368-109">ホーム ページから**店舗の財務**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="84368-110">**新しい明細書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-110">Select **New statement**.</span></span>
3. <span data-ttu-id="84368-111">**店舗番号**フィールドで、ドロップダウンからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="84368-112">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-112">Select **OK**.</span></span>
5. <span data-ttu-id="84368-113">**設定**グループには、どのトランザクションを明細書に含めるか、どのように明細行にグループ化するかを制御する設定があります。</span><span class="sxs-lookup"><span data-stu-id="84368-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="84368-114">**設定**グループを開き、これらの設定を変更することもできますが、既定値を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="84368-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="84368-115">**明細書の方法**フィールドで明細行をグループ化する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="84368-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="84368-116">特定のスタッフ メンバーまたはレジスターの明細書のみ計算する場合、スタッフ メンバーまたはレジスターを**スタッフ/レジスター** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="84368-117">**決済方法**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="84368-118">アクション ウィンドウから**明細書の計算**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="84368-119">**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-119">Select **Yes**.</span></span>
    - <span data-ttu-id="84368-120">明細書を計算した後、各支払方法の合計金額と使用された明細書の方法が記された行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="84368-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="84368-121">入力、または更新する必要がある場合、各行に計算済金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="84368-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="84368-122">計算済フィールドには、POS で実行した支払/入金申告の金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="84368-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="84368-123">アクション ウィンドウから**明細書の転記**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="84368-124">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-124">Select **Close**.</span></span>
11. <span data-ttu-id="84368-125">ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="84368-125">Close the pane.</span></span>
12. <span data-ttu-id="84368-126">ホーム ページで、**店舗の財務**を選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="84368-127">**転記済明細書**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="84368-127">Select the **Posted statements** tab.</span></span>

