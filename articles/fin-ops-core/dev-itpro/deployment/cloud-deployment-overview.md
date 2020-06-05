---
title: クラウド展開の概要
description: このトピックでは、展開するクラウド環境とサブスクリプション、誰がどのタスクを実行できるか、および Finance and Operations アプリで管理する必要があるデータおよびカスタマイズについて説明します。
author: kfend
manager: AnnBe
ms.date: 05/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 860325872c7b1ec76ee45fbcd948d8cb26ae11ff
ms.sourcegitcommit: ed97db691b1bfb1e7db5827958f5d582fb1232fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2020
ms.locfileid: "3392323"
---
# <a name="cloud-deployment-overview"></a>クラウド配置の概要

[!include [banner](../includes/banner.md)]
 
Finance and Operations アプリをクラウドに展開するにあたって、Microsoft と作業をするには、展開先の環境とサブスクリプションについての理解と、タスクの可能が実行な担当者と、管理の必要があるデータとカスタマイズについて理解している必要があります。 配置と実装の高速化に役立つ Full Microsoft FastTrack for Dynamics 365 に登録することをお勧めします。このプログラムは、より迅速なビジネス価値の実現を支援するトレーニングとコンサルティングを提供します。 詳細については、 [Microsoft FastTrack](../../fin-ops/get-started/fasttrack-dynamics-365-overview.md) を参照してください。 代わりに Essentials FastTrack プログラムの使用を選択すると、実装プロジェクトの管理に役立つ Lifecycle Services (LCS) の実装プロジェクト方法を使用します。 

## <a name="customer-lifecycle-subscriptions-and-deployment-topologies"></a>顧客のライフ サイクル、サブスクリプション、および展開のトポロジ
Microsoft は、すべての顧客がすべてのクラウド配置に対して次と類似するライフサイクルに従うため、各フェーズで別の環境トポロジが必要になると想定しています。 

- 評価
- 必要に応じカスタマイズを行う
- レベル 1 サンドボックスでのカスタマイズおよびパートナー ソリューションのインストールとテスト (開発またはテスト環境) 
- レベル 2 サンドボックス環境のテストのカスタマイズ、パートナー ソリューション、データ構成
- 高可用性の運用環境にカスタマイズとデータ構成を展開する

