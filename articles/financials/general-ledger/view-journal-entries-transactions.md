---
title: "仕訳入力およびトランザクションの表示"
description: "この記事は、仕訳入力およびトランザクションを表示するためのさまざまな方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13031
ms.assetid: 281c7ea6-4dfd-4d1f-994f-c361ee299dbe
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9768154e117ca09ae84c6a9c82d43000752c2b34
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="view-journal-entries-and-transactions"></a><span data-ttu-id="6cf70-103">仕訳入力およびトランザクションの表示</span><span class="sxs-lookup"><span data-stu-id="6cf70-103">View journal entries and transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cf70-104">この記事は、仕訳入力およびトランザクションを表示するためのさまざまな方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-104">This article explains the various ways that you can view journal entries and transactions.</span></span> 

<span data-ttu-id="6cf70-105">仕訳帳とトランザクションを表示するには、データにアクセスするためにいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="6cf70-105">Users who want to view journals and transactions have several ways to access the data.</span></span> <span data-ttu-id="6cf70-106">ドリルダウン機能を提供する [照会] ページを活用でき 、または一般会計のさまざまなレポート オプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-106">They can take advantage of inquiry pages that provide drill-down ability, or they can use various report options in the general ledger.</span></span>

## <a name="voucher-transactions"></a><span data-ttu-id="6cf70-107">伝票トランザクション</span><span class="sxs-lookup"><span data-stu-id="6cf70-107">Voucher transactions</span></span>
<span data-ttu-id="6cf70-108">**伝票トランザクション**は、条件を指定したさまざまなテーブルおよびフィールドから探している残高やトランザクションを選択できる照会ページです。</span><span class="sxs-lookup"><span data-stu-id="6cf70-108">**Voucher transactions** is an inquiry page where you can select from various tables and fields to specify criteria for the balance or transaction that you're searching for.</span></span> <span data-ttu-id="6cf70-109">たとえば、特定の日付または勘定のすべてのトランザクション、または特定の転記階層にある **作業** タイプのすべてのトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-109">For example, you can view all transactions for a specific date or account, or all transactions of the **Operating** type that are in a specific posting layer.</span></span> <span data-ttu-id="6cf70-110">既定では、ページには、仕訳帳番号、伝票、日付、および主勘定が表示されますが、検索を絞り込むために、追加のテーブル、フィールド、および条件を追加できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-110">By default, the page shows the journal number, voucher, date, and main account, but you can add additional tables, fields, and criteria to narrow down your search.</span></span>

## <a name="audit-trail"></a><span data-ttu-id="6cf70-111">監査証跡</span><span class="sxs-lookup"><span data-stu-id="6cf70-111">Audit trail</span></span>
<span data-ttu-id="6cf70-112">**監査証跡**は、トランザクション タイプ、説明、トランザクションの作成者、およびトランザクションの作成日を表示した照会ページです。</span><span class="sxs-lookup"><span data-stu-id="6cf70-112">**Audit trail** is an inquiry page that shows the types of transactions, descriptions, who the transactions were created by, and when they were created.</span></span> <span data-ttu-id="6cf70-113">**監査証跡** 照会ページで、伝票トランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-113">From the **Audit trail** inquiry page, you can view the voucher transactions.</span></span>

## <a name="financial-reports"></a><span data-ttu-id="6cf70-114">財務諸表</span><span class="sxs-lookup"><span data-stu-id="6cf70-114">Financial reports</span></span>
<span data-ttu-id="6cf70-115">財務諸表を実行して一般会計トランザクションの検討および分析もできます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-115">You can also explore and analyze general ledger transactions by running financial reports.</span></span> <span data-ttu-id="6cf70-116">財務諸表のデザインは、勘定、分析コード、勘定カテゴリ、またはその 3 つの組み合わせに基づくことができるため、さまざまな方法でドリルダウンすることによりトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-116">Because the design of financial reports can be based on accounts, dimensions, account categories, or a combination of the three, you can view the transactions by drilling down in various ways.</span></span> <span data-ttu-id="6cf70-117">一般会計トランザクションに関する詳細情報が必要な場合は、レポート デザインの一部にトランザクション プロパティを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-117">If you require more information for general ledger transactions, you can also include multiple transaction properties as part of the report design.</span></span> <span data-ttu-id="6cf70-118">また、一般会計残高を構成するトランザクションを表示するには、**試算表** リスト ページからの場合と同じように、勘定トランザクションにドリルダウンできます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-118">Additionally, if you want to see the transactions that make up a general ledger balance, you can drill down to account transactions, just as you can from the **Trial balance** list page.</span></span>

