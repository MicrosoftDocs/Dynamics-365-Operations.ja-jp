---
title: 雇用されていない作業者
description: 将来雇用、現職、または過去の職歴が存在しない作業者は、雇用されていない作業者フォームに表示されます。
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71cb119e533e64b14badf65f55e8c4d5aa4c4b2f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356587"
---
# <a name="workers-without-employment"></a>雇用されていない作業者

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

将来雇用、現職、または過去の職歴が存在しない作業者は、**雇用されていない作業者** フォームに表示されます。 この状態を持つ作業者は、雇用レコードのない作業者をインポートする場合や、**作業者 > 雇用履歴** を使用して作業者の雇用を削除する場合に表示されます。

既定では、**雇用されていない作業者** フォームは次のロールに使用できます。

- 人事管理アシスタント
- 人事管理マネージャー
- 採用担当者
- 報酬と給付金のマネージャー
- 給与管理者
- 給与マネージャー
- トレーニング マネージャー

**雇用されていない作業者** リストで、一覧表示された個人を削除できます。 既定では、この権限は人事管理アシスタントのロールに与えられます。 この権限は、次の手順で他のロールにも付与できます。

1. **システム管理** を選択し、**セキュリティの構成** を選択します。

2. **権限** タブで、**権限** リストを **作業者の管理** にフィルター処理します。

   [![特権リストのフィルター処理。](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. **参照** 列で、**メニュー項目の表示** を選択します。

4. **メニュー項目の表示** で、**HcmWorkersWithoutEmployment** を選択します。

   [![フォームの選択。](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. **削除** のアクセス許可を **付与** に設定します。

6. **未公開のオブジェクト** タブを選択します。

7. **すべて公開** を選択します。

   [![変更の公開。](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]