---
title: 支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する
description: このトピックでは、支払ターミナルの拡張機能のカスタム エラー メッセージを作成する方法について説明します。
author: ''
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2018-07-20
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ea117efdbe3c905cc67286080b15a2553a8039dc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369908"
---
# <a name="create-custom-localized-error-messages-for-payment-terminal-extensions"></a><span data-ttu-id="954f8-103">支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="954f8-103">Create custom localized error messages for payment terminal extensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="954f8-104">このトピックでは、支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="954f8-104">This topic explains how to create custom localized error messages for payment terminal extensions.</span></span> <span data-ttu-id="954f8-105">これらのカスタム エラー メッセージは、支払いターミナルが販売時点管理 (POS) ターミナルを使用しているレジ係に、特定の支払いが失敗した理由に関する関連情報を与えるために、最も頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="954f8-105">These custom error messages are most often used so that the payment terminal can give the cashier who is using the point of sale (POS) terminal relevant information about why a specific payment was unsuccessful.</span></span> <span data-ttu-id="954f8-106">たとえば、外部の支払ターミナルまたはゲートウェイは、支払いプロバイダーとのトラブルシューティングに関連する一意の識別子 (参照番号またはトランザクション識別子など) を返すことがあります。</span><span class="sxs-lookup"><span data-stu-id="954f8-106">For example, the external payment terminal or gateway might return unique identifiers (such as reference numbers or transaction identifiers) that are relevant for troubleshooting with the payment provider.</span></span>

## <a name="key-terms"></a><span data-ttu-id="954f8-107">重要な用語</span><span class="sxs-lookup"><span data-stu-id="954f8-107">Key terms</span></span>

| <span data-ttu-id="954f8-108">期間</span><span class="sxs-lookup"><span data-stu-id="954f8-108">Term</span></span> | <span data-ttu-id="954f8-109">説明</span><span class="sxs-lookup"><span data-stu-id="954f8-109">Description</span></span> |
|---|---|
| <span data-ttu-id="954f8-110">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="954f8-110">Payment connector</span></span> | <span data-ttu-id="954f8-111">POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="954f8-111">An extension library that is written to integrate the POS with a payment terminal.</span></span> |

## <a name="overview"></a><span data-ttu-id="954f8-112">概要</span><span class="sxs-lookup"><span data-stu-id="954f8-112">Overview</span></span>
<span data-ttu-id="954f8-113">このトピックの残りのセクションでは、支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する次の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="954f8-113">The remaining sections in this topic describe the following steps for creating custom localized error messages for payment terminal extensions:</span></span>

