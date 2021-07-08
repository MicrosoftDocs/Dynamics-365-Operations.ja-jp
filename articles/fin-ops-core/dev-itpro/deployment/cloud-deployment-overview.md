---
title: クラウド展開の概要
description: このトピックでは、クラウド環境とサブスクリプション、誰がどのタスクを実行できるか、および管理する必要があるデータとカスタマイズについて説明します。
author: LaneSwenka
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: bd30a8906b09f899a30c9b069dc0b76c84bf5c1c
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216600"
---
# <a name="cloud-deployment-overview"></a>クラウド配置の概要

[!include [banner](../includes/banner.md)]
 
Finance and Operations アプリをクラウドに展開するにあたって、Microsoft と作業をするには、展開先の環境とサブスクリプションについての理解と、タスクの可能が実行な担当者と、管理の必要があるデータとカスタマイズについて理解している必要があります。 配置と実装の高速化に役立つ Full Microsoft FastTrack for Dynamics 365 に登録することをお勧めします。このプログラムは、より迅速なビジネス価値の実現を支援するトレーニングとコンサルティングを提供します。 詳細については、 [Microsoft FastTrack](/dynamics365/fasttrack/) を参照してください。 代わりに Essentials FastTrack プログラムの使用を選択すると、実装プロジェクトの管理に役立つ Lifecycle Services (LCS) の実装プロジェクト方法を使用します。 

## <a name="customer-lifecycle-subscriptions-and-environment-types"></a>顧客のライフ サイクル、サブスクリプション、デプロイのトポロジ
Microsoft は、すべての顧客がすべてのクラウド配置に対して次と類似するライフサイクルに従うため、各フェーズで別の環境トポロジが必要になると想定しています。 

- 評価
- 必要に応じてカスタマイズを行います。
- マスターデータまたはトランザクション データがないモジュール構成のみを含む "ゴールデン構成" 環境を使用します。  これは、データ移行テストと最終的な本稼働にむけたベースラインとなります。
- レベル 1 サンドボックス (開発またはテスト環境) におけるカスタマイズとパートナー ソリューションのインストールおよびテストします。 
- レベル 2 サンドボックス環境におけるカスタマイズ、パートナー ソリューション、データ構成のテストします。
- 可用性の高い運用環境にカスタマイズとデータ構成をデプロイします。

