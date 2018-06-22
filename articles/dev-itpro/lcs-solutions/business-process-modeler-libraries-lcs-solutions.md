---
title: "LCS ソリューションのビジネス プロセス モデラー ライブラリの設定"
description: "このトピックでは、ビジネス プロセス モデラー (BPM) ライブラリを作成して使用する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196953
ms.assetid: 6e6d6896-edef-4739-98ad-c4ea19180972
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 14a0aa2fefbcb9085c7c4ae22881561fc3f7bad7
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-business-process-modeler-libraries-for-an-lcs-solution"></a><span data-ttu-id="80ef4-103">LCS ソリューションのビジネス プロセス モデラー ライブラリの設定</span><span class="sxs-lookup"><span data-stu-id="80ef4-103">Set up Business process modeler libraries for an LCS solution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80ef4-104">このトピックでは、ビジネス プロセス モデラー (BPM) ライブラリを作成して使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-104">This topic explains how to create and work with Business process modeler (BPM) libraries.</span></span>

<a name="create-a-business-process-library"></a><span data-ttu-id="80ef4-105">業務プロセス ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="80ef4-105">Create a business process library</span></span>
---------------------------------

<span data-ttu-id="80ef4-106">ビジネス プロセス モデラー (BPM) ライブラリを作成するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-106">There are two ways to create a Business process modeler (BPM) library.</span></span> <span data-ttu-id="80ef4-107">明細行記録またはタスク記録がない新しいライブラリを作成、または既存のライブラリをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-107">You can create a new library that has no lines or task recordings, or you can copy an existing library.</span></span>

1.  <span data-ttu-id="80ef4-108">Microsoft Dynamics Lifecycle Services (LCS) で、プロジェクトを開き、**追加ツール** セクションが表示されるまで右にスクロールしてから、**ビジネス プロセス モデラー** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-108">In Microsoft Dynamics Lifecycle Services (LCS), open a project, scroll to the right until you see the **More tools** section, and then click the **Business process modeler** tile.</span></span> <span data-ttu-id="80ef4-109">３ つのセクション (ライブラリのタイプごとに1つずつ) が表示される **業務プロセス ライブラリ** ページ:</span><span class="sxs-lookup"><span data-stu-id="80ef4-109">The **Business process libraries** page that appears has three sections, one for each type of library:</span></span>
    -   <span data-ttu-id="80ef4-110">**自分のライブラリ** – ユーザーが作成または追加したビジネス プロセス。</span><span class="sxs-lookup"><span data-stu-id="80ef4-110">**My libraries** – Business processes that users have created or added.</span></span>
    -   <span data-ttu-id="80ef4-111">**コーポレート ライブラリ** - 組織内のユーザーがアップロードした独自の業務プロセス。</span><span class="sxs-lookup"><span data-stu-id="80ef4-111">**Corporate libraries** – Custom business processes that someone in your organization has uploaded.</span></span>
    -   <span data-ttu-id="80ef4-112">**グローバル ライブラリ** – 産業間の標準の業務プロセス。</span><span class="sxs-lookup"><span data-stu-id="80ef4-112">**Global libraries** – Cross-industry standard business processes.</span></span> <span data-ttu-id="80ef4-113">[![業務プロセス ライブラリページの 3 種類のライブラリ](./media/bpm_02.png)](./media/bpm_02.png)</span><span class="sxs-lookup"><span data-stu-id="80ef4-113">[![Three types of libraries on the Business process libraries page](./media/bpm_02.png)](./media/bpm_02.png)</span></span>

2.  <span data-ttu-id="80ef4-114">新しいライブラリを作成するには、任意のライブラリを右クリックし、ウィンドウの左下隅にある **作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-114">To create a new library, right-click any library, and then, in the lower-left corner of the window, click **Create**.</span></span> <span data-ttu-id="80ef4-115">既存のライブラリをコピーするには、そのライブラリを右クリックし、ウィンドウの左下隅にある **コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-115">To copy an existing library, right-click that library, and then, in the lower-left corner of the window, click **Copy**.</span></span> <span data-ttu-id="80ef4-116">[![コピー ボタンの場所](./media/bpm_03.png)](./media/bpm_03.png)</span><span class="sxs-lookup"><span data-stu-id="80ef4-116">[![Location of the Copy button](./media/bpm_03.png)](./media/bpm_03.png)</span></span>
3.  <span data-ttu-id="80ef4-117">ライブラリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-117">Enter a name for the library.</span></span>

