---
title: SysAppWorkspace クラスを使用してワークスペースを構成する
description: このトピックでは、SysAppWorkspace クラスを使用してサーバー上のワークスペースを構成および公開する方法について説明します。
author: robinarh
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 65f9a6c6b73ce0b64a314cea52c8cfc8955f8484
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752232"
---
# <a name="configure-workspaces-by-using-the-sysappworkspace-class"></a><span data-ttu-id="5eb57-103">SysAppWorkspace クラスを使用してワークスペースを構成する</span><span class="sxs-lookup"><span data-stu-id="5eb57-103">Configure workspaces by using the SysAppWorkspace class</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="5eb57-104">ワークスペース クラス **SysAppWorkspace** は、サーバー上でワークスペースを作成、構成および公開する開始点です。</span><span class="sxs-lookup"><span data-stu-id="5eb57-104">Workspace class, **SysAppWorkspace**, is the starting point to create, configure and publish workspaces on the server.</span></span> <span data-ttu-id="5eb57-105">sysAppWorkspace で使用できる API には、次のカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-105">The following categories of APIs are available for use in sysAppWorkspace</span></span>

- <span data-ttu-id="5eb57-106">**ワークスペースの属性** - これはモバイルワークスペースを構築するために、ページ、タスク、エンティティ、ルックアップ、リレーションシップの作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-106">**Workspace attributes** - This is used to create pages, tasks, entities, lookups, relationships in order to build mobile workspaces.</span></span> 
    - <span data-ttu-id="5eb57-107">フリート管理のモバイル アプリのサンプル プロジェクトをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-107">Download the sample project for Fleet Management Mobile App.</span></span> <span data-ttu-id="5eb57-108">これは、[Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) で発見された .axpp ファイルです。</span><span class="sxs-lookup"><span data-stu-id="5eb57-108">This is an .axpp file found at [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples).</span></span>
    - <span data-ttu-id="5eb57-109">ファイルをダウンロードした後、運用開発環境で Visual Studio を開き、**Dynamics 365 > Import Project** を選び、ダウンロードされたプロジェクト ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-109">After downloading the file, open Visual Studio on your Operations development environment, select **Dynamics 365 > Import Project**, and browse for the downloaded project file.</span></span> <span data-ttu-id="5eb57-110">同じダイアログ ボックスで、**上書き** を選び、**新しいソリューションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-110">On the same dialog box, select **Overwrite** and select **Create a new solution**.</span></span> <span data-ttu-id="5eb57-111">インポートが完了したら、ソリューションをビルドします (または、フリート管理 モデルをビルドします)。</span><span class="sxs-lookup"><span data-stu-id="5eb57-111">After the import is complete, build the solution (or build the Fleet Management model).</span></span> 
    - <span data-ttu-id="5eb57-112">例を確認するには、まず FMReservationManagementWorkspace クラスを確認し、ワークスペースに含まれるすべてのページとアクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-112">To review the example, start by reviewing the FMReservationManagementWorkspace class to see all the pages and actions included in the workspace.</span></span> <span data-ttu-id="5eb57-113">ソリューション エクスプローラーを使用して、ページとタスク クラス、およびそれらに含まれるすべての資産を検索します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-113">Use Solution Explorer to find page and task classes, and all the assets included in each.</span></span> <span data-ttu-id="5eb57-114">各 API の詳細については、API リファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb57-114">Use the API reference for more details on each API.</span></span>
    - <span data-ttu-id="5eb57-115">モバイル ワークスペースは、X + + 属性 APIs またはその両方の組み合わせを使用して、デザイナー ウィンドウから作成できます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-115">A mobile workspace can be created through designer pane, using X++ attribute APIs or a combination of both.</span></span> <span data-ttu-id="5eb57-116">デザイナーから AOT にモバイル アプリのメタデータをインポートする方法については、この後の「ワークスペース クラスを使用して AOT リソースからワークスペースを発行」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb57-116">See the "Use the workspace class to publish workspaces from AOT resources" section below for more details about how to import mobile app metadata from designer to AOT.</span></span> <span data-ttu-id="5eb57-117">サンプル プロジェクトのフリート管理モバイル アプリは、X + + 属性 APIs を使用して作成された完全なモバイル アプリです。</span><span class="sxs-lookup"><span data-stu-id="5eb57-117">The sample project Fleet Management Mobile App is a complete mobile app built using X++ attribute APIs.</span></span>

