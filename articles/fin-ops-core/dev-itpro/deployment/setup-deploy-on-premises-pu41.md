---
title: オンプレミス環境の設定と配置 (Platform update 41 以降)
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 41 以降を計画、設定、展開する方法について説明します。
author: faix
ms.date: 06/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: Platform update 41
ms.openlocfilehash: d9cffa6213208a0efde90546e6dddfd71142bd9e
ms.sourcegitcommit: d49b27df81bd30537b504a8679462b71210f4462
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2021
ms.locfileid: "6277399"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-update-41-and-later"></a>オンプレミス環境の設定と配置 (Platform update 41 以降)

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 41 以降を計画、設定、展開する方法について説明します。 プラットフォーム更新プログラム 41 はバージョン 10.0.17 で利用可能です。

[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) が利用可能です。 そこでは、オンプレミス展開に関する質問またはフィードバックをすべて投稿できます。

## <a name="finance--operations-components"></a>Finance + Operations のコンポーネント

Finance + Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。

- Application Object Server (AOS)
- ビジネス インテリジェンス (BI)
- 財務レポート/管理レポーター

これらのコンポーネントは、次のシステム ソフトウェアによって異なります。

- Microsoft Windows Server 2019 または Microsoft Windows Server 2016 (英語オペレーティング システムのインストールのみがサポートされます。)
- Microsoft SQL Server 2016 SP2

    > [!IMPORTANT]
    > フルテキスト検索を有効にする必要があります。

- SQL Server Reporting Services (SSRS)

    SSRS は BI 仮想マシン (VM) に展開されます。 SSRS ノードには、ローカルで実行されているデータベース エンジン インスタンスも必要です。

- SQL Server Integration Services (SSIS)

    SSIS は AOS VM に展開されます。

- SQL Server Management Studio
- スタンドアロン Microsoft Azure Service Fabric 7.2 以降
- Microsoft Windows PowerShell 5.0 以降
- Windows Server 2019 または Windows Server 2016 での Active Directory フェデレーション サービス (AD FS)
- ドメイン コントローラー

    > [!IMPORTANT]
    > ドメイン コントローラーは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。 ドメイン機能レベルの詳細については、次のトピックを参照してください。
    >
    > - [Active Directory 機能レベルとは?](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))
    > - [Active Directory Domain Services (AD DS) 機能のレベルを理解する](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))
    > - [双方向の完全な信頼](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)

- 次はオプションですが、**強く** お勧めします: Windows Server 2019 または Windows Server 2016 の Active Directory 証明書サービス (AD CS)

## <a name="lcs"></a>LCS

Finance + Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。 配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。 LCS からのみ配置を開始することができます。 LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。

## <a name="authentication"></a>認証

オンプレミス アプリケーションは AD FS で動作します。 LCS と対話するには、Azure Active Directory (Azure AD) も設定する必要があります。 展開を完了し、LCS ローカル エージェントを構成するには、Azure AD が必要です。 Azure AD テナントがまだない場合は、Azure AD が提供するオプションのいずれかを使用して無料のものを取得できます。 詳細については、[クイックスタート: テナントの設定](/azure/active-directory/develop/active-directory-howto-tenant)を参照してください。

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance + Operations は スタンドアロン Service Fabric を使用します。 詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。

Finance + Operations の設定では、Service Fabric 内に一連のアプリケーションを展開します。 展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成されることにより定義されます。

- **AOSNodeType** – このタイプのノードは、AOS (ビジネス ロジック) をホストします。
- **OrchestratorType** – このノード タイプのノードは Service Fabric のプライマリ ノードとして機能し、展開およびサービスロジックをホストします。
- **ReportServerType** – このタイプのノードは、SSRS およびレポート ロジックをホストします。
- **MRType** – このタイプのノードは Management Reporter ロジックをホストします。

## <a name="infrastructure"></a>インフラストラクチャ

