---
title: チェコ共和国向け会計登録サービス統合サンプルの展開ガイドライン (レガシ)
description: この記事では、Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) から、チェコ共和国向け会計統合サンプルを展開するためのガイドラインを提供します。
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7406a6443f851fcfa9757deed57c108ba7b6e069
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473907"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-the-czech-republic-legacy"></a>チェコ共和国向け会計登録サービス統合サンプルの展開ガイドライン (レガシ)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> この記事のガイドラインに 従う必要があるのは、Microsoft Dynamics 365 Commerce バージョン10.0.28以前を使用している場合のみです。 Commerce バージョン 10.0.29 では、チェコ共和国の会計登録サービス統合サンプルは、Commerce ソフトウエア開発キット (SDK) で提供されています。 詳細については、[チャネル コンポーネントの構成](./emea-cze-fi-sample.md#configure-channel-components) を参照してください。

この記事では、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) に Dynamics 365 Commerce Retail SDK から、チェコ共和国向け会計登録サービス統合サンプルを展開するためのガイドラインを提供します。 この会計統合サンプルの詳細については、[チェコ共和国向け会計登録サービス統合サンプル](emea-cze-fi-sample.md) を参照してください。 

チェコ共和国向け会計統合サンプルは Retail SDK の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。 このサンプルは、Commerce runtime (CRT) とハードウェア ステーションの拡張機能で構成されます。 このサンプルを実行する際は、CRT とハードウェア ステーション プロジェクトを変更して構築する必要があります。 この記事で説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

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
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>会計コネクタ拡張機能の有効化

[ハードウェア ステーション](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) または [POS レジスター](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) で会計コネクタ拡張機能を有効にできます。

### <a name="enable-hardware-station-extensions"></a>ハードウェア ステーション拡張機能を有効化する

ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** 配下の **HardwareStationSamples.sln** ソリューションを開きます。

#### <a name="efrsample-component"></a>EFRSample コンポーネント

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

### <a name="production-environment"></a>運用環境

前述の手順で、会計登録サービス統合サンプルの構成要素である拡張機能を有効化しました。 さらに、この手順に従って、Commerce コンポーネントを含む配置可能パッケージを作成し、それらのパッケージを運用環境に適用する必要があります。

1. **RetailSdk\\Assets** フォルダー配下にあるパッケージ構成ファイルに、次の変更を加えます。

    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsCzechia" />
        ```

    - **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

2. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 展開可能なパッケージに CRT 拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
4. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
5. [チェコ共和国向け Commerce の設定](emea-cze-fi-sample.md#set-up-commerce-for-the-czech-republic) で説明されている必要な設定タスクをすべて完了します。

## <a name="design-of-extensions"></a>拡張機能の設計

チェコ共和国向け会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいています。 会計統合ソリューションの設計に関する詳細は、[会計統合サンプル設計の概要](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して会計登録サービスからの応答を処理することです。

CRT 拡張機能は **Runtime.Extensions.DocumentProvider.EFRSample** です。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーに使用する単一の **DocumentProviderEFRFiscalCZE** 要求ハンドラーがあります。 これは会計登録サービスの会計ドキュメントを生成する際に使用します。

このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするのは次のイベントです: 販売、顧客前金口座、顧客手付金。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – この要求は会計登録サービスによる応答を返します。 この応答は保存できるように文字列形式にシリアル化されます。

#### <a name="configuration"></a>構成

構成ファイル **DocumentProviderFiscalEFRSampleCzech** は、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- VAT 率のマッピング
- 既定の VAT グループ
- 前金の VAT グループ

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計登録サービスと通信できます。

ハードウェア ステーション拡張機能は **HardwareStation.Extension.EFRSample** という名前です。 これは HTTP または HTTPS プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計登録サービスに送信します。 また、会計登録サービスから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EFRHandler** 要求ハンドラーは、会計登録サービスへの要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントを会計登録サービスに送信し、その応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求は会計登録サービスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求は会計登録サービスの初期化に使用します。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位 (ms) で表した時間。このコネクタは会計登録サービスからの応答を待機します。

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
