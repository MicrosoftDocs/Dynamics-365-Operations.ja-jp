---
title: Commerce runtime (CRT) の拡張機能
description: このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/21/2021
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
ms.openlocfilehash: 1c6ea1ea65e9ff249ce3762b89da4dabb3c9d388
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070204"
---
# <a name="commerce-runtime-crt-extensibility"></a><span data-ttu-id="46cf6-103">Commerce runtime (CRT) の拡張機能</span><span class="sxs-lookup"><span data-stu-id="46cf6-103">Commerce runtime (CRT) extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46cf6-104">このトピックでは、Commerce Runtime (CRT) を拡張するさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-104">This topic describes various ways that you can extend the commerce runtime (CRT).</span></span> <span data-ttu-id="46cf6-105">ここでは、拡張プロパティの概念について説明し、CRT エンティティに加えて拡張プロパティに永続性を持たせる方法、および持たせないようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-105">It explains the concept of extension properties, and shows how to add them to a CRT entity so that they are persistent and so that they aren't persistent.</span></span>

<span data-ttu-id="46cf6-106">CRT にはコア ビジネス ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-106">CRT contains the core business logic.</span></span> <span data-ttu-id="46cf6-107">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-107">If you want to add or modify any business logic, you should customize CRT.</span></span> <span data-ttu-id="46cf6-108">C# を使用して、すべての CRT コードが開発され、コンパイルされてクラス ライブラリとしてリリースされます (.NET アセンブリ)。</span><span class="sxs-lookup"><span data-stu-id="46cf6-108">All the CRT code is developed by using C#, and then it's compiled and released as class libraries (.NET assemblies).</span></span> <span data-ttu-id="46cf6-109">販売時点管理 (POS) はシン クライアントです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-109">Point of sale (POS) is a thin client.</span></span> <span data-ttu-id="46cf6-110">すべてのビジネス ロジックは、CRT で行われます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-110">All the business logic is done in CRT.</span></span> <span data-ttu-id="46cf6-111">POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-111">POS calls CRT to perform any business logic, and then CRT processes the information and sends it back to POS.</span></span>

<span data-ttu-id="46cf6-112">すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-112">Every CRT service consists of a group of one or more requests and responses.</span></span> <span data-ttu-id="46cf6-113">POS が、Retail Server に要求を送信し、Retail Server は CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-113">POS sends a request to Retail Server, and Retail Server calls CRT.</span></span> <span data-ttu-id="46cf6-114">続いて CRT は要求を処理し、応答を送り返します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-114">CRT then processes the request and sends back the response.</span></span>

<span data-ttu-id="46cf6-115">たとえば、CRT の製品サービスには、製品関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-115">For example, the Product service in CRT contains all the product-related requests and responses, each of which is run in a different flow.</span></span> <span data-ttu-id="46cf6-116">同様に、CRT の顧客サービスには、顧客関連のすべての要求/応答が含まれています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-116">Likewise, the Customer service in CRT contain all the customer-related requests and responses.</span></span> <span data-ttu-id="46cf6-117">次の表に、顧客サービスの要求を示します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-117">The following table shows the requests in the Customer service.</span></span>

| <span data-ttu-id="46cf6-118">要求</span><span class="sxs-lookup"><span data-stu-id="46cf6-118">Request</span></span>                                      | <span data-ttu-id="46cf6-119">目的</span><span class="sxs-lookup"><span data-stu-id="46cf6-119">Purpose</span></span>                                                                          |
|----------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="46cf6-120">SaveCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-120">SaveCustomerServiceRequest</span></span>                   | <span data-ttu-id="46cf6-121">この要求は、POS から顧客を保存する場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-121">This request is called when you save a customer from POS.</span></span>                        |
| <span data-ttu-id="46cf6-122">GetCustomersServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-122">GetCustomersServiceRequest</span></span>                   | <span data-ttu-id="46cf6-123">この要求は、選択した顧客の詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-123">This request is used to get the details of the selected customer.</span></span>                |
| <span data-ttu-id="46cf6-124">CustomersSearchServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-124">CustomersSearchServiceRequest</span></span>                | <span data-ttu-id="46cf6-125">この要求は、POS から顧客検索を行う場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-125">This request is run when you do a customer search from POS.</span></span>                      |
| <span data-ttu-id="46cf6-126">GetCustomerGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-126">GetCustomerGroupsServiceRequest</span></span>              | <span data-ttu-id="46cf6-127">この要求は、顧客グループの詳細を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-127">This request is used to get the details of the customer group.</span></span>                   |
| <span data-ttu-id="46cf6-128">InitiateLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-128">InitiateLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="46cf6-129">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-129">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="46cf6-130">FinalizeLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-130">FinalizeLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="46cf6-131">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-131">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="46cf6-132">UnlinkFromExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-132">UnlinkFromExistingCustomerServiceRequest</span></span>     | <span data-ttu-id="46cf6-133">この内部要求は、下位互換性のためのものです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-133">This internal request is for backward compatibility.</span></span>                             |
| <span data-ttu-id="46cf6-134">GetCustomerBalanceServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-134">GetCustomerBalanceServiceRequest</span></span>             | <span data-ttu-id="46cf6-135">この要求は、顧客勘定の残高を取得します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-135">This request gets the balance for the customer account.</span></span>                          |
| <span data-ttu-id="46cf6-136">GetOrderHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-136">GetOrderHistoryServiceRequest</span></span>                | <span data-ttu-id="46cf6-137">この要求は、顧客の注文履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-137">This request gets the customer's order history.</span></span>                                  |
| <span data-ttu-id="46cf6-138">GetPurchaseHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-138">GetPurchaseHistoryServiceRequest</span></span>             | <span data-ttu-id="46cf6-139">この要求は、顧客の最近の購入履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-139">This request gets the history of the customer's recent purchases.</span></span>                |
| <span data-ttu-id="46cf6-140">CustomerSearchByFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-140">CustomerSearchByFieldsServiceRequest</span></span>         | <span data-ttu-id="46cf6-141">フィールド (ヒント検索) を使用して顧客を検索する際に、この要求が実行されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-141">This request is run when you search for customers by using fields (hint search).</span></span> |
| <span data-ttu-id="46cf6-142">GetCustomerSearchFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="46cf6-142">GetCustomerSearchFieldsServiceRequest</span></span>        | <span data-ttu-id="46cf6-143">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-143">This request gets the list of customer search fields (hint fields).</span></span>              |

## <a name="crt-extension-patterns"></a><span data-ttu-id="46cf6-144">CRT 拡張パターン</span><span class="sxs-lookup"><span data-stu-id="46cf6-144">CRT extension patterns</span></span>

