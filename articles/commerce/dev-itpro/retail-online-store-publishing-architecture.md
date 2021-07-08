---
title: オンライン ストア チャネルの公開
description: このトピックには、Commerce モジュールからオンライン ストアにカタログを公開する方法を理解するための概念に関する情報が含まれています。
author: mugunthanm
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: AX 10.0.10
ms.openlocfilehash: ee634cccea13ce4bfc5f1b432f2f9b537116b686
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186628"
---
# <a name="publish-an-online-store-channel"></a><span data-ttu-id="806f1-103">オンライン ストア チャネルの公開</span><span class="sxs-lookup"><span data-stu-id="806f1-103">Publish an online store channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="806f1-104">このトピックには、Commerce モジュールからオンライン ストアにカタログを公開する方法を理解するための概念に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="806f1-104">This topic contains conceptual information to understand how catalogs are published from the Commerce module to an online store.</span></span>

## <a name="publish-an-online-store-channel"></a><span data-ttu-id="806f1-105">オンライン ストア チャネルの公開</span><span class="sxs-lookup"><span data-stu-id="806f1-105">Publish an online store channel</span></span>

<span data-ttu-id="806f1-106">Commerce オンライン店舗チャネルを公開するとき、Microsoft Dynamics 365 Commerce と SharePoint 間でオンライン ストアの基本構造をレプリケートします。</span><span class="sxs-lookup"><span data-stu-id="806f1-106">When you publish a Commerce online store channel, you replicate the basic structure of your online store between Microsoft Dynamics 365 Commerce and Microsoft SharePoint.</span></span> <span data-ttu-id="806f1-107">**コマース** モジュールでオンライン ストア チャネルの基本構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-107">You create the basic structure of your online store channel in the **Commerce** module.</span></span> <span data-ttu-id="806f1-108">オンライン ストア チャネルを公開する前に、以下の設定タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="806f1-108">Before you can publish an online store channel, you must complete the following setup tasks:</span></span>

1. <span data-ttu-id="806f1-109">組織階層にオンライン ストアを追加します。</span><span class="sxs-lookup"><span data-stu-id="806f1-109">Add the online store to the organization hierarchy.</span></span>
2. <span data-ttu-id="806f1-110">オンライン ストアを作成し、プロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="806f1-110">Create the online store and configure properties.</span></span>
3. <span data-ttu-id="806f1-111">サイトのカテゴリ階層をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="806f1-111">Configure the category hierarchy of your site.</span></span>

<span data-ttu-id="806f1-112">これらの手順を完了した後は、オンライン ストアに製品スキーマを公開する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="806f1-112">After you've completed these steps, you're ready to publish the product schema to the online store.</span></span>

1. <span data-ttu-id="806f1-113">**オンライン ストア** ページからオンライン ストアを作成して公開します。</span><span class="sxs-lookup"><span data-stu-id="806f1-113">You create the online store and publish it from the **Online stores** page.</span></span> <span data-ttu-id="806f1-114">状態は、**ドラフト** から **処理中** に変更されました。</span><span class="sxs-lookup"><span data-stu-id="806f1-114">The status is changed from **Draft** to **In progress**.</span></span>
2. <span data-ttu-id="806f1-115">Finances and Operations は、カテゴリ階層 (コマース階層) およびプロパティのスナップショットを取得します。</span><span class="sxs-lookup"><span data-stu-id="806f1-115">Finances and Operations takes a snapshot of the category hierarchies (the Commerce hierarchy) and properties.</span></span>
3. <span data-ttu-id="806f1-116">Commerce Data Exchange: Async Server はコマース店舗データベース内のオンライン ストア、階層、およびプロパティについての情報を読み取り、Commerce Runtime (CRT) に情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="806f1-116">Commerce Data Exchange: Async Server reads information about the online store, hierarchies, and properties in the Commerce store database, and sends that information to the commerce runtime (CRT).</span></span>
4. <span data-ttu-id="806f1-117">Async Server はチャネル データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="806f1-117">Async Server synchronizes the tables in the channel database.</span></span>
5. <span data-ttu-id="806f1-118">コマース公開ジョブは、CRT アプリケーション プログラミング インターフェイス (API) から実行され、オンライン ストアで作成したサイトの階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-118">The Commerce publishing job runs from the CRT application programming interface (API) and creates hierarchies for the site that you created in the online store.</span></span>
6. <span data-ttu-id="806f1-119">Commerce Data Exchange: Real-time Service は、CRT API から公開ジョブ アクションの状態を受け取り、状態を公開します。</span><span class="sxs-lookup"><span data-stu-id="806f1-119">Commerce Data Exchange: Real-time Service receives the status of the publishing job actions from the CRT API and publishes that status.</span></span> <span data-ttu-id="806f1-120">状態は、**公開済** または **エラー** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="806f1-120">The status is either **Published** or **Error**.</span></span>

