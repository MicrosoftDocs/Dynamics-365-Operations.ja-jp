---
title: Common Data Service の Core HR エンティティ
description: Core HR は、Common Data Service を使用して、拡張性シナリオおよび統合シナリオを有効にします。
author: andreabichsel
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-08-11
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6adbd3966fc3aedd0eab83cd8c4714860d6a0e7e
ms.sourcegitcommit: e895b3bbe309f4043d9aaa2a257f0c6e5698923b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899449"
---
# <a name="core-hr-entities-in-common-data-service"></a>Common Data Service の Core HR エンティティ

Core HR は、Common Data Service を使用して、拡張性シナリオおよび統合シナリオを有効にします。

Common Data Service の詳細については、[Common Data Service とは何か](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)を参照してください。

> [!IMPORTANT]
> Common Data Service の以前のリリース (1.0) は、使用できなくなります。 2019 年 4 月 15 日、Core HR および Common Data Service (1.0) 間の統合がオフになります。 アップグレードの詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)を参照してください。

次の Core HR エンティティは、Common Data Service で使用できます。

## <a name="benefit-entities"></a>Benefit エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 給付金計算頻度 | cdm_benefitcalculationfrequency |
| ベネフィット計算頻度支払期間 | cdm_benefitcalculationfrequencypayperiod |
| ベネフィット計算レート | cdm_benefitcalculationrate |
| ベネフィット計算レートの詳細 | cdm_benefitcalculationratedetail |
| ベネフィット オプション | cdm_benefitoption |
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
| 報酬構成 | cdm_compensationstructure |
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
| ワーカー割り当ての配置 | cdm_positionworkerassignmentmap |
| 職務タイプ | cdm_jobtype |
| 言語 | cdm_language |

## <a name="leave-and-absence-entities"></a>休暇エンティティ

| 氏名 | エンティティ |
| --- | --- |
| 空欄のトランザクションから移動 | cdm_leavebanktransaction |
| 加入契約から移動 | cdm_leaveenrollment |
| 休暇計画 | cdm_leaveplan |
| 休暇申請 | cdm_leaverequest |
| 要求の詳細から移動 | cdm_leaverequestdetail |
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
| 作業カレンダーの休日ライン | cdm_workcalendarholidayline |
| 作業カレンダーの時間間隔 | cdm_workcalendartimeinterval (個人定義フィールドサポートは有効になっていません) |
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

### <a name="leave"></a>休暇
![休暇](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>作業カレンダー
![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)
