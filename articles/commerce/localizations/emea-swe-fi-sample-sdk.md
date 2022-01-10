---
title: スウェーデン向け制御ユニットプリンター統合サンプルの配置ガイドライン (レガシ)
description: このトピックでは、 Retail SDK による、スウェーデン向け制御ユニット登録サービス統合サンプルの展開ガイドラインを提供します
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: c0e301305fb0d99ab2f8c811f9f560bc5008e02b
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944893"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>スウェーデン向け制御ユニットプリンター統合サンプルの配置ガイドライン (レガシ)

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) を利用した  Retail ソフトウェア開発キット (SDK) による、スウェーデン向け制御ユニット統合サンプルの展開ガイドラインを提供します。 この会計統合サンプルの詳細については、[スウェーデン向け制御ユニット統合サンプル](emea-swe-fi-sample.md) を参照してください。 

スウェーデン向け会計統合サンプルは、Retail SDK の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。 このサンプルは、Commerce Runtime (CRT)、ハードウェア ステーション、販売時点管理 (POS) で構成されます。 このサンプルを実行するには、CRT、ハードウェア ステーション、および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

### <a name="enable-crt-extensions"></a>CRT 拡張機能の有効化

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** で **CommerceRuntimeSamples.sln** ソリューションを開きます。

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample コンポーネント

1. **Runtime.Extensions.DocumentProvider.CleanCashSample** プロジェクトを探して、ビルドします。
2. **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** ファイルをインターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>拡張機能の構成ファイル

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>ハードウェア ステーション拡張機能を有効化する

ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** 配下の **HardwareStationSamples.sln** ソリューションを開きます。

#### <a name="cleancash-component"></a>CleanCash コンポーネント

1. **HardwareStation.Extension.CleanCashSample** プロジェクトを探して、ビルドします。
2. **Extension.CleanCashSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.HardwareStation.CleanCashSample.dll** と **Interop.CleanCash\_1\_1.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。

    - **共有ハードウェア ステーション:** ファイルを、IIS ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
    - **Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

4. ハードウェア ステーションの拡張機能に対する拡張機能構成ファイルを見つけます。 ファイルの名前は **HardwareStation.Extension.config** です。

    - **共有ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所にあります。
    - **Modern POS の専用ハードウェア ステーション:** このファイルは Modern POS クライアントのブローカーの場所にあります。

5. 構成ファイルの **構成** セクションに、次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Modern POS 拡張コンポーネントの有効化

1. **RetailSdk\\POS** 配下の **ModernPOS.sln** ソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**実行** コマンドを使用して、Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

2. **extensions.json** ファイルに以下の行を追加して、読み込む必要のあるエクステンションを有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

3. ソリューションをリビルドします。
4. デバッガーでModern POS を実行し、機能をテストします。

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS 拡張コンポーネントの有効化

1. **RetailSdk\\POS** 配下の **CloudPOS.sln** ソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. **extensions.json** ファイルに以下の行を追加して、読み込む必要のあるエクステンションを有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

3. ソリューションをリビルドします。
4. **実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。

## <a name="production-environment"></a>実稼働環境

前述の手順で、制御ユニット統合サンプルの構成要素である拡張機能を有効化しました。 さらに、この手順に従って、Commerce コンポーネントを含む配置可能パッケージを作成し、それらのパッケージを実稼働環境に適用する必要があります。

1. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 展開可能なパッケージに CRT 拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. **RetailSDK\\POS\\Extensions** 配下の **extensions.json** ファイルで、以下の行を追加して POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
5. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
6. [制御ユニットとの統合設定](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) で説明されている必要な設定タスクをすべて完了します。

## <a name="design-of-the-extensions"></a>拡張機能の設計

### <a name="crt-extension-design"></a>CRT 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して制御ユニットからの応答を処理することです。

CRT 拡張機能は **Runtime.Extensions.DocumentProvider.CleanCashSample** です。

会計統合ソリューションの設計については、[会計デバイスの会計登録プロセスおよび会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) を参照してください。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーに使用する単一の **DocumentProviderCleanCash** 要求ハンドラーがあります。 このハンドラーは、制御ユニットの会計ドキュメントを作成するために使用されます。

このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは制御ユニットに登録するべきサービス固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在、販売イベントと監査イベントがサポートされています。

#### <a name="configuration"></a>構成

構成ファイル **DocumentProviderFiscalCleanCashSample** は、拡張機能プロジェクトの **構成** フォルダーにあります。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- VAT コードのマッピング

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、制御ユニットと通信できます。

