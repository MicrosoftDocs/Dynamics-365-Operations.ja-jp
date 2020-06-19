---
title: オンプレミス環境での小売チャネルのコンポーネントのインストール手順
description: このトピックでは、オンプレミス環境でのコマース チャネルのコンポーネントのインストール手順について説明します。
author: jashanno
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 3e17193189a86aeb952edd90442a096b8a47e3a3
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426383"
---
# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a>オンプレミス環境での小売チャネルのコンポーネントのインストール手順

[!include[banner](../includes/banner.md)]

このトピックでは、オンプレミス環境でのコマース チャネルのコンポーネントのインストール手順について説明します。

## <a name="overview"></a>概要

オンプレミス環境では、チャネル機能は Commerce Scale Unit (自己ホスト) の使用により排他的に有効になります。 概要については、[Commerce Scale Unit (自己ホスト)](../../../retail/dev-itpro/retail-store-system-begin.md) を参照してください。 

クラウド展開とは異なり、オンプレミス環境では Lifecycle Services (LCS) 経由でチャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。 Commerce Scale Unit (自己ホスト) をインストールすることによってのみ、チャネル コンポーネントを使用できます。

## <a name="prerequisites"></a>必要条件 

チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。 この手順は、[オンプレミス環境の設定と配置 (Platform update 12 以降)](setup-deploy-on-premises-pu12.md)で説明されています。 さらに、コマースの全機能を使用するは、バージョン 8.1.1 をインストールする必要があります。 バージョン 8.1.2 に更新することをお勧めします。

> [!NOTE]
> 誰もが自由にアクセスできない、セキュリティで保護されたネットワークを使用して、Commerce Scale Unit をバック オフィスに接続することが絶対に必要です。 さらに、バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の Commerce Scale Unit デバイスのみに許可されるように制限してください。 つまり、ファイアウォールが存在する必要があります。ホワイトリストへの追加を強くお勧めします。

## <a name="installation-steps"></a>インストール手順

