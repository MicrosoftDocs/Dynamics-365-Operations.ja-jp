---
title: Commerce runtime (CRT) の拡張機能
description: このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: afd8f3e47820fbb7f1f3e621e64390e4f012f316
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683364"
---
# <a name="commerce-runtime-crt-extensibility"></a><span data-ttu-id="5780a-103">Commerce runtime (CRT) の拡張機能</span><span class="sxs-lookup"><span data-stu-id="5780a-103">Commerce runtime (CRT) extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5780a-104">このトピックでは、Commerce Runtime (CRT) を拡張するさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5780a-104">This topic describes various ways that you can extend the commerce runtime (CRT).</span></span> <span data-ttu-id="5780a-105">拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5780a-105">It explains the concept of extension properties, and shows how to add them to a CRT entity both with and without persistence.</span></span>

<span data-ttu-id="5780a-106">CRT にはコア ビジネス ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5780a-106">CRT contains the core business logic.</span></span> <span data-ttu-id="5780a-107">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-107">If you want to add or modify any business logic, you should customize CRT.</span></span> <span data-ttu-id="5780a-108">C# を使用して、すべての CRT コードが開発され、コンパイルされてクラス ライブラリとしてリリースされます (.NET アセンブリ)。</span><span class="sxs-lookup"><span data-stu-id="5780a-108">All the CRT code is developed by using C#, and then it's compiled and released as class libraries (.NET assemblies).</span></span> <span data-ttu-id="5780a-109">販売時点管理 (POS) はシン クライアントです。</span><span class="sxs-lookup"><span data-stu-id="5780a-109">Point of sale (POS) is a thin client.</span></span> <span data-ttu-id="5780a-110">すべてのビジネス ロジックは、CRT で行われます。</span><span class="sxs-lookup"><span data-stu-id="5780a-110">All the business logic is done in CRT.</span></span> <span data-ttu-id="5780a-111">POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-111">POS calls CRT to perform any business logic, and CRT processes the information and then sends it back to POS.</span></span>

<span data-ttu-id="5780a-112">すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-112">Every CRT service consists of a group of one or more requests and responses.</span></span> <span data-ttu-id="5780a-113">POS が、Retail Server に要求を送信し、Retail Server は CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5780a-113">POS sends a request to Retail Server, and Retail Server calls CRT.</span></span> <span data-ttu-id="5780a-114">続いて CRT は要求を処理し、応答を送り返します。</span><span class="sxs-lookup"><span data-stu-id="5780a-114">CRT then processes the request and sends back the response.</span></span>

<span data-ttu-id="5780a-115">たとえば、CRT の顧客サービスには、顧客関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。</span><span class="sxs-lookup"><span data-stu-id="5780a-115">For example, the Customer service in CRT contains all the customer-related requests and responses, each of which is run in a different flow.</span></span> <span data-ttu-id="5780a-116">同様に、CRT の製品サービスには製品に関連するすべての要求と応答が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5780a-116">Likewise, the Product service in CRT contain all the product-related requests and responses.</span></span> <span data-ttu-id="5780a-117">次の表に、顧客サービスの要求を示します。</span><span class="sxs-lookup"><span data-stu-id="5780a-117">The following table shows the requests in the Customer service.</span></span>

| <span data-ttu-id="5780a-118">要求</span><span class="sxs-lookup"><span data-stu-id="5780a-118">Request</span></span>                                      | <span data-ttu-id="5780a-119">目的</span><span class="sxs-lookup"><span data-stu-id="5780a-119">Purpose</span></span>                                                                          |
|----------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5780a-120">SaveCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-120">SaveCustomerServiceRequest</span></span>                   | <span data-ttu-id="5780a-121">この要求は、POS から顧客を保存する場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-121">This request is called when you save a customer from POS.</span></span>                        |
| <span data-ttu-id="5780a-122">GetCustomersServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-122">GetCustomersServiceRequest</span></span>                   | <span data-ttu-id="5780a-123">この要求は、選択した顧客の詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-123">This request is used to get the details of the selected customer.</span></span>                |
| <span data-ttu-id="5780a-124">CustomersSearchServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-124">CustomersSearchServiceRequest</span></span>                | <span data-ttu-id="5780a-125">この要求は、POS から顧客検索を行う場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-125">This request is run when you do a customer search from POS.</span></span>                      |
| <span data-ttu-id="5780a-126">GetCustomerGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-126">GetCustomerGroupsServiceRequest</span></span>              | <span data-ttu-id="5780a-127">この要求は、顧客グループの詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-127">This request is used to get the details of the customer group.</span></span>                   |
| <span data-ttu-id="5780a-128">InitiateLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-128">InitiateLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="5780a-129">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="5780a-129">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="5780a-130">FinalizeLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-130">FinalizeLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="5780a-131">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="5780a-131">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="5780a-132">UnlinkFromExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-132">UnlinkFromExistingCustomerServiceRequest</span></span>     | <span data-ttu-id="5780a-133">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="5780a-133">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="5780a-134">GetCustomerBalanceServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-134">GetCustomerBalanceServiceRequest</span></span>             | <span data-ttu-id="5780a-135">この要求は、顧客勘定の残高を取得します。</span><span class="sxs-lookup"><span data-stu-id="5780a-135">This request gets the balance for the customer account.</span></span>                          |
| <span data-ttu-id="5780a-136">GetOrderHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-136">GetOrderHistoryServiceRequest</span></span>                | <span data-ttu-id="5780a-137">この要求は、顧客の注文履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="5780a-137">This request gets the customer's order history.</span></span>                                  |
| <span data-ttu-id="5780a-138">GetPurchaseHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-138">GetPurchaseHistoryServiceRequest</span></span>             | <span data-ttu-id="5780a-139">この要求は、顧客の最近の購入履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="5780a-139">This request gets the history of the customer's recent purchases.</span></span>                |
| <span data-ttu-id="5780a-140">CustomerSearchByFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-140">CustomerSearchByFieldsServiceRequest</span></span>         | <span data-ttu-id="5780a-141">フィールド (ヒント検索) を使用して顧客を検索する際に、この要求が実行されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-141">This request is run when you search for customers by using fields (hint search).</span></span> |
| <span data-ttu-id="5780a-142">GetCustomerSearchFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="5780a-142">GetCustomerSearchFieldsServiceRequest</span></span>        | <span data-ttu-id="5780a-143">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="5780a-143">This request gets the list of customer search fields (hint fields).</span></span>              |

