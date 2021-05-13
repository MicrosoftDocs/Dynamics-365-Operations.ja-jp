---
title: LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する (プレビュー)
description: このトピックでは、カスタム ハードウェアとローカル ビジネス データ (LBD) に基づく配置を使用して、オンプレミスのエッジ スケール ユニットをプロビジョニングする方法について説明します。
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 23ae1892f410dcbf0de5e656e35b0291372877dc
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938264"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

エッジ スケール ユニットは、Supply Chain Management の分散ハイブリッド トポロジで重要な役割を果たします。 ハイブリッド トポロジでは、Supply Chain Management のクラウド ハブとクラウド内またはエッジ上の追加のスケール ユニットとの間でワークロードを配布できます。

エッジ スケール ユニットは、ローカル ビジネス データ (LBD) [オンプレミス環境](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) を作成することで配置できます。 その後、Supply Chain Management の分散ハイブリッド トポロジで スケール ユニットとして機能するように構成します。 これは、オンプレミスの LBD 環境を、ハブとして機能するように構成されたクラウド内の Supply Chain Management 環境に関連付けることで実現されます。  

エッジ スケール ユニットは、現在プレビュー中です。 したがって、このタイプの環境は、[プレビュー条件](https://aka.ms/scmcnepreviewterms) に従ってのみ使用できます。

このトピックでは、オンプレミスの LBD 環境をエッジ スケール ユニットとして設定し、それをハブに関連付ける方法について説明します。

## <a name="deployment-overview"></a>配置の概要

次に配置の手順の概要について示します。

1. **Microsoft Dynamics Lifecycle Services (LCS) で LBD プロジェクトの LBD スロットを有効にします。**

    プレビュー時に、LBD エッジ スケール ユニットは既存の LBD 顧客をターゲットとしています。 追加の 60 日間限定 LBD サンドボックス スロットは、特定の顧客の状況でにのみ提供されます。

1. ***空* のデータベースを使用して LBD 環境を設定および配置します。**

    LCS を使用して、最新のトポロジと空のデータベースで LBD 環境を配置します。 詳細については、このトピックの後半にある[空のデータベースを使用して LBD 環境の設定および配置](#set-up-deploy) セクションを参照してください。 ハブおよびスケール ユニット環境間で、プラットフォーム更新プログラム 43 以上を備えた Supply Chain Management バージョン 10.0.19 を使用する必要があります。

1. **LCS でターゲット パッケージを LBD プロジェクト資産にアップロードします。**

    アプリケーション、プラットフォーム、およびハブとエッジ スケール ユニット間で使用するカスタマイズ パッケージを準備します。 詳細については、このトピックの後半にある[LCS でターゲット パッケージを LBD プロジェクト資産にアップロード](#upload-packages) を参照してください。

1. **ターゲット パッケージを使用して LBD 環境にサービスを提供します。**

    この手順により、同じビルドとカスタマイズがハブとスポークに配置されます。 詳細については、このトピックの後半にある[ターゲット パッケージを使用して LBD 環境にサービスを提供](#service-target-packages) セクションを参照してください。

1. **スケール ユニットの構成とワークロードの割り当てを完了します。**

    詳細については、このトピックの後半の[LBD エッジ スケール ユニットをハブに割り当てる](#assign-edge-to-hub) セクションを参照してください。

このトピックの残りのセクションでは、これらの手順を完了する方法に関する詳細をさらに提供します。

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a> 空のデータベースを使用して LBD 環境を設定および配置

この手順により、機能的な LBD 環境が作成されます。 ただし、環境はアプリケーションとプラットフォーム バージョンがハブ環境と同じである必要はありません。 また、カスタマイズされていないので、スケール ユニットとして機能することはまだ有効ではありません。

1. [オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 41 以降)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) の指示に従います。 ハブおよびスケール ユニット環境間で、プラットフォーム更新プログラム 43 以上を備えた Supply Chain Management バージョン 10.0.19 を使用する必要がある

    > [!IMPORTANT]
    > このトピックの手順を完了する **前** に、このセクションの残りの部分を読みます。

1. infrastructure\\ConfigTemplate.xml ファイルで構成を説明する前に、次のスクリプトを実行します。

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > このスクリプトは、エッジ スケール ユニットの配置に必要ない構成を削除します。

1. [データベースの構成](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) で説明されているように、空のデータを含むデータベースを設定します。 この手順では空の data.bak ファイルを使用します。
1. 配置前スクリプトを設定します。 詳細については、[ローカル エージェントの配置前スクリプトと配置後スクリプト](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md) を参照してください。

    1. **インフラストラクチャ スクリプト** の **ScaleUnit** フォルダーから、環境で設定されたエージェント ファイル ファイル ストレージ共有の **スクリプト** フォルダーに内容をコピーします。 通常、パスは  \\\\lbdiscsi01\\agent\\Scripts です。
    2. 必要なパラメータを使用してスクリプトを呼び出す **PreDeployment.ps1** スクリプトを作成します。 配置前スクリプトは、エージェント ファイルストレージ共有の **スクリプト** フォルダーに配置する必要があります。 そうしない場合は実行されません。 通常、パスは \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1 です。

        PreDeployment.ps1 スクリプトの内容は、次の例のようになります。

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a> LCS でターゲット パッケージを LBD プロジェクト資産にアップロード

この手順では、LBD スケール ユニット環境に移行するアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズを準備します。

1. ハブ環境に適用されたものと同じ、結合されたアプリケーション/プラットフォーム パッケージを、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。
1. ハブ環境に適用されたカスタム配置可能パッケージのコピーを取得し、LCS オンプレミス プロジェクトのアセット ライブラリにアップロードします。

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a> ターゲット パッケージを使用して LBD 環境にサービスを提供

この手順では、LBD スケール ユニット環境のアプリケーション バージョン、プラットフォーム バージョン、およびカスタマイズをハブに対応するようになります。

1. 前の手順でアップロードした結合されたアプリケーション/プラットフォーム パッケージを使用して、LBD 環境にサービスを提供します。
1. 前の手順でアップロードしたカスタム配置可能パッケージを使用して、LBD 環境にサービスを提供します。

    ![管理を選択 > LCS で更新プログラムを適用](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "管理を選択 > LCS で更新プログラムを適用")

    ![カスタマイズ パッケージの選択](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "カスタマイズ パッケージの選択")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a> LBD エッジ スケール ユニットをハブに割り当てる

エッジ スケール ユニットがまだプレビューされている間に、GitHub で利用可能な [スケール ユニット配置および構成ツール](https://github.com/microsoft/SCMScaleUnitDevTools) を使用して、LBD エッジ スケール ユニットをハブに割り当てる必要があります。 このプロセスにより、LBD 構成をエッジ スケール ユニットとして機能させ、ハブに関連付けることができます。 このプロセスは、1 ボックス開発環境の構成に似ています。

1. [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) の最新のリリースをダウンロードし、ファイルの内容を解凍します。
1. `UserConfig.sample.xml` ファイルのコピーを作成し、`UserConfig.xml` と名前を付けます。
1. [スケール ユニットとワークロードの配置ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations) で説明したように、Azure AD テナントに Microsoft Azure Active Directory (Azure AD) アプリケーションを作成します。
    1. 作成されると、ハブの Azure AD アプリケーション フォーム (SysAADClientTable) に移動します。
    1. 新しいエントリを作成し、作成したアプリケーションの ID に **クライアント ID** を設定します。 **名前** を *ScaleUnits*、**ユーザー ID** を *管理者* に設定します。

1. [スケール ユニットとワークロードの配置ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations) で説明したように、Active Directory フェデレーション サービス (AD FS) アプリケーションを作成します。
    1. 作成されると、エッジ スケール ユニットの Azure AD アプリケーション フォーム (SysAADClientTable) に移動します。
    1. 新しいエントリを作成し、作成したアプリケーションの ID に **クライアント ID** を設定します。 **ユーザー ID** を *管理者* に設定します。

1. `UserConfig.xml` ファイルを変更します。
    1. `InterAOSAADConfiguration` セクションで、以前作成した Azure AD アプリケーションからの情報を入力します。
        - `AppId` 要素に、Azure アプリケーションのアプリケーション ID を入力します。
        - `AppSecret` 要素に、Azure アプリケーションのアプリケーション シークレットを入力します。
        - `Authority` 要素には、テナントのセキュリティ オーソリティを指定する URL が含まれている必要があります。

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. `ScaleUnitConfiguration` セクションの最初の `ScaleUnitInstance` セクションで、`AuthConfiguration` セクションを変更します。
        - `AppId` 要素に、Azure アプリケーションのアプリケーション ID を入力します。
        - `AppSecret` 要素に、Azure アプリケーションのアプリケーション シークレットを入力します。
        - `Authority` 要素には、テナントのセキュリティ オーソリティを指定する URL が含まれている必要があります。

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. また、これと同じ `ScaleUnitInstance` に、次の値を設定します:
        - `Domain` 要素で、ハブの URL を指定します。 例: `https://cloudhub.sandbox.operations.dynamics.com/`
        - `EnvironmentType` 要素で、値が `LCSHosted` に設定されている必要があります。

    1. `ScaleUnitConfiguration` セクションの 2 つ目の `ScaleUnitInstance` セクションで、`AuthConfiguration` セクションを変更します。
        - `AppId` 要素に、AD FS アプリケーションのアプリケーション ID を入力します。
        - `AppSecret` 要素に、ADFS アプリケーションのアプリケーション シークレットを入力します。
        - `Authority` 要素には、AD FS インスタンスの URL が含まれている必要があります。

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. また、これと同じ `ScaleUnitInstance` に、次の値を設定します:
        - `Domain` 要素で、エッジ スケール ユニットの URL を指定します。 例: https://ax.contoso.com/
        - `EnvironmentType` 要素で、値が LBD に設定されている必要があります。
        - `ScaleUnitId` 要素には、`Configure-CloudandEdge.ps1`  配置前スクリプトの構成時に `InstanceId` に指定した値と同じ値を入力します。

        > [!NOTE]
        > 既定の ID (@A) を使用しない場合、ワークロード セクションの各 ConfiguredWorkload に対して ScaleUnitId を更新してください。

1. PowerShell を開き、`UserConfig.xml` ファイルを含むフォルダーに移動します。

1. このコマンドを使用してツールを実行します。

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > すべてのアクションの後、ツールを再起動する必要があります。

1. このツールで **2. ワークロードのインストールのための環境を準備** を選択します。 次の手順を実行します:
    1. **1. ハブを準備** を選択します。
    1. **2. スケール ユニットを準備** を選択します。

    > [!NOTE]
    > このコマンドをクリーン インストールから実行していない場合にエラーが発生した場合は、次の操作を行います:
    >
    > - `aos-storage` フォルダーからすべてのフォルダーを削除します (`GACAssemblies` を除く)。
    > - ビジネス データ データベース (AXDB) で次の SQL コマンドを実行します。
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. ビジネス データ データベース (AXDB) で次の SQL コマンドを実行します。

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. ビジネス データベース (AXDB) で変更追跡が有効になっていることを確認
    1. SQL Server Management Studio (SSMS) を開始します。
    1. ビジネス データベース (AXDB) を右クリックし、プロパティ を選択します。
    1. 開くウィンドウで **変更追跡** を選択し、次の設定を行います。

        - **変更追跡:** *True*
        - **留保期間:** *7*
        - **留保単位:** *Days*
        - **自動クリーンアップ:** *True*

1. ツールで **3. ワークロードをインストール** を選択します。 次の手順を実行します:
    1. **1. ハブでインストール** を選択します。
    1. **2. スケール ユニットでインストール** を選択します。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
