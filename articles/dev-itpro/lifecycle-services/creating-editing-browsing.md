---
title: "BPM ライブラリの作成、編集、および参照"
description: "このトピックでは、BPM ライブラリを作成または編集する方法と、既存のライブラリを参照する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: 
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 2d123a054e05c5a3d239ea5115d31c2582903552
ms.openlocfilehash: 938272e761a32476c7a43f6084e010ff2e3aa696
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2018

---

# <a name="create-edit-and-browse-bpm-libraries"></a><span data-ttu-id="97427-103">BPM ライブラリの作成、編集、および参照</span><span class="sxs-lookup"><span data-stu-id="97427-103">Create, edit, and browse BPM libraries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97427-104">このトピックでは、ビジネス プロセス モデラー (BPM) ライブラリーの作成、編集、参照の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="97427-104">This topic provides information about how to create, edit, and browse Business process modeler (BPM) libraries.</span></span> <span data-ttu-id="97427-105">グローバル ライブラリまたは企業ライブラリである BPM ライブラリを参照できることに注意することが重要です。</span><span class="sxs-lookup"><span data-stu-id="97427-105">It's important to note You can browse a BPM library that is a global library or a corporate library.</span></span> <span data-ttu-id="97427-106">ただし、BPM ライブラリを編集および使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトの一部にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97427-106">However, before you can edit and work with a BPM library, it must be part of your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="97427-107">Microsoft によって配布されるライブラリは**グローバル ライブラリ**下に表示され、組織によって公開されているライブラリは**コーポレート ライブラリ**下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="97427-107">Libraries that are distributed by Microsoft appear under **Global libraries**, whereas libraries that are published by your organization appear under **Corporate libraries**.</span></span>

  >[!NOTE]
  ><span data-ttu-id="97427-108">BPM ローカライズはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="97427-108">BPM localization is not supported.</span></span> <span data-ttu-id="97427-109">EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="97427-109">If you edit in the new BPM client in any language other than EN-US, your changes will only display when you view the BPM in the language in which the changes were made.</span></span> <span data-ttu-id="97427-110">EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97427-110">To view any changes made in EN-US, you must synchronize with Visual Studio Team Server before the changes will display.</span></span>

## <a name="create-a-bpm-library"></a><span data-ttu-id="97427-111">BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="97427-111">Create a BPM library</span></span>
<span data-ttu-id="97427-112">BPM ライブラリを作成する方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="97427-112">There are several ways to author a BPM library.</span></span> <span data-ttu-id="97427-113">クライアントで直接構築、または Excel テンプレートをインポートすることにより、最初からそれを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-113">You can do so from scratch either building directly in the client or by importing an Excel template.</span></span> <span data-ttu-id="97427-114">また、既存のライブラリをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="97427-114">Additionally, you can copy an existing library.</span></span> <span data-ttu-id="97427-115">このセクションでは、これらの各方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="97427-115">This section walks through each of these methods.</span></span>

### <a name="use-the-bpm-client"></a><span data-ttu-id="97427-116">BPM クライアントの使用</span><span class="sxs-lookup"><span data-stu-id="97427-116">Use the BPM client</span></span> 

1. <span data-ttu-id="97427-117">**業務プロセス ライブラリ**ページで、**新しいライブラリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-117">On the **Business process libraries** page, select **New library**.</span></span>
     <span data-ttu-id="97427-118">![Select_new_library](./media/Select_new_library.PNG "新しいライブラリ")</span><span class="sxs-lookup"><span data-stu-id="97427-118">![Select_new_library](./media/Select_new_library.PNG "New library")</span></span>
2. <span data-ttu-id="97427-119">新しいライブラリ名を入力し、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-119">Enter a name for the new library, and then select **Create**.</span></span>
     <span data-ttu-id="97427-120">![Create_new_library](./media/Create_new_library.PNG "新しいライブラリの作成")</span><span class="sxs-lookup"><span data-stu-id="97427-120">![Create_new_library](./media/Create_new_library.PNG "Create new library")</span></span>
    
