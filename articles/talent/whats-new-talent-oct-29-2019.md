---
title: Dynamics 365 Talent (2019 年 10 月 29 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897445"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Dynamics 365 Talent (2019 年 10 月 29 日) の新機能および変更された機能

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2586 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>ロールのない関係者は既定で削除すべき (371233)

Talent で新しい環境をプロビジョニングする場合、**ロールが存在しない関係者を削除**が既定でオンになります。 この設定がオンになっている場合を除き、作業者を削除しても、作業者に関連付けられている関係者は削除されません。 この変更により、作業者のインポート、変更、または再インポートを行う必要がある場合に、グローバル アドレス帳の重複レコードが制限されます。

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>下書きおよびキャンセルされた休暇要求は、Common Data Service で削除が許可されるべき (376999)

この変更により、Common Data Service でステータスが**下書き**または**キャンセル済**になっている休暇依頼を削除できます。

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>カスタム フィールド フォームで適用をクリックしても、カスタム フィールドの追加リスト値が Common Data Service に反映されない (379599)

すでに Common Data Service と同期している既存のカスタム フィールドに新しいリスト値を追加すると、**カスタム フィールド** フォームで変更を適用した後に、Common Data Serivce で使用できるようになります。

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>1 つ以上の雇用がある場合、会社間でオンボーディング チェックリストを適用 (371270)

今週のリリースにより、**作業者フォーム > チェックリスト**で、1 つ以上の雇用のある従業員にチェックリストを適用することができます。

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>福利厚生の自由登録プレビュー機能は削除されました

Microsoft では、[Core HR ドライブのオペレーショナル エクセレンスにおける戦略的投資](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)ブログ投稿におけるお知らせと共に、パブリック プレビューから福利厚生の自由登録機能を削除しました。 新しい機能が将来リリースされます。 福利厚生の自由登録機能は、運用上の用途としてはまだサポートされていません。

## <a name="coming-soon"></a>間もなく公開

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。

### <a name="feature-management-workspace"></a>機能管理ワークスペース

機能は、すべてのリリースで追加および更新されます 機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。

機能管理に伴う変更の詳細については、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を参照してください。
