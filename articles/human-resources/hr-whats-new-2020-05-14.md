---
title: Dynamics 365 Human Resources (2020年5月14日) の新機能と変更された機能
description: この記事では、2020 年 5 月 14 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 308dd4fc75ab656359e80b518cec00fc74d42ea6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852946"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Dynamics 365 Human Resources (2020年5月14日) の新機能と変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3244 に適用されます。 一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。

## <a name="platform-changes"></a>プラットフォームの変更

プラットフォームの変更は今週のリリースに含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.10 のプラットフォーム更新プログラム (2020 年 5 月)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md) を参照してください。 このリリースには、バグ修正や保存されたビューへの変更が含まれています。
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Dataverse の候補リストがすべての列挙と一致することを保証する (436343)

Dataverse の候補リストがすべての列挙と一致するようになっています。

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>申請の量に応じた休暇申請のワークフローを構成できるようにする (300044)

申請の量に応じて休暇申請のワークフローを設定することができます。
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>高度なセキュリティが有効になっている場合、新しい作業者フォームにて[表示] メニューを使用してデータが公開されます (403185)

このリリースでは、高度なアクセスが有効になっており、他社の作業者がアクセスできるように設定されている場合に、法人間での作業者の閲覧方法が修正されます。

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>単体のプランまたは単一の会社ので連続した休暇取得を可能にする (318844)

この変更により、会社やプランの見越し計上を実行できます。
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>登録された作業者フォームに該当する職位のフルタイム換算 (FTE) を表示する (414658)

休暇タイプで [FTE] オプションが有効になっている場合は、作業者の職位の FTE 値によって作業者の見越計上率が決まります。 このフィールドは、 **登録された作業者** フォームと **一括登録** ダイアログに含まれるようになりました。

## <a name="add-leave-balance-expiration-batch-job-431266"></a>休暇残数の有効期限バッチジョブの追加 (431266)

新しいバッチジョブを日次で実行できるようになりました。 これにより、有効期限が当日になると、残日数が減少します。

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>作業者の個人連絡担当者を使用して、従業員の個人の連絡先をエクスポートしても、親関係タイプの個人連絡先がエクスポートされない (345893)

**作業者の個人連絡担当者** データ エンティティ ( DMF の **HcmPersonalContactPersonEntity** と OData の **PersonalContactPerson**) は、**親** のリレーションシップ タイプが設定されている個人の連絡先をエクスポートできませんでした。 この問題は、この変更後に作成される個人の連絡先に対して修正されています。 **親** タイプの既存の個人連絡先 は、将来的なリリースで修正されます。

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>休暇と欠勤の両方としてマークされている場合に、理由コードに異なるシナリオのものが表示される (434163)

この変更により、合理化された従業員入力を有効にすると、理由コードが休暇および欠勤コードのみに制限されます。

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>プレビュー機能で、従業員に未来日付の休暇を割り当てるとエラーが表示される (433555)

この変更により、休暇計画に2つの休暇タイプが割り当てられていて、従業員を割り当てようとした場合のエラーが修正されます。

## <a name="getting-started-banner-appears-for-all-users-441731"></a>全ユーザーに "はじめに" バナーが表示される (441731)

この変更により、システム管理者やデータ管理者以外のユーザーに対して、[はじめに] のバナーが表示されなくなります。 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Dataverse 作業者の住所エンティティの勤務時間の発効日が、Human Resources とは異なる (425071)

この変更により、特定のシナリオでは、住所の日付に基づいて住所情報の整合性が保たれます。

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>承認済の休暇申請に添付ファイルを追加できない (425407)

今週のリリースでは、休暇申請を変更することなく、承認された休暇申請に添付ファイルを追加することができます。

## <a name="in-preview"></a>プレビュー

## <a name="leave-suspension"></a>休暇の停止

従業員に対し Human Resources で休暇および欠勤を中断できます。 休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。 一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。 詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)

ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>指定した休暇タイプの休暇取得を一時停止する (272447)

今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF エンティティが見越し計上の停止に使用可能 (429549)

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>見越計上の停止に理由コードが追加されました (429547)

見越計上の中断に理由コードが追加されました。

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>人事パラメータから休職,、欠勤パラメータへの移行を開始

このリリースでは、人事管理パラメータと休暇・欠勤のパラメータの組み合わせに対応しています。

## <a name="carry-forward-rules"></a>繰越ルール

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]