---
title: "オンプレミス配置のシステム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition オンプレミス配置のシステム要件を一覧表示します。"
author: kfend
manager: AnnBe
ms.date: 08/02/2017
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
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: ja-jp
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>オンプレミス配置のシステム要件

[!include[banner](../includes/banner.md)]

このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition オンプレミス配置のシステム要件を一覧表示します。 Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。

## <a name="network-requirements"></a>ネットワーク要件
Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (オンプレミス) は、Internet Protocol Version 4 (IPv4) または Internet Protocol Version 6 (IPv6) を使用するネットワークで動作できます。 システムを計画して次のガイドラインを使用するには、ネットワーク環境を検討してください。

### <a name="network-response-time"></a>ネットワークの応答時間
次の表では、Web ブラウザーと Application Object Server (AOS) の間の接続およびオンプレミス システムでの AOS とデータベースの間の接続のネットワークの最小要件を一覧表示します。

| 先頭値     | Web ブラウザから AOS へ                      | AOS からデータベースへ |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| 帯域幅 | ユーザーあたり毎秒 50 キロバイト (KBps) | 毎秒 100 メガバイト (MBps) |
| 待機時間   | 250 ～ 300 ミリ秒 (ms) 未満     | 1 ミリ秒 (ローカル エリア ネットワーク [LAN] のみ) 未満。 AOS およびデータベースは、同一配置である必要があります。 |

- Finance and Operations (オンプレミス) は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントから Finance and Operations をホストするデータ センターまでの待機時間のことです。
- Finance and Operations (オンプレミス) の帯域幅の要件はシナリオによって異なります。 一般的なシナリオでは、ブラウザーおよび Finance and Operations サーバーの間に 1 秒あたり 50 KBps 以上の帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、より高い帯域幅を勧めます。 特定の帯域幅の量は、用途によって異なります。

AOS および Microsoft SQL Server データベースが異なるデータセンターにある配置はサポートされていません。 AOS および SQL Server データベースは、同一配置である必要があります。 

一般に、Finance and Operations は、ブラウザーからサーバーへのラウンド トリップを減らすために最適化されます。 ブラウザー クライアントからデータセンターへのラウンド トリップの数は各ユーザーの操作ごとに 0 または 1 であり、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 特定のケースでのパフォーマンスの最良の指標として、Finance and Operations 以外の環境に対する実時間シミュレーションを使用することをお勧めします。 

### <a name="lan-environments"></a>LAN 環境
LAN 環境において、Microsoft Windows Server の Microsoft Remote Desktop は、Finance and Operations に接続する必要はありません。 ただし、Remote Desktop では、サーバーの配置を構成する仮想マシン (VMs) 上でのサービス操作に必要な場合があります。

### <a name="wan-environments"></a>WAN 環境
広域ネットワーク (WAN) 環境において、Windows Server の Remote Desktop は、Finance and Operations に接続する必要はありません。

### <a name="internet-connectivity-requirements"></a>インターネット接続要件
Finance and Operations (オンプレミス) は、ユーザー ワークステーションからインターネットに接続する必要はありません。 ただし、一部の機能はインターネットに接続されていないと、利用できません。

|                    |   |
|--------------------|---|
| **ブラウザー クライアント** | インターネットに接続されていないイントラネット シナリオは、オンプレミス配置オプションの設計ポイントです。 Microsoft Dynamics Lifecycle Services (LCS) のヘルプおよびタスク ガイド ライブラリなどのクラウド サービスを必要とする一部の機能は、利用できません。 |
| **サーバー**         | AOS または Microsoft Service Fabric 層は、LCS と通信できる必要があります。 オンプレミス ブラウザーベースのクライアントには、インターネットへのアクセスは不要です。 |
| **テレメトリ**      | 接続に長時間の障害があると、テレメトリ データが失われる可能性があります。 LCS への接続の中断は、オンプレミスのアプリケーション機能に影響しません。 |
| **LCS**            | 配置、コードの配置、およびサービス操作には、LCS への接続が必要です。 |

## <a name="telemetry-data-transfer-to-the-cloud"></a>クラウドへのテレメトリ データの転送
ほとんどのテレメトリ データはローカルに保存され、Microsoft Windows のイベント ビューアーを使用してアクセスできます。 テレメトリ イベントの小さなサブセットは、診断のためにクラウド内の Microsoft テレメトリ パイプラインに転送されます。 顧客データおよびユーザー識別可能なデータは、Microsoft に送信されたテレメトリ データの一部ではありません。 VM 名は、LCS ポータルからの環境管理および診断を支援するために、Microsoft へ送信されます。