### <a name="use-excel-import"></a><span data-ttu-id="97427-121">Excel のインポートを使用</span><span class="sxs-lookup"><span data-stu-id="97427-121">Use Excel Import</span></span>

1. <span data-ttu-id="97427-122">**業務プロセス ライブラリ**ページで、**Excel からインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-122">On the **Business process libraries** page, select **Import from Excel**.</span></span>
     <span data-ttu-id="97427-123">![Import_from_Excel](./media/Import_from_Excel.PNG "Excel からインポート")</span><span class="sxs-lookup"><span data-stu-id="97427-123">![Import_from_Excel](./media/Import_from_Excel.PNG "Import from Excel")</span></span>
2. <span data-ttu-id="97427-124">ウィンドウから **ダウンロード テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-124">Select **Download template** from the pane.</span></span> <span data-ttu-id="97427-125">ダウンロードしたら、ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="97427-125">Once downloaded, open the file.</span></span>
3. <span data-ttu-id="97427-126">テンプレートにはいくつかの列があり、最も重要なのは **Id** および **Parent Id** です。各行を新しい ID 番号に関連付けます。行を子項目にする場合は、親 ID 列に追加する行の ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="97427-126">The template has several columns, most importantly **Id** and **Parent Id**. Associate each line with a new Id number, if you'd like to make a line a child item, add the Id of the line you'd like it to fall under in the parent Id column.</span></span> <span data-ttu-id="97427-127">the</span><span class="sxs-lookup"><span data-stu-id="97427-127">the</span></span> 
4. <span data-ttu-id="97427-128">完了したら、テンプレートを保存して BPM に戻ります。</span><span class="sxs-lookup"><span data-stu-id="97427-128">Once complete, save the template and return to BPM.</span></span>
5. <span data-ttu-id="97427-129">インポート ウィンドウを使用して、**参照** を選択して、更新済のテンプレートをアップロードし、新しいライブラリの名前を入力し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-129">Using the import pane, select **Browse** to upload the updated template, enter a name for the new library, and select **Import**.</span></span> 
    <span data-ttu-id="97427-130">![Download_template](./media/Download_template.PNG "テンプレートのダウンロード")</span><span class="sxs-lookup"><span data-stu-id="97427-130">![Download_template](./media/Download_template.PNG "Download template")</span></span>
 
### <a name="copy-a-library"></a><span data-ttu-id="97427-131">ライブラリのコピー</span><span class="sxs-lookup"><span data-stu-id="97427-131">Copy a library</span></span> 

1. <span data-ttu-id="97427-132">**業務プロセス ライブラリ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="97427-132">Open the **Business process libraries** page.</span></span> 
2. <span data-ttu-id="97427-133">コピーするライブラリのタイルで、省略記号ボタン (...) を選択し、**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-133">On the tile for the library that you want to copy, select the ellipsis button (…), and then select **Copy**.</span></span>
    <span data-ttu-id="97427-134">![Copy_a_library](./media/Copy_a_library.PNG "ライブラリのコピー")</span><span class="sxs-lookup"><span data-stu-id="97427-134">![Copy_a_library](./media/Copy_a_library.PNG "Copy library")</span></span>   
3. <span data-ttu-id="97427-135">ライブラリ名を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-135">Enter a name for the library, and then click **Create**.</span></span>
    <span data-ttu-id="97427-136">![a_copied_library の作成](./media/Create_a_copied_library.PNG "ライブラリのコピーを作成")</span><span class="sxs-lookup"><span data-stu-id="97427-136">![Create a_copied_library](./media/Create_a_copied_library.PNG "Create copied library")</span></span>


