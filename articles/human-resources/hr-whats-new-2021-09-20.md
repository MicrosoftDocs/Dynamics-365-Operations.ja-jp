---
title: Dynamics 365 Human Resources の新機能と変更された機能 2021 年 9 月 20 日
description: この記事では、2021 年 9 月 20 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59f1b0e3c35d1dce045b4a3932d99fab398e5516
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069759"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Dynamics 365 Human Resources の新機能と変更された機能 2021 年 9 月 20 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4464 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md) |
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号 | 問題 | Description |
|---|---|---|
| 619774 | 住所の説明への編集は、リアルタイムでは Dataverse に同期されません。 | 作業者の住所の説明を編集しても、更新された説明が Dataverse にリアルタイムでは同期されません。 **ロジスティクスの場所** のテーブルのサブスクリプションが更新され、更新が送信されます。 |
| 614603| **作業者** ページで **作業者の人事アクション** パラメーターが選択されていない場合のエラー。 | 新規の作業者を雇用するとき、または **作業者** ページに移動するとき、**人事アクション** がオフになっていても、「フィールドの **人事アクションタイプ** を入力する必要があります」というエラーが表示されます。 |
| 615367 | **承認済の時間オフ** タブでは警告が表示され、誤って表示されます。 | **休暇タイプごとに休暇単位を構成する** 機能を有効にする前に休暇単位が **日数** に設定されている場合、**承認済休暇** タブに無効な警告および正しくない列が表示されます。 |


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
| 福利厚生明細書の **従業員セルフサービス** の **レポート パラメータ** ページが正しくありません。 | **従業員セルフサービス** の **福利厚生明細書** に移動すると、**レポート パラメータ** ページには、バックグラウンドのクイック タブに **含めるレコード** と **実行するレコード** が表示されます。  これらを削除する必要があります。 |
| 終了した期間および将来の期間が、福利厚生明細書の **レポート パラメーター** ページに表示されます。 | **福利厚生明細書レポート** の行先ページに移動すると、決算が完了した、または将来日付である福利厚生計画期間を選択すると、空白のページが表示されます。 リストに表示する必要があるのは、現在の福利厚生計画の期間のみです。 |
|GERレポート宛先を使用してレポートを電子メールで送信するとエラーが発生します。 | 福利厚生明細書は、**GERレポートの送信先** ページ内のメール パラメーターを使用するように設定できます。 設定を完了してレポートを印刷すると、ユーザーに書式設定エラーが発生し、福利厚生に関する明細書が送信されません。|


## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

| フィーチャー | 細目 |
|---|---|
| プラットフォーム 更新プログラム 10.0.21 (45) | プラットフォーム更新プログラム 10.0.21 のロールアウトは、2021 年 10 月 4 日のサービス リリースで開始する予定です。 詳細については、[財務と運用アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) を参照してください。 |
|業務仕訳の拡張レポート ビュー | この機能は、次の展開で既定で有効になります。 |


## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

