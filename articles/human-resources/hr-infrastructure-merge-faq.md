---
title: Dynamics 365 Human Resources インフラストラクチャ統合 FAQ
description: この記事では、Microsoft Dynamics 365 Human Resources および財務と運用アプリのインフラストラクチャの統合に関してよく寄せられる質問に回答します。
author: twheeloc
ms.date: 08/13/2021
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
ms.openlocfilehash: 8c005f677624336b4194bebea6d69667182128b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880483"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources インフラストラクチャ統合 FAQ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この記事では、Microsoft Dynamics 365 Human Resources および財務と運用アプリのインフラストラクチャの統合に関してよく寄せられる質問に回答します。

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources インフラストラクチャ統合とは ?

Dynamics 365 Human Resources は、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、および Dynamics 365 Project Operations などの他の財務と運用アプリとは異なるインフラストラクチャを使用するスタンドアロン アプリケーションです。 インフラストラクチャの統合により、Dynamics 365 Human Resources は他の財務と運用アプリと同じインフラストラクチャになります。

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>インフラストラクチャ統合の価値と利点

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>組織で Dynamics 365 Human Resources を使用して HR 操作を管理しています。 これらの変更からどのようなメリットがありますか ?

- これらの変更により、Dynamics 365 の Human Resources (HR) 機能の複数のセットが原因で発生する混乱が削除されます。
- これらは、Microsoft Power Platform の拡張性と、ビジネス ロジックおよび機能オプションを拡張する方法の両方を提供します。
- これらは、アプリケーション ライフサイクル管理 (ALM)、Microsoft Dynamics Lifecycle Services (LCS)、地理的な可用性、拡張性などの点で、Dynamics 365 Human Resources と財務と運用アプリの間に一貫性をもたらします。
- 共有サービスや工具を利用してコストを削減できます。

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>組織では、Dynamics 365 Finance、Supply Chain Management、Commerce、または Project Operations で Human Resources モジュールを使用します。 これらの変更からどのようなメリットがありますか ?

Dynamics 365 Human Resources で行われた機能と投資は、Dynamics 365 Finance で HR モジュールを使用している顧客が利用できるようになります。 これらの機能には、休暇および欠勤管理、福利厚生管理、タスク管理などの機能があります。

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>現在使用している機能が失われるか ?

