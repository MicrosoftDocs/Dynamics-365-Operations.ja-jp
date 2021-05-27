---
title: Dynamics 365 Human Resources (2021 年 2 月 22 日) の新機能および変更された機能
description: このトピックでは、2021 年 2 月 22 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e23dc5d39aa96fd08c7b37422795b22c1463dc9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019301"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Dynamics 365 Human Resources (2021 年 2 月 22 日) の新機能および変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3988 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams 用 Dynamics 365 Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 529994 | **作業者** フォームの **呼称** フィールドを変更しても Dataverse 更新がトリガーできない | **作業者** フォームで **呼称** フィールドが更新されるときに Dataverse が更新されない問題を修正しました。 |
| 532651 | 報酬分析 PBI レポートですべての会社のメトリックスを計算する際に通貨換算が使用されない | 報酬分析 PBI レポートで通貨換算が正確に実行されなかった問題を修正しました。 |
| 552226 | ライフ イベント処理が閉じ、単一ライフ イベントのプランが複数回再開される  | 従業員が複数の法人に属し、ライフ イベントが発生すると、その従業員が属する法人ごとにライフ イベント レコードが生成される問題を修正しました。 ライフ イベントを処理する場合、処理する法人を選択する必要があります。 ただし、処理ロジックはこの法人に対して制約を与えるものではありません。 代わりに、すべての法人を処理し、選択した法人のプランを閉じて再開します。 このアクションは、同じ法人内で複数回処理を行うライフ イベントであり、結果としてライフ イベントの影響を受ける各プランが複数回終了/再開されます。 |
| 518064 | 既定の被指名人として複数がマークされている場合に、適用できるプランで選択された扶養者が 1 人のみである | 複数の既定の被指名人が、適用できるプランで自動選択されない問題を修正しました。 これにより個人の連絡先に主な受益者を指定することもできます。 複数の受益者がいる場合、主な受益者は適用できるプランで 100% と表示されます。 |
| 552365 | プラットフォーム更新プログラム 40 にアップグレードした後、自分のデータベースの持ち込み (BYOD) エクスポート ジョブが失敗する | プラットフォーム更新プログラム 40 を環境に適用後、BYOD エクスポートが失敗する問題を修正しました。 |
| 547123 | ダッシュボードのタスク リストで照会されるタスク数が制限される | タスク リストに表示されるタスクの数は、読み込もうとしているタスクの数が多すぎることで発生するパフォーマンスの問題を修正するために、15 に制限されるようになりました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| マネージャーの休暇を会社間で表示 | [マネージャーの従業員休暇を会社間で表示](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [休暇と欠勤のパラメータのコンフィギュレーション](./hr-leave-and-absence-parameters.md) |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 従業員がビジネスの連絡先情報を編集するのを制限する | [従業員がビジネスの連絡先情報を編集するのを制限する](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse の専門用語の更新

2020 年 11 月より、 Common Data Service は [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro) に改名されます。 詳細については、Power Apps ブログの [公式声明](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)を参照してください。 この改名により、Dataverse で一部の用語が更新されています。 たとえば、*エンティティ* は *テーブル* になり、*フィールド* は *列* になります。 詳細については、[用語の更新](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)を参照してください。

このリリースでは、Dynamics 365 Human Resources と Dataverse の統合に関する用語は、アプリケーション全体で更新されており、これら変更が反映されています。 たとえば、**Common Data Service 統合** フォームが **Microsoft Dataverse 統合** となっています。

Dynamics 365 Human Resources と Microsoft Dataverse の統合の詳細については、[Microsoft Dataverse の統合を構成する](./hr-admin-integration-common-data-service.md) と [Microsoft Dataverse の仮想テーブルを構成する](./hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。

## <a name="updates-to-service-deployment"></a>サービス配置に関する更新

2021 年 2 月 22 日リリース版以降、地域のサービス更新配置を調整しています。 調整には、グローバル地域で Human Resources サービスの更新を受け取る順序の変更や、更新ステージ間の待ち時間の変更が含まれます。 これらの変更により、サービスの安定性、品質、およびサポート性の向上のために、安全な配置の実施 (SDP) に沿った作業が強化されます。

今後も、2 週間の配置頻度を実行していきます。 ただし、更新プログラムは、通常、以前のリリースとは異なる 2 週間サイクルの日に Human Resources 環境に適用されることになります。

サービス更新プロセスの詳細については、[更新プロセス](./hr-admin-setup-update-process.md)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]