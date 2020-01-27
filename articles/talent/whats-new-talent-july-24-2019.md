---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 23 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2019
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
ms.search.validFrom: 2019-07-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffbb29fb89ed6a3fd6db11f2c8d656ab565c43f3
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897652"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-23-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 23 日)

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="pdf-renderer-for-candidate-documents"></a>応募書類のPDFレンダラー

Attract ユーザーは、添付ファイルをダウンロードする代わりに、ドキュメント ビューアーで応募の PDF の添付ファイルを表示できるようになりました。

### <a name="signing-up-for-attract-user-research-group"></a>Attract ユーザー リサーチ グループへのサインアップ 

製品の新機能を計画またはプレビュー機能を出荷する時、指示を伝えるのに役立つユーザーを探しています。 関心のあるユーザーが、アプリのサインアップ リンクを使用して、ユーザー リサーチ グループの一部としてサインアップできるようになりました。

### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの**承認**セクションに表示されます。 承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2394 に適用されます。

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Service のカスタム フィールドに対するエンティティのサポート 

このリリースにより、**作業カレンダー**および**作業カレンダー**日が Common Data Service のカスタム フィールドをサポートするようになりました。

### <a name="restrict-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまな種類の休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、HR によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを**実稼働**または**サンドボックス**のどちらかに指定することができます。 **サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。 既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>マネージャー セルフサービスの業績に関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行により、従業員と共同管理をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。 

## <a name="coming-soon"></a>間もなく公開

### <a name="region-support-for-canada-and-southeast-asia"></a>カナダおよび東南アジアの地域サポート

2019 年 8 月 1 日に、カナダおよび東南アジアの地域で Talent が使用可能になることをお知らせします。 この変更により、カナダおよびアジアの地域で環境を作成できるようになり、それらの場所だけですべての Talent データが管理されるようになります。 新しい環境ダイアログで場所を選択し、[Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) で説明されているように、その環境を LCS での Talent のプロビジョニングに使用することにより、新しい地域に環境を作成することができます。

他の地域からカナダおよびアジア地域への既存のプロジェクトのデータ移行はサポートされていません。 新しいプロジェクトのみ、これら新しくサポートされる地域にプロビジョニングできます。
