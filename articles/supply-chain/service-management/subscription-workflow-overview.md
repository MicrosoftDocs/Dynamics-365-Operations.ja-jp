---
title: 定期売買ワークフローの概要
description: このトピックでは、定期売買ワークフローの概要を示します。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05111ab53e8bf19bb25869155284cdc9d6ea3b2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242280"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="e15a2-103">定期売買ワークフローの概要</span><span class="sxs-lookup"><span data-stu-id="e15a2-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e15a2-104">自分が照明法人の定期売買管理者で、法人が照明装置メンテナンスの定期売買を提供しているとします。</span><span class="sxs-lookup"><span data-stu-id="e15a2-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="e15a2-105">また、顧客が会社に連絡して照明装置メンテナンスの年間定期売買を購入するとします。</span><span class="sxs-lookup"><span data-stu-id="e15a2-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="e15a2-106">定期売買の設定</span><span class="sxs-lookup"><span data-stu-id="e15a2-106">Setting up subscriptions</span></span>

<span data-ttu-id="e15a2-107">定期売買を設定するには、まず新しいサービス合意の定期売買グループを作成するか、定期売買グループが存在することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e15a2-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="e15a2-108">定期売買グループが存在する場合は、1 年を通して顧客に請求を行い、販売収益を毎月見越計上するように定期売買グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e15a2-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="e15a2-109">定期売買の設定方法の詳細については、「[定期売買グループの設定](set-up-subscription-groups.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="e15a2-110">定期売買グループを作成したら、定期売買を作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e15a2-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="e15a2-111">サービスの定期売買を作成する方法の詳細については、[定期売買グループからのサービスの定期売買の作成](create-service-subscriptions-from-subscription-group.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="e15a2-112">定期売買トランザクションの作成および変更</span><span class="sxs-lookup"><span data-stu-id="e15a2-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="e15a2-113">定期売買を設定したら、最初の請求期間 (1 年間) の定期売買手数料トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e15a2-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="e15a2-114">トランザクションのタイプは **通常** です。</span><span class="sxs-lookup"><span data-stu-id="e15a2-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="e15a2-115">したがって、作成できる定期売買トランザクションは、**期間タイプ** フォームで事前に作成した期間に対応する開始日と終了日を持つトランザクションに限られます。</span><span class="sxs-lookup"><span data-stu-id="e15a2-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="e15a2-116">手数料トランザクションの詳細については、[定期売買手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="e15a2-117">顧客に対して定期売買を設定したら、すべての表示価格から 10 パーセント値引きしてサービスを提供するという交渉が成立したことを考慮します。</span><span class="sxs-lookup"><span data-stu-id="e15a2-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="e15a2-118">したがって、作成したトランザクション手数料の価格を下方修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e15a2-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="e15a2-119">その日のうちに顧客から電話があり、照明装置のサービス合意を求めてはいるものの、年内に新しい照明装置を導入する予定との連絡を受けました。</span><span class="sxs-lookup"><span data-stu-id="e15a2-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="e15a2-120">したがって、必要なメンテナンス対象期間は 2013 年 10 月までのみであることがわかりました。</span><span class="sxs-lookup"><span data-stu-id="e15a2-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="e15a2-121">顧客の定期売買の月数を下方修正するには、タイプが **下方修正日数** である新しい定期売買手数料トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e15a2-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="e15a2-122">日数を下方修正する方法の詳細については、[定期売買手数料の日数の引き下げ](reduce-the-days-on-subscription-fees.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="e15a2-123">定期売買トランザクションの請求および見越計上</span><span class="sxs-lookup"><span data-stu-id="e15a2-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="e15a2-124">定期売買の設定が完了し、顧客に対して定期売買の請求を行う準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="e15a2-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="e15a2-125">定期売買の請求方法の詳細については、「[定期売買トランザクションの請求](invoice-subscription-transactions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="e15a2-126">2 日後に顧客から電話があり、定期売買をユーロではなく米ドルで請求するように依頼されました。</span><span class="sxs-lookup"><span data-stu-id="e15a2-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="e15a2-127">このため、訂正票に加えて、正しい通貨で新しい定期売買トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e15a2-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="e15a2-128">定期売買トランザクションの貸方への記入方法の詳細については、「[定期売買トランザクションの貸方記入](credit-subscription-transactions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="e15a2-129">毎月月末に、顧客の定期売買からの 1 か月分の収益を損益勘定および仕掛品勘定に見越計上します。</span><span class="sxs-lookup"><span data-stu-id="e15a2-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="e15a2-130">定期売買の収益を見越計上方法の詳細については、[未収の定期売買収益](accrue-subscription-revenue.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e15a2-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]