---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 4 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528051"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 4 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="coming-soon-in-attract"></a>Attract で間もなく公開

### <a name="job-approvals-on-the-home-page"></a>ホーム ページのジョブ承認

承認は、ダッシュボードの **承認** セクションに表示されます。 承認者は **自分に割り当て済み** で自分の承認を確認できます。 このセクションでは、ジョブ ID、タイトル、他の承認者、およびジョブが割り当てられた日付について示します。 承認のためにジョブを送信するユーザーは、**ユーザーにより要求済** で自分のジョブを確認できます。 このセクションでは、送信されたジョブを承認する必要がある承認者について示します。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2330 に適用されます。

### <a name="new-page-to-validate-position-hierarchy-data"></a>職位階層データを検証する新しいページ

人事管理 (HR) スタッフおよび管理者は、誤ってインポートされた循環参照に対して管理階層を検証できます。 この新しいページは、**組織管理 \> リンク \> 職位 \> 職位階層の検証** でアクセスすることができます。

### <a name="specify-reason-codes-on-leave-types"></a>休暇タイプの理由コードの指定

組織は、休暇申請に関する追加情報を要求する場合があります。 休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休暇申請で固有の休暇タイプについては理由コードが必要

従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 この要件は、会社のポリシーや規制要件が原因であることがあります。 どの休暇タイプに理由コードが必要かを指定できます。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します

従業員の休暇を追跡し、どのように計算するかを理解する機能は、HR が従業員の質問に答えるのに役立つだけでなく、従業員への正確な休暇の付与を保証することにも役立ちます。 HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは休暇残高の背後にある理由を確認することができるようになりました。

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Talent からレコードを削除しても、Common Data Service からは削除されません。

Talent: Core HR から削除されたレコードは、Common Data Service からも削除されるようになりました。

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>変動報酬プランの有効期限の開始日と終了日は反映されません。

今回のリリースでは、開始日が計画の開始日より前、または終了日が計画の終了日より後である場合に、従業員を変動報酬プランに登録することはできません。 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>ユーザーがキャンセルを選択した場合、業績の確認のコメントは削除されます

このリリースは、ユーザーがコメントの変更を開始した後に **キャンセル** を選択した場合、確認のコメントが削除されるという問題を修正します。 

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを **実稼働** または **サンドボックス** のどちらかに指定することができます。 **サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働** インスタンス タイプに更新されます。 既存のインスタンスのいずれかを **サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

### <a name="restrict-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまな種類の休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、HR によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="coming-soon-in-core-hr"></a>Core HR で間もなく公開

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>マネージャー セルフサービスの業績に関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行により、従業員と共同管理をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスがスムーズに行われることを保証できます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。 

### <a name="print-performance-reviews"></a>業績の確認の印刷

従業員、マネージャー、および HR は、従業員の業績の確認を印刷できるようになります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]