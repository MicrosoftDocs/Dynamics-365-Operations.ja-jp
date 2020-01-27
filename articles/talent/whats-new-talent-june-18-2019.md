---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 18 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 06/18/2019
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
ms.search.validFrom: 2019-06-18
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4323496736ddf3e3558f15679789cbc13013720c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898992"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-18-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 18 日)

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="coming-soon-in-attract"></a>Attract で間もなく公開

### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの**承認**セクションに表示されます。 承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2347 に適用されます。

### <a name="confirmation-of-course-participants-causes-an-error"></a>コース参加者の確認でエラーが発生する

コース参加者に関するレポートを印刷するためのダイアログ ボックスは削除されました。 このレポートは、Talent ではサポートされていません。

### <a name="the-compensation-section-of-the-transfer-worker-page-isnt-available-in-some-scenarios"></a>一部のシナリオでは、移動作業者ページの報酬セクションは使用できません。

この変更により、ユーザーは**移動作業者**ページの入力時に報酬データを入力できるようになります。

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>プレビュー機能はサンドボックス環境でのみ有効になります

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを**実稼働**または**サンドボックス**のどちらかに指定することができます。 **サンドボックス** インスタンス タイプにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。 既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

### <a name="restrict-the-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまなタイプの休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、Human resources (HR) によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="coming-soon-in-core-hr"></a>Core HR で間もなく公開

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

次のエンティティは、カスタム フィールドをサポートします: 給与所得コードおよび報酬基準点。 

### <a name="new-common-data-service-entities"></a>新しい Common Data Service エンティティ

理由コード エンティティが、Common Data Service に追加されます。

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>マネージャー セルフサービスの直接および拡張レポートに関する業績情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスがスムーズに行われることを保証できます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。

### <a name="print-performance-reviews"></a>業績の確認の印刷

従業員、マネージャー、および HR は、従業員の業績の確認を印刷できるようになります。
