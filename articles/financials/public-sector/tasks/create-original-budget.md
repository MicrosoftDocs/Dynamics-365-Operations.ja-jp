--- 
title: "公的機関の元の予算の作成および暫定予算エントリのリバース"
description: "元の予算エントリを作成し、予算モデルおよび暫定予算金額を含む分析コード値を使用している場合、暫定予算金額を取り消すことができます。"
author: twheeloc
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f50cc6bf8ec533db677d290c52dbd711d7a1de8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-original-budget-and-reverse-preliminary-budget-entries-in-the-public-sector"></a><span data-ttu-id="73bb2-103">公的機関の元の予算の作成および暫定予算エントリのリバース</span><span class="sxs-lookup"><span data-stu-id="73bb2-103">Create an original budget and reverse preliminary budget entries in the public sector</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73bb2-104">元の予算エントリを作成し、予算モデルおよび暫定予算金額を含む分析コード値を使用している場合、暫定予算金額を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-104">When you create an original budget entry and use the budget model and dimension values that contain preliminary budget amounts, the preliminary budget amounts can be reversed.</span></span> <span data-ttu-id="73bb2-105">この手順は、公的機関部門の PSUS のデモ会社のデータを使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="73bb2-105">This procedure was created using the PSUS demo company data in the public sector partition.</span></span>

1. <span data-ttu-id="73bb2-106">[予算作成] > [予算登録エントリ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-106">Go to Budgeting > Budget register entries.</span></span>
2. <span data-ttu-id="73bb2-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-107">Click New.</span></span>
3. <span data-ttu-id="73bb2-108">[予算モデル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-108">In the Budget model field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="73bb2-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-109">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="73bb2-110">[予算コード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-110">In the Budget code field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="73bb2-111">リストで [元の予算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-111">In the list, click Original budget.</span></span>
7. <span data-ttu-id="73bb2-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-112">Click Save.</span></span>
8. <span data-ttu-id="73bb2-113">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-113">Click Add line.</span></span>
9. <span data-ttu-id="73bb2-114">オプション: ヘッダーの日付を変更する場合は、新しい日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-114">Optional: If you want to change the date from the one in the header, enter a new date.</span></span> <span data-ttu-id="73bb2-115">この日付により、予算が記録される会計年度期間が決まります。</span><span class="sxs-lookup"><span data-stu-id="73bb2-115">This date determines the fiscal period that the budget will be recorded to.</span></span>
10. <span data-ttu-id="73bb2-116">[勘定構造] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="73bb2-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="73bb2-118">[分析コード値] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-118">In the Dimension values field, specify the desired values.</span></span>
13. <span data-ttu-id="73bb2-119">[金額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="73bb2-119">In the Amount field, enter a number.</span></span>
14. <span data-ttu-id="73bb2-120">[通貨] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-120">In the Currency field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="73bb2-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="73bb2-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-122">Click Save.</span></span>
17. <span data-ttu-id="73bb2-123">[予算残高の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-123">Click Update budget balances.</span></span>
    * <span data-ttu-id="73bb2-124">オプション: [暫定予算のリバース] オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="73bb2-124">Optional: You can select the Reverse preliminary budget option.</span></span> <span data-ttu-id="73bb2-125">すべての暫定予算エントリ、または指定した予算コードを持つ暫定予算エントリのみを取り消しできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="73bb2-125">Note that you can reverse all preliminary budget entries, or only the preliminary budget entries that have the budget code that you specify.</span></span>  
    * <span data-ttu-id="73bb2-126">オプションを選択するには、ページ上部の [ロック解除] のアイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-126">To make optional selections, click the Unlock icon at the top of the page.</span></span>  
18. <span data-ttu-id="73bb2-127">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73bb2-127">Click Update.</span></span>


