---
title: ビジネス プロセス モデラーのライブラリ (更新された BPM エクスペリエンス )
description: このトピックでは、更新されたビジネス プロセス モデラー (BPM) ライブラリ エクスペリエンスを作成して使用する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Lifecycle Services
ms.custom: 196953
ms.assetid: 6e7h6896-edef-4739-98ad-c9ea12880972
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: 8d49906a7e9630dff52de2540045873273e80d93
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811710"
---
# <a name="business-process-modeler-library-updated-bpm-experience"></a><span data-ttu-id="9b618-103">ビジネス プロセス モデラーのライブラリ (更新された BPM エクスペリエンス )</span><span class="sxs-lookup"><span data-stu-id="9b618-103">Business process modeler library (updated BPM experience)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b618-104">このトピックでは、ビジネス プロセス モデラー (BPM) ライブラリを作成して使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b618-104">This topic explains how to create and work with Business process modeler (BPM) libraries.</span></span>

<a name="create-a-business-process-library"></a><span data-ttu-id="9b618-105">業務プロセス ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="9b618-105">Create a business process library</span></span>
---------------------------------

<span data-ttu-id="9b618-106">BPM ライブラリを作成する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-106">There are two ways to create a BPM library.</span></span> <span data-ttu-id="9b618-107">明細行記録またはタスク記録がない新しいライブラリを作成、または既存のライブラリをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="9b618-107">You can create a new library that has no lines or task recordings, or you can copy an existing library.</span></span>

1.  <span data-ttu-id="9b618-108">Microsoft Dynamics Lifecycle Services (LCS) で、プロジェクトを開き、**追加ツール** セクションが表示されるまで右にスクロールしてから、**ビジネス プロセス モデラー** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-108">In Microsoft Dynamics Lifecycle Services (LCS), open a project, scroll to the right until you see the **More tools** section, and then select the **Business process modeler** tile.</span></span> <span data-ttu-id="9b618-109">３ つのセクション (ライブラリのタイプごとに1つずつ) が表示される **業務プロセス ライブラリ** ページ:</span><span class="sxs-lookup"><span data-stu-id="9b618-109">The **Business process libraries** page that appears has three sections, one for each type of library:</span></span>

    -   <span data-ttu-id="9b618-110">**自分のライブラリ** – ユーザーが作成または追加したビジネス プロセス。</span><span class="sxs-lookup"><span data-stu-id="9b618-110">**My libraries** – Business processes that users have created or added.</span></span>
    -   <span data-ttu-id="9b618-111">**コーポレート ライブラリ** - 組織内のユーザーがアップロードした独自の業務プロセス。</span><span class="sxs-lookup"><span data-stu-id="9b618-111">**Corporate libraries** – Custom business processes that someone in your organization has uploaded.</span></span>
    -   <span data-ttu-id="9b618-112">**グローバル ライブラリ** – 産業間の標準の業務プロセス。</span><span class="sxs-lookup"><span data-stu-id="9b618-112">**Global libraries** – Cross-industry standard business processes.</span></span>

    <span data-ttu-id="9b618-113">[![業務プロセス ライブラリページの 3 種類のライブラリ](./media/bpm_02.png)](./media/bpm_02.png)</span><span class="sxs-lookup"><span data-stu-id="9b618-113">[![Three types of libraries on the Business process libraries page](./media/bpm_02.png)](./media/bpm_02.png)</span></span>

