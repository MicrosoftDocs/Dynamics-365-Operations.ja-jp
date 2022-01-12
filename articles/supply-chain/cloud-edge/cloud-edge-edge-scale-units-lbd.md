---
title: LBD を使用したカスタム ハードウェアへのエッジのスケール ユニットの展開
description: このトピックでは、カスタム ハードウェアとローカル ビジネス データ (LBD) に基づく配置を使用して、オンプレミスのエッジ スケール ユニットをプロビジョニングする方法について説明します。
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2407d4e3c6adaf5df2e8f5440ee8336f86012caf
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920676"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>LBD を使用したカスタム ハードウェアへのエッジのスケール ユニットの展開

[!include [banner](../includes/banner.md)]

エッジ スケール ユニットは、Supply Chain Management の分散ハイブリッド トポロジで重要な役割を果たします。 ハイブリッド トポロジでは、Supply Chain Management のクラウド ハブとクラウド内またはエッジ上の追加のスケール ユニットとの間でワークロードを配布できます。

エッジ スケール ユニットは、ローカル ビジネス データ (LBD) [オンプレミス環境](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) を作成することで配置できます。 その後、Supply Chain Management の分散ハイブリッド トポロジで スケール ユニットとして機能するように構成します。 これは、オンプレミスの LBD 環境を、ハブとして機能するように構成されたクラウド内の Supply Chain Management 環境に関連付けることで実現されます。  

このトピックでは、オンプレミスの LBD 環境をエッジ スケール ユニットとして設定し、それをハブに関連付ける方法について説明します。

## <a name="deployment-overview"></a>配置の概要

次に配置の手順の概要について示します。

1. **Microsoft Dynamics Lifecycle Services (LCS) で LBD プロジェクトの LBD スロットを有効にします。**

