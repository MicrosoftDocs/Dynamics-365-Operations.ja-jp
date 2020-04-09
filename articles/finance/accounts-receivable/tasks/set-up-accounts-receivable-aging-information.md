---
title: 売掛金勘定のエイジング情報の設定および生成
description: このガイドでは、エイジング期間の定義、顧客残高のエイジング、および [指定の期間に達している残高] リストと [回収] ページでの残高表示の設定方法を説明します。
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3c1ec73da27a08aa7a6cd859d1adac772916e4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140182"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="da89e-103">売掛金勘定のエイジング情報の設定および生成</span><span class="sxs-lookup"><span data-stu-id="da89e-103">Set up and generate accounts receivable aging information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da89e-104">このガイドでは、エイジング期間の定義、顧客残高のエイジング、および [指定の期間に達している残高] リストと [回収] ページでの残高表示の設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="da89e-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="da89e-105">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="da89e-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="da89e-106">エイジング期間の定義の作成</span><span class="sxs-lookup"><span data-stu-id="da89e-106">Create an aging period definition</span></span>
1. <span data-ttu-id="da89e-107">**ナビゲーション ウィンドウ > モジュール > 与信および回収 > 設定 > エイジング期間の定義**に移動します。</span><span class="sxs-lookup"><span data-stu-id="da89e-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Aging period definitions**.</span></span>
2. <span data-ttu-id="da89e-108">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="da89e-108">Click **New**.</span></span>
3. <span data-ttu-id="da89e-109">**エイジング期間の定義**フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="da89e-109">In the **Aging period definition** field, type a value.</span></span>
4. <span data-ttu-id="da89e-110">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="da89e-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="da89e-111">**下に追加**をクリックし、新しいエイジング期間を挿入します。</span><span class="sxs-lookup"><span data-stu-id="da89e-111">Click **Add below** to insert a new aging period.</span></span>
6. <span data-ttu-id="da89e-112">**期間**フィールドで、エイジング レポートに表示する説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="da89e-112">In the **Period** field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="da89e-113">**単位**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="da89e-113">In the **Unit** field, enter a number.</span></span>
8. <span data-ttu-id="da89e-114">**間隔**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-114">In the **Interval** field, select an option.</span></span> <span data-ttu-id="da89e-115">元帳期間は、元帳のカレンダーの期間に一致します。</span><span class="sxs-lookup"><span data-stu-id="da89e-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="da89e-116">日付タイプの間隔は、日、週、月、四半期、年で定義します。</span><span class="sxs-lookup"><span data-stu-id="da89e-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="da89e-117">無制限の場合、最初または最後の期間かに応じて、直前の期間の前または後のすべてのトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="da89e-118">**エイジング インジケーター** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-118">In the **Aging indicator** field, select an option.</span></span>
10. <span data-ttu-id="da89e-119">グリッドの上部で期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="da89e-120">最も古いエイジング期間の定義の説明を更新</span><span class="sxs-lookup"><span data-stu-id="da89e-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="da89e-121">**期間**フィールドで、エイジング期間の新しい説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="da89e-121">In the **Period** field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="da89e-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="da89e-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="da89e-123">残高のエイジング</span><span class="sxs-lookup"><span data-stu-id="da89e-123">Age the balances</span></span>
1. <span data-ttu-id="da89e-124">**与信および回収 > 定期処理のタスク > 指定の期間に達している顧客残高**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="da89e-124">Go to **Credit and collections > Periodic tasks > Age customer balances**.</span></span>
2. <span data-ttu-id="da89e-125">**エイジング期間の定義**フィールドで、作成したエイジング期間の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-125">In the **Aging period definition** field, select the aging period definition that you created.</span></span>
    + <span data-ttu-id="da89e-126">各エイジング期間の定義に対して、有効なスナップショットを 1 つずつ持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="da89e-126">You can have one active snapshot for each aging period definition.</span></span>  
    + <span data-ttu-id="da89e-127">すべての顧客が既定で処理されます。</span><span class="sxs-lookup"><span data-stu-id="da89e-127">All customers are processed by default.</span></span> <span data-ttu-id="da89e-128">この選択を使用すると、顧客の回収プールを 1 つ計算できます。</span><span class="sxs-lookup"><span data-stu-id="da89e-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    + <span data-ttu-id="da89e-129">エイジングに対して使用するトランザクションから日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-129">Select the date from the transaction that you will use for the aging.</span></span>  
    + <span data-ttu-id="da89e-130">エイジングに対する「現在」の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="da89e-131">既定では今日ですが、このフィールドを [選択した日付] に変更すると、使用する日付を選べます。</span><span class="sxs-lookup"><span data-stu-id="da89e-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="da89e-132">バッチ処理のために、今日の日付を使用します。</span><span class="sxs-lookup"><span data-stu-id="da89e-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="da89e-133">**会社**範囲を展開します。</span><span class="sxs-lookup"><span data-stu-id="da89e-133">Expand the **Company** range.</span></span> <span data-ttu-id="da89e-134">スナップショットに含む会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="da89e-135">現在の会社が既定で選択されます。</span><span class="sxs-lookup"><span data-stu-id="da89e-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="da89e-136">**OK** をクリックしてスナップショットを処理します。</span><span class="sxs-lookup"><span data-stu-id="da89e-136">Click **Ok** to process the snapshot.</span></span> <span data-ttu-id="da89e-137">これには時間がかかるため、スライダーが消えるまでしばらく待ち、メッセージ センターからのメッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="da89e-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="da89e-138">[指定の期間に達している残高] リストと [回収] ページに残高を表示します。</span><span class="sxs-lookup"><span data-stu-id="da89e-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="da89e-139">**与信および回収 > 回収 > 指定の期間に達している残高**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="da89e-139">Go to **Credit and collections > Collections > Aged balances**.</span></span> <span data-ttu-id="da89e-140">リスト ページには、顧客の残高が表示されます。</span><span class="sxs-lookup"><span data-stu-id="da89e-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="da89e-141">エイジング アイコンが、最も古いトランザクションのエイジング期間を示します。</span><span class="sxs-lookup"><span data-stu-id="da89e-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="da89e-142">残高を持つ顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="da89e-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="da89e-143">エイジングした残高を表示するには、**エイジング情報**ボックスの領域を展開します。</span><span class="sxs-lookup"><span data-stu-id="da89e-143">Expand the **Aging fact** box area to view the aged balances.</span></span> <span data-ttu-id="da89e-144">ファクト ボックスのエイジング期間の定義は、パラメータで指定されている既定のエイジング期間の定義から取得されます。</span><span class="sxs-lookup"><span data-stu-id="da89e-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="da89e-145">[収集] メニューを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="da89e-145">You can change it using the Collect menu.</span></span>  

