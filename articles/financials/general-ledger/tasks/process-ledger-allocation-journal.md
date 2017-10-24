--- 
title: "元帳配賦仕訳帳の処理"
description: "[配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。"
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="bee2f-103">元帳配賦仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="bee2f-103">Process ledger allocation journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bee2f-104">[配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="bee2f-105">配賦仕訳帳を作成するためには、少なくとも 1 つの有効な [元帳配賦ルール] が必要です。</span><span class="sxs-lookup"><span data-stu-id="bee2f-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="bee2f-106">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="bee2f-107">[総勘定元帳] > [配賦] > [配賦要求の処理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="bee2f-108">[ルール] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="bee2f-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bee2f-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bee2f-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee2f-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bee2f-111">[現在の日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="bee2f-112">[元帳] がルールの [データ ソース] である場合、[現在の日付] はとても重要です。</span><span class="sxs-lookup"><span data-stu-id="bee2f-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="bee2f-113">この日付けによって、どの元帳残高を配賦に含めるかを制御します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="bee2f-114">[ゼロ ソース] フィールドで [停止] を選択します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="bee2f-115">この操作により配賦プロセスを停止し、配賦元の金額ゼロが選択されたことを示すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="bee2f-116">[提案オプション] フィールドで、「提案のみ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="bee2f-117">[提案のみ] を選択し、[総勘定元帳] に配賦を転記する前に、[配賦仕訳帳] の結果を確認し、また必要に応じて承認します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="bee2f-118">[GL 転記日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="bee2f-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee2f-119">Click OK.</span></span>
9. <span data-ttu-id="bee2f-120">[総勘定元帳] > [配賦] > [配賦仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bee2f-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="bee2f-121">[行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee2f-121">Click Lines.</span></span>
11. <span data-ttu-id="bee2f-122">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee2f-122">Click Post.</span></span>
12. <span data-ttu-id="bee2f-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bee2f-123">Click Post.</span></span>


