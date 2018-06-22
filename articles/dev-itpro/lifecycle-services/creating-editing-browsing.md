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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9b629c6c144925c7ef5c46423aefe25bf2bad5ba
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-edit-and-browse-bpm-libraries"></a><span data-ttu-id="b1b24-103">BPM ライブラリの作成、編集、および参照</span><span class="sxs-lookup"><span data-stu-id="b1b24-103">Create, edit, and browse BPM libraries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1b24-104">このトピックでは、ビジネス プロセス モデラー (BPM) ライブラリーの作成、編集、参照の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-104">This topic provides information about how to create, edit, and browse Business process modeler (BPM) libraries.</span></span> <span data-ttu-id="b1b24-105">グローバル ライブラリまたは企業ライブラリである BPM ライブラリを参照できることに注意することが重要です。</span><span class="sxs-lookup"><span data-stu-id="b1b24-105">It's important to note You can browse a BPM library that is a global library or a corporate library.</span></span> <span data-ttu-id="b1b24-106">ただし、BPM ライブラリを編集および使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトの一部にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1b24-106">However, before you can edit and work with a BPM library, it must be part of your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b1b24-107">Microsoft によって配布されるライブラリは**グローバル ライブラリ**下に表示され、組織によって公開されているライブラリは**コーポレート ライブラリ**下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-107">Libraries that are distributed by Microsoft appear under **Global libraries**, whereas libraries that are published by your organization appear under **Corporate libraries**.</span></span>

## <a name="create-a-bpm-library"></a><span data-ttu-id="b1b24-108">BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="b1b24-108">Create a BPM library</span></span>
<span data-ttu-id="b1b24-109">BPM ライブラリを作成する方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="b1b24-109">There are several ways to author a BPM library.</span></span> <span data-ttu-id="b1b24-110">クライアントで直接構築、または Excel テンプレートをインポートすることにより、最初からそれを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-110">You can do so from scratch either building directly in the client or by importing an Excel template.</span></span> <span data-ttu-id="b1b24-111">また、既存のライブラリをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-111">Additionally, you can copy an existing library.</span></span> <span data-ttu-id="b1b24-112">このセクションでは、これらの各方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-112">This section walks through each of these methods.</span></span>

### <a name="use-the-bpm-client"></a><span data-ttu-id="b1b24-113">BPM クライアントの使用</span><span class="sxs-lookup"><span data-stu-id="b1b24-113">Use the BPM client</span></span> 

1. <span data-ttu-id="b1b24-114">**業務プロセス ライブラリ**ページで、**新しいライブラリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-114">On the **Business process libraries** page, select **New library**.</span></span>
     <span data-ttu-id="b1b24-115">![Select_new_library](./media/Select_new_library.PNG "新しいライブラリ")</span><span class="sxs-lookup"><span data-stu-id="b1b24-115">![Select_new_library](./media/Select_new_library.PNG "New library")</span></span>
2. <span data-ttu-id="b1b24-116">新しいライブラリ名を入力し、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-116">Enter a name for the new library, and then select **Create**.</span></span>
     <span data-ttu-id="b1b24-117">![Create_new_library](./media/Create_new_library.PNG "新しいライブラリの作成")</span><span class="sxs-lookup"><span data-stu-id="b1b24-117">![Create_new_library](./media/Create_new_library.PNG "Create new library")</span></span>
    
### <a name="use-excel-import"></a><span data-ttu-id="b1b24-118">Excel のインポートを使用</span><span class="sxs-lookup"><span data-stu-id="b1b24-118">Use Excel Import</span></span>

1. <span data-ttu-id="b1b24-119">**業務プロセス ライブラリ**ページで、**Excel からインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-119">On the **Business process libraries** page, select **Import from Excel**.</span></span>
     <span data-ttu-id="b1b24-120">![Import_from_Excel](./media/Import_from_Excel.PNG "Excel からインポート")</span><span class="sxs-lookup"><span data-stu-id="b1b24-120">![Import_from_Excel](./media/Import_from_Excel.PNG "Import from Excel")</span></span>
