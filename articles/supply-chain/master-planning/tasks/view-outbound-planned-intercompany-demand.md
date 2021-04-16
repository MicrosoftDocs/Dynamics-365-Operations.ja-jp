---
title: 計画企業内需要 (アウトバウンド) の表示
description: この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2eb361e1c1d18369d6b945ec18a7e3a6a1ebfb97
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829597"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="7b5b3-103">計画企業内需要 (アウトバウンド) の表示</span><span class="sxs-lookup"><span data-stu-id="7b5b3-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b5b3-104">この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="7b5b3-105">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="7b5b3-106">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-106">Click Master planning.</span></span>
2. <span data-ttu-id="7b5b3-107">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="7b5b3-108">[計画] フィールドで、プラン 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="7b5b3-109">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-109">Click Run.</span></span>
4. <span data-ttu-id="7b5b3-110">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="7b5b3-111">これは、マスタ プランに使用する並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="7b5b3-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-112">Click OK.</span></span>
    * <span data-ttu-id="7b5b3-113">しばらく時間がかかる場合があります</span><span class="sxs-lookup"><span data-stu-id="7b5b3-113">This may take a while.</span></span>  
6. <span data-ttu-id="7b5b3-114">[計画企業内需要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="7b5b3-115">[計画企業内需要 (アウトバウンド)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="7b5b3-116">このページは、内部サプライ チェーンの仕入先によって達成されるすべての計画需要の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="7b5b3-117">[上流の需要の詳細] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="7b5b3-118">このセクションでは、どのように需要が達成されるかについての詳細を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="7b5b3-119">ここで追加情報を表示する前に、提供会社で実行するマスター プランを待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b5b3-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]