プロジェクトのいくつかのフェーズでは、すべての環境を一度に実行することができます。 既定のライセンスおよび使用可能な層の詳細については、[Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

条件、顧客、パートナー、および Microsoft サブスクリプションについて聞く場合があります。 *顧客あるいはパートナー サブスクリプション* とは、顧客やパートナーが独自の Azure サブスクリプションをもって、評価と開発の目的のためだけに Finance and Operations アプリを配置することを意味します。 顧客やパートナーは、Azure 価格リストに基づいて Azure サブスクリプションに展開されるリソースに対して支払います。 *Microsoft サブスクリプション*とは、顧客が Finance and Operations ライセンスを購入し、Microsoft が管理する Azure サブスクリプションに環境を配置できることを意味します。これにより、顧客には Azure からの別個の請求はありません。 各 Enterprise オファーでは、既定で 3 つの環境が含まれています。 

- 1 つの階層 1 サンド ボックス (ここでは、開発またはビルド環境です)。
- ユーザー受け入れテスト (UAT) 用の、1 つの階層 2 サンド ボックス (マルチ ボックス環境) です。
- 高可用性 (HA) を備えた 1 つの実稼働環境。 この環境は、Microsoftによって管理され、運用されます。

追加の環境は、アドオンとして購入する場合があります。 ライセンスおよび Microsoft Dynamics 365 に何が含まれるかの詳細については、[Microsoft Dynamics 365 Enterprise edition ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。

ライフサイクルが使用可能な環境にどうマップするかを次に示します。

| ライフサイクルのフェーズ               | 環境                               | 定期売買                                        |
|-------------------------------|-------------------------------------------|-----------------------------------------------------|
| 評価および分析       | デモ、ワン ボックス                             | 顧客またはパートナーのサブスクリプション。                                |
| カスタマイズ                     | 開発/ビルド、1 つボックス                        | Microsoft サブスクリプション、パートナー/顧客サブスクリプション、またはローカル VM
| ユーザー受け入れテスト (UAT) | 第 2 層のサンド ボックス、マルチ ボックス環境 | Microsoft サブスクリプション                              |
| Go live                       | 生産、高可用性マルチボックス環境                    | Microsoft サブスクリプション                              |

## <a name="features-of-a-production-instance"></a>実稼働インスタンスの機能
実稼働インスタンスには、次の機能があります。

## <a name="security-and-compliance"></a>セキュリティとコンプライアンス
Finance and Operations は、PA-DSS 3.1 認定を受けています。これは、コンポーネント間のすべての通信が何もしなくても保護されることを意味します。 

Microsoft Azure のすべての Finance and Operations フロント エンド仮想マシンは、TLS 1.2 のみを受け入れるように配置時に構成されます。 

> [!IMPORTANT]
> 購入したアドオン サンドボックスを含む Microsoft 管理対象のサンドボックスに管理者権限を持つお客様は、次のガイドラインに従わなければなりません。
> - 既定では、レベル 1 - 5 のすべてのサンドボックスで自動 Windows の更新が有効になっているため、無効にしないでください。 これにより、Microsoft がセキュリティまたは重大なインフラストラクチャの更新を自分の環境にプッシュするたびに、環境に最新の更新プログラムが適用され、毎月 Microsoft からリリースされたオペレーティング システムの修正プログラムが更新されます。  
> - これらの環境の管理者パスワードは、変更しないでください。 変更済管理者パスワードをもつ環境では、Microsoft がフラグを設定します。 Microsoft は、管理者パスワードをリセットする権利を保有し、実際にリセットします。  
> - Microsoft 管理対象 VM に新しいユーザー アカウントを追加することは、許可されていません。 Microsoft は、通知することなく新しく追加されたユーザー アカウントを削除する権利を保有し、実際に削除します。

> [!IMPORTANT]
> Finance and Operations は、現時点では FedRAMP ATO の対象外です。 Finance and Operations を米国でプロビジョニングする場合、 [トラスト センター](https://www.microsoft.com/trustcenter/privacy/dynamics365-finance-operations)で説明されているように、残りのすべての顧客データは米国のデータ センターで保管されます。 Finance and Operations では、その他の Dynamics 365 US Government や Office 365 GCC コンプライアンス属性 (たとえば、米国の検査担当者によるアクセス、および CJIS と IRS 1075 のサポートなど) には対応していません。  

## <a name="remote-desktop"></a>リモート デスクトップ

### <a name="microsoft-managed-environments"></a>Microsoft が管理する環境
顧客は、Microsoft Remote Desktop (RDP) を介して、仮想マシン (VM) に接続するための追加セットアップを完了する必要があります。 この追加の設定は、 レベル 1 〜 レベル 5 のサンドボックスとアドオンを含む、Microsoft が管理するすべての環境に適用されます。 レベル 1 からレベル 5 のサンドボックス環境に接続するためには、明示的に組織の IP アドレス空間からのアクセスを有効にする (ホワイトリストする) 必要があります。 これは、リモート デスクトップを介して仮想マシンに接続するために使用される IP アドレス スペースを入力できる**環境ページ** (**Maintain** > **Enable Access**) にアクセスできる Lifecycle Services (LCS) ユーザーによって実行できます。 アクセス ルールは、単一の IP アドレス (例: 10.10.10.10) または IP アドレスの範囲 (例: 192.168.1.0/24) です。 セミコロン (;) で区切られたリスト (例: 10.10.10.10;20.20.20.20;192.168.1.0/24) として複数のエントリを一度に追加する場合があります。 これらのエントリは、環境の仮想ネットワークに関連付けられている Azure ネットワーク セキュリティ グループの設定に使用されます。 詳細については、[ネットワークのセキュリティ グループでネットワーク トラフィックのフィルター処理](/azure/virtual-network/virtual-networks-nsg) を参照してください。

> [!IMPORTANT]
> 顧客は、上記の明示的な IP ホワイトリストのルールを通じて RDP エンドポイントを確実に保護する必要があります。 IP ホワイトリスト ルールは、次の条件に準拠する必要があります。
> - IP ホワイトリスト ルールはアスタリスク/ゼロを使用することはできません。
> - ワイド IP アドレスの範囲は使用しないでください。
> - IP アドレス範囲は、顧客の CORPNET に限定する必要があります。 
> - 顧客の CORPNET (ホーム オフィスなど) 外のコンピューターをサンドボックス環境へ接続するために使用する場合は、サンドボックス環境へ接続するために使用するコンピューターの特定の IP アドレスのみを追加する必要があります。
> - Azure データセンター IP アドレス範囲を追加しないでください。
> - コーヒー店の場所などで、パブリック IP アドレスを追加しないでください。     
> - IP ホワイトリスト ルールは、使用していないときに削除する必要があります。 環境 IP ホワイトリスト ルールを定期的に確認することをお勧めします。

> [!WARNING]
> Microsoft は Microsoft 管理環境で定期的なテストを実行して、環境が十分に制限されていることを検証します。
> Microsoft は、通知することなく即座に上記のガイドラインに違反している IP アドレス ホワイトリストのルールを削除する権利を保有し、実際に削除します。
 
### <a name="partnercustomer-managed-environments"></a>パートナー/お客様の管理環境 
既定では、Microsoft 以外が管理するすべての環境でリモート デスクトップが有効になります。 顧客は自分たちのサブスクリプションに所属している環境へのアクセスを制限することをお勧めします。 これは、Azure ポータルの環境でネットワーク セキュリティ グループのルールを直接設定することで実行できます。

## <a name="windows-remoting-winrm"></a>Windows Remoting (WinRM)
Windows Remoting (WinRM) はすべての環境で無効です。 Azure ポータルを使用して、サブスクリプションに属する環境で WinRM を有効にすることはできますが、これを行わないことを強くお勧めします。

> [!WARNING]
> WinRM を有効にするための例外は、Microsoft が管理する環境では許可されません。 

## <a name="availability"></a>使用可能性
Finance and Operations アプリの保証稼働時間は 99.9% です。 計画的なダウンタイムは月 1 回発生し、8 時間以内に終了します。 ダウンタイム中に完了した作業は必ずしも 8 時間かかるとは限らないため、お客様の環境がダウンすると予想される時間を常にお知らせします。 詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../lifecycle-services/lcs-support.md) を参照してください。

### <a name="high-availability-features"></a>高可用性機能
サービスの可用性を確保するため、すべての運用環境はデフォルトの Azure 高可用性 (HA) 機能を使用して保護されています。 HA 機能はデータ センター内の単一のノードの失敗により引き起こされるダウンタイムを回避する方法を提供し、DR 機能はデータ センター全体に広く影響を及ぼす機能停止を防止します。 単一障害点イベントを防止するために、Azure 使用可能性セットが使用されます。 Azure 可用性セットの詳細については、[Windows VM のAzure 可用性セット ガイドライン](/azure/virtual-machines/windows/infrastructure-availability-sets-guidelines) を参照してください。
データベースの高可用性は Azure SQL を通してサポートされます。 詳細については、[Azure SQL データベースの事業継続性の概要](/azure/sql-database/sql-database-business-continuity) を参照してください。

### <a name="disaster-recovery-features"></a>障害復旧の機能
実稼動環境は、以下のものを含む Azure 障害復旧サポートで構成されます。
- プライマリ データベースの Azure SQL アクティブ geo レプリケーション、復旧ポイント見積 (RPO) は < 5 秒です。 詳細については、[概要: フェールオーバー グループおよび有効なジオレプリケーション](/azure/sql-database/sql-database-geo-replication-overview) を参照してください。 
- 他の Azure リージョンでの Azure blob storage (ドキュメントの添付ファイルを含む) のジオ重複コピー。 詳細については、[ジオ重複ストレージ](/azure/storage/common/storage-redundancy-grs) を参照してください。
- Azure SQL および Azure ブログ記憶域レプリケーションの同じセカンダリ地域。  

プライマリのデータ格納場所のみレプリケーションがサポートされます。 つまり、プライマリ データベースから変換されたデータを使用する Management Reporter やエンティティ格納などの 一部のアプリケーション コンポーネントは、リカバリ サイトが設定され、サービスが開始された後に生成されなければなりません。 顧客コード コンポーネントと回復されたデータの格納場所を使用してサイトを再展開し、RTO (Recovery Time Objective) を 10 時間、Recovery Point Objective を 5 秒に設定します。 詳細については、[Azure SQL データベース ポイントインタイム復元](https://azure.microsoft.com/blog/azure-sql-database-point-in-time-restore/) を参照してください。

## <a name="service-availability"></a>サービスの可用性 
Dynamics Lifecycle Services (LCS) を使用して、他の Microsoft Azure データ センターに Finance and Operations アプリを展開できます。 Azure は一般に世界中のデータセンターや地理的な場所で利用可能です。 Finance and Operations アプリでは、顧客は自分の顧客データが格納される地域またはデータセンターを指定することができます。 Microsoft は、データの持続性のためにデータを他の領域に複製する場合がありますが、地理的な場所の外部に顧客データを複製または移動しません。 詳細については、[サービス説明のホワイト ペーパー](https://aka.ms/D365-Cloud-Service-Operations)をご覧ください。

> [!IMPORTANT]
> 顧客データがどこに格納されているかに関係なく、マイクロソフトは顧客またはエンドユーザーがアクセスできる場所を管理したり制限したりしません。
詳細については、 [Finance and Operations データの格納場所](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="why-does-the-status-display-maintenance-on-my-environment-in-lcs"></a>LCS の環境で状態が [メンテナンス] と表示されるのはなぜですか。
最高のエクスペリエンスとパフォーマンスを提供するために、Microsoft は環境の保守作業を行います。 これらの一部の保守作業中に、環境の状態として次のいずれかの状態が表示される場合があります。

- メンテナンスの準備中
- メンテナンスの準備完了
- メンテナンス中

環境がこの状態になり、状態が [配置済] に戻るまでは、パッケージ アプリケーションなどのライフサイクル操作を実行することができません。 Finance and Operations アプリに対する影響はありません。 ユーザーはサービスが中断されることなく、通常の操作を続行できます。 管理操作により環境がこの状態になる前に電子メール通知が送信されます。

### <a name="how-do-i-connect-to-the-sql-database-on-my-sandbox-environment"></a>サンドボックス環境で SQL データベースに接続するにはどうすればよいですか。
次の手順に従って、Tier 2+ のサンドボックス環境内の SQL データベースに接続してください。

> [!IMPORTANT]
> 実稼働データベースに直接接続することはできません。

1. 接続先のデータベースを含む Tier 2+ の環境に属するAOS VMのいずれかにリモートデスクトップを接続します。
2. SQL Server Management Studio を起動します。
3. 接続の詳細を取得するには、次の手順を使用します。
    1. **Lifecycle Services サービス ポータル** の **環境の詳細** ページに移動します。
    2. **データベースのアカウント** セクションから、SQL Server、データベース名、axdbadmin の資格情報を取得します。
4. **SQL Server に接続する** ダイアログ ボックスで、次の手順を実行します。
    1. (ServerName).database.windows.net と入力します。(ServerName) は LCS から取得したデータベース サーバーの名前です。
    2. **認証** に使用する SQL Server の認証を選択します。
    3. **ログイン** には axdbadmin を使用します。
    4. AxdbadminのLC にて取得したパスワードを入力します。
    5. **オプション** を選択します。
    6. **データベースに接続する** ドロップダウン リストで、LCSから取得したデータベースの名前を入力します。
    7. **接続** を選択します。

### <a name="how-do-i-access-a-development-instance"></a>開発インスタンスにどのようにアクセスしますか。
開発インスタンスへのアクセス、オンプレミス開発 VM の構成、開発者と管理者の構成設定を確認する方法については、 [開発環境の展開とアクセス](../dev-tools/access-instances.md) を参照してください。

### <a name="how-do-i-deploy-a-demo-environment"></a>デモ環境をどのように展開しますか
デモ環境には、Microsoft のデモ データのみが含まれています。 デモ環境を使用して既定のフィーチャーと機能を参照することができます。 詳細については、「[デモ環境の配置](deploy-demo-environment.md)」を参照してください。

### <a name="how-do-i-move-my-customizations-between-environments"></a>環境間でカスタマイズを移動するにはどうすればよいですか。
カスタマイズを開発からサンドボックスまたは実稼動環境に移行する方法については、 [配置可能なモデルのパッケージの作成](../deployment/create-apply-deployable-package.md) を参照してください。

### <a name="can-i-bring-my-own-domain-name"></a>所有のドメイン名を使用することができますか。
Azure Active Directory (AAD) が実行中で、AAD インスタンスの管理者が Finance and Operations アプリを AAD を使用して有効にした場合、自分のドメイン名を使用することができます。 これは通常、ライセンスを購入した後、オフィスの電子メールで行われます。 オファーを承諾するリンクをクリックすると、AAD がユーザーに対して設定されます。

### <a name="can-i-add-guest-aad-accounts-as-users"></a>ゲスト AAD アカウントをユーザーとして追加できますか。
Azure Active Directory 内で適切に AAD アカウントを構成して、AAD 内で Finance and Operations アプリを有効にした場合は、ゲストの AAD アカウントを追加することができます。 

### <a name="why-am-i-no-longer-able-to-see-the-private-aos-machines-in-one-or-more-of-my-tier-2-through-tier-5-sandbox-environments"></a>プライベート AOS マシンを Tier 2 から Tier 5 のサンドボックス環境の 1 つ以上で表示できなくなったのはなぜですか?
Private AOS VM は、かつて AOS と BI コンピューター間の通信を保護する必要があったため、環境構成の一部でした。 最新の更新プログラムでは、AOS と BI マシン間のすべての通信は直接セキュリティで保護され、中間プライベート AOS 機械は不要になりました。 したがって、プライベート AOS マシンを削除する段階にあります。 バッチでマシンを削除しているので、環境の一部だけがプライベート AOS 機械を削除したことが判明することがあります。 この変更は、機能性やセキュリティにいかなる影響も及ぼさず、お客様には透明になります。

### <a name="why-am-i-no-longer-able-to-remote-desktop-into-one-or-more-of-my-tier-1-through-tier-5-microsoft-managed-sandbox-environments"></a>リモート デスクトップを自分の階層 1 から階層 5 のいずれかの Microsoft 管理サンドボックス環境で表示することができなくなったのはなぜですか。
Microsoft が管理するレベル 1 〜 レベル 5 のサンドボックス環境では、特定の IP アドレス セット (ホワイトリスト) を制限するために、リモート デスクトップ管理エンドポイントが必要です。 Microsoft は、定期的に環境が十分に制限されていることを検証します。 Microsoft は、通知なく上記のガイドラインに違反している IP アドレス ホワイトリストのルールを即座に削除する権利を保有します。 これらの理由の 1 つのためにデスクトップを環境にリモートすることができない場合があります。 
- 現在の IP アドレスがホワイトリストにありません。
- ご使用の IP が、ホワイトリストに記載されている IP アドレスから変更されています。 
- Microsoft は、ガイドラインに違反していたため、ホワイトリストの IP アドレスを含む規則を削除しました。

環境へのアクセスを回復するには、接続先のコンピュータの IP アドレスを追加する必要があります。 これを行うには、このドキュメントの [[リモート デスクトップ](#remote-desktop)] セクションの手順を実行します。
