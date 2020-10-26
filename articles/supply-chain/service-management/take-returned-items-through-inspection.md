---
title: 検査による返却品目の受入
description: 検査による返却品目を受け入れます。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc42f9c5ece8e2c2570cadf623f52648b7b174e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985794"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="d4c8c-103">検査による返却品目の受入</span><span class="sxs-lookup"><span data-stu-id="d4c8c-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="d4c8c-104">**在庫管理** \> **定期処理** \> **品質管理** \> **検査指示**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="d4c8c-105">検査する返品品目に対応する注文明細行を検索します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="d4c8c-106">1 つの検査指示は、1 つの品目番号にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="d4c8c-107">品目番号が異なる 10 個の品目が一度の出荷で返品されて検査に送られる場合、10 個の別々の検査指示が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="d4c8c-108">品目を調べた後、**廃棄コード**フィールドで選択を行って、品目に対する作業、および関連する財務トランザクションの処理方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="d4c8c-109">たとえば、品目を在庫に戻して顧客に払戻したり、品目を廃棄して顧客に交換品目を送ったり、品目を貸方なしで顧客に返送したりします。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="d4c8c-110">1 つの品目番号のバッチに含まれる複数の返品品目に同一の廃棄コードを割り当てられない場合、サブバッチごとに異なる廃棄コードを割り当てるために検査指示を分割 (<STRONG>機能</STRONG> &gt; <STRONG>分割</STRONG>) する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="d4c8c-111">検査が終了したら、**完了レポート**をクリックし、返品品目をリリースして着荷仕訳帳のエントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="d4c8c-112">次に、品目を入庫した担当者または部門が、在庫に戻される品目の仕訳を処理します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="d4c8c-113">- または -</span><span class="sxs-lookup"><span data-stu-id="d4c8c-113">–or–</span></span>
    
    <span data-ttu-id="d4c8c-114">検査指示を終了し、いずれかの**在庫**機能を使用して品目を在庫に直接移動します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="d4c8c-115">フォームを閉じて、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d4c8c-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c8c-116">参照</span><span class="sxs-lookup"><span data-stu-id="d4c8c-116">See also</span></span>

[<span data-ttu-id="d4c8c-117">返品品目の廃棄方法の指定</span><span class="sxs-lookup"><span data-stu-id="d4c8c-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