## <a name="import-a-sections-of-another-library"></a><span data-ttu-id="97427-137">別のライブラリのセクションのインポート</span><span class="sxs-lookup"><span data-stu-id="97427-137">Import a sections of another library</span></span>
1. <span data-ttu-id="97427-138">**業務プロセス ライブラリ**ページを開いて、編集するライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="97427-138">Openn the **Business process libraries** page, and then open the library you want to edit.</span></span> 
2. <span data-ttu-id="97427-139">インポートする明細行に移動して**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-139">Navigate to the line you would like to import to and select **Import**.</span></span>
     <span data-ttu-id="97427-140">![Select_import](./media/Select_import.PNG "インポートを選択")</span><span class="sxs-lookup"><span data-stu-id="97427-140">![Select_import](./media/Select_import.PNG "Select import")</span></span>
3. <span data-ttu-id="97427-141">**子として** または **兄弟として** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-141">Select **As child** or **As sibling**.</span></span>
     <span data-ttu-id="97427-142">![Select_child_or_sibling](./media/Select_child_or_sibling.PNG "子または兄弟を選択")</span><span class="sxs-lookup"><span data-stu-id="97427-142">![Select_child_or_sibling](./media/Select_child_or_sibling.PNG "Select child or sibling")</span></span>
4. <span data-ttu-id="97427-143">ウィンドウで、インポートするライブラリを選択して**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-143">In the pane, choose the library you would like to import from and click **Import**.</span></span>
     <span data-ttu-id="97427-144">![Choose_library](./media/Choose_library.PNG "ライブラリの選択")</span><span class="sxs-lookup"><span data-stu-id="97427-144">![Choose_library](./media/Choose_library.PNG "Choose library")</span></span>


## <a name="add-a-new-process"></a><span data-ttu-id="97427-145">新しいプロセスの追加</span><span class="sxs-lookup"><span data-stu-id="97427-145">Add a new process</span></span>

1. <span data-ttu-id="97427-146">BPM ライブラリで、既存のプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-146">In the BPM library, select an existing process.</span></span>
2. <span data-ttu-id="97427-147">**プロセスの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-147">Select **Add process**.</span></span> <span data-ttu-id="97427-148">または選択したプロセス ノードの子または兄弟としてプロセスを追加することを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-148">You can select to add the process as a child or a sibling of the selected process node.</span></span> <span data-ttu-id="97427-149">この方法で、業務プロセスの意味的な階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="97427-149">In this way, you can create a semantic hierarchy of business processes.</span></span>

    <span data-ttu-id="97427-150">![プロセスを追加する](./media/NEWBPM_BlogPost06.png "プロセスの追加")</span><span class="sxs-lookup"><span data-stu-id="97427-150">![Adding a process](./media/NEWBPM_BlogPost06.png "Add process")</span></span>

## <a name="edit-the-properties-of-a-process"></a><span data-ttu-id="97427-151">プロセスのプロパティを編集</span><span class="sxs-lookup"><span data-stu-id="97427-151">Edit the properties of a process</span></span>

1. <span data-ttu-id="97427-152">BPM ライブラリで、編集するプロセス ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-152">In the BPM library, select the process node to edit.</span></span>
2. <span data-ttu-id="97427-153">右ウィンドウの**概要**タブで**編集モード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-153">In the right pane, on the **Overview** tab, click **Edit mode**.</span></span>
3. <span data-ttu-id="97427-154">プロセス ノードの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="97427-154">Enter a name and description for the process node.</span></span>
4. <span data-ttu-id="97427-155">プロセスが適用される業界と国または地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-155">Select the industries and the countries or regions that the process applies to.</span></span> <span data-ttu-id="97427-156">また、キーワードおよびリンクを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="97427-156">You can also add keywords and links.</span></span> <span data-ttu-id="97427-157">キーワードでカテゴリ、認定作業、またはその他のメタデータを定義できます。</span><span class="sxs-lookup"><span data-stu-id="97427-157">Keywords let you define categories, work streams, or other metadata.</span></span> <span data-ttu-id="97427-158">リンク (URL) を使用して、外部サイトまたはドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="97427-158">Links (URLs) let you reference external sites or documentation.</span></span>

    <span data-ttu-id="97427-159">![プロセス プロパティ](./media/NEWBPM_BlogPost08-194x300.png "プロセスの詳細")</span><span class="sxs-lookup"><span data-stu-id="97427-159">![Process properties](./media/NEWBPM_BlogPost08-194x300.png "Process details")</span></span>

