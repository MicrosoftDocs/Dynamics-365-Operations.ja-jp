---
title: 休暇パラメーターのコンフィギュレーション
description: Dynamics 365 Human Resources で休暇のための人事管理パラメーターを定義します。
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997104"
---
# <a name="configure-leave-and-absence-parameters"></a>休暇パラメーターのコンフィギュレーション

Dynamics 365 Human Resources で休暇計画を設定する前に、下記を含むすべての関連する人事管理パラメーターの設定を確認することをお勧めします。

- 休暇申請の番号順序
- 育児介護休業法 (FMLA) 設定
- 休暇申請のための従業員セルフ サービス設定
- 休暇および欠勤パラメーター

## <a name="view-and-change-human-resources-parameters"></a>人事管理パラメーターの表示および変更

1. **休暇および欠勤** のページで、**リンク** タブを選択します。

2. **設定** で、**人事管理パラメーター** を選択します。

3. **番号順序** タブで、**休暇申請 ID** のための **番号順序コード** を確認し、必要に応じて変更します。 この設定により、休暇申請に自動的に ID を割り当てるために使用される順序が決まります。

4. **FMLA** タブで、FMLA の設定を確認し必要に応じて変更します。

5. **従業員セルフ サービス** タブで、マネージャーが従業員に代わって休暇申請を入力できるようにするかどうかを指定します。

7. **保存** を選択します。

>[!IMPORTANT]
>現在、会社全体の休暇と欠勤の表示はプレビューで表示します。 休暇と欠勤のオプションを表示するには、**サンドボックス** 環境で有効にする必要があります。 プレビュー機能を有効にする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

## <a name="view-and-change-human-resources-shared-parameters"></a>人事管理共有パラメーターの表示および変更

1. **人事管理** ページで、**リンク** タブを選択します。

2. **設定** で、**人事管理共有パラメーター** を選択します。

3. **詳細アクセス** タブで、**会社全体で休暇表示を有効にする** で **はい** を選択して、会社全体で休暇を表示できるようにします。

4. **保存** を選択します。

## <a name="view-and-change-leave-and-absence-parameters"></a>休暇と欠勤のパラメータの表示および変更

1. **休暇および欠勤** のページで、**リンク** タブを選択します。

2. **設定** で、**休暇および欠勤パラメーター** を選択します。

3. **一般** タブで、次パラメーターを設定します:
 
    - **休暇および欠勤の単位** を時間数または日数に設定します。 日数の場合、**半日定義を有効にする** を選択して、従業員が休暇申請の 1 日の前半または後半のいずれかを選択できるようにします。 

    - **勤続月数の有効日** を選択して、勤続月数を使用して休暇計画の見越計上レートが有効になる時期を設定します。

    - **残日数の計算** を選択して、今日の残日数、または見越計上期間の残日数を表示します。 **今日現在の残日数** を選択すると、残日数には今日時点のすべての見越、調整、および申請の合計が表示されます。 **見越計上期間の時点での残日数** を選択した場合、残日数には、休暇計画の頻度で定義された見越計上期間の時点でのすべての見越、調整、申請の合計が表示されます。 

    - 繰り越し有効期限バッチジョブの開始時刻を設定します。  
    
    - **はい** を選択すると、**従業員に休暇の購入を許可する** と **従業員の休暇の売却を許可する** ことができます。 これらのオプションに対して **はい** を選択すると、休暇の購入と売却ポリシーの作成と、従業員が休暇の購入と売却の申請を送信できるようになります。

## <a name="configure-calendar-parameters"></a>カレンダー パラメーターのコンフィギュレーション

1. **休暇および欠勤** のページで、**リンク** タブを選択します。

2. **設定** で、**休暇および欠勤パラメーター** を選択します。

3. **カレンダー** タブで、カレンダーの設定を必要に応じて変更します。

4. **保存** を選択します。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