<span data-ttu-id="46cf6-145">CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-145">Before you learn about the CRT extension patterns, you should understand how a CRT extension can be created.</span></span> <span data-ttu-id="46cf6-146">CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-146">CRT is just a collection of C# class libraries (.NET assemblies).</span></span> <span data-ttu-id="46cf6-147">C# でクラス ライブラリ プロジェクトを作成し、次のサブセクションに示すパターンを使用してすべての CRT 拡張を実行できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-147">You can create a class library project in C# and do all the CRT extension by using the patterns that are shown in the following subsections.</span></span> <span data-ttu-id="46cf6-148">これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-148">Always use the samples that Microsoft provides as templates for your extension, because these samples have the correct assembly references, Microsoft .NET Framework version, output type, and build parameters.</span></span> <span data-ttu-id="46cf6-149">また、他のすべての必須パラメーターがコンフィギュレーション済みです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-149">Additionally, all the other required parameters are preconfigured.</span></span> <span data-ttu-id="46cf6-150">同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-150">You can find the CRT sample extension in the Retail software development kit (SDK), at …\\RetailSDK\\SampleExtensions\\CommerceRuntime.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-151">Finance and Operations アプリのバージョン 10.0.16 の場合は、CRT 拡張プロジェクトのすべてのクラス ライブラリで .NET Standard 2.0 を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-151">As of version 10.0.16 of Finance and Operations apps, all class libraries for CRT extension projects must use .NET Standard 2.0 for the target framework.</span></span>

### <a name="create-a-new-crt-service"></a><span data-ttu-id="46cf6-152">新しい CRT サービスの作成</span><span class="sxs-lookup"><span data-stu-id="46cf6-152">Create a new CRT service</span></span>

<span data-ttu-id="46cf6-153">新しい機能または新しい仕様を作成できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-153">You can create new functionality or a new feature.</span></span>

### <a name="override-the-existing-service"></a><span data-ttu-id="46cf6-154">既存のサービスを上書きする</span><span class="sxs-lookup"><span data-stu-id="46cf6-154">Override the existing service</span></span>

<span data-ttu-id="46cf6-155">完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-155">You can completely override existing functionality or customize it according to your business flow.</span></span> <span data-ttu-id="46cf6-156">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-156">Here are some examples:</span></span>

+ <span data-ttu-id="46cf6-157">POS 検索機能を上書きして、ローカル データベースまたは Commerce 本社で検索するのではなく、外部システムから検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-157">You want to override the POS search functionality to search from an external system instead of searching in a local database or Commerce headquarters.</span></span> <span data-ttu-id="46cf6-158">または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-158">Alternatively, you can do an override, call the standard functionality, and do some additional custom logic.</span></span>
+ <span data-ttu-id="46cf6-159">ローカル データベースまたは Commerce 本社を検索し、外部システムを検索した後、結果をマージまたは変更します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-159">Search for a customer in a local database or Commerce headquarters, search for the customer in an external system, and then merge or modify the results.</span></span>

<span data-ttu-id="46cf6-160">ハンドラーの上書きは避けてください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-160">Avoid overriding the handler.</span></span> <span data-ttu-id="46cf6-161">プレ トリガーまたはポスト トリガーを使用すると、CRT の拡張機能のシナリオのほとんどを実装できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-161">You can implement most of the CRT extension scenarios by using pre-triggers or post-triggers.</span></span> <span data-ttu-id="46cf6-162">上書きが必要なのは、既存の機能を完全に置換する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-162">Overrides are required only when you want to completely replace the existing functionality.</span></span>

### <a name="crt-data-service-and-data-service-with-entities"></a><span data-ttu-id="46cf6-163">CRT データ サービス、およびエンティティ付きデータ サービス</span><span class="sxs-lookup"><span data-stu-id="46cf6-163">CRT data service and data service with entities</span></span>

<span data-ttu-id="46cf6-164">CRT データ サービスを使用してチャネル データベースからデータまたはエンティティを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-164">You can use the CRT data service to read data or entities from the channel database.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-165">CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (**Runtime.Workflow**、**Runtime.Services**、**Runtime.DataServices** のクラスなど) を参照したり使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-165">CRT extension code should not refer to or use any of the CRT business logic classes, methods, or handlers (such as classes from **Runtime.Workflow**, **Runtime.Services**, or **Runtime.DataServices**).</span></span> <span data-ttu-id="46cf6-166">これらのクラスには下位互換性がないので、アップグレード中に拡張機能が無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-166">Because these classes aren't backward compatible, extensions could be broken during an upgrade.</span></span> <span data-ttu-id="46cf6-167">拡張では、**Runtime.\*.Messages**、**Runtime.Framework**、**Runtime.Data**、**Runtime.Entities** の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-167">Extensions should use only request, response, and entity classes from **Runtime.\*.Messages**, **Runtime.Framework**, **Runtime.Data**, and **Runtime.Entities**.</span></span>

### <a name="triggers"></a><span data-ttu-id="46cf6-168">トリガー</span><span class="sxs-lookup"><span data-stu-id="46cf6-168">Triggers</span></span>

<span data-ttu-id="46cf6-169">任意の要求の前後に追加ロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-169">You can run additional logic before or after any request.</span></span>

<span data-ttu-id="46cf6-170">前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-170">In the pre-trigger, you can do some validation, custom logic, and so on.</span></span>

<span data-ttu-id="46cf6-171">ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-171">In the post-trigger, you can add some custom information to the request and send it to POS.</span></span> <span data-ttu-id="46cf6-172">または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-172">Alternatively, you can modify the result that is returned from the standard functionality or do some additional business logic.</span></span>

