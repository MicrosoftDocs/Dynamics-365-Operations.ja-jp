---
title: Finance and Operations アプリのサービス説明
description: このトピックでは、Finance and Operations アプリのサービス説明を示します。
author: tomhig
ms.date: 11/17/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 262cf00bdca63876c284be40954ca5de559b993a
ms.sourcegitcommit: f11ad8d7ee8a4d2ee1a1bb601622b50e14955c4a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2021
ms.locfileid: "7825403"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Finance and Operations アプリのサービス説明

[!include[banner](../includes/banner.md)]

Finance and Operations アプリは、[Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/) をベースにして構築されたエンタープライズ リソース プランニング (ERP) のサービスとしてのソフトウェア (SaaS) の提供です。 Finance and Operations サービスは、組織固有の要件をサポートする ERP 機能を提供し、インフラストラクチャの管理を必要とせずに、絶えず変化するビジネス環境に適応するのに役立ちます。 Finance and Operations アプリケーションは、次のソリューション領域の 1 つ以上を含めることができます。

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

これらのアプリケーションは、[ビジネス インテリジェンス](/power-bi/fundamentals/power-bi-service-overview)、[インフラストラクチャ](https://azure.microsoft.com/global-infrastructure/)、[コンピューティング](/azure/service-fabric/service-fabric-overview)、[データベース サービス](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) とともに、組織が業界固有の運用業務プロセスを実行できます。 実装パートナーによってサポートされている顧客は、固有のビジネス プロセスに最適な業務アプリケーション ロジックのコンフィギュレーションを決定します。 機能および業務プロセスは、次のソリューションの 1 つまたは組み合わせによって強化または拡張できます。

- 組み込みの [個人用設定のエクスペリエンス](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md) ツール
- [Visual Studio](https://visualstudio.microsoft.com) ベースの [Finance and Operations ソフトウェア開発キット (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) と [Azure DevOps ビルドの自動化](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- [AppSource](https://appsource.microsoft.com/partners) の独立系ソフトウェア ベンダー (ISV) ソリューション

要件に基づいて、顧客はソリューションのアプローチを選択します。 実装パートナーと協力して、[Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md) で提供されるツールとベスト プラクティスを利用して、ソリューションの定義、開発、およびテストを行います。 一般的なシナリオは 4 つあります。

- 標準の Finance and Operations アプリの「すぐに利用できる」コンフィギュレーション (拡張機能なし)
- 1 つ以上の ISV ソリューションを含む Finance and Operations アプリのコンフィギュレーション
- 1 つ以上の顧客固有の拡張機能を含む Finance and Operations アプリのコンフィギュレーション
- 顧客固有の拡張機能と 1 つ以上の ISV ソリューションの組み合わせを含む Finance and Operations アプリのコンフィギュレーション

組織は、単純で透過的なサブスクリプション モデルを使用して、ユーザーと業務プロセスを簡単に追加することで、ビジネスの成長に合わせることができます。 詳細については、[Dynamics 365 ライセンス ガイド](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365) を参照してください。

## <a name="operating-model"></a>運用モデル

Finance and Operations アプリの運用モデルでは、サービスの有効期間中の顧客、実装パートナー、Microsoft に対する特定のロールと職責を定義しています。 詳細については、[クラウドの工程とサービス](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md) を参照してください。

### <a name="customer-activities"></a>顧客活動

顧客は、[Dynamics 365 実装ガイド](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide)、[Success by Design](/dynamics365/fasttrack/success-by-design-overview) のフレームワーク、[Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) で提供されるツールとベスト プラクティスのテンプレートに従って、パートナーや [Microsoft FastTrack](/dynamics365/fasttrack/) と協力し、ソリューションを実装します。 一般的な活動は次のとおりです。

- ユーザー ID とセキュリティ管理
- 業務プロセスの定義、開発、および操作
- 拡張機能の定義、開発、テスト、および操作
- 非実稼働環境の監視と管理
- アプリケーションの更新の管理と拡張機能の検証
- ISV ソリューションとサード パーティの統合の管理

### <a name="microsoft-responsibilities"></a>Microsoft の責任

Microsoft は、Microsoft SaaS サブスクリプションで顧客のサンドボックスと実稼働環境を展開し、アクティブに監視し、サービスを提供することにより Finance and Operations サービスを管理します。 この管理には、サービスを実行し、サービスの正常性について顧客と事前通信するために必要なシステム インフラストラクチャを割り当てることが含まれます。 責任には次のものが含まれます。

**インフラストラクチャ管理**
- セキュリティと分離
- オペレーティング システムと仮想化
- サーバー、ストレージ、ネットワーク
- データ センターの電源、ネットワーク、冷却

**アプリケーション プラットフォーム管理**
- 24 時間年中無休のアプリケーションの監視と通知
- 診断、プラットフォームの更新、パッチ、サービスの更新
- アプリケーションのルート指定、負荷分散、サイト レプリケーション
- 環境のプロビジョニングと管理
- データベース管理、高可用性 (HA)/障害復旧 (DR)、スケール、操作
- 配置の計算、スケール アップ、スケール ダウン

## <a name="system-configuration"></a>システム コンフィギュレーション

Finance and Operations アプリケーションは、トランザクションの量とユーザー負荷に応じてスケールします。 顧客の実装ごとに、次の要素で構成される固有のソリューションが生成されます。

- **データ構成** – 動作、組織のレイアウト、マスター データの構造 (財務分析コードや在庫分析コードなど)、トランザクション追跡の精度を制御する一意のパラメーター セット。
- **拡張機能とコンフィギュレーション** – コード拡張機能、ISV ソリューション、およびワークフロー、統合、レポート コンフィギュレーションを含む固有のコンフィギュレーションを使用する拡張機能メカニズム。
- **使用パターン** – オンラインとバッチの使用の固有の組み合わせ、統合されたデータ フローのためのアップストリームとダウンストリームシステム統合する機能、顧客が業務プロセスで使用する情報ビューに基づいて区別する機能。

Microsoft は、トランザクション量とユーザーの同時実行を処理できるサイズの顧客実稼働環境を構成します。 Microsoft が担当するタスクは次のとおりです。

- [LCS のサブスクリプション見積もりツール](../../dev-itpro/lifecycle-services/subscription-estimator.md) の顧客のプロファイル情報に基づいて、実稼働環境のリソースを正しく割り当てる
- 実稼働環境におけるサービスの可用性を継続的に監視および診断する
- Finance and Operations アプリでのシステム パフォーマンスの問題の分析とトラブルシューティング

実装がハイ パフォーマンスになるように構成されていることを確認するには、顧客は次のタスクを完了する必要があります。

- [LCS サブスクリプション見積ツール](../../dev-itpro/lifecycle-services/subscription-estimator.md) で Finance and Operations 実装に関する正確な使用状況情報を提供します。
- パフォーマンスとスケールの拡張機能を構築およびテストします。
- パフォーマンスのデータ構成を適切にテストします。
- 運用前に [パフォーマンス テスト](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) を実行して、スケーラビリティを確認します。

## <a name="onboarding-and-implementation"></a>オンボードと実装

次の表は、一般的なオンボードと実装のイベントを示しています。

| 申請 | 想定される Microsoft のアクション | 想定される顧客/実装パートナー アクション |
|---|---|---|
| 最初のオファーの購入 | LCS プロジェクトは、顧客によってトリガーされたイベントに基づいて、オファーの購入後に作成されます。 | エンタープライズ契約 (EA) またはクラウド ソリューション プロバイダー (CSP) の [業務プロセス](before-you-buy.md) を実行します。 パートナーが顧客のテナントを作成します (該当する場合)。 |
| アドオン購入 | 実装時に選択されたアドオンへのアクセスを顧客に付与します。 | 適用できません |
| 実装の計画と分析 | [ビジネス プロセス モデラー (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) や [Azure DevOps との相互運用性](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md) など、LCS に関連するツールを提供します。 | プロジェクト計画を実行し、Azure DevOps を設定し、システム オンボードを完了して、管理者アカウントを設定します。 |

詳細については、[実装プロジェクトのオンボード](../imp-lifecycle/onboard.md) を参照してください。

## <a name="globalization"></a>グローバリゼーション

Finance and Operations アプリは、世界中の複数の Azure リージョンで提供されます。 Finance and Operations アプリは、さまざまな国/地域および母国語をサポートする機能を提供します。 詳細については、[ローカライズと規制の機能](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features) を参照してください。

### <a name="countryregion-specific-considerations"></a>国/地域固有の考慮事項

- 現地のデータ所在地を必要とするフランスの法人とビジネスを行う規制対象の業界または商業組織の顧客は、[フランスの Finance and Operations](../../dev-itpro/deployment/france-local-deployment.md) を確認する必要があります。
- 中国で事業を行っている顧客は、[中国の 21Vianet で運用されている Finance and Operations](../../dev-itpro/deployment/china-local-deployment.md) を確認する必要があります。
- ロシアで事業を行っている顧客は、[ロシアの個人データローカリゼーション法](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia) を確認する必要があります。

### <a name="general-data-protection-regulation-gdpr"></a>一般データ保護規則 (GDPR)

Finance and Operations アプリでは、Microsoft はプロセッサとして動作します。 データ プロセッサとして、Finance and Operations は、顧客がデータ コントローラーとしての GDPR 責務に適応するのに役立つプロセスと機能を提供します。 詳細については、[GDPR の概要](../../dev-itpro/gdpr/gdpr-guide.md) を参照してください。

## <a name="environment-and-data-management"></a>環境とデータ管理

このセクションでは、サービスで発生する一般的な環境およびデータ管理イベントについて説明します。

### <a name="environment-and-data-management-events-for-production-instances"></a>実稼働インスタンスの環境およびデータ管理イベント

LCS は、環境およびデータ管理タスクの実行に使用される [セルフサービス ツール](../../dev-itpro/deployment/infrastructure-stack.md) および [データベース移動操作](../../dev-itpro/database/dbmovement-operations.md) を提供します。 次にいくつか例を挙げます。

**イベント:** [実稼働インスタンスの要求](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- [Go-Live チェックリスト](../imp-lifecycle/prepare-go-live.md) に入力し、[Microsoft FastTrack](/dynamics365/fasttrack/) チームに送信します。
- 実稼働インスタンスを要求する前に、[LCS サブスクリプション見積ツール](../../dev-itpro/lifecycle-services/subscription-estimator.md) を完了してください。
- [LCS 手法](../../dev-itpro/lifecycle-services/create-methodology.md) で指定されているすべての実装タスクを完了します。

**イベント:** [サンドボックス データベースを実稼働インスタンスにコピーする](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- モック Go-Live または実際の Go-Live の切り替えのために実行されます。

**イベント**: [メンテナンス モード](../../dev-itpro/sysadmin/maintenance-mode.md)

1. LCS でメンテナンス モードをオンにします。
2. 必要なメンテナンスを完了します。
3. LCS でメンテナンス モード をオフにします。

### <a name="environment-and-data-management-events-for-non-production-instances"></a>非実稼働インスタンスの環境およびデータ管理イベント

LCS は、環境およびデータ管理タスクの実行に使用される [セルフサービス プロビジョニング](../../dev-itpro/deployment/infrastructure-stack.md) および [データベース移動操作](../../dev-itpro/database/dbmovement-operations.md) を提供します。 次にいくつか例を挙げます。

**イベント:** [新しいサンドボックスインスタンスの配置](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- すべての必要なインスタンスが [計画され](../imp-lifecycle/environment-planning.md)、該当するアドオン オファーが購入されていることを確認してください。
- LCS で配置プロセスを実行します。
- LCS チェックリストで指定されているすべてのタスクを完了します。
    
>[!NOTE]
>開発サンドボックス環境は、[顧客の Azure サブスクリプションに配置](../../dev-itpro/dev-tools/access-instances.md) され、顧客によって管理される仮想マシン (VM)です。

**イベント:** [ゴールデン構成データーベースをサンドボックスから実稼働にコピーする](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- モック Go-Live または実際の Go-Live の切り替えのために実行されます。

**イベント:** [実稼働ポイントインタイム バックアップを非実稼働インスタンスに復元する](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- LCSの [データベースの更新](../../dev-itpro/database/database-refresh.md) オプションを実行します。
- コピー後: スクリプトを介して機密データの削除または難読化し、環境固有のアプリケーション コンフィギュレーション (統合エンドポイントなど) の調整、およびユーザーの有効化または追加を行います。 これらの変更は、[データ パッケージ](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package) を適用することによって行われることに注意してください。

**イベント:** [非実稼働インスタンス データベースのポイントインタイム復元](../../dev-itpro/database/database-point-in-time-restore.md)

- プロセスを元に戻すことはできないことを受け入れます。
- LCS のポイントインタイム復元操作を実行します。

**イベント:** トラブルシューティングおよび [デバッグ](../../dev-itpro/database/dbmovement-scenario-debugdiag.md) のレベル 2 のサンドボックス データーベースを開発サンドボックスにコピーします

- レベル 2 のサンドボックス環境で LCS のデータベース エクスポート操作を実行します。
- 開発環境でデータベースをインポートして更新します。

## <a name="data-backup-and-retention"></a>データのバックアップと保持

SaaS サブスクリプションの Finance and Operations 環境のデーターベースは、自動バックアップによって保護されています。 実稼働環境では、Microsoft がロールバックしない限り、自動バックアップは 28 日間保持されます。 サンドボックス (レベル 2+) 環境では、それらは 7 日間保持されます。 計画されたメンテナンス更新中に障害が発生した場合、実稼働環境のロールバックを実行できます。

自動バックアップの詳細については、[自動バックアップ - Azure SQL Database および Azure SQL Managed Instance](/azure/azure-sql/database/automated-backups-overview?tabs=single-database) を参照してください。

## <a name="service-activity-responsibilities"></a>サービス活動の責任

次の表では、サービスの一般的なシナリオと活動について説明します。 また、Microsoft、顧客、または Microsoft と顧客の両方が活動に対して責任を持っているかどうかも示します。

| 活動 | Microsoft の責任 | 顧客の責任 |
|---|---|---|
| **初期テナントのプロビジョニング** | | |
| サブスクリプション見積もりツールを使用して LCS の予測される負荷のサイズを決定し、特定の環境をプロビジョニングするように要求します。 | | X |
| すべての実稼働インスタンスと非実稼働インスタンスをプロビジョニングします。 | X | |
| 配置された実稼働インスタンスと非実稼働インスタンスを検証します。 | | X |
| **サービスの更新** | |
| 指定された非実稼働インスタンスおよび実稼働インスタンスにサービス更新を適用します。 | X | |
| LCS からサンドボックス インスタンスにサービス更新を手動で適用します。 更新を定義、開発、テストし、コード更新パッケージを LCS に提供します。 | | X |
| 要求およびスケジュールの拡張機能の更新が実稼働インスタンスに適用されます。 | | X |
| 更新が適用される前に、実稼働インスタンスのコードとデータのバックアップを作成します。 | X | |
| 障害が発生した場合は、実稼働インスタンスをコードおよびデータのバックアップにロールバックします。 | X | |
| **データ管理 (バックアップ、復元、更新)** | | |
| データベースをバックアップします。 | X | |
| 高可用性と障害復旧計画を決定します。 | X | |
| 実稼働インスタンス データベースのパフォーマンスを監視します。 | X | |
| パフォーマンスの実稼働インスタンス データベースを調整します。 | X | |
| 実稼働インスタンス データベースのポイントインタイム更新を非実稼働インスタンスに対して実行します。 | | X |
| **インフラストラクチャの更新** | | |
| 定期的なインフラストラクチャの更新をスケジュールします。 | X | |
| **スケール アップとスケール ダウン (ユーザー、ストレージ、インスタンス)** | | |
| 追加のユーザーおよび非実稼働アドオンを購入します。 | | X |
| LCS サブスクリプション見積もりツールの使用状況の変更を更新します。 | | X |
| サービスの使用に影響を与える重要なパフォーマンスの問題を報告します。 | | X |
| 該当するサービスに必要なリソースを事前に管理します。 | X | |
| インシデントを調査し、トラブルシューティングを行います。 | X | |
| **セキュリティ (ユーザー アクセス)** | | |
| サービスへのユーザー アクセスを提供します。 | | X |
| LCS を介して配置されたインスタンスの管理と運用のために LCS プロジェクトのアクセスを提供します。 | | X |
| **実稼働インスタンスの監視** | | |
| 実稼働インスタンスを 24 時間年中無休で監視します。 | X | |
| 実稼働インスタンスが関係するインシデントについて、顧客に事前に通知します。 | X | |
| **非実稼働インスタンスの管理および監視** | | |
| LCS を使用して非実稼働インスタンスを管理します。 | | X |
| 非実稼働インスタンスを監視します。 | | X |

## <a name="service-update-strategy"></a>サービス更新の戦略

[ソフトウェアのライフサイクル ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md) に従って、Finance and Operations アプリは継続的にサービスおよびサポートされる製品を対象とする [Microsoft Modern Lifecycle ポリシー](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy) に従います。 

Microsoft は、次の月に毎年 8 つの Finance and Operations アプリのサービス更新をリリースします。

- 1 月
- 2 月
- 4 月
- 5 月
- 7 月
- 8 月
- 10 月
- 11 月

>[!NOTE]
>4 月と 10 月は主な機能のリリース サイクルです。 顧客は、個々のサービス更新を最大 3 回の連続更新サイクルで一時停止できます。

詳細については、次のトピックを確認してください。

- [One Version のサービス更新の概要](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [LCS によるサービスの更新の構成](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [LCS によるサービスの更新の一時停止](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [LCS によるサービスの更新に関する通知を受け取る](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [サービスの更新を検証するための回帰テスト ツール](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 のロードマップとリリース サイクル](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>セキュリティと管理アクセス権

Finance and Operations の実稼働環境への管理アクセス権は、厳密に制御され、ログに記録されます。 顧客データは、[Microsoft オンライン サービスの使用条件](https://www.microsoft.com/licensing/terms/productoffering) に従って処理されます。 

### <a name="customer-administrative-access"></a>顧客管理アクセス権

次の表に示すように、顧客のテナント管理者は、実稼働インスタンスまたは非実稼働インスタンスにアクセスできます。

| 環境タイプ | 使用方法 | 顧客のアクセスのレベル |
|---|---|---|
| **非実稼働**<br>階層 1 のサンドボックス | 顧客が開発、デモ、またはトレーニング目的で顧客が配置する非実稼働環境。 | レベル 1 のサンドボックス (クラウド ホスト環境とも呼ばれます) は、LCS から顧客の Azure サブスクリプションに配置される顧客管理 VM です。 これは顧客の Azure サブスクリプションの VM なので、顧客はリモート デスクトップを介してこの環境への完全な管理アクセス権を持っています。 |
| **非実稼働**<br>レベル 2 (またはそれ以上) のサンドボックス | ユーザー受入テスト、統合テスト、トレーニング、ステージング、またはその他の実稼働前のシナリオに対して顧客が配置する非実稼働環境。 | レベル 2 以上のサンドボックスは、Finance and Operations SaaS サブスクリプションに配置されます。 非実稼働環境に関連付けられている Azure SQL データベースへのアクセスは、[ジャストインタイム アクセス](../../dev-itpro/database/database-just-in-time-jit-access.md) を介して許可されます。 リモート デスクトップ アクセスは使用できません。 |
| **実稼働** | プロジェクトで [初回 Go-Live の準備](/imp-lifecycle/environment-planning.md#production-system-readiness) ができたら、実稼働環境を配置することができます。 | 実稼働環境は、SaaS サブスクリプションに配置されます。 すべてのアクセスは、ブラウザ、サービス エンドポイント、または LCS を介して行われます。 |

### <a name="microsoft-administrative-access"></a>Microsoft の管理アクセス権

次の表は、Microsoft の管理者ごとに異なるアクセス レベルを示しています。

| 管理者 | 顧客データ |
|---|---|
| Operations 対応チーム<br>(主要な人員にのみ制限されます) | アクセスは、サポート チケットを介して許可されます。 アクセスは監査され、サポート活動の期間に限定されます。 |
| Microsoft 顧客サポート サービス (CSS) | 直接アクセスはありません。 顧客は、画面共有を使用して、サポート スタッフと一緒に作業して問題をデバッグできます。 |
| エンジニアリング | 直接アクセスはありません。 Operations 対応チームは、画面共有を使用して、エンジニアリングと一緒に作業して問題をデバッグできます。 |
| Microsoft のその他 | アクセスはありません。 |

## <a name="monitoring"></a>監視

Microsoft は、顧客の実稼働インスタンスを監視および診断するための広範なツールセットに投資しています。 Microsoft は、顧客の実稼働環境を 24 時間年中無休で監視しています。 詳細については、[運用サポートと監視](../imp-lifecycle/production-support-monitoring.md) を参照してください。

| Microsoft の責任 | 顧客の責任 |
|---|---|
| <ul><li>サービスの利用可能性を監視します。</li><li>Application Object Server (AOS)、バッチ、データのインポート/エクスポート フレームワーク (DIXF)、Commerce、Management Reporter などの重要なコンポーネントの正常性指標とウォッチドッグを介して、継続的に監視および警告します。</li><li>インフラストラクチャ サービス (Azure Active Directory\[Azure AD\] や Azure SQL など) によって発生するパフォーマンスの低下を監視します。</li><li>単一のプロセスまたはバッチ ジョブが異常を引き起こしていると Microsoft が判断した場合、そのプロセスまたはジョブは顧客との通信後に終了します。</li></ul> | <ul><li>機能およびパフォーマンスの問題が発生する可能性があるアプリケーション構成および拡張機能の変更を監視します。</li><li>アプリケーション エラーは、監視ツールを使用して診断する必要があります。 これらのツールを使用して、ユーザーによって報告されたパフォーマンスの異常を診断します。</li><li>システムに予想されるピーク時の使用量を超える負荷が予想される場合は、Microsoft に通知してください。</li><li>該当するサービスが実稼働インスタンスで使用できない場合、顧客は LCS を使用して [稼働停止](../../dev-itpro/lifecycle-services/report-production-outage.md) を報告できます。</li></ul> |

顧客は、オンラインで LCS を介してサポート要求を送信することにより、Microsoft が最も効果的かつ効率的な方法で、迅速かつ深い技術的な専門知識を提供することができます。 電話のオプションを利用することもできますが、オンライン オプションが利用できない場合にのみ使用してください。 詳細については、[電話サポート オプション](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support) を参照してください。

## <a name="incident-management"></a>インシデント管理

Microsoft は重要度レベルに基づいてインシデントに対応し、修正を行います。 Microsoft のインシデントの重要度レベルは、インシデントの初期評価中、および影響と範囲に関する詳細情報が利用可能になったときに変更できます。 インシデントが軽減された場合、そのインシデントの重要度は変更されません。

重要度レベルの詳細については、[この重要度テーブル](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request) を参照してください。

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>高い可用性と障害復旧による事業の継続性 

Microsoft は、Azure リージョンの広範囲で稼働停止が発生した場合は、Finance and Operations アプリの実稼働インスタンスの事業の継続性と障害復旧を提供します。 詳細については、[事業の継続性と障害復旧](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md) を参照してください。

- **高可用性** – HA 機能は、Azure データセンター内の単一のノードの失敗により引き起こされるダウンタイムを防ぐ方法を提供します。 各サービスのクラウド アーキテクチャは、計算層に Azure 可用性セットを使用して、単一障害点イベントを防止します。 データベースの HA は、[Azure SQL HA 機能](/azure/azure-sql/database/high-availability-sla) 通じて提供されます。
- **障害復旧** – [Azure の障害復旧機能](/azure/best-practices-availability-paired-regions) は、Azure データセンター全体に大きな影響を与える障害から各サービスを保護します。 これらの機能例を次に示します。

    - プライマリ データベース (ビジネス データベース) の Azure SQL のアクティブ geo レプリケーション。
    - 他の Azure リージョンでの Azure Blob Storage (ドキュメントの添付ファイルを含む) のジオ重複コピー。
    - Azure SQL および Azure Blob Storage レプリケーションのセカンダリ地域。

プライマリのデータ格納場所は、レプリケーションでサポートされています。 したがって、Management Reporter やエンティティ格納などの各サービスのコンポーネントは、プライマリ データベースから変換されたデータを使用します。 このデータは、リカバリ サイトの設定およびサービスの開始後に生成する必要があります。 顧客コード コンポーネントと回復されたデータの格納場所は、サイトを再配置するために使用されます。 この再配置により、ネットワークやその他のコンポーネントとともに計算ノードのレプリケーションを指定し、回復されたデータ格納を使用してセカンダリ サイトを設定できます。 障害復旧を使用して顧客の実稼働インスタンスを復旧する場合、Microsoft と顧客は [インシデント管理](service-description.md#incident-management) の責任を満たします。

Microsoft の障害復旧の計画と手順は、System and Organization Controls (SOC) の監査を通じて定期的に検証されます。 これらのコンプライアンス監査では、Dynamics 365 Finance and Operations アプリを含む、Microsoft の DR の技術的および手順のプロセスが証明されます。 [SOC コンプライアンス](/compliance/regulatory/offering-soc-2) 監査レポートおよびその他のすべてのコンプライアンス レポートは、[Microsoft Trust Center コンプライアンスのサービス](/compliance/regulatory/offering-home) で利用できます。

| Microsoft の責任 | 顧客の責任 |
|---|---|
| Microsoft は、プライマリ実稼働インスタンスが配置されると、Azure ペア データセンターにセカンダリ環境をプロビジョニングします。 詳細については、[事業の継続性と障害復旧 (BCDR): Azure Paired Regions](/azure/best-practices-availability-paired-regions) を参照してください。 | None |
| Microsoft は、プライマリ実稼働インスタンスを配置すると、Azure SQL と Azure Blob Storage のジオ重複が有効します。 | None |
| Microsoft は、Azure SQL データベースの自動バックアップを有効にします。 | None |
| <p>障害が発生した場合、Microsoft は、顧客に対してフェールオーバーを実行する必要があるかどうか、およびデータが失われるかどうかを判断します。 データ損失は最大 5 秒です。 詳細については、[Azure SQL データベース ジオ リストア](https://azure.microsoft.com/blog/azure-sql-database-geo-restore) を参照してください。</p><p>データが失われた場合、Microsoft は、フェールオーバーのために顧客のサインオフを要求します。</p> | データが失われた場合、フェールオーバーをトリガーするために、顧客は書面によるサインオフの提供が必要となる場合があります。 |
| フェールオーバーが発生した場合、該当するサービスは限定モードで機能します。 フェールオーバー モードでは、更新のメンテナンスは、トリガーできません。 | 顧客は、フェールオーバー モードでパッケージの配置、またはその他の定期的なメンテナンス要求を要求できません。 |
| データセンターが運用可能になると、Microsoft はプライマリの Azure 地域の実稼働インスタンスにフェール バックします。 通常の運用を再開します。 | 顧客は、プライマリの Azure 地域の実稼働インスタンスに対するフェールバックでサインオフが必要となる場合があります。 |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operations サポートの提供

技術サポートは、Finance and Operations サービスが提供されるマーケットで提供されます。 [サポート エクスペリエンス](../../dev-itpro/lifecycle-services/lcs-support.md) は、LCS または Finance and Operations アプリで提供されます。 次にいくつか例を挙げます。

- LCS の [問題検索](../../dev-itpro/lifecycle-services/issue-search-lcs.md)
- Finance and Operations アプリの [統合された技術サポート](../../dev-itpro/lifecycle-services/support-experience.md)
- LCS の [クラウドを利用したサポート](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md)

Microsoft では、Finance and Operations のお客様に 3 つのサポートプラン (プレミア、Professional Direct、およびサブスクリプションに含まれるサポート) を提供しています。 サポート レベルはプランごとに異なります。 次の表に、3 つのプランの比較を示します。

| サポート機能 | プレミア | Professional Direct | サブスクリプション |
|---|---|---|---|
| 無制限の障害/対応インシデント送信 | あり | あり | あり |
| LCS 経由での 24 時間年中無休アクセス | あり | あり | あり |
| インシデントの応答時間 | 1 時間未満 | 1 時間未満 | 翌営業日 |
| 相談時間 | プールは契約ごとに取得されます。 | なし | なし |
| 専任のサポート アカウント マネージャー | あり | なし | なし |
| 専任のサポート エンジニア | 別の契約に基づいて行われる | なし | なし |

詳細については、[サポート概要](/power-platform/admin/support-overview) を参照してください。

### <a name="process-to-engage-support"></a>サポートを受けるためのプロセス

Finance and Operations アプリが関係するインシデントが発生した場合、顧客は LCS を通じて Microsoft にサポート チケットを送信します。 CSS は、顧客のサポート プランと、CSS で指定されたインシデントの重要度に基づいて、インシデントを処理します。

### <a name="service-level-agreement"></a>サービス レベル アグリーメント

Microsoft は、サービスの月あたり 99.9% の可用性レートを約束しています。 Microsoft がサービス レベル アグリーメント (SLA) で説明されている該当するサービスのサービス レベルを達成および維持しない場合、顧客はそのサービスの月間サービス料金の一部をクレジットとして受け取ることができる場合があります。 サービス クレジットを開始する方法の詳細については、SLAの [請求](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services) セクションを参照してください。

## <a name="important-resources"></a>重要なリソース

- **[トラスト センター](https://www.microsoft.com/trust-center)** – Finance and Operations データが保管されている場所に関する情報に加え、プライバシー、コンプライアンス、およびセキュリティ手順に関する追加情報を取得します。
- **[ライセンス条件とドキュメント](https://www.microsoftvolumelicensing.com/)** – Microsoft ボリューム ライセンス プログラムを通じてライセンスされている製品およびサービスの使用に関連するライセンス条件、条件、補足情報にすばやくアクセスできます。
- **[ライセンス条件](https://www.microsoft.com/licensing/product-licensing/)** – このページのリソースでは、Microsoft の商用ライセンス プログラムを通じて購入するソフトウェアおよびオンライン サービス製品の契約条件を定義しています。
- **[Microsoft Lifecycle ポリシー](/lifecycle/)** – このページでは、製品のライフを通してサポートを受けるための一貫した予測可能なガイドラインを示します。
- **[ライセンス ガイド](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Dynamics 365 のライセンスを取得する方法の詳細については、このガイドを参照してください。
- **[カスタマー サポート](https://dynamics.microsoft.com/support/)** – Dynamics 365 アプリの業界をリードするサポートを利用できます。
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – アプリケーションのライフサイクルを管理し、予測可能で反復可能な高品質の実装を行います。

## <a name="definitions"></a>定義

### <a name="azure-region"></a>[Azure リージョン](/azure/availability-zones/az-overview#regions)

1 つ以上の Azure のデータセンターが存在する地理的地域。 たとえば、米国やヨーロッパが含まれます。

### <a name="business-process-modeler-bpm"></a>[ビジネス プロセス モデラー (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Finance and Operations アプリでサポートされているアメリカ生産性品質センター (APQC) の業務プロセス定義を使用して、指定された実装のフィットギャップ分析を完了するのに役立つ LCS のツール。

### <a name="cloud-solution-provider"></a>クラウド ソリューション プロバイダー

Microsoft クラウド ソリューション プロバイダー (CSP) プログラムの一部であり、付加価値のあるクラウド サービス、サポート、1 つの請求書、および大規模な顧客管理を提供するパートナー。

### <a name="customer"></a>顧客

Finance and Operations アプリを使用し、Office 365 のテナントによって表されるビジネス エンティティ。

### <a name="development-environment"></a>開発環境

拡張機能の開発に使用される非実稼働サンドボックス環境。 顧客は、この環境を LCS から独自の Azure サブスクリプションに配置します。 この環境は、デモ、トレーニング、または他のテスト タスクにも使用できます。 レベル 1 の [サンドボックス](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher) とも呼ばれます。

### <a name="downtime"></a>ダウンタイム

Microsoft が自動正常性監視およびシステム ログから判断したように、有効期間が切れていないプラットフォームまたはサービス インフラストラクチャの障害のため、ユーザーがアクティブなテナントにサインインまたはアクセスできない期間。 ダウンタイムには、予定されたダウンタイム、サービス アドオン機能が利用できない、サービスの変更によるサービスへのアクセスの失敗、またはスケール単位の能力を超えている期間は含まれません。

### <a name="implementation-partner"></a>実装パートナー

顧客が Finance and Operations ソリューションをカスタマイズ、構成、実装、および管理するために選択したパートナー。

### <a name="incident"></a>インシデント

顧客が Finance and Operations サービスを使用している間に発生し、LCS 経由でチケットを送信する際に発生する場合。

### <a name="microsoft-customer-support-services-css"></a>Microsoft 顧客サポート サービス (CSS)

Finance and Operations アプリの品質サービスを提供することに専念する Microsoft のグローバル サポート チーム。

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

トライアルから実装、実稼働後の管理とサポートまで、Finance and Operations アプリのライフサイクル管理のための管理ポータル。 詳細については、[Lifecycle Services のリソース](../../dev-itpro/lifecycle-services/lcs.md) を参照してください。

### <a name="non-production-instance"></a>非実稼働インスタンス

顧客が拡張機能の検証および他の開発タスクの実行に使用するサービスの次のいずれかのインスタンス。

- **サンドボックス レベル 1** – 開発者インスタンス (顧客がホストしている)
- **サンドボックス レベル 2** – スタンダード承認テスト インスタンス
- **サンドボックス レベル 3 から 5** – アドオン サンドボックス

レベル 2 から 5 の詳細については、[正しいレベル 2 以上の環境の選択](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment) を参照してください。

### <a name="production-instance"></a>実稼働インスタンス

顧客が日常の「ライブ」のトランザクションや業務プロセスを管理するために使用する Finance and Operations 環境。

### <a name="sandbox-environment"></a>サンドボックス環境

顧客がデモ、トレーニング、ユーザー受入テスト、拡張機能の検証、他のテスト作業に使用する非実稼働環境。

### <a name="service"></a>サービス

Finance and Operations アプリに含まれるいずれかのコア サービス。

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Microsoft オンライン サービスのサービス レベル契約 (SLA)

SLA は Microsoft オンライン サービスに適用されます。 詳細については、[サービス レベル契約](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services) を参照してください。

### <a name="service-update"></a>サービスの更新

Microsoft は、サービスの更新を通じて、一貫した基準で Finance and Operations 環境を提供しています。 顧客は、業務ニーズに基づいて、独自のサービス更新カレンダーを設定します。 詳細については、[1 つのバージョンのサービス更新](../../dev-itpro/lifecycle-services/oneversion-overview.md) を参照してください。

### <a name="user"></a>ユーザー

Finance and Operations 環境を使用し、顧客のテナントに関連付けられている 1 人のユーザー。
