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
# <a name="buy-and-sell-leave"></a><span data-ttu-id="e32a7-103">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="e32a7-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e32a7-104">Dynamics 365 Human Resources では、会社が設定した [購入と売却] のポリシーに基づいて、[休暇の購入] および [売却] の要求を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="e32a7-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="e32a7-105">休暇購入の申請</span><span class="sxs-lookup"><span data-stu-id="e32a7-105">Request to buy leave</span></span>

1. <span data-ttu-id="e32a7-106">**従業員セルフ サービス** ワークスペースで、**休暇残日数** タイルで **休暇購入の申請** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="e32a7-107">**休暇のタイプ** を追加し、購入したい休暇の金額を **金額** に入力します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="e32a7-108">申請を送信する準備ができたら、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="e32a7-109">残高は、更新の前に自動的に更新されるか、または更新前に承認プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="e32a7-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="e32a7-110">これは、購入ポリシーがどのように構成されているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e32a7-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="e32a7-111">休暇売却の申請</span><span class="sxs-lookup"><span data-stu-id="e32a7-111">Request to sell leave</span></span>

1. <span data-ttu-id="e32a7-112">**従業員セルフ サービス** ワークスペースで、**休暇残日数** タイルで **休暇売却の申請** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="e32a7-113">**休暇のタイプ** を追加し、売却する休暇の金額を **金額** に入力します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="e32a7-114">申請を送信する準備ができたら、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="e32a7-115">残高は、更新の前に自動的に更新されるか、または更新前に承認プロセスが開始されます。</span><span class="sxs-lookup"><span data-stu-id="e32a7-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="e32a7-116">これは、購入ポリシーがどのように構成されているかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e32a7-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="e32a7-117">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e32a7-117">Troubleshooting</span></span> 

<span data-ttu-id="e32a7-118">休暇の売買申請ワークフローが失敗した場合、**EssLeaveBuySellRequestApprover** 権限を持つユーザーは、すべての休暇の売買申請のメッセージ ログを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="e32a7-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="e32a7-119">これを行うには、**休暇および欠勤 > リンク > すべての休暇売買申請 > メッセージ ログ** (左上) に移動します。</span><span class="sxs-lookup"><span data-stu-id="e32a7-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="e32a7-120">**メッセージ ログ** には、トランザクションがどのように処理されたか、また関連付けられているワークフロー履歴がユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e32a7-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="e32a7-121">参照</span><span class="sxs-lookup"><span data-stu-id="e32a7-121">See also</span></span>

[<span data-ttu-id="e32a7-122">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="e32a7-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="e32a7-123">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="e32a7-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
