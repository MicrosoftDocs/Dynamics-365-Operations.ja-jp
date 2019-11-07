---
title: レポート サーバーのアーキテクチャ
description: この記事では、Retail サーバーのアーキテクチャについて説明します。 Retail サーバーは、Retail Modern 販売時点管理 (POS) および電子商取引クライアントのステートレス サービスとビジネス ロジックを提供します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 31521
ms.assetid: 3a169648-592b-4616-9834-598c0244a852
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cb206758fbee5a5a04c79a3616c94a4d10576105
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570594"
---
# <a name="retail-server-architecture"></a><span data-ttu-id="f42a3-104">レポート サーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="f42a3-104">Retail Server architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f42a3-105">この記事では、Retail サーバーのアーキテクチャについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-105">This article describes the architecture of Retail Server.</span></span> <span data-ttu-id="f42a3-106">Retail サーバーは、Retail Modern 販売時点管理 (POS) および電子商取引クライアントのステートレス サービスとビジネス ロジックを提供します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-106">Retail Server provides stateless services and business logic for Retail Modern Point of Sale (POS) and E-Commerce clients.</span></span>

<a name="retail-server-architecture"></a><span data-ttu-id="f42a3-107">レポート サーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="f42a3-107">Retail Server architecture</span></span>
--------------------------

<span data-ttu-id="f42a3-108">Commerce Runtime は Retail サーバー レイヤーにラップされます。</span><span class="sxs-lookup"><span data-stu-id="f42a3-108">The commerce runtime is wrapped in a Retail Server layer.</span></span> <span data-ttu-id="f42a3-109">Retail サーバーは、タブレットや電話で店舗とオンラインの両方のシン クライアントをサポートするために、Web API および OData を使用します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-109">Retail Server uses a web API and OData to support thin clients both in the store and online on tablets and phones.</span></span> <span data-ttu-id="f42a3-110">Commerce Runtime は Commerce Data Exchange サービスを通じて Retail Headquarters と通信します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-110">The commerce runtime communicates with Retail Headquarters through Commerce Data Exchange services.</span></span> <span data-ttu-id="f42a3-111">次の図は、Retail サーバーのアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="f42a3-111">The following diagram shows the architecture of Retail Server.</span></span> 

<span data-ttu-id="f42a3-112">[![Retail サーバーのアーキテクチャの図](./media/retailserver.png)](./media/retailserver.png)</span><span class="sxs-lookup"><span data-stu-id="f42a3-112">[![Retail server architecture diagram](./media/retailserver.png)](./media/retailserver.png)</span></span> 

