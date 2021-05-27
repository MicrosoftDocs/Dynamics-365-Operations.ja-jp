---
title: 給付金管理ワークスペース
description: このトピックでは、Dynamics 365 Human Resources の給付金管理ワークスペースについて説明します。
author: andreabichsel
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a2325da54b8d47ef39d0aacb5dac87107ebdd5bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019566"
---
# <a name="benefits-management-workspace"></a>給付金管理ワークスペース

[!include [applies to](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

このトピックでは、Dynamics 365 Human Resources の **給付金管理** ワークスペースについて説明します。

> [!NOTE]
> **給付金管理** ワークスペースを表示するには、まず機能管理の **(プレビュー) 給付金管理ワークスペース** 機能を有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](../hr-admin-manage-features.md)を参照してください。<br><br>![給付金管理ワークスペースを有効にする](./media/hr-benefits-management-workspace-enable.png)

**給付金管理** ワークスペースを使用すると、確認が必要な福利厚生項目をすばやく表示できます。 このページでは、次のものを確認できます。

- アクションを待っている品目の合計
- 選択が未確認の作業者
- 最近福利厚生に加入した作業者
- 将来のライフ イベントを持つ作業者
- 登録されていない新規採用
- 有効なライフ イベントを持つ作業者
- プランが未選択で、オープン登録を行っている作業者

![給付金管理ワークスペース](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>アクション項目の表示

タイルまたはタブを選択して、アクション項目を表示できます。タブを選択すると、ワークスペース ページの右側で作業者を表示および選択できます。

![アクション項目](./media/hr-benefits-management-workspace-action-items.png)

タイルを選択した場合は、その領域のページに移動します。 たとえば、これらのタイルのいずれかを選択すると、**作業者の給付金プラン** ページが表示され、次の操作を実行する必要がある従業員に対してフィルター処理されます。

- **未確認の選択**
- **計画がチェック アウトされていない登録を開く**
- **給付金に登録済み**
- **新規採用が未登録**

![作業者給付金計画](./media/hr-benefits-management-workspace-plans.png)

**有効なライフ イベント** または **将来のライフ イベント** タイルを選択すると、有効なライフ イベントまたは将来のライフ イベントのリストが表示されます。

![ライフ イベント](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>処理中

登録の適格性、ライフ イベント、またはレート変更の更新を処理するには、ナビゲーション バーで適切な項目を選択します。

![処理中](./media/hr-benefits-management-workspace-processing.png)

プロセス結果を表示するには、ページで **プロセス結果** を選択します。

![プロセス結果](./media/hr-benefits-management-workspace-process-results.png)

給付金処理の詳細については、以下を参照してください。

- [登録適格性の処理](hr-benefits-process-enrollment-eligibility.md)
- [ライフ イベントの変更の処理](hr-benefits-process-life-event-changes.md)
- [ライフ イベントの適格性の処理](hr-benefits-process-life-event-eligibility.md)
- [ライフ イベントの処理](hr-benefits-process-life-events.md)
- [レート変更の処理](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>期間の変更

異なる給付金の期間を表示するには、**期間** ドロップダウンから選択します。

![期間の変更](./media/hr-benefits-management-workspace-period.png)

## <a name="view-more-options"></a>その他のオプションの表示

詳細情報および実行できるアクションを表示するには、**リンク** を選択します。

![リンク](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>参照

[福利厚生の管理の概要](hr-benefits-management-overview.md)