<span data-ttu-id="46cf6-173">CRT トリガーの拡張機能の作成方法については、[Commerce Runtime (CRT) トリガーの拡張機能](commerce-runtime-extensibility-trigger.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-173">For information about how to create CRT trigger extensions, see [Commerce runtime (CRT) triggers extension](commerce-runtime-extensibility-trigger.md).</span></span>

### <a name="extension-properties"></a><span data-ttu-id="46cf6-174">拡張プロパティ</span><span class="sxs-lookup"><span data-stu-id="46cf6-174">Extension properties</span></span>

<span data-ttu-id="46cf6-175">任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-175">You can add custom properties to any CRT entity and send it to POS.</span></span> <span data-ttu-id="46cf6-176">拡張プロパティはキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-176">Extension properties are key-value pairs.</span></span> <span data-ttu-id="46cf6-177">POS で拡張プロパティを設定すると、CRT で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-177">If you set an extension property in POS, it will be available in CRT.</span></span> <span data-ttu-id="46cf6-178">同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-178">Likewise, if you set an extension property in CRT, it will be available in POS.</span></span> <span data-ttu-id="46cf6-179">また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-179">You can also set extension properties at the level of the request, the response, or the request context.</span></span> <span data-ttu-id="46cf6-180">既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-180">By default, extension properties aren't stored in and read from the database.</span></span> <span data-ttu-id="46cf6-181">拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-181">To read or set extension properties, you must write custom code.</span></span> <span data-ttu-id="46cf6-182">ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-182">However, that custom code is automatically sent between POS and CRT.</span></span>

<span data-ttu-id="46cf6-183">たとえば、POS の顧客エンティティにいくつかの追加情報をキャプチャして表示したいとします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-183">For example, you want to capture and show some additional information to the Customer entity in POS.</span></span> <span data-ttu-id="46cf6-184">この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-184">In this case, you can add a post-trigger to fetch all your custom properties for customers, add them to the Customer entity as extension properties, and then send those extension properties to POS.</span></span>

<span data-ttu-id="46cf6-185">POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-185">You can also send extension properties from POS to CRT and store them in your custom table.</span></span> <span data-ttu-id="46cf6-186">または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または Commerce 本社への送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-186">Alternatively, you can do some custom logic based on those properties, or send it to Commerce headquarters.</span></span>

<span data-ttu-id="46cf6-187">製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-187">All CRT entities, such as products, customers, transactions, and parameters, support extension properties.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-188">属性もまたサポートされます (コンフィギュレーション駆動型の開発)。</span><span class="sxs-lookup"><span data-stu-id="46cf6-188">Attributes are also supported (configuration-driven development).</span></span> <span data-ttu-id="46cf6-189">拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-189">For extension properties, you must create a custom table and store the data.</span></span> <span data-ttu-id="46cf6-190">ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成する場合は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-190">However, attributes are configuration driven and aren't required to create table fields.</span></span> <span data-ttu-id="46cf6-191">したがって、読み取りおよび更新操作にコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-191">Therefore, no code is required for read and update operations.</span></span>

<span data-ttu-id="46cf6-192">属性についての詳細は、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-192">For details about the attributes, see the following topics:</span></span>

+ [<span data-ttu-id="46cf6-193">注文属性</span><span class="sxs-lookup"><span data-stu-id="46cf6-193">Order attributes</span></span>](order-attributes.md)
+ [<span data-ttu-id="46cf6-194">顧客属性</span><span class="sxs-lookup"><span data-stu-id="46cf6-194">Customer attributes</span></span>](customer-attributes.md)

### <a name="extend-commerce-data-exchange---real-time-service-classes"></a><span data-ttu-id="46cf6-195">Commerce Data Exchange - リアルタイム サービス クラスの拡張</span><span class="sxs-lookup"><span data-stu-id="46cf6-195">Extend Commerce Data Exchange - Real-time Service classes</span></span>

<span data-ttu-id="46cf6-196">CRT から Commerce 本部の同期呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-196">You can do synchronous call from CRT to Commerce headquarters.</span></span>

<span data-ttu-id="46cf6-197">Commerce Data Exchange - リアル タイム サービスを拡張する方法についての詳細は、[Commerce Data Exchange - リアル タイム サービスの拡張](extend-commerce-data-exchange.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-197">For information about how to extend Commerce Data Exchange - Real-time service, see [Extend Commerce Data Exchange - Real-time Service](extend-commerce-data-exchange.md).</span></span>

## <a name="retail-server-extension"></a><span data-ttu-id="46cf6-198">Retail Server の拡張機能</span><span class="sxs-lookup"><span data-stu-id="46cf6-198">Retail Server extension</span></span>

<span data-ttu-id="46cf6-199">新しい Retail Server API を作成する方法については、[新しい Retail Server 拡張 API の作成](retail-server-icontroller-extension.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-199">For information about how to create new Retail Server APIs, see [Create a new Retail Server extension API](retail-server-icontroller-extension.md).</span></span>

## <a name="register-the-crt-extension"></a><span data-ttu-id="46cf6-200">CRT 拡張機能の登録</span><span class="sxs-lookup"><span data-stu-id="46cf6-200">Register the CRT extension</span></span>

### <a name="online"></a><span data-ttu-id="46cf6-201">オンライン</span><span class="sxs-lookup"><span data-stu-id="46cf6-201">Online</span></span>

<span data-ttu-id="46cf6-202">オンライン モードの場合 (POS が Retail Server に接続された場合)、CRT の拡張を終了後、拡張ライブラリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-202">For online mode (that is, when POS is connected to Retail Server), after you've finished extending CRT, put the extension library in the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span> <span data-ttu-id="46cf6-203">**CommerceRuntime.Ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-203">In the **CommerceRuntime.Ext.config** file, update the **composition** section with the information about the custom library, as shown in the following example.</span></span>

```xml
<add source="assembly" value="your custom library name" />
```

<span data-ttu-id="46cf6-204">たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成** セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-204">For example, if the name of your custom library is **Contoso.Commerce.Runtime.CustomerSearchSample**, add the following line in the **composition** section.</span></span>

```xml
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

### <a name="offline"></a><span data-ttu-id="46cf6-205">オフライン</span><span class="sxs-lookup"><span data-stu-id="46cf6-205">Offline</span></span>

<span data-ttu-id="46cf6-206">オフライン モードの場合は、CRT の拡張を終了後、カスタム ライブラリを **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-206">For offline mode, after you've finished extending CRT, put the custom library in the **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span> <span data-ttu-id="46cf6-207">**CommerceRuntime.MPOSOffline.ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-207">In the **CommerceRuntime.MPOSOffline.ext.config** file, update the **composition** section with the information about the custom library, as shown in the following example.</span></span>

```xml
<add source="assembly" value="your custom library name" />.
```

## <a name="register-the-extension-configuration-in-the-commerceruntimeextconfig-file"></a><span data-ttu-id="46cf6-208">CommerceRuntime.Ext.config ファイルに拡張コンフィギュレーションを登録する</span><span class="sxs-lookup"><span data-stu-id="46cf6-208">Register the extension configuration in the CommerceRuntime.Ext.config file</span></span>

<span data-ttu-id="46cf6-209">拡張機能では、**\<settings\>** ノードの **CommerceRuntime.Ext.config** ファイルにキー値のコンフィギュレーションを登録できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-209">Your extension can register key-value configurations in the **CommerceRuntime.Ext.config** file in the **\<settings\>** node.</span></span>

<span data-ttu-id="46cf6-210">**\<settings\>** ノードは、CommerceRuntime コンポーネントを設定するために使用されるキーと値のペアのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-210">The **\<settings\>** node is a collection of key-value pairs that is used to configure the CommerceRuntime components.</span></span> <span data-ttu-id="46cf6-211">この規則では、設定用のキーにそのキーが構成している機能領域を表す接頭語を付け、接頭語とキーの区切りとしてピリオド (.) を使用します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-211">The convention is to prefix the keys for settings with a representation of the functional area that the keys are configuring, and to use a period (.) as the separator between prefixes and keys.</span></span> <span data-ttu-id="46cf6-212">CRT の初期化では、この規則が適用されるので、拡張コンフィギュレーション値の前には必ず **ext** を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-212">Extension configuration values must be prefixed with **ext**, because the CRT initialization enforces this convention.</span></span> <span data-ttu-id="46cf6-213">その接頭語を持たない拡張子は読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-213">Any extension that doesn't have that prefix won't be loaded.</span></span> <span data-ttu-id="46cf6-214">追加の接頭語を追加して、キーの構成サブ領域を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-214">More prefixes can be added to represent the subarea that the keys are configuring.</span></span> <span data-ttu-id="46cf6-215">次の例では、キーと値のペアを示しています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-215">The following example shows a key-value pair.</span></span>

```xml
<add name="ext.SalesTransaction.Storage.CartSerializationFormat" value="XML" />
```

<span data-ttu-id="46cf6-216">Commerce Data Exchange - リアルタイム サービスへの呼び出しでの HTTP バインドのタイムアウトについては、メソッドごとにタイムアウトを秒単位でを設定します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-216">For HTTP binding time-outs on calls to Commerce Data Exchange - Real-time Service, configure the time-out in seconds per method.</span></span> <span data-ttu-id="46cf6-217">このタイムアウト値は、**CommerceRuntime.config** で設定された **maxExtensionTimeoutInSeconds** 値によって制限されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-217">This time-out value is limited by the **maxExtensionTimeoutInSeconds** value, which is set in the **CommerceRuntime.config** file.</span></span>

```xml
<add name="ext.RealTimeServiceClient.TimeoutInSeconds.InvokeExtensionMethod.ContosoRetailStoreHours_UpdateStoreHours" value="300" />
```

<span data-ttu-id="46cf6-218">CRT 拡張コンフィグレーションからキー値を読み取るために、**RequestContext.Runtime.Configuration** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-218">To read the key value from the CRT extension configuration, use **RequestContext.Runtime.Configuration**.</span></span> <span data-ttu-id="46cf6-219">次の例では、値を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-219">The following example shows how to retrieve a value.</span></span>

```csharp
string key = context.Runtime.Configuration.GetSettingValue("ext.SalesTransaction.Storage.CartSerializationFormat") ?? string.Empty;
```

<span data-ttu-id="46cf6-220">上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-220">The preceding steps are used for manual deployment and testing on your development box.</span></span> <span data-ttu-id="46cf6-221">拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-221">To package the extension and deploy it to production or user acceptance testing (UAT), use the information in the packaging document.</span></span>

## <a name="debug-crt"></a><span data-ttu-id="46cf6-222">デバッグ CRT</span><span class="sxs-lookup"><span data-stu-id="46cf6-222">Debug CRT</span></span>

### <a name="attach-the-crt-extension-project-online"></a><span data-ttu-id="46cf6-223">CRT 拡張 Project Online を関連付ける</span><span class="sxs-lookup"><span data-stu-id="46cf6-223">Attach the CRT extension project online</span></span>

<span data-ttu-id="46cf6-224">POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを **w3wp.exe** プロセス (Retail Server の インターネット インフォメーション サービス \[IIS\] プロセス) に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-224">To debug CRT from POS, attach the CRT extension project to the **w3wp.exe** process (the Internet Information Services \[IIS\] process for Retail Server) when POS is connected to Retail Server.</span></span>

### <a name="attach-the-crt-extension-project-offline"></a><span data-ttu-id="46cf6-225">オフラインで CRT 拡張プロジェクトを関連付ける</span><span class="sxs-lookup"><span data-stu-id="46cf6-225">Attach the CRT extension project offline</span></span>

<span data-ttu-id="46cf6-226">オフライン デバッグの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-226">For offline debugging, attach the CRT extension project to the **dllhost.exe** process.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-227">CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (**Runtime.Workflow**、**Runtime.Services**、**Runtime.DataServices** のクラスなど) を参照したり使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-227">CRT extension code should not refer to or use any of the CRT business logic classes, methods, or handlers (such as classes from **Runtime.Workflow**, **Runtime.Services**, or **Runtime.DataServices**).</span></span> <span data-ttu-id="46cf6-228">これらのクラスには下位互換性がないので、アップグレード中に拡張機能が無効になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-228">Because these classes aren't backward compatible, extensions could be broken during an upgrade.</span></span> <span data-ttu-id="46cf6-229">拡張では、**Runtime.\*.Messages**、**Runtime.Framework**、**Runtime.Data**、**Runtime.Entities** の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-229">Extensions should use only request, response, and entity classes from **Runtime.\*.Messages**, **Runtime.Framework**, **Runtime.Data**, and **Runtime.Entities**.</span></span>

## <a name="sample-to-create-a-new-crt-service-class"></a><span data-ttu-id="46cf6-230">新しい CRT サービス クラス作成のサンプル</span><span class="sxs-lookup"><span data-stu-id="46cf6-230">Sample to create a new CRT service class</span></span>

<span data-ttu-id="46cf6-231">新しいサービス クラスを作成し、1 つ以上の要求または応答を実装できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-231">You can create a new service class, and implement one or more requests and responses.</span></span> <span data-ttu-id="46cf6-232">この方法を使用して新しい機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-232">Use this approach to create a new feature.</span></span>

<span data-ttu-id="46cf6-233">新しい CRT サービスに次のクラスを実装します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-233">Implement the following classes for a new CRT service:</span></span>

- <span data-ttu-id="46cf6-234">**クラスのリクエスト** – このクラスは、POS、Retail サーバー、e コマース、CRT ワークフロー クラスの作業の要求を行います。</span><span class="sxs-lookup"><span data-stu-id="46cf6-234">**Request class** – This class is the POS, Retail Server, e-commerce, or CRT workflow class that is the request to do something.</span></span>
- <span data-ttu-id="46cf6-235">**応答クラス** – このクラスは、呼び出し元の要求に基づいて、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-235">**Response class** – This class returns the response, based on the request to the caller.</span></span>
- <span data-ttu-id="46cf6-236">**ハンドラー クラス** – このクラスには、要求のコア ロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-236">**Handler class** – This class contains the core logic for the request.</span></span> <span data-ttu-id="46cf6-237">ハンドラー クラスで、他の要求を呼び出して、カスタム ロジック、および他のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-237">In the handler class, you can call other requests, do custom logic, and perform other tasks.</span></span>

<span data-ttu-id="46cf6-238">作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-238">For serialization to work, the new request type must implement the **\[DataContract\]** and **\[DataMember\]** attributes.</span></span>

### <a name="request-class"></a><span data-ttu-id="46cf6-239">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="46cf6-239">Request class</span></span>

```csharp
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

### <a name="response-class"></a><span data-ttu-id="46cf6-240">応答クラス</span><span class="sxs-lookup"><span data-stu-id="46cf6-240">Response class</span></span>

<span data-ttu-id="46cf6-241">新しい応答タイプは要求タイプに似ています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-241">The new response type resembles the request type.</span></span>

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

<span data-ttu-id="46cf6-242">次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-242">Next, you must create a new CRT service that uses the request and response types.</span></span>

## <a name="create-a-new-crt-service-class"></a><span data-ttu-id="46cf6-243">新しい CRT サービス クラスの作成</span><span class="sxs-lookup"><span data-stu-id="46cf6-243">Create a new CRT service class</span></span>

1. <span data-ttu-id="46cf6-244">新しいサービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-244">Implement the new service.</span></span>

    ```csharp
    public class StoreHoursDataService : IRequestHandlerAsync
    ```

2. <span data-ttu-id="46cf6-245">インターフェイスのメンバー 2 つを実装します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-245">Implement two members of the interface.</span></span> <span data-ttu-id="46cf6-246">**SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-246">The **SupportedRequestTypes** member returns a list of all requests that this service can handle.</span></span> <span data-ttu-id="46cf6-247">**実行** メソッドは、このサービスの要求が実行された場合に、CRT が呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-247">The **execute** method is the method that CRT calls if a request for this service is run.</span></span>

    ```csharp
    public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                  return new[] 
                  {
                        typeof(GetStoreHoursDataRequest),
                        typeof(UpdateStoreDayHoursDataRequest),
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
                else if (reqType == typeof(UpdateStoreDayHoursDataRequest))
                {
                    return await this.UpdateStoreDayHoursAsync((UpdateStoreDayHoursDataRequest)request).ConfigureAwait(false);
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
            
            private async Task<Response> UpdateStoreDayHoursAsync(UpdateStoreDayHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(request.StoreDayHours, "request.StoreDayHours");
                if (request.StoreDayHours.DayOfWeek < 1 || request.StoreDayHours.DayOfWeek > 7)
                {
                    throw new DataValidationException(DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_ValueOutOfRange);
                }

                InvokeExtensionMethodRealtimeRequest extensionRequest = new InvokeExtensionMethodRealtimeRequest(
                    "ContosoRetailStoreHours_UpdateStoreHours",
                    request.StoreDayHours.Id,
                    request.StoreDayHours.DayOfWeek,
                    request.StoreDayHours.OpenTime,
                    request.StoreDayHours.CloseTime);
                InvokeExtensionMethodRealtimeResponse response = await request.RequestContext.ExecuteAsync<InvokeExtensionMethodRealtimeResponse>(extensionRequest).ConfigureAwait(false);
                ReadOnlyCollection<object> results = response.Result;

                long recId = Convert.ToInt64(results[0]);

                using (var databaseContext = new DatabaseContext(request.RequestContext))
                {
                    ParameterSet parameters = new ParameterSet();
                    parameters["@bi_Id"] = recId;
                    parameters["@i_Day"] = request.StoreDayHours.DayOfWeek;
                    parameters["@i_OpenTime"] = request.StoreDayHours.OpenTime;
                    parameters["@i_ClosingTime"] = request.StoreDayHours.CloseTime;
                    await databaseContext.ExecuteStoredProcedureNonQueryAsync("[ext].UPDATESTOREDAYHOURS", parameters, resultSettings: null).ConfigureAwait(false);
                }

                return new UpdateStoreDayHoursDataResponse(request.StoreDayHours);
            }
    ```

3. <span data-ttu-id="46cf6-248">このトピックで先に説明されたように、 CRT 拡張子を登録します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-248">Register the CRT extension as described earlier in this topic.</span></span>

<span data-ttu-id="46cf6-249">前のサンプル コードに、**UpdateStoreDayHoursDataRequest** と **UpdateStoreDayHoursDataResponse** の実装がありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-249">The preceding sample code is missing the implementation of **UpdateStoreDayHoursDataRequest** and **UpdateStoreDayHoursDataResponse**.</span></span> <span data-ttu-id="46cf6-250">完全なサンプル コードは、Retail SDK の **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.StoreHoursSample** フォルダーで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-250">The full sample code is available in the Retail SDK, at **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.StoreHoursSample**.</span></span>

## <a name="implement-a-new-crt-service-that-handles-a-single-new-request"></a><span data-ttu-id="46cf6-251">1 つの新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="46cf6-251">Implement a new CRT service that handles a single new request</span></span>

<span data-ttu-id="46cf6-252">単一の要求サービスを作成すると少し便利になります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-252">It's slightly easier to create a single-request service.</span></span>

```C#
namespace Contoso
{
    namespace Commerce.Runtime.CrossLoyaltySample
    {
        using System;
        using System.Threading.Tasks;
        using Messages;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Service class responsible executing the service requests.
        /// </summary>
        public class CrossLoyaltyCardService : SingleAsyncRequestHandler<GetCrossLoyaltyCardRequest>
        {
            /// <summary>
            /// Process method. 
            /// </summary>
            /// <param name="request">The request with the loyalty number.</param>
            /// <returns>The discount value.</returns>
            protected override async Task<Response> Process(GetCrossLoyaltyCardRequest request)
            {
                if (request == null)
                {
                    throw new ArgumentNullException("request");
                }

                var serviceResponse = new GetCrossLoyaltyCardResponse(0);

                //Business logic

                return await Task.FromResult(serviceResponse);
            }
        }
    }
}
```

## <a name="implement-a-crt-service-that-overrides-the-functionality-of-an-existing-request"></a><span data-ttu-id="46cf6-253">既存の要求の機能をオーバーライドする CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="46cf6-253">Implement a CRT service that overrides the functionality of an existing request</span></span>

<span data-ttu-id="46cf6-254">場合によっては要求タイプと応答タイプで十分ですが、別のロジックを実行するには標準のサービス実装ロジックを変更する必要があります。また、外部サービスと統合してそのロジックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-254">In some cases, the request and response types are sufficient, but you must change the out-of-box service implementation logic to perform different logic, or you must integrate with an external service to perform that logic.</span></span> <span data-ttu-id="46cf6-255">既定の実装のオーバーライドは、ロジックを完全に置換する場合にのみ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-255">An override of the default implementation must be done only when you want to completely replace the logic.</span></span> <span data-ttu-id="46cf6-256">たとえば、標準の税の実装を使用するのではなくサード パーティの税ロジックを使用する場合は、税サービス要求を上書きします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-256">For example, if you don't want to use the out-of-box tax implementation but want to use third-party tax logic instead, override the tax service request.</span></span> <span data-ttu-id="46cf6-257">その他のシナリオのほとんどは、要求にプレ トリガーまたはポスト トリガーを追加することで達成できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-257">Most other scenarios can be achieved by adding a pre-trigger or post-trigger to the request.</span></span> <span data-ttu-id="46cf6-258">要求を上書きしないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-258">Try to avoid overriding the request.</span></span> <span data-ttu-id="46cf6-259">要求を上書きすると、カスタム ロジックが実行され、この上書きされた要求で行われる将来の拡張機能が利用できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-259">When you override the request, the custom logic will be run, and you might not get the future enhancements that are done in this overridden request.</span></span>

<span data-ttu-id="46cf6-260">また、**commerceRuntime.ext.Config** ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-260">Additionally, registration in the **commerceRuntime.ext.Config** file must precede registration of the service that should be overridden.</span></span> <span data-ttu-id="46cf6-261">この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-261">This registration order is important because of the way that the Managed Extensibility Framework (MEF) loads the extension dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="46cf6-262">ファイルより高いタイプが優先されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-262">The types that are higher in the file take precedence.</span></span>

<span data-ttu-id="46cf6-263">CRT 要求をオーバーライドするには、次の例にあるパターンに従って標準の **CreateOrUpdateCustomerDataRequest** 要求をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-263">To override any CRT request, follow the pattern in the following example that overrides the out-of-box **CreateOrUpdateCustomerDataRequest** request.</span></span>

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

                return new SingleEntityDataServiceResponse<Customer>(customer);
            }
        }
    }
}
```

## <a name="run-the-base-handler-in-the-extension"></a><span data-ttu-id="46cf6-264">拡張機能で基本ハンドラーを実行する</span><span class="sxs-lookup"><span data-stu-id="46cf6-264">Run the base handler in the extension</span></span>

### <a name="nothandledresponse"></a><span data-ttu-id="46cf6-265">NotHandledResponse</span><span class="sxs-lookup"><span data-stu-id="46cf6-265">NotHandledResponse</span></span>

<span data-ttu-id="46cf6-266">一部のシナリオでは、オーバーライドされたロジックで基本ハンドラーを実行する場合、**new NotHandledResponse()** を返すことによって基本ハンドラーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-266">If the overridden logic runs the base handler for some scenarios, execution of the base handler can be achieved by returning **new NotHandledResponse()**.</span></span> <span data-ttu-id="46cf6-267">**NotHandledResponse** が返された場合、CRT フレームワークは、基本または帯域外ロジックの実行を要求する拡張機能を使用するため、 帯域外ハンドラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-267">If **NotHandledResponse** is returned, the CRT framework will use the extension that is requesting to run the base or out-of-band logic, and will run the out-of-band handler.</span></span>

<span data-ttu-id="46cf6-268">**NotHandledResponse** は、拡張機能によって基本ハンドラー ロジックが実行される場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-268">**NotHandledResponse** can be used in scenarios where the extension runs the base handler logic.</span></span> <span data-ttu-id="46cf6-269">たとえば、オーバーライドされた要求が基本ハンドラー ロジックを実行する場合、実行する基本ハンドラーに **NotHandledResponse** を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-269">For example, if the overridden request runs the base handler logic, it can return **NotHandledResponse** for the base handler to run.</span></span> <span data-ttu-id="46cf6-270">または、拡張機能によってカスタム ロジックと基本ロジックが実行される場合は、カスタム ロジックを実行した後で **NotHandledResponse** を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-270">Alternatively, if the extension runs custom logic and base logic, the extension code can return **NotHandledResponse** after it runs the custom logic.</span></span>

```csharp
private Response GetCustomReceiptFieldForSalesTransactionReceipts(GetLocalizationCustomReceiptFieldServiceRequest request)
{
    ThrowIf.Null(request.SalesOrder, nameof(request.SalesOrder));

    string receiptFieldName = request.CustomReceiptField;
    string receiptFieldValue = string.Empty;

    if (request.SalesOrder.TaxCalculationType == TaxCalculationType.GTE)
    {
        switch (receiptFieldName)
        {
            case "Sample":
                receiptFieldValue = this.GetGstRegistrationNumber(request);
                break;
            default:
                return new NotHandledResponse();
        }
    }
    else
    {
        return new NotHandledResponse();
    }

    int receiptFieldLength = request.ReceiptItemInfo == null ? 0 : request.ReceiptItemInfo.Length;
    var returnValue = ReceiptStringUtils.WrapString(receiptFieldValue, receiptFieldLength);

    return new GetCustomReceiptFieldServiceResponse(returnValue);
}
```

## <a name="run-an-extension-request-for-a-channel-type"></a><span data-ttu-id="46cf6-271">チャネル タイプに対して拡張要求を実行する</span><span class="sxs-lookup"><span data-stu-id="46cf6-271">Run an extension request for a channel type</span></span>

<span data-ttu-id="46cf6-272">場合によっては、拡張要求を特定のチャネル タイプに対してのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-272">Sometimes, an extension request must be run only for a specific channel type.</span></span> <span data-ttu-id="46cf6-273">たとえば、要求はオンライン チャネルに対して実行する必要がありますが、小売チャネル (物理店舗) については実行する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-273">For example, the request might have to be run for the online channel but not for the retail channel (physical store).</span></span> <span data-ttu-id="46cf6-274">このような場合は、要求を実行する前にチャネル タイプを確認します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-274">In these cases, before you run the request, check the channel type.</span></span> <span data-ttu-id="46cf6-275">その後、カスタム ロジックを実行するか、**NotHandledResponse()** を呼び出して基本ロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-275">Then run the custom logic, or run the base logic by calling **NotHandledResponse()**.</span></span>

```csharp
if (requestContext.GetChannel().OrgUnitType == RetailChannelType.RetailStore)
{
    // run your extension code here.
}
else
{
    return new NotHandledResponse();
}
```

## <a name="implement-a-new-crt-entity-and-use-it-in-the-new-crt-service"></a><span data-ttu-id="46cf6-276">新しい CRT エンティティの実装および新しい CRT サービスでの使用</span><span class="sxs-lookup"><span data-stu-id="46cf6-276">Implement a new CRT entity and use it in the new CRT service</span></span>

<span data-ttu-id="46cf6-277">すべての新しいエンティティは、**CommerceEntity** タイプから継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-277">Any new entity must inherit from the **CommerceEntity** type.</span></span> <span data-ttu-id="46cf6-278">このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-278">When you use this type, lots of low-level functionality is automatically handled for you.</span></span> <span data-ttu-id="46cf6-279">次の例は **StoreHours** サンプルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-279">The following example is taken from the **StoreHours** sample.</span></span> <span data-ttu-id="46cf6-280">データベース テーブルにバインドされたエンティティを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-280">It shows how to create an entity that is bound to the database table.</span></span> <span data-ttu-id="46cf6-281">このシナリオは共通です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-281">This scenario is common.</span></span>

```csharp
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

