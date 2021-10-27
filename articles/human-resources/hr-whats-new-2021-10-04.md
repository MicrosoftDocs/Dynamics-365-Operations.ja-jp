---
title: Dynamics 365 Human Resources の新機能および変更された機能 2021 年 10 月 5 日
description: このトピックでは、2021 年 10 月 5 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 10/05/2021
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
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 206c7f590b495278b7899271db0e83b3a4da3edc
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641433"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Dynamics 365 Human Resources の新機能および変更された機能 2021 年 10 月 5 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4485 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| プラットフォーム 更新プログラム 10.0.21 (45) | -- | [Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新する可能性があります:

| 問題の番号 | 問題 | 説明 |
|---|---|---|
| 598896 | 従業員の金額は、従業員が登録を完了するまで表示されません | **従業員セルフサービス** ページでは、福利厚生の従業員の金額が表示されません。 福利厚生の従業員の金額は、**給付金セルフサービス** ページに表示されます。  |
| 613440 | **データ管理** からデータをエクスポートできない | **データ管理** でプロジェクトのデータをエクスポートすると 、エクスポートが予期せず失敗します。 |
| 618327 | 終了した期間および将来の期間は、ベ福利厚生明細書の **レポート パラメーター** ページに表示されます | **従業員セルフサービス** の **福利厚生明細書** に移動すると、**レポート パラメータ** ページには、バックグラウンドのクイック タブに **含めるレコード** と **実行するレコード** が表示されます。 これらのセクションは削除されました。|
| 618326 | **従業員セルフサービス** で、福利厚生明細書の **レポート パラメータ** のページが正しく表示されない| **福利厚生明細書レポート** の対象ページに移動すると、決算が完了した、または将来日付である福利厚生計画期間を選択すると、空白のページが表示されました。 リストに表示する必要があるのは、現在の福利厚生計画の期間のみです。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオン/オフにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| Eligibility のカスタム フィールド |[適格性処理でのカスタム フィールドのサポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [適格性処理でのカスタム フィールドの使用](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| 福利厚生の明細書 |[福利厚生の明細書](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [福利厚生の明細書](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>福利厚生の明細書に関する既知の問題

| 問題 | 説明 |
|---|---|
|**GER レポートの宛先** を使用して、レポートを電子メールで送信するとエラーが発生します | 福利厚生明細書を設定することで、**GERレポートの送信先** ページ内のメール パラメーターを使用できます。 設定を完了してレポートを印刷すると、ユーザーに書式設定エラーが発生し、福利厚生に関する明細書が送信されません。|

## <a name="feature-management-changes"></a>機能管理の変更

| フィーチャー | 説明 |
|---|---|
|業務仕訳の拡張レポート ビュー | この機能は、次のリリースでは既定で有効になります。 |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

| フィーチャー | 詳細 |
|---|---|
| プラットフォーム 更新プログラム 10.0.22 (46) | プラットフォーム更新プログラム 10.0.22 のロールアウトは、2021 年 11 月 1 日のサービス リリースで開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.22 のプラットフォーム更新プログラム (2021 年 11 月) ](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22) を参照してください。 |



## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
