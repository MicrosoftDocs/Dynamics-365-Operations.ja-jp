---
title: "職位の予算作成のトラブルシューティング"
description: "この記事は、職位の予算作成をコンフィギュレーションするときに提起される可能性のある質問に対する回答を提供します。 これは、予算原価要素、報酬グループ、および報酬グリッドの作成方法に関する、よく寄せられる質問に対処します。"
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 77ee178ddc942a3ae4d5669e5efbf29337648df1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="1ae6f-104">職位の予算作成のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1ae6f-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ae6f-105">この記事は、職位の予算作成をコンフィギュレーションするときに提起される可能性のある質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="1ae6f-106">これは、予算原価要素、報酬グループ、および報酬グリッドの作成方法に関する、よく寄せられる質問に対処します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="1ae6f-107">人事管理で [予測職位] ページが見つからないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="1ae6f-108">予測職位は予算作成に移動されました。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="1ae6f-109">予算原価要素をどうして削除できませんか</span><span class="sxs-lookup"><span data-stu-id="1ae6f-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="1ae6f-110">予測職位に割り当てられている予算原価要素は削除できません。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="1ae6f-111">予算原価要素を削除するには、その前に、すべての予測職位からその予算原価要素を削除してください。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="1ae6f-112">**ヒント:** 予算原価要素が割り当てられているすべての職位を検索するには、[**予算原価要素**] ページの原価要素を選択し、[**職位の更新**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="1ae6f-113">原価要素を使用している職位が上部グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="1ae6f-114">どのように各原価要素を開かずに複数の予測職位から原価要素を削除できますか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="1ae6f-115">原価要素を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-115">You can’t remove a cost element.</span></span> <span data-ttu-id="1ae6f-116">ただし、予算計画サイクルの日付の範囲外になるように開始日と終了日を変更した場合、その予算計画サイクルの予測職位に原価要素は割り当てられなくなります。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="1ae6f-117">この変更を加えるには、予算原価要素を開き、[**原価計算**] クイックタブで [**日付の変更**] を開き、有効日または有効期限を変更します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="1ae6f-118">その後、原価要素が割り当てられているすべての予測職位を自動的に更新するには [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="1ae6f-119">**ヒント:** この方法を使用する場合、開始日と終了日が該当する範囲外にある**すべての**予測職位から予算原価要素が削除されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="1ae6f-120">この効果が予定外のことである場合は、予算原価要素を削除する各予測職位を開き、手動で変更を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="1ae6f-121">予算原価要素の [原価計算] クイック タブに年間金額を入力できないのはどうしてですか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="1ae6f-122">システムは値を計算するための割合を必要とするので、[**計算基準**] クイック タブに予算原価要素が存在する場合、年間金額を入力できません。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="1ae6f-123">この値を変更するには、[**計算基準**] クイック タブからすべての予算原価要素を削除してください。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="1ae6f-124">予算原価タイプを収入から別の予算原価タイプに変更できないのはどうしてですか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="1ae6f-125">一部の予算原価要素は、計算の基礎として、収入原価要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="1ae6f-126">[**予算原価タイプ**] フィールドを変更するには、すべての予算原価要素の [**計算基準**] クイック タブから収入原価要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="1ae6f-127">予算原価要素の予算原価要素明細行の日付を変更できないのはどうしてですか</span><span class="sxs-lookup"><span data-stu-id="1ae6f-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="1ae6f-128">予算原価要素が予測職位によって使用されているときは、予算原価要素明細行の日付を変更できません。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="1ae6f-129">この制限は、予測職位が予算原価要素のガイドラインにかならず準拠するのを保証するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="1ae6f-130">日付を変更するには、[**原価計算**] クイック タブで [**日付の変更**] をクリックして新しい日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="1ae6f-131">その後、原価要素が割り当てられている予測職位を更新するには [**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="1ae6f-132">[報酬グループ] ページで予算原価要素の原価を変更できないのはどうしてですか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="1ae6f-133">予算原価要素は、[**予算原価要素**] ページでのみ作成および変更できます。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="1ae6f-134">予測職位の原価要素の日付を変更するときエラー メッセージが表示されるのはどうしてですか。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="1ae6f-135">予測職位の原価要素明細行の日付は、次の範囲にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="1ae6f-136">職位の有効日と有効期限。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="1ae6f-137">予算原価要素の有効日と有効期限。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="1ae6f-138">予測職位の予算計画プロセスに関連付けられている予算サイクルの開始日と終了日。</span><span class="sxs-lookup"><span data-stu-id="1ae6f-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





