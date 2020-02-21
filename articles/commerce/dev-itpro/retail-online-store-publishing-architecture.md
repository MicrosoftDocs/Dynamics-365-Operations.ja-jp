---
title: オンライン ストア公開アーキテクチャ
description: このトピックには、コマース モジュールから Microsoft SharePoint 2013 製品内のオンライン ストアにチャネルおよびカタログを公開する方法を開発者およびシステム管理者が理解するための概念的情報が含まれています。 発行プロセスを理解することで、オンライン ストアの開発、管理、トラブルシューティングに役立ちます。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 72124
ms.assetid: c9ab2a6c-ea19-4c21-a2d9-35a8d516b48b
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dc71a52ee0cb1208e1b63558f5ec1061918a66d2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004639"
---
# <a name="online-store-publishing-architecture"></a><span data-ttu-id="97f90-104">オンライン ストア公開アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="97f90-104">Online store publishing architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97f90-105">このトピックには、コマース モジュールから Microsoft SharePoint 2013 製品内のオンライン ストアにチャネルおよびカタログを公開する方法を開発者およびシステム管理者が理解するための概念的情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="97f90-105">This topic contains conceptual information to help developers and system administrators understand how channels and catalogs are published from the commerce module to an online store in Microsoft SharePoint 2013 Products.</span></span> <span data-ttu-id="97f90-106">発行プロセスを理解することで、オンライン ストアの開発、管理、トラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="97f90-106">Understanding the publishing process can help you develop, manage, and troubleshoot your online store.</span></span>

<a name="publish-an-online-store-channel"></a><span data-ttu-id="97f90-107">オンライン ストア チャネルの公開</span><span class="sxs-lookup"><span data-stu-id="97f90-107">Publish an online store channel</span></span>
-------------------------------------

<span data-ttu-id="97f90-108">コマース オンライン ストア チャネルを公開するとき、Microsoft Dynamics 365 Commerce と SharePoint 間でオンライン ストアの基本構造をレプリケートします。</span><span class="sxs-lookup"><span data-stu-id="97f90-108">When you publish a Commerce online store channel, you replicate the basic structure of your online store between Microsoft Dynamics 365 Commerce and Microsoft SharePoint.</span></span> <span data-ttu-id="97f90-109">**コマース** モジュールでオンライン ストア チャネルの基本構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-109">You create the basic structure of your online store channel in the **Commerce** module.</span></span> <span data-ttu-id="97f90-110">オンライン ストア チャネルを公開する前に、以下の設定タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97f90-110">Before you can publish an online store channel, you must complete the following setup tasks:</span></span>

1.  <span data-ttu-id="97f90-111">組織階層にオンライン ストアを追加します。</span><span class="sxs-lookup"><span data-stu-id="97f90-111">Add the online store to the organization hierarchy.</span></span>
2.  <span data-ttu-id="97f90-112">オンライン ストアを作成し、プロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="97f90-112">Create the online store and configure properties.</span></span>
3.  <span data-ttu-id="97f90-113">サイトのカテゴリ階層をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="97f90-113">Configure the category hierarchy of your site.</span></span>

<span data-ttu-id="97f90-114">これらの手順を完了した後は、オンライン ストアに製品スキーマを公開する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="97f90-114">After you've completed these steps, you're ready to publish the product schema to the online store.</span></span>

1.  <span data-ttu-id="97f90-115">**オンライン ストア** ページからオンライン ストアを作成して公開します。</span><span class="sxs-lookup"><span data-stu-id="97f90-115">You create the online store and publish it from the **Online stores** page.</span></span> <span data-ttu-id="97f90-116">状態は、**ドラフト** から **処理中** に変更されました。</span><span class="sxs-lookup"><span data-stu-id="97f90-116">The status is changed from **Draft** to **In progress**.</span></span>
2.  <span data-ttu-id="97f90-117">Finances and Operations は、カテゴリ階層 (コマース階層) およびプロパティのスナップショットを取得します。</span><span class="sxs-lookup"><span data-stu-id="97f90-117">Finances and Operations takes a snapshot of the category hierarchies (the Commerce hierarchy) and properties.</span></span>
3.  <span data-ttu-id="97f90-118">Commerce Data Exchange: Async Server はコマース店舗データベース内のオンライン ストア、階層、およびプロパティについての情報を読み取り、Commerce Runtime (CRT) に情報を送信します。</span><span class="sxs-lookup"><span data-stu-id="97f90-118">Commerce Data Exchange: Async Server reads information about the online store, hierarchies, and properties in the Commerce store database, and sends that information to the commerce runtime (CRT).</span></span>
4.  <span data-ttu-id="97f90-119">Async Server はチャネル データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="97f90-119">Async Server synchronizes the tables in the channel database.</span></span>
5.  <span data-ttu-id="97f90-120">コマース公開ジョブは、CRT アプリケーション プログラミング インターフェイス (API) から実行され、オンライン ストアで作成したサイトの階層を作成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-120">The Commerce publishing job runs from the CRT application programming interface (API) and creates hierarchies for the site that you created in the online store.</span></span>
6.  <span data-ttu-id="97f90-121">Commerce Data Exchange: Real-time Service は、CRT API から公開ジョブ アクションの状態を受け取り、状態を公開します。</span><span class="sxs-lookup"><span data-stu-id="97f90-121">Commerce Data Exchange: Real-time Service receives the status of the publishing job actions from the CRT API and publishes that status.</span></span> <span data-ttu-id="97f90-122">状態は、**公開済** または **エラー** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="97f90-122">The status is either **Published** or **Error**.</span></span>

