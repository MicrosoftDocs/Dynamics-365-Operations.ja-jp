---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 25 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 98ac7df9fa33635814b390427fd3292bdc1175ed
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528648"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 25 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="coming-soon-in-attract"></a>Attract で間もなく公開

### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの **承認** セクションに表示されます。 承認者は **自分に割り当て済み** で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済** で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2357 に適用されます。

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>基本職位に対して表示された正しくない値 (314266)

これらの変更によって、すべてのページ上で **基本職位** 設定が一貫して表示されます。

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>確認中のワークフローをリコールした後、編集できない (318180)

ワークフロー経由でリコールされた確認が編集できるようになりました。

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>確認中の最終コメント フィールドが翻訳されない (325921)

**最終コメント** ラベルは、Talent で翻訳されるようになります。

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>プレビュー機能はサンドボックス環境でのみ有効になります

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを **実稼働** または **サンドボックス** のどちらかに指定することができます。 **サンドボックス** インスタンス タイプにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働** インスタンス タイプに更新されます。 既存のインスタンスのいずれかを **サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

## <a name="in-preview"></a>プレビュー

### <a name="restrict-the-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまなタイプの休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、Human resources (HR) によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="coming-soon-in-core-hr"></a>Core HR で間もなく公開

### <a name="feature-management-area-in-talent"></a>Talent における機能管理領域

機能の問題のため、**システム管理** から **機能管理** が削除されます。 将来のリリースで、**機能管理** を再紹介します。 

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

次のエンティティは、カスタム フィールドをサポートします: **給与所得コード**、**固定報酬イベント**、**報酬グリッド**、**支払期間**、および **報酬基準点設定**。 

### <a name="new-common-data-service-entities"></a>新しい Common Data Service エンティティ

**理由コード** エンティティが、Common Data Service に追加されます。

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>マネージャー セルフサービスの直接および拡張レポートに関する業績情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。

### <a name="print-performance-reviews"></a>業績の確認の印刷

従業員、マネージャー、および HR は、従業員の業績の確認を印刷できるようになります。
