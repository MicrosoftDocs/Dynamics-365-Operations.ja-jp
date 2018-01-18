--- 
title: "オンラインの販売と支払の転記"
description: "この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: ddcee5b2ccb5337f2ef4c7fb4c66b2208c231d2a
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="b06cf-103">オンラインの販売と支払の転記</span><span class="sxs-lookup"><span data-stu-id="b06cf-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b06cf-104">この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="b06cf-105">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="b06cf-106">[すべてのワークスペース] > [小売店舗の財務] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="b06cf-107">[注文の同期] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="b06cf-108">[組織階層] のフィールドで、「地域ごとの小売店舗」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="b06cf-109">店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="b06cf-110">選択した項目を追加するには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="b06cf-111">[バックグラウンドで実行] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="b06cf-112">[バッチ処理] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="b06cf-113">[再実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-113">Click Recurrence.</span></span>
7. <span data-ttu-id="b06cf-114">[終了日なし] のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-114">Select the No end date option.</span></span>
8. <span data-ttu-id="b06cf-115">[カウント] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b06cf-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="b06cf-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-116">Click OK.</span></span>
10. <span data-ttu-id="b06cf-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b06cf-117">Click OK.</span></span>


