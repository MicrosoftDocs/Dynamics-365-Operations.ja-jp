---
title: "Commerce Runtime (CRT) のサービス"
description: "このトピックでは、小売チャネルおよび価格設定機能のコア ビジネス ロジックを含むポータブル .NET ライブラリの集合である Commerce runtime (CRT) サービスについて説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-18-05
ms.dyn365.ops.version: AX 8.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 35182afafd3649b9669564b289cdfc5a39975e20
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="commerce-runtime-crt-services"></a><span data-ttu-id="f5f84-103">Commerce Runtime (CRT) のサービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-103">Commerce runtime (CRT) services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5f84-104">Commerce runtime (CRT) は、小売チャネルおよび価格設定機能のコア ビジネス ロジックを含む、ポータブル .NET ライブラリの集合です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-104">Commerce runtime (CRT) is a collection of portable .NET libraries that contain the core business logic for the retail channel and pricing functionality.</span></span> <span data-ttu-id="f5f84-105">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-105">To add or modify any business logic, you should customize CRT.</span></span> <span data-ttu-id="f5f84-106">Retail Modern POS またはクラウド POS は、ビジネス ロジックの実行を要求するため CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-106">Retail Modern POS or Cloud POS calls CRT to request that it perform business logic.</span></span> <span data-ttu-id="f5f84-107">CRT は要求を処理し、小売販売時点管理に応答を送り返します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-107">CRT processes the request and then sends the response back to retail point of sale.</span></span> <span data-ttu-id="f5f84-108">小売販売時点管理はシン クライアントのようで、すべてのビジネス ロジックを CRT で実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-108">Retail point of sale is like a thin client, all the business logic should be done in CRT.</span></span>

<span data-ttu-id="f5f84-109">CRT サービスは、要求/応答のグループです。</span><span class="sxs-lookup"><span data-stu-id="f5f84-109">A CRT service is a group of requests/responses.</span></span> <span data-ttu-id="f5f84-110">POS で作業する際はいつでも、POSは Retail サーバーに要求を送り、Retail サーバーは CRT を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-110">Any time that you do something in POS, POS sends a request to Retail server, and Retail server calls CRT.</span></span> <span data-ttu-id="f5f84-111">CRT は要求を処理し、応答を送り返します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-111">CRT processes the request and sends back the response.</span></span>

<span data-ttu-id="f5f84-112">このトピックでは、ビジネス シナリオにカスタマイズ可能な重要な要求/応答の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-112">This topic shows some important requests/responses that you can customize for your business scenario.</span></span>

<span data-ttu-id="f5f84-113">CRT には、次の 3 つの主要なレイヤーがあります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-113">There are three main layers in CRT:</span></span>

- <span data-ttu-id="f5f84-114">サービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-114">Services</span></span>
- <span data-ttu-id="f5f84-115">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f5f84-115">Workflow</span></span>
- <span data-ttu-id="f5f84-116">データ アクセス</span><span class="sxs-lookup"><span data-stu-id="f5f84-116">Data Access</span></span>

<span data-ttu-id="f5f84-117">ビジネス ロジックのすべての CRT カスタマイズがワークフローまたはデータ アクセス レイヤーのサービスで実行可能で、CRT が作業するに必要な他のコア レイヤーは、ランタイム、認証、およびデータ アクセスのマネージャーであり、これらのレイヤーのカスタマイズは避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-117">All CRT customization for business logic can be done in Services, Workflow or Data Access layers, other core layers that are required for CRT to work are runtime, authentication, and data access managers and you should avoid any customization on these layers.</span></span>

## <a name="overall-flow"></a><span data-ttu-id="f5f84-118">全体的な流れ</span><span class="sxs-lookup"><span data-stu-id="f5f84-118">Overall flow</span></span>
<span data-ttu-id="f5f84-119">全体的なフローは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-119">The overall flow looks like this:</span></span>

<span data-ttu-id="f5f84-120">CRT サービス要求\<\> 1 つ以上のワークフロー要求\<\> 1 つ以上のデータ アクセス要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-120">CRT service request \< \> Zero or more workflow requests \< \> Zero or more data access requests</span></span>

<span data-ttu-id="f5f84-121">たとえば、複数のワークフローおよびデータ アクセス要求が呼び出されて**販売注文の作成**サービス要求が実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-121">For example, multiple workflow and data access requests are called to perform the **Create sales order** service request.</span></span>

## <a name="crt-services"></a><span data-ttu-id="f5f84-122">CRT サービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-122">CRT services</span></span>

<span data-ttu-id="f5f84-123">各 CRT サービスには、1 つ以上の要求または応答が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5f84-123">Each CRT service contains one or more requests/responses.</span></span> <span data-ttu-id="f5f84-124">たとえば、CRT の顧客サービスには、顧客関連のすべての要求/応答が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5f84-124">For example, the Customer service in CRT contains all the customer-related requests/responses.</span></span> <span data-ttu-id="f5f84-125">各要求または応答は、さまざまなフローで実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-125">Each request/response is run in a different flow.</span></span>

### <a name="default-crt-services"></a><span data-ttu-id="f5f84-126">既定の CRT サービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-126">Default CRT services</span></span>

<span data-ttu-id="f5f84-127">CRT の多くのサービスは、小売チャンネルおよび店舗運営の機能をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f5f84-127">Many services in CRT support the functionality of the retail channel and store operations.</span></span> <span data-ttu-id="f5f84-128">独自のサービスを追加したり、既存のサービスを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-128">You can add your own services or extend the existing services.</span></span> <span data-ttu-id="f5f84-129">次の表では、さまざまなビジネス サービス用にカスタマイズする可能性があるサービスの一部について説明します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-129">The following table describes some of the services that you might customize for various business services.</span></span>

<span data-ttu-id="f5f84-130">各サービスの詳細については、以下のRetail ソフトウェア開発キット (SDK) の CRT 要求/応答 ドキュメントを参照してください。 …\\RetailSDK\\Code\\Documents\\CommerceRuntimeMessages.chm.</span><span class="sxs-lookup"><span data-stu-id="f5f84-130">For more information about each service, see the CRT request/response document in the Retail software development kit (SDK), at …\\RetailSDK\\Code\\Documents\\CommerceRuntimeMessages.chm.</span></span>

