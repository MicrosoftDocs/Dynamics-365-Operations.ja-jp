---
title: Dynamics 365 Human Resources の新機能および変更された機能 2020 年 9 月 26 日
description: このトピックでは、2020 年 9 月 26 日の Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f56371519f0f0fcd6e90c8bc107dd8b1326132b4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467004"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 2020 年 9 月 26 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。 更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3589-hf.3 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です:

- **プラットフォーム更新プログラム 10.0.13 が使用できるようになりました**: 更新プログラムの詳細については、[Finance and Operations アプリ バージョン 10.0.13 に対するプラットフォーム更新プログラム (2020 年 10 月)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13) を参照してください。

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックが更新される場合があります。

| 問題の番号 | 出庫 | 説明 |
| --- | --- | --- |
| 469495 | 既定の財務分析コード グリッドとダイアログ ボックスの更新 | 財務分析コード グリッドとダイアログ ボックスは、Human Resources 全体で更新されます。 |
| 474887 | 休暇申請作業項目が手動決定で誤ったリンクを開く | ワークフロー コンフィギュレーションに手動決定が含まれている場合、**自分自身に割り当てられた作業項目** から休暇申請に移動すると、誤ったリンクが開き、手動決定用に割り当てられたものではなく、現在のユーザーによって作成された空白のフォームまたは休暇申請が表示されます。 |
| 474962 | 休暇と欠勤パラメーター エンティティにあいまいなラベルのフィールドがある | 休暇と欠勤パラメーター エンティティ ラベルが更新され、わかりやすくなりました。 |
| 481401 | 発生日基準が発生開始日より後で月末の場合、発生処理がハングする | 発生日基準が発生開始日より後で月末の場合、発生処理に遅延が発生しないように更新されます。 |
| 447167 | 期限が切れるレコード リストに非アクティブな従業者が含まれる | **人事管理** の **期限が切れるレコード** タブには、に非アクティブな従業者が含まれていました。 現在は、アクティブな従業者のみが含まれます。 |
| 486840 | **自分自身に割り当てられた作業項目** から誤った休暇申請が開く | **自分自身に割り当てられた作業項目** から休暇申請を選択しても、現在のユーザーに割り当てられた直近の休暇申請を開かなくなりました。 |
| 506868 | **職位** エンティティの Dataverse **タイトル** フィールドが設定されていません | **職務** と **職位** エンティティの **タイトル** フィールドが未指定として表示されました。 現在、**タイトル** フィールドが表示されます。 |
| 430359 | 管理者ロールと従業員ロールが割り当てられているオフボード チェックリスト タスクにアクセスできない | 将来の退職日が決まっている従業者が、従業員ロールまたは管理者ロールしか持っていない場合、チェックリストのタスクにアクセスできませんでした。 これにより、従業員ロールまたは管理者ロールしか持っていないユーザーは、将来の退職日でオフボード タスクにアクセスできます。 |
| 458102 | 新規従業員が、作成時に **従業者給与情報** エンティティに表示されない | 新規従業員は、エンティティをエクスポートする前に従業員の給与情報を開くことなく、従業者給与情報に含まれます。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| ワークフローの申請と承認の強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>間もなく公開

今後のリリースでは、次の新しい機能が予定されています:

- [マネージャー セルフサービスのカスタム リンク](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)
[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[更新プロセス](hr-admin-setup-update-process.md)
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]