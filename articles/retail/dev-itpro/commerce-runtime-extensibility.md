---
title: Commerce Runtime (CRT) および Retail サーバーの拡張機能
description: このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。 また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。
author: mugunthanm
manager: AnnBe
ms.date: 07/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5536c6f8dbc6885924397565247fe9bb25a109ef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537575"
---
# <a name="commerce-runtime-crt-and-retail-server-extensibility"></a><span data-ttu-id="ed9f4-105">Commerce Runtime (CRT) および Retail サーバーの拡張機能</span><span class="sxs-lookup"><span data-stu-id="ed9f4-105">Commerce runtime (CRT) and Retail Server extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed9f4-106">このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-106">This topic describes various ways that you can extend the commerce runtime (CRT) and Retail Server.</span></span> <span data-ttu-id="ed9f4-107">拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-107">It explains the concept of extension properties, and shows how to add them to a CRT entity both with and without persistence.</span></span> <span data-ttu-id="ed9f4-108">また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-108">It also shows how to add an action to a Retail Server controller and add a controller for an entity.</span></span>

<span data-ttu-id="ed9f4-109">CRT にはコア ビジネス ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-109">CRT contains the core business logic.</span></span> <span data-ttu-id="ed9f4-110">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-110">If you want to add or modify any business logic, you should customize CRT.</span></span> <span data-ttu-id="ed9f4-111">C# を使用して、すべての CRT コードが開発およびコンパイルされ、クラス ライブラリとしてリリースされます (.NET アセンブリ)。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-111">All the CRT code is developed by using C#, and it's then compiled and released as class libraries (.NET assemblies).</span></span> <span data-ttu-id="ed9f4-112">小売販売時点管理 (POS) はシン クライアントです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-112">Retail point of sale (POS) is a thin client.</span></span> <span data-ttu-id="ed9f4-113">すべてのビジネス ロジックは、CRT で行われます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-113">All the business logic is done in CRT.</span></span> <span data-ttu-id="ed9f4-114">POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-114">POS calls CRT to perform any business logic, and CRT processes the information and then sends it back to POS.</span></span> 

<span data-ttu-id="ed9f4-115">すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-115">Every CRT service consists of a group of one or more requests and responses.</span></span> <span data-ttu-id="ed9f4-116">POS で作業する際はいつでも、POSは Retail サーバーに要求を送り、Retail サーバーは CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-116">Any time that you do something in POS, POS sends a request to Retail Server, and Retail Server calls CRT.</span></span> <span data-ttu-id="ed9f4-117">続いて CRT は要求を処理し、応答を送り返します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-117">CRT then processes the request and sends back the response.</span></span>

<span data-ttu-id="ed9f4-118">たとえば、CRT の顧客サービスには、顧客関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-118">For example, the Customer service in CRT contains all the customer-related requests and responses, each of which is run in a different flow.</span></span> <span data-ttu-id="ed9f4-119">同様に、CRT の製品サービスには製品に関連するすべての要求と応答が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-119">Likewise, the Product service in CRT contain all the product-related requests and responses.</span></span> <span data-ttu-id="ed9f4-120">次の表に、顧客サービスの要求を示します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-120">The following table shows the requests in the Customer service.</span></span>

| <span data-ttu-id="ed9f4-121">要求</span><span class="sxs-lookup"><span data-stu-id="ed9f4-121">Request</span></span>                                      | <span data-ttu-id="ed9f4-122">目的</span><span class="sxs-lookup"><span data-stu-id="ed9f4-122">Purpose</span></span>                                                                          |
|----------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed9f4-123">SaveCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-123">SaveCustomerServiceRequest</span></span>                   | <span data-ttu-id="ed9f4-124">この要求は、POS から顧客を保存する場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-124">This request is called when you save a customer from POS.</span></span>                        |
| <span data-ttu-id="ed9f4-125">GetCustomersServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-125">GetCustomersServiceRequest</span></span>                   | <span data-ttu-id="ed9f4-126">この要求は、選択した顧客の詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-126">This request is used to get the details of the selected customer.</span></span>                |
| <span data-ttu-id="ed9f4-127">CustomersSearchServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-127">CustomersSearchServiceRequest</span></span>                | <span data-ttu-id="ed9f4-128">この要求は、POS から顧客検索を行う場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-128">This request is run when you do a customer search from POS.</span></span>                      |
| <span data-ttu-id="ed9f4-129">GetCustomerGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-129">GetCustomerGroupsServiceRequest</span></span>              | <span data-ttu-id="ed9f4-130">この要求は、顧客グループの詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-130">This request is used to get the details of the customer group.</span></span>                   |
| <span data-ttu-id="ed9f4-131">InitiateLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-131">InitiateLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="ed9f4-132">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-132">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="ed9f4-133">FinalizeLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-133">FinalizeLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="ed9f4-134">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-134">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="ed9f4-135">UnlinkFromExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-135">UnlinkFromExistingCustomerServiceRequest</span></span>     | <span data-ttu-id="ed9f4-136">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-136">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="ed9f4-137">GetCustomerBalanceServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-137">GetCustomerBalanceServiceRequest</span></span>             | <span data-ttu-id="ed9f4-138">この要求は、顧客勘定の残高を取得します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-138">This request gets the balance for the customer account.</span></span>                          |
| <span data-ttu-id="ed9f4-139">GetOrderHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-139">GetOrderHistoryServiceRequest</span></span>                | <span data-ttu-id="ed9f4-140">この要求は、顧客の注文履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-140">This request gets the customer's order history.</span></span>                                  |
| <span data-ttu-id="ed9f4-141">GetPurchaseHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-141">GetPurchaseHistoryServiceRequest</span></span>             | <span data-ttu-id="ed9f4-142">この要求は、顧客の最近の購入履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-142">This request gets the history of the customer's recent purchases.</span></span>                |
| <span data-ttu-id="ed9f4-143">CustomerSearchByFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-143">CustomerSearchByFieldsServiceRequest</span></span>         | <span data-ttu-id="ed9f4-144">フィールド (ヒント検索) を使用して顧客を検索する際に、この要求が実行されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-144">This request is run when you search for customers by using fields (hint search).</span></span> |
| <span data-ttu-id="ed9f4-145">GetCustomerSearchFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="ed9f4-145">GetCustomerSearchFieldsServiceRequest</span></span>        | <span data-ttu-id="ed9f4-146">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-146">This request gets the list of customer search fields (hint fields).</span></span>              |

<span data-ttu-id="ed9f4-147">**CRT がサポートする拡張子パターンのタイプ**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-147">**Types of extension patterns that CRT supports**</span></span>

