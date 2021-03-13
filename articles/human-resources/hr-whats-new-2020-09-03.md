---
title: Dynamics 365 Human Resources (2020 年 9 月 3 日) の新機能および変更された機能
description: このトピックでは、2020 年 9 月 3 日に更新された、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41763a8817d0c39b14284a247cf3e46678e7811b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130858"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Dynamics 365 Human Resources (2020 年 9 月 3 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3504 に適用されます。 一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。

Human Resources の今後の機能の詳細については、[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) を参照してください。 Human Resources の更新プロセスの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

## <a name="in-this-release"></a>今回のリリース

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Human Resources 全体の新しい既定の財務分析コード グリッドとダイアログ パターン (469495)

財務分析コードの新しいパターンが、次の領域で使用できるようになりました:

- 職位アクション (フォーム: **HcmPositionActionDetail**)
- 給与所得コード (フォーム: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>休暇および欠勤カレンダーの機能拡張が有効になっていない場合、会社の休暇カレンダーにエントリが表示されない (484406)

今回のリリースでは、会社の休暇カレンダーに休暇エントリが表示されない問題が修正されています。 この問題は、機能管理オプション **休暇および欠勤カレンダーの機能拡張** が有効になっていない場合にのみ発生します。

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity の問題 (467597)

今回のリリースでは、**BenefitsPlanEmployee** エンティティに関する問題が修正されています。 作業者の登録をインポートする際に、**補充コード** と **計画タイプ コード** が正しく設定されるようになりました。 この問題により、従業員の福利厚生プランが **作業者の福利厚生プラン** フォームと、従業員セルフ サービスの **オープン登録** フォームに正しく表示されませんでした。

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>電子ファイル 1094-C の出力で XML に文字がない (435190)

この変更により、IRS への送信時に必要な文字が 1094-C 出力ファイルにないという問題が修正されています。

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>固定報酬フォームにマップされた従業員の変動報酬テーブル (476117)

この変更により、固定報酬フィールドが固定報酬フォームと連携します。 現在、変動報酬フィールドは、変動報酬フォームでのみ使用できます。

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>休暇タイプにマイナスの最小残高がある場合に、登録前に休暇申請を許可する (469917)

この変更により、登録にマイナスの最小残高があっても、プランに登録する前に休暇申請を入力することは禁止されます。 申請は、プランが有効な場合にのみ入力または送信できます。

### <a name="document-templates-dont-download-457279"></a>ドキュメント テンプレートがダウンロードされない (457279)

この変更により、すべてのドキュメント テンプレートをダウンロードできるようになりました。 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>データが、報酬プラン レポートの支払レート フィールドに行ではなく、列ヘッダーとして表示される (476077)

分析レポートに、**支払レート** の正しい情報が表示されるようになりました。

## <a name="in-preview"></a>プレビュー

### <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、以下を参照してください。

- Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- Human Resources ドキュメントの [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="human-resources-app-in-teams-preview-features"></a>Teams の Human Resources アプリにおけるプレビュー機能
 
-  **通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。 承認者は、休暇申請を承認または拒否することができます。 申請が承認または拒否された場合は、送信者に通知されます。 詳細については、以下を参照してください。
   - Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources ドキュメントの [Teams の Human Resources アプリの通知を有効にする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams)
   - Human Resources ドキュメントの [個々のユーザーの Teams の通知をオンまたはオフにする](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users)
   - Human Resources ドキュメントの [Teams の通知](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications)
   - Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)
 
- **マネージャーの休暇カレンダー** : マネージャーは、直属の部下の承認済み休暇、および保留中の休暇をカレンダーで確認することができます。 このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。 詳細については、以下を参照してください。
   - Dynamics 365 2020 リリース ウェーブ 2 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)
   - Human Resources ドキュメントの [チームの休暇カレンダーの表示](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar)

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション (477004)

ダッシュボードの右側の列に、**自分に割り当てられた作業項目** リストを配置するための新しいオプションが使用可能になりました。 この変更により、すべての作業項目とタスク一覧が同じ領域に表示されます。 この機能を有効にするには、機能管理で **プレビュー - ワークフロー エクスペリエンスの拡張機能** をオンにします。 プレビュー機能をオンにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

この機能は、人事アクション フォームに表示されるワークフロー オプションも促進します。 すばやくアクセスできるように、アクション クイック タブ上にも、ワークフロー オプションは表示されます。 詳細については、以下を参照してください。 

- Dynamics 365 2020 のリリース ウェーブ 2 プランの [組織および人事管理ワークフロー エクスペリエンスの機能強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)

![自分自身に割り当てられた作業項目](./media/hr-workflow-work-items-assigned-to-me.png)

![ワークフロー項目のクイックアクセス](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>間もなく公開

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。

### <a name="benefits-management-reason-codes"></a>福利厚生管理の理由コード

福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。 福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。 名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。 この変更は将来使用可能になり、既存の機能には影響しません。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)