<span data-ttu-id="80ef4-118">今作成したライブラリは、**自分のライブラリ** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-118">The library that you created now appears under **My libraries**.</span></span>

## <a name="update-publish-or-delete-a-business-process-library"></a><span data-ttu-id="80ef4-119">ビジネス・プロセス・ライブラリの更新、発行、または削除</span><span class="sxs-lookup"><span data-stu-id="80ef4-119">Update, publish, or delete a business process library</span></span>
<span data-ttu-id="80ef4-120">ライブラリの名前または説明を変更、組織内の他の人が表示できるようにライブラリを公開、またはライブラリを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-120">You can change the name or description of a library, publish a library so that other people in your organization can view it, or delete a library.</span></span>

-   <span data-ttu-id="80ef4-121">**業務プロセス ライブラリ**ページで、右クリックしてライブラリを更新、公開、または削除します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-121">On the **Business process libraries** page, right-click the library to update, publish, or delete.</span></span> <span data-ttu-id="80ef4-122">ウィンドウの左下で **編集**、**発行**、**削除** のいずれかをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-122">Then, in the lower-left corner of the window, click **Edit**, **Publish**, or **Delete**.</span></span>
    -   <span data-ttu-id="80ef4-123">**編集**では、ライブラリの名前と説明を変更できます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-123">**Edit** lets you change the name and description of the library.</span></span>
    -   <span data-ttu-id="80ef4-124">**公開**は、**コーポレート ライブラリ**のライブラリのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-124">**Publish** creates a copy of the library under **Corporate libraries**.</span></span> <span data-ttu-id="80ef4-125">このライブラリは、組織内の全員が利用できます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-125">This library will be available to everyone in your organization.</span></span>
    -   <span data-ttu-id="80ef4-126">**削除**は、ライブラリとそれに格納されているすべての情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-126">**Delete** deletes the library and any information that is stored in it.</span></span>

## <a name="modify-a-business-process-library"></a><span data-ttu-id="80ef4-127">業務プロセス ライブラリの変更</span><span class="sxs-lookup"><span data-stu-id="80ef4-127">Modify a business process library</span></span>
<span data-ttu-id="80ef4-128">業務プロセス明細行または業務プロセス ライブラリ内の階層を変更または更新するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="80ef4-128">Follow these steps to change or update the business process lines or hierarchy in your business process library.</span></span>

1.  <span data-ttu-id="80ef4-129">更新するライブラリを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-129">Select and open the library to update.</span></span>
2.  <span data-ttu-id="80ef4-130">左ウィンドウの**主要なビュー**で**作成と編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-130">In the left pane, under **Core views**, click **Author and edit**.</span></span>
3.  <span data-ttu-id="80ef4-131">必要な変更をするには、次の 1 つまたは複数の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-131">Follow one or more of these steps to make the required changes:</span></span>
    -   <span data-ttu-id="80ef4-132">業務プロセスの明細行の階層を並べ替えるには、階層内でプロセスをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-132">To rearrange the hierarchy of the business process lines, drag the processes in the hierarchy.</span></span>
    -   <span data-ttu-id="80ef4-133">ノードを削除するには、中央ウィンドウでビジネス プロセスをクリックし、右ウィンドウで **削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-133">To delete a node, click a business process in the center pane, and then click **Delete** in the right pane.</span></span>
    -   <span data-ttu-id="80ef4-134">新しいノードを作成するには、中央ウィンドウの上部にある **新規ビジネス プロセス** フラグを、新しいノードが表示される階層内の場所にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-134">To create a new node, drag the **New Business Process** flag at the top of the center pane to the place in the hierarchy where the new node should appear.</span></span> <span data-ttu-id="80ef4-135">[![BPM\_06](./media/bpm_06.png)](./media/bpm_06.png)</span><span class="sxs-lookup"><span data-stu-id="80ef4-135">[![BPM\_06](./media/bpm_06.png)](./media/bpm_06.png)</span></span>
    -   <span data-ttu-id="80ef4-136">既存の業務プロセス ライブラリから業務プロセスをインポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-136">To import business processes from existing business process libraries, follow these steps:</span></span>
        1.  <span data-ttu-id="80ef4-137">中央のウィンドウの**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-137">Click **Import** in the center pane.</span></span>
        2.  <span data-ttu-id="80ef4-138">表示されるページの右側で、業務プロセスをインポートするライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-138">On the right side of the page that appears, select the library to import business processes from.</span></span>
        3.  <span data-ttu-id="80ef4-139">必須ビジネス プロセスをページ左側の階層にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-139">Drag the required business processes into the hierarchy on the left side of the page.</span></span>

