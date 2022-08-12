---
title: Human Resources の顧客の移行に関するよく寄せられる質問
description: この記事では、Microsoft Dynamics 365 Human Resources のインフラストラクチャを統合した財務と運用アプリへの移行に関してよく寄せられる質問に回答します。
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151083"
---
# <a name="human-resources-customer-migration"></a>Human Resources の顧客の移行

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Dynamics 365 Human Resources の顧客は財務と運用インフラストラクチャに移行する計画を立てるにはどうしたらよいでしょうか?

影響を受けるのは Microsoft Dynamics 365 Human Resources の顧客の 2 つのカテゴリであり、最新の財務と運用インフラストラクチャであることを確認するために変更を加える必要があります。

- Dynamics 365 Human Resources を使用し、Dynamics 365 からの他の操作アプリを使用しない顧客
- Dynamics 365 Human Resources および Dynamics 365 Finance の両方、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、または Dynamics 365 Project Operations を使用する顧客

顧客は、所属するカテゴリに関係なく、財務と運用インフラストラクチャの新しく作成された環境にデータを移動し、マージが正常に完了した検証を行う必要があります。

今後は、Dynamics 365 Human Resources アプリには他の運用アプリとは別の独自の財務と運用環境が用意されます。 このようにして、顧客は現在のデータを結合することなく、機能拡張オプションを活用できます。 Microsoft は、運用環境に移行する前に、顧客がデータ移行のテストおよび検証に使用できるツールとサンドボックス環境を提供します。 このツールによって自動化に近いプロセスが有効され、2022 年 8 月から 11 月の間に使用できます。

財務と運用インフラストラクチャで他のアプリを使用している顧客は、人事管理データを既存の環境とマージすることができます。 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>顧客は財務と運用インフラストラクチャにいつ移行しますか?

各会社の移行は、会社の現在の構成と、財務と運用インフラストラクチャに移行する準備が完了している場合に依存します。 顧客が Microsoft パートナーと協力して、今後の最適な方法を決定するようお勧めします。

- Dynamics 365 Finance の **人事管理** モジュールを使用する組織は、通常の 1 バージョン更新プロセスの一部として、Dynamics 365 Human Resources からの新しい機能を有効にできます。 新しい機能が 2022 年 1 月から一般に利用できる予定です。
- Dynamics 365 Human Resources を使用する組織は、インフラストラクチャ統合の完了に使用できるツールへのアクセス権を持っています。 Microsoft は、移行中に顧客と協力し、サービスが中断されるのを防ぐのに役立ちます。 移行ツールが使用可能になった時刻から移行を行う顧客の場合、移行期間が 12 ~ 18 か月になります。
- Dynamics 365 Human Resources と **人事管理** モジュールの両方を使用する組織は、スタンドアロンの人事管理インフラストラクチャを財務と運用インフラストラクチャに移動できます。 また、統合ツールを使用して環境を単一の環境にすることもできます。 2 つの環境をマージするための要件や時間枠はありません。

最新情報については、[リリース計画](/dynamics365/release-plans/) を定期的にチェックしてください。

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>顧客は引き続き、Dynamics 365 Human Resources と人事管理モジュール間のカスタム統合を必要としますか?

- Dynamics 365 Human Resources と現在統合されている他の財務と運用インフラストラクチャ環境の両方を持つ顧客は、マージ後も引き続き 2 つの環境を統合する必要があります。
- 既存の財務と運用アプリ環境とは別の Dynamics 365 Human Resources 環境を選択した顧客は、環境の統合を継続して行い、両方の環境でデータを利用できる状態にする必要があります。
- 顧客は引き続きデータ インテグレーターを使用して 2 つの環境間のデータをコピーできます。 移行後にデータを単一の環境にマージする顧客は、すべてのデータが 1 つのデータベースに含まれるため、データの統合が不要になります。

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>顧客の ISV ソリューションは自動的に移行されますか?

