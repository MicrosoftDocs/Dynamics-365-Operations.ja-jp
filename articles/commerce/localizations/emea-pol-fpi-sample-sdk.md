---
title: ポーランド向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)
description: この記事では、Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) からポーランド向け会計プリンターの統合サンプルを展開するためのガイドラインを提供します。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 883f09f73e3b372d6896b6702e54e2e664cff4d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286529"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>ポーランド向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で Microsoft Dynamics 365 Commerce Retail ソフトウェア開発キット (SDK) から、ポーランド向け会計プリンター統合サンプルを展開するためのガイドラインを提供します。 この会計統合サンプルの詳細については、[ポーランド向け会計プリンター統合サンプル](emea-pol-fpi-sample.md) を参照してください。 

ポーランド向け会計統合サンプルは、Retail SDK の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。 このサンプルは、Commerce runtime (CRT) とハードウェア ステーションの拡張機能で構成されます。 このサンプルを実行する際は、CRT とハードウェア ステーション プロジェクトを変更して構築する必要があります。 この記事で説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

### <a name="commerce-runtime-extension-components"></a>Commerce Runtime 拡張機能コンポーネント

Retail SDK は CRT 拡張機能コンポーネントを含みます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** で **CommerceRuntimeSamples.sln** ソリューションを開きます。

1. **Runtime.Extensions.DocumentProvider.PosnetSample** プロジェクトを探して、ビルドします。
2. **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします:

    - **Commerce Scale Unit:** ファイルをインターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Commerce サービスを再起動します:

    - **Commerce Scale Unit:** IIS マネージャから Commerce のサービス サイトを再起動します。
    - **クライアント ブローカー:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。

### <a name="hardware-station-extension-components"></a>ハードウェア ステーション拡張コンポーネント

Retail SDK はハードウェア ステーション拡張機能コンポーネントを含みます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** 配下の **HardwareStationSamples.sln** ソリューションを開きます。

1. **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** プロジェクトを探して、ビルドします。
2. **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを配置したハードウェア ステーション マシンにコピーします。

    - **リモート ハードウェア ステーション:** ファイルを、IIS ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。 プリンター ドライバ ライブラリ (**libposcmbth.dll**, **libcmbth\_serial.dll** と **cmbth\_pl.lng**) をコピーします。

4. ハードウェア ステーションの拡張機能の構成ファイルを見つけます。 ファイルの名前は **HardwareStation.Extension.config** です。

    - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。

5. 構成ファイルの **構成** セクションに、次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. ハードウェア ステーション サービスを再起動します。

    - **リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。

## <a name="production-environment"></a>運用環境

前述の手順では、会計登録サービス統合サンプルの構成要素である拡張機能を有効にしました。 さらに、この手順に従って、Commerce コンポーネントを含む配置可能パッケージを作成し、それらのパッケージを運用環境に適用する必要があります。

1. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの **構成** セクションに、次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 展開可能なパッケージに CRT 拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
1. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。

## <a name="design-of-extensions"></a>拡張機能の設計

ポーランド向け会計プリンター統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいています。 会計統合ソリューションの設計に関する詳細は、[会計統合サンプル設計の概要](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、プリンターに特化したドキュメントを生成して会計プリンターからの応答を処理することです。

CRT 拡張子は **Runtime.Extensions.DocumentProvider.PosnetSample** です。 この拡張機能は、POSNET 仕様 19-3678 で定義されている JavaScript Object Notation (JSON) 形式のプリンタ固有のコマンドセットを生成します。

会計統合ソリューションの設計については、[会計デバイスとサービスの会計登録プロセスおよび会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) を参照してください。

#### <a name="request-handler"></a>要求ハンドラー

**DocumentProviderPosnetProtocol** 要求ハンドラーは、会計プリンタからドキュメントを生成するリクエストのエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計プリンターに登録するべきプリンター固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするイベントを次に示します: 販売、X レポートの印刷、Z レポートの印刷。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーにあります。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- VAT 率のマッピング
- 支払/入金タイプのマッピング
- 預金の支払タイプ

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計プリンターと通信できます。

ハードウェア ステーションの拡張機能は **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** にあります。 この拡張機能は、POSNET ドライバの機能を呼び出して、CRT の拡張機能が生成したコマンドを会計プリンターに送信します。 また、デバイス エラーも処理します。

#### <a name="request-handler"></a>要求ハンドラー

**FiscalPrinterHandler** リクエスト ハンドラーは、会計の周辺機器への要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントをプリンターに送信し、会計プリンターからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求はデバイスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求はプリンターの初期化に使用します。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーに存在します。 このファイルによって、Commerce Headquarters からコネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **接続文字列** – デバイスへの接続の詳細を、ドライバーがサポートしているフォーマットで記述した文字列です。 詳細については、POSNET ドライバーのドキュメントを参照してください。
- **日時の同期** – プリンターの日時を接続したハードウェア ステーションと同期する必要があるかどうかを指定する値。
- **デバイスのタイムアウト** – ドライバーがデバイスからの応答を待機する時間を、ミリ秒単位 (ms) で表します。 詳細については、POSNET ドライバーのドキュメントを参照してください。
