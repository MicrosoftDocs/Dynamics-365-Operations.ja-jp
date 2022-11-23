---
title: Dynamics 365 Human Resources での顧客の財務と運用インフラへの移行
description: 財務と運用インフラにMicrosoft Dynamics 365 Human Resources を移行された顧客の事例をご紹介します。
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4df9a68ea0128378224bf77bd66423fd2e13fa55
ms.sourcegitcommit: e5b290bac7e8f468167caa1a5607aac6eac9aaea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760365"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Dynamics 365 Human Resources 顧客の移行

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

顧客移行とは、顧客データベースを財務と業務インフラに「リフトアンドシフトする」 (移動) させることです。 自動化された移行ツールが使用されます。 その結果、顧客の人事データベースを利用した新しい財務と運用環境が完成しました。

## <a name="prerequisites"></a>必要条件

### <a name="user-access-and-permissions"></a>ユーザーアクセスとアクセス許可

- Microsoft Dynamics Lifecycle Services ユーザーには、**組織の管理者** ロールが必要です。
- ユーザーは[Azure DevOps プロジェクトを作成](/azure/devops/organizations/projects/create-project)するか、既存の Azure DevOps プロジェクトを使用できる必要があります。
- ユーザーは、[Azure DevOps 個人用アクセス セキュリティ トークンを作成する](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate)アクセス許可を持っている、または使用できるトークンが必要です。

### <a name="dataverse-environment-backup-sandbox"></a>Dataverse 環境のバックアップ (サンドボックス)

 - 任意だが推奨: 人事部の本番環境のコピーを使用して、既存の人事部サンドボックス環境を更新します。
 - Power Platform 管理センターを使用して 新規 Dataverse 環境を作成します。
 - スタンドアロンの Human Resources アプリにリンクされている既存の Dataverse 環境を、前の手順で作成した環境にコピーします。