<span data-ttu-id="97f90-123">チャンネルを公開する特定の手順については、[オンライン ストアの設定](https://msdn.microsoft.com/jj682095) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97f90-123">For the specific procedures to publish a channel, see [Set up an online store](https://msdn.microsoft.com/jj682095).</span></span> <span data-ttu-id="97f90-124">チャンネルを公開した後は、カタログを公開できます。</span><span class="sxs-lookup"><span data-stu-id="97f90-124">After you've published the channel, you can publish a catalog.</span></span>

## <a name="publish-an-online-store-catalog"></a><span data-ttu-id="97f90-125">オンライン ストア カタログの公開</span><span class="sxs-lookup"><span data-stu-id="97f90-125">Publish an online store catalog</span></span>
<span data-ttu-id="97f90-126">製品カタログを使用すると、オンライン ストアで提供する製品を識別できます。</span><span class="sxs-lookup"><span data-stu-id="97f90-126">A product catalog lets you identify the products that you want to offer in your online stores.</span></span> <span data-ttu-id="97f90-127">カタログを作成するときは、製品が提供されるオンライン ストアを識別し、製品を追加し、販売促進の詳細の追加によって製品の提供を強化します。</span><span class="sxs-lookup"><span data-stu-id="97f90-127">When you create a catalog, you identify the online stores where the products will be offered, add products, and enhance the product offerings by adding merchandising details.</span></span> <span data-ttu-id="97f90-128">カタログが承認された後、オンライン ストアで製品を使用できるようにカタログを公開します。</span><span class="sxs-lookup"><span data-stu-id="97f90-128">After the catalog is approved, you publish it to make products available in the online store.</span></span> <span data-ttu-id="97f90-129">製品カタログを発行する前に、以下の設定タスクを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97f90-129">Before you can publish a product catalog, you must complete the following setup tasks:</span></span>

1.  <span data-ttu-id="97f90-130">製品を設定し、階層、品揃え、およびバリアントを構成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-130">Set up products, and configure hierarchies, assortments, and variants.</span></span>
2.  <span data-ttu-id="97f90-131">製品カタログを設定し、属性グループおよびワークフローを構成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-131">Set up product catalogs, and configure attribute groups and workflow.</span></span>

<span data-ttu-id="97f90-132">これらの手順を完了した後は、オンライン ストア カタログを公開する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="97f90-132">After you've completed these steps, you're ready to publish the online store catalog.</span></span>

1.  <span data-ttu-id="97f90-133">Finances and Operations は、コマース データベース内の製品テーブルを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="97f90-133">Finances and Operations reads the product tables in the Commerce database.</span></span>
2.  <span data-ttu-id="97f90-134">Async Server はチャネル データベースのすべての製品を同期します。</span><span class="sxs-lookup"><span data-stu-id="97f90-134">Async Server synchronizes all products in the channel database.</span></span>
3.  <span data-ttu-id="97f90-135">CRT/パブリッシュ コネクターは、*一覧*を作成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-135">The CRT/Publishing Connector creates a *listing*.</span></span> <span data-ttu-id="97f90-136">一覧は、特定の時点におけるチャネルの製品のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="97f90-136">A listing is an instance of a product for a channel at a given point in time.</span></span> <span data-ttu-id="97f90-137">たとえば、「ジーンズ」という名前の製品があり、この製品には「赤」という名前のバリアントがあります。</span><span class="sxs-lookup"><span data-stu-id="97f90-137">For example, you have a product that is named “jeans”, and this product has a variant that is named “red”.</span></span> <span data-ttu-id="97f90-138">この場合、システムは「赤いジーンズ」の一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="97f90-138">In this case, the system creates a listing for “red jeans”.</span></span>
4.  <span data-ttu-id="97f90-139">システムは、リスティングに新しい属性が追加されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="97f90-139">The system determines whether any new attributes were added for the listing.</span></span> <span data-ttu-id="97f90-140">新しい属性が追加された場合 (例えば、一覧表示「赤いジーンズ」には、**テクスチャ**という名前の新しい属性が含まれ、この属性がチャンネル レベルで**組み込まれている**とマークされている場合)、システムではカスタム サイト内の列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="97f90-140">If new attribute were added (for example, if the “red jeans” listing includes a new attribute that is named **texture**, and this attribute is marked as **Included** at the channel level), the system creates a custom site column for that attribute.</span></span> <span data-ttu-id="97f90-141">また、リスト アイテムの新しいルールが作成され、「赤いジーンズ」リストの新しい行が作成され、SharePoint でプロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="97f90-141">The system also creates a new rule for the list item and completes the process in SharePoint by creating a new row for the “red jeans” listing.</span></span>
5.  <span data-ttu-id="97f90-142">CRT では、一覧の公開状況を記録します。</span><span class="sxs-lookup"><span data-stu-id="97f90-142">The CRT records the publishing status for the listing.</span></span>
6.  <span data-ttu-id="97f90-143">Async Server は、一覧の公開ステータスを他のすべての公開ステータスと同期します。</span><span class="sxs-lookup"><span data-stu-id="97f90-143">Async Server synchronizes the publishing status of the listing with all other publishing statuses.</span></span> <span data-ttu-id="97f90-144">状態は、**公開済** または **エラー** のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="97f90-144">The status is either **Published** or **Error**.</span></span>

