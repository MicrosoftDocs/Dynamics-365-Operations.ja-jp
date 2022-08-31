---
title: フランスのキャッシュ レジスターの配置ガイドライン
description: この記事では、フランスの Microsoft Dynamics 365 Commerce のローカライズで、キャッシュ レジスター機能を有効化する方法について説明します。
author: EvgenyPopovMBS
ms.date: 08/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: France
ms.author: josaw
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.18
ms.search.industry: Retail
manager: annbe
ms.openlocfilehash: f1fe4538e26c97bef72e289b22643d1d1d9c614b
ms.sourcegitcommit: 78d41eeef0a8a8e94ed502bd89778414231a31ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305164"
---
# <a name="deployment-guidelines-for-cash-registers-for-france"></a>フランスのキャッシュ レジスターの配置ガイドライン

[!include [banner](../includes/banner.md)]

> [!WARNING]
> この記事で説明されている手順を実装する必要があります (Commerce Version 10.0.28以前を使用している場合)。 バージョン10.0.29から、フランスで必要なすべての Commerce チャンネル コンポーネントがチェック ボックスから有効化されます。 Commerce Version 10.0.28 以前を使用している場合で、Commerce バージョン10.0.29 以降に移行する場合は、[Commerce Version 10.0.29 に移行する](#migrate-to-commerce-version-10029-or-later) の手順に従う必要があります。

この記事では、フランスの Microsoft Dynamics 365 Commerce のローカライズで、キャッシュ レジスター機能を有効化する方法について説明します。 ローカライズは、コンポーネントのいくつかの拡張機能で構成されます。 たとえば、拡張機能を使用すると、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、および販売時点管理 (POS) での支払取引の登録、販売取引のデジタル署名、およびローカルの形式で X および Z レポートの印刷を行えます。 フランスのローカライズの詳細については、 [フランスのキャッシュ レジスター機能](./emea-fra-cash-registers.md) を参照してください。 フランス向け Commerce の設定方法の詳細については、[フランス向け Commerce の設定](./emea-fra-cash-registers.md#set-up-commerce-for-france)を参照してください。

> [!NOTE]
> フランス向け Commerce キャッシュ レジスター機能のこのバージョンは、[会計統合フレームワーク](./fiscal-integration-for-retail-channel.md) に基づいています。 フランスのレガシー版デジタル署名サンプルについては、[フランスのキャッシュ レジスターの配置ガイドライン (レガシー)](./emea-fra-deployment.md) を参照してください。 レガシー版デジタル署名サンプルを使用する既存の環境でフランスの会計統合機能を有効にする方法のガイドラインについては、[フランスのレガシー Commerce 機能から移行する](./emea-fra-fi-migration.md)を参照してください。

## <a name="development-environment"></a>開発環境

次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。

### <a name="enable-commerce-runtime-extension-components"></a>Commerce Runtime 拡張コンポーネントの有効化

#### <a name="registerauditeventfrance-component"></a>RegisterAuditEventFrance コンポーネント

RegisterAuditEventFrance コンポーネントを有効にするには、次の手順に従います。

1. Commerce Runtime (CRT) の拡張コンフィギュレーション ファイルを検索します。

    - **小売サーバー:** ファイルは **commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) 小売サーバー サイトの場所の下にある **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventFrance" />
    ```

#### <a name="receiptsfrance-component"></a>ReceiptsFrance コンポーネント

ReceiptsFrance コンポーネントを有効にするには、次の手順に従います。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **小売 Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsFrance" />
    ```

#### <a name="xzreportsfrance-component"></a>XZReportsFrance コンポーネント

XZReportsFrance コンポーネントを有効にするには、次の手順に従います。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **小売 Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsFrance" />
    ```

#### <a name="restrictingshiftduration-component"></a>RestrictingShiftDuration コンポーネント

RestrictingShiftDuration コンポーネントを有効にするには、次の手順に従います。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **小売 Server:** ファイル名は **commerceruntime.ext.config** で、IIS Retail Server サイトがある場所の下の **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Modern POS 拡張コンポーネントの有効化

Modern POS 拡張コンポーネントを有効にするには、次の手順に従います。

1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできることを確認します。 また、**実行** コマンドを使用して、Visual Studio から Modern POS を実行できることを確認します。

    > [!NOTE]
    > Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。

1. **extensions.json** ファイルで、次の明細行を追加することによって読み込まれる必要のある拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/Receipts.FR"
            }, 
            {
                "baseUrl": "Microsoft/FifAuditEvent.FR"
            },
            {
                "baseUrl": "Microsoft/RestrictShiftDuration"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細について、またソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

1. ソリューションをリビルドします。
1. デバッガーでModern POS を実行し、機能をテストします。

### <a name="enable-cloud-pos-extension-components"></a>Cloud POS 拡張コンポーネントの有効化

Cloud POS 拡張コンポーネントを有効にするには、次の手順に従います。

1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできることを確認します。
1. **extensions.json** ファイルで、次の明細行を追加することによって読み込まれる必要のある拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/Receipts.FR"
            }, 
            {
                "baseUrl": "Microsoft/FifAuditEvent.FR"
            },
            {
                "baseUrl": "Microsoft/RestrictShiftDuration"
            }
        ]
    }
    ```

    > [!NOTE]
    > 詳細について、またソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。

1. ソリューションをリビルドします。
1. **実行** コマンドを使用してソリューションを実行し、Retail ソフトウェア開発キット (SDK) ハンドブックにある手順を実行します。

## <a name="production-environment"></a>運用環境

Commerce コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを運用環境で適用するには、以下の手順に従います。

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** パッケージ コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml 
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsFrance" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventFrance" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsFrance" />
    ```

1. **RetailSDK\\POS\\拡張機能** フォルダーの下にある **extensions.json** ファイルで、次の行を追加して POS 拡張機能を有効にします。

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/Receipts.FR"
            }, 
            {
                "baseUrl": "Microsoft/FifAuditEvent.FR"
            },
            {
                "baseUrl": "Microsoft/RestrictShiftDuration"
            }
        ]
    }
    ```

1. Visual Studio ユーティリティ用の MSBuild コマンド プロンプトを起動し、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
1. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。

## <a name="migrate-to-commerce-version-10029-or-later"></a>Commerce Version 10.0.29 以降に移行する

Commerce Version 10.0.28 以前を使用し、バージョン10.0.29 以降に移行する場合は、このセクションに説明されている手順が必要です。 Commerce 環境を正しく更新するには、次の手順に従う必要があります。

1. Commerce headquarters を更新します。
1. **機能管理** ワークスペースで、[フランス特有の機能](./emea-fra-cash-registers.md#enable-features-for-france) を有効にして、その変更をチャネルに配布します。
1. Commerce Runtime、クラウド POS、および Modern POS を更新し、フランスのレガシの拡張機能を除外します。
    - **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** ファイルの Commerce Runtime 拡張 :
        - Microsoft.Dynamics.Commerce.Runtime.ReceiptsFrance
        - Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventFrance
        - Microsoft.Dynamics.Commerce.Runtime.RestrictShiftDuration
        - Microsoft.Dynamics.Commerce.Runtime.XZReportsFrance
    - **extensions.json** ファイルの POS 拡張機能:
        - Microsoft/Receipts.FR
        - Microsoft/FifAuditEvent.FR
        - Microsoft/RestrictShiftDuration
        
