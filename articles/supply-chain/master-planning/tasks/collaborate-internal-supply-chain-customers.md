---
title: 社内サプライ チェーンの顧客との共同作業
description: この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb807a904afaba09d0dc364c06f964c135d3cfb1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208665"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="5394d-103">社内サプライ チェーンの顧客との共同作業</span><span class="sxs-lookup"><span data-stu-id="5394d-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5394d-104">この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5394d-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="5394d-105">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="5394d-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="5394d-106">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5394d-106">Click Master planning.</span></span>
2. <span data-ttu-id="5394d-107">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5394d-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="5394d-108">[計画] フィールドで、プラン 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="5394d-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="5394d-109">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5394d-109">Click Run.</span></span>
4. <span data-ttu-id="5394d-110">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5394d-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="5394d-111">これは、マスタ プランに使用する並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="5394d-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="5394d-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5394d-112">Click OK.</span></span>
    * <span data-ttu-id="5394d-113">しばらく時間がかかる場合があります</span><span class="sxs-lookup"><span data-stu-id="5394d-113">This may take a while.</span></span>  
6. <span data-ttu-id="5394d-114">[計画企業内需要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5394d-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="5394d-115">[計画企業内需要 (アウトバウンド)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5394d-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="5394d-116">このページは、内部サプライ チェーンの仕入先によって達成されるすべての計画需要の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="5394d-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="5394d-117">[上流の需要の詳細] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5394d-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="5394d-118">このセクションでは、どのように需要が達成されるかについての詳細を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5394d-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="5394d-119">ここで追加情報を表示する前に、提供会社で実行するマスター プランを待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5394d-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

