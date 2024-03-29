---
title: 従業員の休暇の管理
description: Dynamics 365 Human Resources で従業員の休暇を管理する。
author: twheeloc
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ef671ee42848d079cf1ff9bc2328216df4e9e20
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888791"
---
# <a name="manage-employee-leave"></a>従業員の休暇の管理

>[!Important]
>この記事で説明した機能は、現在スタンドアロンの Dynamics 365 Human Resources の顧客が利用できます。 Finance のリリース 10.0.26 以降に、Finance インフラストラクチャの今後のリリースで、一部またはすべての機能を使用できます。


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

従業員の休暇は、休暇タイプで管理できます。 ここには、期限切れの休暇登録と休暇タイプの残高調整が含まれています。 

## <a name="adjust-leave-balances"></a>休暇残高の調整

1. 従業員のレコードで、**休暇** を選択します。

2. **休暇と欠勤の設定** を選択します。

3. **残高の調整** を選択します。

4. **休暇タイプ** を選択します。

5. **調整する量** を入力します。 

6. 必要に応じて **日** を選択できます。 

従業員の休暇残高を調整する際には、理由コードとコメントを含めることができます。 

これで、休暇残数にカーソルを合わせると、次の情報が表示されます。

- **利用可** – **今年度の合計** 値から、**今年度の取得** 金額を差し引いた値。
- **今年度の合計** – 年度のすべての見越計上、調整、および繰り越し。
- **今年取得した休暇** – すべての承認済休暇。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇および欠勤要求の管理](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