2. <span data-ttu-id="b1b24-121">ウィンドウから **ダウンロード テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-121">Select **Download template** from the pane.</span></span> <span data-ttu-id="b1b24-122">ダウンロードしたら、ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-122">Once downloaded, open the file.</span></span>
3. <span data-ttu-id="b1b24-123">テンプレートにはいくつかの列があり、最も重要なのは **Id** および **Parent Id** です。各行を新しい ID 番号に関連付けます。行を子項目にする場合は、親 ID 列に追加する行の ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-123">The template has several columns, most importantly **Id** and **Parent Id**. Associate each line with a new Id number, if you'd like to make a line a child item, add the Id of the line you'd like it to fall under in the parent Id column.</span></span> <span data-ttu-id="b1b24-124">the</span><span class="sxs-lookup"><span data-stu-id="b1b24-124">the</span></span> 
4. <span data-ttu-id="b1b24-125">完了したら、テンプレートを保存して BPM に戻ります。</span><span class="sxs-lookup"><span data-stu-id="b1b24-125">Once complete, save the template and return to BPM.</span></span>
5. <span data-ttu-id="b1b24-126">インポート ウィンドウを使用して、**参照** を選択して、更新済のテンプレートをアップロードし、新しいライブラリの名前を入力し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-126">Using the import pane, select **Browse** to upload the updated template, enter a name for the new library, and select **Import**.</span></span> 
    <span data-ttu-id="b1b24-127">![Download_template](./media/Download_template.PNG "テンプレートのダウンロード")</span><span class="sxs-lookup"><span data-stu-id="b1b24-127">![Download_template](./media/Download_template.PNG "Download template")</span></span>
 
### <a name="copy-a-library"></a><span data-ttu-id="b1b24-128">ライブラリのコピー</span><span class="sxs-lookup"><span data-stu-id="b1b24-128">Copy a library</span></span> 

1. <span data-ttu-id="b1b24-129">**業務プロセス ライブラリ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-129">Open the **Business process libraries** page.</span></span> 
2. <span data-ttu-id="b1b24-130">コピーするライブラリのタイルで、省略記号ボタン (...) を選択し、**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-130">On the tile for the library that you want to copy, select the ellipsis button (…), and then select **Copy**.</span></span>
    <span data-ttu-id="b1b24-131">![Copy_a_library](./media/Copy_a_library.PNG "ライブラリのコピー")</span><span class="sxs-lookup"><span data-stu-id="b1b24-131">![Copy_a_library](./media/Copy_a_library.PNG "Copy library")</span></span>   
3. <span data-ttu-id="b1b24-132">ライブラリ名を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-132">Enter a name for the library, and then click **Create**.</span></span>
    <span data-ttu-id="b1b24-133">![a_copied_library の作成](./media/Create_a_copied_library.PNG "ライブラリのコピーを作成")</span><span class="sxs-lookup"><span data-stu-id="b1b24-133">![Create a_copied_library](./media/Create_a_copied_library.PNG "Create copied library")</span></span>


## <a name="import-a-sections-of-another-library"></a><span data-ttu-id="b1b24-134">別のライブラリのセクションのインポート</span><span class="sxs-lookup"><span data-stu-id="b1b24-134">Import a sections of another library</span></span>
1. <span data-ttu-id="b1b24-135">**業務プロセス ライブラリ**ページを開いて、編集するライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-135">Openn the **Business process libraries** page, and then open the library you want to edit.</span></span> 
2. <span data-ttu-id="b1b24-136">インポートする明細行に移動して**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-136">Navigate to the line you would like to import to and select **Import**.</span></span>
     <span data-ttu-id="b1b24-137">![Select_import](./media/Select_import.PNG "インポートを選択")</span><span class="sxs-lookup"><span data-stu-id="b1b24-137">![Select_import](./media/Select_import.PNG "Select import")</span></span>
3. <span data-ttu-id="b1b24-138">**子として** または **兄弟として** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-138">Select **As child** or **As sibling**.</span></span>
     <span data-ttu-id="b1b24-139">![Select_child_or_sibling](./media/Select_child_or_sibling.PNG "子または兄弟を選択")</span><span class="sxs-lookup"><span data-stu-id="b1b24-139">![Select_child_or_sibling](./media/Select_child_or_sibling.PNG "Select child or sibling")</span></span>
4. <span data-ttu-id="b1b24-140">ウィンドウで、インポートするライブラリを選択して**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-140">In the pane, choose the library you would like to import from and click **Import**.</span></span>
     <span data-ttu-id="b1b24-141">![Choose_library](./media/Choose_library.PNG "ライブラリの選択")</span><span class="sxs-lookup"><span data-stu-id="b1b24-141">![Choose_library](./media/Choose_library.PNG "Choose library")</span></span>


## <a name="add-a-new-process"></a><span data-ttu-id="b1b24-142">新しいプロセスの追加</span><span class="sxs-lookup"><span data-stu-id="b1b24-142">Add a new process</span></span>

