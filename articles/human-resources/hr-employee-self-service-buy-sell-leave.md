---
title: 休暇の売買
description: このトピックでは、Dynamics 365 Human Resources で休暇の売買申請を提出する方法について説明します。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 695840516849dcfeb69895f6808d828d5878c59b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688179"
---
# <a name="buy-and-sell-leave"></a>休暇の売買


>[!Important]
>このトピックで説明した機能は、現在スタンドアロンの Dynamics 365 Human Resources の顧客が利用できます。 Finance のリリース 10.0.26 以降に、Finance インフラストラクチャの今後のリリースで、一部またはすべての機能を使用できます。

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

休暇の売買申請ワークフローが失敗した場合、**EssLeaveBuySellRequestApprover** 権限を持つユーザーは、すべての休暇の売買申請のメッセージ ログを確認することができます。 これを行うには、**休暇と欠勤 > リンク > 休暇売買申請 > メッセージ ログ** (左上) に移動します。 **メッセージ ログ** には、トランザクションがどのように処理されたか、また関連付けられているワークフロー履歴がユーザーに表示されます。


## <a name="see-also"></a>参照

[休暇の概要](hr-leave-and-absence-overview.md)</br>
[休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
