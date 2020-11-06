---
title: 銀行管理ワークスペース
description: このトピックでは、銀行管理ワークスペースに関する情報を示します。 このワークスペースは、会社の銀行口座に関連する情報を表示し、概要ビューと分析ページが含まれます。 概要ビューでは、概要タイル、銀行口座情報、残高チャート、および関連情報を表示します。 分析ページは、Microsoft Power BI の機能を使用して、銀行口座残高に関連付けられているビジュアルを表示します。
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4b7d2da346880278f684a796f2d649e7da52b647
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097189"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="3397d-106">銀行管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="3397d-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3397d-107">**銀行管理** ワークスペースは、会社の銀行口座に関連する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3397d-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="3397d-108">このワークスペースには、 **概要** ビューと **分析** ページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3397d-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="3397d-109">**概要** ビューでは、概要タイル、銀行口座情報、残高チャート、および関連情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3397d-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="3397d-110">**分析** ページは、Microsoft Power BI の機能を使用して、銀行口座残高に関連付けられているビジュアルを表示します。</span><span class="sxs-lookup"><span data-stu-id="3397d-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="3397d-111">概要ビュー</span><span class="sxs-lookup"><span data-stu-id="3397d-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="3397d-112">概要</span><span class="sxs-lookup"><span data-stu-id="3397d-112">Summary</span></span>

<span data-ttu-id="3397d-113">**概要** セクションのタイルは、銀行口座の概要を示し、最も頻繁に使用する必要があるページにすばやくアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3397d-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="3397d-114">口座調整情報は、詳細な口座調整機能に固有です。</span><span class="sxs-lookup"><span data-stu-id="3397d-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="3397d-115">**銀行口座** ページの **詳細な口座調整** オプションを **はい** と設定してある銀行口座の場合にだけ情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3397d-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="3397d-116">**概要** セクションから、すべての法人間で銀行口座の電子銀行ファイルをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3397d-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="3397d-117">銀行口座</span><span class="sxs-lookup"><span data-stu-id="3397d-117">Bank accounts</span></span>

<span data-ttu-id="3397d-118">法人の各銀行口座は、 **銀行口座** セクションのカードによって表されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="3397d-119">現在の残高が表示され、その集計残高金額を構成するトランザクションをドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="3397d-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="3397d-120">**つなぎ勘定トランザクションを** 金額でも、その集計金額を構成するトランザクションをドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="3397d-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="3397d-121">つなぎ勘定トランザクションとは、連結機能を使用して転記されたが、まだクリアされていない、保留中のトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="3397d-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="3397d-122">**保留中の残高** 金額は、現在の残高マイナスつなぎ勘定、または保留中、のトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="3397d-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="3397d-123">銀行口座が前回調整された時期もカードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="3397d-124">この情報は、銀行口座の詳細な口座調整が有効になっている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="3397d-125">差引</span><span class="sxs-lookup"><span data-stu-id="3397d-125">Balance</span></span>

<span data-ttu-id="3397d-126">**残高** チャートは、 **銀行口座** セクションで選択した銀行口座の履歴残高情報、または法人のすべての銀行口座の履歴残高情報の概要、のいずれかを表示します。</span><span class="sxs-lookup"><span data-stu-id="3397d-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="3397d-127">この情報は、現在の週、現在の月、現在の年、過去 5 年間、およびすべての期間 (銀行口座の完全な履歴) など、まざまな期間で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="3397d-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="3397d-128">単一の銀行口座の **残高** チャートを表示している場合、残高履歴は銀行口座の通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="3397d-129">法人のすべての銀行口座のチャートを表示している場合、残高履歴は会計通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="3397d-130">データが最後に更新された時に関する情報は、チャートの上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3397d-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="3397d-131">必要なデータを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="3397d-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="3397d-132">関連情報</span><span class="sxs-lookup"><span data-stu-id="3397d-132">Related information</span></span>

<span data-ttu-id="3397d-133">**関連情報** セクションから、 **一般仕訳帳** ページを開き銀行間振替を実行します。</span><span class="sxs-lookup"><span data-stu-id="3397d-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="3397d-134">**銀行トランザクション** ページ、および **つなぎ勘定トランザクション** ページもすばやく開くことができます。</span><span class="sxs-lookup"><span data-stu-id="3397d-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="3397d-135">分析ビュー</span><span class="sxs-lookup"><span data-stu-id="3397d-135">Analytics view</span></span>

<span data-ttu-id="3397d-136">**分析** ページは、現在の会社の銀行口座に関する重要なメトリックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3397d-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="3397d-137">このページでは以下の視覚エフェクト機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="3397d-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="3397d-138">システム通貨での銀行預金残高の合計</span><span class="sxs-lookup"><span data-stu-id="3397d-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="3397d-139">法人ごとの残高</span><span class="sxs-lookup"><span data-stu-id="3397d-139">Balance by legal entity</span></span>
-   <span data-ttu-id="3397d-140">銀行口座通貨での、現在の実績対予測残高</span><span class="sxs-lookup"><span data-stu-id="3397d-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="3397d-141">銀行口座ごとの残高</span><span class="sxs-lookup"><span data-stu-id="3397d-141">Balance by bank account</span></span>
-   <span data-ttu-id="3397d-142">通貨別残高</span><span class="sxs-lookup"><span data-stu-id="3397d-142">Balance by currency</span></span>

<span data-ttu-id="3397d-143">**現金の概要 – すべての会社** ワークスペースから、すべての会社での銀行分析を表示できます。</span><span class="sxs-lookup"><span data-stu-id="3397d-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="3397d-144">詳細については、[現金の概要 Power BI コンテンツ](Cash-Overview-Power-BI-content.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3397d-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>