## <a name="crt-extension-patterns"></a><span data-ttu-id="5780a-144">CRT 拡張パターン</span><span class="sxs-lookup"><span data-stu-id="5780a-144">CRT extension patterns</span></span>

<span data-ttu-id="5780a-145">CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-145">Before you learn about the CRT extension patterns, you should understand how a CRT extension can be created.</span></span> <span data-ttu-id="5780a-146">CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="5780a-146">CRT is just a collection of C# class libraries (.NET assemblies).</span></span> <span data-ttu-id="5780a-147">C# でクラス ライブラリ プロジェクトを作成し、次の表に示すパターンを使用してすべての CRT 拡張を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-147">You can create a class library project in C# and do all the CRT extension by using the patterns that are shown in the following table.</span></span> <span data-ttu-id="5780a-148">これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。</span><span class="sxs-lookup"><span data-stu-id="5780a-148">Always use the samples that Microsoft provides as template for your extension, because these samples have the correct assembly references, Microsoft .NET Framework version, output type, and build parameters.</span></span> <span data-ttu-id="5780a-149">また、他のすべての必須パラメーターがコンフィギュレーション済みです。</span><span class="sxs-lookup"><span data-stu-id="5780a-149">Additionally, all the other required parameters are preconfigured.</span></span> <span data-ttu-id="5780a-150">同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-150">You can find the CRT sample extension in the Retail software development kit (SDK), at …\\RetailSDK\\SampleExtensions\\CommerceRuntime.</span></span>

### <a name="create-a-new-crt-service"></a><span data-ttu-id="5780a-151">新しい CRT サービスの作成</span><span class="sxs-lookup"><span data-stu-id="5780a-151">Create a new CRT service</span></span>

<span data-ttu-id="5780a-152">新機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-152">Create a new functionality/feature.</span></span>

### <a name="override-existing-service"></a><span data-ttu-id="5780a-153">既存のサービスを上書きする</span><span class="sxs-lookup"><span data-stu-id="5780a-153">Override existing Service</span></span>

<span data-ttu-id="5780a-154">完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="5780a-154">You can completely override existing functionality or customize it according to your business flow.</span></span> <span data-ttu-id="5780a-155">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="5780a-155">Here are some examples:</span></span>

+ <span data-ttu-id="5780a-156">POS 検索機能を上書きして、ローカル データベースまたは本社で検索するのではなく、外部システムから検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-156">You want to override the POS search functionality to search from an external system instead of searching in a local database or HQ.</span></span> <span data-ttu-id="5780a-157">または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="5780a-157">Alternatively, you can do an override, call the standard functionality, and do some additional custom logic.</span></span>
+ <span data-ttu-id="5780a-158">ローカル データベースまたは HQ、および外部システムを検索した後、最後に結果をマージまたは変更します。</span><span class="sxs-lookup"><span data-stu-id="5780a-158">Search for a customer in a local database or HQ, and in an external system, and then finally merge or modify the result.</span></span>
+ <span data-ttu-id="5780a-159">ハンドラーの上書きは避けてください。</span><span class="sxs-lookup"><span data-stu-id="5780a-159">Avoid overriding the handler.</span></span> <span data-ttu-id="5780a-160">プレトリガーまたはポストトリガーを使用すると、CRT の拡張機能のシナリオのほとんどを実装できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-160">You can implement most of the CRT extension scenarios by using pre or post triggers.</span></span> <span data-ttu-id="5780a-161">上書きが必要なのは、既存の機能を完全に置換する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="5780a-161">Overriding is required only when you want to completely replace the existing functionality.</span></span></li>

### <a name="triggers"></a><span data-ttu-id="5780a-162">トリガー</span><span class="sxs-lookup"><span data-stu-id="5780a-162">Triggers</span></span>

<span data-ttu-id="5780a-163">任意の要求の前後に追加ロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-163">You can execute additional logic before or after any request.</span></span>

<span data-ttu-id="5780a-164">前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-164">In the pre-trigger, you can do some validation, custom logic, and so on.</span></span>

<span data-ttu-id="5780a-165">ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-165">In the post-trigger, you can add some custom information to the request and send it to POS.</span></span> <span data-ttu-id="5780a-166">または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="5780a-166">Alternatively, you can modify the result that is returned from the standard functionality or do some additional business logic.</span></span>

### <a name="extension-properties"></a><span data-ttu-id="5780a-167">拡張プロパティ</span><span class="sxs-lookup"><span data-stu-id="5780a-167">Extension properties</span></span>

<span data-ttu-id="5780a-168">任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-168">You can add custom properties to any CRT entity and send it to POS.</span></span> <span data-ttu-id="5780a-169">拡張プロパティはキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="5780a-169">Extension properties are key-value pairs.</span></span> <span data-ttu-id="5780a-170">POS で拡張プロパティを設定すると、CRT で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5780a-170">If you set an extension property in POS, it will be available in CRT.</span></span> <span data-ttu-id="5780a-171">同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-171">Likewise, if you set an extension property in CRT, it will be available in POS.</span></span> <span data-ttu-id="5780a-172">また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5780a-172">You can also set extension properties at the level of the request, the response, or the request context.</span></span> <span data-ttu-id="5780a-173">既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。</span><span class="sxs-lookup"><span data-stu-id="5780a-173">By default, extension properties aren't stored in and read from the database.</span></span> <span data-ttu-id="5780a-174">拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-174">To read or set extension properties, you must write custom code.</span></span> <span data-ttu-id="5780a-175">ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-175">However, that custom code is automatically sent between POS and CRT.</span></span>

<span data-ttu-id="5780a-176">たとえば、POS の顧客エンティティーにいくつかの追加情報をキャプチャして表示したいとします。</span><span class="sxs-lookup"><span data-stu-id="5780a-176">For example, you want to capture and show some additional information to the customer entity in POS.</span></span> <span data-ttu-id="5780a-177">この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張子プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-177">In this case, you can add a post-trigger to fetch all your custom properties for customer, add them to the customer entity as extension properties, and send those extension properties to POS.</span></span>

<span data-ttu-id="5780a-178">POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-178">You can also send extension properties from POS to CRT and store them in your custom table.</span></span> <span data-ttu-id="5780a-179">または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または本社への送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="5780a-179">Alternatively, you can do some custom logic based on those properties, or send it to HQ.</span></span>

