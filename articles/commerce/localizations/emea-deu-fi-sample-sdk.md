---
title: ドイツ向け会計登録サービス統合サンプルの展開ガイドライン (レガシ)
description: この記事では、Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) から、ドイツ向け会計統合サンプルを展開するためのガイドラインを提供します。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 9f6ecc715e10538806998459b7fd837648494ad7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845840"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>ドイツ向け会計登録サービス統合サンプルの展開ガイドライン (レガシ)

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) から Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) でドイツ向け会計登録サービス統合サンプルを展開するためのガイドラインを提供します。 この会計統合サンプルの詳細については、[ドイツ向け会計登録サービス統合サンプル](emea-deu-fi-sample.md) を参照してください。 

ドイツ向け会計統合サンプルは Retail SDK の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。 このサンプルは、Commerce runtime (CRT) とハードウェア ステーションの拡張機能で構成されます。 このサンプルを実行する際は、CRT とハードウェア ステーション プロジェクトを変更して構築する必要があります。 この記事で説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

### <a name="enable-commerce-runtime-extensions"></a>Commerce Runtime 拡張機能を有効化する

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** で **CommerceRuntimeSamples.sln** ソリューションを開きます。

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample コンポーネント

1. **Runtime.Extensions.DocumentProvider.EFRSample** プロジェクトを探して、構築します。
2. **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** ファイルをインターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR コンポーネント

1. **Runtime.Extensions.DocumentProvider.DataModelEFR** プロジェクトを探して、構築します。
2. **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** ファイルを IIS Commerce Scale Unit サイトの場所の配下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>拡張機能の構成ファイル

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>会計コネクタ拡張機能の有効化

[ハードウェア ステーション](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) または [POS レジスター](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) で会計コネクタ拡張機能を有効にできます。

#### <a name="enable-hardware-station-extensions"></a>ハードウェア ステーション拡張機能を有効化する

ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** 配下の **HardwareStationSamples.sln** ソリューションを開きます。

##### <a name="efrsample-component"></a>EFRSample コンポーネント

1. **HardwareStation.Extension.EFRSample** プロジェクトを探して、構築します。
2. **Extension.EFRSample\\bin\\Debug** フォルダーで、以下のアセンブリ ファイルを見つけます。

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。

    - **共有ハードウェア ステーション:** ファイルを、IIS ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
    - **Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

4. ハードウェア ステーションの拡張機能に対する拡張機能構成ファイルを見つけます。 ファイルの名前は **HardwareStation.Extension.config** です。

    - **共有ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
    - **Modern POS の専用ハードウェア ステーション:** ファイルは、Modern POS クライアント ブローカーの場所にあります。

5. 構成ファイルの **構成** セクションに、次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>拡張機能を有効化する

POS 拡張機能サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\PosFiscalConnectorSample** フォルダーにあります。

レガシ SDK で POS 拡張機能サンプルを読み取るには、次の手順に従います。

1. **Pos.Extension** フォルダをレガシ SDK の POS **拡張機能** フォルダー (たとえば `C:\RetailSDK\src\POS\Extensions`) にコピーします。
1. **Pos.Extension** フォルダーのコピーの名前を **PosFiscalConnector** に変更します。
1. **PosFiscalConnector** フォルダから次のフォルダーとファイルを削除します。

    - bin
    - DataService
    - devDependencies
    - ライブラリ
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdtmModel.g.xml
    - tsconfig.json

1. **CloudPos.sln**、または **ModernPos.sln** を開きます。
1. **Pos.Extensions** プロジェクトで、**PosFiscalConnector** フォルダーを含めます。
1. **extensions.json** ファイルを開いて、**PosFiscalConnector** 拡張機能を追加します。
1. SDK を構築します。

### <a name="production-environment"></a>実稼働環境

前述の手順では、会計登録サービス統合サンプルの構成要素である拡張機能を有効にしました。 さらに、この手順に従って、Commerce コンポーネントを含む配置可能パッケージを作成し、それらのパッケージを実稼働環境に適用する必要があります。

1. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次の行を追加します。

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 展開可能なパッケージに CRT 拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
4. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
5. [ドイツ向け Commerce の設定](emea-deu-fi-sample.md#set-up-commerce-for-germany) で説明されている必要な設定タスクをすべて完了します。

## <a name="design-of-extensions"></a>拡張機能の設計

ドイツ向け会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいています。 会計統合ソリューションの設計に関する詳細は、[会計統合サンプル設計の概要](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して会計登録サービスからの応答を処理することです。

CRT 拡張機能は **Runtime.Extensions.DocumentProvider.EFRSample** です。 会計統合ソリューションの設計に関する詳細は、[コマースチャネルの会計統合の概要](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーに対応した要求ハンドラーが 1 つあります: **DocumentProviderEFRFiscalDEU**。 このハンドラーは、会計登録サービスの会計ドキュメントを生成する際に使用します。 これは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – この要求は拡張データとともに応答を返します。

#### <a name="configuration"></a>構成

構成ファイル **DocumentProviderFiscalEFRSampleGermany** は、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

以下の設定を追加します:

- **VAT 税率マッピング** – 税率値のマッピング。会計サービスに送信する要求の **TaxG** (税グループ) 属性の値に対する消費税コードに対して設定します。
- **ギフト カードと前金の税グループ** – ギフト カードや前金を含む操作に基づいて、会計サービスに送信する要求の **TaxG** 属性の値。
- **テンダー タイプのマッピング** – 会計サービスに送信する要求の、**PayG** (支払グループ) 属性の値に対する支払方法のマッピング。
- **VAT 控除の税グループ** – 納税義務を免除された業務に基づいて、会計サービスに送信する要求の **TaxG** 属性の値。
- **顧客データを含める** – このパラメーターをオンにすると、顧客をトランザクションに追加した場合に、名前や住所などの顧客情報を会計サービスへの要求に含めます。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計登録サービスと通信できます。

ハードウェア ステーション拡張機能は **HardwareStation.Extension.EFRSample** です。 これは HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計登録サービスに送信します。 また、会計登録サービスから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EFRHandler** 要求ハンドラーは、会計登録サービスへの要求を処理するエントリ ポイントです。 このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントを会計登録サービスに送信し、その応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求は会計登録サービスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求は会計登録サービスの初期化に使用します。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

以下の設定を追加します:

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位 (ms) で表した時間。ドライバーは会計登録サービスからの応答を待機します。
- **会計登録通知を表示する** – このパラメーターをオンにすると、会計サービスからの通知を POS でユーザー メッセージとして表示します。

### <a name="pos-fiscal-connector-extension-design"></a>POS 会計コネクタ拡張機能の設計

POS 会計コネクタ拡張機能の目的は、POS からの会計登録サービスと通信することです。 これは通信に HTTPS プロトコルを使用します。

#### <a name="fiscal-connector-factory"></a>会計コネクタ ファクトリー

会計コネクタ ファクトリーは、コネクタ名を会計コネクタの実装にマップし、これは  **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** ファイルにあります。 このコネクタ名は、Commerce 本部で指定した会計コネクタの名前と一致する必要があります。

#### <a name="efr-fiscal-connector"></a>EFR 会計コネクタ

EFR 会計コネクタは **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** ファイルにあります。 これは、次の要求をサポートする **IFiscalConnector** インターフェイスを実装します。

- **FiscalRegisterSubmitDocumentClientRequest** – この要求はドキュメントを会計登録サービスに送信し、その応答を返します。
- **FiscalRegisterIsReadyClientRequest** – この要求は会計登録サービスの正常性確認に使用します。
- **FiscalRegisterInitializeClientRequest** – この要求は会計登録サービスの初期化に使用します。

#### <a name="configuration"></a>構成

この構成ファイルは、[Dynamics 365 Commerce ソリュション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** フォルダーにあります。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位 (ms) で表した時間。このコネクタは会計登録サービスからの応答を待機します。