Dynamics 365 Human Resources および財務と運用アプリの HR モジュールの間には機能的な同等性があります。 Dynamics 365 Human Resources は、同様の機能に優先されます。 詳細については [機能管理の概要](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

### <a name="will-the-experience-change-for-my-users"></a>ユーザーの経験は変わりますか ?

新しい HR 機能は、機能管理を通じて管理されます。 顧客がそれを取り入れるかどうかを決めることができます。 場合によっては、機能が変更される場合があります。 このような場合は、ドキュメントが提供されます。

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>既存の顧客であり、Finance and Operations インフラストラクチャの HR モジュールとカスタム統合による Dynamics 365 Human Resources の両方を使用している場合、この変更はどう影響しますか。

Dynamics 365 Human Resources と Dynamics 365 Finance の HR モジュール間のカスタム統合は不要になります。 すべての HR データは、他の財務と運用アプリと同じデータベースに保存されます。

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Dynamics 365 Human Resources から財務と運用アプリへの移行

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>組織では、Dynamics 365 Human Resources を使用して HR 操作を管理しています。 新しいエクスペリエンスに移行する場合、どのような計画を立てる必要がありますか ?

組織で Dynamics 365 Human Resources を使用しているが、他の財務と運用アプリを使用していない場合は、Human Resources 環境が新しいインフラストラクチャに移行されます。 この移行プロセスの多くが自動化されます。 データベースを移行し、それを新しいインフラストラクチャと同期させるプロセスが配置されます。

さらに、運用環境を移行する前に、移行プロセスをテストし、データとエクスペリエンスを検証できるツールが開始されます。

組織で Dynamics 365 Human Resources とその他の財務と運用アプリの両方を使用している場合は、データが新しい環境に正しく移行されることを確認するために、検証のためにより多くの時間を計画する必要があります。 新しいインフラストラクチャへの移行によって、Human Resources 環境のデータが Finance and Operations 環境に統合されます。 競合するデータでは、競合の解決方法を特定するためにユーザー入力が必要です。 ユーザーと管理者は、競合するデータ マッピングを管理し、運用環境を移行する前にサンドボックス環境で移行をテストする必要があります。

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>組織では、Dynamics 365 Finance、Supply Chain Management、Commerce、または Project Operations で Human Resources モジュールを使用します。 新しいエクスペリエンスに移行する場合、どのような計画を立てる必要がありますか ?

財務と運用アプリで HR モジュールを使用している組織の場合、Dynamics 365 Human Resources の新機能は、標準の 1 つのバージョン更新プロセスを通じて環境に適用されます。 各更新で使用可能になると、環境に新しい機能が表示される可能性があります。 機能管理を使用して新しい機能を有効にできますが、これらの機能を検証する必要があります。 環境に対する他の更新を検証するために、設定されているプロセスに従います。 財務と運用アプリに更新を適用する方法の詳細については、[1 つのバージョンの概要](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md) を参照してください。

### <a name="when-will-my-organization-be-migrated"></a>組織はいつ移行されますか ?

各組織の移行は、その現在の構成と、新しいインフラストラクチャに移行する準備が完了している場合に依存します。 これらの日付は変更される可能性があります。

- 財務と運用アプリで HR モジュールを使用している組織は、通常の 1 バージョン更新プロセスの一環として Dynamics 365 Human Resources の HR 機能を受け取ります。 新しい機能が 2022 年 1 月から一般に利用できる予定です。
- Dynamics 365 Human Resources のみを使用している組織は、移行ツールにアクセスできるため、2022 年半ばからテストを開始して移行を開始できます。 新しいインフラストラクチャへの移行を完了する必要がある日付はまだ決定されていません。 ただし、移行ツールが使用可能になる日付から少なくとも 1 年後になります。
- Dynamics 365 Human Resources とその他の財務と運用アプリの両方を使用している組織は、移行ツールにアクセスできるため、2022 年後半からテストを開始して移行を開始できます。 新しいインフラストラクチャへの移行を完了する必要がある日付はまだ決定されていません。 ただし、移行ツールが使用可能になる日付から少なくとも 1 年後になります。

Dynamics 365 Human Resources の新機能の詳細については、[Human Resources の新機能または変更点](./hr-admin-whats-new.md)を参照してください。

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>組織が Dynamics 365 Human Resources でまだ稼働していません。 財務と運用アプリの Human Resources モジュール、またはレガシ インフラストラクチャの Dynamics 365 Human Resources アプリを使用して稼働する必要がありますか。

考慮すべき重要な項目は、どの HR 機能が必要で、いつ新しいインフラストラクチャで使用できるかという点です。 組織が人員管理のコア機能を必要とする場合、この機能は現在、新しいインフラストラクチャの財務と運用アプリの HR モジュールで使用できます。 財務と運用アプリの HR モジュールと Dynamics 365 Human Resources アプリの間の機能パリティは、10.0.25 リリース版に含まれる予定で、2022 年 3 月には一般公開される予定です。 チーム アプリや Dataverse エンティティ統合のような統合機能は、後のリリース版で使用できます。

組織の HR 機能のニーズが、組織が稼働する時間枠内に新しいインフラストラクチャで使用できる場合は、財務と運用アプリの Human Resources モジュールで稼働する方が簡単な場合があります。 その結果、Dynamics 365 Human Resources アプリケーションへの標準のアプリケーション アップグレードが行われ、顧客は既に新しいインフラストラクチャに存在するので移行が容易になります。 組織が、レガシ インフラストラクチャの Dynamics 365 Human Resources アプリケーションで稼働することにした場合は、新しいインフラストラクチャに移行するために環境の移行が必要になります。 これは、新しいインフラストラクチャで稼働することにより回避できます。

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Dynamics 365 Human Resources (**休暇および欠勤**、**給付金管理** など) でのみ利用できる新機能を使用しています。 これらの機能を、Finance and Operations インフラストラクチャの Human Resources モジュールでも利用できるようになりますか。

はい、Dynamics 365 Human Resources のすべてのモジュールは財務と運用アプリでそのまま動作し、100% の機能パリティがあります。 現在、HR でこれらの機能を使用している顧客の全体的な移行戦略の一環として、顧客データが移行され、Finance and Operations インフラストラクチャで引き続き機能するようになります。

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>新しい Dynamics 365 Human Resources の福利厚生管理機能を使用しています。 福利厚生データを使用して給与機能を利用できるように、Finance and Operations インフラストラクチャの HR モジュールとのカスタム統合を構築しました。 これらのカスタム統合は今後必要になりますか ?

インフラストラクチャの統合の一環として、HR データは他の財務と運用アプリと同じデータベースに取り込まれます。 財務と運用アプリのモジュール間の統合は不要になります。

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>組織では、Dynamics 365 Human Resources で 1 つ以上の ISV ソリューションを使用しています。 ISV ソリューションは自動的に移行されますか ?

独立系ソフトウェア ベンダー (ISV) ソリューションの移行経験は、ソリューションの統合方法によって異なります。 Microsoft は、新しいインフラストラクチャへの円滑な移行を実現するために、ISV と密接な連携を行います。

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>組織では、LinkedIn Talent Hub と Dynamics 365 Human Resources の統合を使用しています。 インフラストラクチャの変更が完了した後も、この統合は引き続き機能しますか ?

いいえ、LinkedIn タレント ハブの統合は、新しいインフラストラクチャへの移行後は機能しません。 LinkedIn タレント ハブの統合サービスは、レガシ Dynamics 365 Human Resources インフラストラクチャと破棄されます。

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>組織では、Teams の Human Resources アプリを使用しています。 インフラストラクチャの変更が完了した後も、アプリは引き続き機能しますか ?

はい、Teams の Human Resources アプリは、新しいインフラストラクチャへの移行後も引き続き機能します。

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>組織では、Dynamics 365 Human Resources でカスタム セキュリティを構成しています。 インフラストラクチャの変更が完了した後も、カスタム セキュリティは引き続き適用されますか ?

はい、カスタム セキュリティ構成は新しいインフラストラクチャへのデータ移行に含まれます。

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>データの統合機能を使用して、Dynamics 365 Human Resources アプリと財務と運用アプリの間でデータを移動しています。 現在統合されているデータはどのように影響を受けますか ?

現在 Dynamics 365 Human Resources にある HR データは、Dataverse と同期されます。 その後、データ インテグレーターを使用して、財務と運用アプリとの一方向の同期を行うことができます。 新しいインフラストラクチャへの移行後、HR データは財務と運用アプリにネイティブになります。 データの統合機能は、財務と運用アプリと Human Resources の間でデータを同期する必要がなくなります。

Human Resources の現在の Dataverse ネイティブ データ テーブルは、新しいインフラストラクチャ上の環境からのデータを引き続き同期します。 エンティティは、二重書き込みをサポートするように変換されます。 他の Dynamics 365 アプリ用にこれらのテーブルに対してデータ統合を介して構成されたその他のデータ統合は、現在構成されているとおりに引き続き機能します。

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>二重書き込みを使用して、Dataverse と他の財務と運用アプリ間で HR データを移動しています。 現在統合中のデータが、新しいインフラストラクチャへの移行によってどのような影響を受けますか ?

HR データは、新しいインフラストラクチャ上の環境の財務と運用アプリにネイティブになります。 二重書き込みを使用して、HR データを新しい環境と Dataverse 環境の間で移動します。

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources から 1 つ以上の外部システムへのカスタム統合を構築しました。 インフラストラクチャの変更が完了した後、新しい統合を開発する必要がありますか ?

統合エンドポイントによって異なります。 財務と運用アプリで使用できる統合テクノロジの詳細、および最適な統合テクノロジを選択する方法については、[統合の概要](../fin-ops-core/dev-itpro/data-entities/integration-overview.md) を参照してください。

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Dynamics 365 Human Resources の Dataverse を拡張しました。 これらの拡張機能は自動的に移行されますか ?

新しいインフラストラクチャ上の環境に参加する Dynamics 365 Human Resources と Finance and Operations 環境が同じ Dataverse 環境に接続されている場合、2 つのアプリは移行後も同じ Dataverse 環境に接続されたままになります。 Dataverse 拡張機能に対する移行は必要ありません。

ただし、Dynamics 365 Human Resources および Finance and Operations 環境が現在別々の Dataverse 環境に接続されている場合は、2 つの Dataverse 環境を組み合わせて、新しいインフラストラクチャ上の単一の環境に接続する必要があります。 この Dataverse 移行では、Human Resources ソリューションの標準である Dataverse テーブルを、新しい Dataverse 環境に接続して再同期することができます。 Dataverse 環境に対する拡張機能は自動的に移行しませんが、新しい環境に再配置する必要があります。 Dataverse 拡張機能を管理するには、管理ソリューションを使用することをお勧めします。 詳細については、[ソリューションの概要](/powerapps/developer/data-platform/introduction-solutions)を参照してください。

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>Dynamics 365 Human Resources 内のカスタム フィールド機能は利用しました。カスタム フィールド イメージは自動的に移行しますか ?
はい、追加されたカスタム フィールドは新しいインフラストラクチャに移行します。

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources と連携するように Microsoft Power Automate フローや Microsoft Power Apps を構成しました。 これらの Microsoft Power Platform コンポーネントは移行され、インフラストラクチャの変更が完了した後に自動的に機能しますか ?

Power Apps、Power Automate フロー、およびその他の Microsoft Power Platform のカスタマイズは、 Dataverse 拡張機能に似ています。 新しいインフラストラクチャへの移行後に自動的に機能するかどうかは、移行前に Human Resources アプリと財務と運用アプリが同じ Power Apps 環境に接続されているかどうかによって異なります。

アプリが現在同じ Power Apps 環境に接続されている場合、新しいインフラストラクチャに移行した後も、アプリは引き続きその Power Apps 環境に接続されます。 この場合、Power Apps、Power Automate フロー、およびその他の Microsoft Power Platform のカスタマイズは、追加の構成なしで引き続き機能します。 管理ソリューションを使用して、Dataverse 上のアプリケーション拡張機能を管理することをお勧めします。 詳細については、[ソリューションの概要](/powerapps/developer/data-platform/introduction-solutions)を参照してください。

ただし、Human Resources アプリと財務と運用アプリが別々の Power Apps 環境に接続されている場合は、移行の一環としてそれらを組み合わせる必要があります。 このタスクでは、Power Apps およびその他のカスタマイズを新しい環境に再配置する必要があります。

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Dynamics 365 Human Resources の Dataverse 仮想テーブルを有効にしました。 移行中にこれらのテーブルはどうなりますか ?

移行後、新しいインフラストラクチャ上の環境が、現在 Dynamics 365 Human Resources に接続されている Dataverse 環境に接続されたままの場合、その環境で生成された Dataverse 仮想テーブルは、追加の構成なしで引き続き機能します。

ただし、移行後に新しいインフラストラクチャ上の環境が別の Dataverse 環境に接続されている場合は、新しい Dataverse 環境で仮想テーブルを再生成する必要があります。

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>申請者追跡システム (ATS) API、給与 API、Dynamics 365 Human Resources 用の Dataverse 仮想テーブル、または Dataverse Web API の他のエンティティを使用して統合を開発しました。 これらの統合は、インフラストラクチャの変更が完了した後も引き続き機能しますか ?

移行後、新しいインフラストラクチャ上の環境が、現在 Dynamics 365 Human Resources に接続されている Dataverse 環境に接続されたままの場合、Dataverse Web API に対して開発された統合は、移行が完了した後も引き続き機能します。

ただし、移行後に新しいインフラストラクチャ上の環境が別の Dataverse 環境に接続されている場合、Dataverse Web API に対して開発された統合は、新しい Dataverse 環境に接続するように再構成する必要があります。

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>環境を移行すると、Azure リージョンに影響はありますか ?

通常、移行中、HumanResources 環境は同じ Azure リージョンにとどまることが予想されます。 唯一の例外は、Human Resources 環境が別のリージョンにある Finance and Operations 環境と統合される場合です。 この場合、Human Resources 環境は、Finance and Operations 環境の Azure リージョンに移行されます。

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>組織は、1 つ以上のビジネス プロセスを Dynamics 365 Human Resources のワークフローに依存しています。 ワークフローは自動的に移行されますか ?

はい、ワークフロー構成、ワークフロー履歴、および現在の進行中のワークフローが移行されます。

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>移行プロセスを支援するために利用できるトレーニングとリソースは何ですか ?

移行プロセスの各ステップを詳細に説明する完全なドキュメントが提供されます。 必要に応じて、ビデオやワークショップなどの追加のトレーニング リソースも利用できる場合があります。

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>組織は、インターフェイスの使いやすさを向上させるために、Dynamics 365 Human Resources に保存済みビューを作成しました。 保存されたビューは自動的に移行されますか ?

はい、保存されたビューは新しいインフラストラクチャに移行されます。

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Dynamics 365 Human Resources で Ceridian を使用しています。 インフラストラクチャの変更が完了した後、Ceridian 統合は利用可能になりますか ? 

Ceridian との統合は、給与 API ベースの統合に移行されます。 Dynamics 365 Human Resources に現在存在するファイルベースの統合は、Finance and Operations インフラストラクチャに移行されません。 詳細については、[給与 API の概要](./hr-admin-integration-payroll-api-introduction.md)を参照してください。

### <a name="how-will-the-migration-affect-the-service-update-process"></a>移行はサービス更新プロセスにどのように影響しますか ?

移行後は、ALM とサービスの更新に関して顧客の柔軟性が向上します。 サービスの更新は、Human Resources 環境に自動的に適用されなくなります。 代わりに、サービスは 1 つのバージョンのサービスの更新プロセスと機能に従います。 したがって、更新の構成オプションは LCS を通じて利用できます。 詳細については、[1 つのバージョンの概要](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md)を参照してください。

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>移行は、Dynamics 365 Human Resources の LCS プロジェクトにどのように影響しますか ?

新しいインフラストラクチャへの移行により、Dynamics 365 Human Resources 環境の管理が LCS の Finance and Operations 実装プロジェクトに移行されます。 移行によって Dynamics 365 Human Resources が既存の Finance and Operations 環境に統合される場合、Human Resources LCS プロジェクトは財務と運用アプリの LCS 実装プロジェクトに統合されます。 現在 Dynamics 365 Human Resources のみを使用している場合は、新しい LCS 実装プロジェクトが作成され、既存の Human Resources LCS プロジェクトが新しいプロジェクトに移行されます。

新しいプロジェクトは、財務と運用アプリが使用するするのと同じタイプのプロジェクトになります。 環境管理と同じ機能を備えています。 詳細については、[Lifecycle Services のリソース](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)を参照してください。

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>タスクの記録を Human Resources のビジネス プロセス モデラーにリンクしました。 ビジネス プロセス モデラーはどのように移行され、LCS に統合されますか ?

LCS プロジェクトのビジネス プロセス ライブラリは、Human Resources の新しい LCS プロジェクトに移行されます。

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>組織は現在、Dynamics 365 Human Resources のみを使用しています。 インフラストラクチャの変更が完了した後、開発機能について詳しく知るために利用できるリソースは何ですか ?

Microsoft Power Platform の拡張性オプションと、Finance and Operations の拡張性オプションの両方が利用可能になり、開発に使用できます。 詳細については、 [開発およびカスタマイズのホーム ページ](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md) を参照してください。

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Dynamics 365 Human Resources の機能を有効にしました。 これらの機能は移行中に自動的に有効になりますか ?

新しいインフラストラクチャで機能が自動的に有効になるかどうかは、機能ごとに個別に決定されます。 この情報は、機能のドキュメントに含まれます。

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>移行中に BYOD データベースはどうなりますか ?

独自のデータベースを戻す (BYOD) のインポートおよびエクスポート構成は、新しいインフラストラクチャに移行されます。

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>移行中に Azure Data Lake はどうなりますか ?

財務と運用アプリで Azure Data Lake Storage 用に現在構成されているエクスポートは、移行後も同じ構成を維持します。

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>現在 Dynamics AX 2012 を使用しています。 現在利用可能なアップグレード ツールを使用して、AX 2012 の HR モジュールを Dynamics 365 Human Resources にアップグレードしますか ?

はい。 Dynamics 365 Human Resources は、財務と運用アプリの統合されたコードベースとインフラストラクチャに含まれます。 Dynamics  AX 2012 から Dynamics 365 Human Resources へのアップグレードでは、最新バージョンの財務と運用アプリへのアップグレードに使用されるものと同じアップグレード パスとツールが使用されます。

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Dynamics 365 Human Resources でドキュメント処理を使用します。 移行中にドキュメントはどうなりますか ?

ドキュメントは既存のドキュメント ストレージに残ります。 それらは、新しいインフラストラクチャの環境に再マップされます。

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>移行後、Dynamics 365 Human Resources で構成したバッチ処理はどうなりますか ?

該当するバッチ処理は、新しいインフラストラクチャに自動的に移行されます。

## <a name="licensing-impact"></a>ライセンスへの影響

このドキュメントは、使用権を対象とする法的ドキュメントに取って代わるものではありません。

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>組織で Dynamics 365 Human Resources を使用して HR 操作を管理しています。 ライセンスやコストは変わりますか ?

Dynamics 365 Human Resources ライセンスを購入した顧客は影響を受けません。 これらの顧客にライセンス移行はありません。 Human Resources に固有の追加のサンドボックス最小在庫管理単位 (SKU) は適用されなくなります。 この場合、顧客は少しだけ低い費用で財務と運用アプリ Tier 2 サンドボックスを購入することを選択できます。 Human Resources サンドボックスを購入した既存の顧客は、追加費用なしで財務と運用アプリ Tier 2 サンドボックスに移行されます。

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>組織では、Dynamics 365 Finance、Supply Chain Management、Commerce、または Project Operations で Human Resources モジュールを使用します。 ライセンスやコストは変わりますか ?

Dynamics 365 アプリの既存のユーザーとスタンド アロンの Dynamics 365 Finance、Supply Chain Management、Commerce、および Project Operations のユーザーは、2025 年 2 月まで、または現在のライセンス契約の期限が切れるまで、これらのライセンスの一部として Human Resources にアクセスできます。 コスト削減に役立つ場合は、早期に Human Resources ライセンスに移行することができます。 2025 年 2 月以降、既存の CSP および EA のすべての顧客は、HR モジュールをロール オフし、Human Resources ライセンスを購入して、財務と運用アプリに導入される新機能を利用する必要があります。

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>組織は、Dynamics 365 Finance、Supply Chain Management、Commerce、または Project Operations を使用しています。 インフラストラクチャの統合をサポートするために、追加の環境を購入する必要がありますか ?

インフラストラクチャの変更をサポートするために、追加の環境は必要ありません。

