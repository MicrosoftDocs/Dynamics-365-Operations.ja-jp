---
title: "オンプレミス環境の設定と配置"
description: "このトピックでは、オンプレミス環境の計画、設定、および展開方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>オンプレミス環境の設定と配置

このドキュメントでは、展開を計画し、インフラストラクチャを設定し、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (オンプレミス) を展開する方法について説明します。

## <a name="finance-and-operations-components"></a>Finance and Operations のコンポーネント

Finance and Operations アプリケーションは、次の 3 つの主要なコンポーネントで構成されています。

- Application Object Server (AOS)
- ビジネス インテリジェンス (BI)
- 財務レポート/管理レポーター

これらのコンポーネントは、次のシステム ソフトウェアによって異なります。

- Microsoft Windows Server 2016
- 以下の特徴を有する Microsoft SQL Server 2016 SP1:

    - フルテキスト インデックス検索が有効にされている。
    - SQL Server Reporting Services (SSRS)。
    - SQL Server Integration Services (SSIS)。
    
     > [!NOTE]
     > フルテキスト検索が有効になっていない場合、アプリケーションは実行されません。

- SQL Server Management Studio
- Standalone Microsoft Azure Service Fabric
- Windows PowerShell 5.0 以降
- Windows Server 2016 での Active Directory Federation Services (AD FS)

  ドメインコントローラーは、2012 R2 以降のドメイン機能レベルが実装されている Windows Server 2012 R2 以降である必要があります。

  ドメイン機能レベルの詳細については、以下を参照してください。 
  - [Active Directory 機能レベルとは](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations のビットは、Microsoft Dynamics Lifecycle Services (LCS) を通じて配布されます。 配置する前に、[エンタープライズ契約](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) チャンネルを通じてライセンス キーを購入し、LCS でオンプレミス プロジェクトを設定します。 LCS からのみ配置を開始することができます。 LCS でオンプレミス プロジェクトを設定する方法の詳細については、[Lifecycle Services でのオンプレミス プロジェクトの作成](../lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。

## <a name="authentication"></a>認証

オンプレミス アプリケーションは AD FS で動作します。 LCS と対話するには、Azure Active Directory (Azure AD) も設定する必要があります。

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations は Standalone Service Fabric を使用します。 詳細については、[Service Fabric ドキュメント](/azure/service-fabric/) を参照してください。

## <a name="infrastructure"></a>インフラストラクチャ

Finance and Operations は、ハイパー集約アーキテクチャで動作するように設計されています。 ハードウェア構成には、次のコンポーネントが含まれます。

- Windows Server 2016 仮想マシン (VM) に基づく Standalone Service Fabric クラスター
- SQL Server (Clustered SQL と Always-On の両方がサポートされています)
- 認証のための AD FS
- ストレージ用の Server Message Block (SMB) バージョン 3 のファイル共有
- オプション: Microsoft Office Server 2017

詳細については、[システム要求](../get-started/system-requirements.md) およびサイジングのガイドラインを参照してください。

### <a name="hardware-layout"></a>ハードウェア レイアウト

[オンプレミス環境のハードウェア サイジング](../get-started/hardware-sizing-on-premises-environments.md) で推奨されるサイジングに基づいて、インフラストラクチャと Service Fabric クラスターを計画します。 Service Fabric クラスターを計画する方法の詳細については、[Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

次の表は、ハードウェア レイアウトの例を示しています。 この例は、設定を説明するためにこのトピック全体で使用されています。

> [!NOTE]
> Service Fabric クラスターのプライマリ ノードには、少なくとも 3 つのノードが必要です。 この例では [**OrchestratorType**] を主要なノード タイプとして指定します。

| マシンの目的                                 | マシンの名前    | IP アドレス    |
|-------------------------------------------------|-----------------|---------------|
| ドメイン コントローラー                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| ファイル サーバー                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On クラスター                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| クライアント                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric クラスター/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric クラスター/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric クラスター/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric クラスター/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric クラスター/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric クラスター/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric クラスター/Management Reporter ノード | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric クラスター/SSRS ノード                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>段取り

### <a name="prerequisites"></a>前提条件

セットアップを開始する前に、次の前提条件を満たす必要があります。 これらの前提条件の設定は、このドキュメントの範囲外です。

- Active Directory Domain Services (AD DS) がネットワークにインストールされ、構成されています。
- AD FS が配置されています。
- SQL Server、SSRS、および Management Studio がインストールされています。

### <a name="overview"></a>概要

Finance and Operations のインフラストラクチャを設定するには、以下の手順を完了する必要があります。

1. ドメイン名と DNS ゾーンの計画
2. 証明書の計画と取得
3. ユーザーとサービス アカウントの計画
4. DNS ゾーンの作成とレコードの追加
5. VM のドメインへの参加
6. VM への前提条件ソフトウェアの追加
7. LCS からセットアップ スクリプトのダウンロード
8. コンフィギュレーションの記述
9. 証明書のインストール
10. スタンドアロン Service Fabric CLuster の設定
11. テナント用 LCS 接続の構成
12. ファイル ストレージの設定
13. SQL Server の設定
14. データベースの構成
15. 資格情報の暗号化
16. SSRS の設定
17. AD FS のコンフィギュレーション

### <a name="plan-your-domain-name-and-dns-zones"></a>ドメイン名と DNS ゾーンの計画

AOS のプロダクション インストールには、公的に登録されたドメイン名を使用することをお勧めします。 このようにして、外部アクセスが必要な場合は、ネットワークの外部からアクセスできます。

たとえば、会社のドメインが contoso.com の場合、Finance and Operations (オンプレミス) は d365ffo.onprem.contoso.com であり、ホスト名は次のようになります。

- AOS の機械の場合 ax.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 sf.d365ffo.onprem.contoso.com

### <a name="plan-and-acquire-your-certificates"></a>証明書の計画と取得

Service Fabric クラスターと展開されているすべてのアプリケーションを保護するには、Secure Sockets Layer (SSL) 証明書が必要です。 プロダクションとサンドボックスのワークロードについては、[DigiCert](https://www.digicert.com/ssl-certificate/)、[Comodo](https://ssl.comodo.com/)、[Symantec](https://www.websecurity.symantec.com/ssl-certificate)、[GoDaddy](https://www.godaddy.com/web-security/ssl-certificate)、または [GlobalSign](https://www.globalsign.com/en/ssl/) などの認証局から証明書を取得することをお勧めします。 ドメインが [Active Directory 証明書サービス](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS) で設定されている場合は、AD CS を介して証明書を作成します。 証明書ごとに、プライベート キーが作成されたキーの交換を含める必要があり、個人情報交換 (.pfx) ファイルにエクスポート可能な必要があります。

自己署名証明書は、テスト目的でのみ使用できます。 便宜上、セットアップ スクリプトには、自己署名証明書を生成およびエクスポートするスクリプトが含まれています。 前述のように、これらの証明書は、テスト目的でのみ使用する必要があります。

| 目的                                      | 説明 | 追加条件 |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL 証明書                   | この証明書は、ネットワーク上の SQL Server インスタンスとクライアント アプリケーションの間で転送されるデータを暗号化するために使用されます。 | <p>証明書の場合、ドメイン名は、SQL Server のインスタンスまたはリスナーの完全修飾ドメイン名 (FQDN) と一致する必要があります。</p><p>たとえば、SQL のリスナーが DAX7SQLAOSQLA のコンピューターにホストされている場合、証明書の DNS 名は、DAX7SQLAOSQLA.onprem.contoso.com です。</p> |
| Service Fabric Server 証明書            | この証明書を使用して、Service Fabric ノード間のノードからノードの通信を保護します。 この証明書は、クラスターに接続するクライアントに提示されるサーバー証明書としても使用されます。 | <p>証明書のドメイン名は、AOS および Service Fabric がホストしている DNS ゾーンと一致する必要があります。</p><p>たとえば、証明書のドメイン名は、\*. onprem.contoso.com または \*. contoso.com の可能性があります。</p><p>ワイルドカードの証明書を使用する場合は、1 つだけのレベルにワイルドカード文字が適用されます。 前例の \*.contoso.com のように、複数のレベルの場合、サブドメイン、サブジェクト代替名 (SAN) を証明書に適用する必要があります。</p> |
| Service Fabric Client 証明書            | この証明書は、クライアントによって Service Fabric クラスターを表示および管理するために使用されます。 | |
| 証明書の暗号化                     | この証明書は、SQL Server パスワードとユーザー アカウントのパスワードなどの重要な情報を暗号化するために使用されます。 | <p>証明書キーの使用にはデータ暗号化 (10) が含まれている必要がありますが、サーバー認証またはクライアント認証は含めないでください。</p><p>詳細については、[Service Fabric アプリケーションでの機密情報の管理](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management) を参照してください。</p> |
| AOS SSL 証明書                          | <p>この証明書は、AOS Web サイトに接続するクライアントに提示されるサーバー証明書としても使用されます。 また、WCF (Windows Communication Foundation) / SOAP (Simple Object Access Protocol) 証明書を有効にするためにも使用されます。</p><p>ワイルドカードの証明書である場合、Service Fabric Server 証明書を使用することができます。</p> | <p>証明書のドメイン名は、AOS および Service Fabric がホストしている DNS ゾーンと一致する必要があります。</p><p>たとえば、証明書のドメイン名は、\*.d365ffo.onprem.contoso.com、\*.onprem.contoso.com、または \*.contoso.com の可能性があります。</p><p>ワイルドカードの証明書を使用する場合は、1 つだけのレベルにワイルドカードが適用されます。 前例の \*.contoso.com のように、複数のレベルの場合、サブドメインの SAN を証明書に適用する必要があります。</p> |
| セッション認証証明書           | この証明書は、AOS がユーザーのセッション情報を保護するために使用します。 | これも、LCS からの配置時に使用される**ファイル共有**証明書です。 |
| データの暗号化とデータ署名の証明書 | これらの証明書は、機密情報を暗号化するために AOS によって使用されます。 | |
| 財務報告クライアント証明書       | この証明書を使用して、財務報告サービスと AOS 間の通信を保護します。 | |
| 報告証明書                        | この証明書を使用して、SSRS と AOS 間の通信を保護します。 | |
| オンプレミス ローカル エージェント証明書           | <p>この証明書は、オンプレミスでホストされているローカル エージェントと LCS 間の通信を保護するのに役立ちます。</p><p>この証明書を使用すると、Azure AD テナントに代わってローカル エージェントが動作し、LCS と通信して配置を編成および監視することができます。</p> | |

### <a name="plan-your-users-and-service-accounts"></a>ユーザーとサービス アカウントの計画

Finance and Operations (オンプレミス) を機能させるために、いくつかのユーザー アカウントまたはサービス アカウントを作成する必要があります。 サービス アカウントの管理グループ (gMSAs)、ドメイン アカウント、および SQL アカウントの組み合わせを作成する必要があります。 次の表は、このトピックで使用されるユーザー アカウント、その目的、および名前の例を示しています。

| ユーザー アカウント                                            | 種類           | 目的 | ユーザー名 |
|---------------------------------------------------------|----------------|---------|-----------|
| 財務レポート アプリケーション サービス アカウント         | gMSA           |         | Contoso\\svc-FRAS$ |
| 財務レポート プロセス サービス アカウント             | gMSA           |         | Contoso\\svc-FRPS$ |
| 財務レポート クリック ワンス デザイナー サービス アカウント | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS サービス アカウント                                     | gMSA           | このユーザーは、将来校正するために作成する必要があります。 今後のリリースでは、AOS を gMSA と連携させる予定です。 このユーザーを設定時に作成することで、gMSA へのシームレスな移行が保証されます。 | Contoso\\svc-AXSF$ |
| AOS サービス アカウント                                     | ドメイン アカウント | AOS は GA のリリースでこのユーザーを使用します。 | Contoso\\AXServiceUser |
| AOS SQL DB 管理者ユーザー                                   | SQL ユーザー       | Finance and Operations は、このユーザーを使用して SQL\* を認証します。 このユーザーも、今後のリリースで gMSA ユーザーに置き換えられます。 | AXDBAdmin |
| ローカル配置エージェント サービス アカウント                  | gMSA           | このアカウントは、ローカル エージェントによって、さまざまなノードでの展開を調整するために使用されます。 | Contoso\\Svc-LocalAgent$ |

\* SQL 認証の SQL ユーザー名とパスワードは、暗号化されてファイル共有に格納されているため、保護されています。

### <a name="create-dns-zones-and-add-a-records"></a>DNS ゾーンの作成とレコードの追加

DNS は AD DS と統合されており、ネットワーク内のリソースを整理、管理、検索することができます。 AOS ホスト名と Service Fabric クラスタの DNS 正引き検索ゾーンと A レコードを作成します。 この設定例では、DNS ゾーン名は d365ffo.onprem.contoso.com で、A レコード/ホスト名は次のとおりです。

- AOS の機械の場合 **ax**.d365ffo.onprem.contoso.com
- Service Fabric クラスターの場合 **sf**.d365ffo.onprem.contoso.com

#### <a name="add-a-dns-zone"></a>DNS ゾーンの追加

DNS ゾーンを追加するには、次の手順を実行します。

1. ドメイン コントローラー マシンにサインインし、[**開始**] をクリックし、[**dnsmgmt.msc**] と入力して DNS マネージャーを起動します。
2. ドメイン コントローラー名を右クリックし、[**新しいゾーン**] \> [**次へ**] の順にクリックします。
3. [**プライマリ ゾーン**] を選択します。
4. [**Active Directory にゾーンを保存 (DNS サーバーが書き込み可能なドメインコントローラーの場合にのみ使用可能)**] のチェック ボックスが選択されたままの状態で、[**次へ**] をクリックします。
5. [**このドメイン (Contoso.com) のドメイン コントローラーで実行されているすべての DNS サーバーに対して**] を選択し、[**次へ**] クリックします。
6. [**前方参照ゾーン**] を選択し、[**次へ**] をクリックします。
7. 設定するゾーン名を入力して、[**次へ**] をクリックします。 たとえば、[**d365ffo.onprem.contoso.com**] と入力します。
8. [**動的更新を許可しない**] を選択し、[**次へ**] をクリックします。

#### <a name="set-up-an-a-record-for-aos"></a>AOS の A レコードを設定する

新しい DNS ゾーンで、[**AOSNodeType**] タイプの Service Fabric クラスター ノード**ごと**に、[**ax.d365ffo.onprem.contoso.com**] という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを右クリックして、[**新しいホスト**] をクリックします。
2. Service Fabric ノードの名前と IP アドレス (10.179.108.12 など) を入力し、[**ホストの追加**] をクリックします。

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Orchestrator の A レコードを設定する

新しい DNS ゾーンで、[**OrchestratorType**] タイプの Service Fabric クラスター ノード**ごと**に、[**sf.d365ffo.onprem.contoso.com**] という名前の 1 つの A レコードを作成します。 他のノード タイプの A レコードは作成しないでください。

1. 新しいゾーンを右クリックして、[**新しいホスト**] をクリックします。
2. Service Fabric ノードの名前と IP アドレス (10.179.108.15 など) を入力し、[**ホストの追加**] をクリックします。

#### <a name="join-vms-to-the-domain"></a>VM のドメインへの参加

各 VM をドメインに参加させるには、[Windows Server 2016 を Active Directory ドメインに参加する方法](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html) の各手順を完了します。 または、Windows PowerShell スクリプトを使用します。

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
VM をドメインに参加させた後に、ローカル管理者グループに AOS サービスアカウント (Contoso\svc-AXSF$、Contoso\svc-AXSF$) を追加します。 これを行う方法については、[ローカル グループにメンバーを追加する](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) の記事で確認します。

#### <a name="disable-user-access-control"></a>ユーザー アクセスの制御を無効にする 

**すべて**の Service Fabric ノードで、ユーザー アクセスの制御を無効にするには、次のスクリプトを実行します。
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> スクリプトが正常に完了したら、ノードを再起動する必要があります。

#### <a name="add-prerequisite-software-to-vms"></a>VM への前提条件ソフトウェアの追加

次の表に、各ノード タイプのマシンに適用する必要があるソフトウェアを示します。

> [!NOTE]
> コンポーネントをインストールした後、コンピューターを再起動する必要があります。

| ノード タイプ | コンポーネント | コマンド |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC ドライバー | [SQL Server - Windows + Linux 用 Microsoft ODBC ドライバー 13.1](https://www.microsoft.com/en-us/download/details.aspx?id=53339) を参照してください。 |
| AOS       | Microsoft .NET Framework version 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework version 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | インターネット インフォメーション サービス (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ | [Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ](https://support.microsoft.com/en-us/help/3179560) を参照してください。 |
| AOS       | Microsoft Access データベース エンジン 2010 再頒布可能パッケージ | [Microsoft Access データベース エンジン 2010 再頒布可能パッケージ](https://www.microsoft.com/en-us/download/details.aspx?id=13255) を参照してください。 |
| BI        | The .NET Framework バージョン 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework バージョン 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | **ネイティブ**モードの SQL Server Reporting Services 2016 | |
| MR        | The .NET Framework バージョン 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework バージョン 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual Studio 2013 用 Visual C++ 再頒布可能パッケージ | [Microsoft Visual Studio 2013 用 Microsoft Visual C++ 再頒布可能パッケージ](https://support.microsoft.com/en-us/help/3179560) を参照してください。 |

#### <a name="download-setup-scripts-from-lcs"></a>LCS からセットアップ スクリプトのダウンロード

セットアップ エクスペリエンスを向上させるためのスクリプトをいくつか紹介しています。 LCS からセットアップ スクリプトをダウンロードするには、次の手順に従います。

1. LCS にログイン (<https://lcs.dynamics.com/v2>)。
2. ダッシュボードで、[**共有資産ライブラリー**] タイルをクリックします。
3. [**モデル**] タブをクリックします。
4. グリッドで、[**Dynamics 365 for Operations - オンプレミス配置スクリプト**] 行を選択します。
5. [**バージョン**] をクリックして、スクリプトの最新版をダウンロードします。

### <a name="describe-your-configuration"></a>コンフィギュレーションの記述

このセクションでは、実行する必要のあるスクリプトに関する情報を提供します。 スクリプトは、実行する必要がある順番で説明されています。 スクリプトを実行するには、テンプレート ファイルを $(downloadPath)\\ConfigTemplate.xml に入力します。 ConfigTemplate.xml ファイルには、Service Fabric クラスター、それらを構成するために使用される証明書、および関連する証明書へのアクセスを許可する必要があるアカウントが記述されています。 提供されている例では、このトピックで説明するインフラストラクチャの例の値が記入されています。 テンプレート ファイルは、次のセクションで使用されます。

#### <a name="create-the-domain-account-for-a-service-user"></a>サービス ユーザーのドメイン アカウントの作成

次のコマンドを実行して、ドメイン ユーザー アカウント contoso\\AXServiceUser を作成します。

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>gMSAs の作成

1. ディレクトリを **$(DownloadPath)** に変更し、次の Windows PowerShell コマンドを実行します。

    > [!NOTE]
    > このスクリプトはユーザーを作成しません。 代わりに、ドメイン コントローラー マシン上で手動で実行する必要があるコマンドを出力します。

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Windows PowerShell ウィンドウには、コマンドの出力をコピーします。 改行が削除されていることを確認し、昇格された権限を使用して Active Directory ドメイン コントローラー マシンの行を実行します (右クリックして、[**管理者として実行**] をクリックします)。
3. Active Directory ドメイン コントローラー マシンで次のスクリプトを実行して、アカウントが正常に作成されたことを検証します。 サービス アカウントの命名規則に一致するパターンを置き換えた後でスクリプトを実行することを確認してください。

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. クライアント マシンで、Export-AddGMSAsONVMScript.ps1 スクリプトを実行します。 このスクリプトは、各 Service Fabric VM 上で実行されるスクリプトを生成し、各 VM 名に対応するフォルダーに追加します。

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS の停止

リモート デスクトップ プロトコル (RDP) を使用して各 Service Fabric VM に接続し、[Web サーバー (IIS 7) の開始または停止](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx) の手動手順を完了します。 または、RDP を使用することにより、次の Windows PowerShell スクリプトを使用して、各 Service Fabric VM に接続します。

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS 機能はインストールする必要がありますが、製品の IIS dll にいくつかの依存関係があるため無効にしてください。_

### <a name="install-certificates"></a>証明書のインストール

1. 有効な CA からこのトピックの前半に記載されている証明書を取得した場合は、ConfigTemplate.xml ファイルの証明書に、.pfx ファイル名と拇印を入力します。 [**generateSelfSignedCert**] 属性を [**False**] に設定し、[**exportable**] 属性を [**False**] に設定します。 .pfx ファイルを $(DownloadPath)\\InfrastructureScripts\\Certs フォルダーにコピーします。
2. 自己署名証明書を使用している場合 (テスト目的のみ)、次のスクリプトを実行します。 自己署名証明書を作成するには、ConfigTemplate.xml ファイルで、[**generateSelfSignedCert**] が [**True**] に設定され、[**exportable**] が [**True**] に設定されていることを確認します。 スクリプトは証明書の拇印で XML を更新します。

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. プライベート キー (.pfx ファイル) を使用して、新しい証明書をエクスポートします。 次のスクリプトを使用して、Windows PowerShell でエクスポート コマンドを生成して実行します。 .Pfx ファイルは、Certs フォルダーに入ります。

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > 証明書がインストールされていて、cert:\\CurrentUser\\My に存在する必要があります。 証明書もエクスポート可能である必要があります。

    自己署名証明書を使用している場合は、次のセクションに進んでください。 この手順を完了する必要はありません。

4. .pfx ファイルを $(DownloadPath)\\InfrastructureScripts\\Certs folder フォルダーにエクスポートまたはコピーした後、次のコマンドを実行して、VM に対応するフォルダに配置されるスクリプトを生成します。

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. 各フォルダ内のスクリプトを、フォルダ名に対応する VM にコピーします。
6. 各 VM で、次のスクリプトを表示されている順に実行します。

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>スタンドアロン Service Fabric クラスターの設定

1. 次のコマンドを実行して、ClusterConfig.json ファイルを生成します。

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    詳細については、[手順 1B: 複数のマシンでクラスターを作成する](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster)、[X.509 証明書を使用して Windows スタンドアロン クラスターを保護する](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security)、および[Windows Server で実行されているスタンドアロン クラスターを作成する](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster) を参照してください。

2. [Service Fabric スタンドアロン インストール パッケージ](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) を使用中の Service Fabric ノードのいずれかにダウンロードします。 zip ファイルをダウンロードしたら、zip ファイルを右クリックし、[**プロパティ**] をクリックしてブロックを解除します。 ダイアログ ボックスで、右下の [**ブロック解除**] チェック ボックスを選択します。
3. ZIP ファイルを Service Fabric クラスター内のいずれかのノードにコピーし、解凍します。
4. 次のコマンドを実行して、すべてのノードのポート 443 および 445 に受信ファイアウォール ルールを作成します。

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. 次のコマンドを実行して、SSRS ノードのみのポート 80 に受信ファイアウォール ルールを作成します。

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. ClusterConfig.json ファイルをスタンドアロン Service Fabric の解凍されたインストール場所にコピーします。
7. 高度な権限を使用して Windows PowerShell の解凍されたインストール場所に移動し、次のコマンドを実行して ClusterConfig をテストします。

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. テストが成功した場合は、次のコマンドを実行してクラスターを展開します。

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. クラスターが作成された後は、任意のクライアント マシンで Service Fabric エクスプローラーを開き、インストールを検証します。

    1. まだインストールされていない場合、CurrentUser\\My に Service Fabric クライアント証明書をインストールします。
    2. [**IE 設定**] \> [**互換モード**] に移動し、[**互換モードでイントラネット サイトを表示する**] チェック ボックスをオフにします。
    3. `https://sf.d365ffo.onprem.contoso.com:19080` に移動します。sf.d365ffo.onprem.contoso.com は、ゾーンで指定されている Service Fabric クラスターのホスト名です。 DNS 名前解決が設定されていない場合は、マシンの IP アドレスを使用します。
    4. クライアントの証明書を選択します。 [**Service Fabric エクスプローラー**] ページが表示されます。

### <a name="configure-lcs-connectivity-for-the-tenant"></a>テナント用 LCS 接続の構成

Finance and Operations の展開とサービスは、オンプレミスのローカル エージェントを使用して LCS を通じて調整されます。 LCS から Finance and Operations テナントへの接続を確立するには、Azure AD テナント (たとえば、Contoso.Onmicrosoft.com) の代わりに動作するローカル エージェントを可能にする証明書をコンフィギュレーションする必要があります。

CA から取得したオンプレミス エージェントの証明書またはスクリプトを使用して生成した自己署名証明書を使用します。

グローバル管理者ディレクトリの役割を持つユーザー アカウントだけが、LCS を承認するための証明書を追加できます。 既定では、組織の Microsoft Office 365 にサインアップする担当者が、ディレクトリのグローバル管理者になります。

> [!NOTE]
> テナントごとに証明書を正確に 1 回構成する必要があります。 すべてのオンプレミス環境では、同じ証明書を使用して LCS に接続できます。

1. Azure PowerShell の最新バージョンをクライアント マシンにダウンロードしてインストールします。 詳細については、[Azure PowerShell のインストールおよびコンフィギュレーション](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0) を参照してください。
2. [顧客の Azure ポータル](https://portal.azure.com) にサインインして、グローバル管理者ディレクトリの役割があることを確認します。
3. $(DownloadPath)\\InfrastructureScripts から次のスクリプトを実行します。

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>ファイル ストレージの設定

高可用性の 2 つの SMB 3.0 ファイル共有を設定する必要があります。 SMB 3.0 を有効にする方法については、[SMB セキュリティの強化](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) を参照してください。
セキュリティで保護されたダイアレクト ネゴシエーションでは、SMB 2.0 または 3.0 から SMB 1.0 へのダウングレードを検出または防止できません。 このため、SMB 暗号化のすべての機能を利用するには、SMB 1.0 サーバーを無効にすることを強くお勧めします

> [!NOTE]
> 環境内の残りの部分でデータが保護されていることを保証するために、BitLocker ドライブ暗号化をすべてのマシンで有効にする必要があります。 BitLocker を有効にする方法については、[BitLocker: Windows Server 2012 以降で配置する方法](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server) を参照してください。

- AOS にアップロードされるユーザー ドキュメントを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\aos-storage)。
- 配置を調整するための最新のビルド ファイルと構成ファイルを格納するファイル共有 (たとえば、\\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > 共有に入れるファイルの最大パス長を超えないように、このファイル共有パスはできるだけ短くしておいてください。

1. ファイル共有マシンで、次のコマンドを実行します。

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>\\\\DAX7SQLAOFILE1\\aos-storage ファイル共有の設定

2. サーバー マネージャーで、[**ファイルと保管サービス**] \> [**共有**] を選択します。
3. [**タスク**] \> [**新しい共有**] をクリックして、[**aos-storage**] という名前で新しい共有を作成します。
4. [**OrchestratorNodeType**] を除いて、Service Fabric クラスター内の各マシンに対して [**変更**] 許可を与えます。
5. AOS ドメイン ユーザー (contoso\\AXServiceUser) と gMSA ユーザー (contoso\\svc-AXSF) に対して、[**変更**] アクセス許可を付与します。

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>\\\\DAX7SQLAOFILE1\\aos-storage エージェント ファイル共有の設定

6. サーバー マネージャーへ戻り、[**ファイルと保管サービス**] \> [**共有**] を選択します。
7. [**タスク**] \> [**新しい共有**] をクリックして、[**agent**] という名前で新しい共有を作成します。
8. ローカル展開エージェント (contoso\\svc-LocalAgent$) の gMSA ユーザーに対して [**フル コントロール**] のアクセス許可を与えます。

### <a name="set-up-sql-server"></a>SQL Server の設定

1. 高可用性を備えた SQL Server 2016 SP1 を、SAN (ストレージ エリア ネットワーク) を含む SQL クラスターまたは Always-On 構成のいずれかとしてインストールします。  [**データベース エンジン、レポート サービス、フルテキスト検索**] および [**管理ツール**] が既にインストールされていることを確認します。
> [!NOTE]
> SQL Always On が [初期データ同期ページの選択 (可用性グループ ウィザードで常に使用する)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) を選択して設定され、[セカンダリ データベースを手動で準備する](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs) に従っていることを確認してください。
2. ドメイン ユーザーとして SQL サービスを実行します。
3. Finance and Operations を構成するために CA から SSL 証明書を取得します。 テストの目的で、自己署名証明書を作成して使用することができます。

**クラスター化された SQL インスタンスの自己署名証明書**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Always-On SQL インスタンスの自己署名証明書**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. 証明書を使用して、[Microsoft 管理コンソールを使用して SQL Server のインスタンスに対して SSL 暗号化を有効にする方法](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) の手順を完了し、SQL サーバーで SSL を構成します。
5. クラスターの各ノードに対して、次の手順を実行します。 変更が行われた後、非アクティブなノードで変更を加えて、それにフェール オーバーするようにしてください。

    1. 証明書を LocalMachine\\My にインポートします。
    2. SQL サービスを実行するために使用されるサービス アカウントに証明書のアクセス許可を付与します。 Microsoft 管理コンソール (MMC) で証明書 (certlm.msc) を右クリックし、[**タスク**] \> [**秘密キーの管理**] をクリックします。
    3. 証明書の拇印を HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate に追加します。
    4. Microsoft SQL Server 構成マネージャーで、[**ForceEncryption**] を [**はい**] に設定します。

6. 証明書の公開鍵 (.cer ファイル) をエクスポートし、各 Service Fabric ノードの信頼できるルートにインストールします。

### <a name="configure-the-orchestratordata-database"></a>OrchestratorData データベースのコンフィギュレーション

1.  空のデータベースを作成し、[**OrchestratorData**] という名前をつけます。 このデータベースは、オンプレミスのローカル エージェントによって配置を調整するために使用されます。
2.  データベースにローカル エージェント gMSA (svc-LocalAgent$) **db\_owner** アクセス許可を与えます。

    1. ツリーで、サーバー名を展開し、[**セキュリティ**] \> [**ログイン**] を展開し、右クリックして、[**新しいログイン**] をクリックします。

        ![新しいログイン コマンド](./media/OPSetup_01_NewLogin.png)


    2. [**svc-LocalAgent$**] サービス アカウントを調べます。 [**場所**] をクリックして、[**ディレクトリ全体**] を選択し、[**オブジェクト タイプ**] をクリックして、[**サービス アカウント**] を選択します。

        ![[ユーザー]、[サービス アカウント]、または [グループ] ダイアログ ボックスを選択する](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. [**ServerRole の割り当て**] を [**パブリック**] に設定します。
    4. **db\_owner** データベース ロールのアクセス許可を OrchestratorData データベースに割り当てます。

### <a name="configure-the-finance-and-operations-database"></a>Finance and Operations データベースの構成

1. LCS にログイン (<https://lcs.dynamics.com/v2>)。
2. ダッシュボードで、[**共有資産ライブラリー**] タイルをクリックします。
3. [**モデル**] タブをクリックする 
4. グリッドで、[**Dynamics 365 for Operations on-premises, Enterprise Edition - デモデータ**] 行をクリックして zip をダウンロードします。
5. Zip には空のデモデータ .bak ファイルが含まれています。 必要に応じて適切な .bak ファイルを選択します。 たとえば、デモ データが必要な場合は、AxBootstrapDB_Demodata.bak ファイルを復元します。 
6. AxBootstrapDB_DemoData.bak データベースを復元します。
7. データベースの名前を [**AXDBRAIN**] に変更します。
8. 復元したデータベースで、次のクエリを実行します。

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. データベース ファイルを更新します。

    1. データベースを右クリックし、[**プロパティ**] をクリックします。
    2. [**ファイル**] をクリックして、データベース ファイルのプロパティを変更します。
    3. [**初期サイズ (MB)**] フィールドに、5,120 を超える値を入力します。

        ![データベース プロパティ ダイアログ ボックス](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. [**AXDBBuild\_Data**] で、[**自動拡張/最大化**] フィールドを [**200**] メガバイト (MB) に設定します。
    5. [**AXDBBuild\_Log**] で、[**自動拡張/最大化**] フィールドを [**500**] MB に設定します。

        ![[自動拡張] ダイアログ ボックスの変更](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. SQL 認証が有効になっている新しいユーザーを作成します (axdbadmin)。
6. 次の表の情報を使用して、ユーザーおよびデータベースのロールをマップします。

    | ユーザー             | 種類    | データベース ロール |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. svc-AXSF$ ユーザーおよび axdbadmin SQL ユーザーに、tempdb データベース内の次のロールへのアクセス権を与えます。

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Management Studio で、次の Transact SQL (T-SQL) コマンドを実行します。

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. 次のコマンドを実行します。
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>財務レポート データベースのコンフィギュレーション

1.  空のデータベースを作成し、[**FinancialReporting**] という名前をつけます。
2.  次の表の情報を使用して、ユーザーおよびデータベースのロールをマップします。

    | ユーザー             | 種類 | データベース ロール |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>資格情報の暗号化

1. 任意のクライアント マシンで、LocalMachine\\My certificate store に暗号化証明書をインストールします。
2. 現在のユーザーにこの証明書の秘密キーへの読み取りアクセスを許可します。
3. 次のようにして、Credentials.json ファイルを作成します。

    ```
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

    - [**AccountPassword**] は、AOS ドメインユーザー (contoso\\axserviceuser) の暗号化されたドメイン ユーザー パスワードです。
    - [**SqlUser**] は、Finance and Operations データベース (AXDBRAIN) にアクセスできる暗号化された SQL ユーザー (axdbadmin) です。[**SqlPassword**] は暗号化された SQL パスワードです。

4. .json ファイルを SMB ファイル共有、\\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json にコピーします。
5. 暗号化された値で Credentials.json ファイルを更新します。

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Credentials.json で、[**\<encryptedDomainUserPassword\>**] を暗号化されたドメイン パスワードに置き換えます。
    2. [**\<encryptedSqlUser\>**] を暗号化された Finance and Operations SQL ユーザーに置き換えます。
    3. [**\<encryptedSqlPassword\>**] を Finance and Operations SQL パスワードに置き換えます。
    
### <a name="set-up-ssrs"></a>SSRS の設定

1.  開始する前に、このトピックの冒頭に記載されている前提条件がインストールされていることを確認してください。
2.  [オンプレミス配置の SQL Server Reporting Services のコンフィギュレーション](../analytics/configure-ssrs-on-premises.md) の手順に従います。

### <a name="configure-ad-fs"></a>AD FS のコンフィギュレーション

この手順を完了する前に、AD FS を Windows Server 2016 に展開する必要があります。 AD FS を展開する方法については、[Windows Server 2016 配置ガイドおよび 2012 R2 AD FS 配置ガイド](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide) を参照してください。

Finance and Operations では、AD FS の既定で標準のコンフィギュレーション以外の追加のコンフィギュレーションが必要です。 以下の手順では、Windows PowerShell は AD FS ロール サービスがインストールされているマシン上で実行されます。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。 たとえば、ユーザーには、ドメイン管理者アカウントが必要です。

1. AD FS 識別子を構成して、AD FS トークン発行者と一致するようにします。

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. 混在環境用に AD FS を構成していない限り、イントラネット認証接続用に Windows 統合認証 (WIA) を無効にする必要があります。 WIA を AD FS で使用できるように構成する方法の詳細については、[AD FS で Windows 統合認証 (WIA) を使用するようにブラウザを構成する](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia) を参照してください。

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. サインインの場合、ユーザーの電子メール アドレスは許容される認証入力でなければなりません。

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

AD FS が認証を交換するために Finance and Operations を信頼するためには、AD FS アプリケーション グループの下の AD FS にさまざまなアプリケーション エントリを登録する必要があります。 設定プロセスをスピードアップし、エラーを減らすために、次のスクリプトを使用して登録します。 Publish-ADFSApplicationGroup.ps1 スクリプトと D365FO-OP ディレクトリを、AD FS ロール サービスがインストールされているマシンにコピーします。 次に、AD FS を管理するための十分なアクセス許可を持つユーザー アカウント (管理者アカウントなど) を使用してスクリプトを実行します。 スクリプトの使用方法の詳細については、スクリプトに記載されているドキュメントを参照してください。 後の手順の LCS でこの情報を要求されるため、出力に指定されているクライアント ID を書き留めておいてください。

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS の管理コンソールは次の図のようになります。 サーバー マネージャーを開き、[**ツール**] \> [**AD FS の管理**] をクリックして、左側のツリー ビューの下部にある [**アプリケーション グループ**] をクリックします。 詳細を表示するには、アプリケーション グループをダブルクリックします。

![アプリケーション グループのプロパティ](./media/OPSetup_05_ApplicatioGroupProperties.png)

最後に、サニティ チェックのために、Web ブラウザーで `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` に移動して、[**AOSNodeType**] タイプの Service Fabric ノード上の AD FS OpenID コンフィギュレーション URL にアクセスできることを確認します。 サイトが安全でないことを示すメッセージが表示された場合は、AD FS SSL 証明書が信頼済ルート証明機関ストアに追加されていません。 この手順については、「AD FS 展開ガイド」で説明されています。 URL に正常にアクセスすると、AD FS コンフィギュレーションを含む JavaScript Object Notation (JSON) ファイルが返され、AD FS URL が信頼されていることがわかります。

これで、インフラストラクチャの設定は完了です。 以下のセクションでは、[LCS](https://lcs.dynamics.com) にナビゲートしてコネクタをセットアップし、Dynamics 365 for Finance and Operations 環境を導入する方法について説明します。

## <a name="configure-connector-and-install-on-premises-local-agent"></a>コネクタを構成し、オンプレミスのローカル エージェントをインストールする

1. [LCS](https://lcs.dynamics.com/) にサインインし、オンプレミスの実装プロジェクトを開きます。
2. ハンバーガー メニューで、[**プロジェクト設定**] をクリックします。

    ![プロジェクト設定コマンド](./media/OPSetup_06_ProjectSettings.png)

3. [**オンプレミス コネクタ**] をクリックします。
4. 新しいコネクタを作成するには、[**追加**] をクリックします。
5. [**ホスト インフラストラクチャ設定**] タブで、エージェント インストーラーをダウンロードします。

    ![[ホスト インフラストラクチャ設定] タブで、エージェント インストーラー ボタンをダウンロードする](./media/OPSetup_07_DownloadAgentInstaller.png)

6. zip ファイルがブロックされていないことを確認します。 ファイルを右クリックし、[**プロパティ**] をクリックして、[**ブロック解除**] を選択します。
7. [**OrchestratorType**] タイプの Service Fabric ノードの 1 つでエージェント インストーラーを解凍します。
8. [**構成エージェント**] タブで、コンフィギュレーションの設定を入力します。
9. コンフィギュレーションを保存し、[**コンフィギュレーションのダウンロード**] をクリックして、localagent-config.json コンフィギュレーション ファイルをダウンロードします。

    ![[エージェントの設定] タブの [コンフィギュレーションのダウンロード] ボタン](./media/OPSetup_08_DownloadConfigurations.png)

10. localagent-config.json ファイルを、エージェント インストーラー パッケージが配置されているマシンにコピーします。
11. コマンド プロンプト ウィンドウで、エージェント インストーラーを含むフォルダに移動して、次のコマンドを実行します。

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > このコマンドを実行するユーザーは、OrchestratorData データベースに対して **db\_owner** のアクセス許可を持っている必要があります。
    
12. ローカル エージェントが正常にインストールされると、LCS のオンプレミス コネクタに戻ることができます。
13. [**設定の検証**] タブで [**メッセージ エージェント**] ボタンをクリックします。 これにより、ローカル エージェントへの LCS 接続がテストされます。 接続が正常に確立されると、ページは下の図のようになります。

     ![エージェントの検証](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Finance and Operations (オンプレミス) 環境向けに Dynamics 365 を導入する

1. LCS のオンプレミス プロジェクトに移動し、[**環境**]、[**サンドボックス**] に移動し、[**構成**] をクリックします。
2. [**環境トポロジー**] を選択し、ウィザードを実行して展開を開始します。
3. ローカル エージェントは展開要求を受け取り、展開を開始し、準備ができたら LCS に再度通知します。

