---
title: Dynamics 365 Talent (2019 年 12 月 3 日) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528696"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Dynamics 365 Talent (2019 年 12 月 3 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2646 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="feature-management-workspace"></a>機能管理ワークスペース

**機能管理** ワークスペースでは、各リリースで可能になる機能の一覧を表示できます。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。 機能管理の詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

すべての新機能は少なくとも 30 日間、通常は 30-60 日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 **機能管理** ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。
 
場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (**機能管理** ワークスペースなど)。
 
機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 **機能管理** ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>バッチ ジョブ履歴のクリーンアップの自動スケジューリングを追加 (332528)

この変更により、**バッチ ジョブ履歴** が毎晩実行され、30 日以上前のバッチ ジョブ履歴項目が削除されます。

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>作業者のアクションで、ID 番号の長さが ID のタイプと一致しない場合、Talent が応答しない (390971)

このリリースにより、ID 番号の長さが ID タイプ内の定義と一致しない場合に発生する問題が修正されます。 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>固定報酬は、職位の詳細に対する変更のあるレベルを更新しない (348085)

今週のリリースでは、従業員に対して新しい固定報酬レコードを作成する時点での職位に関連付けられているジョブは、**報酬開始日** によって決定されます。

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>作業者または契約社員のみである場合、作業者、従業員、および契約社員のリストが、両方の作業者タイプを表示する (384473)

この変更は、入力された作業者のタイプ (契約社員または従業員) を正確に反映します。

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>セキュリティ ポリシーにより、新規採用アクションの電子メール通知に名前情報が含まれない (383402)

この変更により、高度なセキュリティが有効になっている場合、ワークフローのプレースホルダー内の名または姓フィールドに表示される情報が修正されます。

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>システムが、同じ日に対して全日の休暇要求を 2 回許可する (379284)

この変更により、同じ日に 2 つの休暇要求を発行することはできなくなりました。 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>住所の変更一覧を有効日順に並べ替える必要がある (352798)

この変更により、住所の変更一覧が **有効日** 順に並べ替えられました。

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>休暇要求について、Common Data Service から Talent への削除を許可する必要がある (376999)

この変更により、ドラフトおよびキャンセルされた休暇要求を Common Data Service から削除し、その後 Talentから削除できるようになりました。

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>同じ所得コードが従業員に割り当てられている場合、所得コードの削除が許可される (371792)

このリリースでは、システムから所得コードを削除する前、最初に従業員から所得コードを削除する必要があります。

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>2 つの承認ステージのある休暇と欠勤のワークフローの完了に失敗する (391116)

この変更により、要求に対して 1 つ以上の承認ステージがコンフィギュレーションされている場合、休暇および欠勤ワークフローはすべてのステップを継続します。

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Talent で更新または入力された場合、発行日が Common Data Service に同期されない (397361)。

この変更により、**個人 ID** レコードの発行日が Talent から Common Data Service に同期されない場合の問題が修正されます。

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>職位にマネージャーを割り当てた時に発生する階層の循環参照エラー (386659)

この変更により、職位に新しいマネージャを割り当てる時に循環参照エラーが発生する固有のシナリオが修正されます。

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>カスタム フィールドをサポートするようになった Common Data Service エンティティ

次の Common Data Service エンティティが、カスタム フィールドをサポートするようになりました。

| 氏名 | エンティティ |
| --- | --- |
| 銀行口座出金 | cdm_bankaccountdisbursement |
| 給付金計算頻度 | cdm_benefitcalculationfrequency |
| 給付金計算頻度支払期間 | cdm_benefitcalculationfrequencypayperiod |
| 給付金計算レート | cdm_benefitcalculationrate |
| 給付金計算レートの詳細 | cdm_benefitcalculationratedetail |
| 福利厚生オプション | cdm_benefitoption |
| 給付金計画 | cdm_benefitplan (カスタム フィールド サポートに対して有効化されていない) |
| 給付金タイプ | cdm_benefittype |
| 業務プロセス カレンダー | cdm_businessprocesscalendar |
| 業務プロセス グループの割り当て | cdm_businessprocessgroupassignment |
| 業務プロセス ライブラリ タスク グループ | cdm_businessprocesslibrarytaskgroup |
| 業務プロセス ステージ | cdm_businessprocessstage |
| チェックリストのテンプレート ヘッダー | cdm_businessprocesstemplateheader |
| チェックリストのテンプレート タスク | cdm_businessprocesstemplatetask |
| 法人 | cdm_company |
| 報酬固定プラン | cdm_compensationfixedplan |
| 報酬グリッド | cdm_compensationgrid |
| 報酬レベル | cdm_compensationlevel |
| 報酬支払頻度 | cdm_compensationpayfrequency |
| 報酬基準点設定 | cdm_compensationreferencepointsetup |
| 報酬基準点設定ライン | cdm_compensationreferencepointsetupline |
| 報酬地域 | cdm_compensationregion |
| 報酬構造 | cdm_compensationstructure |
| 報酬変動プラン | cdm_compensationvariableplan |
| 報酬変動プラン レベル | cdm_compensationvariableplanlevel |
| 報酬変動プラン タイプ | cdm_compensationvariableplantype |
| 部門 | cdm_department |
| 雇用 | cdm_employment |
| 出身民族 | cdm_ethnicorigin |
| 固定報酬イベント | cdm_fixedcompensationevent |
| ジョブ | cdm_job |
| 職務権限 | cdm_jobfunction |
| 職位 | cdm_jobposition |
| 職務タイプ | cdm_jobtype |
| 言語 | cdm_language |
| 休暇バンク トランザクション | cdm_leavebanktransaction |
| 休暇登録 | cdm_leaveenrollment |
| 休暇計画 | cdm_leaveplan |
| 休暇申請 | cdm_leaverequest |
| 休暇申請詳細情報 | cdm_leaverequestdetail |
| 休暇タイプ | cdm_leavetype |
| 休暇タイプの理由コード | cdm_leavetypereasoncode |
| 支払サイクル | cdm_paycycle |
| 支払期間 | cdm_payperiod |
| 給与所得コード | cdm_payrollearningcode |
| 個人 ID の発行機関 | cdm_personidentificationissuingagency |
| 職位タイプ | cdm_positiontype |
| 職位作業者割り当て | cdm_positionworkerassignmentmap |
| 理由コード | cdm_reasoncode |
| スキルのタイプ | cdm_skilltype |
| 税地域 | cdm_taxregion |
| 給付ルール | cdm_vestingrule |
| 退役軍人状態 | cdm_veteranstatus |
| 作業カレンダー | cdm_workcalendar |
| 作業カレンダー日 | cdm_workcalendarday |
| 作業カレンダーの休日 |cdm_workcalendarholiday |
| 作業カレンダーの休日行 | cdm_workcalendarholidayline |
| 作業カレンダー時間間隔 | cdm_workcalendartimeinterval (カスタム フィールド サポートに対しては有効化されていない) |
| ワーカー | cdm_worker |
| 作業者の住所 | cdm_workeraddress |
| 作業者の銀行口座 | cdm_workerbankaccount |
| 作業者の固定報酬 | cdm_workerfixedcompensation |
| 作業者の個人詳細 | cdm_workerpersonaldetail |
| 作業者の ID 番号 | cdm_workerpersonidentificationnumber |
| 作業者の ID タイプ | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>プレビュー

プレビュー機能は **サンドボックス** 環境でのみ有効になります。

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。
