---
title: QR コードの生成とレシートへの印刷
description: このトピックでは、統一支払インターフェイス (UPI) クイック応答 (QR) コードを生成してレシートに印刷する方法について説明します。
author: prabhatb2011
ms.date: 03/14/2021
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
ms.openlocfilehash: fd938f76a31c329aa4aa2f1000f9a59624ec7d1b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021867"
---
# <a name="generate-qr-codes-and-print-them-on-receipts"></a><span data-ttu-id="ce8a6-103">QR コードの生成とレシートへの印刷</span><span class="sxs-lookup"><span data-stu-id="ce8a6-103">Generate QR codes and print them on receipts</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="ce8a6-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="ce8a6-104">Prerequisites</span></span>

<span data-ttu-id="ce8a6-105">Commerce Runtime (CRT) で QR コードを生成する機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.13 で導入されました。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-105">Functionality for generating QR codes in the Commerce runtime (CRT) was introduced in Microsoft Dynamics 365 Commerce version 10.0.13.</span></span> <span data-ttu-id="ce8a6-106">したがって、このトピックの情報はバージョン 10.0.13 以降でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-106">Therefore, the information in this topic is valid only for version 10.0.13 and later.</span></span>

<span data-ttu-id="ce8a6-107">Commerce バージョン 10.0.17 以降では、Retail Hardware Station を使用したレシートへの QR コードの印刷がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-107">Commerce versions 10.0.17 and later support printing QR codes on receipts using Retail Hardware Station.</span></span> <span data-ttu-id="ce8a6-108">10.0.16 以前のバージョンでは、QR コードは Modern POS (MPOS) からのみ印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-108">In versions 10.0.16 and earlier, QR codes can only be printed from Modern POS (MPOS).</span></span>

## <a name="data-schema-changes"></a><span data-ttu-id="ce8a6-109">データ スキーマの変更</span><span class="sxs-lookup"><span data-stu-id="ce8a6-109">Data schema changes</span></span>

<span data-ttu-id="ce8a6-110">請求書の印刷は Dynamics 365 Commerce でサポートされていないため、販売時点管理 (POS) には UPI 関連のフィールドはありません。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-110">Because invoice printing isn't supported in Dynamics 365 Commerce, there are no UPI-related fields in Point of sale (POS).</span></span> <span data-ttu-id="ce8a6-111">したがって、フィールドをコードのカスタマイズのスコープ内に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-111">Therefore, the fields should be added in the scope of code customization.</span></span> <span data-ttu-id="ce8a6-112">**UPIId** および **UPIName** の 2 つの文字列フィールドを追加して、RetailStoreTenderTypeTable テーブルを拡張することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-112">We recommend that you extend the RetailStoreTenderTypeTable table by adding two string fields: **UPIId** and **UPIName**.</span></span> <span data-ttu-id="ce8a6-113">このカスタマイズの一環として、**RetailStoreTenderTypeTable** を拡張して、ユーザー インターフェイス (UI) のフィールドを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-113">As part of this customization, you should extend the **RetailStoreTenderTypeTable** form to edit the fields in the user interface (UI).</span></span> <span data-ttu-id="ce8a6-114">また、チャネル データ スキーマを拡張し、ジョブをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-114">You should also extend the channel data schema and download jobs.</span></span> <span data-ttu-id="ce8a6-115">詳細については、[チャネル データベース拡張機能](../dev-itpro/channel-db-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-115">For more information, see [Channel database extensions](../dev-itpro/channel-db-extensions.md).</span></span>

## <a name="set-up-receipts-in-commerce-headquarters"></a><span data-ttu-id="ce8a6-116">Commerce 本社でレシートを設定する</span><span class="sxs-lookup"><span data-stu-id="ce8a6-116">Set up receipts in Commerce headquarters</span></span>

1. <span data-ttu-id="ce8a6-117">QR コードの新しいカスタム レシート フィールドに使用される新しい言語テキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-117">Create a new language text that will be used for a new custom receipt field for a QR code:</span></span>

    1. <span data-ttu-id="ce8a6-118">**Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **言語テキスト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-118">Go to **Retail and Commerce** > **Retail and commerce IT** > **Channel setup** > **POS profiles** > **Language text**.</span></span>
    2. <span data-ttu-id="ce8a6-119">**POS** タブの **POS 言語テキスト** クイック タブで、**追加** を選択して言語テキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-119">On the **POS** tab, on the **POS language text** FastTab, select **Add** to create a language text.</span></span>
    3. <span data-ttu-id="ce8a6-120">**言語 ID** フィールドで、新しい言語テキストの言語を指定します (たとえば、米国英語の場合は **en-us**)。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-120">In the **Language ID** field, specify the language of the new language text (for example, **en-us** for US English).</span></span>
    4. <span data-ttu-id="ce8a6-121">**テキスト ID** フィールドに、新しい言語テキストの識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-121">In the **Text ID** field, enter the identifier of the new language text.</span></span>
    5. <span data-ttu-id="ce8a6-122">**テキスト** フィールドに、新しい言語テキスト (たとえば、**税金請求書 QR コード**) を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-122">In the **Text** field, enter the new language text (for example, **Tax invoice QR code**).</span></span>

       ![QR コード レシート フィールドの言語テキストを作成する](media/language-text-page.png)

