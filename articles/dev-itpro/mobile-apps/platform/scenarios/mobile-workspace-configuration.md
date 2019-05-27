---
title: SysAppWorkspace クラスを使用してワークスペースを構成する
description: このトピックでは、SysAppWorkspace クラスを使用してサーバー上のワークスペースを構成および公開する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 9b0e6ae43d082dff8c62fbd39e385b3c9835b788
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537437"
---
# <a name="configure-workspaces-by-using-the-sysappworkspace-class"></a><span data-ttu-id="74825-103">SysAppWorkspace クラスを使用してワークスペースを構成する</span><span class="sxs-lookup"><span data-stu-id="74825-103">Configure workspaces by using the SysAppWorkspace class</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="74825-104">ワークスペース クラス **SysAppWorkspace** は、サーバー上でワークスペースを作成、構成および公開する開始点です。</span><span class="sxs-lookup"><span data-stu-id="74825-104">Workspace class, **SysAppWorkspace**, is the starting point to create, configure and publish workspaces on the server.</span></span> <span data-ttu-id="74825-105">sysAppWorkspace で使用できる API には、次の 2 つのカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="74825-105">The following two categories of APIs are available for use in sysAppWorkspace;</span></span>

+ <span data-ttu-id="74825-106">**ワークスペースの属性**; はモバイルワークスペースを構築するために、ページ、タスク、エンティティ、ルックアップ、リレーションシップの作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="74825-106">**Workspace attributes**; used to create pages, tasks, entities, lookups, relationships in order to build mobile workspaces.</span></span> 

    <span data-ttu-id="74825-107">[フリート管理のモバイル アプリのサンプル プロジェクトをダウンロードする](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.axpp ファイル)。</span><span class="sxs-lookup"><span data-stu-id="74825-107">[Download the sample project for Fleet Management Mobile App](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.axpp file).</span></span>
    <span data-ttu-id="74825-108">*ファイルをダウンロードした後、オペレーション開発環境で Visual Studio を開き、Dynamics 365 > プロジェクトのインポートをクリックし、ダウンロードしたプロジェクト ファイルを閲覧します。同じダイアログで、上書きにチェックを入れ、新しいソリューションの作成にチェックを入れます。インポートが完了した後、ソリューションを構築 (またはフリート管理モデルを構築) します。例を確認するには、まず、ワークスペースに含まれるすべてのページとアクションを見るために、'FMReservationManagementWorkspace' クラスを確認します。ソリューション エクスプローラを使用して、ページおよびタスク クラスを検索し、それぞれに含まれるすべての資産を検索してください。各 API の詳細については、API リファレンスを使用してください。*</span><span class="sxs-lookup"><span data-stu-id="74825-108">*After downloading the file, open Visual Studio on your Operations development environment, then click Dynamics 365 > Import Project, and browse for the downloaded project file. On the same dialog, check "overwrite" and check "create a new solution". After the import is complete, build the solution (or build the Fleet Management model). To review the example, start by reviewing 'FMReservationManagementWorkspace' class to see all the pages and actions included in the workspace. Use Solution Explorer to find page and task classes, and all the assets included in each. Use the API reference for more details on each API.*</span></span>
    
    <span data-ttu-id="74825-109">**X++ モバイル ワークスペースは、デザイナー ウィンドウで、X++ 属性 API またはその両方の組み合わせを使用して作成できます。 デザイナーから AOT へのモバイル アプリ メタデータのインポートの詳細については、以下の「ワークスペース クラスを使用して AOT リソースのワークスペースを公開する」を参照してください。上記のサンプルは、X++ 属性 API を使用して構築された完全なモバイル アプリです。**</span><span class="sxs-lookup"><span data-stu-id="74825-109">**A mobile workspace can be created through designer pane, using X++ attribute APIs or a combination of both. See topic 'Use the workspace class to publish workspaces from AOT resources' below for more details on importing mobile app metadata from designer to AOT. Sample above is a complete mobile app built using X++ attribute APIs.**</span></span>

+ <span data-ttu-id="74825-110">**ワークスペース メタデータ クラス**; はモバイル ワークスペースのためのメタデータへのサーバー側のビジネス ロジックを調査し、適用するために使用します。</span><span class="sxs-lookup"><span data-stu-id="74825-110">**Workspace metadata classes**; used to inspect and apply server-side business logic to metadata for mobile workspaces.</span></span> 

