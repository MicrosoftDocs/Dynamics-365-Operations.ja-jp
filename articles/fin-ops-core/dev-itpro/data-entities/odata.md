---
title: データ プロトコル (OData) を開く
description: このトピックでは、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24841
ms.assetid: 7137b0a0-1473-4134-b769-ede5e07fd6f5
ms.search.region: Global
ms.search.industry: ''
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13191dbc85571101e6a8fe34adf06fcda8a2e0bb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183468"
---
# <a name="open-data-protocol-odata"></a><span data-ttu-id="f6038-103">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="f6038-103">Open Data Protocol (OData)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6038-104">このトピックでは、Open Data Protocol (OData) に関する情報を提供し、OData V4 を使用して更新可能なビューを公開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f6038-104">This topic provides information about Open Data Protocol (OData) and explains how you can use OData V4 to expose updatable views.</span></span>

## <a name="what-is-odata"></a><span data-ttu-id="f6038-105">OData とは</span><span class="sxs-lookup"><span data-stu-id="f6038-105">What is OData?</span></span>
<span data-ttu-id="f6038-106">OData は、データを作成および消費するための標準プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="f6038-106">OData is a standard protocol for creating and consuming data.</span></span> <span data-ttu-id="f6038-107">OData の目的は、作成、読み取り、更新、削除 (CRUD) 操作のための Representational State Transfer (REST) に基づくプロトコルを提供することです。</span><span class="sxs-lookup"><span data-stu-id="f6038-107">The purpose of OData is to provide a protocol that is based on Representational State Transfer (REST) for create, read, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="f6038-108">OData は、さまざまなプログラムからの情報にアクセスするために、HTTP および JavaScript Object Notation (JSON) などの Web テクノロジーを適用します。</span><span class="sxs-lookup"><span data-stu-id="f6038-108">OData applies web technologies such as HTTP and JavaScript Object Notation (JSON) to provide access to information from various programs.</span></span> <span data-ttu-id="f6038-109">OData には次のメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="f6038-109">OData provides the following benefits:</span></span>

- <span data-ttu-id="f6038-110">これにより、開発者は RESTful Web サービスを使用してデータを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-110">It lets developers interact with data by using RESTful web services.</span></span>
- <span data-ttu-id="f6038-111">これにより、見つけやすい方法でデータを共有する簡単で一貫した方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-111">It provides a simple and uniform way to share data in a discoverable manner.</span></span>
- <span data-ttu-id="f6038-112">製品を越えた広範な統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f6038-112">It enables broad integration across products.</span></span>
- <span data-ttu-id="f6038-113">HTTP プロトコル スタックを使用して統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f6038-113">It enables integration by using the HTTP protocol stack.</span></span>

<span data-ttu-id="f6038-114">OData の詳細については、次の Web ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6038-114">For more information about OData, see the following webpages.</span></span>

| <span data-ttu-id="f6038-115">トピック</span><span class="sxs-lookup"><span data-stu-id="f6038-115">Topic</span></span>                                                               | <span data-ttu-id="f6038-116">Webpage</span><span class="sxs-lookup"><span data-stu-id="f6038-116">Webpage</span></span>                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="f6038-117">OData 標準</span><span class="sxs-lookup"><span data-stu-id="f6038-117">OData standards</span></span>                                                     | <https://www.odata.org/documentation/>                   |
| <span data-ttu-id="f6038-118">OData: Web、クラウド、モバイル デバイスなどのデータ アクセス</span><span class="sxs-lookup"><span data-stu-id="f6038-118">OData: Data access for the web, the cloud, mobile devices, and more</span></span> | <https://docs.microsoft.com/aspnet/web-api/overview/odata-support-in-aspnet-web-api/>    |

