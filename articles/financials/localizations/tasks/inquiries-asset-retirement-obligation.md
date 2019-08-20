---
title: 資産除去責務に関連するトランザクションの照会
description: 日本では、資産除去責務 (ARO) のトランザクションと金額は、基になる固定資産とは別にレポートする必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans, AssetTable, AssetRetirementObligation_JP, AssetRetirementObligationExplorer_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e83cab94b04fe14cd5f14a071261cdd7e56da720
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852632"
---
# <a name="inquiries-of-the-asset-retirement-obligation-related-transactions"></a><span data-ttu-id="329bd-103">資産除去責務に関連するトランザクションの照会</span><span class="sxs-lookup"><span data-stu-id="329bd-103">Inquiries of the asset retirement obligation related transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="329bd-104">日本では、資産除去責務 (ARO) のトランザクションと金額は、基になる固定資産とは別にレポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="329bd-104">For Japan, transactions and amounts of asset retirement obligations (ARO) need to be reported separately from the underlying fixed assets.</span></span> 



<span data-ttu-id="329bd-105">このタスクでは、ARO 固有の金額とトランザクションの表示方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="329bd-105">Use this task to learn how to view the ARO-specific amounts and transactions.</span></span> 



<span data-ttu-id="329bd-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="329bd-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="329bd-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="329bd-107">This task uses the JPMF demo company data.</span></span>


## <a name="view-aro-transaction"></a><span data-ttu-id="329bd-108">[ARO トランザクション] の表示</span><span class="sxs-lookup"><span data-stu-id="329bd-108">View ARO transaction</span></span>
1. <span data-ttu-id="329bd-109">[固定資産] > [資産除去責務] > [資産除去責務トランザクションの照会] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="329bd-109">Go to Fixed assets > Asset retirement obligations > Asset retirement obligation transaction inquiry.</span></span>
    * <span data-ttu-id="329bd-110">ARO 関連のトランザクションは、集計のためタイプに分類されます。</span><span class="sxs-lookup"><span data-stu-id="329bd-110">ARO-related transactions are categorized into types for summarization.</span></span>  

## <a name="explore-aro"></a><span data-ttu-id="329bd-111">ARO の明細表示</span><span class="sxs-lookup"><span data-stu-id="329bd-111">Explore ARO</span></span>
1. <span data-ttu-id="329bd-112">クリックして [固定資産番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="329bd-112">Click to follow the link in the Fixed asset number field.</span></span>
    * <span data-ttu-id="329bd-113">[固定資産] ページから固定資産番号を検索して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="329bd-113">You also can find the fixed asset number and open it from the Fixed assets page.</span></span>  
2. <span data-ttu-id="329bd-114">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="329bd-114">On the Action Pane, click Fixed asset.</span></span>
3. <span data-ttu-id="329bd-115">[資産除去責務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="329bd-115">Click Asset retirement obligation.</span></span>
4. <span data-ttu-id="329bd-116">[明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="329bd-116">Click Explore.</span></span>
    * <span data-ttu-id="329bd-117">これらのタブは、[予定金額]、[転記 (実際の) 金額] および差額をそれぞれ表示します。</span><span class="sxs-lookup"><span data-stu-id="329bd-117">The tabs display the Planned amount, Posted (actual) amount and Difference respectively.</span></span>  
5. <span data-ttu-id="329bd-118">[転記金額] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="329bd-118">Expand or collapse the Posted amount section.</span></span>
6. <span data-ttu-id="329bd-119">[差異] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="329bd-119">Expand or collapse the Difference section.</span></span>

