---
title: OData
description: "このトピックでは、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 24841
ms.assetid: 7137b0a0-1473-4134-b769-ede5e07fd6f5
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 3e1ee17855fa86467e7bbfec67473594fe00cdbf
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="odata"></a><span data-ttu-id="b523e-103">OData</span><span class="sxs-lookup"><span data-stu-id="b523e-103">OData</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b523e-104">この記事では、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b523e-104">This article provides information about Open Data Protocol (OData) and explains how you can use OData V4 to expose updatable views.</span></span>

## <a name="what-is-odata"></a><span data-ttu-id="b523e-105">OData とは</span><span class="sxs-lookup"><span data-stu-id="b523e-105">What is OData?</span></span>
<span data-ttu-id="b523e-106">OData は、データを作成および消費するための標準プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="b523e-106">OData is a standard protocol for creating and consuming data.</span></span> <span data-ttu-id="b523e-107">OData の目的は、作成、読み取り、更新、削除 (CRUD) 操作のための Representational State Transfer (REST) に基づくプロトコルを提供することです。</span><span class="sxs-lookup"><span data-stu-id="b523e-107">The purpose of OData is to provide a protocol that is based on Representational State Transfer (REST) for create, read, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="b523e-108">OData は、さまざまなプログラムからの情報にアクセスするために、HTTP および JavaScript Object Notation (JSON) などの Web テクノロジーを適用します。</span><span class="sxs-lookup"><span data-stu-id="b523e-108">OData applies web technologies such as HTTP and JavaScript Object Notation (JSON) to provide access to information from various programs.</span></span> <span data-ttu-id="b523e-109">OData には次のメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="b523e-109">OData provides the following benefits:</span></span>

- <span data-ttu-id="b523e-110">これにより、開発者は RESTful Web サービスを使用してデータを操作できます。</span><span class="sxs-lookup"><span data-stu-id="b523e-110">It lets developers interact with data by using RESTful web services.</span></span>
- <span data-ttu-id="b523e-111">これにより、見つけやすい方法でデータを共有する簡単で一貫した方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-111">It provides a simple and uniform way to share data in a discoverable manner.</span></span>
- <span data-ttu-id="b523e-112">製品を越えた広範な統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b523e-112">It enables broad integration across products.</span></span>
- <span data-ttu-id="b523e-113">HTTP プロトコル スタックを使用して統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b523e-113">It enables integration by using the HTTP protocol stack.</span></span>

<span data-ttu-id="b523e-114">OData の詳細については、次の Web ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-114">For more information about OData, see the following webpages.</span></span>

| <span data-ttu-id="b523e-115">トピック</span><span class="sxs-lookup"><span data-stu-id="b523e-115">Topic</span></span>                                                               | <span data-ttu-id="b523e-116">Webpage</span><span class="sxs-lookup"><span data-stu-id="b523e-116">Webpage</span></span>                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="b523e-117">OData 標準</span><span class="sxs-lookup"><span data-stu-id="b523e-117">OData standards</span></span>                                                     | <http://www.odata.org/documentation/>                   |
| <span data-ttu-id="b523e-118">OData: Web、クラウド、モバイル デバイスなどのデータ アクセス</span><span class="sxs-lookup"><span data-stu-id="b523e-118">OData: Data access for the web, the cloud, mobile devices, and more</span></span> | <http://msdn.microsoft.com/en-us/data/hh237663.aspx>    |
| <span data-ttu-id="b523e-119">例を通じた OData</span><span class="sxs-lookup"><span data-stu-id="b523e-119">OData through examples</span></span>                                              | <http://msdn.microsoft.com/en-us/library/ff478141.aspx> |

