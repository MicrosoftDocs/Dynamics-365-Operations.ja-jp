---
title: Microsoft Flow 内のビジネス イベント
description: このトピックでは、Finance and Operations コネクタを介して Microsoft Flow での消費に使用可能なビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 01/29/2019
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
ms.openlocfilehash: 40545536f5ea8b2cea601eb430af60dac0a852ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369513"
---
# <a name="business-events-in-microsoft-flow"></a><span data-ttu-id="d44ce-103">Microsoft Flow 内のビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="d44ce-103">Business events in Microsoft Flow</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="d44ce-104">ビジネス イベントは Microsoft Finance and Operations コネクタを介して Microsoft Flow で消費することができます。 </span><span class="sxs-lookup"><span data-stu-id="d44ce-104">Business events can be consumed in Microsoft Flow via the Microsoft Finance and Operations connector.</span></span> <span data-ttu-id="d44ce-105">Finance and Operations コネクタには **ビジネス イベントの発生時** という名前のトリガーがあります。</span><span class="sxs-lookup"><span data-stu-id="d44ce-105">The Finance and Operations connector has a trigger that is named **when a business event happens**.</span></span> <span data-ttu-id="d44ce-106">このトリガーは、Microsoft Dynamics 365 for Finance and Operations のターゲット インスタンスで使用可能なビジネス イベントの購読に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-106">This trigger can be used to subscribe to any of the business events that are available in the target instance of Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="d44ce-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="d44ce-107">Prerequisite</span></span>

<span data-ttu-id="d44ce-108">ビジネス イベントについて理解することは重要です。</span><span class="sxs-lookup"><span data-stu-id="d44ce-108">It's important that you understand business events.</span></span> <span data-ttu-id="d44ce-109">詳細については[ビジネス イベント](home-page.md) のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d44ce-109">For more information, see the [Business events](home-page.md) documentation.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="d44ce-110">Microsoft Flow 用 Finance and Operations コネクタはプレビュー中です。</span><span class="sxs-lookup"><span data-stu-id="d44ce-110">The Finance and Operations connector for Microsoft Flow is in preview.</span></span>
> - <span data-ttu-id="d44ce-111">ビジネス イベントは以前のプラットフォーム リリースでは使用可能でないため、**ビジネス イベント発生時** トリガーは、Platform update 24 またはそれ以降を実行する Finance and Operations インスタンスでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="d44ce-111">The **when a business event happens** trigger works only with Finance and Operations instances that run Platform update 24 or later, because business events aren't available in earlier platform releases.</span></span>

## <a name="subscribing-to-business-events-and-unsubscribing-from-them"></a><span data-ttu-id="d44ce-112">ビジネス イベントの購読および購読解除</span><span class="sxs-lookup"><span data-stu-id="d44ce-112">Subscribing to business events and unsubscribing from them</span></span>

<span data-ttu-id="d44ce-113">**ビジネス イベント発生時** トリガーをフローに追加した後、以下の情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d44ce-113">After the **when a business event happens** trigger is added to a flow, the following information must be provided:</span></span>

- <span data-ttu-id="d44ce-114">**インスタンス** - ビジネス イベントが発生する Finance and Operations インスタンスのホスト名を指定します。</span><span class="sxs-lookup"><span data-stu-id="d44ce-114">**Instance** – Specify the host name of the Finance and Operations instance where business events occur.</span></span> <span data-ttu-id="d44ce-115">環境インスタンスは指定されたドロップダウン メニューで利用可能である必要がありますが、環境が一覧表示されていない場合はカスタム値として入力することができます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-115">Environment instances should be available in the provided drop-down menu, but if an environment is not listed it can be entered as a custom value.</span></span>
- <span data-ttu-id="d44ce-116">**カテゴリ** - ビジネス イベントのカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="d44ce-116">**Category** – Select the category of business events.</span></span> <span data-ttu-id="d44ce-117">**ビジネス イベント** フィールドにそのカテゴリのビジネス イベントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-117">The **Business event** field then shows the business events in that category.</span></span>
- <span data-ttu-id="d44ce-118">**ビジネス イベント** - 選択したカテゴリで利用可能なビジネス イベント。</span><span class="sxs-lookup"><span data-stu-id="d44ce-118">**Business event** – The available business events in the selected category.</span></span>
- <span data-ttu-id="d44ce-119">**法人** - ビジネス イベントが購読されている法人を指定します。</span><span class="sxs-lookup"><span data-stu-id="d44ce-119">**Legal entity** – Specify the legal entity where the business event is being subscribed to.</span></span> <span data-ttu-id="d44ce-120">フローは Finance and Operations 内の法人でビジネス イベントが発生するときにトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-120">The flow will be triggered when the business event occurs in that legal entity in Finance and Operations.</span></span> <span data-ttu-id="d44ce-121">既定では、このフィールドは空白で、ビジネス イベントは **すべて** の法人で購読されます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-121">By default, this field is blank and the business event is subscribed to in **all** legal entities.</span></span>

