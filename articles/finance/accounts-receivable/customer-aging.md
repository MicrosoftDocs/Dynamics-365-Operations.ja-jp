---
title: 顧客エイジング レポート
description: 顧客エイジング レポートには、日付間隔またはエイジング期間でソートされた顧客からの支払い残高が表示されます。
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974864"
---
# <a name="customer-aging-report"></a><span data-ttu-id="90dd1-103">顧客エイジング レポート</span><span class="sxs-lookup"><span data-stu-id="90dd1-103">Customer aging report</span></span> 

<span data-ttu-id="90dd1-104">**顧客エイジング**レポートには、日付間隔またはエイジング期間でソートされた顧客からの支払い残高が表示されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="90dd1-105">このレポートを生成するとき、次の既定のパラメーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="90dd1-106">これらのパラメーターを使用して、レポートに表示されるデータをフィルタリングできます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="90dd1-107">詳細については、[コレクションの設定](set-up-collections.md) 参照してください。</span><span class="sxs-lookup"><span data-stu-id="90dd1-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90dd1-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="90dd1-108">Field</span></span></p></th>
<th><p><span data-ttu-id="90dd1-109">説明</span><span class="sxs-lookup"><span data-stu-id="90dd1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-110"><strong>請求分類</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-111">レポートに含める請求分類を 1 つ以上選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="90dd1-112">**注記:** このコントロールは、<STRONG>公的機関</STRONG>のコンフィギュレーション キーが選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-113"><strong>請求分類のない取引を含める</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-114">このチェック ボックスが選択された場合、請求分類が割り当てられていないすべてのトランザクションがレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="90dd1-115">**注記:** このコントロールは、<STRONG>公的機関</STRONG>のコンフィギュレーション キーが選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-116"><strong>エイジングの時点</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-117">現在のエイジング バケットで使用される日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-118"><strong>時点の残高</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-119">表示する顧客残高の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="90dd1-120">これは、トランザクションの締日とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-121"><strong>開始日</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-122">レポートに含める最初の期間間隔またはエイジング期間内の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-123"><strong>基準</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-124">レポートの基準となる日付タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="90dd1-125"><strong>トランザクションの日付</strong> – トランザクションの転記日付。</span><span class="sxs-lookup"><span data-stu-id="90dd1-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="90dd1-126">たとえば、これは、期限の計算の基礎となる請求日である場合もあります。</span><span class="sxs-lookup"><span data-stu-id="90dd1-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="90dd1-127"><strong>期限</strong> – 支払条件に基づくトランザクションの期限。</span><span class="sxs-lookup"><span data-stu-id="90dd1-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="90dd1-128"><strong>文書日付</strong> – 期限の計算基準であるユーザー定義の文書日付。</span><span class="sxs-lookup"><span data-stu-id="90dd1-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-129"><strong>エイジング期間の定義</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-130">エイジング期間の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-130">Select an aging period definition.</span></span> <span data-ttu-id="90dd1-131">エイジング期間の定義を選択した場合、<strong>サイクル間隔</strong>フィールドは使用されません。</span><span class="sxs-lookup"><span data-stu-id="90dd1-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="90dd1-132">エイジング期間が 6 を超えるエイジング期間の定義は、レポートの印刷に使用できません。</span><span class="sxs-lookup"><span data-stu-id="90dd1-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="90dd1-133">**注記:** エイジング期間は、<STRONG>エイジング期間の定義</STRONG>ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-134"><strong>エイジング期間の説明を印刷</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-135">レポートの各エイジング期間列の上部にエイジング期間の説明を含めるには、<strong>はい</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="90dd1-136">列ヘッダーのないレポートを印刷するには、<strong>いいえ</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-137"><strong>間隔</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-138">各期間の日数または月数を入力して、使用する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="90dd1-139">たとえば、エイジング情報を週単位で表示させる場合は、このフィールドに 7 を入力し、<strong>日付/月</strong>フィールドで <strong>日付</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="90dd1-140">**注記:** このフィールドに入力する情報は、エイジング期間の定義を選択しなかった場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="90dd1-141">それ以外の場合、印刷方向はエイジング期間の定義で定義されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-142"><strong>日/月</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-143"><strong>サイクル間隔</strong>フィールドで期間を定義する際に使用する単位として、<strong>日付</strong>または<strong>月</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-144"><strong>印刷方向</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-145">残高を計算するかどうかを選択し、過去または将来の期間のエイジング レポートを印刷します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="90dd1-146">日付は、フィールド<strong>での残高</strong>にて選択した日付を基準にして評価されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="90dd1-147">過去の期間の情報を表示する場合は、<strong>後方</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="90dd1-148">将来の期間の情報を表示する場合は、<strong>前方</strong>を選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="90dd1-149">**注記:** このフィールドに入力する情報は、エイジング期間の定義を選択しなかった場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-150"><strong>細目</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-151">レポートに表示される残高に含まれるトランザクションをリストするために選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-152"><strong>トランザクション通貨での金額を含める</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-153">会計通貨の金額に加え、トランザクション通貨の金額を含めるために選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="90dd1-154">このチェック ボックスが選択されていない場合、レポートの金額は会計通貨でのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-155"><strong>マイナス残高</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-156">残高がマイナスの顧客 ID を含めるために選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90dd1-157"><strong>残高がゼロの口座を除外します</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-158">残高がゼロの顧客勘定を除外するために選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90dd1-159"><strong>支払状態</strong></span><span class="sxs-lookup"><span data-stu-id="90dd1-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="90dd1-160">決済されていない支払を表示するために選択します。</span><span class="sxs-lookup"><span data-stu-id="90dd1-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="90dd1-161">これらは、レポートの最初の列に表示されます。</span><span class="sxs-lookup"><span data-stu-id="90dd1-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