2.  <span data-ttu-id="9b618-114">新しいライブラリを作成するには、任意のライブラリを右クリックし、ウィンドウの左下隅にある**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-114">To create a new library, right-click any library, and then, in the lower-left corner of the window, select **Create**.</span></span> <span data-ttu-id="9b618-115">既存のライブラリをコピーするには、そのライブラリを右クリックし、ウィンドウの左下隅にある**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-115">To copy an existing library, right-click that library, and then, in the lower-left corner of the window, select **Copy**.</span></span>

    <span data-ttu-id="9b618-116">[![コピー ボタンの場所](./media/bpm_03.png)](./media/bpm_03.png)</span><span class="sxs-lookup"><span data-stu-id="9b618-116">[![Location of the Copy button](./media/bpm_03.png)](./media/bpm_03.png)</span></span>

    -   <span data-ttu-id="9b618-117">**グローバル ライブラリ** – 産業間の標準の業務プロセス。</span><span class="sxs-lookup"><span data-stu-id="9b618-117">**Global libraries** – Cross-industry standard business processes.</span></span> 
    
    <span data-ttu-id="9b618-118">[![業務プロセス ライブラリページの 3 種類のライブラリ](./media/bpm_02.png)](./media/bpm_02.png)</span><span class="sxs-lookup"><span data-stu-id="9b618-118">[![Three types of libraries on the Business process libraries page](./media/bpm_02.png)](./media/bpm_02.png)</span></span>

3.  <span data-ttu-id="9b618-119">ライブラリ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b618-119">Enter a name for the library.</span></span>

<span data-ttu-id="9b618-120">今作成したライブラリは、**自分のライブラリ** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b618-120">The library that you created now appears under **My libraries**.</span></span>

## <a name="update-publish-or-delete-a-business-process-library"></a><span data-ttu-id="9b618-121">ビジネス・プロセス・ライブラリの更新、発行、または削除</span><span class="sxs-lookup"><span data-stu-id="9b618-121">Update, publish, or delete a business process library</span></span>
<span data-ttu-id="9b618-122">ライブラリの名前または説明を変更、組織内の他の人が表示できるようにライブラリを公開、またはライブラリを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="9b618-122">You can change the name or description of a library, publish a library so that other people in your organization can view it, or delete a library.</span></span>

-   <span data-ttu-id="9b618-123">**業務プロセス ライブラリ**ページで、右クリックしてライブラリを更新、公開、または削除します。</span><span class="sxs-lookup"><span data-stu-id="9b618-123">On the **Business process libraries** page, right-click the library to update, publish, or delete.</span></span> <span data-ttu-id="9b618-124">ウィンドウの左下で**編集**、**発行**、**削除**のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-124">Then, in the lower-left corner of the window, select **Edit**, **Publish**, or **Delete**.</span></span>

    -   <span data-ttu-id="9b618-125">**編集**では、ライブラリの名前と説明を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9b618-125">**Edit** lets you change the name and description of the library.</span></span>
    -   <span data-ttu-id="9b618-126">**公開**は、**コーポレート ライブラリ**のライブラリのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="9b618-126">**Publish** creates a copy of the library under **Corporate libraries**.</span></span> <span data-ttu-id="9b618-127">このライブラリは、組織内の全員が利用できます。</span><span class="sxs-lookup"><span data-stu-id="9b618-127">This library will be available to everyone in your organization.</span></span>
    -   <span data-ttu-id="9b618-128">**削除**は、ライブラリとそれに格納されているすべての情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="9b618-128">**Delete** deletes the library and any information that is stored in it.</span></span>

## <a name="modify-a-business-process-library"></a><span data-ttu-id="9b618-129">業務プロセス ライブラリの変更</span><span class="sxs-lookup"><span data-stu-id="9b618-129">Modify a business process library</span></span>
<span data-ttu-id="9b618-130">業務プロセス明細行または業務プロセス ライブラリ内の階層を変更または更新するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9b618-130">Follow these steps to change or update the business process lines or hierarchy in your business process library.</span></span>

