---
title: 収益認識の概要
description: このトピックでは、収益認識機能に関する情報を提供します。 この機能により、複数要素注文の収益価格と収益スケジュールの両方を認識するための会社固有のルールを定義できる、柔軟なフレームワークが提供されます。
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: edc0bab7287e271f1d1197d87a95709599e12b5b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820548"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="1b7a6-104">収益認識の概要</span><span class="sxs-lookup"><span data-stu-id="1b7a6-104">Revenue recognition overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b7a6-105">製品、サービス、サブスクリプションなどの複数の要素を販売する業界の会社では、一連の会社固有および業界固有のガイドラインに基づいて収益を認識できるように、複数要素注文を細分化できる能力が求められます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-105">Companies in industries that sell multiple elements, such as products, services, subscriptions, and so on, must be able to break out multi-element orders so that revenue can be recognized based on a set of company-specific and industry-specific guidelines.</span></span>

> [!NOTE]
> <span data-ttu-id="1b7a6-106">収益認識機能は、機能管理を使用して有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-106">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="1b7a6-107">現時点では、コンフィギュレーション キーを使用して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-107">Currently, you must use configuration keys to turn it on.</span></span>

> <span data-ttu-id="1b7a6-108">バンドル機能を含む収益認識は、Commerce チャネル (eコマース、POS、コール センター) での使用はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-108">Revenue recognition, including bundle functionality, isn't supported for use in Commerce channels (e-commerce, POS, call center).</span></span> <span data-ttu-id="1b7a6-109">収益認識で構成された品目は、Commerce チャネルで作成された注文やトランザクションに追加できません。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-109">Items configured with revenue recognition should not be added to orders or transactions created in Commerce channels.</span></span>

<span data-ttu-id="1b7a6-110">一般に、収益認識プロセスは、次のタスクを実行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-110">In general, the revenue recognition process can be used to perform these tasks:</span></span>

* <span data-ttu-id="1b7a6-111">複数要素注文のコンポーネントの価値に基づいて適切な収益価格が確実に認識されるように、収益を配賦します。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-111">Allocate revenue, to help ensure that the appropriate revenue price is recognized, based on the value of the components on multi-element orders.</span></span>
* <span data-ttu-id="1b7a6-112">時間の経過と共に収益を認識するための契約期間と割合を表す収益スケジュールに基づいて、収益を繰り延べます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-112">Defer revenue, based on a revenue schedule that represents the contractual time frame and percentages for recognizing revenue over time.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

<span data-ttu-id="1b7a6-113">上記の [Dynamics 365 Finance で収益認識を使用する方法](https://youtu.be/v3amIsiqvoo) ビデオは、YouTube で視聴できる [Finance and Operations のプレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-113">The [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

<span data-ttu-id="1b7a6-114">収益認識機能、収益価格と収益スケジュールの両方を認識するための会社固有のルールを定義できる、柔軟なフレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-114">The Revenue recognition feature provides a flexible framework that lets you define company-specific rules for recognizing both the revenue price and the revenue schedule.</span></span>

<span data-ttu-id="1b7a6-115">リリース済製品は、販売注文ドキュメントの収益認識をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-115">Released products are used to support revenue recognition on sales order documents.</span></span> <span data-ttu-id="1b7a6-116">リリース済製品には、収益価格と収益スケジュールを決定するために必要な設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-116">The released products contain the setup that is required to determine the revenue price and the revenue schedule.</span></span> <span data-ttu-id="1b7a6-117">販売注文は、時間および実費払プロジェクトから作成することができます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-117">The sales order can originate from a Time and materials project.</span></span>

<span data-ttu-id="1b7a6-118">会社は、収益価格機能を使用せずに収益スケジュール機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-118">Companies can use the revenue schedule functionality without using the revenue price functionality.</span></span> <span data-ttu-id="1b7a6-119">したがって、販売注文明細行の価格は、収益または繰延収益のどちらかとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-119">Therefore, the price on the sales order lines will be used as either revenue or deferred revenue.</span></span> <span data-ttu-id="1b7a6-120">収益スケジュールが販売注文明細行に存在する場合は、その販売注文明細行の価格が繰り延べられます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-120">If a revenue schedule exists on the sales order line, the price on the sales order line will be deferred.</span></span> <span data-ttu-id="1b7a6-121">収益スケジュールが販売注文明細行に存在しない場合は、請求時に販売注文明細行の価格が収益勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-121">If a revenue schedule doesn't exist on the sales order line, the price on the sales order line will be posted to a revenue account when it's invoiced.</span></span>

<span data-ttu-id="1b7a6-122">収益価格は、販売注文が確認されたとき、または請求書が転記されたときに計算されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-122">The revenue price is calculated either when the sales order is confirmed or when the invoice is posted.</span></span> <span data-ttu-id="1b7a6-123">請求書が転記される前の収益価格をプレビューするには、販売注文を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-123">To preview the revenue price before the invoice is posted, you must confirm the sales order.</span></span>

<span data-ttu-id="1b7a6-124">販売注文が確認されると、販売注文明細行に収益スケジュールがある場合に、予定収益スケジュールも作成されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-124">When the sales order is confirmed, an expected revenue schedule is also created if any sales order line has a revenue schedule.</span></span> <span data-ttu-id="1b7a6-125">販売注文が請求されると、予定収益スケジュールは削除され、予定収益スケジュールは実際の収益認識スケジュールに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-125">When the sales order is invoiced, the expected revenue schedule is deleted, and the expected revenue schedule is replaced with the actual revenue recognition schedule.</span></span>

<span data-ttu-id="1b7a6-126">収益認識スケジュールの詳細は、販売注文明細行ごとに管理されます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-126">The details of the revenue recognition schedule are maintained for each sales order line.</span></span> <span data-ttu-id="1b7a6-127">したがって、収益認識マネージャーは、詳細を表示し、契約上の責務が完了した時点で明細行を収益にリリースできます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-127">Therefore, the revenue recognition manager can view the details and can release lines to revenue when the contractual obligation has been completed.</span></span> <span data-ttu-id="1b7a6-128">各期間の終了時に、収益認識マネージャーは収益仕訳帳を作成して、設定した日付またはそれ以前にスケジュール明細行をリリースできます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-128">At the end of each period, the revenue recognition manager can create a revenue journal to release any schedule lines that are due on or before a date they define.</span></span> <span data-ttu-id="1b7a6-129">この収益仕訳帳はすぐには転記されません。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-129">This revenue journal isn't posted immediately.</span></span> <span data-ttu-id="1b7a6-130">したがって、収益認識マネージャーは、正しい金額が繰延収益から実際の収益にリリースされているかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-130">Therefore, the revenue recognition manager can verify that the correct amounts are being released from deferred revenue to actual revenue.</span></span>

<span data-ttu-id="1b7a6-131">契約の変更により、新しい販売注文明細行が既存の販売注文または新しい販売注文に追加されるようになった場合は、再配賦プロセスを実行して、販売注文のすべての明細行の収益価格を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="1b7a6-131">If a contractual change causes a new sales order line to be added either to the existing sales order or a new sales order, a reallocation process can be run to correct the revenue price across all lines on the sales orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]