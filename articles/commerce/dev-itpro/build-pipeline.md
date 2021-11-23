---
title: 独立したパッケージ SDK のビルド パイプラインの設定
description: このトピックでは、拡張コードに対して Cloud Scale Unit およびセルフサービスの配置可能パッケージを生成できるよう、Retail ソフトウェア開発キット (SDK) のビルド パイプラインを設定する方法について説明します。
author: mugunthanm
ms.date: 05/17/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 05-17-2020
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 1e51109d1e8ca8901e4aa50aac8fb5ff0bc4b54f
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782922"
---
# <a name="set-up-a-build-pipeline-for-the-independent-packaging-sdk"></a>独立したパッケージ SDK のビルド パイプラインの設定

[!include [banner](../../includes/banner.md)]

このトピックでは、拡張コードに対して Cloud Scale Unit およびセルフサービスの配置可能パッケージを生成できるよう、Retail ソフトウェア開発キット (SDK) のビルド パイプラインを設定する方法について説明します (新しい独立系拡張モデルを使用)。

このトピックは、Retail SDK 10.0.19 以降に適用されます。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) から Retail SDK の以前のバージョンを使用している場合、このトピックに記載されている手順は機能しません。 このトピックの情報は、新しい独立した拡張モデル (つまり、パブリック フィードからパッケージを消費している場合) と、独立系梱包および拡張機能モデルを使用している場合に適用されます。

## <a name="set-up-a-build-pipeline-in-azure-devops-to-generate-a-cloud-scale-unit-extension-package"></a>Azure DevOps のビルド パイプラインを設定し、Cloud Scale Unit 拡張パッケージを生成

1. Microsoft Azure DevOps 組織にサイン インします。
2. **パイプライン** を選び、**新しいパイプライン** を選択します。
3. 拡張コードのソース リポジトリ (リポジトリ) を選択します。
4. **既存の Azure Pipelines YAML ファイル** を選択します。
5. [Dynamics365Commerce.ScaleUnit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/tree/release/9.29) GitHub リポジトリから、[build-pipeline.yml ファイル](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/blob/release/9.29/Pipeline/YAML_Files/build-pipeline.yml) を選び、取得します。

    > [!NOTE]
    > YAML ファイルは、[Dynamics365Commerce.ScaleUnit GitHub リポジトリの Pipeline/PowerShellScripts ディレクトリ](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/tree/release/9.29/Pipeline/PowerShellScripts) のスクリプトの一部を参照します。 これら全てのスクリプトをリポジトリに含めてください。 サンプル リポジトリをクローンする場合、すべてのスクリプトが既に含まれています。

6. **続行** を選択します。

    YAML ファイルのスクリプトはソリューション全体を構築し、アウトプット (CloudScaleUnitExtensionPackage.zip パッケージ) をビルド用に **公開済みアーティファクト** のドロップ ロケーションにアップロードします。

    > [!NOTE]
    > YAML ファイルはリポジトリのソリューション ファイルを検索し、ソリューションを構築して、CloudScaleUnitExtensionPackage.zip パッケージを検索します。 したがって、拡張機能プロジェクトと梱包プロジェクトがソリューションにリンクされている必要があります。 拡張プロジェクトをモデル化する方法については、[Dynamics365Commerce.ScaleUnit GitHub リポジトリ](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/tree/release/9.29) のサンプルを参照します。

7. 変更を保存し、キューにビルドを追加します。
8. ビルドが完了すると、**公開済みアーティファクト** から **ScaleUnitPackage_(Build.BuildNumber).zip** パッケージをダウンロードできます。

## <a name="set-up-a-release-pipeline-for-the-cloud-scale-unit-extension-package"></a>Cloud Scale Unit 拡張パッケージのリリース パイプラインを設定

ベスト プラクティスとして、個別のビルド パイプラインとリリース パイプラインを設定する必要があります。 個別のリリース パイプラインを作成する場合は、LCS の **資産のアップロード** を使い、CloudScaleUnitExtensionPackage.zip パッケージをアセット ライブラリにアップロードできます。 別のリリース パイプラインにではなく、LCS にアップロードする場合は、タスクをビルド パイプラインの一部として追加できます。

次の手順に従って、リリース パイプラインを設定して、CloudScaleUnitExtensionPackage.zip パッケージを LCS のアセット ライブラリにアップロードします。

