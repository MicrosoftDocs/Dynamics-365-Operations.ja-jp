---
title: オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 から 40)
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 から 40 を計画、設定、展開する方法について説明します。
author: PeterRFriis
ms.date: 06/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: ac33ec5ae68a035e376a4b57f6421ef81258dc88
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595001"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-updates-12-through-40"></a>オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12 から 40)

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) プラットフォーム更新プログラム 12 から 40 を計画、設定、展開する方法について説明します。

[ローカル ビジネス データ Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=13595809&view=all) が利用可能です。 オンプレミス展開に関する質問またはフィードバックをそこに投稿することができます。

このトピックの内容に関する質問やフィードバックがある場合は、このページ下の **コメント** セクションに転記してください。

## <a name="finance--operations-components"></a>Finance + Operations のコンポーネント

Finance + Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。

- Application Object Server (AOS)
- ビジネス インテリジェンス (BI)
- 財務レポート/管理レポーター

これらのコンポーネントは、次のシステム ソフトウェアによって異なります。

- Microsoft Windows Server 2016 (英語 OS のインストールのみがサポートされます)
- Microsoft SQL Server 2016 SP1 および SP2 (プラットフォーム更新プログラム 33 から) には次の機能があります。
  - フルテキスト インデックス検索が有効にされている。
  - SQL Server Reporting Services (SSRS) - これは BI 仮想マシンに配置されます。
  - SQL Server Integration Services (SSIS) - これは AOS 仮想マシンに配置されます。

    > [!WARNING]
    > 完全なテキスト検索を有効にする必要があります。