- <span data-ttu-id="954f8-114">**[カスタム エラー メッセージを作成します](#Create-custom-error-messages)** – このセクションでは、返すことが可能で POS に表示される支払コネクタでカスタム エラー メッセージを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="954f8-114">**[Create custom error messages](#Create-custom-error-messages)** – This section explains how to create custom error messages in the payment connector that can be returned and shown in the POS.</span></span>
- <span data-ttu-id="954f8-115">**[ローカライズ済みエラー メッセージを作成します](#Create-localized-error-messages)** – このセクションでは、返され、POS に表示される支払コネクタでエラー メッセージをローカライズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="954f8-115">**[Create localized error messages](#Create-localized-error-messages)** – This section explains how to localize the error messages in the payment connector that are returned and shown in the POS.</span></span>

## <a name="create-custom-error-messages"></a><span data-ttu-id="954f8-116">カスタム エラー メッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="954f8-116">Create custom error messages</span></span>
<span data-ttu-id="954f8-117">POS でカスタム エラー メッセージをトリガーするには、**AuthorizePaymentTerminalDeviceResponse** オブジェクトに渡される **paymentInfo** の**エラー**プロパティに、適切なエラーを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="954f8-117">To trigger a custom error message in the POS, you must set the appropriate error in the **Errors** property of the **paymentInfo** object that is passed to the **AuthorizePaymentTerminalDeviceResponse** object.</span></span> <span data-ttu-id="954f8-118">具体的には、辞退済の支払の組み込みエラー メッセージの代わりに、カスタム エラー メッセージを使用する POS を強制するように、**PaymentError** オブジェクトのコンストラクター上の **isLocalized** パラメーターを **true** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="954f8-118">Specifically, you must set the **isLocalized** parameter on the constructor of the **PaymentError** object to **true** to force the POS to use the custom error message instead of the built-in error message for a declined payment.</span></span>

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
                    typeof(AuthorizePaymentTerminalDeviceRequest),
                    ...
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
            Response response;
            if (requestType == typeof(AuthorizePaymentTerminalDeviceRequest))
            {
                response = this.AuthorizePayment((AuthorizePaymentTerminalDeviceRequest)request);
            }
            else if (...)
            {
                ...
            }
            else
            {
                throw new NotSupportedException(string.Format(CultureInfo.InvariantCulture, "Request '{0}' is not supported.", request));
            }
            return response;
        }

        /// <summary>
        /// Authorize payment.
        /// </summary>
        /// <param name="request">The authorize payment request.</param>
        /// <returns>The authorize payment response.</returns>
        public AuthorizePaymentTerminalDeviceResponse AuthorizePayment(AuthorizePaymentTerminalDeviceRequest request)
        {
            ThrowIf.Null(request, "request");
            ...

            // Assuming the external payment terminal/gateway returned a decline and a reference number.
            // Construct the custom error message and set the payment error on the 'paymentInfo' object set
            // on the response.
            PaymentInfo paymentInfo = new PaymentInfo();
            bool isLocalized = true;
            string errorMessage = string.Format("The payment was declined. Reference number '{0}'.", referenceNumber);
            PaymentError paymentError = new PaymentError(ErrorCode.Decline, errorMessage, isLocalized);
            paymentInfo.Errors = new PaymentError[] { paymentError };
            return new AuthorizePaymentTerminalDeviceResponse(paymentInfo);
        }
    }
}
```

<span data-ttu-id="954f8-119">POS でカスタム エラー メッセージを表示する方法を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="954f8-119">The following illustration shows how the custom error message appears in the POS.</span></span>

![POS での支払のカスタム エラー メッセージ](media/PAYMENTS/CUSTOM-ERRORS/POS-Custom-Payment-Error.jpg)

## <a name="create-localized-error-messages"></a><span data-ttu-id="954f8-121">ローカライズされたエラー メッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="954f8-121">Create localized error messages</span></span>

### <a name="create-resource-files-for-each-locale"></a><span data-ttu-id="954f8-122">ロケールごとにリソース ファイルを作成する</span><span class="sxs-lookup"><span data-stu-id="954f8-122">Create resource files for each locale</span></span>
<span data-ttu-id="954f8-123">ローカライズされたエラー メッセージを支払コネクタから POS に返すには、サポートするロケールごとにローカライズされたリソース ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="954f8-123">To return localized error messages from the payment connector to the POS, you must create localized resource files for each locale that you plan to support.</span></span> <span data-ttu-id="954f8-124">リソース ファイルを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="954f8-124">To create a resource file, follow these steps.</span></span>

1. <span data-ttu-id="954f8-125">Microsoft Visual Studio では、コネクタのプロジェクト (または、必要に応じてサブフォルダー) を右クリックし、**追加 \> 新しい項目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="954f8-125">In Microsoft Visual Studio, right-click the connector project (or a subfolder, as required), and then select **Add \> New Item**.</span></span>
2. <span data-ttu-id="954f8-126">新しい**新しい項目の追加**ダイアログ ボックスで、左側のウィンドウで **Visual C# 項目**を、中央のウィンドウで**リソース ファイル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="954f8-126">In the new **Add New Item** dialog box, select **Visual C# Items** in the left pane and **Resource File** in the center pane.</span></span>

    ![Visual Studio の新しいリソース ファイルを作成する](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-New-Resource-File.jpg)

<span data-ttu-id="954f8-128">作成するすべてのリソース ファイルのファイル名には、ローカライズされたサテライト アセンブリを生成できるように、カルチャ固有の接尾語 (例: **en-us**) が必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="954f8-128">Note that a culture-specific postfix (for example, **en-us**) is required in the file name of every resource file that you create, so that localized satellite assemblies can be generated.</span></span>

<span data-ttu-id="954f8-129">完了したら、次のリソース ファイルがプロジェクト内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="954f8-129">When you've finished, the following resource files should be present in your project.</span></span> <span data-ttu-id="954f8-130">次の図では 1 つの余分なロケールのみを示していますが (**en-us**)、必要なだけ多くのロケールのサポートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="954f8-130">Although the following illustration shows only one extra locale (**en-us**), you can add support for as many locales as you require.</span></span>

<span data-ttu-id="954f8-131">カルチャがニュートラルのリソース ファイル (この例では **Messages.resx**) が定義されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="954f8-131">Make sure that a culture-neutral resources file (**Messages.resx** in this example) is defined.</span></span> <span data-ttu-id="954f8-132">このファイルは、特定のカルチャのファイルが見つからない場合、予備として使用されます。</span><span class="sxs-lookup"><span data-stu-id="954f8-132">This file is used as a fallback if the file for a specific culture is missing.</span></span>

![Visual Studio のリソース ファイル](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Layout-Resource-File.jpg)

<span data-ttu-id="954f8-134">次の図が示すように、Visual Studio でリソース ファイルに正しいプロパティが設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="954f8-134">You must also make sure that the correct properties are set for the resource files in Visual Studio, as shown in the following illustration.</span></span>

![Visual Studio の新しいリソース ファイルのプロパティ](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Properties-Resource-File.jpg)

### <a name="create-custom-localized-error-messages"></a><span data-ttu-id="954f8-136">ローカライズされたカスタム エラー メッセージを作成する</span><span class="sxs-lookup"><span data-stu-id="954f8-136">Create custom localized error messages</span></span>
<span data-ttu-id="954f8-137">すべてのリソース ファイルには、カスタマイズし、ローカライズするすべてのエラー メッセージを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="954f8-137">Every resource file must contain every error message that you want to customize and localize.</span></span> <span data-ttu-id="954f8-138">次の図は、リソース ファイルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="954f8-138">The following illustration shows an example of a resource file.</span></span> <span data-ttu-id="954f8-139">**CustomPaymentConnector_Decline** エントリは、特定のロケールの適切なメッセージを取得するコードで参照されています。</span><span class="sxs-lookup"><span data-stu-id="954f8-139">Notice that the **CustomPaymentConnector_Decline** entry is referenced in the code to retrieve the appropriate message for a specific locale.</span></span> <span data-ttu-id="954f8-140">各ロケールのすべてのリソース ファイルには、ローカライズされたメッセージの同一のセットが必要です。</span><span class="sxs-lookup"><span data-stu-id="954f8-140">Every resource file for every locale should have an identical set of localized messages.</span></span>

![Visual Studio でのリソース ファイルの内容](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Content-Resource-File.jpg)

### <a name="load-the-localized-message-in-the-connector-code"></a><span data-ttu-id="954f8-142">コネクタ コードで、ローカライズされたメッセージを読み込む</span><span class="sxs-lookup"><span data-stu-id="954f8-142">Load the localized message in the connector code</span></span>
<span data-ttu-id="954f8-143">次の例では、ローカライズされたメッセージを読み込むために支払コネクタ コードの最初に作成したリソース ファイルの使用方法が確認できます。</span><span class="sxs-lookup"><span data-stu-id="954f8-143">The following example shows how you can use the resource files that you created earlier in your payment connector code to load a localized message.</span></span> <span data-ttu-id="954f8-144">プロセスは、2 つの手順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="954f8-144">The process consists of two steps:</span></span>

1. <span data-ttu-id="954f8-145">リクエストのロケールにアクセスするには、 **OpenPaymentTerminalDeviceRequest** リクエスト中に **terminalSettings** が取得されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="954f8-145">Make sure that **terminalSettings** is retrieved during the **OpenPaymentTerminalDeviceRequest** request, to access the locale for the request.</span></span>
2. <span data-ttu-id="954f8-146">**AuthorizePaymentTerminalDeviceRequest** 呼び出し (または同等の呼び出し) 中に、**terminalSettings** の **Locale** プロパティを使用して、ローカライズされたメッセージの正しいリソースファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="954f8-146">During the **AuthorizePaymentTerminalDeviceRequest** call (or equivalent calls), use the **Locale** property on **terminalSettings** to retrieve the correct resource file for the localized message.</span></span>

> [!NOTE]
> <span data-ttu-id="954f8-147">次の使用例は、支払コネクタ コードの実行時に、ローカライズされたメッセージの読込のしくみを表示するために大幅に簡素化されました。</span><span class="sxs-lookup"><span data-stu-id="954f8-147">The following example has been significantly simplified to show the mechanics of loading localized messages during the runtime of your payment connector code.</span></span> <span data-ttu-id="954f8-148">ただし、適切なリソース ファイルの読み込みを管理する新しいクラスのセットを導入することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="954f8-148">However, we recommend that you introduce a new set of classes to manage loading of the appropriate resource file.</span></span>

``` csharp
namespace Contoso.Commerce.HardwareStation.PaymentSample 
{ 
    /// <summary>
    /// <c>Simulator</c> manager payment device class.
    /// </summary>
    public class PaymentDeviceSample : INamedRequestHandler
    {
        // Cached version of the terminal settings retrieved during the OpenPaymentTerminalDeviceRequest call.
        private SettingsInfo terminalSettings;

