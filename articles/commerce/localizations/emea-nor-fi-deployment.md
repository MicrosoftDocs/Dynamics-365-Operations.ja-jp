---
title: ノルウェーのキャッシュ レジスタの配置ガイドライン
description: この記事では、ノルウェーの Microsoft Dynamics 365 Commerce のローカライズで、キャッシュ レジスター機能を有効化する方法について説明します。
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 9149e9da7222699e9ca996b69e56fff07b77a737
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2022
ms.locfileid: "9345994"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>ノルウェーのキャッシュ レジスタの配置ガイドライン

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> この記事で説明されている手順を実装する必要があります (Microsoft Dynamics 365 Commerce バージョン 10.0.29 以降を使用している場合)。 Commerce version 10.0.28 以前では、Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail ソフトウェア開発キット (SDK) の以前のバージョンを使用する必要があります。 詳細は、[ノルウェー向けキャッシュ レジスター展開ガイドライン (レガシ)](./emea-nor-loc-deployment-guidelines.md)を参照してください。 Commerce Version バージョン 10.0.28 以前を使用している場合で、Commerce バージョン10.0.29 以降に移行する場合は、[ノルウェー向けレガシ Commerce 機能から移行する](./emea-nor-fi-migration.md) の手順に従う必要があります。

この記事では、ノルウェーの Commerce のローカライズで、キャッシュ レジスター機能を有効化する方法について説明します。 このローカリゼーションは、カスタム フィールドをレシートに印刷、追加の監査イベント、販売取引、販売時点管理 (POS) での支払取引の登録、販売取引のデジタル署名、ローカルの形式で X および Z レポートの印刷を行える等のアクションを実行できるようにする、いくつかのコンポーネント拡張機能から構成されています。 ノルウェーのローカライズの詳細については、 [ノルウェーのキャッシュ レジスター機能](./emea-nor-cash-registers.md) を参照してください。 ノルウェー向け Commerce の設定方法の詳細については、[ノルウェー向け Commerce の設定](./emea-nor-cash-registers.md#setting-up-commerce-for-norway)を参照してください。

## <a name="set-up-fiscal-registration-for-norway"></a>ノルウェー向け会計登録の設定

ノルウェーの会計登録サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Commerce SDK の一部となっています。 このサンプルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\SequentialSignatureNorway** フォルダーにあります。 この [サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) は、Commerce Runtime (CRT) の拡張機能である 会計ドキュメント プロバイダーと会計コネクタから構成されています。 Commerce SDK の使用方法の詳細については、[Commerce SDK サンプルと GitHub と NuGet からのリファレンス パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) と [独立パッケージSDK のパイプラインを設定する](../dev-itpro/build-pipeline.md) をご覧ください。

[Commerce チャンネルの会計統合を設定する](./setting-up-fiscal-integration-for-retail-channel.md)で説明されている会計登録の設定手順を実行します:

1. [会計登録プロセスの設定](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 会計登録プロセスにおける[ノルウェー固有](#configure-the-fiscal-registration-process)の設定を必ずメモしてください。
1. [エラーの処理の設定](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [延期された会計登録の手動実行を可能にする](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="configure-the-fiscal-registration-process"></a>会計登録プロセスの構成

以下の手順で、Commerce 本部でノルウェーの会計登録プロセスを有効にしてください。

1. Commerce SDK から会計ドキュメント プロバイダーと会計コネクタのコンフィギュレーション ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. 使用可能な最後のリリース分岐を開きます。
    1. **src \> FiscalIntegration \> SequentialSignatureNorway \> CommerceRuntime** を開きます。
    1. 会計ドキュメント プロバイダー構成ファイルを、**DocumentProvider.SequentialSignNorway \> 構成 \> DocumentProviderSequentialSignatureNorwaySample.xml** でダウンロードします。
    1. 会計コネクター構成ファイルを **Connector.SequentialSignNorway \> 構成 \> ConnectorSequentialSignatureNorwaySample.xml** でダウンロードします。

1. **Retail と Commerce \> 本社の設定 \> パラメーター \> Shared パラメーター** の順にクリックします。 **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。 コネクタの機能プロファイルを新規に作成し、ドキュメント プロバイダーと、先に読み込んだコネクタを選択します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。 新しいコネクター テクニカル プロファイルを作成し、先に読み込んだコネクターを選択します。 コネクタのタイプを **内部** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ フループ** に移動し、先ほど作成したコネクタ機能プロファイル用の新しい会計コネクタ グループを作成します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計登録プロセス** の順に移動します。 新しい会計登録プロセスと会計登録プロセス ステップを作成し、以前に作成した会計コネクタ グループを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 登録プロセスを有効化する、店舗にリンクされている機能プロファイルを選択します。 **会計登録プロセス** クイックタブで、以前に作成した会計登録プロセスを選択します。 **会計サービス** クイックタブで、先ほど作成したコネクタのテクニカル・プロファイルを選択します。 
1. **Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。 配送スケジュールを開き、**1070** と **1090** のジョブを実行してチャネル データベースにデータを転送します。

### <a name="configure-the-digital-signature-parameters"></a>デジタル署名のパラメータの構成

店舗での販売取引のデジタル署名に使用する証明書を設定する必要があります。 署名には、Azure Key Vault に格納されているデジタル証明書が使用されます。 Modern POS のオフラインモードでは、Modern POS がインストールされているマシンのローカル ストレージに保存されているデジタル証明書を使用して署名を行うこともできます。

Key Vault のストレージに保存されている電子証明書を使用する前に、以下の手順を完了する必要があります。

1. Key Vault ストレージを作成する必要があります。 Commerce Scale Unit と同じ地理的領域にストレージを配置することをお勧めします。
1. 証明書は、base64 文字列のシークレットとして、Key Vault のストレージにアップロードする必要があります。
1. Application Object Server (AOS) アプリケーションには、Key Vault ストレージからシークレットを読み取る権限が必要です。

Key Vault を操作する方法の詳細については、[Azure Key Vault の使用を開始する](/azure/key-vault/key-vault-get-started)を参照してください。

次に、**キー コンテナー パラメータ** ページで、Key Vault ストレージにアクセスするためのパラメータを指定する必要があります:

- **名前** と **説明** -  Key Vault ストレージの名前と説明です。
- **Key Vault URL** - Key Vault ストレージの URL。
- **Key Vault クライアント** - 認証のために Key Vault ストレージに関連付けられている Azure Active Directory (Azure AD) アプリケーションのインタラクティブ クライアント ID。 このクライアントは、ストレージから機密情報を読み取るためのアクセス許可が必要です。
- **Key Vault シークレット キー** - Key Vault ストレージで認証のために使用される Azure AD アプリケーションと関連している秘密キー。
- **名前**、**説明**、**シークレットの参照** - 証明書の名前、説明、シークレットの参照。

次に、Key Vault またはローカルの証明書ストレージに保存されている証明書のコネクタを構成する必要があります。 このコネクタは、チャンネル側で署名するために使用されます。

1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。
1. **設定** クイックタブで、デジタル署名に対して次のパラメータを指定します:

    - **シークレット名** - 前述の **Key Vault パラメータ** ページで設定したシークレットの名前を選択します。
    - **ローカル証明書のサムプリント** – ローカルに保存されている証明書のサムプリントを入力します。
    - **ハッシュ アルゴリズム** -   **SHA1** など、Microsoft .NET がサポートしている暗号化ハッシュアルゴリズムの一つを指定します。
    - **証明書店舗名** – このフィールドはオプションです。 これを使用して、ローカル証明書の検索に使用する既定の店舗名を指定します。
    - **証明書ストアの場所** – このフィールドはオプションです。 これを使用して、ローカル証明書の検索に使用する既定の店舗の場所を指定します。
    - **最初にローカル証明書を試す** - データの署名に、Key Vault の証明書ではなく、ローカル ストアの証明書を既定で使用する場合は、このオプションを選択します。
    - **正常性チェックの有効化** – 正常性チェック手順の詳細については、[会計登録の正常性チェック](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check)を参照してください。

> [!NOTE]
> - 現在、ノルウェーでは **SHA1** 暗号ハッシュ アルゴリズムのみが認められています。
> - CRT でローカル証明書を検索するプロセスを簡略化するために、既定の店舗名および店舗の場所が追加されます。 X509StoreProvider には、証明書が保存されるフォルダーの一覧があります。 既定のストア名と既定のストアの場所が指定されていない場合、X509StoreProvider はそのリスト上のすべてのフォルダで証明書の検索を試みます。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

#### <a name="development-environment"></a>開発環境

サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Commerce SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\SequentialSignatureNorway** 配下で **SequentialSignatureNorway.sln** を開き、ビルドします。
1. CRT 拡張機能をインストールします:

    1. CRT 拡張機能のインストーラを見つけます。

        - **Commerce Scale Unit:** **SequentialSignatureNorway\\ScaleUnit\\ScaleUnit.SequentialSignNorway.Installer\\bin\\Debug\\net461** フォルダで、**ScaleUnit.SequentialSignNorway.Installer** インストーラーを探します。
        - **Modern POS 上のローカル CRT:** **SequentialSignatureNorway\\ModernPOS\\ModernPos.SequentialSignNorway.Installer\\bin\\Debug\\net461** フォルダで、**ModernPos.SequentialSignNorway.Installer** インストーラーを探します。

    1. コマンド ラインから CRT 拡張機能インストーラーを起動します。

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **最新 POS のローカル CRT:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>運用環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **SequentialSignatureNorway build-pipeline.yaml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **パイプライン\\YAML_Files** フォルダにあります。

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Modern POS のオフライン モードでのデジタル署名を有効にします。

Modern POSでオフライン モードでのデジタル署名を有効にするには、新しい端末で Modern POS を有効化した後、これらの手順に従う必要があります。

1. POS にサインインします。
1. **データベースの接続の状態** ページで、オフライン データベースが完全に同期されていることを確認します。 **ダウンロードの保留中** フィールドの値が **0** (ゼロ) の場合、データベースは完全に同期しています。
1. POS からのサインアウト
1. オフライン データベースが完全に同期するのを待機します。
1. POS にサインインします。
1. **データベースの接続の状態** ページで、オフライン データベースが完全に同期されていることを確認します。 **オフライン データベースで取引を保留中** フィールドの値が **0** (ゼロ) の場合、データベースは完全に同期しています。
1. Modern POS を再度開きます。
