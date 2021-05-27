---
title: TDS 決済プロセスの定期実行
description: このトピックでは、源泉徴収 (TDS) の定期実行について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: cfab08a4190bf51518bd4a9b445b229a5081e87d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023377"
---
# <a name="run-the-periodic-tds-settlement-process"></a><span data-ttu-id="ea1e1-103">TDS 決済プロセスの定期実行</span><span class="sxs-lookup"><span data-stu-id="ea1e1-103">Run the periodic TDS settlement process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea1e1-104">このトピックでは、源泉徴収 (TDS) の定期実行について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-104">This topic explains how to settle periodic Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="ea1e1-105">**税 \> 申告 \> 源泉徴収税 \> 源泉徴収税の支払** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-105">Go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="ea1e1-106">[![源泉徴収税の支払ダイアログボックス](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)</span><span class="sxs-lookup"><span data-stu-id="ea1e1-106">[![Withholding tax payment dialog box](./media/apac-ind-TDS-47.png)](./media/apac-ind-TDS-47.png)</span></span>

2. <span data-ttu-id="ea1e1-107">**源泉徴収税の支払** ダイアログ ボックス で、の **税タイプ** フィールドで、**TDS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-107">In the **Withholding tax payment** dialog box, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="ea1e1-108">**税勘定番号 (TAN)** フィールドで、決済プロセスを実行する税勘定番号 (TAN) を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-108">In the **Tax Account Number (TAN)** field, select the Tax Account Number (TAN) to run the settlement process for.</span></span>
4. <span data-ttu-id="ea1e1-109">**源泉徴収税コンポーネント グループ** フィールドで、決済プロセスを実行する TDS コンポーネント グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-109">In the **Withholding tax component group** field, select the TDS component group to run the settlement process for.</span></span>
5. <span data-ttu-id="ea1e1-110">**決済期間** フィールドで、決済プロセスを実行する TDS の決済期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-110">In the **Settlement period** field, select the TDS settlement period to run the settlement process for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea1e1-111">TDS 決済プロセスは、**源泉徴収税の精算期間** ページの **期間** タブ (**税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税の精算期間**) のTDS決済期間に対して設定されているすべての期間に対して実行されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-111">The TDS settlement process is run for all periods that are set up for the TDS settlement period on the **Periods** tab of the **Withholding tax settlement periods** page (**Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**).</span></span>

6. <span data-ttu-id="ea1e1-112">**開始日** フィールドで、TDS 決済プロセスの実行開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-112">In the **From date** field, select the start date to run the TDS settlement process from.</span></span>

    <span data-ttu-id="ea1e1-113">決済期間内の特定の期間については、その期間に定められた開始日を「開始日」の日付とします。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-113">For a specific period within the settlement period, the start date that is defined for the period is taken as the "from" date.</span></span> <span data-ttu-id="ea1e1-114">たとえば、TDS 決済期間には、2009 年 4 月 1 日から 4 月 30 日まで、2009 年 5 月 1 日から 5 月 31 日の 2 つの期間があります。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-114">For example, the TDS settlement period has two periods: April 1 through April 30, 2009, and May 1 through May 31, 2009.</span></span> <span data-ttu-id="ea1e1-115">**開始日** フィールドに **2009年4月6日 (2009年4月6日)** を選択した場合でも、決済プロセスは 2009 年 4 月 1 日から実行されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-115">If you select **04/06/2009** (April 6, 2009) as the start date in the **From date** field, the settlement process will still run from April 1, 2009.</span></span>

    <span data-ttu-id="ea1e1-116">**開始日** フィールドに後の期間を入力しても、決済期間内の前の期間を決済しない場合、それ以前の期間については決済は発生しません。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-116">If you enter a later period in the **From date** field, but without settling a previous period within the settlement period, the settlement won't occur for any previous periods.</span></span> <span data-ttu-id="ea1e1-117">たとえば、TDS 決済期間には、2009 年 4 月 1 日から 4 月 30 日まで、2009 年 5 月 1 日から 5 月 31 日まで、2009 年 6 月 1 日から 6 月 30 日までの 3 つの期間があります。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-117">For example, the TDS settlement period has three periods: April 1 through April 30, 2009, May 1 through May 31, 2009, and June 1 through June 30, 2009.</span></span> <span data-ttu-id="ea1e1-118">**開始日** フィールドで開始日として **2009年5月1日** (2009年5月1日) を選択した場合、決済プロセスは 2009 年 5 月 1 日から 5 月 31 日までしか実行されません。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-118">If you select **05/01/2009** (May 1, 2009) as the start date in the **From date** field, the settlement process will run only from May 1 through May 31, 2009.</span></span> <span data-ttu-id="ea1e1-119">決済は 2009 年 4 月 1 日から 4 月 30 日の間は実行されません。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-119">The settlement won't occur for April 1 through April 30, 2009.</span></span>

