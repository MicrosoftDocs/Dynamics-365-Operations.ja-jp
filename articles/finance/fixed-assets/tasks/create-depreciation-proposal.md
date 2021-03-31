---
title: 償却提案の作成
description: このトピックでは、減価償却のバッチの提案の働きと、固定資産に対して減価償却を提案する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4852b25ef628cdef6f75f6edf550c539e344a4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227067"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="e6e48-103">償却提案の作成</span><span class="sxs-lookup"><span data-stu-id="e6e48-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6e48-104">このトピックでは、減価償却のバッチの提案の働きと、固定資産に対して減価償却を提案する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="e6e48-105">このタスクでは USMF のデモ会社および経理担当者のロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="e6e48-106">償却提案の作成</span><span class="sxs-lookup"><span data-stu-id="e6e48-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="e6e48-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 償却提案の作成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="e6e48-108">**仕訳帳名** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="e6e48-109">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="e6e48-110">月間の減価償却を 1 つの仕訳帳明細行に集計する場合に、**減価償却の集計** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="e6e48-111">たとえば、終了日の値が 2015 年 3 月 31 日の場合、以下の説明が生成されます: "2015 年 1 月 31 日以降の減価償却。"</span><span class="sxs-lookup"><span data-stu-id="e6e48-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="e6e48-112">提案された仕訳帳明細行の **日付** フィールドは、2015 年 3 月 31 日に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e6e48-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="e6e48-113">償却提案は資産、資産グループ、または他の検索条件別に、**フィルター** オプションを使用してフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="e6e48-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="e6e48-114">**固定資産に対する取得提案または償却提案の作成** フォームを使用すると、減価償却をバッチで提案できます。</span><span class="sxs-lookup"><span data-stu-id="e6e48-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="e6e48-115">これは、より多くのシステム リソースを使用する大規模な提案に対して推奨されています。</span><span class="sxs-lookup"><span data-stu-id="e6e48-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="e6e48-116">バッチのオプションを選択した場合、その処理中に他のタスクも実行できます。</span><span class="sxs-lookup"><span data-stu-id="e6e48-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="e6e48-117">この方法で減価償却を提案する場合、減価償却は固定資産の価値モデルに対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="e6e48-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="e6e48-118">**仕訳帳の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="e6e48-119">減価償却のエントリを確認します</span><span class="sxs-lookup"><span data-stu-id="e6e48-119">Review depreciation entries</span></span>
1. <span data-ttu-id="e6e48-120">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="e6e48-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e6e48-122">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-122">Select **Lines**.</span></span>
4. <span data-ttu-id="e6e48-123">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6e48-123">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]