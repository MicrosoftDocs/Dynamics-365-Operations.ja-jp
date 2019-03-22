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
ms.reviewer: shylaw
ms.search.scope: Operations, Retail
ms.search.region: Sweden
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: 958285e4dbbee486d92c171d52356199c12cdf4f
ms.sourcegitcommit: 0e01d3907b70261aee2df3e3ce0dde2f1343a43a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/27/2019
ms.locfileid: "770170"
---
# <a name="sample-for-retail-pos-integration-with-control-units-for-sweden"></a>スウェーデン用の管理単位との Retail POS の統合

[!include [banner](../includes/banner.md)]

**サンプル コードの通知**

**このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。**

**技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。**

このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Microsoft Dynamics 365 for Retail 拡張機能を作成する方法を示します。 特に、このサンプルには Microsoft Dynamics for Retail POS をスウェーデンの管理単位と統合するコードが含まれています。 たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。 CleanCash® API のバージョン1.1.4 が使用されます。 API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。

このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。 Retail SDK をダウンロードして使用する方法については、[Retail SDK ドキュメント](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。 このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。 このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 また Microsoft Visual Studio オンライン (VSO) のような、どのファイルも変更されていないソース管理システムを使用することをお勧めします。


> [!NOTE]
> 使用している Microsoft Dynamics 365 for Retail のバージョンによって、このトピックの手順の一部が異なります。 詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

1. ハードウェア ステーション コンポーネントを拡張します。

   1. **RetailSDK\SampleExtensions\HardwareStation** で ハードウェア ステーション ソリューションを開きます。
   2. **HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。
   3. **Extension.FiscalRegisterSample\bin\Debug** で以下のファイルを検索します。

       - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
       - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション
       - **Interop.CleanCash_1_1.dll** アセンブリ

   4. ファイルを配置した ハードウェア ステーション マシンにコピーします。

       - **リモート ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。
       - **ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。

   5. ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。

      # <a name="retail-73-and-earliertabretail-7-3"></a>[Retail 7.3 以前](#tab/retail-7-3)

      **リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config**で、IIS ハードウェア ステーション サイトの場所にあります。

      **ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config**で、Modern POS クライアント ブローカーの場所にあります。

      # <a name="retail-731-and-latertabretail-7-3-1"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

      ファイルの名前は **HardwareStation.Extension.config** です。

      **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。

      **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

    ---

    6. コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

    7. ハードウェア ステーション サービスを再起動します。

        - **リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。
        - **ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。

2. CRT コンポーネントの拡張。

   1. **RetailSdk\SampleExtensions\CommerceRuntime** の下の、CRT ソリューション、**CommerceRuntimeSamples.sln** を開きます。
   2. **Runtime.Extensions.FiscalRegisterReceiptSample** プロジェクトを探して、構築します。
   3. CRT の ext.config ファイルを検索します。

       - **小売サーバー:** ファイルは **commerceRuntime.ext.config** で、IIS 小売サーバー サイトの場所の下の **bin\ext** フォルダーにあります。
       - **Modern POS のローカル CRT:** ファイルの名前は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所の **bin\ext** フォルダーにあります。

   4. コンフィギュレーション ファイルで CRT の変更を登録します。

       ``` xml
       <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
       ```

       > [!NOTE]
       > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。 これらのファイルはカスタマイズのためのものではありません。

   5. **Extensions.FiscalRegisterReceiptSample\bin\Debug** で、**Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** アセンブリを検索します。
   6. アセンブリを CRT 拡張機能フォルダーにコピーします。

       - **Retail サーバー:** IIS 小売サーバー サイトの場所の **\bin\ext** フォルダーにコピーします。
       - **Modern POS 上のローカル CRT:** アセンブリをローカル CRT クライアント ブローカーの場所の下の **\ext** フォルダーにコピーします。

      > [!NOTE]
      > CRT と Retail サーバーのすべてのコードの変更は、RetailSdk\SampleExtensions の一部です。 したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。

3. Modern POS コンポーネントの拡張。

    1. **RetailSdk\POS\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。 また、Modern POS が **Run** コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。 (Modern POS をカスタマイズしないでください。 ユーザー アカウント制御 [UAC] を有効にして、必要に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。)
    2. **Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。
    3. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    3. 適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. ソリューションをリビルドします。
    5. デバッガーでModern POS を実行し、機能をテストします。

4. クラウド POS コンポーネントの拡張。

    1. **RetailSdk\POS\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。
    2. **Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。
    3. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    3. 適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    4. ソリューションをリビルドします。
    5. **実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。
    6. 機能をテストします。

5. 小売用バックオフィスで、会計登録構成と、その他の必要なパラメーターを設定します。 詳細については、「[スウェーデンのキャッシュ レジスター](emea-swe-cash-registers.md)」を参照してください。

## <a name="production-environment"></a>実稼働環境

以下の手順に従い、実稼働環境で小売コンポーネントを含む配置可能パッケージを作成して適用します。

1. POS コンポーネントの拡張

    1. 除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。
    2. 適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能を有効にします。

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

1. **RetailSdk\Assets** フォルダーのパッケージ構成ファイルに、次の変更を加えます。

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

        ---

2. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
3. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