<span data-ttu-id="5780a-180">製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="5780a-180">All CRT entities, such as products, customers, transactions, and parameters, support extension properties.</span></span>

> [!NOTE]
> <span data-ttu-id="5780a-181">属性もまたサポートされます (コンフィギュレーション駆動型の開発)。</span><span class="sxs-lookup"><span data-stu-id="5780a-181">Attributes are also supported (configuration-driven development).</span></span> <span data-ttu-id="5780a-182">拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-182">For extension properties, you must create a custom table and store the data.</span></span> <span data-ttu-id="5780a-183">ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成するために必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="5780a-183">However, attributes are configuration-driven and aren't required in order to create table fields.</span></span> <span data-ttu-id="5780a-184">したがって、読み取りおよび更新操作にコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5780a-184">Therefore, no code is required for read and update operations.</span></span>

<span data-ttu-id="5780a-185">属性についての詳細は、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5780a-185">For details about the attributes, see the following topics:</span></span>

+ [<span data-ttu-id="5780a-186">注文属性</span><span class="sxs-lookup"><span data-stu-id="5780a-186">Order attributes</span></span>](order-attributes.md)
+ [<span data-ttu-id="5780a-187">顧客属性</span><span class="sxs-lookup"><span data-stu-id="5780a-187">Customer attributes</span></span>](customer-attributes.md)

### <a name="real-time-transaction-service-calls"></a><span data-ttu-id="5780a-188">リアルタイム トランザクション サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="5780a-188">Real-time transaction service calls</span></span>

<span data-ttu-id="5780a-189">CRT から HQ の同期呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-189">You can do synchronous call from CRT to HQ.</span></span>

### <a name="crt-data-service-and-data-service-with-entity"></a><span data-ttu-id="5780a-190">CRT データ サービス、およびエンティティ付きデータ サービス</span><span class="sxs-lookup"><span data-stu-id="5780a-190">CRT data service and data service with entity</span></span>

<span data-ttu-id="5780a-191">チャンネル データベースからデータ/エンティティを読み取るためのデータ サービス。</span><span class="sxs-lookup"><span data-stu-id="5780a-191">Data service to read data/entity from channel database.</span></span>

> [!NOTE]
> <span data-ttu-id="5780a-192">CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (Runtime.Workflow、Runtime.Services、Runtime.DataServices のクラスなど) を参照したり使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5780a-192">CRT extension code should not refer to or use any of the CRT business logic classes, methods, or handlers (such as classes from Runtime.Workflow, Runtime.Services, or Runtime.DataServices).</span></span> <span data-ttu-id="5780a-193">これらのクラスには、下位互換性がありません。アップグレード中に拡張機能が無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-193">These classes are not backward compatible, which could break extensions during an upgrade.</span></span> <span data-ttu-id="5780a-194">拡張では、Runtime.\*.Messages、Runtime.Framework、Runtime.Data、Runtime.Entities の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-194">Extensions should only use request, response, and entity classes from Runtime.\*.Messages, Runtime.Framework, Runtime.Data, and Runtime.Entities.</span></span>

## <a name="register-the-crt-extension"></a><span data-ttu-id="5780a-195">CRT 拡張機能の登録</span><span class="sxs-lookup"><span data-stu-id="5780a-195">Register the CRT extension</span></span>

### <a name="online"></a><span data-ttu-id="5780a-196">オンライン</span><span class="sxs-lookup"><span data-stu-id="5780a-196">Online</span></span>

<span data-ttu-id="5780a-197">オンラインの場合 (POS が Retail Server に接続された場合)、CRT を拡張した後、拡張ライブラリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="5780a-197">For online (when POS is connected to Retail Server), after extending CRT, put the extension library in the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span> <span data-ttu-id="5780a-198">**CommerceRuntime.Ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。</span><span class="sxs-lookup"><span data-stu-id="5780a-198">Update the **composition** section in the **CommerceRuntime.Ext.config** file with the custom library information, as shown in the following example.</span></span>

```xml
<add source="assembly" value="your custom library name" />
```

<span data-ttu-id="5780a-199">たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="5780a-199">For example, if the name of your custom library is **Contoso.Commerce.Runtime.CustomerSearchSample**, add the following line in the **composition** section.</span></span>

```xml
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

### <a name="offline"></a><span data-ttu-id="5780a-200">オフライン</span><span class="sxs-lookup"><span data-stu-id="5780a-200">Offline</span></span>

<span data-ttu-id="5780a-201">オフラインの場合は、CRT を拡張した後、カスタム ライブラリを **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="5780a-201">For offline, after extending CRT, put the custom library in the **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span> <span data-ttu-id="5780a-202">**CommerceRuntime.MPOSOffline.ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。</span><span class="sxs-lookup"><span data-stu-id="5780a-202">Update the **composition** section in the **CommerceRuntime.MPOSOffline.ext.config** file with the custom library information, as shown in the following example.</span></span>

```xml
<add source="assembly" value="your custom library name" />.
```

## <a name="register-the-extension-configuration-in-the-commerceruntimeextconfig-file"></a><span data-ttu-id="5780a-203">CommerceRuntime.Ext.config ファイルに拡張コンフィギュレーションを登録する</span><span class="sxs-lookup"><span data-stu-id="5780a-203">Register the extension configuration in the CommerceRuntime.Ext.config file</span></span>

<span data-ttu-id="5780a-204">拡張機能では、**\<settings\>** ノードの **CommerceRuntime.Ext.config** ファイルに任意のキー値のコンフィギュレーションを登録できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-204">Your extension can register any key-value configurations in the **CommerceRuntime.Ext.config** file in the **\<settings\>** node.</span></span>

<span data-ttu-id="5780a-205">この **\<settings\>** ノードは、CommerceRuntime コンポーネントを設定するために使用されるキーと値のペアのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="5780a-205">This **\<settings\>** node is a key-value pair collection used to configure the CommerceRuntime components.</span></span> <span data-ttu-id="5780a-206">この規則では、接頭語を設定キーの前に付けて、区切り記号としてピリオド (.) を使用して、コンフィギュレーションしている機能領域を表します。</span><span class="sxs-lookup"><span data-stu-id="5780a-206">The convention is to prefix settings keys to represent the functional area they are configuring using a period (.) as separator.</span></span> <span data-ttu-id="5780a-207">Commerce Runtime の初期化では、この規則が適用され、それ以外の場合は読み込まれないので、拡張コンフィギュレーション値の前には必ず **ext** を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-207">Extension configuration values MUST be prefixed with **ext**, because the Commerce Runtime initialization enforces this convention and will not load otherwise.</span></span> <span data-ttu-id="5780a-208">追加の接頭語を追加して、制御するサブ領域を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-208">Additional prefixes can be added to represent the sub-area they control.</span></span> <span data-ttu-id="5780a-209">次の例では、キーと値のペアを設定しています。</span><span class="sxs-lookup"><span data-stu-id="5780a-209">The following example sets a key-value pair.</span></span>

```xml
      <add name="ext.SalesTransaction.Storage.CartSerializationFormat" value="XML" />
