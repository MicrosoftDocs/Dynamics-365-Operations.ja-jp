---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)
description: このトピックでは、2020 年 9 月 16 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 591a6f3f4aabdb164e4fde5e80259fb6872167d9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694455"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 9 月 16 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3557 に適用されます。 一部の機能の横にあるかっこ内の数字は、参照用に Lifecycle Services (LCS) サポート番号を示しています。

## <a name="included-in-this-release"></a>このリリースに含まれる

-  [保存されているビュー - 一般提供](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- 詳細については、[保存されているビュー](../fin-ops-core/fin-ops/get-started/saved-views.md) を参照してください。 

- **職位アクション** フォームには、更新された分析コード グリッドと新しいダイアログがあります (469495)。

- **Human Resources 共有パラメーター** の **詳細なアクセス** で **作業者情報へのアクセス制限** を "はい" に設定すると、福利厚生フォームには適切な作業者のみが表示されるようになりました (393384)。

- **WorkCalendar** エンティティの新しいカレンダー生成オプション (477055):<br>- 既定の終了時刻<br>- 既定の開始時刻<br>- 金曜日は就業日ですか<br>- 月曜日は就業日ですか<br>- 土曜日は就業日ですか<br>- 日曜日は就業日ですか<br>- 木曜日は就業日ですか<br>- 火曜日は就業日ですか<br>- 水曜日は就業日ですか<br>- 作業カレンダーの休日 ID

- **LeaveBankTransactionV1** エンティティには、理由コードが含まれるようになりました (477823)。

- タスク記録を保存できるようになりました (492923)。

- データが **HCMWorkerContactEntity** から正常に公開されるようになりました (427620)。

- 契約社員作業者タイプの **報酬** クイック タブが、**作業者アクション** フォームに表示されるようになりました (482494)。

- **固定報酬** を設定した場合、**レベル** と **プラン** フィールドが必須になりました。 これらのフィールドを空白のままにすると、エラー メッセージが表示されます (482497)。

- **福利厚生** の **プラン タイプ** フィールドがドロップ ダウンリストになりました (488768)。

- システム管理者は、カスタム フィールドが Human Resources から削除された場合に、通知を受け取るようになりました (481408)。

- 従業員のプロセスを終了する間、ロックされているように見えた後、Human Resources は期待どおりに動作し、選択した会社を変更しません (479877)。 

- マネージャーは、個人用設定を使用して数値列を追加できなくなりました (485317)。

- マネージャーは、有効期限切れ ID 番号からデータ範囲フィルターを削除できなくなりました (485321)。

- **報告先** フィールドが空の場合でも、職位にカーソルを合わせると職位の詳細が表示されます (433328)。

- 従業員が、従業員セルフ サービスで福利厚生プラン情報を表示できるようになりました (481676)。

- 従業員は、すべての登録済コースを表示できるようになりました (429048)。

- **プロフェッショナル証明書** ページの表示オプションを制限できるようになりました。 表示オプションを現在の法人、作業者ステータス別、および作業者タイプ別に制限できます (451501)。 


## <a name="in-preview"></a>プレビュー

### <a name="human-resources-app-in-teams"></a>Teams の Human Resources アプリ

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、以下を参照してください。

- Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources ドキュメントの [Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams の Human Resources アプリにおけるプレビュー機能
 
-  **通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。 承認者は、休暇申請を承認または拒否できます。 申請が承認または拒否された場合は、送信者に通知されます。 詳細については、以下を参照してください。
   - Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources ドキュメントの [Teams の Human Resources アプリの通知を有効にする](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)
   - Human Resources ドキュメントの [個々のユーザーの Teams の通知をオンまたはオフにする](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)
   - Human Resources ドキュメントの [Teams の通知](./hr-teams-leave-app.md#respond-to-teams-notifications)
   - Human Resources ドキュメントの [チームの休暇カレンダーの表示](./hr-teams-leave-app.md#view-your-teams-leave-calendar)
 
- **マネージャーの休暇カレンダー**: マネージャーは、直属の部下の承認済みおよび保留中の休暇をカレンダー表示で確認できます。 このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。 詳細については、以下を参照してください。
   - Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources ドキュメントの [チームの休暇カレンダーの表示](./hr-teams-leave-app.md#view-your-teams-leave-calendar)

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション (477004)

ダッシュボードの右側の列に、**自分に割り当てられた作業項目** リストを配置するための新しいオプションが使用可能になりました。 この変更により、すべての作業項目とタスク一覧が同じ領域に表示されます。 この機能を有効にするには、機能管理で **プレビュー - ワークフロー エクスペリエンスの拡張機能** をオンにします。 プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

この機能は、人事アクション フォームに表示されるワークフロー オプションも促進します。 すばやくアクセスできるように、アクション クイック タブ上にも、ワークフロー オプションは表示されます。 詳細については、以下を参照してください。 

- Dynamics 365 2020 のリリース ウェーブ 2 プランの [組織および人事管理ワークフロー エクスペリエンスの機能強化](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)

![自分自身に割り当てられた作業項目。](./media/hr-workflow-work-items-assigned-to-me.png)

![ワークフロー項目のクイック アクセス。](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>休暇および欠勤カレンダー

このリリースには、休暇および欠勤カレンダーの追加カレンダー オプションが含まれています。 詳細については、[チームおよび会社カレンダーの表示](./hr-employee-self-service-calendar.md) を参照してください。

## <a name="coming-soon"></a>間もなく公開

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。

### <a name="benefits-management-reason-codes"></a>福利厚生管理の理由コード

福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。 福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。 名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。 この変更は将来使用可能になり、既存の機能には影響しません。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
