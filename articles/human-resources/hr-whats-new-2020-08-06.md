---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 8 月 6 日)
description: このトピックでは、2020 年 8 月 6 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 263650cae4b8408f1f7a4a27c43294d2f51c1444
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800144"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 8 月 6 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3444 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="platform-update-1001236-is-now-available"></a>プラットフォーム更新プログラム 10.0.12(36) が使用できるようになりました。

詳細については、[Finance and Operations アプリのバージョン 10.0.12 のプラットフォーム更新プログラム (2020 年 8 月)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12) を参照してください。

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ
 
福利厚生管理エンティティはリリースされてます。 DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。 福利厚生管理テンプレートは、データの移動に使用できます。 テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。 詳細については、以下を参照してください。

- Dynamics 365 2020 リリース ウェーブ 1 プランでの [DMF エンティティのサポート](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support)
- [データ管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire は、休暇要求を購入および販売するためのワークフローを作成します (446557)

詳細については、以下を参照してください。

- [従業員が ](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)Dynamics 365 2020 リリースウェーブ 2 プランを購入および販売することを許可します。
- [休暇の売買ポリシーの管理](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [休暇の売買](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>アクセスが制限されている作業者の郵便番号 V2 エンティティ (459126)

この変更により、**作業者の郵便アドレス V2** エンティティは、ユーザーに付与される法人アクセスに基づいて制限されます。

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>ワークフローの電子メールハイパーリンク適切なレビューを開くことができない (437398)

プレースホルダーを使用してレビュー ワークフローの業績評価を開くと、メールで生成されたハイパーリンクによって、選択したレコードが表示されるようになります。

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>休暇要求の購買や販売のための新規エンティティ (473180)

これで、データ管理フレームワーク エンティティは、休暇を購入して販売するために使用できるようになります。 詳細については、 [データ管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages) を参照してください。

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>レコード情報を表示したり、高度なフィルタを使用したりすると、ユーザーが他の従業員のレコード (472490) にアクセスできるようになります。

この変更により、従業員セルフサービス ユーザーは、従業員セルフサービスを使用している場合にのみ自分のレコードにアクセスできるようになります。 フィルタ オプションを変更しているときにレコード情報を表示すると、もう一方のデータは表示されなくなります。

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>終了した作業者レコードが含まれる従業員管理分析 (382893)

今回のリリースでは、人事管理分析では、有効な作業者のみが含まれるようになりました。 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>従業員の昇給を処理できません (473125)

この変更により、新しい昇給の有効日を変更した場合に昇給を入力できるようになります。

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>レビュー ワークフローを 2 回以上開始できます (467541)

この変更により、業績評価のワークフローを 1 回だけ開始できます。 マネージャの状態では、確認を開始するためのオプションが表示されなくなります。

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>承認済の休暇要求をキャンセルすると、休暇要求のワークフローがエラーで終了する (472063)

このリリースでは、承認済の休暇要求をキャンセルすると、要求の状態は承認されたままになり、ワークフローは続行します。

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>テンプレートから新しいレビューを作成するときに、システムが終了した作業者を提案しする (460624)

この変更により、新しいレビューをテンプレートから作成するときに、終了した作業者を使用できるようになります。 雇用対象日外の従業員に対してレビューを作成することはできません。

## <a name="position-hierarchy-circular-reference-detection-415879"></a>職位階層の循環参照検出 (415879)

この変更により、配置階層の循環参照検出は、単一時点に制限されています。 異なる日付に対して循環参照検出を実行して、レポート構造に循環参照が含まれていないことを確認できます。

## <a name="buy-and-sell-leave"></a>休暇の売買 

一部の組織では、従業員が休暇を購入または売却できるという利点があります。 このプロセスは、多くの場合、手動で管理します。 この機能により、人事部門のポリシーと申請の管理を自動化します。 休暇管理プロセスを合理化し、ミスをなくすことができます。 詳細については、以下を参照してください。

- [従業員が ](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)Dynamics 365 2020 リリースウェーブ 2 プランを購入および販売することを許可します。
- [休暇の売買ポリシーの管理](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [休暇の売買](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>1 社または 1 プランの有給休暇

顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。 この機能を使用することで、異なる休暇年数や有給休暇ポリシーを持つ顧客に向けた有給休暇のプロセスを明確化します。 詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。

## <a name="add-attachments-to-time-off-requests"></a>添付ファイルを休暇申請に追加

承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。 従業員はこれらの添付ファイルを追加できます。 また、休暇申請がどのように更新されるかについても、より深く理解することができます。 詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。

## <a name="add-reason-code-to-accrual-suspensions"></a>休暇付与の一時停止に理由コードが追加されました 

見越計上の中断に理由コードが追加されました。

## <a name="carry-forward-rules"></a>繰越ルール 

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>指定した休暇タイプに対する休暇付与の一時停止

無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="in-preview"></a>プレビュー

### <a name="mandatory-fields"></a>必須項目

人事管理のパーソナル化機能を使用することにより、フィールドを必須にすることができます。 この機能には **保存されたビュー** が必要です。 保存されたビューに関する詳細については、次を参照してください。

- [保存ビュー - Dynamics 365 2020 リリース ウェーブ 2 プランの一般提供](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) 
- [保存されたビューを十分に活用するフォームの作成](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、以下を参照してください。

- Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF エンティティで休暇付与の一時停止が可能

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="coming-soon"></a>間もなく公開

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。

## <a name="known-issues"></a>既知の問題

**機能管理** ワークスペースには、通常使用可能な場合にプレビュー機能として無効になっている機能が表示される場合があります。 正しくないステータスを示す一般的な機能を以下に示します。 

1.  給付金管理
2.  ケース管理
3.  データベースのログ記録 (監査)
4.  1 つの会社または 1 つの計画の休暇の見越計上
5.  休暇の見越計上の中断
6.  残高調整の理由コードとコメント
7.  休暇の売買
8.  休暇および欠勤カレンダー
9.  休暇繰越ルール
10. 休暇の見越計上の監査
11. 休暇の見越計上の削除
12. 休暇の見越計上の丸め
13. 1 つの休暇計画で複数の休暇タイプを構成
14. 短期休暇の更新
15. 見越計上に従業員の FTE を使用する
16. 会社間報酬ビュー
17. 業績の確認の印刷
18. 休暇の見越計上における休日の修正

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]