プロジェクトのいくつかのフェーズでは、すべての環境を一度に実行することができます。 既定のライセンスおよび使用可能な層の詳細については、[Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

クラウドがホストする用語、または Microsoft サブスクリプションがあることがわかります。 *クラウドでホストされるサブスクリプション* とは、顧客やパートナーが各自の Azure サブスクリプションを使用して、評価や開発の目的のためだけに Finance and Operations アプリをデプロイすることを意味します。 顧客やパートナーは、Azure 価格リストに基づいて Azure サブスクリプションに展開されるリソースに対して支払います。 *Microsoft サブスクリプション* とは、顧客が Finance and Operations ライセンスを購入し、Microsoft が管理する Azure サブスクリプションに環境をデプロイできることを意味します。そのため、顧客への Azure からの別個の請求は発生しません。 

各 エンタープライズには、既定で 2 つの環境が含まれています。
- ユーザー受け入れテスト (UAT) に使用する、階層 2 サンド ボックス (マルチ ボックス環境)。
- 高い可用性 (HA) を備えた実稼働環境。 

追加の環境は、アドオンとして購入する場合があります。 ライセンスや Microsoft Dynamics 365 の内容についての詳細情報は、 [Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

ライフサイクルが使用可能な環境にどうマップするかを次に示します。  Lifecycle Services プロジェクトにすでに環境がデプロイされている場合は、各環境の詳細ページに環境のタイプと環境のサブタイプが表示されます。

| ライフサイクルのフェーズ      | 環境の階層         | サブスクリプション            | 環境タイプ                 | 環境のサブタイプ 
|-------------------------------|---------------------------------|--------------------------------------|---------------------------------------------|---------------------------------------------|
| 評価および分析       | 階層 1 のサンドボックス | クラウド ホスト | 顧客管理 | デモ
| カスタマイズ                     | 階層 1 のサンドボックス | クラウド ホスト または VHD | 顧客管理 | 開発
| ゴールデン構成          | 階層 1 のサンドボックス | クラウド ホスト | 顧客管理 | 開発
| ユーザー受け入れテスト (UAT) | 階層 2-5 のサンドボックス | Microsoft                 | Microsoft 管理、またはセルフサービス | 適用できません
| Go live                       | 実稼働 | Microsoft                    | Microsoft 管理、またはセルフサービス | 適用できません     

*環境のパフォーマンスを向上させるために、階層 2-5 を購入することも可能です。階層が増えるほど、演算およびデータベースの能力が確保されます。*
*セルフサービス環境タイプの詳細については、[セルフサービス デプロイメントの概要](infrastructure-stack.md) を参照してください。*

> [!IMPORTANT]
> 階層 1 のサンドボックス環境は、2020 年 11 月以降、Microsoft によって管理されなくなりました。 階層 1 環境は、デモ、構築、開発の目的で、Lifecycle Services (LCS) から顧客の Azure サブスクリプションに直接配置できます。

### <a name="environment-lifecycle-operations"></a>環境ライフサイクルの操作
Lifecycle Services における環境管理者またはプロジェクト所有者のロールを持つユーザーは、それぞれの環境に対してさまざまなライフサイクルの操作を実行できます。  多くの場合、これらの操作には、タスクが完了するまでの環境でのダウンタイムが含まれます。  これらの操作は、**管理** ボタンの下または横に配置され、各環境の詳細ページに表示されます。

| ライフサイクル操作 | 説明 | 詳細
|---------------------|-------------|------------|
| ソフトウェアの適用 | Microsoft 更新プログラム、ISV ソリューション、または独自のカスタマイズ パッケージをインストールします。 | [クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)
| アクセスを有効にする | リモート デスクトップやデータベースへのアクセスに使用する IP のリストを許可する | このトピックで後述する[リモートデスクトップ](cloud-deployment-overview.md#remote-desktop)のセクションを参照してください
| サービスの再起動 | ご利用の環境のコンポーネントを再起動する機能 | [環境サービスの再開](../lifecycle-services/restart-environment-services.md)
| データベースの移動 | 完全データライフサイクル管理 | [データベース移動操作](../database/dbmovement-operations.md)
| メンテナンス モード | 管理者のみのアクセスで構成を変更する機能 | [メンテナンス モード](../sysadmin/maintenance-mode.md)
| アップグレード | 7. x から最新バージョンへのアップグレード コードとデータ | [最新の更新プログラムに移行するためのプロセス](../migration-upgrade/upgrade-latest-update.md)
| 割り当て解除 | 使用されていない環境をオフにしたり、失敗したアクションのトラブルシューティングを行ったりする機能 | 適用できません
| 開始 | 環境の使用を有効にする機能 | 適用できません
| 消去 | 既に割り当てを解除された環境を削除する機能 | 適用できません


## <a name="security-and-compliance"></a>セキュリティとコンプライアンス
Finance and Operations は、PA-DSS 3.1 認定を受けています。これは、コンポーネント間のすべての通信が何もしなくても保護されることを意味します。 

Microsoft Azure のすべての Finance and Operations フロント エンド仮想マシンは、TLS 1.2 のみを受け入れるように配置時に構成されます。 

> [!IMPORTANT]
> 購入したアドオン サンドボックスを含む Microsoft 管理対象のサンドボックスに管理者権限を持つお客様は、次のガイドラインに従わなければなりません。
> - 既定では、レベル 1 - 5 のすべてのサンドボックスで自動 Windows の更新が有効になっているため、無効にしないでください。 これにより、Microsoft がセキュリティまたは重大なインフラストラクチャの更新を自分の環境にプッシュするたびに、環境に最新の更新プログラムが適用され、毎月 Microsoft からリリースされたオペレーティング システムの修正プログラムが更新されます。  
> - これらの環境の管理者パスワードは、変更しないでください。 変更済管理者パスワードをもつ環境では、Microsoft がフラグを設定します。 Microsoft は、管理者パスワードをリセットする権利を保有し、実際にリセットします。  
> - Microsoft 管理対象 VM に新しいユーザー アカウントを追加することは、許可されていません。 Microsoft は、通知することなく新しく追加されたユーザー アカウントを削除する権利を保有し、実際に削除します。

> Finance and Operations は、現時点では FedRAMP ATO の対象外です。 Finance and Operations を米国でプロビジョニングする場合、[Dynamics 365 の国際的な可用性](https://www.microsoft.com/trustcenter/privacy/dynamics365-finance-operations) で説明されているように、顧客の保存データは米国のデータ センターで保管されます。 Finance and Operations では、その他の Dynamics 365 US Government や Microsoft 365 GCC コンプライアンス属性 (米国の検査担当者によるアクセス、および CJIS と IRS 1075 のサポートなど) には対応していません。 

## <a name="remote-desktop"></a>リモート デスクトップ

### <a name="microsoft-managed-environments"></a>Microsoft が管理する環境

> [!WARNING]
> Microsoft は、顧客およびパートナーがリモート デスクトップを使用できないようにします。  各環境では、最初に管理者アクセス権が削除されますが、仮想マシンへの管理者以外のアクセスは許可されています。 その後は、すべてのアクセスが削除されます。 この段階的な削除の各手順では、各環境で設定された通知リストにメールが送信されます。 リモート デスクトップ アクセスは、2020 年の 11 月までに削除されます。

顧客は、Microsoft リモート デスクトップ (RDP) を介して、仮想マシン (VM) に接続するための追加設定を完了する必要があります。 この追加の設定は、 レベル 1 〜 レベル 5 のサンドボックスとアドオンを含む、Microsoft が管理するすべての環境に適用されます。 レベル 1 からレベル 5 のサンドボックス環境に接続するには、明示的に組織の IP アドレス空間からのアクセスを有効 (セーフ リスト化) にする必要があります。 これは、リモート デスクトップを介して仮想マシンに接続するために使用される IP アドレス スペースを入力できる **環境ページ** (**Maintain** > **Enable Access**) にアクセスできる Lifecycle Services (LCS) ユーザーによって実行できます。 アクセス ルールは、単一の IP アドレス (例: 10.10.10.10) または IP アドレスの範囲 (例: 192.168.1.0/24) です。 セミコロン (;) で区切られたリスト (例: 10.10.10.10;20.20.20.20;192.168.1.0/24) として複数のエントリを一度に追加する場合があります。 これらのエントリは、環境の仮想ネットワークに関連付けられている Azure ネットワーク セキュリティ グループの設定に使用されます。 詳細については、[セキュリティ ポリシー](/azure/virtual-network/security-overview#security-rules)を参照してください。

> [!IMPORTANT]
> 顧客は、上記の明示的な IP セーフ リストのルールを通じて RDP エンドポイントを確実に保護する必要があります。 IP セーフ リストのルールは、次の条件に準拠する必要があります。
> - IP セーフ リストのルールには、アスタリスク/ゼロを使用することはできません。
> - ワイド IP アドレスの範囲は使用しないでください。
> - IP アドレス範囲は、顧客の CORPNET に限定する必要があります。 
> - 顧客の CORPNET (ホーム オフィスなど) 外のコンピューターをサンドボックス環境へ接続するために使用する場合は、サンドボックス環境へ接続するために使用するコンピューターの特定の IP アドレスのみを追加する必要があります。
> - Azure データセンター IP アドレス範囲を追加しないでください。
> - コーヒー店の場所などで、パブリック IP アドレスを追加しないでください。     
> - 使用されていない IP セーフ リストのルールは削除する必要があります。 環境 IP におけるセーフ リストのルールを定期的に確認することを推奨します。

> Microsoft は Microsoft 管理環境で定期的なテストを実行して、環境が十分に制限されていることを検証します。
> Microsoft は、上記のガイドラインに違反した IP アドレスのセーフ リストのルールを、通知することなく直ちに削除する権利を保有しています。
 
### <a name="partnercustomer-managed-environments"></a>パートナー/お客様の管理環境 
既定では、Microsoft によって管理されていないすべての環境でリモート デスクトップが有効になります。 顧客は自分たちのサブスクリプションに所属している環境へのアクセスを制限することをお勧めします。 これは、Azure ポータルの環境でネットワーク セキュリティ グループのルールを直接設定することで実行できます。

## <a name="windows-remoting-winrm"></a>Windows Remoting (WinRM)
Windows Remoting (WinRM) はすべての環境で無効です。 Azure ポータルを使用して、サブスクリプションに属する環境で WinRM を有効にすることはできますが、これを行わないことを強くお勧めします。

> [!WARNING]
> WinRM を有効にするための例外は、Microsoft が管理する環境では許可されません。 

## <a name="availability"></a>使用可能性
Finance and Operations アプリの保証稼働時間は 99.9% です。 計画的なダウンタイムは月 1 回発生し、8 時間以内に終了します。 ダウンタイム中に完了した作業は必ずしも 8 時間かかるとは限らないため、お客様の環境がダウンすると予想される時間を常にお知らせします。 詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../lifecycle-services/lcs-support.md) を参照してください。

### <a name="high-availability-features"></a>高可用性機能
サービスの可用性を確保するため、すべての運用環境はデフォルトの Azure 高可用性 (HA) 機能を使用して保護されています。 HA 機能はデータ センター内の単一のノードの失敗により引き起こされるダウンタイムを回避する方法を提供し、DR 機能はデータ センター全体に広く影響を及ぼす機能停止を防止します。 単一障害点イベントを防止するために、Azure 使用可能性セットが使用されます。 Azure の可用性セットの詳細については、[可用性ゾーンを使用してデータセンター レベルの障害から保護する](/azure/virtual-machines/windows/manage-availability#use-availability-zones-to-protect-from-datacenter-level-failures)を参照してください。
データベースの高可用性は Azure SQL を通してサポートされます。 詳細については、[Azure SQL データベースの事業継続性の概要](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview) を参照してください。

#### <a name="database-backup-retention"></a>データベースのバックアップ保持
Microsoft 管理対象環境またはセルフサービスの階層 2 ~ 5 環境のデータベースでは、Azure SQL によって数分おきに自動バックアップが実行されます。 これらのバックアップは、Lifecycle Services の時点での復元機能を過去 14 日間まで使用することで復元できます。 実稼働タイプ環境の場合、バックアップを最大 28 日間復元できます。 階層 1 または顧客管理環境の場合は、データベース バックアップは自動的ではなく、必要に応じて手動で実行する必要があります。

### <a name="disaster-recovery-features"></a>障害復旧の機能
実稼動環境は、以下のものを含む Azure 障害復旧サポートで構成されます。
- Azure SQL のアクティブ geo レプリケーションは、実稼働環境の Finance and Operations データベースに対して構成されています。 SQL レプリケーションの詳細については、[geo レプリケーションとフェールオーバー グループの比較](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#compare-geo-replication-with-failover-groups) を参照してください。 
- 他の Azure リージョンでの Azure blob storage (ドキュメントの添付ファイルを含む) のジオ重複コピー。 詳細については、[Azure 冗長性](/azure/storage/common/storage-redundancy) を参照してください。
- Azure SQL および Azure ブログ記憶域レプリケーションの同じセカンダリ地域。  

プライマリのデータ格納場所のみレプリケーションがサポートされます。 Financial Reporting サービスおよびエンティティ格納データベースは、プライマリ データベースから変換されたデータを使用し、リカバリ サイトの設定および Finance and Operations サービスの開始後に生成する必要があります。 

## <a name="service-availability-in-azure-regions"></a>Azure リージョンにおけるサービスの可用性
Dynamics Lifecycle Services (LCS) を使用して、Microsoft Azure データ センターのサブセットに Finance and Operations アプリを展開できます。 Azure は一般に世界中のデータセンターや地理的な場所で利用可能です。 Finance and Operations アプリでは、顧客は自分の顧客データが格納される地域またはデータセンターを指定することができます。 Microsoft は、データの持続性のためにデータを他の領域に複製する場合がありますが、地理的な場所の外部に顧客データを複製または移動しません。 詳細については、[サービス説明のホワイト ペーパー](https://aka.ms/D365-Cloud-Service-Operations)をご覧ください。

> [!IMPORTANT]
> 顧客データがどこに格納されているかに関係なく、マイクロソフトは顧客またはエンドユーザーがアクセスできる場所を管理したり制限したりしません。
詳細については、[Dynamics 365 の国際的な可用性](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location) を参照してください。

### <a name="upcoming-changes-to-region-availability"></a>利用可能なリージョンに関する将来の変更
Dynamics 365 ソリューションは、複数のサービスで構成されています。 Dynamics 365 アプリケーション、Power Platform および Azure サービスがそれぞれ依存している状況からしても、サービスに関して必要となるマトリックスは非常に大きくなり、拡大しています。 当社は必要なサービスのポートフォリオ全体を確実に利用していただけるようにするため、世界中のデータセンター リージョンのサブセットを選択する戦略を固めてきました。 当社の計画は、ソリューションにおけるコンポーネント サービス間の遅延を最小限に抑えることを目的としており、このため、指定された各データセンターにおいて、利用可能なサービスのポートフォリオ全体を用意することに重点をおいています。

加えて、Finance and Operations アーキテクチャでは、柔軟性と信頼性を高め、よりシームレスな保守が行えるように、セルフサービスで構築するための機能拡張が行われています。 より少数のデータセンターで、セルフサービスでの展開をより十分に活用していただくことにより、お客様は材料効率を高めることができます。 この移行には、Azure リージョンのサブセットを選択することによる利点もあります。 その趣旨で、Finance and Operations アプリの利用可能な地域は、すべての新しいプロジェクトに対して、<strong>北米の米国東部、米国西部、および米国中部に制限されることになります</strong>。 サポートされている国と地域についての最新の一覧は、[Dynamics 365 の国際的な可用性](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location)を参照してください。

米国東部 2、米国西部 2、米国中西部、米国中北部、米国中南部へのサポートは、現在これらの地域で Microsoft マネージド環境のデータを保存しているプロジェクトと環境で引き続き利用できます。 

> [!Note]
> 2020 年 10 月 19 日より、Microsoft はお客様と協力して、適切なデータ センターにデータを移動します。 これは、段階的なアプローチで実施されます。 対象のお客様は、サポートされるリージョンにデータが移行される前に、事前の通知を受信します。

Dynamics 365 または Power Platform ファミリーの一部ではないが、Dynamics 365 および Power Platform サービスに近いものを必要とするお客様のワークロードが他にもある場合 、Microsoft は、お客様と協力して移行全体の計画を調整します。 詳細については、[クラウド配置の概要: よく寄せられる質問](cloud-deployment-overview.md#frequently-asked-questions) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-does-the-status-display-maintenance-on-my-environment-in-lcs"></a>LCS の環境で状態が [メンテナンス] と表示されるのはなぜですか。
最高のエクスペリエンスとパフォーマンスを提供するために、Microsoft は環境の保守作業を行います。 これらの一部の保守作業中に、環境の状態として次のいずれかの状態が表示される場合があります。

- メンテナンスの準備中
- メンテナンスの準備完了
- メンテナンス中

環境がこの状態になり、状態が [配置済] に戻るまでは、パッケージ アプリケーションなどのライフサイクル操作を実行することができません。 Finance and Operations アプリに対する影響はありません。 ユーザーはサービスが中断されることなく、通常の操作を続行できます。 管理操作により環境がこの状態になる前に電子メール通知が送信されます。

### <a name="how-do-i-connect-to-the-sql-database-on-my-sandbox-environment"></a>サンドボックス環境で SQL データベースに接続するにはどうすればよいですか?
サンドボックス環境で SQL データベースに接続するには、[ジャストインタイムのアクセスを有効にする](../database/database-just-in-time-JIT-access.md) の手順に従ってください。

### <a name="how-do-i-access-a-development-instance"></a>開発インスタンスにどのようにアクセスしますか。
開発インスタンスへのアクセス、オンプレミス開発 VM の構成、開発者と管理者の構成設定を確認する方法については、 [開発環境の展開とアクセス](../dev-tools/access-instances.md) を参照してください。

### <a name="how-do-i-deploy-a-demo-environment"></a>デモ環境をどのように展開しますか?
デモ環境には、Microsoft のデモ データのみが含まれています。 デモ環境を使用して既定のフィーチャーと機能を参照することができます。 詳細については、「[デモ環境の配置](deploy-demo-environment.md)」を参照してください。

### <a name="how-do-i-move-my-customizations-between-environments"></a>環境間でカスタマイズを移動するにはどうすればよいですか。
カスタマイズを開発からサンドボックスまたは実稼動環境に移行する方法については、 [配置可能なモデルのパッケージの作成](../deployment/create-apply-deployable-package.md) を参照してください。

### <a name="can-i-bring-my-own-domain-name"></a>所有のドメイン名を使用することができますか。
Azure Active Directory (AAD) が実行中で、AAD インスタンスの管理者が Finance and Operations アプリを AAD を使用して有効にした場合、自分のドメイン名を使用することができます。 これは通常、ライセンスを購入した後、オフィスの電子メールで行われます。 オファーを承諾するリンクをクリックすると、AAD がユーザーに対して設定されます。

### <a name="can-i-add-guest-aad-accounts-as-users"></a>ゲスト AAD アカウントをユーザーとして追加できますか。
Azure Active Directory 内で適切に AAD アカウントを構成して、AAD 内で Finance and Operations アプリを有効にした場合は、ゲストの AAD アカウントを追加することができます。 

### <a name="why-am-i-no-longer-able-to-see-the-private-aos-machines-in-one-or-more-of-my-tier-2-through-tier-5-sandbox-environments"></a>プライベート AOS マシンを 階層 2 から階層 5 のサンドボックス環境の 1 つ以上で表示できなくなったのはなぜですか?
Private AOS VM は、かつて AOS と BI コンピューター間の通信を保護する必要があったため、環境構成の一部でした。 最新の更新プログラムでは、AOS と BI マシン間のすべての通信は直接セキュリティで保護され、中間プライベート AOS 機械は不要になりました。 したがって、プライベート AOS マシンを削除する段階にあります。 バッチでマシンを削除しているので、環境の一部だけがプライベート AOS 機械を削除したことが判明することがあります。 この変更は、機能性やセキュリティにいかなる影響も及ぼさず、お客様には透明になります。

### <a name="why-am-i-no-longer-able-to-remote-desktop-into-one-or-more-of-my-tier-1-through-tier-5-microsoft-managed-sandbox-environments"></a>リモート デスクトップを自分の階層 1 から階層 5 のいずれかの Microsoft 管理サンドボックス環境で表示することができなくなったのはなぜですか?
Microsoft が管理する階層 1 から階層 5 のサンドボックス環境では、 リモート デスクトップ管理のエンド ポイントを特定の IP アドレス セット (セーフ リスト) に制限する必要があります。 Microsoft は、定期的に環境が十分に制限されていることを検証します。 Microsoft は、上記のガイドラインに違反した IP アドレスのセーフ リストのルールを予告なしに直ちに削除する権利を保有しています。 これらの理由の 1 つのためにデスクトップを環境にリモートすることができない場合があります。 

- ご自身が現在使用している IP アドレスはセーフ リストに含まれません。
- ご利用の IP は、セーフ リストに記載されている IP アドレスから変更されています。 
- Microsoft は、ガイドラインに違反していたため、ご利用の IP アドレスを含むルールをセーフリストから削除しました。

環境へのアクセスを回復するには、接続先のコンピュータの IP アドレスを追加する必要があります。 これを行うには、このトピック前半の[リモート デスクトップ](#remote-desktop) セクションの手順を実行します。

### <a name="when-will-the-availability-of-reduced-regions-go-into-effect-for-new-onboarding"></a>削減された領域の可用性は、いつ新しいオンボードに有効になりますか?
2020 年 8 月 1 日から、Finance and Operations の新しいプロジェクトは次の地域にオンボードされます。

- 米国東部
- 米国西部
- 米国中部
 > [!IMPORTANT]
 > 米国中部は、2021 年 4 月 1 日から始まるセルフサービス移行のオプションではなくなりました。
-   米国東部 2
-   米国西部 2
-   西中央アメリカ
-   米国中北部
-   米国中南部

このことは、格納データが 2020 年 8 月以前に非推奨領域に保有されている環境には影響しません。 近い将来、非推奨の地域の顧客を削減した領域に移動するための移行計画があります。

### <a name="im-unable-to-redeploy-an-environment-after-deleting-it-the-environment-slot-is-missing"></a>環境を削除すると再配置ができません、環境スロットが欠落しています。 
これは、ライセンスが期限切れになったためです。つまり、環境スロットを取得するために必要な最低限のライセンスが不要になったことを意味します。  [サブスクリプションのステータス](../../fin-ops/get-started/subscription-overview.md#how-can-i-find-the-subscription-status) を確認し、有効期限が切れたライセンスを再開してから、再配置を有効にしてください。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