## <a name="view-and-modify-task-recordings-in-a-business-process-library"></a><span data-ttu-id="80ef4-140">業務プロセス ライブラリにあるタスクの記録の表示および変更</span><span class="sxs-lookup"><span data-stu-id="80ef4-140">View and modify task recordings in a business process library</span></span>
1.  <span data-ttu-id="80ef4-141">作業するライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-141">Open the library that you want to work in.</span></span>
2.  <span data-ttu-id="80ef4-142">関連付けられたタスク記録がある業務プロセスの明細行に移動し、リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-142">Navigate to the business process line that has a task recording associated with it, and click the link.</span></span>
3.  <span data-ttu-id="80ef4-143">手動でフロー チャートを変更するには、**Activities** の下にタイルをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-143">Drag the tiles under **Activities** to manually modify the flow chart.</span></span> <span data-ttu-id="80ef4-144">[![BPM\_09](./media/bpm_09.png)](./media/bpm_09.png)</span><span class="sxs-lookup"><span data-stu-id="80ef4-144">[![BPM\_09](./media/bpm_09.png)](./media/bpm_09.png)</span></span>
4.  <span data-ttu-id="80ef4-145">変更されたフローチャートの Microsoft Visio 図をアップロードするには、**Visio** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-145">To upload a Microsoft Visio diagram of the modified flow chart, click the **Visio** tab.</span></span>

## <a name="structure-a-business-process-library"></a><span data-ttu-id="80ef4-146">業務プロセス ライブラリの構造化</span><span class="sxs-lookup"><span data-stu-id="80ef4-146">Structure a business process library</span></span>
<span data-ttu-id="80ef4-147">ビジネス プロセス ライブラリには、**主要な業務プロセス**と**サポート プロセス**という 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-147">There are two sections in business process libraries: **Core Business Processes** and **Support Processes**.</span></span> <span data-ttu-id="80ef4-148">**コア ビジネス プロセス** セクションには、ソリューションのすべてのカスタム業務プロセスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-148">The **Core Business Processes** section should include all custom business processes for your solution.</span></span> <span data-ttu-id="80ef4-149">すべてのカスタマイズおよび機能をエンドツーエンドのシナリオでカバーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-149">All customizations and functionality should be covered in end-to-end scenarios.</span></span> <span data-ttu-id="80ef4-150">タスク記録は、このセクションのすべてのプロセスに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-150">Task recordings should be created for all processes in this section.</span></span> <span data-ttu-id="80ef4-151">ソリューションに関連するアメリカ生産性品質センター (APQC) の処理を、**サポート プロセス** セクションにインポートします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-151">Import American Productivity & Quality Center (APQC) processes that are relevant to your solution into the **Support Processes** section.</span></span> <span data-ttu-id="80ef4-152">このセクションには、カスタム ビジネス プロセスは含まれません。</span><span class="sxs-lookup"><span data-stu-id="80ef4-152">This section should not include any custom business processes.</span></span> <span data-ttu-id="80ef4-153">このセクションのプロセスのタスク記録を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="80ef4-153">You don't have to create task recordings for processes in this section.</span></span> <span data-ttu-id="80ef4-154">業務プロセス ライブラリを、方法およびマーケティング材料にある説明およびサマリと一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-154">Your business process library should be aligned with the descriptions and summaries in your methodology and your marketing material.</span></span>

