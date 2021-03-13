---
title: 仕入先コラボレーションを使用した委託販売在庫の監視
description: この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f2e782bed4cd9f2f13e2ee45afffaef277279131
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020132"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="f0a02-103">仕入先コラボレーションを使用した委託販売在庫の監視</span><span class="sxs-lookup"><span data-stu-id="f0a02-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0a02-104">この手順は、顧客との委託販売で置いた製品の在庫レベルに関する情報を表示する際の仕入先との連携方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="f0a02-105">顧客が在庫品目の所有権を取得したときの在庫品目の移動状況をチェックすることができます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="f0a02-106">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="f0a02-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="f0a02-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="f0a02-108">移動した在庫品目を表示する</span><span class="sxs-lookup"><span data-stu-id="f0a02-108">View consumed inventory</span></span>
1. <span data-ttu-id="f0a02-109">[仕入先コラボレーション] > [委託販売在庫] > [委託販売在庫から受領された製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="f0a02-110">リストは、委託製品在庫の所有権が仕入先から顧客に変更されたとき生成された製品受領明細行を示します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="f0a02-111">数量およびその他の情報を確認するには、右にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="f0a02-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="f0a02-112">このリストにある情報で顧客の請求書を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="f0a02-113">また、データを Microsoft Excel にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="f0a02-114">[発注書を表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f0a02-114">Click View purchase order.</span></span>
3. <span data-ttu-id="f0a02-115">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="f0a02-116">明細行が委託製品としてマークされます。ヘッダー セクションは発注書が「受領」の状態であることを示します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="f0a02-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="f0a02-118">手持在庫の表示</span><span class="sxs-lookup"><span data-stu-id="f0a02-118">View on-hand inventory</span></span>
1. <span data-ttu-id="f0a02-119">[仕入先コラボレーション] > [委託販売在庫] > [手持委託販売在庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="f0a02-120">手持委託製品在庫ページは、顧客の倉庫で所有している在庫を示します。</span><span class="sxs-lookup"><span data-stu-id="f0a02-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="f0a02-121">[規模のタブを表示] をクリックして、サイトや倉庫などその他の規模を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f0a02-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   

