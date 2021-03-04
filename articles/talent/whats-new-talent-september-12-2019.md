---
title: Dynamics 365 for Talent (2019 年 9 月 10 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461750"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Dynamics 365 for Talent (2019 年 9 月 10 日) の新機能および変更された機能

このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="candidate-e-mail-login"></a>候補者の電子メール ログイン

候補者は、任意の電子メール アドレスを使用してアカウントを作成し、Talent キャリア サイトにログインしてジョブ応募したり、申請ステータスを確認できるようになります。 これは、既にソーシャルアカウントまたは組織の資格情報を使用して、Talent キャリア サイトにログオンできることに加えて実行できることです。

### <a name="job-activation-and-posting"></a>ジョブの有効化と転記

ジョブの有効化と転記に関しては、いくつかの変更が加えられました。 LinkedIn または Broadbean を含む、Talent キャリア サイトまたは外部のジョブ ボードに転記する前に、ジョブを有効にする必要があります。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2482 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>サンドボックス環境および試用環境で、プレビュー機能を有効にできます

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。 サンドボックス タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存のインスタンスのいずれかをサンドボックス インスタンス タイプに更新する場合は、変更要求を開始するよう サポート に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](./provisioning-talent.md) を参照してください。

### <a name="platform-update-29"></a>プラットフォーム update 29

プラットフォーム更新プログラム 29 に関する詳細については [Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 (2019 年 10 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29) を参照してください。

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>データ管理フレームワークで使用できる新しいジョブ基本エンティティ (347202)

このリリースにより、データのインポート/エクスポートに対して新しい基本ジョブ エンティティが使用できます。 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>従業員の高度セキュリティ ポリシーで職位階層で職位が正しく表示されません (354868)

このリリースにより、アクセスが制限された場合、"空白の" 従業員として職位が開いた状態で表示されなくなります。

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>ジョブ フォーム終了ボックスが特定の状況でフォームを閉じることができません (342467)

このリリースには、すべてのシナリオでジョブ フォームを閉じることができるようにする変更が含まれています。

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>人事管理マネージャー ロールに対して、従業員レコードの新しいケースがロックされています (337111)

この変更により、ケース管理フォームは、従業員フォームからアクセスするときにロックされなくなります。

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>雇用終了日の既定値は常に 23:59:59 です (351492)

この変更により、雇用を手動で終了するときに、雇用日を 23:59:59 以外の時間に変更できます。

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>データ管理を通じて所得コードの有効期限を設定できません (336604)

このリリースでは、**PayrollWorkerPositionEarningCodeEntity** エンティティを通じて期限切れになる所得コードを設定できます。

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>従業員の開発分析レポートにデータが表示されません (348737)

今週のリリースでは、従業員のスキルの分析が、正確なレポートを提供するよう更新されました。

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>雇用日/雇用時間の条件の規定値が一日の始めではありません (349101)

この変更により、開始日時の既定値が一日の始めに、終了日時の既定値が一日の終わりになります。

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>従業員アクション フォームの雇用終了日を変更するとエラーが表示されます (354092) 

この変更により、従業員アクションの一環として雇用終了日を変更した場合に発生する問題が修正されます。

### <a name="applying-onboarding-checklists-across-companies-338433"></a>会社間で研修チェックリストを適用します (338433)

このリリースでは、サインインした法人以外の法人で雇用されている従業員に対してチェックリストを適用する機能が提供されるようになります。

## <a name="in-preview"></a>プレビュー

### <a name="streamlined-employee-entry-and-navigation"></a>合理化された従業員の入力とナビゲーション

この機能は、サンドボックス環境で使用可能になりました。 この機能を有効にするには、**システム管理 > リンク > 設定 > システム パラメーター > プレビュー機能** に移動します。 **拡張された作業者フォームおよびナビゲーション** を選択します。 これにより、これらの変更がすべてのユーザーに対して有効になります。 このオプションはいつでもオフにすることができます。

詳細については、[合理化された従業員の入力とナビゲーション](./streamlined-employee-entry.md) を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]