1. ***空* のデータベースを使用して LBD 環境を設定および配置します。**

    LCS を使用して、最新のトポロジと空のデータベースで LBD 環境を配置します。 詳細については、このトピックの後半にある[空のデータベースを使用して LBD 環境の設定および配置](#set-up-deploy) セクションを参照してください。 ハブおよびスケール ユニット環境間で、Supply Chain Management バージョン 10.0.21 以降を使用する必要があります。

1. **LCS でターゲット パッケージを LBD プロジェクト資産にアップロードします。**

    アプリケーション、プラットフォーム、およびハブとエッジ スケール ユニット間で使用するカスタマイズ パッケージを準備します。 詳細については、このトピックの後半にある[LCS でターゲット パッケージを LBD プロジェクト資産にアップロード](#upload-packages) を参照してください。

1. **ターゲット パッケージを使用して LBD 環境にサービスを提供します。**

    この手順により、同じビルドとカスタマイズがハブとスポークに配置されます。 詳細については、このトピックの後半にある[ターゲット パッケージを使用して LBD 環境にサービスを提供](#service-target-packages) セクションを参照してください。

1. **スケール ユニットの構成とワークロードの割り当てを完了します。**

    詳細については、このトピックの後半の[LBD エッジ スケール ユニットをハブに割り当てる](#assign-edge-to-hub) セクションを参照してください。

このトピックの残りのセクションでは、これらの手順を完了する方法に関する詳細をさらに提供します。

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a> 空のデータベースを使用して LBD 環境を設定および配置

この手順により、機能的な LBD 環境が作成されます。 ただし、環境はアプリケーションとプラットフォーム バージョンがハブ環境と同じである必要はありません。 また、カスタマイズされていないので、スケール ユニットとして機能することはまだ有効ではありません。

1. [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) の指示に従います。 ハブおよびスケール ユニット環境間で、Supply Chain Management バージョン 10.0.21 以降を使用する必要があります。 さらに、バージョン 2.12.0 以降のインフラストラクチャ スクリプトを使用する必要があります。 

    > [!IMPORTANT]
    > このトピックの手順を完了する **前** に、このセクションの残りの部分を読みます。

1. infrastructure\\ConfigTemplate.xml ファイルで構成を説明する前に、次のスクリプトを実行します。

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > このスクリプトは、エッジ スケール ユニットの配置に必要ない構成を削除します。

1. [データベースの構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) で説明されているように、空のデータを含むデータベースを設定します。 この手順では空の data.bak ファイルを使用します。
1. [データベースの構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)手順が完了したら、次のスクリプトを実行して、スケール ユニット ALM オーケストレーター データベースを構成します。

    > [!NOTE]
    > [データベースの構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)手順では、Financial Reporting データベースを構成しないでください。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Initialize-Database.ps1 スクリプトは、以下の処理を行います:

    1. **ScaleUnitAlmDb** という名前の空のデータベースを作成します。
    2. 次の表に基づいて、データベース ロールにユーザーをマップします。

        | ユーザー            | 種類 | データベース ロール |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. 引き続き、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) の指示に従います。
1. [AD FS の構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb)手順が完了したら、次の手順に従います。

    1. ALM オーケストレーション サービスと Application Object Server (AOS) との通信を可能にする、新しい Active Directory フェデレーション サービス (AD FS) アプリケーションを作成します。

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. ALM オーケストレーション サービスとスケール ユニット管理サービスとの通信を可能にする新しい Azure Active Directory(Azure AD) アプリケーションを作成します。

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. 引き続き、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) の指示に従います。 ローカル エージェントのコンフィギュレーションを入力する必要がある場合、必ずエッジ スケール ユニット機能を有効にし、必要なすべてのパラメーターを指定します。

    ![エッジ スケール ユニットの機能を有効化する。](media/EnableEdgeScaleUnitFeatures.png "エッジ スケール ユニットの機能を有効化する")

1. LCS から環境を展開する前に、展開前のスクリプトを設定します。 詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md) を参照してください。

    1. **インフラストラクチャ スクリプト** の **ScaleUnit** フォルダーから、環境で設定されたエージェント ファイル ファイル ストレージ共有の **スクリプト** フォルダーに Configure-CloudAndEdge.ps1 スクリプトをコピーします。 通常、パスは  \\\\lbdiscsi01\\agent\\Scripts です。
    2. 必要なパラメータを使用してスクリプトを呼び出す **PreDeployment.ps1** スクリプトを作成します。 配置前スクリプトは、エージェント ファイルストレージ共有の **スクリプト** フォルダーに配置する必要があります。 そうしない場合は実行されません。 通常、パスは \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1 です。

        PreDeployment.ps1 スクリプトの内容は、次の例のようになります。

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > InstanceId パラメータは、2 文字にのみにする必要があります。 最初の文字は @ で、2 番目の文字は英語のアルファベットの任意の大文字にできます。
        >
        > - 有効な値:
        >   - @D
        >   - @X
        > - 無効な値:
        >   - @a
        >   - @4
        >   - @#

1. 使用可能な最新の基準トポロジを使用して環境を配置します。
1. 環境を配置したら、次の手順に従います。

    1. ビジネス データ データベース (AXDB) で次の SQL コマンドを実行します。

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. 同時最大バッチ セッションの値を 4 よりも大きい値に増やします。

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. ビジネス データベース (AXDB) で変更追跡が有効になっていることを確認します。

        1. SQL Server Management Studio (SSMS) を起動します。
        1. ビジネス データベース (AXDB) を選択したまま (または右クリック) にしてから、**プロパティ** を選択します。
        1. 表示されたウィンドウで **変更追跡** を選択し、次の値を設定します。

            - **変更追跡:** *True*
            - **留保期間:** *7*
            - **留保単位:** *Days*
            - **自動クリーンアップ:** *True*

    1. スケール ユニットで Azure AD アプリケーション テーブルに、(Create-ADFSServerApplicationForEdgeScaleUnits.ps1 スクリプトを使用して) 前の手順で作成した AD FS アプリケーション ID を追加します。 この手順は、ユーザー インターフェイス (UI) を通じて手動で実行できます。 次のスクリプトを使用してデータベースを介して実行することもできます。

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Azure Key Vault と Azure AD アプリケーションを設定してスケール ユニット間の通信を有効にする

1. 環境を配置した後、追加の Azure AD アプリケーションを作成し、ハブとスケール ユニットの間の信頼済の通信を有効にしてください。

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. アプリケーションを作成した後、クライアント シークレットを作成し、その情報を Azure Key Vault に保存する必要があります。 さらに、作成した Azure AD アプリケーションにアクセス権を付与して、キー コンテナーに保管されたシークレットを取得できるようにする必要があります。 便宜上、次のスクリプトによって、必要なすべてのアクションが自動的に実行されます。

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > 指定された **KeyVaultName** 値を持つキー コンテナーが存在しない場合、スクリプトによって自動的にキー コンテナーが作成されます。

1. 前の手順で作成した (Create-SpokeToHubAADApplication.ps1 スクリプトを使用して) Azure AD アプリケーション ID を、ハブ内の Azure AD アプリケーション テーブルに追加します。 この手順は、UI を通じて手動で実行できます。

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a> LCS でターゲット パッケージを LBD プロジェクト資産にアップロード

この手順では、LBD スケール ユニット環境に移行するアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズを準備します。

1. ハブ環境に適用されたものと同じ、結合されたアプリケーション/プラットフォーム パッケージを、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。
1. ハブ環境に適用されたカスタム配置可能パッケージのコピーを取得し、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a> ターゲット パッケージを使用して LBD 環境にサービスを提供

この手順では、LBD スケール ユニット環境のアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズをハブに対応するようになります。

1. 前の手順でアップロードした結合されたアプリケーション/プラットフォーム パッケージを使用して、LBD 環境にサービスを提供します。
1. 前の手順でアップロードしたカスタム配置可能パッケージを使用して、LBD 環境にサービスを提供します。

    ![LCS で更新を適用する。](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "LCS で更新を適用する")

    ![カスタマイズ パッケージの選択。](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "カスタマイズ パッケージの選択")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a> LBD エッジ スケール ユニットをハブに割り当てる

エッジ スケール ユニットの構成および管理は、スケール ユニット管理ポータルを介して行います。 詳細については、[スケール ユニット マネージャー ポータルを使用したスケール ユニットとワークロードの管理](./cloud-edge-landing-page.md#scale-unit-manager-portal)を参照してください。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
