---
title: イタリア向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)
description: このトピックでは、Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) による、イタリア向け会計プリンターの統合サンプルの展開ガイドラインを提供します。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 93aca34239affb41998f4309d7c03f29f7b5f003
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076889"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>イタリア向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) を利用した Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) による、イタリア向け会計プリンター統合サンプルの展開ガイドラインを提供します。 この会計統合サンプルの詳細については、[イタリア向け会計プリンター統合サンプル](emea-ita-fpi-sample.md) を参照してください。 

イタリア向け会計統合サンプルは、Retail SDK の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。 このサンプルは、Commerce runtime (CRT) とハードウェア ステーションの拡張機能で構成されます。 このサンプルを実行する際は、CRT とハードウェア ステーション プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime 拡張機能コンポーネント

Retail SDK は CRT 拡張機能コンポーネントを含みます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** で **CommerceRuntimeSamples.sln** ソリューションを開きます。

1. **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** プロジェクトを探して、構築します。
2. **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** アセンブリ ファイルを見つけます。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** ファイルをインターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Commerce Scale Unit を再起動する

    - **Commerce Scale Unit:** IIS マネージャーから Commerce Scale Unit サイトを再起動します。
    - **クライアント ブローカー:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。

### <a name="hardware-station-extension-components"></a>ハードウェア ステーション拡張コンポーネント

Retail SDK はハードウェア ステーション拡張機能コンポーネントを含みます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** 配下の **HardwareStationSamples.sln** ソリューションを開きます。

1. **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** プロジェクトを見つけて構築します。
2. **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll** アセンブリ ファイルを見つけます。
3. アセンブリ ファイルを配置したハードウェア ステーション マシンにコピーします。

    - **リモート ハードウェア ステーション:** ファイルを、IIS ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
    - **ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

4. ハードウェア ステーションの拡張機能の構成ファイルを見つけます。 ファイルの名前は **HardwareStation.Extension.config** です。

    - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
    - **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

5. 構成ファイルの **合成** セクションに、次のセクションを追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. ハードウェア ステーション サービスを再起動します。

    - **リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。
    - **ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。

## <a name="production-environment"></a>実稼働環境

Commerce コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用するには、以下の手順に従います。

1. このトピックの前半にある [開発環境](#development-environment) セクションで説明した手順を完了します。
2. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 展開可能なパッケージに CRT 拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Visual Studio ユーティリティを MSBuild コマンド プロンプトで起動してから、Retail SDK フォルダー配下で **msbuild** を実行し、展開可能なパッケージを作成します。
5. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。

## <a name="design-of-extensions"></a>拡張機能の設計

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、プリンターに特化したドキュメントを生成して会計プリンターからの応答を処理することです。

CRT 拡張機能は **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** です。

会計統合ソリューションの設計については、[会計デバイスとサービスの会計登録プロセスおよび会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

#### <a name="request-handler"></a>要求ハンドラー

**DocumentProviderEpsonFP90III** 要求ハンドラーは、会計プリンタからドキュメントを生成するリクエストのエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計プリンターに登録するべきプリンター固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするイベントを次に示します: 販売、X レポートの印刷、Z レポートの印刷。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- VAT コードのマッピング
- VAT 率のマッピング
- 支払/入金タイプのマッピング
- 領収書番号のバーコード タイプ
- 預金の支払タイプ

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計プリンターと通信できます。

ハードウェア ステーションの拡張機能は **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample** です。 この拡張機能は HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計プリンターに送信します。 また、会計プリンターから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EpsonFP90IIISample** 要求ハンドラーは、会計の周辺機器への要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントをプリンターに送信し、会計プリンターからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求はデバイスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求はプリンターの初期化に使用します。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters からコネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **エンドポイント アドレス** – プリンターの URL。
- **日時の同期** – プリンターの日時を接続したハードウェア ステーションと同期する必要があるかどうかを指定する値。