独立系ソフトウェア ベンダー (ISV) ソリューションの移行経験は、ソリューションの統合方法によって異なります。 Microsoft は、財務と運用インフラストラクチャへの円滑な移行を提供するために、ISV と密接な連携を行います。 多くの ISV ソリューションは、Microsoft Power Platform の機能を使用して Dataverse で構築されます。 これらのソリューションは、Dynamics 365 Human Resources 環境と Dataverse 環境間の Dataverse の統合によって異なります。 この Dataverse統合は、インフラストラクチャ統合の一部として廃止予定です。 財務と運用インフラストラクチャでは、Dataverse 統合の機能を置き換えるために、新しい二重書き込みマップが計画 されています。

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Dynamics 365 Human Resources と他の Dynamics 365 アプリ間でデータを移動するデータ インテグレーターにはどのような影響を与えますか?

顧客は財務と運用インフラストラクチャに移行した後、2 つの環境間のデータの統合を継続する必要があります。 顧客は引き続きデータ インテグレーターを使用して、これらのデータ移行タスクを実行できます。 既存の財務と運用アプリ環境とは別の Dynamics 365 Human Resources 環境を選択した顧客は、両方の環境間でのデータの統合を継続して行う必要があります。 顧客が 2 つの環境を単一の環境にマージする場合、2 つの環境間の統合は不要になります。

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>移行後、財務と運用インフラストラクチャの Dynamics 365 Human Resources と Dataverse 間のデータの移行はどうなりますか?

Dynamics 365 Human Resources および Dataverse 間の現行の Dataverse 統合は、財務と運用インフラストラクチャの一部として非推奨となる予定です。 財務と運用エンティティを Dataverse テーブルにマップする二重書き込みマップを導入する計画があります。 実装に必要な二重書き込みマップを顧客が決定する必要があります。 ビジネス ロジックを実行するために Dataverse でデータを複製する業務上の特定のニーズがある場合に限り、仮想テーブルを統合および ISV ソリューションに使用することをお勧めします。

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>移行は、Dynamics 365 Human Resources の Dataverse 拡張機能にどのように影響しますか?

顧客は運用環境を移行する前に、サンドボックス環境に移行することが必要になります。 顧客がサンドボックス環境の移行を行う場合は、Dataverse 環境のコピーを作成して新しい財務と運用の移行された環境に接続する必要があります。 顧客の運用環境と一致するように環境のデータと環境に対応するソリューションの両方を顧客がコピーすることをお勧めします。

顧客が Dynamics 365 Human Resources 運用環境を移行する準備が整った場合、Microsoft はデータベースと Azure Blob Storage を自動的に移行します。 移行されたデータベースとストレージによって、財務と運用インフラストラクチャの新しい環境が同じ Dataverse 運用環境にポイントされます。 データの Dataverse へのコピーを続行するには、Dataverse に構築された統合、拡張機能、および ISV ソリューションに必要な二重書き込みマップを顧客が有効にする必要があります。

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Dynamics 365 Human Resources のために構築された Microsoft Power Platform コンポーネントは、インフラストラクチャの移行が完了した後に自動的に機能しますか?

Power Apps で作成されたアプリ、Power Automate で作成されたフロー、および他の Microsoft Power Platform のカスタマイズは Dataverse 拡張機能です。 顧客の運用環境の移行中は、拡張機能も含めて Dataverse 環境に影響はありません。 アプリ、フロー、および Power Microsoft Platform に関するその他のカスタマイズは、コンフィギュレーションを追加することなく、引き続き機能する必要があります。

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>移行中に Dynamics 365 Human Resources の Dataverse 仮想テーブル エンティティはどうなりますか?

顧客が Dynamics 365 Human Resources 環境を財務と運用インフラストラクチャに移行する場合、環境は Dynamics 365 Human Resources に現在接続されている Dataverse 環境に接続されたままです。 環境で生成された Dataverse 仮想テーブルは、コンフィギュレーションを追加する必要なく、引き続き動作します。 顧客の既存の財務と運用環境に接続されている Dataverse 環境で仮想テーブルを再生成する必要がある場合があります。

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>インフラストラクチャ統合の完了後に、申請者追跡システム (ATS) API、給与 API、Dynamics 365 Human Resources の Dataverse 仮想テーブル、または Dataverse Web API のその他のエンティティを使用する統合はどのように機能しますか?