- <span data-ttu-id="5eb57-118">**ワークスペース メタデータ クラス** - これはモバイル ワークスペースのためのメタデータへのサーバー側のビジネス ロジックを調査し、適用するために使用します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-118">**Workspace metadata classes** - This is used to inspect and apply server-side business logic to metadata for mobile workspaces.</span></span> 

<span data-ttu-id="5eb57-119">サーバー側の APIs の完全一覧については、[サーバー側の開発 (ワークスペース X++ APIs)](../mobile-workspace-server-apis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5eb57-119">For a complete list of server-side APIs, see [Server-side development (workspace X++ APIs)](../mobile-workspace-server-apis.md).</span></span>


## <a name="create-a-new-workspace-class"></a><span data-ttu-id="5eb57-120">新しいワークスペース クラスを作成する</span><span class="sxs-lookup"><span data-stu-id="5eb57-120">Create a new workspace class</span></span>
<span data-ttu-id="5eb57-121">ワークスペースに **SysAppWorkspace** クラスを使用するには、 **SysAppWorkspace** クラスを拡張してワークスペース用に新しいクラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-121">To use the **SysAppWorkspace** class for your workspace, you must create a new class for the workspace by extending the **SysAppWorkspace** class.</span></span> <span data-ttu-id="5eb57-122">新しいクラスを使用してワークスペース メタデータを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-122">You can then use the new class to modify workspace metadata.</span></span> <span data-ttu-id="5eb57-123">新しいクラスは、モバイル アプリのライフ サイクル管理のフックも提供します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-123">The new class also provides hooks for life cycle management of the mobile app.</span></span>

<span data-ttu-id="5eb57-124">ワークスペース用の新しいワークスペース クラスを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5eb57-124">Follow these steps to create a new workspace class for your workspace.</span></span>

1. <span data-ttu-id="5eb57-125">ワークスペース用の新しいクラスを作成し、それを **SysAppWorkspace** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-125">Create a new class for your workspace, and extend it from the **SysAppWorkspace** class.</span></span>

    ![ワークスペース クラス](media/workspace-api/WorkspaceClass.png)

2. <span data-ttu-id="5eb57-127">新しいクラスに **SysAppWorkspaceAttribute** 属性を追加し、ワークスペースの **AppID** 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-127">Add the **SysAppWorkspaceAttribute** attribute to the new class, and provide the **AppID** value of your workspace.</span></span> <span data-ttu-id="5eb57-128">アプリ用アプリ ID はモバイル アプリ デザイナー内の **概要** ページで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-128">You can find the app ID for your app on the **Summary** page in the mobile app designer.</span></span>

    ![ワークスペース概要のアプリ ID](media/workspace-api/workspaceSummary.png)

    ![ワークスペース クラスの AppID 値](media/workspace-api/WorkspaceClassWithAppId.png)

3. <span data-ttu-id="5eb57-131">オプション: ワークスペースがアプリケーション オブジェクト ツリー (AOT) リソースの場合、AOT リソースの名前を **SysAppWorkspaceAttribute** コンストラクターの 2 番目のパラメーターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-131">Optional: If your workspace is an Application Object Tree (AOT) resource, provide the AOT resource name as the second parameter for the **SysAppWorkspaceAttribute** constructor.</span></span>

    ![ワークスペース クラスの AOT リソース名。](media/workspace-api/WorkspaceClassWithAOTResource.png)

## <a name="use-the-workspace-class-to-publish-workspaces-from-aot-resources"></a><span data-ttu-id="5eb57-133">AOT リソースからワークスペースを発行するには、workspace クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-133">Use the workspace class to publish workspaces from AOT resources</span></span>
<span data-ttu-id="5eb57-134">ワークスペースはデータベース内に配置することができます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-134">Workspaces can reside in the database.</span></span> <span data-ttu-id="5eb57-135">リソースとして AOT に常駐することもできます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-135">They can also reside in the AOT as resources.</span></span> <span data-ttu-id="5eb57-136">AOT リソースに格納されているワークスペースを可視化するには、ワークスペース・クラスを作成し、そのワークスペースを含む AOT リソースの名前をポイントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-136">To provide visibility into workspaces that are stored in AOT resources, you must create a workspace class and point it to the name of the AOT resource that contains the workspace.</span></span> <span data-ttu-id="5eb57-137">AOT リソースとして保管されているワークスペースは、モバイル アプリ デザイナーを使用して編集または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="5eb57-137">Workspaces that are stored as AOT resources can't be edited or deleted by using the mobile app designer.</span></span> <span data-ttu-id="5eb57-138">これらのワークスペースはエクスポートのみ可能です。</span><span class="sxs-lookup"><span data-stu-id="5eb57-138">Those workspace can only be exported.</span></span>

<span data-ttu-id="5eb57-139">AOT リソースとして存在するワークスペースを公開するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5eb57-139">Follow these steps to publish a workspace that resides in an AOT resource.</span></span>

1. <span data-ttu-id="5eb57-140">データベースに格納されるワークスペースを作成するとき、AOT リソースとして保存できるように、それをモバイル アプリ デザイナーからエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-140">When you're developing a workspace that is stored in the database, you must export it from the mobile app designer so that it can be stored as an AOT resource.</span></span> <span data-ttu-id="5eb57-141">ワークスペースは XML ファイル形式でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-141">The workspace is exported as an XML file.</span></span>

    ![ワークスペースをエクスポート](media/workspace-api/ExportWorkspace.png)

2. <span data-ttu-id="5eb57-143">モバイル アプリのデザイナーからワークスペースを削除します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-143">Delete the workspace from the mobile app designer.</span></span> <span data-ttu-id="5eb57-144">それを後で AOT リソースから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-144">You will load it from an AOT resource later.</span></span>

    ![ワークスペースの削除](media/workspace-api/DeleteWorkspace.png)

3. <span data-ttu-id="5eb57-146">新しい AOT リソースを作成し、リソースのエクスポートされたワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-146">Create a new AOT resource, and select the exported workspace for the resource.</span></span>

    ![リソースとしてのワークスペース](media/workspace-api/WorkspaceAsResource.png)

4. <span data-ttu-id="5eb57-148">ワークスペース用の新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-148">Create a new class for your workspace.</span></span> <span data-ttu-id="5eb57-149">このクラスは、**SysAppWorkspace** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-149">This class should extend **SysAppWorkspace**.</span></span> <span data-ttu-id="5eb57-150">**SysAppWorkspaceAttribute** 属性をクラスに適用し、リソースを含むアプリ ID と AOT リソース名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-150">Apply the **SysAppWorkspaceAttribute** attribute to the class, and provide the app ID and the AOT resource name that contains the resource.</span></span>

    ![新しいワークスペース クラス](media/workspace-api/NewWorkspaceClass.png)

5. <span data-ttu-id="5eb57-152">クラスをビルドして、モバイル アプリ デザイナーを再オープンします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-152">Build the class, and reopen the mobile app designer.</span></span>

    <span data-ttu-id="5eb57-153">ワークスペースが公開されました。</span><span class="sxs-lookup"><span data-stu-id="5eb57-153">The workspace is now published.</span></span> <span data-ttu-id="5eb57-154">これはデザイナーに表示されますが、編集または削除できません。</span><span class="sxs-lookup"><span data-stu-id="5eb57-154">It appears in the designer, but can't be edited or deleted.</span></span> <span data-ttu-id="5eb57-155">ワークスペースがメタデータから読み込まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5eb57-155">Note that the workspace is loaded from metadata.</span></span>

    ![メタデータ内のワークスペース](media/workspace-api/WorkspaceInMetadata.png)

## <a name="update-a-workspace-that-has-already-been-published"></a><span data-ttu-id="5eb57-157">発行済みワークスペースの更新</span><span class="sxs-lookup"><span data-stu-id="5eb57-157">Update a workspace that has already been published</span></span>
<span data-ttu-id="5eb57-158">ワークスペースが AOT リソースの一部である場合、モバイル アプリ デザイナーを使用して編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="5eb57-158">If your workspace is part of an AOT resource, you can't edit it by using the mobile app designer.</span></span> <span data-ttu-id="5eb57-159">次の例では、**MyWorkspace** というワークスペースが AOT に存在し、そこには **WorkspaceInAOT** というバッキング クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="5eb57-159">In the following example, a workspace that is named **MyWorkspace** exists in the AOT, and it has a backing class that is named **WorkspaceInAOT**.</span></span>

![AOT 内のワークスペース](media/workspace-api/UpdateWorkspaceInAOT.png)

![AOT 内にある公開済みのワークスペース](media/workspace-api/UpdateWorkspaceInAOTAndPublished.png)

<span data-ttu-id="5eb57-162">ワークスペースを編集するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5eb57-162">Follow these steps to edit the workspace.</span></span>

1. <span data-ttu-id="5eb57-163">モバイル アプリ デザイナーを使用して、ワークスペースをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-163">Export the workspace by using the mobile app designer.</span></span> <span data-ttu-id="5eb57-164">デザイナーは、AOT に保存されているワークスペースの新しいアプリ ID を自動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-164">The designer automatically creates new app IDs for workspaces that are stored in the AOT.</span></span>
2. <span data-ttu-id="5eb57-165">モバイル アプリ デザイナーを使用して、新しくエクスポートされたワークスペースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-165">Import the newly exported workspace by using the mobile app designer.</span></span>

   1. <span data-ttu-id="5eb57-166">オプション: 名前を変更します。新たに追加されたワークスペースを他のワークスペースと区別できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-166">Optional: Change the name so that the newly added workspace can be distinguished from other workspaces.</span></span>
   2. <span data-ttu-id="5eb57-167">新しく作成したワークスペースのアプリ ID をコピーします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-167">Copy the app ID of the newly created workspace.</span></span>

      ![データベースの新しいワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspace.png)

      ![新しいワークスペースの詳細](media/workspace-api/UpdateWorkspaceNewWorkspaceDetails.png)

3. <span data-ttu-id="5eb57-170">バッキング クラスを拡張し、**SysAppWorkspaceAttribute** 属性を適用し、新しいアプリ ID を指定する新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-170">Create a new class that extends your backing class, apply the **SysAppWorkspaceAttribute** attribute, and specify the new app ID.</span></span>

    ![メタデータ内のワークスペース](media/workspace-api/UpdateWorkspaceNewWorkspaceClass.png)

<span data-ttu-id="5eb57-172">新しいワークスペースおよびバッキング クラスでの作業を続行することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5eb57-172">You can now continue to work with your new workspace and the backing class.</span></span> <span data-ttu-id="5eb57-173">変更を行なった後、AOT ベース ワークスペースとそれらをマージできます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-173">After you've finished making your changes, you can merge them with the AOT-based workspace.</span></span>

## <a name="delete-a-workspace-that-is-an-aot-resource"></a><span data-ttu-id="5eb57-174">AOT リソースであるワークスペースの削除</span><span class="sxs-lookup"><span data-stu-id="5eb57-174">Delete a workspace that is an AOT resource</span></span>
<span data-ttu-id="5eb57-175">モバイル ワークスペースが AOT リソースとして格納されている場合は、それをモバイル アプリ デザイナーを使用して削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="5eb57-175">When a mobile workspace is stored as an AOT resource, you can't delete it by using the mobile app designer.</span></span> <span data-ttu-id="5eb57-176">AOT リソースとして存在するワークスペースを削除するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5eb57-176">Follow these steps to delete a workspace that exists as an AOT resource.</span></span>

1. <span data-ttu-id="5eb57-177">ワークスペースを含む AOT リソースを削除します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-177">Delete the AOT resource that contains the workspace.</span></span>

    ![削除するワークスペース](media/workspace-api/WorkspaceAsResourceToBeDeleted.png)

2. <span data-ttu-id="5eb57-179">ワークスペース用に作成されたワークスペース クラスを削除します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-179">Delete the workspace class that was created for the workspace.</span></span>

    ![削除するワークスペース クラス](media/workspace-api/WorkspaceClassToBeDeleted.png)

3. <span data-ttu-id="5eb57-181">AOT リソースおよびクラスを含む完全なモデル ビルドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-181">Do a full model build that contains the AOT resource and the class.</span></span> <span data-ttu-id="5eb57-182">次の図は、アプリケーション基準モデルの完全なビルドを示しています。</span><span class="sxs-lookup"><span data-stu-id="5eb57-182">The following illustrations shows a full build of the Application Foundation model.</span></span> <span data-ttu-id="5eb57-183">アプリケーション基盤モデルには、AOT リソースとワークスペース クラスも含まれます。</span><span class="sxs-lookup"><span data-stu-id="5eb57-183">The Application Foundation model also contains the AOT resource and workspace class.</span></span> <span data-ttu-id="5eb57-184">フルビルドをスピードアップするには、**オプション** タブですべての選択をクリアします。</span><span class="sxs-lookup"><span data-stu-id="5eb57-184">To speed up the full build, you can clear all the selections on the **Options** tab.</span></span>

    ![完全なビルド メニュー項目](media/workspace-api/FullBuildMenuItem.png)

    ![完全なビルド](media/workspace-api/FullBuild.png)

4. <span data-ttu-id="5eb57-187">ビルドが完了したら、モバイル アプリ デザイナーを再オープンして、ワークスペースが存在しないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5eb57-187">When the build is completed, reopen the mobile app designer, and verify that the workspace is no longer there.</span></span>



[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]