```

<span data-ttu-id="5780a-210">リアルタイム サービス呼び出しでの HTTP バインドのタイムアウトについては、メソッドごとにタイムアウトを秒単位でを設定します。</span><span class="sxs-lookup"><span data-stu-id="5780a-210">For HTTP binding timeouts on Realtime Service calls, configure the timeout in seconds per method.</span></span> <span data-ttu-id="5780a-211">このタイムアウト値は、**CommerceRuntime.config** で設定された **maxExtensionTimeoutInSeconds** によって制限されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-211">This timeout value is limited by **maxExtensionTimeoutInSeconds**, which set in **CommerceRuntime.config**.</span></span>

```xml
<add name="ext.RealTimeServiceClient.TimeoutInSeconds.InvokeExtensionMethod.ContosoRetailStoreHours_UpdateStoreHours" value="300" />
```

<span data-ttu-id="5780a-212">CRT 拡張コンフィグからキー値を読み取るために、拡張コードは、**RequestContext.Runtime.Configuration** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-212">To read the key-value from the CRT extension config, extension code can use **RequestContext.Runtime.Configuration**.</span></span> <span data-ttu-id="5780a-213">次の例では、値を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5780a-213">The following example shows how to retrieve a value.</span></span>

```csharp
 string key = context.Runtime.Configuration.GetSettingValue("ext.SalesTransaction.Storage.CartSerializationFormat") ?? string.Empty;
```

<span data-ttu-id="5780a-214">上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-214">The preceding steps are used for manual deployment and testing in your development box.</span></span> <span data-ttu-id="5780a-215">拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="5780a-215">To package the extension and deploy it to production or user acceptance testing (UAT), use the information in the packaging document.</span></span>

## <a name="debugging-crt"></a><span data-ttu-id="5780a-216">CRT のデバッグ</span><span class="sxs-lookup"><span data-stu-id="5780a-216">Debugging CRT</span></span>

### <a name="attach-online"></a><span data-ttu-id="5780a-217">オンラインで関連付け</span><span class="sxs-lookup"><span data-stu-id="5780a-217">Attach online</span></span>

<span data-ttu-id="5780a-218">POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを、**w3wp.exe** (Retail Server の IIS プロセス) に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-218">To debug CRT from POS, you should attach the CRT extension project to **w3wp.exe** (the IIS process for Retail Server) when POS is connected to Retail server.</span></span>

### <a name="attach-offline"></a><span data-ttu-id="5780a-219">オフラインで関連付け</span><span class="sxs-lookup"><span data-stu-id="5780a-219">Attach offline</span></span>

<span data-ttu-id="5780a-220">オフラインの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5780a-220">For offline, attach the CRT extension project to the **dllhost.exe** process.</span></span>

## <a name="using-extension-properties-on-crt-entities-requests-and-responses"></a><span data-ttu-id="5780a-221">CRT エンティティ、依頼および応答での拡張プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="5780a-221">Using extension properties on CRT entities, requests, and responses</span></span>

<span data-ttu-id="5780a-222">既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。</span><span class="sxs-lookup"><span data-stu-id="5780a-222">One way to add new data to an existing CRT entity is to use extension properties.</span></span> <span data-ttu-id="5780a-223">拡張プロパティは、エンティティのキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="5780a-223">Extension properties are key-value pairs on the entity.</span></span> <span data-ttu-id="5780a-224">既定では、これらのキーと値のペアはデータベースで保持されません。</span><span class="sxs-lookup"><span data-stu-id="5780a-224">By default, these key-value pairs aren't persisted in the database.</span></span> <span data-ttu-id="5780a-225">拡張プロパティを保持するためには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-225">To persist an extension property, you must write custom code.</span></span>

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a><span data-ttu-id="5780a-226">CRT エンティティでの拡張プロパティの永続的な使用</span><span class="sxs-lookup"><span data-stu-id="5780a-226">Using extension properties on CRT entities with persistence</span></span>

<span data-ttu-id="5780a-227">エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-227">Any extension property that you add to an entity stays in memory for POS and CRT for the lifetime of either the object or the transaction, depending on the scenario.</span></span> <span data-ttu-id="5780a-228">拡張プロパティは、アプリケーションの境界にもまたがって移動します。</span><span class="sxs-lookup"><span data-stu-id="5780a-228">The extension property also travels across application boundaries.</span></span> <span data-ttu-id="5780a-229">たとえば、Retail Modern POS に拡張プロパティを追加し、Retail Server または CRT を呼び出すと、キーと値のペアがそのフロー全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-229">For example, if you add an extension property in Retail Modern POS and then call Retail Server or CRT, the key-value pair is available during the whole flow.</span></span> <span data-ttu-id="5780a-230">また、そのエンティティが Commerce Data Exchange: Real-time Service を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-230">Additionally, if that entity is sent to during a call to Commerce Data Exchange: Real-time Service, the key-value pair is available during the process.</span></span>

> [!NOTE]
> <span data-ttu-id="5780a-231">HQ では、拡張プロパティは顧客と注文に対してのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-231">For HQ, extension properties are sent only for customers and orders.</span></span>

<span data-ttu-id="5780a-232">ただし、既述のように、拡張プロパティは既定では保持されません。</span><span class="sxs-lookup"><span data-stu-id="5780a-232">However, as mentioned earlier, the extension property isn't persisted by default.</span></span> <span data-ttu-id="5780a-233">拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-233">If you want to persist an extension property, you must do data modeling to help guarantee that you make the correct design choices about where the data should reside.</span></span> <span data-ttu-id="5780a-234">新しいテーブルと結合を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5780a-234">We recommend that you use a new table and a join.</span></span> <span data-ttu-id="5780a-235">この方法は、ほとんどの要件に適合します。</span><span class="sxs-lookup"><span data-stu-id="5780a-235">This approach fits most requirements well.</span></span> <span data-ttu-id="5780a-236">Retail SDK の **EmailPreference** サンプルは、代表的なエンド ツー エンドの例を提供します。</span><span class="sxs-lookup"><span data-stu-id="5780a-236">The **EmailPreference** sample in the Retail SDK provides a good end-to-end example.</span></span>

<span data-ttu-id="5780a-237">**Retail SDK のサンプル コードの場所**</span><span class="sxs-lookup"><span data-stu-id="5780a-237">**Location of the sample code in the Retail SDK**</span></span>

<span data-ttu-id="5780a-238">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="5780a-238">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

<span data-ttu-id="5780a-239">**スクリプトの場所**</span><span class="sxs-lookup"><span data-stu-id="5780a-239">**Location of the scripts**</span></span>

<span data-ttu-id="5780a-240">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="5780a-240">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

<span data-ttu-id="5780a-241">**エンティティに拡張子プロパティを設定する構文**</span><span class="sxs-lookup"><span data-stu-id="5780a-241">**Syntax to set an extension property on an entity**</span></span>

```csharp
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