1.  <span data-ttu-id="9b618-131">更新するライブラリを選択して開きます。</span><span class="sxs-lookup"><span data-stu-id="9b618-131">Select and open the library to update.</span></span>
2.  <span data-ttu-id="9b618-132">左ウィンドウの**主要なビュー**で**作成と編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-132">In the left pane, under **Core views**, select **Author and edit**.</span></span>
3.  <span data-ttu-id="9b618-133">必要な変更をするには、次の 1 つまたは複数の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9b618-133">Follow one or more of these steps to make the required changes:</span></span>

    -   <span data-ttu-id="9b618-134">業務プロセスの明細行の階層を並べ替えるには、階層内でプロセスをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="9b618-134">To rearrange the hierarchy of the business process lines, drag the processes in the hierarchy.</span></span>
    -   <span data-ttu-id="9b618-135">ノードを削除するには、中央ウィンドウでビジネス プロセスを選択し、右ウィンドウで**削除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-135">To delete a node, select a business process in the center pane, and then select **Delete** in the right pane.</span></span>
    -   <span data-ttu-id="9b618-136">新しいノードを作成するには、中央ウィンドウの上部にある **新規ビジネス プロセス** フラグを、新しいノードが表示される階層内の場所にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="9b618-136">To create a new node, drag the **New Business Process** flag at the top of the center pane to the place in the hierarchy where the new node should appear.</span></span>

        <span data-ttu-id="9b618-137">[![新しい業務プロセス フラグ](./media/bpm_06.png)](./media/bpm_06.png)</span><span class="sxs-lookup"><span data-stu-id="9b618-137">[![New Business Process flag](./media/bpm_06.png)](./media/bpm_06.png)</span></span>

    -   <span data-ttu-id="9b618-138">既存の業務プロセス ライブラリから業務プロセスをインポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9b618-138">To import business processes from existing business process libraries, follow these steps:</span></span>

        1.  <span data-ttu-id="9b618-139">中央のウィンドウの**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-139">Select **Import** in the center pane.</span></span>
        2.  <span data-ttu-id="9b618-140">表示されるページの右側で、業務プロセスをインポートするライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-140">On the right side of the page that appears, select the library to import business processes from.</span></span>
        3.  <span data-ttu-id="9b618-141">必須ビジネス プロセスをページ左側の階層にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="9b618-141">Drag the required business processes into the hierarchy on the left side of the page.</span></span>

## <a name="view-and-modify-task-recordings-in-a-business-process-library"></a><span data-ttu-id="9b618-142">業務プロセス ライブラリにあるタスクの記録の表示および変更</span><span class="sxs-lookup"><span data-stu-id="9b618-142">View and modify task recordings in a business process library</span></span>
1.  <span data-ttu-id="9b618-143">作業するライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b618-143">Open the library that you want to work in.</span></span>
2.  <span data-ttu-id="9b618-144">関連付けられたタスク記録がある業務プロセスの明細行に移動し、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-144">Navigate to the business process line that has a task recording associated with it, and select the link.</span></span>
3.  <span data-ttu-id="9b618-145">手動でフロー チャートを変更するには、**Activities** の下にタイルをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="9b618-145">Drag the tiles under **Activities** to manually modify the flow chart.</span></span>

    <span data-ttu-id="9b618-146">[![フロー チャートを手動で変更](./media/bpm_09.png)](./media/bpm_09.png)</span><span class="sxs-lookup"><span data-stu-id="9b618-146">[![Manually modifying the flow chart](./media/bpm_09.png)](./media/bpm_09.png)</span></span>

4.  <span data-ttu-id="9b618-147">変更されたフローチャートの Microsoft Visio 図をアップロードするには、**Visio** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-147">To upload a Microsoft Visio diagram of the modified flow chart, select the **Visio** tab.</span></span>

## <a name="structure-a-business-process-library"></a><span data-ttu-id="9b618-148">業務プロセス ライブラリの構造化</span><span class="sxs-lookup"><span data-stu-id="9b618-148">Structure a business process library</span></span>
<span data-ttu-id="9b618-149">ビジネス プロセス ライブラリには、**主要な業務プロセス**と**サポート プロセス**という 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="9b618-149">There are two sections in business process libraries: **Core Business Processes** and **Support Processes**.</span></span> <span data-ttu-id="9b618-150">**コア ビジネス プロセス** セクションには、ソリューションのすべてのカスタム業務プロセスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-150">The **Core Business Processes** section should include all custom business processes for your solution.</span></span> <span data-ttu-id="9b618-151">すべてのカスタマイズおよび機能をエンドツーエンドのシナリオでカバーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-151">All customizations and functionality should be covered in end-to-end scenarios.</span></span> <span data-ttu-id="9b618-152">タスク記録は、このセクションのすべてのプロセスに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-152">Task recordings should be created for all processes in this section.</span></span> <span data-ttu-id="9b618-153">ソリューションに関連するアメリカ生産性品質センター (APQC) の処理を、**サポート プロセス** セクションにインポートします。</span><span class="sxs-lookup"><span data-stu-id="9b618-153">Import American Productivity & Quality Center (APQC) processes that are relevant to your solution into the **Support Processes** section.</span></span> <span data-ttu-id="9b618-154">このセクションには、カスタム ビジネス プロセスは含まれません。</span><span class="sxs-lookup"><span data-stu-id="9b618-154">This section should not include any custom business processes.</span></span> <span data-ttu-id="9b618-155">このセクションのプロセスのタスク記録を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9b618-155">You don't have to create task recordings for processes in this section.</span></span> <span data-ttu-id="9b618-156">業務プロセス ライブラリを、方法およびマーケティング材料にある説明およびサマリと一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-156">Your business process library should be aligned with the descriptions and summaries in your methodology and your marketing material.</span></span>

