---
title: Dataverse テーブル
description: Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。
author: twheeloc
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c8378418bdd0f4cb3f22b38a44e35179aad3ca33
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534236"
---
# <a name="dataverse-tables"></a>Dataverse テーブル


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。

> [!NOTE]
> Human Resources エンティティは Dataverse テーブルに対応します。 Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください

次の Dataverse テーブルは、Human Resources エンティティで利用できます。

## <a name="benefit-tables"></a>福利厚生テーブル

| 氏名 | テーブル |
| --- | --- |
| 給付金計算頻度 | cdm_benefitcalculationfrequency |
| 給付金計算頻度支払期間 | cdm_benefitcalculationfrequencypayperiod |
| 給付金計算レート | cdm_benefitcalculationrate |
| 給付金計算レートの詳細 | cdm_benefitcalculationratedetail |
| 福利厚生オプション | cdm_benefitoption |
| 給付金計画 | cdm_benefitplan (カスタム フィールド サポートに対して有効化されていない) |
| 給付金タイプ | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>ビジネス プロセス タスク テーブル

| 氏名 | テーブル |
| --- | --- |
| 業務プロセス カレンダー | cdm_businessprocesscalendar |
| 業務プロセス グループの割り当て | cdm_businessprocessgroupassignment |
| 業務プロセス ライブラリ タスク グループ | cdm_businessprocesslibrarytaskgroup |
| 業務プロセス ステージ | cdm_businessprocessstage |
| チェックリストのテンプレート ヘッダー | cdm_businessprocesstemplateheader |
| チェックリストのテンプレート タスク | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>報酬テーブル

| 氏名 | テーブル |
| --- | --- |
| 固定報酬プラン | cdm_compensationfixedplan |
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
| 固定報酬イベント | cdm_fixedcompensationevent |
| 給付ルール | cdm_vestingrule |
| 作業者の固定報酬 | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>組織テーブル

| 氏名 | テーブル |
| --- | --- |
| 部門 | cdm_department |
| 雇用 | cdm_employment |
| 法人 | cdm_company |
| ジョブ | cdm_job |
| 職務権限 | cdm_jobfunction |
| 職位 | cdm_jobposition |
| 職位タイプ | cdm_positiontype |
| 職位作業者割り当て | cdm_positionworkerassignmentmap |
| 職位分析コード | cdm_jobpositiondimension|
| 職務タイプ | cdm_jobtype |
| 言語 | cdm_language |
| タイトル | cdm_title |

> [!NOTE]
> **職位タイプ** に使用する財務分析コード 、**作業者の職位割り当て**、および **従業員** は、Dataverse にて一方向の統合機能が用意されています。 財務分析コードの更新は、現在のところ、 Dataverse から Human Resources へは同期されません。 

## <a name="leave-and-absence-tables"></a>休暇と欠勤テーブル

| 氏名 | テーブル |
| --- | --- |
| 休暇バンク トランザクション | cdm_leavebanktransaction |
| 休暇登録 | cdm_leaveenrollment |
| 休暇計画 | cdm_leaveplan |
| 休暇申請 | cdm_leaverequest |
| 休暇申請詳細情報 | cdm_leaverequestdetail |
| 休暇タイプ | cdm_leavetype |
| 休暇タイプの理由コード | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>給与テーブル

| 氏名 | テーブル |
| --- | --- |
| 支払サイクル | cdm_paycycle |
| 支払期間 | cdm_payperiod |
| 給与所得コード | cdm_payrollearningcode |
| 銀行口座支出 | cdm_bankaccountdisbursement |
| 税地域 | cdm_taxregion |

## <a name="worker-tables"></a>作業者テーブル

| 氏名 | テーブル |
| --- | --- |
| 作業者 | cdm_worker |
| 作業者住所 | cdm_workeraddress |
| 作業者の個人詳細 | cdm_workerpersonaldetail |
| ワーカーの個人識別番号 | cdm_workerpersonidentificationnumber |
| 作業者の ID タイプ | cdm_workerpersonidentificationtype |
| 作業カレンダー | cdm_workcalendar |
| 作業カレンダー日 | cdm_workcalendarday |
| 作業カレンダーの休日 |cdm_workcalendarholiday |
| 作業カレンダーの休日行 | cdm_workcalendarholidayline |
| 作業カレンダー時間間隔 | cdm_workcalendartimeinterval (カスタム フィールド サポートに対しては有効化されていない) |
| 作業者の銀行口座 | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>作業者の設定テーブル

| 氏名 | テーブル |
| --- | --- |
| 退役軍人状態 | cdm_veteranstatus |
| 出身民族 | cdm_ethnicorigin |
| 理由コード | cdm_reasoncode |
| 個人 ID の発行機関 | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>能力テーブル

| 氏名 | テーブル |
| --- | --- |
| スキルのタイプ | cdm_skilltype |

## <a name="table-relationship-models"></a>テーブル関係モデル

### <a name="worker"></a>ワーカー

![作業者。](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>職務および職位

![職務および職位。](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>給付金

![給付金。](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>報酬

![報酬。](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>休暇

![休暇。](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>作業カレンダー

![作業カレンダー。](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>参照

[データ統合テクノロジの選択](hr-admin-integration-choose-technology.md)<br>
[Dataverse 統合のコンフィギュレーション](hr-admin-integration-common-data-service.md)<br>
[構成 Dataverse 仮想テーブル](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resources 仮想テーブルに関するよく寄せられる質問](hr-admin-virtual-entity-faq.md)<br>
[Microsoft Dataverse とは](/powerapps/maker/data-platform/data-platform-intro)<br>
[用語の更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