<span data-ttu-id="f42a3-113">Retail サーバーは、次の概念を使用します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-113">Retail Server uses the following concepts.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="f42a3-114">概念</span><span class="sxs-lookup"><span data-stu-id="f42a3-114">Concept</span></span></th>
<th><span data-ttu-id="f42a3-115">説明</span><span class="sxs-lookup"><span data-stu-id="f42a3-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f42a3-116">エンティティ タイプ</span><span class="sxs-lookup"><span data-stu-id="f42a3-116">Entity type</span></span></td>
<td><span data-ttu-id="f42a3-117">エンティティ タイプは監視するライフ サイクルを持つエンティティです。</span><span class="sxs-lookup"><span data-stu-id="f42a3-117">An entity type is an entity that has a life cycle that you want to monitor.</span></span> <span data-ttu-id="f42a3-118">各エンティティ タイプには、キーがあります。</span><span class="sxs-lookup"><span data-stu-id="f42a3-118">Each entity type has a key.</span></span> <span data-ttu-id="f42a3-119">エンティティ タイプの例は<strong>顧客</strong>です。</span><span class="sxs-lookup"><span data-stu-id="f42a3-119">An example of an entity type is <strong>Customer</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f42a3-120">複合型</span><span class="sxs-lookup"><span data-stu-id="f42a3-120">Complex type</span></span></td>
<td><span data-ttu-id="f42a3-121">複合型は、特定の関連プロパティをグループ化して重複を防止するよう設計された OData 概念です。</span><span class="sxs-lookup"><span data-stu-id="f42a3-121">A complex type is an OData concept that is designed to prevent duplication by grouping specific related properties.</span></span> <span data-ttu-id="f42a3-122">これらの関連するプロパティは、複数のエンティティで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="f42a3-122">These related properties can be reused in multiple entities.</span></span> <span data-ttu-id="f42a3-123">たとえば、<strong>顧客</strong>は顧客のアドレスを持つエンティティ タイプです。</span><span class="sxs-lookup"><span data-stu-id="f42a3-123">For example, <strong>Customer</strong> is an entity type that has a customer address.</span></span> <span data-ttu-id="f42a3-124">この顧客アドレスは、アドレス行、市町村、都道府県、および郵便番号を含むラッパーです。</span><span class="sxs-lookup"><span data-stu-id="f42a3-124">This customer address is a wrapper that contains an address line, city, state, and ZIP/postal code.</span></span> <span data-ttu-id="f42a3-125">したがって、<strong>顧客の住所</strong>は、他のエンティティ タイプにより再利用できる複合型です。</span><span class="sxs-lookup"><span data-stu-id="f42a3-125">Therefore, <strong>Customer address</strong> is a complex type that can be reused by other entity types.</span></span> <span data-ttu-id="f42a3-126">たとえば、<strong>注文</strong>エンティティ タイプは、<strong>顧客</strong>エンティティ タイプに関連付けられている同じ住所情報を必要とし、したがって<strong>顧客住所</strong>複合型を再利用します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-126">For example, the <strong>Order</strong> entity type requires the same address information that is associated with the <strong>Customer</strong> entity type and therefore reuses the <strong>Customer address</strong> complex type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f42a3-127">コントローラー</span><span class="sxs-lookup"><span data-stu-id="f42a3-127">Controller</span></span></td>
<td><span data-ttu-id="f42a3-128">コントローラーは、エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールするエンティティ タイプのマッピングです。</span><span class="sxs-lookup"><span data-stu-id="f42a3-128">A controller is a mapping for an entity type that controls create, read, update, and delete (CRUD) behaviors and actions for the entity type.</span></span> <span data-ttu-id="f42a3-129">各 commerce エンティティに、コントローラーが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f42a3-129">A controller is provided for each commerce entity.</span></span> <span data-ttu-id="f42a3-130">以下のコントローラーをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="f42a3-130">You can customize the following controllers:</span></span>
<ul>
<li><span data-ttu-id="f42a3-131">カート</span><span class="sxs-lookup"><span data-stu-id="f42a3-131">Carts</span></span></li>
<li><span data-ttu-id="f42a3-132">カタログ</span><span class="sxs-lookup"><span data-stu-id="f42a3-132">Catalogs</span></span></li>
<li><span data-ttu-id="f42a3-133">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="f42a3-133">Categories</span></span></li>
<li><span data-ttu-id="f42a3-134">コマース</span><span class="sxs-lookup"><span data-stu-id="f42a3-134">Commerce</span></span></li>
<li><span data-ttu-id="f42a3-135">コマース リスト</span><span class="sxs-lookup"><span data-stu-id="f42a3-135">Commerce Lists</span></span></li>
<li><span data-ttu-id="f42a3-136">複合キー エンティティ</span><span class="sxs-lookup"><span data-stu-id="f42a3-136">Composite Key Entity</span></span></li>
<li><span data-ttu-id="f42a3-137">コントローラ アセンブリ リゾルバー</span><span class="sxs-lookup"><span data-stu-id="f42a3-137">Controller Assembly Resolver</span></span></li>
<li><span data-ttu-id="f42a3-138">顧客</span><span class="sxs-lookup"><span data-stu-id="f42a3-138">Customers</span></span></li>
<li><span data-ttu-id="f42a3-139">従業員</span><span class="sxs-lookup"><span data-stu-id="f42a3-139">Employees</span></span></li>
<li><span data-ttu-id="f42a3-140">バインドできないアクション</span><span class="sxs-lookup"><span data-stu-id="f42a3-140">Non-Bindable Action</span></span></li>
<li><span data-ttu-id="f42a3-141">組織単位</span><span class="sxs-lookup"><span data-stu-id="f42a3-141">Org Units</span></span></li>
<li><span data-ttu-id="f42a3-142">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="f42a3-142">Picking Lists</span></span></li>
<li><span data-ttu-id="f42a3-143">製品</span><span class="sxs-lookup"><span data-stu-id="f42a3-143">Products</span></span></li>
<li><span data-ttu-id="f42a3-144">発注書</span><span class="sxs-lookup"><span data-stu-id="f42a3-144">Purchase Orders</span></span></li>
<li><span data-ttu-id="f42a3-145">販売注文</span><span class="sxs-lookup"><span data-stu-id="f42a3-145">Sales Orders</span></span></li>
<li><span data-ttu-id="f42a3-146">シフト</span><span class="sxs-lookup"><span data-stu-id="f42a3-146">Shifts</span></span></li>
<li><span data-ttu-id="f42a3-147">在庫棚卸仕訳帳</span><span class="sxs-lookup"><span data-stu-id="f42a3-147">Stock Counts Journals</span></span></li>
<li><span data-ttu-id="f42a3-148">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="f42a3-148">Transfer Orders</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f42a3-149">メタデータ</span><span class="sxs-lookup"><span data-stu-id="f42a3-149">Metadata</span></span></td>
<td><span data-ttu-id="f42a3-150">メタデータは、クライアントとサーバーの間の契約を定義します。</span><span class="sxs-lookup"><span data-stu-id="f42a3-150">Metadata defines the contract between the client and the server.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f42a3-151">自分自身のエンティティ タイプまたは複合タイプを作成して、既存のコントローラーを拡張し、新しいコントローラーを追加し、メタデータをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="f42a3-151">You can create your own entity type or complex type, extend an existing controller, add a new controller, and customize the metadata.</span></span> <span data-ttu-id="f42a3-152">Commerce ランタイムをカスタマイズする場合は、Retail サーバーのさまざまなコンポーネントもカスタマイズし、これらの変更を Retail Modern POS クライアントに公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f42a3-152">If you customize the commerce runtime, you must also customize various components in Retail Server to expose those changes to your Retail Modern POS clients.</span></span>