- SQL Server Management Studio
- スタンドアロン Microsoft Azure Service Fabric
- Microsoft Windows PowerShell 5.0 以降
- Windows Server 2016 での Active Directory Federation Services (AD FS)
- ドメイン コントローラー

  > [!WARNING]
  > ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。    ドメイン機能レベルの詳細については、次のトピックを参照してください。
  >   - [Active Directory 機能レベルとは](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))
  >   - [Active Directory ドメイン サービス機能のレベルを理解する](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))
  >   - [双方向の完全な信頼](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance + Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。 配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。 LCS からのみ配置を開始することができます。 LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。

## <a name="authentication"></a>認証

オンプレミス アプリケーションは AD FS で動作します。 LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。 配置を完了し、LCS ローカル エージェントを構成するには、AAD が必要です。 AAD テナントがまだない場合は、AAD によって提供されるオプションのいずれかを使用して無料のものを取得できます。 詳細については、[Azure Active Directory テナントを取得する方法](/azure/active-directory/develop/active-directory-howto-tenant) を参照してください。

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance + Operations は スタンドアロン Service Fabric を使用します。 詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。

Finance + Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。 展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。

- **AOSNodeType** - アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。
- **OrchestratorType** - Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。
- **ReportServerType** - SSRS およびレポート ロジックをホストします。
- **MRType** - 管理レポート ロジックをホストします。

## <a name="infrastructure"></a>インフラストラクチャ

Finance + Operations には、非 Microsoft 仮想化プラットフォーム (特に VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。 詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw) を参照してください。 要するに、私たちはこの環境で当社製品をサポートしています。 ただし、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまず顧客に依頼する場合があります。

VMWare を使用している場合は、次の Web ページに記載されている修正プログラムを実装する必要があります。
- [仮想マシンをハードウェア バージョン 11 にアップグレード後、ネットワーク依存ワークロードのパフォーマンスが低下する (2129176)](https://kb.vmware.com/s/article/2129176)
- [vmxnet3 仮想アダプターのいくつかの問題](https://vinfrastructure.it/2016/05/several-issues-vmxnet3-virtual-adapter)

> [!IMPORTANT]
> Dynamics 365 Finance + Operations (オンプレミス) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。 ただし、[Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。

ハードウェア構成には、次のコンポーネントが含まれます。

- Windows Server 2016 仮想マシン (VM) に基づく スタンドアロン Service Fabric Cluster
- Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)
- 認証のための AD FS
- ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有
- オプション: Microsoft Office Server 2017

詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) を参照してください。

### <a name="hardware-layout"></a>ハードウェア レイアウト

[オンプレミス環境のハードウェア サイジング要件](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric Cluster を計画します。 Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

次のテーブルは、ハードウェア レイアウトの例を示しています。 この例は、設定を説明するためにこのトピック全体で使用されています。 次の手順で指定されているマシン名と IP アドレスを、ご使用の環境のマシンの名前と IP アドレスに置き換える必要があります。

> [!NOTE]
> Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。 この例では **OrchestratorType** を主要なノード タイプとして指定します。

| マシンの目的          | SF ノード タイプ     | コンピューター名    | IP アドレス    |
|--------------------------|------------------|-----------------|---------------|
| ドメイン コントローラー        |                  | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                    |                  | DAX7SQLAOADFS1  | 10.179.108.3  |
| ファイル サーバー              |                  | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On クラスター    |                  | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                          |                  | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                          |                  | DAX7SQLAOSQLA   | 10.179.108.9  |
| クライアント                   |                  | SQLAOCLIENT1    | 10.179.108.11 |
| AOS 1                    | AOSNodeType      | SQLAOSF1AOS1    | 10.179.108.12 |
| AOS 2                    | AOSNodeType      | SQLAOSF1AOS2    | 10.179.108.13 |
| AOS 3                    | AOSNodeType      | SQLAOSF1AOS3    | 10.179.108.14 |
| オーケストレータ 1           | OrchestratorType | SQLAOSF1ORCH1   | 10.179.108.15 |
| オーケストレータ 2           | OrchestratorType | SQLAOSF1ORCH2   | 10.179.108.16 |
| オーケストレータ 3           | OrchestratorType | SQLAOSF1ORCH3   | 10.179.108.17 |
| Management Reporter ノード | MRType           | SQLAOSMR1       | 10.179.108.18 |
| SSRS ノード                | ReportServerType | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>段取り

### <a name="prerequisites"></a>前提条件

セットアップを開始する前に、次の前提条件が満たされている必要があります。 これらの前提条件の設定は、このドキュメントの範囲外です。

- Active Directory Domain Services (AD DS) は、ネットワークにインストールして構成する必要があります。
- AD FS は、展開する必要があります。
- SQL Server 2016 SP2 は SSRS コンピューターにインストールされている必要があります。
- SQL Server Reporting Services 2016 は、SSRS コンピューターに **ネイティブ** モードでインストールする必要があります。

次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。

| ノード タイプ | コンポーネント | 細目 |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC ドライバー 13 | [ODBC ドライバー 13.1](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) |
| AOS       | SNAC – ODBC ドライバー 17 | このドライバーは、PU15 以上へのアップグレードに必要です。<https://aka.ms/downloadmsodbcsql> |
| AOS       | Microsoft .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| AOS       | Microsoft .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| AOS       | Microsoft .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| AOS       | インターネット インフォメーション サービス (IIS) | **Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console |
| AOS       | SQL Server Management Studio 17.2 | <https://go.microsoft.com/fwlink/?linkid=854085> |
| AOS       | Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| AOS       | Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://lcs.dynamics.com/V2/SharedAssetLibrary>> モデル > "VC ++ 17 再頒布可能" |
| AOS       | Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> |
| BI        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| BI        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| BI        | Microsoft .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| BI        | SQL Server Management Studio 17.2 | <https://go.microsoft.com/fwlink/?linkid=854085> |
| MR        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| MR        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| MR        | Microsoft .NET Framework version 4.7.2 (CLR 4.0) | https://dotnet.microsoft.com/download/thank-you/net472-offline |
| MR        | Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| ORCH      | Microsoft .NET Framework version 4.0–4.8 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net48-offline> |

### <a name="overview"></a>概要

Finance + Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。 開始する前にすべての手順を読むと、セットアップを計画しやすくなります。

1. [ドメイン名と DNS ゾーンの計画](#plandomain)
2. [証明書の計画と取得](#plancert)
3. [ユーザーとサービス アカウントの計画](#plansvcacct)
4. [DNS ゾーンの作成と A レコードの追加](#createdns)
5. [VM のドメインへの参加](#joindomain)
6. [LCS からセットアップ スクリプトのダウンロード](#downloadscripts)
7. [コンフィギュレーションの記述](#describeconfig)
8. [証明書の構成](#configurecert)
9. [VM を設定する](#setupvms)
10. [スタンドアロン Service Fabric クラスターの設定](#setupsfcluster)
11. [テナント用 LCS 接続の構成](#configurelcs)
12. [ファイル ストレージの設定](#setupfile)
13. [SQL Server の設定](#setupsql)
14. [データベースを構成する](#configuredb)
15. [資格情報の暗号化](#encryptcred)
16. [資産除去債務 (SSIS) の設定](#setupssis)
17. [資産除去債務 (SSRS) の設定](#setupssrs)
18. [AD FS のコンフィギュレーション](#configureadfs)
19. [コネクタを構成し、オンプレミスのローカル エージェントをインストールする](#configureconnector)
20. [リモート処理が使用されたら、CredSSP を終了処理する](#teardowncredssp)
21. [LCS から Finance + Operations 環境を配置する](#deploy)
22. [Finance + Operations 環境への接続](#connect)

### <a name="1-plan-your-domain-name-and-dns-zones"></a><a name="plandomain"></a> 1. ドメイン名と DNS ゾーンの計画

AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。 このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。

たとえば、会社のドメインが contoso.com の場合、Finance + Operations は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。

- AOS の機械の場合 ax.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com

### <a name="2-plan-and-acquire-your-certificates"></a><a name="plancert"></a> 2. 証明書の計画と取得

Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。 プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。 ドメインが [Active Directory 証明書サービス](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772393(v=ws.10)) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。 証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。

自己署名証明書は、テスト目的でのみ使用できます。 便宜上、LCS で提供されるセットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれます。 自己署名スクリプトを使用している場合は、後の手順で作成スクリプトを実行するように指示されます。 先に述べたように、これらの証明書はテスト目的でのみ使用できます。

証明書の推奨設定は次のとおりです:
- 署名アルゴリズム: sha256RSA
- 署名ハッシュ アルゴリズム: sha256
- 公開キー: RSA (2048 ビット)
- Thumbprint アルゴリズム: sha1

| 目的                                      | 説明 | 追加条件 |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL 証明書                   | この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。 | <p>証明書の場合、ドメイン名は SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。 たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.contoso.com です。</p> <p>CN: DAX7SQLAOSQLA.contoso.com <br> DNS 名: DAX7SQLAOSQLA.contoso.com</p> |
| Service Fabric Server 証明書            | <p>この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</p> <p> この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</p> | <p>この証明書には、ドメインの SSL ワイルド カード証明書も使用できます。 たとえば、\*.contoso.com です。 これについて下の表で詳しく説明します。 それ以外の場合は、次の値を使用します:</p> <p>CN: sf.d365ffo.onprem.contoso.com <br> DNS 名: sf.d365ffo.onprem.contoso.com</p> |
| Service Fabric Client 証明書            | この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。 | CN: client.d365ffo.onprem.contoso.com <br> DNS 名: client.d365ffo.onprem.contoso.com |
| 証明書の暗号化                     | この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。 | <p> 証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。 </p><p>証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</p><p>詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</p> <p> CN: axdataenciphermentcert <br> DNS 名: axdataenciphermentcert </p> |
| AOS SSL 証明書                          | <p>この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。 また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</p> | <p>Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。 それ以外の場合は、次の値を使用します:</p> <p> CN: ax.d365ffo.onprem.contoso.com <br> DNS 名: ax.d365ffo.onprem.contoso.com </p> |
| セッション認証証明書           | この証明書は、AOS がユーザーのセッション情報を保護するために使用します。 | <p> この証明書は、LCS からの展開時に使用されるファイル共有証明書です。</p> <p> CN: SessionAuthentication <br> DNS 名: SessionAuthentication </p> |
| データの暗号化証明書                  | これらの証明書は、機密情報を暗号化するために AOS によって使用されます。  | <p>これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。 </p> <p> CN: DataEncryption <br> DNS 名: DataEncryption </p> |
| データ署名の証明書                     | これらの証明書は、機密情報を暗号化するために AOS によって使用されます。  | <p> これは、データ暗号化証明書とは別のもので、プロバイダー **Microsoft の拡張された RSA および AES 暗号化プロバイダー** を使用して作成する必要があります。 </p> <p> CN: DataSigning <br> DNS 名: DataSigning </p> |
| 財務報告クライアント証明書       | この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。 | <p>CN: FinancialReporting <br> DNS 名: FinancialReporting </p>  |
| 報告証明書                        | この証明書を使用して、SSRS と AOS 間の通信を保護します。| <p> **財務報告クライアント証明書を再利用しないでください。** </p> <p> CN: ReportingService <br> DNS 名: ReportingService </p> |
| オンプレミス ローカル エージェント証明書           | <p>この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</p><p>この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</p><p>**注記:** テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</p> | <p> CN: OnPremLocalAgent <br> DNS 名: OnPremLocalAgent </p> |

ドメインの SSL ワイルド カード証明書を使用して、Service Fabric サーバー証明書と AOS SSL 証明書を結合できます。

以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。

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

> [!NOTE]
> ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。

### <a name="3-plan-your-users-and-service-accounts"></a><a name="plansvcacct"></a> 3. ユーザーとサービス アカウントの計画

Finance + Operations を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。 サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。 次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。

| ユーザー アカウント                                            | 種類           | 目的 | ユーザー名 |
|---------------------------------------------------------|----------------|---------|-----------|
| 財務レポート アプリケーション サービス アカウント         | gMSA           |         | Contoso\\svc-FRAS$ |
| 財務レポート プロセス サービス アカウント             | gMSA           |         | Contoso\\svc-FRPS$ |
| 財務レポート クリック ワンス デザイナー サービス アカウント | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS サービス アカウント                                     | gMSA           | このユーザーは、将来校正するために作成する必要があります。 今後のリリースでは、AOS を gMSA と連携させる予定です。 このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。\* | Contoso\\svc-AXSF$ |
| AOS サービス アカウント                                     | ドメイン アカウント | AOS は、一般提供 (GA) リリースでこのユーザーを使用します。 | Contoso\\AXServiceUser |
| AOS SQL DB 管理者ユーザー                                   | SQL ユーザー       | Finance + Operations は、このユーザーを使用して SQL\*\* を認証します。 このユーザーは、今後のリリース \*\*\* で gMSA ユーザーにも置き換えられます。 | AXDBAdmin |
| ローカル配置エージェント サービス アカウント                  | gMSA           | このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。 | Contoso\\Svc-LocalAgent$ |

\* これらのアカウントでは、地域の設定を変更しないでください。 既定の EN-US リージョン設定が必要です。 

\*\* SQL ユーザーのパスワードに特殊文字が含まれている場合、展開中に問題が発生する場合があります。

\*\*\* SQL 認証で使用する SQL ユーザ名とパスワードは暗号化されてファイル共有に保存されているため、安全性が確保されています。

### <a name="4-create-dns-zones-and-add-a-records"></a><a name="createdns"></a> 4. DNS ゾーンの作成とレコードの追加

DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。 次の指示では、AOS ホスト名と Service Fabric クラスターの DNS 前方参照ゾーンと A レコードを作成する手順を示します。 この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。

- AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com

#### <a name="add-a-dns-zone"></a>DNS ゾーンの追加

DNS ゾーンを追加するには、次の手順を実行します。

1. ドメイン コントローラー コンピューターにログインして **スタート** を選択し、**dnsmgmt.msc** と入力して **dnsmgmt (DNS)** アプリケーションを選択することにより DNS マネージャーを起動します。
2. コンソール ツリーでドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。
3. **プライマリ ゾーン** を選択します。
4. **Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ** を選択します。
5. **このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して** を選択し、**次へ** を選択します。
6. **前方参照ゾーン** を選択し、**次へ** を選択します。
7. 設定するゾーン名を入力し、**次へ** をクリックします。 たとえば、**d365ffo.onprem.contoso.com** と入力します。
8. **動的更新を許可しない** を選択し、**次へ** を選択します。
9. **完了** を選択します。

#### <a name="set-up-an-a-record-for-aos"></a>AOS の A レコードを設定する

新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード **ごと** に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. DNS マネージャーの **前方参照ゾーン** フォルダーで、新しく作成したゾーンを検索します。
2. 新しいゾーンを右クリックして、**新しいホスト** を選択します。
3. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**ax** を名前として入力し、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加** を選択します。
4. どのチェック ボックスもオンにしないでください。
5. 各 AOS ノードで手順 1 ～ 4 を繰り返します。

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Orchestrator の A レコードを設定する

新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード **ごと** に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを右クリックして、**新しいホスト** を選択します。
2. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**sf** を名前としてを入力し、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加** を選択します。
3. どのチェック ボックスもオンにしないでください。
4. 各オーケストレータ ノードを繰り返します。

### <a name="5-join-vms-to-the-domain"></a><a name="joindomain"></a> 5. VM のドメインへの参加

各 VM をドメインに参加させるには、[コンピューターをドメインに参加させる](/windows-server/identity/ad-fs/deployment/join-a-computer-to-a-domain)のドキュメントの手順を完了します。 または、次の Windows PowerShell スクリプトを使用します。

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> ドメインにそれらを結合させた後、VM を再起動する必要があります。

### <a name="6-download-setup-scripts-from-lcs"></a><a name="downloadscripts"></a> 6. LCS からのセットアップ スクリプトのダウンロード

セットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介しています。 LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。

> [!IMPORTANT]
> スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。
2. ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。
3. **モデル** タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト** 行を選択します。
4. **バージョン** を選択し、スクリプトの zip ファイルの最新版をダウンロードします。
   >[!Note] 
   > プラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 の以前のバージョンが必要な場合は、バージョン 1 をダウンロードします。
5. zip ファイルを右クリックし、**プロパティ** を選択します。 ダイアログ ボックスで、**ブロック解除** チェック ボックスをオンにします。
6. ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。
7. **infrastructure** という名前のフォルダーにファイルを解凍します。

> [!IMPORTANT]
> このフォルダーの ConfigTemplate.xml ファイルにすべての編集を加える必要があります。

### <a name="7-describe-your-configuration"></a><a name="describeconfig"></a> 7. コンフィギュレーションの記述

インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。
- infrastructure\ConfigTemplate.xml
- infrastructure\D365FO-OP\NodeTopologyDefinition.xml
- infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml

>[!NOTE]
>セットアップ スクリプトが正しく機能するには、環境に基づいてコンフィギュレーション ファイルを更新する必要があります。 これらのファイルは、設定に基づいて適切なコンピューター名、IP アドレス、サービス アカウントおよびドメインで更新してください。

**infrastructure\ConfigTemplate.xml** で説明します。
- アプリケーションが動作するために必要なサービス アカウント
- 通信を保護するために必要な証明書
- データベース コンフィギュレーション
- Service Fabric クラスター構成

    > [!IMPORTANT]
    > Service Fabric クラスタをコンフィギュレーションする際に OrchestratorType の 3 つのフォールト ドメインがあることを確認します。 Service Fabric クラスタをコンフィギュレーションする際、単一のマシンにノードの 1 つのタイプのみが配置されるよう確認します。

各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。

- 各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。
- UAC を有効にするかどうか。
- Windows の機能とシステム ソフトウェアの前提条件。
- 厳密な名前の検証を有効にするかどうか。
- ファイアウォール ポートのリストを開く必要があります。

各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。

- データベース設定。
- ユーザーとロール間のマッピング。

#### <a name="create-gmsa-and-domain-user-accounts"></a>gMSA およびドメイン ユーザー アカウントを作成する

1. **インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。
2. **インフラストラクチャ** フォルダーをドメイン コントローラー マシンにコピーします。
3. 管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。
    > [!IMPORTANT]
    > 次のスクリプトは、ドメイン ユーザー AxServiceUser を作成しません。 ユーザーが作成する必要があります。

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```
    


4. AOS サービス アカウントの **Contoso\svc-AXSF$** および **Contoso\AXServiceUser** をすべての AOS マシンのローカル 管理者グループへ追加します。 詳細については、「[ローカル グループへのメンバーの追加](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772524(v=ws.11))」を参照してください。

5. アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="8-configure-certificates"></a><a name="configurecert"></a> 8. 証明書のコンフィギュレーション

1. **インフラストラクチャ** フォルダーがあるマシンに移動します。
2. 証明書を生成します。 
    1. 自己署名証明書を生成する必要がある場合は、次の設定を行います。
        1. **generateSelfSignedCert** の属性を **true** に設定します。 生成する必要がある証明書にのみこれを設定します。 
        1. 次のコマンドを実行します。 スクリプトによって証明書が作成されます。 証明書をコンピューターの CurrentUser\My certificate store に格納し、XML ファイルのサムプリントを更新します。

        ```powershell
        # Create self-signed certs
        .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```
    1. Active Directory 証明書サービス (AD CS) 証明書を生成する場合は、次の方法で作成します。
        1. 生成したくない証明書の **generateADCSCert** 属性を **false** に設定します。
        1. 次のコマンドを実行します。 スクリプトは、AD CS で証明書テンプレートを作成します。 テンプレートから証明書を生成し、コンピューターの CurrentUser\My certificate store に格納し、XML ファイルのサムプリントを更新します。

        ```powershell
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -CreateTemplates
        .\New-ADCSCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
        ```

        > [!NOTE] 
        > AD CS スクリプトは、ドメイン コントローラーまたはリモート サーバー管理ツールがインストールされている Windows Server で実行する必要があります。

3. 既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルのサムプリントを更新します。 証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。

    > [!WARNING]
    > 存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。 印刷できない特殊文字がある場合、**X509 証明書が無効です** というエラーが表示されます。 拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。
    > ```powershell
    > dir cert:\CurrentUser\My
    > dir cert:\LocalMachine\My
    > dir cert:\LocalMachine\Root
    > ```

4. 各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。 **ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。 エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。

5. 証明書を .pfx ファイルにエクスポートします。 エクスポートの一環として、このスクリプトは、証明書に正しい暗号化プロバイダが設定されているかどうかをチェックします。 

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="9-setup-vms"></a><a name="setupvms"></a> 9. VM の設定
1. 各 VM で実行する必要があるスクリプトをエクスポートします。

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. 次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。

    | コンポーネント | リンクのダウンロード | 必要なファイル名 |
    |-----------|---------------|--------------------|
    | SNAC – ODBC ドライバー 13 | [ODBC ドライバー 13.1](/sql/connect/odbc/windows/release-notes-odbc-sql-server-windows#131) | Msodbcsql .msi |
    | SNAC – ODBC ドライバー 17 | <https://aka.ms/downloadmsodbcsql> | msodbcsql\_17.msi |
    | Microsoft SQL ServerManagement Studio 17.5 | [SSMS 17.5](/sql/ssms/download-sql-server-management-studio-ssms) | SSMS-Setup-\*.exe |
    | Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> | vcredist\_x64.exe |
    | Microsoft Visual Studio 2017 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://lcs.dynamics.com/V2/SharedAssetLibrary>に移動して、資産タイプとして **モデル** を選択して、**VC++ 17 再配布可能ファイル** を選択します。 | vc\_redist.x64\_14\_16\_27024.exe |
    | Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> | AccessDatabaseEngine\_x64.exe |
    | Microsoft .NET Framework version 4.8 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net48-offline> | ndp48-x86-x64-allos-enu.exe |
    | Microsoft .NET Framework version 4.7.2 (CLR 4.0) | <https://dotnet.microsoft.com/download/thank-you/net472-offline> | ndp472-x86-x64-allos-enu.exe |

> [!IMPORTANT]
> - Microsoft SQL Server Management Studio の設定が、対象となるコンピューターのオペレーティング システムと同じ言語であることを確認します。
> - 前の表の **"必要なファイル名"** 列に指定されている名前がインストーラ ファイルに設定されていることを確認してください。
> - **"必要なファイル名"** が異なる場合は、一部のダウンロードの名前を変更する必要があります。 これを行わないと、"Configure-PreReqs.ps1" スクリプトを実行するときにエラーが発生します。  
> - **VC++ 17 再配布可能ファイル** をダウンロードする場合、実行可能ファイルが zip ファイル内に含まれます。

#### <a name="follow-these-steps-for-each-vm-or-use-remoting-from-a-single-machine"></a>各 VM についてこれらのステップに従うか、または単一のコンピューターからリモート処理を使用します。

> [!NOTE]
> 次のセクションでは、複数の VM での実行が必要です。 このプロセスは、指定されたリモート処理スクリプトを使用して、1 台のマシン (`.\Export-Scripts.ps1` を実行するのと同じマシンなど) から必要なスクリプトを実行するオプションを提供することで、簡単に行うことができます。 利用可能な場合、リモート処理スクリプトは、PowerShell セクションの「`# If Remoting`」コメントの後に宣言されます。 リモート処理スクリプトを使用するときは、セクションの残りのスクリプトを実行する必要はありません。そのような例については、セクションの本文を参照してください。 リモート処理では、[WinRM](/windows/win32/winrm/portal) が使用され、特定のケースでは [CredSSP](/windows/win32/secauthn/credential-security-support-provider) が有効になっている必要があります。 CredSSP の有効化と無効化は、実行ごとにリモート処理モジュールによって処理されます。 資格情報の盗難の形でのセキュリティ リスクをもたらすため、CredSSP が使用されていない場合に有効のままにすることはお勧めしません。 設定が完了した場合、[CredSSP を終了処理する](#teardowncredssp) セクションを参照してください。

1. 各 infrastructure\VMs\<VMName>  フォルダーのコンテンツを対応する VM にコピーし (リモート処理スクリプトが使用されている場合は、自動的にターゲット VM にコンテンツをコピーします)、次のスクリプトを管理者として実行します。

    ```powershell
    # Install pre-req software on the VMs.

    # If Remoting, execute
    # .\Configure-PreReqs-AllVMs.ps1 -MSIFilePath <share folder path of the MSIs> -ConfigurationFilePath .\ConfigTemplate.xml

    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > 1. 再起動するように求められるたびにコンピューターを再起動します。 再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。 リモート処理の場合、すべてのマシンがオンラインに戻ったときに AllVM スクリプトを再実行します。
    > 2. リモート処理スクリプトを使用するときに、現在のユーザーが MSI の共有フォルダーにアクセス権を持っている必要があります。
    > 3. リモート処理スクリプトを使用するときに、ユーザーが AOSNoteType、MRType、および ReportServerType タイプのマシンにアクセスしていないことを確認します。 それ以外の場合は、コンピューターにログオンしているユーザーが原因で、リモート処理スクリプトはコンピュータの再起動に失敗します。

2. VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。

    ```powershell
    # If Remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    # Note: Script "Add-GMSAOnVM.ps1" is not present on BI node 
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. 次のスクリプトを実行して VM のセットアップを検証します。

    ```powershell
    # If Remoting, execute
    # .\Test-D365FOConfiguration-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml

    .\Test-D365FOConfiguration.ps1 
    ```

> [!IMPORTANT]
> リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。 [20. Tear down CredSSP](#teardowncredssp) セクションを参照してください。

### <a name="10-set-up-a-standalone-service-fabric-cluster"></a><a name="setupsfcluster"></a> 10. スタンドアロン Service Fabric クラスターの設定

1. [Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。 ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし **プロパティ** を選択してブロックを解除します。 ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。

2. ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。 **インフラストラクチャ** フォルダーが、このフォルダーにアクセスすることを確認します。

3. **インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric Cluster の ClusterConfig.json ファイルを生成します。

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```
4. クラスター コンフィギュレーションへの追加の変更は、環境に基づいて必要な場合があります。 詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。

5. 生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。

6. 上位の権限を使用して Windows PowerShell で  \<ServiceFabricStandaloneInstallerPath\>  にアクセスします。 次のコマンドを実行して ClusterConfig をテストします。

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

7. テストが成功した場合は、次のコマンドを実行してクラスターを展開します。

    ```powershell
    # If using offline (internet-disconnected) install
    # .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json -FabricRuntimePackagePath <Path to MicrosoftAzureServiceFabric.cab download>
    
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

8. クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。

    1. まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。
    2. **IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。
    3. `https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。 DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。
    4. クライアントの証明書を選択します。 **Service Fabric エクスプローラー** ページが表示されます。
    5. すべてのノードが緑で表示されていることを確認します。
    
    > [!IMPORTANT]
    > クライアント マシンが Windows Server 2016 のようなサーバー コンピューターである場合は、**Service Fabric エクスプローラー** ページにアクセスするときに IE のセキュリティ強化の構成をオフにする必要があります。
    > ウィルス対策ソフトウェアがインストールされている場合は、[Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation#environment-setup) ドキュメントのガイダンスに従って除外を設定してください。

### <a name="11-configure-lcs-connectivity-for-the-tenant"></a><a name="configurelcs"></a> 11. テナント用 LCS 接続のコンフィギュレーション

Finance + Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。 LCS から Finance + Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。

証明機関から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。

オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。

グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。 既定では、組織の Microsoft 365 にサインアップする担当者がディレクトリのグローバル管理者です。

> [!IMPORTANT]
> - テナントごとに証明書を正確に **1** 回構成する必要があります。 同じ環境のすべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。
> - Windows Server 2016 などのサーバー コンピューターでこれを実行する場合は、IE セキュリティ強化の構成を一時的にオフに必要があります。 そうしないと、Azure ログイン ウィンドウのコンテンツはブロックされます。

1. [顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。

2. 次のスクリプトを **インフラストラクチャ** フォルダーから実行して、証明書が既に登録されているかどうかを確認します。

    ```powershell
    # If you have issues downloading the Azure PowerShell Az module, run the following:
    # [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    
    Install-Module Az
    Import-Module Az
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -Test
    ```

    > [!IMPORTANT]
    > 既に AzureRM をインストールしている場合は、PowerShell 5.1 の既存の AzureRM インストールと互換性がない可能性があるのため、削除してください。 詳細については、[Azure PowerShell を AzureRM から Az に移行する](/powershell/azure/migrate-from-azurerm-to-az) を参照してください。

3. 証明書が登録されていないことをスクリプトが示している場合は、次のコマンドを実行します。

    ```powershell
    .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint'
    ```

> [!NOTE]
> ログイン アカウントに関連付けられた複数のテナントがある場合、コンテキストが正しいテナントに設定されていることを確認するために、テナント ID をパラメーターとして渡すことができます。

> ```powershell
> .\Add-CertToServicePrincipal.ps1 -CertificateThumbprint 'OnPremLocalAgent Certificate Thumbprint' -TenantId 'xxxx-xxxx-xxxx-xxxx'
> ```

### <a name="12-set-up-file-storage"></a><a name="setupfile"></a> 12.ファイル ストレージの設定

以下の SMB 3.0 ファイル共有を設定する必要があります。

- AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。
- デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。

    > [!WARNING]
    > 共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。

SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn551363(v=ws.11)#BKMK_disablesmb1) を参照してください。

> [!IMPORTANT]
> - セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。 したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。 SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。
> - 環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。 BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。

1. ファイル共有マシンで、次のコマンドを実行します。

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. \\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。

   1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
   2. **タスク**\>**新しい共有** を選択し、新しい共有を作成します。 共有に **aos-storage** と名前を付けます。
   3. **共有のキャッシュを許可** を選択したままにします。
   4. **データ アクセスを暗号化** を確認してください。
   5. OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して **変更** 許可を与えます。
   6. AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更** アクセス許可を付与します。

      >[!NOTE]
      > マシンを追加するために **オブジェクト タイプ** の下の **コンピューター** を、またはサービス アカウントを追加するために **オブジェクト タイプ** 下の **サービス アカウント** を有効にする必要がある場合があります。

3. \\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。

    1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
    2. **タスク**\>**新しい共有** を選択し、新しい共有を作成します。 共有に **エージェント** と名前を付けます。
    3. ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。

    ```PowerShell
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

### <a name="13-set-up-sql-server"></a><a name="setupsql"></a> 13. SQL Server の設定

1. 高可用性を備えた SQL Server 2016 SP2 をインストールします。 (SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。 高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)

    > [!IMPORTANT]
    > [SQL Server および Windows 認証モード](/sql/database-engine/configure-windows/change-server-authentication-mode) を有効にする必要があります。

    高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。 データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。

    > [!NOTE]
    > Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。

2. ドメイン ユーザーまたはグループ管理サービス アカウントとして SQL サービスを実行します。
3. Finance + Operations 向けに SQL Server を構成するために証明機関から SSL 証明書を取得します。 テストの目的で、自己署名証明書または AD CS 証明書を作成して使用することができます。 次の例にあるコンピューター名とドメイン名を置き換える必要があります。

    **Always-On SQL インスタンスの証明書**

    Always-On 用の証明書のテストを設定する場合は、次の **リモート処理** スクリプトを使用します。 これにより、次の **手動** スクリプトが実行され、手順 **a ～ e** が実行されます。

    1. 自己署名証明書

        ```powershell
        .\New-SelfSigned-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
        ```

    1. AD CS 証明書

        ```powershell
        .\New-ADCS-SQLCert-AllVMs.ps1 -SqlMachineNames SQL1,SQL2 -SqlListenerName SQL-LS -ProtectTo CONTOSO\dynuser
        ```

    **SQL Server を使用した Always-On SQL または Windows Serverフェールオーバー クラスタリングの手動自己署名ステップ** 
        
    SQL クラスターの各ノードに対して、次の手順を実行します。 

    1. 次の PowerShell スクリプトを、SQL Server Always-On レプリカごとに実行します。

    ```powershell
    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider' -CertStoreLocation "cert:\LocalMachine\My" -KeyAlgorithm "RSA" -HashAlgorithm "sha256" -KeyLength 2048
    ```

    2. SQL サービスを実行するために使用されるアカウントに証明書のアクセス許可を付与します。 
        1. \[コンピューター証明書の管理\] (**certlm.msc**) を開きます。
        2. 作成した証明書を右クリックし、**タスク** \> **プライベート キーの管理** をクリックします。
        3. SQL Server サービス アカウントを追加し、読み取りアクセスを許可します。
    3. Microsoft SQL Server Configuration Manager で **ForceEncryption** と新しい **証明書** を有効にします。
        1. **SQL Server 構成マネージャー** で、**SQL Server ネットワークの構成** を展開し、**サーバーのインスタンスのプロトコル** を右クリックしてから、**プロパティ** を選択します。
        2. **プロトコル** ダイアログ ボックスの **証明書** タブで、**証明書** ボックスのドロップダウン メニューから目的の証明書を選択します。
        3. **プロパティ** ダイアログ ボックスの **フラグ** タブにある **ForceEncryption** ボックスで、**はい** を選択します。
        4. **OK** を選択して保存します。
    4. 各 SQL クラスター ノードから証明書 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。 Always-On クラスターには少なくとも 2 つの証明書がありますが、追加のレプリカがある場合はそれ以上の証明書が必要になる場合があります。 
    5. SQL Server サービスを再起動します。
   > [!NOTE] 
   > 詳細は、[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console)を参照してください。



> [!IMPORTANT]
> リモート処理を使用していた場合は、設定が完了するとクリーンアップ手順を実行します。 詳細については、[20. CredSSP を終章処理する](#teardowncredssp) セクションを参照してください。

### <a name="14-configure-the-databases"></a><a name="configuredb"></a> 14. データベースのコンフィギュレーション

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。

2. ダッシュボードで、**共有アセット ライブラリ** タイルを選択します。

3. **モデル** タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。

    | リリース | デモ データ |
    |-------|------|
    | オンプレミスの一般提供 (GA) リリース | Dynamics 365 for Operations オンプレミス - デモ データ |
    | オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース | Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 11 デモ データ |
    | オンプレミスのプラットフォーム更新プログラム 2018 年 3 月 12 日リリース | Dynamics 365 for Operations オンプレミス Enterprise Edition - 更新プログラム 12 デモ データ |

4. zip ファイルには空のデモデータ .bak ファイルが含まれています。 必要に応じて、.bak ファイルを選択します。 たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。

5. infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。
    1. データベース名。
    2. db ファイルとログ設定。 dbの設定は、指定された既定値以上にする必要があります。
    3. LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。 Finance + Operations データベースの既定の名前は AXDB です。

   > [!WARNING]
   > - SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。
   > 
   > - 同じ名前のデータベースが存在する場合は、データベースが再利用されます。

6. **インフラストラクチャ** フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。

#### <a name="configure-the-orchestratordata-database"></a>OrchestratorData データベースのコンフィギュレーション

1. 次のスクリプトを実行します。

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   スクリプトは、次の操作を行います。
  
   - **OrchestratorData** という名前の空のデータベースを作成します。 このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。
   - データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。

#### <a name="configure-the-finance--operations-database"></a>Finance + Operations データベースの構成

1. 次のスクリプトを実行します。

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName AOS
   ```

   **Initialize-Database.ps1** スクリプトは、次の操作を行います。

   1. 指定されたバックアップ ファイルからデータベースを復元します。
   2. SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。
   3. AXDB の次の表に基づくデータベース ロールにユーザーをマップします。

      | ユーザー            | 種類    | データベース ロール |
      |-----------------|---------|---------------|
      | svc-AXSF$       | gMSA    | db\_owner     |
      | svc-LocalAgent$ | gMSA    | db\_owner     |
      | svc-FRPS$       | gMSA    | db\_owner     |
      | svc-FRAS$       | gMSA    | db\_owner     |
      | axdbadmin       | SqlUser | db\_owner     |


   4. TempDB の次の表に基づくデータベース ロールにユーザーをマップします。

      | ユーザー            | 種類    | データベース ロール |
      |-----------------|---------|---------------|
      | svc-AXSF$       | gMSA    | db_datareader, db_datawriter, db_ddladmin     |
      | axdbadmin       | SqlUser | db_datareader, db_datawriter, db_ddladmin     |

   **Configure-Database.ps1** スクリプトは、次の操作を行います。

    1. READ_COMMITTED_SNAPSHOT ON を設定
    2. ALLOW_SNAPSHOT_ISOLATION ON を設定
    3. 指定したデータベース ファイルとログの設定を設定
    4. サーバー状態の表示を axdbadmin に付与
    5. イベント セッション変更の権限を axdbadmin に付与
    6. サーバー状態の表示を [contoso\svc AXSF$] に付与
    7. イベント セッションの変更権限を [contoso\svc-AXSF$] に付与

2. データベース ユーザーをリセットするには、次のコマンドを実行します。

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

#### <a name="configure-the-financial-reporting-database"></a>財務レポート データベースのコンフィギュレーション

1. 次のスクリプトを実行します。

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName MR
   ```

   スクリプトは、次の操作を行います。
   1. **FinancialReporting** という名前の空のデータベースを作成します。
   2. 次の表に基づくデータベース ロールにユーザーをマップします。

      | ユーザー            | 種類 | データベース ロール |
      |-----------------|------|---------------|
      | svc-LocalAgent$ | gMSA | db\_owner     |
      | svc-FRPS$       | gMSA | db\_owner     |
      | svc-FRAS$       | gMSA | db\_owner     |

### <a name="15-encrypt-credentials"></a><a name="encryptcred"></a> 15. 資格情報の暗号化

1. 任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。
2. 現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。
3. 次のようにして、Credentials.json ファイルを作成します。

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

    - **AccountPassword** は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。
    - **SqlUser** は、Finance + Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。

4. .json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。
5. 暗号化された値で Credentials.json ファイルを更新します。

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```
    > [!IMPORTANT]
    > *Invoke-ServiceFabricEncryptText* を起動する前に、[Microsoft Azure Service Fabric SDK](/azure/service-fabric/service-fabric-get-started#sdk-installation-only) をインストールする必要があります。
    > Azure Service Fabric SDK をインストールした後で、"Invoke-ServiceFabricEncryptText は認識されないコマンドです" というエラーが発生した場合は、コンピューターを再起動して再試行してください。

    > [!WARNING]
    > すべての **ServiceFabricEncryptText** コマンドの起動が完了したら、Windows PowerShell の履歴を削除することを忘れないでください。 それ以外の場合は、暗号化されていない資格情報が表示されます。

### <a name="16-set-up-ssis"></a><a name="setupssis"></a> 16. SSIS の設定

データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。 各 AOS 仮想マシン上で、次の手順を実行します。

1. マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。
2. **機能の選択** ウィンドウの **機能** ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。
3. セットアップを完了し、インストールが正常に完了したことを確認します。

詳細については、[統合サービスのインストール](/sql/integration-services/install-windows/install-integration-services) を参照してください。

### <a name="17-set-up-ssrs"></a><a name="setupssrs"></a> 17. SSRS の設定

1. 開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。
2. [オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。
    > [!IMPORTANT]
    > SSRS のインストール時にデータベース エンジンをインストールする必要があります。

### <a name="18-configure-ad-fs"></a><a name="configureadfs"></a>18. AD FS のコンフィギュレーション

この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。 AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。

Finance + Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。 以下の Windows PowerShell コマンドを、AD FS ロール サービスがインストールされているマシン上で実行する必要があります。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。 たとえば、ユーザーには、ドメイン管理者アカウントが必要です。 複雑な AD FS シナリオでは、ドメイン管理者に問い合わせてください。

1. AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。

   このコマンドは、Finance + Operations クライアントの **ユーザー** ページ (**システム管理 > ユーザー > ユーザー**) で **ユーザーをインポート** オプションを使用した新しいユーザーの追加に関連しています。

    ```PowerShell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. 混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。 WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。

   このコマンドは、Finance + Operations クライアントへのログイン時のフォーム認証の使用に関連しています。 シングル サインインなどの他のオプションはサポートされていません。

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。

   このコマンドは、電子メール要求の設定に関連しています。 変換ルールなど、追加の設定が必要な他のオプションが使用可能な場合があります。

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

AD FS が認証を交換するために Finance + Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。 設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。 Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。 次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。 (たとえば、管理者アカウントを使用します。)

スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。 後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。 クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises** を開き、ネイティブ アプリケーションでクライアント ID を見つけます。

> [!NOTE]
> 以前に構成した AD FS サーバーを別の環境で再利用する方法については、[複数の環境に同じ AD FS インスタンスを再使用する](./onprem-reuseadfs.md) を参照してください。

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ。](./media/OPSetup_05_ApplicatioGroupProperties.png)

最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。 このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。 サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。 このステップについては、「AD FS 展開ガイド」で説明されています。リモーティングを使用している場合は、次のスクリプトを使用して、Service Fabric クラスター内のすべてのノードに証明書をインストールできます。

```powershell
# If remoting, execute
.\Install-ADFSCert-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。

これで、インフラストラクチャの設定を完了しました。 次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance + Operations 環境を配置する方法について説明します。

### <a name="19-configure-a-connector-and-install-an-on-premises-local-agent"></a><a name="configureconnector"></a> 19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール

1. [LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。
2. ハンバーガー メニューで、**プロジェクト設定** を選択します。

    ![プロジェクト設定コマンドです。](./media/OPSetup_06_ProjectSettings.png)

3. **オンプレミス コネクタ** を選択します。
4. 新しいコネクタを作成するには、**追加** を選択します。 
5. **ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードします。](./media/OPSetup_07_DownloadAgentInstaller.png)
    
6. zip ファイルがブロックされていないことを確認します。 ファイルを右クリックし、**プロパティ** を選択します。 ダイアログ ボックスで **ブロック解除** を選択します。
7. **OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。
8. **構成エージェント** タブで、コンフィギュレーションの設定を入力します。 必要な値を取得するには、そのマシンと構成ファイルにアクセスできる任意のマシンで次のスクリプトを実行します。

    ```powershell
    .\Get-AgentConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

9. コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン。](./media/OPSetup_08_DownloadConfigurations.png)

10. localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。
11. **コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。

12. ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。
13. **設定の検証** タブで、**メッセージ エージェント** を選択して、ローカル エージェントへの LCS 接続をテストします。 接続が正常に確立されると、ページは下図のようになります。

    ![エージェントを検証します。](./media/ValidateAgent.PNG)

### <a name="20-tear-down-credssp-if-remoting-was-used"></a><a name="teardowncredssp"></a> 20. リモート処理が使用された場合、CredSSP を終了処理する

セットアップ中にリモート処理スクリプトのいずれかが使用された場合は、セットアップ プロセスの中断時または完了時に、次のスクリプトを実行してください。

```powershell
.\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
```

前のリモート PowerShell ウィンドウが誤って終了し、CredSSP が有効にまったままである場合、スクリプトにより、コンフィギュレーション ファイルで指定されたすべてのコンピューター上で無効にされます。

### <a name="21-deploy-your-finance--operations-environment-from-lcs"></a><a name="deploy"></a> 21. LCS から Finance + Operations 環境を配置する

1. LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス** に移動してから **構成** を選択します。 必要な値を取得するには、ADFS および DNS サーバー設定にアクセスする必要があるプライマリ ドメイン コントローラ VM で次のスクリプトを実行します。

    ```powershell
    .\Get-DeploymentSettings.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. 新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。

    ![環境を配置します。](./media/Deploy.png)

3. 既存のプラットフォーム更新プログラム 8 またはプラットフォーム更新プログラム 11 を展開する場合: 
    - ローカル エージェントを更新します。 詳細については、[ローカル エージェントの更新](../lifecycle-services/update-local-agent.md) を参照してください。
    - LCS からローカル エージェントを検証します。
    - [環境を再構成して新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md) の手順を実行している間に、プラットフォーム更新 12 を配置します。
4. LCS は準備フェーズ中に環境の Service Fabric アプリケーション パッケージを組み立てます。 配置を開始するローカル エージェントにメッセージを送信します。 下記のように、**準備中** ステータスが表示されます。

    ![準備フェーズ。](./media/Preparing.png)

    以下に示すような環境の詳細ページに移動するには、**完全な詳細** をクリックします。

    ![環境の詳細ページ。](./media/Details_Preparing.png)

5. ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。 表示されているとおりに、配置の開始がしたときに、ステータスは **配置** に変更します。

    ![ステータスを展開に変更します。](./media/Deploying.png)

    ![環境を展開しています。](./media/Details_Deploying.png)

    展開に失敗した場合、LCS のお客様の環境では、**再設定** ボタンは次のように利用可能になります。 基になる問題を修正し、**再コンフィギュレーション** をクリックして、任意のコンフィギュレーションの変更を更新し、**配置** をクリックして配置を再試行します。

    ![再構成ボタンが使用可能になります。](./media/Failed.png)

    再構成の方法の詳細については、[環境を再構成して、新しいプラットフォームまたはトポロジを採用する](../lifecycle-services/reconfigure-environment.md) のトピックを参照してください。 次の図は、正常な配置を示します。

    ![環境が正常に配置されました。](./media/Deployed.png)

### <a name="22-connect-to-your-finance--operations-environment"></a><a name="connect"></a> 22. Finance + Operations 環境への接続
ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのトピックの[ドメイン名と DNS ゾーンの計画](#plandomain) セクションで定義したドメイン名です。

## <a name="additional-resources"></a>追加リソース
- [オンプレミス配置への更新プログラムの適用](apply-updates-on-premises.md)
- [オンプレミス環境の再配置](redeploy-on-prem.md)
- [ドキュメント管理のコンフィギュレーション](../../fin-ops/organization-administration/configure-document-management.md)
- [電子申告 (ER) コンフィギュレーションのインポート](../analytics/electronic-reporting-import-ger-configurations.md)
- [オンプレミス配置でのドキュメントの生成、発行、印刷](../analytics/printing-capabilities-on-premises.md)
- [オンプレミス環境用プロキシの構成](onprem-reverseproxy.md)
- [Finance and Operations アプリのテクニカル サポートの設定](../lifecycle-services/support-experience.md)
- [クライアントのインターネット接続](../user-interface/client-disconnected.md)

## <a name="known-issues"></a>既知の問題

### <a name="error-key-does-not-exist-when-running-the-new-d365fogmsaaccounts-cmdlet"></a>New-D365FOGMSAAccounts cmdlet を実行した際のエラー、「キーが存在しません」
ドメインでグループ管理サービス アカウント パスワードを初めて作成し生成する場合は、最初に **キー配分サービス KDS ルート キー** を作成する必要があります。 詳細については、[キー配分サービス KDS ルート キーの作成](/windows-server/security/group-managed-service-accounts/create-the-key-distribution-services-kds-root-key)を参照してください。

### <a name="error-the-winrm-client-cannot-process-the-request-when-running-the-remoting-script-configure-prereqs-allvms-cmdlet"></a>リモート処理スクリプト Configure-Prereqs-AllVms cmdlet を実行した際のエラー、「WinRM クライアントは要求を処理できません」
Service Fabric Cluster のすべてのマシンでコンピューター ポリシー **新しい資格情報委任を許可** を有効にするには、エラー メッセージの指示に従う必要があります。

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-config-prereqs-allvms-cmdlet"></a>エラー、「'テスト'パラメータでの引数変換を処理できません」 Config-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません
このエラーを回避するには、**インフラストラクチャ** フォルダーにある Config-Prereqs-AllVms.ps1 の 56 行目の「-Test:$Test」を削除します。

### <a name="error-not-process-argument-transformation-on-parameter-test-cannot-convert-value-systemstring-to-type-systemmanagementautomationswitchparameter-when-running-the-complete-prereqs-allvms-cmdlet"></a>エラー、「'テスト'パラメータでの引数変換を処理できません」 Complete-Prereqs-AllVms cmdlet 実行時、値 "System.String" を、タイプ "System.Management.Automation.SwitchParameter" に変換することはできません
このエラーを回避するには、**インフラストラクチャ** フォルダーにある Complete-Prereqs-AllVms.ps1 の 56、61、66 行目の「-Test:$Test」を削除します。

### <a name="error-install-windowsfeature-the-request-to-add-or-remove-features-on-the-specified-server-failed-when-running-configure-prereqs-on-mrtype-and-reportservertyoe-servers"></a>MRType および ReportServerTyoe サーバーで Configure-Prereqs を実行した際のエラー、「Install-WindowsFeature: 指定されたサーバーへの機能の追加または削除の要求に失敗しました」
.NET Framework 3.5 には、MRType および ReportServerType サーバーが必要です。 ただし、既定では .NET Framework 3.5 ソース ファイルは Windows Server 2016 インストールに含まれていません。 このエラーを回避するには、サーバー マネージャーによって新機能を手動で追加するときに **ソース** オプションを使用してインストールし、ソース ファイルを指定します。

### <a name="error-msis7628-scope-names-should-be-a-valid-scope-description-name-in-ad-fs-configuration-when-running-the-publish-adfsapplicationgroup-cmdlet"></a>Publish-ADFSApplicationGroup cmdlet を実行した際のエラー、「MSIS7628: スコープ名は AD FS コンフィギュレーションで有効なスコープ説明でなければなりません」
このエラーは D365FO-OP-ADFSApplicationGroup で必要とされる OpenID スコープ **allatclaims** が原因で表示されます。ただし、一部の Windows Server 2016 インストールでは表示されないことがあります。 このエラーを回避するには、AD FS Management\Service\Scope Descriptions を使用してスコープの説明 **allatclaims** を追加します。

### <a name="error-admin0077-access-control-policy-does-not-exist-permit-everyone-when-running-the-publish-adfsapplicationgroup-cmdlet"></a>Publish-ADFSApplicationGroup cmdletを実行した際のエラー、「ADMIN0077: アクセス制御ポリシーが存在しません: すべてのユーザーを許可」
英語以外のバージョンの Windows Server 2016 と共に AD FS をインストールすると、すべてのユーザーのアクセス許可のアクセス許可ポリシーがローカル言語で作成されます。 AccessControlPolicyName パラメーターを指定することによりコマンドレットを呼び出します:  

```powershell
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com' -AccessControlPolicyName '<Permit everyone access control policy in your language>'. 
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