<span data-ttu-id="f6038-119">パブリック OData サービス エンドポイントにより、幅広いクライアントにわたって、一貫した方法でデータにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="f6038-119">The public OData service endpoint enables access to data in a consistent manner across a broad range of clients.</span></span> <span data-ttu-id="f6038-120">公開されているすべてのエンティティの一覧を表示するには、OData サービスのルート URLを開きます。</span><span class="sxs-lookup"><span data-stu-id="f6038-120">To see a list of all the entities that are exposed, open the OData service root URL.</span></span> <span data-ttu-id="f6038-121">システムのサービス ルートの URL の形式は **\[お客様の組織のルート URL\]/data** です。</span><span class="sxs-lookup"><span data-stu-id="f6038-121">The URL for the service root on your system has the following format: **\[Your organization's root URL\]/data**</span></span>

## <a name="addressing"></a><span data-ttu-id="f6038-122">アドレス指定</span><span class="sxs-lookup"><span data-stu-id="f6038-122">Addressing</span></span>
<span data-ttu-id="f6038-123">次のテーブルでは、フリート管理サンプルのリソースと対応する URL を示しています。</span><span class="sxs-lookup"><span data-stu-id="f6038-123">The following table describes the resources and the corresponding URLs in the Fleet Management sample.</span></span>


| <span data-ttu-id="f6038-124">リソース</span><span class="sxs-lookup"><span data-stu-id="f6038-124">Resource</span></span>            | <span data-ttu-id="f6038-125">URL</span><span class="sxs-lookup"><span data-stu-id="f6038-125">URL</span></span>                                                                     | <span data-ttu-id="f6038-126">説明</span><span class="sxs-lookup"><span data-stu-id="f6038-126">Description</span></span>                                                    |
|---------------------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f6038-127">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="f6038-127">Service endpoint</span></span>    | <span data-ttu-id="f6038-128">\[組織のルート URL\]/data/</span><span class="sxs-lookup"><span data-stu-id="f6038-128">\[Your organization's root URL\]/data/</span></span>                                  | <span data-ttu-id="f6038-129">OData エンティティのルート サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="f6038-129">The root service endpoint for OData entities</span></span>                   |
| <span data-ttu-id="f6038-130">エンティティ コレクション</span><span class="sxs-lookup"><span data-stu-id="f6038-130">Entity collection</span></span>   | <span data-ttu-id="f6038-131">\[組織のルート URL\]/data/Customers</span><span class="sxs-lookup"><span data-stu-id="f6038-131">\[Your organization's root URL\]/data/Customers</span></span>                         | <span data-ttu-id="f6038-132">すべての顧客のコレクション</span><span class="sxs-lookup"><span data-stu-id="f6038-132">The collection of all customers</span></span>                                |
| <span data-ttu-id="f6038-133">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f6038-133">Entity</span></span>              | <span data-ttu-id="f6038-134">\[組織のルート URL\]/data/Customers("\[キー\]")</span><span class="sxs-lookup"><span data-stu-id="f6038-134">\[Your organization's root URL\]/data/Customers("\[key\]")</span></span>              | <span data-ttu-id="f6038-135">エンティティのコレクションから 1 つのエンティティ</span><span class="sxs-lookup"><span data-stu-id="f6038-135">A single entity from the entity collection</span></span>                     |
| <span data-ttu-id="f6038-136">ナビゲーション プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6038-136">Navigation property</span></span> | <span data-ttu-id="f6038-137">\[組織のルート URL\]/data/Customers("\[キー\]")/Reservations</span><span class="sxs-lookup"><span data-stu-id="f6038-137">\[Your organization's root URL\]/data/Customers("\[key\]")/Reservations</span></span> | <span data-ttu-id="f6038-138">顧客からその顧客の引当までのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="f6038-138">The navigation from a customer to that customer's reservations</span></span> |
| <span data-ttu-id="f6038-139">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f6038-139">Property</span></span>            | <span data-ttu-id="f6038-140">\[組織のルート URL\]/data/Customers("\[キー\]")/FirstName</span><span class="sxs-lookup"><span data-stu-id="f6038-140">\[Your organization's root URL\]/data/Customers("\[key\]")/FirstName</span></span>    | <span data-ttu-id="f6038-141">顧客の名</span><span class="sxs-lookup"><span data-stu-id="f6038-141">The customer's first name</span></span>                                      |

## <a name="odata-services"></a><span data-ttu-id="f6038-142">OData サービス</span><span class="sxs-lookup"><span data-stu-id="f6038-142">OData services</span></span>
<span data-ttu-id="f6038-143">OData REST エンドポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="f6038-143">We provide an OData REST endpoint.</span></span> <span data-ttu-id="f6038-144">このエンドポイントは、アプリケーション オブジェクト ツリー (AOT) の **IsPublic** としてマークされているすべてのデータ エンティティを公開します。</span><span class="sxs-lookup"><span data-stu-id="f6038-144">This endpoint exposes all the data entities that are marked as **IsPublic** in the Application Object Tree (AOT).</span></span> <span data-ttu-id="f6038-145">ユーザーがデータを挿入およびシステムから取得するために使用できる完全な CRUD (作成、取得、更新、および削除) 機能をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f6038-145">It supports complete CRUD (create, retrieve, update, and delete) functionality that users can use to insert and retrieve data from the system.</span></span> <span data-ttu-id="f6038-146">この機能の詳細なラボは、LCS の方法論に基づいています。</span><span class="sxs-lookup"><span data-stu-id="f6038-146">Detailed labs for this feature are on the LCS methodology.</span></span>

<!--For more information, see the [Office Mix presentation about OData Services](https://mix.office.com/watch/1aym08mqyjghi).-->

<span data-ttu-id="f6038-147">OData サービスを使用するためのコード例は、「[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/ODataConsoleApplication)」です。</span><span class="sxs-lookup"><span data-stu-id="f6038-147">Code examples for consuming OData services are available in the [Microsoft Dynamics AX Integration GitHub repository](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/ODataConsoleApplication).</span></span>

### <a name="supported-features-from-the-odata-specification"></a><span data-ttu-id="f6038-148">OData 仕様からサポートされている機能</span><span class="sxs-lookup"><span data-stu-id="f6038-148">Supported features from the OData specification</span></span>

<span data-ttu-id="f6038-149">[OData 仕様](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html) に従って、OData サービスで使用可能な上位レベルの機能は次のとおりです.</span><span class="sxs-lookup"><span data-stu-id="f6038-149">The following are the high-level features that are enabled for the OData service, per the [OData specification](https://docs.oasis-open.org/odata/odata/v4.0/odata-v4.0-part1-protocol.html).</span></span>

- <span data-ttu-id="f6038-150">CRUD サポートは、転記、パッチ、挿入、および削除の HTTP 動詞サポートにより処理されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-150">CRUD support is handled through HTTP verb support for POST, PATCH, PUT, and DELETE.</span></span>
- <span data-ttu-id="f6038-151">利用可能なクエリ オプションは</span><span class="sxs-lookup"><span data-stu-id="f6038-151">Available query options are:</span></span>

    - <span data-ttu-id="f6038-152">$filter</span><span class="sxs-lookup"><span data-stu-id="f6038-152">$filter</span></span>
    - <span data-ttu-id="f6038-153">$count</span><span class="sxs-lookup"><span data-stu-id="f6038-153">$count</span></span>
    - <span data-ttu-id="f6038-154">$orderby</span><span class="sxs-lookup"><span data-stu-id="f6038-154">$orderby</span></span>
    - <span data-ttu-id="f6038-155">$skip</span><span class="sxs-lookup"><span data-stu-id="f6038-155">$skip</span></span>
    - <span data-ttu-id="f6038-156">$top</span><span class="sxs-lookup"><span data-stu-id="f6038-156">$top</span></span>
    - <span data-ttu-id="f6038-157">$expand</span><span class="sxs-lookup"><span data-stu-id="f6038-157">$expand</span></span>
    - <span data-ttu-id="f6038-158">$select</span><span class="sxs-lookup"><span data-stu-id="f6038-158">$select</span></span>

- <span data-ttu-id="f6038-159">OData サービスでは、最大ページ サイズが 1,000 のサービス ドリブン ページングをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f6038-159">The OData service supports serving driven paging with a maximum page size of 1,000.</span></span>

<span data-ttu-id="f6038-160">詳細については、以下を参照してください: [エンティティにバインドされている OData アクション](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398355)</span><span class="sxs-lookup"><span data-stu-id="f6038-160">For more information, see: [OData actions that are bound to entities](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398355).</span></span>

#### <a name="filter-details"></a><span data-ttu-id="f6038-161">フィルター詳細</span><span class="sxs-lookup"><span data-stu-id="f6038-161">Filter details</span></span>

<span data-ttu-id="f6038-162">$filter には組み込みの演算子があります。</span><span class="sxs-lookup"><span data-stu-id="f6038-162">There are built-in operators for $filter:</span></span>

- <span data-ttu-id="f6038-163">次の値と等しい</span><span class="sxs-lookup"><span data-stu-id="f6038-163">Equals</span></span>
- <span data-ttu-id="f6038-164">等しくない</span><span class="sxs-lookup"><span data-stu-id="f6038-164">Not equals</span></span>
- <span data-ttu-id="f6038-165">次の値より大きい</span><span class="sxs-lookup"><span data-stu-id="f6038-165">Greater than</span></span>
- <span data-ttu-id="f6038-166">次の値以上</span><span class="sxs-lookup"><span data-stu-id="f6038-166">Greater than or equal</span></span>
- <span data-ttu-id="f6038-167">次の値より小さい</span><span class="sxs-lookup"><span data-stu-id="f6038-167">Less than</span></span>
- <span data-ttu-id="f6038-168">次の値以下</span><span class="sxs-lookup"><span data-stu-id="f6038-168">Less than or equal</span></span>
- <span data-ttu-id="f6038-169">かつ</span><span class="sxs-lookup"><span data-stu-id="f6038-169">And</span></span>
- <span data-ttu-id="f6038-170">又は</span><span class="sxs-lookup"><span data-stu-id="f6038-170">Or</span></span>
- <span data-ttu-id="f6038-171">ない</span><span class="sxs-lookup"><span data-stu-id="f6038-171">Not</span></span>
- <span data-ttu-id="f6038-172">追加</span><span class="sxs-lookup"><span data-stu-id="f6038-172">Addition</span></span>
- <span data-ttu-id="f6038-173">減算</span><span class="sxs-lookup"><span data-stu-id="f6038-173">Subtraction</span></span>
- <span data-ttu-id="f6038-174">乗算</span><span class="sxs-lookup"><span data-stu-id="f6038-174">Multiplication</span></span>
- <span data-ttu-id="f6038-175">区分</span><span class="sxs-lookup"><span data-stu-id="f6038-175">Division</span></span>

<span data-ttu-id="f6038-176">また、**Contains** オプションを $filter 要求とともに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f6038-176">You can also use the **Contains** option with $filter requests.</span></span> <span data-ttu-id="f6038-177">これは、ワイルドカード文字として実装されています。</span><span class="sxs-lookup"><span data-stu-id="f6038-177">It has been implemented as a wildcard character.</span></span> <span data-ttu-id="f6038-178">例: `http://host/service/EntitySet?$filter=StringField eq '\*retail\*'`</span><span class="sxs-lookup"><span data-stu-id="f6038-178">For example: `http://host/service/EntitySet?$filter=StringField eq '\*retail\*'`</span></span>

<span data-ttu-id="f6038-179">詳細については、「[OData 演算子](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part2-url-conventions/odata-v4.0-errata02-os-part2-url-conventions-complete.html#_Toc406398096)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6038-179">For more information, see [OData operators](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part2-url-conventions/odata-v4.0-errata02-os-part2-url-conventions-complete.html#_Toc406398096).</span></span>

#### <a name="batch-requests"></a><span data-ttu-id="f6038-180">バッチ要求</span><span class="sxs-lookup"><span data-stu-id="f6038-180">Batch requests</span></span>
<span data-ttu-id="f6038-181">OData サービスでは、バッチ要求がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f6038-181">Batch requests are supported in the OData service.</span></span> <span data-ttu-id="f6038-182">詳細については、「[OData バッチ要求](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398359)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6038-182">For more information, see [OData batch requests](https://docs.oasis-open.org/odata/odata/v4.0/errata02/os/complete/part1-protocol/odata-v4.0-errata02-os-part1-protocol-complete.html#_Toc406398359).</span></span>

#### <a name="metadata-annotations"></a><span data-ttu-id="f6038-183">メタデータの注釈</span><span class="sxs-lookup"><span data-stu-id="f6038-183">Metadata annotations</span></span>

<span data-ttu-id="f6038-184">/data/$ メタデータは、注釈を提供します。</span><span class="sxs-lookup"><span data-stu-id="f6038-184">/data/$metadata provides annotations.</span></span> <span data-ttu-id="f6038-185">EnumType は、$metadata でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f6038-185">EnumType is support in $metadata.</span></span>

![EnumType メタデータ](./media/metadata.png)

### <a name="cross-company-behavior"></a><span data-ttu-id="f6038-187">会社間動作</span><span class="sxs-lookup"><span data-stu-id="f6038-187">Cross-company behavior</span></span>

<span data-ttu-id="f6038-188">既定では、OData はユーザーの既定の会社に属しているデータのみを返します。</span><span class="sxs-lookup"><span data-stu-id="f6038-188">By default, OData returns only data that belongs to the user's default company.</span></span> <span data-ttu-id="f6038-189">ユーザーの既定の会社以外のデータを表示するには、**?cross-company=true** クエリ オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="f6038-189">To see data from outside the user's default company, specify the **?cross-company=true** query option.</span></span> <span data-ttu-id="f6038-190">このオプションは、ユーザーがアクセスできるすべての会社のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="f6038-190">This option will return data from all companies that the user has access to.</span></span>

<span data-ttu-id="f6038-191">**例:** `http://[baseURI\]/data/FleetCustomers?cross-company=true`</span><span class="sxs-lookup"><span data-stu-id="f6038-191">**Example:** `http://[baseURI\]/data/FleetCustomers?cross-company=true`</span></span>

<span data-ttu-id="f6038-192">既定の会社ではない特定の会社ごとにフィルター処理するには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="f6038-192">To filter by a particular company that isn't your default company, use the following syntax:</span></span>

`http://[baseURI\]/data/FleetCustomers?$filter=dataAreaId eq 'usrt'&cross-company=true`

### <a name="validate-methods"></a><span data-ttu-id="f6038-193">メソッドの検証</span><span class="sxs-lookup"><span data-stu-id="f6038-193">Validate methods</span></span>

<span data-ttu-id="f6038-194">次のテーブルは、OData スタックが対応するデータ エンティティで暗黙的に呼び出す検証方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-194">The following table summarizes the validate methods that the OData stack calls implicitly on the corresponding data entity.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f6038-195">OData</span><span class="sxs-lookup"><span data-stu-id="f6038-195">OData</span></span></th>
<th><span data-ttu-id="f6038-196">メソッド (呼び出される順序で一覧表示されます)</span><span class="sxs-lookup"><span data-stu-id="f6038-196">Methods (listed in the order in which they are called)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6038-197">新規</span><span class="sxs-lookup"><span data-stu-id="f6038-197">Create</span></span></td>
<td><ol>
<li><span data-ttu-id="f6038-198"><strong>クリア ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-198"><strong>Clear()</strong></span></span></li>
<li><span data-ttu-id="f6038-199"><strong>Initvalue()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-199"><strong>Initvalue()</strong></span></span></li>
<li><span data-ttu-id="f6038-200"><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</span><span class="sxs-lookup"><span data-stu-id="f6038-200"><strong>PropertyInfo.SetValue()</strong> for all specified fields in the request</span></span></li>
<li><span data-ttu-id="f6038-201"><strong>Validatefield()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-201"><strong>Validatefield()</strong></span></span></li>
<li><span data-ttu-id="f6038-202"><strong>Defaultrow</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-202"><strong>Defaultrow</strong></span></span></li>
<li><span data-ttu-id="f6038-203"><strong>Validatewrite()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-203"><strong>Validatewrite()</strong></span></span></li>
<li><span data-ttu-id="f6038-204"><strong>書き込み ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-204"><strong>Write()</strong></span></span></li>
</ol></td>
</tr>
<tr>
<td><span data-ttu-id="f6038-205">更新</span><span class="sxs-lookup"><span data-stu-id="f6038-205">Update</span></span></td>
<td><ol>
<li><span data-ttu-id="f6038-206"><strong>Forupdate()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-206"><strong>Forupdate()</strong></span></span></li>
<li><span data-ttu-id="f6038-207"><strong>再表示 ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-207"><strong>Reread()</strong></span></span></li>
<li><span data-ttu-id="f6038-208"><strong>クリア ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-208"><strong>Clear()</strong></span></span></li>
<li><span data-ttu-id="f6038-209"><strong>Initvalue()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-209"><strong>Initvalue()</strong></span></span></li>
<li><span data-ttu-id="f6038-210"><strong>PropertyInfo.SetValue()</strong> 要求の指定されたすべてのフィールド</span><span class="sxs-lookup"><span data-stu-id="f6038-210"><strong>PropertyInfo.SetValue()</strong> for all specified fields in the request</span></span></li>
<li><span data-ttu-id="f6038-211"><strong>Validatefield()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-211"><strong>Validatefield()</strong></span></span></li>
<li><span data-ttu-id="f6038-212"><strong>Defaultrow()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-212"><strong>Defaultrow()</strong></span></span></li>
<li><span data-ttu-id="f6038-213"><strong>Validatewrite()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-213"><strong>Validatewrite()</strong></span></span></li>
<li><span data-ttu-id="f6038-214"><strong>書き込み ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-214"><strong>Write()</strong></span></span></li>
</ol></td>
</tr>
<tr>
<td><span data-ttu-id="f6038-215">消去</span><span class="sxs-lookup"><span data-stu-id="f6038-215">Delete</span></span></td>
<td><ol>
<li><span data-ttu-id="f6038-216"><strong>Forupdate()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-216"><strong>Forupdate()</strong></span></span></li>
<li><span data-ttu-id="f6038-217"><strong>再表示 ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-217"><strong>Reread()</strong></span></span></li>
<li><span data-ttu-id="f6038-218"><strong>checkRestrictedDeleteActions()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-218"><strong>checkRestrictedDeleteActions()</strong></span></span></li>
<li><span data-ttu-id="f6038-219"><strong>Validatedelete()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-219"><strong>Validatedelete()</strong></span></span></li>
<li><span data-ttu-id="f6038-220"><strong>削除 ()</strong></span><span class="sxs-lookup"><span data-stu-id="f6038-220"><strong>Delete()</strong></span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="exposing-odata-entities"></a><span data-ttu-id="f6038-221">OData エンティティを公開</span><span class="sxs-lookup"><span data-stu-id="f6038-221">Exposing OData entities</span></span>
<span data-ttu-id="f6038-222">OData エンティティは、更新可能なビューの概念に基づいています。</span><span class="sxs-lookup"><span data-stu-id="f6038-222">OData entities are based on the concept of an updatable view.</span></span> <span data-ttu-id="f6038-223">更新可能なビューの **IsPublic** プロパティが **TRUE** 設定されているとき、そのビューは最上位レベルの OData エンティティとして公開されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-223">When the **IsPublic** property for an updatable view is set to **TRUE**, that view is exposed as a top-level OData entity.</span></span>

## <a name="setting-navigation-properties-between-odata-entities"></a><span data-ttu-id="f6038-224">OData エンティティ間のナビゲーション プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="f6038-224">Setting navigation properties between OData entities</span></span>
<span data-ttu-id="f6038-225">OData エンティティ間のリンクは、ナビゲーション プロパティによって記述されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-225">Links between OData entities are described by a navigation property.</span></span> <span data-ttu-id="f6038-226">ナビゲーション プロパティでは、アソシエーションの一方から他方までのナビゲーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f6038-226">Navigation properties describe the navigation from one end of an association to the other end.</span></span>

#### <a name="adding-actions-on-odata-entities"></a><span data-ttu-id="f6038-227">OData エンティティでのアクションの追加</span><span class="sxs-lookup"><span data-stu-id="f6038-227">Adding actions on OData entities</span></span>
<span data-ttu-id="f6038-228">アクションで動作をデータ モデルに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-228">Actions let you inject behaviors into the data model.</span></span> <span data-ttu-id="f6038-229">アクションを追加するには、更新可能なビューにメソッドを追加し、そのメソッドを特定の属性で修飾します。</span><span class="sxs-lookup"><span data-stu-id="f6038-229">To add actions, add a method to the updatable view, and decorate that method with specific attributes.</span></span> <span data-ttu-id="f6038-230">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-230">Here is an example.</span></span>

```
[SysODataActionAttribute("CalcMaintenanceDuration", true)]
public int CalculateMaintenanceDuration()
{
    //do something
    return 0;
}
```

<span data-ttu-id="f6038-231">この例では、**SysODataActionAttribute** クラスがアクションとして公開されている **CalculateMaintenanceDuration** メソッドを修飾します。</span><span class="sxs-lookup"><span data-stu-id="f6038-231">In this example, the **SysODataActionAttribute** class decorates the **CalculateMaintenanceDuration** method that is exposed as an action.</span></span> <span data-ttu-id="f6038-232">属性の最初の引数は公開されているアクションの名前で、2 番目の引数はこのアクションが常に利用可能かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-232">The first argument of the attribute is the publicly exposed name of the action, and the second argument indicates whether this action is always available.</span></span> <span data-ttu-id="f6038-233">アクションとして公開されているメソッドは、任意のプリミティブ型または別のパブリックの更新可能なビューを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="f6038-233">Methods that are exposed as actions can return any primitive type or another public updatable view.</span></span> <span data-ttu-id="f6038-234">このメソッドが公開されると、OData $ メタデータに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-234">After this method is exposed, it appears in the OData $metadata.</span></span> <span data-ttu-id="f6038-235">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-235">Here is an example.</span></span>

```
<Action Name="CalcMaintenanceDuration" IsBound="true">
    <Parameter Name="ViewMaintenance" Type="Microsoft.Dynamics.AX.Resources.ViewMaintenance"/>
    <ReturnType Type="Edm.String" />
</Action>

```

<span data-ttu-id="f6038-236">次の OData アクションの例では、パラメーターで取り、リストを返します。</span><span class="sxs-lookup"><span data-stu-id="f6038-236">The following example of an OData action takes in a parameter and returns a list.</span></span>

```
[SysODataActionAttribute("GetColors", true),
    SysODataCollectionAttribute("return", Types::Record, "CarColor")]
public List GetColorsByAvailability(boolean onlyAvailableVehicles)
{
    List returnList = new List(Types::Record);
    // do something
    return returnList;
}
```

<span data-ttu-id="f6038-237">この例では、OData は **SysODataCollectionAttribute** クラスによって X++ から強く定型化されたコレクションを公開できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-237">In this example, the **SysODataCollectionAttribute** class enables OData to expose strongly typed collections from X++.</span></span> <span data-ttu-id="f6038-238">このクラスは次の 3 つのパラメーターを取ります。</span><span class="sxs-lookup"><span data-stu-id="f6038-238">This class takes in three parameters:</span></span>

- <span data-ttu-id="f6038-239">リストを示すパラメーターの名前 (メソッドの戻り値として **return** を返します)。</span><span class="sxs-lookup"><span data-stu-id="f6038-239">The name of the parameter that is a list (Use **return** for the return value of the method.)</span></span>
- <span data-ttu-id="f6038-240">この一覧のメンバーの X++ タイプ</span><span class="sxs-lookup"><span data-stu-id="f6038-240">The X++ type of the members of this list</span></span>
- <span data-ttu-id="f6038-241">コレクションに含まれている OData リソースのパブリック名</span><span class="sxs-lookup"><span data-stu-id="f6038-241">The public name of the OData resource that is contained in the collection</span></span>

<span data-ttu-id="f6038-242">これらのアクションが公開された後、サービス ルートの URL から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f6038-242">After these actions are exposed, they can be invoked from the service root URL.</span></span>

<span data-ttu-id="f6038-243">ソース コード内の **SysODataActionAttribute** 属性を検索することにより、データ エンティティ上で定義されたアクションを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f6038-243">You can find actions that are defined on data entities by searching for the **SysODataActionAttribute** attribute in the source code.</span></span>

## <a name="querying-or-browsing-an-odata-endpoint"></a><span data-ttu-id="f6038-244">OData エンドポイントの照会や参照</span><span class="sxs-lookup"><span data-stu-id="f6038-244">Querying or browsing an OData endpoint</span></span>
<span data-ttu-id="f6038-245">OData は、データベースに対して豊富なクエリを作成できる SQL に似た言語を有効にして、結果に希望するデータ項目のみが含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="f6038-245">OData enables an SQL-like language that lets you create rich queries against the database, so that the results include only the data items that you want.</span></span> <span data-ttu-id="f6038-246">クエリを作成するには、リソース パスに条件を追加します。</span><span class="sxs-lookup"><span data-stu-id="f6038-246">To create a query, append criteria to the resource path.</span></span> <span data-ttu-id="f6038-247">たとえば、ブラウザで次のクエリ オプションを加えることによって、**顧客**エンティティ コレクションのクエリを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f6038-247">For example, you can query the **Customers** entity collection by appending the following query options in your browser.</span></span>

| <span data-ttu-id="f6038-248">URL</span><span class="sxs-lookup"><span data-stu-id="f6038-248">URL</span></span>                                                                        | <span data-ttu-id="f6038-249">説明</span><span class="sxs-lookup"><span data-stu-id="f6038-249">Description</span></span> |
|----------------------------------------------------------------------------|-------------|
| <span data-ttu-id="f6038-250">\[組織のルート URL\]/data/Customers</span><span class="sxs-lookup"><span data-stu-id="f6038-250">\[Your organization's root URL\]/data/Customers</span></span>                            | <span data-ttu-id="f6038-251">すべての顧客の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-251">List all the customers.</span></span> |
| <span data-ttu-id="f6038-252">\[組織のルート URL\]/data/Customers?$top=3</span><span class="sxs-lookup"><span data-stu-id="f6038-252">\[Your organization's root URL\]/data/Customers?$top=3</span></span>                     | <span data-ttu-id="f6038-253">最初の 3 つのレコードを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-253">List the first three records.</span></span> |
| <span data-ttu-id="f6038-254">\[組織のルート URL\]/data/Customers?$select=FirstName,LastName</span><span class="sxs-lookup"><span data-stu-id="f6038-254">\[Your organization's root URL\]/data/Customers?$select=FirstName,LastName</span></span> | <span data-ttu-id="f6038-255">すべての顧客の一覧を表示しますが、姓名のプロパティだけを表示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-255">List all the customers, but show only the first name and last name properties.</span></span> |
| <span data-ttu-id="f6038-256">\[組織のルート URL\]/data/Customers?$format=json</span><span class="sxs-lookup"><span data-stu-id="f6038-256">\[Your organization's root URL\]/data/Customers?$format=json</span></span>               | <span data-ttu-id="f6038-257">JavaScript クライアントとやり取りするために使用できる JSON 形式ですべての顧客の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="f6038-257">List all the customers in a JSON format that can be used to interact with JavaScript clients.</span></span> |

<span data-ttu-id="f6038-258">OData プロトコルは、エンティティで多くの似たフィルター処理とクエリ オプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f6038-258">The OData protocol supports many similar filtering and querying options on entities.</span></span> <span data-ttu-id="f6038-259">クエリ オプションの完全なセットについては、[Windows Communication Foundation](https://msdn.microsoft.com/library/ff478141.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6038-259">For the full set of query options, see [Windows Communication Foundation](https://msdn.microsoft.com/library/ff478141.aspx).</span></span>

## <a name="authentication"></a><span data-ttu-id="f6038-260">認証</span><span class="sxs-lookup"><span data-stu-id="f6038-260">Authentication</span></span>
<span data-ttu-id="f6038-261">OData は、サーバーと同じ認証スタック上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="f6038-261">OData sits on the same authentication stack as the server.</span></span> <span data-ttu-id="f6038-262">認証の詳細については、[サービス エンドポイント](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f6038-262">For more information about the authentication, see [Service endpoints](services-home-page.md).</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="f6038-263">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="f6038-263">Tips and tricks</span></span>

### <a name="run-multiple-requests-in-a-single-transaction"></a><span data-ttu-id="f6038-264">1 つのトランザクションで複数の要求を実行</span><span class="sxs-lookup"><span data-stu-id="f6038-264">Run multiple requests in a single transaction</span></span>
<span data-ttu-id="f6038-265">OData バッチ フレームワークは、*変更セット*を使用します。</span><span class="sxs-lookup"><span data-stu-id="f6038-265">The OData batch framework uses *changesets*.</span></span> <span data-ttu-id="f6038-266">各変更セットには、単一アトミック ユニットとして扱われるべき要求のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f6038-266">Each changeset contains a list of requests that should be treated as single atomic unit.</span></span> <span data-ttu-id="f6038-267">つまり、すべての要求が正常に実行されるか、要求が失敗した場合はすべての要求が正常に実行されません。</span><span class="sxs-lookup"><span data-stu-id="f6038-267">In other words, either all the requests are run successfully or, if any request fails, none of the requests are run successfully.</span></span> <span data-ttu-id="f6038-268">次の例は、単一の変更セット内に要求のリストを持つバッチ要求を送信する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f6038-268">The following example shows how to send a batch request that has a list of requests in a single changeset.</span></span>

<span data-ttu-id="f6038-269">**SaveChanges()** の **SaveChangesOptions.BatchWithSingleChangeset** オプションを使用すると、単一の変更セットにすべての要求がバンドルされていることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-269">The **SaveChangesOptions.BatchWithSingleChangeset** option in **SaveChanges()** helps guarantee that all requests are bundled into a single changeset.</span></span>

```
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
```

### <a name="prevent-unset-records-from-being-posted-when-you-use-an-odata-client"></a><span data-ttu-id="f6038-270">OData クライアントを使用する場合に設定されていないレコードが転記されることを防止する</span><span class="sxs-lookup"><span data-stu-id="f6038-270">Prevent unset records from being posted when you use an OData client</span></span>
<span data-ttu-id="f6038-271">例 1 に示すように、OData クライアントを使用して新しいレコードを作成するときは、設定されていないプロパティが要求の本体に含まれ、既定値がそれらのプロパティに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f6038-271">When you create a new record by using an OData client, as shown in example 1, properties that aren't set are included in the body of the request, and default values are assigned to them.</span></span> <span data-ttu-id="f6038-272">この動作を回避し、明示的に設定されたプロパティのみをポストするには、例 2 に示すように、**SaveChanges()** の **SaveChangesOptions.PostOnlySetProperties** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f6038-272">To prevent this behavior and post only properties that are set explicitly, use the **SaveChangesOptions.PostOnlySetProperties** option in **SaveChanges()**, as shown in example 2.</span></span>

<span data-ttu-id="f6038-273">**例 1**</span><span class="sxs-lookup"><span data-stu-id="f6038-273">**Example 1**</span></span>

```
public static void CreateVendor(Resources context)
{
    var vendorCollection = new DataServiceCollection<Vendor>(context);
    var vendor = new Vendor();
    vendorCollection.Add(vendor);
    // set properties
    context.SaveChanges();
}
```

<span data-ttu-id="f6038-274">**例 2**</span><span class="sxs-lookup"><span data-stu-id="f6038-274">**Example 2**</span></span>

```
public static void CreateVendor(Resources context)
{
    var vendorCollection = new DataServiceCollection<Vendor>(context);
    var vendor = new Vendor();
    vendorCollection.Add(vendor);
    // set properties

    // Save specifying PostOnlySetProperties flag
    context.SaveChanges(SaveChangesOptions.PostOnlySetProperties);
}
```

### <a name="handling-duplicate-names-between-enums-and-entities-in-metadata"></a><span data-ttu-id="f6038-275">メタデータ内の列挙とエンティティ間の重複する名前の処理</span><span class="sxs-lookup"><span data-stu-id="f6038-275">Handling duplicate names between enums and entities in metadata</span></span>
<span data-ttu-id="f6038-276">列挙とエンティティが同じ名前を共有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f6038-276">There are instances where enums and entities share the same name.</span></span> <span data-ttu-id="f6038-277">この名前の重複により、OData クライアント コードの生成エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f6038-277">This name duplication results in OData client code generation errors.</span></span> <span data-ttu-id="f6038-278">このエラーから回復するには [GitHub のヘルパー コード](https://github.com/Microsoft/Dynamics-AX-Integration/blob/master/ServiceSamples/ODataConsoleApplication/MetadataDocumentValidator.cs) を、削除しなければならない重複する名前のインスタンスを識別するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-278">To recover from this error, the [helper code in gitHub](https://github.com/Microsoft/Dynamics-AX-Integration/blob/master/ServiceSamples/ODataConsoleApplication/MetadataDocumentValidator.cs) can be used to identify duplicate name instances that must be removed.</span></span> <span data-ttu-id="f6038-279">生成されたメタデータ ドキュメントは、クライアント側で Odata ロジックの処理を進めるために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f6038-279">The generated metadata document can be used for further processing of the Odata logic on the client side.</span></span>

### <a name="array-fields"></a><span data-ttu-id="f6038-280">配列フィールド</span><span class="sxs-lookup"><span data-stu-id="f6038-280">Array fields</span></span>
<span data-ttu-id="f6038-281">OData はエンティティで配列フィールドをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f6038-281">OData does not support array fields in entities.</span></span> <span data-ttu-id="f6038-282">OData で使用されるエンティティを設計するときにこれを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6038-282">This must be taken into consideration when designing entities that will be used with OData.</span></span>