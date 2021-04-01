---
title: 公的機関の暫定予算の作成
description: 特定の予算モデルと分析コード値の、暫定予算登録エントリを作成できます。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40371809f3855e57db4bc12f5466f7cef5cec600
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235559"
---
# <a name="create-a-preliminary-budget-for-public-sector"></a><span data-ttu-id="e6666-103">公的機関の暫定予算の作成</span><span class="sxs-lookup"><span data-stu-id="e6666-103">Create a preliminary budget for Public sector</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6666-104">特定の予算モデルと分析コード値の、暫定予算登録エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e6666-104">You can create preliminary budget register entries for a specific budget model and dimension values.</span></span> <span data-ttu-id="e6666-105">実際の予算が承認された後、元の予算登録エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e6666-105">After the actual budget is approved, you can create original budget register entries.</span></span> <span data-ttu-id="e6666-106">この手順は、公的機関部門の PSUS のデモ会社のデータを使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="e6666-106">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="e6666-107">[予算作成] > [予算登録エントリ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e6666-107">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="e6666-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-108">Click New.</span></span>
3. <span data-ttu-id="e6666-109">[予算モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6666-109">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e6666-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6666-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e6666-111">[予算コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6666-111">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e6666-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6666-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e6666-113">[理由コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6666-113">In the Reason code field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e6666-114">一覧で、目的のレコードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-114">In the list, click the desired record.</span></span>
9. <span data-ttu-id="e6666-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-115">Click Save.</span></span>
10. <span data-ttu-id="e6666-116">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-116">Click Add line.</span></span>
    * <span data-ttu-id="e6666-117">オプション: ヘッダーの日付を変更する場合は、新しい日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6666-117">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="e6666-118">この日付により、予算が記録される会計年度期間が決まります。</span><span class="sxs-lookup"><span data-stu-id="e6666-118">This date determines the fiscal period that the budget will be recorded to.</span></span> <span data-ttu-id="e6666-119">他のフィールドに入力するためにタスク ガイドを表示するには、ページ上部の [ロック解除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-119">When viewing the task guide, to fill out other fields, click Unlock at the top of the page.</span></span>  
11. <span data-ttu-id="e6666-120">[勘定構造] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6666-120">In the Account structure field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="e6666-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6666-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="e6666-122">[分析コード値] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6666-122">In the Dimension values field, specify the desired values.</span></span>
14. <span data-ttu-id="e6666-123">[金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e6666-123">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="e6666-124">金額のタイプも入力できます。</span><span class="sxs-lookup"><span data-stu-id="e6666-124">You can also enter an amount type.</span></span>  
15. <span data-ttu-id="e6666-125">[通貨] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="e6666-125">In the Currency field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e6666-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e6666-126">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e6666-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-127">Click Save.</span></span>
18. <span data-ttu-id="e6666-128">[予算残高の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-128">Click Update budget balances.</span></span>
19. <span data-ttu-id="e6666-129">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-129">Click Update.</span></span>
    * <span data-ttu-id="e6666-130">更新の結果を表示するには、青色のバーの [メッセージの詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e6666-130">To see the results of the update, click Message details on the blue bar.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]