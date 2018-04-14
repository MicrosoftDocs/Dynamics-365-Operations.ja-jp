--- 
title: "小売明細書のパラメーター コンフィギュレーション"
description: "この手順では、小売明細書の作成に影響を及ぼす、転記または小売パラメーターのコンフィギュレーションを示します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1322c5beaa2455c0a3f70bb5e28af55ac110eaf3
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="b440c-103">小売明細書のパラメーター コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b440c-103">Parameter configurations for Retail statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b440c-104">この手順では、小売明細書の作成に影響を及ぼす、転記または小売パラメーターのコンフィギュレーションを示します。</span><span class="sxs-lookup"><span data-stu-id="b440c-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="b440c-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b440c-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="b440c-106">[小売りとコマース] > [本社の設定] > [パラメーター] > [小売パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b440c-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="b440c-107">[転記] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b440c-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="b440c-108">期間割引金額を転記する場合は「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="b440c-109">既定の勘定を使用するには「標準」を選択します。あるいは、各期間割引に使用する勘定を定義するには「定期処理」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="b440c-110">在庫明細行が集計可能である場合には、「集計」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="b440c-111">請求書や支払が明細書の転記プロセス中に自動的に決済される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="b440c-112">金庫保管トランザクションが集計される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="b440c-113">銀行入金トランザクションが集計される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="b440c-114">明細書の転記の集計を有効にする場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="b440c-115">明細書の転記時に注文を同時に作成および処理するには「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b440c-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="b440c-116">各バッチ ジョブのタスクで処理される最大注文を入力します。</span><span class="sxs-lookup"><span data-stu-id="b440c-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="b440c-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b440c-117">Click Save.</span></span>


