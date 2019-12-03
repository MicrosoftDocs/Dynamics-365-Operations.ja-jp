---
title: バッチ追跡品目の処理の改善
description: このトピックでは、小売明細書転記プロセス時のバッチ追跡品目のバッチの処理に対して行われた改善について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770166"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="5563b-103">バッチ追跡品目の処理の改善</span><span class="sxs-lookup"><span data-stu-id="5563b-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="5563b-104">Retail 販売時点管理 (POS) では、バッチ追跡品目のバッチ番号を販売時に取得することはできません。</span><span class="sxs-lookup"><span data-stu-id="5563b-104">In Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="5563b-105">ただし、特定の構成では、顧客の注文または明細書の転記を通じて販売が本社に転記されるとき、Microsoft Dynamics システムは、バッチ追跡品目に対して有効なバッチ番号が存在することと、請求プロセスで有効なバッチ番号が使用されることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="5563b-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="5563b-106">製品に対して有効なバッチ番号が存在する場合は、顧客注文の請求プロセスと、明細書の転記からの販売注文請求プロセスでそのバッチ番号が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5563b-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="5563b-107">それ以外の場合、顧客注文請求プロセスは転記できず、POS ユーザーにはエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5563b-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="5563b-108">その結果、明細書を転記しようとするとエラー状態になります。</span><span class="sxs-lookup"><span data-stu-id="5563b-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="5563b-109">このエラー状態は、製品のマイナス在庫が有効になっていても発生します。</span><span class="sxs-lookup"><span data-stu-id="5563b-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="5563b-110">Retail バージョン 10.0.4 以降で行われた改善では、バッチ追跡品目に対してマイナス在庫が有効になっているとき、在庫が 0 (ゼロ) であるか、またはバッチ番号が使用できない場合、明細書の転記を通じた顧客注文の請求と販売注文の請求がブロックされないことが保証されます。</span><span class="sxs-lookup"><span data-stu-id="5563b-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="5563b-111">この新しい機能では、バッチ番号が使用できないとき、販売明細行の既定のバッチ ID が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5563b-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="5563b-112">顧客注文に使用される既定のバッチ ID を定義するには、**小売パラメーター** ページの **顧客注文** タブの **注文** クイック タブで、**既定のバッチ ID** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5563b-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="5563b-113">明細書の転記を通じた販売注文の請求に使用される既定のバッチ ID を定義するには、**小売パラメーター** ページの **転記** タブの **在庫更新** クイック タブで、**既定のバッチ ID** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5563b-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="5563b-114">この機能は、特定の店舗倉庫および品目に対して高度な倉庫管理が有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5563b-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="5563b-115">後のリリースでは、この機能は、高度な倉庫管理が使用されていない場合にもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5563b-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="5563b-116">倉庫管理が複雑でない場合、明細書を転記する際にバッチ追跡項目の処理を改善するためのサポートが Retail バージョン 10.0.5 に導入されました。</span><span class="sxs-lookup"><span data-stu-id="5563b-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