<span data-ttu-id="ed9f4-148">CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-148">Before you learn about the CRT extension patterns, you should understand how a CRT extension can be created.</span></span> <span data-ttu-id="ed9f4-149">CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-149">CRT is just a collection of C# class libraries (.NET assemblies).</span></span> <span data-ttu-id="ed9f4-150">C# でクラス ライブラリ プロジェクトを作成し、次の表に示すパターンを使用してすべての CRT 拡張を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-150">You can create a class library project in C# and do all the CRT extension by using the patterns that are shown in the following table.</span></span> <span data-ttu-id="ed9f4-151">これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-151">Always use the samples that Microsoft provides as template for your extension, because these samples have the correct assembly references, Microsoft .NET Framework version, output type, and build parameters.</span></span> <span data-ttu-id="ed9f4-152">また、他のすべての必須パラメーターがコンフィギュレーション済みです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-152">Additionally, all the other required parameters are preconfigured.</span></span> <span data-ttu-id="ed9f4-153">同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-153">You can find the CRT sample extension in the Retail software development kit (SDK), at …\\RetailSDK\\SampleExtensions\\CommerceRuntime.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ed9f4-154">拡張機能のパターン</span><span class="sxs-lookup"><span data-stu-id="ed9f4-154">Extensibility pattern</span></span></th>
<th><span data-ttu-id="ed9f4-155">目的</span><span class="sxs-lookup"><span data-stu-id="ed9f4-155">Purpose</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ed9f4-156">新しい CRT サービスの作成</span><span class="sxs-lookup"><span data-stu-id="ed9f4-156">Create a new CRT service</span></span></td>
<td><span data-ttu-id="ed9f4-157">新機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-157">Create a new functionality/feature.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed9f4-158">既存のサービスを上書きする</span><span class="sxs-lookup"><span data-stu-id="ed9f4-158">Override existing Service</span></span></td>
<td>
<p><span data-ttu-id="ed9f4-159">完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-159">You can completely override existing functionality or customize it according to your business flow.</span></span></p>
<p><span data-ttu-id="ed9f4-160">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-160">Here are some examples:</span></span>
<ul>
<li><span data-ttu-id="ed9f4-161">POS 検索機能を上書きして、ローカル データベースまたは本社で検索するのではなく、外部システムから検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-161">You want to override the POS search functionality to search from an external system instead of searching in a local database or HQ.</span></span> <span data-ttu-id="ed9f4-162">または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-162">Alternatively, you can do an override, call the standard functionality, and do some additional custom logic.</span></span></li>
<li><span data-ttu-id="ed9f4-163">ローカル データベースまたは HQ、および外部システムを検索した後、最後に結果をマージまたは変更します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-163">Search for a customer in a local database or HQ, and in an external system, and then finally merge or modify the result.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ed9f4-164">トリガー</span><span class="sxs-lookup"><span data-stu-id="ed9f4-164">Triggers</span></span></td>
<td>
<p><span data-ttu-id="ed9f4-165">任意の要求の前後に追加ロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-165">You can execute additional logic before or after any request.</span></span></p>
<p><span data-ttu-id="ed9f4-166">前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-166">In the pre-trigger, you can do some validation, custom logic, and so on.</span></span></p>
<p><span data-ttu-id="ed9f4-167">ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-167">In the post-trigger, you can add some custom information to the request and send it to POS.</span></span> <span data-ttu-id="ed9f4-168">または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-168">Alternatively, you can modify the result that is returned from the standard functionality or do some additional business logic.</span></span></p>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ed9f4-169">拡張プロパティ</span><span class="sxs-lookup"><span data-stu-id="ed9f4-169">Extension properties</span></span></td>
<td>
<p><span data-ttu-id="ed9f4-170">任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-170">You can add custom properties to any CRT entity and send it to POS.</span></span> <span data-ttu-id="ed9f4-171">拡張プロパティはキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-171">Extension properties are key-value pairs.</span></span> <span data-ttu-id="ed9f4-172">POS で拡張プロパティを設定すると、CRT で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-172">If you set an extension property in POS, it will be available in CRT.</span></span> <span data-ttu-id="ed9f4-173">同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-173">Likewise, if you set an extension property in CRT, it will be available in POS.</span></span> <span data-ttu-id="ed9f4-174">また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-174">You can also set extension properties at the level of the request, the response, or the request context.</span></span> <span data-ttu-id="ed9f4-175">既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-175">By default, extension properties aren't stored in and read from the database.</span></span> <span data-ttu-id="ed9f4-176">拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-176">To read or set extension properties, you must write custom code.</span></span> <span data-ttu-id="ed9f4-177">ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-177">However, that custom code is automatically sent between POS and CRT.</span></span></p>
<p><span data-ttu-id="ed9f4-178">たとえば、POS の顧客エンティティーにいくつかの追加情報をキャプチャして表示したいとします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-178">For example, you want to capture and show some additional information to the customer entity in POS.</span></span> <span data-ttu-id="ed9f4-179">この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張子プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-179">In this case, you can add a post-trigger to fetch all your custom properties for customer, add them to the customer entity as extension properties, and send those extension properties to POS.</span></span></p>
<p><span data-ttu-id="ed9f4-180">POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-180">You can also send extension properties from POS to CRT and store them in your custom table.</span></span> <span data-ttu-id="ed9f4-181">または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または本社への送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-181">Alternatively, you can do some custom logic based on those properties, or send it to HQ.</span></span></p>
<p><span data-ttu-id="ed9f4-182">製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-182">All CRT entities, such as products, customers, transactions, and parameters, support extension properties.</span></span></p>
<blockquote>[!NOTE]<br>
<span data-ttu-id="ed9f4-183">属性もまたサポートされます (コンフィギュレーション駆動型の開発)。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-183">Attributes are also supported (configuration-driven development).</span></span> <span data-ttu-id="ed9f4-184">拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-184">For extension properties, you must create a custom table and store the data.</span></span> <span data-ttu-id="ed9f4-185">ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成するために必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-185">However, attributes are configuration-driven and aren't required in order to create table fields.</span></span> <span data-ttu-id="ed9f4-186">したがって、読み取りおよび更新操作にコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-186">Therefore, no code is required for read and update operations.</span></span></blockquote>
<p><span data-ttu-id="ed9f4-187">属性についての詳細は、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-187">For details about the attributes, see the following topics:</span></span></p>
<ul>
<li><span data-ttu-id="ed9f4-188"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/order-attributes">注文属性</a></span><span class="sxs-lookup"><span data-stu-id="ed9f4-188"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/order-attributes">Order attributes</a></span></span></li>
<li><span data-ttu-id="ed9f4-189"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/customer-attributes">顧客属性</a></span><span class="sxs-lookup"><span data-stu-id="ed9f4-189"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/customer-attributes">Customer attributes</a></span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ed9f4-190">リアルタイム トランザクション サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="ed9f4-190">Real-time transaction service calls</span></span></td>
<td><span data-ttu-id="ed9f4-191">CRT から HQ の同期呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-191">You can do synchronous call from CRT to HQ.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed9f4-192">CRT データ サービス、およびエンティティ付きデータ サービス</span><span class="sxs-lookup"><span data-stu-id="ed9f4-192">CRT data service and data service with entity</span></span></td>
<td><span data-ttu-id="ed9f4-193">チャネル データベース データ アクセスの特殊なデータ サービスおよび Retail サーバー エクスポージャのエンティティ。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-193">Specialized data service for channel database data access and entity for Retail Server exposures.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ed9f4-194">**5 月の更新プログラム以降で、7.1 の CRT 拡張を手動で展開**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-194">**Manually deploying the CRT extension for 7.1 with May update and later**</span></span>

<span data-ttu-id="ed9f4-195">CRT を拡張すると、オンラインの **…\\RetailServer\\webroot\\bin\\Ext** フォルダーにカスタム ライブラリを配置します (POS が Retail サーバーに接続された場合)。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-195">After you extend CRT, you should put the custom library in the **…\\RetailServer\\webroot\\bin\\Ext** folder for online (that is, when POS is connected to Retail Server).</span></span> <span data-ttu-id="ed9f4-196">**CommerceRuntime.Ext.config** ファイル内で、ここに示すカスタム ライブラリ情報を使用して**構成**セクションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-196">You should also update the **composition** section in the **CommerceRuntime.Ext.config** file with the custom library information, as shown here.</span></span>

