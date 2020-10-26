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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e54c69b0411ba88e808a08dcd2e2e1a194ada8
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984848"
---
# <a name="inquiries-of-the-asset-retirement-obligation-related-transactions"></a><span data-ttu-id="9b098-103">資産除去責務に関連するトランザクションの照会</span><span class="sxs-lookup"><span data-stu-id="9b098-103">Inquiries of the asset retirement obligation related transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9b098-104">日本では、資産除去責務 (ARO) のトランザクションと金額は、基になる固定資産とは別にレポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b098-104">For Japan, transactions and amounts of asset retirement obligations (ARO) need to be reported separately from the underlying fixed assets.</span></span> 



<span data-ttu-id="9b098-105">このタスクでは、ARO 固有の金額とトランザクションの表示方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b098-105">Use this task to learn how to view the ARO-specific amounts and transactions.</span></span> 



<span data-ttu-id="9b098-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b098-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="9b098-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b098-107">This task uses the JPMF demo company data.</span></span>


## <a name="view-aro-transaction"></a><span data-ttu-id="9b098-108">[ARO トランザクション] の表示</span><span class="sxs-lookup"><span data-stu-id="9b098-108">View ARO transaction</span></span>
1. <span data-ttu-id="9b098-109">[固定資産] > [資産除去責務] > [資産除去責務トランザクションの照会] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9b098-109">Go to Fixed assets > Asset retirement obligations > Asset retirement obligation transaction inquiry.</span></span>
    * <span data-ttu-id="9b098-110">ARO 関連のトランザクションは、集計のためタイプに分類されます。</span><span class="sxs-lookup"><span data-stu-id="9b098-110">ARO-related transactions are categorized into types for summarization.</span></span>  

## <a name="explore-aro"></a><span data-ttu-id="9b098-111">ARO の明細表示</span><span class="sxs-lookup"><span data-stu-id="9b098-111">Explore ARO</span></span>
1. <span data-ttu-id="9b098-112">クリックして [固定資産番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="9b098-112">Click to follow the link in the Fixed asset number field.</span></span>
    * <span data-ttu-id="9b098-113">[固定資産] ページから固定資産番号を検索して開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9b098-113">You also can find the fixed asset number and open it from the Fixed assets page.</span></span>  
2. <span data-ttu-id="9b098-114">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b098-114">On the Action Pane, click Fixed asset.</span></span>
3. <span data-ttu-id="9b098-115">[資産除去責務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b098-115">Click Asset retirement obligation.</span></span>
4. <span data-ttu-id="9b098-116">[明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9b098-116">Click Explore.</span></span>
    * <span data-ttu-id="9b098-117">これらのタブは、[予定金額]、[転記 (実際の) 金額] および差額をそれぞれ表示します。</span><span class="sxs-lookup"><span data-stu-id="9b098-117">The tabs display the Planned amount, Posted (actual) amount and Difference respectively.</span></span>  
5. <span data-ttu-id="9b098-118">[転記金額] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9b098-118">Expand or collapse the Posted amount section.</span></span>
6. <span data-ttu-id="9b098-119">[差異] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="9b098-119">Expand or collapse the Difference section.</span></span>

