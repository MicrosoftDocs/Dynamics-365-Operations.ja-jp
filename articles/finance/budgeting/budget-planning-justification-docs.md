---
title: 予算計画の妥当性ドキュメント
description: 妥当性ドキュメントは、予算を要求する人物に対して特定の予算が必要な理由の記述を提供します。
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445310"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="b12b1-103">予算計画の妥当性ドキュメント</span><span class="sxs-lookup"><span data-stu-id="b12b1-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b12b1-104">妥当性ドキュメントは、予算を要求する人物に対して特定の予算が必要な理由の記述を提供します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="b12b1-105">予算計画テンプレートは、Microsoft Word で予算管理者によって作成され、現在の予算計画プロセスに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="b12b1-106">予算の所有者はテンプレートを開き、予算の要求に基づいて Word に自動的にデータを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="b12b1-107">カスタマイズされた妥当性ドキュメントの保存および予算計画への関連付けを行う前に、追加のテキストやデータを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="b12b1-108">Microsoft Word 用 Microsoft Dynamics Office アドインの設定</span><span class="sxs-lookup"><span data-stu-id="b12b1-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="b12b1-109">新規の Microsoft Word 文書を開きます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="b12b1-110">リボンの **挿入** をクリックして、**ストア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="b12b1-111">Microsoft Dynamics アドインを検索して、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="b12b1-112">Word の右ウィンドウで、**サーバー情報の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="b12b1-113">サーバー URL を入力するか貼り付けて、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="b12b1-114">Microsoft Word での妥当性テンプレートの定義</span><span class="sxs-lookup"><span data-stu-id="b12b1-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="b12b1-115">ログイン後、Microsoft Dynamics Office アドインの **デザイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="b12b1-116">ヘッダー情報については、**フィールドの追加** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="b12b1-117">BudgetPlanJustification のエンティティ データ ソースを選択して、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="b12b1-118">**注記:** このエンティティは、どの妥当性ドキュメントにも必要です。</span><span class="sxs-lookup"><span data-stu-id="b12b1-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="b12b1-119">他のエンティティを使用できますが、このエンティティが含まれていない場合は、Microsoft Dynamics 365 Finance に戻るアップロードが失敗します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-119">Other entities can be used but the upload back to Microsoft Dynamics 365 Finance will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="b12b1-120">Word ドキュメントの BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenter、DocumentNumber のラベルと値を追加します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="b12b1-121">**注記:** 必要であれば、標準ラベルではなく独自のカスタム ラベルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="b12b1-122">**完了** をクリックして、ヘッダー セクションを完了します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="b12b1-123">予算計画金額の明細行レベルの詳細については、**テーブルの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="b12b1-124">再度、BudgetPlanJustification のエンティティ データ ソースを選択して、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="b12b1-125">EffectiveDate、ScenarioName、AccountDisplayValue、AccountingCurrencyExpenseAmount のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="b12b1-126">**注記:** コメントが個別の予算計画明細行内で使用できる場合、ここのテーブルに追加できます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="b12b1-127">エンド ユーザーに提示する説明をさらに追加して、ドキュメントに必要な書式やスタイルを実行します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="b12b1-128">ドキュメントをローカル コンピューターに保存し、ファイルを閉じてから次に進みます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="b12b1-129">妥当性テンプレートを使用するための予算計画プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="b12b1-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="b12b1-130">**予算作成** &gt; **設定** &gt; **予算計画** &gt; **妥当性ドキュメント テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-130">Go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="b12b1-131">**新規** をクリックして、新しく作成された Microsoft Word 文書を参照します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="b12b1-132">テンプレートの表示名と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-132">Enter a template display name and description.</span></span> <span data-ttu-id="b12b1-133">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-133">Click **OK**.</span></span>
4.  <span data-ttu-id="b12b1-134">**予算作成** &gt; **設定** &gt; **予算** **計画** &gt; **予算計画プロセス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="b12b1-135">妥当性テンプレートを使用する必要があるプロセスを選択して、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="b12b1-136">**妥当性ドキュメント テンプレート** フィールドで、適切なテンプレートを選択して保存します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="b12b1-137">カスタマイズされた妥当性ドキュメントの編集および保存</span><span class="sxs-lookup"><span data-stu-id="b12b1-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="b12b1-138">新しい予算計画を作成するか、既存の予算計画を開きます。</span><span class="sxs-lookup"><span data-stu-id="b12b1-138">Create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="b12b1-139">**妥当性** ドロップダウン メニューで、**妥当性の新規作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b12b1-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="b12b1-140">詳細を入力した後、**妥当性** ドロップダウン メニューからカスタマイズされたドキュメントを選択してアップロードします。</span><span class="sxs-lookup"><span data-stu-id="b12b1-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>




