---
title: 償却提案を作成します
description: この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "361294"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="e7df4-103">償却提案を作成します</span><span class="sxs-lookup"><span data-stu-id="e7df4-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7df4-104">この手順では、減価償却のバッチ提案がどうのように機能するか、および固定資産の減価償却を提案する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="e7df4-105">このタスクでは USMF のデモ会社および経理担当者のロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="e7df4-106">償却提案を作成します</span><span class="sxs-lookup"><span data-stu-id="e7df4-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="e7df4-107">[固定資産] > [仕訳入力] > [償却提案の作成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="e7df4-108">[仕訳帳名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e7df4-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7df4-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e7df4-110">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e7df4-111">月間の減価償却を 1 つの仕訳帳明細行に集計する場合に、減価償却の集計オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="e7df4-112">たとえば、終了日の値が 2015 年 3 月 31 日の場合、次の説明: “2015 年 1 月 31 日以降の原価償却” が作成されます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="e7df4-113">提案された仕訳帳明細行の [日付] フィールドは、2015 年 3 月 31 日に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="e7df4-114">償却提案は資産、資産グループ、または他の検索条件別に、フィルター オプションを使用してフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="e7df4-115">固定資産のフォームの取得提案または償却提案を作成すると、減価償却をバッチで提案できます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="e7df4-116">これは、より多くのシステム リソースを使用する大規模な提案に対して推奨されています。</span><span class="sxs-lookup"><span data-stu-id="e7df4-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="e7df4-117">バッチのオプションを選択した場合、その処理中に他のタスクも実行できます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="e7df4-118">この方法で減価償却を提案する場合、減価償却は固定資産の価値モデルに対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="e7df4-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="e7df4-119">[仕訳帳の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7df4-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="e7df4-120">減価償却のエントリを確認します</span><span class="sxs-lookup"><span data-stu-id="e7df4-120">Review depreciation entries</span></span>
1. <span data-ttu-id="e7df4-121">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="e7df4-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e7df4-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e7df4-123">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7df4-123">Click Lines.</span></span>
4. <span data-ttu-id="e7df4-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7df4-124">Click Post.</span></span>

