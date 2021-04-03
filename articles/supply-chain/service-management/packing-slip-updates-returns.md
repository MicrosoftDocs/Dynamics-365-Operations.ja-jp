---
title: 返品による梱包明細票の更新
description: 返品品目を在庫に入庫する前に、それらの品目が属する注文の梱包明細を更新する必要があります。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87dfad2247c84f8e85074739cfff4a2d1b9f8567
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259701"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="7e80d-103">返品による梱包明細票の更新</span><span class="sxs-lookup"><span data-stu-id="7e80d-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="7e80d-104">返品品目を在庫に入庫する前に、それらの品目が属する注文の梱包明細を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e80d-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="7e80d-105">請求書更新プロセスが財務トランザクションに対する更新であるのと同様に、梱包明細更新プロセスは在庫レコードの現物更新であり、在庫の変更をコミットすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="7e80d-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="7e80d-106">返品の場合、処分アクションに割り当てられる手順は、梱包明細の更新中に実行されます。</span><span class="sxs-lookup"><span data-stu-id="7e80d-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="7e80d-107">梱包明細の更新は、着荷仕訳帳または返品注文で処理できます。</span><span class="sxs-lookup"><span data-stu-id="7e80d-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="7e80d-108">梱包明細の転記プロセスの一環として、顧客の出荷ドキュメントに記載されている梱包明細参照番号を注文明細行に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="7e80d-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="7e80d-109">このアソシエーションはオプションであり、また参照専用です。</span><span class="sxs-lookup"><span data-stu-id="7e80d-109">This association is optional and for reference only.</span></span> <span data-ttu-id="7e80d-110">これによってトランザクションの更新は行われません。</span><span class="sxs-lookup"><span data-stu-id="7e80d-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="7e80d-111">予定の返品品目のうち到着してないものがある場合、梱包明細の更新対象には入庫された数量だけを含めることとします。</span><span class="sxs-lookup"><span data-stu-id="7e80d-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="7e80d-112">残りの返品荷物が到着するまで残りの品目は注文に残します。</span><span class="sxs-lookup"><span data-stu-id="7e80d-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="7e80d-113">検査担当者が在庫内のどこに品目が保管されているかわからない場合など、品目が検査から出荷および入荷部門に返送されてきた場合、対応する梱包明細を更新して、検査の結果として指定される廃棄コードを正しく登録し、それに従って行動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e80d-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="7e80d-114">販売契約書に基づく返品品目の梱包明細を更新すると、数量または金額の変更を反映するために、その品目の販売契約書の確約が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="7e80d-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="7e80d-115">参照</span><span class="sxs-lookup"><span data-stu-id="7e80d-115">See also</span></span>

[<span data-ttu-id="7e80d-116">返品による請求書更新の実行</span><span class="sxs-lookup"><span data-stu-id="7e80d-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]