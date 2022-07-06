---
title: インドのキャッシュ レジスターの配置ガイドライン
description: この記事は、Commerce のインド向けローカライズ用配置ガイドです。
author: AlexChern0v
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: India
ms.search.industry: Retail
ms.author: jiaqia
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: b50f6890e1d6c452a3a8dab2f52412c32a4c79e7
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027076"
---
# <a name="deployment-guidelines-for-cash-registers-for-india"></a>インドのキャッシュ レジスターの配置ガイドライン

[!include [banner](../includes/banner.md)]

この記事は、インドの Dynamics 365 Commerce アプリのローカライズで商品及びサービス税 (GST) の要件を有効にする方法を示す配置ガイドです。 インドのローカライズの詳細については、[インド向けのキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。

> [!WARNING]
> - [新たに独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、インド向けの GST 統合には使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retailソフトウェア開発キット (SDK) の以前のバージョンを使用する必要があります。 今後のバージョンで、コマース ローカライズの新しい独立したパッケージと拡張モデルのサポートを計画しています。
> - 小売 SDK のダウンロードと使用方法については、 [小売 ソフトウェアの開発キット(SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

この機能は、Commerce Runtime (CRT)、ハードウェア ステーション、販売時点管理 (POS) で構成されます。 この機能を使用するには、CRT 拡張機能の構成を変更する必要があります。 POS プロジェクトを変更して構築する必要があります。 この記事で説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 どのファイルも変更されていない場合は、Microsoft Visual Studio Online (VSO) のようなソース管理システムを利用することを推奨します。

## <a name="prerequisites"></a>必要条件

Visual C++ 再頒布可能パッケージが GST 計算を実行するマシン上にあることを確認します。 クラウド POS、およびオンライン モードの Modern POS の場合、このマシンは Commerce Scale Unit です。 オフライン モードの Modern POS の場合、それは Modern POS マシン自身です。 パッケージをダウンロードする方法については、[Visual C++ 再頒布可能パッケージをダウンロード](https://www.microsoft.com/download/details.aspx?id=48145)を参照してください。

## <a name="development-environment"></a>開発環境

機能をテストして拡張できるように開発環境を設定するには、次の手順を実行します。

### <a name="the-crt-extension-components"></a>CRT 拡張コンポーネント

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Commerce Scale Unit:** ファイル名は **Commerceruntime.ext.config** で、Microsoft インターネット インフォメーション サービス (IIS) Commerce Scale Unit サイト下の **bin\\ext** フォルダーにあります。
    - **Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所の下にあります。

2. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > 上に示すように、拡張機能の順序を保持します。

    > [!WARNING]
    > **commerceruntime.config** および **CommerceRuntime.MPOSOffline.config** ファイルを編集してはいけません。 これらのファイルはカスタマイズのためのものではありません。

### <a name="the-commerce-scale-unit-extension-components"></a>Commerce Scale Unit の拡張コンポーネント

1. Commerce Scale Unit サイトがある場所の下にあるルート フォルダーの **web.config** ファイルを開きます。
2. コンフィギュレーション ファイルの **extensionComposition** セクションで拡張機能を登録します。

``` xml
<add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
```

### <a name="the-clientbroker-extension-components"></a>ClientBroker 拡張コンポーネント

1. ローカル CRT クライアント ブローカーの場所の下にある **RetailProxy.MPOSOffline.ext.config** を開きます。
2. コンフィギュレーション ファイルの **extensionComposition** セクションで、プロキシ拡張機能を登録します。

``` xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
```

### <a name="the-modern-pos-extension-components"></a>Modern POS 拡張コンポーネント

税登録の ID 拡張機能を有効にするには、次の手順に従います。

1. **RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、Modern POS が Run コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。 (Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 [UAC] を有効にして、以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)
2. **POS.Extensions\extensions.json** ファイルで、次の行を追加することによって拡張機能を有効にします:

    ``` xml
    {
        "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. ソリューションをビルドします。
4. Modern POS を実行し、機能をテストします。

### <a name="the-cloud-pos-extension-components"></a>クラウド POS 拡張コンポーネント

税登録の ID 拡張機能を有効にするには、次の手順に従います。

1. **RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
2. **POS.Extensions\extensions.json** で、次の行を追加することによって拡張機能を有効にします。

    ``` xml
    {
        "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

3. ソリューションをビルドします。
4. クラウド POS を実行し、機能をテストします。

### <a name="set-up-required-parameters-in-headquarters"></a>バックオフィスで要求されるパラメーターを設定します

詳細については、[インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) を参照してください。

## <a name="production-environment"></a>運用環境

以下の手順に従い、コンポーネントを含む配置可能パッケージを作成して、パッケージを運用環境で適用します。

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdIndia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.GenericTaxEngine" />
    ```

    > [!IMPORTANT]
    > 上に示すように、拡張機能の順序を保持します。

2. **RetailSdk\\Assets** フォルダーの下の **RetailProxy.MPOSOffline.ext.config** コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.RetailProxy.TaxRegistrationIdIndia" />
    ```

3. Web のコンフィギュレーション ファイルを更新します。 **RetailSDK\Packages\RetailServer\Code\web.config** ファイルの **extensionComposition** セクションに次の行を追加します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Retail.RetailServer.TaxRegistrationIdIndia" />
    ```

4. **RetailSDK\POS\Extensions\extensions.json** ファイルで、以下の行を追加して税登録の ID POS 拡張機能を有効にします:

    ``` xml
    {
        "baseUrl": "Microsoft/TaxRegistrationId.IN"
    }
    ```

5. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
6. LCS 経由または手動でパッケージを適用します。 詳細については、 [小売の配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
