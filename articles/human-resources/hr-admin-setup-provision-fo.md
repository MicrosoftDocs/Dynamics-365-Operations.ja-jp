---
title: 財務と運用のインフラストラクチャに人事管理をプロビジョニングする
description: この記事では、財務と運用のインフラストラクチャに Microsoft Dynamics 365 Human Resources の新しい運用環境をプロビジョニングするプロセスについて説明します。
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178415"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>財務と運用のインフラストラクチャに人事管理をプロビジョニングする

_**適用先:** 財務と運用アプリのインフラストラクチャ上の人事管理_ 

> [!NOTE]
> 2022 年 7 月から、スタンドアロンの人事管理インフラストラクチャに新しい人事管理環境をプロビジョニングすることはできず、新しい Microsoft Dynamics Lifecycle Services (LCS) プロジェクトを作成することもできません。 顧客は、財務および運用のインフラストラクチャに人事管理の環境を展開することができます。

この記事では、財務と運用のインフラストラクチャに Microsoft Dynamics 365 Human Resources の新しい運用環境をプロビジョニングするプロセスについて説明します。

## <a name="prerequisites"></a>必要条件

新しい環境のプロビジョニングを開始する前に、次の前提条件が整っている必要があります。

- クラウド ソリューション プロバイダー (CSP) またはエンタープライズ アーキテクチャ (EA) 契約を通して Human Resources を購入しました。 Human Resources サービス プランがすでに含まれている既存の Dynamics 365 ライセンスがあり、この記事の手順を完了できない場合は、サポートにお問い合わせください。
- グローバル管理者は [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) にサインインし、財務と運用の新しいプロジェクトを作成しました。

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources 試用環境のプロビジョニング

> [!NOTE]
> 2022 年 4 月から、人事管理の試用環境は、スタンドアロン アプリケーションでは使用できません。 財務と運用アプリ内の人事管理機能の評価に関心を持つ潜在顧客は、30 日間の無料試用版をデモ データと共に使用できます。 Dynamics 365 Finance には、スタンドアロン アプリケーションのマージを通じて Finance インフラストラクチャに提供される人事管理機能が含められます。 詳細については、[HR 製品のマージによる顧客向け機能の統合](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers)を参照してください。 Dynamics 365 Finance 試用版の詳細については、ステップ バイ ステップ [ガイド](../fin-ops-core/fin-ops/get-started/before-you-buy.md)を参照してください。

## <a name="plan-human-resources-environments"></a>Human Resources の環境を計画する

最初に Human Resources を作成する前に、プロジェクトに必要な環境を慎重に計画する必要があります。 人事管理への基本的なサブスクリプションには、運用環境と既定のスタンダード承認テスト (サンドボックス) 環境の 2 つの環境が含まれます。 プロジェクトの複雑さに応じて、プロジェクト活動をサポートするため、追加の環境を購入するオプションがあります。

オプションの追加環境について考慮事項があります。

- **データ移行** – サンドボックス環境をプロジェクト全体でテストに使用できるようにするためのデータ移行活動。 追加の環境があることにより、テストと構成の活動が別の環境で同時に行われている間も、データ移行活動を継続することができます。
- **統合** – ネイティブ統合や、給与、申請者追跡システム、福利厚生システムやプロバイダーなどのカスタム統合を含む統合の構成とテスト。
- **トレーニング** – 新しいシステムを使用するよう従業員をトレーニングするために、一連のトレーニング データを使用して構成された別の環境が必要となる場合があります。 
- **複数フェーズのプロジェクト** – プロジェクトの最初の移動後に計画されているプロジェクト フェーズで構成、データ移行、テスト、その他の活動に対応するにあたって、追加の環境が必要となる場合があります。
- **開発** – 財務と運用のインフラストラクチャで、ソリューションを拡張し、独自のカスタマイズを開発することができます。 各開発者は、独自の開発環境を使用する必要があります。 詳細については、トピック [開発環境の配置とアクセス](/fin-ops-core/dev-itpro/dev-tools/access-instances) を参照してください。
- **GOLD** – 新しい展開の場合、構成およびデータ移行のために別の GOLD 環境を使用するのが一般的です。 この環境は、実装全体で他の環境を更新するために使用することができます。 基準コンフィギュレーションおよびデータ移行のある新しい運用環境を作成するために使用されます。 Go-live 準備プロセスを完了するまで、財務と運用のインフラストラクチャに運用環境を配置することはできません。 詳細については、「[Go-Live の準備](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live)」を参照してください。

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> 環境を考慮する場合は、次の方法をお勧めします。
>
> - 既定のスタンダード承認テスト (以前のサンドボックス) 環境または別の環境を使用して、Go-live 前にモック カットオーバーを行います。
> - Go-Live のカットオーバー時には、最終データを運用環境に移行するために必要な各データ パッケージを含む、詳細なカットオーバー チェックリストを作成します。 このレコメンデーションは、コンフィギュレーションを保存する別の GOLD 環境がある場合は特に重要です。
> - プロジェクト全体のテスト環境として、既定のスタンダード承認テスト (以前のサンドボックス) 環境または別の階層 2 以上の環境を使用します。 追加の環境が必要な場合、組織は追加費用で購入することができます。