2.  <span data-ttu-id="ce8a6-124">QR コードの新しいカスタム レシート フィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-124">Create a new custom receipt field for a QR code:</span></span>

    1. <span data-ttu-id="ce8a6-125">**Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **カスタム フィールド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-125">Go to **Retail and Commerce** > **Retail and commerce IT** > **Channel setup** > **POS profiles** > **Custom field**.</span></span>
    2. <span data-ttu-id="ce8a6-126">アクション ウィンドウで **新規** を選択して、フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-126">On the Action Pane, select **New** to add a field.</span></span>
    3. <span data-ttu-id="ce8a6-127">**名前** フィールドに、新しいフィールドの名前を入力します (たとえば、**TAXINVOICE\_QR**)。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-127">In the **Name** field, enter a name for the new field (for example, **TAXINVOICE\_QR**).</span></span>
    4. <span data-ttu-id="ce8a6-128">**タイプ** フィールドで、**レシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-128">In the **Type** field, select **Receipt**.</span></span>
    5. <span data-ttu-id="ce8a6-129">**キャプション テキスト ID** フィールドに、以前に作成した言語テキストの **テキスト ID** 値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-129">In the **Caption text ID** field, enter the **Text ID** value from the language text that you created earlier.</span></span>

        ![QR コードのレシート カスタム フィールドを作成する](media/custom-fields.png)

3.  <span data-ttu-id="ce8a6-131">QR コードのカスタム フィールドをレシートに追加します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-131">Add a custom field for a QR code to a receipt:</span></span>

    1. <span data-ttu-id="ce8a6-132">**Retail と Commerce** > **Retail および Commerce IT** > **チャネル設定** > **POS プロファイル** > **レシートの形式** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-132">Go to **Retail and Commerce** > **Retail and commerce IT** > **Channel setup** > **POS** > **Receipt formats**.</span></span>
    2. <span data-ttu-id="ce8a6-133">QR コードを追加するレシートを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-133">Select the receipt to add a QR code to.</span></span>
    3. <span data-ttu-id="ce8a6-134">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-134">On the Action Pane, select **Designer**.</span></span>
    4. <span data-ttu-id="ce8a6-135">レシート デザイナーをダウンロードし、それを実行して、ログインします。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-135">Download the receipt designer, run it, and sign in.</span></span>
    5. <span data-ttu-id="ce8a6-136">レシートのヘッダーまたはフッターにカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-136">Add a custom field to the receipt header or footer.</span></span>

4. <span data-ttu-id="ce8a6-137">変更をチャネル データベースと同期します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-137">Sync the changes with the channel database:</span></span>

    1. <span data-ttu-id="ce8a6-138">**Retail と Commerce** > **Retail および Commerce IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-138">Go to **Retail and Commerce** > **Retail and commerce IT** > **Distribution schedule**.</span></span>
    2. <span data-ttu-id="ce8a6-139">ジョブ **1070** および **1090** を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-139">Run jobs **1070** and **1090**.</span></span>

## <a name="create-a-crt-extension-to-support-printing-qr-codes"></a><span data-ttu-id="ce8a6-140">QR コードの印刷をサポートする CRT 拡張機能を作成する</span><span class="sxs-lookup"><span data-stu-id="ce8a6-140">Create a CRT extension to support printing QR codes</span></span>

<span data-ttu-id="ce8a6-141">QR コードの新しいカスタム レシート フィールドをサポートするには、URL 文字列を作成して QR コードを作成する CRT 拡張機能を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-141">To support the new custom receipt field for a QR code, you must create a CRT extension that will create a URL string and generate a QR code for it.</span></span> <span data-ttu-id="ce8a6-142">レシートにカスタム フィールドを追加する方法については、[Commerce Store レシートを拡張する](../dev-itpro/retail-sdk/retail-sdk-samples.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-142">For an example that shows how to add a custom field to a receipt, see [Extend Commerce Store receipts](../dev-itpro/retail-sdk/retail-sdk-samples.md).</span></span>

<span data-ttu-id="ce8a6-143">次の手順に従って、QR コードの新しいカスタム レシート フィールドを処理します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-143">Follow these steps to handle the new custom receipt field for a QR code.</span></span>