## <a name="create-a-task-recording-and-associate-it-with-a-business-process"></a><span data-ttu-id="9b618-157">タスク記録を作成し、業務プロセスに関連付ける</span><span class="sxs-lookup"><span data-stu-id="9b618-157">Create a task recording and associate it with a business process</span></span>

<span data-ttu-id="9b618-158">カスタム データとカスタマイズを持つ環境では、タスク記録を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b618-158">Task recordings should be created in an environment that has your custom data and customizations.</span></span> <span data-ttu-id="9b618-159">タスク レコーダーの詳細については、 [タスク レコーダー の リソース](../user-interface/task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b618-159">For reference information about Task recorder, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>

### <a name="create-a-task-recording"></a><span data-ttu-id="9b618-160">タスク記録の作成</span><span class="sxs-lookup"><span data-stu-id="9b618-160">Create a task recording</span></span>

1.  <span data-ttu-id="9b618-161">アプリケーションで、右上隅にある**設定**ボタンを選択してから、**タスク レコーダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-161">In the application, select the **Settings** button in the upper-right corner, and then select **Task recorder**.</span></span>
2.  <span data-ttu-id="9b618-162">**記録の作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-162">Select **Create recording**.</span></span>
3.  <span data-ttu-id="9b618-163">記録の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9b618-163">Enter a name and description for the recording.</span></span>
4.  <span data-ttu-id="9b618-164">記録するタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9b618-164">Perform the task that you want to record.</span></span>
5.  <span data-ttu-id="9b618-165">タスクを終了したら、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-165">When you've completed the task, select **Stop**.</span></span>
6.  <span data-ttu-id="9b618-166">新しいタスク記録を LCS にアップロードする場合は、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="9b618-166">If you want to upload your new task recording to LCS, continue to the next section.</span></span> <span data-ttu-id="9b618-167">記録をローカル コンピューターに保存するか、記録を Microsoft Word ドキュメントに変換するには、適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-167">To save your recording to your local computer or convert the recording to a Microsoft Word document, select the appropriate option.</span></span>

### <a name="associate-a-task-recording-with-a-business-process"></a><span data-ttu-id="9b618-168">タスク記録と業務プロセスの関連付け</span><span class="sxs-lookup"><span data-stu-id="9b618-168">Associate a task recording with a business process</span></span>

1.  <span data-ttu-id="9b618-169">**LCS に保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-169">Select **Save to LCS**.</span></span>
2.  <span data-ttu-id="9b618-170">業務プロセス ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-170">Select a business process library.</span></span>
3.  <span data-ttu-id="9b618-171">記録に関連付ける業務プロセス ラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-171">Select the business process line to associate with the recording.</span></span>
4.  <span data-ttu-id="9b618-172">**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-172">Select **OK**.</span></span>

<span data-ttu-id="9b618-173">LCS の業務プロセス ライブラリで記録するタスクを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b618-173">You can now view the task recording in the business process library in LCS.</span></span>

