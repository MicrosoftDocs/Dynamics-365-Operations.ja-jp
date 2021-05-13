---
title: 開発環境の配置とアクセス
description: このトピックでは、開発インスタンスへのアクセス、ローカル開発 VM の構成、および開発者と管理者のための構成設定を見つける方法について説明します。
author: laneswenka
ms.date: 09/22/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10031
ms.assetid: 4be8b7a1-9632-4368-af41-6811cd100a37
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03c958302e654ef908381d38e4fec7992e57622c
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923239"
---
# <a name="deploy-and-access-development-environments"></a>開発環境の配置とアクセス

[!include [banner](../includes/banner.md)]

このトピックでは、開発インスタンスへのアクセス、ローカル開発仮想マシン (VM) の構成、および開発者と管理者にとって重要な構成設定を見つける方法について説明します。

## <a name="definitions"></a>定義

| 期間      | 定義                             |
|-----------|----------------------------------------|
| エンド ユーザー  | Web クライアントを使用してインスタンスにアクセスするユーザー。 エンド ユーザーは、インスタンスにアクセスするには Microsoft Azure Active Directory (Azure AD) の資格情報が必要で、そのインスタンスのユーザーとしてプロビジョニングまたは追加する必要があります。 |
| 開発者 | Microsoft Visual Studio 環境でコードを開発するユーザー。 開発者は、開発環境 (VM) へのリモート デスクトップ アクセスが必要です。 開発者アカウントは、VM の管理者である必要があります。      |


## <a name="deploying-cloud-development-environments"></a>クラウド開発環境の配置

LCS プロジェクトにクラウドの開発環境を配置する:

1. LCS プロジェクトと Azure サブスクリプションの間に接続を作成します。 Azure サブスクリプション ID が必要であり、サブスクリプションの使用を承認します。
2. 配置する **環境** の下で **+** を選択します。

    ![LCS Onboard の方法](media/access-instances-5.jpeg)
    
3. アプリケーションとプラットフォーム バージョンを選択します。
4. 環境のトポロジを選択します。 詳細については、[プレビュー サブスクリプションのサインアップ](sign-up-preview-subscription.md) を参照してください。
    
5. クラウドでホストされている環境を選択した場合は、使用する Azure コネクタを選択します。 **配置** を選択します。

    ![環境の配置](media/access-instances-3.jpeg)
    
![クラウド ホスト インスタンス](media/CloudHostedPicture.jpg)

## <a name="cloud-environment-that-is-provisioned-through-lcs"></a>LCS を通じてプロビジョニングされるクラウド環境

クラウド環境が LCS を通じてプロビジョニングされると、次の操作が行われます。
+ クラウド環境を要求するユーザーは、その環境内の管理者としてプロビジョニングされます。
+ ユーザー アカウントは開発用 VM にプロビジョニングされ、リモート デスクトップを使用して環境へのアクセスを許可します。これらの資格情報は LCS の環境ページからアクセスできます。

### <a name="accessing-an-instance-through-a-url"></a>URL を試用したインスタンスへのアクセス

エンド ユーザーはシステムにアクセスできます。 管理者は、インスタンスの **ユーザー** ページを使用して、このシステムにユーザーを追加することができます。 これらの追加のユーザーは LCS 内のユーザーである必要はないことに注意してください。 LCS プロジェクト サイトからは、クラウド環境のベース URL を取得します。

1. LCS プロジェクト ページに移動します。
2. **環境** セクションで、配置された環境をクリックします。
3. 環境ページが開くと、右上隅で、**ログイン** &gt; **Finance and Operations にログオン** をクリックして、アプリケーションにアクセスできます。
4. 有効なエンド ユーザー資格情報を使用して、アプリケーションにサインインします。 現在の LCS ユーザーが最初に環境を展開したユーザーである場合は、そのユーザーは有効な終了ユーザーおよびアプリケーションの管理者である可能性があります。
5. ブラウザーで、サインインした後にベース URL を記録します。 たとえば、ベース URL は、`https://dynamicsAx7aosContoso.cloud.dynamics.com` である可能性があります。

### <a name="accessing-the-cloud-instance-through-remote-desktop"></a>リモート デスクトップを使用したクラウド インスタンスへのアクセス

クラウド環境は、エンド ユーザーおよび開発者の両方としてアクセスできます。 開発者は、リモート デスクトップの資格情報を使用してシステムにアクセスできます。 リモート デスクトップの資格情報は、LCS プロジェクト サイトの環境ページから取得されます (このトピックの前の図を参照してください)。

