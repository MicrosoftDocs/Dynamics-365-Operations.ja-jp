---
title: "クラウド配置の概要"
description: "このトピックでは、展開するクラウド環境とサブスクリプション、誰がどのタスクを実行できるか、および Microsoft Dynamics 365 for Finance and Operations で管理する必要があるデータおよびカスタマイズについて説明します。"
author: kfend
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: 
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8767b7047da208c340c56538f54ee6e88595c206
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="cloud-deployment-overview-for-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations のクラウド展開の概要

[!include [banner](../includes/banner.md)]
 
Microsoft Dynamics 365 for Operations をクラウドに展開するために Microsoft とともに作業するには、展開先の環境およびサブスクリプションについて理解し、だれがどのタスクを実行することができ、管理する必要があるデータおよびカスタマイズについて理解している必要があります。 配置と実装の高速化に役立つ Full Microsoft FastTrack for Dynamics 365 に登録することをお勧めします。このプログラムは、より迅速なビジネス価値の実現を支援するトレーニングとコンサルティングを提供します。 詳細については、[Microsoft FastTrack for Dynamics 365 の概要](../../fin-and-ops/get-started/fasttrack-dynamics-365-overview.md) を参照してください。 代わりに Essentials FastTrack プログラムの使用を選択すると、実装プロジェクトの管理に役立つ Lifecycle Services (LCS) の実装プロジェクト方法を使用します。 

## <a name="customer-lifecycle-subscriptions-and-deployment-topologies"></a>顧客のライフ サイクル、サブスクリプション、および展開のトポロジ
Microsoft は、すべての顧客がすべてのクラウド配置に対して次と類似するライフサイクルに従うため、各フェーズで別の環境トポロジが必要になると想定しています。 

- 評価
- 必要に応じカスタマイズを行う
- レベル 1 サンドボックスでのカスタマイズおよびパートナー ソリューションのインストールとテスト (開発またはテスト環境) 
- レベル 2 サンドボックス環境のテストのカスタマイズ、パートナー ソリューション、データ構成
- 高可用性の運用環境にカスタマイズとデータ構成を展開する