<span data-ttu-id="d44ce-122">フローが保存されると、選択したビジネス イベントに対するサブスクリプションが環境インスタンスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-122">When the flow is saved, a subscription to the selected business event is added into the environment instance.</span></span> <span data-ttu-id="d44ce-123">サブスクリプション プロセスの一部として、必要なエンドポイントが設定され、対応するビジネス イベントが有効にされます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-123">As part of the subscription process, the required endpoint is set up, and the corresponding business event is activated.</span></span>

<span data-ttu-id="d44ce-124">トリガーまたはフローのいずれかが削除されると、ビジネス イベントは自動的に購読解除されます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-124">If either the trigger or the flow is deleted, the business event is automatically unsubscribed from.</span></span>

<span data-ttu-id="d44ce-125">複数のフローが、異なる法人内の同じビジネス イベントを購読することができます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-125">Multiple flows can subscribe to the same business event in different legal entities.</span></span>

## <a name="other-ways-to-consume-business-events-in-microsoft-flow"></a><span data-ttu-id="d44ce-126">Microsoft Flow 内のビジネス イベントを消費する他の方法</span><span class="sxs-lookup"><span data-stu-id="d44ce-126">Other ways to consume business events in Microsoft Flow</span></span>

<span data-ttu-id="d44ce-127">前のセクションでは、Finance and Operations 内でトリガーを使用することにより Microsoft Flow から直接ビジネス イベントを購読する方法について説明しました。</span><span class="sxs-lookup"><span data-stu-id="d44ce-127">The previous section explains how you can subscribe to business events directly from Microsoft Flow by using the trigger in the Finance and Operations connector.</span></span> <span data-ttu-id="d44ce-128">ただし、[Microsoft Flow 用イベント グリッド コネクタ](https://docs.microsoft.com/connectors/azureeventgrid/) を使用することにより、Microsoft Azure Event Grid から Microsoft Flow 内のビジネス イベントを消費することもできます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-128">However, you can also consume business events in Microsoft Flow from Microsoft Azure Event Grid, by using the [Event Grid connector for Microsoft Flow](https://docs.microsoft.com/connectors/azureeventgrid/).</span></span>

<span data-ttu-id="d44ce-129">実装内の他の統合で既に使用されている場合、イベント グリッドは Microsoft Flow 内のビジネス イベントを消費するための実行可能なアプローチである可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d44ce-129">Event Grid might be a viable approach for consuming business events in Microsoft Flow if it's already being used for other integrations in an implementation.</span></span> <span data-ttu-id="d44ce-130">同じ法人内のビジネス イベントが複数のフローをトリガする必要がある場合、イベント グリッドからビジネス イベントを消費することを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d44ce-130">If a business event in the same legal entity must trigger multiple flows, you should consider consuming the business event from Event Grid.</span></span>

<span data-ttu-id="d44ce-131">このアプローチは、コネクタが Microsoft Flow 内のビジネス イベントで使用可能である場合、ビジネス イベントのエンドポイントとして使用されるメッセージングまたはイベント プラットフォームに対して適用することができます。</span><span class="sxs-lookup"><span data-stu-id="d44ce-131">This approach is applicable to any messaging or event platform that is used as an endpoint for business events, provided that a connector is available for it in Microsoft Flow.</span></span>
