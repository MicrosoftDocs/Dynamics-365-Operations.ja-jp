---
title: Common Data Service エンティティ
description: Microsoft Dynamics 365 Human Resources は、Common Data Service を使用して拡張性シナリオおよび統合シナリオを有効にします。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530009"
---
# <a name="common-data-service-entities"></a>Common Data Service エンティティ

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources は、Common Data Service を使用して拡張性シナリオおよび統合シナリオを有効にします。

Common Data Service の詳細については、[Common Data Service とは何か](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)を参照してください。

次の人事管理エンティティは、Common Data Service で使用できます。

## <a name="benefit-entities"></a>Benefit エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 給付金計算頻度 | cdm_benefitcalculationfrequency |
| 給付金計算頻度支払期間 | cdm_benefitcalculationfrequencypayperiod |
| 給付金計算レート | cdm_benefitcalculationrate |
| 給付金計算レートの詳細 | cdm_benefitcalculationratedetail |
| 福利厚生オプション | cdm_benefitoption |
| 給付金計画 | cdm_benefitplan (ユーザー定義サポートは有効になっていません) |
| 給付金タイプ | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>ビジネス プロセス タスク エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 業務プロセス カレンダー | cdm_businessprocesscalendar |
| 業務プロセス グループの割り当て | cdm_businessprocessgroupassignment |
| 業務プロセス ライブラリ タスク グループ | cdm_businessprocesslibrarytaskgroup |
| 業務プロセス ステージ | cdm_businessprocessstage |
| チェックリストのテンプレート ヘッダー | cdm_businessprocesstemplateheader |
| チェックリストのテンプレート タスク | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>報酬エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 報酬固定計画 | cdm_compensationfixedplan |
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
| ワーカー固定報酬 | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>組織エンティティ

| 氏名 | エンティティ |
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
> **職位タイプ** に使用する財務分析コード 、**作業者の職位割り当て**、および **従業員** は、Common Data Service にて一方向の統合機能が用意されています。 財務分析コードの更新は、現在のところ、 Common Data Service から Human Resources へは同期されません。 

## <a name="leave-and-absence-entities"></a>休暇エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 休暇バンク トランザクション | cdm_leavebanktransaction |
| 加入契約から移動 | cdm_leaveenrollment |
| 休暇計画 | cdm_leaveplan |
| 休暇申請 | cdm_leaverequest |
| 休暇申請詳細情報 | cdm_leaverequestdetail |
| 休暇タイプ | cdm_leavetype |
| 休暇タイプの理由コード | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>給与エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 支払サイクル | cdm_paycycle |
| 支払期間 | cdm_payperiod |
| 給与所得コード | cdm_payrollearningcode |
| 銀行口座支出 | cdm_bankaccountdisbursement |
| 税地域 | cdm_taxregion |

## <a name="worker-entities"></a>作業者エンティティ

| 氏名 | エンティティ |
| --- | --- |
| ワーカー | cdm_worker |
| ワーカーの住所 | cdm_workeraddress |
| ワーカーの個人情報詳細 | cdm_workerpersonaldetail |
| ワーカーの個人識別番号 | cdm_workerpersonidentificationnumber |
| 作業者の ID タイプ | cdm_workerpersonidentificationtype |
| 作業カレンダー | cdm_workcalendar |
| 作業カレンダー日 | cdm_workcalendarday |
| 作業カレンダーの休日 |cdm_workcalendarholiday |
| 作業カレンダーの休日行 | cdm_workcalendarholidayline |
| 作業カレンダー時間間隔 | cdm_workcalendartimeinterval (個人定義フィールドサポートは有効になっていません) |
| ワーカーの銀行口座 | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>ワーカーの設定エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 退役軍人状態 | cdm_veteranstatus |
| 出身民族 | cdm_ethnicorigin |
| 理由コード | cdm_reasoncode |
| 個人識別発行代理店 | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>コンピテンシー エンティティ

| 氏名 | エンティティ |
| --- | --- |
| スキルの種類 | cdm_skilltype |

## <a name="entity-relationship-models"></a>エンティティ関係モデル

### <a name="worker"></a>ワーカー

![ワーカー](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>職務および職位

![職務および職位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>福利厚生

![福利厚生](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>報酬

![報酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>離脱

![離脱](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>作業カレンダー

![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>参照

[データ統合テクノロジの選択](hr-admin-integration-choose-technology.md)</br>
[Common Data Service 統合のコンフィギュレーション](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]