> [!NOTE]
> データベースを追加する場合は、**Dynamics 365アプリ** を有効にするオプションが **はい** に設定してください。 詳細については、[Power Platform 環境を準備する](hr-cust-migration.md#prepare-a-power-platform-environment) を参照してください

### <a name="dataverse-capacity"></a>Dataverse のキャパシティ

1. Power Platform 管理センターの **集計** ページを使用して、[Dataverse ストレージ](/power-platform/admin/finance-operations-storage-capacity) に環境用コピー用の十分な使用可能な能力が与えらた能力を確認します。
2. 十分な容量がない場合は、[ストレージの空き容量を確保するガイダンス](/power-platform/admin/free-storage-space)を利用して、全体の使用量を減らしてください。 顧客は、[ストレージ容量を追加](/power-platform/admin/add-storage)できます。

## <a name="customer-migration-process"></a>顧客の移行プロセス

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>人事移行のための Lifecycle Services プロジェクトの作成

まず、Lifecycle Services で新しい財務と運用の導入プロジェクトを作成します。 この顧客には、既存の人事 Lifecycle Services プロジェクトが作成されます。 既存の人事環境は、新しい財務と運用プロジェクトに移行されます。

新しいプロジェクトを作成するには、次の手順を実行します。

1. グローバル管理者または指定されたサービス アカウントのユーザーとして、Lifecycle Services にサインインします。
2. Lifecycle Services のホーム ページで、**作成/新規 (+)** を選択します。
3. 製品に財務と運用を選択します。
4. **プロジェクトの目的** フィールドで、**導入** を選択します。
5. プロジェクトの名前と説明を入力します。
6. **プロジェクトのカスタム タイプ** フィールドで、**Microsoft Dynamics 365 Human Resources の移行** を選択します。
7. チェック ボックスをオンにして、条件に同意します。
8. **作成** を選択します。

新しい Lifecycle Services プロジェクトを作成したら、以下の手順で設定と構成を行います。

1. **プロジェクトのオンボード** を選択して、プロジェクトのオンボードを完了します。 詳細については、[プロジェクトの研修](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md)を参照してください。

    - 現在の環境と同じ地域を選択します。 この選択は移行に影響を与える影響を受け取らない。
    - レガシ システムの場合は、**その他** を選択 します。

2. プロジェクトの設定を完了させます。 この手順の一環として、必要に応じて SharePoint オンライン ライブラリ、Azure DevOps、Azure 接続を構成する必要があります。 詳細については、[Lifecycle Services (LCS) ユーザー ガイド](../dev-itpro/lifecycle-services/lcs-user-guide.md)を参照してください。

> [!NOTE]
> 顧客は、既存の Azure DevOps プロジェクトと関連する個人用アクセス セキュリティ トークンを使用できます。 既存のプロジェクトを使用する場合、そのプロジェクトに関連する構成が自動的に利用可能になり、正確性を確認することができます。

### <a name="migrate-a-human-resources-sandbox-environment"></a>人事のサンドボックス環境の移行

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>サンドボックス環境の移行準備

新しい Lifecycle Services プロジェクトが作成され、プロジェクトのオンボーディングプロセスが完了すると、最初の環境を移行する準備ができています。 このプロセスを開始する前に、スタンドアロン インフラストラクチャ上の運用環境から移行するサンドボックス環境を更新することをお勧めします。

#### <a name="prepare-a-power-platform-environment"></a>Power Platform 環境の準備

> [!NOTE]
> この手順は、移行前の環境でのみ使用できます。 運用環境を移行した場合、運用環境に付属する既存の Power Platform 管理センターの環境は引き継がれます。 データベースを追加する際、**Dynamics 365 アプリを有効にする** ボタンが **はい** に設定されていることを確認します。 

- Power platform 管理センターで、サンドボックスの移行に使用する [データベースがある環境を作成](/power-platform/admin/create-environment#create-an-environment-with-a-database) するか、既存の環境を選択します。
- [環境をコピー](/power-platform/admin/copy-environment) して、マッピングに使用する Power Platform 環境を更新します。

#### <a name="migrate-the-sandbox-environment"></a>サンドボックス環境の移行

1. グローバル管理者または指定されたサービス アカウントのユーザーとして、Lifecycle Services にサインインします。

    > [!NOTE]
    > 名前付きのユーザー アカウントを使用することをお勧めします。 サインインするユーザーは、スタンドアロンの人事 Lifecycle Services プロジェクトにおいて、**プロジェクト オーナーま** たは **環境マネージャー** のセキュリティロールを持っている必要があります。

2. 新しく作成された人事移行プロジェクトを開きます。
3. 移行方法とプロジェクト オンボードの適切なフェーズを確認し、完了する移行方法論とプロジェクトのオンボードの適切なフェーズを確認し、完了します。
4. プロジェクト ダッシュボードの **既定: 標準受入テスト** ウィンドウで、**HR の移行** を選択します。
5. **移行する環境の選択** ウィンドウで、適切な Lifecycle Services プロジェクトと、作成元の人事環境 (作成元のスタンドアロン人事アプリケーションから) を選択します。
6. **新しい Power Platform 環境へのマッピング** を有効にし、適切な Power Platform 環境を選択します。 その後、**次へ** を選択します。
7. **展開の設定 (財務と運用 - サンドボックス)** ウィザードを完了して詳細と顧客のサインオフを確認し、**展開** を選択します。

環境の状態に進捗状況が示されます。 この状態は、**荷積み** から **展開中**、**展開後** に変更されます。

> [!NOTE]
> 稼働中のプロジェクト準備完了チェックリストが完了するまで、生産ウィンドウは使用できません。 詳細については、「[Go-Live の準備](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)」を参照してください。

#### <a name="considerations-and-assumptions"></a>考察と仮定

テナント上の Lifecycle Services プロジェクトに、次のような特徴を持つ人事サンドボックス環境が存在します。

- 人事マージ環境は、マージされた既存の環境にリンクされません。 特定の人事管理環境で一度に実行できる移行は 1 回のみです。
- 一度に許可される数は、人事管理ライセンスに基づいて指定されます。 十分なライセンスがテナントに対して購入されている場合は、追加の環境がプロジェクトの **環境** ウィンドウに表示されます。
- 移行は同じ種類の環境に対して実施する必要があります。 つまり、サンドボックスからサンドボックス、または運用から運用への移行のみ可能です。

    > [!NOTE]
    > 本番環境かサンドボックスかを判断する際には、人事の環境タイプのみが考慮されます。 環境の分類に誤りがある (本番環境がサンドボックス環境と表示されている、またはサンドボックス環境が本番環境と表示されている) 場合は、サポートまでご連絡ください。

- 移行に失敗した場合は、失敗のエラー メッセージが表示され、**削除** ボタンが使用可能になります。 このボタンを使用して、失敗した移行を削除します。 その後、環境を再移行することができます。

#### <a name="validate-the-sandbox-migration"></a>サンドボックスの移行を検証する

移行プロセスが正常に完了した後、詳細なテスト計画を作成して、すべての業務プロセスを検証およびサインオフします。

テストを開始する前に、次の詳細を検証します:

- 移行した環境にアクセスできる場所 (生成された URL) を確認します。
- 移行したサンドボックスにユーザーがアクセスできることを確認します。
- 移行したサンドボックス環境に関連する Dataverse 環境にアクセスできることを確認します。
- さまざまなデータをスポットチェックして、最新のデータが使用可能な日付を確認します。
- 検証のために重要なビジネス プロセスを完了します。
- セキュリティポリシーが適用できることを確認します。
- バッチジョブが期待通りに起動することを確認します。

移行したサンドボックスにはリモート デスクトップでのアクセスはできません。 セルフサービス機能およびツールを使用して、Tier 2+ サンドボックス環境に対して以下のアクションを実行することができます:

- [Azure SQL データベース](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database) にアクセスします。
- [ログ ファイル](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files)にアクセスします。
- [perfmon ツール](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools)を使用します。
- [メンテナンス モードのオン/オフ](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs)を切り替えます。
- [サービス](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services)を再起動します。
- [Regression Suite Automation Tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool) を構成します。

詳細については、 [セルフサービス配置の FAQ](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md) をご参照ください。

### <a name="migrate-a-human-resources-production-environment"></a>人事の運用環境の移行

移行と検証が完了した後は、次の手順に従って運用環境を移行します。

#### <a name="prerequisites"></a>必要条件

- サブスクリプション エスティメーターが完成していること。
- 本稼働の[準備評価](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md)を完了する必要があります。

#### <a name="migrate-the-production-environment"></a>運用環境の移行

1. グローバル管理者または指定されたサービス アカウントのユーザーとして、Lifecycle Services にサインインします。

    > [!NOTE]
    > 名前付きのユーザー アカウントを使用することをお勧めします。 サインインするユーザーは、Lifecycle Services プロジェクトの **プロジェクト オーナー** または **環境マネージャー** のセキュリティ ロールを持っている必要があります。

2. 新しい人事移行プロジェクトを開きます。
3. 移行方法論とプロジェクト オンボードの適切なフェーズを確認し、完了します。
4. プロジェクト ダッシュボードの **運用** ウィンドウで、**HR の移行** を選択します。
5. **移行する環境の選択** ウィンドウで、適切な Lifecycle Services プロジェクトと、作成元の人事環境 (作成元のスタンドアロン人事アプリケーションから) を選択します。 その後、**次へ** を選択します。
6. **展開の設定 (財務と運用 - サンドボックス)** ウィザードを完了して詳細と顧客のサインオフを確認し、**展開** を選択します。

環境の状態には、展開の進行状況が表示されます。 この状態は、**荷積み** から **展開中**、**展開後** に変更されます。

#### <a name="post-migration-considerations"></a>移行後の考慮事項

- ご利用の環境に最新の[品質アップデート](/fin-ops-core/fin-ops/get-started/quality-updates)を適用します。
- [仮想テーブル](hr-admin-integration-common-data-service-virtual-entities.md)を使用している 場合は、エンドポイントを変更します。
- デュアル書き込み統合の変更 有効にする必要があるエンティティを評価します。
- 統合のためにデュアル書き込みの代わりに仮想テーブルを使用することを検討してください。

#### <a name="dual-write-integration"></a>二重書き込みの統合

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Microsoft Power Platform デュアル書き込み統合の設定

1. Power Platform 管理センターにアクセスし、左側のナビゲーションから **環境** を選択します。
2. 以前にコピー/更新された環境を選択し、状態が **準備完了** となっていることを確認します。
3. Lifecycle Services に移動し、移行プロジェクトの状態が **展開済み** となっている必要があります。
4. 移行した環境で、**完全な詳細** を選択して追加の詳細を確認し、[デュアル書き込みアプリケーションを設定](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments)します。
5. **デュアル書き込みアプリケーションの構成** ウィンドウで、データベース間のデータのマッピングと同期に合意するチェック ボックスをオンにし、**構成** を選択します。
6. メッセージ ボックスに、デュアル書き込みの構成が成功したという通知が表示された場合は、**OK** を選択します。
7. 詳細で設定の進行状況を確認することができます。
8. 構成の完了後は、**Power Platform 環境へのリンク** を選択して、使用可能なデータ エンティティを同期します。
9. 状態が、環境が正常にリンクされたことを示している場合は、Power Platform 管理センターに移動して、適切なデータ エンティティを確認して選択します。
10. 左ウィンドウで、**Dynamics 365 アプリの \> リソース** を選択します。
11. デュアル書き込み人事アプリの状態が **有効** になっていることを確認します。
12. デュアル書き込み人事管理アプリを選択し、**インストール** を選択します。
13. **デュアル書き込み Dynamics 365 Human Resources アプリのインストール** ウィンドウ で、パッケージをインストールする適切な環境を選択します。
14. サービス条件に合意する場合は、チェック ボックスをオンにし、**インストール** を選択します。
15. Dynamics 365 アプリ環境では、インストールの進行中に 状態が **インストール中** になります。 インストールが完了すると、状態が **インストール済** に更新されます。

##### <a name="review-and-apply-a-dual-write-solution"></a>デュアル書き込みソリューションの確認と適用

1. 新規財務と運用環境で、**データ管理\> デュアル書き込み** に移動します。
2. **ソリューションの適用** を選択します。
3. ウィンドウで、**Dynamics のインストール済ソリューション**、**デュアル書き込みアプリケーション コア エンティティ マップ**、**Dynamics 365 Human Resources マップ** を選択します。 続いて **適用** を選択します。 ソリューションが適用されていることを確認するメッセージが表示されます。 ソリューションが正常に適用されると、利用可能なすべてのテーブル マップが表示されます。
4. 利用可能なテーブル マップを確認し、デュアル書き込みによる統合を選択し実行します。
5. テーブル マップに対して初めてデュアル書き込み統合を実行する場合は、**初期同期** チェック ボックス をオンにします。 ソースの人事管理環境に既存の統合がある場合は、テーブル マップの統合を実行するときに **初期同期** チェック ボックスをオンにする必要があります。

#### <a name="recommended-practices"></a>推奨される運用

このセクションでは、スタンドアロンのインフラストラクチャから財務と運用のインフラストラクチャに移行する場合の推奨事項について説明します。

- 人事環境の移行に関して Microsoft Dynamics パートナーと一緒に作業することを強くお勧めします。
- 移行した環境で、ユーザー受入テスト (UAT) 全体を実施するために適切な時間を計画します。
- 統合を移行する詳細な手順を計画および文書化し、移行される環境に移行します。
- 移行に伴うカットオーバーのプロセスを概説する詳細なチェックリストを作成します。
- 移行の実行中は、業務に適切なダウンタイムを計画します。
- FastTrack の認定を受けた顧客は、FastTrack のソリューション アーキテクトと連携して、移行プロセスの監督支援を受けることを強くお勧めします。
- 最初の移行を行う前に、スタンドアロンのインフラストラクチャでサンドボックス環境を更新することを強くお勧めします。 この更新には、移行先のサンドボックス環境と接続されている Dataverse 環境も含める必要があります。
- Lifecycle Services プロジェクトの展開、移行、作成時には、サービス アカウントを使用することを強くお勧めします。
- UAT 検証用の環境を、最新の一般入手可能バージョン (GA) リリースにアップグレードする計画をたてます。 詳細については、[考慮が必要な事項](hr-infrastructure-merge.md#considerations) を参照してください。
