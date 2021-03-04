---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 10 月 6 日)
description: このトピックでは、2020 年 10 月 6 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
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
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe01a2b82b72bf38bb537ed7b2bf5560235817d9
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529831"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 10 月 6 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。 更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3636 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 休暇カレンダーへの追加の分析情報 | [休暇カレンダー ビューに追加の分析情報を提供する](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [チームおよび会社のカレンダーの表示](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

>[!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックが更新される場合があります。

| 問題の番号 | 出庫 | 説明 |
| --- | --- | --- |
| 448806 | **既定の ID タイプ** は、HCM パラメーターで **RecID** としてエクスポートされる | Human Resources パラメーター エンティティにこの変更を加えると、**既定の ID タイプ** を表示する列が追加されます。 |
| 492923 | タスク記録が Lifecycle Services (LCS) に保存されない | タスク記録を LCS に保存できるようになりました。 |
| 429950 | 職位の変更中に固定報酬が正しく終了しない | **異動従業者** ページで従業者の職位を変更する場合、終了報酬日は、職位の終了日の 1 日前に設定されていました。 報酬終了日が職位終了日と同じになりました。 |
| 467214 | **給与分析** は、**支払レート換算名** が **年次** に設定されている場合にのみ表示される | **年次** 以外の名前の給与レートが報酬分析に表示されませんでした。 この更新により、報酬分析では、すべての支払レート換算を使用するようになりました。 **時間** 別または **給与** 別にレポートを実行すると、時間以外の期間を使用する支払レート換算が、**給与** フィルターに含まれます。 **時間** フィルターには、**時間** 単位の支払レートのみが含まれます。 |
| 482464 | **レビュー** を表示しているときに、フィルターを適用しても **詳細** ビューがグリッド ビューに変更されない | フィルターを適用すると、レビュー グリッドが正常に表示されます。 |
| 483184 | **休暇登録** レコードで **調整済開始日** として **層基準** を選択したときに、Human Resources は休暇の発生を生成しません |**調整済開始日** が入力され、休暇の発生を生成する時に使用されます。  |
| 509731 | 将来の退職従業者の休暇申請が、退職日後の休暇申請の場合、問題が発生する | 申請が退職日よりも前であれば、退職日が決まっている従業員の休暇申請が送信できるようになりました。 |
| 510716 | 報酬分析では、**男性平均時給** に男性従業員と女性従業員の両方が含まれている | 報酬分析では、**報酬の人口統計分析** の **男性平均時給** には女性の平均時給が含まれていました。 現在は、男性のみが含まれています。 |
| 511348 | 福利厚生セルフ サービスでは、本日から福利厚生期間終了まで有効な給付プランのみを表示する必要がある | 失効した給付プランが、**福利厚生の登録** ページで従業員に表示されていました。 この修正により、これらのプランが削除されます。 |
| 512706 | 次のフィールドを読み取り専用に設定します:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | アクションの完了後、分析コードの詳細の **追加** ボタンと **削除** ボタンが正しく有効になりませんでした。 この **職位アクションの詳細** ページの更新により、アクションの完了後にフィールドが編集不可になります。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| ワークフローの申請と承認の強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Common Data Service for Human Resources の仮想エンティティ | [Common Data Service での Dynamics 365 Human Resources コア データの展開](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Common Data Service 仮想エンティティの構成](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>間もなく公開

次の新しい機能が、今後のリリースで予定されています:

- **Common Data Service に含まれるチェックリスト エンティティ**: オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Common Data Service ですぐに使用可能になります。

- **福利厚生管理の理由コード**: 福利厚生管理の理由コードは、Human Resources の既存の理由コードと間もなく結合されます。 福利厚生管理で 15 文字を超える理由コードを作成した場合は、福利厚生管理の **理由コード** フォームで理由コードの名前を 15 文字以下に変更する必要があります。 名前を更新すると、理由コードが人事管理の既存の理由コード フォームの下に表示されます。 この変更は将来使用可能になり、既存の機能には影響しません。

- **マネージャー セルフサービスでのカスタム リンク**: マネージャーをサポートするために、マネージャー セルフサービスの機能を拡張しています。 **自分のチーム** タブにカスタム リンクを追加する機能を追加します。この機能は、従業員セルフサービスの **個人情報タブ** にあるカスタム リンク機能に似ています。 詳細については、[マネージャー セルフサービスのカスタム リンク](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) を参照してください。

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]