1. 以前に作成した [アプリケーションの共有](setup-deploy-on-premises-pu12.md#setupfile) ( **LocalAgent** 共有フォルダではありません) にて、共有を行う場所のルートディレクトリに **selfservicepackages** という名称のフォルダを作成します。  
2. 各 AOS コンピューターで、簡単にアクセスできるディレクトリを作成します (**C:/selfservicepackages** など)。
3. いづれかのAOSコンピュータ (どれでも構いません) 上で、次のPowerShellスクリプトを実行します。

    ```powershell
    .\RetailUpdateDatabase.ps1 -envName '<Environment name>' -AosUrl 'https://<My Environment Name>.com/namespaces/AXSF/' -SendProductSupportTelemetryToMicrosoft
    ```
    > [!IMPORTANT]
    > 上記の手順は、バージョン10.0以降にて有効です。  Retail オンプレミス機能のオリジナル 8.1.3 版では、オリジナルバージョンのスクリプト区切り文字を使用する必要があります。
    >
    > ```powershell
    > .\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database>' -DatabaseName '<Database name for AOS database>' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages, such as **C:/selfservicepackages**>' -SendProductSupportTelemetryToMicrosoft
    > ```
    > - パラメーター **- envName** は、環境が生成されるときに作成時に既知である必要があります。
    > - 従来のパラメータ **-DatabaseServer** および **-DatabaseName** が環境設定に基づいて認識される必要があります。
    > - パラメーター **-SendProductSupportTelemetryToMicrosoft** は、Microsoft へのテレメトリを有効にするための必須の値です。  これは、Microsoft によるサポートを最大限に受けるために不可欠です。
    > - このスクリプトは、サービスのユーザーとロールの更新や、レジストリ キーの更新を含むさまざまなアクションを実行します。

4. それぞれのAOS コンピューターで、次の PowerShell スクリプトを実行します。

   ```powershell
   .\RetailUpdateDatabase.ps1 -RetailSelfServicePackages 'C:\RetailSelfService\Packages'
   ```

    > [!NOTE]
    > パラメーター **-RetailSelfServicePackages** は、この手順の最初で作成したフル パスの場所です (**C:/selfservicepackages**)。

5.  コマース インストーラーを使用するには、LCS から適切なバイナリ更新をダウンロードしてください。 手順については、 [Lifecycle Services (LCS) から更新プログラムをダウンロードする](../migration-upgrade/download-hotfix-lcs.md) を参照してください。
6.  ZIP ファイルを展開し、すべてのセルフ サービス インストーラーを、手順 2 において各 AOS コンピューターで定義および作成された **C:/selfservicepackages** フォルダーにコピーします。 6 つのセルフ サービス インストーラーは次のとおりです。 
    - AsyncServerConnectorServiceSetup.exe
    - RealtimeServiceAX63Setup.exe
    - HardwareStationSetup.exe
    - ModernPosSetup.exe
    - ModernPosSetupOffline.exe
    - StoreSystemSetup.exe
7.  ADFS コンピューターに移動し、InfrastructureScripts フォルダに移動してください。 これは、以前に実行した PowerShell スクリプトがあったのと同じファイル ディレクトリです (**RetailUpdateDatabase.ps1**)。 PowerShell スクリプト **Create-ADFSServerApplicationForRetail.ps1** を見つけます。
8.  ご利用の ADFS コンピューターで、新規 PowerShell ウィンドウから **.\Create-ADFSServerApplicationForRetail -HostUrl 'https://ax.d365ffo.onprem.contoso.com'** コマンドを使用してこのスクリプトを実行します。 **HostUrl** の値は Service Fabric にて確認することができます。  **HostUrl** 値を見つけるには、 **Service Fabric** &gt; **アプリケーション ファブリック:/AXSF** &gt; **詳細** &gt; **Aad_AADValidAudience** に移動します。
9.  AD FS 管理の **アプリケーション グループ** から新しく生成されたサーバー アプリケーションにアクセスします。
10.  新しく生成されたサーバー アプリケーションを編集し、**シークレットをリセット** を選択します。

     > [!NOTE]
     > これは、各 Commerce Scale Unit でこのスクリプトを実行する重要なセキュリティ手法です。  これにより、セキュリティが最大化され、セキュリティ侵害が発生した場合のワークロードが最小化されます。 
     >
     > このシークレットを安全に保つことが重要です。 このシークレットは、1 回だけコピーしてください。システムに保存しないでください。  生成されたクライアント ID とシークレットは、Commerce Scale Unit インストーラーの実行中に使用されるため、後で使用する必要があります。  シークレットはいつでも再度リセットできますが、前のシークレットを使用した Commerce Scale Unit で更新する必要があります。

11.  **Retail とコマース** &gt; **バックオフィスの設定** &gt; **コマース スケジューラ** &gt; **Microsoft Dynamics AX のコネクタ**の順に移動します。
12.  アクション ウィンドウで **編集** を選択します。
13.  **プロファイル** フィールドに、**既定**値を入力します。  必要に応じて、**説明** フィールドに説明を入力します。

     > [!NOTE]
     > 手順 12 ～ 14 の以下のフィールドには既に値が入っている可能性があります。 これが発生した場合、この一連の手順を省略し、そこから続行します。 選択可能なプロファイル タイトル (この場合は既定値) があることが重要です。

14.   **Web アプリケーション名** フィールドに、**RetailCDXRealTimeService** と入力します。
15.  **プロトコル** フィールドで、**https** を選択します。
16.  **通称**フィールドに、**AXServiceUser@contoso.com** と入力します。
17.  アクション ウィンドウで、 **保存** を選択します。
18.  バックオフィスで、**Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマースの共有パラメーター**の順に移動します。
19.  **セキュリティ** タブを選択します。
20.  **取引サービスの従来のプロパティ** の下位ヘッダーにて、 **Real-time サービス プロファイル** フィールドを選択し、新たに作成した **既定** 値を選択します。
21.  **ID プロバイダー** タブを選択します。
22.  **ID プロバイダー**クイック タブで、**追加**を選択します。
23.  新しい **発行者** 行で、新しい ID プロバイダー値 **https://sts.windows.net/** をフィールドに入力します。
24.  アクション ウィンドウで、 **保存** を選択します。
25.  **Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース パラメーター**の順に移動します。
26.  **全般**タブで、**初期化**リンクを選択し、コマース機能のシード データを構成します。

     > [!NOTE]
     > 初めてダウンロードが試みられるとき、インストーラーは関連するページからダウンロードされません。  これは、インストーラーはダウンロードの場所に配置されているだけであり、関連付けられているデータベースの値がまだ存在しないためです。  バックオフィスで、**ダウンロード**機能が試行されると (たとえば、Commerce Scale Unit または Modern POS)、エラーが表示され、2 回目にダウンロードが試みられたときにインストーラーをダウンロードできるようにする自動アップロード機能が開始されます。 (インストーラーのダウンロードがもう一度試みられるまで 1 分待ってください)。
     >
     > 周辺機器シミュレータ (本社の ハードウェアプロファイル ページにてダウンロードできます) は、最低でも1つのハードウェア プロファイルが作成され、動作可能となるまで使用することができません。 それらが完了していれば、以下のスクリプトを実行することができます。
     >
     > ```powershell
     > .\RetailUpdateDatabase.ps1 -envName 'LBDenv1' -UpdateRetailHardwareProfileSelfServicePackage
     > ```

28. Commerce Scale Unit をインストールするためのインストール手順に従います。 手順については、[Commerce Scale Unit (自己ホスト) のコンフィギュレーションとインストール](../../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md) を参照してください。  このドキュメントの複数の場所に、オンプレミス配置の指示に対する変更を参照するメモがあります。 これらの変更を記録することが重要です。 