## <a name="domain-requirements"></a>ドメイン要件
Finance and Operations (オンプレミス) をインストールする場合は、次のドメイン要件を検討してください:

- Finance and Operations (オンプレミス) コンポーネントをホストする VMs は、Active Directory ドメインに属している必要があります。 Active Directory ドメイン サービス (AD DS) は、ネイティブ モードで構成する必要があります。
- Finance and Operations (オンプレミス) コンポーネントを実行する VMs は、相互にアクセスする必要があります。 このアクセスは、AD DS で設定されています。 
- ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。

## <a name="hardware-requirements"></a>ハードウェア要件
このセクションでは、Finance and Operations (オンプレミス) の実行に必要なハードウェアについて説明します。

システム構成、データ合成、および使用するアプリケーションと機能に基づいて、実際のハードウェア要件は異なります。 Finance and Operations (オンプレミス) のための適切なハードウェア選択に影響を与えるいくつかの要因を、以下に示します。

- 時間あたりのトランザクション数
- 同時ユーザー数

## <a name="minimum-infrastructure-requirements"></a>最小限のインフラストラクチャ要件
Finance and Operations (オンプレミス) では、Service Fabric を使用して、AOS、バッチ、データ管理、Management reporter、および環境オーケストレータ サービスをホストします。 

SQL Server は、生産用として少なくとも 2 つのノードを持つ高可用性 HADRON の設定が必要です。

次の図は、Service Fabric クラスターのノードの最小推奨数を示しています。