ハードウェア ステーション拡張機能は **HardwareStation.Extension.CleanCashSample** です。 これは HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを制御ユニットに送信します。 また、制御ユニットから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**CleanCashHandler** 要求ハンドラーは、制御ユニットに対する要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – このリクエストは、制御ユニットにドキュメントを送信し、制御ユニットからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求は制御ユニットの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求は、制御ユニットの初期化に使用されます。

#### <a name="configuration"></a>構成

構成ファイルは、拡張機能プロジェクトの **構成** フォルダーにあります。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **接続文字列** - 制御ユニットの接続設定。
- **タイムアウト** – ドライバーが制御ユニットからの応答を待機する時間を、ミリ秒単位で表します。

## <a name="migrating-from-the-earlier-integration-sample"></a>以前の統合サンプルからの移行

[スウェーデン向けの制御ユニットと POS の統合に以前のサンプル](retail-sdk-control-unit-sample.md)を使用している場合、そのサンプルから現在の統合サンプルに移行する必要があるかもしれません。 この変更を受けて、今後のスウェーデン向け機能の更新をタイムリーに受けるためには、アップグレードしたり、構築した拡張機能のコードや設定を微調整したり、ソリューションを再構築する必要があるかもしれません。 作成した拡張機能のロジックを大きく変更する必要はありません。 何も変更しなければ、以前の統合サンプルと既存のカスタマイズは引き続き動作します。 そのため、自分の環境に合わせて計画し、準備し、取り込みすることができます。

### <a name="migration-process"></a>移行プロセス

以前の統合サンプルから現在の制御ユニット統合サンプルへの移行は、段階的なアップデートのコンセプトに基づく必要があります。 つまり、POS やハードウェア ステーションのコンポーネントのアップデートを始める前に、Commerce 本部と Commerce Scale Unit のコンポーネントは全て既にアップデートされている必要があります。

イベントやトランザクションが二重に署名されてしまう (以前の拡張機能と現在の拡張機能の両方で署名されてしまう) 状況や、設定が不足しているためにイベントやトランザクションが署名されない状況を防ぐには、以前のサンプルを使用しているすべての POS とハードウェア ステーション機器の電源を切ってから、同時にアップデートすることをお勧めします。 この同時更新は、例えば、店舗の機能プロファイルとハードウェア ステーションのハードウェア プロファイルを更新することで、店舗ごとに行うことができます。

移行のプロセスは以下のステップで構成されています。

