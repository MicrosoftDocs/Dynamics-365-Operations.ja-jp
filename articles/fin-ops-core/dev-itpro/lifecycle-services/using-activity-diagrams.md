---
title: ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する
description: このトピックでは、BPM ライブラリでアクティビティ図を使用する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: c779d8e3effbb11f05c77f795354cd03f8b42cca
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627573"
---
# <a name="work-with-activity-diagrams-in-business-process-modeler-libraries"></a><span data-ttu-id="9621f-103">ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する</span><span class="sxs-lookup"><span data-stu-id="9621f-103">Work with activity diagrams in Business process modeler libraries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9621f-104">活動ダイアグラムを業務プロセスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-104">You can associate an activity diagram with a business process.</span></span> <span data-ttu-id="9621f-105">活動ダイアグラムは、提案されたソフトウェア ソリューションで業務プロセスまたはタスクを完了する方法について記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9621f-105">Activity diagrams are used to describe how a business process or task is completed in a proposed software solution.</span></span>

<span data-ttu-id="9621f-106">活動ダイアグラムには 3 つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="9621f-106">There are three types of activity diagrams:</span></span>

- <span data-ttu-id="9621f-107">**タスク記録** – Finance and Operations のタスク記録に関連する業務プロセスには、自動的に生成される活動ダイアグラムおよびプロセスの手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9621f-107">**Task recordings** – Business processes that are associated with task recordings for Finance and Operations, include activity diagrams and process steps that are automatically generated.</span></span>
- <span data-ttu-id="9621f-108">**Microsoft Visio** – Visio ファイルを手動でアップロードすることによって、業務プロセスを Visio 図に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-108">**Microsoft Visio** – You can associate a business process with a Visio diagram by manually uploading a Visio file.</span></span>
- <span data-ttu-id="9621f-109">**ユーザー定義** – ビジネス プロセス モデラー (BPM) 活動ダイアグラムを手動で作成または編集できます。</span><span class="sxs-lookup"><span data-stu-id="9621f-109">**User-defined** – You can manually create or edit a Business process modeler (BPM) activity diagram.</span></span>

<span data-ttu-id="9621f-110">アクティビティ図に加え、詳細なプロセスの手順を使用して業務プロセスを記述できます。</span><span class="sxs-lookup"><span data-stu-id="9621f-110">In addition to activity diagrams, you can describe a business process by using detailed process steps.</span></span>

## <a name="browse-activity-diagrams"></a><span data-ttu-id="9621f-111">活動ダイアグラムの参照</span><span class="sxs-lookup"><span data-stu-id="9621f-111">Browse activity diagrams</span></span>
<span data-ttu-id="9621f-112">BPM ライブラリ内の **図** 列は、特定の業務プロセスがアクティビティ図に関連付けられているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9621f-112">The **Diagrams** column in your BPM library indicates whether a particular business process is associated with an activity diagram.</span></span> <span data-ttu-id="9621f-113">列の番号は、ダイアグラムを含む子プロセスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="9621f-113">The number in the column indicates the number of child processes that include diagrams.</span></span> <span data-ttu-id="9621f-114">番号の横にあるシンボルは、現在のノードまたはプロセスがダイアグラムに関連付けられているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9621f-114">The symbol next to the number indicates whether the current node or process is associated with a diagram.</span></span> <span data-ttu-id="9621f-115">これらのインジケーターは、Visio ダイアグラムには適用されません。</span><span class="sxs-lookup"><span data-stu-id="9621f-115">These indicators don't apply to Visio diagrams.</span></span>

<span data-ttu-id="9621f-116">[![monitoringanddiagnostics01](./media/browse_activity_diagrams.JPG)](./media/browse_activity_diagrams.JPG)</span><span class="sxs-lookup"><span data-stu-id="9621f-116">[![monitoringanddiagnostics01](./media/browse_activity_diagrams.JPG)](./media/browse_activity_diagrams.JPG)</span></span>

<span data-ttu-id="9621f-117">アクティビティ図を表示または編集するには、業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9621f-117">To view or edit an activity diagram, select the business process, and then, in the right pane, on the **Overview** tab, select **Diagrams**.</span></span> <span data-ttu-id="9621f-118">**フローチャート** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9621f-118">The **Flowchart** page appears.</span></span>

## <a name="upload-task-recording"></a><span data-ttu-id="9621f-119">作業記録のアップロード</span><span class="sxs-lookup"><span data-stu-id="9621f-119">Upload Task Recording</span></span>
<span data-ttu-id="9621f-120">タスク記録をアップロードするには、アップロードする業務プロセス ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="9621f-120">To upload a task recording, open the business process library that you want to upload to.</span></span> <span data-ttu-id="9621f-121">タスクの記録をアップロードするプロセス手順を選択し、**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9621f-121">Select the process step that you want to upload the task recording to, and then click **Upload**.</span></span>

