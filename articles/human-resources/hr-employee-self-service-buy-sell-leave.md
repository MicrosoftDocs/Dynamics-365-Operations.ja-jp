---
title: 休暇の売買
description: Dynamics 365 Human Resources では、会社が設定した [購入と売却] のポリシーに基づいて、[休暇の購入] および [売却] の要求を送信することができます。
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271491"
---
# <a name="buy-and-sell-leave"></a>休暇の売買

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources では、会社が設定した [購入と売却] のポリシーに基づいて、[休暇の購入] および [売却] の要求を送信することができます。  

## <a name="request-to-buy-leave"></a>休暇購入の申請

1. **従業員セルフ サービス** ワークスペースで、**休暇残日数** タイルで **休暇購入の申請** を選択します。 

2. **休暇のタイプ** を追加し、購入したい休暇の金額を **金額** に入力します。 

3. 申請を送信する準備ができたら、**送信** を選択します。 

残高は、更新の前に自動的に更新されるか、または更新前に承認プロセスが開始されます。 これは、購入ポリシーがどのように構成されているかによって異なります。

## <a name="request-to-sell-leave"></a>休暇売却の申請

1. **従業員セルフ サービス** ワークスペースで、**休暇残日数** タイルで **休暇売却の申請** を選択します。 

2. **休暇のタイプ** を追加し、売却する休暇の金額を **金額** に入力します。 

3. 申請を送信する準備ができたら、**送信** を選択します。

残高は、更新の前に自動的に更新されるか、または更新前に承認プロセスが開始されます。 これは、購入ポリシーがどのように構成されているかによって異なります。


## <a name="troubleshooting"></a>トラブルシューティング 

休暇の売買申請ワークフローが失敗した場合、**EssLeaveBuySellRequestApprover** 権限を持つユーザーは、すべての休暇の売買申請のメッセージ ログを確認することができます。 これを行うには、**休暇および欠勤 > リンク > すべての休暇売買申請 > メッセージ ログ** (左上) に移動します。 **メッセージ ログ** には、トランザクションがどのように処理されたか、また関連付けられているワークフロー履歴がユーザーに表示されます。


## <a name="see-also"></a>参照

[休暇の概要](hr-leave-and-absence-overview.md)</br>
[休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
