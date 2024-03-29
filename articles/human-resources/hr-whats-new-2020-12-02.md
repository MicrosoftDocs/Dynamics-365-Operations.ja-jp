---
title: Dynamics 365 Human Resources (2020 年 12 月 2 日) の新機能および変更された機能
description: この記事では、2020 年 12 月 2 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cecef6d2e73b42126b1be100dca52ebd8d9270fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848110"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Dynamics 365 Human Resources (2020 年 12 月 2 日) の新機能および変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3788 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| マネージャーは職位の採用要求を送信できます | [マネージャーは空いている職位の採用要求を送信できます](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [採用要求の追加](./hr-personnel-recruit.md#add-a-recruiting-request) |
| 人材管理で改善された候補者のプロファイル | [人材管理で改善された候補者のプロファイル](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [候補者プロファイルの追加または編集](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| 簡素化された採用プロバイダーとの統合を有効化 | [簡素化された採用プロバイダーとの統合を有効化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [職務候補者の採用](./hr-personnel-recruit.md) |
| マネージャー セルフサービスのカスタム リンク | [マネージャー セルフサービスのカスタム リンク](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [マネージャー セルフサービスのカスタム リンク](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号 | 問題 | Description |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult には、処理に使用された日時を含める必要があります。 | BenefitEligibity 処理結果に、以前は含まれていなかった前回の処理の datetimestamp が含まれています。 |
| 526903 | **人事管理の共有パラメーター** で **被指名人の自動選択** がオンになっているときは、扶養者のいるプランでは給付金の登録は失敗します。 | **被指名人の自動選択** オプションで既定の被指名人がオンになっているときに発生する扶養者に対する給付金登録の失敗に関する問題が解決されました。 |
| 521922 | **詳細なしで休暇を表示** パラメーターでは、チームの休暇カレンダーにある休暇要求の詳細を表示します。 | **詳細なしで休暇を表示** が **休暇パラメーター** で **はい** に設定されているときに、休暇タイプ、休暇タイプの色、および日付の詳細がチームの休暇カレンダーに表示されていました。 これが解決すると、今度は休暇タイプが表示されなくなり、チームの休暇カレンダーにあるすべての休暇タイプに既定の休暇タイプの色 (濃い青) が使用されます。 |
| 527316 | 職務、職位、および作業者の通知に対するタイトルの変更は同期されません。 | 以前、タイトルの関係は、職務、職位、および作業者のエンティティに追加されました。 このリレーションの同期は、Human Resources から Dataverseの同期には適用しますが、Dataverse からの通知には適用しませんでした。 この問題は解決されました。 |
| 512275 | **休暇パラメーター** から色のオプションを削除します。 | これで休暇タイプで色が定義され、**休暇パラメーター** で色のオプションが不要になったため、色のオプションが削除されました。 |
| 437112 | 従業員の職位割り当て時に誤解を招くエラー メッセージ テキスト。 | 作業者を採用して有効でない職位を割り当てようとしているときに表示されるエラー メッセージを更新しました。 更新済メッセージ **指定された職位は雇用開始日の時点で有効ではありません。この職位の期間を確認してください。** |
| 527816 | **休暇** ページのパフォーマンス問題。 | **休暇** ページでパフォーマンスが改善されました。 |
| 523158 | BenefitPeriodMigrationUpgrade と BenefitPlanMigrationUpgrade は実行されません。 | 適切に実行されていない **期間** および **プラン** に関連する給付金移行職務に関する問題が解決されました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| ワークフローの申請と承認の強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn タレント ハブとの統合 | [LinkedIn タレント ハブとの統合](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub との統合](./hr-admin-integration-linkedin.md) |
|マネージャーの休暇を会社間で表示 | [マネージャーの従業員休暇を会社間で表示](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [休暇と欠勤のパラメータのコンフィギュレーション](./hr-leave-and-absence-parameters.md) |
|休暇残高に追加の分析情報を提供する| [休暇残高に追加の分析情報を提供する](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [従業員の休暇の管理](./hr-leave-and-absence-manage-employee-leave.md) |
| マネージャーは職位の採用要求を送信できます | [マネージャーは空いている職位の採用要求を送信できます](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [採用要求の追加](./hr-personnel-recruit.md#add-a-recruiting-request) |
| 人材管理で改善された候補者のプロファイル | [人材管理で改善された候補者のプロファイル](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [候補者プロファイルの追加または編集](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| 簡素化された採用プロバイダーとの統合を有効化 | [簡素化された採用プロバイダーとの統合を有効化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [職務候補者の採用](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]