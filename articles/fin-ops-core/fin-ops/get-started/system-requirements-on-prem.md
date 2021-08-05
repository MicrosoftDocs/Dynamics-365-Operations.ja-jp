---
title: オンプレミス配置のシステム要件
description: このトピックでは、オンプレミス配置のシステム要件を一覧表示します。
author: PeterRFriis
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: ed8022983a749c4cd1667fcd122277f35b13d4a4
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638818"
---
# <a name="system-requirements-for-on-premises-deployments"></a>オンプレミス配置のシステム要件

[!include [banner](../includes/banner.md)]

このトピックは、現在のバージョンの Microsoft Dynamics 365 Finance + Operations (オンプレミス) 配置のシステム要件を一覧表示します。 インストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。

> [!IMPORTANT]
> Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Dynamics 365 Finance + Operations (オンプレミス) 配置。

## <a name="network-requirements"></a>ネットワーク要件

Dynamics 365 Finance + Operations (オンプレミス) は、インターネット プロトコル バージョン 4 (IPv4) またはインターネット プロトコル バージョン 6 (IPv6) を使用するネットワークで処理できます。 システムを計画して次のガイドラインを使用するには、ネットワーク環境を検討してください。

### <a name="network-response-time"></a>ネットワークの応答時間

次の表では、Web ブラウザーと Application Object Server (AOS) の間の接続およびオンプレミス システムでの AOS とデータベースの間の接続のネットワークの最小要件を一覧表示します。

| 先頭値     | Web ブラウザから AOS へ                      | AOS からデータベースへ                                                                            |
|-----------|-----------------------------------------|--------------------------------------------------------------------------------------------|
| 帯域幅 | ユーザーあたり毎秒 50 キロバイト (KBps) | 毎秒 100 メガバイト (MBps)                                                            |
| 待機時間   | 250 ～ 300 ミリ秒 (ms) 未満     | 1 ミリ秒 (ローカル エリア ネットワーク \[LAN\] のみ) 未満。 AOS およびデータベースは、同一配置である必要があります。 |

- Finance + Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントから Finance + Operations をホストするデータ センターまでの待機時間のことです。
- 帯域幅の要件は、シナリオによって異なります。 一般的なシナリオでは、ブラウザーおよびサーバーの間に 50 KBps 以上の帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、より高い帯域幅を勧めます。 特定の帯域幅の量は、用途によって異なります。

AOS および Microsoft SQL Server データベースが異なるデータセンターにある配置はサポートされていません。 AOS および SQL Server データベースは、同一配置である必要があります。

一般に、Finance + Operations は、ブラウザーからサーバーへのラウンド トリップを減らすために最適化されます。 ブラウザー クライアントからデータセンターへのラウンド トリップの数は各ユーザーの操作ごとに 0 または 1 であり、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 特定のケースでのパフォーマンスの最良の指標として、非実稼働環境に対する実時間シミュレーションを使用することをお勧めします。

### <a name="lan-environments"></a>LAN 環境

LAN 環境において、Microsoft Windows Server の Microsoft Remote Desktop は、Finance + Operations に接続する必要はありません。 ただし、Remote Desktop では、サーバーの配置を構成する仮想マシン (VMs) 上でのサービス操作に必要な場合があります。

### <a name="wan-environments"></a>WAN 環境

広域ネットワーク (WAN) 環境において、Windows Server の Remote Desktop は、Finance + Operations に接続する必要はありません。

### <a name="internet-connectivity-requirements"></a>インターネット接続要件

Finance + Operations は、ユーザー ワークステーションからインターネットに接続する必要はありません。 ただし、一部の機能はインターネットに接続されていないと、利用できません。

<table>
<tbody>
<tr>
<td><strong>ブラウザー クライアント</strong></td>
<td>インターネットに接続されていないイントラネット シナリオは、オンプレミス配置オプションの設計ポイントです。 Microsoft Dynamics Lifecycle Services (LCS) のヘルプおよびタスク ガイド ライブラリなどのクラウド サービスを必要とする一部の機能は、利用できません。</td>
</tr>
<tr>
<td><strong>サーバー</strong></td>
<td>AOS または Microsoft Azure Service Fabric 層は、LCS と通信できる必要があります。 オンプレミス ブラウザーベースのクライアントには、インターネットへのアクセスは不要です。</td>
</tr>
<tr>
<td><strong>テレメトリ</strong></td>
<td>接続に長時間の障害があると、テレメトリ データが失われる可能性があります。 LCS への接続の中断は、オンプレミスのアプリケーション機能に影響しません。</td>
</tr>
<tr>
<td><strong>LCS</strong></td>
<td>配置、コードの配置、およびサービス操作には、LCS への接続が必要です。</td>
</tr>
</tbody>
</table>

