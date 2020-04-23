---
title: 返品された製品の着荷仕訳を転記
description: 返品された製品の着荷仕訳を転記します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c96f1499cf9ef93a56a636f990aa5d0d183f9627
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202133"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="2d7c5-103">返品された製品の着荷仕訳を転記</span><span class="sxs-lookup"><span data-stu-id="2d7c5-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2d7c5-104">返品を処理するには、まず返品数量を確認し、着荷仕訳帳の数量フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="2d7c5-105">次に、廃棄コードを選択するか、返品品目の検査が必要であることを示します。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="2d7c5-106">これらの手順を完了したら、返品注文の着荷仕訳帳を転記できます。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="2d7c5-107">**在庫管理** \> **定期処理** \> **着荷の概要**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="2d7c5-108">**設定名**フィルターで、**返品注文**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="2d7c5-109">入庫の一覧が長い場合は、**範囲**領域のフィールドを使用して一覧を絞り込みます。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="2d7c5-110">転記する返品注文の明細行を検索し、**着荷に関する選択**ボックスをオンにして、**着荷開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="2d7c5-111">**仕訳帳** \> **入庫の着荷の表示**をクリックして、**在庫場所仕訳帳**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="2d7c5-112">詳細情報を表示するには、仕訳帳を選択し、<STRONG>明細行</STRONG>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="2d7c5-113">必要な更新を行い、**転記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="2d7c5-114">仕訳帳が転記された後、返品品目は在庫に登録され、品目が倉庫に到着したことが**返品注文**フォームに示されます。</span><span class="sxs-lookup"><span data-stu-id="2d7c5-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d7c5-115">参照</span><span class="sxs-lookup"><span data-stu-id="2d7c5-115">See also</span></span>

<span data-ttu-id="2d7c5-116">[在庫場所仕訳帳 (フォーム)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="2d7c5-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  