## <a name="set-up-and-use-task-guides"></a><span data-ttu-id="9b618-174">タスク ガイドの設定および使用</span><span class="sxs-lookup"><span data-stu-id="9b618-174">Set up and use task guides</span></span>
<span data-ttu-id="9b618-175">タスク記録はタスク ガイドとして再生できます。</span><span class="sxs-lookup"><span data-stu-id="9b618-175">Task recordings can be played as task guides.</span></span> <span data-ttu-id="9b618-176">タスク ガイドは、業務プロセスを完了するための手順をユーザーに説明するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b618-176">Task guides are used to guide users through the steps for completing business processes.</span></span> <span data-ttu-id="9b618-177">タスク ガイドを設定して使用する前に、タスク記録を作成し、LCS の業務プロセス ライブラリに保存してください。</span><span class="sxs-lookup"><span data-stu-id="9b618-177">Before you set up and use task guides, create task recordings, and save them to a business process library in LCS.</span></span>

### <a name="set-up-task-guides"></a><span data-ttu-id="9b618-178">タスク ガイドの設定</span><span class="sxs-lookup"><span data-stu-id="9b618-178">Set up task guides</span></span>

1.  <span data-ttu-id="9b618-179">アプリケーションで、**システム管理** &gt; **設定** &gt; **システム パラメーター**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-179">In the application, select **System administration** &gt; **Setup** &gt; **System parameters**.</span></span>
2.  <span data-ttu-id="9b618-180">**ヘルプ**タブで、連携する業務プロセス ライブラリが格納されている LCS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-180">On the **Help** tab, select the LCS project where the business process library that you want to work with is stored.</span></span>
3.  <span data-ttu-id="9b618-181">タスク ガイドとして再生するタスクの記録を持つ業務プロセス ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-181">Select the business process libraries that have the task recordings that you want to play as task guides.</span></span>
4.  <span data-ttu-id="9b618-182">必要に応じて業務プロセス ライブラリの順序を調整します。</span><span class="sxs-lookup"><span data-stu-id="9b618-182">Adjust the order of the business process libraries as you require.</span></span> <span data-ttu-id="9b618-183">ビジネス プロセス ライブラリの順序によって、タスク ガイドが表示される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="9b618-183">The order of the business process libraries determines the order that the task guides appear in.</span></span> <span data-ttu-id="9b618-184">したがって、ユーザーがタスク ガイド機能を使用すると、最初のビジネス プロセス ライブラリのタスク ガイドが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b618-184">Therefore, the task guides for the first business process library appear first when a user uses the task guide functionality.</span></span>

### <a name="use-task-guides"></a><span data-ttu-id="9b618-185">タスク ガイドの使用</span><span class="sxs-lookup"><span data-stu-id="9b618-185">Use task guides</span></span>

1.  <span data-ttu-id="9b618-186">アプリケーションで、タスク ガイドを実行するページを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b618-186">In the application, open the page where you want to run the task guide.</span></span>
2.  <span data-ttu-id="9b618-187">右上隅にある**設定**ボタンを選択してから、**タスク レコーダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-187">In the upper-right corner, select the **Settings** button, and then select **Task recorder**.</span></span>
3.  <span data-ttu-id="9b618-188">タスク ガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-188">Select a task guide.</span></span>
4.  <span data-ttu-id="9b618-189">**タスク ガイドの開始**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-189">Select **Start Task guide**.</span></span>
5.  <span data-ttu-id="9b618-190">タスク ガイドのステップに従います。</span><span class="sxs-lookup"><span data-stu-id="9b618-190">Follow the steps in the task guide.</span></span> <span data-ttu-id="9b618-191">**ロック解除**を選択すると、タスク ガイドに従わずに処理することができます。</span><span class="sxs-lookup"><span data-stu-id="9b618-191">If you select **Unlock**, you can work without following the task guide.</span></span>
6.  <span data-ttu-id="9b618-192">完了したら、**タスク ガイドの停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9b618-192">When you've finished, select **Stop Task guide**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="9b618-193">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9b618-193">Additional resources</span></span>
--------

[<span data-ttu-id="9b618-194">AppSource でアプリを公開するための要件</span><span class="sxs-lookup"><span data-stu-id="9b618-194">Requirements for publishing apps on AppSource</span></span>](lcs-solutions-app-source.md)