## <a name="telemetry-data-transfer-to-the-cloud"></a>クラウドへのテレメトリ データの転送

ほとんどのテレメトリ データはローカルに保存され、Microsoft Windows のイベント ビューアーを使用してアクセスできます。 テレメトリ イベントの小さなサブセットは、診断のためにクラウド内の Microsoft テレメトリ パイプラインに転送されます。 顧客データおよびユーザー識別可能なデータは、Microsoft に送信されたテレメトリ データの一部ではありません。 VM 名は、LCS ポータルからの環境管理および診断を支援するために、Microsoft へ送信されます。

## <a name="domain-requirements"></a>ドメイン要件

Finance + Operations をインストールする場合は、次のドメイン要件を検討してください:

- Finance + Operations コンポーネントをホストする VM は、Active Directory ドメインに属している必要があります。 Active Directory Domain Services (AD DS) は、ネイティブ モードで構成する必要があります。
- Finance + Operations コンポーネントを実行する VM は、相互にアクセスする必要があります。 このアクセスは、AD DS で構成されています。
- ドメイン コントローラは、Microsoft Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。

### <a name="full-2-way-trust"></a>双方向の完全な信頼
Windows Server 2008 R2 ドメイン機能レベル (DFL) 上の会社のドメイン コントローラーと互換性を保つために、Windows Server 2008 R2 DFL ユーザー ドメインと Windows Server 2012 R2 DFL Finance + Operations サービス ドメインの間の双方向の完全な信頼は、プラットフォーム更新 33 以降でサポートされています。

つまり、Finance + Operations (オンプレミス) アプリケーションのユーザーは、Windows Server 2008 R2 DFL メインから取得され、Finance + Operations (オンプレミス) インフラストラクチャとサービスをホストするリソースとサービス アカウントは Windows Server 2012 R2 DFL ドメインから取得されます。

双方向の完全な信頼の設定の例を次に示します。

<img src="./media/2WayTrust.png" width="700" hspace="50" alt="Examples of supported full 2-way trust between DFL versions"/>

#### <a name="known-limitations-with-using-the-full-2-way-trust-setup"></a>双方向の完全な信頼設定を使用した場合の既知の制限
* Windows Server 2008 R2 ユーザー ドメインからのセキュリティ グループのインポートはサポートされていません。

## <a name="hardware-requirements"></a>ハードウェア要件

このセクションでは、Finance + Operations の実行に必要なハードウェアについて説明します。

システム構成、データ合成、および使用する機能に基づいて、実際のハードウェア要件は異なります。 適切なハードウェア選択に影響を与えるいくつかの要因を、以下に示します。

- 時間あたりのトランザクション数
- 同時ユーザー数

## <a name="minimum-infrastructure-requirements"></a>最小限のインフラストラクチャ要件

Finance + Operations では、Service Fabric を使用して、AOS、バッチ、データ管理、Management reporter、および環境オーケストレータ サービスをホストします。

SQL Server は、生産用として少なくとも 2 つのノードを持つ高可用性 HADRON の設定が必要です。

次の図は、Service Fabric クラスターのノードの最小推奨数を示しています。

[![Service Fabric Cluster の推奨されるノード数。](./media/Minimum-infrastructure-Jan2017.png)](./media/Minimum-infrastructure-Jan2017.png)

## <a name="processor-and-ram-requirements"></a>プロセッサおよび RAM 要件

次の表では、この配置オプションを実行するために必要な役割ごとに求められるプロセッサの数およびランダムアクセス メモリ (RAM) の量を示します。 詳細については、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) の Service Fabric スタンドアロン クラスターに推奨する最小要件を参照してください。

> [!NOTE]
> その他の Microsoft ソフトウェアが同じコンピューターにインストールされている場合、システムはそのソフトウェアのハードウェア要件も満たす必要があります。 他のサーバー アプリケーションが AOS と同じコンピューターにインストールされている場合、これらのサーバー アプリケーションを RAM の 1 ギガバイト (GB) に制限することをお勧めします。

**ロールおよびトポロジ タイプのサイズ変更**