1. <span data-ttu-id="b1b24-143">BPM ライブラリで、既存のプロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-143">In the BPM library, select an existing process.</span></span>
2. <span data-ttu-id="b1b24-144">**プロセスの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-144">Select **Add process**.</span></span> <span data-ttu-id="b1b24-145">または選択したプロセス ノードの子または兄弟としてプロセスを追加することを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-145">You can select to add the process as a child or a sibling of the selected process node.</span></span> <span data-ttu-id="b1b24-146">この方法で、業務プロセスの意味的な階層を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-146">In this way, you can create a semantic hierarchy of business processes.</span></span>

    <span data-ttu-id="b1b24-147">![プロセスを追加する](./media/NEWBPM_BlogPost06.png "プロセスの追加")</span><span class="sxs-lookup"><span data-stu-id="b1b24-147">![Adding a process](./media/NEWBPM_BlogPost06.png "Add process")</span></span>

## <a name="edit-the-properties-of-a-process"></a><span data-ttu-id="b1b24-148">プロセスのプロパティを編集</span><span class="sxs-lookup"><span data-stu-id="b1b24-148">Edit the properties of a process</span></span>

1. <span data-ttu-id="b1b24-149">BPM ライブラリで、編集するプロセス ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-149">In the BPM library, select the process node to edit.</span></span>
2. <span data-ttu-id="b1b24-150">右ウィンドウの**概要**タブで**編集モード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-150">In the right pane, on the **Overview** tab, click **Edit mode**.</span></span>
3. <span data-ttu-id="b1b24-151">プロセス ノードの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-151">Enter a name and description for the process node.</span></span>
4. <span data-ttu-id="b1b24-152">プロセスが適用される業界と国または地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-152">Select the industries and the countries or regions that the process applies to.</span></span> <span data-ttu-id="b1b24-153">また、キーワードおよびリンクを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-153">You can also add keywords and links.</span></span> <span data-ttu-id="b1b24-154">キーワードでカテゴリ、認定作業、またはその他のメタデータを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-154">Keywords let you define categories, work streams, or other metadata.</span></span> <span data-ttu-id="b1b24-155">リンク (URL) を使用して、外部サイトまたはドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-155">Links (URLs) let you reference external sites or documentation.</span></span>

    <span data-ttu-id="b1b24-156">![プロセス プロパティ](./media/NEWBPM_BlogPost08-194x300.png "プロセスの詳細")</span><span class="sxs-lookup"><span data-stu-id="b1b24-156">![Process properties](./media/NEWBPM_BlogPost08-194x300.png "Process details")</span></span>

5. <span data-ttu-id="b1b24-157">プロパティの編集を完了したら、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-157">When you've finished editing the properties, click **Save**.</span></span>

## <a name="move-a-process"></a><span data-ttu-id="b1b24-158">プロセスの移動</span><span class="sxs-lookup"><span data-stu-id="b1b24-158">Move a process</span></span>

<span data-ttu-id="b1b24-159">プロセス ノードを移動するか、BPM 階層内の別の親ノードに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-159">You can move a process node or assign it to another parent node in the BPM hierarchy.</span></span>

1. <span data-ttu-id="b1b24-160">移動するをプロセス ノードを選択し、**プロセスの移動** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-160">Select the process node to move, and then click **Move process**.</span></span> <span data-ttu-id="b1b24-161">プロセスを上下に移動を選択するか、**移動** を選択してさらにオプションを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-161">You can select to move the process up or down, or you can select **Move** to see more options.</span></span>

    <span data-ttu-id="b1b24-162">![プロセスを移動する](./media/NEWBPM_BlogPost09.png "プロセスの移動")</span><span class="sxs-lookup"><span data-stu-id="b1b24-162">![Moving a process](./media/NEWBPM_BlogPost09.png "Move process")</span></span>

2. <span data-ttu-id="b1b24-163">**移動**を選択した場合は、階層を参照し、プロセスの移動先のノードを選択し、**子として移動**または**兄弟として移動**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-163">If you selected **Move**, you can browse the hierarchy, select a node to move the process to, and then select **Move as child** or **Move as sibling**.</span></span> <span data-ttu-id="b1b24-164">移動操作をキャンセルするには、**キャンセル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-164">To cancel the move operation, click **Cancel**.</span></span>

## <a name="delete-a-process"></a><span data-ttu-id="b1b24-165">プロセスの削除</span><span class="sxs-lookup"><span data-stu-id="b1b24-165">Delete a process</span></span>

<span data-ttu-id="b1b24-166">ビジネス プロセスを削除するには、削除するプロセスを選択し、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-166">To delete a business process, select the process to delete, and then select **Delete**.</span></span>

## <a name="copy-a-global-or-corporate-library-to-your-project"></a><span data-ttu-id="b1b24-167">グローバルまたは会社のライブラリをプロジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-167">Copy a global or corporate library to your project</span></span>