<span data-ttu-id="46cf6-282">サービスで新しいエンティティを使用する場合、プロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-282">When you want to use the new entity in a service, the process is straightforward.</span></span> <span data-ttu-id="46cf6-283">このトピックで前述されているように、**IRequestHandler** から派生した新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-283">As was described earlier in this topic, you create a new service that is derived from **IRequestHandler**.</span></span> <span data-ttu-id="46cf6-284">次に、新しいエンティティを使用するか返すかのいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-284">You then either use or return the new entity.</span></span> <span data-ttu-id="46cf6-285">次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="46cf6-285">The following example shows how to read the entity from the database and return it as part of the response.</span></span>

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
> <span data-ttu-id="46cf6-286">Commerce エンティティは、スレッド セーフです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-286">Commerce entities aren't thread safe.</span></span> <span data-ttu-id="46cf6-287">したがって、別のスレッドが書き込みを行っている時、同じオブジェクトを読み取りまたは変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-287">Therefore, the same object should not be read or modified when another thread is writing to it.</span></span> <span data-ttu-id="46cf6-288">この制限は、拡張コードのカスタム エンティティと標準エンティティに適用されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-288">This restriction applies to custom entities and out-of-box entities in the extension code.</span></span> <span data-ttu-id="46cf6-289">同一の共有オブジェクトに対して読み取り/書き込みの操作を同期的に実行する場合は、2 つの異なるスレッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="46cf6-289">You should avoid having two different threads when you do synchronous read or write activities for the same shared object.</span></span>