<span data-ttu-id="9621f-122">[![activitydiagrams01](./media/activity_diagrams_01.jpg)](./media/activity_diagrams_01.jpg)</span><span class="sxs-lookup"><span data-stu-id="9621f-122">[![activitydiagrams01](./media/activity_diagrams_01.jpg)](./media/activity_diagrams_01.jpg)</span></span>


<span data-ttu-id="9621f-123">右ウィンドウで、**参照**をクリックしてファイルを選択してから**アップロード**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9621f-123">In the right pane, click **Browse** to choose a file, and then click **Upload**.</span></span>

<span data-ttu-id="9621f-124">[![activitydiagrams02](./media/activity_diagrams_02.jpg)](./media/activity_diagrams_02.jpg)</span><span class="sxs-lookup"><span data-stu-id="9621f-124">[![activitydiagrams02](./media/activity_diagrams_02.jpg)](./media/activity_diagrams_02.jpg)</span></span>


## <a name="activity-diagrams-that-are-created-from-task-recordings"></a><span data-ttu-id="9621f-125">タスク記録から作成された活動ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="9621f-125">Activity diagrams that are created from task recordings</span></span>
<span data-ttu-id="9621f-126">環境でタスク記録を作成して、Microsoft Dynamics Lifecycle Services (LCS) に直接保存することができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-126">You can create a task recording in your environment and save it directly to Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9621f-127">この方法で、タスク記録を BPM ライブラリ内の業務プロセスと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-127">In this way, you can associate the task recording with a business process in a BPM library.</span></span> <span data-ttu-id="9621f-128">詳細については、[ヘルプ システムに接続する](../../fin-ops/get-started/help-connect.md) および [ドキュメントの作成またはタスク記録を使用してトレーニングする](../user-interface/task-recorder-training-docs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9621f-128">For more information, see [Connecting the help system](../../fin-ops/get-started/help-connect.md) and [Create documentation or training using task recordings](../user-interface/task-recorder-training-docs.md).</span></span>

<span data-ttu-id="9621f-129">タスク レコーダー ツールを使用すると、配布可能な記録ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9621f-129">The Task recorder tool lets you create a distributable recording file.</span></span> <span data-ttu-id="9621f-130">記録ファイルは、.axtr ファイル名拡張子を持ちます。</span><span class="sxs-lookup"><span data-stu-id="9621f-130">Recording files have the .axtr file name extension.</span></span> <span data-ttu-id="9621f-131">手動で記録ファイルをアップロードすることにより、BPM 内の業務プロセスをタスク記録に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-131">You can associate a business process in BPM with a task recording by manually uploading the recording file.</span></span> 

<span data-ttu-id="9621f-132">記録ファイルをアップロードするには、業務プロセスを選択し、右ウィンドウの **概要** タブで **アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9621f-132">To upload a recording file, select the business process, and then, in the right pane, on the **Overview** tab, select **Upload**.</span></span>

<span data-ttu-id="9621f-133">BPM は作成されたすべてのタスク記録の活動ダイアグラムと詳細なプロセスの手順を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="9621f-133">BPM automatically generates an activity diagram and detailed process steps for all task recordings that are created.</span></span> <span data-ttu-id="9621f-134">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="9621f-134">The following illustration shows an example.</span></span>

<span data-ttu-id="9621f-135">![活動ダイアグラムおよびタスク記録プロセスの手順の例](./media/NEWBPM_BlogPost17-1024x483.png "活動ダイアグラムおよびタスク記録プロセスの手順の例")</span><span class="sxs-lookup"><span data-stu-id="9621f-135">![Example of an activity diagram and process steps for a task recording](./media/NEWBPM_BlogPost17-1024x483.png "Example of an activity diagram and process steps for a task recording")</span></span>

## <a name="edit-activity-diagrams"></a><span data-ttu-id="9621f-136">活動ダイアグラムを編集</span><span class="sxs-lookup"><span data-stu-id="9621f-136">Edit activity diagrams</span></span>
<span data-ttu-id="9621f-137">アクティビティ図を編集するには、フローチャートの空白部分を右クリックし、下部のツールバーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9621f-137">To edit an activity diagram, right-click on a blank area of the flowchart, and then, on the bottom toolbar, select **Edit**.</span></span> <span data-ttu-id="9621f-138">BPM フローチャートの詳細については、[ビジネス プロセス モデラーのフローチャート](flowcharts-business-process-modeler.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9621f-138">For more information about BPM flowcharts, see [Flowcharts in Business process modeler](flowcharts-business-process-modeler.md).</span></span>

