---
title: "返品注文に対する交換のコンフィギュレーションとプロセス"
description: "このトピックでは、Microsoft Dynamics 365 for Retail で返品に対する交換のコンフィギュレーションを行う方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="6440a-103">返品注文に対する交換のコンフィギュレーションとプロセス</span><span class="sxs-lookup"><span data-stu-id="6440a-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6440a-104">以前のバージョンの Microsoft Dynamics 365 for Retail では、小売用バックオフィスで返品注文ドキュメントを使用することにより、顧客注文に対する返品が処理されていました。</span><span class="sxs-lookup"><span data-stu-id="6440a-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail headquarters.</span></span> <span data-ttu-id="6440a-105">ただし、返品注文ドキュメントを使用できるのは、返品されている製品の処理のみです。</span><span class="sxs-lookup"><span data-stu-id="6440a-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="6440a-106">返品された製品は、返品注文明細行の数量が負の数になっていることでわかります。</span><span class="sxs-lookup"><span data-stu-id="6440a-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="6440a-107">これに対して、売上は、数量が正の数になっています。</span><span class="sxs-lookup"><span data-stu-id="6440a-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="6440a-108">ただし、返品注文ドキュメントでは、負の数量はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6440a-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="6440a-109">この制限があるため、以前のバージョンの Retail では、返品注文ドキュメントを使用して製品の交換を行うシナリオはサポートされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="6440a-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="6440a-110">しかし、返品注文で交換を行うシナリオをサポートする機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="6440a-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="6440a-111">現在の Retail では、返品注文ドキュメントではなく、販売注文ドキュメントを使用してこれらのタイプのトランザクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="6440a-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="6440a-112">返品注文での交換をサポートするように Retail を構成する</span><span class="sxs-lookup"><span data-stu-id="6440a-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="6440a-113">返品注文での交換をサポートするようにシステムを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6440a-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="6440a-114">**[小売] \> [本社の設定] \> [パラメーター] \> [小売パラメーター]** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6440a-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="6440a-115">**顧客注文** クイック タブで、**返品注文を販売注文として処理する** オプションで **はい** を設定します。</span><span class="sxs-lookup"><span data-stu-id="6440a-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="6440a-116">**グローバル構成配送スケジュール** ジョブ (**1110**) を実行します。</span><span class="sxs-lookup"><span data-stu-id="6440a-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="6440a-117">交換を行う</span><span class="sxs-lookup"><span data-stu-id="6440a-117">Make an exchange</span></span>

<span data-ttu-id="6440a-118">前のセクションの記載に従ってシステムを構成した後、販売時点管理 (POS) のユーザーは、販売注文または販売請求書を選択して返品の処理を行います。これは、以前のバージョンの Retail と同様です。</span><span class="sxs-lookup"><span data-stu-id="6440a-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="6440a-119">ただし、返品品目がカートに追加された後、ユーザーは新しい販売明細行をカートに追加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6440a-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="6440a-120">これらの新しい販売明細行については、顧客注文明細行を処理するために必要なすべての属性をユーザーが定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6440a-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="6440a-121">これらの属性には、配送方法やフルフィルメント場所が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6440a-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="6440a-122">取引に対する支払額は、返品注文明細行と販売注文明細行の正味金額になります。</span><span class="sxs-lookup"><span data-stu-id="6440a-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="6440a-123">取引に対して支払が行われると、小売用バックオフィスで、返品注文が販売注文ドキュメントとして転記され、システムにより即座に返品明細行の請求処理が行われます。</span><span class="sxs-lookup"><span data-stu-id="6440a-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="6440a-124">カートのさまざまな金額をわかりやすくするため、新しく 3 つの金額フィールドがカートに追加されています。</span><span class="sxs-lookup"><span data-stu-id="6440a-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="6440a-125">画面デザイナーを使用することで、これらの新しいフィールドを POS のユーザー インターフェイス (UI) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6440a-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="6440a-126">**充当済預金** – ユーザーが顧客注文の集荷を行う場合に、取引に適用される預金額です。</span><span class="sxs-lookup"><span data-stu-id="6440a-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="6440a-127">預金の上書きがなく、10% の預金率が構成されている場合、このフィールドの金額は、顧客注文の合計額の 90% になります。</span><span class="sxs-lookup"><span data-stu-id="6440a-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="6440a-128">**金額の実行** – 顧客注文の作成時または編集時、あるいは顧客注文の交換中に、配送モードが **実行** に設定されていた明細行の合計額です。</span><span class="sxs-lookup"><span data-stu-id="6440a-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="6440a-129">このフィールドの金額には、税金および諸費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6440a-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="6440a-130">**返品金額** – 顧客注文の交換中の数量が負の値の明細行の合計金額です。</span><span class="sxs-lookup"><span data-stu-id="6440a-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="6440a-131">このフィールドの金額には、税金および諸費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6440a-131">The amount in this field includes taxes and charges.</span></span>

