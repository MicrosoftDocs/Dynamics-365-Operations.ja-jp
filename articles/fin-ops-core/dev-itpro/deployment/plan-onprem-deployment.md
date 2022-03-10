---
title: オンプレミス配置の計画および準備
description: このトピックは、オンプレミス展開の計画と準備に役立ちます。
author: PeterRFriis
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: ec3d19795d44fbc7442d5991c730ecc5d54d0e5e
ms.sourcegitcommit: 378c9340176956862687ae8d55c636486e3105d3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/27/2022
ms.locfileid: "8044543"
---
# <a name="plan-and-prepare-for-on-premises-deployments"></a>オンプレミス配置の計画および準備

[!include [banner](../includes/banner.md)]

Dynamics 365 Finance + Operations (on-premises) は、顧客データ センターでビジネス プロセスの実行をサポートします。 この配置オプションでは、アプリケーション サーバーおよび Microsoft SQL Server データベースは顧客のデータ センター内で実行されます。

このトピックは、オンプレミス展開の計画と準備に役立ちます。

> [!IMPORTANT]
> Dynamics 365 Finance + Operations (on-premises) は、Microsoft Azure クラウド サービス を含む、任意のパブリック クラウド インフラストラクチャではサポートされていません。 ただし、[Microsoft Azure Stack HCI](https://azure.microsoft.com/products/azure-stack/hci/) および [Microsoft Azure Stack Hub](https://azure.microsoft.com/products/azure-stack/hub/) での実行はサポートされています。

## <a name="differences-between-cloud-deployments-and-on-premises-deployments"></a>クラウド展開とオンプレミス展開の違い
クラウド展開とオンプレミス展開の機能は異なります。 これらの違いは、計画に影響します。 違いについては、次のトピックで説明します。
- [配置オプション](choose-deployment-type.md)
- [クラウドとオンプレミスの機能比較](../../fin-ops/get-started/cloud-prem-comparison.md)
- [Finance and Operations の削除済みまたは推奨されない機能](../migration-upgrade/deprecated-features.md)

## <a name="how-lcs-is-used-with-on-premises-deployments"></a>オンプレミス配置で LCS を使用する方法
Microsoft Dynamics Lifecycle Services (LCS) は、アプリケーション ライフサイクルを管理するためのツールおよびサービスを提供するアプリケーション管理ポータルです。 顧客とパートナーは LCS を使用して、クラウドとオンプレミスの両方の導入を管理します。 以下のタスクに対して LCS を使用することができます。
- クラウド環境とオンプレミス環境を展開します。
- 環境を保守します。
- 管理する環境の正常性を監視、診断、および分析します (クラウドのみ)。
- 製品の問題や規制機能を検索します。
- サポートを受けます。

LCS の詳細については、 [Lifecycle Services のリソース](../lifecycle-services/lcs.md) を参照してください。

## <a name="environments"></a>環境
計画する必要のある環境には 4 つのタイプがあります。 このセクションでは、4 つの環境と、それらにアクセスして展開する方法について説明します。

### <a name="demo-environment"></a>デモ環境
デモ環境にサインアップして、システムについて学習することができます。 デモ環境は、クラウドとオンプレミスの両方の展開に適用されます。 詳細については、 [プレビュー サブスクリプションのサインアップ](../dev-tools/sign-up-preview-subscription.md) を参照してください。

### <a name="developer-environment"></a>開発者環境
開発経験は、クラウドとオンプレミスの配置で同じです。 開発者環境にアクセスするには、 [開発環境の配置とアクセス](../dev-tools/access-instances.md) を参照してください。

### <a name="sandbox-environment"></a>サンドボックス環境
ビジネス ユーザーと機能チームのメンバーは、サンドボックス環境を使用してアプリケーション機能を検証します。 この機能には、カスタマイズ内容や Microsoft Dynamics AX 2012 環境から継承されたデータが含まれます。 オンプレミス サンドボックス環境を展開するには、 [オンプレミス環境の設定と配置のホーム ページ](setup-deploy-on-premises-environments.md) を参照してください。

少なくとも、オンプレミスのサンドボックス環境には次のものが必要です。
- 環境オーケストレータを実行している 3 台のコンピューター
- Application Object Server (AOS) を実行する 2 台のコンピューター
- Management Reporter (MR) を実行している 1 台のコンピューター
- ローカル SQL Server (データベース エンジン) を使用する SQL Server Reporting Services (SSRS) を実行する 1 台のコンピューター
- Active Directory を実行している 1 台のコンピューター
- SQL Server を実行している 1 台のコンピューター (データベース エンジン)

### <a name="production-environment"></a>実稼働環境
実働環境は、ユーザーや顧客がアクセスできる実際の展開です。 実稼働環境を展開するには、 [オンプレミス環境の設定と配置のホーム ページ](setup-deploy-on-premises-environments.md) を参照してください。

少なくとも、オンプレミスの実稼動環境には次のものが必要です。
- 環境オーケストレータを実行している 3 台のコンピューター
- Application Object Server (AOS) を実行している 3 台のコンピューター
- Management Reporter (MR) を実行している 1 台のコンピューター
- ローカル SQL Server (データベース エンジン) を使用する SQL Server Reporting Services (SSRS) を実行する 1 台のコンピューター
- SQL Server を実行している 2 台以上のコンピューター (データベース エンジン)
- Active Directory を実行している 2 台以上のコンピューター

## <a name="service-fabric"></a>Service Fabric
オンプレミス配置では、 Azure Service Fabric スタンドアロンクラスターが使用されます。 Service Fabric は、企業規模の大規模なアプリケーションを構築および管理するための次世代の Microsoft ミドルウェア プラットフォームです。 Service Fabric スタンドアロン クラスターは、Windows Server を実行しているどのコンピューターにも展開することができます。

オンプレミス配置には、各サンドボックス環境のスタンドアロン クラスターと各実稼働環境のスタンドアロン クラスターがあります。 両方のタイプのクラスターに、次のロールまたはノード タイプが配置されます。
- Application Object Servers (AOS) – アプリケーション機能をクライアント、バッチ、およびインポート/エクスポートのシナリオで実行する機能を提供します。
- Management Reporter (MR) – 財務レポートの機能を提供します。
- SQL Server Reporting Services (SSRS): ドキュメント レポート機能を提供します。
- 環境オーケストレータ – LCS からオンプレミス環境管理を有効にします。

次の図は、Service Fabric スタンドアロン クラスターに配置されたノード タイプを示しています。

![Service Fabric スタンドアロン クラスターに配置されるノード タイプ。](media/on-premises-overview-01.png)

### <a name="service-fabric-resources"></a>Service Fabric リソース
Service Fabric の詳細については、次のトピックを参照してください。
- [Azure Service Fabric documentation](/azure/service-fabric) - サービスファブリックの詳細について。
- [Service Fabric application upgrade](/azure/service-fabric/service-fabric-application-upgrade)- Azure Service Fabric アプリケーションは、定期的なアップグレードを必要となるサービスです。
- [Service Fabric のスタンドアロン クラスター展開の計画と準備](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) - Service Fabric クラスターおよびウィルス対策の除外に関する追加情報

## <a name="system-requirements"></a>システム要件
[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md)でシステム要件を確認し、オンプレミス展開が必要なコンピューターの台数を確認します。

## <a name="hardware-sizing"></a>ハードウェアのサイズ
オンプレミス環境におけるハードウェアおよびインフラストラチャのサイズ設定のプロセスを開始する前に、 [オンプレミス配置のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md) および [オンプレミス環境の設定と配置のホーム ページ](setup-deploy-on-premises-environments.md) に精通し、基盤となるインフラストラクチャを確実に把握します。 最適なパフォーマンスを得るには、システム設定のベストプラクティスに十分注意します。 ドキュメントを確認した後、トランザクションと同時実行ユーザー量の見積および平均コア スループットに基づいて、環境のサイズを変更するプロセスを開始できます。

### <a name="factors-that-affect-sizing"></a>サイズ設定に影響する要因
サイズに影響を与える主な要因は次のとおりです。
- トランザクションの特性
- ユーザー特性 - タイプおよび同時実行
- データ構成
- 拡張子
- レポート使用パターン
- サード パーティ ソリューション

より詳細なデータを収集するほど、正確にサイジングを見積もることができます。 ハードウェアのサイジングは、データをサポートしていないため、不正確になる可能性があります。 収集する必要のある最小限のデータは、1 時間あたりのトランザクション明細行のピーク負荷です。 サイズ変更に影響する要因を次の図に示します。

![サイズ変更要因。](media/sizing-factors.png)

左から右に、サイジングを正確に推定するために必要な最初の最も重要な要素は、トランザクション プロファイルまたはトランザクション特性です。 1 時間あたりのピーク トランザクション量を検索することは重要です。 複数のピーク期間がある場合は、これらの期間を正確に定義する必要があります。

インフラストラクチャに影響を及ぼす負荷を理解するようになると、これらの要因についてさらに詳しく理解する必要があります。
- **トランザクション** – トランザクションには、通常、日または週全体で特定のピークがあります。 ピークは、トランザクション タイプによって異なる場合があります。 たとえば、時間と経費のエントリーでは、通常、1 週間に 1 回ピークを示しますが、販売注文票は、その日の統合またはトリクルによって一括して到着する可能性があります。
- **同時ユーザー数** – 同時ユーザー数は、サイズを設定する上で 2 番目に重要な要因です。 同時ユーザー数のみに基づいて信頼性の高いサイズの見積を取得することはできません。 同時ユーザーが使用できる唯一のデータである場合は、トランザクションの概数を見積もり、データが増えたときにこれをやり直します。 正確な同時ユーザー定義は次の通りです。
    - 名前付きユーザーは同時ユーザーではありません。
    - 同時ユーザーは、常に名前付きユーザーのサブセットです。
    - ピーク時の負荷は、最大の同時実行のサイズを定義します。
    同時ユーザーについては、ユーザーは次のすべての基準を満たす必要があります。
        - ユーザーはログオンしています。
        - カウント時に稼働中の取引や問い合わせがあります。
        - セッションはアイドル状態ではありません。
- **データ構成** - データ構成とは、システムをどのように設定してコンフィギュレーションするかということです。 たとえば、これは、法人の数、品目番号、BOM レベルの数、およびセキュリティ設定がどの程度複雑かを含みます。 これらの要因のそれぞれはパフォーマンスには影響しない可能性があるが、影響はインフラストラクチャに関しては賢明な選択肢を使用することで相殺できます。
- **拡張機能** – カスタマイズはシンプルまたは複雑になり得ます。 カスタマイズの数と複雑さと使用の性質は、必要なインフラストラクチャのサイズにさまざまな影響を与えます。 複雑なカスタマイズの場合は、効率性のテストだけでなく、インフラストラクチャのニーズを理解するのに役立つように、パフォーマンス評価を行う必要があります。 拡張機能が、パフォーマンスとスケーラビリティにおけるベストプラクティスに従ってコード化されていない場合、これはさらに重要です。
- **レポートと分析** – レポートと分析には、通常、データベースのシステムに対する大量のクエリの実行が含まれます。 データを大量に使用するレポートが実行される頻度を下げると、影響を減らすことができます。 クエリのデザインがパフォーマンスをどのように影響するかを理解することも重要です。
- **サード パーティのソリューション** 1 – これらのソリューションは、ISV のように、拡張と同じ意味合いと推奨事項を持っています。

## <a name="sizing-your-environment"></a>環境のサイズ変更
サイジング要件を決定するには、処理する必要のあるトランザクションのピーク量を知る必要があります。 Management Reporter や SSRS などのほとんどの補助システムは、ミッション クリティカルではありません。 結果として、このトピックは主に AOS と SQL Server に焦点を当てています。

一般に、計算層はスケールアウトされ、N + 1 形式で設定する必要があります。つまり、3 つの AOS を推定する場合は、4 つ目の AOS を追加します。 データベース層は、常に常時使用可能な設定で設定する必要があります。

### <a name="sql-server-oltp"></a>SQL Server (OLTP)

#### <a name="sizing"></a>サイズ変更

- 1 時間あたり DB サーバー上のコアあたり 3K 〜 15K のトランザクション明細行。
- プライマリー SQL Server の一般的な AOS と SQL のコア比率 3:1。 高可用性コンフィギュレーションに基づいて、追加のコアが必要です。
    - データベースに重い操作を処理すると、これが 2:1 に回帰する可能性があります。
- 次の要因には、変動が影響します。
    - 使用中のパラメータ設定。
    - 拡張機能のレベル。
    - データベース ログやアラートなどの追加機能の使用。 極端なデータベース ロギングにより、コアあたりのスループットは 1 時間当たり 3K 以下にさらに低下します。
    - データ構成の複雑さ。 たとえば、シンプルな勘定科目表と細かい綿密な勘定科目表は、スループットに影響を与えます。
    - トランザクションの特性。
    - 各コアの 2 GB から 4 BG までのメモリーです。
    - 管理リポーターや SSRS データベースなどの DB サーバー上の補助データベース。
    - Temp DB = 物理プロセッサと同数のファイルを持つ DB サイズの 15 ％。
    - 同時のトランザクション ボリューム/使用量の合計に基づく SAN サイズとスループット。

#### <a name="high-availability"></a>高可用性

クラスターまたはミラーリングの設定で、常に SQL Server を使用する必要があります。 2 番目の SQL ノードは、1 次ノードと同じ数のコアを持つ必要があります。

#### <a name="active-directory-federation-services-ad-fs"></a>Active Directory フェデレーション サービス (AD FS)
広告のサイズ変更について、[広告のサーバーの処理能力ドキュメント](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity)を参照してください。 A[サイズ変更スプレッドシート](https://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)は、展開内のインスタンスの数を計画するために使用できます。

### <a name="aos-online-and-batch"></a>AOS (オンラインおよびバッチ)

#### <a name="sizing"></a>サイズ変更

- トランザクションの量と使用法サイズの変更
    - コアあたり 2K から 6K の明細行
    - インスタンスあたり 16 GB
    - 標準ボックス – 4 から 24 コア
    - コアあたり 10 から 15 のエンタープライズ ユーザー
    - コアあたり 15 から 25 のアクティブ ユーザー
    - コアあたり 25 から 50 のチーム メンバー
- バッチ
    - コアあたり 1 から 4 のバッチ スレッド
    - バッチ ウィンドウの特性に基づくサイズ
- AOS、データ管理、およびバッチは、Service Fabric 内で同じ役割を果たすことに注意してください。 Microsoft Dynamics AX 2012 のように、これらの 3 つのワークロードをまとめてサイズ調整する必要があります。
- ここでは、SQL Server と同じ変動要因が適用されます。

#### <a name="high-availability"></a>高可用性
- 推測する以上に少なくとも 1 から 2 の AOS があることを確認してください。
- 少なくとも 3 から 4 つの仮想ホストが使用可能であることを確認してください。

### <a name="management-reporter"></a>Management Reporter
ほとんどの場合、広範囲に使用されない限り、2 つのノードを使用する推奨最小要件が適切に動作します。 頻繁な使用がある場合のみ、3 つ以上のノードを必要とし、その後は必要に応じてを縮尺を調整することができます。

### <a name="sql-server-reporting-services"></a>SQL Server Reporting Services
Finance + Operations の現在のリリースは、1 つの SSRS ノードしか展開できません。 テスト中に SSRS ノードを監視し、SSRS で使用可能なコアの数を必要に応じて増やします。 SSRS VM とは異なる仮想ホストで事前構成されたセカンダリ ノードを使用できることを確認してください。 これは、SSRS または仮想ホストをホストする仮想マシンに問題がある場合に重要です。 この場合、ノードは交換する必要があります。

### <a name="environment-orchestrator"></a>環境オーケストレーター
オーケストレータ サービスは、展開および LCS との関連する通信を管理するサービスです。 このサービスはプライマリ Service Fabric サービスとして展開され、最低 3 台の VM が必要です。 このサービスは、サービス ファブリック オーケストレーション サービスと同じ場所に配置されています。 これは、クラスターのピーク負荷に合わせたサイズにする必要があります。 詳細については、 [Service Fabric スタンドアロン クラスタの展開計画](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation)を参照してください。

### <a name="virtualization-and-oversubscription"></a>仮想化と過剰加入
AOS のようなミッション クリティカルなサービスは、コア、メモリ、ディスクなどの専用リソースを持つ仮想ホストでホストする必要があります。

## <a name="authentication-methods"></a>認証方法

オンプレミスの配置では、次の認証方法が使用されます。

- **Azure Active Directory(Azure AD)** - Azure AD は LCS へのログインに使用される認証方法です。 Azure AD は LCS ローカル エージェントの構成に使用されます。 詳細については、「[Azure Active Directory とは何か](/azure/active-directory/active-directory-whatis)」を参照してください。
- **Active Directory ドメイン サービス (AD DS)** - Finance + Operations コンポーネントをホストするコンピューターは、Active Directory ドメインに属している必要があります。 Active Directory ドメイン サービス (AD DS) はネイティブ モードで構成する必要があります。 詳細については、[Active Directory ドメイン サービス](/windows-server/identity/ad-ds/active-directory-domain-services) を参照してください。
- **Active Directory フェデレーション サービス (AD FS)** - AD FS は、オンプレミス配置で使用される認証方法です。 AD FS は、Microsoft 365、クラウド ベースの SaaS アプリケーション、会社のネットワーク上のアプリケーションを含むさまざまなアプリケーション全体でアクセス制御とシングル サインオンを提供します。
  - IT 組織については、同じ資格情報とポリシーのセットに基づいて、最新および従来のアプリケーション、クラウドのオンプレミスの両方への署名とアクセス制御を提供できます。
  - ユーザーについては、同じ、使い慣れたアカウントの資格情報を使用してシームレスなサインを提供します。
  - 開発者については、組織のディレクトリに ID があるユーザーを認証するための簡単な方法を提供します。 つまり、認証や識別ではなく、アプリケーションに力を注ぐことができます。

    詳細については、[Active Directory フェデレーション サービス](/windows-server/identity/active-directory-federation-services) を参照してください。

## <a name="data-stored-in-azure-data-centers"></a>Azure データ センターに保存されたデータ

Finance + Operations のオンプレミス配置オプションは、オンプレミスのコア顧客データを格納します。 コア顧客データは、[Microsoft Trust Center](https://www.microsoft.com/trustcenter/privacy/how-microsoft-defines-customer-data) で提供される顧客データ定義のサブセットです。

次のテーブルは、米国内にある Azure データ センターに顧客データを保存するために使用されるサービスの概要を示しています。 サービスには、Lifecycle Services (LCS)、Microsoft Office サインアップ ポータルおよび Azure Active Directory が含まれます。 これらのサービスにより、サポート インシデントの初期オンボーディング、開始、追跡、サービスの更新とアップグレードが可能になります。 コア顧客データと呼ばれる他のすべての顧客データは、オンプレミスに保管されます。

| サポート サービス               | 顧客データの定義                      |
|---------------------------------------|----------------------------------------------------|
| Microsoft Dynamics Lifecycle Services | プロジェクトには、プロジェクトのコンテンツおよびファイルが格納されます。 これには、アプリケーション構成データ、コード、メタデータ、アプリケーションやビジネス プロセス モデルを構成するデータ アセットが含まれます。 |
| Microsoft Office サインアップ ポータル        | オンボード プロセス中に収集された顧客情報。  |
| Microsoft Azure Active Directory      | LCS と Azure DevOps の認証。   |

追加のサービスまたはコンポーネントは、必要に応じてオンプレミス配置を拡張するためにコンフィギュレーションすることができます。ただし、コンフィギュレーションの選択により、コア顧客データが顧客データ センターの外部に転送される可能性があります。 たとえば、オンプレミス配置の外部サービスを統合するために使用されるデータ管理機能のコンフィギュレーションにより、オンプレミス配置外のコア顧客データが転送される可能性があります。

## <a name="next-steps"></a>次のステップ

このトピックに記載されている計画活動を完了した後、 [オンプレミス配置のホーム ページ](on-premises-deployment-landing-page.md) の [研修](on-premises-deployment-landing-page.md#onboard) セクションにリストされている手順を開始することができます。

計画、展開、メンテナンス、およびトラブルシューティングの詳細については、実装を通じて [オンプレミス配置のホーム ページ](on-premises-deployment-landing-page.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
