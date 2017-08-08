---
title: "システム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 Finance and Operations, Enterprise Edition クラウドおよびオンプレミス配置のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: ja-jp
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>システム要件

[!include[banner](../includes/banner.md)]


このトピックでは、現在のバージョンの Microsoft Dynamics 365 Finance and Operations,Enterprise Edition,クラウドおよびオンプレミス配置のシステム要件を一覧表示します。 Finance and Operations をインストールする前に、必要に応じて、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。


## <a name="supported-microsoft-office-applications"></a>サポートされている Microsoft Office アプリケーション
次の Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。
-   Microsoft Excel と Word のアドインを実行するには、Windows か Mac 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要件の詳細については、[Office 統合トラブルシューティング](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting) を参照してください。
-   [Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

# <a name="system-requirements-specific-to-cloud-deployments"></a>クラウド配置に固有のシステム要件
## <a name="network-requirements"></a>ネットワーク要件
-   Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 これは、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データ センターまでの待機時間です。 <http://www.azurespeed.com> でネットワーク待機時間をテストすることをお勧めします。
-   Finance and Operations の帯域幅の要件はシナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。 ただし、大がかりなカスタマイズを必要とするワークスペースやシナリオなど、高度な伝送データ要件があるシナリオでは、帯域幅を増やすことをお勧めします。

一般に、Finance and Operations は、インターネットに最適化されます。 ブラウザー クライアントから Azure データ センターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。 

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客には、Finance and Operations のプレビュー バージョンを使用します。

## <a name="net-framework-requirements"></a>.NET Framework 要件
Finance and Operations では、ドキュメント回覧エージェントなどのすべてのクリックワンス アプリケーション用として .NET Framework バージョン 4.6.2 が必要です。 インストール手順については、[.NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー
Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。


-   Windows 10 の Microsoft Edge (公開されている最新のバージョン)
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)
-   Mac OS X 10.10 (Yosemite)、 10.11 (El Capitan) または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)

各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。 

> [!NOTE]
> -   プレリリース版の Chrome 拡張機能をインストールすると、スクリーンショット イメージをタスク レコーダーでキャプチャし、生成された Microsoft Word ドキュメントに含めることができます。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   ワークフロー エディターは ClickOnce アプリケーションとして起動されます。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。 ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。
> -   財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。 匿名モードで Chrome を使用している場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
> -   PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS でサポートされている Web ブラウザー

Retail Cloud POS は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

-   Windows 10 の Microsoft Edge (公開されている最新のバージョン)
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS 要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail Modern POS は Windows 10 Pro、Enterprise、また Enterprise Long Term Servicing Branch (LTSB) エディションでのみサポートされています。

### <a name="minimum-system-requirements"></a>最少システム要件

-   最少のサポートされている解像度は 1280 × 1024 です。
-   Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。
    -   最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。
    -   最低でも、3 ギガバイト (GB) の RAM が必要です。
    -   インターネットにアクセスできる必要があります。

## <a name="retail-hardware-station-requirements"></a>Retail hardware station 要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail hardware station は、以下のオペレーティング システムでサポートされます。
    -   Windows 7 Professional、Enterprise、また Ultimate エディション 
    
    > [!NOTE]
    > Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。

    -   Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション
    -   Windows 10 Pro、Enterprise、また Enterprise LTSB エディション

### <a name="minimum-system-requirements"></a>最少システム要件

コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。

-   インターネット インフォメーション サービス (IIS)
-   サード パーティのハードウェア

## <a name="retail-store-scale-unit-requirements"></a>Retail Store スケール ユニット要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。
    -   Windows 7 Professional、Enterprise、また Ultimate エディション
    -   Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション
    -   Windows 10 Pro、Enterprise、また Enterprise LTSB エディション

### <a name="minimum-system-requirements"></a>最少システム要件

-   4 GB の RAM
-   コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
-   少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

### <a name="recommended-system-requirements"></a>推奨システム要件

-   6 GB の RAM
-   コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)
-   少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

## <a name="connector-requirements"></a>コネクタの要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Connector for Microsoft Dynamics AX には、**Async Server Connector service** および **Real-time service for Dynamics AX 2012 R3** の 2 つのインストーラーがあります。
-   どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   次のオペレーティング システムでは、両方のコンポーネントがサポートされています。
    -   Windows 7 Professional、Enterprise、また Ultimate エディション
    -   Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション
    -   Windows 10 Pro、Enterprise、また Enterprise LTSB エディション
    -   Windows Server 2012 R2、Windows Server 2016

