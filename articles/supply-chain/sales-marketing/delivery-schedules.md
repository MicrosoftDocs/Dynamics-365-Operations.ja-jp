---
title: 配送スケジュール
description: 配送スケジュールより、1 つの販売注文、販売見積、または発注書に複数の配送を使用するときに、注文明細行数量を追跡することができます。
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d77468a02379fefa105ba21376c7f3a7be337819
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210057"
---
# <a name="delivery-schedules"></a><span data-ttu-id="34773-103">配送スケジュール</span><span class="sxs-lookup"><span data-stu-id="34773-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34773-104">配送スケジュールより、1 つの販売注文、販売見積、または発注書に複数の配送を使用するときに、注文明細行数量を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="34773-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="34773-105">注文または見積の明細行の合計数量を複数の出荷で配送する必要がある場合に、配送スケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="34773-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="34773-106">個々の出荷は、配送明細行で表示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="34773-107">複数の配送明細行は、1 つの配送スケジュールを構成します。</span><span class="sxs-lookup"><span data-stu-id="34773-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="34773-108">配送明細行が配送日、数量、配送配送のモード、および保管分析コード (サイトおよび倉庫などの) で異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34773-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="34773-109">**配送スケジュールの例**</span><span class="sxs-lookup"><span data-stu-id="34773-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="34773-110">注文合計 (元の注文明細行)</span><span class="sxs-lookup"><span data-stu-id="34773-110">Total order (original order line)</span></span> | <span data-ttu-id="34773-111">600 脚の椅子</span><span class="sxs-lookup"><span data-stu-id="34773-111">600 chairs</span></span>                               |
| <span data-ttu-id="34773-112">要求された配送スケジュール</span><span class="sxs-lookup"><span data-stu-id="34773-112">Requested delivery schedule</span></span>       | <span data-ttu-id="34773-113">1 か月ごとに 100 脚の椅子</span><span class="sxs-lookup"><span data-stu-id="34773-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="34773-114">要求された配送の期間</span><span class="sxs-lookup"><span data-stu-id="34773-114">Requested time frame for delivery</span></span> | <span data-ttu-id="34773-115">6 か月、各月の初日</span><span class="sxs-lookup"><span data-stu-id="34773-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="34773-116">このシナリオでは、顧客は 6 か月の期間にわたって 100 脚の椅子をバッチにして 600 脚の椅子を配送するように要求しています。</span><span class="sxs-lookup"><span data-stu-id="34773-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="34773-117">引き渡し要件を追跡するには、配送スケジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="34773-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="34773-118">配送スケジュール ページで、6 通の配送明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="34773-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="34773-119">各配送明細行が 100 脚の椅子を含み、それらの 100 脚の椅子の配送日を表示します。</span><span class="sxs-lookup"><span data-stu-id="34773-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="34773-120">この場合、各行は 6 か月の連続した月の初日で相殺されます。</span><span class="sxs-lookup"><span data-stu-id="34773-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="34773-121">配送スケジュールを作成すると、元の注文明細行のタイプが自動的に**複数の配送を含む発注明細行**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="34773-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="34773-122">このタイプの行は、業務行として参照され、アイコンで示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="34773-123">配送明細行には、別のアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="34773-124">配送明細行の数量を変更すると、業務行は配送スケジュールの合計数量に更新されます。</span><span class="sxs-lookup"><span data-stu-id="34773-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="34773-125">売買契約が注文の割引合計を定義している場合、配送スケジュールを使用すると、オーダーが別の出荷に分割される場合でも、合計注文割引の適用対象となるようにします。</span><span class="sxs-lookup"><span data-stu-id="34773-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="34773-126">配送スケジュールがある注文は、出荷明細行に対して処理されます。</span><span class="sxs-lookup"><span data-stu-id="34773-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="34773-127">処理には、梱包明細、製品受領書、および請求の転記が含まれます。</span><span class="sxs-lookup"><span data-stu-id="34773-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="34773-128">配送スケジュールのある注文と見積の印刷文書には、配送明細行のみが記載されます。</span><span class="sxs-lookup"><span data-stu-id="34773-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="34773-129">これらには、元の明細行 (業務行) は記載されません。</span><span class="sxs-lookup"><span data-stu-id="34773-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="34773-130">**注記:** また、次のアクションの実行時には、配送明細行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="34773-131">転記</span><span class="sxs-lookup"><span data-stu-id="34773-131">Post</span></span>
-   <span data-ttu-id="34773-132">ページのコピー</span><span class="sxs-lookup"><span data-stu-id="34773-132">Copy pages</span></span>
-   <span data-ttu-id="34773-133">リスト ページおよびレポートの表示</span><span class="sxs-lookup"><span data-stu-id="34773-133">Browse list pages and reports</span></span>

<span data-ttu-id="34773-134">販売見積を確認すると、結果の販売注文には、複数の配送を含む注文明細行でも配送スケジュール全体が表示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="34773-135">また、全体の配送スケジュールは、販売注文、販売見積、発注書などのすべての主要なページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="34773-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>