1. Azure DevOps で、**リリース** から **新しいパイプライン** を選び、**テンプレートの空のジョブ** を選択します。
2. 新しいリリース パイプラインの名前を入力します。 既定の名前は、**アプリ パイプライン \> 新しいリリース パイプライン** です。
3. パイプラインで、**コンポーネントを追加** を選択します。
4. **コンポーネントを追加** ダイアログ ボックスでプロジェクトを選び、以前のセクションで作成したビルド パイプラインを選択します。
5. オプション: 作成したコンポーネントで **トリガー** ボタン (稲妻記号) を選択し、継続的配置トリガーを有効にしてから、ブランチなどを選択できます。

    > [!NOTE]
    > リリース パイプラインには、リリースのトリガー時期と方法が指定できる他のオプションも用意されています。

6. **保存** を選択して、パイプラインを保存します。 フォルダ名の入力を求めるメッセージが表示された場合は、任意のフォルダ名を入力します。
7. **ステージ** を選び、ステージ 1 **LCS に資産をアップデート** の名前を変え、**ジョブ 1** を選択します。
8. **タスク** で、**エージェント ジョブ** を選択します。
9. **タスクの追加** で、**Dynamics Lifecycle Services (LCS) 資産のアップロード** を検索し、**追加** を選択します。
10. アップロード タスクを設定するには、[Azure Pipelines を使用して資産をアップロード](../../fin-ops-core/dev-itpro/dev-tools/pipeline-asset-upload.md) の手順に従います。 タスクで、次の値を設定します。

    - **資産のタイプ:** CloudScaleUnitExtensionPackage
    - **アップロードするファイル:** $(System.DefaultWorkingDirectory)/\_ScaleUnit-CI/drop/ScaleUnitPackage\_$(Release.Artifacts.\_ScaleUnit-CI.BuildNumber).zip
    - **LCS 資産名:** ScaleUnitPackage\_$(Release.Artifacts.\_ScaleUnit-CI.BuildNumber)

        > [!NOTE]
        > 資産名は、名前付けガイドラインに従って変更できます。

11. タスクの構成が完了したら、**保存** を選び、リリース パイプラインを保存します。
12. **パイプライン** タブでパイプラインを選び、**リリースの作成** を選択します。
13. **新しいリリースの作成** ダイアログ ボックスで、Cloud Scale Unit コンポーネントを選び、**作成** からリリースを手動でトリガーします。

リリース パイプラインを自動化するには、継続的ビルドを構成します。 詳細については、[パイプラインのリリース](/azure/devops/pipelines/release) ドキュメントを参照します。

## <a name="set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages"></a>Retail セルフ サービス パッケージを生成するには、Azure DevOps のビルド パイプラインを設定

次の手順に従い、Retail Modern POS、Hardware Station および Cloud Scale Unit (セルフ ホスト) インストーラーを生成します。

