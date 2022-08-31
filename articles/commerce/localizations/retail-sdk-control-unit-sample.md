---
title: スウェーデンの制御ユニットとの POS の統合サンプル (レガシ)
description: この記事は、スウェーデンの管理単位統合サンプルのビルドとインストールのガイドです。
author: EvgenyPopovMBS
ms.date: 12/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Sweden
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-2-28
ms.openlocfilehash: 279959f557be40b8bc977d16a921b176a27a48da
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323450"
---
# <a name="sample-for-pos-integration-with-control-units-for-sweden-legacy"></a>スウェーデンの制御ユニットとの POS の統合サンプル (レガシ)

[!include [banner](../includes/banner.md)]

> [!NOTE]
> このサンプル会計統合機能は、[会計統合フレームワーク](fiscal-integration-for-retail-channel.md)を利用しておらず、今後の更新で非推奨になります。 代わりに、[スウェーデン向け制御ユニット統合サンプル](emea-swe-fi-sample.md) を使用する必要があります。

このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Dynamics 365 Commerce 拡張機能を作成する方法を示します。 特に、このサンプルには Retail POS をスウェーデンの管理単位と統合するコードが含まれています。 コントロール ユニットは、POS がペアリングされているハードウェア ステーションに物理的に接続されていることを前提としています。 たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。 CleanCash® API のバージョン1.1.4 が使用されます。 API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。

このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。 小売 SDK のダウンロードと使用方法については、 [小売 ソフトウェアの開発キット(SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。

このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。 このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。 この記事で説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。 ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。

> [!NOTE]
> 使用しているコマースのバージョンによって、この記事の手順の一部が異なります。 詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。
>
> Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。 この記事は、アプリの以前の複数のバージョンに適用されるため、この記事全体で *Retail サーバー* を使用します。


## <a name="overview-of-integration-with-control-units"></a>コントロール ユニットとの統合の概要

サンプルには、次の機能が含まれます。

- 営業、返品、レシートのコピーは、POS がペアリングされているハードウェア ステーションに物理的に接続済みのコントロール ユニットに自動登録されます。
- 登録されたトランザクションのコントロール ユニットの制御コードと製造番号は、コントロール ユニットからキャプチャされ、トランザクションに保存されます。 (このデータは _会計データ_ とも呼ばれます。) 会計データは、**店舗のトランザクション** ページで表示できます。
- コントロール ユニットの制御コードと製造番号のカスタム フィールドはレシート形式に追加できるため、トランザクションの会計データをレシートに印刷できます。
- トランザクションの会計データは、**電子ジャーナル (スウェーデン)** チャネル レポートに印刷されます。
- コントロール ユニットでのトランザクションの登録中に障害が発生した場合、トランザクションの会計データは空白のままになります。 この場合、新しいトランザクションを開始することはできず、現在のシフトを閉じることもできません。 オペレーターは、未登録のトランザクションをコントロール ユニットに再登録するよう求められます。 2 回目の試行が失敗した場合、オペレーターは、特別な許可があれば登録をスキップできます。 オペレーターがコントロール ユニットでのトランザクションの登録をスキップした場合、このイベントに関する情報は会計データではなくトランザクションに保存されます。

> [!NOTE]
> 現時点では、コントロール ユニット統合サンプルは顧客注文をサポートしていません。 ただし、顧客注文をサポートするサンプルは、後日入手可能になります。

## <a name="setting-up-integration-with-control-units"></a>コントロール ユニットとの統合のセットアップ

Retail POS がスウェーデンのコントロール ユニットと統合されるように、次の設定を指定する必要があります。

1. 会計登録の構成を作成し、ハードウェア プロファイルに割り当てます。

    1. **会計登録の構成** ページで、新しい会計登録の構成レコードを作成します。 構成の名前と説明を設定します。
    2. 構成の内容を入力します。 このサンプルで構成は、消費税コードとコントロール ユニットの VAT グループ間のマッピングを確立する XML ファイルです。 最大 4 つの消費税コードをマッピングできます。 次の構成例では、**VAT10** および **VAT20** はマッピングする必要がある消費税コードを表しています。

        ``` xml
        <UnitConfiguration>
            <TaxMapping>
                <Tax taxCode="VAT10" controlUnitTaxId="1"/>
                <Tax taxCode="VAT20" controlUnitTaxId="2"/>
            </TaxMapping>
        </UnitConfiguration>
        ```

        アクション ペインで **サンプル構成のエクスポート** をクリックして、サンプル構成をエクスポートすることもできます。

    3. **ハードウェア プロファイル** ページで、POS がペアリングされ、コントロール ユニットが接続されているハードウェア ステーションのハードウェア プロファイルを選択します。 **会計登録** ファストタブで、以下のフィールドを設定します。

        - **会計登録** フィールドで、**サードパーティ要因** を選択します。
        - **構成** フィールドで、作成した会計登録の構成名を選択します。

2. レシートレイアウト用のカスタム フィールドを設定し、コントロール ユニットの制御コードと製造番号がレシートに印刷されるようにします。

    1. **言語テキスト** ページで、カスタムレシートレイアウト フィールドのキャプションに 2 つのレコードを追加します。 適切なフィールドで、キャプションの言語 ID (たとえば **sv-se**)、テキスト ID (たとえば **900001** や **900002**)、キャプション テキスト (たとえば **制御コード** や **コントロール ユニット ID** ) を指定します。
    2. **カスタム フィールド** ページで、カスタムレシートレイアウトのフィールドに 2 つのレコードを追加します。 **タイプ** フィールドで、**レシート** を選択します。 カスタム レシート レイアウトのフィールドの名前とキャプションを指定します。

        - 制御コード:

            - **名前:** **FiscalRegisterControlCode**
            - **キャプション テキスト ID**: 制御コード フィールドに指定したテキスト ID (前の例では **900001**)

        - コントロール ユニットの製造番号:

            - **名前:** **FiscalRegisterId**
            - **キャプション テキスト ID**: コントロール ユニット ID フィールドに指定したテキスト ID (前の例では **900002**)

    3. 販売レシートの形式については、レシート レイアウトの **フッター** セクションのレシート形式デザイナーで、指定されたキャプションのフィールドを追加します (前の例では **制御コード** および **コントロール ユニット**)。

3. 店舗の作業者の POS アクセス許可グループおよび個々のアクセス許可の設定を更新します。 アクセス許可グループに割り当てられている作業者が会計登録を省略できるようにするには、**会計登録のスキップを許可する** チェックボックスをオンにします。

## <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

1. ハードウェア ステーション コンポーネントを拡張します。

    1. **RetailSDK\\SampleExtensions\\HardwareStation** から ハードウェア ステーション ソリューションを開きます。
    2. **HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。
    3. 拡張機能アセンブリおよび設定を検索します。

        # <a name="retail-73-and-earlier"></a>[Retail 7.3 以前](#tab/retail-7-3)

        **Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。

        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション
        - **Interop.CleanCash\_1\_1.dll** アセンブリ

        # <a name="retail-731-and-later"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        **Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。

        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ
        - **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション
        - **Interop.CleanCash\_1\_1.dll** アセンブリ

        # <a name="retail-100-and-later"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

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

        # <a name="retail-73-and-earlier"></a>[Retail 7.3 以前](#tab/retail-7-3)

        - **リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config** で、IIS ハードウェア ステーション サイトの場所にあります。
        - **ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config** で、Modern POS クライアント ブローカーの場所にあります。

        # <a name="retail-731-and-later"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        ファイルの名前は **HardwareStation.Extension.config** です。

        - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
        - **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

        # <a name="retail-100-and-later"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        ファイルの名前は **HardwareStation.Extension.config** です。

        - **リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。
        - **ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。

        ---

    6. コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。

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
        > commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては **いけません**。 これらのファイルはカスタマイズのためのものではありません。

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
    6. **実行** コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。
    7. 機能をテストします。

5. 本社で、会計登録構成と、その他の必要なパラメーターを設定します。 詳細については、[スウェーデンのキャッシュ レジスター機能](emea-swe-cash-registers.md) を参照してください。

## <a name="production-environment"></a>運用環境

以下の手順に従い、運用環境でコマース コンポーネントを含む配置可能パッケージを作成して適用します。

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
        <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
        ```

    2. ハードウェア ステーション構成ファイルの **構成** セクションに、次のセクションを追加します。

        # <a name="retail-73-and-earlier"></a>[Retail 7.3 以前](#tab/retail-7-3)

        **HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-later"></a>[Retail 7.3.1 およびそれ以降](#tab/retail-7-3-1)

        **HardwareStation.Extension.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```
        
        # <a name="retail-100-and-later"></a>[Retail 10.0 およびそれ以降](#tab/retail-10-0)

        **HardwareStation.Extension.config** 構成ファイルを変更します。

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```

        ---

3. **BuildTools\\Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。

   - 展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。
        ``` xml
        <ISV_CommerceRuntime_CustomizableFileInclude="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll"/>
        ```

4. Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。
5. Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。 詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
