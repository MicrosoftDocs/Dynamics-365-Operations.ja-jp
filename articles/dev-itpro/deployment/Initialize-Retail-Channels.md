---
title: クラウドでホストされている Retail チャネル コンポーネントの初期化
description: このトピックでは、クラウドでホストされている Retail チャネル コンポーネントの初期化方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 12/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 797706f1411d1608919ee5060d65abd199707d36
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369315"
---
# <a name="initialize-cloud-hosted-retail-channel-components"></a><span data-ttu-id="ce77d-103">クラウドでホストされている Retail チャネル コンポーネントの初期化</span><span class="sxs-lookup"><span data-stu-id="ce77d-103">Initialize cloud-hosted Retail channel components</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce77d-104">アプリケーション バージョン 8.1.2.x 以降を持つレベル 2 サンドボックスまたは運用環境を使用している場合、販売時点管理 (POS) 操作またはクラウド内の Retail サーバーを使用する電子商取引操作に Retail チャネル機能を使用する前に、クラウドにホストされている Retail チャネル コンポーネントを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce77d-104">If you're using a Tier-2 sandbox or production environment that has application version 8.1.2.x or later, you must initialize Retail channel components that are hosted in the cloud before you can use Retail channel functionality either for point of sale (POS) operations or for e-Commerce operations that use Retail Server in the cloud.</span></span>

<span data-ttu-id="ce77d-105">このトピックでは、クラウドでホストされている Retail チャネル コンポーネントを初期化するための手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-105">This topic describes the steps for initializing cloud-hosted Retail channel components.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ce77d-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="ce77d-106">Prerequisites</span></span>

1. <span data-ttu-id="ce77d-107">アプリケーション バージョン 8.1.2.x またはそれ以降を持つレベル 2 サンドボックスまたは運協環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-107">Deploy a Tier-2 sandbox or production environment that has application version 8.1.2.x or later.</span></span>
2. <span data-ttu-id="ce77d-108">Microsoft Dynamics Lifecycle Services (LCS) で、サポート リクエストを作成し、**クラウドでホストされている Retail チャネル コンポーネントのアクセス権の要求**と入力します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-108">In Microsoft Dynamics Lifecycle Services (LCS), create a support request, and enter **Access request for cloud-hosted Retail channel components**.</span></span>

<span data-ttu-id="ce77d-109">要求は、5 営業日以内に完了されます。</span><span class="sxs-lookup"><span data-stu-id="ce77d-109">The request will be completed within five business days.</span></span>

## <a name="initialize-cloud-hosted-retail-channel-components-as-part-of-a-new-environment-deployment"></a><span data-ttu-id="ce77d-110">新しい環境の展開の一部としてクラウドでホストされている Retail チャネル コンポーネントを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-110">Initialize cloud-hosted Retail channel components as part of a new environment deployment</span></span>

1. <span data-ttu-id="ce77d-111">LCS の環境の詳細 ページで、**環境機能 \> Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-111">In LCS, on the environment details page, select **Environment features \> Retail**.</span></span>
2. <span data-ttu-id="ce77d-112">Retail 設定配置ページで、**初期化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-112">On the Retail setup deployment page, select **Initialize**.</span></span>
3. <span data-ttu-id="ce77d-113">初期化する Retail チャネル コンポーネントのバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-113">Select the version of the Retail channel components to initialize.</span></span>

## <a name="additional-considerations-if-you-initialize-cloud-hosted-retail-channel-components-in-an-existing-environment"></a><span data-ttu-id="ce77d-114">既存の環境でクラウドにホストされた Retail チャネル コンポーネントを初期化する場合の追加の考慮事項</span><span class="sxs-lookup"><span data-stu-id="ce77d-114">Additional considerations if you initialize cloud-hosted Retail channel components in an existing environment</span></span>

<span data-ttu-id="ce77d-115">環境でクラウドでホストされている Retail チャネル コンポーネントを既に使用している場合、初期化はそれらのコンポーネントの更新時にダウンタイムを減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ce77d-115">If you're already using cloud-hosted Retail channel components in an environment, initialization will help reduce the downtime when those components are updated.</span></span> <span data-ttu-id="ce77d-116">初期化を行う前に、追加の計画が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce77d-116">Additional planning is required before you do the initialization.</span></span>

1. <span data-ttu-id="ce77d-117">POS のすべてのシフトがクローズしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ce77d-117">Make sure that all shifts at the POS are closed.</span></span>
2. <span data-ttu-id="ce77d-118">すべての P ジョブが正常に完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-118">Make sure that all P-jobs have been successfully completed.</span></span>
3. <span data-ttu-id="ce77d-119">すべての POS デバイスからサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="ce77d-119">Sign out of all POS devices.</span></span>

<span data-ttu-id="ce77d-120">Retail サーバーに依存する店舗およびオンライン チャネルのすべての工程で、5 時間のダウンタイム ウィンドウを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce77d-120">You should plan for a five-hour downtime window for the store and any online channel operations that depend on Retail Server.</span></span>

<span data-ttu-id="ce77d-121">初期化期間中に実行される内容を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-121">Here is what occurs during the initialization period:</span></span>

- <span data-ttu-id="ce77d-122">クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能がオンの場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="ce77d-122">Cloud-hosted Retail channels won't work (unless POS offline capability is turned on).</span></span>
- <span data-ttu-id="ce77d-123">オフライン機能がオンになっている POS デバイスは機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="ce77d-123">POS devices that offline capability is turned on for will have reduced functionality.</span></span>
- <span data-ttu-id="ce77d-124">Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="ce77d-124">Any e-Commerce clients that depend on Retail Server will be disrupted.</span></span>
- <span data-ttu-id="ce77d-125">Retail Store Scale Unit でホストされているチャネルは影響されません。</span><span class="sxs-lookup"><span data-stu-id="ce77d-125">Channels that are hosted on Retail Store Scale Units won't be affected.</span></span>
- <span data-ttu-id="ce77d-126">本社機能は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="ce77d-126">Head office functionality won't be affected.</span></span>

<span data-ttu-id="ce77d-127">初期化が完了した後に起きる事柄を示します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-127">Here is what occurs after initialization is completed:</span></span>

- <span data-ttu-id="ce77d-128">アクティブ化されたすべての POS デバイスのデバイス有効化状態は保持されます。</span><span class="sxs-lookup"><span data-stu-id="ce77d-128">The device activation state of all activated POS devices will be preserved.</span></span> <span data-ttu-id="ce77d-129">したがって、デバイスを再度有効化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ce77d-129">Therefore, the devices won't have to be reactivated.</span></span>
- <span data-ttu-id="ce77d-130">スタンドアロン ハードウェア ステーション インスタンスは引き続き機能します。</span><span class="sxs-lookup"><span data-stu-id="ce77d-130">Stand-alone hardware station instances will continue to work.</span></span>
- <span data-ttu-id="ce77d-131">POS チャンネル側のレポートはリセットされ、データを初期化する前に表示されません。</span><span class="sxs-lookup"><span data-stu-id="ce77d-131">POS channel–side reports will be reset and won't show data from before the initialization.</span></span>
