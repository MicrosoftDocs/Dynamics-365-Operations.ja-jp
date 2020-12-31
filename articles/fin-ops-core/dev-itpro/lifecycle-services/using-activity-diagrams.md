---
title: ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する
description: このトピックでは、BPM ライブラリでアクティビティ図を使用する方法について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 776ad8a4505d888286f1f9fbca6700d69b33df81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681042"
---
# <a name="work-with-activity-diagrams-in-business-process-modeler-libraries"></a><span data-ttu-id="0d93a-103">ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する</span><span class="sxs-lookup"><span data-stu-id="0d93a-103">Work with activity diagrams in Business process modeler libraries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d93a-104">活動ダイアグラムを業務プロセスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-104">You can associate an activity diagram with a business process.</span></span> <span data-ttu-id="0d93a-105">活動ダイアグラムは、提案されたソフトウェア ソリューションで業務プロセスまたはタスクを完了する方法について記述するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-105">Activity diagrams are used to describe how a business process or task is completed in a proposed software solution.</span></span>

<span data-ttu-id="0d93a-106">活動ダイアグラムには 2 つの種類があります。</span><span class="sxs-lookup"><span data-stu-id="0d93a-106">There are two types of activity diagrams:</span></span>

- <span data-ttu-id="0d93a-107">**タスク記録** – Finance and Operations のタスク記録に関連する業務プロセスには、自動的に生成される活動ダイアグラムおよびプロセスの手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-107">**Task recordings** – Business processes that are associated with task recordings for Finance and Operations, include activity diagrams and process steps that are automatically generated.</span></span>
- <span data-ttu-id="0d93a-108">**Microsoft Visio** – Visio ファイルを手動でアップロードすることによって、業務プロセスを Visio 図に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-108">**Microsoft Visio** – You can associate a business process with a Visio diagram by manually uploading a Visio file.</span></span>


## <a name="browse-activity-diagrams"></a><span data-ttu-id="0d93a-109">活動ダイアグラムの参照</span><span class="sxs-lookup"><span data-stu-id="0d93a-109">Browse activity diagrams</span></span>
<span data-ttu-id="0d93a-110">BPM ライブラリ内の **図** 列は、特定の業務プロセスがアクティビティ図に関連付けられているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-110">The **Diagrams** column in your BPM library indicates whether a particular business process is associated with an activity diagram.</span></span> <span data-ttu-id="0d93a-111">列の番号は、ダイアグラムを含む子プロセスの数を示します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-111">The number in the column indicates the number of child processes that include diagrams.</span></span> <span data-ttu-id="0d93a-112">番号の横にあるシンボルは、現在のノードまたはプロセスがダイアグラムに関連付けられているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-112">The symbol next to the number indicates whether the current node or process is associated with a diagram.</span></span> <span data-ttu-id="0d93a-113">これらのインジケーターは、Visio ダイアグラムには適用されません。</span><span class="sxs-lookup"><span data-stu-id="0d93a-113">These indicators don't apply to Visio diagrams.</span></span>

<span data-ttu-id="0d93a-114">[![monitoringanddiagnostics01](./media/browse_activity_diagrams.JPG)](./media/browse_activity_diagrams.JPG)</span><span class="sxs-lookup"><span data-stu-id="0d93a-114">[![monitoringanddiagnostics01](./media/browse_activity_diagrams.JPG)](./media/browse_activity_diagrams.JPG)</span></span>

<span data-ttu-id="0d93a-115">アクティビティ図を表示するには、業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-115">To view an activity diagram, select the business process, and then, in the right pane, on the **Overview** tab, select **Diagrams**.</span></span> <span data-ttu-id="0d93a-116">**フローチャート** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-116">The **Flowchart** page appears.</span></span> 


## <a name="upload-task-recording"></a><span data-ttu-id="0d93a-117">作業記録のアップロード</span><span class="sxs-lookup"><span data-stu-id="0d93a-117">Upload Task Recording</span></span>
<span data-ttu-id="0d93a-118">タスク記録をアップロードするには、アップロードする業務プロセス ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-118">To upload a task recording, open the business process library that you want to upload to.</span></span> <span data-ttu-id="0d93a-119">タスクの記録をアップロードするプロセス手順を選択し、**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d93a-119">Select the process step that you want to upload the task recording to, and then click **Upload**.</span></span>