| <span data-ttu-id="f5f84-131">サービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-131">Service</span></span>                    | <span data-ttu-id="f5f84-132">説明</span><span class="sxs-lookup"><span data-stu-id="f5f84-132">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="f5f84-133">AddressService</span><span class="sxs-lookup"><span data-stu-id="f5f84-133">AddressService</span></span>             | <span data-ttu-id="f5f84-134">このサービスは、住所を確認し、市町村、市区郡、都道府県などの場所情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-134">This service verifies addresses and gets location information, such as cities, counties, or states.</span></span> |
| <span data-ttu-id="f5f84-135">BarcodeService</span><span class="sxs-lookup"><span data-stu-id="f5f84-135">BarcodeService</span></span>             | <span data-ttu-id="f5f84-136">このサービスは、マスクとバーコード タイプに基づいて、スキャンしたバーコードを処理し、バーコードから数量と価格を計算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-136">This service processes the barcode that was scanned, based on the mask and barcode types, and calculates the quantity and price from the barcode.</span></span> |
| <span data-ttu-id="f5f84-137">CartService</span><span class="sxs-lookup"><span data-stu-id="f5f84-137">CartService</span></span>                | <span data-ttu-id="f5f84-138">このサービスは、トランザクションからカートを取得し、トランザクション テーブルから販売トランザクション サービスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-138">This service gets the cart from the transaction and sales transaction service from the transaction tables.</span></span> |
| <span data-ttu-id="f5f84-139">ChargeService</span><span class="sxs-lookup"><span data-stu-id="f5f84-139">ChargeService</span></span>              | <span data-ttu-id="f5f84-140">このサービスは、自動請求、諸費用価格、およびトランザクションの出荷費用を計算するロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-140">This service implements logic that calculates automatic charges, price charges, and shipping charges for transactions.</span></span> |
| <span data-ttu-id="f5f84-141">CouponService</span><span class="sxs-lookup"><span data-stu-id="f5f84-141">CouponService</span></span>              | <span data-ttu-id="f5f84-142">このサービスは、検証およびクーポン関連の要求を更新します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-142">This service validates and updates coupon-related requests.</span></span> |
| <span data-ttu-id="f5f84-143">CurrencyService</span><span class="sxs-lookup"><span data-stu-id="f5f84-143">CurrencyService</span></span>            | <span data-ttu-id="f5f84-144">このサービスは、為替レートに基づいて通貨を変換します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-144">This service converts currencies, based on exchange rates.</span></span> |
| <span data-ttu-id="f5f84-145">CustomerService</span><span class="sxs-lookup"><span data-stu-id="f5f84-145">CustomerService</span></span>            | <span data-ttu-id="f5f84-146">このサービスには顧客の保存、購買履歴、顧客の取得および顧客残高などの、顧客に関連する操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5f84-146">This service contains customer related operations such as Save cusotomer, purchase history, get customer and customer balance.</span></span> |
| <span data-ttu-id="f5f84-147">従業員サービス</span><span class="sxs-lookup"><span data-stu-id="f5f84-147">EmployeeService</span></span>            | <span data-ttu-id="f5f84-148">このサービスは、従業員関連の情報と店舗別の従業員を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-148">This service gets employee-related information and employees by store.</span></span> |
| <span data-ttu-id="f5f84-149">FormattingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-149">FormattingService</span></span>          | <span data-ttu-id="f5f84-150">このサービスは、数字、通貨、および日付の形式のロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-150">This service implements logic for the format of numbers, currencies, and dates.</span></span> |
| <span data-ttu-id="f5f84-151">GiftCardService</span><span class="sxs-lookup"><span data-stu-id="f5f84-151">GiftCardService</span></span>            | <span data-ttu-id="f5f84-152">このサービスは、ギフト カードの発行、残高の取得、値の付加などのギフト カードに関連する内部の活動に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-152">This service provides information about internal activities that are related to gift cards, such as issuing the gift card, getting the balance, and adding value.</span></span> |
| <span data-ttu-id="f5f84-153">LoyaltyService</span><span class="sxs-lookup"><span data-stu-id="f5f84-153">LoyaltyService</span></span>             | <span data-ttu-id="f5f84-154">このサービスは、リピート顧客に報酬を与えるプログラムを実装します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-154">This service implements a program that rewards repeat customers.</span></span> |
| <span data-ttu-id="f5f84-155">NotificationService</span><span class="sxs-lookup"><span data-stu-id="f5f84-155">NotificationService</span></span>        | <span data-ttu-id="f5f84-156">このサービスは、POS 通知サービスを管理します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-156">This service maintains the POS notification service.</span></span> |
| <span data-ttu-id="f5f84-157">PaymentService</span><span class="sxs-lookup"><span data-stu-id="f5f84-157">PaymentService</span></span>             | <span data-ttu-id="f5f84-158">このサービスでは、オンライン ストアから支払サービスに接続し、クレジット カード認証を提供し、コンフィギュレーション済の支払処理を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-158">This service lets you connect your online store to a payment service to provide credit card authorization and use preconfigured payment processing.</span></span> <span data-ttu-id="f5f84-159">また、支払いサービスを拡張して、サード パーティの支払いプロセッサを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-159">You can also extend the payment service to add additional third-party payment processors.</span></span> |
| <span data-ttu-id="f5f84-160">ProductService</span><span class="sxs-lookup"><span data-stu-id="f5f84-160">ProductService</span></span>             | <span data-ttu-id="f5f84-161">このサービスは、製品関連およびバリアントに関連する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-161">This service gets product-related and variant-related information.</span></span> |
| <span data-ttu-id="f5f84-162">ProductsService</span><span class="sxs-lookup"><span data-stu-id="f5f84-162">ProductsService</span></span>            | <span data-ttu-id="f5f84-163">このサービスは、製品およびバリアントに関連する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-163">This service gets information that is related to products and variants.</span></span> |
| <span data-ttu-id="f5f84-164">PricingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-164">PricingService</span></span>             | <span data-ttu-id="f5f84-165">このサービスは、リアル タイムで品目の価格を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-165">This service gets the price of an item in real time.</span></span> <span data-ttu-id="f5f84-166">基準価格および任意の利用可能な割引に基づいて、価格が調整されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-166">The price is adjusted, based on the base price and any applicable discounts.</span></span> <span data-ttu-id="f5f84-167">各小売業者の割引をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-167">Discounts can be customized for each retailer.</span></span> |
| <span data-ttu-id="f5f84-168">ProductAvailabilityService</span><span class="sxs-lookup"><span data-stu-id="f5f84-168">ProductAvailabilityService</span></span> | <span data-ttu-id="f5f84-169">このサービスは、販売可能な製品の数量を計算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-169">This service calculates the quantities of products that are available to sell.</span></span> |
| <span data-ttu-id="f5f84-170">ReasonCodeService</span><span class="sxs-lookup"><span data-stu-id="f5f84-170">ReasonCodeService</span></span>          | <span data-ttu-id="f5f84-171">このサービスは、POS 操作またはワークフローに対して必要な理由コードを取得し計算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-171">This service calculates and gets the required reason code for POS operations or any workflow.</span></span> |
| <span data-ttu-id="f5f84-172">ReceiptService</span><span class="sxs-lookup"><span data-stu-id="f5f84-172">ReceiptService</span></span>             | <span data-ttu-id="f5f84-173">このサービスは入庫の詳細を取得し、フォーマットします。</span><span class="sxs-lookup"><span data-stu-id="f5f84-173">This service gets and formats the receipt details.</span></span> |
| <span data-ttu-id="f5f84-174">RoundingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-174">RoundingService</span></span>            | <span data-ttu-id="f5f84-175">このサービスは、支払/入金タイプおよび店舗に基づいて、支払/入金金額を丸めます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-175">This service rounds the tender amount, based on the tender type and store.</span></span> |
| <span data-ttu-id="f5f84-176">SalesOrderService</span><span class="sxs-lookup"><span data-stu-id="f5f84-176">SalesOrderService</span></span>          | <span data-ttu-id="f5f84-177">このサービスは、顧客のショッピング カートに基づいて、販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-177">This service creates a sales order, based on a customer shopping cart.</span></span> |
| <span data-ttu-id="f5f84-178">SearchProductsService</span><span class="sxs-lookup"><span data-stu-id="f5f84-178">SearchProductsService</span></span>      | <span data-ttu-id="f5f84-179">このサービスは、入力テキストに基づいて、製品を検索します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-179">This service searches products, based on the input text.</span></span> |
| <span data-ttu-id="f5f84-180">ShippingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-180">ShippingService</span></span>            | <span data-ttu-id="f5f84-181">このサービスは、送料を計算し、現在の注文の出荷オプションを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-181">This service calculates shipping costs and determines shipping options for the current order.</span></span> |
| <span data-ttu-id="f5f84-182">StockCountService</span><span class="sxs-lookup"><span data-stu-id="f5f84-182">StockCountService</span></span>          | <span data-ttu-id="f5f84-183">このサービスは在庫仕訳帳を作成し、コミット、および同期します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-183">This service creates, commits, and synchronizes stock journals.</span></span> |
| <span data-ttu-id="f5f84-184">StoreOperationService</span><span class="sxs-lookup"><span data-stu-id="f5f84-184">StoreOperationService</span></span>      | <span data-ttu-id="f5f84-185">このサービスは、保存と削除、支払/入金申告、および仕訳帳の検索など店舗関連の工程のサービスを管理します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-185">This service maintains store-related operation services, such as Save and Drop, Tender declaration, and Search journal.</span></span> |
| <span data-ttu-id="f5f84-186">TaxService</span><span class="sxs-lookup"><span data-stu-id="f5f84-186">TaxService</span></span>                 | <span data-ttu-id="f5f84-187">このサービスは、現在の注文に対する売上税を計算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-187">This service calculates the sales tax for the current order.</span></span> <span data-ttu-id="f5f84-188">Microsoft Dynamics 365 for Finance and Operations、またはサード パーティの売上税サービスから売上税情報を利用することができます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-188">You can use sales tax information from Microsoft Dynamics 365 for Finance and Operations, or from a third-party sales tax service.</span></span> |
| <span data-ttu-id="f5f84-189">TotalingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-189">TotalingService</span></span>            | <span data-ttu-id="f5f84-190">このサービスは、販売トランザクションおよび販売明細行の合計を計算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-190">This service calculates the totals on the sales transactions and sales lines.</span></span> |

