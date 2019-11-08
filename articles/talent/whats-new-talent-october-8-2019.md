---
title: Dynamics 365 Talent (2019 年 10 月 8 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626065"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Dynamics 365 Talent (2019 年 10 月 8 日) の新機能および変更された機能

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2542 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>パブリック プレビューからの福利厚生の自由登録の削除

Microsoft では、[Core HR ドライブのオペレーショナル エクセレンスにおける戦略的投資](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/)ブログ投稿におけるお知らせと共に、2019 年 10 月 18 日のパブリック プレビューから自由登録機能を削除しています。 代わりに、新しい機能が将来リリースされます。 現在パブリック プレビューにある福利厚生の自由登録機能は、運用上の用途ではサポートされません。 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Common Data Service 統合は、新しいプロビジョニングで既定でオフになりました (343675)
 
新しい環境が準備されると Common Data Service 統合はオフになります。 詳細については、[Common Data Service 統合のコンフィギュレーション](hr-common-data-service-integration.md) を参照してください。

### <a name="streamlined-employee-entry-and-navigation"></a>合理化された従業員の入力とナビゲーション

従業員の入力とナビゲーションの機能をすべての環境で使用できるようになりました。 この機能を有効にするには、**システム管理 \> リンク \> 設定 \> システム パラメーター \> プレビュー機能**に移動し、**拡張された作業者フォームとナビゲーション**を選択します。 この機能は、すべてのユーザーに対して有効になります。 このオプションはいつでもオフにすることができます。

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プラン[合理化された従業員のデータ入力](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry)を参照してください。

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>問題: Attract および Onboard により、無効な作業者が Core HR に作成される (380517)

今週のリリースでは、Attract および Onboard により無効な作業者が Core HR に作成されるという問題が修正されます。

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>問題: 従業員の退職に際してマネージャーが別の会社にサインインすると、ワークフローが失敗する (346852)

マネージャーがサインインしている法人に基づいてワークフローが失敗することはなくなりました。

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>問題: HcmOnboardingWorkerChecklistTaskEntity に関する情報が不足している (349591)

このリリースには、**HcmOnboardingWorkerChecklistTaskEntity** に関する追加情報が含まれています。 次にいくつか例を挙げます。

- **グループ名** 割り当てられたタイプが**グループ**の場合
- **従業員名** 割り当てられたタイプが**従業員**の場合
- **マネージャー名** 割り当てられたタイプが**マネージャー**の場合

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>問題: Common Data Service 管理においてエンティティがアルファベット順にリストされていない (377414)

エンティティは、**CDS 管理**ページにアルファベット順にリストされるようになりました。

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>問題: 未来の日付で雇用タイプを変更しても、職位割り当てが許可されない (339958)

この変更により、作業者タイプが変更された場合 (たとえば、従業員から契約社員へ) に職位割り当てが可能になります。

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>問題: Common Data Service 休暇バンク トランザクション エンティティを更新すると、Talent に新しいレコードが作成される (352938)

休暇バンク トランザクションの Common Data Service が更新されると、休暇トランザクションが更新されるようになりました。

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>問題: フィードバック項目の添付ファイルのタイトルに、フィードバックの説明が表示される (343765)

フィードバックの説明は、添付ファイルのタイトルに表示されなくなります。

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a>問題: 報酬ワークフローのコメント フィールドに正しくない内容が表示される (339297)

この変更により、**%HcmActionState.HcmWorkerActionComment.Comments%** フィールドの内容が表示されます。

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>問題: WorkCalendarEntity と WorkCalendarDayEntity が OData を通して公開されていない (376329)

このリリースでは、**WorkCalendarEntity** および **WorkCalendarDayEntity** がオープン データ プロトコル (OData) を通して使用できるようになりました。

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a>問題: OData が使用されると HCMWorkerEntity の速度が低下する (375221)

変更により、Microsoft Excel ブック デザイナーが使用される場合、**HCMWorkerEntity** のパフォーマンスは向上します。

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>問題: 業績仕訳帳を削除して新しい仕訳帳を作成した後に、マネージャー業績仕訳帳入力でエラーが表示される (336061)

このリリースでは、1 つの業績仕訳帳が削除され、その後すぐに新しい仕訳帳が作成された場合に発生する問題が修正されています。 この修正により、マネージャーのセルフサービスの動作が変更されます。

## <a name="coming-soon"></a>間もなく公開

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。
