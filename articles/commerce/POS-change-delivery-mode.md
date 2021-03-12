---
title: POS の荷渡方法の変更
description: このトピックでは、POS の荷渡方法の変更操作のコンフィギュレーション方法および使用方法について説明します。
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6bfe27a7b4a768da00c67e307a0bd7e57b333d11
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965430"
---
# <a name="change-mode-of-delivery-in-pos"></a><span data-ttu-id="6622e-103">POS の荷渡方法の変更</span><span class="sxs-lookup"><span data-stu-id="6622e-103">Change mode of delivery in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6622e-104">このトピックでは、販売時点管理 (POS) の「荷渡方法の変更」機能の設定方法および使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6622e-104">This topic describes how to set up and use the "change mode of delivery" functionality in your point of sale (POS) environment.</span></span> 

<span data-ttu-id="6622e-105">Dynamics 365 Commerce バージョン 10.0.10 以降では、POS 画面レイアウトへの **荷渡方法の変更** 操作 (647) の追加が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6622e-105">In Dynamics 365 Commerce versions 10.0.10 and later, the **Change mode of delivery** operation (647) is available to add to your POS screen layouts.</span></span>

<span data-ttu-id="6622e-106">荷渡方法の変更機能により、POS トランザクションで 1 つ以上の出荷コンフィギュレーションの販売明細行に対して、荷渡方法を変更するオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="6622e-106">The change mode of delivery feature provides you with the option to change the mode of delivery for one or more shipment-configured sales lines on the POS transaction.</span></span> <span data-ttu-id="6622e-107">以前のバージョンの Commerce では、出荷用にコンフィギュレーションされた既存の明細行の荷渡方法を変更する場合、**すべて出荷** または **選択された出荷** のコンフィギュレーション フロー全体を使用する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="6622e-107">In previous versions of Commerce, you had to go through the full **Ship all** or **Ship selected** configuration flows if you wanted to change the mode of delivery on an existing line that was configured for shipment.</span></span> <span data-ttu-id="6622e-108">この処理には時間がかかり、明細行の配送元または配送日が誤って変更される可能性がありました。</span><span class="sxs-lookup"><span data-stu-id="6622e-108">This process was time consuming and could result in accidental changes to the delivery origin or delivery dates for the line.</span></span> <span data-ttu-id="6622e-109">この新しい機能により、これら販売明細行の荷渡方法を効率的に更新する代替方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="6622e-109">The new functionality provides an alternative method for efficiently updating the mode of delivery on these sales lines.</span></span>

<span data-ttu-id="6622e-110">POS ボタン グリッドのボタンに操作を追加する方法の詳細については、[販売時点管理の画面レイアウト](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6622e-110">For more information about how to add an operation to a button on your POS button grid, see [Screen layouts for the point of sale](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).</span></span>

<span data-ttu-id="6622e-111">POS でこの機能がコンフィギュレーションされた後、**荷渡方法の変更** を選択すると、荷渡方法を変更するトランザクションの明細行を選択できる一覧のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6622e-111">After this feature is configured in POS, when you select **Change mode of delivery**, you will be presented with a list page that allows you to choose the lines of the transaction that you want to change the mode of delivery for.</span></span> <span data-ttu-id="6622e-112">明細行の一部またはすべてを選択するか、または何も変更せずに終了することができます。</span><span class="sxs-lookup"><span data-stu-id="6622e-112">You can choose some or all of the lines, or exit without making any changes.</span></span> <span data-ttu-id="6622e-113">変更可能なリストの明細行は、以前に出荷用にコンフィギュレーションされた販売明細行のみです。</span><span class="sxs-lookup"><span data-stu-id="6622e-113">The sales lines that were previously configured for shipment are the only lines in the list that you can change.</span></span> <span data-ttu-id="6622e-114">集荷または Carryout に指定された明細行を変更する場合、**すべて出荷** または **選択された出荷** 操作を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6622e-114">If you want to change a line designated for pickup or carryout to ship, you must use the **Ship all** or **Ship selected** operations.</span></span> <span data-ttu-id="6622e-115">逆に、出荷として指定された明細行を集荷または Carryout に変更する場合、**すべて集荷**、**選択された集荷**、**すべて Carryout**、または **選択された Carryout** 操作を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6622e-115">Conversely, if you want to change a line designated as a shipment to a pickup or carryout, you must use the  **Pickup all**, **Pickup selected**, **Carryout all**, or **Carryout selected** operations.</span></span>

<span data-ttu-id="6622e-116">変更する明細行を選択した後、**荷渡方法の変更** をクリックすると、荷渡方法のオプションの選択を求められます。</span><span class="sxs-lookup"><span data-stu-id="6622e-116">After you select the lines that you want to change, click **Change mode of delivery** to be prompted to select the delivery mode options.</span></span> <span data-ttu-id="6622e-117">変更する明細行を複数選択した場合、POS は、選択した製品すべてが許容できるようにコンフィギュレーションされた荷渡方法のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6622e-117">If you selected multiple lines to change, POS will only display modes of delivery that have been configured as allowable for all of the selected products.</span></span> <span data-ttu-id="6622e-118">荷渡方法をコンフィギュレーションして、特定の製品および配送先住所をサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="6622e-118">Modes of delivery can be configured to support specific products and delivery addresses.</span></span> <span data-ttu-id="6622e-119">ある製品と住所の組み合わせには受け入れられる荷渡方法が、選択した別の製品と住所の組み合わせでは受け入れられない場合、その荷渡方法は使用できません。</span><span class="sxs-lookup"><span data-stu-id="6622e-119">If there is a mode of delivery that is acceptable for one product and address combination but is not acceptable for another selected product and address combination, the mode of delivery is not available.</span></span> <span data-ttu-id="6622e-120">ある製品に別の製品でサポートされていない荷渡方法を選択する場合、各明細行に対して別々に 1 つずつ荷渡方法を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6622e-120">You may need to select lines one by one and change the mode of delivery for each line separately if you want to select a mode of delivery for one product that is not supported by another product.</span></span>  

<span data-ttu-id="6622e-121">新しい荷渡方法を選択した後、トランザクション ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6622e-121">After you select the new mode of delivery, the transaction page is displayed.</span></span> <span data-ttu-id="6622e-122">新しい荷渡方法の選択を確認するには、トランザクション リストの **荷渡** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6622e-122">To review your new delivery mode selections, select the **Delivery** tab on the transaction list.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6622e-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6622e-123">Additional resources</span></span>

[<span data-ttu-id="6622e-124">コール センター注文の作成</span><span class="sxs-lookup"><span data-stu-id="6622e-124">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="6622e-125">配送モードによるトランザクション メールのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="6622e-125">Customize transactional emails by mode of delivery</span></span>](customize-email-delivery-mode.md)