[![Service Fabric クラスターの推奨されるノード数](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>プロセッサおよび RAM 要件
次の表では、この配置オプションを実行するために必要な役割ごとに求められるプロセッサの数およびランダムアクセス メモリ (RAM) の量を示します。 詳細については、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) の Service Fabric スタンドアロン クラスターに推奨する最小要件を参照してください。

> [!NOTE]
> その他の Microsoft ソフトウェアが同じコンピューターにインストールされている場合、システムはそのソフトウェアのハードウェア要件も満たす必要があります。 他のサーバー アプリケーションが AOS と同じコンピューターにインストールされている場合、これらのサーバー アプリケーションを 1 ギガバイト (GB) の RAM に制限することをお勧めします。

[**ロールおよびトポロジ タイプのサイズ変更**]

| トポロジ   | 役割 (ノード タイプ)              | 推奨されるプロセッサ コア | 推奨メモリ (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| 生産 | AOS,データ管理、バッチ   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | オーケストレータ                  | 4                           | 16                      |
| サンドボックス    | AOS,データ管理、バッチ   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | オーケストレータ                  | 4                           | 16                      |

**生産およびサンド ボックス配置用の最小サイズ設定の見積\***

| トポロジ                                        | 役割                          | インスタンスの数 |
|-------------------------------------------------|-------------------------------|---------------------|
| 生産                                      | AOS (データ管理、バッチ)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | オーケストレータ\*\*              | 3                   |
| サンドボックス                                         | AOS,データ管理、バッチ   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | オーケストレータ                  | 3                   |
| *生産とサンドボックス集計の概要ー* |                               | *16*                |

\*この表の数字は、プレビュー顧客によって検証されており、顧客からのフィードバックに基づいて調整されるかもしれません。

\*\* オーケストレータはプライマリ ノード タイプとして指定され、また Service Fabric サービスの実行にも使用されます。

**バック エンド SQL Server と AD DS の初期推定値**

<table>
<thead>
<tr>
<th></th>
<th>役割</th>
<th>VMs/ インスタンス</th>
<th>コア</th>
<th>コア合計</th>
<th>インスタンス 16 GB あたりのメモリー</th>
<th>メモリー合計 (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>共有インフラストラクチャ</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>ファイル サーバー / ストレージ エリア ネットワーク / 高可用性ストレージ</td>
<td colspan="5"><p>バック エンド記憶域は、ランタイム ストレージ エリア ネットワーク (SAN) のソリッド ステート ドライブ (SSDs) に基づく必用があります。</p>
<p>1 秒あたりのサイズと入力 / 出力オペレーション (IOPS) スループットは、ワークロードのサイズに基づきます。</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>共有インフラストラクチャの概要</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\*SQL Server サイズは、ワークロードに大きく依存します。 詳細については、[オンプレミス環境のハードウェアのサイズ変更](hardware-sizing-on-premises-environments.md) を参照してください。

## <a name="storage"></a>保管

- **AOS** - Finance and Operations (オンプレミス) を使用して、サーバー メッセージ ブロック (SMB) 3.0 共有に構造化されていないデータを格納します。 詳細については、「[Windows Server 2016 の Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)」を参照してください。
- **SQL** – 次のオプションは実行可能です。

    - 高可用性 SSD 設定
    - オンライン トランザクション 処理 (OLTP) スループットに対して最適化された SAN
    - 高パフォーマンス直接接続ストレージ (DAS) 

- **SQL サーバーとデータの管理 IOPS** – データ管理と SQL Server の両方のストレージには、少なくとも 1 秒あたり 2,000 IOPS が必要です。 生産 IOPS はさまざまな要因に依存します。 詳細については、[オンプレミス環境のハードウェアのサイズ変更](hardware-sizing-on-premises-environments.md) を参照してください。
- **VM IOPS** – 各 VM は少なくともt 100 書き込み IOPS が必要です。

## <a name="virtual-host-requirements"></a>仮想ホストの要件
Finance and Operations (オンプレミス) 環境の仮想ホストを設定する場合は、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) と [Service Fabric クラスターの説明](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description) のガイドラインを参照してください。 各仮想ホストには、サイズ変更されているインフラストラクチャ用のコアが十分にある必要があります。 SQL Server が物理ハードウェア上に存在し、その他のすべてが仮想化されている場合は、複数の高度な構成が可能です。 SQL Server が仮想化されている場合、ディスク サブシステムは高速 SAN または同等のものにする必要があります。 いずれの場合も、仮想ホストの基本設定が高可用性および重複であることを確認してください。 いずれの場合も、仮想化を使用する場合は、VM スナップショットを作成する必要はありません。

## <a name="software-requirements-for-all-server-computers"></a>すべてのサーバー コンピュータのソフトウェア要件
Finance and Operations (オンプレミス) コンポーネントをインストールする前に、次のソフトウェアがコンピュータに存在している必要があります:

- Microsoft .NET Framework バージョン 4.5.1 またはそれ以降
- Service Fabric

詳細については、[Service Fabric クラスターの計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

## <a name="supported-server-operating-systems"></a>サポートされるサーバー オペレーティング システム
次の表では、Finance and Operations コンポーネントでサポートされているサーバー オペレーティング システムを示します。

| オペレーティング システム                                     | 摘要 |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter または Standard | これらの要件は、AOS をホストするデータベースおよび Service Fabric クラスターに対するものです。 |

## <a name="software-requirements-for-database-servers"></a>データベース サーバーのソフトウェア要件

- 64 ビット バージョンの SQL Server 2016 のみがサポートされています。
- 実稼動環境では、使用している SQL Server のバージョンの最新の累積的な更新プログラム (CU) をインストールすることをお勧めします。
- Finance and Operations (オンプレミス) では、大文字小文字を区別しない、アクセントを区別する、カナを区別する、および幅を区別しない Unicode 照合順序をサポートします。 照合順序は、AOS インスタンスを実行しているコンピュータの Windows ロケールと一致する必要があります。 新しいインストールを設定する場合は、SQL Server 照合の代わりに Windows 照合を選択することをお勧めします。 SQL Server データベースの照合順序を選択する方法の詳細については、「[SQL Server に関するドキュメント](/sql/sql-server/sql-server-technical-documentation)」を参照してください。

次の表では、Finance and Operations データベースでサポートされている SQL Server バージョンを一覧表示します。 詳細については、「[SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) の最小ハードウェア要件」を参照してください。

| 必要量                                                      | 摘要 |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard エディションまたは Enterprise エディション | SQL Server 2016 のハードウェア要件については、「[SQL Server 2016 インストール用のハードウェアおよびソフトウェア要件](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)」を参照してください。 |

## <a name="software-requirements-for-application-object-server-aos"></a>Application Object Server (AOS) のソフトウェア要件 
- SQL Server Integation Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>レポート サーバー (BI) のソフトウェア要件
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>クライアント コンピュータのソフトウェア要件
Finance and Operations Web アプリケーションは、HTML 5.0 に準拠している Web ブラウザーを備えた任意のデバイス上で実行できます。 Microsoft が確認した特定のデバイス / ブラウザーの組み合わせは、次の通りです。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)
- Mac OS X 10.10 (Yosemite)、 10.11 (El Capitan) または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory フェデレーション サービスのソフトウェア要件 
Windows Server 2016 の Active Directory Federation Services (AD FS) は必要です。

ドメイン コントローラは、Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。 ドメイン機能レベルの詳細については、次のページを参照してください。

- [Active Directory 機能レベルとは](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>サポートされている Microsoft Office アプリケーション
次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。

-   Microsoft Excel と Microsoft Word のアドインを実行するには、Windows か Mac 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
-   [Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>小売コンポーネントのハードウェアおよびソフトウェア要件
現在、Finance and Operations (オンプレミス) は Retail コンポーネントを含んでいません。