        // Resource manager to retrieve localized messages.
        private ResourceManager messagesResourceManager;

        /// <summary>
        /// Initializes a new instance of the <see cref="PaymentDeviceSample"/> class.
        /// </summary>
        public PaymentDeviceSample()
        {
            this.messagesResourceManager = new ResourceManager("Contoso.Commerce.HardwareStation.PaymentSample.PaymentDeviceSample .Resources.Messages", typeof(PaymentDeviceSample).GetTypeInfo().Assembly);
        }

        /// <summary>
        /// Gets the collection of supported request types by this handler.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                    typeof(OpenPaymentTerminalDeviceRequest),
                    typeof(AuthorizePaymentTerminalDeviceRequest),
                    ...
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
            Response response;
            if (requestType == typeof(OpenPaymentTerminalDeviceRequest))
            {
                response = this.Open((OpenPaymentTerminalDeviceRequest)request);
            }
            else if (requestType == typeof(AuthorizePaymentTerminalDeviceRequest))
            {
                response = this.AuthorizePayment((AuthorizePaymentTerminalDeviceRequest)request);
            }
            else if (...)
            {
                ...
            }
            else
            {
                throw new NotSupportedException(string.Format(CultureInfo.InvariantCulture, "Request '{0}' is not supported.", request));
            }
            return response;
        }

