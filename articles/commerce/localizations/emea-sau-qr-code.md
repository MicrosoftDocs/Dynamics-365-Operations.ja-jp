---
title: サウジアラビア向け QR コードの生成とレシートへの印刷
description: この記事では、Microsoft Dynamics 365 Commerce でサウジアラビアで使用できる QR コードを印刷するための機能の概要を説明します。
author: EvgenyPopovMBS
ms.date: 01/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Saudi Arabia
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2021-11-04
ms.openlocfilehash: 1327900ba05122db0575683d3d169ccb16b2b165
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337363"
---
# <a name="generate-qr-codes-and-print-them-on-receipts-for-saudi-arabia"></a>サウジアラビア向け QR コードの生成とレシートへの印刷

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce でサウジアラビアで使用できる QR コードを印刷するための機能の概要を説明します。

サウジアラビアに通常の住所を持つ法人にリンクされている店舗では、ユーザーは現金払いトランザクションまたは販売注文トランザクションのレシートに QR コードを印刷できます。 QR コードには、次の情報が含まれます。

| 順番 | フィールド                                                    | データ ソース |
|----------| ---------------------------------------------------------|-------------|
| 1        | 会社名                                             | 法人の名前 |
| 2        | 会社の VAT 登録番号                          | 法人の税登録番号 |
| 3        | トランザクションの日時                             | 小売用店舗トランザクションの日時 |
| 4        | 合計受領額 (付加価値税 \[VAT\] を含む) | 小売店舗トランザクションの合計金額 |
| 5        | レシートに含まれる VAT の合計金額                  | 小売店舗トランザクションに係る税額の合計額 |

> [!NOTE]
> 顧客注文トランザクションの作成時に、合計受領額は、配送実行モードを使用するすべてのトランザクション明細行の合計金額を加算して計算されます。

