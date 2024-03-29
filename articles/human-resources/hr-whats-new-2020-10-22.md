---
title: Dynamics 365 Human Resources の新機能および変更された機能 2020 年 10 月 22 日
description: この記事では、2020 年 10 月 22 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b183ea08a2decc2696ca3bc3997b5cf7f04652d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068064"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 2020 年 10 月 22 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この記事では、Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。 更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3680 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| プラットフォーム更新プログラム 10.0.14(38) | -- | [財務と運用アプリのバージョン 10.0.14 のプラットフォーム更新プログラム (2020 年 11 月)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| 組織および人事管理ワークフロー エクスペリエンスの強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号| 問題  | Description|
| --- | --- | --- |
| 437922 | DMF エンティティを使用して FMLA 時間をインポートすると、読み取り専用エラーが発生します。 | FMLA 時間エンティティを使用して、FMLA ケースに関連付けられた時間をインポートできませんでした。 インポートした時間がケースの残り時間を超えないようにするロジックを追加しました。 |
| 512019 | **前回の繰越** 合計が正しくありません。 | **休暇** ページで、**現在の日付** を次の会計年度期間の初日に変更すると、**年次休暇** タイプの **前回の繰越** 合計が正しく表示されませんでした。 これにより、正しい合計が表示されるようになりました。 |
| 458639 | **作業者の連絡先** エンティティは変更追跡モードをサポートしていません。 | **作業者の連絡先** エンティティを更新して、自分のデータベース (BYOD) シナリオで使用できるようにしました。|
| 505347 | トレーニング マネージャーは、合理化された作業者機能が有効になっている場合に、従業員の休暇申請を送信できます。 | HR アシスタントと HR マネージャー以外のロールは、従業員の time0off 申請を送信できません。 |
| 513490 | 福利厚生管理ログ: 補償オプションのないプランのログを追加します。 | **補償オプションのないプラン** のログ結果を有効にしました。 これらは **プロセス結果** テーブルに表示され、正しく並べ替えられて上部に表示されます。 |
| 517021 | **計画タイプ** にタイプ別に 1 つの登録がある場合、同じ **計画タイプ** コードを持つ複数の計画を選択できません。 | 1 回の登録のみが許可される計画の選択制限を変更しました。 制限は、**計画タイプ** ではなく、**計画タイプ コード** レベルになりました。 この変更により、HSA や FSA などの両方とも同じタイプの計画が可能になりますが、別の **計画タイプ コード** を指定することもできます。 これにより、同じ登録期間に対して両方を選択できます。 |
| 444791 | 報酬プランで **アクセス制限** がオンになっている場合、従業員セルフサービスで報酬を表示することはできません。 | 従業員セルフサービス **報酬** カードでは、従業員が **アクセス制限** をオンにしてプランに登録し、特定のロールに割り当てられた場合、現在の報酬額と増加率は "0" と表示されていました。 この問題を解決し、従業員とマネージャーが自分自身と直属の部下の報酬詳細を常に確認できるようにしました。 |
| 457542 | コースが終了した後にコースの詳細を更新しても、コースを受講した従業員の情報も同じようには更新されません。 | コースを閉じて再び開いた後にコースの詳細を変更すると、従業員情報が正しく更新されるようになりました。 |
| 515342 | **CDSLeaveRequestDetailEntity** を使用してデータを挿入できません。 会社が見つからないか、存在しません。 | **CDSLeaveRequestDetailEntity** を使用してデータを挿入できるようになりました。 |
| 514743 | Microsoft Exchange 使用時の **電子メール パラメーター** フォームのエラー。 | 電子メール プロバイダーが **Exchange** に設定されている場合、メッセージ 「ファイルまたはアセンブリを読み込みできませんでした」 が **電子メール パラメーター** ページに表示されます。 この修正により、**電子メール パラメーター** ページを期待どおりに読み込み、保存することもできます。 |


## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| ワークフローの申請と承認の強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Dataverse for Human Resources の仮想エンティティ | [Dataverse での Dynamics 365 Human Resources コア データの展開](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse 仮想エンティティの構成](hr-admin-integration-common-data-service-virtual-entities.md) |
| LinkedIn タレント ハブとの統合 | [LinkedIn タレント ハブとの統合](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn タレント ハブとの統合](./hr-admin-integration-linkedin.md) |
| マネージャー セルフサービスのカスタム リンク | [マネージャー セルフサービスのカスタム リンク](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [マネージャー セルフサービスのカスタム リンク](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。


## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
