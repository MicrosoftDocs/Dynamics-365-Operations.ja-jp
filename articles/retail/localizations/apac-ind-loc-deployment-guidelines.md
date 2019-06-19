---
title: インドのキャッシュ レジスターの配置ガイドライン
description: このトピックは、インドの小売ローカライズ用配置ガイドです。
author: AlexChern0v
manager: ralin
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: shylaw
ms.search.region: India
ms.search.industry: Retail
ms.author: jiaqia
ms.search.scope: Retail
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: a636ddaf42c4545cfd3c988d34f00e35cf714545
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571596"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a>インドのキャッシュ レジスターの配置ガイドライン

[!include [banner](../includes/banner.md)]

このトピックは、インドの Microsoft Dynamics 365 for Retail ローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。 インドの小売ローカライズの詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。

このサンプルは、小売ソフトウェア開発キット (SDK) の一部です。 リテール SDK をダウンロードして使用する方法については、[リテール SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このサンプルは Commerce runtime (CRT) の拡張機能で構成されます。 このサンプルを実行するには、CRT プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。

> [!NOTE]
> 使用しているバージョンによって、このトピックの手順の一部が異なります。 詳細については、[Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md)を参照してください。

## <a name="prerequisites"></a>必要条件

Visual C++ 再頒布可能パッケージが商品及びサービス税 (GST) 計算を実行するマシン上にあることを確認します。 クラウド POS、およびオンライン モードの Modern POS の場合、このマシンは小売サーバーです。 オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。 パッケージを取得するには、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=30679)を参照してください。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

### <a name="the-crt-extension-components"></a>CRT 拡張コンポーネント

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、CRT ソリューション **CommerceRuntimeSamples.sln** を開きます。 このソリューションは **RetailSdk\\SampleExtensions\\CommerceRuntime** の下にあります。

#### <a name="generic-tax-engine-component"></a>汎用税エンジン コンポーネント

# <a name="retail-731tabretail-7-3-1"></a>[Retail 7.3.1](#tab/retail-7-3-1)

1. **Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。
2. 以下のファイルを検索します:

    - **Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:

        - Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll

    - **Reference\\Newtonsoft.Json\\9.0.0.0** フォルダー内:

        - Newtonsoft.Json.dll

    - **Reference\\TaxEngine** フォルダー内:

        - Microsoft.Dynamics365.Tax.Core.dll
        - Microsoft.Dynamics365.Tax.DataAccessor.dll
        - Microsoft.Dynamics365.Tax.DataAccessFramework.dll
        - Microsoft.Dynamics365.Tax.DataModel.dll
        - Microsoft.Dynamics365.Tax.Metadata.dll
        - Microsoft.Dynamics365.LocalizationFramework.dll
        - Microsoft.Dynamics365.LocalizationFrameworkCore.dll
        - Microsoft.Dynamics365.ElectronicReportingMapping.dll
        - Microsoft.Dynamics365.XppSupportLayer.dll

    - 以下のフォルダーを **Reference\\Z3** フォルダー内で見つけます:

        - x86
        - x64

3. 11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:

    - **小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。

4. CRT の拡張機能のコンフィギュレーション ファイルを検索します。

    - **小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-732-and-latertabretail-7-3-2"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

1. **Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。
2. 以下のファイルを検索します:

    - **Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:

        - Contoso.Commerce.Runtime.GenericTaxEngine.dll

    - **References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:

        - Newtonsoft.Json.dll

    - **References\\Microsoft.Dynamics.AX.TaxEngine.7.3.42\\XppModule\\TaxEngine\\bin** フォルダー内:

        - Microsoft.Dynamics365.LocalizationFramework.dll
        - Microsoft.Dynamics365.Tax.Core.dll
        - Microsoft.Dynamics365.Tax.DataAccessFramework.dll
        - Microsoft.Dynamics365.Tax.DataAccessor.dll
        - Microsoft.Dynamics365.Tax.DataModel.dll
        - Microsoft.Dynamics365.Tax.Metadata.dll

    - **References\\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\\XppModule\\ElectronicReporting\\bin** フォルダー内:

        - Microsoft.Dynamics365.ElectronicReportingMapping.dll
        - Microsoft.Dynamics365.LocalizationFrameworkCore.dll
        - Microsoft.Dynamics365.XppSupportLayer.dll

    - 以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:

        - x86
        - x64

3. 11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:

    - **小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。

4. CRT の拡張機能のコンフィギュレーション ファイルを検索します。

    - **小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-813-and-latertabretail-8-1-3"></a>[Retail 8.1.3 およびそれ以降](#tab/retail-8-1-3)

1. **Runtime.Extensions.GenericTaxEngine** プロジェクトを探して、構築します。
2. 以下のファイルを検索します:

    - **Extensions.GenericTaxEngine\\bin\\Debug** フォルダー内:

        - Contoso.Commerce.Runtime.GenericTaxEngine.dll

    - **References\\Newtonsoft.Json.9.0.1\\lib\\net45** フォルダー内:

        - Newtonsoft.Json.dll

    - **References\\Microsoft.Dynamics.AX.TaxEngine.8.0.26\\XppModule\\TaxEngine\\bin** フォルダー内:

        - Microsoft.Dynamics365.LocalizationFramework.dll
        - Microsoft.Dynamics365.Tax.Core.dll
        - Microsoft.Dynamics365.Tax.DataAccessFramework.dll
        - Microsoft.Dynamics365.Tax.DataAccessor.dll
        - Microsoft.Dynamics365.Tax.DataModel.dll
        - Microsoft.Dynamics365.Tax.Metadata.dll

    - **References\\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\\XppModule\\ElectronicReporting\\bin** フォルダー内:

        - Microsoft.Dynamics365.ElectronicReportingMapping.dll
        - Microsoft.Dynamics365.LocalizationFrameworkCore.dll
        - Microsoft.Dynamics365.XppSupportLayer.dll

    - 以下のフォルダーを **References\\Z3.4.5.0\\lib\\net40** フォルダーで探します:

        - x86
        - x64

