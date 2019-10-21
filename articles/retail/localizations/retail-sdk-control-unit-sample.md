---
title: スウェーデン用の管理単位との Retail POS の統合
description: このトピックは、スウェーデンの管理単位統合サンプルのビルドとインストールのガイドです。
author: EvgenyPopovMBS
manager: Annbe
ms.date: 02/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Sweden
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 01966f56dba1dc9e83b9f246eae44899b7c4c059
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025396"
---
# <a name="sample-for-retail-pos-integration-with-control-units-for-sweden"></a>スウェーデン用の管理単位との Retail POS の統合

[!include [banner](../includes/banner.md)]

**サンプル コードの通知**

**このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。**

**技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。**

このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Dynamics 365 Retail 拡張機能を作成する方法を示します。 特に、このサンプルには Retail POS をスウェーデンの管理単位と統合するコードが含まれています。 たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。 CleanCash® API のバージョン1.1.4 が使用されます。 API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。

このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。 Retail SDK をダウンロードして使用する方法については、[Retail SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。 このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。

> [!NOTE]
> 使用しているバージョンによって、このトピックの手順の一部が異なります。 詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

1. ハードウェア ステーション コンポーネントを拡張します。

    1. **RetailSDK\\SampleExtensions\\HardwareStation**から ハードウェア ステーション ソリューションを開きます。
    2. **HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。
    3. 拡張機能アセンブリおよび設定を検索します。

        # <a name="retail-73-and-earliertabretail-7-3"></a>[Retail 7.3 以前](#tab/retail-7-3)

        **Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。

        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション
        - **Interop.CleanCash\_1\_1.dll** アセンブリ

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        **Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。

        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション
        - **Interop.CleanCash\_1\_1.dll** アセンブリ

        # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        **Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。

        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション

        **RetailSDK\\References\\Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1\\lib\\net451** にて次のファイルを検索します。

        - **Interop.CleanCash\_1\_1.dll** アセンブリ

        ---

    4. ファイルを配置した ハードウェア ステーション マシンにコピーします。

        - **リモート ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
        - **ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

    5. ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。

        # <a name="retail-73-and-earliertabretail-7-3"></a>[Retail 7.3 以前](#tab/retail-7-3)

        - **リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config**で、IIS ハードウェア ステーション サイトの場所にあります。
        - **ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config**で、Modern POS クライアント ブローカーの場所にあります。

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        ファイルの名前は **HardwareStation.Extension.config** です。

        - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
        - **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

        # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        ファイルの名前は **HardwareStation.Extension.config** です。

        - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
        - **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

        ---

    6. コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。

        # <a name="retail-73-and-earliertabretail-7-3"></a>[Retail 7.3 以前](#tab/retail-7-3)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```

        ---

    7. ハードウェア ステーション サービスを再起動します。

        - **リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。
        - **ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。

2. CRT コンポーネントの拡張。

    1. **RetailSdk\\SampleExtensions\\CommerceRuntime** 配下の、 CRT ソリューション、 **CommerceRuntimeSamples.sln** を開きます。
    2. **Runtime.Extensions.FiscalRegisterReceiptSample** プロジェクトを探して、構築します。
    3. CRT の ext.config ファイルを検索します。

        - **Retail Server:** : ファイルは IIS 小売サーバー が格納されている場所の **bin\\ext** フォルダー 配下に **commerceRuntime.ext.config** という名前で作成されています。
        - **Modern POS上のローカル CRT :** ファイルは、ローカル CRT クライアントブローカーが格納されている場所の **bin\\ext** フォルダ配下に、 **CommerceRuntime.MPOSOffline.Ext.config** という名前で作成されています。

    4. コンフィギュレーション ファイルで CRT の変更を登録します。

        ``` xml
        <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
        ```

        > [!NOTE]
        > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

    5. **Extensions.FiscalRegisterReceiptSample\\bin\\Debug** で、 **Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** アセンブリを検索します。
    6. アセンブリを CRT 拡張機能フォルダーにコピーします。

        - **小売りサーバー:** アセンブリを IIS Retail Server が格納されている場所の配下にある **\\bin\\ext** フォルダーにコピーします。
        - **Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。

        > [!NOTE]
        > CRT および Retail サーバーに対するコードの変更はすべて、RetailSdk\\SampleExtensions の一部となります。 したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。

3. Modern POS コンポーネントの拡張。

    1. **RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、Modern POS が **Run** コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。 (Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 \[UAC\] を有効にし、必要に応じて既にインストールされている Modern POS のインスタンスをアンインストールする必要があります。
    2. **Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。
    3. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    4. 以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    5. ソリューションをリビルドします。
    6. デバッガーでModern POS を実行し、機能をテストします。

4. クラウド POS コンポーネントの拡張。

    1. **RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
    2. **Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。
    3. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    4. 以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    5. ソリューションをリビルドします。
    6. **実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。
    7. 機能をテストします。

5. 小売用バックオフィスで、会計登録構成と、その他の必要なパラメーターを設定します。 詳細については、「[スウェーデンのキャッシュ レジスター](emea-swe-cash-registers.md)」を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、実稼働環境で小売コンポーネントを含む配置可能パッケージを作成して適用します。

1. POS コンポーネントの拡張

    1. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    2. 以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

2. **RetailSdk\\Assets** フォルダのパッケージ構成ファイルに、次の変更を加えます。

    1. **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次のセクションを追加します。

        ``` xml
        <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
        ```

    2. ハードウェア ステーション構成ファイルの **構成** セクションに、次のセクションを追加します。

        # <a name="retail-73-and-earliertabretail-7-3"></a>[Retail 7.3 以前](#tab/retail-7-3)

        **HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-latertabretail-7-3-1"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        **HardwareStation.Extension.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```
        
        # <a name="retail-100-and-latertabretail-10-0"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        **HardwareStation.Extension.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```

        ---

3. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
4. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
