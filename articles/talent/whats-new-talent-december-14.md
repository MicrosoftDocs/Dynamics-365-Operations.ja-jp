---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 12 月 14 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518441"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 12 月 14 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.2085**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="changes"></a>変更

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>米国 – ACA (Affordable Care Act) が 2018 税年度 の 1095 B および 1095-C フォームをサポート

毎年、該当する大規模雇用者 (ALE) は各フルタイム従業員に 1095-C を提供する必要があります。 また、雇用主が自家保険を提供する場合、1095-C (ALE の場合) および 1095-B (小規模の雇用者の場合) を、提供される健康プログラムの対象となるフルタイムまたはパートタイム従業員に提供する必要があります。 この機能には、1095-C および 1095-B の両方の印刷可能なフォームが用意されています。

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>インポート中は HcmPerfJournalEntity の SubmittedByPersonId フィールドが無視されます。

業績仕訳帳入力のインポート中およびエクスポート中に、**送信者**フィールドは無視されます。 この変更によって、**インポート/エクスポート**値がエクスポート中のテーブルの値に反映され、インポート時にインポート ファイルで指定された値にシステムが更新されます。

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>[休暇と欠勤] ワークスペースの分析タブで、非システム管理者ロールの "OpenConnectionError" エラーを表示

この更新により、**休暇と欠勤**ワークスペースの**分析**タブを開いた時のエラーが表示されなくなりました。

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>従業員セルフ サービス、タイルの失敗から親ノードを取得する職位階層のドリルダウン

職位階層が既存のワークスペースに表示されるよう個人用に設定された時の「親ノード取得の失敗」エラーを修正する変更が行われ、職位が階層内で選択されるようになりました。  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>システム管理者は職位ページの給与タブを確認する必要があります

「給与作業者と職位詳細を管理」の既存の権限に正しいセキュリティ要素を加える変更が行われました。 この変更により、既定では、給与管理者が職位ページ上の給与フィールドにアクセスできます。

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>業務の確認をマネージャーに送信しているとき、および %Reviews.PerfPeriod% プレースホルダ―を送信指示で使用しているときのエラー

送信指示で ％Reviews.PerfPeriod％ プレースホルダーを使用する場合に「null 参照」エラーを修正する変更が行われました。

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>作業者の勤続日数がうるう日の場合、要員指標 Power BI レポートにエラーが表示されます

この変更により、うるう日は Power BI でサポートされます。

### <a name="integration-between-core-hr-and-attract"></a>Core HR と Attract 間の統合

採用候補者に関連する Core HR と Attract の統合を更新するための変更が行われました。 採用候補者を**人材管理**ワークスペースに表示するため、次の Common Data Service エンティティが使用されます。

求人応募
- 状態理由はオファー承諾済に設定する必要があります。
-   候補者および求人の提供

候補者
-   候補者情報の提供

求人
-   求人 ID および求人参加者の提供

求人参加者
-   採用マネージャーへの提供

候補者が人事管理に追加されると、候補者カードで利用可能な新しいオプションを使用して候補者を消去することもできるようになりました。

## <a name="coming-soon"></a>間もなく公開

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>休暇と欠勤: 未来の休暇と休暇残高の予測

従業員が休暇を予測し、現在の休暇残高に影響を与えずに将来の休暇時間要求ができるようにするための変更が行われたため、休暇残高の表示方法も変更されました。 

現在表示されている使用可能な残高は、現在までの見越しおよび承認されたすべての休暇申請を含む申請に対して利用可能な休暇の量です。 

予測機能がリリースされると、表示されている残高は、現在までの見越額および申請を含めて、現在の休暇の残高に変更されます。 従業員およびマネージャーの両方が、**休暇**カードと**残高休暇**ウィンドウにある従業員およびマネージャー セルフサービスで更新された残高を参照できます。 **人員**ワークスペースと従業員の**割り当て済の休暇計画**ウィンドウにある更新済みの残高は HR マネージャーが参照できます。

## <a name="known-issue"></a>既知の問題

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Finance and Operations との統合のマッピング エラー

次の問題は、Dynamics 365 for Finance and Operations を統合するための現在のテンプレートで識別されています。 新しいテンプレートは、間もなく公開され、作成されたすべての新しい統合プロジェクトに適用されます。 既存の統合プロジェクトのために、タスク マッピングを更新できます。 更新されたマッピングについては、次の表を参照してください。 

>[!NOTE]
> ジョブ職位から職位親ジョブ割り当てタスクはデータが統合されていません。 この問題は現在調査中です。 現在のマッピングに回避策はありません。 

部門から作業単位タスクは、次のマッピングの更新が必要です。

| 既存のソース フィールド          | 新規ソース フィールド |
| -------------------------------|------------------|
| cdm_description (説明)  | cdm_name (名前)  |

追加のマッピングも追加する必要があります。 最後の**なし**フィールドを選択して、次のマッピングを追加します。

| ソース フィールド                   | 出力先フィールド    |
| -------------------------------|----------------------|
| cdm_description (説明)  | NAMEALIAS (NAMEALIAS)|

更新されたマッピングは、次の画像のようになります。

![部門から作業単位タスク](./media/DepartmentMapping.png)


ジョブからジョブ詳細タスクへは、次のマッピングの更新が必要です。

| 既存のソース フィールド          | 新規ソース フィールド                   |
| -------------------------------|------------------------------------|
| cdm_name (名前)                | cdm_description (説明)      |
| cdm_name (名前)         | cdm_jobdescription (職務明細書)|


更新されたマッピングは、以下の画像のようになります。

![ジョブからジョブ詳細タスク](./media/JobMapping.png)

作業者から作業タスクへは、次のマッピングの更新が必要です。

| 既存のソース フィールド                 | 新規ソース フィールド                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (電子メール アドレス 1)   | cdm_primaryemailaddress (主要な電子メール アドレス |
| cdm_telephone1 (電話1)          | cdm_primarytelephone (代表電話)       |

性別フィールドの変換は、更新する必要があります。 性別の**fn** (機能) マップを選択し、次の値のマッピングを更新します。

| Common Data Service 値                   | Finance and Operations 値                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | 男性                                             |
| 75440001                    | 女性                                           |
| 75440002                    | なし                                             | 
| 75440003                    | 不特定                                      |

更新されたマッピングは、次の画像のようになります。

![作業者から作業者タスク](./media/WorkerMapping.png)

![性別フィールドの変換](./media/WorkerTransform.png)