1. Azure DevOps 組織にサイン インします。
2. **パイプライン** を選び、**新しいパイプライン** を選択します。
3. ソース リポジトリを選択します。
4. **既存の Azure Pipelines YAML ファイル** を選択します。
5. [ Dynamics365Commerce.InStore GitHub リポジトリの Pipeline/YAML\_Files ディレクトリから YAML ファイル (build-pipeline.yml)](https://github.com/microsoft/Dynamics365Commerce.InStore/blob/release/9.29/Pipeline/YAML_Files/build-pipeline.yml) を選択します。

    > [!NOTE]
    > YAML ファイルは、[Dynamics365Commerce.InStore GitHub リポジトリの Pipeline/PowerShellScripts ディレクトリ](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.29/Pipeline/PowerShellScripts) のスクリプトの一部を参照します。 これら全てのスクリプトをリポジトリに含めてください。 サンプル リポジトリをクローンする場合、すべてのスクリプトが既に含まれています。

6. **続行** を選択します。

    YAML ファイルには、証明書を使用して Modern POS および Hardware Station インストーラーに署名する手順が示されています。 スクリプトでは、Azure Key Vault の証明書ファイルが検索され、その証明書ファイルが署名に使用されます。 Azure Key Vault から証明書を読むには、アプリケーション ID、シークレット、証明書名およびタイムスタンプ サーバーの詳細 (タイムスタンプを使用して証明書に署名するために) を指定する必要があります。 詳細については、[Azure Key Vault から Azure ポータルを使用して証明書を設定および取得](/azure/key-vault/certificates/quick-create-portal) を参照します。

    パイプライン内のキー コンテナーとタイムスタンプ サーバーの詳細を表示するには、ビルド パイプラインの **変数** タブに次の変数を作成し、その値を指定します。 変数のセキュリティを確保するには、変数タイプとして **シークレット** を選択します。

    - ApplicationId
    - AzureKeyVaultURI
    - CertificateName
    - SecretValue
    - タイムスタンプ

        この変数の値として、`http://timestamp.digicert.com` の通り、タイムスタンプ プロバイダを指定できます。

    Azure に証明書を格納していない場合は、**セキュア タスク** オプションまたは Azure Pipelines がサポートする他のオプションを使用して、インストーラーに署名できます。

    インストーラに署名する必要がな場合は、署名ステップを YAML ファイルから削除できます。 YAML ファイルで、**PowerShell\@2** タスクを検索して、削除します。

    YAML ファイルのスクリプトはソリューション全体を構築し、アウトプット (HardwareStation.Installer.exe および ModernPos.Installer.exe パッケージ) をビルド用に **公開済みアーティファクト** のドロップ ロケーションにアップロードします。

    > [!NOTE]
    > YAML ファイルはリポジトリのソリューション ファイルを検索し、ソリューションを構築して、HardwareStation.Installer.exe および ModernPos.Installer.exe パッケージを検索します。 したがって、拡張機能プロジェクトと梱包プロジェクトがソリューションにリンクされている必要があります。 拡張プロジェクトをモデル化する方法については、[Dynamics365Commerce.InStore GitHub リポジトリ](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.29) のサンプルを参照します。

7. 変更を保存し、キューにビルドを追加します。
8. ビルドが完了すると、**公開済みアーティファクト** から **HardwarePos.Installer.exe** および **ModernPos.Installer.exe** パッケージをダウンロードできます。

## <a name="set-up-a-release-pipeline-for-retail-self-service-packages"></a>Retail セルフサービス パッケージのリリース パイプラインの設定

ベスト プラクティスとして、個別のビルド パイプラインとリリース パイプラインを設定する必要があります。 個別のリリース パイプラインを作成する場合は、LCS の **資産のアップロード** を使い、HardwareStation.Installer.exe および ModernPos.Installer.exe パッケージをアセット ライブラリにアップロードできます。 別のリリース パイプラインにではなく、LCS にアップロードする場合は、タスクをビルド パイプラインの一部として追加できます。

これらの手順に従い、リリース パイプラインを設定して、HardwareStation.Installer.exe および ModernPos.Installer.exe パッケージを LCS のアセット ライブラリにアップロードします。

1. Azure DevOps で、**リリース** から **新しいパイプライン** を選び、**テンプレートの空のジョブ** を選択します。
2. 新しいリリース パイプラインの名前を入力します。 既定の名前は、**アプリ パイプライン \> 新しいリリース パイプライン** です。
3. パイプラインで、**コンポーネントを追加** を選択します。
4. **コンポーネントを追加** ダイアログ ボックスで、リポジトリ プロジェクトを選び、以前のセクションで作成したビルド パイプラインを選択します。
5. オプション: 作成したコンポーネントで **トリガー** ボタン (稲妻記号) を選択し、継続的配置トリガーを有効にしてから、ブランチなどを選択できます。

    > [!NOTE]
    > リリース パイプラインには、リリースのトリガー時期と方法が指定できる他のオプションも用意されています。

6. **保存** を選択して、パイプラインを保存します。 フォルダ名の入力を求めるメッセージが表示された場合は、任意のフォルダ名を入力します。
7. **ステージ** を選び、ステージ 1 **LCS に資産をアップデート** の名前を変え、**ジョブ 1** を選択します。
8. **タスク** で、**エージェント ジョブ** を選択します。
9. **タスクの追加** で、**Dynamics Lifecycle Services (LCS) 資産のアップロード** を検索し、**追加** を選択します。
10. アップロード タスクを完全に設定するには、[Azure Pipelines を使用して資産をアップロード](../../fin-ops-core/dev-itpro/dev-tools/pipeline-asset-upload.md) の手順に従います。 タスクで、次の値を設定します。

    - **資産のタイプ:** Retail Self-Service Package
    - **アップロードするファイル:** $(System.DefaultWorkingDirectory)/\_CommerceSDK-Signing-EXE/drop/Installer\_$(Release.Artifacts.\_CommerceSDK-Signing-EXE.BuildNumber).exe
    - **LCS 資産名:** Installer\_$(Release.Artifacts.\_CommerceSDK-Signing-EXE.BuildNumber)

11. タスクの構成が完了したら、**保存** を選び、リリース パイプラインを保存します。
12. **パイプライン** タブでパイプラインを選び、**リリースの作成** を選択します。
13. **新しいリリースの作成** ダイアログ ボックスで、コンポーネントを選び、**作成** からリリースを手動でトリガーします。

リリース パイプラインを自動化するには、継続的ビルドを構成します。 詳細については、[パイプラインのリリース](/azure/devops/pipelines/release) ドキュメントを参照します。