## <a name="create-a-task-recording-and-associate-it-with-a-business-process"></a><span data-ttu-id="80ef4-155">タスク記録を作成し、業務プロセスに関連付ける</span><span class="sxs-lookup"><span data-stu-id="80ef4-155">Create a task recording and associate it with a business process</span></span>
<span data-ttu-id="80ef4-156">カスタム データとカスタマイズを持つ Microsoft Finance and Operations 環境では、タスク記録を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-156">Task recordings should be created in a Microsoft Finance and Operations environment that has your custom data and customizations.</span></span> <span data-ttu-id="80ef4-157">タスク レコーダーに関する参照情報については、「[Microsoft Dynamics 365 for Finance and Operations のタスク レコーダー](../user-interface/task-recorder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80ef4-157">For reference information about Task recorder, see [Task Recorder in Microsoft Dynamics 365 for Finance and Operations](../user-interface/task-recorder.md).</span></span>

### <a name="create-a-task-recording"></a><span data-ttu-id="80ef4-158">タスク記録の作成</span><span class="sxs-lookup"><span data-stu-id="80ef4-158">Create a task recording</span></span>

1.  <span data-ttu-id="80ef4-159">Finance and Operations で、右上隅にある**設定**ボタンをクリックしてから、**タスク レコーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-159">In Finance and Operations, click the **Settings** button in the upper-right corner, and then click **Task recorder**.</span></span>
2.  <span data-ttu-id="80ef4-160">**記録の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-160">Click **Create recording**.</span></span>
3.  <span data-ttu-id="80ef4-161">記録の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-161">Enter a name and description for the recording.</span></span>
4.  <span data-ttu-id="80ef4-162">記録するタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-162">Perform the task that you want to record.</span></span>
5.  <span data-ttu-id="80ef4-163">タスクを終了したら、**停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-163">When you've completed the task, click **Stop**.</span></span>
6.  <span data-ttu-id="80ef4-164">新しいタスク記録を LCS にアップロードする場合は、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-164">If you want to upload your new task recording to LCS, continue to the next section.</span></span> <span data-ttu-id="80ef4-165">記録をローカル コンピューターに保存するか、記録を Microsoft Word ドキュメントに変換するには、適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-165">To save your recording to your local computer or convert the recording to a Microsoft Word document, select the appropriate option.</span></span>

### <a name="associate-a-task-recording-with-a-business-process"></a><span data-ttu-id="80ef4-166">タスク記録と業務プロセスの関連付け</span><span class="sxs-lookup"><span data-stu-id="80ef4-166">Associate a task recording with a business process</span></span>

1.  <span data-ttu-id="80ef4-167">**LCS に保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-167">Click **Save to LCS**.</span></span>
2.  <span data-ttu-id="80ef4-168">業務プロセス ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-168">Select a business process library.</span></span>
3.  <span data-ttu-id="80ef4-169">記録に関連付ける業務プロセス ラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-169">Select the business process line to associate with the recording.</span></span>
4.  <span data-ttu-id="80ef4-170">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-170">Click **OK**.</span></span>

<span data-ttu-id="80ef4-171">LCS の業務プロセス ライブラリで記録するタスクを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="80ef4-171">You can now view the task recording in the business process library in LCS.</span></span>