5. <span data-ttu-id="97427-160">プロパティの編集を完了したら、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-160">When you've finished editing the properties, click **Save**.</span></span>

## <a name="move-a-process"></a><span data-ttu-id="97427-161">プロセスの移動</span><span class="sxs-lookup"><span data-stu-id="97427-161">Move a process</span></span>

<span data-ttu-id="97427-162">プロセス ノードを移動するか、BPM 階層内の別の親ノードに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="97427-162">You can move a process node or assign it to another parent node in the BPM hierarchy.</span></span>

1. <span data-ttu-id="97427-163">移動するをプロセス ノードを選択し、**プロセスの移動** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-163">Select the process node to move, and then click **Move process**.</span></span> <span data-ttu-id="97427-164">プロセスを上下に移動を選択するか、**移動** を選択してさらにオプションを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-164">You can select to move the process up or down, or you can select **Move** to see more options.</span></span>

    <span data-ttu-id="97427-165">![プロセスを移動する](./media/NEWBPM_BlogPost09.png "プロセスの移動")</span><span class="sxs-lookup"><span data-stu-id="97427-165">![Moving a process](./media/NEWBPM_BlogPost09.png "Move process")</span></span>

2. <span data-ttu-id="97427-166">**移動**を選択した場合は、階層を参照し、プロセスの移動先のノードを選択し、**子として移動**または**兄弟として移動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-166">If you selected **Move**, you can browse the hierarchy, select a node to move the process to, and then select **Move as child** or **Move as sibling**.</span></span> <span data-ttu-id="97427-167">移動操作をキャンセルするには、**キャンセル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-167">To cancel the move operation, click **Cancel**.</span></span>

## <a name="delete-a-process"></a><span data-ttu-id="97427-168">プロセスの削除</span><span class="sxs-lookup"><span data-stu-id="97427-168">Delete a process</span></span>

<span data-ttu-id="97427-169">ビジネス プロセスを削除するには、削除するプロセスを選択し、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="97427-169">To delete a business process, select the process to delete, and then select **Delete**.</span></span>

## <a name="copy-a-global-or-corporate-library-to-your-project"></a><span data-ttu-id="97427-170">グローバルまたは会社のライブラリをプロジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="97427-170">Copy a global or corporate library to your project</span></span>

<span data-ttu-id="97427-171">グローバル ライブラリまたは企業ライブラリである BPM ライブラリを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-171">You can browse a BPM library that is a global library or a corporate library.</span></span> <span data-ttu-id="97427-172">ただし、BPM ライブラリを編集および使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトの一部にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97427-172">However, before you can edit and work with a BPM library, it must be part of your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="97427-173">Microsoft によって配布されるライブラリは**グローバル ライブラリ**下に表示され、組織によって公開されているライブラリは**コーポレート ライブラリ**下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="97427-173">Libraries that are distributed by Microsoft appear under **Global libraries**, whereas libraries that are published by your organization appear under **Corporate libraries**.</span></span>

## <a name="browse-a-bpm-library"></a><span data-ttu-id="97427-174">BPM ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="97427-174">Browse a BPM library</span></span>

