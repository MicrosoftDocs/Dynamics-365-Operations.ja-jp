---
title: 元帳配賦仕訳帳の処理
description: '[配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。'
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846370"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="439c1-103">元帳配賦仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="439c1-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="439c1-104">[配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="439c1-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="439c1-105">配賦仕訳帳を作成するためには、少なくとも 1 つの有効な [元帳配賦ルール] が必要です。</span><span class="sxs-lookup"><span data-stu-id="439c1-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="439c1-106">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="439c1-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="439c1-107">[総勘定元帳] > [配賦] > [配賦要求の処理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="439c1-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="439c1-108">[ルール] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="439c1-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="439c1-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="439c1-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="439c1-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="439c1-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="439c1-111">[現在の日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="439c1-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="439c1-112">[元帳] がルールの [データ ソース] である場合、[現在の日付] はとても重要です。</span><span class="sxs-lookup"><span data-stu-id="439c1-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="439c1-113">この日付けによって、どの元帳残高を配賦に含めるかを制御します。</span><span class="sxs-lookup"><span data-stu-id="439c1-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="439c1-114">[ゼロ ソース] フィールドで [停止] を選択します。</span><span class="sxs-lookup"><span data-stu-id="439c1-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="439c1-115">この操作により配賦プロセスを停止し、配賦元の金額ゼロが選択されたことを示すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="439c1-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="439c1-116">[提案オプション] フィールドで、「提案のみ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="439c1-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="439c1-117">[提案のみ] を選択し、[総勘定元帳] に配賦を転記する前に、[配賦仕訳帳] の結果を確認し、また必要に応じて承認します。</span><span class="sxs-lookup"><span data-stu-id="439c1-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="439c1-118">[GL 転記日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="439c1-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="439c1-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="439c1-119">Click OK.</span></span>
9. <span data-ttu-id="439c1-120">[総勘定元帳] > [配賦] > [配賦仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="439c1-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="439c1-121">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="439c1-121">Click Lines.</span></span>
11. <span data-ttu-id="439c1-122">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="439c1-122">Click Post.</span></span>
12. <span data-ttu-id="439c1-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="439c1-123">Click Post.</span></span>