<span data-ttu-id="5780a-242">**例**</span><span class="sxs-lookup"><span data-stu-id="5780a-242">**Example**</span></span>

<span data-ttu-id="5780a-243">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="5780a-243">**Scenario**</span></span>

<span data-ttu-id="5780a-244">顧客エンティティおよび拡張用に作成された新しい拡張テーブルとフィールドは、拡張テーブルからそれらのフィールドを読み取り、POS に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-244">A new extension table and fields created for the Customer entity and extension need to read those fields from the extension table and send them to POS.</span></span>

<span data-ttu-id="5780a-245">チャネル データベースを拡張する場合は、拡張テーブルにメイン テーブルの主キーを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5780a-245">When you extend the channel database, it's always a good idea to include the primary key from the main table in the extension table.</span></span> <span data-ttu-id="5780a-246">つまり、直接の関係を持たずに、主キーを使用して拡張テーブルからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="5780a-246">That is, don't have a direct relation, and then read the data from the extension table by using the primary key.</span></span>

<span data-ttu-id="5780a-247">**ステップ**</span><span class="sxs-lookup"><span data-stu-id="5780a-247">**Steps**</span></span>

1. <span data-ttu-id="5780a-248">メイン テーブルの主キーを持つチャネル データベース拡張スキーマで **顧客** エンティティの拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-248">Create the extension table for the **Customer** entity in the channel database extension schema that has the primary key of the main table.</span></span>
2. <span data-ttu-id="5780a-249">**顧客** エンティティを読み取る CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="5780a-249">Identify the CRT data request that reads the **Customer** entity.</span></span>
3. <span data-ttu-id="5780a-250">データ要求の転記トリガーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5780a-250">Add a post-trigger for the data request.</span></span> <span data-ttu-id="5780a-251">**顧客** テーブルの主キーを使用して、拡張テーブルを照会し、カスタム フィールドを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-251">You will then be able to use the primary key of the **Customer** table to query your extension table to read the custom fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5780a-252">ポスト トリガー要求でエンティティの主キーを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-252">You can get the primary key for the entity in the post-trigger request.</span></span> <span data-ttu-id="5780a-253">エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5780a-253">That request will have the entity object, and that entity object will have all the required fields.</span></span>

4. <span data-ttu-id="5780a-254">カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。</span><span class="sxs-lookup"><span data-stu-id="5780a-254">Add the custom fields as extension properties to the shared parameters entity in the CRT post-trigger, and send it to POS.</span></span>

## <a name="reading-extension-properties-in-triggers"></a><span data-ttu-id="5780a-255">トリガーの拡張機能プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="5780a-255">Reading extension properties in triggers</span></span>

<span data-ttu-id="5780a-256">顧客テーブルからデータを読み込む要求は、GetCustomerDataRequest です。</span><span class="sxs-lookup"><span data-stu-id="5780a-256">The request that reads the data from the Customer table is GetCustomerDataRequest.</span></span> <span data-ttu-id="5780a-257">次の例では、この要求のポスト トリガーを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5780a-257">The following example shows how you can add a post-trigger for this request.</span></span>