| トポロジ   | 役割 (ノード タイプ)              | 推奨されるプロセッサ コア | 推奨メモリ (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| 生産 | AOS,データ管理、バッチ   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | オーケストレータ                  | 4                           | 16                      |
|            | SQL Server                    | 8                           | 32                      |
| サンドボックス    | AOS,データ管理、バッチ   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | オーケストレータ                  | 4                           | 16                      |
|            | SQL Server                    | 8                           | 32                      |

**生産およびサンド ボックス配置用の最小サイズ設定の見積**

| トポロジ                                        | 役割                          | インスタンスの数 |
|-------------------------------------------------|-------------------------------|---------------------|
| 生産                                      | AOS (データ管理、バッチ)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | オーケストレータ\*\*              | 3                   |
|                                                 | SQL Server                    | 2                   |
| サンドボックス                                         | AOS,データ管理、バッチ   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | オーケストレータ                  | 3                   |
|                                                 | SQL Server                    | 1                   |
| *生産とサンドボックス集計の概要ー* |                               | *19*                |

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
<td colspan="5">バック エンド記憶域は、ランタイム ストレージ エリア ネットワーク (SAN) のソリッド ステート ドライブ (SSDs) に基づく必用があります。
<p>1 秒あたりのサイズと入力 / 出力オペレーション (IOPS) スループットは、ワークロードのサイズに基づきます。</p>
</td>
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

\*SQL Server サイズは、ワークロードに大きく依存します。 詳細については、[オンプレミス環境のハードウェアのサイズ変更要件](hardware-sizing-on-premises-environments.md) を参照してください。 サンド ボックスと生産環境の 個別 SQL Server 機械を使用する必要があります。 ただし、すべてのサンド ボックス環境で、SQL Server を共有できます。

## <a name="storage"></a>保管

- **AOS** - Finance + Operations を使用して、サーバー メッセージ ブロック (SMB) 3.0 共有に構造化されていないデータを格納します。 詳細については、[Windows Server 2016 の Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview) を参照してください。
- **SQL** – 次のオプションは実行可能です。

    - 高可用性 SSD 設定
    - オンライン トランザクション 処理 (OLTP) スループットに対して最適化された SAN
    - 高パフォーマンス直接接続ストレージ (DAS)

- **SQL サーバーとデータの管理 IOPS** – データ管理と SQL Server の両方のストレージには、少なくとも 2,000 IOPS が必要です。 生産 IOPS はさまざまな要因に依存します。 詳細については、[オンプレミス環境のハードウェアのサイズ変更要件](hardware-sizing-on-premises-environments.md) を参照してください。
- **VM IOPS** – 各 VM は少なくともt 100 書き込み IOPS が必要です。

## <a name="virtual-host-requirements"></a>仮想ホストの要件

環境の仮想ホストを設定する場合は、[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) と [Service Fabric クラスターの説明](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description) のガイドラインを参照してください。 各仮想ホストには、サイズ変更されているインフラストラクチャ用のコアが十分にある必要があります。 SQL Server が物理ハードウェア上に存在し、その他のすべてが仮想化されている場合は、複数の高度な構成が可能です。 SQL Server が仮想化されている場合、ディスク サブシステムは高速 SAN または同等のものにする必要があります。 いずれの場合も、仮想ホストの基本設定が高可用性および重複であることを確認してください。 いずれの場合も、仮想化を使用する場合は、VM スナップショットを作成する必要はありません。

Finance + Operations には、非 Microsoft 仮想化プラットフォーム (具体的には VMWare) での操作に関する Microsoft の標準サポート ポリシーが適用されます。 詳細については、[Microsoft ソフトウェアのサポート ポリシー](https://support.microsoft.com/help/897615/support-policy-for-microsoft-software-that-runs-on-non-microsoft-hardw)を参照してください。 つまり、この環境では製品をサポートしますが、問題の調査を依頼された場合、仮想化プラットフォームのない状態または Microsoft 仮想化プラットフォームで問題を再現するようまずお客様に依頼する場合があります。

## <a name="software-requirements-for-all-server-computers"></a>すべてのサーバー コンピュータのソフトウェア要件

Finance + Operations コンポーネントをインストールする前に、次のソフトウェアがコンピュータに存在している必要があります:

- Microsoft .NET Framework。 バージョン情報については、[配置の設定](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md#setup)を参照してください。
- Service Fabric

詳細については、[Service Fabric クラスターの計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を参照してください。

## <a name="supported-server-operating-systems"></a>サポートされるサーバー オペレーティング システム

次の表は、サポートされているサーバー オペレーティング システムの一覧を示します。

| オペレーティング システム                                     | 摘要 |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter または Standard | これらの要件は、AOS をホストするデータベースおよび Service Fabric クラスターに対するものです。<p>en-US OS インストールのみがサポートされます。</p> |

## <a name="software-requirements-for-database-servers"></a>データベース サーバーのソフトウェア要件

- 64 ビット バージョンの SQL Server 2016 のみがサポートされています。
- サーバーおよびデータベースの照合順序では、**SQL\_Latin1\_General\_CP1\_CI\_AS** のみ有効です。 SQL Server データベースの照合順序を選択する方法の詳細については、「[SQL Server に関するドキュメント](/sql/sql-server/sql-server-technical-documentation)」を参照してください。
- 実稼動環境では、使用している SQL Server のバージョンの最新の累積的な更新プログラム (CU) をインストールすることをお勧めします。

次の表では、データベースでサポートされている SQL Server バージョンを一覧表示します。 詳細については、「[SQL Server](https://www.microsoft.com/sql-server/sql-server-2016) の最小ハードウェア要件」を参照してください。

| 必要量                                                      | 摘要 |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server2016 Standard Edition または Enterprise Edition | SQL Server 2016 のハードウェア要件については、「[SQL Server 2016 インストール用のハードウェアおよびソフトウェア要件](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)」を参照してください。 |

## <a name="software-requirements-for-application-object-server-aos"></a>Application Object Server (AOS) のソフトウェア要件

- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>レポート サーバー (BI) のソフトウェア要件

- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>クライアント コンピュータのソフトウェア要件

ユーザーは、これらの一般的なブラウザの最新バージョンを使用して Finance + Operations にアクセスできます。

- Microsoft Edge (推奨: [Chromium ベースの Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))
- Google Chrome
- Apple Safari
- Internet Explorer 11 (非推奨)

> [!NOTE]
> パフォーマンスを最適化し、最適なエクスペリエンスを提供するために、最新のブラウザ、特に Microsoft Edge の最新バージョンを使用することをお勧めします。 

### <a name="internal-explorer-deprecation"></a>Internal Explorer の廃止 
2020 年 12 月に Internet Explorer 11 のサポートが廃止され、2021 年 8 月にブラウザーのサポートが終了します。 詳細については、[Internet Explorer 非推奨のお知らせ](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps) を参照してください。

バージョン 10.0.20 から、Internal Exploler (IE) で Finance and Operations アプリにアクセスするユーザーにそのブラウザーに対するサポートの終了に関する通知が表示されます。 2021 年 8 月 17 日より前に、複数の IE ユーザーに対して、IE サポートが間もなく終了するという情報メッセージが表示されます。 その日以降、サポートが正式に終了したという警告が IE ユーザーに表示されます。 組織は、IE がユーザーにとって必須になっている以外は、これらの通知を継続することが推奨されます。そのケースでは、**Internet Explorer のサポート終了通知** 機能を無効にし、ユーザー ベースを Microsoft Edge または他の最新のブラウザーに移行する内部プロセスに依存することによりこれらの通知の非表示を選択できます。 

Finance and Operations アプリ内の IE の使用をブロックするための現在の目標は 2022 年 4 月です。 組織およびユーザーがそのブロックに対応するために、2022 年 1 月以降、IE ユーザーには IE サポートが間もなくブロックされることを示す無視できないエラー メッセージが表示されます。 このエラー メッセージは **Internet Explorer のサポート終了通知** 機能によって制御 **されない** ので、組織がこのメッセージを非表示にする必要がある場合、 顧客は Microsoft サポートに連絡する必要があります。    

### <a name="special-considerations"></a>特別な注意事項
- タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。
- 財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。 Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
- PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory フェデレーション サービスのソフトウェア要件

Windows Server 2016 の Active Directory フェデレーション サービス (AD FS) は必要です。

ドメイン コントローラは、Windows Server 2012 R2 またはそれ以降であり、ドメイン機能レベルは 2012 R2 またはそれ以上である必要があります。 ドメイン機能レベルの詳細については、次のページを参照してください。

- [Active Directory 機能レベルとは](/previous-versions/windows/it-pro/windows-server-2003/cc787290(v=ws.10))
- [Active Directory ドメイン サービス機能のレベルを理解する](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))
- [双方向の完全な信頼](../../fin-ops/get-started/system-requirements-on-prem.md#full-2-way-trust)

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

次の Microsoft Office アプリケーションは、オンプレミス配置でサポートされています。

- Microsoft Excel と Microsoft Word のアドインを実行するには、Windows 用の Microsoft Office 2016 (またはそれ以降) をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
- Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="hardware-and-software-requirements-for-commerce-components"></a>コマース コンポーネントのハードウェアおよびソフトウェア要件

現在、Finance + Operations はコマース コンポーネントを含んでいません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