顧客が Dynamics 365 Human Resources 環境を財務と運用インフラストラクチャに移行する場合、環境は Dynamics 365 Human Resources に現在接続されている Dataverse 環境に接続されたままです。 Dataverse Web API に対して開発された統合は、移行の完了後も引き続き機能します。

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>組織では、Dynamics 365 Human Resources でカスタム セキュリティを構成しています。 インフラストラクチャの移行が完了した後も、引き続き適用されますか?

はい、カスタム セキュリティ構成はデータ移行に含まれます。

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Dynamics 365 Human Resources のワークフローは自動的に移行されますか?

はい、ワークフロー構成、ワークフロー履歴、および現在の進行中のワークフローがマージされたインフラストラクチャに移行されます。

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Dynamics 365 Human Resources に保存されたビューは自動的に移行されますか?

はい、保存されたビューはマージされたインフラストラクチャに移行されます。

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Dynamics 365 Human Resources で有効になる機能は、インフラストラクチャ統合後に自動的に利用できるでしょうか?

- **人事管理** モジュールを使用する顧客のために、Dynamics 365 Human Resources でのみ使用できる機能は機能管理によって管理されます。 通常、これらの機能は既定で有効にされません。 既定で有効にする必要がある機能は文書化されます。
- Dynamics 365 Human Resources を使用する顧客のために、この機能はインフラストラクチャで使用できます。 使用できない機能が文書化されます。 現在の Dynamics 365 Human Resources 環境で有効になっているすべての機能管理キーは、マージされたインフラストラクチャで有効になります。 詳細については [機能管理の概要](/fin-ops/get-started/feature-management-overview.md) を参照してください。

## <a name="what-happens-to-byod-databases-during-the-migration"></a>移行中に BYOD データベースはどうなりますか?

独自のデータベースを戻す (BYOD) のインポートおよびエクスポート構成は、財務と運用インフラストラクチャに移行されます。

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>顧客の環境を移行すると、Azure リージョンに影響はありますか?

Dynamics 365 Human Resources 環境は、移行のために同じ Azure リージョンに残ります。 環境を別の Azure リージョンに移動する必要がある場合、顧客は標準の手順に従って、移行の完了後に新しいリージョンに移行する必要があります。

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>移行中に Azure Data Lake はどうなりますか?

財務と運用アプリで Azure Data Lake 用に現在構成されているエクスポートは、移行後も同じ構成を維持します。

> [!NOTE]
> 人事管理環境から Dataverse へのデータの書き込みを続行するには、二重書き込みマップを有効にする必要があります。

人事管理データを Data Lake にエクスポートする顧客は、財務と運用インフラストラクチャへの移行の後でこの機能を有効にできます。 詳細については、[Data Lake - Azure アーキテクチャ センター](/azure/architecture/data-guide/scenarios/data-lake) を参照してください。

顧客は、複数の財務と運用環境を同じ Data Lake にリンクできます。 ただし、各環境は異なるフォルダーとコンテナーをポイントします。 後から環境をマージする予定の顧客は、アプローチを慎重に計画する必要があります。
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>顧客が現在人事管理モジュールを使用している場合、どのような移行が必要になりますか?

**人事管理** モジュールを使用している顧客には、1 つの標準バージョン更新プロセスを通して Dynamics 365 Human Resources から環境に適用される新機能があります。 各更新で使用可能になると、環境に新しい機能が表示される可能性があります。 顧客が機能管理を使用して機能を有効にできます。 顧客は、既に設定されているプロセスを使用してこれらの新しい機能を検証し、環境に対する他の更新を検証するために使用する必要があります。

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>外部システムへのカスタム統合はどうなりますか?