<span data-ttu-id="46cf6-290">前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-290">In the preceding example, the CRT runtime engine automatically makes a query to the channel database via the registered data adapter.</span></span> <span data-ttu-id="46cf6-291">名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-291">It queries a type that has the name **crt.ISVRetailStoreHoursView**, and generates a **where** clause and columns as specified in the code.</span></span> <span data-ttu-id="46cf6-292">カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。</span><span class="sxs-lookup"><span data-stu-id="46cf6-292">The customizer is responsible for providing the SQL objects as part of the customization.</span></span>

## <a name="using-extension-properties-on-crt-entities-requests-and-responses"></a><span data-ttu-id="46cf6-293">CRT エンティティ、依頼および応答での拡張プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="46cf6-293">Using extension properties on CRT entities, requests, and responses</span></span>

<span data-ttu-id="46cf6-294">既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-294">One way to add new data to an existing CRT entity is to use extension properties.</span></span> <span data-ttu-id="46cf6-295">拡張プロパティは、エンティティのキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="46cf6-295">Extension properties are key-value pairs on the entity.</span></span> <span data-ttu-id="46cf6-296">既定では、これらのキーと値のペアはデータベースで保持されません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-296">By default, these key-value pairs don't persist in the database.</span></span> <span data-ttu-id="46cf6-297">拡張プロパティを保持するためには、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-297">To make an extension property persist, you must write custom code.</span></span>

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a><span data-ttu-id="46cf6-298">CRT エンティティでの拡張プロパティの永続的な使用</span><span class="sxs-lookup"><span data-stu-id="46cf6-298">Using extension properties on CRT entities with persistence</span></span>