## <a name="ledger-reports"></a><span data-ttu-id="6cf70-119">元帳レポート</span><span class="sxs-lookup"><span data-stu-id="6cf70-119">Ledger reports</span></span>
<span data-ttu-id="6cf70-120">財務諸表に加えて、一般会計トランザクションを表示するには、次の元帳レポートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-120">In addition to the financial reports, you can use the following ledger reports to view general ledger transactions:</span></span>

-   <span data-ttu-id="6cf70-121">**分析コード明細書** – このレポートには、日付および勘定別にトランザクションが表示されます。またオプションとして分析コードおよび期間別にトランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-121">**Dimension statement** – This report shows transactions by day and account, and there are also options to show transactions by dimension and period.</span></span>
-   <span data-ttu-id="6cf70-122">**元帳トランザクション リスト** – このレポートは、勘定のトランザクション通貨、会計通貨、およびレポート通貨でトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-122">**Ledger transaction list** – This report shows transactions in transaction, accounting, and reporting currencies for an account.</span></span>
-   <span data-ttu-id="6cf70-123">**仕訳帳の印刷** – このレポートには、仕訳帳の転記結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-123">**Print journal** – This report shows the result of a posted journal.</span></span> <span data-ttu-id="6cf70-124">仕訳帳バッチ番号または仕訳帳タイプでレポートを実行できます。また、追加のフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="6cf70-124">You can run the report by journal batch number or journal type, or add additional fields.</span></span>
-   <span data-ttu-id="6cf70-125">**仕訳帳別転記済トランザクション** – このレポートは、仕訳帳に転記され、伝票によってグループ化されたトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-125">**Posted transactions by journal** – This report shows the transactions that have been posted to a journal, grouped by voucher.</span></span>
-   <span data-ttu-id="6cf70-126">**日付別トランザクション リスト** – このレポートは、仕訳帳番号、伝票、および勘定科目とともに、日付別のトランザクションをすべて表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-126">**Transaction list by date** – This report shows all the transactions by date, together with the journal number, voucher, and ledger account.</span></span> <span data-ttu-id="6cf70-127">また、トランザクション通貨、会計通貨、およびレポート通貨でトランザクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-127">It also shows the transactions in the transaction, accounting, and reporting currencies.</span></span>
-   <span data-ttu-id="6cf70-128">**トランザクション発生元** – このトランザクション レポートには、仕訳帳別に、またトランザクション通貨、会計通貨、およびレポート通貨別に、勘定を表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-128">**Transaction origin** – This transaction report shows the account by journal, and by transaction, accounting, and reporting currency.</span></span> <span data-ttu-id="6cf70-129">また、相手勘定として使用された仕訳帳の各行を表示します。</span><span class="sxs-lookup"><span data-stu-id="6cf70-129">It also shows each line of the journal that was used as an offset.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6cf70-130">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="6cf70-130">Additional resources</span></span>
- [<span data-ttu-id="6cf70-131">総勘定元帳残高</span><span class="sxs-lookup"><span data-stu-id="6cf70-131">General ledger account balances</span></span>](general-ledger-account-balances.md) 
- [<span data-ttu-id="6cf70-132">会計ソース エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="6cf70-132">Accounting source explorer</span></span>](../accounts-payable/accounting-source-explorer.md)
- [<span data-ttu-id="6cf70-133">財務報告</span><span class="sxs-lookup"><span data-stu-id="6cf70-133">Financial reporting</span></span>](financial-reporting-getting-started.md)
- [<span data-ttu-id="6cf70-134">仕訳入力の表示</span><span class="sxs-lookup"><span data-stu-id="6cf70-134">View journal entries</span></span>](tasks/view-journal-entries-or-transactions.md)




