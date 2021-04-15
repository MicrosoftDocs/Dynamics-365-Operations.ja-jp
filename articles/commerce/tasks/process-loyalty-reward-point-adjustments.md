---
title: ロイヤルティ報酬ポイント調整の処理
description: この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。
author: scott-tucker
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eae943985cc2bd706c0c3c4ec7b0470e3a54bff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802626"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="0f355-103">ロイヤルティ報酬ポイント調整の処理</span><span class="sxs-lookup"><span data-stu-id="0f355-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f355-104">この手順では、ロイヤルティ カード情報を検索し、ロイヤルティ報酬ポイントを調整する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0f355-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="0f355-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="0f355-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="0f355-106">このタスクはコマース工程マネージャー ロールまたは顧客サービス マネージャ ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="0f355-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="0f355-107">[ロイヤルティ カード] に移動</span><span class="sxs-lookup"><span data-stu-id="0f355-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="0f355-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="0f355-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0f355-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0f355-110">[カード トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-110">Click Card transactions.</span></span>
    * <span data-ttu-id="0f355-111">このページでは、選択したロイヤルティ カードのすべてのロイヤルティ トランザクションを確認できます。</span><span class="sxs-lookup"><span data-stu-id="0f355-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="0f355-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0f355-112">Close the page.</span></span>
6. <span data-ttu-id="0f355-113">[カードの調整] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="0f355-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-114">Click New.</span></span>
8. <span data-ttu-id="0f355-115">[報酬ポイント] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0f355-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="0f355-116">[金額または数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f355-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="0f355-117">正の金額または負の金額を使用して、ロイヤルティ カードにポイントを追加、または削除できます。</span><span class="sxs-lookup"><span data-stu-id="0f355-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="0f355-118">[ロイヤルティ プログラム] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0f355-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="0f355-119">[コメント] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f355-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="0f355-120">[調整の転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="0f355-121">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-121">Click Yes.</span></span>
14. <span data-ttu-id="0f355-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0f355-122">Close the page.</span></span>
    * <span data-ttu-id="0f355-123">通常、 [報酬のポイントの集計] タブの報酬ポイント調整の結果を表示するには、この時点でページを更新します。しかし、タスク ガイドとしてこれを実行している場合、更新するとタスク ガイドが終了してしまうので、今すぐ更新しないでください。</span><span class="sxs-lookup"><span data-stu-id="0f355-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="0f355-124">[カード トランザクション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f355-124">Click Card transactions.</span></span>
16. <span data-ttu-id="0f355-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0f355-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]