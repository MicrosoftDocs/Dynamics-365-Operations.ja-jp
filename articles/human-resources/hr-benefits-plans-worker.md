---
title: 作業者の福利厚生計画の作成
description: この記事では、Microsoft Dynamics 365 Human Resources で、作業者の給付金プランを作成、選択、および確認する方法について説明します。
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 688382b68ead73b496fd80fb5967e243611d9507
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895963"
---
# <a name="create-worker-benefit-plans"></a>作業者の福利厚生計画の作成

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources で作業者の給付金プランを作成して、従業員の給付金プランを選択および給付金プランの選択を確認することができます。 通常、従業員は従業員のセルフ サービスを使用して給付金プランを選択し、給付金プランの管理者はその選択を確認します。 

1. **給付金管理** ワーク スペースの **プラン** で、**作業者の給付金プラン** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | 期間 | プラン クイック タブでプランをフィルタ処理するために使用する給付金期間を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 たとえば、2015 という名前で作成した期間を選択して、2015 に対して給付金登録のすべての選択を確認します。 |
   | ワーカー | プラン クイック タブでプランをフィルター処理するために使用する作業者を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 法人エンティティ | プラン クイック タブでプランをフィルター処理するために使用する法人を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 補償オプション | プラン クイック タブでプランをフィルタ処理するために使用する補償オプションを指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 既定 | 既定のプランであるかどうかに基づいて、給付金プランをフィルター処理します。 プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | ステータス | それらの状態に基づいて、給付金プランをフィルター処理します。 プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 確認書 | プラン クイック タブでプランをフィルター処理するために使用する確認状態を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 取消 | プラン クイック タブでプランをフィルター処理するために使用する削除状態を指定します。プランをフィルター処理して、すべてのプラン レコードのサブセットを選択し、そのサブセットを確認できるようにします。 |
   | 有効な日付フィルター | 有効期限が切れているか、有効になっているか、または将来有効になるかに基づいて、プランをフィルター処理します。 プラン クイック タブに表示するプランに対応するチェック ボックスを選択します。 |
   | 計画 | プラン クイック タブには、指定したフィルター基準を満たすプランが表示されます。 HR スタッフによって設定された関連コンフィギュレーション オプションと、従業員によって選択された登録の選択は、各行に含まれています。 修飾フィールドでは、プランの選択に検証の競合があるかどうかを指定します。 |

4. **保存** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