Finance + Operations には、非 Microsoft 仮想化プラットフォーム (特に VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。 詳細については、[Microsoft 以外のハードウェア仮想化ソフトウェアで実行される Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。 要するに、Microsoft はこの環境で製品をサポートしています。 ただし、Microsoft が問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまず顧客に依頼する場合があります。

VMware を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。

- [仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)](https://kb.vmware.com/s/article/2129176)
- [vmxnet3 仮想アダプターのいくつかの問題](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

 > [!WARNING]
 > Dynamics 365 Finance + Operations (オンプレミス) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。 ただし、[Microsoft Azure スタック ハブ](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。

ハードウェア構成には、次のコンポーネントが含まれます。

- Windows Server 2019 または Windows Server 2016 VM に基づく スタンドアロン Service Fabric Cluster
- SQL Server (Clustered SQL と Always-On の両方がサポートされます。)
- 認証のための AD FS
- ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有
- オプション: Microsoft Office Server 2017

詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) を参照してください。

### <a name="hardware-layout"></a>ハードウェア レイアウト

[オンプレミス環境のハードウェア サイジング要件](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric Cluster を計画します。 Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

次のテーブルは、ハードウェア レイアウトの例を示しています。 この例は、設定を示すためにこのトピック全体で使用されています。 設定が完了すると、次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。

> [!NOTE]
> Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。 この例では **OrchestratorType** を主要なノード タイプとして指定します。 3 つ以上の VM を持つノード タイプがある場合、クラスターの信頼性を高めるために、そのノードタイプをプライマリ (シード) ノード タイプにすることを検討します。 

| マシンの目的          | Service Fabric ノード タイプ | コンピューター名    | IP アドレス    |
|--------------------------|--------------------------|-----------------|---------------|
| ドメイン コントローラー        |                          | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                    |                          | DAX7SQLAOADFS1  | 10.179.108.3  |
| ファイル サーバー              |                          | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On クラスター    |                          | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                          |                          | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                          |                          | DAX7SQLAOSQLA   | 10.179.108.9  |
| クライアント                   |                          | SQLAOCLIENT1    | 10.179.108.11 |
| AOS 1                    | AOSNodeType              | SQLAOSF1AOS1    | 10.179.108.12 |
| AOS 2                    | AOSNodeType              | SQLAOSF1AOS2    | 10.179.108.13 |
| AOS 3                    | AOSNodeType              | SQLAOSF1AOS3    | 10.179.108.14 |
| オーケストレータ 1           | OrchestratorType         | SQLAOSF1ORCH1   | 10.179.108.21 |
| オーケストレータ 2           | OrchestratorType         | SQLAOSF1ORCH2   | 10.179.108.22 |
| オーケストレータ 3           | OrchestratorType         | SQLAOSF1ORCH3   | 10.179.108.23 |
| Management Reporter ノード | MRType                   | SQLAOSMR1       | 10.179.108.31 |
| SSRS ノード 1              | ReportServerType         | SQLAOSFBI1      | 10.179.108.41 |

次の表に、バッチ実行と対話型セッションが専用ノードで実行されるハードウェア レイアウトの例を示します。 詳細については、[オンプレミス配置でのバッチのみおよび対話型のみの AOS ノードのコンフィギュレーション](./onprem-batchonly.md)を参照してください。

| マシンの目的          | Service Fabric ノード タイプ   | コンピューター名    | IP アドレス    |
|--------------------------|----------------------------|-----------------|---------------|
| ドメイン コントローラー        |                            | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                    |                            | DAX7SQLAOADFS1  | 10.179.108.3  |
| ファイル サーバー              |                            | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On クラスター    |                            | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                          |                            | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                          |                            | DAX7SQLAOSQLA   | 10.179.108.9  |
| クライアント                   |                            | SQLAOCLIENT1    | 10.179.108.11 |
| AOS 1                    | BatchOnlyAOSNodeType       | SQLAOSF1AOS1    | 10.179.108.12 |
| AOS 2                    | BatchOnlyAOSNodeType       | SQLAOSF1AOS2    | 10.179.108.13 |
| AOS 3                    | BatchOnlyAOSNodeType       | SQLAOSF1AOS3    | 10.179.108.14 |
| AOS 4                    | InteractiveOnlyAOSNodeType | SQLAOSF1AOS4    | 10.179.108.15 |
| AOS 5                    | InteractiveOnlyAOSNodeType | SQLAOSF1AOS5    | 10.179.108.16 |
| AOS 6                    | InteractiveOnlyAOSNodeType | SQLAOSF1AOS6    | 10.179.108.17 |
| オーケストレータ 1           | OrchestratorType           | SQLAOSF1ORCH1   | 10.179.108.21 |
| オーケストレータ 2           | OrchestratorType           | SQLAOSF1ORCH2   | 10.179.108.22 |
| オーケストレータ 3           | OrchestratorType           | SQLAOSF1ORCH3   | 10.179.108.23 |
| Management Reporter ノード | MRType                     | SQLAOSMR1       | 10.179.108.31 |
| SSRS ノード 1              | ReportServerType           | SQLAOSFBI1      | 10.179.108.41 |

## <a name="overview-of-the-setup-process"></a>設定プロセスの概要

Finance + Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。 開始する前にすべての手順を読むと、セットアップを計画しやすくなります。

1. [ドメイン名と DNS ゾーンの計画](#plandomain)
1. [証明書の計画と取得](#plancert)
1. [ユーザーとサービス アカウントの計画](#plansvcacct)
1. [DNS ゾーンの作成と A レコードの追加](#createdns)
1. [VM のドメインへの参加](#joindomain)
1. [LCS からセットアップ スクリプトのダウンロード](#downloadscripts)
1. [コンフィギュレーションの記述](#describeconfig)
1. [証明書の構成](#configurecert)
1. [VMs を設定する](#setupvms)
1. [スタンドアロン Service Fabric クラスターの設定](#setupsfcluster)
1. [テナント用 LCS 接続の構成](#configurelcs)
1. [ファイル ストレージの設定](#setupfile)
1. [SQL Server の設定](#setupsql)
1. [データベースを構成する](#configuredb)
1. [資格情報の暗号化](#encryptcred)
1. [SSIS を設定する](#setupssis)
1. [SSRS を設定する](#setupssrs)
1. [AD FS のコンフィギュレーション](#configureadfs)
1. [コネクタを構成し、オンプレミスのローカル エージェントをインストールする](#configureconnector)
1. [リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)
1. [LCS から Finance + Operations 環境を配置する](#deploy)
1. [Finance + Operations 環境への接続](#connect)

## <a name="setup"></a>段取り

### <a name="prerequisites"></a>必要条件

セットアップを開始する前に、次の前提条件が満たされている必要があります。 これらの前提条件の設定は、このドキュメントの範囲外です。

- Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。
- AD FS は、展開する必要があります。
- SQL Server 2016 SP2 は SSRS コンピューターにインストールされている必要があります。
- SQL Server Reporting Services 2016 は、SSRS コンピューターに **ネイティブ** モードでインストールされる (コンフィギュレーションはされない) 必要があります。
- オプション: AD CS がネットワークにインストールおよびコンフィギュレーションされます。

次の表は、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされる必須ソフトウェアを示します。

| ノード タイプ | コンポーネント | 細目 |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC ドライバー 13 | [ODBC ドライバー 13.1](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) |
| AOS       | SNAC – ODBC ドライバー 17.5.x | [ODBC ドライバー 17.5.2](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows?view=sql-server-ver15#1752&preserve-view=true) |
| AOS       | Microsoft .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| AOS       | Microsoft .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| AOS       | Microsoft .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| AOS       | Microsoft Internet Information Services (IIS) | **Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console |
| AOS       | SQL Server Management Studio 17.9.1 | [SSMS 17.9.1](/sql/ssms/release-notes-ssms?view=sql-server-ver15#1791&preserve-view=true) |
| AOS       | Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| AOS       | Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。 |
| AOS       | Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> |
| BI        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| BI        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| BI        | .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| BI        | SQL Server Management Studio 17.9.1 | [SSMS 17.9.1](/sql/ssms/release-notes-ssms?view=sql-server-ver15#1791&preserve-view=true) |
| MR        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| MR        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| MR        | .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| MR        | Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| ORCH      | Microsoft .NET Framework version 4.0–4.8 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net48-offline> |

### <a name="step-1-plan-your-domain-name-and-dns-zones"></a><a name="plandomain"></a>手順 1、 ドメイン名と DNS ゾーンの計画

AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。 このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。

たとえば、会社のドメインが contoso.com の場合、Finance + Operations は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。

- AOS の機械の場合 ax.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com

### <a name="step-2-plan-and-acquire-your-certificates"></a><a name="plancert"></a>手順 2、 証明書の計画と取得

Service Fabric Cluster と展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。 プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。 ドメインが [AD CS](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)) で設定されている場合は、Microsoft セットアップ スクリプトを使用してテンプレートと証明書を作成できます。 証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。

自己署名証明書は、テスト目的でのみ使用できます。 便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。 自己署名スクリプトを使用している場合は、このトピックの後の手順で作成スクリプトを実行するように指示されます。 前述の通り、これらの証明書はテスト目的でのみ使用できます。

> [!IMPORTANT]
> Microsoft は、AD CS による自動証明書の作成をサポートして、セットアップ スクリプトによる自己署名証明書の生成のサポートを終了する予定です。

証明書の推奨設定を次に示します。

- **署名アルゴリズム:** sha256RSA
- **署名ハッシュ アルゴリズム:** sha256
- **公開キー:** RSA (2048 ビット)
- **Thumbprint アルゴリズム:** sha1

| 目的                                      | 説明 | 追加条件 |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL 証明書                   | この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。 | <p>証明書の場合、ドメイン名は SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。 たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書のドメイン ネーム システム (DNS) 名は、DAX7SQLAOSQLA.contoso.com です。</p><ul><li>**共通名 (CN):** DAX7SQLAOSQLA.contoso.com</li><li>**DNS 名:** DAX7SQLAOSQLA.contoso.com</li></ul> |
| Service Fabric Server 証明書            | この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。 これはクラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。 | <p>この証明書については、\*.contoso.com などのドメイン用ワイルドカード SSL 証明書を使用することもできます。 (詳細については、このテーブルに続くテキストを参照してください。) それ以外の場合は、次の値を使用します。</p><ul><li>**CN:** sf.d365ffo.onprem.contoso.com</li><li>**DNS 名:** sf.d365ffo.onprem.contoso.com</li></ul> |
| Service Fabric Client 証明書            | クライアントはこの証明書を使用して Service Fabric cluster を表示および管理します。 | <ul><li>**CN:** client.d365ffo.onprem.contoso.com</li><li>**DNS 名:** client.d365ffo.onprem.contoso.com</li></ul> |
| 暗号化証明書                     | この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。 | <p>証明書は、**Microsoft Enhanced Cryptographic Provider v1.0** プロバイダーを使用して作成する必要があります。</p><p>証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</p><p>詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</p><ul><li>**CN:** axdataenciphermentcert</li><li>**DNS 名:** axdataenciphermentcert</li></ul> |
| AOS SSL 証明書                          | <p>この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書として使用されます。 また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</p> | <p>Service Fabric サーバー証明書として使用したのと同じワイルドカード SSL 証明書を使用できます。 それ以外の場合は、次の値を使用します:</p><ul><li>**CN:** ax.d365ffo.onprem.contoso.com</li><li>**DNS 名:** ax.d365ffo.onprem.contoso.com</li></ul> |
| セッション認証証明書           | AOS はこの証明書を使用してユーザーのセッション情報を保護します。 | <p>この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</p><ul><li>**CN:** SessionAuthentication</li><li>**DNS 名:** SessionAuthentication </li></ul> |
| データの暗号化証明書                  | AOS はこの証明書を使用して機密情報を暗号化します。 | <p>この証明書は、**Microsoft Enhanced RSA and AES Cryptographic Provider** プロバイダーを使用して作成する必要があります。</p><ul><li>**CN:** DataEncryption</li><li>**DNS 名:** DataEncryption</li></ul> |
| データ署名の証明書                     | AOS はこの証明書を使用して機密情報を暗号化します。 | <p>この証明書はデータ暗号化証明書とは別のもので、**Microsoft Enhanced RSA and AES Cryptographic Provider** プロバイダーを使用して作成する必要があります。</p><ul><li>**CN:** DataSigning</li><li>**DNS 名:** DataSigning</li></ul> |
| Financial Reporting クライアント証明書       | この証明書を使用して、Financial Reporting サービスと AOS 間の通信を保護します。 | <ul><li>**CN:** FinancialReporting</li><li>**DNS 名:** FinancialReporting</li></ul> |
| 報告証明書                        | この証明書を使用して、SSRS と AOS 間の通信を保護します。| <p>**重要:** Financial Reporting クライアント証明書を再利用 **しない** でください。</p><ul><li>**CN:** ReportingService</li><li>**DNS 名:** ReportingService</li></ul> |
| SSRS Web サーバー証明書                  | この証明書は、SSRS Web サーバーに接続するクライアント (AOS) に提示されるサーバー証明書として使用されます。 | <p>証明書のドメイン名は SSRS ノードの SSRN と一致する必要があります。</p><ul><li>**CN:** BI1.contoso.com</li><li>**DNS 名:** BI1.contoso.com</li></ul>
| オンプレミス ローカル エージェント証明書           | <p>この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。 これにより、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して展開を編成および監視することができます。</p><p>**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</p> | <ul><li>**CN:** OnPremLocalAgent</li><li>**DNS 名:** OnPremLocalAgent</li></ul> |

ドメインのワイルドカード SSL 証明書を使用して、Service Fabric サーバー証明書と AOS SSL 証明書を結合できます。

以下は、AOS SSL 証明書と組み合わせた Service Fabric サーバー証明書の例です。

#### <a name="subject-name"></a>件名

```Text
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a>件名の代替名

```Text
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

> [!IMPORTANT]
> ワイルドカード証明書を使用して、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できます。 したがって、\*.onprem.contoso.com の証明書は ax.d365ffo.onprem.contoso.com では無効になります。

### <a name="step-3-plan-your-users-and-service-accounts"></a><a name="plansvcacct"></a>手順 3、 ユーザーとサービス アカウントの計画

Finance + Operations を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。 サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。 次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。

| ユーザー アカウント                                            | 種類 | 目的 | ユーザー名 |
|---------------------------------------------------------|------|---------|-----------|
| 財務レポート アプリケーション サービス アカウント         | gMSA | | Contoso\\svc-FRAS$ |
| 財務レポート プロセス サービス アカウント             | gMSA | | Contoso\\svc-FRPS$ |
| 財務レポート クリック ワンス デザイナー サービス アカウント | gMSA | | Contoso\\svc-FRCO$ |
| AOS サービス アカウント                                     | gMSA | 将来校正するためにこのユーザーを作成する必要があります。 Microsoft は今後のリリースで、AOS を gMSA と連携させる予定です。 このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。\* | Contoso\\svc-AXSF$ |
| SSRS ブートストラッパー サービス アカウント                       | gMSA | レポート サービス ブートストラッパーは、このアカウントを使用して SSRS サービスをコンフィギュレーションします。 | Contoso\\svc-ReportSvc$ |
| AOS サービス アカウント                                     | ドメイン アカウント | AOS は、一般提供 (GA) リリースでこのユーザーを使用します。\* | Contoso\\ AXServiceUser |
| AOS SQL DB 管理者ユーザー                                   | SQL ユーザー | Finance + Operations は、このユーザーを使用して SQL\*\* を認証します。 このユーザーは、今後のリリース \*\*\* で gMSA ユーザーにも置き換えられます。 | AXDBAdmin |
| ローカル配置エージェント サービス アカウント                  | gMSA | ローカル エージェントはこのアカウントを使用して、さまざまなノードでの展開を調整します。 | Contoso\\ Svc-LocalAgent$ |

\* これらのアカウントでは、地域の設定を変更しないでください。 既定の EN-US リージョン設定が必要です。 

\*\* SQL ユーザーのパスワードに特殊文字が含まれている場合、展開中に問題が発生する場合があります。

\*\*\* SQL 認証で使用する SQL ユーザ名とパスワードは暗号化されてファイル共有に保存されているため、安全性が確保されています。

### <a name="step-4-create-dns-zones-and-add-a-records"></a><a name="createdns"></a>手順 4、 DNS ゾーンの作成と A レコードの追加

DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。 次の手順では、AOS ホスト名と Service Fabric Cluster の DNS 前方参照ゾーンと A レコードを作成する手順を示します。 この例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。

- AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com

#### <a name="add-a-dns-zone"></a>DNS ゾーンの追加

1. ドメイン コントローラー コンピューターにサインインして、**スタート** を選択します。 次に、**dnsmgmt.msc** を入力し **dnsmgmt (DNS)** アプリケーションを選択して、DNS マネージャーを開きます。
2. コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。
3. **プライマリ ゾーン** を選択します。
4. **Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ** を選択します。
5. **このドメインのドメイン コントローラーで実行されているすべての DNS サーバーに対して : Contoso.com** を選択し、**次へ** を選択します。
6. **前方参照ゾーン** を選択し、**次へ** を選択します。
7. 設定するゾーン名を入力し、**次へ** をクリックします。 たとえば、**d365ffo.onprem.contoso.com** と入力します。
8. **動的更新を許可しない** を選択し、**次へ** を選択します。
9. **完了** を選択します。

#### <a name="set-up-an-a-record-for-aos"></a>AOS の A レコードを設定する

新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric cluster ノード **ごと** に、ax.d365ffo.onprem.contoso.com という名前の A レコードを 1 つ作成します。 他のノード タイプの A レコードは作成しないでください。

1. DNS マネージャーの **前方参照ゾーン** フォルダーで、新しく作成したゾーンを検索します。
2. 新しいゾーンを選択したまま (または右クリック) にしてから、**新しいホスト** を選択します。
3. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**ax** を名前として、**10.179.108.12** を IP アドレスとして入力します。) 次に **ホストの追加** を選択します。
4. 両方のチェック ボックスをオフのままにします。
5. 追加の AOS ノードごとに手順 1 から 4 を繰り返します。

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Orchestrator の A レコードを設定する

新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric Cluster **ごと** に、sf.d365ffo.onprem.contoso.com という名前の A レコードを 1 つ作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを選択したまま (または右クリック) にしてから、**新しいホスト** を選択します。
2. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**sf** を名前として、**10.179.108.15** を IP アドレスとして入力します。) 次に **ホストの追加** を選択します。
3. 両方のチェック ボックスをオフのままにします。
4. 追加のオーケストレーター ノードごとに手順 1 から 3 を繰り返します。

### <a name="step-5-join-vms-to-the-domain"></a><a name="joindomain"></a>手順 5、 VM のドメインへの参加

各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)の手順を完了します。 または、次の Windows PowerShell スクリプトを使用します。

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> ドメインにそれらを結合させた後、VM を再起動する必要があります。

### <a name="step-6-download-setup-scripts-from-lcs"></a><a name="downloadscripts"></a>手順 6、 LCS からセットアップ スクリプトのダウンロード

Microsoft ではセットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介してきました。 LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。

> [!IMPORTANT]
> スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。
2. ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。
3. **モデル** を資産タイプとして選択してから、グリッドで、**Dynamics 365 for Operations オンプレミス - 展開スクリプト** の行を選択します。
4. **バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。
5. zip ファイルをダウンロードした後、ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。 **プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。
6. zip ファイルをスクリプトの実行に使用するコンピューターにコピーします。
7. **infrastructure** という名前のフォルダーにファイルを解凍します。

> [!IMPORTANT]
> このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加えるよう確認します。

### <a name="step-7-describe-your-configuration"></a><a name="describeconfig"></a>手順 7、 コンフィギュレーションの記述

インフラストラクチャのセットアップ スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。

- infrastructure\\ConfigTemplate.xml
- infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml
- infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml

> [!IMPORTANT]
> セットアップ スクリプトの正常に機能するように、環境のセットアップに基づいて、これらのコンフィギュレーション ファイルを適切なコンピュータ名、IP アドレス、サービス アカウント、およびドメインで更新する必要があります。

infrastructure\\ConfigTemplate.xml コンフィギュレーション ファイルでは、次の詳細について説明します。

- アプリケーションが機能するために必要なサービス アカウント
- 通信を保護するために必要な証明書
- データベース コンフィギュレーション
- Service Fabric Cluster コンフィギュレーション

    > [!IMPORTANT]
    > Service Fabric cluster をコンフィギュレーションする際に、主要なノード タイプ (**OrchestratorType**) の 3 つのフォールト ドメインがあることを確認します。 また、1 台のコンピューターに展開できるノードのタイプは 1 つだけになるようにします。

Service Fabric ノード タイプごとに、infrastructure\\D365FO-OP\\NodeTopologyDefinition.xml コンフィギュレーション ファイルでは、次の詳細について説明します。

- 各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング
- ユーザー アカウント制御 (UAC) が有効であるかどうか
- Windows の機能とシステム ソフトウェアの前提条件
- 厳密な名前の検証を有効にするかどうか
- 開くファイアウォール ポートの一覧
- アカウントがコンピューターに必要とするアクセス許可

データベースごとに、infrastructure\\D365FO-OP\\DatabaseTopologyDefinition.xml コンフィギュレーション ファイルでは、次の詳細について説明します。

- データベース設定
- ユーザーとロールの間のマッピング

#### <a name="create-gmsa-and-domain-user-accounts"></a>gMSA およびドメイン ユーザー アカウントを作成する

1. **インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるコンピューターに移動します。
1. **インフラストラクチャ** フォルダーをドメイン コントローラー マシンにコピーします。
1. 管理者特権モードで Windows PowerShell を開き、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。

    > [!IMPORTANT]
    > これらのコマンドでは、AxServiceUser ドメイン ユーザーを作成しません。 ユーザーが作成する必要があります。

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

1. アカウントまたはコンピューターを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの **ConfigTemplate.xml** ファイルを更新し、このコンピューターにコピーしてから次のコマンドを実行します。

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="step-8-configure-certificates"></a><a name="configurecert"></a>手順 8、 証明書の構成

1. 最初に **インフラストラクチャ** フォルダーを展開したコンピューターに移動します。
2. 証明書を生成します。

    1. 証明書を生成する必要がある場合は、次のコマンドを実行します。 これらのコマンドは AD CS で証明書テンプレートを作成し、テンプレートから証明書を生成して、コンピューターの **CurrentUser\\My** 証明書ストアに格納してから、XML ファイルのサムプリントを更新します。

        ```powershell
        # If you must create self-signed certs, set the generateSelfSignedCert attribute to true.
        #.\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -CreateTemplates
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

        > [!NOTE]
        > これらのコマンドは、ドメイン コントローラー コンピューター、または Windows Server を実行していてリモート サーバー管理ツール (KMT) がインストールされているコンピューターで実行する必要があります。

    1. 証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateADCSCert** タグを **false** に設定します。

3. 以前に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、**ConfigTemplate.xml** ファイルのサムプリントを更新します。 証明書は **CurrentUser\\My** 証明書ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。

    > [!WARNING]
    > 特定するのが難しい先頭の印刷不可能な特殊文字があるため、証明書管理ツール (certlm.msc) を使用してサムプリントをコピーしないでください。 印刷できない特殊文字がある場合、次のエラー メッセージが表示されます: 「X509 証明書が無効です」 サムプリントを取得するには、Windows PowerShell コマンドの結果を参照するか、Windows PowerShell で次のコマンドを実行します。
    >
    > ```powershell
    > dir cert:\CurrentUser\My
    > dir cert:\LocalMachine\My
    > dir cert:\LocalMachine\Root
    > ```

4. 各証明書の **ProtectTo** タグで、Active Directory ユーザーまたはグループのセミコロンで区切られた一覧を指定します。 **ProtectTo** タグで指定されたユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。 エクスポートした証明書を保護するため、スクリプトではパスワードがサポートされていません。
5. 証明書を .pfx ファイルにエクスポートします。 エクスポート プロセスの一環として、次のコマンドは、証明書に正しい暗号化プロバイダが設定されているかどうかをチェックします。 

    ```powershell
    # Exports .pfx files into a directory VMs\<VMName>. All the certs will be written to the infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="step-9-set-up-vms"></a><a name="setupvms"></a>手順 9、 VMs を設定する

1. 次のコマンドを実行して、各 VM で実行する必要があるスクリプトをエクスポートします。

    ```powershell
    # Exports the script files to be executed on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. 次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。

    | コンポーネント | リンクのダウンロード | 必要なファイル名 |
    |-----------|---------------|--------------------|
    | SNAC – ODBC ドライバー 13 | [ODBC ドライバー 13.1](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) | Msodbcsql .msi |
    | SNAC – ODBC ドライバー 17.5.x | [ODBC ドライバー 17.5.2](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows?view=sql-server-ver15#1752&preserve-view=true) | msodbcsql\_17.msi |
    | SQL Server Management Studio 17.9.1 | [SSMS 17.9.1](/sql/ssms/release-notes-ssms?view=sql-server-ver15#1791&preserve-view=true) | SSMS-Setup-\*.exe |
    | Microsoft Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> | vcredist\_x64.exe |
    | Microsoft Visual Studio 2017 用 Visual C++ 再頒布可能パッケージ | <https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。 | vc\_redist.x64\_14\_16\_27024.exe |
    | Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> | AccessDatabaseEngine\_x64.exe |
    | .NET Framework version 4.8 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net48-offline> | ndp48-x86-x64-allos-enu.exe |
    | .NET Framework version 4.7.2 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net472-offline> | ndp472-x86-x64-allos-enu.exe |

> [!IMPORTANT]
> - Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。
> - 前の表の "必要なファイル名" 列に指定されている名前がインストーラ ファイルに設定されていることを確認してください。 予期した名前がないファイルの名前を変更します。 そうしないと、Configure-PreReq.ps1 スクリプトの実行時にエラーが発生します。
> - VC++ 17 再配布可能ファイル をダウンロードする場合、実行可能ファイルが zip ファイル内に含まれます。

次に、各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。

> [!NOTE]
> - 次の手順では、複数の VM での実行が必要です。 ただし、プロセスを簡略化するために、提供されるリモート処理スクリプトを使用できます。 これらのスクリプトを使用すると、**.\\Export-Scripts.ps1** コマンドの実行に使用されるのと同じコンピューターなど、単一のコンピューターから必要なスクリプトを実行できます。 リモート処理スクリプトが利用可能な場合、Windows PowerShell セクションの **\# If Remoting** コメントの後に宣言されます。 リモート処理スクリプトを使用する場合、セクション内の残りのスクリプトを実行する必要がない可能性があります。 この場合は、セクション テキストを参照してください。
> - リモート処理では [WinRM](/windows/win32/winrm/portal) を使用します。 場合によっては、[CredSSP](/windows/win32/secauthn/credential-security-support-provider) を有効にする必要があります。 リモート処理モジュールでは、実行ごとに CredSSP を有効または無効にします。 使用しない場合は、CredSSP を無効にすることをお勧めします。 そうしないと、資格情報の盗難リスクが伴います。 設定が完了したら、このトピック後半の[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。

1. 各 **infrastructure\\VMs\\\<VMName\>** フォルダーの内容を、対応する VM にコピーします。 (リモート処理スクリプトを使用している場合は、コンテンツが自動的に対象の VM にコピーされます。) 続いて、次のコマンドを管理者として実行します。

    ```powershell
    # Install prereq software on the VMs.

    # If remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > - 再起動するように求められるたびにコンピューターを再起動します。 すべての前提条件がインストールされるまでは、各再起動後に **.\\Configure-PreReqs.ps1** コマンドを必ず再実行してください。 リモート処理の場合、すべてのコンピューターがオンラインに戻ったときに AllVM スクリプトを再実行します。
    > - リモート処理スクリプトを使用する場合は、現在のユーザーが MSI が配置されているファイル共有フォルダーにアクセスできることを確認してください。 さらに、ユーザーが **AOSNodeType**、**MRType**、**ReportServerType** タイプのコンピューターにアクセスしていないことを確認してください。 そうしないと、ユーザーがログインしている理由によって、リモート処理スクリプトがコンピューターの再起動に失敗します。

2. 次のコマンドを実行して VM 設定を完了します。

    ```powershell
    # If remoting, execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Complete-PreReqs.ps1
    ```

3. 次のコマンドを実行して VM 設定を検証します。

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> リモート処理を使用していた場合は、設定の完了後にクリーンアップ手順を実行します。 手順については、[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。

### <a name="step-10-set-up-a-standalone-service-fabric-cluster"></a><a name="setupsfcluster"></a>手順 10、 スタンドアロン Service Fabric クラスターの設定

1. [Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を Service Fabric ノードのいずれかにダウンロードします。
2. zip ファイルをダウンロードした後、ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。 **プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。
3. ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。 **インフラストラクチャ** フォルダーが、このフォルダーにアクセスすることを確認します。
3. **インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric **ClusterConfig.json** ファイルを生成します。

    ```powershell
    .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```

4. 環境に基づいて、クラスター コンフィギュレーションへの追加の変更が必要な場合があります。 詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および [Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)を参照してください。
5. 生成された **ClusterConfig.json** ファイルを **\<ServiceFabricStandaloneInstallerPath\>** にコピーします。
6. 管理者特権モードで Windows PowerShell を開き、**\<ServiceFabricStandaloneInstallerPath\>** に移動して、次のコマンドを実行して **ClusterConfig.go** ファイルをテストします。

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. テストが成功した場合は、次のコマンドを実行してクラスターを展開します。

    ```powershell
    # If using offline (internet-disconnected) install
    # .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json -FabricRuntimePackagePath <Path to MicrosoftAzureServiceFabric.cab download>

    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. クラスターが作成された後、任意のクライアント コンピューターで Service Fabric Explorer を開き、インストールを検証します。

    1. まだインストールされていない場合、**CurrentUser\\My** 証明書ストアで Service Fabric クライアント証明書をインストールします。
    2. Internet Explorer で、**ツール** (ギヤ記号) を選択してから、**互換性表示の設定** を選択します。 **互換性表示でイントラネット サイトを表示する** チェック ボックスをオフにします。
    3. `https://sf.d365ffo.onprem.contoso.com:19080` に移動します。**sf.d365ffo.onprem.contoso.com** は、ゾーンで指定されている Service Fabric Cluster のホスト名です。 DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。
    4. クライアントの証明書を選択します。 **Service Fabric Explorer** ページが表示されます。
    5. すべてのノードが緑で表示されることを確認します。

    > [!IMPORTANT]
    > - クライアント コンピューターがサーバー コンピューター (たとえば、Windows Server 2019 を実行しているコンピューター) である場合は、**Service Fabric Explorer** ページにアクセスするときに Internet Explorer のセキュリティ強化の構成をオフにする必要があります。
    > - 任意のウィルス対策ソフトウェアをインストールする場合は、除外を設定してください。 [Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従ってください。

### <a name="step-11-configure-lcs-connectivity-for-the-tenant"></a><a name="configurelcs"></a>手順 11、 テナント用 LCS 接続の構成

オンプレミスのローカル エージェントは、LCS を通じて Finance + Operations の展開とサービスを調整するために使用されます。 LCS から Finance + Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。

CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。 オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。

グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。 既定では、組織の Microsoft 365 にサインアップする担当者がディレクトリのグローバル管理者です。

> [!IMPORTANT]
> - テナントごとに証明書を正確に **1** 回構成する必要があります。 同じ環境のすべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。
> - サーバー コンピューター ( Windows Server 2019 を実行しているコンピューターなど) で以下のスクリプトを実行する場合は、Internet Explorer セキュリティ強化の構成を一時的にオフにする必要があります。 そうしないと、Azure のサインイン ページのコンテンツがブロックされます。

1. 顧客の [Azure ポータル](https://portal.azure.com)にサインインして、グローバル管理者ディレクトリの役割があることを確認します。
2. 次のコマンドを **インフラストラクチャ** フォルダーから実行して、証明書が既に登録されているかどうかを確認します。

    ```powershell
    # If you have issues downloading the Azure PowerShell Az module, run the following:
    # [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

    Install-Module Az
    Import-Module Az
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -Test
    ```

    > [!IMPORTANT]
    > 既に AzureRM をインストールしている場合は、Windows PowerShell 5.1 の既存の AzureRM インストールとの互換性がない可能性があるため、削除してください。 詳細については、[Azure PowerShell を AzureRM から Az に移行する](/powershell/azure/migrate-from-azurerm-to-az)を参照してください。

3. 証明書が登録されていないことをスクリプトが示している場合は、次のコマンドを実行します。

    ```powershell
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint'
    ```

> [!NOTE]
> ログイン アカウントに関連付けられた複数のテナントがある場合、次のコマンドを実行してテナント ID をパラメーターとして渡すことができます。 これにより、コンテキストが正しいテナントに設定されていることを確認できます。
>
> ```powershell
> .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -TenantId 'xxxx-xxxx-xxxx-xxxx'
> ```

### <a name="step-12-set-up-file-storage"></a><a name="setupfile"></a>手順 12、 ファイル ストレージの設定

以下の SMB 3.0 ファイル共有を設定する必要があります。

- AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。
- デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。

    > [!WARNING]
    > 共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。

SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1) を参照してください。

> [!IMPORTANT]
> - セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。 したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。 これにより、SMB 暗号化のすべての機能を利用できます。
> - 環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのコンピューターで有効にする必要があります。 BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。

1. ファイル共有マシンで、次のコマンドを実行します。

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. **\\\\DAX7SQLAOFILE1\\aos-storage** ファイル共有を設定します。

    1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
    2. **タスク** \> **新しい共有** を選択し、共有を作成します。 新しい共有に **aos-storage** と名前を付けます。
    3. **共有のキャッシュを許可** を選択したままにします。
    4. **データ アクセスを暗号化** チェック ボックスをオンにします。
    5. **OrchestratorType** を除いて、Service Fabric cluster 内のすべてのマシンに対して **変更** 許可を与えます。
    6. AOS ドメイン ユーザー (**contoso\\AXServiceUser**) と gMSA ユーザー (**contoso\\svc-AXSF$**) に対して、**変更** 許可を与えます。

    > [!NOTE]
    > コンピュータを追加するには、**オブジェクト タイプ** で **コンピューター** を有効にする場合があります。 サービス アカウントを追加するには、**オブジェクト タイプ** で **サービス アカウント** を有効にする場合があります。

3. **\\\\DAX7SQLAOFILE1\\agent** ファイル共有を設定します。

    1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
    2. **タスク** \> **新しい共有** を選択し、共有を作成します。 新しい共有に **エージェント** と名前を付けます。
    3. ローカル展開エージェント (**contoso\\svc-LocalAgent$**) の gMSA ユーザーに対して **フル コントロール** の許可を与えます。

    ```powershell
    # Specify user names
    $AOSDomainUser = 'Contoso\AXServiceUser';
    $LocalDeploymentAgent = 'contoso\svc-LocalAgent$';

    # Specify the path
    $AosStorageFolderPath = 'D:\aos-storage';
    $AgentFolderPath = 'D:\agent';

    # Create new directory
    $AosStorageFolder = New-Item -type directory -path $AosStorageFolderPath;
    $AgentFolder = New-Item -type directory -path $AgentFolderPath;

    # Create new SMB share
    New-SmbShare –Name aos-storage -Path $AosStorageFolderPath -EncryptData $True
    New-SmbShare –Name agent -Path $AgentFolderPath

    # Set ACL for AOS storage folder
    $Acl = Get-Acl $AosStorageFolder.FullName;
    $Ar = New-Object system.security.accesscontrol.filesystemaccessrule($AOSDomainUser,'Modify','Allow');
    $Acl.SetAccessRule($Ar);
    Set-Acl $AosStorageFolder.FullName $Acl;

    # Set ACL for AgentFolder
    $Acl = Get-Acl $AgentFolder.FullName;
    $Ar = New-Object system.security.accesscontrol.filesystemaccessrule($LocalDeploymentAgent,'FullControl','Allow');
    $Acl.SetAccessRule($Ar);
    Set-Acl $AgentFolder.FullName $Acl;
    ```

### <a name="step-13-set-up-sql-server"></a><a name="setupsql"></a>手順 13、 SQL Server の設定

1. SQL Server のインスタンスが 1 つでも十分なサンドボックス環境に展開する場合を除いて、高可用性を備えた SQL Server 2016 SP2 をインストールします。 (ただし、高可用性シナリオをテストするため、サンドボックス環境に高可用性を備えた SQL Server をインストールすることもできます。)

    > [!IMPORTANT]
    > [SQL Server および Windows 認証モード](/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。

    高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。 データベース エンジン、SSRS、フルテキスト検索、および SQL Server 管理ツールがインストール済みであることを確認します。

    > [!NOTE]
    > Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。

2. ドメイン ユーザーまたは gMSA のいずれかとして SQL サービスを実行します。
3. Finance + Operations 向けに SQL Server を構成するために CA から SSL 証明書を取得します。 テストの目的で、AD CS を通じて生成された証明書を作成して使用することができます。 次の例にあるコンピューター名とドメイン名を置き換える必要があります。

    **Always-On SQL 可用性グループの AD CS 証明書**

    Always-On 用の証明書のテストを設定する場合は、次のリモート処理スクリプトを使用します。 このスクリプトは、次に示す手動スクリプトと同じように機能します。

    ```powershell
    #If you need to create self-signed certs
    #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser

    .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
    ```

    **単一の SQL 可用性グループの AD CS 証明書**

    ```powershell
    #If you need to create self-signed certs
    #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1 -ProtectTo CONTOSO\dynuser

    .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1 -ProtectTo CONTOSO\dynuser
    ```

    **SQL Server を使用した Always-On SQL 可用性グループまたは Windows Server フェールオーバー クラスタリングの手動 AD CS 手順** 

    SQL クラスターの各ノードに対して、次の手順を実行します。 

    1. 次の Windows PowerShell コマンドを、SQL Server Always-On レプリカごとに実行します。

        ```powershell
        #If you need to create self-signed certs
        #.\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser -GenerateCertOnly

        .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser -GenerateCertOnly
        ```

    2. SQL サービスを実行するために使用されるアカウントに証明書のアクセス許可を付与します。

        1. 証明書管理ツール (**certlm.msc**) を開きます。
        2. 作成した証明書を選択したまま (または右クリック) してから、**タスク** \> **秘密キーの管理** をクリックします。
        3. SQL Server サービス アカウントを追加し、**読み取り** アクセスを許可します。

    3. SQL Server 構成マネージャーで **ForceEncryption** と新しい証明書を有効にします。

        1. SQL Server 構成マネージャーを開き、**SQL Server ネットワーク構成** を展開し、**\[サーバー インスタンス\] 用プロトコル** を選択したまま (または右クリック) にしてから、**プロパティ** を選択します。
        2. **プロトコル** ダイアログ ボックスの、**証明書** タブの、**証明書** フィールドで、目的の証明書を選択します。
        3. **フラグ** タブの **ForceEncryption** ボックスで、**はい** を選択します。
        4. **OK** を選択して変更を保存します。

    4. 各 SQL クラスター ノードから証明書 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。 Always-On クラスターには少なくとも 2 つの証明書があります。 ただし、追加レプリカがある場合はそれ以上の証明書が必要になる場合があります。 
    5. SQL サービスを再起動します。

    > [!NOTE] 
    > 詳細は、[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)を参照してください。

> [!IMPORTANT]
> リモート処理を使用していた場合は、設定の完了後にクリーンアップ手順を実行します。 手順については、[手順 20、リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)セクションを参照してください。

### <a name="step-14-configure-the-databases"></a><a name="configuredb"></a>手順 14、 データベースを構成する

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。
2. ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。
3. 資産タイプとして **モデル** を選択します。 次にグリッドで、必要なリリースのデータ タイプを選択し、zip ファイルをダウンロードします。

    | リリース |  データベース |
    |---------|----------|
    | オンプレミス プラットフォーム更新プログラム 41 | Dynamics 365 for Operations オンプレミス、バージョン 10.0.17 デモ データ |
    | オンプレミス プラットフォーム更新プログラム 41 | Dynamics 365 for Operations オンプレミス、バージョン 10.0.17 空のデータ |

4. zip ファイルには、単一のバックアップ (.bak) ファイルが含まれます。 必要に応じて、ダウンロードするファイルを選択します。
5. **infrastructure\\ConfigTempate.xml** ファイルのデータベース セクションが、次の情報と共に正しく構成されているか確認します。

    - データベース名。
    - データベース ファイルとログ設定。 データベース設定は、指定された既定値以上にする必要があります。
    - 以前にダウンロードしたバックアップ ファイルのパス。 Finance + Operations データベースの既定の名前は **AXDB** です。

    > [!IMPORTANT]
    > - SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して **読み取り** アクセス権を持っている必要があります。
    > - 既に既存のデータベースの名前が同じである場合は、上書きされません。

6. **インフラストラクチャ** フォルダーを SQL Server コンピューターにコピーします。 次に、管理者特権モードで Windows PowerShell を開き、フォルダーに移動します。

#### <a name="configure-the-orchestratordata-database"></a>OrchestratorData データベースのコンフィギュレーション

- 次のコマンドを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
    ```

    Initialize-Database.ps1 スクリプトは、以下の処理を行います:

    1. **OrchestratorData** という名前の空のデータベースを作成します。 このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。
    1. データベースでローカル エージェント gMSA (**svc-LocalAgent$**) に **db\_owner** アクセス許可を与えます。

#### <a name="configure-the-finance--operations-database"></a>Finance + Operations データベースの構成

1. 次のコマンドを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
    .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
    ```

    Initialize-Database.ps1 スクリプトは、以下の処理を行います:

    1. 指定されたバックアップ ファイルからデータベースを復元します。
    2. SQL 認証が有効になっている新しいユーザーを作成します (**axdbadmin**)。
    3. **AXDB** データベースの次の表に基づいて、データベース ロールにユーザーをマップします。

        | ユーザー            | 種類    | データベース ロール |
        |-----------------|---------|---------------|
        | svc-AXSF$       | gMSA    | db\_owner     |
        | svc-LocalAgent$ | gMSA    | db\_owner     |
        | svc-FRPS$       | gMSA    | db\_owner     |
        | svc-FRAS$       | gMSA    | db\_owner     |
        | axdbadmin       | SqlUser | db\_owner     |

    4. **TempD** データベースの次の表に基づいて、データベース ロールにユーザーをマップします。

        | ユーザー      | 種類    | データベース ロール |
        |-----------|---------|---------------|
        | svc-AXSF$ | gMSA    | db\_datareader、db\_datawriter、db\_ddladmin |
        | axdbadmin | SqlUser | db\_datareader、db\_datawriter、db\_ddladmin |

    Configure-Database.ps1 スクリプトは、以下の処理を行います:

    1. **READ\_COMMITTED\_SNAPSHOT** を **オン** に設定します。
    2. **ALLOW\_SNAPSHOT\_ISOLATION** を **オン** に設定します。
    3. 指定したデータベースファイル と ログの設定を行います。
    4. **VIEW SERVER STATE** 権限を **axdbadmin** に付与します。
    5. **ALTER ANY EVENT SESSION** 権限を **axdbadmin** に付与します。
    6. **VIEW SERVER STATE** 権限を **\[contoso\\svc-AXSF$\]** に付与します。
    7. **ALTER ANY EVENT SESSION** 権限を **\[contoso\\svc-AXSF$\]** に付与します。

2. データベース ユーザーをリセットするには、次のコマンドを実行します。

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a>財務レポート データベースのコンフィギュレーション

- 次のコマンドを実行します。

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
    ```

    Initialize-Database.ps1 スクリプトは、以下の処理を行います:

    1. **FinancialReporting** という名前の空のデータベースを作成します。
    2. 次の表に基づいて、データベース ロールにユーザーをマップします。

        | ユーザー            | 種類 | データベース ロール |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |
        | svc-FRPS$       | gMSA | db\_owner     |
        | svc-FRAS$       | gMSA | db\_owner     |

### <a name="step-15-encrypt-credentials"></a><a name="encryptcred"></a>手順 15、 資格情報の暗号化

1. 任意のクライアント コンピューターで、**LocalMachine\\My** 証明書ストアに暗号化証明書をインストールします。
2. 現在のユーザーにこの証明書の秘密キーへの **読み取り** アクセスを許可します。
3. 次のようにして、**Credentials.json** ファイルを作成します。

    ```json
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** – AOS ドメインユーザー (**contoso\\axserviceuser**) の暗号化されたドメイン ユーザー パスワード。
    - **SqlUser** – Finance + Operations データベース (**AXDB**) にアクセス権限が付与されている暗号化された SQL ユーザー (**axdbadmin**)
    - **SqlPassword** – 暗号化された SQL パスワード。

4. .json ファイルを SMB ファイル共有: **\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json** にコピーします。
5. 暗号化された値で **Credentials.json** ファイルを更新します。

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```

    > [!IMPORTANT]
    > - **Invoke-ServiceFabricEncryptText** コマンドを呼び出す前に、[Microsoft Azure Service Fabric ソフトウェア開発キット (SDK)](/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。
    > - Service Fabric SDK をインストールした後で、次のエラー メッセージが表示されます:「Invoke-ServiceFabricEncryptText は認識されないコマンドです」 この場合は、コンピュータを再起動し、もう一度やり直してください。

    > [!WARNING]
    > すべての **ServiceFabricEncryptText** コマンドの起動が完了したら、Windows PowerShell の履歴を削除することを忘れないでください。 それ以外の場合は、暗号化されていない資格情報が表示されます。

### <a name="step-16-set-up-ssis"></a><a name="setupssis"></a>手順 16、 SSIS を設定する

データ管理と SSIS ワークロードを有効にするには、各 AOS VM に SSIS をインストールする必要があります。 各 AOS VM で、次の手順に従います。

1. コンピューターに SSIS インストールへのアクセス許可があることを確認し、**SSIS セットアップ** ウィザードを開きます。
2. **機能の選択** ページの **機能** ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。
3. セットアップを完了し、インストールが正常に完了したことを確認します。

詳細については、[統合サービス (SSIS) のインストール](/sql/integration-services/install-windows/install-integration-services)を参照してください。

### <a name="step-17-set-up-ssrs"></a><a name="setupssrs"></a>手順 17、 SSRS を設定する

複数の SSRS ノードを構成できます。 詳細については、[SSRS ノードの高可用性の構成](./onprem-SSRSHA.md)を参照してください。

1. 開始する前に、このトピックの冒頭に記載されている[前提条件](#prerequisites)が満たされていることを確認します。

    > [!IMPORTANT]
    > - SSRS のインストール時にデータベース エンジンをインストールする必要があります。
    > - SSRS インスタンスを構成 **しない** でください。 レポート サービスは、すべてを自動的に構成されます。
    > - Platform update 41 より古い基準トポロジが配置されている環境では、次の手順を実行する必要はありません。 このような環境では、[オンプレミス配置の SQL Server Reporing Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) に従って SSSR を手動で構成する必要があります。

1. 各 BI ノードについては、次の手順を実行します。

    1. **インフラストラクチャ** フォルダーをコピーします。 次に、管理者特権モードで Windows PowerShell を開き、フォルダーに移動します。
    1. 次のコマンドを実行します。

        ```powershell
        .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName BI
        .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName BI
        ```

        Initialize-Database.ps1 スクリプトは、gMSA を次のデータベースおよびロールにマップします。

        | ユーザー           |  データベース | データベース ロール |
        |----------------|----------|---------------|
        | svc-ReportSvc$ | マスター   | db\_owner |
        | svc-ReportSvc$ | msdb     | db\_datareader、db\_datawriter、db\_securityadmin |

        Configure-Database.ps1 スクリプトは、以下のアクションを実行します:

        - **CREATE ANY DATABASE** 権限を **\[contoso\\svc-ReportSvc$\]** に付与します。
    
    > [!NOTE]
    > これらのスクリプトは SSRS を構成 **できません**。 配置中に、そのノードに配置されたService Fabric サービス (ReportingService) によって SSRS が構成されます。
    > 
    > 代わりに、これらのスクリプトは、Service Fabric サービス (ReportingService) が必要なコンフィギュレーションを実行するために必要なアクセス許可を付与します。

### <a name="step-18-configure-ad-fs"></a><a name="configureadfs"></a>手順 18、 AD FS のコンフィギュレーション

この手順を完了する前に、AD FS を Windows Server 2019 または Windows Server 2016 に展開する必要があります。 AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。

Finance + Operations では、既定で標準のコンフィギュレーション以外の、AD FS の追加のコンフィギュレーションが必要です。 以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。 たとえば、ユーザーには、ドメイン管理者アカウントが必要です。 複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。

1. AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。

    このコマンドは、Finance + Operations クライアントの **ユーザー** ページ (**システム管理** \> **ユーザー** \> **ユーザー**) での **ユーザーをインポートする** オプションの使用による新しいユーザーの追加に関連しています。

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. 混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。 WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。

    このコマンドは、Finance + Operations クライアントへのサインイン時のフォーム認証の使用に関連しています。 シングル サインインなどの他のオプションはサポートされていません。

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。

    このコマンドは、電子メール要求の設定に関連しています。 変換ルールなど、他のオプションも利用できる場合がありますが、追加の設定が必要です。

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

AD FS が認証を交換するために Finance + Operations を信頼できるようにするには、AD FS で AD FS アプリケーション グループの下にさまざまなアプリケーション エントリを登録する必要があります。 設定プロセスをスピードアップしてエラーを減らすために、Publish-ADFSApplicationGroup.ps1 スクリプトを使用して登録します。 このスクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているコンピューターにコピーします。 次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。 (たとえば、管理者アカウントを使用します。)

スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。 後に LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。 クライアント ID を失った場合は、AD FS がインストールされているコンピューターにサインインし、サーバー マネージャーを開き、**ツール** \> **AD FS 管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations オンプレミス** の順に移動します。 ネイティブ アプリケーションでクライアント ID を検索できます。

> [!NOTE]
> 以前に構成した AD FS サーバーを別の環境で再利用する方法については、[複数の環境に同じ AD FS インスタンスを再使用する](./onprem-reuseadfs.md) を参照してください。

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。 このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。 サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。 この手順については、「AD FS 展開ガイド」で説明されています。 リモート処理を使用している場合は、次のコマンドを実行して Service Fabric Cluster のすべてのノードに証明書をインストールできます。

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

URL にアクセスできる場合、JavaScript Object Notation (JSON) ファイルが返されます。 このファイルには AD FS コンフィギュレーションが含まれており、AD FS URL が信頼されていることを示します。

これで、インフラストラクチャの設定を完了しました。 次のセクションでは、コネクタを設定して LCS に Finance + Operations 環境を展開する方法について説明します。

### <a name="step-19-configure-a-connector-and-install-an-on-premises-local-agent"></a><a name="configureconnector"></a>手順 19、 コネクタを構成し、オンプレミスのローカル エージェントをインストールする

1. [LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。
2. メニュー ボタン (ハンバーガーまたはハンバーガー ボタンと呼ばれる場合もあります) を選択してから、**プロジェクト設定** を選択します。
3. **オンプレミス コネクタ** を選択します。
4. **追加** を選択して、新しいオンプレミス コネクタを作成します。 
5. **1: ホスト インフラストラクチャ設定** タブで、**エージェント インストーラーをダウンロードする** を選択します。
6. zip ファイルのダウンロード後、そのファイルがブロックされていないことを確認します。 ファイルを選択したまま (または右クリック) にしてから、**プロパティ** を選択します。 **プロパティ** ダイアログ ボックスで、**ブロック解除** チェック ボックスを選択します。
7. **OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。
8. ファイルの解凍後、LCS のオンプレミス コネクタに戻ります。
9. **2: エージェントのコンフィギュレーション** タブで、**コンフィギュレーションの入力** を選択し、コンフィギュレーション設定を入力します。 必要な値を取得するには、**インフラストラクチャ** フォルダーと最新のコンフィギュレーション ファイルを持つすべてのコンピューターで次のコマンドを実行します。

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

10. コンフィギュレーションを保存してから、**コンフィギュレーションのダウンロード** を選択して **localagent-config.json** コンフィギュレーション ファイルをダウンロードします。
11. **localagent-config.json** ファイルを、エージェント インストーラー パッケージが展開されているコンピューターにコピーします。
12. **コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。

13. ローカル エージェントが正常にインストールされてから、LCS のオンプレミス コネクタに戻るようにします。
14. **3: 設定の検証** タブで、**メッセージ エージェント** を選択して、ローカル エージェントへの LCS 接続をテストします。 接続が正常に確立されると、下のメッセージが表示されます: 「検証が完了しました。 エージェントへの接続が確立されました。」

### <a name="step-20-tear-down-credssp-if-remoting-was-used"></a><a name="teardowncredssp"></a>手順 20、 リモート処理が使用されたら、CredSSP を終了処理する

セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了後に、次のコマンドを実行してください。

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

以前のリモート処理 Windows PowerShell ウィンドウが誤って終了し、CredSSP が有効になったままである場合、このコマンドにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。

### <a name="step-21-deploy-your-finance--operations-environment-from-lcs"></a><a name="deploy"></a>手順 21、 LCS から Finance + Operations 環境を配置する

1. LCS で、オンプレミスの実装プロジェクトを開きます。
2. **環境** \> **サンドボックス** に移動し、**コンフィギュレーション** を選択します。 必要な値を取得するには、プライマリ ドメイン コントローラ VM で次のコマンドを実行します。 その VM には、ADFS および DNS サーバー設定へのアクセス許可が必要です。

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

3. 新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。

    準備フェーズ中に、LCS は環境の Service Fabric アプリケーション パッケージを組み立てます。 配置を開始するローカル エージェントにメッセージを送信します。 環境ステータスが **準備中** であることに注意します。

    ![準備状態の環境](./media/Preparing2021.png)

4. 環境の詳細ページで、**完全な詳細** を選択します。 ページの右上隅には、環境ステータスが **準備中** として表示されることを確認します。

    ![準備中ステータスを表示する環境の詳細ページ](./media/Details_Preparing2021.png)

    ローカル エージェントは展開要求を受け取り、展開を開始し、環境の準備ができたら LCS に再度通知します。 展開を開始すると、環境の状態が **展開中** に変わることに注意します。

    ![展開状態の環境](./media/Deploying2021.png)

5. 環境の詳細ページで、**完全な詳細** を選択します。 ページの右上隅には、環境ステータスが **展開中** として表示されることを確認します。

    ![展開中ステータスを表示する環境の詳細ページ](./media/Details_Deploying2021.png)

6. 展開に失敗すると、環境の状態が **失敗** に変更され、**再構成** ボタンが環境で使用可能になります。 基になる問題を修正し、**再構成** を選択して、任意のコンフィギュレーションの変更を更新してから、**展開** の再試行を選択します。

    ![失敗状態の環境で使用する再構成ボタン](./media/Failed2021.png)

    環境を再構成する方法の詳細については、[環境を再構成して、新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md)を参照してください。

次の図は、正常な展開を示します。 ページの右上隅には、環境ステータスが **展開済** として表示されることを確認します。

![環境が正常に展開された](./media/Deployed2021.png)

### <a name="step-22-connect-to-your-finance--operations-environment"></a><a name="connect"></a>手順 22、 Finance + Operations 環境への接続

- Web ブラウザーで、`https://[yourD365FOdomain]/namespaces/AXSF` に移動します。そこでは **yourD365FOdomain** がこのトピック前半の [手順 1. ドメイン名と DNS ゾーンの計画](#plandomain)セクションで定義したドメイン名です。

## <a name="known-issues"></a>既知の問題

### <a name="when-you-run-the-new-d365fogmsaaccounts-cmdlet-you-receive-the-following-error-message-key-does-not-exist"></a>New-D365FOFOSAAccounts cmdlet を実行すると、次のエラー メッセージが表示されます: 「キーが存在しません」 

ドメインで gMSA パスワードを初めて作成し生成する場合は、最初にキー配分サービス KDS ルート キーを作成する必要があります。 詳細については、[キー配分サービス KDS ルート キーの作成](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。

### <a name="when-you-run-the-remoting-script-configure-prereqs-allvms-cmdlet-you-receive-the-following-error-message-the-winrm-client-cannot-process-the-request"></a>リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行すると、次のエラー メッセージが表示されます: 「WinRM クライアントは要求を処理できません」

Service Fabric Cluster のすべてのコンピューターで **新しい資格情報委任を許可する** コンピューター ポリシーを有効にするには、エラー メッセージの指示に従います。

### <a name="when-you-configure-prereqs-on-servers-of-the-mrtype-and-reportservertype-types-you-receive-the-following-error-message-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed"></a>MRType および ReportServerType タイプのサーバーで Configure-Prereqs を実行すると次のエラー メッセージが表示されます:「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」 

.NET Framework version 3.5 は、**MRType** および **ReportServerType** タイプのサーバーでは必須です。 ただし、既定では .NET Framework version 3.5 のソース ファイルは Windows Server 2016 インストールに含まれていません。 このエラーを回避するには、.NET Framework Version 3.5 をインストールします。 サーバー マネージャーを使用して新機能を手動で追加する場合、**ソース** オプションを使用してソース ファイルを指定します。

### <a name="when-you-run-the-publish-adfsapplicationgroup-cmdlet-you-receive-the-following-error-message-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration"></a>Publish-ADFSApplicationGroup cmdlet を実行すると次のエラー メッセージが表示されます:「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」

このエラーは、D365FO-OP-ADFSApplicationGroup が必要とする OpenID **allatclaims** スコープが、一部の Windows Server 2016 インストールでは表示されないために発生します。 エラーを回避するには、サーバー マネージャーを開き、**ツール** /> **AD FS の管理** /> **サービス** /> **スコープの説明** の順に移動し、**allatclaims** スコープの説明を追加します。

### <a name="when-you-run-the-publish-adfsapplicationgroup-cmdlet-you-receive-the-following-error-message-admin0077-access-control-policy-does-not-exist-permit-everyone"></a>Publish-ADFSApplicationGroup cmdlet を実行すると次のエラー メッセージが表示されます:「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可してください」

英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、**すべてのユーザーを許可する** アクセス許可ポリシーがローカル言語で作成されます。 次の方法で cmdlet を呼び出して **AccessControlPolicyName** パラメーターを指定します。

```powershell
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'
```

## <a name="additional-resources"></a>追加リソース

- [オンプレミス配置への更新プログラムの適用](apply-updates-on-premises.md)
- [オンプレミス環境の再配置](redeploy-on-prem.md)
- [ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)
- [電子申告 (ER) コンフィギュレーションのインポート](../analytics/electronic-reporting-import-ger-configurations.md)
- [オンプレミス配置でのドキュメントの生成、発行、印刷](../analytics/printing-capabilities-on-premises.md)
- [オンプレミス環境用プロキシの構成](onprem-reverseproxy.md)
- [Finance and Operations アプリのテクニカル サポートの設定](../lifecycle-services/support-experience.md)
- [クライアント インターネット接続](../user-interface/client-disconnected.md)