<span data-ttu-id="b1b24-168">グローバル ライブラリまたは企業ライブラリである BPM ライブラリを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-168">You can browse a BPM library that is a global library or a corporate library.</span></span> <span data-ttu-id="b1b24-169">ただし、BPM ライブラリを編集および使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトの一部にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1b24-169">However, before you can edit and work with a BPM library, it must be part of your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b1b24-170">Microsoft によって配布されるライブラリは**グローバル ライブラリ**下に表示され、組織によって公開されているライブラリは**コーポレート ライブラリ**下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-170">Libraries that are distributed by Microsoft appear under **Global libraries**, whereas libraries that are published by your organization appear under **Corporate libraries**.</span></span>

## <a name="browse-a-bpm-library"></a><span data-ttu-id="b1b24-171">BPM ライブラリの参照</span><span class="sxs-lookup"><span data-stu-id="b1b24-171">Browse a BPM library</span></span>

1. <span data-ttu-id="b1b24-172">**業務プロセス ライブラリ**ページで、参照するライブラリのタイルをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-172">On the **Business process libraries** page, double-click the tile for the library that you want to browse.</span></span>
2. <span data-ttu-id="b1b24-173">BPM ライブラリで、プロセスを選択してそのサブステップを表示します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-173">In the BPM library, select a process to view its substeps.</span></span>

    <span data-ttu-id="b1b24-174">![プロセスおよびそのサブステップ](./media/2.PNG "プロセスおよびそのサブステップ")</span><span class="sxs-lookup"><span data-stu-id="b1b24-174">![Process and its substeps](./media/2.PNG "Process and its substeps")</span></span>

3. <span data-ttu-id="b1b24-175">ツールバーのボタンを使用して、プロセスを子プロセスまたは兄弟プロセスとして追加、削除、またはインポートします。</span><span class="sxs-lookup"><span data-stu-id="b1b24-175">Use the buttons on the toolbar to add, delete, or import processes as a child or a sibling.</span></span> <span data-ttu-id="b1b24-176">また、**すべて折りたたみ** を選択して親プロセスのみを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-176">You can also select **Collapse all** to view only parent processes.</span></span> 

    <span data-ttu-id="b1b24-177">![ツールバー](./media/3.PNG "ツールバー")</span><span class="sxs-lookup"><span data-stu-id="b1b24-177">![Toolbar](./media/3.PNG "Toolbar")</span></span>

## <a name="search-a-bpm-library"></a><span data-ttu-id="b1b24-178">BPM ライブラリを検索</span><span class="sxs-lookup"><span data-stu-id="b1b24-178">Search a BPM library</span></span>

<span data-ttu-id="b1b24-179">BPM ライブラリ内で語または語句を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-179">You can search for words or phrases in your BPM library.</span></span> <span data-ttu-id="b1b24-180">検索機能は、ビジネス プロセスの名前と説明を検索します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-180">The search functionality searches the names and descriptions of business processes.</span></span>

- <span data-ttu-id="b1b24-181">_単語_を検索するには、検索ボックスに検索語を入力し、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-181">To search for a _word_, enter the search word in the search box, and then press Enter.</span></span>
- <span data-ttu-id="b1b24-182">_語句_を検索するには、検索語句を二重引用符で囲みます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-182">To search for a _phrase_, put double quotation marks around the search phrase.</span></span>

    <span data-ttu-id="b1b24-183">たとえば、検索ボックスで**テクノロジ** (単語) または **"情報技術"** (語句) を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-183">For example, enter **technology** (word) or **"information technology"** (phrase) in the search box.</span></span>

- <span data-ttu-id="b1b24-184">Microsoft Dynamics 365 for Finance and Operations のタスク記録の一部である、ライブラリ内にある、アプリケーション オブジェクト ツリー (AOT) 要素を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-184">You can also search for Application Object Tree (AOT) elements that are part of the task recordings for Microsoft Dynamics 365 for Finance and Operations, that are in your library.</span></span> <span data-ttu-id="b1b24-185">通常、これらの AOT 要素はページまたはメニュー項目の名前です。</span><span class="sxs-lookup"><span data-stu-id="b1b24-185">Typically, these AOT elements are the names of pages or menu items.</span></span> <span data-ttu-id="b1b24-186">AOT 要素を検索するとき、それにドル記号 ($) の接頭語を付けます。</span><span class="sxs-lookup"><span data-stu-id="b1b24-186">When you search for an AOT element, prefix it with a dollar sign ($).</span></span> <span data-ttu-id="b1b24-187">たとえば、検索ボックスで **$CustTable**を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1b24-187">For example, enter **$CustTable** in the search box.</span></span>

<span data-ttu-id="b1b24-188">![検索ボックス](./media/searching.png "検索ボックス")</span><span class="sxs-lookup"><span data-stu-id="b1b24-188">![Search box](./media/searching.png "Search box")</span></span>

