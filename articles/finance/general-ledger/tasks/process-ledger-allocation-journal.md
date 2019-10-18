---
title: 元帳配賦仕訳帳の処理
description: このトピックでは、Dynamics 365 Finance での配賦要求の処理方法について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/26/2019
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
ms.openlocfilehash: 882362a03e4fc4e249b092caea374640813eef88
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186075"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="fd34b-103">元帳配賦仕訳帳の処理</span><span class="sxs-lookup"><span data-stu-id="fd34b-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd34b-104">このトピックでは、配賦要求の処理方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="fd34b-105">[配賦要求の処理] ページを使用して、[総勘定元帳] に転記する前に確認および承認したり、[総勘定元帳] に直接転記することが可能な配賦仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="fd34b-106">配賦仕訳帳を作成するためには、少なくとも 1 つの有効な [元帳配賦ルール] が必要です。</span><span class="sxs-lookup"><span data-stu-id="fd34b-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="fd34b-107">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="fd34b-108">ナビゲーション ウィンドウで、**モジュール > 一般会計 > 配賦 > 配賦要求の処理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="fd34b-109">**ルール** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="fd34b-110">**現在の日付**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="fd34b-111">元帳がルールのデータ ソースである場合、**現在の日付**はとても重要です。</span><span class="sxs-lookup"><span data-stu-id="fd34b-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="fd34b-112">この日付けによって、どの元帳残高を配賦に含めるかを制御します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="fd34b-113">**ゼロ ソース** フィールドで**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="fd34b-114">この操作により配賦プロセスを停止し、配賦元の金額ゼロが選択されたことを示すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="fd34b-115">**提案オプション** フィールドで、**提案のみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="fd34b-116">**提案のみ**を選択し、総勘定元帳に配賦を転記する前に、配賦仕訳帳の結果を確認し、また必要に応じて承認します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="fd34b-117">[GL 転記日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="fd34b-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-118">Select **OK**.</span></span>
7. <span data-ttu-id="fd34b-119">ナビゲーション ウィンドウで、**モジュール > 一般会計 > 配賦 > 配賦仕訳帳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="fd34b-120">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-120">Select **Lines**.</span></span>
9. <span data-ttu-id="fd34b-121">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-121">Select **Post**.</span></span>
10. <span data-ttu-id="fd34b-122">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd34b-122">Select **Post**.</span></span>

