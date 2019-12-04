---
title: オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)
description: このトピックでは、オンプレミス環境の計画、設定、および展開方法について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 9edb9c924737565959d0d13b8d6818f74b32a3b7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770933"
---
# <a name="set-up-and-deploy-on-premises-environments-platform-updates-8-and-11"></a>オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 8 および 11)

[!include [banner](../includes/banner.md)]

このトピックでは、展開を計画し、インフラストラクチャを設定し、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (オンプレミス)、プラットフォーム更新プログラム 8 および 11 を展開する方法について説明します。

> [!IMPORTANT]
> このトピックは、プラットフォーム更新プログラム 8 および 11 にオンプレミス環境を展開する場合にのみ適用されます。 プラットフォーム更新 12 への展開に関する詳細については、[オンプレミス環境の設定と配置 (プラットフォーム更新 12 以降)](setup-deploy-on-premises-pu12.md) を参照してください。

## <a name="finance-and-operations-components"></a>Finance and Operations のコンポーネント

Finance and Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。

- Application Object Server (AOS)
- ビジネス インテリジェンス (BI)
- 財務レポート/管理レポーター

これらのコンポーネントは、次のシステム ソフトウェアによって異なります。

- Microsoft Windows サーバー 2016
- 以下の特徴を有する Microsoft SQL Server2016 SP1:
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
  >   - [Active Directory 機能レベルとは](https://technet.microsoft.com/library/cc787290(v=ws.10).aspx)
  >   - [Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。 配置する前に、[エンタープライズ契約](https://www.microsoft.com/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。 LCS からのみ配置を開始することができます。 LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。

## <a name="authentication"></a>認証

オンプレミス アプリケーションは AD FS で動作します。 LCS と対話するには、Azure Active Directory (AAD) も設定する必要があります。 配置を完了し LCS ローカル エージェントを構成するには、AAD が必要です。

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations は スタンドアロン Service Fabric を使用します。 詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。

Finance and Operations の設定は、Service Fabric (SF) 内に一連のアプリケーションを配置します。 展開中に、クラスター内の各ノードは、次のいずれかのノード タイプを持つように構成によって定義されます。

- **AOSNodeType**: アプリケーション オブジェクト サーバー (ビジネス ロジック) をホストします。
- **OrchestratorType**: Service Fabric のプライマリ ノードとして機能し、配置およびサービスロジックをホストします。
- **ReportServerType**: SSRS およびレポート ロジックをホストします。
- **MRType**: 管理レポート ロジックをホストします。

## <a name="infrastructure"></a>インフラストラクチャ

Finance and Operations は、Windows Server に基づく Hyper-V 仮想化環境で作業するよう設計されています。

 > [!WARNING]
 > Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Finance and Operations のオンプレミス配置。

ハードウェア構成には、次のコンポーネントが含まれます。

- Windows Server 2016 仮想マシン (VM) に基づく Standalone Service Fabric Cluster
- Microsoft SQL Server (Clustered SQL と Always-On の両方がサポートされています)
- 認証のための AD FS
- ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有
- オプション: Microsoft Office Server 2017

詳細については、[オンプレミス配置のためのシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) およびサイジングのガイドラインを参照してください。

### <a name="hardware-layout"></a>ハードウェア レイアウト

[オンプレミス環境のハードウェア サイジング要件](../../fin-ops/get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric Cluster を計画します。 Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

次のテーブルは、ハードウェア レイアウトの例を示しています。 この例は、設定を説明するためにこのトピック全体で使用されています。

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
- SQL Server 2016 SP1 は SSRS コンピューターにインストールされている必要があります。
- SQL Server Reporting Services 2016 は、SSRS コンピューターに**ネイティブ** モードでインストールする必要があります。

次の必須ソフトウェアは、LCS からダウンロードされたインフラストラクチャ セットアップ スクリプトによって VM にインストールされます。

| ノード タイプ | コンポーネント | 詳細情報 |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC ドライバー | <https://www.microsoft.com/download/details.aspx?id=53339> |
| AOS       | Microsoft .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| AOS       | Microsoft .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| AOS       | インターネット インフォメーション サービス (IIS) | **Windows の機能:** WAS、WAS-Process-Model、WAS-NET-Environment、WAS-Config-APIs、Web-Server、Web-WebServer、Web-Security、Web-Filtering、Web-App-Dev、Web-Net-Ext、Web-Mgmt-Tools、Web-Mgmt-Console |
| AOS       | SQL Server Management Studio 17.2 | <https://go.microsoft.com/fwlink/?linkid=854085> |
| AOS       | Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| AOS       | Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> |
| BI        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| BI        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| BI        | SQL Server Management Studio 17.2 | <https://go.microsoft.com/fwlink/?linkid=854085> |
| MR        | .NET Framework version 2.0–3.5 (CLR 2.0) | **Windows の機能:** NET-Framework-Features、NET-Framework-Core、NET-HTTP-Activation、NET-Non-HTTP-Activ |
| MR        | .NET Framework version 4.0–4.6 (CLR 4.0) | **Windows の機能:** NET-Framework-45-Features、NET-Framework-45-Core、NET-Framework-45-ASPNET、NET-WCF-Services45、NET-WCF-TCP-PortSharing45 |
| MR        | Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |

### <a name="overview"></a>概要

Finance and Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。

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
20. [LCS から Finance and Operations (オンプレミス) 環境を配置する](#deploy)
21. [Finance and Operations (オンプレミス) 環境に接続する](#connect)

### <a name="plandomain"></a> 1. ドメイン名と DNS ゾーンの計画

AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。 このようにして、外部アクセスが必要な場合は、ネットワークの外部からインストールにアクセスできます。

たとえば、会社のドメインが contoso.com の場合、Finance and Operations (オンプレミス) は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。

- AOS の機械の場合 ax.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com

### <a name="plancert"></a> 2. 証明書の計画と取得

Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。 プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。 ドメインが [Active Directory 証明書サービス](https://technet.microsoft.com/library/cc772393(v=ws.10).aspx) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。 証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。

自己署名証明書は、テスト目的でのみ使用できます。 便宜上、セットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれています。 先に述べたように、これらの証明書はテスト目的でのみ使用できます。

| 目的                                      | 説明 | 追加条件 |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL 証明書                   | この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。 | 証明書の場合、ドメイン名は、SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。 たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.onprem.contoso.com です。 |
| Service Fabric Server 証明書            | <p>この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。</p> <p> この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。</p> | <p>ドメインの SSL ワイルドカード証明書を使用することができます。 たとえば、\*.contoso.com です。</p><p><strong>注記:</strong> ワイルド カード証明書は、発行先となるドメインの最初のレベル サブドメインのみをセキュリティ保護できるようにします。</p><p>この例では、Service Fabric ドメインが sf.d365ffo.onprem.contoso.com であるため、証明書にサブジェクト代替名 (SAN) としてこれを含める必要があります。 証明機関と連携して、追加の SAN を取得する必要があります。</p> |
| Service Fabric Client 証明書            | この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。 | |
| 証明書の暗号化                     | この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。  | <p> 証明書は、プロバイダー **Microsoft Enhanced Cryptographic Provider v1.0** を使用して作成する必要があります。 </p><p>証明書キーの使用にはデータ暗号化 (10) が含まれている必要があり、サーバー認証またはクライアント認証は含めないでください。</p><p>詳細については、[Service Fabric アプリケーションでの機密情報の管理](/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</p> |
| AOS SSL 証明書                          | <p>この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。 また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</p><p>Service Fabric サーバー証明書として使用するのと同じワイルドカード証明書を使用することができます。</p> | <p>この例では、ドメイン名 ax.d365ffo.onprem.contoso.com を、Service Fabric Server 証明書としてサブジェクト代替名 (SAN) に追加する必要があります。</p> |
| セッション認証証明書           | この証明書は、AOS がユーザーのセッション情報を保護するために使用します。 | この証明書は、LCS からの展開時に使用されるファイル共有証明書です。 |
| データの暗号化証明書 | これらの証明書は、機密情報を暗号化するために AOS によって使用されます。  | これはプロバイダー **Microsoft Enhanced RSA および AES Cryptographic Provider** を使用して作成する必要があります。 |
| データ署名の証明書 | これらの証明書は、機密情報を暗号化するために AOS によって使用されます。  | これは、データ暗号化証明書とは別のもので、プロバイダー**Microsoft の拡張された RSA および AES 暗号化プロバイダー**を使用して作成する必要があります。 |
| 財務報告クライアント証明書       | この証明書は、財務報告サービスと AOS 間の通信を保護するのに役立ちます。   この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。 |  |
| 報告証明書                        | この証明書を使用して、SSRS と AOS 間の通信を保護します。| **財務報告クライアント証明書を再利用しないでください。** |
| オンプレミス ローカル エージェント証明書           | <p>この証明書は、オンプレミスと LCS でホストされているローカル エージェント間の通信を保護するのに役立ちます。</p><p>この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</p><p><strong>注記:</strong> テナントにはオンプレミス ローカル エージェント証明書が 1 つだけ必要です。</p>| |

以下は、AOS SSL 証明書と組み合わせた Service Fabric Server 証明書の例です。

#### <a name="subject-name"></a>件名

```
CN = *.d365ffo.onprem.contoso.com
```

#### <a name="subject-alternative-names"></a>件名の代替名

```
DNS Name=ax.d365ffo.onprem.contoso.com
DNS Name=sf.d365ffo.onprem.contoso.com
DNS Name=*.d365ffo.onprem.contoso.com
```

### <a name="plansvcacct"></a> 3. ユーザーとサービス アカウントの計画

Finance and Operations (オンプレミス) を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。 サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。 次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。

| ユーザー アカウント                                            | 種類           | 目的 | ユーザー名 |
|---------------------------------------------------------|----------------|---------|-----------|
| 財務レポート アプリケーション サービス アカウント         | gMSA           |         | Contoso\\svc-FRAS$ |
| 財務レポート プロセス サービス アカウント             | gMSA           |         | Contoso\\svc-FRPS$ |
| 財務レポート クリック ワンス デザイナー サービス アカウント | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS サービス アカウント                                     | gMSA           | このユーザーは、将来校正するために作成する必要があります。 今後のリリースでは、AOS を gMSA と連携させる予定です。 このユーザーを設定時に作成することで、gMSA へのシームレスな移行を確実にすることができます。 | Contoso\\svc-AXSF$ |
| AOS サービス アカウント                                     | ドメイン アカウント | AOS は、一般提供 (GA) リリースでこのユーザーを使用します。 | Contoso\\AXServiceUser |
| AOS SQL DB 管理者ユーザー                                   | SQL ユーザー       | Finance and Operations は、このユーザーを使用して SQL\* を認証します。 このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。 | AXDBAdmin |
| ローカル配置エージェント サービス アカウント                  | gMSA           | このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。 | Contoso\\Svc-LocalAgent$ |

\* SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。

### <a name="createdns"></a> 4. DNS ゾーンの作成とレコードの追加

DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。 AOS ホスト名と Service Fabric クラスタの DNS 正引き検索ゾーンと A レコードを作成します。 この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。

- AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com

#### <a name="add-a-dns-zone"></a>DNS ゾーンの追加

DNS ゾーンを追加するには、次の手順を実行します。

1. ドメイン コントローラー マシンにサインインし、**開始** を選択し、**dnsmgmt.msc** と入力して DNS マネージャーを起動します。
2. ドメイン コントローラー名を右クリックし、**新しいゾーン** \> **次へ** の順に選択します。
3. **プライマリ ゾーン** を選択します。
4. **Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメイン コントローラーの場合にのみ使用可能)** のチェック ボックスが選択されたままの状態で、**次へ**を選択します。
5. **このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して** を選択し、**次へ** を選択します。
6. **前方参照ゾーン** を選択し、**次へ** を選択します。
7. 設定するゾーン名を入力し、**次へ**をクリックします。 たとえば、**d365ffo.onprem.contoso.com** と入力します。
8. **動的更新を許可しない** を選択し、**次へ** を選択します。

#### <a name="set-up-an-a-record-for-aos"></a>AOS の A レコードを設定する

新しい DNS ゾーンで、**AOSNodeType** タイプの Service Fabric クラスター ノード**ごと**に、**ax.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを右クリックして、**新しいホスト** を選択します。
2. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**10.179.108.12** を IP アドレスとして入力します。) **ホストの追加**を選択します。

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Orchestrator の A レコードを設定する

新しい DNS ゾーンで、**OrchestratorType** タイプの Service Fabric クラスター ノード**ごと**に、**sf.d365ffo.onprem.contoso.com** という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを右クリックして、**新しいホスト** を選択します。
2. Service Fabric ノードの 名前および IP アドレスを入力します。 (たとえば、**10.179.108.15** を IP アドレスとして入力します。) **ホストの追加**を選択します。

### <a name="joindomain"></a> 5. VM のドメインへの参加

各 VM をドメインに参加させるには、[Windows Server 2016 を Active Directory ドメインに参加させる方法](https://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) の各手順を完了します。 または、次の Windows PowerShell スクリプトを使用します。

```powershell
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
```

> [!IMPORTANT]
> ドメインにそれらを結合させた後、VM を再起動する必要があります。

VM をドメインに参加させた後、ローカル管理者グループに AOS サービス アカウント **Contoso\svc-AXSF$** と **Contoso\AXServiceUser** を追加します。 詳細については、「[ローカル グループへのメンバーの追加](https://technet.microsoft.com/library/cc772524(v=ws.11).aspx)」を参照してください。

### <a name="downloadscripts"></a> 6. LCS からのセットアップ スクリプトのダウンロード

> [!IMPORTANT]
> スクリプトは、オンプレミス インフラストラクチャと同じドメイン内のコンピューターから実行する必要があります。

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。
2. ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。
3. **モデル**タブの、グリッドで、**Dynamics 365 for Operations オンプレミス - 配置スクリプト - 最新**行を選択します。
4. **バージョン** ボタンをクリックし、**バージョン 1** を選択します。
5. zip ファイルを右クリックし、**プロパティ** を選択します。 ダイアログ ボックスで、**ブロック解除**チェック ボックスをオンにします。
6. ZIP ファイルをスクリプトの実行に使用するマシンにコピーします。
7. **infrastructure** という名前のフォルダーにファイルを解凍します。

> [!IMPORTANT]
> このフォルダーの ConfigTemplate.xml にすべての編集を加える必要があります。

### <a name="describeconfig"></a> 7. コンフィギュレーションの記述

インフラストラクチャの設定 スクリプトは、次のコンフィギュレーション ファイルを使用して設定を実行します。
- infrastructure\ConfigTemplate.xml
- infrastructure\D365FO-OP\NodeTopologyDefintion.xml
- infrastructure\D365FO-OP\DatabaseTopologyDefintion.xml

**infrastructure\ConfigTemplate.xml** で説明します。
- アプリケーションが動作するために必要なサービス アカウント
- 通信を保護するために必要な証明書
- データベース コンフィギュレーション
- Service Fabric クラスター構成

各 Service Fabric ノード タイプについて、**infrastructure\D365FO-OP\NodeTopologyDefinition.xml** で説明します。

- 各ノード タイプとアプリケーション、ドメインとサービス アカウント、および証明書間のマッピング。
- UAC を有効にするかどうか
- Windows の機能とシステム ソフトウェアの前提条件
- 厳密な名前の検証を有効にするかどうか
- 開くファイアウォール ポートのリスト

各データベースについて、**infrastructure\D365FO-OP\DatabaseTopologyDefinition.xml** で説明します。

- DB 設定
- ユーザーとロールの間のマッピング

#### <a name="create-gmsa-and-domain-user-accounts"></a>gMSA およびドメイン ユーザー アカウントを作成する

1. **インフラストラクチャ** フォルダーに展開したインフラストラクチャ スクリプトがあるマシンに移動します。
2. **インフラストラクチャ**フォルダーをドメイン コントローラー マシンにコピーします。
3. 管理者特権モードで Windows PowerShell を起動し、ディレクトリを **infrastructure** フォルダーに変更して、次のコマンドを実行します。

    ```powershell
    Import-Module .\D365FO-OP\D365FO-OP.psd1
    New-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

4. アカウントまたはマシンを変更する必要がある場合は、元の **インフラストラクチャ** フォルダーの ConfigTemplate.xml ファイルを更新し、このマシンにコピーしてから次のスクリプトを実行します。

    ```powershell
    Update-D365FOGMSAAccounts -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="configurecert"></a> 8. 証明書のコンフィギュレーション

1. **インフラストラクチャ** フォルダーがあるマシンに移動します。
2. 自己署名証明書を生成する必要がある場合は、次のコマンドを実行します。 スクリプトは証明書を作成し、それらをコンピューターの「CurrentUser\My certificate store」に格納し、XML ファイルのサムプリントを更新します。

    ```powershell
    # Create self-signed certs
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    証明書を再利用する必要があるため、証明書を生成する必要がない場合は、**generateSelfSignedCert** タグを **false** に設定します。

3. 既に生成されている SSL 証明書を使用している場合は、証明書生成をスキップし、configTemplate.xml ファイルの拇印を更新します。 証明書は CurrentUser\My ストアにインストールする必要があり、その秘密キーはエクスポート可能でなければなりません。

> [!WARNING]
> 存在する場合に特定するのが難しい先頭の印刷不可能な特殊文字のため、証明書マネージャーは拇印をコピーするために使用しないでください。 非印刷可能な特殊文字が存在する場合、**X509 証明書が有効ではない**というエラーが表示されます。 拇印を取得するには、PowerShell コマンドの結果を参照するか、PowerShell で次のコマンドを実行します。
> ```powershell
> dir cert:\CurrentUser\My
> dir cert:\LocalMachine\My
> dir cert:\LocalMachine\Root
> ```

4. 各証明書の **ProtectTo** でユーザーまたはグループのセミコロンで区切られた一覧を指定します。 **ProtectTo** タグで指定された Active Directory ユーザーとグループのみに、スクリプトを使用してエクスポートされる証明書をインポートするアクセス許可があります。 エクスポートした証明書を保護するため、スクリプトによりパスワードがサポートされていません。

5. 証明書を .pfx ファイルにエクスポートします。

    ```powershell
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will be written to infrastructure\Certs folder.
    .\Export-PfxFiles.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupvms"></a> 9. VM の設定
1. 各 VM で実行する必要があるスクリプトをエクスポートします。

    ```powershell
    # Exports the script files to be execute on each VM into a directory VMs\<VMName>.
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

2. 次の Microsoft Windows Installers (MSI) を全ての VM でアクセス可能なファイル共有にダウンロードします。

| コンポーネント | リンクのダウンロード |
|-----------|---------------|
| SNAC – ODBC ドライバー | <https://www.microsoft.com/download/details.aspx?id=53339> |
| Microsoft SQL ServerManagement Studio 17.2 | <https://go.microsoft.com/fwlink/?linkid=854085> |
| Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | <https://support.microsoft.com/help/3179560> |
| Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | <https://www.microsoft.com/download/details.aspx?id=13255> |

#### <a name="follow-these-steps-for-each-vm"></a>各 VM について、これらのステップに従います。

1. 各 infrastructure\VMs\<VMName> フォルダーのコンテンツを対応する VM にコピーし、次のスクリプトを実行します。

    ```powershell
    # Install pre-req software on the VMs.
    .\Configure-PreReqs.ps1 -MSIFilePath <path of the MSIs>
    ```

    > [!IMPORTANT]
    > 再起動するように求められるたびにコンピューターを再起動します。 再起動した後、すべての前提条件がインストールされるまで、`.\Configure-PreReqs.ps1` スクリプトを再実行することを確認します。

2. VM セットアップを完了するため、存在する場合は、次のスクリプトを実行します。

    ```powershell
    .\Add-GMSAOnVM.ps1
    .\Import-PfxFiles.ps1
    .\Set-CertificateAcls.ps1
    ```

3. 次のスクリプトを実行して VM のセットアップを検証します。

    ```powershell
    .\Test-D365FOConfiguration.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

### <a name="setupsfcluster"></a> 10. スタンドアロン Service Fabric クラスターの設定

1. [Service Fabric スタンドアロン インストール パッケージ](https://go.microsoft.com/fwlink/?LinkId=730690) を使用中の Service Fabric ノードのいずれかにダウンロードします。 ZIP ファイルをダウンロードした後、 ZIP ファイルを右クリックし**プロパティ**を選択してブロックを解除します。 ダイアログ ボックスで、右下の **ブロック解除** チェック ボックスを選択します。

2. ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。 **インフラストラクチャ**フォルダーが、このフォルダーにアクセスすることを確認します。

3. **インフラストラクチャ** フォルダーに移動し、次のコマンドを実行して Service Fabric Cluster の ClusterConfig.json ファイルを生成します。

    ```powershell
   .\New-SFClusterConfig.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -TemplateConfig <ServiceFabricStandaloneInstallerPath>\ClusterConfig.X509.MultiMachine.json
    ```

    詳細については、[手順 1B: 複数のマシンでクラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。

4. 生成された ClusterConfig.json ファイルを \<ServiceFabricStandaloneInstallerPath\> にコピーします。

5. 上位の権限を使用して Windows PowerShell で \<ServiceFabricStandaloneInstallerPath\> に移動します。 次のコマンドを実行して ClusterConfig をテストします。

    ```powershell
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

6. テストが成功した場合は、次のコマンドを実行してクラスターを展開します。

    ```powershell
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

7. クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。

    1. まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。
    2. **IE 設定** \> **互換モード** に移動し、**互換モードでイントラネット サイトを表示する** チェック ボックスをオフにします。
    3. `https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。 DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。
    4. クライアントの証明書を選択します。 **Service Fabric エクスプローラー** ページが表示されます。

### <a name="configurelcs"></a> 11. テナント用 LCS 接続のコンフィギュレーション

Finance and Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。 LCS から Finance and Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。

CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。

オンプレミス エージェント証明書は、テナントごとに複数のサンドボックス環境および実稼動環境で再利用できます。

グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。 既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者です。

> [!IMPORTANT]
> テナントごとに証明書を正確に 1 回構成する必要があります。 すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。

1. Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。 詳細については [Azure PowerShell サービス管理モジュールのインストール](https://docs.microsoft.com/powershell/azure/servicemanagement/install-azure-ps?view=azuresmps-4.0.0) を参照してください。
2. [顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。
3. $(DownloadPath)\\InfrastructureScripts から次のスクリプトを実行します。
    ```powershell
    .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
    ```

### <a name="setupfile"></a> 12.ファイル ストレージの設定

以下の SMB 3.0 ファイル共有を設定する必要があります。

- AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。
- デプロイメントを調整するための最新のビルド ファイルと構成ファイルを保存するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent)。

    > [!WARNING]
    > 共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。

SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](https://technet.microsoft.com/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) を参照してください。

> [!IMPORTANT]
> - セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。 したがって、SMB 1.0 サーバーを無効にすることを強くお勧めします。 SMB 1.0 サーバーを無効にすることで、SMB 暗号化のすべての機能を利用できます。
> - 環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。 BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。

1. ファイル共有マシンで、次のコマンドを実行します。

    ```powershell
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```

2. \\\\DAX7SQLAOFILE1\\aos-storage ファイル共有を設定するには、これらの手順に従います。

    1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
    2. **タスク**\>**新しい共有** を選択し、新しい共有を作成します。 共有に **aos-storage** と名前を付けます。
    3. OrchestratorType を除いて、Service Fabric クラスター内のすべてのマシンに対して**変更**許可を与えます。
    4. AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF$) に対して、**変更**アクセス許可を付与します。

3. \\\\DAX7SQLAOFILE1\\ エージェント ファイル共有を設定するには、これらの手順に従います。

    1. サーバー マネージャーで、**ファイルと保管サービス** \> **共有** を選択します。
    2. **タスク**\>**新しい共有** を選択し、新しい共有を作成します。 共有に**エージェント**と名前を付けます。
    3. ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して **フル コントロール** のアクセス許可を与えます。

### <a name="setupsql"></a> 13. SQL Server の設定

1. 高可用性を備えた SQL Server 2016 SP1 をインストールします。 (SQL Server の 1 つのインスタンスで十分なサンドボックス環境に配置している場合を除きます。 高可用性シナリオをテストするため、サンドボックス環境に高可用性の SQL Server をインストールできます。)

    高可用性を備えた SQL Server を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールすることができます。 データベース エンジン、SSRS、フルテキスト検索、および管理ツールがインストール済みであることを確認します。

    > [!NOTE]
    > Always-On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) で説明されているとおりに設定され、[セカンダリ データベースを手動で準備する](/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) の指示に従っていることを確認します。

2. ドメイン ユーザーとして SQL サービスを実行します。
3. Finance and Operations を構成するために CA から SSL 証明書を取得します。 テストの目的で、自己署名証明書を作成して使用することができます。

    **クラスター化された SQL インスタンスの自己署名証明書**

    ```powershell
    New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
    ```

    **Always-On SQL インスタンスの自己署名証明書**

    テスト証明書の**手動**作成。
    ```powershell
    # https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

    # Manually create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
    # Run script on each node
    $computerName = $env:COMPUTERNAME.ToLower()
    $domain = $env:USERDNSDOMAIN.ToLower()
    $listenerName = 'dax7sqlaosqla'
    $cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'
    ```

4. SQL サーバーで SSL を構成するには、証明書を使用します。 [Microsoft 管理コンソールを使用して SQL Server のインスタンスに対する SSL 暗号化を有効にする方法](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) の手順に従います。
5. SQL クラスターの各ノードに対して、次の手順を実行します。 非アクティブなノードで変更を加えて、変更が行われた後フェール オーバーするようにしてください。

    1. LocalMachine\\My に証明書をインポートします。Always-On を設定していない限り、証明書は既にノードに存在します。
    2. SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。 Microsoft 管理コンソール (MMC) で証明書 (**certlm.msc**) を右クリックし、**タスク** \> **秘密キーの管理**を選択します。
    3. 証明書の拇印を HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate に追加します。
    4. Microsoft SQL Server 構成マネージャーで、**ForceEncryption** を**はい**に設定します。

6. 証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。

### <a name="configuredb"></a> 14. データベースのコンフィギュレーション

1. [LCS](https://lcs.dynamics.com/v2) にサインインします。

2. ダッシュボードで、**共有アセット ライブラリ**タイルを選択します。

3. **モデル**タブで、必要なリリースのデモ データを選択し、zip ファイルをダウンロードします。

| リリース | デモ データ |
|-------|------|
| オンプレミスの一般提供 (GA) リリース | Dynamics 365 for Operations (オンプレミス) - デモ データ |
| オンプレミスのプラットフォーム更新プログラム 2017 年 11 月 11 日リリース | Dynamics 365 for Operations, Enterprise edition (オンプレミス) - 更新プログラム 11 デモ データ |

4. zip ファイルには空のデモデータ .bak ファイルが含まれています。 必要に応じて、.bak ファイルを選択します。 たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルをダウンロードします。

5. infrastructure\ConfigTempate.xml のデータベース セクションが、次のように正しく構成されているか確認します。
    1. データベース名。
    2. db ファイルとログ設定。 dbの設定は、指定された既定値以上にする必要があります。
    3. LCS 共有アセット ライブラリからダウンロードされるバックアップ ファイルへのパス。 Finance and Operations データベースの既定の名前は AXDB です。

   > [!WARNING]
   > 1. SQL サービスを実行しているユーザーとスクリプトを実行しているユーザーは、バックアップ ファイルが格納されているフォルダーまたは共有に対して READ アクセス権を持っている必要があります。
   > 
   > 2. 同じ名前のデータベースが存在する場合は、データベースが再利用されます。

6. **インフラストラクチャ**フォルダーを SQL Server マシンにコピーし、権限を昇格した PowerShell ウィンドウでそのフォルダーに移動します。

#### <a name="configure-the-orchestratordata-database"></a>OrchestratorData データベースのコンフィギュレーション

1. 次のスクリプトを実行します。

   ```powershell
   .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName Orchestrator
   ```

   スクリプトは、次の操作を行います。
  
   - **OrchestratorData** という名前の空のデータベースを作成します。 このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。
   - データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。

#### <a name="configure-the-finance-and-operations-database"></a>Finance and Operations データベースの構成

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
    5. サーバー状態の表示を [contoso\svc AXSF$] に付与

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

### <a name="encryptcred"></a> 15. 資格情報の暗号化

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
    - **SqlUser** は、Finance and Operations データベース (AXDB) にアクセスできる暗号化された SQL ユーザー (axdbadmin) で、**SqlPassword** は暗号化された SQL パスワードです。

4. .json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。
5. 暗号化された値で Credentials.json ファイルを更新します。

    ```powershell
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | Set-Clipboard
    ```

### <a name="setupssis"></a> 16. SSIS の設定

データ管理と統合ワークロードを有効にするには、各 AOS 仮想マシンに SSIS をインストールする必要があります。 各 AOS 仮想マシン上で、次の手順を実行します。

1. マシンに SSIS インストールへのアクセス許可があることを確認し、SSIS セットアップ ウィザードを開きます。
2. **機能の選択**ウィンドウの**機能**ウィンドウで、**Integration Services** および **SQL クライアント接続 SDK** のチェック ボックスをオンにします。
3. セットアップを完了し、インストールが正常に完了したことを確認します。

詳細については、[統合サービスのインストール](https://docs.microsoft.com/sql/integration-services/install-windows/install-integration-services) を参照してください。

### <a name="setupssrs"></a> 17. SSRS の設定

1. 開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。
2. [オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。

### <a name="configureadfs"></a>18. AD FS のコンフィギュレーション

この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。 AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。

Finance and Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。 以下の手順では、Windows PowerShell は AD FS ロール サービスがインストールされているマシン上で実行されます。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。 たとえば、ユーザーには、ドメイン管理者アカウントが必要です。

1. AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。

    ```powershell
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. 混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。 WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。

    ```powershell
    Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
    ```

3. サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。

    ```powershell
    Add-Type -AssemblyName System.Net
    $fqdn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
    $domainName = $fqdn.Substring($fqdn.IndexOf('.')+1)
    Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
    ```

AD FS が認証を交換するために Finance and Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。 設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。 Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。 次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウントを使用してスクリプトを実行します。 (たとえば、管理者アカウントを使用します。)

スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。 後の手順の LCS でこの情報が必要となるため、出力に指定されているクライアント ID を書き留めておいてください。 クライアント ID を紛失した場合、AD FS がインストールされているコンピューターにログインし、**サーバー マネージャー** \> **ツール** \> **AD FS の管理** \> **アプリケーション グループ** \> **Microsoft Dynamics 365 for Operations On-premises**を開き、ネイティブ アプリケーションでクライアント ID を見つけます。

```powershell
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
```

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

最後に、**AOSNodeType** タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。 このチェックを行うには、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` を開きます。 サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。 この手順については、「AD FS 展開ガイド」で説明されています。

URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。

これで、インフラストラクチャの設定を完了しました。 次のセクションでは、[LCS](https://lcs.dynamics.com) にアクセスしてコネクタを設定し、Finance and Operations 環境を配置する方法について説明します。

### <a name="configureconnector"></a> 19. コネクタのコンフィギュレーションと、オンプレミスのローカル エージェントのインストール

1. [LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。
2. ハンバーガー メニューで、**プロジェクト設定**を選択します。

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. **オンプレミス コネクタ** を選択します。
4. 新しいコネクタを作成するには、**追加** を選択します。
5. **ホスト インフラストラクチャ設定** タブで、エージェント インストーラーをダウンロードします。

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)
6. zip ファイルがブロックされていないことを確認します。 ファイルを右クリックし、**プロパティ** を選択します。 ダイアログ ボックスで**ブロック解除**を選択します。
7. **OrchestratorType** タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。
8. **構成エージェント** タブで、コンフィギュレーションの設定を入力します。
9. コンフィギュレーションを保存し、**コンフィギュレーションのダウンロード** を選択して、localagent-config.json コンフィギュレーション ファイルをダウンロードします。

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。
11. **コマンド プロンプト** ウィンドウで、エージェント インストーラーを含むフォルダーに移動して、次のコマンドを実行します。

    ```powershell
    LocalAgentCLI.exe Install <path of config.json>
    ```

    > [!NOTE]
    > このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。

12. ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻るようにします。
13. **設定の検証**タブで、**メッセージ エージェント**を選択して、ローカル エージェントへの LCS 接続をテストします。 接続が正常に確立されると、ページは下図のようになります。

    ![エージェントの検証](./media/ValidateAgent.PNG)

### <a name="deploy"></a> 20. LCS から Finance and Operations (オンプレミス) 環境を配置する

1. LCS で、オンプレミス プロジェクトに移動し、**環境** > **サンドボックス**に移動してから**構成**を選択します。
2. 新しい展開では、環境のトポロジを選択し、展開を開始するウィザードを完了します。
3. 既存の配置がある場合は、[オンプレミス環境の再配置](redeploy-on-prem.md) のトピックを参照します。
4. ローカル エージェントは配置要求を受け取り、配置を開始し、環境の準備ができたら LCS に再度通知します。

展開に失敗した場合、LCS のお客様の環境では、**再設定**ボタンは利用可能になります。 基になる問題を修正し、**再コンフィギュレーション**をクリックして、任意のコンフィギュレーションの変更を更新し、**配置**をクリックして配置を再試行します。

### <a name="connect"></a> 21. Finance and Operations (オンプレミス) 環境に接続する

ブラウザーで、https://[yourD365FOdomain]/namespaces/AXSF に移動し、そこでは yourD365FOdomain がこのドキュメントの[ドメイン名と DNS ゾーンの計画](#plandomain) セクションで定義したドメイン名です。

## <a name="additional-resources"></a>追加リソース
- [オンプレミス配置への更新プログラムの適用](apply-updates-on-premises.md)
- [オンプレミス環境の再配置](redeploy-on-prem.md)