<span data-ttu-id="b523e-120">パブリック OData サービス エンドポイントにより、幅広いクライアントにわたって、一貫した方法でデータにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="b523e-120">The public OData service endpoint enables access to data in a consistent manner across a broad range of clients.</span></span> <span data-ttu-id="b523e-121">公開されているすべてのエンティティの一覧を表示するには、OData サービスのルート URLを開きます。</span><span class="sxs-lookup"><span data-stu-id="b523e-121">To see a list of all the entities that are exposed, open the OData service root URL.</span></span> <span data-ttu-id="b523e-122">システムのサービス ルートの URL の形式は **[お客様の組織のルート URL]/data** です。</span><span class="sxs-lookup"><span data-stu-id="b523e-122">The URL for the service root on your system has the following format: **[Your organization's root URL]/data**</span></span>

## <a name="addressing"></a><span data-ttu-id="b523e-123">アドレス指定</span><span class="sxs-lookup"><span data-stu-id="b523e-123">Addressing</span></span>
<span data-ttu-id="b523e-124">次のテーブルでは、フリート管理サンプルのリソースと対応する URL を示しています。</span><span class="sxs-lookup"><span data-stu-id="b523e-124">The following table describes the resources and the corresponding URLs in the Fleet Management sample.</span></span>


| <span data-ttu-id="b523e-125">リソース</span><span class="sxs-lookup"><span data-stu-id="b523e-125">Resource</span></span>            | <span data-ttu-id="b523e-126">URL</span><span class="sxs-lookup"><span data-stu-id="b523e-126">URL</span></span>                                                                     | <span data-ttu-id="b523e-127">説明</span><span class="sxs-lookup"><span data-stu-id="b523e-127">Description</span></span>                                                    |
|---------------------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b523e-128">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="b523e-128">Service endpoint</span></span>    | <span data-ttu-id="b523e-129">\[組織のルート URL\]/data/</span><span class="sxs-lookup"><span data-stu-id="b523e-129">\[Your organization's root URL\]/data/</span></span>                                  | <span data-ttu-id="b523e-130">OData エンティティのルート サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="b523e-130">The root service endpoint for OData entities</span></span>                   |
| <span data-ttu-id="b523e-131">エンティティ コレクション</span><span class="sxs-lookup"><span data-stu-id="b523e-131">Entity collection</span></span>   | <span data-ttu-id="b523e-132">\[組織のルート URL\]/data/Customers</span><span class="sxs-lookup"><span data-stu-id="b523e-132">\[Your organization's root URL\]/data/Customers</span></span>                         | <span data-ttu-id="b523e-133">すべての顧客のコレクション</span><span class="sxs-lookup"><span data-stu-id="b523e-133">The collection of all customers</span></span>                                |
| <span data-ttu-id="b523e-134">エンティティ</span><span class="sxs-lookup"><span data-stu-id="b523e-134">Entity</span></span>              | <span data-ttu-id="b523e-135">\[組織のルート URL\]/data/Customers("\[キー\]")</span><span class="sxs-lookup"><span data-stu-id="b523e-135">\[Your organization's root URL\]/data/Customers("\[key\]")</span></span>              | <span data-ttu-id="b523e-136">エンティティのコレクションから 1 つのエンティティ</span><span class="sxs-lookup"><span data-stu-id="b523e-136">A single entity from the entity collection</span></span>                     |
| <span data-ttu-id="b523e-137">ナビゲーション プロパティ</span><span class="sxs-lookup"><span data-stu-id="b523e-137">Navigation property</span></span> | <span data-ttu-id="b523e-138">\[組織のルート URL\]/data/Customers("\[キー\]")/Reservations</span><span class="sxs-lookup"><span data-stu-id="b523e-138">\[Your organization's root URL\]/data/Customers("\[key\]")/Reservations</span></span> | <span data-ttu-id="b523e-139">顧客からその顧客の引当までのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="b523e-139">The navigation from a customer to that customer's reservations</span></span> |
| <span data-ttu-id="b523e-140">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b523e-140">Property</span></span>            | <span data-ttu-id="b523e-141">\[組織のルート URL\]/data/Customers("\[キー\]")/FirstName</span><span class="sxs-lookup"><span data-stu-id="b523e-141">\[Your organization's root URL\]/data/Customers("\[key\]")/FirstName</span></span>    | <span data-ttu-id="b523e-142">顧客の名</span><span class="sxs-lookup"><span data-stu-id="b523e-142">The customer's first name</span></span>                                      |

## <a name="odata-services"></a><span data-ttu-id="b523e-143">OData サービス</span><span class="sxs-lookup"><span data-stu-id="b523e-143">OData services</span></span>
<span data-ttu-id="b523e-144">OData REST エンドポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="b523e-144">We provide an OData REST endpoint.</span></span> <span data-ttu-id="b523e-145">このエンドポイントは、アプリケーション オブジェクト ツリー (AOT) の **IsPublic** としてマークされているすべてのデータ エンティティを公開します。</span><span class="sxs-lookup"><span data-stu-id="b523e-145">This endpoint exposes all the data entities that are marked as **IsPublic** in the Application Object Tree (AOT).</span></span> <span data-ttu-id="b523e-146">ユーザーがデータを挿入およびシステムから取得するために使用できる完全な CRUD (作成、取得、更新、および削除) 機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="b523e-146">It supports complete CRUD (create, retrieve, update, and delete) functionality that users can use to insert and retrieve data from the system.</span></span> <span data-ttu-id="b523e-147">この機能の詳細なラボは、LCS の方法論に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b523e-147">Detailed labs for this feature are on the LCS methodology.</span></span> 

<span data-ttu-id="b523e-148">詳細については、[OData サービスに関する Office Mix プレゼンテーション](https://mix.office.com/watch/1aym08mqyjghi) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-148">For more information, see the [Office Mix presentation about OData Services](https://mix.office.com/watch/1aym08mqyjghi).</span></span>

<span data-ttu-id="b523e-149">OData サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/ODataConsoleApplication) です。</span><span class="sxs-lookup"><span data-stu-id="b523e-149">Code examples for consuming OData services are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/ODataConsoleApplication).</span></span>

### <a name="supported-features-from-the-odata-specification"></a><span data-ttu-id="b523e-150">OData 仕様からサポートされている機能</span><span class="sxs-lookup"><span data-stu-id="b523e-150">Supported features from the OData specification</span></span>

<span data-ttu-id="b523e-151">[OData 仕様](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html) に従って、OData サービスで使用可能な上位レベルの機能は次のとおりです.</span><span class="sxs-lookup"><span data-stu-id="b523e-151">The following are the high-level features that are enabled for the OData service, per the [OData specification](http://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html).</span></span>

- <span data-ttu-id="b523e-152">CRUD サポートは、転記、パッチ、挿入、および削除の HTTP 動詞サポートにより処理されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-152">CRUD support is handled through HTTP verb support for POST, PATCH, PUT, and DELETE.</span></span> 
- <span data-ttu-id="b523e-153">利用可能なクエリ オプションは</span><span class="sxs-lookup"><span data-stu-id="b523e-153">Available query options are</span></span>
  -   <span data-ttu-id="b523e-154">$filter</span><span class="sxs-lookup"><span data-stu-id="b523e-154">$filter</span></span>
  -   <span data-ttu-id="b523e-155">$count</span><span class="sxs-lookup"><span data-stu-id="b523e-155">$count</span></span>
  -   <span data-ttu-id="b523e-156">$orderby</span><span class="sxs-lookup"><span data-stu-id="b523e-156">$orderby</span></span>
  -   <span data-ttu-id="b523e-157">$skip</span><span class="sxs-lookup"><span data-stu-id="b523e-157">$skip</span></span>
  -   <span data-ttu-id="b523e-158">$top</span><span class="sxs-lookup"><span data-stu-id="b523e-158">$top</span></span>
  -   <span data-ttu-id="b523e-159">$expand</span><span class="sxs-lookup"><span data-stu-id="b523e-159">$expand</span></span>
  -   <span data-ttu-id="b523e-160">$select</span><span class="sxs-lookup"><span data-stu-id="b523e-160">$select</span></span>
- <span data-ttu-id="b523e-161">OData サービスでは、最大ページ サイズが 1,000 のサービス ドリブン ページングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b523e-161">The OData service supports serving driven paging with a maximum page size of 1,000.</span></span>

<span data-ttu-id="b523e-162">詳細については、以下を参照してください: [エンティティにバインドされている OData アクション](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398355)</span><span class="sxs-lookup"><span data-stu-id="b523e-162">For more information, see: [OData actions that are bound to entities](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398355).</span></span>

#### <a name="filter-details"></a><span data-ttu-id="b523e-163">フィルター詳細</span><span class="sxs-lookup"><span data-stu-id="b523e-163">Filter details</span></span>

<span data-ttu-id="b523e-164">$filter には組み込みの演算子があります</span><span class="sxs-lookup"><span data-stu-id="b523e-164">There are built-in operators for $filter</span></span>
-   <span data-ttu-id="b523e-165">次の値と等しい</span><span class="sxs-lookup"><span data-stu-id="b523e-165">Equals</span></span>
-   <span data-ttu-id="b523e-166">等しくない</span><span class="sxs-lookup"><span data-stu-id="b523e-166">Not equals</span></span>
-   <span data-ttu-id="b523e-167">次の値より大きい</span><span class="sxs-lookup"><span data-stu-id="b523e-167">Greater than</span></span>
-   <span data-ttu-id="b523e-168">次の値以上</span><span class="sxs-lookup"><span data-stu-id="b523e-168">Greater than or equal</span></span>
-   <span data-ttu-id="b523e-169">次の値より小さい</span><span class="sxs-lookup"><span data-stu-id="b523e-169">Less than</span></span>
-   <span data-ttu-id="b523e-170">次の値以下</span><span class="sxs-lookup"><span data-stu-id="b523e-170">Less than or equal</span></span>
-   <span data-ttu-id="b523e-171">かつ</span><span class="sxs-lookup"><span data-stu-id="b523e-171">And</span></span>
-   <span data-ttu-id="b523e-172">又は</span><span class="sxs-lookup"><span data-stu-id="b523e-172">Or</span></span>
-   <span data-ttu-id="b523e-173">ない</span><span class="sxs-lookup"><span data-stu-id="b523e-173">Not</span></span>
-   <span data-ttu-id="b523e-174">追加</span><span class="sxs-lookup"><span data-stu-id="b523e-174">Addition</span></span>
-   <span data-ttu-id="b523e-175">減算</span><span class="sxs-lookup"><span data-stu-id="b523e-175">Subtraction</span></span>
-   <span data-ttu-id="b523e-176">乗算</span><span class="sxs-lookup"><span data-stu-id="b523e-176">Multiplication</span></span>
-   <span data-ttu-id="b523e-177">区分</span><span class="sxs-lookup"><span data-stu-id="b523e-177">Division</span></span>

<span data-ttu-id="b523e-178">また、**Contains** オプションを $filter 要求とともに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b523e-178">You can also use the **Contains** option with $filter requests.</span></span> <span data-ttu-id="b523e-179">これは、ワイルドカード文字として実装されています。</span><span class="sxs-lookup"><span data-stu-id="b523e-179">It has been implemented as a wildcard character.</span></span> <span data-ttu-id="b523e-180">例: `http://host/service/EntitySet?$filter=StringField eq '\*retail\*'`</span><span class="sxs-lookup"><span data-stu-id="b523e-180">For example: `http://host/service/EntitySet?$filter=StringField eq '\*retail\*'`</span></span>

<span data-ttu-id="b523e-181">詳細については、「[OData 演算子](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part2-url-conventions/odata-v4.0-errata02-os-part2-url-conventions-complete.html#_Toc406398096)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-181">For more information, see [OData operators](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part2-url-conventions/odata-v4.0-errata02-os-part2-url-conventions-complete.html#_Toc406398096).</span></span>

#### <a name="batch-requests"></a><span data-ttu-id="b523e-182">バッチ要求</span><span class="sxs-lookup"><span data-stu-id="b523e-182">Batch requests</span></span>
<span data-ttu-id="b523e-183">OData サービスでは、バッチ要求がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b523e-183">Batch requests are supported in the OData service.</span></span> <span data-ttu-id="b523e-184">詳細については、「[OData バッチ要求](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398359)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-184">For more information, see [OData batch requests](http://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398359).</span></span>

#### <a name="metadata-annotations"></a><span data-ttu-id="b523e-185">メタデータの注釈</span><span class="sxs-lookup"><span data-stu-id="b523e-185">Metadata annotations</span></span>

<span data-ttu-id="b523e-186">/data/$ メタデータは、注釈を提供します。</span><span class="sxs-lookup"><span data-stu-id="b523e-186">/data/$metadata provides annotations.</span></span> <span data-ttu-id="b523e-187">EnumType は、$metadata でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b523e-187">EnumType is support in $metadata.</span></span>

![EnumType メタデータ](./media/metadata.png)


### <a name="cross-company-behavior"></a><span data-ttu-id="b523e-189">会社間動作</span><span class="sxs-lookup"><span data-stu-id="b523e-189">Cross-company behavior</span></span>

<span data-ttu-id="b523e-190">既定では、OData はユーザーの既定の会社に属しているデータのみを返します。</span><span class="sxs-lookup"><span data-stu-id="b523e-190">By default, OData returns only data that belongs to the user's default company.</span></span> <span data-ttu-id="b523e-191">ユーザーの既定の会社以外のデータを表示するには、**?cross-company=true** クエリ オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="b523e-191">To see data from outside the user's default company, specify the **?cross-company=true** query option.</span></span> <span data-ttu-id="b523e-192">このオプションは、ユーザーがアクセスできるすべての会社のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="b523e-192">This option will return data from all companies that the user has access to.</span></span> 

<span data-ttu-id="b523e-193">**例:** `http://[baseURI\]/data/FleetCustomers?cross-company=true`</span><span class="sxs-lookup"><span data-stu-id="b523e-193">**Example:** `http://[baseURI\]/data/FleetCustomers?cross-company=true`</span></span>

<span data-ttu-id="b523e-194">既定の会社ではない特定の会社ごとにフィルター処理するには、次の構文を使用します。`http://[baseURI\]/data/FleetCustomers?$filter=dataAreaId eq 'usrt'&cross-company=true`</span><span class="sxs-lookup"><span data-stu-id="b523e-194">To filter by a particular company that isn't your default company, use the following syntax: `http://[baseURI\]/data/FleetCustomers?$filter=dataAreaId eq 'usrt'&cross-company=true`</span></span>

### <a name="validate-methods"></a><span data-ttu-id="b523e-195">メソッドの検証</span><span class="sxs-lookup"><span data-stu-id="b523e-195">Validate methods</span></span>

<span data-ttu-id="b523e-196">次のテーブルは、OData スタックが対応するデータ エンティティで暗黙的に呼び出す検証方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-196">The following table summarizes the validate methods that the OData stack calls implicitly on the corresponding data entity.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b523e-197">OData</span><span class="sxs-lookup"><span data-stu-id="b523e-197">OData</span></span></th>
<th><span data-ttu-id="b523e-198">メソッド (呼び出される順序で一覧表示されます)</span><span class="sxs-lookup"><span data-stu-id="b523e-198">Methods (listed in the order in which they are called)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b523e-199">新規</span><span class="sxs-lookup"><span data-stu-id="b523e-199">Create</span></span></td>
<td><ol>
<li><span data-ttu-id="b523e-200"><strong>クリア ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-200"><strong>Clear()</strong></span></span></li>
<li><span data-ttu-id="b523e-201"><strong>Initvalue()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-201"><strong>Initvalue()</strong></span></span></li>
<li><span data-ttu-id="b523e-202"><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</span><span class="sxs-lookup"><span data-stu-id="b523e-202"><strong>PropertyInfo.SetValue()</strong> for all specified fields in the request</span></span></li>
<li><span data-ttu-id="b523e-203"><strong>Validatefield()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-203"><strong>Validatefield()</strong></span></span></li>
<li><span data-ttu-id="b523e-204"><strong>Defaultrow</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-204"><strong>Defaultrow</strong></span></span></li>
<li><span data-ttu-id="b523e-205"><strong>Validatewrite()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-205"><strong>Validatewrite()</strong></span></span></li>
<li><span data-ttu-id="b523e-206"><strong>書き込み ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-206"><strong>Write()</strong></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b523e-207">更新</span><span class="sxs-lookup"><span data-stu-id="b523e-207">Update</span></span></td>
<td><ol>
<li><span data-ttu-id="b523e-208"><strong>Forupdate()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-208"><strong>Forupdate()</strong></span></span></li>
<li><span data-ttu-id="b523e-209"><strong>再表示 ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-209"><strong>Reread()</strong></span></span></li>
<li><span data-ttu-id="b523e-210"><strong>クリア ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-210"><strong>Clear()</strong></span></span></li>
<li><span data-ttu-id="b523e-211"><strong>Initvalue()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-211"><strong>Initvalue()</strong></span></span></li>
<li><span data-ttu-id="b523e-212"><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</span><span class="sxs-lookup"><span data-stu-id="b523e-212"><strong>PropertyInfo.SetValue()</strong> for all specified fields in the request</span></span></li>
<li><span data-ttu-id="b523e-213"><strong>Validatefield()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-213"><strong>Validatefield()</strong></span></span></li>
<li><span data-ttu-id="b523e-214"><strong>Defaultrow()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-214"><strong>Defaultrow()</strong></span></span></li>
<li><span data-ttu-id="b523e-215"><strong>Validatewrite()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-215"><strong>Validatewrite()</strong></span></span></li>
<li><span data-ttu-id="b523e-216"><strong>書き込み ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-216"><strong>Write()</strong></span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b523e-217">消去</span><span class="sxs-lookup"><span data-stu-id="b523e-217">Delete</span></span></td>
<td><ol>
<li><span data-ttu-id="b523e-218"><strong>Forupdate()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-218"><strong>Forupdate()</strong></span></span></li>
<li><span data-ttu-id="b523e-219"><strong>再表示 ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-219"><strong>Reread()</strong></span></span></li>
<li><span data-ttu-id="b523e-220"><strong>checkRestrictedDeleteActions()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-220"><strong>checkRestrictedDeleteActions()</strong></span></span></li>
<li><span data-ttu-id="b523e-221"><strong>Validatedelete()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-221"><strong>Validatedelete()</strong></span></span></li>
<li><span data-ttu-id="b523e-222"><strong>削除 ()</strong></span><span class="sxs-lookup"><span data-stu-id="b523e-222"><strong>Delete()</strong></span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="exposing-odata-entities"></a><span data-ttu-id="b523e-223">OData エンティティを公開</span><span class="sxs-lookup"><span data-stu-id="b523e-223">Exposing OData entities</span></span>
<span data-ttu-id="b523e-224">OData エンティティは、更新可能なビューの概念に基づいています。</span><span class="sxs-lookup"><span data-stu-id="b523e-224">OData entities are based on the concept of an updatable view.</span></span> <span data-ttu-id="b523e-225">更新可能なビューの **IsPublic** プロパティが **TRUE** 設定されているとき、そのビューは最上位レベルの OData エンティティとして公開されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-225">When the **IsPublic** property for an updatable view is set to **TRUE**, that view is exposed as a top-level OData entity.</span></span>

## <a name="setting-navigation-properties-between-odata-entities"></a><span data-ttu-id="b523e-226">OData エンティティ間のナビゲーション プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="b523e-226">Setting navigation properties between OData entities</span></span>
<span data-ttu-id="b523e-227">OData エンティティ間のリンクは、ナビゲーション プロパティによって記述されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-227">Links between OData entities are described by a navigation property.</span></span> <span data-ttu-id="b523e-228">ナビゲーション プロパティでは、アソシエーションの一方から他方までのナビゲーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b523e-228">Navigation properties describe the navigation from one end of an association to the other end.</span></span>

#### <a name="adding-actions-on-odata-entities"></a><span data-ttu-id="b523e-229">OData エンティティでのアクションの追加</span><span class="sxs-lookup"><span data-stu-id="b523e-229">Adding actions on OData entities</span></span>
<span data-ttu-id="b523e-230">アクションで動作をデータ モデルに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="b523e-230">Actions let you inject behaviors into the data model.</span></span> <span data-ttu-id="b523e-231">アクションを追加するには、更新可能なビューにメソッドを追加し、そのメソッドを特定の属性で修飾します。</span><span class="sxs-lookup"><span data-stu-id="b523e-231">To add actions, add a method to the updatable view, and decorate that method with specific attributes.</span></span> <span data-ttu-id="b523e-232">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-232">Here is an example.</span></span>

    [SysODataActionAttribute("CalcMaintenanceDuration", true)]
    public int CalculateMaintenanceDuration()
    {
        //do something
        return 0;
    }

<span data-ttu-id="b523e-233">この例では、**SysODataActionAttribute** クラスがアクションとして公開されている **CalculateMaintenanceDuration** メソッドを修飾します。</span><span class="sxs-lookup"><span data-stu-id="b523e-233">In this example, the **SysODataActionAttribute** class decorates the **CalculateMaintenanceDuration** method that is exposed as an action.</span></span> <span data-ttu-id="b523e-234">属性の最初の引数は公開されているアクションの名前で、2 番目の引数はこのアクションが常に利用可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-234">The first argument of the attribute is the publicly exposed name of the action, and the second argument indicates whether this action is always available.</span></span> <span data-ttu-id="b523e-235">アクションとして公開されているメソッドは、任意のプリミティブ型または別のパブリックの更新可能なビューを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b523e-235">Methods that are exposed as actions can return any primitive type or another public updatable view.</span></span> <span data-ttu-id="b523e-236">このメソッドが公開されると、OData $ メタデータに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-236">After this method is exposed, it appears in the OData $metadata.</span></span> <span data-ttu-id="b523e-237">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-237">Here is an example.</span></span>

<span data-ttu-id="b523e-238">[![OData $ メタデータで公開されているメソッド](./media/1_odata.png)](./media/1_odata.png)</span><span class="sxs-lookup"><span data-stu-id="b523e-238">[![Exposed method in the OData $metadata](./media/1_odata.png)](./media/1_odata.png)</span></span>

<span data-ttu-id="b523e-239">次の OData アクションの例では、パラメーターで取り、リストを返します。</span><span class="sxs-lookup"><span data-stu-id="b523e-239">The following example of an OData action takes in a parameter and returns a list.</span></span>

    [SysODataActionAttribute("GetColors", true),
     SysODataCollectionAttribute("return", Types::Record, "CarColor")]
    public List GetColorsByAvailability(boolean onlyAvailableVehicles)
    {
        List returnList = new List(Types::Record);
        // do something
        return returnList;
    }

<span data-ttu-id="b523e-240">この例では、OData は **SysODataCollectionAttribute** クラスによって X++ から強く定型化されたコレクションを公開できます。</span><span class="sxs-lookup"><span data-stu-id="b523e-240">In this example, the **SysODataCollectionAttribute** class enables OData to expose strongly typed collections from X++.</span></span> <span data-ttu-id="b523e-241">このクラスは次の 3 つのパラメーターを取ります。</span><span class="sxs-lookup"><span data-stu-id="b523e-241">This class takes in three parameters:</span></span>

- <span data-ttu-id="b523e-242">リストを示すパラメーターの名前 (メソッドの戻り値として **return** を返します)。</span><span class="sxs-lookup"><span data-stu-id="b523e-242">The name of the parameter that is a list (Use **return** for the return value of the method.)</span></span>
- <span data-ttu-id="b523e-243">この一覧のメンバーの X++ タイプ</span><span class="sxs-lookup"><span data-stu-id="b523e-243">The X++ type of the members of this list</span></span>
- <span data-ttu-id="b523e-244">コレクションに含まれている OData リソースのパブリック名</span><span class="sxs-lookup"><span data-stu-id="b523e-244">The public name of the OData resource that is contained in the collection</span></span>

<span data-ttu-id="b523e-245">これらのアクションが公開された後、サービス ルートの URL から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="b523e-245">After these actions are exposed, they can be invoked from the service root URL.</span></span> 

<span data-ttu-id="b523e-246">ソース コード内の **SysODataActionAttribute** 属性を検索することにより、データ エンティティ上で定義されたアクションを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b523e-246">You can find actions that are defined on data entities by searching for the **SysODataActionAttribute** attribute in the source code.</span></span>

## <a name="querying-or-browsing-an-odata-endpoint"></a><span data-ttu-id="b523e-247">OData エンドポイントの照会や参照</span><span class="sxs-lookup"><span data-stu-id="b523e-247">Querying or browsing an OData endpoint</span></span>
<span data-ttu-id="b523e-248">OData は、データベースに対して豊富なクエリを作成できる SQL に似た言語を有効にして、結果に希望するデータ項目のみが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="b523e-248">OData enables an SQL-like language that lets you create rich queries against the database, so that the results include only the data items that you want.</span></span> <span data-ttu-id="b523e-249">クエリを作成するには、リソース パスに条件を追加します。</span><span class="sxs-lookup"><span data-stu-id="b523e-249">To create a query, append criteria to the resource path.</span></span> <span data-ttu-id="b523e-250">たとえば、ブラウザで次のクエリ オプションを加えることによって、**顧客**エンティティ コレクションのクエリを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b523e-250">For example, you can query the **Customers** entity collection by appending the following query options in your browser.</span></span>

| <span data-ttu-id="b523e-251">URL</span><span class="sxs-lookup"><span data-stu-id="b523e-251">URL</span></span>                                                                      | <span data-ttu-id="b523e-252">説明</span><span class="sxs-lookup"><span data-stu-id="b523e-252">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b523e-253">\[組織のルート URL\]/data/Customers</span><span class="sxs-lookup"><span data-stu-id="b523e-253">\[Your organization's root URL\]/data/Customers</span></span>                            | <span data-ttu-id="b523e-254">すべての顧客の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-254">List all the customers.</span></span>                                                                       |
| <span data-ttu-id="b523e-255">\[組織のルート URL\]/data/Customers?$top=3</span><span class="sxs-lookup"><span data-stu-id="b523e-255">\[Your organization's root URL\]/data/Customers?$top=3</span></span>                     | <span data-ttu-id="b523e-256">最初の 3 つのレコードを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-256">List the first three records.</span></span>                                                                 |
| <span data-ttu-id="b523e-257">\[組織のルート URL\]/data/Customers?$select=FirstName,LastName</span><span class="sxs-lookup"><span data-stu-id="b523e-257">\[Your organization's root URL\]/data/Customers?$select=FirstName,LastName</span></span> | <span data-ttu-id="b523e-258">すべての顧客の一覧を表示しますが、姓名のプロパティだけを表示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-258">List all the customers, but show only the first name and last name properties.</span></span>                |
| <span data-ttu-id="b523e-259">\[組織のルート URL\]/data/Customers?$format=json</span><span class="sxs-lookup"><span data-stu-id="b523e-259">\[Your organization's root URL\]/data/Customers?$format=json</span></span>               | <span data-ttu-id="b523e-260">JavaScript クライアントとやり取りするために使用できる JSON 形式ですべての顧客の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="b523e-260">List all the customers in a JSON format that can be used to interact with JavaScript clients.</span></span> |

<span data-ttu-id="b523e-261">OData プロトコルは、エンティティで多くの似たフィルター処理とクエリ オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b523e-261">The OData protocol supports many similar filtering and querying options on entities.</span></span> <span data-ttu-id="b523e-262">クエリ オプションの完全なセットについては、[Windows Communication Foundation](http://msdn.microsoft.com/en-us/library/ff478141.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-262">For the full set of query options, see [Windows Communication Foundation](http://msdn.microsoft.com/en-us/library/ff478141.aspx).</span></span>

## <a name="authentication"></a><span data-ttu-id="b523e-263">認証</span><span class="sxs-lookup"><span data-stu-id="b523e-263">Authentication</span></span>
<span data-ttu-id="b523e-264">OData は、サーバーと同じ認証スタック上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b523e-264">OData sits on the same authentication stack as the server.</span></span> <span data-ttu-id="b523e-265">認証の詳細については、[サービス エンドポイント](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b523e-265">For more information about the authentication, see [Service endpoints](services-home-page.md).</span></span>


## <a name="tips-and-tricks"></a><span data-ttu-id="b523e-266">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="b523e-266">Tips and tricks</span></span>

### <a name="run-multiple-requests-in-a-single-transaction"></a><span data-ttu-id="b523e-267">1 つのトランザクションで複数の要求を実行</span><span class="sxs-lookup"><span data-stu-id="b523e-267">Run multiple requests in a single transaction</span></span>
<span data-ttu-id="b523e-268">OData バッチ フレームワークは、*変更セット*を使用します。</span><span class="sxs-lookup"><span data-stu-id="b523e-268">The OData batch framework uses *changesets*.</span></span> <span data-ttu-id="b523e-269">各変更セットには、単一アトミック ユニットとして扱われるべき要求のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b523e-269">Each changeset contains a list of requests that should be treated as single atomic unit.</span></span> <span data-ttu-id="b523e-270">つまり、すべての要求が正常に実行されるか、要求が失敗した場合はすべての要求が正常に実行されません。</span><span class="sxs-lookup"><span data-stu-id="b523e-270">In other words, either all the requests are run successfully or, if any request fails, none of the requests are run successfully.</span></span> <span data-ttu-id="b523e-271">次の例は、単一の変更セット内に要求のリストを持つバッチ要求を送信する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b523e-271">The following example shows how to send a batch request that has a list of requests in a single changeset.</span></span> 

<span data-ttu-id="b523e-272">**SaveChanges()** の **SaveChangesOptions.BatchWithSingleChangeset** オプションを使用すると、単一の変更セットにすべての要求がバンドルされていることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="b523e-272">The **SaveChangesOptions.BatchWithSingleChangeset** option in **SaveChanges()** helps guarantee that all requests are bundled into a single changeset.</span></span> 

    public static void CreateProductColors(Resources context)
        {
            var productColorsCollection = new DataServiceCollection<ProductColor>(context);

            var color1 = new ProductColor();
            productColorsCollection.Add(color);
            color1.ColorId = "New Color1"; // set any other properties needed

            var color2 = new ProductColor();
            productColorsCollection.Add(color1);
            color2.ColorId = "New Color2"; // set any other properties needed

            context.SaveChanges(SaveChangesOptions.BatchWithSingleChangeset);
        }

### <a name="prevent-unset-records-from-being-posted-when-you-use-an-odata-client"></a><span data-ttu-id="b523e-273">OData クライアントを使用する場合に設定されていないレコードが転記されることを防止する</span><span class="sxs-lookup"><span data-stu-id="b523e-273">Prevent unset records from being posted when you use an OData client</span></span>
<span data-ttu-id="b523e-274">例 1 に示すように、OData クライアントを使用して新しいレコードを作成するときは、設定されていないプロパティが要求の本体に含まれ、既定値がそれらのプロパティに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b523e-274">When you create a new record by using an OData client, as shown in example 1, properties that aren't set are included in the body of the request, and default values are assigned to them.</span></span> <span data-ttu-id="b523e-275">この動作を回避し、明示的に設定されたプロパティのみをポストするには、例 2 に示すように、**SaveChanges()** の **SaveChangesOptions.PostOnlySetProperties** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="b523e-275">To prevent this behavior and post only properties that are set explicitly, use the **SaveChangesOptions.PostOnlySetProperties** option in **SaveChanges()**, as shown in example 2.</span></span>

<span data-ttu-id="b523e-276">**例 1**</span><span class="sxs-lookup"><span data-stu-id="b523e-276">**Example 1**</span></span>

    public static void CreateVendor(Resources context)
        {
            var vendorCollection = new DataServiceCollection<Vendor>(context);
            var vendor = new Vendor();
            vendorCollection.Add(vendor);
            // set properties
            context.SaveChanges();
        }

<span data-ttu-id="b523e-277">**例 2**</span><span class="sxs-lookup"><span data-stu-id="b523e-277">**Example 2**</span></span>

    public static void CreateVendor(Resources context)
        {
            var vendorCollection = new DataServiceCollection<Vendor>(context);
            var vendor = new Vendor();
            vendorCollection.Add(vendor);
            // set properties

            // Save specifying PostOnlySetProperties flag
            context.SaveChanges(SaveChangesOptions.PostOnlySetProperties);
        }