QR コードは、base64 変換をタグ長値 (TLV) 形式でエンコードされたトランザクション情報に適用することによって生成されます。 ザカート・税・税関庁 (ZATCA) は、QR コードの検証に使用できるツールを提供します。 電子請求書発行の要件および QR コード検証機能の詳細については、[ZATCA の電子請求書ポータル](https://zatca.gov.sa/en/E-Invoicing/Pages/default.aspx)を参照してください。

## <a name="set-up-qr-codes"></a>QR コードの設定

QR コードを生成してサウジアラビア向けのレシートにを印刷するには、次のタスクを行う必要があります。

1. カスタム フィールドを設定して、販売レシートのレシート形式で使用できるようにします。
1. レシート形式を設定します。
1. コマース パラメーターで、QR コード分析コードを指定します。
1. Commerce runtime (CRT) 拡張機能を有効にします。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売レシートのレシート形式で使用できるようにする

販売時点管理 (POS) レシート形式で使用される言語テキストおよびカスタム フィールドを構成することができます。 **言語テキスト** ページで、レシート レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

| 言語 ID | テキスト ID | テキスト         |
|-------------|---------|--------------|
| ja       | 900001  | QR コード (SA) |

> [!NOTE]
> レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**カスタム フィールド** ページで、レシート レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name             | 種類    | キャプション テキスト ID |
|------------------|---------|-----------------|
| INVOICEQRCODE_SA | 受信 | 900001          |

### <a name="configure-receipt-formats"></a>レシート形式を設定する

必要なレシート形式ごとに、**印刷動作** フィールドを **常に印刷** にします。

レシート形式デザイナーで、レシートの **フッター** セクションに、次のカスタム フィールドを追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

- **QR コード (SA)** – このフィールドは、QR コードをレシートに印刷します。

レシート形式の使用方法の詳細については、[レシート形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

### <a name="specify-qr-code-dimensions-in-commerce-parameters"></a>コマース パラメーターで、QR コード分析コードを指定する

コマース パラメーター ページの **コンフィギュレーション パラメーター** タブで、次のコンフィギュレーション パラメーターを追加します。

- **QrCodeWidth** - ピクセル単位の QR コード画像の幅。 パラメーターに適切な値を指定します。
- **QrCodeHeight** - ピクセル単位の QR コード画像の高さ。 パラメーターに適切な値を指定します。

> [!NOTE]
> レシートに QR コードを印刷するには、これらのコンフィギュレーション パラメーターの値を指定する必要があります。 パラメーターの既定値のサポートは、今後のアップデートで追加される可能性があります。

### <a name="enable-crt-extensions"></a>CRT 拡張機能の有効化

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、このローカライズ機能は使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retailソフトウェア開発キット (SDK) の以前のバージョンを使用する必要があります。 (Microsoft は今後のバージョンの新しい独立した梱包および拡張機能モデルに、ローカライズ機能のサポートを追加する予定です。)

#### <a name="development-environment"></a>開発環境

次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail サーバー:** ファイル名は **commerceruntime.ext.config** で、インターネット インフォメーション サービス (IIS) Retail サーバー サイトの場所にある **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSaudiArabia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
    ```

#### <a name="production-environment"></a>運用環境

以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを運用環境で適用します。

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** パッケージ コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSaudiArabia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
    ```

1. Visual Studio ユーティリティ用の MSBuild コマンド プロンプトを起動し、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
1. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。

## <a name="print-qr-code-images-on-opos-printers"></a>OPOS プリンターで QR コードのイメージを印刷する

Retail POS 用 Object Linking and Embedding (OPOS) プリンターを使用する場合、QR コード画像用のプリンター固有の要件をサポートする，追加のカスタマイズを実装する必要がある場合があります。 たとえば、PNG 形式から BMP 形式に QR コード画像を変換する必要がある場合があります。 このセクションでは、このタイプのカスタマイズの例を示します。

> [!NOTE]
> このカスタマイズの例は、EPSON TM-T88V OPOS プリンターを使用してテストしました。 別のプリンター メーカーまたはモデルをサポートするように変更が必要な場合があります。

新しい拡張機能を作成し、環境に追加するには、これらの手順に従います。

1. Retail SDK をインストールします。 詳細については、[Retail ソフトウェア開発キット (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。
1. Retail SDK で、Commerce のバージョンに基づき、次のコードを使用して、**RetailSdk\\SampleExtensions\\CommerceRuntime** の **CommerceRuntimeSamples.sln** ソリューションの下に C\# プロジェクトを作成します。

    # <a name="commerce-10025-and-earlier"></a>[10.0.25 およびそれ以前の Commerce](#tab/commerce-10-0-25)

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.props" />
        <Import Project="..\..\..\BuildTools\Common.props" />
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.settings" />

        <PropertyGroup>
            <TargetFramework>netstandard2.0</TargetFramework>
            <AssemblyName>$(AssemblyNamePrefix).Commerce.Runtime.QrCodeExtension</AssemblyName>
            <RootNamespace>Contoso.Commerce.Runtime.QrCodeExtension</RootNamespace>
            <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
        </PropertyGroup>

        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.targets" />

        <ItemGroup>
            <PackageReference Include="Microsoft.Dynamics.Commerce.Runtime.Framework" Version="$(FrameworkRepoPackagesVersion)" />
            <PackageReference Include="Microsoft.Dynamics.Commerce.Runtime.Services.Messages" Version="$(ChannelRepoPackagesVersion)" />
            <PackageReference Include="System.Drawing.Common" Version="4.7.0" />
        </ItemGroup>

        <ItemGroup>
            <Reference Include="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting">
                <HintPath>..\..\..\..\..\nuget packages\microsoft.dynamics.commerce.runtime.electronicreporting.9.35.21321.4\lib\netstandard2.0\Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting.dll</HintPath>
            </Reference>
        </ItemGroup>

        <ItemGroup>
            <Folder Include="Properties\" />
        </ItemGroup>
    </Project>
    ```

    また、IIS Retail Server サイトの場所の下にある **Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting.dll** ライブラリ リファレンスへの **HintPath** 要素の値を変更する必要もあります。

    # <a name="commerce-10026-and-later"></a>[10.0.26 およびそれ以降の Commerce](#tab/commerce-10-0-26)

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.props" />
        <Import Project="..\..\..\BuildTools\Common.props" />
        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.settings" />

        <PropertyGroup>
            <TargetFramework>netstandard2.0</TargetFramework>
            <AssemblyName>$(AssemblyNamePrefix).Commerce.Runtime.QrCodeExtension</AssemblyName>
            <RootNamespace>Contoso.Commerce.Runtime.QrCodeExtension</RootNamespace>
            <AutoGenerateBindingRedirects>true</AutoGenerateBindingRedirects>
        </PropertyGroup>

        <Import Project="..\..\..\BuildTools\Microsoft.Dynamics.RetailSdk.Build.targets" />

        <ItemGroup>
            <PackageReference Include="Microsoft.Dynamics.Commerce.Runtime.Framework" Version="$(FrameworkRepoPackagesVersion)" />
            <PackageReference Include="Microsoft.Dynamics.Commerce.Runtime.Services.Messages" Version="$(ChannelRepoPackagesVersion)" />
            <PackageReference Include="Microsoft.Dynamics.Commerce.Runtime.Localization.Services.Messages" Version="$(ChannelRepoPackagesVersion)" />
            <PackageReference Include="System.Drawing.Common" Version="4.7.0" />
        </ItemGroup>

        <ItemGroup>
            <Folder Include="Properties\" />
        </ItemGroup>
    </Project>
    ```

    ---

1. Commerce のバージョンに基づき、次のコードを使用して、拡張クラスを作成します。

    # <a name="commerce-10025-and-earlier"></a>[10.0.25 およびそれ以前の Commerce](#tab/commerce-10-0-25)

    ```C#
    /**
     * SAMPLE CODE NOTICE
     * 
     * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
     * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
     * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
     * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
     */

    using System.Drawing;
    using System.Drawing.Imaging;
    using System.IO;

    namespace Contoso
    {
        namespace Commerce.Runtime.QrCodeExtension
        {
            using System;
            using System.Collections.Generic;
            using System.Threading.Tasks;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

            /// <summary>
            /// The extension for QR code printing.
            /// </summary>
            internal class QrCodeServiceExtension : IRequestHandlerAsync
            {
                /// <summary>
                /// Printer horizontal resolution for image.
                /// </summary>
                private const float PrinterXDpi = 60f;

                /// <summary>
                /// Printer vertical resolution for image.
                /// </summary>
                private const float PrinterYDpi = 90f;

                /// <summary>
                /// Printer pixel format for image.
                /// </summary>
                private const PixelFormat PrinterPixelFormat = PixelFormat.Format8bppIndexed;

                /// <summary>
                /// Gets the collection of supported request types by this service.
                /// </summary>
                public IEnumerable<Type> SupportedRequestTypes
                {
                    get => new[] {typeof(EncodeQrCodeServiceRequest)};
                }

                /// <summary>
                /// Processes the request.
                /// </summary>
                /// <param name="request">The request.</param>
                /// <returns>The response.</returns>
                public async Task<Response> Execute(Request request)
                {
                    ThrowIf.Null(request, nameof(request));

                    switch (request)
                    {
                        case EncodeQrCodeServiceRequest encodeQrCodeServiceRequest:
                        {
                            EncodeQrCodeServiceResponse nextResponse = await this.ExecuteNextAsync<EncodeQrCodeServiceResponse>(encodeQrCodeServiceRequest).ConfigureAwait(false);

                            if (nextResponse != null)
                            {
                                var qrCodeBmp = string.IsNullOrWhiteSpace(nextResponse.QRcode) ? nextResponse.QRcode : ConvertToGenericCompatibilityImage(nextResponse.QRcode);
                                return new EncodeQrCodeServiceResponse(qrCodeBmp);
                            }

                            return nextResponse;
                        }
                    }

                    return new NotHandledResponse();
                }

                /// <summary>
                /// Converts QR code image from any format to compatible with printer.
                /// </summary>
                /// <param name="base64data">Base64 image.</param>
                /// <returns>Image that Compatible with printer.</returns>
                private static string ConvertToGenericCompatibilityImage(string base64data)
                {
                    string convertedQrCode = base64data;
                    byte[] imageBytes = Convert.FromBase64String(convertedQrCode);
                    using (MemoryStream msOriginal = new MemoryStream(imageBytes))
                    using (MemoryStream msConverted = new MemoryStream())
                    {
                        var bitmapOriginal = new Bitmap(msOriginal);
                        if (!IsFormatCompatible(bitmapOriginal) || !AreResolutionAndPixelFormatCompatible(bitmapOriginal))
                        {
                            var bitmapConverted = bitmapOriginal;

                            if (!AreResolutionAndPixelFormatCompatible(bitmapOriginal))
                            {
                                var rectangle = new Rectangle(0, 0, bitmapOriginal.Width, bitmapOriginal.Height);
                                bitmapConverted = bitmapOriginal.Clone(rectangle, PrinterPixelFormat);
                                bitmapConverted.SetResolution(PrinterXDpi, PrinterYDpi);
                            }

                            bitmapConverted.Save(msConverted, ImageFormat.Bmp);
                        }

                        convertedQrCode = Convert.ToBase64String(msConverted.ToArray());
                    }

                    return convertedQrCode;
                }

                /// <summary>
                /// Verifies if the resolution and pixel format of bitmap are compatible with printer requirements.
                /// </summary>
                /// <param name="source">Bitmap.</param>
                /// <returns>True if compatible; otherwise false.</returns>
                private static bool AreResolutionAndPixelFormatCompatible(Bitmap source)
                {
                    return source.VerticalResolution == PrinterYDpi &&
                           source.HorizontalResolution == PrinterXDpi &&
                           source.PixelFormat == PrinterPixelFormat;
                }

                /// <summary>
                /// Verifies if the format of bitmap is compatible with printer requirements.
                /// </summary>
                /// <param name="source">Bitmap.</param>
                /// <returns>True if compatible; otherwise false.</returns>
                private static bool IsFormatCompatible(Bitmap source)
                {
                    return source.RawFormat.Equals(ImageFormat.Bmp);
                }
            }
        }
    }
    ```

    # <a name="commerce-10026-and-later"></a>[10.0.26 およびそれ以降の Commerce](#tab/commerce-10-0-26)

    ```C#
    /**
     * SAMPLE CODE NOTICE
     * 
     * THIS SAMPLE CODE IS MADE AVAILABLE AS ISMICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
     * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
     * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
     * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
     */

    using System.Drawing;
    using System.Drawing.Imaging;
    using System.IO;
    using Microsoft.Dynamics.Commerce.Runtime.Localization.Services.Messages;

    namespace Contoso
    {
        namespace Commerce.Runtime.QrCodeExtension
        {
            using System;
            using System.Collections.Generic;
            using System.Threading.Tasks;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;

            /// <summary>
            /// The extension for QR code printing.
            /// </summary>
            internal class QrCodeServiceExtension : IRequestHandlerAsync
            {
                /// <summary>
                /// Printer horizontal resolution for image.
                /// </summary>
                private const float PrinterXDpi = 60f;

                /// <summary>
                /// Printer vertical resolution for image.
                /// </summary>
                private const float PrinterYDpi = 90f;

                /// <summary>
                /// Printer pixel format for image.
                /// </summary>
                private const PixelFormat PrinterPixelFormat = PixelFormat.Format8bppIndexed;

                /// <summary>
                /// Gets the collection of supported request types by this service.
                /// </summary>
                public IEnumerable<Type> SupportedRequestTypes
                {
                    get => new[] {typeof(EncodeQrCodeServiceRequest)};
                }

                /// <summary>
                /// Processes the request.
                /// </summary>
                /// <param name="request">The request.</param>
                /// <returns>The response.</returns>
                public async Task<Response> Execute(Request request)
                {
                    ThrowIf.Null(request, nameof(request));

                    switch (request)
                    {
                        case EncodeQrCodeServiceRequest encodeQrCodeServiceRequest:
                        {
                            EncodeQrCodeServiceResponse nextResponse = await this.ExecuteNextAsync<EncodeQrCodeServiceResponse>(encodeQrCodeServiceRequest).ConfigureAwait(false);

                            if (nextResponse != null)
                            {
                                var qrCodeBmp = string.IsNullOrWhiteSpace(nextResponse.QRCode) ? nextResponse.QRCode : ConvertToGenericCompatibilityImage(nextResponse.QRCode);
                                return new EncodeQrCodeServiceResponse(qrCodeBmp);
                            }

                            return nextResponse;
                        }
                    }

                    return new NotHandledResponse();
                }

                /// <summary>
                /// Converts QR code image from any format to compatible with printer.
                /// </summary>
                /// <param name="base64data">Base64 image.</param>
                /// <returns>Image that Compatible with printer.</returns>
                private static string ConvertToGenericCompatibilityImage(string base64data)
                {
                    string convertedQrCode = base64data;
                    byte[] imageBytes = Convert.FromBase64String(convertedQrCode);
                    using (MemoryStream msOriginal = new MemoryStream(imageBytes))
                    using (MemoryStream msConverted = new MemoryStream())
                    {
                        var bitmapOriginal = new Bitmap(msOriginal);
                        if (!IsFormatCompatible(bitmapOriginal) || !AreResolutionAndPixelFormatCompatible(bitmapOriginal))
                        {
                            var bitmapConverted = bitmapOriginal;

                            if (!AreResolutionAndPixelFormatCompatible(bitmapOriginal))
                            {
                                var rectangle = new Rectangle(0, 0, bitmapOriginal.Width, bitmapOriginal.Height);
                                bitmapConverted = bitmapOriginal.Clone(rectangle, PrinterPixelFormat);
                                bitmapConverted.SetResolution(PrinterXDpi, PrinterYDpi);
                            }

                            bitmapConverted.Save(msConverted, ImageFormat.Bmp);
                        }

                        convertedQrCode = Convert.ToBase64String(msConverted.ToArray());
                    }

                    return convertedQrCode;
                }

                /// <summary>
                /// Verifies if the resolution and pixel format of bitmap are compatible with printer requirements.
                /// </summary>
                /// <param name="source">Bitmap.</param>
                /// <returns>True if compatible; otherwise false.</returns>
                private static bool AreResolutionAndPixelFormatCompatible(Bitmap source)
                {
                    return source.VerticalResolution == PrinterYDpi &&
                           source.HorizontalResolution == PrinterXDpi &&
                           source.PixelFormat == PrinterPixelFormat;
                }

                /// <summary>
                /// Verifies if the format of bitmap is compatible with printer requirements.
                /// </summary>
                /// <param name="source">Bitmap.</param>
                /// <returns>True if compatible; otherwise false.</returns>
                private static bool IsFormatCompatible(Bitmap source)
                {
                    return source.RawFormat.Equals(ImageFormat.Bmp);
                }
            }
        }
    }
    ```

    ---

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.QrCodeExtension" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSaudiArabia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
    ```

1. **BuildTools** フォルダの下にある **Customization.settings** パッケージ カスタマイズ設定ファイルに、以下の行を追加して、展開可能なパッケージに CRT 拡張機能を含めます。

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.QrCodeExtension.dll" />
    ```

1. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
1. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