1. <span data-ttu-id="ce8a6-144">Retail ソフトウェア開発キット (SDK) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-144">Install the Retail software development kit (SDK).</span></span> <span data-ttu-id="ce8a6-145">詳細については、[Retail ソフトウェア開発キット (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-145">For more information, see [Retail software development kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>
2.  <span data-ttu-id="ce8a6-146">Retail SDK で、C\# プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-146">In the Retail SDK, create a C\# project.</span></span>
3.  <span data-ttu-id="ce8a6-147">新しい C\# プロジェクトで、次のパッケージの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-147">In the new C\# project, add references to the following packages:</span></span>

    - <span data-ttu-id="ce8a6-148">Microsoft.Dynamics.Commerce.Runtime.DataModel.India</span><span class="sxs-lookup"><span data-stu-id="ce8a6-148">Microsoft.Dynamics.Commerce.Runtime.DataModel.India</span></span>
    - <span data-ttu-id="ce8a6-149">Microsoft.Dynamics.Commerce.Runtime.DataServices</span><span class="sxs-lookup"><span data-stu-id="ce8a6-149">Microsoft.Dynamics.Commerce.Runtime.DataServices</span></span>
    - <span data-ttu-id="ce8a6-150">Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting</span><span class="sxs-lookup"><span data-stu-id="ce8a6-150">Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting</span></span>
    - <span data-ttu-id="ce8a6-151">Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine</span><span class="sxs-lookup"><span data-stu-id="ce8a6-151">Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine</span></span>
    - <span data-ttu-id="ce8a6-152">Microsoft.Dynamics.Commerce.Runtime.Services.Messages</span><span class="sxs-lookup"><span data-stu-id="ce8a6-152">Microsoft.Dynamics.Commerce.Runtime.Services.Messages</span></span>
    - <span data-ttu-id="ce8a6-153">Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia</span><span class="sxs-lookup"><span data-stu-id="ce8a6-153">Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia</span></span>

4. <span data-ttu-id="ce8a6-154">処理するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-154">Create a class to handle.</span></span> 

    ```C#
    public class GetSalesTransactionCustomReceiptFieldService : IRequestHandlerAsync, ICountryRegionAware.
    {
        // Add code here.
    }
    ```
       
5. <span data-ttu-id="ce8a6-155">新しいカスタム レシート フィールドを処理し、QR コードを文字列として返すハンドラー メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-155">Implement a handler method that will handle the new custom receipt field and return a QR code as a string.</span></span>

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
          case "TAXINVOICE\_QR":
            receiptFieldValue = await GetQRCode(request).ConfigureAwait(false);
            break;
          default:
            return new NotHandledResponse();
      }
      return new GetCustomReceiptFieldServiceResponse(receiptFieldValue);
    }
    ```

    <span data-ttu-id="ce8a6-156">ハンドラーには次の手順を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-156">The handler should include the following steps.</span></span>

    1. <span data-ttu-id="ce8a6-157">リクエスト パラメーターとして渡される販売注文 (**SalesOrder**) に基づいて UPI リンクを生成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-157">Generate UPI link based on the sales order (**SalesOrder**) that is passed as the request parameter.</span></span>
    2. <span data-ttu-id="ce8a6-158">**EncodeQrCodeServiceRequest** を実行して QR コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-158">Run **EncodeQrCodeServiceRequest** to generate a QR code.</span></span> <span data-ttu-id="ce8a6-159">(**EncodeQrCodeServiceRequest** は、**Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting** パッケージの一部です。)</span><span class="sxs-lookup"><span data-stu-id="ce8a6-159">(**EncodeQrCodeServiceRequest** is part of the **Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting** package.)</span></span>
    3. <span data-ttu-id="ce8a6-160">`<>` タグで返される QR コード文字列をラップします。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-160">Wrap the QR code string that is returned in a `<>` tag.</span></span>

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

6. <span data-ttu-id="ce8a6-161">**CommerceRuntime.Ext.config** に必要な拡張機能を追加します。ここで **Contoso.Commerce.Runtime.ReceiptsIndia** は、QR コード アセンブリを印刷するための新しい拡張機能の名前です。</span><span class="sxs-lookup"><span data-stu-id="ce8a6-161">Add the required extensions to **CommerceRuntime.Ext.config**. Here, **Contoso.Commerce.Runtime.ReceiptsIndia** is the name of the new extension for printing the QR code assembly.</span></span>

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
           <add source="assembly"
       value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
          </composition>
       </commerceRuntimeExtensions>
    ```

## <a name="appendix-a"></a><span data-ttu-id="ce8a6-162">付録 A</span><span class="sxs-lookup"><span data-stu-id="ce8a6-162">Appendix A</span></span>
### <a name="sample-of-a-crt-extension-class-for-printing-qr-codes"></a><span data-ttu-id="ce8a6-163">QR コードを印刷するための CRT 拡張クラスのサンプル</span><span class="sxs-lookup"><span data-stu-id="ce8a6-163">Sample of a CRT extension class for printing QR codes</span></span>

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
        using Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia.Messages;

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
                    return new\[\]
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
                    return new\[\]
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
                private async Task<Response&>
           GetCustomReceiptFieldForSalesTransactionReceiptsAsync(GetSalesTransactionCustomReceiptFieldServiceRequest request)
                {
                    ThrowIf.Null(request.SalesOrder, 
           $"{nameof(request)},{nameof(request.SalesOrder)}");
                    string receiptFieldName = request.CustomReceiptField;
                    string receiptFieldValue = string.Empty;
                    switch (receiptFieldName)
                    {
                        case "TAXINVOICE\_QR":
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
   