<span data-ttu-id="46cf6-299">エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-299">Any extension property that you add to an entity stays in memory for POS and CRT for the lifetime of either the object or the transaction, depending on the scenario.</span></span> <span data-ttu-id="46cf6-300">拡張プロパティは、アプリケーションの境界にもまたがって移動します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-300">The extension property also travels across application boundaries.</span></span> <span data-ttu-id="46cf6-301">たとえば、Retail Modern POS に拡張プロパティを追加し、Retail Server または CRT を呼び出すと、キーと値のペアがそのフロー全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-301">For example, if you add an extension property in Retail Modern POS and then call Retail Server or CRT, the key-value pair is available during the whole flow.</span></span> <span data-ttu-id="46cf6-302">また、そのエンティティが Commerce Data Exchange - リアルタイム サービス を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-302">Additionally, if that entity is sent during a call to Commerce Data Exchange - Real-time Service, the key-value pair is available during the process.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-303">Commerce 本社では、拡張プロパティは顧客と注文に対してのみ送信されます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-303">For Commerce headquarters, extension properties are sent only for customers and orders.</span></span>

<span data-ttu-id="46cf6-304">ただし、既述のように、拡張プロパティは既定では保持されていません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-304">However, as was mentioned earlier, the extension property doesn't persist by default.</span></span> <span data-ttu-id="46cf6-305">拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-305">If you want an extension property to persist, you must do data modeling to ensure that you make the correct design choices about where the data should reside.</span></span> <span data-ttu-id="46cf6-306">新しいテーブルと結合を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-306">We recommend that you use a new table and a join.</span></span> <span data-ttu-id="46cf6-307">この方法は、ほとんどの要件に適合します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-307">This approach fits most requirements well.</span></span> <span data-ttu-id="46cf6-308">Retail SDK の **EmailPreference** サンプルは、代表的なエンド ツー エンドの例を提供します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-308">The **EmailPreference** sample in the Retail SDK provides a good end-to-end example.</span></span>

