---
title: 休暇ポリシーの売買管理
description: Dynamics 365 Human Resources で従業員が休暇を売買できるようにすることができます。
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 89563204cf1423ddce47d7bacace8f14edf87005
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115999"
---
# <a name="manage-buy-and-sell-leave-policies"></a>休暇の売買ポリシーの管理

休暇の売買ポリシーを作成することで、従業員が休暇の購入や売却ができるようにすることができます。 これらのポリシーを構成して、承認にワークフローを使用したり、最大金額とレートを設定したり、購買と販売のレートを設定したりすることができます。 

## <a name="enable-employees-to-buy-and-sell-leave"></a>従業員が休暇を売買できるようにする

1. **休暇および欠勤パラメーター** ページで、**従業員の休暇の購入を許可する** と **従業員の休暇の売却を許可する** に対して **はい** を選択します。

## <a name="create-a-buy-and-sell-leave-policy"></a>休暇の売買ポリシーの作成

1. **休暇および欠勤** のページで、**リンク** タブを選択します。 

2. **休暇ポリシーの売買** を選択します。

3. **新規** を選択します。

4. **休暇ポリシーの売買** で ポリシーの **名前** と **説明** を入力します。 

5. **ポリシー タイプ** を選択します。 

   利用可能なポリシー タイプは、**金額** と **週あたりの時間数** です。 **金額** を選択して、従業員が売買できる上限金額の **固定金額** を入力します。 **週あたりの時間数** を選択した場合は、従業員に割り当てられた作業時間カレンダーで定義されている作業時間が、ポリシーの上限金額を決定するために使用されます。 

6. ポリシーに対して **開始日** と **終了日** を選択します。 休暇の売買申請は、この時間枠でのみ提出することができます。 

7. ポリシーで使用する **ワークフロー ID** を選択します。 すべての売買の申請では、このワークフローを使用してレビューと承認が行われます。 

8. **ポリシーの購入** で、**フルタイム相当** (FTE) を選択すると、従業員の職位で定義された FTE に基づいて上限金額を比例配分します。 ポリシー タイプが **金額** の場合は、**上限固定金額** を入力します。 

9. **追加** を選択して、休暇を購入する従業員の休暇タイプを追加します。 ポリシーには複数の休暇タイプを追加できます。 

10. 休暇タイプに **勤続月数** を入力して、異なる勤続月数で従業員が購入できる上限金額を決定できるようにします。 

11. 休暇タイプに **上限金額** を入力します。 

12. 従業員が休暇を購入する **レート** を入力します。 

13. 必要に応じて、休暇を購入するために使用する **所得コード** を入力します。 

14. 必要に応じて、休暇タイプの上限金額を決定するために FTE を使用するかどうかを設定します。 

15. 売却ポリシーを作成するには、**売却ポリシー** に記載の手順8 から 14 を実行してください。 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>休暇および不就業プランに対する、休暇ポリシーの売買を追加する

1. **休暇** ページで、休暇および不就業プランを選択します。

2. **ルール** で **休暇ポリシーの売買** を選択します。

## <a name="see-also"></a>参照

[休暇の概要](hr-leave-and-absence-overview.md)</br>
[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md)</br>
[休暇計画の累計](hr-leave-and-absence-accrue.md)</br>
[休暇の売買](hr-employee-self-service-buy-sell-leave.md)

