---
title: Financial Reporting に関するよく寄せられる質問
description: このトピックでは、よく寄せられる Financial Reporting に関する質問の一覧を示します。
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249309"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="8e6de-103">Financial Reporting に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8e6de-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="8e6de-104">このトピックでは、よく寄せられる Financial Reporting に関する質問の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="8e6de-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="8e6de-105">ツリー セキュリティを使用して、レポートへのアクセスを制限するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="8e6de-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="8e6de-106">シナリオ: USMF デモ会社では、一部の貸借対照表レポートを、Financial Reporting のすべてのユーザーが D365 で表示できるようにしたくないと考えています。</span><span class="sxs-lookup"><span data-stu-id="8e6de-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="8e6de-107">解決策: ツリー セキュリティを利用すると、あるレポートへのアクセスを制限して、特定のユーザーのみがレポートにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8e6de-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="8e6de-108">Financial Reporter レポート デザイナーにログインします</span><span class="sxs-lookup"><span data-stu-id="8e6de-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="8e6de-109">新しいツリー定義を作成します (ファイル | 新規 | ツリー定義)。a.</span><span class="sxs-lookup"><span data-stu-id="8e6de-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="8e6de-110">**ユニットのセキュリティ** 列の **集計** 行をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="8e6de-111">i.</span><span class="sxs-lookup"><span data-stu-id="8e6de-111">i.</span></span>    <span data-ttu-id="8e6de-112">ユーザーとグループをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="8e6de-113">1. このレポートにアクセスするユーザーまたはグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e6de-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="8e6de-114">[![ユーザー画面](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="8e6de-115">[![セキュリティ画面](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="8e6de-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="8e6de-116">b.</span><span class="sxs-lookup"><span data-stu-id="8e6de-116">b.</span></span>    <span data-ttu-id="8e6de-117">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-117">Click **Save**.</span></span>
  
<span data-ttu-id="8e6de-118">[![保存ボタン](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="8e6de-119">レポート定義で、新しいツリー定義を追加します</span><span class="sxs-lookup"><span data-stu-id="8e6de-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="8e6de-120">[![ツリー定義フォーム](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="8e6de-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="8e6de-121">A.</span><span class="sxs-lookup"><span data-stu-id="8e6de-121">A.</span></span>  <span data-ttu-id="8e6de-122">ツリー定義で、設定をクリックし、レポート ユニットの選択で、すべてのユニットを含むのチェックボックスをオンにします</span><span class="sxs-lookup"><span data-stu-id="8e6de-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="8e6de-123">[![レポート ユニットの選択フォーム](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="8e6de-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="8e6de-124">**変更前:** [![変更前のスクリーンショット](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="8e6de-125">**変更後:** [![変更後のスクリーンショット](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="8e6de-126">注: 上記のメッセージの理由は、ユニットのセキュリティを適用した後、ユーザーがそのレポートにアクセスできないためです。</span><span class="sxs-lookup"><span data-stu-id="8e6de-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="8e6de-127">D365 の残高と一致しない勘定を特定するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="8e6de-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="8e6de-128">D365 で予想される値と一致しないレポートがある場合、それらの勘定との差異を特定するために実行できるいくつかの手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8e6de-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="8e6de-129">Financial Reporter レポート デザイナーでの操作</span><span class="sxs-lookup"><span data-stu-id="8e6de-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="8e6de-130">新しい行定義を作成します。a.</span><span class="sxs-lookup"><span data-stu-id="8e6de-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="8e6de-131">編集 | 分析コードからの行の挿入をクリックします。i.</span><span class="sxs-lookup"><span data-stu-id="8e6de-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="8e6de-132">MainAccount を選択します。[![主勘定の選択の画面](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="8e6de-133">ii.</span><span class="sxs-lookup"><span data-stu-id="8e6de-133">ii.</span></span> <span data-ttu-id="8e6de-134">OK をクリックします。b.</span><span class="sxs-lookup"><span data-stu-id="8e6de-134">Click Ok b.</span></span>    <span data-ttu-id="8e6de-135">行定義を保存します。</span><span class="sxs-lookup"><span data-stu-id="8e6de-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="8e6de-136">新しい列定義を作成します。[![新しい列定義の作成](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="8e6de-137">新しいレポート定義を作成します。a.</span><span class="sxs-lookup"><span data-stu-id="8e6de-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="8e6de-138">設定をクリックして、次のチェックボックスをオフにします。[![設定フォーム](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="8e6de-139">レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8e6de-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="8e6de-140">レポートを Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="8e6de-141">D365 で:</span><span class="sxs-lookup"><span data-stu-id="8e6de-141">In D365:</span></span> 
1.  <span data-ttu-id="8e6de-142">一般会計 | 照会およびレポート | 試算表をクリックします。a.</span><span class="sxs-lookup"><span data-stu-id="8e6de-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="8e6de-143">パラメーター i.</span><span class="sxs-lookup"><span data-stu-id="8e6de-143">Parameters i.</span></span>  <span data-ttu-id="8e6de-144">開始日: 会計年度の開始日 ii.</span><span class="sxs-lookup"><span data-stu-id="8e6de-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="8e6de-145">終了日: レポート作成の対象日 iii.</span><span class="sxs-lookup"><span data-stu-id="8e6de-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="8e6de-146">財務分析コード: 主勘定セットを設定します。[![主勘定フォーム](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="8e6de-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="8e6de-147">b.</span><span class="sxs-lookup"><span data-stu-id="8e6de-147">b.</span></span>    <span data-ttu-id="8e6de-148">計算をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-148">Click Calculate</span></span>

2.  <span data-ttu-id="8e6de-149">レポートを Excel にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="8e6de-149">Export the report to Excel</span></span>

<span data-ttu-id="8e6de-150">これで、FR Excel レポートから D365 試算表レポートにデータをコピーして、[決算残高] 列を比較できます。</span><span class="sxs-lookup"><span data-stu-id="8e6de-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]