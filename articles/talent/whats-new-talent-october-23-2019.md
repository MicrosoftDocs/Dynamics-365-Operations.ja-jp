---
title: Dynamics 365 Talent (2019 年 10 月 23 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
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
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68e3f428215bdc4f9a4ce0dd69cfd4482c72fbf3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006267"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Dynamics 365 Talent (2019 年 10 月 23 日) の新機能および変更された機能

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2569 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム 30

詳細については、[Finance and Operations アプリのプラットフォーム更新プログラム 30 (2019 年 11 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30) を参照してください。

### <a name="remove-benefits-open-enrollment-preview-feature"></a>福利厚生の自由登録プレビュー機能を削除する

Microsoft では、[Core HR ドライブのオペレーショナル エクセレンスにおける戦略的投資](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)ブログ投稿におけるお知らせと共に、2019 年 10 月 18 日のパブリック プレビューから自由登録機能を削除しています。 代わりに、新しい機能が将来リリースされます。 現在パブリック プレビューにある福利厚生の自由登録機能は、運用上の用途ではサポートされません。

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>作業者フォームで国/地域を 2 回選択すると発生するエラー (350294)

今週のリリースでは、**作業者**フォームで国/地域を選択した際に発生する問題が修正されました。

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>手動入力を許可しない、が true に設定されている場合、財務分析コード値が既定で組み合わせ表示フィールドに設定される (340097)

この変更により、財務分析コードを設定し、手動入力を許可しないオプションを使用すると、システムは分析コード値を**組み合わせ表示**フィールドに正しく既定設定します。

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>個人連絡先フォームのリレーション ルックアップに新しいリレーション タイプを追加する必要がある (347691)

このリリースには、**リレーション タイプ** テーブルに新しいリレーション タイプを追加し、その変更を個人の連絡先のリレーション ルックアップに反映する新しい機能が含まれています。

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>カスタム フィールドの追加リスト値が Common Data Service に反映されない (379599)

今週のリリースでは、既に Common Data Service と同期されている既存のカスタム フィールドに新しいリスト値を追加すると、エンティティに変更を適用した後に新しいピッキング リスト値が表示されます。

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>雇用条件ページで、Excel で開くを選択すると、すべての従業員の雇用条件が表示される (348073)

このリリースでは、選択した従業員の雇用条件のみが Excel で開きます。 会社のセキュリティもすべて尊重されます。

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>作業カレンダーの休日エンティティと作業カレンダーのエンティティの間の関連付けが Common Data Service にない (324178)

この関係は、リリースによって追加されています。 この変更により、従業員の稼働日が PowerApps に表示されるようになります。 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>コンフィギュレーション可能階層を持つ従業員セルフサービス ワークフローの使用時にエラーが発生する (370132)

今回のリリースでは、コンフィギュレーション可能な階層を使用してワークフローをコンフィギュレーションする方法について、より優れたメッセージングを利用できます。 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>システムが、割り当て可能日が有効化した日よりも早い新しい職位の作成を許可する (340103)

この変更により、**割り当てに使用可能**な日付が職位を**有効化** した日付より前の場合には警告が表示されます。

## <a name="coming-soon"></a>間もなく公開

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。

### <a name="feature-management-workspace"></a>機能管理ワークスペース

機能は、すべてのリリースで追加および更新されます 機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。

機能管理に伴う変更の詳細については、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を参照してください。