## <a name="create-an-lcs-project"></a>LCS プロジェクトの作成

Human Resources 環境を管理するために LCS を使用するには、最初に LCS プロジェクトを作成する必要があります。 人事管理の環境を財務と運用のインフラストラクチャに移行する場合、財務と運用アプリ用の新しい LCS プロジェクトを作成する必要があります。 詳細については、[人事管理の環境を移行する](hr-admin-migrate-overview)を参照してください。 その他の財務と運用アプリ用の LCS プロジェクトが既にある場合、**機能管理** ワークスペースの人事管理機能を有効にすることができます。 詳細については [機能管理の概要](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

新しい顧客が人事管理にサインアップするとき、サブスクリプションには実装プロジェクト ワークスペースが含まれます。 顧客がサービスを有効にした後、テナント管理者はテナント アカウントを使用して <https://lcs.dynamics.com> にサインインする必要があります。 プロジェクト ワークスペースが組織に自動で作成されます。 詳細については、[財務と運用アプリの顧客向け Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs)を参照してください。

> [!NOTE]
> プロビジョニングを成功させるためには、人事管理の環境のプロビジョニングに使用するアカウントが、人事管理の環境に関連する Power Apps 環境の **システム管理者** ロールまたは **システム カスタマイザー** ロールのいずれかに割り当てられている必要があります。 Microsoft Power Platform でユーザーにセキュリティ ロールを割り当てる方法の詳細については、[リソースに対するユーザー セキュリティの構成](/power-platform/admin/database-security)を参照してください。

環境の配置を開始する前に、LCS プロジェクトの研修プロセスを完了する必要があります。 詳細については、[プロジェクトの研修](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding)を参照してください。 LCS の使用方法に関する詳細については、[Lifecycle Services (LCS) ユーザー ガイド](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide)を参照してください。

## <a name="deploy-human-resources-environments"></a>人事管理の環境を配置する

人事管理を含め、財務と運用アプリをクラウドに展開するためには、展開先の環境およびサブスクリプションについて、だれがどのタスクを実行することができるのか、また管理する必要があるデータおよびカスタマイズについて理解している必要があります。 新しい環境を配置する場合、名前付きユーザーの代わりにサービス アカウントを使用することをお勧めします。 財務と運用のインフラストラクチャに環境を展開する方法の詳細については、[クラウド展開の概要](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview)を参照してください。

財務と運用のインフラストラクチャに人事管理の運用環境を配置するには、Go-live 準備プロセスを完了する必要があります。 詳細については、「[Go-Live の準備](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live)」を参照してください。 このプロセスには、LCS のサブスクリプション見積もりツールが含まれます。 詳細については、[サブスクリプション見積もりツール](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator)を参照してください。

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Microsoft Power Platform と人事管理の統合

Microsoft Power Platform は、Power Platform 管理者センターを介した Dynamics 365 アプリケーションの一連の機能を提供します。 Microsoft Power Platform を使用して、人事管理データの使用を統合、拡張することができます。 人事管理と Microsoft Power Platform を統合する方法の詳細については、[Microsoft Power Platform と財務と運用アプリの統合](/fin-ops-core/dev-itpro/power-platform/overview)を参照してください。

## <a name="supported-geographies"></a>サポートされている地域

人事管理でサポートされている言語と地域の詳細については、[グローバル仕様: サポートされる国と言語について](https://dynamics.microsoft.com/availability-reports/)を参照してください。

## <a name="grant-access-to-the-environment"></a>環境へのアクセスを付与

既定では、環境を作成したグローバル管理者がそこにアクセスできます。 追加のアプリケーション ユーザーに対するアクセス権を明示的に付与する必要があります。 Human Resources 環境では、ユーザーを追加し、適切な役割を割り当てる必要があります。 詳細については、[新規ユーザーの作成](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) および [ユーザーのセキュリティ ロールへの割り当て](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) を参照してください。

## <a name="additional-resources"></a>追加リソース
財務と運用アプリのインフラストラクチャの LCS におけるプロジェクトの使用および管理に関する詳細については、次のリソースを参照してください。

- [Lifecycle Services のリソース](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS) ユーザー ガイド](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [セルフサービス配置の概要](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [データベース移動操作ホーム ページ](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