<span data-ttu-id="f5f84-191">拡張シナリオでは、サービス クラス内の要求のいずれかを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-191">For extension scenarios, you can override any of the requests in the service class.</span></span> <span data-ttu-id="f5f84-192">たとえば、顧客の検索フローを変更するには、**CustomerService** サービスから、**CustomersSearchServiceRequest** リクエストを拡張します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-192">For example, to change the customer search flow, extend the **CustomersSearchServiceRequest** request from the **CustomerService** service.</span></span>

> [!NOTE]
> <span data-ttu-id="f5f84-193">サービス クラスをカスタマイズしません。</span><span class="sxs-lookup"><span data-stu-id="f5f84-193">You don't customize the service class.</span></span> <span data-ttu-id="f5f84-194">代わりに、サービス クラス内の要求/応答を拡張します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-194">Instead, you extend the request/response in the service class.</span></span> <span data-ttu-id="f5f84-195">それ自体では、サービス クラスにはロジックがありません。</span><span class="sxs-lookup"><span data-stu-id="f5f84-195">By itself, the service class doesn't have any logic.</span></span> <span data-ttu-id="f5f84-196">正しい要求への呼び出しをルーティングします。</span><span class="sxs-lookup"><span data-stu-id="f5f84-196">It just routes the call to the correct request.</span></span>

## <a name="sample-service-class-implementation"></a><span data-ttu-id="f5f84-197">サービス クラス実装の例</span><span class="sxs-lookup"><span data-stu-id="f5f84-197">Sample service class implementation</span></span>

```C#
public class MyService : IRequestHandler
{
    /// <summary>
    /// Gets the collection of supported request types by this handler.
    /// </summary>

    public IEnumerable<Type> SupportedRequestTypes
    {
        get
        {
            return new[]
            {
                typeof(MyRequest),
                typeof(MyRequest1),
                typeof(MyRequest2),
            };
        }
    }

    /// <summary>
    /// Entry point to my service. Takes a service request and returns the result
    /// of the request execution.
    /// </summary>

    /// <param name="request">The my service request to execute.</param>

    /// <returns>Result of executing request, or null object for void operations.</returns>

    public Response Execute(Request request)
    {
        if (request == null)
        {
            throw new ArgumentNullException("request");
        }
        Type requestType = request.GetType();
        Response response;
        if (requestType == typeof(MyRequest))
        {
            response = MyRequestCustomMethod((MyRequest)request);
        }
        else if (requestType == typeof(MyRequest1))
        {
            response = MyRequest1CustomMethod ((MyRequest1)request);
        }
        else if (requestType == typeof(MyRequest2))
        {
            response = MyRequest2CustomMethod ((MyRequest2)request);
        }
        else
        {
            throw new NotSupportedException(string.Format(CultureInfo.InvariantCulture, "Request '{0}' is not supported.", request.GetType().ToString()));
        }
        return response;
    }
    private static MyResponse MyRequestCustomMethod (MyRequest request)
    {
        return myresponse;
    }
}
```

## <a name="extension-pattern-for-crt"></a><span data-ttu-id="f5f84-198">CRT 拡張パターン</span><span class="sxs-lookup"><span data-stu-id="f5f84-198">Extension pattern for CRT</span></span>

- <span data-ttu-id="f5f84-199">**新しいサービス クラスを作成し、1 つまたは複数の要求 / 応答を実装** – このアプローチを使用して、新しい機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-199">**Create a new service class, and implement one or more requests/responses** – Use this approach to create a new feature.</span></span>
- <span data-ttu-id="f5f84-200">**コア要求/応答のオーバーライド** – このアプローチを使用して、標準ワークフローまたはビジネス ロジックを変更します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-200">**Override the core request/response** – Use this approach to modify the standard workflow or business logic.</span></span>
- <span data-ttu-id="f5f84-201">**応答/要求のプレ トリガーまたはポスト トリガーの追加** – このアプローチを使用して、ビジネス ロジックまたはカスタム フィールドなどを追加します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-201">**Add a pre-trigger or post-trigger for any request/response** – Use this approach to add business logic or add custom fields, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="f5f84-202">データ アクセス要求、ワークフロー要求、またはサービス要求を作成するかどうかは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="f5f84-202">It doesn't matter whether you create a data access request, a workflow request, or a service request.</span></span> <span data-ttu-id="f5f84-203">CRT のすべての内容は、要求または応答です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-203">Everything in CRT is a request/response.</span></span> <span data-ttu-id="f5f84-204">要求/応答に必要なロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-204">You write the logic that is required in the request/response.</span></span> <span data-ttu-id="f5f84-205">要求が論理上の理由から異なるタイプに分類されても、全て同じフレームワーク観点です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-205">Although the requests are classified into different types for logical reasons, everything is the same from the framework perspective.</span></span>

<span data-ttu-id="f5f84-206">次の 3 つのクラスは、すべての要求/応答で実装されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-206">The following three classes will be implemented in all our requests/responses:</span></span>

- <span data-ttu-id="f5f84-207">**クラスのリクエスト** – このクラスは、POS/Retail サーバー/E コマース/CRT ワークフロー クラスの作業の要求を行います。</span><span class="sxs-lookup"><span data-stu-id="f5f84-207">**Request class** – This class is POS/Retail server/E-commerce/CRT workflow class that is the request to do something.</span></span>
- <span data-ttu-id="f5f84-208">**応答クラス** – このクラスは、呼び出し元の要求に基づいて、応答を返します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-208">**Response class** – This class returns the response, based on the request to the caller.</span></span>
- <span data-ttu-id="f5f84-209">**ハンドラー クラス** – このクラスには、要求のコア ロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-209">**Handler class** – This class contains the core logic for the request.</span></span> <span data-ttu-id="f5f84-210">ハンドラー クラスで、他の要求を呼び出して、カスタム ロジックなどを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-210">In the handler class, you can call other requests, do custom logic, and so on.</span></span>

### <a name="request-class"></a><span data-ttu-id="f5f84-211">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="f5f84-211">Request class</span></span>

```C#
public class MyRequest : Request
{
    /// <summary>
    /// Initializes a new instance of the <see cref="MyRequest"/> class.
    /// </summary>

    public MyRequest ()
    {
    }

    // other properties
}
```

### <a name="response-class"></a><span data-ttu-id="f5f84-212">応答クラス</span><span class="sxs-lookup"><span data-stu-id="f5f84-212">Response class</span></span>

```C#
public sealed class MyResponse : Response
{
    /// <summary>
    /// Initializes a new instance of the <see cref=" MyResponse"/> class.
    /// </summary>

    public MyResponse ()
    {
    }
}
```

### <a name="handler-class"></a><span data-ttu-id="f5f84-213">ハンドラー クラス</span><span class="sxs-lookup"><span data-stu-id="f5f84-213">Handler class</span></span>

```C#
public sealed class MyRequestHandler : SingleRequestHandler< MyRequest, MyResponse >
{
    /// <summary>
    /// Saves (updating if it exists and creating a new one if it does not) the shopping cart on the request.
    /// </summary>

    /// <param name="request">The request.</param>

    /// <returns><see cref=" MyResponse "/> object containing the cart with updated item quantities.</returns>

    protected override MyResponse Process(MyRequest request)
    {
        //logic class.
    }
}
```

### <a name="addressservice"></a><span data-ttu-id="f5f84-214">AddressService</span><span class="sxs-lookup"><span data-stu-id="f5f84-214">AddressService</span></span>

<span data-ttu-id="f5f84-215">住所サービスでは、さまざまな拡張シナリオに対する次の要求/応答をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f5f84-215">The Address service supports the following requests/responses for various extension scenarios.</span></span>

