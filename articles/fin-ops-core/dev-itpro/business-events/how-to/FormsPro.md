---
title: ビジネスイベントと Microsoft Forms Pro
description: このトピックでは、製品の出荷時に調査がユーザーに送信されるシナリオについて説明します。
author: murrayfife
ms.date: 08/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: mufife
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 7358fd3dc3010cabed6499a7850c1d92de5f39c8
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5940914"
---
# <a name="business-events-and-microsoft-forms-pro"></a><span data-ttu-id="2f69c-103">ビジネス イベントおよび Microsoft Forms Pro</span><span class="sxs-lookup"><span data-stu-id="2f69c-103">Business events and Microsoft Forms Pro</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="2f69c-104">このトピックでは、Microsoft Forms Pro を使用してビジネス イベントで使用できる調査を作成するシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-104">This topic goes through a scenario where Microsoft Forms Pro is used to create a survey that can be used with business events.</span></span> <span data-ttu-id="2f69c-105">特にここで説明するシナリオでは製品が出荷されたときに調査が顧客に送信されます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-105">Specifically, in the scenario that is described here, a survey is sent to customers when a product has been shipped.</span></span> <span data-ttu-id="2f69c-106">調査情報は Forms Pro を使用して収集されます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-106">The survey information is gathered by using Forms Pro.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f69c-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="2f69c-107">Prerequisites</span></span>

<span data-ttu-id="2f69c-108">Forms Pro を使用したことがない場合は、まず [Forms Pro のドキュメント](/forms-pro/) を読んで使用方法を学習します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-108">If you haven't used Forms Pro before, you should first read the [Forms Pro documentation](/forms-pro/) to learn how to use it.</span></span>

## <a name="scenario"></a><span data-ttu-id="2f69c-109">シナリオ</span><span class="sxs-lookup"><span data-stu-id="2f69c-109">Scenario</span></span>

1. <span data-ttu-id="2f69c-110">調査の作成</span><span class="sxs-lookup"><span data-stu-id="2f69c-110">Create a survey.</span></span> <span data-ttu-id="2f69c-111">調査に入力したタイトルに基づいて Forms Pro はアンケートの質問を提案します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-111">Based on the title that you enter for the survey, Forms Pro suggests survey questions.</span></span>

    ![Forms Pro が提案する調査の質問](../../media/Forms_Pro1.png)

2. <span data-ttu-id="2f69c-113">販売注文は出荷を追跡します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-113">The sales order tracks the shipment.</span></span> <span data-ttu-id="2f69c-114">製品が出荷されると、販売注文のステータスが **配送済** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-114">When the product has been shipped, the status of the sales order is changed to **Delivered**.</span></span>

    ![ステータスが「配送済」の販売注文](../../media/SalesOrder1.png)

    <span data-ttu-id="2f69c-116">そのため、**ステータス** フィールドの値が変更されるたびにアラートを作成するように、販売注文でアラートを構成します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-116">Therefore, configure an alert on the sales order, so that an alert is created whenever the value of the **Status** field is changed.</span></span> <span data-ttu-id="2f69c-117">アラートがビジネス イベントとして送信されるように、必ず **外部に送信** オプションを **はい** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="2f69c-117">Be sure to set the **Send externally** option to **Yes**, so that the alert will be sent out as a business event.</span></span>

    ![警告](../../media/Alerts1.png)

3. <span data-ttu-id="2f69c-119">販売注文のステータスが更新されるたびにビジネス イベントにトリガーされるフローを設定します (次のステップの図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="2f69c-119">Set up the flow that will be triggered by the business event whenever the status of the sales order is updated (see the illustration in the next step).</span></span> <span data-ttu-id="2f69c-120">トリガーされた後、フローはフォーム コネクタを使用して、販売注文に登録されている顧客の電子メール アドレスに調査を送信します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-120">After it's triggered, the flow will use the Forms connector to send the survey to the customer email address that is registered on the sales order.</span></span>

    <span data-ttu-id="2f69c-121">シナリオに必要な顧客の電子メール アドレスとその他の情報は、ビジネス イベント ペイロードに含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f69c-121">The customer email address and other information that is required for the scenario must be in the payload of the business event.</span></span> <span data-ttu-id="2f69c-122">ペイロードにこのデータがない場合は、適切なフィールドが含まれるように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-122">If the payload doesn't have this data, it can be extended so that it includes the appropriate fields.</span></span> <span data-ttu-id="2f69c-123">詳細については [ビジネス イベント開発者ドキュメント](../business-events-dev-doc.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f69c-123">For more information, see the [Business events developer documentation](../business-events-dev-doc.md).</span></span>

4. <span data-ttu-id="2f69c-124">このシナリオの調整には Microsoft Power Automate が使用されるため、アプリケーションで **変更ベースのアラートが発生した場合** ビジネス イベントを有効化しないでください。</span><span class="sxs-lookup"><span data-stu-id="2f69c-124">Because Microsoft Power Automate is used to orchestrate this scenario, don't activate the **When a change based alert occurs** business event in the application.</span></span> <span data-ttu-id="2f69c-125">代わりに、ビジネス イベントを直接サブスクライブするように Power Automate を設定します。</span><span class="sxs-lookup"><span data-stu-id="2f69c-125">Instead, set up Power Automate so that it subscribes directly to the business event.</span></span>

    ![Flow](../../media/Flow1.png)

5. <span data-ttu-id="2f69c-127">フローは設定が完了するとトリガーされ、販売注文のステータスが更新されるたびに調査が送信されます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-127">After you've finished setting up the flow, it will be triggered and send out the survey whenever the sales order's status is updated.</span></span>

    ![調査](../../media/Survey1.png)

    <span data-ttu-id="2f69c-129">ユーザーが調査に入力して送信すると Forms Pro に分析が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f69c-129">As users fill in the survey and submit it, Forms Pro shows some analytics.</span></span>

    ![Forms Pro の調査分析](../../media/Forms_Pro2.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
