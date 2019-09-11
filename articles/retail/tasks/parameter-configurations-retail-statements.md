---
title: 小売明細書に影響を及ぼす 小売パラメーターのコンフィギュレーション
description: このトピックでは、小売明細書の作成や転記が小売パラメーターのコンフィギュレーションにどのように影響を及ぼすかを示します。
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867274"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a><span data-ttu-id="408be-103">小売明細書に影響を及ぼす 小売パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="408be-103">Configure Retail parameters that affect retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="408be-104">このトピックでは、小売明細書の作成や転記が小売パラメーターのコンフィギュレーションにどのように影響を及ぼすかを示します。</span><span class="sxs-lookup"><span data-stu-id="408be-104">This topic demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="408be-105">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="408be-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="408be-106">ナビゲーション ウィンドウで、**モジュール > 小売りとコマース > 本社の設定 > パラメーター > 小売パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="408be-106">In the navigation pane, go to **Modules > Retail and commerce > Headquarters setup  > Parameters > Retail parameters**.</span></span>
2. <span data-ttu-id="408be-107">**転記**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-107">Select the **Posting** tab.</span></span>
    - <span data-ttu-id="408be-108">期間割引金額を転記する場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-108">Select **Yes** if you want to post the periodic discount amounts specifically.</span></span>  
    - <span data-ttu-id="408be-109">既定の勘定を使用するには、**標準**を選択します。あるいは、各期間割引に使用する勘定を定義するには、**定期処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-109">Select **Standard** to use default accounts, or select **Periodic** if you want to define which account to use for each periodic discount.</span></span>  
      - <span data-ttu-id="408be-110">在庫明細行が集計可能である場合には、**集計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-110">Select **Summary** if inventory lines should get aggregated whenever possible.</span></span>  
      - <span data-ttu-id="408be-111">請求書や支払が明細書の転記プロセス中に自動的に決済される場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-111">Select **Yes** if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
      - <span data-ttu-id="408be-112">金庫保管トランザクションが集計される場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-112">Select **Yes** if Safe drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="408be-113">銀行入金トランザクションが集計される場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-113">Select **Yes** if Bank drop transactions should get aggregated.</span></span>  
      - <span data-ttu-id="408be-114">明細書の転記の集計を有効にする場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-114">Select **Yes** to turn aggregation on for Statement posting.</span></span>  
      - <span data-ttu-id="408be-115">明細書の転記時に注文を同時に作成および処理する場合は、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-115">Select **Yes** to create and process orders in parallel when statements are posted.</span></span>  
      - <span data-ttu-id="408be-116">各バッチ ジョブのタスクで処理される最大注文を入力します。</span><span class="sxs-lookup"><span data-stu-id="408be-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="408be-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="408be-117">Select **Save**.</span></span>

