---
title: 会計統合サンプル用のビルド パイプラインの設定
description: この記事では、サンプル コードに対して Cloud Scale Unit およびセルフサービスの配置可能パッケージを生成およびリリースできるよう、Microsoft Dynamics 365 Commerce の Retail ソフトウェア開発キット (SDK) からの会計統合サンプルのビルド パイプラインとリリース パイプラインを設定する方法について説明します。
author: Sergio1C
ms.date: 12/21/2021
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: v-seskry
ms.search.validFrom: ''
ms.openlocfilehash: 61386fa8eb93d5092653d174b131e190dc6a19d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884830"
---
# <a name="set-up-a-build-pipeline-for-a-fiscal-integration-sample"></a>会計統合サンプル用のビルド パイプラインの設定

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の Retail ソフトウェア開発キット (SDK) からの[会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) のビルド パイプラインとリリース パイプラインを設定する方法について説明します。 これにより、 [独立したパッケージおよび拡張モデル](../dev-itpro/build-pipeline.md) を使用して、サンプルコードに対してCloud Scale Unit およびセルフサービスの配置可能パッケージを生成およびリリースできます。

> [!NOTE]
> Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) から Retail SDK の以前のバージョンを使用している場合、この記事に記載されている手順は機能しません。 LCS で開発者 VM から Retail SDK を使用している場合に会計統合サンプルを配置するために必要な手順については、対応する会計統合サンプルのドキュメントを参照してください。

## <a name="set-up-a-build-pipeline-in-azure-devops-to-generate-cloud-scale-unit-extension-packages-and-retail-self-service-packages"></a>Azure DevOps のビルド パイプラインを設定し、Cloud Scale Unit 拡張パッケージと Retail セルフサービス パッケージを生成

1. Azure DevOps 組織にサイン インします。
1. **パイプライン** を選び、**新しいパイプライン** を選択します。
1. 会計統合ソリューションのソース リポジトリ (リポジトリ) [Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) を選択します。
1. **既存の Azure Pipelines YAML ファイル** を選択します。
1. [Dynamic365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **Pipeline\\YAML_Files** フォルダーから適切な YAML ファイルを選択または取得します。 サンプルのテンプレート YAML ファイルを見つける方法の詳細については、会計統合ソリューションの readme.md ファイルまたは会計統合サンプルのパブリック ドキュメントを参照してください。
1. **続行** を選択します。

    YAML ファイルには、証明書を使用して Scale Unit、Modern POS および Hardware Station 拡張機能インストーラーに署名する手順が示されています。 スクリプトでは、Azure Key Vault の証明書ファイルが検索され、次に証明書ファイルを署名に使用します。 Azure Key Vault から証明書を読み取るには、アプリケーション ID、シークレット名、および証明書名を指定する必要があります。 タイムスタンプを使用して証明書に署名するには、タイムスタンプ サーバーの詳細も指定する必要があります。 詳細については、[Azure Key Vault から Azure ポータルを使用して証明書を設定および取得](/azure/key-vault/certificates/quick-create-portal) を参照します。

    パイプライン内のキー コンテナーとタイムスタンプ サーバーの詳細を表示するには、ビルド パイプラインの **変数** タブに次の変数を作成し、その値を指定します。 変数のセキュリティを確保するには、変数タイプとして **シークレット** を選択します。

    - **ApplicationId**
    - **AzureKeyVaultURI**
    - **CertificateName**
    - **SecretValue**
    - **Timestamp**- この変数の値として、`http://timestamp.digicert.com` などのタイムスタンプ プロバイダーを指定できます。

    Azure に証明書を格納していない場合は、**セキュア タスク** オプションまたは Azure Pipelines がサポートする他のオプションを使用して、インストーラーに署名できます。

    インストーラに署名する必要がな場合は、署名ステップを YAML ファイルから削除できます。 YAML ファイルで、**PowerShell\@2** タスクを検索して、削除します。

    YAML ファイルのスクリプトはソリューション全体を構築し、アウトプット ファイルをビルド用に **公開済みアーティファクト** の格納場所にアップロードします。 出力ファイルは、CloudScaleUnitExtensionPackage.zip と、次の Retail セルフ サービス拡張パッケージです: HardwareStation.\*Installer.exe、ScaleUnit.\*Installer.exe、および ModernPOS.\*Installer.exe。

    > [!NOTE]
    > Retail セルフ サービス拡張パッケージの名前では、アスタリスク (\*) は会計統合ソリューションの名前を表します。
    >
    > 会計統合のサンプルによっては、一部の Commerce コンポーネントの拡張機能は不要な場合があります。 そのため、一部の出力ファイルを省略する場合があります。

1. 変更を保存し、キューにビルドを追加します。
1. ビルドが完了すると、**公開済みアーティファクト** からパッケージをダウンロードできます。

    - **Commerce Scale Unit パッケージ**

        - ScaleUnitPackage_$(BuildNumber).zip

    - **Retail セルフサービス拡張パッケージ**

        - HardwareStation.\*.Installer_$(BuildNumber).exe
        - ScaleUnit.\*.Installer_$(BuildNumber).exe
        - ModernPOS.\*.Installer_$(BuildNumber).exe

        これらのパッケージ名では、アスタリスク (**\***) が会計統合ソリューションの名前を表します。

## <a name="set-up-a-release-pipeline-for-the-cloud-scale-unit-extension-package"></a>Cloud Scale Unit 拡張パッケージのリリース パイプラインを設定

会計統合サンプルの Cloud Scale Unit 拡張パッケージ用のリリース パイプラインを設定するには、[Cloud Scale Unit 拡張パッケージのリリース パイプラインを設定](../dev-itpro/build-pipeline.md#set-up-a-release-pipeline-for-the-cloud-scale-unit-extension-package) に従います。

## <a name="set-up-a-release-pipeline-for-retail-self-service-packages"></a>Retail セルフサービス パッケージのリリース パイプラインの設定

会計統合サンプル用の Retail セルフサービス パッケージ用のリリース パイプラインを設定するには、[Retail セルフサービス パッケージのリリース パイプラインの設定](../../commerce/dev-itpro/build-pipeline.md#set-up-a-release-pipeline-for-retail-self-service-packages) の手順に従います。
