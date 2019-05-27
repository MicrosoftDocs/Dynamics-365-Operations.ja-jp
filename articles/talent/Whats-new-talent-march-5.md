---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 3 月 5 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4ad32ef71c87f52e59959d80c21ae7fcd6d6524
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518499"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a>Dynamics 365 for Talent の新機能および変更された機能 (2019 年 3 月 5 日)

[!include [banner](includes/banner.md)]

このトピックでは、 Talent の新機能または変更された機能について説明します

## <a name="changes-in-attract"></a>Attract の変更

### <a name="extending-option-sets-in-attract"></a>Attract のオプション セットの拡張

Attract には、Common Data Service 内のオプション セットである複数のフィールドがあります。 **不採用**理由フィールド、**雇用タイプ**フィールド、および**勤続タイプ**フィールドをはじめとするオプション セットを拡張するための新しい機能が導入されました。

> [!IMPORTANT]
> LinkedIn 機能へのジョブ求人転記には、**ジョブの詳細**ページの**雇用タイプ**および**勤続タイプ**フィールドの使用が求められます。 これらのフィールドの既定値は LinkedIn でサポートされ、ジョブが転記されるときに表示されます。 LinkedIn にジョブ求人を転記していて、これらのフィールドの既存のオプション セット値を変更した場合、ジョブ求人は転記されますが、LinkedIn はカスタム**雇用タイプ**および**勤続タイプ**の値を表示しません。

## <a name="changes-in-onboarding"></a>オンボードの変更

### <a name="private-preview-for-onboard-teams"></a>Onboard チームのプライベート プレビュー
組織全体でテンプレートを簡単に共有して共同作業できるようになりました。 詳細については、[Onboard チームを使用して、組織全体のベスト プラクティスを共有する](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams) を参照してください。

### <a name="private-preview-for-assignee-placeholders"></a>割り当て先のプレース ホルダーのプライベート プレビュー
活動を個人の代わりにロールに割り当てることにより、テンプレートを強化できます。 ロールは、ガイドの作成時に個人に割り当てられます。 詳細については、[活動をロールに割り当てることによってガイド管理を合理化する](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles) を参照してください。

## <a name="changes-in-core-hr"></a>Core HR の変更
**ビルド 8.1.2178**

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a>HR または明細行のマネージャーが休暇申請を送信または更新するときに、ワークフローを自動承認またはワークフローに従うようにコンフィギュレーションします。
従業員のマネージャーまたは HR によって提出された場合に休暇要求が自動的に承認されるように、新しいワークフローの条件が追加されました。 ワークフローでのこの自動承認を達成するための 1 つの方法は、ワークフローの承認で自動アクションを有効にすることです。

追加された条件には以下が含まれます:

- 送信者 - 要求をワークフローに送信したユーザーのシステムのユーザー ID を評価するために使用します。
- 次のユーザーの代理で送信 - 休暇要求が要求に関連付けられている作業者の代理として送信されたかどうかを評価するために使用されます。
- 人事管理が送信 - 要求をワークフローに送信したシステム ユーザーが人事管理ロールに属しているかどうかを評価するために使用されます。
- マネージャーが送信 - ワークフローに休暇要求を送信したユーザーが要求に関連付けられている作業者の明細行の階層マネージャーかどうかを評価するために使用されます。

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a>従業員の固定報酬を将来の職位の割り当てのために有効化する
従業員が将来の開始日で組織に参加するのは一般的です。 この変更により、将来の職位の割り当てを持つ従業員に対する固定報酬の定義が有効化されます。

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a>職位の編集時に職位給与フィールドが空白になる
この変更により、既存の職位の変更を要求するときに、給与フィールドは既定で現在の値になります。

### <a name="other-miscellaneous-bug-fixes"></a>その他の雑費のバグ修正
このリリースには、他のマイナーなバグ修正が含まれています。

### <a name="upgrade-to-common-data-service"></a>Common Data Service へのアップグレード
Common Data Service へのアップグレードの期限が近づいています。 データベースをアップグレードする必要があるかどうかを決定するために、PowerApps 管理者センターにサインインします。 期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。

## <a name="coming-soon"></a>間もなく公開

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)
多くの組織で、報酬および福利厚生のマネージャーは、経営幹部または地域の従業員のレコードなど、特定の報酬レコードにのみアクセスできます。 この変更により、組織内のさまざまな従業員数の報酬プランを管理および維持できます。 固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。 与えられたアクセス権を持つロールのみが、それらの従業員の報酬を処理できます。

###  <a name="platform-update-24"></a>プラットフォーム update 24
プラットフォーム更新プログラム 24 の詳細については、[Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24) を参照してください。
