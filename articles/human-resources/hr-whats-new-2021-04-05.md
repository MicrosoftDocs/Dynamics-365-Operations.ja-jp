---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 4 月 5 日)
description: このトピックでは、2021 年 4 月 5 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 24f5ab1e1e321f2d783449a5ba9a1fb1523920ae
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021082"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 4 月 5 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4074 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 従業員がビジネスの連絡先情報を編集するのを制限する | [従業員がビジネスの連絡先情報を編集するのを制限する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [個人情報の編集の制限](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 550852 | 承認 **ボタン** は、**レビュー** フォームで設定された必須フィールドでは検証されません。 | **レビュー** フォームのフィールドを必須に設定し、マネージャ ロールの変更を公開すると、フォームは予想どおり検証されません。 |
| 559564 | 固定報酬の変更に対する履歴作業者アクションの変更では、終了したユーザーに対してエラーが発生します。 | 終了した従業員報酬の作業者アクションでエラーが発生します。 従業員が終了した後で、終了前の昇格の作業者アクションでエラーが発生します。 |
| 560074 | 雇用カテゴリのドロップダウンは **作業者タイプ** でフィルタリングされておらず、従業員および契約社員のカテゴリが表示されます。 | **従業員** フォームでは、**雇用カテゴリ** ドロップダウンに、従業員の作業s者タイプに基づいて、従業員または契約社員のカテゴリが表示されます。 |
| 567388 | 新しく作成された従業員の情報の一部は、Dataverse の **cdm_worker** テーブルにすぐには同期されません。 | 新しい従業員レコードを作成すると、新しいレコードは Dataverse の **cdm_worker** テーブルに同期されますが、すべてのプロパティは Dataverse レコードに含まれません。 |
| 563837 | 人事管理表示で使用できない機能。 | 人事管理に適用されないいくつかの機能は、機能管理に表示されます。 これらの機能は、人事管理で有効にできる機能の一覧から削除されます。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |
| プラットフォーム 更新プログラム 10.0.17 (41) | Platform update10.0.17 は、2021 年 4 月 19 日の次のリリースで、展開を開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.17 のプラットフォーム更新プログラム (2021 年 4 月) ](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) を参照してください。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]