```csharp
namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System;
        using System.Collections.Generic;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Class that implements a post trigger for the GetCustomerDataRequest request type.
        /// </summary>
        public class GetCustomerTriggers : IRequestTriggerAsync
        {
            /// <summary>
            /// Gets the supported requests for this trigger.
            /// </summary>
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] { typeof(GetCustomerDataRequest) };
                }
            }

            /// <summary>
            /// Post trigger code to retrieve extension properties.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>
            public async Task OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(response, "response");

                var customer = ((SingleEntityDataServiceResponse<Customer>)response).Entity;

                if (customer == null)
                {
                    return;
                }

                var query = new SqlPagedQuery(QueryResultSettings.SingleRecord)
                {
                    DatabaseSchema = "ext",
                    Select = new ColumnSet(new string[] { "EMAILOPTIN" }),
                    From = "CUSTOMEREXTENSIONVIEW",
                    Where = "ACCOUNTNUM = @accountNum AND DATAAREAID = @dataAreaId"
                };

                query.Parameters["@accountNum"] = customer.AccountNumber;
                query.Parameters["@dataAreaId"] = request.RequestContext.GetChannelConfiguration().InventLocationDataAreaId;
                using (var databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var extensionsResponse = await databaseContext.ReadEntityAsync<ExtensionsEntity>(query).ConfigureAwait(false);
                    ExtensionsEntity extensions = extensionsResponse.FirstOrDefault();

                    var emailOptIn = extensions != null ? extensions.GetProperty("EMAILOPTIN") : null;
                    if (emailOptIn != null)
                    {
                        customer.SetProperty("EMAILOPTIN", emailOptIn);
                    }
                }
            }

            /// <summary>
            /// Pre trigger code.
            /// </summary>
            /// <param name="request">The request.</param>
            public async Task OnExecuting(Request request)
            {
                // It's only stub to handle async signature.
                await Task.CompletedTask;
            }
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="5780a-258">新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-258">You must change this query, based on your new field and table, or whatever condition you're using.</span></span> <span data-ttu-id="5780a-259">テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5780a-259">When you design the table, make sure that you have the primary key field from the parent table, so that you can query it by using the CRT entity.</span></span> <span data-ttu-id="5780a-260">ほとんどの CRT エンティティには、**RecId** フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-260">Most CRT entities should have the primary key field in them, such as the **RecId** field or another relevant unique field that is used to select the record.</span></span>

## <a name="saving-extension-properties-by-overriding-the-handler"></a><span data-ttu-id="5780a-261">ハンドラーを上書きすることによる拡張プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="5780a-261">Saving extension properties by overriding the handler</span></span>

<span data-ttu-id="5780a-262">**シナリオ**</span><span class="sxs-lookup"><span data-stu-id="5780a-262">**Scenario**</span></span>

<span data-ttu-id="5780a-263">顧客用に新しい拡張テーブルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="5780a-263">You created a new extension table for Customer.</span></span> <span data-ttu-id="5780a-264">顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。</span><span class="sxs-lookup"><span data-stu-id="5780a-264">When values for the extension field for customer come from POS or CRT, you want to store the values in your custom table.</span></span>

> [!NOTE]
> <span data-ttu-id="5780a-265">拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-265">You can set extension properties either in a trigger or by overriding the handler.</span></span> <span data-ttu-id="5780a-266">拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-266">If you just set some extension properties by reading from your extension table, you can use triggers.</span></span>

<span data-ttu-id="5780a-267">**ステップ**</span><span class="sxs-lookup"><span data-stu-id="5780a-267">**Steps**</span></span>

1. <span data-ttu-id="5780a-268">メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-268">Create your extension table for Customers in the channel table that has the primary key relation to the main table.</span></span> <span data-ttu-id="5780a-269">(この場合、メイン テーブルは **CustTable** です。)</span><span class="sxs-lookup"><span data-stu-id="5780a-269">(In this case, the main table is **CustTable**.)</span></span>
2. <span data-ttu-id="5780a-270">**CustTable** にデータを設定する CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="5780a-270">Identify the CRT data request that sets data in **CustTable**.</span></span>
3. <span data-ttu-id="5780a-271">ハンドラを上書きし、基本要求を呼び出して、メイン テーブル (**CustTable**) に値を設定してから、拡張テーブルに値を設定します。</span><span class="sxs-lookup"><span data-stu-id="5780a-271">Override the handler, and call the base request to set values in the main table (**CustTable**) and then the extension table.</span></span>

> [!NOTE]
> <span data-ttu-id="5780a-272">拡張コードでは、拡張手順またはビューに必要な追加のプロパティを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-272">Extension code can pass additional properties required for the extension procedure or view.</span></span> <span data-ttu-id="5780a-273">拡張プロパティは CRT のプレトリガーまたはポストトリガーに保存できますが、CRT ハンドラーをオーバーライドする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5780a-273">Extension properties can be saved in the CRT pre or post triggers, you no not need to override the CRT handler.</span></span> <span data-ttu-id="5780a-274">ハンドラーのオーバーライドは避け、ほとんどの CRT 拡張機能のシナリオはプレトリガーまたはポストトリガーで達成できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-274">Avoid overriding the handler, most of the CRT extension scenarios can be achieved in pre or post trigger.</span></span>

<span data-ttu-id="5780a-275">次の例では、使用される SQL スクリプトがありません。</span><span class="sxs-lookup"><span data-stu-id="5780a-275">The example that follows doesn't have the SQL scripts that are used.</span></span> <span data-ttu-id="5780a-276">完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。</span><span class="sxs-lookup"><span data-stu-id="5780a-276">You can find the full sample code and scripts at the following locations in the Retail SDK.</span></span>

<span data-ttu-id="5780a-277">**Retail SDK のサンプル コードの場所**</span><span class="sxs-lookup"><span data-stu-id="5780a-277">**Location of the sample code in the Retail SDK**</span></span>

<span data-ttu-id="5780a-278">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="5780a-278">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

<span data-ttu-id="5780a-279">**スクリプトの場所**</span><span class="sxs-lookup"><span data-stu-id="5780a-279">**Location of the scripts**</span></span>

<span data-ttu-id="5780a-280">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="5780a-280">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

<span data-ttu-id="5780a-281">**例**</span><span class="sxs-lookup"><span data-stu-id="5780a-281">**Example**</span></span>

```csharp
namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System.Threading.Tasks;
        using System.Transactions;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Create or update customer data request handler.
        /// </summary>
        public sealed class CreateOrUpdateCustomerDataRequestHandler : SingleAsyncRequestHandler<CreateOrUpdateCustomerDataRequest>
        {
            /// <summary>
            /// Executes the workflow to create or update a customer.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <returns>The response.</returns>
            protected override async Task<Response> Process(CreateOrUpdateCustomerDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (var databaseContext = new DatabaseContext(request.RequestContext))
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
                        parameters["@TVP_EXTENSIONPROPERTIESTABLETYPE"] = new ExtensionPropertiesExtTableType(request.Customer.RecordId, request.Customer.ExtensionProperties).DataTable;
                        await databaseContext.ExecuteStoredProcedureNonQueryAsync("[ext].UPDATECUSTOMEREXTENSIONPROPERTIES", parameters, resultSettings: null).ConfigureAwait(false);
                    }

                    transactionScope.Complete();

                    return response;
                }
            }
        }
    }
}
```

<span data-ttu-id="5780a-282">**後で読み込むプロパティを有効にする構文**</span><span class="sxs-lookup"><span data-stu-id="5780a-282">**Syntax to enable the property to be read later**</span></span>

```C#
var property = entity.GetProperty("EXTENSION_PROPERTY_ADDED");
```

## <a name="using-extension-properties-on-crt-request-and-response-types"></a><span data-ttu-id="5780a-283">CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="5780a-283">Using extension properties on CRT request and response types</span></span>

<span data-ttu-id="5780a-284">エンティティと同様、拡張機能プロパティを設定および取得するために要求および応答タイプを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-284">Like entities, request and response types can be extended to set and get extension properties.</span></span> <span data-ttu-id="5780a-285">ただし、要求のライフサイクルでのみ存続し、POS では使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="5780a-285">However, they will persist only for the lifecycle of the request and won't be available in POS.</span></span> <span data-ttu-id="5780a-286">それらをデータベースに保存する場合は、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-286">If you want to save them to the database, you must write custom code.</span></span>

```C#
request.SetProperty("PropertyName", true);
response.SetProperty("PropertyName2", true);
var PropertyName = request.GetProperty("PropertyName");
var BoolPropertyName2 = response.GetProperty("PropertyName2");
```

<span data-ttu-id="5780a-287">**設定または POS の拡張子プロパティの読み取り**</span><span class="sxs-lookup"><span data-stu-id="5780a-287">**Setting or reading extension properties in POS**</span></span>

<span data-ttu-id="5780a-288">POS で拡張プロパティーを設定して、POS アプリケーション プログラミング インターフェース (API) を使用してそれらを CRT に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-288">You can set extension properties in POS and send them to CRT by using the POS application programming interfaces (APIs).</span></span> <span data-ttu-id="5780a-289">または、エンティティ レベルで拡張機能プロパティの送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="5780a-289">Alternatively, you can send extension properties at the entity level.</span></span>

<span data-ttu-id="5780a-290">カート行に拡張プロパティを設定するには、SaveExtensionPropertiesOnCartLinesClientRequest を使用します。</span><span class="sxs-lookup"><span data-stu-id="5780a-290">To set an extension property on the cart line, you use SaveExtensionPropertiesOnCartLinesClientRequest.</span></span> <span data-ttu-id="5780a-291">同様に、買い物カゴ ヘッダーに対して、SaveExtensionPropertiesOnCartClientRequest を使用します。</span><span class="sxs-lookup"><span data-stu-id="5780a-291">Likewise, for the cart header, you use SaveExtensionPropertiesOnCartClientRequest.</span></span>

<span data-ttu-id="5780a-292">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5780a-292">Here is an example.</span></span>

```C#
let sampleExtensionProperty = <ProxyEntities.CommerceProperty>{
    Key: "sampleExtensionProperty",
    Value: <ProxyEntities.CommercePropertyValue>{
        BooleanValue: false
    }
};
this.context.runtime.executeAsync(new SaveExtensionPropertiesOnCartClientRequest([sampleExtensionProperty]));
```

## <a name="reading-the-extension-property-from-the-cart-in-pos"></a><span data-ttu-id="5780a-293">POS のカートから拡張プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="5780a-293">Reading the extension property from the cart in POS</span></span>

```typescript
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

