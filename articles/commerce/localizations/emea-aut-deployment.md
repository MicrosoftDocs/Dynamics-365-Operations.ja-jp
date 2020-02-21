---
title: オーストラリアのキャッシュ レジスターの配置ガイドライン
description: このトピックは、オーストリアのローカライズ用配置ガイドです。
author: AlexChern0v
manager: ezubov
ms.date: ''
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.search.region: Austria
ms.search.industry: Retail
ms.author: v-alexec
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b33979c98cf9f6e8436526850f17a33421698847
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004685"
---
# <a name="deployment-guidelines-for-cash-registers-for-austria"></a>オーストラリアのキャッシュ レジスターの配置ガイドライン

[!include[banner](../includes/banner.md)]

このトピックは、Dynamics 365 Commerce のオーストラリアでのローカライズを有効にする方法を示す配置ガイドです。 ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。 たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷し、追加の監査イベントを登録し、EFSTA システムと Electronical 会計登録ソフトウェアとの統合サンプルを含めることができます。 オーストリアのローカライズの詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md) を参照してください。

統合サンプルは、会計統合フレームワークに基づいて作成されました。 会計統合機能の詳細については、 [小売チャンネルの財政統合の概要](fiscal-integration-for-retail-channel.md) を参照してください。これらのサンプルは、市販ソフトウェア開発キット (SDK)の一部です。 SDK のインストールと使用方法についての詳細は、[Retail ソフトウェア開発キット (SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このローカライズは、Commerce runtime (CRT)、ハードウェア ステーション、および POS の拡張機能で構成されます。 このサンプルを実行するには、CRT、ハードウェア ステーション、および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Azure DevOps のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。

## <a name="development-environment"></a>開発環境

次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。

### <a name="crt-extension-components"></a>CRT 拡張コンポーネント

CRT サンプルには、CRT 拡張コンポーネントが含まれます。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\CommerceRuntime** にある、.CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample コンポーネント

1. **Runtime.Extensions.DocumentProvider.EFRSample** プロジェクトを探して、構築します。
2. **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** フォルダーで、**Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** アセンブリ ファイルを検索します。
3. アセンブリ ファイルを CRT 拡張機能フォルダーにコピーします。

    - **Commerce Scale Unit:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

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

    - **Commerce Scale Unit:** アセンブリを Microsoft インターネット インフォメーション サービス (IIS) Commerce Scale Unit のサイトがある場所の下の **\\bin\\ext** フォルダーにコピーします。
    - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

4. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail とコマース:** ファイル名は **commerceruntime.ext.config** で、IIS Retail とコマース サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

5. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="enable-microsoft-components"></a>Microsoft コンポーネントを有効にする

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 拡張コンフィギュレーション ファイルで CRT の変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="hardware-station-extension-components"></a>ハードウェア ステーション拡張コンポーネント

ハードウェア ステーション拡張コンポーネントは、ハードウェア ステーション サンプルに含まれています。 次の手順を完了するには、**RetailSdk\\SampleExtensions\\HardwareStation** にある、ソリューション、**HardwareStationSamples.sln.sln** を開きます。

#### <a name="efrsample-component"></a>EFRSample コンポーネント

1. **HardwareStation.Extension.EFRSample** プロジェクトを探して、構築します。
2. **Extension.EFRSample\\bin\\Debug** フォルダーで、以下のファイルを探します。

    - **Contoso.Commerce.HardwareStation.EFRSample.dll** アセンブリ
    - **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** アセンブリ

3. アセンブリ ファイルをハードウェア ステーション拡張機能フォルダーにコピーします。

    - **共有ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
    - **Modern POS の専用ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

4. 拡張コンフィギュレーション ファイルのハードウェア ステーションの拡張機能の **HardwareStation.Extension.config** が見つかりません。

    - **共有ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
    - **Modern POS の専用ハードウェア ステーション:** ファイルは、Modern POS クライアント ブローカーの場所にあります。

5. コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

2. **extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

3. ソリューションをリビルドします。
4. デバッガーでModern POS を実行し、機能をテストします。

### <a name="cloud-pos-extension-components"></a>クラウド POS 拡張コンポーネント

1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. **extensions.json**で、次の明細行を追加することによって拡張機能が読み込まれるようにします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

3. ソリューションをリビルドします。
4. **実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。

### <a name="set-up-required-parameters-in-headquarters"></a>バックオフィスで要求されるパラメーターを設定します

#### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効にするには、次の手順を使用してバックオフィスを設定します。 詳細については、[小売チャネルの会計統合の設定](./setting-up-fiscal-integration-for-retail-channel.md) を参照してください。

1. **コマース共有パラメーター**を開き、**全般**タブで**会計統合**を有効にします。
2. **Retail とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ** メニューを開きます。 RetailSdk からコネクタ構成を読み込みます。 ファイルは、SampleExtensions\HardwareStation\Extension.EFRSample\Configuration\ConnectorEFRSampleAustria.xml の下に保存されています。
3. **Retail とコマース \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** メニューを開きます。 RetailSdk からドキュメント プロバイダー コンフィギュレーションを読み込みます。

    コンフィギュレーション ファイルは **SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration** の下にあります:

    - DocumentProviderEFRSampleAustria.xml
    - DocumentProviderNonFiscalEFRSampleAustria.xml

4. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル**を開きます。 上記の手順からドキュメント プロバイダーごとに 2 つの新しいプロファイルを作成し、読み込まれたコネクタを選択します。 必要な場合は、データ マッピング設定を更新します。
5. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル**を開きます。 上記の手順から新しいプロファイルを作成し、読み込まれたコネクタを選択します。 必要な場合は、接続設定を更新します。
6. **Retail とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ**を開きます。 上記の手順からコネクタの機能プロファイルごとに 2 つの新しいグループを作成します。
7. **Retail とコマース \> チャネル設定 \> 会計統合 \> 登録プロセス**を開きます。 新しいプロセスを作成します。 上記の手順から両方のコネクタの機能グループを選択します。
8. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル**を開きます。 登録プロセスを有効化する、店舗にリンクされているプロファイルを選択します。 **会計登録プロセス** タブを展開します。上記の手順から作成された登録プロセスを選択します。 POS で非会計イベントの登録を有効にするには、**機能** クイック タブで **監査** プロパティを有効にします。
9. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル**を開きます。 会計プリンターの接続先のハードウェア ステーションにリンクされているプロファイルを選択します。 **会計周辺機器** を展開します。コネクタの技術的なプロファイルを選択します。

詳細については、[オーストリアの会計登録サービス統合サンプル](./emea-aut-fi-sample.md)を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。

1. [クラウド POS 拡張コンポーネント](#cloud-pos-extension-components)、またはこのトピックで既に見た[Modern POS 拡張コンポーネント](#modern-pos-extension-components)セクションで手順を完了します。
2. **RetailSdk\\Assets** folder フォルダーの下にあるパッケージ コンフィギュレーション ファイルに、次の変更を加えます。

    1. **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルの**構成**セクションに、次の行を追加します。

        ```xml  
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    2. **HardwareStation.Extension.config** 構成ファイルで、**合成** セクションに追加の行を追加します。

        ```xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        ```

3. **BuildTools\Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。

        ```xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample" />
        ```

4. Visual Studio utility 用に、MSBuild コマンド プロンプトを起動し 、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
5. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、 [小売の配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md)を参照してください。
6. [バックオフィスで要求されるパラメーターの設定](#set-up-required-parameters-in-headquarters) を完了します