### <a name="location-of-the-sample-code-in-the-retail-sdk"></a><span data-ttu-id="46cf6-309">Retail SDK のサンプル コードの場所</span><span class="sxs-lookup"><span data-stu-id="46cf6-309">Location of the sample code in the Retail SDK</span></span>

<span data-ttu-id="46cf6-310">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="46cf6-310">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

### <a name="location-of-the-scripts"></a><span data-ttu-id="46cf6-311">スクリプトの場所</span><span class="sxs-lookup"><span data-stu-id="46cf6-311">Location of the scripts</span></span>

<span data-ttu-id="46cf6-312">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="46cf6-312">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

### <a name="syntax-to-set-an-extension-property-on-an-entity"></a><span data-ttu-id="46cf6-313">エンティティに拡張子プロパティを設定する構文</span><span class="sxs-lookup"><span data-stu-id="46cf6-313">Syntax to set an extension property on an entity</span></span>

```csharp
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

### <a name="example"></a><span data-ttu-id="46cf6-314">例</span><span class="sxs-lookup"><span data-stu-id="46cf6-314">Example</span></span>

#### <a name="scenario"></a><span data-ttu-id="46cf6-315">シナリオ</span><span class="sxs-lookup"><span data-stu-id="46cf6-315">Scenario</span></span>

<span data-ttu-id="46cf6-316">顧客エンティティおよび拡張用に作成された新しい拡張テーブルとフィールドは、拡張テーブルからそれらのフィールドを読み取り、POS に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-316">A new extension table and fields that were created for the Customer entity and extension must read those fields from the extension table and send them to POS.</span></span>

<span data-ttu-id="46cf6-317">チャネル データベースを拡張する場合は、拡張テーブルにメイン テーブルの主キーを含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="46cf6-317">When you extend the channel database, it's always a good idea to include the primary key from the main table in the extension table.</span></span> <span data-ttu-id="46cf6-318">つまり、直接の関係を持たずに、主キーを使用して拡張テーブルからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-318">That is, don't have a direct relation, and then read the data from the extension table by using the primary key.</span></span>

#### <a name="steps"></a><span data-ttu-id="46cf6-319">ステップ</span><span class="sxs-lookup"><span data-stu-id="46cf6-319">Steps</span></span>

1. <span data-ttu-id="46cf6-320">メイン テーブルの主キーを持つチャネル データベース拡張スキーマで 顧客 エンティティの拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-320">Create the extension table for the Customer entity in the channel database extension schema that has the primary key of the main table.</span></span>
2. <span data-ttu-id="46cf6-321">顧客エンティティを読み取る CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-321">Identify the CRT data request that reads the Customer entity.</span></span>
3. <span data-ttu-id="46cf6-322">データ要求の転記トリガーを追加します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-322">Add a post-trigger for the data request.</span></span> <span data-ttu-id="46cf6-323">顧客 テーブルの主キーを使用して、拡張テーブルを照会し、カスタム フィールドを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-323">You will then be able to use the primary key of the Customer table to query your extension table to read the custom fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46cf6-324">ポスト トリガー要求でエンティティの主キーを取得できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-324">You can get the primary key for the entity in the post-trigger request.</span></span> <span data-ttu-id="46cf6-325">エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="46cf6-325">That request will have the entity object, and that entity object will have all the required fields.</span></span>

4. <span data-ttu-id="46cf6-326">カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-326">Add the custom fields as extension properties to the shared parameters entity in the CRT post-trigger, and send it to POS.</span></span>

## <a name="reading-extension-properties-in-triggers"></a><span data-ttu-id="46cf6-327">トリガーの拡張機能プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="46cf6-327">Reading extension properties in triggers</span></span>

<span data-ttu-id="46cf6-328">顧客テーブルからデータを読み込む要求は、**GetCustomerDataRequest** です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-328">The request that reads the data from the Customer table is **GetCustomerDataRequest**.</span></span> <span data-ttu-id="46cf6-329">次の例では、この要求のポスト トリガーを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-329">The following example shows how you can add a post-trigger for this request.</span></span>

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
> <span data-ttu-id="46cf6-330">新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-330">You must change this query, based on your new field and table, or whatever condition you're using.</span></span> <span data-ttu-id="46cf6-331">テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-331">When you design the table, make sure that you have the primary key field from the parent table, so that you can query it by using the CRT entity.</span></span> <span data-ttu-id="46cf6-332">ほとんどの CRT エンティティには、**RecId** フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-332">Most CRT entities should have the primary key field in them, such as the **RecId** field or another relevant unique field that is used to select the record.</span></span>

## <a name="saving-extension-properties-by-overriding-the-handler"></a><span data-ttu-id="46cf6-333">ハンドラーを上書きすることによる拡張プロパティの保存</span><span class="sxs-lookup"><span data-stu-id="46cf6-333">Saving extension properties by overriding the handler</span></span>

### <a name="scenario"></a><span data-ttu-id="46cf6-334">シナリオ</span><span class="sxs-lookup"><span data-stu-id="46cf6-334">Scenario</span></span>

<span data-ttu-id="46cf6-335">顧客用に新しい拡張テーブルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="46cf6-335">You created a new extension table for Customer.</span></span> <span data-ttu-id="46cf6-336">顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-336">When values for the extension field for Customer come from POS or CRT, you want to store the values in your custom table.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-337">拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-337">You can set extension properties either in a trigger or by overriding the handler.</span></span> <span data-ttu-id="46cf6-338">拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-338">If you just set some extension properties by reading from your extension table, you can use triggers.</span></span>

### <a name="steps"></a><span data-ttu-id="46cf6-339">ステップ</span><span class="sxs-lookup"><span data-stu-id="46cf6-339">Steps</span></span>

1. <span data-ttu-id="46cf6-340">メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-340">Create your extension table for Customer in the channel table that has the primary key relation to the main table.</span></span> <span data-ttu-id="46cf6-341">(この場合、メイン テーブルは CustTable です。)</span><span class="sxs-lookup"><span data-stu-id="46cf6-341">(In this case, the main table is CustTable.)</span></span>
2. <span data-ttu-id="46cf6-342">CustTable にデータを設定する CRT データ要求を識別します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-342">Identify the CRT data request that sets data in CustTable.</span></span>
3. <span data-ttu-id="46cf6-343">ハンドラーを上書きし、メイン テーブル (CustTable) で値を設定する基本要求を呼び出してから、拡張テーブルで値を設定する基本要求を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-343">Override the handler, and call the base request to set values in the main table (CustTable) and then in the extension table.</span></span>

> [!NOTE]
> <span data-ttu-id="46cf6-344">拡張コードでは、拡張手順またはビューに必要な追加のプロパティを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-344">Extension code can pass additional properties that are required for the extension procedure or view.</span></span> <span data-ttu-id="46cf6-345">拡張プロパティは、CRT プレ トリガーまたはポスト トリガーに保存できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-345">Extension properties can be saved in the CRT pre-triggers or post-triggers.</span></span> <span data-ttu-id="46cf6-346">CRT ハンドラーを上書きする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-346">You don't have to override the CRT handler.</span></span> <span data-ttu-id="46cf6-347">ハンドラーのオーバーライドは避けます。ほとんどの CRT 拡張機能のシナリオはプレ トリガーまたはポスト トリガーで達成できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-347">You should avoid overriding the handler, because most of the CRT extension scenarios can be achieved in pre-triggers or post-triggers.</span></span>

<span data-ttu-id="46cf6-348">次の例では、使用される SQL スクリプトがありません。</span><span class="sxs-lookup"><span data-stu-id="46cf6-348">The example that follows doesn't have the SQL scripts that are used.</span></span> <span data-ttu-id="46cf6-349">完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-349">You can find the full sample code and scripts in the following locations in the Retail SDK.</span></span>

### <a name="location-of-the-sample-code-in-the-retail-sdk"></a><span data-ttu-id="46cf6-350">Retail SDK のサンプル コードの場所</span><span class="sxs-lookup"><span data-stu-id="46cf6-350">Location of the sample code in the Retail SDK</span></span>

<span data-ttu-id="46cf6-351">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span><span class="sxs-lookup"><span data-stu-id="46cf6-351">…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample</span></span>

### <a name="location-of-the-scripts"></a><span data-ttu-id="46cf6-352">スクリプトの場所</span><span class="sxs-lookup"><span data-stu-id="46cf6-352">Location of the scripts</span></span>

<span data-ttu-id="46cf6-353">…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference</span><span class="sxs-lookup"><span data-stu-id="46cf6-353">…\\RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference</span></span>

### <a name="example"></a><span data-ttu-id="46cf6-354">例</span><span class="sxs-lookup"><span data-stu-id="46cf6-354">Example</span></span>

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

### <a name="syntax-to-enable-the-property-to-be-read-later"></a><span data-ttu-id="46cf6-355">後で読み込むプロパティを有効にする構文</span><span class="sxs-lookup"><span data-stu-id="46cf6-355">Syntax to enable the property to be read later</span></span>

```C#
var property = entity.GetProperty("EXTENSION_PROPERTY_ADDED");
```

## <a name="using-extension-properties-on-crt-request-and-response-types"></a><span data-ttu-id="46cf6-356">CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="46cf6-356">Using extension properties on CRT request and response types</span></span>

<span data-ttu-id="46cf6-357">エンティティと同様、拡張機能プロパティを設定および取得するために要求および応答タイプを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-357">Like entities, request and response types can be extended to set and get extension properties.</span></span> <span data-ttu-id="46cf6-358">ただし、要求のライフサイクルでのみ存続し、POS では使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-358">However, they persist only for the lifecycle of the request and won't be available in POS.</span></span> <span data-ttu-id="46cf6-359">それらをデータベースに保存する場合は、カスタム コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46cf6-359">If you want to save them to the database, you must write custom code.</span></span>

```C#
request.SetProperty("PropertyName", true);
response.SetProperty("PropertyName2", true);
var PropertyName = request.GetProperty("PropertyName");
var BoolPropertyName2 = response.GetProperty("PropertyName2");
```

### <a name="setting-or-reading-extension-properties-in-pos"></a><span data-ttu-id="46cf6-360">設定または POS の拡張子プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="46cf6-360">Setting or reading extension properties in POS</span></span>

<span data-ttu-id="46cf6-361">POS で拡張プロパティーを設定して、POS API を使用してそれらを CRT に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-361">You can set extension properties in POS and send them to CRT by using the POS APIs.</span></span> <span data-ttu-id="46cf6-362">または、エンティティ レベルで拡張機能プロパティの送信が可能です。</span><span class="sxs-lookup"><span data-stu-id="46cf6-362">Alternatively, you can send extension properties at the entity level.</span></span>

<span data-ttu-id="46cf6-363">カート行に拡張プロパティを設定するには、**SaveExtensionPropertiesOnCartLinesClientRequest** を使用します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-363">To set an extension property on the cart line, you use **SaveExtensionPropertiesOnCartLinesClientRequest**.</span></span> <span data-ttu-id="46cf6-364">同様に、買い物カゴ ヘッダーに対して、**SaveExtensionPropertiesOnCartClientRequest** を使用します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-364">Likewise, for the cart header, you use **SaveExtensionPropertiesOnCartClientRequest**.</span></span>

<span data-ttu-id="46cf6-365">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="46cf6-365">Here is an example.</span></span>

```C#
let sampleExtensionProperty = <ProxyEntities.CommerceProperty>{
    Key: "sampleExtensionProperty",
    Value: <ProxyEntities.CommercePropertyValue>{
        BooleanValue: false
    }
};
this.context.runtime.executeAsync(new SaveExtensionPropertiesOnCartClientRequest([sampleExtensionProperty]));
```

## <a name="reading-the-extension-property-from-the-cart-in-pos"></a><span data-ttu-id="46cf6-366">POS のカートから拡張プロパティの読み取り</span><span class="sxs-lookup"><span data-stu-id="46cf6-366">Reading the extension property from the cart in POS</span></span>

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

<span data-ttu-id="46cf6-367">同様に、製品、顧客、および住所など他のすべてのエンティティから拡張機能プロパティを読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="46cf6-367">Likewise, you can read the extension property from all the other entities, such as products, customers, and addresses.</span></span>