<span data-ttu-id="0d93a-120">[![activitydiagrams01](./media/activity_diagrams_01.jpg)](./media/activity_diagrams_01.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d93a-120">[![activitydiagrams01](./media/activity_diagrams_01.jpg)](./media/activity_diagrams_01.jpg)</span></span>


<span data-ttu-id="0d93a-121">右ウィンドウで、**参照** をクリックしてファイルを選択してから **アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d93a-121">In the right pane, click **Browse** to choose a file, and then click **Upload**.</span></span>

<span data-ttu-id="0d93a-122">[![activitydiagrams02](./media/activity_diagrams_02.jpg)](./media/activity_diagrams_02.jpg)</span><span class="sxs-lookup"><span data-stu-id="0d93a-122">[![activitydiagrams02](./media/activity_diagrams_02.jpg)](./media/activity_diagrams_02.jpg)</span></span>


## <a name="activity-diagrams-that-are-created-from-task-recordings"></a><span data-ttu-id="0d93a-123">タスク記録から作成された活動ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="0d93a-123">Activity diagrams that are created from task recordings</span></span>

> <span data-ttu-id="0d93a-124">[!重要] ビジネス プロセス モデラーのフローチャート図は、非推奨になりました。</span><span class="sxs-lookup"><span data-stu-id="0d93a-124">[!IMPORTAMT] Flowchart diagrams in Business process modeler have been deprecated.</span></span> <span data-ttu-id="0d93a-125">非推奨の詳細については、[ビジネス プロセス モデラーのフローチャートの図](removed-deprecated-features.md#flowchart-diagrams-in-business-process-modeler) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d93a-125">To learn more about the deprecation, see [Flowchart diagrams in Business process modeler](removed-deprecated-features.md#flowchart-diagrams-in-business-process-modeler).</span></span>

<span data-ttu-id="0d93a-126">環境でタスク記録を作成して、Microsoft Dynamics Lifecycle Services (LCS) に直接保存することができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-126">You can create a task recording in your environment and save it directly to Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="0d93a-127">この方法で、タスク記録を BPM ライブラリ内の業務プロセスと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-127">In this way, you can associate the task recording with a business process in a BPM library.</span></span> <span data-ttu-id="0d93a-128">詳細については、[ヘルプ システムの接続](../../fin-ops/get-started/help-connect.md) および [タスク レコーダーを使用したドキュメントやトレーニングの作成](../user-interface/task-recorder-training-docs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d93a-128">For more information, see [Connecting the help system](../../fin-ops/get-started/help-connect.md) and [Create documentation or training with Task Recorder](../user-interface/task-recorder-training-docs.md).</span></span>

<span data-ttu-id="0d93a-129">タスク レコーダー ツールを使用すると、配布可能な記録ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-129">The Task recorder tool lets you create a distributable recording file.</span></span> <span data-ttu-id="0d93a-130">記録ファイルは、.axtr ファイル名拡張子を持ちます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-130">Recording files have the .axtr file name extension.</span></span> <span data-ttu-id="0d93a-131">手動で記録ファイルをアップロードすることにより、BPM 内の業務プロセスをタスク記録に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-131">You can associate a business process in BPM with a task recording by manually uploading the recording file.</span></span> 

<span data-ttu-id="0d93a-132">記録ファイルをアップロードするには、業務プロセスを選択し、右ウィンドウの **概要** タブで **アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-132">To upload a recording file, select the business process, and then, in the right pane, on the **Overview** tab, select **Upload**.</span></span>

<span data-ttu-id="0d93a-133">BPM は作成されたすべてのタスク記録の活動ダイアグラムと詳細なプロセスの手順を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-133">BPM automatically generates an activity diagram and detailed process steps for all task recordings that are created.</span></span> <span data-ttu-id="0d93a-134">次の図は、例を示します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-134">The following illustration shows an example.</span></span>

<span data-ttu-id="0d93a-135">![活動ダイアグラムおよびタスク記録プロセスの手順の例](./media/NEWBPM_BlogPost17-1024x483.png "活動ダイアグラムおよびタスク記録プロセスの手順の例")</span><span class="sxs-lookup"><span data-stu-id="0d93a-135">![Example of an activity diagram and process steps for a task recording](./media/NEWBPM_BlogPost17-1024x483.png "Example of an activity diagram and process steps for a task recording")</span></span>


## <a name="visio-files"></a><span data-ttu-id="0d93a-136">Visio ファイル</span><span class="sxs-lookup"><span data-stu-id="0d93a-136">Visio files</span></span>
<span data-ttu-id="0d93a-137">業務プロセスを Visio 図に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-137">You can associate a business process with a Visio diagram.</span></span> <span data-ttu-id="0d93a-138">この機能は通常、タスク記録では表現できない高度なプロセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d93a-138">Typically, this functionality is used for high-level processes that can't be represented by a task recording.</span></span>

> [!Note]
> <span data-ttu-id="0d93a-139">BPM は .vsd および .vsdx ファイルをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0d93a-139">BPM supports .vsd and .vsdx files.</span></span> <span data-ttu-id="0d93a-140">ただし、.vsdm ファイル (マクロ対応の Visio 図面ファイル) はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0d93a-140">However, it doesn't support .vsdm files (macro-enabled Visio drawing files).</span></span> <span data-ttu-id="0d93a-141">.vsd ファイルにマクロが含まれている場合、BPM マクロの実行が無効になります。</span><span class="sxs-lookup"><span data-stu-id="0d93a-141">If a .vsd file contain macros, BPM disables the execution of the macros.</span></span>

<span data-ttu-id="0d93a-142">Visio ファイルを表示またはアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-142">To view or upload a Visio file, follow these steps.</span></span>

1. <span data-ttu-id="0d93a-143">業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d93a-143">Select the business process, and then, in the right pane, on the **Overview** tab, select **Diagrams**.</span></span>
2. <span data-ttu-id="0d93a-144">**フローチャート** ページで、**Visio** タブを選択します。詳細については、[ビジネス プロセス モデラーのフローチャート (BPM)](flowcharts-business-process-modeler.md) の未接続のフローチャート セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d93a-144">On the **Flowchart** page, select the **Visio** tab. For more information, see the "Unconnected flowcharts" section in [Flowcharts in Business process modeler (BPM)](flowcharts-business-process-modeler.md).</span></span>

