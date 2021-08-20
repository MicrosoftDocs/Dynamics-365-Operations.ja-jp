---
title: Dynamics 365 Human Resources 2021 年 5 月 3 日 の新機能または変更された機能
description: このトピックでは、2021 年 5 月 3 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 05/03/2021
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
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1bfbfabc8ba9c41dfd02c205755042f82387f5e09c88722e2503316bc1cf5feb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770363"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Dynamics 365 Human Resources 2021 年 5 月 3 日 の新機能または変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4140 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| ライフ イベントが作成されると、情報バーを追加します。 | - | ライフ イベントを作成すると、情報バーに作成されたライフ イベントのタイプを示すメッセージが表示されます。

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 559312 |  従業員の固定報酬プランを作成する際にレベルは表示されません。 |  ユーザーのタイム ゾーンと会社のタイム ゾーンが一致しない場合、ジョブに対する報酬レベルは読み取ることができません。 クエリが更新され、UTC 時刻に基づいてフェッチされます。 |
| 573676  | **福利厚生計画** フォームで新しい期間を追加できません。 | フォームが更新され、**福利厚生計画** の **期間** クイック タブで、**新規** ボタンが有効化されます。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 休暇ワークフロー エクスペリエンスの強化 | [休暇ワークフロー エクスペリエンスの強化](https://go.microsoft.com/fwlink/?linkid=2147528) | [休暇申請](hr-employee-self-service-request-time-off.md)|
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
| 休暇見越計上のトランザクション監査 | - | [休暇見越計上のトランザクション監査](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| プラットフォーム 更新プログラム 10.0.18 (42) | プラットフォーム更新プログラム10.0.18 は、2021 年 5 月 17 日のサービス リリースで、展開を開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.18 のプラットフォーム更新プログラム (2021 年 5 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) を参照してください。 |
| 給付金管理適格性ルールでのカスタム フィールドのサポート  | [適格性処理のカスタム フィールド サポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
