---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 9 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 99a7e6130d45229011a185087d4872fe34b8224a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897629"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 9 日)

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

### <a name="coming-soon-in-attract"></a>Attract で間もなく公開

#### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの**承認**セクションに表示されます。 承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2374 に適用されます。

### <a name="platform-update-28-for-finance-and-operations"></a>Finance and Operations のプラットフォーム更新プログラム 28

Finance and Operations のプラットフォーム更新プロフラム 28 の詳細については、[Dynamics 365 Finance and Operations プラットフォーム更新プロフラム 28 (2019 年 7 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28) を参照してください。

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Common Data Service のカスタム フィールドに対するエンティティのサポート 

次のエンティティは、カスタム フィールドをサポートします。 

- **固定報酬プラン**
- **報酬基準点設定**
- **報酬基準点設定ライン**
- **給与所得コード**
- **支払期間**
- **固定報酬イベント**
- **報酬グリッド**

Talent で更新されたすべてのエンティティを表示するには

1. **システム管理**を選択して**リンク**を選択し、**Common data service の構成**を選択します。
2. **CDS エンティティ名** ドロップダウン メニューを選択します。 一覧表示されたエンティティすべては最新バージョンです。 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Common Data Service の作業者エンティティに追加された姓名

**姓名**フィールドは、**作業者**エンティティに追加されました。

### <a name="full-time-equivalent-higher-than-10"></a>1.0 を超えるフルタイム相当

職位のすべてのフルタイム従業員に 1.0 を超える値が入力された場合、警告が表示されるようになりました。 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>雇用が将来の日付の場合、作業者ページに警告は表示されません。

**人事管理**ワークスペースの**既存の従業員**のリストから**作業者**に移動する場合、将来の雇用が存在することを示すメッセージは表示されなくなります。 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Talent で業務プロセスを削除することはできません。

業務プロセスは、**業務プロセス** ワークスペースで削除することができるようになりました。

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>見越計上期間の時点で残高を使用している場合、見越計上のない計画について、休暇の残高にゼロは表示されません。

見越計上なしで設定された計画に残高を表示できるようになりました。

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを**実稼働**または**サンドボックス**のどちらかに指定することができます。 **サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。 既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

### <a name="restrict-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまな種類の休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、HR によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

## <a name="coming-soon-in-core-hr"></a>Core HR で間もなく公開

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>マネージャー セルフサービスの業績に関する追加情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行により、従業員と共同管理をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。 

### <a name="entities-supporting-custom-fields"></a>カスタム フィールドをサポートするエンティティ

Common Data Service のカスタムフィールドに対して、次のエンティティが有効になります。 

- **休暇タイプ**
- **作業者の銀行口座**
- **作業カレンダー**