| <span data-ttu-id="f5f84-216">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-216">Request</span></span>                            | <span data-ttu-id="f5f84-217">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-217">Purpose</span></span>                                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-218">GetCountryRegionsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-218">GetCountryRegionsServiceRequest</span></span>    | <span data-ttu-id="f5f84-219">この要求は、サポートされている国および地域の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-219">This request gets the list of countries and regions that are supported.</span></span>                         |
| <span data-ttu-id="f5f84-220">GetStateProvincesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-220">GetStateProvincesServiceRequest</span></span>    | <span data-ttu-id="f5f84-221">この要求は、国または地域でサポートされている都道府県の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-221">This request gets the list of states or provinces that are supported for the country or region.</span></span> |
| <span data-ttu-id="f5f84-222">GetCitiesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-222">GetCitiesServiceRequest</span></span>            | <span data-ttu-id="f5f84-223">この要求は、州または地域でサポートされている市町村の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-223">This request gets the list of cities that are supported for the state or region.</span></span>                |
| <span data-ttu-id="f5f84-224">GetDistrictServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-224">GetDistrictServiceRequest</span></span>          | <span data-ttu-id="f5f84-225">この要求は、サポートされている地域の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-225">This request gets the list of districts that are supported.</span></span>                                     |
| <span data-ttu-id="f5f84-226">GetZipCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-226">GetZipCodesServiceRequest</span></span>          | <span data-ttu-id="f5f84-227">この要求は、サポートされている郵便番号の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-227">This request gets the list of ZIP Codes that are supported.</span></span>                                     |
| <span data-ttu-id="f5f84-228">GetFromZipPostalCodeServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-228">GetFromZipPostalCodeServiceRequest</span></span> | <span data-ttu-id="f5f84-229">この要求は、サポートされている郵便番号の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-229">This request gets the list of postal codes supported.</span></span>                                           |
| <span data-ttu-id="f5f84-230">GetAddressFormattingServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-230">GetAddressFormattingServiceRequest</span></span> | <span data-ttu-id="f5f84-231">この要求は、指定した国または地域の住所書式を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-231">This request gets the address format for the specified country or region.</span></span>                       |

### <a name="barcodeservice"></a><span data-ttu-id="f5f84-232">BarcodeService</span><span class="sxs-lookup"><span data-stu-id="f5f84-232">BarcodeService</span></span>

| <span data-ttu-id="f5f84-233">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-233">Request</span></span>                                  | <span data-ttu-id="f5f84-234">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-234">Purpose</span></span>                                                                                          |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-235">ProcessMaskSegmentsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-235">ProcessMaskSegmentsServiceRequest</span></span>        | <span data-ttu-id="f5f84-236">この要求は、バーコード マスクのコンフィギュレーションに基づいて、バーコードを処理します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-236">This request processes the barcode, based on the barcode mask configuration.</span></span>                     |
| <span data-ttu-id="f5f84-237">GetBarcodeTypeServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-237">GetBarcodeTypeServiceRequest</span></span>             | <span data-ttu-id="f5f84-238">この要求は、サポートされているバーコードのタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-238">This request gets the types of barcodes that are supported.</span></span>                                      |
| <span data-ttu-id="f5f84-239">CalculateQuantityFromPriceServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-239">CalculateQuantityFromPriceServiceRequest</span></span> | <span data-ttu-id="f5f84-240">この要求により、価格と数量はスキャンまたは入力されたバーコードに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-240">This request calculates the price and quantity, based on the barcode that is scanned or entered.</span></span> |

### <a name="cartservice"></a><span data-ttu-id="f5f84-241">CartService</span><span class="sxs-lookup"><span data-stu-id="f5f84-241">CartService</span></span>

| <span data-ttu-id="f5f84-242">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-242">Request</span></span>                                                     | <span data-ttu-id="f5f84-243">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-243">Purpose</span></span>                                                                                                    |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-244">GetSalesTransactionsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-244">GetSalesTransactionsServiceRequest</span></span>                          | <span data-ttu-id="f5f84-245">この要求は、小売用バックオフィスから販売トランザクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-245">This request gets the sales transaction from Retail headquarters.</span></span>                                          |
| <span data-ttu-id="f5f84-246">GetCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-246">GetCartServiceRequest</span></span>                                       | <span data-ttu-id="f5f84-247">この要求は、カート ID を使用して、販売トランザクション テーブルからカートを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-247">This request gets the cart from the sales transaction table by using the cart ID.</span></span>                          |
| <span data-ttu-id="f5f84-248">CalculateSalesTransactionServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-248">CalculateSalesTransactionServiceRequest</span></span>                     | <span data-ttu-id="f5f84-249">この要求により、指定した計算モードに基づいて、各種販売トランザクションの合計が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-249">This request calculates the various sales transaction totals, based on the specified calculation mode.</span></span>     |
| <span data-ttu-id="f5f84-250">CalculateEstimatedShippingAuthorizationAmountServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-250">CalculateEstimatedShippingAuthorizationAmountServiceRequest</span></span> | <span data-ttu-id="f5f84-251">この要求により、トランザクションでの見積配送承認金額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-251">This request calculates the estimated shipping authorization amount on the transaction.</span></span>                    |
| <span data-ttu-id="f5f84-252">ConvertSalesTransactionToCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-252">ConvertSalesTransactionToCartServiceRequest</span></span>                 | <span data-ttu-id="f5f84-253">この要求により、渡されるトランザクション ID に基づいて、販売トランザクションがカート トランザクションに変換されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-253">This request converts the sales transaction to a cart transaction, based on transaction ID that is passed.</span></span> |

### <a name="couponservice"></a><span data-ttu-id="f5f84-254">CouponService</span><span class="sxs-lookup"><span data-stu-id="f5f84-254">CouponService</span></span>

| <span data-ttu-id="f5f84-255">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-255">Request</span></span>                               | <span data-ttu-id="f5f84-256">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-256">Purpose</span></span>                                                                                                              |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-257">UpdateCouponCodesOnCartServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-257">UpdateCouponCodesOnCartServiceRequest</span></span> | <span data-ttu-id="f5f84-258">この要求は、カートで使用されているクーポンに基づいて、小売用バックオフィス内のクーポン コードの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-258">This request updates the coupon codes status in Retail headquarters, based on the coupons that are used in the cart.</span></span> |
| <span data-ttu-id="f5f84-259">ValidateCouponCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-259">ValidateCouponCodesServiceRequest</span></span>     | <span data-ttu-id="f5f84-260">この要求は、トランザクションに入力されたクーポン コードを検証します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-260">This request validates the coupon code that is entered in the transactions.</span></span>                                          |
| <span data-ttu-id="f5f84-261">UpdateCouponUsageServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-261">UpdateCouponUsageServiceRequest</span></span>       | <span data-ttu-id="f5f84-262">この要求は、トランザクションのクーポンの使用状況を更新します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-262">This request updates coupon usage for the transaction.</span></span>                                                               |

### <a name="customerservice"></a><span data-ttu-id="f5f84-263">CustomerService</span><span class="sxs-lookup"><span data-stu-id="f5f84-263">CustomerService</span></span>

| <span data-ttu-id="f5f84-264">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-264">Request</span></span>                                      | <span data-ttu-id="f5f84-265">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-265">Purpose</span></span>                                                                  |
|----------------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-266">SaveCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-266">SaveCustomerServiceRequest</span></span>                   | <span data-ttu-id="f5f84-267">この要求は、POS から顧客を保存する場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-267">This request is called when you save a customer from the POS.</span></span>            |
| <span data-ttu-id="f5f84-268">GetCustomersServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-268">GetCustomersServiceRequest</span></span>                   | <span data-ttu-id="f5f84-269">この要求は、選択した顧客の詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-269">This request gets the selected customer details.</span></span>                         |
| <span data-ttu-id="f5f84-270">CustomersSearchServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-270">CustomersSearchServiceRequest</span></span>                | <span data-ttu-id="f5f84-271">この要求は、POS から顧客の検索を行う場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-271">This request is run when you search for a customer from the POS.</span></span>         |
| <span data-ttu-id="f5f84-272">GetCustomerGroupsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-272">GetCustomerGroupsServiceRequest</span></span>              | <span data-ttu-id="f5f84-273">この要求は、顧客グループの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-273">This request gets the customer group details.</span></span>                            |
| <span data-ttu-id="f5f84-274">InitiateLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-274">InitiateLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="f5f84-275">この要求は、下位互換性のための内部要求です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-275">This request is an internal request for backward compatibility.</span></span>          |
| <span data-ttu-id="f5f84-276">FinalizeLinkToExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-276">FinalizeLinkToExistingCustomerServiceRequest</span></span> | <span data-ttu-id="f5f84-277">この要求は、下位互換性のための内部要求です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-277">This request is an internal request for backward compatibility.</span></span>          |
| <span data-ttu-id="f5f84-278">UnlinkFromExistingCustomerServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-278">UnlinkFromExistingCustomerServiceRequest</span></span>     | <span data-ttu-id="f5f84-279">この要求は、下位互換性のための内部要求です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-279">This request is an internal request for backward compatibility.</span></span>          |
| <span data-ttu-id="f5f84-280">GetCustomerBalanceServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-280">GetCustomerBalanceServiceRequest</span></span>             | <span data-ttu-id="f5f84-281">この要求は、顧客の勘定の残高を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-281">This request gets the balance of the customer's account.</span></span>                 |
| <span data-ttu-id="f5f84-282">GetOrderHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-282">GetOrderHistoryServiceRequest</span></span>                | <span data-ttu-id="f5f84-283">この要求は、顧客の注文履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-283">This request gets the customer's order history.</span></span>                          |
| <span data-ttu-id="f5f84-284">GetPurchaseHistoryServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-284">GetPurchaseHistoryServiceRequest</span></span>             | <span data-ttu-id="f5f84-285">この要求は、顧客の最近の購入履歴を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-285">This request gets the history of the customer's recent purchases.</span></span>        |
| <span data-ttu-id="f5f84-286">CustomerSearchByFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-286">CustomerSearchByFieldsServiceRequest</span></span>         | <span data-ttu-id="f5f84-287">この要求は、名前、電話番号などのフィールドを使用して顧客を検索するときに実行されます (ヒント検索)。</span><span class="sxs-lookup"><span data-stu-id="f5f84-287">This request is run when you search customer by using fields such as name, phone number etc. (hint search).</span></span> |
| <span data-ttu-id="f5f84-288">GetCustomerSearchFieldsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-288">GetCustomerSearchFieldsServiceRequest</span></span>        | <span data-ttu-id="f5f84-289">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-289">This request gets the list of customer search fields (hint fields).</span></span>      |

