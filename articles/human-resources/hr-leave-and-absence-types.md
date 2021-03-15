---
title: 休暇タイプのコンフィギュレーション
description: Dynamics 365 Human Resources で、従業員が使用できる休暇のタイプを設定します。
author: andreabichsel
manager: tfehr
ms.date: 06/01/2020
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
ms.openlocfilehash: 6b21d4d631bcdf603b38212f5f76bb78937d3d3c
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115079"
---
# <a name="configure-leave-and-absence-types"></a>休暇タイプのコンフィギュレーション

Dynamics 365 Human Resources で休暇タイプは、従業員がレポートできる休暇のタイプを定義します。 休暇タイプは、組織のニーズに応じてカスタマイズできます。 たとえば次のような休暇タイプを入力します。

- 有給休暇 (PTO)
- 無給休暇
- 有給休暇
- 病気休暇
- 病気休暇
- 家族休暇
- 短期障碍者
- 忌引き休暇

## <a name="add-a-leave-type"></a>休暇タイプの追加

1. **休暇および欠勤** のページで、**リンク** タブを選択します。

2. **設定** で、**休暇および欠勤タイプ** を選択します。

3. **新規** を選択します。

4. **タイプ** に休暇のタイプを入力し、**ワークフロー ID** からワークフローを選択して、**説明** に説明を入力します。

5. **全般** で、**カテゴリ** ドロップダウンから、**なし**、**スケジュール済**、**未スケジュール** を選択します。

6. **所得コード** ドロップダウンから、所得コードを選択します。

7. **理由コードの要否** で、理由コードの要否を選択します。 理由コードを必要とする場合は、それらを追加する必要があります。 **理由コード** で、**追加** を選択し、その横にある **有効** チェックボックスをオンにします。

8. **選択したロールにアクセスを制限** で、アクセスを制限するかどうかを選択します。 次に、**この休暇タイプに対するセキュリティ ロール** でセキュリティ ロールを選択します。 セキュリティ ロールは、この手順のはじめで説明した **ワークフロー ID** で選択したワークフローで定義されています。

9. **カレンダーの色** で、この休暇タイプの休暇と欠勤カレンダーに表示する色を選択します。 

10. **保留関係** で、この休暇タイプで別の休暇タイプを保留にするか、別の休暇タイプで保留にするかを選択します。 保留中の休暇タイプで休暇申請を行うと、保留済み休暇タイプに対して休暇の停止が自動的に作成されます。 

10. **保存** を選択します。

## <a name="configure-leave-type-rules"></a>休暇タイプ ルールの構成

1. 休暇タイプの丸めオプションを設定します。 オプションには、**なし**、**上**、**下**、**四捨五入** があります。 休暇タイプの丸めの精度を設定することもできます。

2. 休暇タイプに **休日の修正** を設定します。 このオプションを選択すると、Human Resources は作業日に含まれる休日の数を使用して、休暇タイプに対する休暇の見越計上の方法を決定します。 たとえば、クリスマスの日が月曜に当たる場合、Human Resources は、見越計上を処理するときに休暇タイプから 1 日を減算します。

   休日は作業時間カレンダーで設定します。 詳細については、[作業時間カレンダーを作成する](hr-leave-and-absence-working-time-calendar.md)を参照してください
   
 3. 休暇タイプに **繰越休暇タイプ** を設定します。 このオプションを選択すると、繰越残日数は指定された休暇タイプに転送されます。 繰越休暇タイプも、休暇および不就業プランに含める必要があります。 
 
 4. 休暇タイプの **有効期限ルール** を定義します。 このオプションを設定すると、日数または月数の単位を選択して、有効期限の期間を設定できます。 有効期限ルールの有効日を設定することもできます。 有効期限の時点で存在する休暇残高は、休暇タイプから差し引かれ、休暇残高に反映されます。 
 
 
## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇および欠勤計画の作成](hr-leave-and-absence-plans.md)
- [作業時間カレンダーの作成](hr-leave-and-absence-working-time-calendar.md)
- [休暇の中断](hr-leave-and-absence-suspend-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]