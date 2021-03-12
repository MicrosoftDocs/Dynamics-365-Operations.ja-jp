---
title: 計画企業内需要 (アウトバウンド) の表示
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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97cccc0d27d1154d8f8cb5018cf5040efcf190a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001777"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="99c3c-103">計画企業内需要 (アウトバウンド) の表示</span><span class="sxs-lookup"><span data-stu-id="99c3c-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99c3c-104">この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="99c3c-105">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="99c3c-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="99c3c-106">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99c3c-106">Click Master planning.</span></span>
2. <span data-ttu-id="99c3c-107">[計画] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="99c3c-108">[計画] フィールドで、プラン 10 を選択します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="99c3c-109">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99c3c-109">Click Run.</span></span>
4. <span data-ttu-id="99c3c-110">[スレッド数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="99c3c-111">これは、マスタ プランに使用する並行スレッドの数を表します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="99c3c-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99c3c-112">Click OK.</span></span>
    * <span data-ttu-id="99c3c-113">しばらく時間がかかる場合があります</span><span class="sxs-lookup"><span data-stu-id="99c3c-113">This may take a while.</span></span>  
6. <span data-ttu-id="99c3c-114">[計画企業内需要] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99c3c-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="99c3c-115">[計画企業内需要 (アウトバウンド)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="99c3c-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="99c3c-116">このページは、内部サプライ チェーンの仕入先によって達成されるすべての計画需要の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="99c3c-117">[上流の需要の詳細] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="99c3c-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="99c3c-118">このセクションでは、どのように需要が達成されるかについての詳細を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="99c3c-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="99c3c-119">ここで追加情報を表示する前に、提供会社で実行するマスター プランを待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99c3c-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