### <a name="pricingservice"></a><span data-ttu-id="f5f84-290">PricingService</span><span class="sxs-lookup"><span data-stu-id="f5f84-290">PricingService</span></span>

| <span data-ttu-id="f5f84-291">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-291">Request</span></span>                                   | <span data-ttu-id="f5f84-292">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-292">Purpose</span></span>                                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-293">CalculatePricesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-293">CalculatePricesServiceRequest</span></span>             | <span data-ttu-id="f5f84-294">この要求により、カートと検索画面に追加される各品目の価格が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-294">This request calculates the price for each item that is added to the cart and on the search screen.</span></span>                   |
| <span data-ttu-id="f5f84-295">CalculateDiscountsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-295">CalculateDiscountsServiceRequest</span></span>          | <span data-ttu-id="f5f84-296">この要求により、カートに追加する各品目の割引が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-296">This request calculates the discount for each item that is added to the cart.</span></span>                                         |
| <span data-ttu-id="f5f84-297">GetIndependentPriceDiscountServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-297">GetIndependentPriceDiscountServiceRequest</span></span> | <span data-ttu-id="f5f84-298">この要求により、価格チェック画面の各品目とその他の非トランザクション関連のフローの価格が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-298">This request calculates the price for each item on the price check screen and in other non-transaction-related flows.</span></span> |
| <span data-ttu-id="f5f84-299">ValidateDiscountsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-299">ValidateDiscountsServiceRequest</span></span>           | <span data-ttu-id="f5f84-300">この要求は従業員に基づいて、入力された割引を検証します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-300">This request validates the discount that is entered, based on the employee.</span></span>                                           |
| <span data-ttu-id="f5f84-301">GetAllPeriodicDiscountsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-301">GetAllPeriodicDiscountsServiceRequest</span></span>     | <span data-ttu-id="f5f84-302">この要求は、コンフィギュレーションされたすべての期間割引を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-302">This request gets all the periodic discounts that are configured.</span></span>                                                     |
| <span data-ttu-id="f5f84-303">GetDiscountCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-303">GetDiscountCodesServiceRequest</span></span>            | <span data-ttu-id="f5f84-304">この要求は、コンフィギュレーションされたすべての割引コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-304">This request gets all the discount codes that are configured.</span></span>                                                         |

### <a name="productservice"></a><span data-ttu-id="f5f84-305">ProductService</span><span class="sxs-lookup"><span data-stu-id="f5f84-305">ProductService</span></span>

