---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 11 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f2ee23733d686480cd4323cab952ae12eceaf142
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897583"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 6 月 11 日)

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="search-engine-optimization-for-job-posts"></a>人材募集のための検索エンジンの最適化

Dynamics 365 Talent: Attract 管理センターで**検索エンジン最適化**が有効にされた後、Attract は Google インデックス作成アプリケーション プログラミング インターフェイス (API) に、新しいジョブの有効化およびポスト時、または既存のジョブが更新された時に Web ページのクローリングを行うよう通知します。 このようにして、ジョブは Google および他の検索エンジンの検索結果に表示されます。

同様に、ジョブをアンポストした場合、Attract はインデックス作成 API に通知し、アンポストされたジョブは検索結果に表示されなくなります。

> [!NOTE]
> Web クローラーには、Web ページのクローリングまたは検索結果の更新のために定義されたタイムフレームはありません。

## <a name="coming-soon-in-attract"></a>Attract で間もなく公開

### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの**承認**セクションに表示されます。 承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2337 に適用されます。

### <a name="platform-update-27-for-finance-and-operations"></a>Finance and Operations のプラットフォーム更新プログラム 27

Finance and Operations のプラットフォーム更新プロフラム 27 の詳細については、[Dynamics 365 Finance and Operations プラットフォーム更新プロフラム 27 (2019 年 6 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27) を参照してください。

### <a name="feature-management-workspace-in-talent"></a>Talent における機能管理ワークスペース

**システム管理**の**機能管理**ワークスペースにより、各リリースで提供されている機能の表示、有効化、無効化、およびスケジュールを行うことができます。 既定では、新機能が無効になっています。 **機能管理**ワークスペースを使用して、ドキュメントを有効にし、表示することができます。

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

発行機関エンティティは、カスタム フィールドをサポートするようになりました。

### <a name="new-common-data-service-entities"></a>新しい Common Data Service エンティティ

タスク グループ エンティティが追加されました。

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>プレビュー機能はサンドボックス環境でのみ有効になります

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。 サンドボックス インスタンス タイプにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。 既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

### <a name="restrict-the-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまなタイプの休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、Human resources (HR) によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="coming-soon-in-core-hr"></a>Core HR で間もなく公開

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>マネージャー セルフサービスのレポートのパフォーマンスに関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスがスムーズに行われることを保証できます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。

### <a name="print-performance-reviews"></a>業績の確認の印刷

従業員、マネージャー、および HR は、従業員の業績の確認を印刷できるようになります。
