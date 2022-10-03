---
title: オンプレミス環境での Retail チャネルのコンポーネントのインストール手順
description: この記事では、オンプレミス環境でのコマース チャネルのコンポーネントのインストール手順について説明します。
author: jashanno
ms.date: 08/31/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: de4bb653a2d344c1ea01ad1e255a9982ba6c4e12
ms.sourcegitcommit: 346a9ca833237836d5e4ca496aeb2b5b24bdb27b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2022
ms.locfileid: "9583767"
---
# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a>オンプレミス環境での Retail チャネルのコンポーネントのインストール手順

[!include[banner](../includes/banner.md)]

この記事では、オンプレミス環境でのコマース チャネルのコンポーネントのインストール手順について説明します。

> [!IMPORTANT]
> 現在、セルフサービス パッケージがオンプレミス環境に正しく適用されないという既知の問題があります。 そのため、インストーラーを Microsoft Dynamics Lifecycle Services から直接プルし、必要に応じて使用することをお勧めします。 この場合、Commerce headquarters はインストーラーのダウンロードに使用されなくなりますが、必要に応じて構成ファイルだけをダウンロードするために使用されます。

オンプレミス環境では、チャネル機能は Commerce Scale Unit (自己ホスト) の使用により排他的に有効になります。 概要については、[Commerce Scale Unit (自己ホスト)](../../../commerce/dev-itpro/retail-store-system-begin.md) を参照してください。 

クラウド展開とは異なり、オンプレミス環境では Lifecycle Services 経由でチャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。 Commerce Scale Unit (自己ホスト) をインストールすることによってのみ、チャネル コンポーネントを使用できます。

## <a name="prerequisites"></a>必要条件 

チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。 この手順は、[オンプレミス環境の設定と配置 (Platform update 41 以降)](setup-deploy-on-premises-pu41.md)で説明されています。 少なくとも、Commerce を完全に機能させるには、バージョン 8.1.1 をインストールする必要があります。 使用可能な最新のアプリケーション バージョンに更新することをお勧めします。

> [!NOTE]
> 誰もが自由にアクセスできない、セキュリティで保護されたネットワークを使用して、Commerce Scale Unit をバック オフィスに接続することが絶対に必要です。 さらに、バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の Commerce Scale Unit デバイスのみに許可されるように制限してください。 この場合、ファイアウォールが必要となるため、セーフ リストへの追加を強くお勧めします。

## <a name="installation-steps"></a>インストール手順

