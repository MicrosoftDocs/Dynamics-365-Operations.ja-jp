---
title: 一般会計と財務諸表の概要
description: 法人の財務レコードを定義および管理するには、一般会計を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e795e641314b4ef81f8972aadf597721995fcc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186535"
---
# <a name="general-ledger-overview"></a><span data-ttu-id="63fd6-103">一般会計の概要</span><span class="sxs-lookup"><span data-stu-id="63fd6-103">General ledger overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63fd6-104">法人の財務レコードを定義および管理するには、一般会計を使用します。</span><span class="sxs-lookup"><span data-stu-id="63fd6-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="63fd6-105">一般会計では借方と貸方のエントリ登録です。</span><span class="sxs-lookup"><span data-stu-id="63fd6-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="63fd6-106">これらのエントリは、勘定科目表に表示される勘定を使用して分類されます。</span><span class="sxs-lookup"><span data-stu-id="63fd6-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="63fd6-107">勘定科目表の計画</span><span class="sxs-lookup"><span data-stu-id="63fd6-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="63fd6-108">主勘定タイプ</span><span class="sxs-lookup"><span data-stu-id="63fd6-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="63fd6-109">配賦ルールに基づいて、金額を、1 つ以上の勘定または勘定と分析コードの組み合わせに配賦または配分できます。</span><span class="sxs-lookup"><span data-stu-id="63fd6-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="63fd6-110">配賦には、固定と変動の 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="63fd6-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="63fd6-111">また、勘定科目間のトランザクションを決済し、通貨金額を再評価することもできます。</span><span class="sxs-lookup"><span data-stu-id="63fd6-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="63fd6-112">会計年度末には、決算トランザクションを生成し、次の会計年度に使用する勘定を用意します。</span><span class="sxs-lookup"><span data-stu-id="63fd6-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="63fd6-113">連結機能を使用すれば、複数の関連する法人の財務結果を 1 つの連結した組織の結果にまとめることができます。</span><span class="sxs-lookup"><span data-stu-id="63fd6-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="63fd6-114">関連会社は、同じデータベースに格納することも、別のデータベースに格納することもできます。</span><span class="sxs-lookup"><span data-stu-id="63fd6-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="63fd6-115">連結と削除の概要</span><span class="sxs-lookup"><span data-stu-id="63fd6-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="63fd6-116">総勘定元帳残高</span><span class="sxs-lookup"><span data-stu-id="63fd6-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="63fd6-117">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="63fd6-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="63fd6-118">[![業務プロセス](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="63fd6-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="63fd6-119">消費税</span><span class="sxs-lookup"><span data-stu-id="63fd6-119">Sales tax</span></span>
<span data-ttu-id="63fd6-120">すべての会社は税金を徴収し、さまざまな税務当局に支払います。</span><span class="sxs-lookup"><span data-stu-id="63fd6-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="63fd6-121">ルールと税率は国/地域、都道府県、市区郡、および市町村によって異なります。</span><span class="sxs-lookup"><span data-stu-id="63fd6-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="63fd6-122">また、ルールは、税務当局が要件を変更した際に、定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63fd6-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="63fd6-123">売上税コードには、徴収額と当局への支払額に関する基本的な情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="63fd6-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="63fd6-124">売上税コードの設定時には、徴収する必要のある金額または割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="63fd6-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="63fd6-125">また、トランザクション金額に金額や割合を適用する各種方法も定義します。</span><span class="sxs-lookup"><span data-stu-id="63fd6-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="63fd6-126">このセクションのトピックでは、税務当局が定める徴収方法と税率に対して売上税コードを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="63fd6-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="63fd6-127">消費税の概要</span><span class="sxs-lookup"><span data-stu-id="63fd6-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="63fd6-128">基準金額および計算方法に基づいた、売上税の税率</span><span class="sxs-lookup"><span data-stu-id="63fd6-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="63fd6-129">消費税支払と丸めルール</span><span class="sxs-lookup"><span data-stu-id="63fd6-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="63fd6-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="63fd6-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="63fd6-131">新機能および開発中の機能</span><span class="sxs-lookup"><span data-stu-id="63fd6-131">What's new and in development</span></span>

<span data-ttu-id="63fd6-132">計画されている新機能については、[Microsoft Dynamics 365 リリース ノート](https://go.microsoft.com/fwlink/?linkid=2010158) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63fd6-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="63fd6-133">ブログ</span><span class="sxs-lookup"><span data-stu-id="63fd6-133">Blogs</span></span>

<span data-ttu-id="63fd6-134">意見、ニュース、その他の情報については、[Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) および[Microsoft Dynamics 365 Finance and Operations - Financials のブログ](https://community.dynamics.com/365/financeandoperations/b/financials) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63fd6-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="63fd6-135">[Microsoft Dynamics Operations Partner Community Blog (Microsoft Dynamics Operations パートナー コミュニティのブログ)](https://community.dynamics.com/partner/b/operationspartnercommunityblog) では、MBS Operations に関する最新情報とトレンドを知るための単一のリソースが Microsoft Dynamics パートナー向けに提供されています。</span><span class="sxs-lookup"><span data-stu-id="63fd6-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="63fd6-136">ビデオ</span><span class="sxs-lookup"><span data-stu-id="63fd6-136">Videos</span></span>

<span data-ttu-id="63fd6-137">[Microsoft Dynamics 365 YouTube チャンネル](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ) のハウツー ビデオをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="63fd6-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="63fd6-138">コミュニティのブログ</span><span class="sxs-lookup"><span data-stu-id="63fd6-138">Community blogs</span></span>

- [<span data-ttu-id="63fd6-139">Dynamics 365 for Finance and Operations の元帳に関する確認事項</span><span class="sxs-lookup"><span data-stu-id="63fd6-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)
