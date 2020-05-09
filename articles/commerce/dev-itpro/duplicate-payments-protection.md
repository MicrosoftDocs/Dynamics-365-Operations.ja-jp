---
title: 支払コネクタの重複支払保護の有効化
description: このトピックでは、指定された支払コネクタで重複支払保護を有効にする方法について説明します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 683d0fc35dda652195cab0b11124be4bca24178c
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138550"
---
# <a name="enable-duplicate-payment-protection-for-payment-connector"></a><span data-ttu-id="d2cd6-103">支払コネクタの重複支払保護の有効化</span><span class="sxs-lookup"><span data-stu-id="d2cd6-103">Enable duplicate payment protection for payment connector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2cd6-104">このトピックでは、支払ターミナルとの統合を管理する支払コネクタの重複支払保護機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-104">This topic describes how to enable duplicate payment protection functionality in a payment connector that manages the integration with a payment terminal.</span></span> <span data-ttu-id="d2cd6-105">*支払コネクタ*は支払ターミナルをPOSに統合するために書き込まれた拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-105">A *payment connector* is an extension library that is written to integrate the POS with a payment terminal.</span></span>

## <a name="overview"></a><span data-ttu-id="d2cd6-106">概要</span><span class="sxs-lookup"><span data-stu-id="d2cd6-106">Overview</span></span>