### <a name="minimum-system-requirements"></a>最少システム要件

-   2 GB の RAM、4 GB の RAM 推奨
-   コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
-   少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件
ローカル仮想マシン (VM) の開発要件については、[オンプレミス実行の VM](../dev-tools/access-instances.md) を参照してください。

# <a name="system-requirements-for-on-premises-deployments"></a>オンプレミス配置のシステム要件

## <a name="network-requirements"></a>ネットワーク要件
Finance and Operations (オンプレミス) は、インターネット プロトコル バージョン 4 (IPv4) またはインターネット プロトコル バージョン 6 (IPv6) を使用するネットワークで処理できます。 システムを計画し、および次のガイドラインを使用する場合には、ネットワーク環境を検討してください。

### <a name="network-response-time"></a>ネットワークの応答時間
次の表では、Web ブラウザーと Application Object Server (AOS) の間の接続およびオンプレミス システムでの AOS とデータベースの間の接続のネットワークの最小要件を一覧表示します。

| 先頭値     | Web ブラウザから AOS へ | AOS からデータベースへ                                            |
|-----------|--------------------|------------------------------------------------------------|
| 帯域幅 | 50 KBps ユーザー単位   | 100 MBps                                                   |
| 待機時間   | < 250 ～ 300 ms       | < 1 ms (LAN のみ)。 AOS およびデータベースは、同一配置である必要があります。 |

- Finance and Operations (オンプレミス) は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントから Finance and Operations をホストするデータ センターまでの待機時間のことです。
- Finance and Operations (オンプレミス) の帯域幅の要件はシナリオによって異なります。 一般的なシナリオでは、ブラウザーおよび Finance and Operations サーバーの間に 1 秒あたり 50 キロバイト (KBps) 以上の帯域幅が必要です。 ただし、大がかりなカスタマイズを必要とするワークスペースやシナリオなど、高度な伝送データ要件があるシナリオでは、帯域幅を増やすことが推奨され、使用によって異なります。
AOS および SQL Server データベースが異なるデータ センターにある配置はサポートされていません。 AOS および SQL Server データベースは、同一配置である必要があります。 一般に、Finance and Operations は、ブラウザーからサーバーへのラウンド トリップを減らすために最適化されます。 ブラウザー クライアントからデータ センターへのラウンド トリップの数は各ユーザーの操作ごとに 0 または 1 であり、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 特定のケースでのパフォーマンスの最良の指標として、Finance and Operations 以外の環境に対する実時間シミュレーションを使用することをお勧めします。 

### <a name="lan-environments"></a>LAN 環境
ローカル エリア ネットワーク (LAN) 環境では、Microsoft Windows Server の Microsoft Remote Desktop は、Finance and Operations に接続する必要はありません。 ただし、サーバーの配置を構成する VM 上でのサービス操作には必要な場合があります。

### <a name="wan-environments"></a>WAN 環境
広域ネットワーク (WAN) 環境では、Windows Server の Remote Desktop は、Finance and Operations に接続する必要はありません。

### <a name="internet-connectivity-requirements"></a>インターネット接続要件
Finance and Operations (オンプレミス) は、エンド ユーザーのワーク ステーションからのインターネット接続を必要としません。 ただし、一部の機能はインターネット接続なしでは利用できません。

| ブラウザー クライアント | インターネット接続のないイントラネット シナリオは、オンプレミス配置オプションの設計ポイントです。 LCS のヘルプおよびタスク ガイド ライブラリなどのクラウド サービスを必要とする一部の機能は利用できません。 |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| サーバー         | AOS または Service Fabric 層は、LCS と通信できる必要があります。 オンプレミス ブラウザ ベースのクライアントには、インターネットへのアクセスは不要です。                                                                                |
| テレメトリ      | 接続に長時間の障害があると、テレメトリ データが失われる可能性があります。 LCS への接続の中断は、オンプレミスのアプリケーション機能に影響を与えません。                                                |
| LCS            | 配置、コードの配置、およびサービス操作には、LCS への接続が必要です。                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>クラウドへのテレメトリ データの転送
ほとんどのテレメトリはローカルに保存され、Microsoft Windows のイベント ビューアーを使用してアクセスできます。 テレメトリ イベントの小さなサブセットは、診断のためにクラウド内の Microsoft テレメトリ パイプラインに転送されます。 顧客データおよびエンド ユーザーの識別可能なデータは、Microsoft に送信されたテレメトリの一部ではありません。 VM 名は、LCS ポータルからの環境管理および診断を支援するために Microsoft に送信されます。

