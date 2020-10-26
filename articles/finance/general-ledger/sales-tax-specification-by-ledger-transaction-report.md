---
title: 元帳トランザクション別消費税詳細のレポート
description: このトピックでは、元帳トランザクション レポート別の消費税詳細を使用して、消費税の計算対象である元帳トランザクションに関する情報を表示および印刷する方法について説明します。
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 438a640124e778b839c660f5e161efa22c319af0
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976094"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="f5581-103">元帳トランザクション別消費税詳細のレポート</span><span class="sxs-lookup"><span data-stu-id="f5581-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5581-104">このトピックでは、**元帳トランザクション別の消費税詳細**レポートを使用して、消費税の計算対象である元帳トランザクションに関する情報を表示および印刷する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f5581-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="f5581-105">税勘定と非課税勘定の対比</span><span class="sxs-lookup"><span data-stu-id="f5581-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="f5581-106">**元帳トランザクション別の消費税詳細**レポートには、税勘定と非課税勘定の両方の税トランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5581-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="f5581-107">これらの勘定は、次のように分類されます。</span><span class="sxs-lookup"><span data-stu-id="f5581-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="f5581-108">**税勘定** – 税トランザクションが転記されると勘定は税勘定と見なされ、**消費税**仕訳帳明細行の主勘定は、消費税支払の勘定または消費税収入の勘定などの税勘定となります。</span><span class="sxs-lookup"><span data-stu-id="f5581-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="f5581-109">**非課税勘定** – 税トランザクションが転記されると勘定は非課税勘定と見なされ、元のトランザクションの主勘定は、収益勘定または経費勘定などの非課税勘定となります。</span><span class="sxs-lookup"><span data-stu-id="f5581-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="f5581-110">税勘定の場合、レポートの**発生元**、**消費税収入**、**消費税支払**列は **0**(ゼロ) と表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5581-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="f5581-111">非課税勘定の場合は、これらの列に金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5581-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="f5581-112">レポート上のデータをフィルタリング</span><span class="sxs-lookup"><span data-stu-id="f5581-112">Filtering the data on the report</span></span>

<span data-ttu-id="f5581-113">レポートを生成するとき、次の既定のフィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f5581-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="f5581-114">これらのフィールドを使用して、レポートに表示されるデータをフィルタリングできます。</span><span class="sxs-lookup"><span data-stu-id="f5581-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="f5581-115">フィールド</span><span class="sxs-lookup"><span data-stu-id="f5581-115">Field</span></span>                      | <span data-ttu-id="f5581-116">説明</span><span class="sxs-lookup"><span data-stu-id="f5581-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="f5581-117">日</span><span class="sxs-lookup"><span data-stu-id="f5581-117">Date</span></span>                       | <span data-ttu-id="f5581-118">**開始**および**終了**セクションのフィールドを使用して、税トランザクションの日付範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="f5581-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="f5581-119">主勘定</span><span class="sxs-lookup"><span data-stu-id="f5581-119">Main account</span></span>               | <span data-ttu-id="f5581-120">**開始**および**終了**セクションのフィールドを使用して、主勘定の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="f5581-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="f5581-121">消費税コード</span><span class="sxs-lookup"><span data-stu-id="f5581-121">Sales tax code</span></span>             | <span data-ttu-id="f5581-122">**開始**および**終了**セクションのフィールドを使用して、消費税コードの範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="f5581-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="f5581-123">グループ化</span><span class="sxs-lookup"><span data-stu-id="f5581-123">Grouping</span></span>                   | <span data-ttu-id="f5581-124">レポートを勘定科目別または消費税コード別にグループ化するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5581-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="f5581-125">消費税コードごとの小計</span><span class="sxs-lookup"><span data-stu-id="f5581-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="f5581-126">消費税コード別の小計を表示するには、このオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f5581-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="f5581-127">合計のみ</span><span class="sxs-lookup"><span data-stu-id="f5581-127">Totals only</span></span>                | <span data-ttu-id="f5581-128">合計のみを表示するには、このオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f5581-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="f5581-129">主勘定のみ</span><span class="sxs-lookup"><span data-stu-id="f5581-129">Main accounts only</span></span>         | <span data-ttu-id="f5581-130">レポートに主勘定のみを含めるには、このオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f5581-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="f5581-131">レポートで非課税勘定のみを表示する</span><span class="sxs-lookup"><span data-stu-id="f5581-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="f5581-132">レポートで非課税勘定のみを表示するには、次の図に示すように、アスタリスク(\*) などのフィルター条件を設定します。</span><span class="sxs-lookup"><span data-stu-id="f5581-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![非課税勘定を表示するレポート](media/taxspecperledgertrans.png)