- <span data-ttu-id="d2cd6-107">[必読](#required-reading) - 支払コネクタに重複支払保護機能の実装を開始する前に必ず読むべきトピックの一覧。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-107">[Required reading](#required-reading) - List of topics that you should be read before starting the implementation of the duplicate payment protection functionality in a payment connector.</span></span> 
- <span data-ttu-id="d2cd6-108">[前提条件](#prerequisites) - 支払コネクタの実装に重複支払保護を有効にする前提条件の一覧。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-108">[Prerequisites](#prerequisites) - List of prerequisites to enable duplicate payment protection in a payment connector implementation.</span></span>
- <span data-ttu-id="d2cd6-109">[重複支払保護フローを理解する](#understanding-duplicate-payment-protection-flows) - 重複支払保護が POS で呼び出される時のさまざまなフローについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-109">[Understanding duplicate payment protection flows](#understanding-duplicate-payment-protection-flows) - Describes the various flows where the duplicate payment protection is invoked in the POS.</span></span>
- <span data-ttu-id="d2cd6-110">[重複支払要求の実装](#implement-duplicate-payment-requests) - 重複支払保護機能をサポートするために実装する必要があるさまざまな支払に関連する要求について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-110">[Implement duplicate payment requests](#implement-duplicate-payment-requests) - Describes the various payment-related requests that need to be implemented to support the duplicate payment protection feature.</span></span>

## <a name="required-reading"></a><span data-ttu-id="d2cd6-111">読む必要があります</span><span class="sxs-lookup"><span data-stu-id="d2cd6-111">Required reading</span></span>
<span data-ttu-id="d2cd6-112">特定の支払コネクタで重複支払保護を有効にする前に、次のトピックを必ずお読みください。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-112">Be sure to read the following topic before enabling duplicate payment protection for a given payment connector.</span></span>

- <span data-ttu-id="d2cd6-113">[支払端末のエンド・ツー・エンド支払統合を作成する](end-to-end-payment-extension.md) - 重複支払保護機能は、このトピックで説明されている支払端末の支払統合に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-113">[Create an end-to-end payment integration for a payment terminal](end-to-end-payment-extension.md) - The duplicate payment protection feature builds on the payment integration for a payment terminal described in this topic.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d2cd6-114">必要条件</span><span class="sxs-lookup"><span data-stu-id="d2cd6-114">Prerequisites</span></span>
<span data-ttu-id="d2cd6-115">支払コネクタの実装で重複支払保護を有効にする前に、次の前提条件が満たされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-115">The following prerequisites must be met before duplicate payment protection can be enabled for a payment connector implementation.</span></span>

### <a name="support-for-unique-transaction-scope-in-payment-terminal-or-payment-gatewayprocessor"></a><span data-ttu-id="d2cd6-116">支払端末または支払ゲートウェイ/プロセッサに固有のトランザクション スコープのサポート</span><span class="sxs-lookup"><span data-stu-id="d2cd6-116">Support for unique transaction scope in payment terminal or payment gateway/processor</span></span>
<span data-ttu-id="d2cd6-117">重複支払保護のサポートを有効にするために、対応する支払端末または支払ゲートウェイ/プロセッサは固有のトランザクション スコープのサポートを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-117">In order to enable support for duplicate payment protection, the corresponding payment terminal or payment gateway/processor must provide support for unique transaction scopes.</span></span> <span data-ttu-id="d2cd6-118">通常、このサポートは支払端末で生成される固有の支払参照識別子を通して、または支払が処理される前に支払ゲートウェイ/プロセッサにより処理されています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-118">This support is usually handled through a unique payment reference identifier that can be generated by the payment terminal or payment gateway/processor before the payment is being processed.</span></span> <span data-ttu-id="d2cd6-119">一意の識別子のサポートなしでは、コネクタは先に開始された取引を、正常に行われた支払の承認と一意に対応付けることができず、これが重複支払保護が失敗する元となります。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-119">Without support for this unique identifier, the connector will not be able to uniquely match a previously initiated transaction with a successful payment authorization, which is at the core of the duplicate payment protection feature.</span></span>

## <a name="understanding-duplicate-payment-protection-flows"></a><span data-ttu-id="d2cd6-120">重複支払保護フローを理解します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-120">Understanding duplicate payment protection flows</span></span>
<span data-ttu-id="d2cd6-121">Retail POS が拡張され、支払コネクタに**承認**要求を出す直前など、POS 全体の様々なシナリオで新しい要求である `GetTransactionReferencePaymentTerminalDeviceRequest` および `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` を呼び出すようになりました。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-121">The Retail POS has been extended to invoke the new requests, `GetTransactionReferencePaymentTerminalDeviceRequest` and `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` in various scenarios across the POS, such as immediately before an **Authorize** request is issued to the payment connector.</span></span> <span data-ttu-id="d2cd6-122">これらの新しい要求の目的は、新しい支払要求を実行する前に、支払コネクタを通して正常に処理された支払を検出し、復元するものです。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-122">The purpose of these new requests is to detect and recover successfully processed payment through the payment connector before a new payment request is issued.</span></span> <span data-ttu-id="d2cd6-123">次の図は、支払要求は支払コネクタを通して正常に処理されたものの、応答を受信する前にPOS がクラッシュしたというシンプルなシナリオを示しています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-123">The following diagram illustrates a simple scenario where a payment request is successfully processed through the payment connector but the POS has crashed before it can receive the response.</span></span> <span data-ttu-id="d2cd6-124">その後、POS は重複支払保護機能により、前の処理済の支払を復元することができます。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-124">Subsequently, the POS is able to recover the previously processed payment through the duplicate payment protection feature.</span></span> 

![重複支払保護フロー](media/PAYMENTS/DUPLICATE-PAYMENT-PROTECTION/DuplicatePaymentProtectionFlow.jpg)


### <a name="supported-pos-flows"></a><span data-ttu-id="d2cd6-126">サポートされている POS フロー</span><span class="sxs-lookup"><span data-stu-id="d2cd6-126">Supported POS flows</span></span>
<span data-ttu-id="d2cd6-127">次のリストは、`GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` が既存の支払を回収するために呼び出される時のすべての POS フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-127">The following list describes all of the POS flows where the `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` is invoked to recover an existing payment.</span></span> <span data-ttu-id="d2cd6-128">これらは、支払取引の処理中にPOS がクラッシュ、または支払端末または支払ゲートウェイへの接続を喪失したときに最も一般的に実行されるフローです。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-128">These are the most commonly executed flows when the POS crashes or loses connectivity to the payment terminal or payment gateway during the processing of a payment transaction.</span></span>

- <span data-ttu-id="d2cd6-129">レジ担当者がカード支払を使用して金額に対して支払を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-129">Cashier invokes payment for any amount using a card payment</span></span>
- <span data-ttu-id="d2cd6-130">レジ担当者が現金支払を使用して金額に対して支払を呼び出します</span><span class="sxs-lookup"><span data-stu-id="d2cd6-130">Cashier invokes payment for any amount using a cash payment</span></span>
- <span data-ttu-id="d2cd6-131">レジ担当者が、カートの明細行を無効化しようとしています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-131">Cashier attempts to void a line on the cart</span></span>
- <span data-ttu-id="d2cd6-132">レジ担当者が取引を無効化しようとしています</span><span class="sxs-lookup"><span data-stu-id="d2cd6-132">Cashier attempts to void the transaction</span></span>
- <span data-ttu-id="d2cd6-133">レジ担当者が取引を停止しようとしています</span><span class="sxs-lookup"><span data-stu-id="d2cd6-133">Cashier attempts to suspend the transaction</span></span>

## <a name="implement-duplicate-payment-requests"></a><span data-ttu-id="d2cd6-134">重複支払要求の実装</span><span class="sxs-lookup"><span data-stu-id="d2cd6-134">Implement duplicate payment requests</span></span>
<span data-ttu-id="d2cd6-135">次のサンプルは、`INamedRequestHandler` での要求を例示します- これは、重複支払保護機能を確実に有効化するために必要な支払コネクタ実装です。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-135">The following sample illustrates the requests on the `INamedRequestHandler` payment connector implementation that are required to fully enable the duplicate payment protection feature.</span></span>

``` csharp
namespace Contoso.Commerce.HardwareStation.PaymentSample 
{ 
    /// <summary>
    /// <c>Simulator</c> manager payment device class.
    /// </summary>
    public class PaymentDeviceSample : INamedRequestHandler
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
                    // New request types specific to the duplicate payment protection feature.
                    typeof(GetTransactionReferencePaymentTerminalDeviceRequest),
                    typeof(GetTransactionByTransactionReferencePaymentTerminalDeviceRequest),
                    
                    // Extended with new functionality.
                    typeof(AuthorizePaymentTerminalDeviceRequest)
                };
            }
        }

        /// <summary>
        /// Executes the payment device simulator operation based on the incoming request type.
        /// </summary>
        /// <param name="request">The payment terminal device simulator request message.</param>
        /// <returns>Returns the payment terminal device simulator response.</returns>
        public Response Execute(Microsoft.Dynamics.Commerce.Runtime.Messages.Request request)
        {
            ThrowIf.Null(request, nameof(request));

            Type requestType = request.GetType();

            if (requestType == typeof(GetTransactionReferencePaymentTerminalDeviceRequest))
            {
                return this.GetTransactionReference((GetTransactionReferencePaymentTerminalDeviceRequest)request);
            }
            else if (requestType == typeof(GetTransactionByTransactionReferencePaymentTerminalDeviceRequest))
            {
                return this.GetTransactionByTransactionReference((GetTransactionByTransactionReferencePaymentTerminalDeviceRequest)request);
            }
            else if (requestType == typeof(AuthorizePaymentTerminalDeviceRequest))
            {
                return this.AuthorizePayment((AuthorizePaymentTerminalDeviceRequest)request);
            }
            ...

            return new NullResponse();
        }
    }
}
```

### <a name="gettransactionreferencepaymentterminaldevicerequest--gettransactionreferencepaymentterminaldeviceresponse"></a><span data-ttu-id="d2cd6-136">GetTransactionReferencePaymentTerminalDeviceRequest / GetTransactionReferencePaymentTerminalDeviceResponse</span><span class="sxs-lookup"><span data-stu-id="d2cd6-136">GetTransactionReferencePaymentTerminalDeviceRequest / GetTransactionReferencePaymentTerminalDeviceResponse</span></span>

#### <a name="description"></a><span data-ttu-id="d2cd6-137">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-137">Description</span></span>
<span data-ttu-id="d2cd6-138">`GetTransactionReferencePaymentTerminalDeviceRequest` は、支払取引の開始時に Retail POS に呼び出され、支払のスコープを設定します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-138">The `GetTransactionReferencePaymentTerminalDeviceRequest` is invoked by the Retail POS at the beginning of a payment transaction and sets the scope of the payment.</span></span> <span data-ttu-id="d2cd6-139">この要求のスコープは、支払明細行が正常にカートに追加されるか、もしくはカードが使用できず、支払コネクタから戻らないことを表示するエラーが出ると終了します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-139">The scope of this request ends once the payment line is successfully added to the cart or an error, indicating that a card cannot be used and returned from the payment connector.</span></span> <span data-ttu-id="d2cd6-140">対応する `GetTransactionReferencePaymentTerminalDeviceResponse` 応答には、支払取引を検索するために支払コネクタによって生成される対応する一意の識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-140">The corresponding `GetTransactionReferencePaymentTerminalDeviceResponse` response will contain the corresponding unique identifier generated by the payment connector to look up a payment transaction.</span></span> <span data-ttu-id="d2cd6-141">ID はアプリケーションの再起動後も維持される必要があり、通常、支払ゲートウェイによって ID が生成されるべきなので、支払コネクタの実装は生成された ID をキャッシュしてはいけないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-141">Note that the payment connector implementation must not cache the generated ID because the ID must survive the application's restarts, typically the ID should be generated by the Payment Gateway.</span></span>

#### <a name="request-signature"></a><span data-ttu-id="d2cd6-142">署名の要求</span><span class="sxs-lookup"><span data-stu-id="d2cd6-142">Request signature</span></span>
``` csharp
public GetTransactionReferencePaymentTerminalDeviceRequest(string lockToken, string posTerminalId, string eftTerminalId);
```

#### <a name="request-variables"></a><span data-ttu-id="d2cd6-143">変数の要求</span><span class="sxs-lookup"><span data-stu-id="d2cd6-143">Request variables</span></span>
| <span data-ttu-id="d2cd6-144">変数</span><span class="sxs-lookup"><span data-stu-id="d2cd6-144">Variable</span></span> | <span data-ttu-id="d2cd6-145">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-145">Description</span></span> |
|---|---|
| <span data-ttu-id="d2cd6-146">lockToken</span><span class="sxs-lookup"><span data-stu-id="d2cd6-146">lockToken</span></span> | <span data-ttu-id="d2cd6-147">支払端末が最初の取引のためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-147">Unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="d2cd6-148">posTerminalId</span><span class="sxs-lookup"><span data-stu-id="d2cd6-148">posTerminalId</span></span> | <span data-ttu-id="d2cd6-149">POS レジスターの固有の名前</span><span class="sxs-lookup"><span data-stu-id="d2cd6-149">Unique name of the POS register.</span></span> |
| <span data-ttu-id="d2cd6-150">eftTerminalId</span><span class="sxs-lookup"><span data-stu-id="d2cd6-150">eftTerminalId</span></span> | <span data-ttu-id="d2cd6-151">EFT POS 端末番号は、POS レジスターまたは共有ハードウェア ステーションを構成します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-151">EFT POS terminal number configured either on the POS register or the shared Hardware Station.</span></span> |

#### <a name="response-signature"></a><span data-ttu-id="d2cd6-152">署名への応答</span><span class="sxs-lookup"><span data-stu-id="d2cd6-152">Response signature</span></span>
``` csharp
public GetTransactionReferencePaymentTerminalDeviceResponse(string id);
```

#### <a name="response-variables"></a><span data-ttu-id="d2cd6-153">変数への応答</span><span class="sxs-lookup"><span data-stu-id="d2cd6-153">Response variables</span></span>
| <span data-ttu-id="d2cd6-154">変数</span><span class="sxs-lookup"><span data-stu-id="d2cd6-154">Variable</span></span> | <span data-ttu-id="d2cd6-155">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-155">Description</span></span> |
|---|---|
| <span data-ttu-id="d2cd6-156">id</span><span class="sxs-lookup"><span data-stu-id="d2cd6-156">id</span></span> | <span data-ttu-id="d2cd6-157">支払取引のスコープに使用する一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-157">Unique identifier used for the scope of the payment transaction.</span></span> |

### <a name="paymenttransactionreferencedata"></a><span data-ttu-id="d2cd6-158">PaymentTransactionReferenceData</span><span class="sxs-lookup"><span data-stu-id="d2cd6-158">PaymentTransactionReferenceData</span></span> 
<span data-ttu-id="d2cd6-159">`GetTransactionReferencePaymentTerminalDeviceRequest` が実行された後、Retail POS は `PaymentTransactionReferenceData` クラスの新しいインスタンスを生成し、重複支払保護スコープを維持するために POS に必要なコンテキスト データを実行します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-159">After the `GetTransactionReferencePaymentTerminalDeviceRequest` is executed, the Retail POS will generate a new instance of the `PaymentTransactionReferenceData` class to carry the required contextual data that is needed for the POS to maintain the duplicate payment protection scope.</span></span> <span data-ttu-id="d2cd6-160">この変数は POS で格納および管理され、キーの支払操作時に既存の取引を確認するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-160">This variable will be stored and maintained in the POS and then used to check for existing transactions during key payment operations.</span></span> 

#### <a name="properties"></a><span data-ttu-id="d2cd6-161">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d2cd6-161">Properties</span></span>
| <span data-ttu-id="d2cd6-162">変数</span><span class="sxs-lookup"><span data-stu-id="d2cd6-162">Variable</span></span> | <span data-ttu-id="d2cd6-163">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-163">Description</span></span> |
|---|---|
| <span data-ttu-id="d2cd6-164">コマンド</span><span class="sxs-lookup"><span data-stu-id="d2cd6-164">Command</span></span> | <span data-ttu-id="d2cd6-165">支払には、呼び出されたコマンドが関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-165">Payment related command that was invoked.</span></span> <span data-ttu-id="d2cd6-166">可能性がある値は、`Sale`、`Refund`、`Activate`、もしくは `Load` です。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-166">Possible values are `Sale`, `Refund`, `Activate`, or `Load`.</span></span> |
| <span data-ttu-id="d2cd6-167">IdFromConnector</span><span class="sxs-lookup"><span data-stu-id="d2cd6-167">IdFromConnector</span></span> | <span data-ttu-id="d2cd6-168">`GetTransactionReferencePaymentTerminalDeviceRequest` 要求を通して生成された一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-168">Unique identifier generated through the `GetTransactionReferencePaymentTerminalDeviceRequest` request.</span></span> |
| <span data-ttu-id="d2cd6-169">InitiatedDate</span><span class="sxs-lookup"><span data-stu-id="d2cd6-169">InitiatedDate</span></span> | <span data-ttu-id="d2cd6-170">元の支払に関連する取引が開始された日付と時刻。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-170">Date and time when the original payment-related transaction was initiated.</span></span> |
| <span data-ttu-id="d2cd6-171">UniqueTransactionId</span><span class="sxs-lookup"><span data-stu-id="d2cd6-171">UniqueTransactionId</span></span> | <span data-ttu-id="d2cd6-172">(支払そのものには特定されていない) カート取引の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-172">Unique identifier for the cart transaction (not specific to a payment itself).</span></span> |
| <span data-ttu-id="d2cd6-173">金額</span><span class="sxs-lookup"><span data-stu-id="d2cd6-173">Amount</span></span> | <span data-ttu-id="d2cd6-174">処理されている支払取引の金額。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-174">Amount of the payment transaction being handled.</span></span> |

### <a name="authorizepaymentterminaldevicerequest"></a><span data-ttu-id="d2cd6-175">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="d2cd6-175">AuthorizePaymentTerminalDeviceRequest</span></span>

#### <a name="description"></a><span data-ttu-id="d2cd6-176">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-176">Description</span></span>
<span data-ttu-id="d2cd6-177">`AuthorizePaymentTerminalDeviceRequest` パラメーターは、新しい要求である `PaymentTransactionReferenceData` をサポートする新しいコンストラクターを提供するよう拡張されています。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-177">`AuthorizePaymentTerminalDeviceRequest` parameter has now been extended to provide a new constructor that supports the new request, `PaymentTransactionReferenceData`.</span></span> <span data-ttu-id="d2cd6-178">このパラメーターの目的は、コンテキスト参照データを管理し、また支払コネクタによって生成され、重複支払を識別し、後でのクエリのために POS により使用される一意の識別子と支払端末または支払ゲートウェイ/プロセッサへの承認要求にスタンプすることです。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-178">The purpose of this parameter is to maintain the contextual reference data and stamp the authorization request to the payment terminal or payment gateway/processor with the unique identifier generated by the payment connector and used by the POS to later query for and identify duplicate payments.</span></span> 

### <a name="gettransactionbytransactionreferencepaymentterminaldevicerequest--gettransactionbytransactionreferencepaymentterminaldeviceresponse"></a><span data-ttu-id="d2cd6-179">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest / GetTransactionByTransactionReferencePaymentTerminalDeviceResponse</span><span class="sxs-lookup"><span data-stu-id="d2cd6-179">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest / GetTransactionByTransactionReferencePaymentTerminalDeviceResponse</span></span>
<span data-ttu-id="d2cd6-180">既存の支払取引が支払端末または支払ゲートウェイ/プロセッサですでに呼び出され、かつ処理されたかどうかを区別するため、特定の支払いに関連した操作の直前に、Retail POS は `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-180">`GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` is invoked by the Retail POS immediately before certain payment-related operations to identify whether an existing payment transaction was already invoked and handled by the payment terminal or payment gateway/processor.</span></span> <span data-ttu-id="d2cd6-181">既存のトランザクションが支払コネクタにより復旧すると、新しい取引をトリガーするためコネクタに返され、短い回路の続く呼び出しがあります。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-181">If an existing transaction is recovered by the payment connector, it will be returned and short circuit subsequent calls to the connector to trigger a new transaction.</span></span>

#### <a name="request-signature"></a><span data-ttu-id="d2cd6-182">署名の要求</span><span class="sxs-lookup"><span data-stu-id="d2cd6-182">Request signature</span></span>
``` csharp
public GetTransactionByTransactionReferencePaymentTerminalDeviceRequest(string lockToken, PaymentTransactionReferenceData transactionReferenceData);
```

#### <a name="request-variables"></a><span data-ttu-id="d2cd6-183">変数の要求</span><span class="sxs-lookup"><span data-stu-id="d2cd6-183">Request variables</span></span>
| <span data-ttu-id="d2cd6-184">変数</span><span class="sxs-lookup"><span data-stu-id="d2cd6-184">Variable</span></span> | <span data-ttu-id="d2cd6-185">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-185">Description</span></span> |
|---|---|
| <span data-ttu-id="d2cd6-186">lockToken</span><span class="sxs-lookup"><span data-stu-id="d2cd6-186">lockToken</span></span> | <span data-ttu-id="d2cd6-187">支払端末が最初の取引のためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-187">Unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="d2cd6-188">transactionReferenceData</span><span class="sxs-lookup"><span data-stu-id="d2cd6-188">transactionReferenceData</span></span> | <span data-ttu-id="d2cd6-189">プロパティ バッグは、支払取引を一意に識別するために使用されるさまざまなプロパティを含みます。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-189">Property bag containing various properties used to uniquely identify a payment transaction.</span></span> <span data-ttu-id="d2cd6-190">詳細については、このトピック [PaymentTransactionReferenceData](#paymenttransactionreferencedata) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-190">For more information, see the section [PaymentTransactionReferenceData](#paymenttransactionreferencedata) in this topic.</span></span> |

#### <a name="response-signature"></a><span data-ttu-id="d2cd6-191">署名への応答</span><span class="sxs-lookup"><span data-stu-id="d2cd6-191">Response signature</span></span>
``` csharp
public GetTransactionByTransactionReferencePaymentTerminalDeviceResponse(PaymentInfo paymentInfo);
```

#### <a name="response-variables"></a><span data-ttu-id="d2cd6-192">変数への応答</span><span class="sxs-lookup"><span data-stu-id="d2cd6-192">Response variables</span></span>
| <span data-ttu-id="d2cd6-193">変数</span><span class="sxs-lookup"><span data-stu-id="d2cd6-193">Variable</span></span> | <span data-ttu-id="d2cd6-194">説明</span><span class="sxs-lookup"><span data-stu-id="d2cd6-194">Description</span></span> |
|---|---|
| <span data-ttu-id="d2cd6-195">paymentInfo</span><span class="sxs-lookup"><span data-stu-id="d2cd6-195">paymentInfo</span></span> | <span data-ttu-id="d2cd6-196">復元された支払取引。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-196">The recovered payment transaction.</span></span> <span data-ttu-id="d2cd6-197">これは、**承認**または**返金**のような、ほかの支払要求などで返される支払応答と同じです。</span><span class="sxs-lookup"><span data-stu-id="d2cd6-197">This is identical to the payment response returned for any other payment request, such as **Authorize** or **Refund**.</span></span> |
                                                                                                                                                                                                                                                                                                            