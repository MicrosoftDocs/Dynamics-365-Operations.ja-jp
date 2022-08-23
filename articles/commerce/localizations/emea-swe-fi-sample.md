---
title: スウェーデン向け制御ユニットの統合サンプル
description: この記事では、Microsoft Dynamics 365 Commerce のスウェーデン向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 3376e6a901b692371a44b5c74c1e6b4afd0cd573
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275069"
---
# <a name="control-unit-integration-sample-for-sweden"></a>スウェーデン向け制御ユニットの統合サンプル

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のスウェーデン向け会計統合サンプルの概要について説明します。

> [!NOTE]
> このサンプルは、[スウェーデンの制御ユニットとの POS 統合のサンプル](retail-sdk-control-unit-sample.md)に代わる、会計統合機能のサンプルです。 以前のサンプルは、[会計統合フレームワーク](./fiscal-integration-for-retail-channel.md)を利用しておらず、今後の更新で非推奨になります。 以前のサンプルから、Dynamics 365 Commerce バージョン **10.0.22 またはそれ以前** に対応したサンプルに移行する方法については、[以前の統合サンプルからの移行](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample) を参照してください。

スウェーデンの Commerce 機能には、POS と *制御ユニット* と呼ばれるスウェーデン固有の会計デバイスとの統合のサンプルが含まれています。 このサンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)を拡張しています。 POS がペアになっているハードウェア ステーションに制御ユニットが物理的に接続されていることが前提です。 このサンプルでは、一例として、Retail Innovation HTT AB の [CleanCash タイプ A](https://www.retailinnovation.se/produkter) 制御ユニットのアプリケーション プログラミング インターフェイス (API) を使用しています。 CleanCash API のバージョン1.1.4 が使用されます。

このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、Retail Innovation HTT AB からハードウェア、ソフトウェア、ドキュメントをリリースしていません。 制御ユニットを取得して操作する方法については、[Retail Retail HTT AB](https://www.retailinnovation.se/) にお問い合わせください。

## <a name="scenarios"></a>シナリオ

スウェーデンの制御ユニットの統合サンプルには、次の機能が含まれています:

- 営業、返品、レシートのコピーは、POS がペアリングされているハードウェア ステーションに物理的に接続済みのコントロール ユニットに自動登録されます。
- 登録されたトランザクションのコントロール ユニットの制御コードと製造番号は、コントロール ユニットからキャプチャされ、トランザクションに保存されます。 このデータは、*会計応答* とも呼ばれます。 会計応答は、**店舗トランザクション** ページで確認できます。
- 制御コードと制御ユニットの製造番号のカスタム フィールドをレシートのレイアウトに追加することができます。 このように、ある取引の会計処理をレシートに印刷することができます。
- トランザクションに対する会計応答は、**電子ジャーナル (スウェーデン)** のチャネル レポートに表示されます。
- いくつかのエラー処理オプションを使用できます。 次にいくつか例を挙げます。

    - 再試行が可能な場合は、会計登録を再試行します。 たとえば、制御ユニットが接続されていない、準備ができていない、応答がないなどの場合には、財政登録を再試行することができます。
    - 会計登録の延期。
    - 会計登録をスキップするか、またはトランザクションを登録済みとしてマークして、失敗した理由と追加情報を取得するための情報コードを含めます。
    - 新しい販売トランザクションの開始時や販売トランザクション確定時に、制御ユニットの可用性を確認します。

### <a name="limitations-of-the-sample"></a>サンプルの制限事項

スウェーデン向けの制御ユニット統合サンプルは、現在カスタマー オーダーのシナリオをサポートしていません。

## <a name="setting-up-the-integration-with-control-units"></a>制御ユニットとの統合のセットアップ

スウェーデンに必要な設定の詳細については、[スウェーデン向け、Commerce の設定](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden)を参照してください。

### <a name="configuring-swedenspecific-receipts"></a>スウェーデン固有のレシートを構成する

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売領収書の領収書形式で使用できるようにする

POS レシートの形式で使用される言語テキストやカスタム フィールドを構成できます。 領収書設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**言語テキスト** ページで、領収書 レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

**言語テキスト** ページの **POS** セクションに、次の POS ラベル を追加 します。

| 言語 ID | テキスト ID | テキスト                  |
|-------------|---------|-----------------------|
| ja       | 900001  | 制御コードを登録する |
| ja       | 900002  | デバイスの登録       |

**カスタム フィールド** ページで、領収書 レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name                         | 種類    | キャプション テキスト ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | 受信 | 900001          |
| SE_FISCALREGISTERID          | 受信 | 900002          |

> [!NOTE]
> 上の表にあるように、正しいカスタム フィールド名を指定することが重要です。 カスタム フィールド名が正確でない場合、領収書のデータが失われます。

#### <a name="configure-receipt-formats"></a>レシート形式を設定する

必要な領収書の形式ごとに、**印刷動作** フィールドの値を **常に印刷** に変更します。

レシート形式デザイナーで、**フッター** セクションに、次のカスタム フィールドを追加します。 フィールド名は、この記事の前述のセクションで定義した言語テキストに対応しています。

- **登録の制御コード** - このフィールドは、制御コードを印刷します。
- **登録デバイス** - このフィールドは、制御ユニットの製造番号を表示します。

レシート形式の使用方法の詳細については、[レシート テンプレートと印刷](../receipt-templates-printing.md) を参照してください。

### <a name="set-up-fiscal-integration-for-sweden"></a>スウェーデン向け、会計統合の設定

スウェーデン向けの制御ユニット統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\CleanCash** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[スウェーデン向け制御ユニットプリンター統合サンプルの配置ガイドライン (レガシ)](emea-swe-fi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

[Commerce チャンネルの会計統合を設定する](setting-up-fiscal-integration-for-retail-channel.md)で説明されている会計統合の設定手順を実行します。

1. [会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 また、[今回の制御ユニット統合サンプルに固有](#set-up-the-registration-process)の会計登録処理の設定をメモしておきます。
1. [エラーの処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [延期された会計登録の手動実行を可能にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効化する場合は、次の手順に従って Commerce Headquarters を設定します。 詳細情報については、[コマース チャネルの会計統合の設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

1. 会計ドキュメント プロバイダーと会計コネクタの構成ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します (例: **[リリース/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**)。
    1. **src \>FiscalIntegration \>CleanCash** を開きます。
    1. 会計ドキュメント プロバイダ構成ファイルを **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (例: [release/9.33 のファイルなど](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)) でダウンロードします。
    1. 会計コネクター構成ファイルを **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (例: [release/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)) でダウンロードします。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダ構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **会計コネクタ 構成ファイル:**  RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。 **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。 新しいコネクタ機能プロファイルを作成します。 以前に読み込んだドキュメント プロバイダーとコネクタを選択します。 必要に応じて [データ マッピング設定](#default-data-mapping) を更新します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。 新しいコネクタ テクニカル プロファイルを作成し、先に読み込んだ会計コネクタを選択します。 必要に応じて [コネクタの設定](#fiscal-connector-settings) を更新します。
6. **Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。 以前に作成したコネクタ機能プロファイルに、新しい会計コネクタ グループを作成します。
7. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計登録プロセス** の順に移動します。 新しい会計登録プロセスと会計登録プロセス ステップを作成し、以前に作成した会計コネクタ グループを選択します。
8. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 登録プロセスを有効化する、店舗にリンクされている機能プロファイルを選択します。 **会計登録プロセス** クイックタブで、以前に作成した会計登録プロセスを選択します。
9. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。 会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。 **会計周辺機器** クイックタブで、先ほど作成したコネクタ テクニカル プロファイルを選択します。
10. 配布スケジュール (**Retail と Commerce \> Retail と Commerce IT \> 配送スケジュール**) を開き、ジョブ **1070** と **1090** を選択してチャネル データベースにデータを転送します。

#### <a name="default-data-mapping"></a>既定のデータ マッピング

次の既定のデータ マッピングは、会計統合サンプルの一部として提供される会計ドキュメント プロバイダー構成に含まれています。

- **付加価値税 (VAT) コード マッピング** - このマッピングは、デバイス固有の付加価値税 (VAT) コードを対応する消費税コードに設定します。 VAT コード マッピングの形式は次のとおりです:

    ```
    1 : code1 ; 2 : code2
    ```

    この形式の説明は以下の通りです:

    - *1* と *2* はデバイス固有の VAT コードです。
    - セミコロン (;) は区切り文字として使用されます。
    - *code1* と *code2* は、Commerce 本部で構成された消費税コードです。 顧客のアプリケーションで設定されている税コードに応じて、サンプル マッピングを変更する必要があります。

    制御ユニットは、最大 4 つの異なる VAT コードをサポートします。 したがって、VAT コード マッピングは、次の方法で設定される場合があります:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > 複数の消費税コードを同じデバイス固有の VAT コードにマッピングできます。

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **接続文字列** - 制御ユニットの接続設定。
- **タイムアウト** – ドライバーが制御ユニットからの応答を待機する時間を、ミリ秒単位で表します。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[スウェーデン向け制御ユニットプリンター統合サンプルの配置ガイドライン (レガシ)](emea-swe-fi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

#### <a name="set-up-the-development-environment"></a>開発環境の設定

開発環境を設定してサンプルのテストと拡張を行う際は、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** で制御ユニット統合ソリューションを開き、ビルドします。
1. CRT 拡張機能をインストールします:

    1. CRT 拡張機能のインストーラを見つけます。

        - **Commerce Scale Unit:**  **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** フォルダで、**ScaleUnit.CleanCash.Installer** インストーラーを探します。
        - **Modern POS 上のローカル CRT:** **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** フォルダ内で、**ModernPOS.CleanCash.Installer** インストーラーを探します。

    2. コマンド ラインから CRT 拡張機能インストーラーを起動します。

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **最新 POS のローカル CRT:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. ハードウェア ステーション拡張機能をインストールする。

    1. **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** フォルダ内で、**HardwareStation.CleanCash.Installer** インストーラーを探します。
    1. コマンド ラインから拡張機能インストーラーを起動します。

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>運用環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **CleanCash build-pipeline.yml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **パイプライン\\YAML_Files** フォルダにあります。

## <a name="design-of-the-extensions"></a>拡張機能の設計

スウェーデン向けの制御ユニット統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\CleanCash** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[スウェーデン向け制御ユニットプリンター統合サンプルの配置ガイドライン (レガシ)](emea-swe-fi-sample-sdk.md)を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="crt-extension-design"></a>CRT 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して制御ユニットからの応答を処理することです。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーに使用する単一の **DocumentProviderCleanCash** 要求ハンドラーがあります。 このハンドラーは、制御ユニットの会計ドキュメントを作成するために使用されます。

このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは制御ユニットに登録するべきサービス固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在、販売イベントと監査イベントがサポートされています。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリの **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** にあります。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、制御ユニットと通信できます。 これは HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを制御ユニットに送信します。 また、制御ユニットから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**CleanCashHandler** 要求ハンドラーは、制御ユニットに対する要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – このリクエストは、制御ユニットにドキュメントを送信し、制御ユニットからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求は制御ユニットの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求は、制御ユニットの初期化に使用されます。

#### <a name="configuration"></a>構成

会計コネクタの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** にあります。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
