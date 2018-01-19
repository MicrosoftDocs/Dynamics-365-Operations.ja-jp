--- 
title: "小売明細書のパラメーター コンフィギュレーション"
description: "この手順では、小売明細書の作成に影響を及ぼす、転記または小売パラメーターのコンフィギュレーションを示します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
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
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: aafccb5c1a3fd98d5f88e450fe138ca7fde44982
ms.contentlocale: ja-jp
ms.lasthandoff: 01/19/2018

---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="1bc1e-103">小売明細書のパラメーター コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1bc1e-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1bc1e-104">この手順では、小売明細書の作成に影響を及ぼす、転記または小売パラメーターのコンフィギュレーションを示します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="1bc1e-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="1bc1e-106">[小売りとコマース] > [本社の設定] > [パラメーター] > [小売パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="1bc1e-107">[転記] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="1bc1e-108">期間割引金額を転記する場合は「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="1bc1e-109">既定の勘定を使用するには「標準」を選択します。あるいは、各期間割引に使用する勘定を定義するには「定期処理」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="1bc1e-110">在庫明細行が集計可能である場合には、「集計」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="1bc1e-111">請求書や支払が明細書の転記プロセス中に自動的に決済される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="1bc1e-112">金庫保管トランザクションが集計される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="1bc1e-113">銀行入金トランザクションが集計される場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="1bc1e-114">明細書の転記の集計を有効にする場合は、「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="1bc1e-115">明細書の転記時に注文を同時に作成および処理するには「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="1bc1e-116">各バッチ ジョブのタスクで処理される最大注文を入力します。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="1bc1e-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1bc1e-117">Click Save.</span></span>