        /// <summary>
        /// Open the payment terminal.
        /// </summary>
        /// <param name="request">The open request.</param>
        /// <returns>The open response.</returns>
        private Response Open(OpenPaymentTerminalDeviceRequest request)
        {
            this.terminalSettings = request.TerminalSettings;
            ...
        }

        /// <summary>
        /// Authorize payment.
        /// </summary>
        /// <param name="request">The authorize payment request.</param>
        /// <returns>The authorize payment response.</returns>
        public AuthorizePaymentTerminalDeviceResponse AuthorizePayment(AuthorizePaymentTerminalDeviceRequest request)
        {
            ...

            // Assuming the external payment terminal/gateway returned a decline and a reference number. Construct 
            // the custom error message and set the payment error on the 'paymentInfo' object set on the response.
            PaymentInfo paymentInfo = new PaymentInfo();
            CultureInfo cultureInfo = new CultureInfo(this.terminalSettings.Locale);
            string localizedString = this.messagesResourceManager.GetString("CustomPaymentConnector_Decline", cultureInfo);
            string errorMessage = string.Format(localizedString, referenceNumber);
            bool isLocalized = true;
            PaymentError paymentError = new PaymentError(ErrorCode.Decline, errorMessage, isLocalized);
            paymentInfo.Errors = new PaymentError[] { paymentError };
            return new AuthorizePaymentTerminalDeviceResponse(paymentInfo);
        }
    }
}
```
