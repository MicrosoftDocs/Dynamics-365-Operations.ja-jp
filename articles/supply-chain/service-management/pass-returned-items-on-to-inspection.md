---
title: 返品品目を検査に渡す
description: 返品品目を登録する場合、品目を在庫に戻すか、なんらかの手段で処分する前に、品目を検査に送ります。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e8205db277715f4f4f9c1ee589f264c0ded6617
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431988"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="b2e36-103">返品品目を検査に渡す</span><span class="sxs-lookup"><span data-stu-id="b2e36-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b2e36-104">返品品目を登録する場合、品目を在庫に戻すか、なんらかの手段で処分する前に、品目を検査に送ることがあります。</span><span class="sxs-lookup"><span data-stu-id="b2e36-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="b2e36-105">**在庫管理** \> **仕訳帳** \> **品目到着** \> **品目到着** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e36-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="b2e36-106">\-または-</span><span class="sxs-lookup"><span data-stu-id="b2e36-106">\-or-</span></span>
    
    <span data-ttu-id="b2e36-107">**在庫管理** \> **仕訳帳** \> **品目到着** \> **生産入力** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b2e36-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="b2e36-108">通常どおり、**在庫場所仕訳帳** フォームで、品目の受入を登録してください。</span><span class="sxs-lookup"><span data-stu-id="b2e36-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b2e36-109">返品品目の受入登録の詳細については、<A href="register-the-receipt-of-returned-items.md">返品品目の受取の登録</A>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2e36-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="b2e36-110">**既定値** タブの、**取扱方法** 領域で、**検査管理** ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b2e36-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="b2e36-111">システムから検査指示が作成され、検査の担当者または担当部署が **検査指示** フォームを使ってこの指示に対応します。</span><span class="sxs-lookup"><span data-stu-id="b2e36-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2e36-112">参照</span><span class="sxs-lookup"><span data-stu-id="b2e36-112">See also</span></span>

[<span data-ttu-id="b2e36-113">検査による返却品目の受入</span><span class="sxs-lookup"><span data-stu-id="b2e36-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="b2e36-114">返品品目の廃棄方法の指定</span><span class="sxs-lookup"><span data-stu-id="b2e36-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