```C#
<add source="assembly" value="your custom library name" />
```

<span data-ttu-id="ed9f4-197">たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-197">For example, if the name of your custom library is **Contoso.Commerce.Runtime.CustomerSearchSample**, add the following line in the **composition** section.</span></span>

```C#
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

<span data-ttu-id="ed9f4-198">オフラインの場合は、カスタム ライブラリを **…\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-198">For offline, you should you put the custom library in the **…\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span> <span data-ttu-id="ed9f4-199">**CommerceRuntime.MPOSOffline.ext.config** ファイル内で、ここに示すカスタム ライブラリ情報を使用して**構成**セクションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-199">You should also update the **composition** section in the **CommerceRuntime.MPOSOffline.ext.config** file with the custom library information, as shown here.</span></span>

```C#
<add source="assembly" value="your custom library name" />.
```

<span data-ttu-id="ed9f4-200">上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-200">The preceding steps are used for manual deployment and testing in your development box.</span></span> <span data-ttu-id="ed9f4-201">拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-201">To package the extension and deploy it to production or user acceptance testing (UAT), use the information in the packaging document.</span></span>

<span data-ttu-id="ed9f4-202">**デバッグ CRT**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-202">**Debugging CRT**</span></span>

<span data-ttu-id="ed9f4-203">POS から CRT をデバッグするには、CRT 拡張機能プロジェクトを、オンラインの **w3wp.exe (Retail サーバーの IIS プロセス)** プロセス (POS が CRT に接続されている場合) に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-203">To debug CRT from POS, you should attach the CRT extension project to the **w3wp.exe (IIS process for Retail server)** process for online (that is, when POS is connected to CRT).</span></span> <span data-ttu-id="ed9f4-204">オフラインの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-204">For offline, attach the CRT extension project to the **dllhost.exe** process.</span></span>

<span data-ttu-id="ed9f4-205">**CRT エンティティ、依頼および応答での拡張機能プロパティの使用**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-205">**Using extension properties on CRT entities and requests and responses**</span></span>

<span data-ttu-id="ed9f4-206">既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-206">One way to add new data to an existing CRT entity is to use extension properties.</span></span> <span data-ttu-id="ed9f4-207">拡張プロパティは、エンティティのキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-207">Extension properties are key-value pairs on the entity.</span></span> <span data-ttu-id="ed9f4-208">既定では、これらのキーと値のペアはデータベースで保持されません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-208">By default, these key-value pairs aren't persisted in the database.</span></span> <span data-ttu-id="ed9f4-209">拡張プロパティを保持するためには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-209">To persist an extension property, you must write custom code.</span></span>

<span data-ttu-id="ed9f4-210">**CRT エンティティでの機能拡張プロパティの永続的な使用**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-210">**Using extension properties on CRT entities with persistence**</span></span>

<span data-ttu-id="ed9f4-211">エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-211">Any extension property that you add to an entity stays in memory for POS and CRT for the lifetime of either the object or the transaction, depending on the scenario.</span></span> <span data-ttu-id="ed9f4-212">拡張プロパティは、アプリケーションの境界にもまたがって移動します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-212">The extension property also travels across application boundaries.</span></span> <span data-ttu-id="ed9f4-213">たとえば、Retail Modern POS に拡張プロパティを追加し、Retail サーバー/CRT を呼び出すと、キーと値のペアがそのフロー全体でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-213">For example, if you add an extension property in Retail Modern POS and then call Retail Server/CRT, the key-value pair is also available during the whole flow.</span></span> <span data-ttu-id="ed9f4-214">また、そのエンティティが Commerce Data Exchange: Real-time Service を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-214">Additionally, if that entity is sent to during a call to Commerce Data Exchange: Real-time Service, the key-value pair is available during the process.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9f4-215">HQ では、拡張プロパティは顧客と注文に対してのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-215">For HQ, extension properties are sent only for customers and orders.</span></span>

<span data-ttu-id="ed9f4-216">ただし、既述のように、拡張プロパティは既定では保持されていません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-216">However, as was mentioned earlier, the extension property isn't persisted by default.</span></span> <span data-ttu-id="ed9f4-217">拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-217">If you want to persist an extension property, you must do data modeling to help guarantee that you make the correct design choices about where the data should reside.</span></span> <span data-ttu-id="ed9f4-218">新しいテーブルと結合を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-218">We recommend that you use a new table and a join.</span></span> <span data-ttu-id="ed9f4-219">この方法は、ほとんどの要件に適合します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-219">This approach fits most requirements well.</span></span> <span data-ttu-id="ed9f4-220">Retail SDK の EmailPreference サンプルは、代表的なエンド ツー エンドの例を提供します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-220">The EmailPreference sample in the Retail SDK provides a good end-to-end example.</span></span>

<span data-ttu-id="ed9f4-221">**Retail SDK のサンプル コードの場所**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-221">**Location of the sample code in the Retail SDK**</span></span>

<span data-ttu-id="ed9f4-222">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="ed9f4-222">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

<span data-ttu-id="ed9f4-223">**スクリプトの場所**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-223">**Location of the scripts**</span></span>

<span data-ttu-id="ed9f4-224">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="ed9f4-224">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

<span data-ttu-id="ed9f4-225">**エンティティに拡張子プロパティを設定する構文**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-225">**Syntax to set an extension property on an entity**</span></span>

```C#
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

<span data-ttu-id="ed9f4-226">**例**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-226">**Example**</span></span>

<span data-ttu-id="ed9f4-227">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-227">**Scenario**</span></span>

<span data-ttu-id="ed9f4-228">小売パラメーターに新しい拡張テーブルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-228">You created a new extension table for Retail parameters.</span></span> <span data-ttu-id="ed9f4-229">その拡張テーブルからフィールドを読み取り、それを POS に送信したいとします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-229">You want to read a field from that extension table and send it to POS.</span></span>

<span data-ttu-id="ed9f4-230">小売チャネルのデータベースを拡張する場合は、メイン テーブルと拡張テーブルの間に主キーの関係を置くことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-230">When you extend the retail channel database, it's always a good idea to have a primary key relation between the main table and the extension table.</span></span> <span data-ttu-id="ed9f4-231">その後、主キーを使用して拡張テーブルからデータを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-231">You can then read the data from the extension table by using the primary key.</span></span>

<span data-ttu-id="ed9f4-232">**ステップ**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-232">**Steps**</span></span>

1. <span data-ttu-id="ed9f4-233">メイン テーブルに主キーの関係があるチャネル テーブル内の、Retail パラメータの拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-233">Create the extension table for Retail parameters in the channel table that has the primary key relation to the main table.</span></span> <span data-ttu-id="ed9f4-234">(この場合、メイン テーブルは小売共有パラメーターです。)</span><span class="sxs-lookup"><span data-stu-id="ed9f4-234">(In this case, the main table is Retail shared parameters.)</span></span>
2. <span data-ttu-id="ed9f4-235">小売パラメーターを読み取る CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-235">Identify the CRT data request that reads the Retail parameters.</span></span>
3. <span data-ttu-id="ed9f4-236">データ要求の転記トリガーを追加します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-236">Add a post-trigger for the data request.</span></span> <span data-ttu-id="ed9f4-237">共有パラメータ テーブルの主キーを使用して、小売共有パラメータの拡張テーブルを照会し、カスタム フィールドを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-237">You will then be able to use the primary key of the shared parameters table to query your extension table for Retail shared parameters and read the custom fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed9f4-238">ポスト トリガー要求でエンティティの主キーを取得できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-238">You can get the primary key for the entity in the post-trigger request.</span></span> <span data-ttu-id="ed9f4-239">エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-239">That request will have the entity object, and that entity object will have all the required fields.</span></span>

