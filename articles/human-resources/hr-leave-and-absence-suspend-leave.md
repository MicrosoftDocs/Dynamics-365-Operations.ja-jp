---
title: 休暇の保留
description: Dynamics 365 Human Resources で従業員の休暇を保留できます。
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805263"
---
# <a name="suspend-leave"></a>休暇の中断

>[!Important]
>この記事で説明した機能は、現在スタンドアロンの Dynamics 365 Human Resources の顧客が利用できます。 Finance のリリース 10.0.26 以降に、Finance インフラストラクチャの今後のリリースで、一部またはすべての機能を使用できます。

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

従業員の休暇を保留して、選択した休暇タイプの処理から発生する休暇を停止することができます。

## <a name="suspend-leave-and-absence-for-an-employee"></a>従業員の休暇および欠勤を中断する

1. 従業員のレコードで、**休暇** を選択します。

2. **休暇の中断** を選択します。

3. **新規** を選択します。

4. **休暇の見越計上の中断** ダイアログ ボックスで、中断の **開始日** および **終了日** と共に **休暇タイプ** を選択します。

5. 必要に応じて、中断の **コメント** を追加できます。 

従業員の休暇が中断されている間に見越計上が処理された場合、中断された休暇タイプの見越計上は行われません。

> [!NOTE]
> 休暇申請で時間休の申請が保留されますが、時間休の申請で休暇申請が保留されることはありません。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md)
- [休暇計画の累計](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