| <span data-ttu-id="f5f84-306">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-306">Request</span></span>                     | <span data-ttu-id="f5f84-307">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-307">Purpose</span></span>                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-308">ProductSearchServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-308">ProductSearchServiceRequest</span></span> | <span data-ttu-id="f5f84-309">この要求は、POS からの検索テキストに基づいて、製品リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-309">This request gets the product list, based on the search text from the POS.</span></span> <span data-ttu-id="f5f84-310">(これは以前の要求です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-310">(This is an old request.</span></span> <span data-ttu-id="f5f84-311">カスタマイズでは、新しい **SearchProductsServiceRequest** 要求を代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-311">For customization, use the new **SearchProductsServiceRequest** request instead.)</span></span> |
| <span data-ttu-id="f5f84-312">GetProductServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-312">GetProductServiceRequest</span></span>    | <span data-ttu-id="f5f84-313">この要求は、製品 ID に基づいて製品を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-313">This request gets the product, based on the product ID.</span></span>                                                                                                                               |
| <span data-ttu-id="f5f84-314">GetProductRefinersRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-314">GetProductRefinersRequest</span></span>   | <span data-ttu-id="f5f84-315">この要求は、製品のリファイナーの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-315">This request retrieves the product refiner values.</span></span>                                                                                                                                    |

### <a name="productsservice"></a><span data-ttu-id="f5f84-316">ProductsService</span><span class="sxs-lookup"><span data-stu-id="f5f84-316">ProductsService</span></span>

| <span data-ttu-id="f5f84-317">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-317">Request</span></span>                          | <span data-ttu-id="f5f84-318">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-318">Purpose</span></span>                                                                      |
|----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-319">GetProductsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-319">GetProductsServiceRequest</span></span>        | <span data-ttu-id="f5f84-320">この要求は用意されている製品の ID に基づいて、製品を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-320">This request gets the products, based on the products IDs that are provided.</span></span> |
| <span data-ttu-id="f5f84-321">GetVariantProductsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-321">GetVariantProductsServiceRequest</span></span> | <span data-ttu-id="f5f84-322">この要求は、マスター タイプ製品の特定のバリエーションを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-322">This request gets specific variations of master type products.</span></span>               |

### <a name="reasoncodeservice"></a><span data-ttu-id="f5f84-323">ReasonCodeService</span><span class="sxs-lookup"><span data-stu-id="f5f84-323">ReasonCodeService</span></span>

| <span data-ttu-id="f5f84-324">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-324">Request</span></span>                                                             | <span data-ttu-id="f5f84-325">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-325">Purpose</span></span>                                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-326">GetReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-326">GetReasonCodesServiceRequest</span></span>                                        | <span data-ttu-id="f5f84-327">この要求は、ワークフローまたは POS 操作に対して必要な理由コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-327">This request gets the required reason code for the workflow or POS operation.</span></span>                               |
| <span data-ttu-id="f5f84-328">CalculateRequiredReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-328">CalculateRequiredReasonCodesServiceRequest</span></span>                          | <span data-ttu-id="f5f84-329">この要求により、ワークフローまたは POS 操作に対して必要な理由コードが計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-329">This request calculates the required reason code for the workflow or POS operation.</span></span>                         |
| <span data-ttu-id="f5f84-330">CalculateCartRequiredReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-330">CalculateCartRequiredReasonCodesServiceRequest</span></span>                      | <span data-ttu-id="f5f84-331">この要求により、カート ワークフローに必要な理由コードが計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-331">This request calculates the required reason code for the cart workflow.</span></span>                                     |
| <span data-ttu-id="f5f84-332">CalculateDropAndDeclareTransactionRequiredReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-332">CalculateDropAndDeclareTransactionRequiredReasonCodesServiceRequest</span></span> | <span data-ttu-id="f5f84-333">この要求により、ドロップおよび支払/入金申告トランザクションに必要な理由コードが計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-333">This request calculates the required reason code for the drop and tender declaration transaction.</span></span>           |
| <span data-ttu-id="f5f84-334">CalculateNonSalesTransactionRequiredReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-334">CalculateNonSalesTransactionRequiredReasonCodesServiceRequest</span></span>       | <span data-ttu-id="f5f84-335">この要求により、支払/入金申告などの販売以外のトランザクションに必要な理由コードが計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-335">This request calculates the required reason code for the non-sales transaction, such as tender declaration.</span></span> |
| <span data-ttu-id="f5f84-336">GetReturnOrderReasonCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-336">GetReturnOrderReasonCodesServiceRequest</span></span>                             | <span data-ttu-id="f5f84-337">この要求は、返品トランザクションに対して必要な理由コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-337">This request gets the required reason code for the return transaction.</span></span>                                      |
| <span data-ttu-id="f5f84-338">ValidateReasonCodeLineForUpdateServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-338">ValidateReasonCodeLineForUpdateServiceRequest</span></span>                       | <span data-ttu-id="f5f84-339">この要求は、カート要求の保存中に追加された理由コード行を検証します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-339">This request validates the reason code lines that are added during the save cart request.</span></span>                   |

### <a name="receiptservice"></a><span data-ttu-id="f5f84-340">ReceiptService</span><span class="sxs-lookup"><span data-stu-id="f5f84-340">ReceiptService</span></span>

| <span data-ttu-id="f5f84-341">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-341">Request</span></span>                               | <span data-ttu-id="f5f84-342">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-342">Purpose</span></span>                                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-343">GetReceiptServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-343">GetReceiptServiceRequest</span></span>              | <span data-ttu-id="f5f84-344">この要求はレシート タイプに基づいて、レシート タイプを取得しレシート データを生成します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-344">This request gets the receipt type and generates the receipt data, based on the receipt type.</span></span>     |
| <span data-ttu-id="f5f84-345">GetCustomReceiptFieldServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-345">GetCustomReceiptFieldServiceRequest</span></span>   | <span data-ttu-id="f5f84-346">この要求を上書きし、受領書に追加されるカスタムフィールドのカスタム ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-346">Override this request, and add custom logic for your custom fields that are added in the receipt.</span></span> |
| <span data-ttu-id="f5f84-347">GetEmailReceiptServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-347">GetEmailReceiptServiceRequest</span></span>         | <span data-ttu-id="f5f84-348">この要求は、印刷と電子メールのシナリオで使用される書式設定された領収書を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-348">This request gets the formatted receipts that will be used for print and email scenarios.</span></span>         |
| <span data-ttu-id="f5f84-349">PopulateTaxSummaryIndiaServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-349">PopulateTaxSummaryIndiaServiceRequest</span></span> | <span data-ttu-id="f5f84-350">この要求は、インドのトランザクションの税集計を設定します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-350">This request populates the tax summary for India transaction.</span></span>                                     |

### <a name="searchproductsservice"></a><span data-ttu-id="f5f84-351">SearchProductsService</span><span class="sxs-lookup"><span data-stu-id="f5f84-351">SearchProductsService</span></span>

| <span data-ttu-id="f5f84-352">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-352">Request</span></span>                      | <span data-ttu-id="f5f84-353">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-353">Purpose</span></span>                                                         |
|------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f5f84-354">SearchProductsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-354">SearchProductsServiceRequest</span></span> | <span data-ttu-id="f5f84-355">この要求は、POS から製品の検索を行う場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-355">This request is run when you search for a product from the POS.</span></span> |

### <a name="taxservice"></a><span data-ttu-id="f5f84-356">TaxService</span><span class="sxs-lookup"><span data-stu-id="f5f84-356">TaxService</span></span>

| <span data-ttu-id="f5f84-357">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-357">Request</span></span>                      | <span data-ttu-id="f5f84-358">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-358">Purpose</span></span>                                                                                                                                                                                            |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-359">CalculateTaxServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-359">CalculateTaxServiceRequest</span></span>   | <span data-ttu-id="f5f84-360">この要求により、トランザクションの税額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-360">This request calculates taxes on the transaction.</span></span>                                                                                                                                                  |
| <span data-ttu-id="f5f84-361">AssignTaxCodesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-361">AssignTaxCodesServiceRequest</span></span> | <span data-ttu-id="f5f84-362">この要求により、税計算前にトランザクションの課税対象の品目に対して税コードが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-362">This request assigns tax codes on the transaction's taxable items before the tax calculation.</span></span> <span data-ttu-id="f5f84-363">**CalculateTaxServiceRequest** 要求の既定の税計算ハンドラーはこのメッセージを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-363">The default tax calculation handler of the **CalculateTaxServiceRequest** request uses this message.</span></span> |
| <span data-ttu-id="f5f84-364">PopulateTaxRatesRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-364">PopulateTaxRatesRequest</span></span>      | <span data-ttu-id="f5f84-365">この要求は、取り消されたトランザクションの税率を設定します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-365">This request populates tax rates for the recalled transaction.</span></span> <span data-ttu-id="f5f84-366">税明細行に対する税率情報は永続化されません。</span><span class="sxs-lookup"><span data-stu-id="f5f84-366">No tax percentage information is persisted for tax lines.</span></span> <span data-ttu-id="f5f84-367">このメッセージ ハンドラーは、情報を復元します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-367">This message handler restores the information.</span></span>                            |

## <a name="workflow-layer"></a><span data-ttu-id="f5f84-368">ワークフロー レイヤー</span><span class="sxs-lookup"><span data-stu-id="f5f84-368">Workflow layer</span></span>

<span data-ttu-id="f5f84-369">サービス レイヤーの上は、ワークフロー レイヤーです。</span><span class="sxs-lookup"><span data-stu-id="f5f84-369">On top of the Services layer is the Workflow layer.</span></span> <span data-ttu-id="f5f84-370">ワークフローは、サービスとビジネス ロジックを共に業務プロセスを定義するコレクションです。</span><span class="sxs-lookup"><span data-stu-id="f5f84-370">A workflow is a collection of services and business logic that together define business processes.</span></span> <span data-ttu-id="f5f84-371">たとえば、顧客がカートに品目を追加すると、価格の取得、検証の実行、在庫数量の確認、出荷費用の計算、税計算、および割引計算をするためワークフローを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-371">For example, when a customer adds an item to the cart, you can use a workflow to get the price, do validation, check the inventory quantity, calculate shipping, calculate tax, and calculate discounts.</span></span> <span data-ttu-id="f5f84-372">既存のワークフローをカスタマイズすることも、新しいワークフローを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-372">You can customize the existing workflows, or you can create new workflows.</span></span> <span data-ttu-id="f5f84-373">ワークフローを使用して、業務プロセスの一部としてサードパーティ製システムに接続することもできます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-373">You can even use a workflow to connect to a third-party system as part of your business processes.</span></span>

<span data-ttu-id="f5f84-374">サービスと同じように、ワークフローは要求/応答パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-374">Just like services, workflows use the request/response pattern.</span></span> <span data-ttu-id="f5f84-375">基本 CRT [要求](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.request.aspx) クラスから継承された要求オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f5f84-375">The request object inherited from the base CRT [Request](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.request.aspx) class.</span></span> <span data-ttu-id="f5f84-376">基本 CRT [応答](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.response.aspx) クラスから継承された応答オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f5f84-376">The response object inherited from the base CRT [Response](https://technet.microsoft.com/en-us/library/microsoft.dynamics.commerce.runtime.messages.response.aspx) class.</span></span> <span data-ttu-id="f5f84-377">ワークフローには、[WorkflowRequestHandler<TRequest, TResponse>](https://technet.microsoft.com/en-us/library/jj764791.aspx) クラスを拡張する要求ハンドラー クラスもあります。</span><span class="sxs-lookup"><span data-stu-id="f5f84-377">A workflow also has a request handler class that extends the [WorkflowRequestHandler<TRequest, TResponse>](https://technet.microsoft.com/en-us/library/jj764791.aspx) class.</span></span> <span data-ttu-id="f5f84-378">ワークフローを作成するには、要求クラスおよび応答クラスを作成し、ワークフローのビジネス ロジックが含まれる要求ハンドラー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-378">To create a workflow, you create a request class and a response class, and you then create a request handler class that contains the business logic for the workflow.</span></span>

<span data-ttu-id="f5f84-379">たとえば、現金払いトランザクションまたは顧客からの注文を作成する場合、注文が作成される前に、多くの異なるステップやワークフローが完了します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-379">For example, when you create a cash-and-carry transaction or a customer order, many different steps or workflows are completed before the order is created.</span></span> <span data-ttu-id="f5f84-380">注文プロセスでのワークフロー ステップの 1 つは、カート要求の保存です。</span><span class="sxs-lookup"><span data-stu-id="f5f84-380">One of the workflow steps in the order process is the Save cart request.</span></span> <span data-ttu-id="f5f84-381">カート要求ワークフローの保存は、POS からカートに加えられる変更の保存を担当します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-381">The Save cart request workflow is responsible for saving any changes that are made to the cart from the POS.</span></span> <span data-ttu-id="f5f84-382">たとえば、買い物カゴに品目を追加したり、数量を変更するなど POS で行う行為は、SaveCart を呼び出して POS とデータベースに変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-382">For example, when you add an item to the cart, change the quantity, and so on, anything that you do in the POS will cause a call to the SaveCart to save the changes to the POS and database.</span></span>

<span data-ttu-id="f5f84-383">次の 3 つのクラスは、カート要求ワークフローの保存で実装されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-383">The following three classes will be implemented in the Save cart request workflow.</span></span>

### <a name="request-class"></a><span data-ttu-id="f5f84-384">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="f5f84-384">Request class</span></span>

```C#
public class SaveCartRequest : Request
{
    /// <summary>
    /// Initializes a new instance of the <see cref="SaveCartRequest"/> class.
    /// </summary>

    public SaveCartRequest()
    {
    }

    // other properties
}
```

### <a name="response-class"></a><span data-ttu-id="f5f84-385">応答クラス</span><span class="sxs-lookup"><span data-stu-id="f5f84-385">Response class</span></span>

```C#
public sealed class SaveCartResponse : Response
{
    /// <summary>
    /// Initializes a new instance of the <see cref="SaveCartResponse"/> class.
    /// </summary>

    public SaveCartResponse()
    {
    }
}
```

### <a name="handler-class"></a><span data-ttu-id="f5f84-386">ハンドラー クラス</span><span class="sxs-lookup"><span data-stu-id="f5f84-386">Handler class</span></span>

```C#
public sealed class SaveCartRequestHandler : SingleRequestHandler<SaveCartRequest, SaveCartResponse>
{
    /// <summary>
    /// Saves (updating if it exists and creating a new one if it does not) the shopping cart on the request.
    /// </summary>

    /// <param name="request">The request.</param>

    /// <returns><see cref="SaveCartResponse"/> object containing the cart with updated item quantities.</returns>

    protected override SaveCartResponse Process(SaveCartRequest request)
    {
        //logic class.
    }
}
```

<span data-ttu-id="f5f84-387">すべてのワークフロー クラスは、同じパターンに従います。</span><span class="sxs-lookup"><span data-stu-id="f5f84-387">All your workflow classes will follow the same pattern.</span></span>

### <a name="default-workflows-and-handlers"></a><span data-ttu-id="f5f84-388">既定のワークフローとハンドラー</span><span class="sxs-lookup"><span data-stu-id="f5f84-388">Default workflows and handlers</span></span>

<span data-ttu-id="f5f84-389">次の表では、既定のワークフローの要求と応答の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-389">The following table lists the default workflow requests and response.</span></span> <span data-ttu-id="f5f84-390">CRT サービスは、ワークフロー要求を呼び出し、小売販売時点管理で実行する操作に基づいて応答します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-390">CRT services call the workflows request and response based on the operation you perform in retail point of sale.</span></span> <span data-ttu-id="f5f84-391">ビジネス シナリオに従って、これらのワークフローの要求と応答のいずれかをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-391">You can customize any of these workflows request and response according to your business scenario.</span></span> 

| <span data-ttu-id="f5f84-392">要求</span><span class="sxs-lookup"><span data-stu-id="f5f84-392">Request</span></span>                           | <span data-ttu-id="f5f84-393">ハンドラー</span><span class="sxs-lookup"><span data-stu-id="f5f84-393">Handler</span></span>                                 | <span data-ttu-id="f5f84-394">目的</span><span class="sxs-lookup"><span data-stu-id="f5f84-394">Purpose</span></span>                                                                                                                    |
|-----------------------------------|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f84-395">AddOrderInvoiceToCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-395">AddOrderInvoiceToCartRequest</span></span>      | <span data-ttu-id="f5f84-396">AddOrderInvoiceToCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-396">AddOrderInvoiceToCartRequestHandler</span></span>     | <span data-ttu-id="f5f84-397">この要求により、請求書はカート行としてのカートに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-397">This request adds the invoice to the cart as a cart line.</span></span>                                                                  |
| <span data-ttu-id="f5f84-398">AddOrRemoveDiscountCodesRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-398">AddOrRemoveDiscountCodesRequest</span></span>   | <span data-ttu-id="f5f84-399">AddOrRemoveDiscountCodesRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-399">AddOrRemoveDiscountCodesRequestHandler</span></span>  | <span data-ttu-id="f5f84-400">この要求により、割引コードはカートに追加またはカートから削除されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-400">This request adds discount codes to the cart or removes them from the cart.</span></span>                                                |
| <span data-ttu-id="f5f84-401">CancelOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-401">CancelOrderRequest</span></span>                | <span data-ttu-id="f5f84-402">CancelOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-402">CancelOrderRequestHandler</span></span>               | <span data-ttu-id="f5f84-403">POS から注文をキャンセルすると、この要求が発生します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-403">This request is triggered when you cancel an order from the POS.</span></span>                                                           |
| <span data-ttu-id="f5f84-404">CopyCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-404">CopyCartRequest</span></span>                   | <span data-ttu-id="f5f84-405">CopyCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-405">CopyCartRequestHandler</span></span>                  | <span data-ttu-id="f5f84-406">この要求は、指定されたカート タイプを含む同一のショッピング カートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-406">This request creates an identical shopping cart that has the specified cart type.</span></span>                                          |
| <span data-ttu-id="f5f84-407">GetAddressRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-407">GetAddressRequest</span></span>                 | <span data-ttu-id="f5f84-408">GetAddressRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-408">GetAddressRequestHandler</span></span>                | <span data-ttu-id="f5f84-409">この要求は、リストから住所を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-409">This request gets the address from the list.</span></span>                                                                               |
| <span data-ttu-id="f5f84-410">GetCardPaymentAcceptPointRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-410">GetCardPaymentAcceptPointRequest</span></span>  | <span data-ttu-id="f5f84-411">GetCardPaymentAcceptPointRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-411">GetCardPaymentAcceptPointRequestHandler</span></span> | <span data-ttu-id="f5f84-412">この要求は、カード支払の受諾ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-412">This request shows the accepting page for card payment.</span></span>                                                                     |
| <span data-ttu-id="f5f84-413">GetCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-413">GetCartRequest</span></span>                    | <span data-ttu-id="f5f84-414">GetCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-414">GetCartRequestHandler</span></span>                   | <span data-ttu-id="f5f84-415">この要求はカート検索基準に基づいて、ショッピング カートを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-415">This request gets the shopping cart, based on the cart search criteria.</span></span>                                                    |
| <span data-ttu-id="f5f84-416">GetDiscountCodesRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-416">GetDiscountCodesRequest</span></span>           | <span data-ttu-id="f5f84-417">GetDiscountCodesRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-417">GetDiscountCodesRequestHandler</span></span>          | <span data-ttu-id="f5f84-418">この要求は、割引コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-418">This request gets the discount codes.</span></span>                                                                                      |
| <span data-ttu-id="f5f84-419">GetOrdersRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-419">GetOrdersRequest</span></span>                  | <span data-ttu-id="f5f84-420">GetOrdersRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-420">GetOrdersRequestHandler</span></span>                 | <span data-ttu-id="f5f84-421">この要求は、販売注文を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-421">This request gets sales orders.</span></span>                                                                                            |
| <span data-ttu-id="f5f84-422">GetPromotionsRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-422">GetPromotionsRequest</span></span>              | <span data-ttu-id="f5f84-423">GetPromotionsRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-423">GetPromotionsRequestHandler</span></span>             | <span data-ttu-id="f5f84-424">この要求は、カートおよびカートの品目のプロモーション ラインと共にショッピング カートを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-424">This request gets the shopping cart together with promotion lines for the cart and the cart items.</span></span>                         |
| <span data-ttu-id="f5f84-425">GetScanResultRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-425">GetScanResultRequest</span></span>              | <span data-ttu-id="f5f84-426">GetScanResultRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-426">GetScanResultRequestHandler</span></span>             | <span data-ttu-id="f5f84-427">この要求は、スキャンまたは入力した情報に基づいて、エンティティの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-427">This request gets the entity details, based on the details that are scanned or typed.</span></span>                                      |
| <span data-ttu-id="f5f84-428">GetSupportedCardTypesRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-428">GetSupportedCardTypesRequest</span></span>      | <span data-ttu-id="f5f84-429">GetSupportedCardTypesRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-429">GetSupportedCardTypesRequestHandler</span></span>     | <span data-ttu-id="f5f84-430">この要求は、指定された通貨に対してサポートされているカートのタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-430">This request retrieves the cart types that are supported for the specified currency.</span></span>                                       |
| <span data-ttu-id="f5f84-431">IssueOrAddToGiftCardRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-431">IssueOrAddToGiftCardRequest</span></span>       | <span data-ttu-id="f5f84-432">IssueOrAddToGiftCardRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-432">IssueOrAddToGiftCardRequestHandler</span></span>      | <span data-ttu-id="f5f84-433">この要求は、ギフト カードを発行またはギフト カードの残高に加算します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-433">This request issues a gift card or adds to a gift card's balance.</span></span>                                                          |
| <span data-ttu-id="f5f84-434">PickAndPackOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-434">PickAndPackOrderRequest</span></span>           | <span data-ttu-id="f5f84-435">PickAndPackOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-435">PickAndPackOrderRequestHandler</span></span>          | <span data-ttu-id="f5f84-436">この要求は、顧客注文に対するピッキング リストの作成および梱包明細の作成の要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-436">This request represents a request for picking list creation and packing slip creation for a customer order.</span></span>                |
| <span data-ttu-id="f5f84-437">PickupAtStoreRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-437">PickupAtStoreRequest</span></span>              | <span data-ttu-id="f5f84-438">PickupAtStoreRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-438">PickupAtStoreRequestHandler</span></span>             | <span data-ttu-id="f5f84-439">この要求は、店舗での集荷の要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-439">This request represents a request for pick-up at the store.</span></span>                                                                |
| <span data-ttu-id="f5f84-440">RecalculateOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-440">RecalculateOrderRequest</span></span>           | <span data-ttu-id="f5f84-441">RecalculateOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-441">RecalculateOrderRequestHandler</span></span>          | <span data-ttu-id="f5f84-442">この要求は、注文ワークフローを再計算するための要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-442">This request represents a request for the recalculate order workflow.</span></span>                                                      |
| <span data-ttu-id="f5f84-443">RecallCustomerOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-443">RecallCustomerOrderRequest</span></span>        | <span data-ttu-id="f5f84-444">RecallCustomerOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-444">RecallCustomerOrderRequestHandler</span></span>       | <span data-ttu-id="f5f84-445">この要求は、販売注文を取得し、カートに変換します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-445">This request gets sales orders and converts them into a cart.</span></span>                                                              |
| <span data-ttu-id="f5f84-446">RecallSalesInvoiceRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-446">RecallSalesInvoiceRequest</span></span>         | <span data-ttu-id="f5f84-447">RecallSalesInvoiceRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-447">RecallSalesInvoiceRequestHandler</span></span>        | <span data-ttu-id="f5f84-448">この要求は、請求書を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-448">This request gets invoices.</span></span>                                                                                                |
| <span data-ttu-id="f5f84-449">ResumeCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-449">ResumeCartRequest</span></span>                 | <span data-ttu-id="f5f84-450">ResumeCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-450">ResumeCartRequestHandler</span></span>                | <span data-ttu-id="f5f84-451">この要求は、中断されたカートを再開するための要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-451">This request represents a request to resume a cart that was suspended.</span></span>                                                     |
| <span data-ttu-id="f5f84-452">SaveCartLinesRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-452">SaveCartLinesRequest</span></span>              | <span data-ttu-id="f5f84-453">SaveCartLinesRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-453">SaveCartLinesRequestHandler</span></span>             | <span data-ttu-id="f5f84-454">この要求は、カート行での作成、更新、削除、または無効操作の要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-454">This request represents a request for create, update, delete, or void operations on the cart line.</span></span>                         |
| <span data-ttu-id="f5f84-455">SaveCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-455">SaveCartRequest</span></span>                   | <span data-ttu-id="f5f84-456">SaveCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-456">SaveCartRequestHandler</span></span>                  | <span data-ttu-id="f5f84-457">この要求は、カートに影響を与える変更を POS で行うときに発生します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-457">This request is triggered when you make any changes in that POS that affect the cart.</span></span>                                      |
| <span data-ttu-id="f5f84-458">SaveCustomerOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-458">SaveCustomerOrderRequest</span></span>          | <span data-ttu-id="f5f84-459">SaveCustomerOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-459">SaveCustomerOrderRequestHandler</span></span>         | <span data-ttu-id="f5f84-460">この要求では、指定されたカート ID と支払カードの情報に基づいて、顧客注文を保存するための要求が開始されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-460">This request initiates a request to save the customer order, based on the specified cart identifier and payment card information.</span></span> |
| <span data-ttu-id="f5f84-461">SaveReasonCodeLineRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-461">SaveReasonCodeLineRequest</span></span>         | <span data-ttu-id="f5f84-462">SaveReasonCodeLineRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-462">SaveReasonCodeLineRequestHandler</span></span>        | <span data-ttu-id="f5f84-463">この要求により、理由コードはカート行で追加または更新されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-463">This request adds or updates a reason code on the cart line.</span></span>                                                                           |
| <span data-ttu-id="f5f84-464">SaveTenderLineRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-464">SaveTenderLineRequest</span></span>             | <span data-ttu-id="f5f84-465">SaveTenderLineRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-465">SaveTenderLineRequestHandler</span></span>            | <span data-ttu-id="f5f84-466">この要求により、指定されたショッピング カートに対して支払/入金の明細行が追加、削除、または更新されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-466">This request adds, removes, or updates a tender line for the given shopping cart.</span></span>                                          |
| <span data-ttu-id="f5f84-467">SaveVoidTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-467">SaveVoidTransactionRequest</span></span>        | <span data-ttu-id="f5f84-468">SaveVoidTransactionRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-468">SaveVoidTransactionRequestHandler</span></span>       | <span data-ttu-id="f5f84-469">この要求は、トランザクションを無効にします。</span><span class="sxs-lookup"><span data-stu-id="f5f84-469">This request voids a transaction.</span></span>                                                                                          |
| <span data-ttu-id="f5f84-470">SubmitSalesTransactionRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-470">SubmitSalesTransactionRequest</span></span>     | <span data-ttu-id="f5f84-471">SubmitOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-471">SubmitOrderRequestHandler</span></span>               | <span data-ttu-id="f5f84-472">この要求では、指定されたカート ID に基づいて、販売トランザクションを送信するための要求が開始されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-472">This request initiates a request to submit the sales transaction, based on the specified cart identifier.</span></span>                         |
| <span data-ttu-id="f5f84-473">SuspendCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-473">SuspendCartRequest</span></span>                | <span data-ttu-id="f5f84-474">SuspendCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-474">SuspendCartRequestHandler</span></span>               | <span data-ttu-id="f5f84-475">この要求は、カートを中断するための要求を表します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-475">This request represents a request to suspend the cart.</span></span>                                                                     |
| <span data-ttu-id="f5f84-476">TransferCartRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-476">TransferCartRequest</span></span>               | <span data-ttu-id="f5f84-477">TransferCartRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-477">TransferCartRequestHandler</span></span>              | <span data-ttu-id="f5f84-478">この要求は、指定されたショッピング カートを転送します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-478">This request transfers the specified shopping cart.</span></span>                                                                        |
| <span data-ttu-id="f5f84-479">UpdateCommissionSalesGroupRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-479">UpdateCommissionSalesGroupRequest</span></span> | <span data-ttu-id="f5f84-480">UpdateCommissionSalesGroupHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-480">UpdateCommissionSalesGroupHandler</span></span>       | <span data-ttu-id="f5f84-481">この要求により、カートまたはカート行の販売担当者を更新するための要求がカプセル化されます。</span><span class="sxs-lookup"><span data-stu-id="f5f84-481">This request encapsulates a request for updating the sales representative on the cart or the cart line.</span></span>                    |
| <span data-ttu-id="f5f84-482">UploadOrderRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-482">UploadOrderRequest</span></span>                | <span data-ttu-id="f5f84-483">UploadOrderRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-483">UploadOrderRequestHandler</span></span>               | <span data-ttu-id="f5f84-484">この要求は、販売注文をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f5f84-484">This request uploads the sales order.</span></span>                                                                                      |
| <span data-ttu-id="f5f84-485">ValidateCartForCheckoutRequest</span><span class="sxs-lookup"><span data-stu-id="f5f84-485">ValidateCartForCheckoutRequest</span></span>    | <span data-ttu-id="f5f84-486">ValidateCartForCheckoutRequestHandler</span><span class="sxs-lookup"><span data-stu-id="f5f84-486">ValidateCartForCheckoutRequestHandler</span></span>   | <span data-ttu-id="f5f84-487">この要求は、チェックアウトのカートを検証します。</span><span class="sxs-lookup"><span data-stu-id="f5f84-487">This request validates the cart for checkout.</span></span>                                                                              |