## <a name="set-up-and-use-task-guides"></a><span data-ttu-id="80ef4-172">タスク ガイドの設定および使用</span><span class="sxs-lookup"><span data-stu-id="80ef4-172">Set up and use task guides</span></span>
<span data-ttu-id="80ef4-173">タスク記録はタスク ガイドとして再生できます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-173">Task recordings can be played as task guides.</span></span> <span data-ttu-id="80ef4-174">タスク ガイドは、業務プロセスを完了するための手順をユーザーに説明するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-174">Task guides are used to guide users through the steps for completing business processes.</span></span> <span data-ttu-id="80ef4-175">タスク ガイドを設定して使用する前に、タスク記録を作成し LCS の業務プロセス ライブラリに保存してください。</span><span class="sxs-lookup"><span data-stu-id="80ef4-175">Before you set up and use task guides, create task recordings and save them to a business process library in LCS.</span></span>

### <a name="set-up-task-guides"></a><span data-ttu-id="80ef4-176">タスク ガイドの設定</span><span class="sxs-lookup"><span data-stu-id="80ef4-176">Set up task guides</span></span>

1.  <span data-ttu-id="80ef4-177">Finance and Operations で、**システム管理** &gt; **設定** &gt; **システム パラメータ**をクリックしてから、**ヘルプ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-177">In Finance and Operations, click **System administration** &gt; **Setup** &gt; **System parameters**, and then click the **Help** tab.</span></span>
2.  <span data-ttu-id="80ef4-178">連携する業務プロセス ライブラリが格納されている LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-178">Select the LCS project where the business process library that you want to work with is stored.</span></span>
3.  <span data-ttu-id="80ef4-179">タスク ガイドとして再生するタスクの記録を持つ業務プロセス ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-179">Select the business process libraries that have the task recordings that you want to play as task guides.</span></span>
4.  <span data-ttu-id="80ef4-180">必要に応じて業務プロセス ライブラリの順序を調整します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-180">Adjust the order of the business process libraries as required.</span></span> <span data-ttu-id="80ef4-181">ビジネス プロセス ライブラリの順序によって、タスク ガイドが表示される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="80ef4-181">The order of the business process libraries determines the order that the task guides appear in.</span></span> <span data-ttu-id="80ef4-182">したがって、ユーザーがタスク ガイド機能を使用すると、最初のビジネス プロセス ライブラリのタスク ガイドが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-182">Therefore, the task guides for the first business process library appear first when a user uses the task guide functionality.</span></span>

### <a name="use-task-guides"></a><span data-ttu-id="80ef4-183">タスク ガイドの使用</span><span class="sxs-lookup"><span data-stu-id="80ef4-183">Use task guides</span></span>

1.  <span data-ttu-id="80ef4-184">Finance and Operations で、タスク ガイドを実行するページを開きます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-184">In Finance and Operations, open the page where you want to run the task guide.</span></span>
2.  <span data-ttu-id="80ef4-185">右上隅にある**設定**ボタンをクリックしてから、**タスク レコーダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-185">In the upper-right corner, click the **Settings** button, and then click **Task recorder**.</span></span>
3.  <span data-ttu-id="80ef4-186">タスク ガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="80ef4-186">Select a task guide.</span></span>
4.  <span data-ttu-id="80ef4-187">**タスク ガイドの開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-187">Click **Start Task guide**.</span></span>
5.  <span data-ttu-id="80ef4-188">タスク ガイドのステップに従います。</span><span class="sxs-lookup"><span data-stu-id="80ef4-188">Follow the steps in the task guide.</span></span> <span data-ttu-id="80ef4-189">**ロック解除**をクリックすると、タスク ガイドに従わずに処理することができます。</span><span class="sxs-lookup"><span data-stu-id="80ef4-189">If you click **Unlock**, you can work without following the task guide.</span></span>
6.  <span data-ttu-id="80ef4-190">完了したら、**タスク ガイドの停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="80ef4-190">When you've finished, click **Stop Task guide**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="80ef4-191">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="80ef4-191">Additional resources</span></span>
--------

[<span data-ttu-id="80ef4-192">AppSource 向け LCS ソリューション ホームページ</span><span class="sxs-lookup"><span data-stu-id="80ef4-192">LCS Solutions for AppSource home page</span></span>](lcs-solutions-app-source.md)



