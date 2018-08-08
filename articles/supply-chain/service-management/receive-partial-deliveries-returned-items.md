---
title: "返品品目の分納の受取"
description: "分納は、返品注文の出荷ではなく返品注文明細行に対して定義されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="e0747-103">返品品目の分納の受取</span><span class="sxs-lookup"><span data-stu-id="e0747-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e0747-104">分納は、返品注文の出荷ではなく返品注文明細行に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="e0747-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="e0747-105">つまり、返品注文内の 1 つの返品注文明細行に示された全数量が入荷し、他の明細行の全数量が入荷しない場合は、分納ではありません。</span><span class="sxs-lookup"><span data-stu-id="e0747-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="e0747-106">これに対して、たとえば、1 つの返品注文明細行にある品目を 10 単位返品するよう指定されているのに 4 単位だけ入荷した場合は、分納です。</span><span class="sxs-lookup"><span data-stu-id="e0747-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="e0747-107">返品荷物の数量が返品注文明細行の全数量より少ない場合、残りの返品数量が入荷するまでそのまま待機することも、部分的な数量を登録および転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0747-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="e0747-108">部分的な数量の登録と転記</span><span class="sxs-lookup"><span data-stu-id="e0747-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="e0747-109">着荷の返品注文を選択した後に、**着荷の概要 - 倉庫: %1、ドック: %2、仕訳帳名: %3**フォームで、**着荷開始**をクリックして着荷仕訳帳を作成し、**仕訳帳** \> **入庫の着荷の表示**をクリックして**在庫場所仕訳帳**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0747-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="e0747-110">操作する仕訳帳明細行を選択し、**明細行**をクリックして**仕訳帳明細行、場所**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0747-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="e0747-111">一部の数量だけが着荷した品目番号の明細行を選択し、**機能** \> **分割**の順にクリックして**分割**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0747-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="e0747-112">**分割数量**フィールドに、入荷済の品目の合計数量を入力し、**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0747-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="e0747-113">**仕訳帳明細行、場所**フォームで、着荷した品目の数量を示す明細行を選択し、**転記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0747-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="e0747-114">品目が着荷したら、追加数量を示す明細行を転記できます。</span><span class="sxs-lookup"><span data-stu-id="e0747-114">You can post the line for the additional quantity after the items have arrived.</span></span>





