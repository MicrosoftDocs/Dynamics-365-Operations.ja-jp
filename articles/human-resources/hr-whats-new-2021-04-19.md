---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 4 月 19 日)
description: このトピックでは、2021 年 4 月 19 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 04/19/2021
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
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1371e453ae51dafe24b2105b1b9b7c38cdb4db4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052364"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 4 月 19 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4113 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| プラットフォーム 更新プログラム 10.0.17 (41) | -- | [Finance and Operations アプリ バージョン 10.0.17 のプラットフォーム更新プログラム (2021 年 4 月)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| 給付金管理フォームでのカスタム フィールドのサポート | [給付金管理でのカスタム フィールドのサポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [福利厚生の管理の概要](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 552164 | **従業員セルフ サービス > 空きのあるコース** の **保存されたビュー** は、議題を含むコースでは機能しない | 保存されたビューが空きのあるコース (ESS) で使用され、コースの 1 つに議題が関連付けられている場合、ビューにはそのコースの複数の行は表示されなくなります |
| 560614 | **給付金 > ライフ イベント オプション** に、ヒント ドキュメントとコード動作の不一致が表示される。 | **ライフ イベント オプション** のヒントが更新され、正しい動作を表示するようになりました。 |
| 560616 | **給付金 > ライフ イベント オプション** は作業者の給付金計画で編集できるが、変更が反映されない。 | ライフ イベント オプション動作が更新され、ヒント ドキュメントごとに扶養者オプションに基づいて有効化または無効化できるようになりました。 |
| 565054 | **詳細なアクセス** がオンの場合に、**雇用されていない作業者** のリストの内容が表示されない。 | このリリースでは、**詳細なアクセス** がオンの場合に、システム管理者にのみ **雇用されていない作業者** リストの内容が表示されるという問題が修正されます。 この修正はセキュリティ上の変更なので、機能管理でオプトインする必要があります。 この機能を有効にすると、詳細なアクセスが有効な場合でも、フォームにアクセスできるロールには内容が表示されます。 詳細については、「[雇用されていない作業者](hr-personnel-workers-without-employment.md)」を参照してください。 |
| 570586 | すべての休暇計画において、その作業者の最新のトランザクションの前に雇用が終了すると、休暇申請の検証が失敗する。 | 雇用が終了した後は、従業員の休暇トランザクションに基づく休暇要求の検証は失敗しません。|
| 570783 | Human Resources 共有パラメーターで会社間休暇を有効にしたり無効にしたりすると、単一の会社で雇用されている従業員が休暇申請でどのような情報を参照できるかが変わる。 | 単一の会社に雇用されている従業員の場合、このパラメーターが有効でも無効でも、休暇の申請の表示に変更はありません。 |
| 572343 | 会社全体で休暇を表示する機能が有効な場合、必要な理由コードが表示されない。 | 会社全体で休暇を表示する機能が有効な場合、理由コードは正しく表示されます。 |
| 573676 | **給付金管理 > リンク > 給付金計画** に **期間** を追加できない。 | 既存の **給付金計画** フォームで **期間** を追加または更新できないバグが修正されました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 休暇ワークフロー エクスペリエンスの強化 | [休暇ワークフロー エクスペリエンスの強化](https://go.microsoft.com/fwlink/?linkid=2147528) | [休暇申請](hr-employee-self-service-request-time-off.md)|
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |
| プラットフォーム 更新プログラム 10.0.18 (42) | プラットフォーム更新プログラム10.0.18 は、2021 年 5 月 17 日のサービス リリースで、展開を開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.18 のプラットフォーム更新プログラム (2021 年 5 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) を参照してください。 |
| 給付金管理適格性ルールでのカスタム フィールドのサポート  | [適格性処理のカスタム フィールド サポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