1. 以前に作成した [アプリケーションの共有](setup-deploy-on-premises-pu41.md#setupfile) (**LocalAgent** 共有フォルダではなく) にて、共有の場所のルート ディレクトリに **selfservicepackages** という名前のフォルダーを作成します。  
2. 各 AOS ノードで、簡単にアクセスできるディレクトリを作成します (**C:\\RetailSelfService** など)。
3. 1 つの AOS ノード (どのノードかは関係ありません) で、**RetailUpdateDatabase.ps1** スクリプトを実行します。 リモート処理スクリプトを使用した場合、このスクリプトは各 AOS ノードのパス **C:\\D365FFO-LBD** で使用できます。

    Commerce Headquarters のバージョンがバージョン 10.0.0 以降の場合は、次の PowerShell スクリプトを実行します。

    ```powershell
    .\RetailUpdateDatabase.ps1 -envName '<Environment name>' -AosUrl 'https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF/' -SendProductSupportTelemetryToMicrosoft
    ```

    Commerce Headquarters のバージョンが 10.0.0 より前のバージョンの場合は、次の PowerShell スクリプトを実行します。

    ```powershell
    .\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database>' -DatabaseName '<Database name for AOS database>' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages, such as C:\RetailSelfService>' -SendProductSupportTelemetryToMicrosoft
    ```

    - **-envName** パラメーターは、当初の配置時に Microsoft Dynamics Lifecycle Services の環境に割り当てられた名前です。
    - **-SendProductSupportTelemetryToMicrosoft** パラメーターは、Microsoft へのテレメトリを有効にするために必要です。 テレメトリは、Microsoft によるサポートを最大限に受けるために不可欠です。
    - スクリプトは、サービスのユーザーとロールの更新や、レジストリ キーの更新を含むさまざまなアクションを実行します。

    > [!IMPORTANT]
    > 現在、セルフサービス パッケージがオンプレミス環境に正しく適用されないという既知の問題があります。 そのため、インストーラーを Lifecycle Services から直接プルし、必要に応じて使用することをお勧めします。 この場合、Commerce headquarters はインストーラーのダウンロードに使用されなくなりますが、必要に応じて構成ファイルだけをダウンロードするために使用されます。

4. それぞれの AOS ノードで、次の PowerShell スクリプトを実行します。

    ```powershell
    .\RetailUpdateDatabase.ps1 -RetailSelfServicePackages 'C:\RetailSelfService\Packages'
    ```

    > [!NOTE]
    > **-RetailSelfServicePackages** パラメーターは、この手順の最初で作成したフル パスの場所です (**C:\\RetailSelfService**)。

5. Commerce インストーラーを取得するには、Lifecycle Services から適切なバイナリ更新をダウンロードしてください。 手順については、 [Lifecycle Services (LCS) から更新プログラムをダウンロードする](../migration-upgrade/download-hotfix-lcs.md) を参照してください。
6. ZIP ファイルを展開し、すべてのセルフサービス インストーラーを、手順 2 において各 AOS コンピューターで定義および作成された **C:\\RetailSelfService** フォルダーにコピーします。 セルフサービス インストーラーは次の 6 つです:

    - AsyncServerConnectorServiceSetup.exe
    - RealtimeServiceAX63Setup.exe
    - HardwareStationSetup.exe
    - ModernPosSetup.exe
    - ModernPosSetupOffline.exe
    - StoreSystemSetup.exe

    > [!NOTE]
    > クラウド環境では、Lifecycle Services で入手可能なものから、Headquarters でセルフサービス インストーラーを同期できます ([Dynamics 365 Commerce のセルフサービス インストーラーの同期](../../../commerce/dev-itpro/synchronize-installers.md))。 オンプレミス環境では、この機能を使用できません。 ただし、これらの環境は Lifecycle Services からダウンロードできます。 この SDK は、展開可能な zip 形式のパッケージ ファイルに含まれています。 セルフサービス インストーラーは、Lifecycle Services **アセット ライブラリ** から入手できます。 Lifecycle Services 内からアップロードやダウンロードの仕組みを使用することはできますが、Headquarters の同期機能は機能しません。

7. AD FS コンピューターに移動し、管理者特権で PowerShell ウィンドウを開き、インフラストラクチャ スクリプト フォルダーを含むファイル共有に移動して、次のコマンドを実行します。 

    ```powershell
    # Host URL is your DNS record\host name for accessing the AOS
    .\Create-ADFSServerApplicationForRetail -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
    ```

    > [!NOTE]
    > セキュリティのベスト プラクティスとして、各 Commerce Scale Unit でこのスクリプトを実行する必要があります。 これにより、セキュリティを最大限に高め、セキュリティ侵害が発生した場合のワークロードを最小限に抑えることができます。

8. AD FS 管理で **アプリケーション グループ** から新しく生成されたサーバー アプリケーションにアクセスします。
9. 新しく生成されたサーバー アプリケーションを編集し、**シークレットをリセット** を選択します。

    > [!NOTE]
    > このシークレットを安全に保つことが重要です。 1 回だけコピーし、システムに保存しないでください。 生成されたクライアント ID とシークレットは、Commerce Scale Unit インストーラーで使用されます。 そのため、後で必要になります。 シークレットはいつでもリセットできますが、前のシークレットを使用した Commerce Scale Unit で更新する必要があります。

10. Commerce Headquarters で、**Retail と Commerce \> Headquarters の設定 \> パラメーター \> Commerce 共有パラメーター** の順に移動します。
11. **セキュリティ** タブの **取引サービスの従来のプロパティ** の下で、**Real-time Service プロファイル** フィールドを選択し、新たに作成した **既定値** の値を選択します。
12. **ID プロバイダー** タブの **ID プロバイダー** FastTab で **追加** を選択します。
13. 新しい **発行者** 行で、新しい ID プロバイダー値 `https://sts.windows.net/` をフィールドに入力します。
14. アクション ウィンドウで、**保存** を選択します。
15. **Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パラメーター** の順にクリックします。
16. **全般** タブで、**初期化** リンクを選択し、コマース機能のシード データを構成します。

    > [!NOTE]
    > - この記事の冒頭にある、重要なメッセージをお読みください。インストーラーがダウンロードのためにバックオフィスを介して機能することがなくなったという既知の問題に関するものです。
    > - 初めてダウンロードを試したときに、インストーラーは関連ページからダウンロードされません。 この動作は、インストーラーはダウンロードの場所に配置されたばかりで、関連付けられているデータベースの値がまだ存在しないために発生します。 Commerce headquarters (例: Commerce Scale Unit や Modern POS) で **ダウンロード** 機能が試行すると、エラーが表示されます。 次に、自動アップロード機能が起動し、2 回目のダウンロード試行時にインストーラーがダウンロードできるようになります。 (1 分待ってからインストーラを再度ダウンロードしてください。)
    > - 周辺機器シミュレータ (本社の ハードウェアプロファイル ページにてダウンロードできます) は、最低でも1つのハードウェア プロファイルが作成され、動作可能となるまで使用することができません。 それらが完了していれば、以下のスクリプトを実行することができます。
    >
    >     ```powershell
    >     .\RetailUpdateDatabase.ps1 -envName '<Environment name>' -UpdateRetailHardwareProfileSelfServicePackage
    >     ```

17. Commerce Scale Unit をインストールするためのインストール手順に従います。 手順については、[Commerce Scale Unit (自己ホスト) のコンフィギュレーションとインストール](../../../commerce/dev-itpro/retail-store-scale-unit-configuration-installation.md) を参照してください。 この記事の複数の場所で、注記はオンプレミス配置の手順の変更に言及しています。 これらの各変更に注意することが重要です。 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
