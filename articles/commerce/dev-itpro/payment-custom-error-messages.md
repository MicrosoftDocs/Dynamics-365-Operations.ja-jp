---
title: 支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する
description: このトピックでは、支払ターミナルの拡張機能のカスタム エラー メッセージを作成する方法について説明します。
author: Reza-Assadi
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2018-07-20
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9466cbf1ae62414488a6a05dfad3a3e5d804bfa7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355440"
---
# <a name="create-custom-localized-error-messages-for-payment-terminal-extensions"></a>支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する

[!include[banner](../includes/banner.md)]

このトピックでは、支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する方法について説明します。 これらのカスタム エラー メッセージは、支払いターミナルが販売時点管理 (POS) ターミナルを使用しているレジ係に、特定の支払いが失敗した理由に関する関連情報を与えるために、最も頻繁に使用されます。 たとえば、外部の支払ターミナルまたはゲートウェイは、支払いプロバイダーとのトラブルシューティングに関連する一意の識別子 (参照番号またはトランザクション識別子など) を返すことがあります。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| 支払コネクタ | POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。 |

## <a name="overview"></a>概要
このトピックの残りのセクションでは、支払ターミナルの拡張機能のローカライズされたカスタム エラー メッセージを作成する次の手順について説明します。

- **[カスタム エラー メッセージを作成します](#create-custom-error-messages)** – このセクションでは、返すことが可能で POS に表示される支払コネクタでカスタム エラー メッセージを作成する方法について説明します。
- **[ローカライズ済みエラー メッセージを作成します](#create-localized-error-messages)** – このセクションでは、返され、POS に表示される支払コネクタでエラー メッセージをローカライズする方法について説明します。

## <a name="create-custom-error-messages"></a>カスタム エラー メッセージを作成する
POS でカスタム エラー メッセージをトリガーするには、**AuthorizePaymentTerminalDeviceResponse** オブジェクトに渡される **paymentInfo** の **エラー** プロパティに、適切なエラーを設定する必要があります。 具体的には、辞退済の支払の組み込みエラー メッセージの代わりに、カスタム エラー メッセージを使用する POS を強制するように、**PaymentError** オブジェクトのコンストラクター上の **isLocalized** パラメーターを **true** に設定する必要があります。

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

POS でカスタム エラー メッセージを表示する方法を次の図に示します。

![POS のカスタム支払エラー メッセージ。](media/PAYMENTS/CUSTOM-ERRORS/POS-Custom-Payment-Error.jpg)

## <a name="create-localized-error-messages"></a>ローカライズされたエラー メッセージを作成する

### <a name="create-resource-files-for-each-locale"></a>ロケールごとにリソース ファイルを作成する
ローカライズされたエラー メッセージを支払コネクタから POS に返すには、サポートするロケールごとにローカライズされたリソース ファイルを作成する必要があります。 リソース ファイルを作成するには、次の手順に従います。

1. Microsoft Visual Studio では、コネクタのプロジェクト (または、必要に応じてサブフォルダー) を右クリックし、**追加 \> 新しい項目** を選択します。
2. 新しい **新しい項目の追加** ダイアログ ボックスで、左側のウィンドウで **Visual C# 項目** を、中央のウィンドウで **リソース ファイル** を選択します。

    ![Visual Studio の新しいリソース ファイルを作成します。](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-New-Resource-File.jpg)

作成するすべてのリソース ファイルのファイル名には、ローカライズされたサテライト アセンブリを生成できるように、カルチャ固有の接尾語 (例: **en-us**) が必要であることに注意してください。

完了したら、次のリソース ファイルがプロジェクト内に表示されます。 次の図では 1 つの余分なロケールのみを示していますが (**en-us**)、必要なだけ多くのロケールのサポートを追加できます。

カルチャがニュートラルのリソース ファイル (この例では **Messages.resx**) が定義されていることを確認してください。 このファイルは、特定のカルチャのファイルが見つからない場合、予備として使用されます。

![Visual Studio のリソース ファイル。](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Layout-Resource-File.jpg)

次の図が示すように、Visual Studio でリソース ファイルに正しいプロパティが設定されていることを確認する必要があります。

![Visual Studio の新しいリソース ファイルのプロパティ。](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Properties-Resource-File.jpg)

### <a name="create-custom-localized-error-messages"></a>ローカライズされたカスタム エラー メッセージを作成する
すべてのリソース ファイルには、カスタマイズし、ローカライズするすべてのエラー メッセージを含める必要があります。 次の図は、リソース ファイルの例を示しています。 **CustomPaymentConnector_Decline** エントリは、特定のロケールの適切なメッセージを取得するコードで参照されています。 各ロケールのすべてのリソース ファイルには、ローカライズされたメッセージの同一のセットが必要です。

![Visual Studio のリソース ファイルのコンテンツ。](media/PAYMENTS/CUSTOM-ERRORS/VisualStudio-Content-Resource-File.jpg)

### <a name="load-the-localized-message-in-the-connector-code"></a>コネクタ コードで、ローカライズされたメッセージを読み込む
次の例では、ローカライズされたメッセージを読み込むために支払コネクタ コードの最初に作成したリソース ファイルの使用方法が確認できます。 プロセスは、2 つの手順で構成されています。

1. リクエストのロケールにアクセスするには、 **OpenPaymentTerminalDeviceRequest** リクエスト中に **terminalSettings** が取得されていることを確認してください。
2. **AuthorizePaymentTerminalDeviceRequest** 呼び出し (または同等の呼び出し) 中に、**terminalSettings** の **Locale** プロパティを使用して、ローカライズされたメッセージの正しいリソースファイルを取得します。

> [!NOTE]
> 次の使用例は、支払コネクタ コードの実行時に、ローカライズされたメッセージの読込のしくみを表示するために大幅に簡素化されました。 ただし、適切なリソース ファイルの読み込みを管理する新しいクラスのセットを導入することをお勧めします。

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]