プロジェクトのいくつかのフェーズでは、すべての環境を一度に実行することができます。 既定のライセンスおよび使用可能な層の詳細については、[Dynamics 365 ライセンス ガイド](http://download.microsoft.com/documents/en-us/dynamics/pricing/Dynamics_365_Enterprise_edition_Licensing_Guide.pdf) を参照してください。

条件、顧客、パートナー、および Microsoft サブスクリプションについて聞く場合があります。 *顧客またはパートナーのサブスクリプション* は、評価および開発目的でのみ、顧客またはパートナーが独自の Azure サブスクリプションをもって Dynamics 365 for Finance and Operations 環境を配置することを意味しています。 顧客やパートナーは、Azure 価格リストに基づいて Azure サブスクリプションに展開されるリソースに対して支払います。 *Microsoft サブスクリプション*は、顧客が Dynamics 365 for Finance and Operations ライセンスを購入し、Microsoft が管理する Azure サブスクリプションに環境を配置できることを意味するため、顧客には Azure からの別個の請求はありません。 各 Enterprise オファーでは、既定で 3 つの環境が含まれています。 

- 1 つの階層 1 サンド ボックス (ここでは、開発またはビルド環境です)。
- ユーザー受け入れテスト (UAT) 用の、1 つの階層 2 サンド ボックス (マルチ ボックス環境) です。
- 高可用性 (HA) を備えた 1 つの実稼働環境。 この環境は、Microsoftによって管理され、運用されます。

追加の環境は、アドオンとして購入する場合があります。 ライセンスおよび Microsoft Dynamics 365 に何が含まれるかの詳細については、[Microsoft Dynamics 365 Enterprise edition ライセンス ガイド](http://download.microsoft.com/documents/en-us/dynamics/pricing/Dynamics_365_Enterprise_edition_Licensing_Guide.pdf) を参照してください。

ライフサイクルが使用可能な環境にどうマップするかを次に示します。

| ライフサイクルのフェーズ               | 環境                               | 定期売買                                        |
|-------------------------------|-------------------------------------------|-----------------------------------------------------|
| 評価および分析       | デモ、ワン ボックス                             | 顧客またはパートナーのサブスクリプション。                                |
| カスタマイズ                     | 開発/ビルド、1 つボックス                        | Microsoft サブスクリプション、パートナー/顧客サブスクリプション、またはローカル VM
| ユーザー受け入れテスト (UAT) | 第 2 層のサンド ボックス、マルチ ボックス環境 | Microsoft サブスクリプション                              |
| Go live                       | 生産、高可用性マルチボックス環境                    | Microsoft サブスクリプション                              |

## <a name="features-of-the-finance-and-operations-production-instance"></a>Features of the Finance and Operations プロダクション インスタンス
Finance and Operations アプリケーション製造インスタンスには、次の機能があります。

## <a name="security-and-compliance"></a>セキュリティとコンプライアンス
Dynamics 365 for Operations は、PA-DSS 3.1 認定を受けています。これは、コンポーネント間のすべての通信が直ちに保護されることを意味します。 

Microsoft Azure のすべての Dynamics 365 for Operations フロントエンド仮想マシンは配置中に TLS 1.2 のみを承諾するようにコンフィギュレーションされています。 

> [!IMPORTANT]
> 購入したアドオン サンドボックスを含む Microsoft 管理対象のサンドボックスに管理者権限を持つお客様は、次のガイドラインに従わなければなりません。
> - 既定では、レベル 1 - 5 のすべてのサンドボックスで自動 Windows の更新が有効になっているため、無効にしないでください。 これにより、Microsoft がセキュリティまたは重大なインフラストラクチャの更新を自分の環境にプッシュするたびに、環境に最新の更新プログラムが適用され、毎月 Microsoft からリリースされたオペレーティング システムの修正プログラムが更新されます。  
> - これらの環境の管理者パスワードは、変更しないでください。 変更済管理者パスワードをもつ環境では、Microsoft がフラグを設定します。 Microsoft は、管理者パスワードをリセットする権利を保有し、実際にリセットします。  
> - Microsoft 管理対象 VM に新しいユーザー アカウントを追加することは、許可されていません。 Microsoft は、通知することなく新しく追加されたユーザー アカウントを削除する権利を保有し、実際に削除します。

## <a name="remote-desktop"></a>リモート デスクトップ

### <a name="microsoft-managed-environments"></a>Microsoft が管理する環境
顧客は、Microsoft Remote Desktop (RDP) を介して、Dynamics 365 for Finance and Operations (VM) に接続するための追加セットアップを完了する必要があります。 この追加の設定は、 レベル 1 〜 レベル 5 のサンドボックスとアドオンを含む、Microsoft が管理するすべての環境に適用されます。 レベル 1 からレベル 5 のサンドボックス環境に接続するためには、明示的に組織の IP アドレス空間からのアクセスを有効にする (ホワイトリストする) 必要があります。 これは、リモート デスクトップを介して仮想マシンに接続するために使用される IP アドレス スペースを入力できる**環境ページ** (**Maintain** > **Enable Access**) にアクセスできる Lifecycle Services (LCS) ユーザーによって実行できます。 アクセス ルールは、単一の IP アドレス (例: 10.10.10.10) または IP アドレスの範囲 (例: 192.168.1.0/24) です。 セミコロン (;) で区切られたリスト (例: 10.10.10.10;20.20.20.20;192.168.1.0/24) として複数のエントリを一度に追加する場合があります。 これらのエントリは、環境の仮想ネットワークに関連付けられている Azure ネットワーク セキュリティ グループの設定に使用されます。 詳細については、[ネットワークのセキュリティ グループでネットワーク トラフィックのフィルター処理](/azure/virtual-network/virtual-networks-nsg) を参照してください。

> [!IMPORTANT]
> 顧客は、上記の明示的な IP ホワイトリストのルールを通じて RDP エンドポイントを確実に保護する必要があります。 IP ホワイトリスト ルールは、以下の条件に準拠し、環境がセキュリティで保護され、知的財産が保護されるようにする必要があります。
> - IP ホワイトリストのルールはスター/ゼロを使用してはならず、インターネットへ環境を開放する
> - ワイド IP アドレスの範囲は使用しないでください。
> - IP アドレス範囲は、お客様の CORPNET に限定する必要があります 
> - 顧客の CORPNET (ホーム オフィスなど) 外のコンピューターをサンド ボックス環境へ接続するために使用する場合は、サンド ボックス環境へ接続するために使用するコンピューターの特定の IP アドレスのみを追加する必要があります。
> - Azure データセンター IP アドレス範囲を追加しないでください
> - コーヒー店の場所などでは、パブリック IP アドレスを構成しないでください。     

> [!WARNING]
> Microsoft は Microsoft 管理環境で定期的なテストを実行して、環境が十分に制限されていることを検証します。
> Microsoft は、通知することなく即座に上記のガイドラインに違反している IP アドレス ホワイトリストのルールを削除する権利を保有し、実際に削除します。
 
### <a name="partnercustomer-managed-environments"></a>パートナー/お客様の管理環境 
既定では、Microsoft 以外が管理するすべての環境でリモート デスクトップが有効になります。 顧客は自分たちのサブスクリプションに所属している環境へのアクセスを制限することをお勧めします。 これは、Azure ポータルの環境でネットワーク セキュリティ グループのルールを直接設定することで実行できます。

## <a name="windows-remoting-winrm"></a>Windows Remoting (WinRM)
Windows Remoting (WinRM) はすべての環境で無効です。 Azure ポータルを使用して、サブスクリプションに属する環境で WinRM を有効にすることはできますが、これを行わないことを強くお勧めします。

> [!WARNING]
> WinRM を有効にするための例外は、Microsoft が管理する環境では許可されません。 

## <a name="availability"></a>適用の対象
Dynamics 365 for Finance and Operations の保証稼働時間は 99.5％ です。 計画的なダウンタイムは月 1 回発生し、8 時間以内に終了します。 ダウンタイム中に完了した作業は必ずしも 8 時間かかるとは限らないため、お客様の環境がダウンすると予想される時間を常にお知らせします。 [Microsoft Dynamics 365 for Finance and Operations および Dynamics Lifecycle Services のサポートを検索](../lifecycle-services/lcs-support.md).

### <a name="high-availability-features"></a>高可用性機能
サービスの可用性を確保するため、すべての運用環境はデフォルトの Azure 高可用性 (HA) 機能を使用して保護されています。 HA 機能はデータ センター内の単一のノードの失敗により引き起こされるダウンタイムを回避する方法を提供し、DR 機能はデータ センター全体に広く影響を及ぼす機能停止を防止します。 Dynamics 365 for Operations クラウド アーキテクチャは、計算層に Azure 可能性セットを使用して、単一ポイント エラーのイベントを防止します。 Azure 可用性セットの詳細については、[Windows VM のAzure 可用性セット ガイドライン](/azure/virtual-machines/windows/infrastructure-availability-sets-guidelines) を参照してください。
データベースの高可用性は Azure SQL を通してサポートされます。 詳細については、[Azure SQL データベースの事業継続性の概要](/azure/sql-database/sql-database-business-continuity) を参照してください。

### <a name="disaster-recovery-features"></a>障害復旧の機能
Finance and Operations の実稼動環境は、以下のものを含む Azure 障害復旧サポートで構成されます。
- プライマリ データベースの Azure SQL アクティブ geo レプリケーション、復旧ポイント見積 (RPO) は < 5 秒です。 詳細については、[概要: フェールオーバー グループおよび有効なジオレプリケーション](/azure/sql-database/sql-database-geo-replication-overview) を参照してください。 
- 他の Azure リージョンでの Azure blob storage (ドキュメントの添付ファイルを含む) のジオ重複コピー。 詳細については、[ジオ重複ストレージ](/azure/storage/common/storage-redundancy-grs) を参照してください。
- Azure SQL および Azure ブログ記憶域レプリケーションの同じセカンダリ地域。  

プライマリのデータ格納場所のみレプリケーションがサポートされます。 つまり、プライマリ データベースから変換されたデータを使用する Management Reporter やエンティティ格納などの 一部の Finance and Operations アプリケーション コンポーネントは、リカバリ サイトが設定され、サービスが開始された後に生成されなければなりません。 顧客コード コンポーネントと回復されたデータの格納場所を使用してサイトを再展開し、RTO (Recovery Time Objective) を 10 時間、Recovery Point Objective を5分に設定します。 詳細については、[Azure SQL データベース ポイントインタイム復元](https://azure.microsoft.com/en-us/blog/azure-sql-database-point-in-time-restore/) を参照してください。

## <a name="service-availability"></a>サービスの可用性 
Dynamics Lifecycle Services (LCS) を使用して、他の Microsoft Azure データ センターに Finance and Operations を展開できます。 Azure は一般に世界中のデータセンターや地理的な場所で利用可能です。 Finance and Operations では、顧客は自分の顧客データが格納される地域またはデータセンターを指定することができます。 Microsoft は、データの持続性のためにデータを他の領域に複製する場合がありますが、地理的な場所の外部に顧客データを複製または移動しません。

**重要:** 顧客データがどこに格納されているかに関係なく、マイクロソフトは顧客またはエンドユーザーがアクセスできる場所を管理したり制限したりしません。
詳細については、[Finance and Operations のデータが格納されている場所](https://www.microsoft.com/en-us/trustcenter/privacy/dynamics365-operations-location) を参照してください。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="how-do-i-access-a-development-instance"></a>開発インスタンスにどのようにアクセスしますか。

開発インスタンスへのアクセス、オンプレミス開発 VM の構成、および開発者と管理者の構成設定を見つける方法については、[インスタンスへのアクセス](../dev-tools/access-instances.md)をご覧ください。

### <a name="how-do-i-deploy-a-demo-environment"></a>デモ環境をどのように展開しますか
デモ環境には、Microsoft のデモ データのみが含まれています。 デモ環境を使用して既定のフィーチャーと機能を参照することができます。 詳細については、「[デモ環境の配置](deploy-demo-environment.md)」を参照してください。

### <a name="how-do-i-move-my-customizations-between-environments"></a>環境間でカスタマイズを移動するにはどうすればよいですか。
カスタマイズを開発環境からサンドボックスまたは実稼働環境に移行するには、[[ランタイム環境に適用するためにモデルの展開可能パッケージを作成する](../deployment/create-apply-deployable-package.md)] を参照してください。

### <a name="can-i-request-a-copy-of-my-production-database"></a>生産データベースのコピーを要求できますか。
顧客は、2 層サンド ボックス環境にインストールされている、財務および工程の本番データベースのコピーを要求できます。 この要求は DSE によって完了されます。

### <a name="can-i-bring-my-own-domain-name"></a>所有のドメイン名を使用することができますか。
Azure Active Directory (AAD) を実行中で、AAD インスタンスの管理者が Finance and Operations アプリケーションを AAD で有効にした場合、自分のドメイン名を使用することができます。 これは通常、ライセンスを購入した後、オフィスの電子メールで行われます。 オファーを承諾するリンクをクリックすると、AAD がユーザーに対して設定されます。

### <a name="can-i-add-guest-aad-accounts-as-finance-and-operations-users"></a>Finance and Operations のユーザーとしてゲスト AAD アカウントを追加できますか。
Azure Active Directory 内で適切に AAD アカウントを構成して、AAD 内で Finance and Operations アプリケーションを有効にした場合、ゲスト AAD アカウントを追加することができます。 

### <a name="why-am-i-no-longer-able-to-see-the-private-aos-machines-in-one-or-more-of-my-tier-2-through-tier-5-sandbox-environmnents"></a>プライベート AOS 機器を階層 2 から階層 5 のサンドボックス環境で表示できなくなったのはなぜですか。
Private AOS VM は、かつて AOS と BI コンピューター間の通信を保護する必要があったため、環境構成の一部でした。 最新の更新プログラムでは、AOS と BI マシン間のすべての通信は直接セキュリティで保護され、中間プライベート AOS 機械は不要になりました。 したがって、プライベート AOS マシンを削除する段階にあります。 バッチでマシンを削除しているので、環境の一部だけがプライベート AOS 機械を削除したことが判明することがあります。 この変更は、機能性やセキュリティにいかなる影響も及ぼさず、お客様には透明になります。

### <a name="why-am-i-no-longer-able-to-remote-desktop-into-one-or-more-of-my-tier-1-through-tier-5-microsoft-managed-sandbox-environments"></a>リモート デスクトップを自分の階層 1 から階層 5 のいずれかの Microsoft 管理サンドボックス環境で表示することができなくなったのはなぜですか。
Microsoft が管理するレベル 1 〜 レベル 5 のサンドボックス環境では、特定の IP アドレス セット (ホワイトリスト) を制限するために、リモート デスクトップ管理エンドポイントが必要です。 Microsoft は、定期的に環境が十分に制限されていることを検証します。 Microsoft は、通知なく上記のガイドラインに違反している IP アドレス ホワイトリストのルールを即座に削除する権利を保有します。 これらの理由の 1 つのためにデスクトップを環境にリモートすることができない場合があります。 
- 現在の IP アドレスがホワイトリストにありません。
- ご使用の IP が、ホワイトリストに記載されている IP アドレスから変更されています。 
- Microsoft は、ガイドラインに違反していたため、ホワイトリストの IP アドレスを含む規則を削除しました。

環境へのアクセスを回復するには、接続先のコンピュータの IP アドレスを追加する必要があります。 これを行うには、このドキュメントの [[リモート デスクトップ](#remote-desktop)] セクションの手順を実行します。

