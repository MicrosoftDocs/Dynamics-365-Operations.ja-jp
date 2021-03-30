---
title: 期末に一般会計を決算
description: このトピックでは、一般会計の期間締めを実行する場合に通常完了するタスクについて説明します
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe90e29e5ae71492519d9ab0d4cab2d12765cf4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212376"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="6b2f3-103">期末に一般会計を決算</span><span class="sxs-lookup"><span data-stu-id="6b2f3-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b2f3-104">このトピックでは、一般会計の期間締めを実行する場合に通常完了するタスクについて説明します</span><span class="sxs-lookup"><span data-stu-id="6b2f3-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="6b2f3-105">一般会計では、期または年度で決算手続きを完了できます。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="6b2f3-106">決算プロセスでは、新しい期間のためのシステムを準備します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="6b2f3-107">新しい年度のシステムを準備するには、年度末決算処理を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="6b2f3-108">各組織には、期末に実行するさまざまなプロセスやステップがあります。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="6b2f3-109">次に、期末のオプションの手順をいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="6b2f3-110">売掛金勘定、買掛金勘定、在庫などの、他のすべてのモジュールのためのすべてのタスクを完了します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="6b2f3-111">すべての仕訳帳が転記されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="6b2f3-112">未実現利益または損失金額を生成するために外貨再評価を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="6b2f3-113">各勘定科目のトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="6b2f3-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="6b2f3-114">配賦要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-114">Process any required allocations.</span></span>
-   <span data-ttu-id="6b2f3-115">手動で期末調整を転記します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="6b2f3-116">トランザクションを仕訳し、**元帳仕訳帳** レポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="6b2f3-117">連結会社または財務報告を使用して連結を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="6b2f3-118">財務報告を使用して期末財務諸表を生成します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="6b2f3-119">他の転記が発生しないように、元帳期間を **保留中** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="6b2f3-120">期末の活動の実行中に、使いやすさのため、期を特定のユーザー グループに制限できます。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="6b2f3-121">決算済みの期間を再度開くことはできないため、期間を **完全に閉じる** に設定するのは、よい考えではありません。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="6b2f3-122">財務期間終了ワークスペースを使用して、さまざまな期末処理プロセスに必要なタスクを整理して追跡できます。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="6b2f3-123">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b2f3-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="6b2f3-124">財務期間終了ワークスペース</span><span class="sxs-lookup"><span data-stu-id="6b2f3-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="6b2f3-125">年度末決算</span><span class="sxs-lookup"><span data-stu-id="6b2f3-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="6b2f3-126">財務期間一括終了</span><span class="sxs-lookup"><span data-stu-id="6b2f3-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]