## <a name="domain-requirements"></a>ドメイン要件
Finance and Operations (オンプレミス) をインストールする場合は、次のドメイン要件を検討してください:

- Finance and Operations (オンプレミス) コンポーネントをホストする仮想マシンは、Active Directory ドメインに属している必要があります。 Active Directory ドメイン サービス (AD DS) は、ネイティブ モードで構成する必要があります。
- Finance and Operations (オンプレミス) コンポーネントを実行する仮想マシンは、Active Directory ドメイン サービスで構成された相互アクセスをする必要があります。 
- ドメイン コントローラは、Microsoft Windows Server 2016 で実行する必要があります。

## <a name="hardware-requirements"></a>ハードウェア要件
このセクションでは、Finance and Operations (オンプレミス) の実行に必要なハードウェアについて説明します。
システム構成、データ構成、および使用するアプリケーションおよび機能に基づいて、実際のハードウェア要件が異なります。 Finance and Operations (オンプレミス) のための適切なハードウェアの選択に影響を与える要因のいくつかを以下に示します:

- 時間あたりのトランザクション数。
- 同時ユーザー数。

## <a name="minimum-infrastructure-requirements"></a>最小限のインフラストラクチャ要件
Finance and Operations (オンプレミス) では、Microsoft Azure Service Fabric を使用して、AOS、バッチ、データ管理、Management reporter、および環境オーケストレータ サービスをホストします。 Microsoft SQL Server Reporting Services (SSRS) は、Service Fabric クラスターではホストされません。
SQL Server は、生産用として少なくとも 2 つのノードを持つ高可用性 HADRON 設定で設定する必要があります。
次の図は、Service Fabric クラスター内のノードの最小推奨数を示しています。

