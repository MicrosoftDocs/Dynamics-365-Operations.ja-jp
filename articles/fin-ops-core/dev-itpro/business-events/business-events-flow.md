---
title: Microsoft Flow 内のビジネス イベント
description: このトピックでは、アプリケーション コネクタを介して Microsoft Flow で使用可能となるビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 529b6d32f33b6b235c451e9f0dd33ffe8d85b4f3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183445"
---
# <a name="business-events-in-microsoft-flow"></a><span data-ttu-id="dabc7-103">Microsoft Flow 内のビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="dabc7-103">Business events in Microsoft Flow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dabc7-104">ビジネス イベントは アプリケーション コネクタを介して Microsoft Flow で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-104">Business events can be consumed in Microsoft Flow via the application connector.</span></span> <span data-ttu-id="dabc7-105">コネクタには**ビジネス イベントの発生時**という名前のトリガーがあります。</span><span class="sxs-lookup"><span data-stu-id="dabc7-105">The connector has a trigger that is named **when a business event occurs**.</span></span> <span data-ttu-id="dabc7-106">このトリガーは、アプリケーションのターゲット インスタンスで使用可能なビジネス イベントの購読に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-106">This trigger can be used to subscribe to any of the business events that are available in the target instance of the application.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="dabc7-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="dabc7-107">Prerequisite</span></span>

<span data-ttu-id="dabc7-108">ビジネス イベントについて理解することは重要です。</span><span class="sxs-lookup"><span data-stu-id="dabc7-108">It's important that you understand business events.</span></span> <span data-ttu-id="dabc7-109">詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dabc7-109">For more information, see the [Business events](home-page.md) documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dabc7-110">ビジネス イベントは以前のプラットフォーム リリースでは使用可能でないため、**ビジネス イベント発生時**トリガーは、Platform update 24 またはそれ以降を実行するアプリケーション インスタンスでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="dabc7-110">The **when a business event happens** trigger works only with application instances that run Platform update 24 or later, because business events aren't available in earlier platform releases.</span></span>

## <a name="subscribing-to-business-events-and-unsubscribing-from-them"></a><span data-ttu-id="dabc7-111">ビジネス イベントの購読および購読解除</span><span class="sxs-lookup"><span data-stu-id="dabc7-111">Subscribing to business events and unsubscribing from them</span></span>

<span data-ttu-id="dabc7-112">**ビジネス イベント発生時** トリガーをフローに追加した後、以下の情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dabc7-112">After the **when a business event happens** trigger is added to a flow, the following information must be provided:</span></span>

- <span data-ttu-id="dabc7-113">**インスタンス** – ビジネス イベントが発生するインスタンスのホスト名を指定します。</span><span class="sxs-lookup"><span data-stu-id="dabc7-113">**Instance** – Specify the host name of the instance where business events occur.</span></span> <span data-ttu-id="dabc7-114">環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-114">Environment instances should be available in the provided drop-down menu, but if an environment is not listed it can be entered as a custom value.</span></span>
- <span data-ttu-id="dabc7-115">**カテゴリ** - ビジネス イベントのカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="dabc7-115">**Category** – Select the category of business events.</span></span> <span data-ttu-id="dabc7-116">**ビジネス イベント** フィールドにそのカテゴリのビジネス イベントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-116">The **Business event** field then shows the business events in that category.</span></span>
- <span data-ttu-id="dabc7-117">**ビジネス イベント** - 選択したカテゴリで利用可能なビジネス イベント。</span><span class="sxs-lookup"><span data-stu-id="dabc7-117">**Business event** – The available business events in the selected category.</span></span>
- <span data-ttu-id="dabc7-118">**法人** - ビジネス イベントが購読されている法人を指定します。</span><span class="sxs-lookup"><span data-stu-id="dabc7-118">**Legal entity** – Specify the legal entity where the business event is being subscribed to.</span></span> <span data-ttu-id="dabc7-119">フローは法人でビジネス イベントが発生するときにトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-119">The flow will be triggered when the business event occurs in that legal entity.</span></span> <span data-ttu-id="dabc7-120">既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-120">By default, this field is blank and the business event is subscribed to in **all** legal entities.</span></span>

<span data-ttu-id="dabc7-121">フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-121">When the flow is saved, a subscription to the selected business event is added into the environment instance.</span></span> <span data-ttu-id="dabc7-122">サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-122">As part of the subscription process, the required endpoint is set up, and the corresponding business event is activated.</span></span>

<span data-ttu-id="dabc7-123">トリガーまたはフローのいずれかを削除または無効化すると、ビジネス イベントは自動的に購読解除されます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-123">If either the trigger or the flow is deleted or disabled, the business event is automatically unsubscribed from.</span></span>

<span data-ttu-id="dabc7-124">複数のフローは、同一もしくは異なる法人内の同じビジネス イベントを購読することができます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-124">Multiple flows can subscribe to the same business event in different legal entities or in the same legal entity.</span></span>

> [!NOTE]
> <span data-ttu-id="dabc7-125">Flow エンドポイントは、手動でコンフィギュレーションすることはできません。</span><span class="sxs-lookup"><span data-stu-id="dabc7-125">The Flow endpoint must not be configured manually.</span></span> <span data-ttu-id="dabc7-126">上記の説明に従って、エンドポイントはフローから自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-126">The endpoint will automatically get created from Flow as explained above.</span></span>

<span data-ttu-id="dabc7-127">Microsoft Flow でビジネス イベントを使用する方法については [Microsoft Flow でビジネス イベントを消費する](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/how-to/how-to-flow) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dabc7-127">For how-to information about using business events in Microsoft Flow, see [Consume business events in Microsoft Flow](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/how-to/how-to-flow).</span></span> 

## <a name="other-ways-to-consume-business-events-in-microsoft-flow"></a><span data-ttu-id="dabc7-128">Microsoft Flow 内のビジネス イベントを消費する他の方法</span><span class="sxs-lookup"><span data-stu-id="dabc7-128">Other ways to consume business events in Microsoft Flow</span></span>

<span data-ttu-id="dabc7-129">前のセクションでは、コネクタ内でトリガーを使用することにより Microsoft Flow から直接ビジネス イベントを購読する方法について説明しました。</span><span class="sxs-lookup"><span data-stu-id="dabc7-129">The previous section explains how you can subscribe to business events directly from Microsoft Flow by using the trigger in the connector.</span></span> <span data-ttu-id="dabc7-130">ただし、[Microsoft Flow 用イベント グリッド コネクタ](https://docs.microsoft.com/connectors/azureeventgrid/) を使用することにより、Microsoft Azure Event Grid から Microsoft Flow 内のビジネス イベントを消費することもできます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-130">However, you can also consume business events in Microsoft Flow from Microsoft Azure Event Grid, by using the [Event Grid connector for Microsoft Flow](https://docs.microsoft.com/connectors/azureeventgrid/).</span></span>

<span data-ttu-id="dabc7-131">実装内の他の統合で既に使用されている場合、イベント グリッドは Microsoft Flow 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="dabc7-131">Event Grid might be a viable approach for consuming business events in Microsoft Flow if it's already being used for other integrations in an implementation.</span></span> <span data-ttu-id="dabc7-132">同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dabc7-132">If a business event in the same legal entity must trigger multiple flows, you should consider consuming the business event from Event Grid.</span></span>

<span data-ttu-id="dabc7-133">このアプローチは、コネクタが Microsoft Flow 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。</span><span class="sxs-lookup"><span data-stu-id="dabc7-133">This approach is applicable to any messaging or event platform that is used as an endpoint for business events, provided that a connector is available for it in Microsoft Flow.</span></span>