![制限された管理者アクセス](media/restricted-admin.png)

配置された **プラットフォーム更新プログラム 12 以前** の環境の対象:
1.  VM 名をクリックします。
2.  表示されているローカル管理者のユーザー名とパスワードを使用して、リモート デスクトップ経由でクラウド VM に接続します。 パスワードの表示アイコンを選択してパスワードを表示することができます。

配置された **プラットフォーム更新プログラム 12 以降** の任意の環境については、特徴的アカウント、開発者アカウントおよび管理者アカウントがあります。 

リモート デスクトップを通じて環境にサインインした後、ブラウザーからローカル アプリケーションにアクセスできるようにする場合、リモート コンピューターからアプリケーションにアクセスするために使用するのと同じベース URL を使用します。 上記のセクションは、このベース URL を LCS から取得する方法について説明します。

## <a name="vm-that-is-running-locally"></a>ローカルで実行されている VM
仮想ハード ディスク (VHD) は LCS からダウンロードができるようになり、ローカル コンピューター上に設定可能です。 このシステムは、開発者によるアクセスを目的としており、Finance and Operations アプリの事前構成済みワンボックス開発環境です。 VHD は、資産タイプの **ダウンロード可能な VHD** の下で、LCS の共有アセットライブラリで使用可能です。

1. LCS のメイン ページに移動して **共有アセット ライブラリ** を選択するか、または [共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動します。 
2. 資産タイプの **ダウンロード可能な VHD** を選択します。
3. 目的の Finance and Operation バージョンに基づいて、探している VHD を検索します。 VHD は、ダウンロードする必要がある複数のファイル パーツに分割されています。 たとえば、 "VHD - 10.0.5" で始まる資産ファイルは、バージョン 10.0.5 をインストールするために必要な別のファイルです。
4. 目的の VHD に関連付けられているすべてのファイル (パーツ) をローカル フォルダーにダウンロードします。
5. ダウンロードが完了したら、ダウンロードした実行可能ファイルを実行して、ソフトウェア使用許諾契約に同意し、VHD を抽出するファイル パスを選択します。
6. これにより、ローカルの仮想マシンを実行するのに使用できるローカル VHD ファイルが作成されます。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。

ダウンロード可能な VHD を POS のカスタマイズに使用するには、次の手順も実行する必要があります。

-   ホスト コンピューターで、入れ子になった VM サポートを有効にします。 詳細については、[入れ子仮想化の仮想マシンで Hyper-v を実行](/virtualization/hyper-v-on-windows/user-guide/nested-virtualization) を参照してください。

### <a name="running-the-virtual-machine-locally"></a>仮想マシンをローカルで実行

Hyper-V マネージャーから VM を実行するには、これらの手順に従います。

1. VM を起動するには、**開始** を選択します。
2. ウィンドウで VM を開くには、**接続** を選択します。
3. ツール バーで **Ctrl + Alt + Delete** ボタンを選択してください。 VM は、ほとんどのキーボード コマンドを受け取りますが、その中に Ctrl + Alt + Del は含まれていません。 したがって、ボタンまたはメニュー コマンドを使用する必要があります。
4. 次の資格情報を使用して VM にログインします。
   - ユーザー名: **管理者**
   - パスワード: <strong>pass@word1</strong>

    > [!TIP]
    > 画面解像度を変更することにより、VM ウィンドウのサイズを変更することができます。 VM でデスクトップを右クリックし、**画面の解像度** をクリックします。 ディスプレイに適した解像度を選択します。
   
5. 管理者ユーザーを準備します。 詳細については、次のセクションを参照してください。
6. バッチ マネージャー サービスを起動します。 このステップは、バッチ ジョブまたはワークフローを実行している場合に必要です。
   1.  管理者として **コマンド プロンプト** ウィンドウを開きます。
   2.  **net start DynamicsAxBatch** と入力し、Enter キーを押します。

   また、サービスを **サービス** ウィンドウから開始することができます。

7. 必要に応じて [更新プログラムを適用](../migration-upgrade/upgrade-latest-platform-update.md#apply-a-platform-update-to-environments-that-are-not-connected-to-lcs) します。

#### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

POS カスタマイズで、ゲスト VM でもこれらの手順に従う必要があります。

1.  [Microsoft Emulator for Windows 10 Mobile Anniversary Update](https://www.microsoft.com/download/details.aspx?id=53424) をダウンロードしてインストールします。
2.  Hyper-V ホスト サービスを起動します。 詳細については、[Hyper-V: Hyper-V 仮想マシン管理サービスを実行している必要があります](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee956894(v=ws.10)) を参照してください。 起動中にエラーが発生した場合は、ゲスト VM で Hyper-V ロールをアンインストールし、再インストールすることもできます。

### <a name="provisioning-the-administrator-user"></a>管理者ユーザーを準備

開発者がアクセスするには、インスタンスで管理者である必要があります。 管理者としての資格情報をプロビジョニングするには、デスクトップにある管理者プロビジョニング ツールを実行し、ツールにメール アドレス (Azure AD 資格情報) を入力します。

1.  デスクトップから、管理者として管理者ユーザーのプロビジョニング ツールを実行します (アイコンを右クリックし、**管理者として実行** をクリックします)。
2.  電子メール アドレスを入力し、**送信** を選択します。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。

#### <a name="for-dynamics-365-for-operations-version-1611"></a>Dynamics 365 for Operations の場合、バージョン 1611

1.  RetailTenantUpdateTool を実行します。
    -   このツールのアイコンは、デスクトップ上で使用できます。
    -   このツールは、次の場所から使用することもできます: C:\windows\System32\WindowsPowerShell\v1.0\PowerShell.exe -File C:\RetailSDK\Tools\RetailTenantUpdateTool.ps1

2.  このツールを開始するには、アイコンをダブルクリックします。 自身の Azure AD 資格情報を求められます。 管理者ユーザーのプロビジョニング ツールで以前使用したものと同じ資格情報を使用する必要があります。

#### <a name="for-dynamics-365-for-operations-70"></a>Dynamics 365 for Operations 7.0 の場合

1.  [IT プロフェッショナル用 Microsoft Online Services サインイン アシスタント RTW](https://go.microsoft.com/fwlink/?LinkID=286152) をインストールします。
2.  [Windows PowerShell (64-ビット バージョン) 用 Azure Active Directory モジュール](/collaborate/connect-redirect?DownloadID=59185) をインストールします。
3.  テナントとユーザー ID の Azure AD を照会します。 Windows PowerShell 統合スクリプト環境 (ISE) ウィンドウを管理者権限で開き、次のコマンドを実行します。 Azure AD 資格情報を求められます。 以前に管理者プロビジョニング ツールで使用したのと同じユーザー アカウントを使用します。

    ```powershell
    $msocred = Get-Credential 
    Connect-MsolService -Credential $msocred 
    $company = Get-MsolCompanyInformation 
    Write-Host "TenantID: $($company.ObjectId)" 
    $msocred.UserName 
    $users = Get-MsolUser -SearchString "$($msocred.username)" 
    foreach($u in $users) 
    { 
        if($u.SignInName -eq $msocred.UserName) 
        { 
            Write-Host "SignInName:$($u.SignInName) UserId: $($u.ObjectId)" 
        } 
    }
    ```
        
    [![Windows PowerShell ISE ウィンドウのコマンド](./media/retailconfig02-1024x529.png)](./media/retailconfig02.png)

4.  次の SQL スクリプトを更新し、その環境の AXDB で実行します。 上記の Windows PowerShell スクリプト出力から次のパラメーターの値を指定します。

    -   **TenantID** – たとえば、c83429a6-782b-4275-85cf-60ebe81250ee
    -   **UserId** – たとえば、a036b5d8-bc8c-4abe-8eec-17516ea913ec

    <!-- -->
    ```sql
    DECLARE @TenantId NVARCHAR(1024)         DECLARE @UserId NVARCHAR(1024) 
    SET @TenantId = ‘‘ 
    SET @UserId = ‘‘ 
    IF(LEN(@TenantId) > 0 AND LEN(@UserId) > 0) 
        BEGIN 
        UPDATE AxDBRAIN.dbo.SYSSERVICECONFIGURATIONSETTING SET [VALUE] = @TenantId WHERE [NAME] = ‘TENANTID’ 
        UPDATE RetailHoustonStore.ax.SYSSERVICECONFIGURATIONSETTING SET [VALUE] = @TenantId WHERE [NAME] = ‘TENANTID’ 
        UPDATE AxDBRAIN.dbo.RETAILSTAFFTABLE SET EXTERNALIDENTITYID = @TenantId, EXTERNALIDENTITYSUBID = @UserId WHERE STAFFID = ‘000160’
        END 
    ELSE 
        BEGIN 
        RAISERROR (15600, -1, -1, ‘TenantId and UserId must be set before running this script’) 
        END
    ```

5.  管理者特権の **コマンド プロンプト** ウィンドウで **IISRESET** を実行することにより、インターネット インフォメーション サービス (IIS) をリセットします。
6.  新しい管理者ユーザーを使用するようにリアルタイム サービス プロファイルを更新します。
    1.  **小売とコマース** &gt; **本社の設定** &gt; **コマース スケジューラ** &gt; **リアルタイム サービス プロファイル** の順に移動します。
    3.  以前に使用したユーザーを使用するように JBB レコードを編集します (たとえば、`administrator@contosoax7.onmicrosoft.com`)。
    4.  既定のチャネル データベースの CDX ジョブ 1070 (スタッフ) を実行します。
    5.  クライアント上の **ダウンロード セッション** ページを表示して、ジョブが成功したことを確認します。

### <a name="base-url-of-the-local-application"></a>ローカル アプリケーションの基本 URL

ユーザーが管理者としてプロビジョニングされた後、ユーザーは次のベース URL に移動してコンピュータ上のインスタンスにアクセスできます: `https://usnconeboxax1aos.cloud.onebox.dynamics.com`。 バージョン管理を使用しており、複数の開発 VMs を同じ Azure DevOps プロジェクトに接続する予定がある場合は、ローカル VM 名を変更してください。 手順については、[ローカル開発 (VHD) 環境の名前変更](../migration-upgrade/vso-machine-renaming.md) を参照してください。

#### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com/`です。　 

クラウド POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com` です。　 構成手順を完了すると、この VM には Azure AD テナントがプロビジョニングされます。 Azure AD 管理者アカウントは、デモ データ内のレジ担当者アカウントにマップされます。 この環境の POS デバイスを簡単にアクティブにするには、このレジ担当者アカウントを使用できます。

-   出納係ユーザー ID: **000160**
-   出納係パスワード: **123**
-   出納係 LE: **USRT**
-   出納係ストア: **ヒューストン**

## <a name="location-of-packages-source-code-and-other-aos-configurations"></a>パッケージ、ソース コード、およびその他の AOS コンフィギュレーションの場所
VM で、AOSWebApplication の web.config file を開くことによって、ほとんどのアプリケーション コンフィギュレーションが表示されます。

1.  IIS を起動します。
2.  **サイト** &gt; **AOSWebApplication** に移動します。
3.  右クリックしてから、**エクスプローラー** をクリックしてエクスプローラーを開きます。
4.  メモ帳や他のテキスト エディターで web.config ファイルを開きます。 多くの開発者や管理者にとって、次のキーが重要です。
    -   **Aos.MetadataDirectory** - このキーは、プラットフォームとアプリケーションのバイナリを含むパッケージ フォルダの場所、およびソースコードをポイントします。 (ソース コードは、開発環境でのみ使用できます。) 一般的な値は、c:\packages、c:\AosServicePackagesLocalDirectory、および J:AosServicePackagesLocalDirectory です。
    -   **DataAccess.Database** - このキーは、データベースの名前を保持します。
    -   **Aos.AppRoot** - このキーは、Application Object Server (AOS) Web アプリケーションのルート フォルダーをポイントします。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

ソフトウェア開発キット (SDK) は、C:\RetailSDK にあります。 アプリケーションの使用およびカスタマイズ方法の詳細については、次のトピックを参照してください。
-   [Retail ソフトウェア開発キット (SDK) アーキテクチャ](../../../commerce/dev-itpro/retail-sdk/retail-sdk-overview.md)
-   [販売時点管理 (POS) デバイスのライセンス認証](../../../commerce/dev-itpro/retail-device-activation.md)

## <a name="redeploying-or-restarting-the-runtime-on-the-vm"></a>VM でのランタイムの再配置または再起動
ローカルのランタイムを再起動して、すべてのパッケージを再配置するには、次の手順を実行します。

1.  ファイル エクスプローラーを開き、C:\CustomerServiceUnit に移動します。
2.  **AOSDeploy.cmd** を右クリックして **管理者として実行** をクリックします。

このプロセス時間がかかる場合があります。 cmd.exe ウィンドウが終了すると、プロセスが完了します。 ランタイムを再配置せずに AOS を再起動するのみの場合は、管理者の **Command Prompt** ウィンドウから **iisreset** を実行するか、IIS から AOSWebApplication を再起動します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]