## <a name="visio-files"></a><span data-ttu-id="9621f-139">Visio ファイル</span><span class="sxs-lookup"><span data-stu-id="9621f-139">Visio files</span></span>
<span data-ttu-id="9621f-140">業務プロセスを Visio 図に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-140">You can associate a business process with a Visio diagram.</span></span> <span data-ttu-id="9621f-141">この機能は通常、タスク記録では表現できない高度なプロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9621f-141">Typically, this functionality is used for high-level processes that can't be represented by a task recording.</span></span> <span data-ttu-id="9621f-142">BPM は .vsd および .vsdx ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9621f-142">BPM supports .vsd and .vsdx files.</span></span> <span data-ttu-id="9621f-143">ただし、.vsdm ファイル (マクロ対応の Visio 図面ファイル) はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9621f-143">However, it doesn't support .vsdm files (macro-enabled Visio drawing files).</span></span> <span data-ttu-id="9621f-144">.vsd ファイルにマクロが含まれている場合、BPM マクロの実行が無効になります。</span><span class="sxs-lookup"><span data-stu-id="9621f-144">If a .vsd file contain macros, BPM disables the execution of the macros.</span></span>

<span data-ttu-id="9621f-145">Visio ファイルを表示またはアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9621f-145">To view or upload a Visio file, follow these steps.</span></span>

1. <span data-ttu-id="9621f-146">業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9621f-146">Select the business process, and then, in the right pane, on the **Overview** tab, select **Diagrams**.</span></span>
2. <span data-ttu-id="9621f-147">**フローチャート**ページで、**Visio** タブを選択します。詳細については、[ビジネス プロセス モデラー](flowcharts-business-process-modeler.md) の「未接続のフローチャート」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9621f-147">On the **Flowchart** page, select the **Visio** tab. For more information, see the "Unconnected flowcharts" section in [Flowcharts in Business process modeler](flowcharts-business-process-modeler.md).</span></span>

## <a name="edit-process-steps"></a><span data-ttu-id="9621f-148">プロセスの手順を編集</span><span class="sxs-lookup"><span data-stu-id="9621f-148">Edit process steps</span></span>
1. <span data-ttu-id="9621f-149">プロセス手順を編集するには、フローチャートの空白部分を右クリックし、下部のツールバーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9621f-149">To edit process steps, right-click on a blank area of the flowchart, and then, on the bottom toolbar, select **Edit**.</span></span>
2. <span data-ttu-id="9621f-150">**プロセスの手順**フィールドに、プロセスの手順を入力します。</span><span class="sxs-lookup"><span data-stu-id="9621f-150">In the **Process steps** field, enter the process steps.</span></span> <span data-ttu-id="9621f-151">行ごとに 1 つのステップを入力します。</span><span class="sxs-lookup"><span data-stu-id="9621f-151">Enter one step per line.</span></span>
3. <span data-ttu-id="9621f-152">ステップをインデントするには、等号 (=) を追加します。</span><span class="sxs-lookup"><span data-stu-id="9621f-152">To indent a step, add an equal sign (=).</span></span> <span data-ttu-id="9621f-153">ステップをインデントすることにより、サブステップとして定義します。</span><span class="sxs-lookup"><span data-stu-id="9621f-153">By indenting steps, you define them as substeps.</span></span> <span data-ttu-id="9621f-154">より深いレベルのインデントであり、階層内のより深いレベルを示す、1 つ以上の等号を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9621f-154">You can add more than one equal sign to indicate a deeper level of indentation and therefore a deeper level in the hierarchy.</span></span>

    <span data-ttu-id="9621f-155">たとえば、以下のプロセスの手順を作成します。</span><span class="sxs-lookup"><span data-stu-id="9621f-155">For example, you want to create the following process steps.</span></span>

    <span data-ttu-id="9621f-156">![ステップおよびサブステップがあるプロセスの例](./media/NEWBPM_BlogPost19.png "ステップおよびサブステップがあるプロセスの例")</span><span class="sxs-lookup"><span data-stu-id="9621f-156">![Example of a process that has steps and substeps](./media/NEWBPM_BlogPost19.png "Example of a process that has steps and substeps")</span></span>

    <span data-ttu-id="9621f-157">この場合、**プロセスの手順**フィールドに次のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="9621f-157">In this case, enter the following text in the **Process steps** field.</span></span>

    ```
    Step 1
    =SubStep 1.1
    =SubStep 1.2
    ==SubSub Step 1.2.1
    Step 2
    =SubStep 2.1
    ```