<span data-ttu-id="5780a-294">同様に、製品、顧客、および住所など他のすべてのエンティティから拡張機能プロパティを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5780a-294">Likewise, you can read the extension property from all the other entities, such as products, customers, and addresses.</span></span>

## <a name="implementing-a-new-crt-service-that-handles-multiple-new-requests"></a><span data-ttu-id="5780a-295">複数の新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="5780a-295">Implementing a new CRT service that handles multiple new requests</span></span>

<span data-ttu-id="5780a-296">新しい CRT サービスを実装することが一般的です。</span><span class="sxs-lookup"><span data-stu-id="5780a-296">It's a typical case to implement a new CRT service.</span></span> <span data-ttu-id="5780a-297">最初に、新しい要求および応答クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-297">First, you must create new request and response classes.</span></span>

## <a name="creating-the-request-and-response-classes"></a><span data-ttu-id="5780a-298">要求および応答クラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="5780a-298">Creating the request and response classes</span></span>

<span data-ttu-id="5780a-299">作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-299">For serialization to work, the new request type must implement the **\[DataContract\]** and **\[DataMember\]** attributes.</span></span>

```C#
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
```

<span data-ttu-id="5780a-300">新しい応答タイプは要求タイプに似ています。</span><span class="sxs-lookup"><span data-stu-id="5780a-300">The new response type resembles the request type.</span></span>

```C#
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
```

<span data-ttu-id="5780a-301">次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-301">Next, you must create a new CRT service that uses the request and response types.</span></span>

## <a name="creating-a-new-crt-service"></a><span data-ttu-id="5780a-302">新しい CRT サービス注文を作成しています</span><span class="sxs-lookup"><span data-stu-id="5780a-302">Creating a new CRT service</span></span>

1. <span data-ttu-id="5780a-303">新しいサービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="5780a-303">Implement the new service.</span></span>

    ```typescript
    public class StoreHoursDataService : IRequestHandlerAsync
    ```

2. <span data-ttu-id="5780a-304">インターフェイスのメンバー 2 つを実装します。</span><span class="sxs-lookup"><span data-stu-id="5780a-304">Implement two members of the interface.</span></span> <span data-ttu-id="5780a-305">**SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="5780a-305">The **SupportedRequestTypes** member returns a list of all requests that this service can handle.</span></span> <span data-ttu-id="5780a-306">**実行** メソッドは、このサービスの要求が実行された場合に、CRT が呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="5780a-306">The **execute** method is the method that the CRT calls for you if a request for this service is run.</span></span>

  ```C#
   public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] 
                    {
                        typeof(GetStoreHoursDataRequest),
                     };
                }
            }

    public async Task<Response> Execute(Request request)
            {
                if (request == null)
                {
                    throw new ArgumentNullException("request");
                }

                Type reqType = request.GetType();
                if (reqType == typeof(GetStoreHoursDataRequest))
                {
                    return await this.GetStoreDayHoursAsync((GetStoreHoursDataRequest)request).ConfigureAwait(false);
                }
                else
                {
                    string message = string.Format(CultureInfo.InvariantCulture, "Request '{0}' is not supported.", reqType);
                    Console.WriteLine(message);
                    throw new NotSupportedException(message);
                }
            }

            private async Task<Response> GetStoreDayHoursAsync(GetStoreHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var query = new SqlPagedQuery(request.QueryResultSettings)
                    {
                        DatabaseSchema = "ext",
                        Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                        From = "CONTOSORETAILSTOREHOURSVIEW",
                        Where = "STORENUMBER = @storeNumber",
                    };

                    query.Parameters["@storeNumber"] = request.StoreNumber;
                    return new GetStoreHoursDataResponse(await databaseContext.ReadEntityAsync<DataModel.StoreDayHours>(query).ConfigureAwait(false));
                }
            }
    ```

3. <span data-ttu-id="5780a-307">このトピックの冒頭で説明したように、CRT の拡張機能を登録します。</span><span class="sxs-lookup"><span data-stu-id="5780a-307">Register the CRT extension as mentioned in the beginning of this topic.</span></span>

## <a name="implementing-a-new-crt-service-that-handles-a-single-new-request"></a><span data-ttu-id="5780a-308">1 つの新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="5780a-308">Implementing a new CRT service that handles a single new request</span></span>

<span data-ttu-id="5780a-309">単一の要求サービスを作成すると少し便利になります。</span><span class="sxs-lookup"><span data-stu-id="5780a-309">It’s slightly easier to create a single-request service.</span></span>