[![Service Fabric クラスターの推奨されるノード数](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>プロセッサおよび RAM 要件
次の表では、この配置オプションを実行するために必要な役割ごとに求められるプロセッサの数およびランダムアクセス メモリ (RAM) の量を示します。 詳細については、Service Fabric スタンドアロン クラスターの最小要件の推奨事項である [Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) を読んでください。

> [!NOTE]
> その他の Microsoft ソフトウェアが同じコンピューターにインストールされている場合、システムはそのソフトウェアのハードウェア要件も満たす必要があります。 AOS と同じコンピュータ上の他のサーバー アプリケーションを 1 ギガバイト (GB) の RAM に制限することをお勧めします。

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

**生産およびサンド ボックス配置用の最小サイズ設定の見積**\*

| トポロジ                                  | 役割                          | インスタンスの数 |
|-------------------------------------------|-------------------------------|---------------------|
| 生産                                | AOS (データ管理、バッチ)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | オーケストレータ\*\*                | 3                   |
| サンドボックス                                   | AOS,データ管理、バッチ   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | オーケストレータ                  | 3                   |
| [*生産およびサンドボックス トポロジの集計*] |                               | 16                  |

\*これらの数値はプレビュー ユーザーによって検証されており、そのフィードバックに基づいて必要に応じて調整されます。

\*\*オーケストレータはプライマリ ノード タイプとして指定され、および Service Fabric サービスの実行にも使用されます。

[**バックエンド SQL Server および AD の初期推定値**]

[![バック エンド SQL サーバーおよび AD の初期推定値](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server サイズは、ワークロードに大きく依存します。 詳細については、「[オンプレミス環境のハードウェアのサイズ変更](#Hardware-sizing-for-on-premises-environments) セクション」を参照してください。

## <a name="storage"></a>保管

- **AOS** - Finance and Operations (オンプレミス) を使用して、サーバー メッセージ ブロック (SMB) 3.0 共有に構造化されていないデータを格納します。 詳細については、「[Windows Server 2016 の Storage Spaces Direct](/windows-server/storage/storage-spaces/storage-spaces-direct-overview)」を参照してください。
- **SQL** – 実行可能なオプション:
    - 高可用性ソリッドステート ドライブ (SSD) の設定。
    - OLTP スループット用に最適化されたストレージ エリア ネットワーク (SAN)。
    - 高パフォーマンス直接接続ストレージ (DAS) 
- **SQL およびデータの管理 IOPS** – データ管理および SQL Server の両方のストレージには、少なくとも 1 秒あたり 2,000 回の入出力操作 (IOPS) が必要です。 生産 IOPS はさまざまな要因に依存します。 詳細については、「オンプレミス環境のハードウェアのサイズ変更」セクションを参照してください。 
- **仮想マシン IOPS** – 各仮想マシンには、少なくとも 100 の書き込み IOPS が必要です。

## <a name="virtual-host-requirements"></a>仮想ホストの要件
Finance and Operations (オンプレミス) 環境の仮想ホストを設定する場合は、次のガイドラインを参照してください: [Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) および [Service Fabric クラスターを説明する](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description)。 各仮想ホストには、サイズ変更されているインフラストラクチャ用のコアが十分にある必要があります。 SQL Server が物理ハードウェア上に存在し、その他のすべてが仮想化されている場合は、複数の高度な構成が可能です。 SQL Server が仮想化されている場合、ディスク サブシステムは高速 SAN または同等のものにする必要があります。 いずれの場合も、仮想ホストの基本設定が高可用性および重複であることを確認してください。 いずれの場合も、仮想化を使用する場合は、VM スナップショットを作成する必要はありません。

## <a name="software-requirements-for-all-server-computers"></a>すべてのサーバー コンピュータのソフトウェア要件
Finance and Operations (オンプレミス) コンポーネントをインストールする前に、次のソフトウェアがコンピュータに存在している必要があります:

- Microsoft .NET Framework Version 4.5.1 またはそれ以上
- Service Fabric の詳細については、「[Service Fabric クラスターの計画および準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)」を参照してください。

## <a name="supported-server-operating-systems"></a>サポートされるサーバー オペレーティング システム
次の表では、Finance and Operations コンポーネントでサポートされているサーバー オペレーティング システムを示します。

| オペレーティング システム                                     | 摘要                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter または Standard | これらの要件は、AOS をホストするデータベースおよび Service Fabric クラスターに対するものです。 |

## <a name="software-requirements-for-database-servers"></a>データベース サーバーのソフトウェア要件

- 64 ビット バージョンの SQL Server 2016 のみがサポートされています。
- 実稼動環境では、使用している SQL Server のバージョンの最新の累積的な更新プログラム (CU) をインストールすることをお勧めします。
- Finance and Operations (オンプレミス) では、大文字小文字を区別しない、アクセントを区別する、カナを区別する、および幅を区別しない Unicode 照合順序をサポートします。 照合順序は、AOS インスタンスを実行しているコンピュータの Windows ロケールと一致する必要があります。 新しいインストールを設定する場合は、SQL Server 照合の代わりに Windows 照合を選択することをお勧めします。 SQL Server データベースの照合順序を選択する方法の詳細については、「[SQL Server に関するドキュメント](/sql/sql-server/sql-server-technical-documentation)」を参照してください。
次の表では、Finance and Operations データベースでサポートされている SQL Server バージョンを一覧表示します。 詳細については、「[SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016) の最小ハードウェア要件」を参照してください。

| 必要量                                                      | 摘要                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard エディションまたは Enterprise エディション | SQL Server 2016 のハードウェア要件については、「[SQL Server 2016 インストール用のハードウェアおよびソフトウェア要件](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server)」を参照してください。 |

## <a name="software-requirements-for-client-computers"></a>クライアント コンピュータのソフトウェア要件
Finance and Operations Web アプリケーションは、HTML5.0 準拠の Web ブラウザーを備えた任意のデバイス上で実行できます。 Microsoft が確認した特定のデバイス / ブラウザーの組み合わせは次のとおりです:

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)
- Mac OS X 10.10 (Yosemite)、 10.11 (El Capitan) または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)

## <a name="software-requirements-for-active-directory-federation-services"></a>Active Directory フェデレーション サービスのソフトウェア要件 
Windows Server 2016 での Active Directory Federation Services (AD FS)

ドメイン コントローラは、2012 R2 以降のドメイン機能レベルの Windows Server 2012 R2 以降である必要があります

ドメイン機能レベルの詳細については、以下を参照してください。 
- [Active Directory 機能レベルとは](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Active Directory ドメイン サービス機能のレベルを理解する](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>小売コンポーネントのハードウェアおよびソフトウェア要件
現時点では、Finance and Operations (オンプレミス) には小売コンポーネントは含まれていません。

<a name="see-also"></a>参照
--------

[Dynamics 365 for Finance and Operations, Enterprise Edition の評価版を取得](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

