---
title: POS で顧客注文集荷を処理する
description: このトピックでは、顧客注文の集荷を処理するための POS アプリケーションで使用できる機能について説明します。
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003756"
---
# <a name="process-customer-order-pickups-in-pos"></a><span data-ttu-id="ecb2e-103">POS で顧客注文集荷を処理する</span><span class="sxs-lookup"><span data-stu-id="ecb2e-103">Process customer order pickups in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ecb2e-104">店舗ピックアップの[顧客注文](customer-orders-overview.md)が作成されると、店舗ユーザーは販売時点管理 (POS) アプリケーションを使用して在庫の集荷を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-104">When a [customer order](customer-orders-overview.md) is created for store pickup, a store user can use the point of sale (POS) application to start the pickup of inventory.</span></span> <span data-ttu-id="ecb2e-105">POS は必要に応じて最終的な支払いのキャプチャを実行します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-105">POS will run the final payment capture as required.</span></span> <span data-ttu-id="ecb2e-106">また、集荷された数量の在庫と財務転記も完了します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-106">It will also complete the inventory and financial posting for the quantities that are picked up.</span></span>

<span data-ttu-id="ecb2e-107">店舗のユーザーは、POSの **注文の取り消し** 操作または **注文の実行** 操作を使用して集荷を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-107">If you're a store user, you can perform the pickup by using either the **Recall order** operation or the **Order fulfillment** operation in POS.</span></span> <span data-ttu-id="ecb2e-108">**集荷** 操作を利用できるようにするには、まず以下のいずれかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-108">To make the **Pick up** operation available, you must first follow one of these steps:</span></span>

- <span data-ttu-id="ecb2e-109">**注文の取り消し** 操作を使用するには、対象の注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-109">To use the **Recall order** operation, search for and select the order that will be picked up.</span></span>
- <span data-ttu-id="ecb2e-110">**注文の実行** 操作を使用するには、1つ以上の注文明細行を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-110">To use the **Order fulfillment** operation, search for and select one or more order lines.</span></span>

<span data-ttu-id="ecb2e-111">選択された注文または注文明細行が、特定の店舗で集荷するように構成されていない場合、または注文がすでに完全に集荷されている場合、**集荷** 操作は利用できません。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-111">If the selected order or order lines aren't configured for pickup at that specific store, or if the order has already been fully picked up, the **Pick up** operation will be unavailable.</span></span>

![集荷の操作](media/pickupoperation.png)

<span data-ttu-id="ecb2e-113">Microsoft Dynamics 365 Commerce バージョン 10.0.17 とそれ以降では、**販売時点管理機能での集荷注文処理のユーザー エクスペリエンスを向上させる** 機能を 、Commerce 本部の機能管理を使用して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-113">In Microsoft Dynamics 365 Commerce version 10.0.17 and later, the **Improved user experience for pick up order processing in Point of Sale** feature can be turned on through Feature management in Commerce headquarters.</span></span> <span data-ttu-id="ecb2e-114">この機能をオフにすると、ユーザーは集荷数量を選択できません。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-114">If this feature is turned off, users can't select pickup quantities.</span></span> <span data-ttu-id="ecb2e-115">既定では、明細行で注文された完全な数量が集荷される数量となります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-115">By default, the full quantity that was ordered for the line is the quantity that will be picked up.</span></span> <span data-ttu-id="ecb2e-116">ユーザーが注文処理を介して集荷を実行する際に、集荷に必要な項目の選択を忘れてしまう可能性があるため、問題となる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-116">This experience can be problematic, because users might forget to select some items for pickup when they perform the pickup through order fulfillment.</span></span>

<span data-ttu-id="ecb2e-117">**販売時点管理機能での集荷注文処理のユーザー エクスペリエンスを向上させる** 機能により、集荷される商品の選択と、集荷される商品の数量をよりコントロールできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-117">The **Improved user experience for pick up order processing in Point of Sale** feature gives users more control over the selection of products that will be picked up and the quantity of those products that will be picked up.</span></span> <span data-ttu-id="ecb2e-118">顧客が **集荷** を選択する前に、注文の実行ページで販売注文のすべての行を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-118">Users don't have to select every line of the sales order on the order fulfillment page before they select **Pick up**.</span></span> <span data-ttu-id="ecb2e-119">選択可能なすべての品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-119">All the items that can be picked up will be shown.</span></span> <span data-ttu-id="ecb2e-120">1つの製品明細行が選択されている場合でも、集荷には複数の明細行を指定できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-120">Users can specify multiple lines for pickup even if only one product line is selected.</span></span>