4. <span data-ttu-id="ed9f4-240">カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-240">Add the custom fields as extension properties to the shared parameters entity in the CRT post-trigger, and send it to POS.</span></span>

<span data-ttu-id="ed9f4-241">**トリガーの拡張機能プロパティの読み取り**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-241">**Reading extension properties in triggers**</span></span>

<span data-ttu-id="ed9f4-242">小売パラメータ テーブルからデータを読み込む要求は、GetChannelConfigurationDataRequest です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-242">The request that reads the data from the Retail parameters table is GetChannelConfigurationDataRequest.</span></span> <span data-ttu-id="ed9f4-243">次の例では、この要求のポスト トリガーを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-243">The following example shows how you can add a post-trigger for this request.</span></span>

```C#
/**
* SAMPLE CODE NOTICE
*
* THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
* OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
* THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
* NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
*/

namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System;
        using System.Collections.Generic;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Class that implements a post trigger for the GetChannelConfigurationDataRequest request type.
        /// </summary>

        public class GetChannelConfigurationDataRequestTriggers : IRequestTrigger
        {
            /// <summary>
            /// Gets the supported requests for this trigger.
            /// </summary>

            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] { typeof(GetChannelConfigurationDataRequest) };
                }
            }

            /// <summary>
            /// Post trigger code to retrieve extension properties.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>

            public void OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(response, "response");
                var channelConfiguration = ((SingleEntityDataServiceResponse<ChannelConfiguration>)response).Entity;
                if (channelConfiguration == null)
                {
                    return;
                }
                var query = new SqlPagedQuery(QueryResultSettings.SingleRecord)
                {
                    DatabaseSchema = "ext",
                    Select = new ColumnSet(new string[] { "CUSTOMFIELD" }),
                    From = "PARAMETERSEXTENSIONVIEW", // Create your own view to read the data from the parameter extension table by passing the primary key from the entity (in this case its Rec ID)
                    Where = "PARAMETERSRECID = @RecId AND DATAAREAID = @dataAreaId" //This query assumes I have PARAMETERSRECID, DATAAREAID and CUSTOMFIELD as new fields in the extension tables.
                };
                query.Parameters["@RecId"] = channelConfiguration.RetailParametersRecId;
                query.Parameters["@dataAreaId"] = request.RequestContext.GetChannelConfiguration().InventLocationDataAreaId;
                using (var databaseContext = new SqlServerDatabaseContext(request))
                {
                    ExtensionsEntity extensions = databaseContext.ReadEntity<ExtensionsEntity>(query).FirstOrDefault();
                    var customField = extensions != null ? extensions.GetProperty("customField") : null;
                    if (customField != null)
                    {
                        **channelConfiguration.SetProperty("CUSTOMFIELD", customField);**
                    }
                }
            }

            /// <summary>
            /// Pre trigger code.
            /// </summary>
            /// <param name="request">The request.</param>

            public void OnExecuting(Request request)
            {
            }
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="ed9f4-244">新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-244">You must change this query, based on your new field and table, or whatever condition you're using.</span></span> <span data-ttu-id="ed9f4-245">テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-245">When you design the table, make sure that you have the primary key field from the parent table, so that you can query it by using the CRT entity.</span></span> <span data-ttu-id="ed9f4-246">ほとんどの CRT エンティティには、**RecId** フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-246">Most CRT entities should have the primary key field in them, such as the **RecId** field or another relevant unique field that is used to select the record.</span></span>

<span data-ttu-id="ed9f4-247">**ハンドラーを上書きすることによる拡張プロパティの設定**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-247">**Setting extension properties by overriding the handler**</span></span>

<span data-ttu-id="ed9f4-248">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-248">**Scenario**</span></span>

<span data-ttu-id="ed9f4-249">顧客用に新しい拡張テーブルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-249">You created a new extension table for Customer.</span></span> <span data-ttu-id="ed9f4-250">顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-250">When values for the extension field for customer come from POS or CRT, you want to store the values in your custom table.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9f4-251">拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-251">You can set extension properties either in a trigger or by overriding the handler.</span></span> <span data-ttu-id="ed9f4-252">拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-252">If you just set some extension properties by reading from your extension table, you can use triggers.</span></span>

<span data-ttu-id="ed9f4-253">**ステップ**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-253">**Steps**</span></span>

1. <span data-ttu-id="ed9f4-254">メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-254">Create your extension table for Customers in the channel table that has the primary key relation to the main table.</span></span> <span data-ttu-id="ed9f4-255">(この場合、メイン テーブルは CustTable です。)</span><span class="sxs-lookup"><span data-stu-id="ed9f4-255">(In this case, the main table is CustTable.)</span></span>
2. <span data-ttu-id="ed9f4-256">CustTable にデータを設定する CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-256">Identify the CRT data request that sets data in CustTable.</span></span>
3. <span data-ttu-id="ed9f4-257">ハンドラを上書きし、メイン テーブル (CustTable) で値を設定する基本要求を呼び出してからテーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-257">Override the handler, and call the base request to set values in the main table (CustTable) and then the extension table.</span></span>

> [!NOTE]
> <span data-ttu-id="ed9f4-258">拡張手順またはビューに必要な追加のプロパティを送信できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-258">You can send any additional properties that you want to your extension procedure or view.</span></span>

<span data-ttu-id="ed9f4-259">次の例では、使用される SQL スクリプトがありません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-259">The example that follows doesn't have the SQL scripts that are used.</span></span> <span data-ttu-id="ed9f4-260">完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-260">You can find the full sample code and scripts at the following locations in the Retail SDK.</span></span>

<span data-ttu-id="ed9f4-261">**Retail SDK のサンプル コードの場所**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-261">**Location of the sample code in the Retail SDK**</span></span>

<span data-ttu-id="ed9f4-262">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="ed9f4-262">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

<span data-ttu-id="ed9f4-263">**スクリプトの場所**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-263">**Location of the scripts**</span></span>

<span data-ttu-id="ed9f4-264">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="ed9f4-264">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

<span data-ttu-id="ed9f4-265">**例**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-265">**Example**</span></span>

```C#
/**
* SAMPLE CODE NOTICE
*
* THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
* OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
* THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
* NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
*/

namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System.Transactions;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data.Types;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer;

        /// <summary>
        /// Create or update customer data request handler.
        /// </summary>

        public sealed class CreateOrUpdateCustomerDataRequestHandler : SingleRequestHandler<CreateOrUpdateCustomerDataRequest, SingleEntityDataServiceResponse<Customer>>
        {
            /// <summary>
            /// Executes the workflow to create or update a customer.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <returns>The response.</returns>

            protected override SingleEntityDataServiceResponse<Customer> Process(CreateOrUpdateCustomerDataRequest request)
            {
                ThrowIf.Null(request, "request");
                using (var databaseContext = new SqlServerDatabaseContext(request))
                using (var transactionScope = new TransactionScope())
                {
                    // Execute original functionality to save the customer.

                    var requestHandler = new Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer.CustomerSqlServerDataService();
                    var response = (SingleEntityDataServiceResponse<Customer>)requestHandler.Execute(request);

                    // Execute additional functionality to save the customer's extension properties.

                    if (!request.Customer.ExtensionProperties.IsNullOrEmpty())
                    {

                        // The stored procedure will determine which extension properties are saved to which tables.

                        ParameterSet parameters = new ParameterSet();
                        parameters["@TVP_EXTENSIONPROPERTIESTABLETYPE"] = new ExtensionPropertiesTableType(request.Customer.RecordId, request.Customer.ExtensionProperties).DataTable;
                        databaseContext.ExecuteStoredProcedureNonQuery("[ext].UPDATECUSTOMEREXTENSIONPROPERTIES", parameters);
                    }
                    transactionScope.Complete();
                    return response;
                }
            }
        }
    }
}
```

<span data-ttu-id="ed9f4-266">**後で読み込むプロパティを有効にする構文**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-266">**Syntax to enable the property to be read later**</span></span>

```C#
var property = entity.GetProperty("EXTENSION_PROPERTY_ADDED");
```

### <a name="using-extension-properties-on-crt-request-and-response-types"></a><span data-ttu-id="ed9f4-267">CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="ed9f4-267">Using extension properties on CRT request and response types</span></span>

<span data-ttu-id="ed9f4-268">エンティティと同様、拡張機能プロパティを設定および取得するために要求および応答タイプを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-268">Like entities, request and response types can be extended to set and get extension properties.</span></span> <span data-ttu-id="ed9f4-269">ただし、要求のライフサイクルでのみ存続し、POS では使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-269">However, they will persist only for the lifecycle of the request and won't be available in POS.</span></span> <span data-ttu-id="ed9f4-270">それらをデータベースに保存する場合は、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-270">If you want to save them to the database, you must write custom code.</span></span>

```C#
request.SetProperty("PropertyName", true);
response.SetProperty("PropertyName2", true);
var PropertyName = request.GetProperty("PropertyName");
var BoolPropertyName2 = response.GetProperty("PropertyName2");
```

<span data-ttu-id="ed9f4-271">**設定または POS の拡張子プロパティの読み取り**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-271">**Setting or reading extension properties in POS**</span></span>

<span data-ttu-id="ed9f4-272">POS で拡張プロパティーを設定して、POS アプリケーション プログラミング インターフェース (API) を使用してそれらを CRT に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-272">You can set extension properties in POS and send them to CRT by using the POS application programming interfaces (APIs).</span></span> <span data-ttu-id="ed9f4-273">または、エンティティ レベルで拡張機能プロパティの送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-273">Alternatively, you can send extension properties at the entity level.</span></span>

<span data-ttu-id="ed9f4-274">カート行に拡張プロパティを設定するには、SaveExtensionPropertiesOnCartLinesClientRequest を使用します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-274">To set an extension property on the cart line, you use SaveExtensionPropertiesOnCartLinesClientRequest.</span></span> <span data-ttu-id="ed9f4-275">同様に、買い物カゴ ヘッダーに対して、SaveExtensionPropertiesOnCartClientRequest を使用します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-275">Likewise, for the cart header, you use SaveExtensionPropertiesOnCartClientRequest.</span></span>

<span data-ttu-id="ed9f4-276">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-276">Here is an example.</span></span>

```Typescript
let sampleExtensionProperty = <ProxyEntities.CommerceProperty>{
    Key: "sampleExtensionProperty",
    Value: <ProxyEntities.CommercePropertyValue>{
        BooleanValue: false
    }
};
this.context.runtime.executeAsync(new SaveExtensionPropertiesOnCartClientRequest([sampleExtensionProperty]));
```

<span data-ttu-id="ed9f4-277">**POS のカートから拡張プロパティの読み取り**</span><span class="sxs-lookup"><span data-stu-id="ed9f4-277">**Reading the extension property from the cart in POS**</span></span>

```Typescript
let getCartRequest: GetCurrentCartClientRequest<GetCurrentCartClientResponse> = new GetCurrentCartClientRequest<GetCurrentCartClientResponse>();
return this.context.runtime.executeAsync(getCartRequest).then((value: ICancelableDataResult<GetCurrentCartClientResponse>) => {
    let cart: Commerce.Proxy.Entities.Cart = (<GetCurrentCartClientResponse>value.data).result;

    // Gets the extension property from the cart.

    let sampleExtensionPropertyValue: boolean;
    if (!ObjectExtensions.isNullOrUndefined(cart) && !ObjectExtensions.isNullOrUndefined(cart.ExtensionProperties)) {
        let SampleCommerceProperties: ProxyEntities.CommerceProperty[] = cart.ExtensionProperties.filter((extensionProperty: ProxyEntities.CommerceProperty) => {
            return extensionProperty.Key === "sampleExtensionProperty";
        });
        sampleExtensionPropertyValue = SampleCommerceProperties.length > 0 ? SampleCommerceProperties[0].Value.BooleanValue : false;
    } else {
        sampleExtensionPropertyValue = false;
    }

    //Resolve the promise according to your scenario and method.

    return Promise.resolve({ canceled: false });
});
```

<span data-ttu-id="ed9f4-278">同様に、製品、顧客、および住所など他のすべてのエンティティから拡張機能プロパティを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-278">Likewise, you can read the extension property from all the other entities, such as products, customers, and addresses.</span></span>

### <a name="implementing-a-new-crt-service-that-handles-multiple-new-requests"></a><span data-ttu-id="ed9f4-279">複数の新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="ed9f4-279">Implementing a new CRT service that handles multiple new requests</span></span>

<span data-ttu-id="ed9f4-280">新しい CRT サービスを実装することが一般的です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-280">It's a typical case to implement a new CRT service.</span></span> <span data-ttu-id="ed9f4-281">最初に、新しい要求および応答クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-281">First, you must create new request and response classes.</span></span>

#### <a name="creating-the-request-and-response-classes"></a><span data-ttu-id="ed9f4-282">要求および応答クラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="ed9f4-282">Creating the request and response classes</span></span>

<span data-ttu-id="ed9f4-283">作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-283">For serialization to work, the new request type must implement the **\[DataContract\]** and **\[DataMember\]** attributes.</span></span>

    using System.Runtime.Serialization;
    using Microsoft.Dynamics.Commerce.Runtime.Messages;

    [DataContract]
    public sealed class GetStoreHoursDataRequest : Request
    {
        public GetStoreHoursDataRequest(string storeNumber)
        {
            this.StoreNumber = storeNumber;
        }

        [DataMember]
        public string StoreNumber { get; private set; }
    }

<span data-ttu-id="ed9f4-284">新しい応答タイプは要求タイプに似ています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-284">The new response type resembles the request type.</span></span>

    [DataContract]
    public sealed class GetStoreHoursDataResponse : Response
    {
        public GetStoreHoursDataResponse(PagedResult dayHours)
        {
            this.DayHours = dayHours;
        }

        [DataMember]
        public PagedResult DayHours { get; private set; }
    }

<span data-ttu-id="ed9f4-285">次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-285">Next, you must create a new CRT service that uses the request and response types.</span></span>

#### <a name="creating-a-new-crt-service"></a><span data-ttu-id="ed9f4-286">新しい CRT サービス注文を作成しています</span><span class="sxs-lookup"><span data-stu-id="ed9f4-286">Creating a new CRT service</span></span>

1.  <span data-ttu-id="ed9f4-287">新しいサービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-287">Implement the new service.</span></span>

        public class StoreHoursDataService : IRequestHandler

2.  <span data-ttu-id="ed9f4-288">インターフェイスのメンバー 2 つを実装します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-288">Implement two members of the interface.</span></span> <span data-ttu-id="ed9f4-289">**SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-289">The **SupportedRequestTypes** member returns a list of all requests that this service can handle.</span></span> <span data-ttu-id="ed9f4-290">実行メソッドは、このサービスの要求が実行された場合に CRT が呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-290">The execute method is the method that the CRT calls for you if a request for this service is run.</span></span>

        public IEnumerable SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                typeof(GetStoreHoursDataRequest),
                };
            }
        }

        public Response Execute(Request request);

3.  <span data-ttu-id="ed9f4-291">CommerceRuntime.Config ファイルで、**合成**セクション (または同等のセクション) を更新してこのサービスを登録します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-291">In the commerceRuntime.Config file, update the **composition** section (or the equivalent section) to register this service.</span></span> <span data-ttu-id="ed9f4-292">アセンブリから 1 つの型またはすべての型を登録できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-292">Note that you can register single types or all types from an assembly.</span></span> <span data-ttu-id="ed9f4-293">CommerceRuntime エンジンは、すべての IRequestHandler 派生タイプを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-293">The CommerceRuntime engine will find all IRequestHandler derived types.</span></span>
4.  <span data-ttu-id="ed9f4-294">オプション: CommerceRuntime テスト ホストを使用してサービスのテストを行います。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-294">Optional: Use the CommerceRuntime Test Host to do a test run of your service.</span></span>

### <a name="implementing-a-new-crt-service-that-handles-a-single-new-request"></a><span data-ttu-id="ed9f4-295">1 つの新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="ed9f4-295">Implementing a new CRT service that handles a single new request</span></span>

<span data-ttu-id="ed9f4-296">単一の要求サービスを作成すると少し便利になります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-296">It’s slightly easier to create a single-request service.</span></span>

    public class CrossLoyaltyCardService : SingleRequestHandler

<span data-ttu-id="ed9f4-297">前の手順で説明したように登録が行われます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-297">Registration is done as described in the previous procedure.</span></span>

### <a name="implementing-a-new-crt-service-that-overrides-the-functionality-of-an-existing-request"></a><span data-ttu-id="ed9f4-298">既存の要求の機能をオーバーライドする新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="ed9f4-298">Implementing a new CRT service that overrides the functionality of an existing request</span></span>

<span data-ttu-id="ed9f4-299">場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-299">In some cases, the request and response types are sufficient, but the service implementation must be changed.</span></span> <span data-ttu-id="ed9f4-300">新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-300">If some new data must be transmitted, you can also extend entity, request, or response objects by using extension properties.</span></span> <span data-ttu-id="ed9f4-301">このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-301">In this scenario, you can create the service as described earlier and use the existing IRequestHandler types.</span></span> <span data-ttu-id="ed9f4-302">また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-302">Additionally, registration in the commerceRuntime.Config file must precede registration of the service that should be overridden.</span></span> <span data-ttu-id="ed9f4-303">この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-303">This registration order is important because of the way that the Managed Extensibility Framework (MEF) loads the extension dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="ed9f4-304">ファイルより高いタイプが優先されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-304">The types that are higher in the file win.</span></span>

### <a name="implementing-a-new-crt-entity-and-using-it-in-new-crt-service"></a><span data-ttu-id="ed9f4-305">新しい CRT エンティティの実装および新しい CRT サービスでの使用</span><span class="sxs-lookup"><span data-stu-id="ed9f4-305">Implementing a new CRT entity and using it in new CRT service</span></span>

<span data-ttu-id="ed9f4-306">すべての新しいエンティティは、**CommerceEntity** タイプであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-306">Any new entity must be of the **CommerceEntity** type.</span></span> <span data-ttu-id="ed9f4-307">このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-307">When you use this type, lots of low-level functionality is automatically handled for you.</span></span> <span data-ttu-id="ed9f4-308">次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-308">The following example, which is taken from the StoreHours sample, shows how to create an entity that is bound to the database table.</span></span> <span data-ttu-id="ed9f4-309">これは、通常のケースです。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-309">This is the usual case.</span></span>

    public class StoreDayHours : CommerceEntity
    {
        private const string DayColumn = "DAY";
        private const string OpenTimeColumn = "OPENTIME";
        private const string CloseTimeColumn = "CLOSINGTIME";
        private const string IdColumn = "RECID";

        public StoreDayHours()
            : base("StoreDayHours")
        {
        }

        [DataMember]
        [Column(DayColumn)]
        public int DayOfWeek
        {
            get { return (int)this[DayColumn]; }
            set { this[DayColumn] = value; }
        }

        [DataMember]
        [Column(OpenTimeColumn)]
        public int OpenTime
        {
            get { return (int)this[OpenTimeColumn]; }
            set { this[OpenTimeColumn] = value; }
        }

        [DataMember]
        [Column(CloseTimeColumn)]
        public int CloseTime
        {
            get { return (int)this[CloseTimeColumn]; }
            set { this[CloseTimeColumn] = value; }
        }

        [Key]
        [DataMember]
        [Column(IdColumn)]
        public long Id
        {
            get { return (long)this[IdColumn]; }
            set { this[IdColumn] = value; }
        }
    }

<span data-ttu-id="ed9f4-310">サービスで新しいエンティティを使用する場合、プロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-310">When you want to use the new entity in a service, the process is straightforward.</span></span> <span data-ttu-id="ed9f4-311">前述のように、派生 IRequestHandler として新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-311">As described earlier, you create a new service as a derived IRequestHandler.</span></span> <span data-ttu-id="ed9f4-312">次に、新しいエンティティを使用するか返すかのいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-312">Then either use or return the new entity.</span></span> <span data-ttu-id="ed9f4-313">次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-313">The following example shows how to read the entity from the database and return it as part of the response.</span></span>

    private GetStoreHoursDataResponse GetStoreDayHours(GetStoreHoursDataRequest request)
    {
        ThrowIf.Null(request, "request");
        using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
        {
            var query = new SqlPagedQuery(request.QueryResultSettings)
            {
                DatabaseSchema = "crt",
                Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                From = "ISVRETAILSTOREHOURSVIEW",
                Where = "STORENUMBER = @storeNumber",
            };

            query.Parameters["@storeNumber"] = request.StoreNumber;
            return new GetStoreHoursDataResponse(databaseContext.ReadEntity(query));
        }
    }

<span data-ttu-id="ed9f4-314">前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-314">For the preceding example, the CRT runtime engine automatically makes a query to the channel database via the registered data adapter.</span></span> <span data-ttu-id="ed9f4-315">名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-315">It queries a type that has the name **crt.ISVRetailStoreHoursView**, and generates a **where** clause and columns as specified in the code.</span></span> <span data-ttu-id="ed9f4-316">カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-316">The customizer is responsible for providing the SQL objects as part of the customization.</span></span>

### <a name="adding-pre-triggers-and-post-triggers-for-a-specific-request"></a><span data-ttu-id="ed9f4-317">特定の要求のプレトリガーとポストトリガーの追加</span><span class="sxs-lookup"><span data-stu-id="ed9f4-317">Adding pre-triggers and post-triggers for a specific request</span></span>

<span data-ttu-id="ed9f4-318">場合によっては、要求の前後で必要になる処理もあります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-318">In some cases, some processing must be done before or after a request is handled.</span></span> <span data-ttu-id="ed9f4-319">追加のコードを実行するために使用できる 2 つのフックがあります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-319">There are two hooks that can be used to run additional code.</span></span> <span data-ttu-id="ed9f4-320">これらのフックはプレトリガーおよびポストトリガーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-320">These hooks are called pre-triggers and post-triggers.</span></span> <span data-ttu-id="ed9f4-321">新しいトリガーを作成して要求に関連付けるには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-321">Follow these steps to create new triggers and associate them with a request.</span></span>

1.  <span data-ttu-id="ed9f4-322">IRequestTrigger を実装する新しいトリガー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-322">Create a new trigger class that implements IRequestTrigger.</span></span>

        public class GetCrossLoyaltyCardRequestTrigger : IRequestTrigger

2.  <span data-ttu-id="ed9f4-323">**IRequest.SupportedRequestTypes** プロパティで、このトリガーを実行する必要がある要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-323">In the **IRequest.SupportedRequestTypes** property, return the list of requests that this trigger should be run for.</span></span>

        public IEnumerable SupportedRequestTypes
        {
            get
            {
                return new[] { typeof(GetCrossLoyaltyCardRequest) };
            }
        }

3.  <span data-ttu-id="ed9f4-324">要求の前後に呼び出される関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-324">Implement the functions that are called before and after the request.</span></span>

        void OnExecuted(Request request, Response response);
        void OnExecuting(Request request);

4.  <span data-ttu-id="ed9f4-325">commerceRuntime.Config ファイルでクラスを登録します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-325">Register the class in the commerceRuntime.Config file.</span></span>

## <a name="retail-server-extensibility-scenarios"></a><span data-ttu-id="ed9f4-326">Retail サーバーの拡張機能シナリオ</span><span class="sxs-lookup"><span data-stu-id="ed9f4-326">Retail Server extensibility scenarios</span></span>
### <a name="adding-a-new-odata-action-to-an-existing-controller"></a><span data-ttu-id="ed9f4-327">既存のコントローラーへの新しい ODATA アクションの追加</span><span class="sxs-lookup"><span data-stu-id="ed9f4-327">Adding a new ODATA action to an existing controller</span></span>

<span data-ttu-id="ed9f4-328">最も簡単なシナリオでは、わずかに異なるユース ケースのために新しいアプリケーション プログラミング インターフェイス (API) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-328">In the easiest scenario, you must add a new application programming interface (API) for a slightly different use case.</span></span> <span data-ttu-id="ed9f4-329">このシナリオを機能させるには、継承によって新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-329">To make this scenario work, you can add the new action through inheritance.</span></span> <span data-ttu-id="ed9f4-330">Retail サーバーへの API の任意の変更については、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-330">For any changes to the APIs to Retail Server, you must follow these steps.</span></span>

1.  <span data-ttu-id="ed9f4-331">新しいアクションまたはコントローラーを実装します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-331">Implement the new action or controller.</span></span>
2.  <span data-ttu-id="ed9f4-332">新しい対応するメタデータを追加するためのモデル出荷時の要件を上書きします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-332">Override the requirements of the model factory to add the new corresponding metadata.</span></span>

<span data-ttu-id="ed9f4-333">次の例は、Retail SDK から取得したもので、既存のコントローラーを拡張して POST アクションを持つようにする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-333">The following example, which is taken from the Retail SDK, shows how to extend an existing controller so that it has a POST action.</span></span>

    public class MyCustomersController : CustomersController
    {
        [HttpPost]
        [CommerceAuthorization(AllowedRetailRoles = new string[] { CommerceRoles.Customer, CommerceRoles.Employee })]
        public decimal GetCrossLoyaltyCardDiscountAction(ODataActionParameters parameters)
        {
            if (parameters == null)
            {
                throw new ArgumentNullException("parameters");
            }

            var runtime = CommerceRuntimeManager.CreateRuntime(this.CommercePrincipal);
            string loyaltyCardNumber = (string)parameters["LoyaltyCardNumber"];

            GetCrossLoyaltyCardResponse resp = runtime.Execute(new GetCrossLoyaltyCardRequest(loyaltyCardNumber), null);

            string logMessage = "GetCrossLoyaltyCardAction successfully handled with card number '{0}'. Returned discount '{1}'.";
            RetailLogger.Log.ExtendedInformationalEvent(logMessage, loyaltyCardNumber, resp.Discount.ToString());
            return resp.Discount;
        }
    }

<span data-ttu-id="ed9f4-334">次に、モデル ファクトリをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-334">Next, override the model factory.</span></span>

    [Export(typeof(IEdmModelFactory))]
    [ComVisible(false)]
    public class CustomizedEdmModelFactory : CommerceModelFactory
    {
        protected override void BuildActions()
        {
            base.BuildActions();
            var var1 = CommerceModelFactory.BindEntitySetAction("GetCrossLoyaltyCardDiscountAction");
            var1.Parameter("LoyaltyCardNumber");
            var1.Returns();
        }
    }

<span data-ttu-id="ed9f4-335">クライアントがこの新しいカスタマイズを使用する前に、新しいモデル ファクトリ用の Retail サーバー プロキシ コードを生成するためにビルド システムを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-335">Before clients can use this new customization, you must adjust the build system to generate the Retail Server proxy code for the new model factory.</span></span> <span data-ttu-id="ed9f4-336">この構成ステップはビルド システムで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-336">This configuration step is done in the build system.</span></span> <span data-ttu-id="ed9f4-337">最後に、web.config ファイルを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-337">Finally, you must adjust the web.config file.</span></span> <span data-ttu-id="ed9f4-338">SDK の Retail サーバーの梱包プロジェクトでは、このステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-338">You must complete this step in the packaging project for Retail Server in the SDK.</span></span> <span data-ttu-id="ed9f4-339">ローカルのテストが行われている場合、テストに使用されるローカル開発トポロジー コンピューターでこの手順を任意で実行できます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-339">If local tests will be done, you can also optionally complete this step on the local development topology machine that is used for testing.</span></span>

### <a name="adding-a-new-simple-controller-for-an-entity"></a><span data-ttu-id="ed9f4-340">エンティティの新しい簡単なコントローラーの追加</span><span class="sxs-lookup"><span data-stu-id="ed9f4-340">Adding a new simple controller for an entity</span></span>

<span data-ttu-id="ed9f4-341">単純なエンティティがあり、データをフェッチするコント ローラーを必要としているとします。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-341">Suppose that you have a simple entity and require a controller to fetch the data.</span></span> <span data-ttu-id="ed9f4-342">例については、Retail SDK で StoreHours サンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-342">For an example, see the StoreHours sample in the Retail SDK.</span></span> <span data-ttu-id="ed9f4-343">新しい Retail サーバー コントローラーには意味があり、低レベルのすべての作業が CRT (新しいエンティティ、要求、応答、およびサービス) で実行されます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-343">A new Retail Server controller makes sense, and all the low-level work is done in the CRT (new entity, request, response, and service).</span></span> <span data-ttu-id="ed9f4-344">新しいコントローラを作成するには、CommerceController から派生します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-344">To create a new controller, you derive from CommerceController.</span></span> <span data-ttu-id="ed9f4-345">例としてここに表示します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-345">An example is shown here.</span></span> <span data-ttu-id="ed9f4-346">コントローラー名は重要であり、エンティティの名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-346">The controller name is important and must match the name of the entity.</span></span>

    [ComVisible(false)]
    public class StoreHoursController : CommerceController
    {
        public override string ControllerName
        {
            get { return "StoreHours"; }
        }

        [HttpPost]
        [CommerceAuthorization(AllowedRetailRoles = new string[] { CommerceRoles.Anonymous, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee })]
        public System.Web.OData.PageResult GetStoreDaysByStore(ODataActionParameters parameters)
        {
            if (parameters == null)
            {
                throw new ArgumentNullException("parameters");
            }

            var runtime = CommerceRuntimeManager.CreateRuntime(this.CommercePrincipal);

            QueryResultSettings queryResultSettings = QueryResultSettings.SingleRecord;
            queryResultSettings.Paging = new PagingInfo(10);

            var request = new GetStoreHoursDataRequest((string)parameters["StoreNumber"]) { QueryResultSettings = queryResultSettings };
            PagedResult hours = runtime.Execute(request, null).DayHours;
            return this.ProcessPagedResults(hours);
        }
    }

<span data-ttu-id="ed9f4-347">新しいエンティティについては、次の例に示すように、工場の **BuildEntitySets()** メソッドを上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-347">For new entities, you must also override the factory’s **BuildEntitySets()** method, as shown in the following example.</span></span>

    [Export(typeof(IEdmModelFactory))]
    [ComVisible(false)]
    public class CustomizedEdmModelFactory : CommerceModelFactory
    {
        protected override void BuildActions()
        {
            base.BuildActions();
            var action = CommerceModelFactory.BindEntitySetAction("GetStoreDaysByStore");
            action.Parameter("StoreNumber");
            action.ReturnsCollectionFromEntitySet("StoreHours");
        }

        protected override void BuildEntitySets()
        {
            base.BuildEntitySets();
            CommerceModelFactory.BuildEntitySet("StoreHours");
        }
    }

### <a name="how-to-call-the-new-retail-server-api-from-mposcloud-pos"></a><span data-ttu-id="ed9f4-348">MPOS/クラウド POS から新しい小売サーバー API を呼び出す方法:</span><span class="sxs-lookup"><span data-stu-id="ed9f4-348">How to call the new retail server API from MPOS/Cloud POS:</span></span>

<span data-ttu-id="ed9f4-349">新しい小売サーバー API を呼び出す前に、以下の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-349">Before calling the new retail server API please make sure you have performed the below steps:</span></span>

1.  <span data-ttu-id="ed9f4-350">Retail サーバー web.config ファイルで新しい Retail サーバー拡張子を登録します: &lt;ソースの追加 =「アセンブリ」値 ="**アセンブリ名**" /&gt; は、extensionComposition セクションの下にあります。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-350">Register your new retail server extension in Retail server web.config file:  &lt;add source="assembly" value="**Your assembly name**" /&gt; under the extensionComposition section.</span></span>
2.  <span data-ttu-id="ed9f4-351">Customization.settings ファイルの新しい Retail サーバー拡張子を追加します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-351">Add the new retail server extension in the Customization.settings file.</span></span> <span data-ttu-id="ed9f4-352">このファイルは、RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt; に存在します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-352">You can find this file in RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt;</span></span>
3.  <span data-ttu-id="ed9f4-353">CRT と Retail サーバー拡張子 dlls の両方を **…\\RetailServer\\webroot\\bin\\Ext** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-353">Move both the CRT and Retail server extension dlls into the **…\\RetailServer\\webroot\\bin\\Ext** folder.</span></span> <span data-ttu-id="ed9f4-354">新しい小売サーバー API に関連する CRT 拡張機能をご使用の場合、**…\\RetailServer\\webroot\\bin\\Ext** フォルダー内の CommerceRuntime.Ext.config ファイルの情報を更新してください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-354">If you have a CRT extension that is related to the new retail server API, then update that information in the CommerceRuntime.Ext.config file in the **…\\RetailServer\\webroot\\bin\\Ext** folder.</span></span>
4.  <span data-ttu-id="ed9f4-355">&lt;ソースの追加 = 「アセンブリ」値 = "**アセンブリ名**" /&gt;</span><span class="sxs-lookup"><span data-stu-id="ed9f4-355">&lt;add source="assembly" value="**Your assembly name**" /&gt;</span></span>
5.  <span data-ttu-id="ed9f4-356">inetmgr を使用して小売サーバーのメタデータを参照し、エンティティが xml で公開されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-356">Use inetmgr to browse to the retail server metadata and verify whether your entity is exposed in the xml.</span></span>
6.  <span data-ttu-id="ed9f4-357">mpos/クラウド POSをコンパイルしてビルドし、プロキシを再生成します。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-357">Compile and build the mpos/Cloud POS to regenerate the proxy.</span></span> <span data-ttu-id="ed9f4-358">コンパイラ中に、mpos は小売サーバーのメタデータで定義されたすべてのエンティティを再生成します。これにより、以下のようなコマース コンテキストを使用して新しいエンティティを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-358">During compile mpos regenerates all the entities defined in the retail server metadata, so that you can call the new entities using the commerce context like below:</span></span>

> [!NOTE]
> <span data-ttu-id="ed9f4-359">Retail サーバー web.config ファイルまたは Retail サーバー フォルダ内で何も変更または追加しないでください。拡張合成セクションは除外され、おそらく bin\ext フォルダにカスタム アセンブリがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-359">Do not change or add anything in the Retail server web.config file or Retail server folder, with the expection of the extension composition section and possibly to copy custom assemblies in the bin\ext folder.</span></span> <span data-ttu-id="ed9f4-360">配置時に web.config ファイル内の extensionComposition セクションのみマージされ、他のセクションはすべて上書きされ、**...\\RetailServer\\webroot\\bin\\Ext** フォルダのアセンブリのみが他のアセンブリとマージされます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-360">During deployment, only the extensionComposition section in the web.config file will be merged, all the other sections will be overwritten and only the assemblies in the **...\\RetailServer\\webroot\\bin\\Ext** folder be merged with other assemblies.</span></span> <span data-ttu-id="ed9f4-361">このファイルは、最新バイナリ パッケージに基づいて上書きされます。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-361">This file will be overwritten based on the latest binary package.</span></span> <span data-ttu-id="ed9f4-362">カスタム アプリケーションの設定を追加、または、変更するのに Retail サーバー web.config ファイルは使用しません。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-362">Do not use the Retail server web.config file to add or modify any custom app settings.</span></span>

#### <a name="cross-loyalty-sample"></a><span data-ttu-id="ed9f4-363">クロス ロイヤルティ サンプル。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-363">Cross loyalty sample:</span></span>

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.customers().getCrossLoyaltyCardDiscountAction(loyaltyCardNumber);
    return request.execute<number>();

#### <a name="store-hours-sample"></a><span data-ttu-id="ed9f4-364">店舗の時間のサンプル:</span><span class="sxs-lookup"><span data-stu-id="ed9f4-364">Store hours sample:</span></span>

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.storeHours().getStoreDaysByStore(storeId);
    return request.execute<Commerce.Proxy.Entities.StoreDayHours[]>();

<span data-ttu-id="ed9f4-365">mpos で新しい小売サーバー API を呼び出す方法について詳しくは、小売 SDK POS.Extension.CrossloaylySample および POS.Extension.SToreHoursSample サンプル プロジェクトをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ed9f4-365">Please refer the retail SDK POS.Extension.CrossloaylySample and POS.Extension.SToreHoursSample sample projects for more details on how to call the new retail server api in mpos.</span></span>
