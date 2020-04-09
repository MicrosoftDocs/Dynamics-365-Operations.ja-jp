---
title: 製造オーダーの終了
description: この手順では、製造オーダーの終了方法を説明します。
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb84d3b1908d6be889a49f7386de876cb52141ab
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149047"
---
# <a name="end-a-production-order"></a><span data-ttu-id="37306-103">製造オーダーの終了</span><span class="sxs-lookup"><span data-stu-id="37306-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37306-104">この手順では、製造オーダーの終了方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="37306-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="37306-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="37306-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37306-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 最後の手順です。</span><span class="sxs-lookup"><span data-stu-id="37306-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="37306-107">製造オーダーの終了</span><span class="sxs-lookup"><span data-stu-id="37306-107">End a production order</span></span>
1. <span data-ttu-id="37306-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="37306-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="37306-109">ステータスが [報告済] つまり完了済の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="37306-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="37306-110">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="37306-111">[終了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-111">Click End.</span></span>
    * <span data-ttu-id="37306-112">このページで、終了する製造オーダーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="37306-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="37306-113">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-113">Click the General tab.</span></span>
5. <span data-ttu-id="37306-114">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="37306-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="37306-115">[仕損方法] フィールドで「配賦」を選択します。</span><span class="sxs-lookup"><span data-stu-id="37306-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="37306-116">[配賦方法] を選択すると、仕損材料の原価は完成品に追加されます。</span><span class="sxs-lookup"><span data-stu-id="37306-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="37306-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="37306-118">計算結果の検証</span><span class="sxs-lookup"><span data-stu-id="37306-118">Validate calculation results</span></span>
1. <span data-ttu-id="37306-119">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="37306-120">[原価の比較の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37306-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="37306-121">製造オーダーの終了後は、見積原価価格を実際の原価価格と比較して製造差異の概要を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="37306-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