[<span data-ttu-id="74825-111">サーバー側の APIs の完全な一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74825-111">See complete list of server-side APIs</span></span>](../mobile-workspace-server-apis.md)



## <a name="create-a-new-workspace-class"></a><span data-ttu-id="74825-112">新しいワークスペース クラスを作成する</span><span class="sxs-lookup"><span data-stu-id="74825-112">Create a new workspace class</span></span>
<span data-ttu-id="74825-113">ワークスペースに **SysAppWorkspace** クラスを使用するには、 **SysAppWorkspace** クラスを拡張してワークスペース用に新しいクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74825-113">To use the **SysAppWorkspace** class for your workspace, you must create a new class for the workspace by extending the **SysAppWorkspace** class.</span></span> <span data-ttu-id="74825-114">新しいクラスを使用してワークスペース メタデータを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="74825-114">You can then use the new class to modify workspace metadata.</span></span> <span data-ttu-id="74825-115">新しいクラスは、モバイル アプリのライフ サイクル管理のフックも提供します。</span><span class="sxs-lookup"><span data-stu-id="74825-115">The new class also provides hooks for life cycle management of the mobile app.</span></span>

<span data-ttu-id="74825-116">ワークスペース用の新しいワークスペース クラスを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74825-116">Follow these steps to create a new workspace class for your workspace.</span></span>

1. <span data-ttu-id="74825-117">ワークスペース用の新しいクラスを作成し、それを **SysAppWorkspace** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="74825-117">Create a new class for your workspace, and extend it from the **SysAppWorkspace** class.</span></span>

    ![ワークスペース クラス](media/workspace-api/WorkspaceClass.png)

2. <span data-ttu-id="74825-119">新しいクラスに **SysAppWorkspaceAttribute** 属性を追加し、ワークスペースの **AppID** 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="74825-119">Add the **SysAppWorkspaceAttribute** attribute to the new class, and provide the **AppID** value of your workspace.</span></span> <span data-ttu-id="74825-120">アプリ用アプリ ID はモバイル アプリ デザイナー内の **概要** ページで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="74825-120">You can find the app ID for your app on the **Summary** page in the mobile app designer.</span></span>

    ![ワークスペース概要のアプリ ID](media/workspace-api/workspaceSummary.png)

    ![ワークスペース クラスの AppID 値](media/workspace-api/WorkspaceClassWithAppId.png)

3. <span data-ttu-id="74825-123">オプション: ワークスペースがアプリケーション オブジェクト ツリー (AOT) リソースの場合、AOT リソースの名前を **SysAppWorkspaceAttribute** コンストラクターの 2 番目のパラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="74825-123">Optional: If your workspace is an Application Object Tree (AOT) resource, provide the AOT resource name as the second parameter for the **SysAppWorkspaceAttribute** constructor.</span></span>

    ![ワークスペース クラスの AOT リソース名。](media/workspace-api/WorkspaceClassWithAOTResource.png)

## <a name="use-the-workspace-class-to-publish-workspaces-from-aot-resources"></a><span data-ttu-id="74825-125">AOT リソースからワークスペースを発行するには、workspace クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="74825-125">Use the workspace class to publish workspaces from AOT resources</span></span>
<span data-ttu-id="74825-126">ワークスペースはデータベース内に配置することができます。</span><span class="sxs-lookup"><span data-stu-id="74825-126">Workspaces can reside in the database.</span></span> <span data-ttu-id="74825-127">リソースとして AOT に常駐することもできます。</span><span class="sxs-lookup"><span data-stu-id="74825-127">They can also reside in the AOT as resources.</span></span> <span data-ttu-id="74825-128">AOT リソースに格納されているワークスペースを可視化するには、ワークスペース・クラスを作成し、そのワークスペースを含む AOT リソースの名前をポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74825-128">To provide visibility into workspaces that are stored in AOT resources, you must create a workspace class and point it to the name of the AOT resource that contains the workspace.</span></span> <span data-ttu-id="74825-129">AOT リソースとして保管されているワークスペースは、モバイル アプリ デザイナーを使用して編集または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="74825-129">Workspaces that are stored as AOT resources can't be edited or deleted by using the mobile app designer.</span></span> <span data-ttu-id="74825-130">これらのワークスペースはエクスポートのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="74825-130">Those workspace can only be exported.</span></span>

<span data-ttu-id="74825-131">AOT リソースとして存在するワークスペースを公開するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74825-131">Follow these steps to publish a workspace that resides in an AOT resource.</span></span>

1. <span data-ttu-id="74825-132">データベースに格納されるワークスペースを作成するとき、AOT リソースとして保存できるように、それをモバイル アプリ デザイナーからエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="74825-132">When you're developing a workspace that is stored in the database, you must export it from the mobile app designer so that it can be stored as an AOT resource.</span></span> <span data-ttu-id="74825-133">ワークスペースは XML ファイル形式でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="74825-133">The workspace is exported as an XML file.</span></span>

    ![ワークスペースをエクスポート](media/workspace-api/ExportWorkspace.png)

2. <span data-ttu-id="74825-135">モバイル アプリのデザイナーからワークスペースを削除します。</span><span class="sxs-lookup"><span data-stu-id="74825-135">Delete the workspace from the mobile app designer.</span></span> <span data-ttu-id="74825-136">それを後で AOT リソースから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="74825-136">You will load it from an AOT resource later.</span></span>

    ![ワークスペースの削除](media/workspace-api/DeleteWorkspace.png)

3. <span data-ttu-id="74825-138">新しい AOT リソースを作成し、リソースのエクスポートされたワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="74825-138">Create a new AOT resource, and select the exported workspace for the resource.</span></span>

    ![リソースとしてのワークスペース](media/workspace-api/WorkspaceAsResource.png)

4. <span data-ttu-id="74825-140">ワークスペース用の新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74825-140">Create a new class for your workspace.</span></span> <span data-ttu-id="74825-141">このクラスは、**SysAppWorkspace** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74825-141">This class should extend **SysAppWorkspace**.</span></span> <span data-ttu-id="74825-142">**SysAppWorkspaceAttribute** 属性をクラスに適用し、リソースを含むアプリ ID と AOT リソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="74825-142">Apply the **SysAppWorkspaceAttribute** attribute to the class, and provide the app ID and the AOT resource name that contains the resource.</span></span>

    ![新しいワークスペース クラス](media/workspace-api/NewWorkspaceClass.png)

5. <span data-ttu-id="74825-144">クラスをビルドして、モバイル アプリ デザイナーを再オープンします。</span><span class="sxs-lookup"><span data-stu-id="74825-144">Build the class, and reopen the mobile app designer.</span></span>

    <span data-ttu-id="74825-145">ワークスペースが公開されました。</span><span class="sxs-lookup"><span data-stu-id="74825-145">The workspace is now published.</span></span> <span data-ttu-id="74825-146">これはデザイナーに表示されますが、編集または削除できません。</span><span class="sxs-lookup"><span data-stu-id="74825-146">It appears in the designer, but can't be edited or deleted.</span></span> <span data-ttu-id="74825-147">ワークスペースがメタデータから読み込まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="74825-147">Note that the workspace is loaded from metadata.</span></span>

    ![メタデータ内のワークスペース](media/workspace-api/WorkspaceInMetadata.png)

## <a name="update-a-workspace-that-has-already-been-published"></a><span data-ttu-id="74825-149">発行済みワークスペースの更新</span><span class="sxs-lookup"><span data-stu-id="74825-149">Update a workspace that has already been published</span></span>
<span data-ttu-id="74825-150">ワークスペースが AOT リソースの一部である場合、モバイル アプリ デザイナーを使用して編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="74825-150">If your workspace is part of an AOT resource, you can't edit it by using the mobile app designer.</span></span> <span data-ttu-id="74825-151">次の例では、**MyWorkspace** というワークスペースが AOT に存在し、そこには **WorkspaceInAOT** というバッキング クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="74825-151">In the following example, a workspace that is named **MyWorkspace** exists in the AOT, and it has a backing class that is named **WorkspaceInAOT**.</span></span>

![AOT 内のワークスペース](media/workspace-api/UpdateWorkspaceInAOT.png)

![AOT 内にある公開済みのワークスペース](media/workspace-api/UpdateWorkspaceInAOTAndPublished.png)

<span data-ttu-id="74825-154">ワークスペースを編集するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74825-154">Follow these steps to edit the workspace.</span></span>

1. <span data-ttu-id="74825-155">モバイル アプリ デザイナーを使用して、ワークスペースをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="74825-155">Export the workspace by using the mobile app designer.</span></span> <span data-ttu-id="74825-156">デザイナーは、AOT に保存されているワークスペースの新しいアプリ ID を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="74825-156">The designer automatically creates new app IDs for workspaces that are stored in the AOT.</span></span>
2. <span data-ttu-id="74825-157">モバイル アプリ デザイナーを使用して、新しくエクスポートされたワークスペースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="74825-157">Import the newly exported workspace by using the mobile app designer.</span></span>

   1. <span data-ttu-id="74825-158">オプション: 名前を変更します。新たに追加されたワークスペースを他のワークスペースと区別できるようにします。</span><span class="sxs-lookup"><span data-stu-id="74825-158">Optional: Change the name so that the newly added workspace can be distinguished from other workspaces.</span></span>
   2. <span data-ttu-id="74825-159">新しく作成したワークスペースのアプリ ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="74825-159">Copy the app ID of the newly created workspace.</span></span>

      ![データベースの新しいワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspace.png)

      ![新しいワークスペースの詳細](media/workspace-api/UpdateWorkspaceNewWorkspaceDetails.png)

3. <span data-ttu-id="74825-162">バッキング クラスを拡張し、**SysAppWorkspaceAttribute** 属性を適用し、新しいアプリ ID を指定する新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="74825-162">Create a new class that extends your backing class, apply the **SysAppWorkspaceAttribute** attribute, and specify the new app ID.</span></span>

    ![メタデータ内のワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspaceClass.png)

<span data-ttu-id="74825-164">新しいワークスペースおよびバッキング クラスでの作業を続行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="74825-164">You can now continue to work with your new workspace and the backing class.</span></span> <span data-ttu-id="74825-165">変更を行なった後、AOT ベース ワークスペースとそれらをマージできます。</span><span class="sxs-lookup"><span data-stu-id="74825-165">After you've finished making your changes, you can merge them with the AOT-based workspace.</span></span>

## <a name="delete-a-workspace-that-is-an-aot-resource"></a><span data-ttu-id="74825-166">AOT リソースであるワークスペースの削除</span><span class="sxs-lookup"><span data-stu-id="74825-166">Delete a workspace that is an AOT resource</span></span>
<span data-ttu-id="74825-167">モバイル ワークスペースが AOT リソースとして格納されている場合は、それをモバイル アプリ デザイナーを使用して削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="74825-167">When a mobile workspace is stored as an AOT resource, you can't delete it by using the mobile app designer.</span></span> <span data-ttu-id="74825-168">AOT リソースとして存在するワークスペースを削除するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="74825-168">Follow these steps to delete a workspace that exists as an AOT resource.</span></span>

1. <span data-ttu-id="74825-169">ワークスペースを含む AOT リソースを削除します。</span><span class="sxs-lookup"><span data-stu-id="74825-169">Delete the AOT resource that contains the workspace.</span></span>

    ![削除するワークスペース](media/workspace-api/WorkspaceAsResourceToBeDeleted.png)

2. <span data-ttu-id="74825-171">ワークスペース用に作成されたワークスペース クラスを削除します。</span><span class="sxs-lookup"><span data-stu-id="74825-171">Delete the workspace class that was created for the workspace.</span></span>

    ![削除するワークスペース クラス](media/workspace-api/WorkspaceClassToBeDeleted.png)

3. <span data-ttu-id="74825-173">AOT リソースおよびクラスを含む完全なモデル ビルドを実行します。</span><span class="sxs-lookup"><span data-stu-id="74825-173">Do a full model build that contains the AOT resource and the class.</span></span> <span data-ttu-id="74825-174">次の図は、アプリケーション基準モデルの完全なビルドを示しています。</span><span class="sxs-lookup"><span data-stu-id="74825-174">The following illustrations shows a full build of the Application Foundation model.</span></span> <span data-ttu-id="74825-175">アプリケーション基盤モデルには、AOT リソースとワークスペース クラスも含まれます。</span><span class="sxs-lookup"><span data-stu-id="74825-175">The Application Foundation model also contains the AOT resource and workspace class.</span></span> <span data-ttu-id="74825-176">フルビルドをスピードアップするには、**オプション** タブですべての選択をクリアします。</span><span class="sxs-lookup"><span data-stu-id="74825-176">To speed up the full build, you can clear all the selections on the **Options** tab.</span></span>

    ![完全なビルド メニュー項目](media/workspace-api/FullBuildMenuItem.png)

    ![完全なビルド](media/workspace-api/FullBuild.png)

4. <span data-ttu-id="74825-179">ビルドが完了したら、モバイル アプリ デザイナーを再オープンして、ワークスペースが存在しないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="74825-179">When the build is completed, reopen the mobile app designer, and verify that the workspace is no longer there.</span></span>

