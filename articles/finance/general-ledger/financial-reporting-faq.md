---
title: Financial Reporting に関するよく寄せられる質問
description: このトピックでは、よく寄せられる Financial Reporting に関する質問の一覧を示します。
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923028"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="12db9-103">Financial Reporting に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="12db9-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="12db9-104">このトピックでは、よく寄せられる Financial Reporting に関する質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="12db9-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="12db9-105">ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="12db9-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="12db9-106">次の例は、ツリー セキュリティを使用してレポートへのアクセスを制限する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="12db9-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="12db9-107">USMF デモ会社には、Financial Reporting のすべてのユーザーがアクセスすべきではない貸借対照表レポートがあります。</span><span class="sxs-lookup"><span data-stu-id="12db9-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="12db9-108">アクセスを制限するには、ツリー セキュリティを使用して、1 つのレポートへのアクセスを制限し、特定のユーザーのみがレポートにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="12db9-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="12db9-109">アクセスを制限するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="12db9-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="12db9-110">Financial Reporter Report Designer にサインインします。</span><span class="sxs-lookup"><span data-stu-id="12db9-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="12db9-111">新しいツリー定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="12db9-111">Create a new tree definition.</span></span> <span data-ttu-id="12db9-112">**ファイル > 新規 > ツリー定義** に移動します。</span><span class="sxs-lookup"><span data-stu-id="12db9-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="12db9-113">**ユニットのセキュリティ** 列の **集計** 行をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="12db9-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="12db9-114">**ユーザーとグループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="12db9-115">このレポートにアクセスする必要があるユーザーまたはグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="12db9-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-116">Select **Save**.</span></span>
7. <span data-ttu-id="12db9-117">レポート定義で、新しいツリー定義を追加します。</span><span class="sxs-lookup"><span data-stu-id="12db9-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="12db9-118">ツリー定義で、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="12db9-119">**レポート ユニットの選択** で、**すべてのユニットを含む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="12db9-120">残高と一致しない勘定は、どのように識別できますか。</span><span class="sxs-lookup"><span data-stu-id="12db9-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="12db9-121">残高が一致しないレポートがある場合は、以下の手順に従って、それぞれの勘定と差異を識別できます。</span><span class="sxs-lookup"><span data-stu-id="12db9-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="12db9-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="12db9-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="12db9-123">Financial Reporter Report Designer で、新しい行定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="12db9-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="12db9-124">**編集 > 分析コードからの行の挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="12db9-125">**MainAccount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="12db9-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-126">Select **OK**.</span></span>
5. <span data-ttu-id="12db9-127">行定義を保存します。</span><span class="sxs-lookup"><span data-stu-id="12db9-127">Save the row definition.</span></span>
6. <span data-ttu-id="12db9-128">新しい列定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="12db9-128">Create a new column definition</span></span>
7. <span data-ttu-id="12db9-129">新しいレポート定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="12db9-129">Create a new report definition.</span></span>
8. <span data-ttu-id="12db9-130">**設定** を選択し、このオプションのマークを解除します。</span><span class="sxs-lookup"><span data-stu-id="12db9-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="12db9-131">レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="12db9-131">Generate the report.</span></span> 
10. <span data-ttu-id="12db9-132">レポートを Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="12db9-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="12db9-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="12db9-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="12db9-134">Dynamics 365 Finance で、**一般会計 > 照会およびレポート > 試算表** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12db9-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="12db9-135">次のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="12db9-135">Set the following parameters:</span></span>
   - <span data-ttu-id="12db9-136">**開始日** - 会計年度の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="12db9-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="12db9-137">**終了日** - レポートを生成する日を入力します。</span><span class="sxs-lookup"><span data-stu-id="12db9-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="12db9-138">**財務分析コード** - このフィールドを **主勘定セット** に設定します。</span><span class="sxs-lookup"><span data-stu-id="12db9-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="12db9-139">**計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="12db9-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="12db9-140">レポートを Microsoft Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="12db9-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="12db9-141">これで、Financial Reporter Excel レポートから試算表レポートにデータをコピーして、**決算残高** 列を比較できます。</span><span class="sxs-lookup"><span data-stu-id="12db9-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]