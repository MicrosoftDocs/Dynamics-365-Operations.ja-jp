---
title: Dataverse テーブル
description: Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838585"
---
# <a name="dataverse-tables"></a>Dataverse テーブル


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。

> [!NOTE]
> Human Resources エンティティは Dataverse テーブルに対応します。 Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください

次の Dataverse テーブルは、Human Resources エンティティで利用できます。

現在の既知の問題に関する詳細情報については、[Lifecycle Services (LCS) の既知の問題](/dev-itpro/lifecycle-services/issue-search-lcs) をご覧ください。

## <a name="benefit-tables"></a>福利厚生テーブル

| Name | テーブル | 既知の問題  | Status |
| --- | --- |    --------|----------  |
| 給付金計算頻度 | cdm_benefitcalculationfrequency |     |     |
| 給付金計算頻度支払期間 | cdm_benefitcalculationfrequencypayperiod |     |     |
| 給付金計算レート | cdm_benefitcalculationrate |    |     |
| 給付金計算レートの詳細 | cdm_benefitcalculationratedetail |753225 | 解決済  |
| 福利厚生オプション | cdm_benefitoption |    |     |
| 給付金計画 | cdm_benefitplan (カスタム フィールド サポートに対して有効化されていない) |    |     |
| 給付金タイプ | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>ビジネス プロセス タスク テーブル

| Name | テーブル |既知の問題  | Status |
| --- | --- |   --------|----------   |
| 業務プロセス カレンダー | cdm_businessprocesscalendar | 751867 | 解決済 |
| 業務プロセス グループの割り当て | cdm_businessprocessgroupassignment | 751869  751863 | 有効|
| 業務プロセス ライブラリ タスク グループ | cdm_businessprocesslibrarytaskgroup |751866 | 終了した |
| 業務プロセス ステージ | cdm_businessprocessstage |      |     |
| チェックリストのテンプレート ヘッダー | cdm_businessprocesstemplateheader |     |     |
| チェックリストのテンプレート タスク | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>報酬テーブル

| Name | テーブル |既知の問題  | Status |
| --- | --- | ----------      | -------    |
| 固定報酬プラン | cdm_compensationfixedplan |754453 | 終了した |
| 報酬グリッド | cdm_compensationgrid |             |     |
| 報酬レベル | cdm_compensationlevel |           |     |
| 報酬支払頻度 | cdm_compensationpayfrequency |                  |     |
| 報酬基準点設定 | cdm_compensationreferencepointsetup |               |     |
| 報酬基準点設定ライン | cdm_compensationreferencepointsetupline |             |     |
| 報酬地域 | cdm_compensationregion |                   |     |
| 報酬構造 | cdm_compensationstructure |    754456        | 終了した    |
| 報酬変動プラン | cdm_compensationvariableplan |               |     |
| 報酬変動プラン レベル | cdm_compensationvariableplanlevel |                |     |
| 報酬変動プラン タイプ | cdm_compensationvariableplantype |               |     |
| 固定報酬イベント | cdm_fixedcompensationevent |               |     |
| 給付ルール | cdm_vestingrule |              |     |
| 作業者の固定報酬 | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>組織テーブル

| Name | テーブル |既知の問題  | Status |
| --- | --- | ----------      | -------    |
| 部門 | cdm_department |  752194    | 終了した    |
| 雇用 | cdm_employment | 762414  |  終了した  |
| 会社 | cdm_company |  |     |
| ジョブ | cdm_job |  |     |
| 職務権限 | cdm_jobfunction |        |     |
| 職位 | cdm_jobposition | 752214      | 終了した    |
| 職位タイプ | cdm_positiontype |            |     |
| 職位作業者割り当て | cdm_positionworkerassignmentmap | 752224    |  終了した   |
| 職位分析コード | cdm_jobpositiondimension|       |     |
| 職務タイプ | cdm_jobtype |      |     |
| 言語 | cdm_language |        |     |
| タイトル | cdm_title |       |     |

> [!NOTE]
> **職位タイプ** に使用する財務分析コード 、**作業者の職位割り当て**、および **従業員** は、Dataverse にて一方向の統合機能が用意されています。 財務分析コードの更新は、現在のところ、 Dataverse から Human Resources へは同期されません。 

## <a name="leave-and-absence-tables"></a>休暇と欠勤テーブル

| Name | テーブル | 既知の問題  | Status |
| --- | --- |   ----------      | -------    |
| 休暇バンク トランザクション | cdm_leavebanktransaction |  752252    |    解決済 |
| 休暇登録 | cdm_leaveenrollment |  752934    |終了した     |
| 休暇計画 | cdm_leaveplan |   752232   |   終了した  |
| 休暇申請 | cdm_leaverequest | 753207     | 終了した    |
| 休暇申請詳細情報 | cdm_leaverequestdetail | 753207     |   終了した  |
| 休暇タイプ | cdm_leavetype |      |     |
| 休暇タイプの理由コード | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>休暇の Dataverse テーブルを使用する二重書き込み統合は、**機能管理** を使用した Microsoft Dynamics 365 Finance で **単一休暇計画の複数の休暇タイプの構成** が有効になっている場合にのみ使用できます。 

## <a name="payroll-tables"></a>給与テーブル

| Name | テーブル |既知の問題  | Status |
| --- | --- |  ----------      | -------    |
| 支払サイクル | cdm_paycycle |    |     |
| 支払期間 | cdm_payperiod |          |     |
| 給与所得コード | cdm_payrollearningcode |   754458        |   終了した  |
| 銀行口座出金 | cdm_bankaccountdisbursement |    751904     |   終了した  |
| 税地域 | cdm_taxregion |          |     |

## <a name="worker-tables"></a>作業者テーブル

| Name | テーブル |既知の問題  | Status |
| --- | --- |----------      | -------    |
| 作業者 | cdm_worker |    751906    |    終了した |
| 作業者住所 | cdm_workeraddress |   754465     |終了した     |
| 作業者の個人詳細 | cdm_workerpersonaldetail |   751906     |   終了した  |
| 作業者の ID 番号 | cdm_workerpersonidentificationnumber |  766704      |   終了した  |
| 作業者の ID タイプ | cdm_workerpersonidentificationtype |        |     |
| 作業カレンダー | cdm_workcalendar |        |     |
| 作業カレンダー日 | cdm_workcalendarday |        |     |
| 作業カレンダーの休日 |cdm_workcalendarholiday |        |     |
| 作業カレンダーの休日行 | cdm_workcalendarholidayline |        |     |
| 作業カレンダー時間間隔 | cdm_workcalendartimeinterval (カスタム フィールド サポートに対しては有効化されていない) |        |     |
| 作業者の銀行口座 | cdm_workerbankaccount |        |     |

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