顧客は統合を財務と運用環境に移行する必要があります。 この環境のエンドポイントは異なっているから、顧客が新しい環境をポイントするために統合を更新または変更する必要がある場合があります。 このタスクは主に手動のプロセスで行い、必要な変更は統合のアーキテクチャによって異なっています。 顧客は、統合を移動するための最善の方法を決定するために、Microsoft パートナーと連携する必要があります。

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>顧客が Dynamics 365 Human Resources 環境を既存の財務と運用環境にマージした場合、Microsoft Power Platform (Dataverse) はどうなりますか?

移行後に顧客が Dynamics 365 Human Resources 環境と既存の財務と運用環境を単一の Dataverse インスタンスにマージする場合、Dataverse 環境をマージ プロセスの一部として統合する必要があります。 このタスクでは、Power Apps や他のカスタマイズを使用して作成されたアプリを新しい環境に再配置する必要があります。

## <a name="what-will-happen-to-documents-during-the-migration"></a>移行中にドキュメントはどうなりますか?

顧客が Dynamics 365 Human Resources 環境を財務と運用インフラストラクチャに移行すると、ドキュメントは既存のドキュメント ストレージに残り、財務と運用インフラストラクチャの新しい環境に自動的にマップされます。

将来のリリースでは、新しいデータ エンティティが提供される予定です。 この変更が行われた後、Dynamics 365 Human Resources 環境を既存の財務と運用環境にマージする選択をした顧客は、ドキュメントをエクスポートして既存の環境に移動できます。

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>移行後、Dynamics 365 Human Resources で構成したバッチ ジョブはどうなりますか?

バッチ ジョブは、財務と運用環境で再構成される必要があります。 顧客は各バッチ ジョブを評価し、財務と運用環境の現在のバッチ ジョブの一覧と比較する必要があります。 顧客は、2 つのバッチ ジョブ セットをマージするときにバッチ スケジュール全体を分析して、バッチ スケジュール、優先順位、またはバッチ グループの変更を行う必要があるかどうかを決定する必要があります。

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>移行は、Dynamics 365 Human Resources の LCS プロジェクトにどのように影響しますか?

顧客は、新しい Microsoft Dynamics Lifecycle Service (LCS) プロジェクトを作成する必要があり、また、財務と運用アプリをプロジェクトタイプとして、製品および **実装** として選択する必要があります。 また、LCS プロジェクトを作成する場合は、サブプロジェクト タイプの新しいフィールドを使用することもできます。 顧客は、既存の人事管理 LCS プロジェクトを財務と運用インフラストラクチャに移行するために、Dynamics 365 Human Resources 移行のオプションを選択する必要があります。

財務と運用 LCS プロジェクトの機能は、人事管理 LCS プロジェクトの機能と異なります。

稼働開始するには、新規顧客は次のタスクを完了する必要があります。

- プロジェクトのオンボード処理を完了します。
- 方法を完了します。
- サブスクリプション見積もりツールに記入します。
- Go-live 準備評価を完了します。

## <a name="how-will-the-business-process-modeler-be-migrated"></a>ビジネス プロセス モデラーはどのように移行されますか?

顧客は、人事管理 LCS プロジェクトからビジネス プロセス モデラー ライブラリをエクスポートし、財務と運用 LCS プロジェクトにインポートする必要があります。 また、顧客が新しい LCS プロジェクトをポイントするために、アプリケーションのヘルプ設定を更新する必要があります。

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>移行はサービス更新プロセスにどのように影響しますか?

移行後は、アプリケーション ライフサイクル管理 (ALM) とサービス更新に関して顧客の柔軟性が向上します。 サービス更新は、人事管理環境に自動的に適用されなくなります。 代わりに、このサービスは 1 つのバージョン サービスの更新プロセスと機能に従い、LCS による更新のコンフィギュレーション オプションが有効になります。

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>顧客はインフラストラクチャの統合に関してFastTrackの支援を受ける資格を得ることができますか?

Microsoft では、マージに役立つ FastTrack から利用できるツールとリソースをまだ定義しています。

## <a name="licensing-impact"></a>ライセンスへの影響

ライセンスが受ける影響の詳細については、[Dynamics 365 Human Resources インフラストラクチャ マージに関するよくある質問](hr-infrastructure-merge-faq.md#licensing-impact) を参照してください。
