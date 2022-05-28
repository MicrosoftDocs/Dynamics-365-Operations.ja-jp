---
title: Dynamics 365 Human Resources 2021 年 5 月 20 日 の新機能、または変更された機能
description: このトピックでは、2021 年 5 月 20 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc7e89fabe1651c858097a6c564b4910a524331f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692754"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Dynamics 365 Human Resources 2021 年 5 月 20 日 の新機能、または変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4189 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| プラットフォーム 更新プログラム 10.0.18 (42) | -- | [財務と運用アプリのバージョン 10.0.18 (2021 年 5 月) のプラットフォーム更新プログラム](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Microsoft Teams 人事管理アプリが半日の定義と日の分割機能に対応 | -- | [Teams での休暇要求の管理](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 問題 |  説明 |
| --- | --- | --- |
| 583776 | 従業員を休暇プランに一括登録すると、レコード エラーが重複する場合がある | このバグは最新のリリースで修正されており、一括休暇計画の登録は正常に処理されます。 |
| 582263 | すべての作業者に対して一度にライフ イベント処理を実行できない | ライフイベント処理で **作業者** フィールドが空欄の場合、すべての作業者が処理される。 |
| 558383 | 既定の指定者が選択されていない場合、基本受取人が 100% としてマークされていない | このバグを修正し、ユーザーが基本受取人のトグルを選択するだけで済むようになりました。|
| 509404 | 部門人数分析が、部門間の従業員の異動を考慮しない |分析結果に部門間の異動も含まれるようになりました|
| 579420 | グリッド内の凍結列が使用できない | 人事管理では利用できない **グリッドの列の凍結** 機能が、「機能管理」では利用できると記載されている。 この機能は、利用可能な機能のリストから削除されました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理適格性ルールでのカスタム フィールドのサポート | [適格性処理のカスタム フィールド サポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[適格性ルールの構成](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 休暇ワークフロー エクスペリエンスの強化 | [休暇ワークフロー エクスペリエンスの強化](https://go.microsoft.com/fwlink/?linkid=2147528) | [休暇申請](hr-employee-self-service-request-time-off.md)|
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
| 休暇見越計上のトランザクション監査 | - | [休暇見越計上のトランザクション監査](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
|  休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