3. 11 のアセンブリ ファイル、および x64 と x86 フォルダーを CRT 拡張機能フォルダーにコピーします:

    - **小売サーバー:** アセンブルを Microsoft インターネット インフォメーション サービス (IIS) 小売サーバーのサイト場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\\ext** フォルダーにコピーします。

4. CRT の拡張機能のコンフィギュレーション ファイルを検索します。

    - **小売サーバー:** ファイルは **commerceruntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

# <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

汎用税エンジン コンポーネントはシールド拡張機能の一部です。

1. CRT の拡張機能のコンフィギュレーション ファイルを検索します。

    - **小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!WARNING]
    > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

---

### <a name="set-up-required-parameters-in-retail-headquarters"></a>小売用バックオフィスで要求されるパラメーターを設定します。

詳細については、[インドのキャッシュ レジスターの販売税統合](./apac-ind-cash-registers.md)を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、小売コンポーネントを含む配置可能パッケージを作成して、パッケージを実稼働環境で適用します。

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    # <a name="retail-731tabretail-7-3-1"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.GenericTaxEngine" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[Retail 8.1.3 およびそれ以降](#tab/retail-8-1-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.GenericTaxEngine" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    ---

2. **RetailSdk\\BuildTools** フォルダーの下の **Customization.settings** パッケージ カスタマイズ構成ファイルで、以下の行を **ItemGroup** セクションに追加して、配置可能パッケージ内の CRT 拡張機能を含めます。

    # <a name="retail-731tabretail-7-3-1"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\TaxEngine\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json\9.0.0.0\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.7.3.42\XppModule\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.7.3.42\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json.9.0.1\lib\net45\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[Retail 8.1.3 およびそれ以降](#tab/retail-8-1-3)

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.GenericTaxEngine.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Core.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.Metadata.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessor.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataAccessFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.Tax.DataModel.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.TaxEngine.8.0.26\XppModule\TaxEngine\bin\Microsoft.Dynamics365.LocalizationFramework.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.LocalizationFrameworkCore.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.ElectronicReportingMapping.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Microsoft.Dynamics.AX.ElectronicReporting.8.0.26\XppModule\ElectronicReporting\bin\Microsoft.Dynamics365.XppSupportLayer.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Newtonsoft.Json.9.0.1\lib\net45\Newtonsoft.Json.dll" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    ---

3. 以下のファイルを修正して、配置可能パッケージに Z3 ライブラリを含めます。

    # <a name="retail-731tabretail-7-3-1"></a>[Retail 7.3.1](#tab/retail-7-3-1)

    - Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj
    - Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj
    - Packages\\RetailServer\\Sdk.RetailServerSetup.proj

    以下の行を **ItemGroup** セクションに追加します。

    ```xml
    <_bin_ext_Z3_x86_File Include="..\..\References\Z3\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="..\..\References\Z3\x64\*.*" />
    ```

    **Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    **Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。
    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-732-and-latertabretail-7-3-2"></a>[Retail 7.3.2 およびそれ以降](#tab/retail-7-3-2)

    - Packages\\ModernPOS.Sdk\\Sdk.ModernPOSSetup.csproj
    - Packages\\ModernPOSOffline.Sdk\\Sdk.ModernPOSSetupOffline.csproj
    - Packages\\RetailServer\\Sdk.RetailServerSetup.proj

    以下の行を **ItemGroup** セクションに追加します。

    ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
    ```

    **Sdk.ModernPOSSetup.csproj** および **Sdk.ModernPOSSetupOffline.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    **Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-813-and-latertabretail-8-1-3"></a>[Retail 8.1.3 およびそれ以降](#tab/retail-8-1-3)

    - Packages\\\_SharedPackagingProjectComponents\\Sdk.ModernPos.Shared.csproj
    - Packages\\RetailServer\\Sdk.RetailServerSetup.proj

    以下の行を **ItemGroup** セクションに追加します。

     ```xml
    <_bin_ext_Z3_x86_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x86\*.*" />
    <_bin_ext_Z3_x64_File Include="$(SdkReferencesPath)\Z3.4.5.0\lib\net40\x64\*.*" />
     ```

    **Sdk.ModernPos.Shared.csproj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\x64" SkipUnchangedFiles="true" />
    ```

    **Sdk.RetailServerSetup.proj** では、以下の行も **\<Target Name="CopyPackageFiles"\>** セクションに追加します。

    ```xml
    <Copy SourceFiles="@(_bin_ext_Z3_x86_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x86" SkipUnchangedFiles="true" />
    <Copy SourceFiles="@(_bin_ext_Z3_x64_File)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\x64" SkipUnchangedFiles="true" />
    ```

    # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

    > [!NOTE]
    > このバージョンには、この手順は適用されません。

    ---

4. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
5. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
