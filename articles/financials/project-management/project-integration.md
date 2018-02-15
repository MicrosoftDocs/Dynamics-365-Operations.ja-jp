---
title: "Microsoft Project クライアント統合"
description: "プロジェクト スケジュールの計画や管理は複雑な題目になるため、プロジェクト マネージャーは、これらのタスク管理に役立つツールを使用する必要があります。 Microsoft Project クライアントとの統合により、プロジェクト作業分解構造を開いて管理するためのサポートが提供されます。"
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: a72963f755f8eddb19b8526d2938eff039ab7df2
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="31fb8-104">Microsoft Project クライアント統合</span><span class="sxs-lookup"><span data-stu-id="31fb8-104">Microsoft Project client integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31fb8-105">プロジェクト スケジュールの計画や管理は複雑な題目になるため、プロジェクト マネージャーは、これらのタスク管理に役立つツールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31fb8-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="31fb8-106">Microsoft Project クライアントとの統合により、プロジェクト作業分解構造を開いて管理するためのサポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="31fb8-107">プロジェクト マネージャーは、変更を Finance and Operations のプロジェクト作業分解構造に公開できます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="31fb8-108">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 2017 年 7 月の更新プログラムを使用している場合、KB 4054797 および 4055884 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31fb8-108">If you are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="31fb8-109">Microsoft Project クライアント アドインの構成</span><span class="sxs-lookup"><span data-stu-id="31fb8-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="31fb8-110">Microsoft Project クライアントとの統合を有効にするためには、 ユーザ クライアントの Microsoft Project アプリケーションに Microsoft Dynamics 365 アドインがインストールされていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="31fb8-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="31fb8-111">これは**プロジェクト管理ワークスペース**を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="31fb8-112">•   ワークスペースの [**リンク**] > [**設定**] セクションの [** クライアント アドインの構成**] フォームをクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="31fb8-113">•   [**開く**] をクリックし、要求されたら [**実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="31fb8-114">Microsoft Project クライアントの、既存のドラフト作業分解構造を開き、編集します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="31fb8-115">Finance and Operations のプロジェクトで既に作業分解構造が作成されている場合、作業分解構造がドラフト ステータスの場合は、Microsoft Project クライアント アプリケーションで作業分解構造を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="31fb8-116">[**プロジェクト**] ページから開くには、[**計画**] タブから [**Microsoft Project で開く**] リンクをクリックします。このページは Microsoft Project クライアント アプリケーション内で、[**Microsoft Dynamics 365**] タブの [**開く**] をクリックすることでも開くことができます。一覧から [**法人**] および [**プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="31fb8-117">ブラウザーとして Internet Explorer を使用している場合、 [**保存**] をクリックして、ファイルがダウンロードされた場所から手動で開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="31fb8-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="31fb8-118">または、[**保存して開く**] をクリックし、Microsoft Project クライアントのファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="31fb8-119">保存するときにファイル名を変更できません。</span><span class="sxs-lookup"><span data-stu-id="31fb8-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="31fb8-120">Microsoft Project クライアントを使用してファイルを編集する前に、チェックする必要があります。[**Microsoft Dynamics 365**] タブの [**チェック アウト**] をクリックします。これにより、他のユーザーが同時に Finance and Operations 内から作業分解構造を編集することを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="31fb8-121">編集を完了した後に作業分解構造を公開するには、[**Microsoft Dynamics 365**] タブの [**チェック イン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="31fb8-122">プロジェクト チームがすでに Finance and Operations のプロジェクトに追加されている場合、リソース リストにはチームメンバーが配置されます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="31fb8-123">プロジェクト チームがまだプロジェクトに追加されていない場合は [**Microsoft Dynamics 365**] タブの [**リソース**] ボタンをクリックして、リソースを選択して Microsoft Project クライアント内でチームを構築できます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="31fb8-124">次のデータは、チェックイン プロセスの一部として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="31fb8-125">•   タスク名</span><span class="sxs-lookup"><span data-stu-id="31fb8-125">•   Task name</span></span>

<span data-ttu-id="31fb8-126">•   開始日</span><span class="sxs-lookup"><span data-stu-id="31fb8-126">•   Start date</span></span>

<span data-ttu-id="31fb8-127">•   終了日</span><span class="sxs-lookup"><span data-stu-id="31fb8-127">•   Finish date</span></span>

<span data-ttu-id="31fb8-128">•   先行処理</span><span class="sxs-lookup"><span data-stu-id="31fb8-128">•   Predecessors</span></span>

<span data-ttu-id="31fb8-129">•   リソース名</span><span class="sxs-lookup"><span data-stu-id="31fb8-129">•   Resource names</span></span>

<span data-ttu-id="31fb8-130">•   カテゴリ</span><span class="sxs-lookup"><span data-stu-id="31fb8-130">•   Category</span></span>

<span data-ttu-id="31fb8-131">•   リソース カテゴリ</span><span class="sxs-lookup"><span data-stu-id="31fb8-131">•   Resource category</span></span>

<span data-ttu-id="31fb8-132">•   作業時間</span><span class="sxs-lookup"><span data-stu-id="31fb8-132">•   Work hours</span></span>

<span data-ttu-id="31fb8-133">•   メモ</span><span class="sxs-lookup"><span data-stu-id="31fb8-133">•   Notes</span></span>

<span data-ttu-id="31fb8-134">•   優先順位</span><span class="sxs-lookup"><span data-stu-id="31fb8-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="31fb8-135">他の列を Microsoft Project クライアント ファイルに追加する場合、それらはファイルに保存されず、ファイルが再び開かれた時には表示されません。</span><span class="sxs-lookup"><span data-stu-id="31fb8-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="31fb8-136">Microsoft Project クライアントを使用して既存のプロジェクトの作業分解構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="31fb8-137">Microsoft Project クライアントを使用して新しい作業分解構造を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="31fb8-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="31fb8-138">Microsoft Project クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="31fb8-139">[**Microsoft Dynamics 365**] タブの、[**開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="31fb8-140">プロジェクトの [**法人**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="31fb8-141">[**プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="31fb8-142">[**Microsoft Dynamics 365**] タブの [**チェック アウト**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="31fb8-143">Finance and Operations に公開する準備ができたら、[**Microsoft Dynamics 365**] タブの [**チェック イン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="31fb8-144">Microsoft Project クライアントを使用して既存プロジェクトの既存の作業分解構造を置換します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="31fb8-145">Microsoft Project クライアントを使用して新しい作業分解構造を作成し、既存のプロジェクトの既存の作業分解構造を置換するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="31fb8-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="31fb8-146">Microsoft Project クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="31fb8-147">Microsoft Project クライアントのスケジュールの作成。</span><span class="sxs-lookup"><span data-stu-id="31fb8-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="31fb8-148">[**Microsoft Dynamics 365**] タブで、[**変更を保存**] > [**既存のプロジェクトを置き換え**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="31fb8-149">プロジェクトの [**法人**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="31fb8-150">[**プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="31fb8-151">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="31fb8-152">Microsoft Project クライアントから新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="31fb8-153">Microsoft Project クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="31fb8-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="31fb8-154">Microsoft Project クライアントのスケジュールの作成。</span><span class="sxs-lookup"><span data-stu-id="31fb8-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="31fb8-155">[**Microsoft Dynamics 365**] タブで、[**変更を保存**] > [**新しいプロジェクトに保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="31fb8-156">プロジェクトの [**法人**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="31fb8-157">必要に応じて**プロジェクト ID** を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="31fb8-158">**プロジェクト名**を入力します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="31fb8-159">[**プロジェクト タイプ**]、[**プロジェクト グループ**] および [**プロジェクト契約 ID**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="31fb8-160">または、[**新規**] をクリックして新しいプロジェクト契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="31fb8-161">リソースに使用する [**カレンダー**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="31fb8-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="31fb8-162">[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="31fb8-162">Click **OK**.</span></span>

