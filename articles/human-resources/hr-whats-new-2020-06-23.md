---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 25 日)
description: このトピックでは、2020 年 6 月 23 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127500"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 23 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3347 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>加入契約は退職した従業員に対して期限切れになると、休暇タイプ、残高、および金額は、休暇登録フォーム にてすべてクリアされます (444867)

**休暇タイプ**、**残高**、および **金額** は、この選択でクリアはされず、維持されるようになります。

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>新しい機能 (1 つの会社または 1 つの計画に対する休暇見越) が有効な場合、予測残高は正しくありません (456553)

1 つの会社または 1 つの計画に対する休暇見越が有効な場合、予測残高は正しいです。

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>ナビゲーション プロパティが重複する可能性のある関係を含むエンティティ (456486)

このリリースでは、複数のエンティティのナビゲーション プロパティ (関係) に関する問題が修正されます。 重複する関係が検出されます。 これらのシナリオは、すべて修正されました。
 
## <a name="cross-company-comments-on-performance-review-455536"></a>パフォーマンス レビューに関する会社間のコメント (455536)

この修正を行うと、会社間コメントがパフォーマンス レビューに表示されるようになります。 この変更により、同じパフォーマンス レビューのために複数の会社で入力された校閲者コメントの表示が修正されます。
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>報酬管理データの表示に不整合があります (432562)

報酬データの一貫した見解が、マネージャーのセルフ サービスで保持されるようになりました。 報酬データは、作業者の **報酬の詳細** にどのように移動するかによって、一貫してマネージャーに表示されるようになっています。
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>固定報酬プランの有効日の既定値は、今日の日付です (411994)

これで、報酬の開始日は、従業員に割り当てられている職位の開始日に基づいています。

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>半日の定義を有効にする休暇と欠勤のフォームが開くと、その定義は無効になります (452607)

この変更により、**半日の定義を有効にする** は、新しい休暇トランザクションが存在するまで有効になります。 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Excel 経由で HcmDiscussionEntity に発行することはできません; TotalRatingScore フィールド エラー (453899)

これで、Excel ブック デザイナーの **HCMDiscussionEntity** を使用して、**TotalRatingScore** 項目を更新できます。

## <a name="in-preview"></a>プレビュー

## <a name="database-logging"></a>データベースのログ

データベース ログを使用すると、監視するテーブルとフィールドを決定できます。 また、Change Tracking を起動するイベントを決定することもできます。 これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。 詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。

## <a name="mandatory-fields"></a>必須項目 

人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。 この機能には **保存されたビュー** が必要です。

## <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。 

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

## <a name="configure-the-name-of-employee-self-service"></a>従業員セルフ サービス名のコンフィギュレーション

**人事管理パラメータ** で新しいオプションが使用可能になり、従業員セルフ サービス ワークスペースの名前をセルフ サービスに更新します。

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse 内ですぐに使用可能になります。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]