1. Commerce 本部のコンポーネントを更新します。
1. Commerce Scale Unit のコンポーネントを更新し、現在のサンプルの拡張機能を有効にします。
1. オフライン対応の MPOS デバイスから、すべてのオフライン トランザクションが同期されていることを確認してください。
1. 前述のサンプルのコンポーネントを使用しているすべてのデバイスをオフにします。
1. [制御ユニットとの統合設定](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) で説明されている必要な設定タスクをすべて完了します。
1. POS とハードウェア ステーションのコンポーネントを更新し、以前のサンプルの一部である拡張機能を無効にし、現在のサンプルの拡張機能を有効にします。

    > [!NOTE]
    > 環境の種類に応じて、このトピックの[開発環境での移行](#migration-in-a-development-environment)または[本番環境での移行](#migration-in-a-production-environment)セクションのいずれかで、移行プロセスに関する技術的な詳細を確認することができます。

### <a name="migration-in-a-development-environment"></a>開発環境での移行

#### <a name="update-crt"></a>CRT の更新

1. **Runtime.Extensions.DocumentProvider.CleanCashSample** プロジェクトを探して、ビルドします。
2. **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** ファイルを IIS Commerce Scale Unit サイトの場所の配下にある **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** ファイルをローカル CRT クライアント ブローカーがある場所の下の **\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **CommerceRuntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Modern POS上のローカル CRT :** ファイルは、ローカル CRT クライアントブローカーが格納されている場所の **bin\\ext** フォルダに、 **CommerceRuntime.MPOSOffline.Ext.config** という名前で作成されています。

    > [!WARNING]
    > CommerceRuntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

5. 拡張機能構成ファイルから古い CRT拡張子を見つけて削除します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > この CRT インスタンスで動作するすべての POS デバイスを更新するまでは、このステップを完了しないでください。

6. 拡張機能設定ファイルに以下の行を追加して、現在のサンプル CRT 拡張機能を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>ハードウェア ステーションの更新

1. **HardwareStation.Extension.CleanCashSample** プロジェクトを探して、ビルドします。
2. **Extension.CleanCashSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.HardwareStation.CleanCashSample.dll** と **Interop.CleanCash\_1\_1.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。

    - **共有ハードウェア ステーション:** ファイルを、IIS ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
    - **Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

4. **HardwareStation.Extension.config** 拡張機能の構成ファイルを探します:

    - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所にあります。
    - **Modern POS のローカル ハードウェア ステーション:** このファイルは Modern POS クライアントのブローカーの場所にあります。

    > [!WARNING]
    > CommerceRuntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

5. 拡張子構成ファイルから以前のハードウェアステーションの拡張機能を探して削除します。

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 以前](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. 拡張機能構成ファイルの **合成** セクションに、次の行を追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Modern POS の更新

1. **RetailSdk\\POS** 配下の **CloudPOS.sln** ソリューションを開きます。
2. **extensions.json** ファイルから以下の行を削除することで、以前の POS 拡張機能を無効にします。

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. **extensions.json** ファイルに以下の行を追加して、現在のサンプル POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>クラウド POS の更新

1. **RetailSdk\\POS** 配下の **ModernPOS.sln** ソリューションを開きます。
2. **extensions.json** ファイルから以下の行を削除することで、以前の POS 拡張機能を無効にします。

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. **extensions.json** ファイルに以下の行を追加して、現在のサンプル POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>運用環境での移行

#### <a name="update-crt"></a>CRT の更新

1. **RetailSdk\\Assets** フォルダ内の **CommerceRuntime.ext.config** と **CommerceRuntime.MPOSOffline.Ext.config** の構成ファイルから、古い CRT 拡張機能を削除します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > この CRT インスタンスで動作するすべての POS デバイスを更新するまでは、このステップを完了しないでください。

2. **RetailSdk\\Assets** フォルダ配下の **CommerceRuntime.ext.config** と **CommerceRuntime.MPOSOffline.Ext.config** の構成ファイルを以下のように変更して、現在のサンプル CRT の拡張機能を有効にします。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. **BuildTools** フォルダの下にある **Customization.settings** パッケージ カスタマイズ設定ファイルに、以下の行を追加して、展開可能なパッケージに現在のサンプルの CRT 拡張機能を含めます。

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>ハードウェア ステーションの更新

1. **HardwareStation.Extension.config** の設定ファイルを変更することで、以前のハードウェア ステーションの拡張子を削除します。

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 以前](#tab/retail-7-3)

    **HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルから以下のセクションを削除します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

    **HardwareStation.Extension.config** 構成ファイルから以下のセクションを削除します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

    **HardwareStation.Extension.config** 構成ファイルから以下のセクションを削除します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. **HardwareStation.Extension.config** 構成ファイルの **composition** セクションに以下の行を追加して、現在のサンプル ハードウェア ステーションの拡張を有効にします。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. **BuildTools** フォルダー配下の **Customization.settings** パッケージ カスタマイズ構成ファイルに、次の変更を加えます。

    - 次の行を削除して、以前のハードウェア ステーションの拡張機能を展開可能なパッケージから除外します。

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - 以下の行を追加して、現在のサンプルのハードウェア ステーション拡張機能を展開可能なパッケージに追加します。

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Modern POS の更新

1. **RetailSdk\\POS** の **CloudPOS.sln** ソリューションを開きます。
2. 古い POS 拡張機能を無効にします:

    - **tsconfig.json** ファイルで、除外リストに **FiscalRegisterSample** フォルダを追加します。
    - **RetailSDK\\POS\\拡張機能** フォルダの下にある **extensions.json** ファイルから次の行を削除します。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. **RetailSDK\\POS\\Extensions** 配下の **extensions.json** ファイルで、以下の行を追加して現在のサンプル POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>クラウド POS の更新

1. **RetailSdk\\POS** 配下の **ModernPOS.sln** ソリューションを開きます。
2. 古い POS 拡張機能を無効にします:

    - **tsconfig.json** ファイルで、除外リストに **FiscalRegisterSample** フォルダを追加します。
    - **RetailSDK\\POS\\拡張機能** フォルダの下にある **extensions.json** ファイルから次の行を削除します。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. **RetailSDK\\POS\\Extensions** 配下の **extensions.json** ファイルで、以下の行を追加して現在のサンプル POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>配置可能パッケージの作成

Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。 LCS 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
