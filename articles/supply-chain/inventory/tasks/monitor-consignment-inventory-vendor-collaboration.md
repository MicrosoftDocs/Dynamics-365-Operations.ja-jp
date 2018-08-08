---
title: "仕入先コラボレーションを使用した委託販売在庫の監視"
description: "この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8e4a620fe5f5ab3c0fae8b04d79e9912111b7ece
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="2f72a-103">仕入先コラボレーションを使用した委託販売在庫の監視</span><span class="sxs-lookup"><span data-stu-id="2f72a-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f72a-104">この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="2f72a-105">顧客が在庫品目の所有権を取得したときの在庫品目の移動状況をチェックすることができます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="2f72a-106">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="2f72a-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="2f72a-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="2f72a-108">移動した在庫品目を表示する</span><span class="sxs-lookup"><span data-stu-id="2f72a-108">View consumed inventory</span></span>
1. <span data-ttu-id="2f72a-109">[仕入先コラボレーション] > [委託販売在庫] > [委託販売在庫から受領された製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="2f72a-110">リストは、委託製品在庫の所有権が仕入先から顧客に変更されたとき生成された製品受領明細行を示します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="2f72a-111">数量およびその他の情報を確認するには、右にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="2f72a-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="2f72a-112">このリストにある情報で顧客の請求書を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="2f72a-113">データを Microsoft Excel にエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="2f72a-114">[発注書を表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f72a-114">Click View purchase order.</span></span>
3. <span data-ttu-id="2f72a-115">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="2f72a-116">明細行が委託製品としてマークされます。ヘッダー セクションは発注書が「受領」の状態であることを示します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="2f72a-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="2f72a-118">手持在庫の表示</span><span class="sxs-lookup"><span data-stu-id="2f72a-118">View on-hand inventory</span></span>
1. <span data-ttu-id="2f72a-119">[仕入先コラボレーション] > [委託販売在庫] > [手持委託販売在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="2f72a-120">手持委託製品在庫のページは、その在庫が顧客の倉庫で所有していることを示します。</span><span class="sxs-lookup"><span data-stu-id="2f72a-120">The On-hand consignment inventory page shows the stock that you own at the customer’s warehouse.</span></span> <span data-ttu-id="2f72a-121">[規模のタブを表示] をクリックして、サイトや倉庫などその他の規模を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2f72a-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