<span data-ttu-id="ecb2e-121">**販売時点管理機能での集荷注文処理のユーザー エクスペリエンスを向上させる** 機能が有効になっている場合で、**集荷** 操作を選択すると、**集荷** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-121">When the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, and you select the **Pick up** operation, the **Pick up** dialog box appears.</span></span> <span data-ttu-id="ecb2e-122">このフィールドでは、集荷する品目と数量を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-122">There, you can select the items and quantities that will be picked up.</span></span> <span data-ttu-id="ecb2e-123">既定では、選択した状態または梱包済み状態の在庫がある注文済数量は、集荷に適格であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-123">By default, any ordered quantity that has inventory in a picked or packed state is considered eligible for pickup.</span></span> <span data-ttu-id="ecb2e-124">既定では、この数量は集荷数量として設定されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-124">By default, that quantity is set as the pickup quantity.</span></span> <span data-ttu-id="ecb2e-125">数量が 0 (ゼロ) で、選択した行のオープン数量 (請求されていない) の合計数量を超えの場合は、入力した数量を変更できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-125">You can change the quantity that was entered, provided that the quantity isn't 0 (zero) and doesn't exceed the total open (that is, non-invoiced) quantity for the selected line.</span></span>

![集荷ダイアログ ボックス](media/pickupselect.png)

<span data-ttu-id="ecb2e-127">集荷する数量を選択し、**集荷** を選択 すると、トランザクション ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-127">After you select the quantities that will be picked up and then select **Pick up**, the transaction page appears.</span></span> <span data-ttu-id="ecb2e-128">[オムニチャネル支払](omni-channel-payments.md)機能が有効になっており、ファイルにクレジット カードで事前に承認された支払がある場合は、支払を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-128">If the [omni-channel payments](omni-channel-payments.md) feature is turned on, and there are pre-authorized credit card payments on file, you must apply the payment.</span></span>

<span data-ttu-id="ecb2e-129">トランザクションページでは、選択された集荷品目の支払期限の合計を計算し、以前に適用された預金または承認されたクレジットカードの支払いを差し引くことで、システムは支払期限の金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-129">On the transaction page, the system calculates the amounts that are due by calculating the total that is due for the selected pickup items and then subtracting any previously applied deposits or authorized credit card payments.</span></span> <span data-ttu-id="ecb2e-130">集荷トランザクションを完了するには、支払を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-130">You must process payment to complete the pickup transaction.</span></span> <span data-ttu-id="ecb2e-131">トランザクション ページの [画面レイアウト](pos-screen-layouts.md) が **トランザクションの終了** 操作を含み、金額が期限を設定するように構成されている場合、支払方法を選択せずにトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-131">If the [screen layout](pos-screen-layouts.md) of the transaction page is configured so that it includes the **Conclude transaction** operation, and no amount is due, you can complete the transaction without selecting a payment method.</span></span> <span data-ttu-id="ecb2e-132">**トランザクションの終了** 操作を使用できない場合は、**合計** ウィンドウで **$0.00 金額の期日** リンクを選択して、支払方法を選択せずにトランザクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-132">If the **Conclude transaction** operation isn't available, you can select the **$0.00 amount due** link in the **Totals** pane to conclude the transaction without having to select a payment method.</span></span>

![顧客注文の集荷トランザクション ページ](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a><span data-ttu-id="ecb2e-134">集荷明細行または集荷数量の変更</span><span class="sxs-lookup"><span data-stu-id="ecb2e-134">Changing pickup lines or quantities</span></span>

<span data-ttu-id="ecb2e-135">集荷品目を選択した後に集荷数量を変更する必要がある場合は、**数量の設定** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-135">If you must change the pickup quantity after you've selected the items that will be picked up, you can select **Set quantity**.</span></span> <span data-ttu-id="ecb2e-136">集荷数量を **0** (ゼロ)に設定したり、注文注文明細に残る未請求の数量を超える値に増やすことはできません。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-136">You can't set the pickup quantity to **0** (zero) or increase it to a value that exceeds the non-invoiced quantity that remains for the ordered line.</span></span> <span data-ttu-id="ecb2e-137">トランザクション カートから集荷行を削除するには、**トランザクションの無効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-137">To remove a pickup line from the transaction cart, select **Void transaction**.</span></span> <span data-ttu-id="ecb2e-138">現在のトランザクションが停止し、**集荷** 操作のフローが再開されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-138">The current transaction will be stopped, and the flow for the **Pick up** operation will be restarted.</span></span>

<span data-ttu-id="ecb2e-139">**販売時点管理機能での集荷注文処理のユーザー エクスペリエンスを向上させる** 機能が有効になっている場合は、トランザクション ページの画面レイアウトに **集荷明細行** の変更操作用のボタンを追加 できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-139">If the **Improve user experience for pick up order processing in Point of Sale** feature is turned on, organizations can add a button for the **Change pickup lines** operation to the screen layout of the transaction page.</span></span> <span data-ttu-id="ecb2e-140">POS で集荷取引カートを作成し、項目を選択した後、集荷項目を変更する必要があるが、トランザクション全体を無効にしたくない場合は、**集荷行の変更** を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-140">After you create the pickup transaction cart in POS and select items, you can select **Change pickup lines** if you must change the pickup items but don't want to void the whole transaction.</span></span> <span data-ttu-id="ecb2e-141">表示された **集荷行の変更** ダイアログ ボックスで、集荷品目と数量を変更できます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-141">In the **Change pickup lines** dialog box that appears, you can change the pickup items and quantities.</span></span> <span data-ttu-id="ecb2e-142">その後、トランザクション カートが更新され、変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="ecb2e-142">The transaction cart is then updated to reflect your changes.</span></span>

![集荷品目の変更ダイアログ ボックス](media/pickupchange.png)