1. <span data-ttu-id="97427-175">**業務プロセス ライブラリ**ページで、参照するライブラリのタイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="97427-175">On the **Business process libraries** page, double-click the tile for the library that you want to browse.</span></span>
2. <span data-ttu-id="97427-176">BPM ライブラリで、プロセスを選択してそのサブステップを表示します。</span><span class="sxs-lookup"><span data-stu-id="97427-176">In the BPM library, select a process to view its substeps.</span></span>

    <span data-ttu-id="97427-177">![プロセスおよびそのサブステップ](./media/2.PNG "プロセスおよびそのサブステップ")</span><span class="sxs-lookup"><span data-stu-id="97427-177">![Process and its substeps](./media/2.PNG "Process and its substeps")</span></span>

3. <span data-ttu-id="97427-178">ツールバーのボタンを使用して、プロセスを子プロセスまたは兄弟プロセスとして追加、削除、またはインポートします。</span><span class="sxs-lookup"><span data-stu-id="97427-178">Use the buttons on the toolbar to add, delete, or import processes as a child or a sibling.</span></span> <span data-ttu-id="97427-179">また、**すべて折りたたみ** を選択して親プロセスのみを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-179">You can also select **Collapse all** to view only parent processes.</span></span> 

    <span data-ttu-id="97427-180">![ツールバー](./media/3.PNG "ツールバー")</span><span class="sxs-lookup"><span data-stu-id="97427-180">![Toolbar](./media/3.PNG "Toolbar")</span></span>

## <a name="search-a-bpm-library"></a><span data-ttu-id="97427-181">BPM ライブラリを検索</span><span class="sxs-lookup"><span data-stu-id="97427-181">Search a BPM library</span></span>

<span data-ttu-id="97427-182">BPM ライブラリ内で語または語句を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-182">You can search for words or phrases in your BPM library.</span></span> <span data-ttu-id="97427-183">検索機能は、ビジネス プロセスの名前と説明を検索します。</span><span class="sxs-lookup"><span data-stu-id="97427-183">The search functionality searches the names and descriptions of business processes.</span></span>

- <span data-ttu-id="97427-184">_単語_を検索するには、検索ボックスに検索語を入力し、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="97427-184">To search for a _word_, enter the search word in the search box, and then press Enter.</span></span>
- <span data-ttu-id="97427-185">_語句_を検索するには、検索語句を二重引用符で囲みます。</span><span class="sxs-lookup"><span data-stu-id="97427-185">To search for a _phrase_, put double quotation marks around the search phrase.</span></span>

    <span data-ttu-id="97427-186">たとえば、検索ボックスで**テクノロジ** (単語) または **"情報技術"** (語句) を入力します。</span><span class="sxs-lookup"><span data-stu-id="97427-186">For example, enter **technology** (word) or **"information technology"** (phrase) in the search box.</span></span>

- <span data-ttu-id="97427-187">Microsoft Dynamics 365 for Finance and Operations のタスク記録の一部である、ライブラリ内にある、アプリケーション オブジェクト ツリー (AOT) 要素を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="97427-187">You can also search for Application Object Tree (AOT) elements that are part of the task recordings for Microsoft Dynamics 365 for Finance and Operations, that are in your library.</span></span> <span data-ttu-id="97427-188">通常、これらの AOT 要素はページまたはメニュー項目の名前です。</span><span class="sxs-lookup"><span data-stu-id="97427-188">Typically, these AOT elements are the names of pages or menu items.</span></span> <span data-ttu-id="97427-189">AOT 要素を検索するとき、それにドル記号 ($) の接頭語を付けます。</span><span class="sxs-lookup"><span data-stu-id="97427-189">When you search for an AOT element, prefix it with a dollar sign ($).</span></span> <span data-ttu-id="97427-190">たとえば、検索ボックスで **$CustTable**を入力します。</span><span class="sxs-lookup"><span data-stu-id="97427-190">For example, enter **$CustTable** in the search box.</span></span>

<span data-ttu-id="97427-191">![検索ボックス](./media/searching.png "検索ボックス")</span><span class="sxs-lookup"><span data-stu-id="97427-191">![Search box](./media/searching.png "Search box")</span></span>

   

