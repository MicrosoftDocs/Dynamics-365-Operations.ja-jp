---
title: インド向け QR コードの生成とレシートへの印刷
description: このトピックでは、インド向けに、統一支払インターフェイス (UPI) クイック応答 (QR) コードを生成してレシートに印刷する方法について説明します。
author: prabhatb2011
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: India
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 06224c265c2a1792f884874e1b39fae3cfd655a1
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462568"
---
# <a name="generate-qr-codes-and-print-them-on-receipts-for-india"></a>インド向け QR コードの生成とレシートへの印刷

[!include [banner](../includes/banner.md)]

このトピックでは、カスタマイズのガイドラインを示し、インド向けに、統一支払インターフェイス (UPI) クイック応答 (QR) コードを生成してレシートに印刷する方法について説明します。

## <a name="prerequisites"></a>必要条件

Commerce Runtime (CRT) で QR コードを生成する機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.13 で導入されました。 したがって、このトピックの情報はバージョン 10.0.13 以降でのみ有効です。

Commerce バージョン 10.0.17 以降では、Retail Hardware Station を使用したレシートへの QR コードの印刷がサポートされています。 10.0.16 以前のバージョンでは、QR コードは Modern POS (MPOS) からのみ印刷できます。

## <a name="data-schema-changes"></a>データ スキーマの変更

請求書の印刷は Dynamics 365 Commerce でサポートされていないため、販売時点管理 (POS) には UPI 関連のフィールドはありません。 したがって、フィールドをコードのカスタマイズのスコープ内に追加する必要があります。 **UPIId** および **UPIName** の 2 つの文字列フィールドを追加して、RetailStoreTenderTypeTable テーブルを拡張することをお勧めします。 このカスタマイズの一環として、**RetailStoreTenderTypeTable** を拡張して、ユーザー インターフェイス (UI) のフィールドを編集する必要があります。 また、チャネル データ スキーマを拡張し、ジョブをダウンロードする必要があります。 詳細については、[チャネル データベース拡張機能](../dev-itpro/channel-db-extensions.md)を参照してください。

## <a name="set-up-receipts-in-commerce-headquarters"></a>Commerce 本社でレシートを設定する

1. QR コードの新しいカスタム レシート フィールドに使用される新しい言語テキストを作成します。

    1. **Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **言語テキスト** に移動します。
    2. **POS** タブの **POS 言語テキスト** クイック タブで、**追加** を選択して言語テキストを作成します。
    3. **言語 ID** フィールドで、新しい言語テキストの言語を指定します (たとえば、米国英語の場合は **en-us**)。
    4. **テキスト ID** フィールドに、新しい言語テキストの識別子を入力します。
    5. **テキスト** フィールドに、新しい言語テキスト (たとえば、**税金請求書 QR コード**) を入力します。

       ![QR コード レシート フィールドの言語テキストの作成。](media/language-text-page.png)

2.  QR コードの新しいカスタム レシート フィールドを作成します。

    1. **Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **カスタム フィールド** に移動します。
    2. アクション ウィンドウで **新規** を選択して、フィールドを追加します。
    3. **名前** フィールドに、新しいフィールドの名前を入力します (たとえば、**TAXINVOICE_QR**)。
    4. **タイプ** フィールドで、**レシート** を選択します。
    5. **キャプション テキスト ID** フィールドに、以前に作成した言語テキストの **テキスト ID** 値を入力します。

        ![QR コードのレシート カスタム フィールドの作成。](media/custom-fields.png)

3.  QR コードのカスタム フィールドをレシートに追加します。

    1. **Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **レシートの形式** に移動します。
    2. QR コードを追加するレシートを選択します。
    3. アクション ウィンドウで、**デザイナー** を選択します。
    4. レシート デザイナーをダウンロードし、それを実行して、ログインします。
    5. レシートのヘッダーまたはフッターにカスタム フィールドを追加します。

4. 変更をチャネル データベースと同期します。

    1. **Retail と Commerce** > **Retail および Commerce IT** > **配送スケジュール** の順に移動します。
    2. ジョブ **1070** および **1090** を実行します。

## <a name="create-a-crt-extension-to-support-printing-qr-codes"></a>QR コードの印刷をサポートする CRT 拡張機能を作成する

QR コードの新しいカスタム レシート フィールドをサポートするには、URL 文字列を作成して QR コードを作成する CRT 拡張機能を作成する必要があります。 レシートにカスタム フィールドを追加する方法については、[Commerce Store レシートを拡張する](../dev-itpro/retail-sdk/retail-sdk-samples.md)を参照してください。

次の手順に従って、QR コードの新しいカスタム レシート フィールドを処理します。

