---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 7 月 8 日)
description: このトピックでは、2020 年 7 月 8 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 07/08/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b277333ea37c2b6157ae9befc9d94f0e35ff97be
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891892"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 7 月 8 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3382 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="database-logging"></a>データベースのログ

データベース ログを使用すると、監視するテーブルとフィールドを決定できます。 また、Change Tracking を起動するイベントを決定することもできます。 これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。 詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。

## <a name="configure-the-name-of-employee-self-service"></a>従業員セルフ サービス名のコンフィギュレーション

**人事管理パラメータ** で、**従業員セルフ サービス** ワークスペースの名前を **セルフ サービス** に変更できるようになりました。 詳細については、[従業員セルフ サービス ワークスペース名の変更](hr-employee-self-service-workspace-name.md) を参照してください

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>期間外の福利厚生管理のオープン登録アクセス

このリリースでは、従業員が登録期間外またはライフ イベントなしで福利厚生のオープン登録にアクセスできるバグを修正します。 そのため、従業員セルフ サービスでオープン登録をデモする必要がある場合は、オープン登録日を今日 (またはそれ以前) に調整して、アクセスできるようにする必要があります。 この設定は、**福利厚生管理 > ルールとオプション期間** で変更できます。

## <a name="email-employee-enrollment-confirmation"></a>従業員の登録確認メール

福利厚生の選択が完了した後、従業員に電子メールを送信できるようになりました。 既定のメッセージを送信するか、組織の電子メール テンプレートを使用することができます。 これらの設定は、**人事管理パラメータ > 福利厚生の管理** にあります。

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>人員ワークスペースの今後の休暇にキャンセルされた休暇が引き続き表示される (441358)

キャンセルされた休暇は、**人員** ワークスペースの休暇カードに今後の休暇として表示されなくなりました。

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>PositionV2 エンティティで部門エンティティのプロパティを使用できない (456486)

重複リレーションを作成せずに部署を追加できるようになりました。

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity は、退職プランの計算フィールドのみを使用する必要がある (459779)

**PayrollWorkerEnrolledBenefitDetailEntity** エンティティをエクスポートする場合、エクスポートは、レート テーブルに基づく計算フィールドを使用するか、バッキング テーブルで **ContributionAmountCur** フィールドを使用するかを決定します。 データ エンティティがロジックは、アプリケーションが通常使用しない状況で、レート テーブルを使用します。 このロジックでは、計算レート テーブルがなく、製品では顧客が指定できないため、エンティティ エクスポートでは、この列の値がゼロになります。
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>人事管理および従業員セルフ サービスにおけるチェコ語での翻訳の混乱 (400276)

このリリースでは、**会社のディレクトリ**、**次の登録済コース**、**職務**、および **職位** の翻訳が修正されます。
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment テーブルでは、作成および変更されたシステム フィールドが有効になっていない (460171)

作成および変更されたシステム フィールドが、Human Resources の **WorkCalendarEmployment** テーブルで有効になりました。
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>将来の従業員の採用および詳細の追加に関する null 参照例外 (455475)

このリリースでは、**採用および詳細の追加** オプションを使用して従業員を採用すると、合理化された従業員エントリのエラー (null 参照) が修正されます。

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Dataverse 作業者エンティティに加えられた変更が、Human Resources に反映されない (455652)

Dataverse の **作業者** エンティティの次のフィールドに加えられた変更は、Human Resources に表示されます:

- **自宅での作業**
- **勤続日数**
- **記念日**
- **元の採用日付**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>職位に割り当てられた職務に基づいて正しい報酬レベルがデフォルト設定されない (394136)

この変更により、正しい報酬レベルが **職位の詳細** の **有効日** レコードと **報酬プラン割り当て** の **開始日** に基づいてデフォルト設定されます。

## <a name="in-preview"></a>プレビュー

## <a name="mandatory-fields"></a>必須項目 

人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。 この機能には **保存されたビュー** が必要です。

## <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、[Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md) を参照してください。 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ
 
福利厚生管理エンティティはリリースされてます。 DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。 福利厚生管理テンプレートは、データの移動に使用できます。 テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。

## <a name="buy-and-sell-leave"></a>休暇の売買 

一部の組織では、従業員が休暇を購入または売却できるという利点があります。 このプロセスは、多くの場合、手動で管理します。 この機能により、人事部門のポリシーと申請の管理を自動化します。 休暇管理プロセスを合理化し、ミスをなくすことができます。 詳細については、以下を参照してください。

- [休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [休暇の売買](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>1 社または 1 プランの有給休暇

顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。 この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。 詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。

## <a name="add-attachments-to-time-off-requests"></a>添付ファイルを休暇申請に追加

承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。 従業員はこれらの添付ファイルを追加できます。 また、休暇申請がどのように更新されるかについても、より深く理解することができます。 詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。

## <a name="add-reason-code-to-accrual-suspensions"></a>休暇付与の一時停止に理由コードが追加されました 

見越計上の中断に理由コードが追加されました。

## <a name="carry-forward-rules"></a>繰越ルール 

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>指定した休暇タイプに対する休暇付与の一時停止

無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF エンティティで休暇付与の一時停止が可能 

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="coming-soon"></a>間もなく公開

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]