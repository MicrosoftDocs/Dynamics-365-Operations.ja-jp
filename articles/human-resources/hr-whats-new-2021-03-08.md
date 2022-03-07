---
title: Dynamics 365 Human Resources (2021 年 3 月 8 日) の新機能および変更された機能
description: このトピックでは、2021 年 3 月 8 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37e4ca0658da4ac8e199223496f715ff1cd92653
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057000"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Dynamics 365 Human Resources (2021 年 3 月 8 日) の新機能および変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4017 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| マネージャーの休暇を会社間で表示 | [マネージャーの従業員休暇を会社間で表示](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [休暇と欠勤のパラメータのコンフィギュレーション](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 486611 | **すべてのカレンダーで休暇の無効化** が有効になっている場合、休暇が休暇カレンダーに表示される | **すべてのカレンダーで休暇の無効化** が有効になっている場合、休暇および欠勤カレンダーの機能拡張が有効になっているときに休暇情報が表示されなくなりました。|
| 508972 | 休暇の銀行トランザクション エンティティに登録の検証がない | 休暇の銀行トランザクション エンティティを使用している場合、プランに登録されていない従業員はインポートできなくなりました。 |
| 554854 | ユーザー オプションの既定の法人が異なる場合、雇用エンティティのカレンダー更新でエラーが発生する | 従業員用カレンダーを更新する雇用エンティティを使用すると、ユーザー オプションの既定の法人が異なる場合でもエラーが出なくなりました。 |
| 558347 | 開始ページを読み込むときに「フォーム コンフィギュレーション (FormRunConfiguration) でレコードを作成できない」と表示される。 | 個人用設定により、開始ページを読み込むときに「フォーム コンフィギュレーション (FormRunConfiguration) でレコードを作成できない」と表示されるエラーが発生します。 |
| 557327 | 給付金管理ワークスペース: ギャップがグリッドの上に表示される。 | 給付金ワークスペースのテーブル グリッドの境界に意図しないギャップが表示されるというユーザーエクスペリエンスの問題が修正されました。 |
| 557334 | 給付金管理ワークスペース: **期間** 選択のドロップダウン ボックスが **概要** タブにのみ表示される | 給付金の **期間** 選択のドロップダウン ボックスは、**概要** タブが給付金ワークスペースで有効な場合にのみ表示され、**プロセス結果** および **リンク** セクションでは表示されません。 |
| 557336 | 給付金管理ワークスペース: **チェック アウト済みプランを使用して登録を開く** テキストが、タイル ビューで切り詰められる | 必要なコンテキストが切り詰められることを避けるため、タイル ビューのテキストを **チェック アウト済プラン...登録を開く** に変更されました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 従業員がビジネスの連絡先情報を編集するのを制限する | [従業員がビジネスの連絡先情報を編集するのを制限する](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]