1. Retail ソフトウェア開発キット (SDK) をインストールします。 詳細については、[Retail ソフトウェア開発キット (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。
2.  Retail SDK で、C\# プロジェクトを作成します。
3.  新しい C\# プロジェクトで、Commerce リリースごとに次のパッケージの参照を追加します。

# <a name="commerce-10024-and-before"></a>[Commerce 10 0 24 とそれ以前](#tab/commerce-10-0-24)

```C#
- Microsoft.Dynamics.Commerce.Runtime.DataModel.India
- Microsoft.Dynamics.Commerce.Runtime.DataServices
- Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting
- Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine
- Microsoft.Dynamics.Commerce.Runtime.Services.Messages
```

# <a name="commerce-10025"></a>[Commerce 10.0.25](#tab/commerce-10-0-25)

```C#
- Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting
- Microsoft.Dynamics.Commerce.Runtime.Services.Messages
- Microsoft.Dynamics.Commerce.Runtime.Localization.Data.Services.Messages
```

# <a name="commerce-10026-and-later"></a>[10.0.26 およびそれ以降の Commerce](#tab/commerce-10-0-26)

```C#
- Microsoft.Dynamics.Commerce.Runtime.Services.Messages
- Microsoft.Dynamics.Commerce.Runtime.Localization.Data.Services.Messages
- Microsoft.Dynamics.Commerce.Runtime.Localization.Services.Messages
```
    
---

4. 処理するクラスを作成します。 

    ```C#
    public class GetSalesTransactionCustomReceiptFieldService : IRequestHandlerAsync, ICountryRegionAware.
    {
        // Add code here.
    }
    ```
       
5. 新しいカスタム レシート フィールドを処理し、QR コードを文字列として返すハンドラー メソッドを実装します。

    ```C#
    /// <summary>
    /// Gets the custom receipt field value for sales receipt.
    /// </summary>
    /// <param name="request>The service request to get custom receipt field value.</param>
    /// <returns>The value of custom receipt field.</returns>
    private async Task<Response>
    GetCustomReceiptFieldForSalesTransactionReceiptsAsync(GetSalesTransactionCustomReceiptFieldServiceRequest
    request)
    {
      ThrowIf.Null(request.SalesOrder, "sales order");
      string receiptFieldName = request.CustomReceiptField;
      string receiptFieldValue = string.Empty;
      switch (receiptFieldName)
      {
          case "TAXINVOICE_QR":
            receiptFieldValue = await GetQRCode(request).ConfigureAwait(false);
            break;
          default:
            return new NotHandledResponse();
      }
      return new GetCustomReceiptFieldServiceResponse(receiptFieldValue);
    }
    ```

    ハンドラーには次の手順を含める必要があります。

    1. リクエスト パラメーターとして渡される販売注文 (**SalesOrder**) に基づいて UPI リンクを生成します。
    2. **EncodeQrCodeServiceRequest** を実行して QR コードを生成します。 (**EncodeQrCodeServiceRequest** は、**Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting** パッケージの一部です。)
    3. `<>` タグで返される QR コード文字列をラップします。

        ```C#
        var qrCodeRequest = new
            EncodeQrCodeServiceRequest(stringBuilder.ToString())
            {
              Width = 150, // Replace with desired QR code width
              Height = 150 // Replace with desired QR code width
            };

            EncodeQrCodeServiceResponse qrCodeDataResponse = await
            request.RequestContext.ExecuteAsync<EncodeQrCodeServiceResponse>(qrCodeRequest).ConfigureAwait(false);
            receiptFieldValue = $"<I:{qrCodeDataResponse.QRcode}>";
            return receiptFieldValue;
        ```  

6. **CommerceRuntime.Ext.config** に必要な拡張子を追加します。ここで、**Contoso.Commerce.Runtime.ReceiptsIndia** は QR コード アセンブリを印刷するための新しい拡張機能の名前です。

    ```xml 
    <commerceRuntimeExtensions>
          <composition>
            <!--
            Register your own assemblies or types here.
            The following example registers MyNewCrtService (and all its request handlers). 
            Any other services are not being overridden:
            <add source="type" value="Contoso.Commerce.Runtime.MyNewCrtService, Contoso.Commerce.Runtime.Services" />
            >add source="assembly" value="Contoso.Commerce.Runtime.Services" />
            -->
           <add source="assembly" value="Contoso.Commerce.Runtime.ReceiptsIndia" />
           <add source="assembly" 
       value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
           <add source="assembly" 
       value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
          </composition>
       </commerceRuntimeExtensions>
    ```
   
## <a name="printing-qr-code-images-on-opos-printers"></a>OPOS プリンターで QR コードのイメージを印刷する

OPOS プリンターを使用している場合、QR コードのイメージを *png* 形式から *bmp* 形式に変換する必要がある場合があります。 この変換の例を次に示します。

   ```C#
    ...
        var qrCodeRequest = new
            EncodeQrCodeServiceRequest(stringBuilder.ToString())
            {
              Width = 150, // Replace with desired QR code width
              Height = 150 // Replace with desired QR code width
            };

            EncodeQrCodeServiceResponse qrCodeDataResponse = await
            request.RequestContext.ExecuteAsync<EncodeQrCodeServiceResponse>(qrCodeRequest).ConfigureAwait(false);

            string qrCode = ConvertImagePNGToBMP(qrCodeDataResponse.QRcode);
            receiptFieldValue = $"<I:{qrCode}>";
            return receiptFieldValue;
    ...
    /// <summary>
    /// Converts an image from "png" to "bmp".
    /// </summary>
    /// <param name="qrCode">Base64 represents the image to convert.</param>
    /// <returns>The image as base64.</returns>
    private static string ConvertImagePNGToBMP(string qrCode)
    {
        string convertedQRCode = qrCode;

        byte[] imageBytes = Convert.FromBase64String(qrCode);
        using (MemoryStream msFrom = new MemoryStream(imageBytes))
        {
            var image = Image.FromStream(msFrom);
            using (MemoryStream msTo = new MemoryStream())
            {
                image.Save(msTo, ImageFormat.Bmp);
                convertedQRCode = Convert.ToBase64String(msTo.ToArray());
            }
        }

        return convertedQRCode;
    }
   ```

## <a name="samples-of-a-crt-extension-class-for-printing-qr-codes"></a>QR コードを印刷するための CRT 拡張クラスのサンプル

Commerce リリース別にグループ化された次のコード ブロックは、QR コードを印刷するための CRT 拡張クラスのサンプルを提供します。

# <a name="commerce-10024-and-before"></a>[Commerce 10 0 24 とそれ以前](#tab/commerce-10-0-24)

```C#
namespace Contoso
{
    namespace Commerce.Runtime.ReceiptsIndia
    {
        using System;
        using System.Collections.Generic;
        using System.Globalization;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        /// <summary>
        /// The extended service to get custom sales receipt field.
        /// </summary>
        public class GetSalesTransactionCustomReceiptFieldService : IRequestHandlerAsync, ICountryRegionAware
        {
            /// <summary>
            /// Gets the supported request types.
            /// </summary>  
            public IEnumerable<Type> SupportedRequestTypes
            {
              get
                {
                    return new[]
                    {
                        typeof(GetSalesTransactionCustomReceiptFieldServiceRequest),
                   };
                }
            }

            /// <summary>
            /// Gets a collection of companies supported by this request handler.
            /// </summary>
            public IEnumerable<string> SupportedCountryRegions
            {
                get
                {
                    return new[]
                    {
                        nameof(CountryRegionISOCode.IN),
                    };
                }
            }
            /// <summary>
            /// Executes the requests.
            /// </summary>
            /// <param name="request">The request parameter.</param>
            /// <returns>The GetReceiptServiceResponse that contains the formatted receipts.</returns>
            public async Task<Response> Execute(Request request)
            {
                ThrowIf.Null(request, nameof(request));
                Type requestedType = request.GetType();
                if (requestedType == typeof(GetSalesTransactionCustomReceiptFieldServiceRequest))
                {
                    return await
           this.GetCustomReceiptFieldForSalesTransactionReceiptsAsync((GetSalesTransactionCustomReceiptFieldServiceRequest)request).ConfigureAwait(false);
                }
                throw new NotSupportedException(string.Format("Request '{0}' is not supported.", request.GetType()));
                }
                /// <summary>
                /// Gets the custom receipt field value for sales receipt.
                /// </summary>
                /// <param name="request">The service request to get custom receipt field value.</param>
                /// <returns>The value of custom receipt field.<returns>
                private async Task<Response>
           GetCustomReceiptFieldForSalesTransactionReceiptsAsync(GetSalesTransactionCustomReceiptFieldServiceRequest request)
                {
                    ThrowIf.Null(request.SalesOrder, 
           $"{nameof(request)},{nameof(request.SalesOrder)}");
                    string receiptFieldName = request.CustomReceiptField;
                    string receiptFieldValue = string.Empty;
                    switch (receiptFieldName)
                    {
                        case "TAXINVOICE_QR":
                            receiptFieldValue = await 
           GetQRCode(request).ConfigureAwait(false);
                                   break;
                              default:
                                   return new NotHandledResponse();
                    }

                    return new GetCustomReceiptFieldServiceResponse(receiptFieldValue);
                }
                /// <summary>
                /// Gets the QR code for the receipt.
                /// </summary>
                /// <param name="request">The service request to get customreceipt field value.</param>
                /// <returns>QR code custom field value.</returns>
                private static async Task<string>
        GetQRCode(GetSalesTransactionCustomReceiptFieldServiceRequest request)
                {
                    var salesOrder = request.SalesOrder;
                    string receiptFieldValue = string.Empty;
                    bool isB2C = await IsB2CTransactionAsync(request.RequestContext, salesOrder).ConfigureAwait(false);
                    if (isB2C)
                    {
                        string gstNumber = await GetStoreGSTIN(request.RequestContext).ConfigureAwait(false);
                        var paymentInfo = await GetPaymentUPIInfo(request.RequestContext, salesOrder).ConfigureAwait(false);
                        string totalAmount = FormatAmount(salesOrder.TotalAmount);
                        string igstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                        "IGST"));
                        string cgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                        "CGST"));
                        string sgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                        "SGST"));
                        string cessAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                        "CESS"));
                        StringBuilder stringBuilder = new
               StringBuilder($"upi://pay?cu={salesOrder.CurrencyCode}");
                        stringBuilder.Append($"&am={totalAmount}");
                        stringBuilder.Append($"&pa={paymentInfo.Item1}");
                        stringBuilder.Append($"&pn={paymentInfo.Item2}");
                        stringBuilder.Append($"&tr={salesOrder.ReceiptId}");
               stringBuilder.Append($"&dt={salesOrder.TransactionDateTime.ToString("dd/MM/yyyy")}");                    
                        stringBuilder.Append($"&no={gstNumber}");
                        stringBuilder.Append($"&IgstAmt = {igstAmt}");
                        stringBuilder.Append($"&CgstAmt = {cgstAmt}");
                        stringBuilder.Append($"&SgstAmt = {sgstAmt}");
                        stringBuilder.Append($"&CesAmt = {cessAmt}");
                        var qrCodeRequest = new
               EncodeQrCodeServiceRequest(stringBuilder.ToString())
                        {
                            Width = 150, // Replace with desired QR code width
                            Height = 150 // Replace with desired QR code width
                        };
               EncodeQrCodeServiceResponse qrCodeDataResponse = await
               request.RequestContext.ExecuteAsync<EncodeQrCodeServiceResponse>(qrCodeRequest).ConfigureAwait(false);
                        receiptFieldValue = $"<I:{qrCodeDataResponse.QRcode}>";
                    }
                    return receiptFieldValue;
                }

                /// <summary>
                /// Gets store GSTIN.
                /// </summary>
                /// <param name="requestContext">Request context.</param>
                /// <returns>Store GSTIN.</returns>
                private static async Task<string> GetStoreGSTIN(RequestContext
                requestContext)
                {
                    var dataRequest = new GetReceiptHeaderGteTaxInfoIndiaDataRequest
                    {
                        QueryResultSettings = QueryResultSettings.SingleRecord,
                    };
                    var headerTaxInformation = await
          requestContext.ExecuteAsync<SingleEntityDataServiceResponse<ReceiptHeaderGteTaxInfoIndia>>(dataRequest).ConfigureAwait(false);
                    return headerTaxInformation.Entity?.GstRegistrationNumber;
                }

                /// <summary>
                /// Gets payment UPI info for the sales order.
                /// </summary>
                /// <param name="requestContext">Request context.</param>
                /// <param name="salesOrder">Sales order.</param>
                /// <returns>Payment info.</returns>
                private static async Task<Tuple<string, string>>
          GetPaymentUPIInfo(RequestContext requestContext, SalesOrder salesOrder)
                {
                    var channelTenderDataRequest = new
          GetChannelTenderTypesDataRequest(requestContext.GetPrincipal().ChannelId,
          QueryResultSettings.AllRecords);
                    var channelTenderTypes = (await
          requestContext.Runtime.ExecuteAsync<EntityDataServiceResponse<TenderType>>(channelTenderDataRequest,
          requestContext).ConfigureAwait(false)).PagedEntityCollection.Results;
                    string upiId = string.Empty;
                    string upiName = string.Empty;
                    int count = salesOrder.ActiveTenderLines.Count;
                    foreach (var tenderLine in salesOrder.ActiveTenderLines)
                    {
                        TenderType tenderType = channelTenderTypes.Where(type =>
                    type.TenderTypeId == tenderLine.TenderTypeId).SingleOrDefault();
                        if (tenderType == null)
                        {
                            continue;
                        }
                        if (!string.IsNullOrEmpty(upiId))
                        {
                            upiId += ",";
                        }
                        if (!string.IsNullOrEmpty(upiName))
                        {
                            upiName += ",";
                        }
                        upiId += tenderType.TenderTypeId; // Here should be customized field UPIId
                        upiName += tenderType.Name; // Here should be customized field UPIName
                        if (count > 1)
                        {
                            string amount = FormatAmount(tenderLine.Amount);
                            upiId += $":{amount}";
                            upiName += $":{amount}";
                        }
                    }
                    return new Tuple<string, string>(upiId, upiName);
                }

                /// <summary>
                /// Gets tax component amount.
                /// </summary>
                /// <param name="salesOrder">Sales order.</param>
                /// <param name="taxComponent">Tax component.</param>
                /// <returns>Tax component amount.</returns>
                private static decimal GetTaxComponentAmount(SalesOrder salesOrder, string taxComponent)
                {
                    decimal taxAmount = 0m;
                    IEnumerable<TaxLineGTE> taxLineGte = 
                salesOrder.ActiveSalesLines.SelectMany(x => x.TaxLines).OfType<TaxLineGTE>();
                    var groups = taxLineGte.GroupBy(x => new { x.TaxComponent }).OrderBy(x =>
                x.Key.TaxComponent);
                    var group = groups.Where(g => string.Equals(g.Key.TaxComponent, 
                taxComponent, StringComparison.InvariantCultureIgnoreCase)).FirstOrDefault();
                    if (group != null)
                    {
                        taxAmount = group.Sum(l => l.Amount);
                    }
                    return taxAmount;
                }

                /// <summary>
                /// Gets the store customer account number based on store type.
                /// </summary>
                /// <returns>The store customer account number.</returns>
                internal static string
            GetStoreCustomerAccountNumberFromChannelProperties(RequestContext requestContext)
                {
                    if (requestContext.GetChannelConfiguration().IsOnlineStore())
                    {
                        if (requestContext.GetPrincipal().IsCustomer)
                        {
                            return requestContext.GetPrincipal().UserId;
                        }
                    }
                    return requestContext.GetChannel().DefaultCustomerAccount;
                }

                ///<summary>
                /// Defines whether the customer is store default customer.
                /// </summary>
                /// <param name="requestContext">Request context.</param>
                /// <param name="customerId">Customer id.</param>
                /// <returns>rue if the customer is store default customer; false otherwise.</returns>
                private static bool IsStoreCustomer(RequestContext requestContext, string customerId)
                {
                    return string.IsNullOrEmpty(customerId)
                        || string.Equals(customerId,
            GetStoreCustomerAccountNumberFromChannelProperties(requestContext),
            StringComparison.InvariantCultureIgnoreCase);
                }
                /// <summary>
                /// Defines whether the transaction is B2C.
                /// </summary>
                /// <param name="requestContext">Request context.</param>
                /// <param name="salesOrder">Sales order.</param>
                /// <returns>True if the transaction is B2C; false otherwise.</returns>
                private static async Task<bool> IsB2CTransactionAsync(RequestContext requestContext, SalesOrder salesOrder)
                {
                    if (IsStoreCustomer(requestContext, salesOrder.CustomerId))
                    {
                        return true;
                    }
                    var customer = await GetCustomerAsync(requestContext, salesOrder.CustomerId).ConfigureAwait(false);
                    if (customer == null)
                    {
                        return true;
                    }
                    var address = customer.GetPrimaryAddress();
                    if (address == null)
                    {
                        return true;
                    }
                    GetPrimaryAddressTaxInformationDataRequest
            getPrimaryAddressTaxInformationDataRequest = new
            GetPrimaryAddressTaxInformationDataRequest(address.LogisticsLocationRecordId);
                    AddressTaxInformationIndia addressTaxInformationIndia = (await
            requestContext.Runtime.ExecuteAsync
            <SingleEntityDataServiceResponse<AddressTaxInformationIndia>>(getPrimaryAddressTaxInformationDataRequest,
            requestContext)
                        .ConfigureAwait(false)).Entity;
                    if (addressTaxInformationIndia == null ||
            addressTaxInformationIndia.GstinRegistrationNumber == null
                            ||
            string.IsNullOrEmpty(addressTaxInformationIndia.GstinRegistrationNumber.RegistrationNumber))
                    {
                        return true;
                    }
                    return false;
                }

                /// <summary>
                /// Gets customer by customer identifier.
                /// </summary>
                /// <param name="customerId">Customer identifier.</param>
                /// <returns>Customer object.</returns>
                private static async Task<Customer> GetCustomerAsync(RequestContext requestContext, string customerId)
                {
                    Customer customer = null;
                    if (!string.IsNullOrWhiteSpace(customerId))
                    {
                        var getCustomerDataRequest = new GetCustomerDataRequest(customerId);
                        SingleEntityDataServiceResponse<Customer> getCustomerDataResponse = await
                requestContext.ExecuteAsync<SingleEntityDataServiceResponse<Customer>>(getCustomerDataRequest).ConfigureAwait(false);
                        customer = getCustomerDataResponse.Entity;
                    }
                    return customer;
                }

                /// <summary>
                /// Formats amount.
                /// </summary>
                /// <param name="amount">Amount to format.</param>
                /// <returns>Formatted amount.</returns>
                private static string FormatAmount(decimal amount)
                {
                    return amount.ToString("0.00", CultureInfo.InvariantCulture);
                }
            }
        }
    }
```     

# <a name="commerce-10025"></a>[Commerce 10.0.25](#tab/commerce-10-0-25)

```C#
namespace Contoso
{
    namespace Commerce.Runtime.ReceiptsIndia
    {
        using System;
        using System.Collections.Generic;
        using System.Globalization;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Localization.Data.Services.Messages.India;
        using Microsoft.Dynamics.Commerce.Runtime.Localization.Entities.India;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        /// <summary>
        /// The extended service to get custom sales receipt field.
        /// </summary>
        public class GetSalesTransactionCustomReceiptFieldService : IRequestHandlerAsync, ICountryRegionAware
        {
            /// <summary>
            /// Gets the supported request types.
            /// </summary>  
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[]
                    {
                       typeof(GetSalesTransactionCustomReceiptFieldServiceRequest),
                    };
                }
            }

            /// <summary>
            /// Gets a collection of companies supported by this request handler.
            /// </summary>
            public IEnumerable<string> SupportedCountryRegions
            {
                get
                {
                    return new[]
                    {
                       nameof(CountryRegionISOCode.IN),
                    };
                }
            }

            /// <summary>
            /// Executes the requests.
            /// </summary>
            /// <param name="request">The request parameter.</param>
            /// <returns>The GetReceiptServiceResponse that contains the formatted receipts.</returns>
            public async Task<Response> Execute(Request request)
            {
                ThrowIf.Null(request, nameof(request));
                Type requestedType = request.GetType();
                if (requestedType == typeof(GetSalesTransactionCustomReceiptFieldServiceRequest))
                {
                    return await this.GetCustomReceiptFieldForSalesTransactionReceiptsAsync((GetSalesTransactionCustomReceiptFieldServiceRequest)request).ConfigureAwait(false);
                }
                throw new NotSupportedException(string.Format("Request '{0}' is not supported.", request.GetType()));
            }

            /// <summary>
            /// Gets the custom receipt field value for sales receipt.
            /// </summary>
            /// <param name="request">The service request to get custom receipt field value.</param>
            /// <returns>The value of custom receipt field.<returns>
            private async Task<Response> GetCustomReceiptFieldForSalesTransactionReceiptsAsync(GetSalesTransactionCustomReceiptFieldServiceRequest request)
            {
                ThrowIf.Null(request.SalesOrder, $"{nameof(request)},{nameof(request.SalesOrder)}");
                string receiptFieldName = request.CustomReceiptField;
                string receiptFieldValue = string.Empty;
                switch (receiptFieldName)
                {
                    case "TAXINVOICE_QR":
                        receiptFieldValue = await GetQRCode(request).ConfigureAwait(false);
                        break;
                    default:
                        return new NotHandledResponse();
                }

                return new GetCustomReceiptFieldServiceResponse(receiptFieldValue);
            }

            /// <summary>
            /// Gets the QR code for the receipt.
            /// </summary>
            /// <param name="request">The service request to get customreceipt field value.</param>
            /// <returns>QR code custom field value.</returns>
            private static async Task<string> GetQRCode(GetSalesTransactionCustomReceiptFieldServiceRequest request)
            {
                var salesOrder = request.SalesOrder;
                string receiptFieldValue = string.Empty;
                bool isB2C = await IsB2CTransactionAsync(request.RequestContext, salesOrder).ConfigureAwait(false);
                if (isB2C)
                {
                    string gstNumber = await GetStoreGSTIN(request.RequestContext).ConfigureAwait(false);
                    var paymentInfo = await GetPaymentUPIInfo(request.RequestContext, salesOrder).ConfigureAwait(false);
                    string totalAmount = FormatAmount(salesOrder.TotalAmount);
                    string igstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "IGST"));
                    string cgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "CGST"));
                    string sgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "SGST"));
                    string cessAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "CESS"));
                    StringBuilder stringBuilder = new StringBuilder($"upi://pay?cu={salesOrder.CurrencyCode}");
                    stringBuilder.Append($"&am={totalAmount}");
                    stringBuilder.Append($"&pa={paymentInfo.Item1}");
                    stringBuilder.Append($"&pn={paymentInfo.Item2}");
                    stringBuilder.Append($"&tr={salesOrder.ReceiptId}");
                    stringBuilder.Append($"&dt={salesOrder.TransactionDateTime.ToString("dd/MM/yyyy")}");
                    stringBuilder.Append($"&no={gstNumber}");
                    stringBuilder.Append($"&IgstAmt = {igstAmt}");
                    stringBuilder.Append($"&CgstAmt = {cgstAmt}");
                    stringBuilder.Append($"&SgstAmt = {sgstAmt}");
                    stringBuilder.Append($"&CesAmt = {cessAmt}");
                    var qrCodeRequest = new EncodeQrCodeServiceRequest(stringBuilder.ToString())
                    {
                        Width = 150, // Replace with desired QR code width
                        Height = 150 // Replace with desired QR code width
                    };
                    EncodeQrCodeServiceResponse qrCodeDataResponse = await
                    request.RequestContext.ExecuteAsync<EncodeQrCodeServiceResponse>(qrCodeRequest).ConfigureAwait(false);
                    receiptFieldValue = $"<L:{qrCodeDataResponse.QRcode}>";
                }
                return receiptFieldValue;
            }

            /// <summary>
            /// Gets store GSTIN.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <returns>Store GSTIN.</returns>
            private static async Task<string> GetStoreGSTIN(RequestContext requestContext)
            {
                var dataRequest = new GetReceiptHeaderTaxInformationDataRequest
                {
                    QueryResultSettings = QueryResultSettings.SingleRecord,
                };
                var headerTaxInformation = await requestContext.ExecuteAsync<SingleEntityDataServiceResponse<ReceiptHeaderTaxInformation>>(dataRequest).ConfigureAwait(false);
                return headerTaxInformation.Entity?.GstRegistrationNumber;
            }

            /// <summary>
            /// Gets payment UPI info for the sales order.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="salesOrder">Sales order.</param>
            /// <returns>Payment info.</returns>
            private static async Task<Tuple<string, string>> GetPaymentUPIInfo(RequestContext requestContext, SalesOrder salesOrder)
            {
                var channelTenderDataRequest = new GetChannelTenderTypesDataRequest(requestContext.GetPrincipal().ChannelId, QueryResultSettings.AllRecords);
                var channelTenderTypes = (await requestContext.Runtime.ExecuteAsync<EntityDataServiceResponse<TenderType>>(channelTenderDataRequest, requestContext).ConfigureAwait(false)).PagedEntityCollection.Results;
                string upiId = string.Empty;
                string upiName = string.Empty;
                int count = salesOrder.ActiveTenderLines.Count;
                foreach (var tenderLine in salesOrder.ActiveTenderLines)
                {
                    TenderType tenderType = channelTenderTypes.Where(type => type.TenderTypeId == tenderLine.TenderTypeId).SingleOrDefault();
                    if (tenderType == null)
                    {
                        continue;
                    }
                    if (!string.IsNullOrEmpty(upiId))
                    {
                        upiId += ",";
                    }
                    if (!string.IsNullOrEmpty(upiName))
                    {
                        upiName += ",";
                    }
                    upiId += tenderType.TenderTypeId; // Here should be customized field UPIId
                    upiName += tenderType.Name; // Here should be customized field UPIName
                    if (count > 1)
                    {
                        string amount = FormatAmount(tenderLine.Amount);
                        upiId += $":{amount}";
                        upiName += $":{amount}";
                    }
                }
                return new Tuple<string, string>(upiId, upiName);
            }

            /// <summary>
            /// Gets tax component amount.
            /// </summary>
            /// <param name="salesOrder">Sales order.</param>
            /// <param name="taxComponent">Tax component.</param>
            /// <returns>Tax component amount.</returns>
            private static decimal GetTaxComponentAmount(SalesOrder salesOrder, string taxComponent)
            {
                decimal taxAmount = 0m;
                IEnumerable<TaxLineGTE> taxLineGte = salesOrder.ActiveSalesLines.SelectMany(x => x.TaxLines).OfType<TaxLineGTE>();
                var groups = taxLineGte.GroupBy(x => new { x.TaxComponent }).OrderBy(x => x.Key.TaxComponent);
                var group = groups.Where(g => string.Equals(g.Key.TaxComponent, taxComponent, StringComparison.InvariantCultureIgnoreCase)).FirstOrDefault();
                if (group != null)
                {
                    taxAmount = group.Sum(l => l.Amount);
                }
                return taxAmount;
            }

            /// <summary>
            /// Gets the store customer account number based on store type.
            /// </summary>
            /// <returns>The store customer account number.</returns>
            internal static string GetStoreCustomerAccountNumberFromChannelProperties(RequestContext requestContext)
            {
                if (requestContext.GetChannelConfiguration().IsOnlineStore())
                {
                    if (requestContext.GetPrincipal().IsCustomer)
                    {
                        return requestContext.GetPrincipal().UserId;
                    }
                }
                return requestContext.GetChannel().DefaultCustomerAccount;
            }

            ///<summary>
            /// Defines whether the customer is store default customer.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="customerId">Customer id.</param>
            /// <returns>rue if the customer is store default customer; false otherwise.</returns>
            private static bool IsStoreCustomer(RequestContext requestContext, string customerId)
            {
                return string.IsNullOrEmpty(customerId)
                    || string.Equals(customerId, GetStoreCustomerAccountNumberFromChannelProperties(requestContext), StringComparison.InvariantCultureIgnoreCase);
            }

            /// <summary>
            /// Defines whether the transaction is B2C.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="salesOrder">Sales order.</param>
            /// <returns>True if the transaction is B2C; false otherwise.</returns>
            private static async Task<bool> IsB2CTransactionAsync(RequestContext requestContext, SalesOrder salesOrder)
            {
                if (IsStoreCustomer(requestContext, salesOrder.CustomerId))
                {
                    return true;
                }
                var customer = await GetCustomerAsync(requestContext, salesOrder.CustomerId).ConfigureAwait(false);
                if (customer == null)
                {
                    return true;
                }
                var address = customer.GetPrimaryAddress();
                if (address == null)
                {
                    return true;
                }
                GetPrimaryAddressTaxInformationDataRequest getPrimaryAddressTaxInformationDataRequest = new GetPrimaryAddressTaxInformationDataRequest(address.LogisticsLocationRecordId);
                AddressTaxInformationIndia addressTaxInformationIndia = (await requestContext.Runtime.ExecuteAsync<SingleEntityDataServiceResponse<AddressTaxInformationIndia>>(getPrimaryAddressTaxInformationDataRequest, requestContext).ConfigureAwait(false)).Entity;
                if (addressTaxInformationIndia == null
                    || addressTaxInformationIndia.GstinRegistrationNumber == null
                    || string.IsNullOrEmpty(addressTaxInformationIndia.GstinRegistrationNumber.RegistrationNumber))
                {
                    return true;
                }
                return false;
            }

            /// <summary>
            /// Gets customer by customer identifier.
            /// </summary>
            /// <param name="customerId">Customer identifier.</param>
            /// <returns>Customer object.</returns>
            private static async Task<Customer> GetCustomerAsync(RequestContext requestContext, string customerId)
            {
                Customer customer = null;
                if (!string.IsNullOrWhiteSpace(customerId))
                {
                    var getCustomerDataRequest = new GetCustomerDataRequest(customerId);
                    SingleEntityDataServiceResponse<Customer> getCustomerDataResponse = await requestContext.ExecuteAsync<SingleEntityDataServiceResponse<Customer>>(getCustomerDataRequest).ConfigureAwait(false);
                    customer = getCustomerDataResponse.Entity;
                }
                return customer;
            }

            /// <summary>
            /// Formats amount.
            /// </summary>
            /// <param name="amount">Amount to format.</param>
            /// <returns>Formatted amount.</returns>
            private static string FormatAmount(decimal amount)
            {
                return amount.ToString("0.00", CultureInfo.InvariantCulture);
            }
        }
    }
}
```   

# <a name="commerce-10026-and-later"></a>[10.0.26 およびそれ以降の Commerce](#tab/commerce-10-0-26)

```C#
namespace Contoso
{
    namespace Commerce.Runtime.ReceiptsIndia
    {
        using System;
        using System.Collections.Generic;
        using System.Globalization;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Localization.Data.Services.Messages.India;
        using Microsoft.Dynamics.Commerce.Runtime.Localization.Entities.India;
        using Microsoft.Dynamics.Commerce.Runtime.Localization.Services.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        /// <summary>
        /// The extended service to get custom sales receipt field.
        /// </summary>
        public class GetSalesTransactionCustomReceiptFieldService : IRequestHandlerAsync, ICountryRegionAware
        {
            /// <summary>
            /// Gets the supported request types.
            /// </summary>  
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[]
                    {
                       typeof(GetSalesTransactionCustomReceiptFieldServiceRequest),
                    };
                }
            }

            /// <summary>
            /// Gets a collection of companies supported by this request handler.
            /// </summary>
            public IEnumerable<string> SupportedCountryRegions
            {
                get
                {
                    return new[]
                    {
                       nameof(CountryRegionISOCode.IN),
                    };
                }
            }

            /// <summary>
            /// Executes the requests.
            /// </summary>
            /// <param name="request">The request parameter.</param>
            /// <returns>The GetReceiptServiceResponse that contains the formatted receipts.</returns>
            public async Task<Response> Execute(Request request)
            {
                ThrowIf.Null(request, nameof(request));
                Type requestedType = request.GetType();
                if (requestedType == typeof(GetSalesTransactionCustomReceiptFieldServiceRequest))
                {
                    return await this.GetCustomReceiptFieldForSalesTransactionReceiptsAsync((GetSalesTransactionCustomReceiptFieldServiceRequest)request).ConfigureAwait(false);
                }
                throw new NotSupportedException(string.Format("Request '{0}' is not supported.", request.GetType()));
            }

            /// <summary>
            /// Gets the custom receipt field value for sales receipt.
            /// </summary>
            /// <param name="request">The service request to get custom receipt field value.</param>
            /// <returns>The value of custom receipt field.<returns>
            private async Task<Response> GetCustomReceiptFieldForSalesTransactionReceiptsAsync(GetSalesTransactionCustomReceiptFieldServiceRequest request)
            {
                ThrowIf.Null(request.SalesOrder, $"{nameof(request)},{nameof(request.SalesOrder)}");
                string receiptFieldName = request.CustomReceiptField;
                string receiptFieldValue = string.Empty;
                switch (receiptFieldName)
                {
                    case "TAXINVOICE_QR":
                        receiptFieldValue = await GetQRCode(request).ConfigureAwait(false);
                        break;
                    default:
                        return new NotHandledResponse();
                }

                return new GetCustomReceiptFieldServiceResponse(receiptFieldValue);
            }

            /// <summary>
            /// Gets the QR code for the receipt.
            /// </summary>
            /// <param name="request">The service request to get customreceipt field value.</param>
            /// <returns>QR code custom field value.</returns>
            private static async Task<string> GetQRCode(GetSalesTransactionCustomReceiptFieldServiceRequest request)
            {
                var salesOrder = request.SalesOrder;
                string receiptFieldValue = string.Empty;
                bool isB2C = await IsB2CTransactionAsync(request.RequestContext, salesOrder).ConfigureAwait(false);
                if (isB2C)
                {
                    string gstNumber = await GetStoreGSTIN(request.RequestContext).ConfigureAwait(false);
                    var paymentInfo = await GetPaymentUPIInfo(request.RequestContext, salesOrder).ConfigureAwait(false);
                    string totalAmount = FormatAmount(salesOrder.TotalAmount);
                    string igstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "IGST"));
                    string cgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "CGST"));
                    string sgstAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "SGST"));
                    string cessAmt = FormatAmount(GetTaxComponentAmount(salesOrder,
                    "CESS"));
                    StringBuilder stringBuilder = new StringBuilder($"upi://pay?cu={salesOrder.CurrencyCode}");
                    stringBuilder.Append($"&am={totalAmount}");
                    stringBuilder.Append($"&pa={paymentInfo.Item1}");
                    stringBuilder.Append($"&pn={paymentInfo.Item2}");
                    stringBuilder.Append($"&tr={salesOrder.ReceiptId}");
                    stringBuilder.Append($"&dt={salesOrder.TransactionDateTime.ToString("dd/MM/yyyy")}");
                    stringBuilder.Append($"&no={gstNumber}");
                    stringBuilder.Append($"&IgstAmt = {igstAmt}");
                    stringBuilder.Append($"&CgstAmt = {cgstAmt}");
                    stringBuilder.Append($"&SgstAmt = {sgstAmt}");
                    stringBuilder.Append($"&CesAmt = {cessAmt}");
                    var qrCodeRequest = new EncodeQrCodeServiceRequest(stringBuilder.ToString())
                    {
                        Width = 150, // Replace with desired QR code width
                        Height = 150 // Replace with desired QR code width
                    };
                    EncodeQrCodeServiceResponse qrCodeDataResponse = await
                    request.RequestContext.ExecuteAsync<EncodeQrCodeServiceResponse>(qrCodeRequest).ConfigureAwait(false);
                    receiptFieldValue = $"<L:{qrCodeDataResponse.QRCode}>";
                }
                return receiptFieldValue;
            }

            /// <summary>
            /// Gets store GSTIN.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <returns>Store GSTIN.</returns>
            private static async Task<string> GetStoreGSTIN(RequestContext requestContext)
            {
                var dataRequest = new GetReceiptHeaderTaxInformationDataRequest
                {
                    QueryResultSettings = QueryResultSettings.SingleRecord,
                };
                var headerTaxInformation = await requestContext.ExecuteAsync<SingleEntityDataServiceResponse<ReceiptHeaderTaxInformation>>(dataRequest).ConfigureAwait(false);
                return headerTaxInformation.Entity?.GstRegistrationNumber;
            }

            /// <summary>
            /// Gets payment UPI info for the sales order.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="salesOrder">Sales order.</param>
            /// <returns>Payment info.</returns>
            private static async Task<Tuple<string, string>> GetPaymentUPIInfo(RequestContext requestContext, SalesOrder salesOrder)
            {
                var channelTenderDataRequest = new GetChannelTenderTypesDataRequest(requestContext.GetPrincipal().ChannelId, QueryResultSettings.AllRecords);
                var channelTenderTypes = (await requestContext.Runtime.ExecuteAsync<EntityDataServiceResponse<TenderType>>(channelTenderDataRequest, requestContext).ConfigureAwait(false)).PagedEntityCollection.Results;
                string upiId = string.Empty;
                string upiName = string.Empty;
                int count = salesOrder.ActiveTenderLines.Count;
                foreach (var tenderLine in salesOrder.ActiveTenderLines)
                {
                    TenderType tenderType = channelTenderTypes.Where(type => type.TenderTypeId == tenderLine.TenderTypeId).SingleOrDefault();
                    if (tenderType == null)
                    {
                        continue;
                    }
                    if (!string.IsNullOrEmpty(upiId))
                    {
                        upiId += ",";
                    }
                    if (!string.IsNullOrEmpty(upiName))
                    {
                        upiName += ",";
                    }
                    upiId += tenderType.TenderTypeId; // Here should be customized field UPIId
                    upiName += tenderType.Name; // Here should be customized field UPIName
                    if (count > 1)
                    {
                        string amount = FormatAmount(tenderLine.Amount);
                        upiId += $":{amount}";
                        upiName += $":{amount}";
                    }
                }
                return new Tuple<string, string>(upiId, upiName);
            }

            /// <summary>
            /// Gets tax component amount.
            /// </summary>
            /// <param name="salesOrder">Sales order.</param>
            /// <param name="taxComponent">Tax component.</param>
            /// <returns>Tax component amount.</returns>
            private static decimal GetTaxComponentAmount(SalesOrder salesOrder, string taxComponent)
            {
                decimal taxAmount = 0m;
                IEnumerable<TaxLineGTE> taxLineGte = salesOrder.ActiveSalesLines.SelectMany(x => x.TaxLines).OfType<TaxLineGTE>();
                var groups = taxLineGte.GroupBy(x => new { x.TaxComponent }).OrderBy(x => x.Key.TaxComponent);
                var group = groups.Where(g => string.Equals(g.Key.TaxComponent, taxComponent, StringComparison.InvariantCultureIgnoreCase)).FirstOrDefault();
                if (group != null)
                {
                    taxAmount = group.Sum(l => l.Amount);
                }
                return taxAmount;
            }

            /// <summary>
            /// Gets the store customer account number based on store type.
            /// </summary>
            /// <returns>The store customer account number.</returns>
            internal static string GetStoreCustomerAccountNumberFromChannelProperties(RequestContext requestContext)
            {
                if (requestContext.GetChannelConfiguration().IsOnlineStore())
                {
                    if (requestContext.GetPrincipal().IsCustomer)
                    {
                        return requestContext.GetPrincipal().UserId;
                    }
                }
                return requestContext.GetChannel().DefaultCustomerAccount;
            }

            ///<summary>
            /// Defines whether the customer is store default customer.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="customerId">Customer id.</param>
            /// <returns>rue if the customer is store default customer; false otherwise.</returns>
            private static bool IsStoreCustomer(RequestContext requestContext, string customerId)
            {
                return string.IsNullOrEmpty(customerId)
                    || string.Equals(customerId, GetStoreCustomerAccountNumberFromChannelProperties(requestContext), StringComparison.InvariantCultureIgnoreCase);
            }

            /// <summary>
            /// Defines whether the transaction is B2C.
            /// </summary>
            /// <param name="requestContext">Request context.</param>
            /// <param name="salesOrder">Sales order.</param>
            /// <returns>True if the transaction is B2C; false otherwise.</returns>
            private static async Task<bool> IsB2CTransactionAsync(RequestContext requestContext, SalesOrder salesOrder)
            {
                if (IsStoreCustomer(requestContext, salesOrder.CustomerId))
                {
                    return true;
                }
                var customer = await GetCustomerAsync(requestContext, salesOrder.CustomerId).ConfigureAwait(false);
                if (customer == null)
                {
                    return true;
                }
                var address = customer.GetPrimaryAddress();
                if (address == null)
                {
                    return true;
                }
                GetPrimaryAddressTaxInformationDataRequest getPrimaryAddressTaxInformationDataRequest = new GetPrimaryAddressTaxInformationDataRequest(address.LogisticsLocationRecordId);
                AddressTaxInformationIndia addressTaxInformationIndia = (await requestContext.Runtime.ExecuteAsync<SingleEntityDataServiceResponse<AddressTaxInformationIndia>>(getPrimaryAddressTaxInformationDataRequest, requestContext).ConfigureAwait(false)).Entity;
                if (addressTaxInformationIndia == null
                    || addressTaxInformationIndia.GstinRegistrationNumber == null
                    || string.IsNullOrEmpty(addressTaxInformationIndia.GstinRegistrationNumber.RegistrationNumber))
                {
                    return true;
                }
                return false;
            }

            /// <summary>
            /// Gets customer by customer identifier.
            /// </summary>
            /// <param name="customerId">Customer identifier.</param>
            /// <returns>Customer object.</returns>
            private static async Task<Customer> GetCustomerAsync(RequestContext requestContext, string customerId)
            {
                Customer customer = null;
                if (!string.IsNullOrWhiteSpace(customerId))
                {
                    var getCustomerDataRequest = new GetCustomerDataRequest(customerId);
                    SingleEntityDataServiceResponse<Customer> getCustomerDataResponse = await requestContext.ExecuteAsync<SingleEntityDataServiceResponse<Customer>>(getCustomerDataRequest).ConfigureAwait(false);
                    customer = getCustomerDataResponse.Entity;
                }
                return customer;
            }

            /// <summary>
            /// Formats amount.
            /// </summary>
            /// <param name="amount">Amount to format.</param>
            /// <returns>Formatted amount.</returns>
            private static string FormatAmount(decimal amount)
            {
                return amount.ToString("0.00", CultureInfo.InvariantCulture);
            }
        }
    }
}
```     

---