<span data-ttu-id="806f1-121">チャンネルを公開する特定の手順については、[オンライン ストアの設定](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="806f1-121">For the specific procedures to publish a channel, see [Set up an online store](/dynamicsax-2012/appuser-itpro/set-up-an-online-store).</span></span> <span data-ttu-id="806f1-122">チャンネルを公開した後は、カタログを公開できます。</span><span class="sxs-lookup"><span data-stu-id="806f1-122">After you've published the channel, you can publish a catalog.</span></span>

## <a name="publish-an-online-store-catalog"></a><span data-ttu-id="806f1-123">オンライン ストア カタログの公開</span><span class="sxs-lookup"><span data-stu-id="806f1-123">Publish an online store catalog</span></span>

<span data-ttu-id="806f1-124">製品カタログを使用すると、オンライン ストアで提供する製品を識別できます。</span><span class="sxs-lookup"><span data-stu-id="806f1-124">A product catalog lets you identify the products that you want to offer in your online stores.</span></span> <span data-ttu-id="806f1-125">カタログを作成するときは、製品が提供されるオンライン ストアを識別し、製品を追加し、販売促進の詳細の追加によって製品の提供を強化します。</span><span class="sxs-lookup"><span data-stu-id="806f1-125">When you create a catalog, you identify the online stores where the products will be offered, add products, and enhance the product offerings by adding merchandising details.</span></span> <span data-ttu-id="806f1-126">カタログが承認された後、オンライン ストアで製品を使用できるようにカタログを公開します。</span><span class="sxs-lookup"><span data-stu-id="806f1-126">After the catalog is approved, you publish it to make products available in the online store.</span></span> <span data-ttu-id="806f1-127">製品カタログを発行する前に、以下の設定タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="806f1-127">Before you can publish a product catalog, you must complete the following setup tasks:</span></span>

1. <span data-ttu-id="806f1-128">製品を設定し、階層、品揃え、およびバリアントを構成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-128">Set up products, and configure hierarchies, assortments, and variants.</span></span>
2. <span data-ttu-id="806f1-129">製品カタログを設定し、属性グループおよびワークフローを構成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-129">Set up product catalogs, and configure attribute groups and workflow.</span></span>

<span data-ttu-id="806f1-130">これらの手順を完了した後は、オンライン ストア カタログを公開する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="806f1-130">After you've completed these steps, you're ready to publish the online store catalog.</span></span>

1. <span data-ttu-id="806f1-131">Finances and Operations は、コマース データベース内の製品テーブルを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="806f1-131">Finances and Operations reads the product tables in the Commerce database.</span></span>
2. <span data-ttu-id="806f1-132">Async Server はチャネル データベースのすべての製品を同期します。</span><span class="sxs-lookup"><span data-stu-id="806f1-132">Async Server synchronizes all products in the channel database.</span></span>
3. <span data-ttu-id="806f1-133">CRT/パブリッシュ コネクターは、*一覧* を作成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-133">The CRT/Publishing Connector creates a *listing*.</span></span> <span data-ttu-id="806f1-134">一覧は、特定の時点におけるチャネルの製品のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="806f1-134">A listing is an instance of a product for a channel at a given point in time.</span></span> <span data-ttu-id="806f1-135">たとえば、「ジーンズ」という名前の製品があり、この製品には「赤」という名前のバリアントがあります。</span><span class="sxs-lookup"><span data-stu-id="806f1-135">For example, you have a product that is named “jeans”, and this product has a variant that is named “red”.</span></span> <span data-ttu-id="806f1-136">この場合、システムは「赤いジーンズ」の一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="806f1-136">In this case, the system creates a listing for “red jeans”.</span></span>
4. <span data-ttu-id="806f1-137">システムは、リスティングに新しい属性が追加されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="806f1-137">The system determines whether any new attributes were added for the listing.</span></span> <span data-ttu-id="806f1-138">新しい属性が追加された場合 (例えば 「赤いジーンズ」 リストに **テクスチャ** という名前の新しい属性が含まれ、この属性がチャネル レベルで **組み込まれている** とマークされている場合)、システムにはこの属性のカスタム サイト内の列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="806f1-138">If a new attribute were added (for example, if the “red jeans” listing includes a new attribute that is named **texture**, and this attribute is marked as **Included** at the channel level), the system creates a custom site column for that attribute.</span></span> <span data-ttu-id="806f1-139">また、リスト アイテムの新しいルールが作成され、「赤いジーンズ」リストの新しい行が作成され、SharePoint でプロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="806f1-139">The system also creates a new rule for the list item and completes the process in SharePoint by creating a new row for the “red jeans” listing.</span></span>
5. <span data-ttu-id="806f1-140">CRT では、一覧の公開状況を記録します。</span><span class="sxs-lookup"><span data-stu-id="806f1-140">The CRT records the publishing status for the listing.</span></span>
6. <span data-ttu-id="806f1-141">Async Server は、一覧の公開ステータスを他のすべての公開ステータスと同期します。</span><span class="sxs-lookup"><span data-stu-id="806f1-141">Async Server synchronizes the publishing status of the listing with all other publishing statuses.</span></span> <span data-ttu-id="806f1-142">状態は、**公開済** または **エラー** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="806f1-142">The status is either **Published** or **Error**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