7. <span data-ttu-id="ea1e1-120">**開始日** フィールドで、TDS の決済トランザクションを転記する日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-120">In the **Transaction date** field, select the date to post the TDS settlement transaction.</span></span>
8. <span data-ttu-id="ea1e1-121">**源泉徴収税の支払バージョン** フィールドで、TDS の決済バージョンを選択します:</span><span class="sxs-lookup"><span data-stu-id="ea1e1-121">In the **Withholding tax payment version** field, select the TDS settlement version:</span></span>

     - <span data-ttu-id="ea1e1-122">**オリジナル** - TDS の決済プロセスを初めて実行する場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-122">**Original** – Use this option to run the TDS settlement process for the first time.</span></span> <span data-ttu-id="ea1e1-123">オリジナルの支払いバージョンは、TAN、源泉徴収票の構成要素グループ、源泉徴収票の決済期間の組み合わせに対して、TDS 決済処理を実行するために一度だけ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-123">The original payment version is used only one time to run the TDS settlement process for a combination of a TAN, a withholding tax component group, and a withholding tax settlement period.</span></span>
    - <span data-ttu-id="ea1e1-124">**最新バージョン** - 指定した期間のTDS決済処理がすでに実行されている場合、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-124">**Latest versions** – Use this option if the TDS settlement process has already been run for the specified period.</span></span> <span data-ttu-id="ea1e1-125">決済プロセスが以前に実行された後に転記された、過去日付の取引を含みます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-125">Include back-dated transactions that were posted after the settlement process was previously run for the period.</span></span> <span data-ttu-id="ea1e1-126">このオプションを使えば、何度でも決済プロセスを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-126">You can use this option to run the settlement process any number of times.</span></span>

9. <span data-ttu-id="ea1e1-127">TDS 決済プロセスを実行して勘定科目に金額を転記するには、**更新** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-127">Select the **Update** check box to run the TDS settlement process and post the amounts to the ledger accounts.</span></span> <span data-ttu-id="ea1e1-128">このチェック ボックスをオフにすると、決済プロセスは実行されず、財務エントリも生成されません。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-128">If this check box is cleared, the settlement process won't be run, and the financial entries won't be generated.</span></span>
10. <span data-ttu-id="ea1e1-129">**OK** を選択して TDS の決済プロセスを実行し、源泉徴収税の支払レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-129">Select **OK** to run the TDS settlement process and generate the withholding tax payment report.</span></span> <span data-ttu-id="ea1e1-130">決済プロセスに含まれる TDS トランザクションの状態が、**決済** ページに **決済済** として表示されます (**買掛金勘定 \> 支払 \> 仕入先支払仕訳帳** に移動し、**明細行** を選択し、**機能** を選択して、**決済** を選択します)。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-130">The status of TDS transactions that are included in the settlement process is shown as **Settled** on the **Settlement** page (go to **Accounts payable \> Payments \> Vendor payment journal**, select **Lines**, select **Functions**, and then select **Settlement**).</span></span>

### <a name="important-points"></a><span data-ttu-id="ea1e1-131">重要な点</span><span class="sxs-lookup"><span data-stu-id="ea1e1-131">Important points</span></span>

- <span data-ttu-id="ea1e1-132">決済時に源泉徴収票の構成要素グループが選択されていない場合、選択された TAN と決済期間のすべての源泉徴収票の構成要素グループに対して決済が行われます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-132">If a withholding tax component group isn't selected during the settlement process, the settlement occurs for all the withholding tax component groups for the selected TAN and settlement period.</span></span> <span data-ttu-id="ea1e1-133">**オープントランザクションの編集** ページの源泉徴収税コンポーネント グループごとに個別の明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-133">A separate line is created for each withholding tax component group on the **Open transaction editing** page.</span></span>
- <span data-ttu-id="ea1e1-134">決済プロセスは、決済期間の評価カテゴリの性質に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-134">The settlement process is based on the nature of assessee category for a settlement period.</span></span> <span data-ttu-id="ea1e1-135">評価カテゴリの性質が **会社** となっているトランザクションが決済され、**オープントランザクションの編集** ページで 1 行として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-135">Transactions where the nature of assessee category is **Company** are settled and are shown as one line on the **Open transaction editing** page.</span></span> <span data-ttu-id="ea1e1-136">評価カテゴリの性質が **会社** 以外のトランザクションが決済され、**オープントランザクションの編集** ページで 1 行として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-136">Transactions where the nature of assessee is something other than **Company** are settled and are shown as one line on the **Open transaction editing** page.</span></span>
- <span data-ttu-id="ea1e1-137">**オープン トランザクションの編集** ページに表示される決済済みの TDS 取引明細の支払期日は、**仕入先** ページで TDS 権限を持つ仕入先に対して定義された支払条件に基づいています。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-137">The due date for the settled TDS transaction lines on the **Open transaction editing** page is based on the terms of payment that are defined for the TDS authority vendor on the **Vendors** page.</span></span> <span data-ttu-id="ea1e1-138">支払条件が TDS 機関の仕入先に対して定義されていない場合は、決済期間の最終日が期日として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ea1e1-138">If the terms of payments aren't defined for the TDS authority vendor, the last day of the settlement period is shown as the due date.</span></span>