```C#
public class CrossLoyaltyCardService : SingleAsyncRequestHandler<GetCrossLoyaltyCardRequest>
```

<span data-ttu-id="5780a-310">前の手順で説明したように登録が行われます。</span><span class="sxs-lookup"><span data-stu-id="5780a-310">Registration is done as described in the previous procedure.</span></span>

## <a name="implementing-a-new-crt-service-that-overrides-the-functionality-of-an-existing-request"></a><span data-ttu-id="5780a-311">既存の要求の機能をオーバーライドする新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="5780a-311">Implementing a new CRT service that overrides the functionality of an existing request</span></span>

<span data-ttu-id="5780a-312">場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-312">In some cases, the request and response types are sufficient, but the service implementation must be changed.</span></span> <span data-ttu-id="5780a-313">新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。</span><span class="sxs-lookup"><span data-stu-id="5780a-313">If some new data must be transmitted, you can also extend entity, request, or response objects by using extension properties.</span></span> <span data-ttu-id="5780a-314">このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5780a-314">In this scenario, you can create the service as described earlier and use the existing IRequestHandler types.</span></span> <span data-ttu-id="5780a-315">また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-315">Additionally, registration in the commerceRuntime.Config file must precede registration of the service that should be overridden.</span></span> <span data-ttu-id="5780a-316">この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。</span><span class="sxs-lookup"><span data-stu-id="5780a-316">This registration order is important because of the way that the Managed Extensibility Framework (MEF) loads the extension dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="5780a-317">ファイルより高いタイプが優先されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-317">The types that are higher in the file win.</span></span>

## <a name="implementing-a-new-crt-entity-and-using-it-in-new-crt-service"></a><span data-ttu-id="5780a-318">新しい CRT エンティティの実装および新しい CRT サービスでの使用</span><span class="sxs-lookup"><span data-stu-id="5780a-318">Implementing a new CRT entity and using it in new CRT service</span></span>

<span data-ttu-id="5780a-319">すべての新しいエンティティは、**CommerceEntity** タイプであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="5780a-319">Any new entity must be of the **CommerceEntity** type.</span></span> <span data-ttu-id="5780a-320">このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-320">When you use this type, lots of low-level functionality is automatically handled for you.</span></span> <span data-ttu-id="5780a-321">次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5780a-321">The following example, which is taken from the StoreHours sample, shows how to create an entity that is bound to the database table.</span></span> <span data-ttu-id="5780a-322">これは、通常のケースです。</span><span class="sxs-lookup"><span data-stu-id="5780a-322">This is the usual case.</span></span>

```C#
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
```

<span data-ttu-id="5780a-323">サービスで新しいエンティティを使用する場合、プロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="5780a-323">When you want to use the new entity in a service, the process is straightforward.</span></span> <span data-ttu-id="5780a-324">前述のように、派生 IRequestHandler として新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-324">As described earlier, you create a new service as a derived IRequestHandler.</span></span> <span data-ttu-id="5780a-325">次に、新しいエンティティを使用するか返すかのいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="5780a-325">Then either use or return the new entity.</span></span> <span data-ttu-id="5780a-326">次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5780a-326">The following example shows how to read the entity from the database and return it as part of the response.</span></span>

```C#
   private async Task<Response> GetStoreDayHoursAsync(GetStoreHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var query = new SqlPagedQuery(request.QueryResultSettings)
                    {
                        DatabaseSchema = "ext",
                        Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                        From = "CONTOSORETAILSTOREHOURSVIEW",
                        Where = "STORENUMBER = @storeNumber",
                    };

                    query.Parameters["@storeNumber"] = request.StoreNumber;
                    return new GetStoreHoursDataResponse(await databaseContext.ReadEntityAsync<DataModel.StoreDayHours>(query).ConfigureAwait(false));
                }
            }
```


> [!NOTE]
> <span data-ttu-id="5780a-327">Commerce エンティティはスレッド セーフではありません。つまり、別のスレッドが書き込みを行っているときに、同じオブジェクトの読み取りや変更を行わないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5780a-327">Commerce entities are not thread safe, which means that the same object should not be read or modified when another thread is writing to it.</span></span> <span data-ttu-id="5780a-328">これは、拡張コードのカスタム エンティティと OOB エンティティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5780a-328">This applies to custom entities and OOB entities in the extension code.</span></span> <span data-ttu-id="5780a-329">同一の共有オブジェクトに対して読み取り/書き込みの操作を同期的に実行する場合は、2 つの異なるスレッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5780a-329">Avoid two different threads when performing read/write activities for the same shared object synchronously.</span></span>

<span data-ttu-id="5780a-330">前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-330">For the preceding example, the CRT runtime engine automatically makes a query to the channel database via the registered data adapter.</span></span> <span data-ttu-id="5780a-331">名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。</span><span class="sxs-lookup"><span data-stu-id="5780a-331">It queries a type that has the name **crt.ISVRetailStoreHoursView**, and generates a **where** clause and columns as specified in the code.</span></span> <span data-ttu-id="5780a-332">カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。</span><span class="sxs-lookup"><span data-stu-id="5780a-332">The customizer is responsible for providing the SQL objects as part of the customization.</span></span>

## <a name="adding-pre-triggers-and-post-triggers-for-a-specific-request"></a><span data-ttu-id="5780a-333">特定の要求のプレトリガーとポストトリガーの追加</span><span class="sxs-lookup"><span data-stu-id="5780a-333">Adding pre-triggers and post-triggers for a specific request</span></span> 

<span data-ttu-id="5780a-334">CRT トリガーの拡張機能の作成方法については、[Commerce Runtime (CRT) トリガーの拡張機能](commerce-runtime-extensibility-trigger.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5780a-334">For information about how to create CRT triggers extension, see [Commerce runtime (CRT) triggers extension](commerce-runtime-extensibility-trigger.md).</span></span>

## <a name="retail-server-extension"></a><span data-ttu-id="5780a-335">Retail Sever の拡張機能</span><span class="sxs-lookup"><span data-stu-id="5780a-335">Retail server extension</span></span>

<span data-ttu-id="5780a-336">新しい Retail Server API を作成する方法については、[新しい Retail Server 拡張 API の作成](retail-server-icontroller-extension.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5780a-336">For information about how to create new Retail server API, see [Create a new Retail Server extension API](retail-server-icontroller-extension.md).</span></span>
