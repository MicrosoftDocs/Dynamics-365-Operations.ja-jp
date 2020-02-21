---
title: Visual Studio の Finance and Operations プロジェクト タイプ
description: Finance and Operations プロジェクト タイプは開発ツールの一部です。
author: RobinARH
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 31781
ms.assetid: d0d12e0e-a417-41b1-b2eb-7c69eee5ac61
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2de1e4ed7526dd8441b66f8966e9a9e98a23afd
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983640"
---
# <a name="finance-and-operations-project-type-in-visual-studio"></a><span data-ttu-id="f5a5f-103">Visual Studio の Finance and Operations プロジェクト タイプ</span><span class="sxs-lookup"><span data-stu-id="f5a5f-103">Finance and Operations project type in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5a5f-104">Finance and Operations プロジェクト タイプは開発ツールの一部です。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-104">The Finance and Operations project type is part of the development tools.</span></span> <span data-ttu-id="f5a5f-105">このプロジェクト タイプは、Visual Studio の他のプロジェクトに似ています。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-105">This project type resembles other projects in Visual Studio.</span></span> <span data-ttu-id="f5a5f-106">これにより、モデルに使用する要素を整理して管理することができます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-106">It helps you organize and manage the elements that you're working with for a model.</span></span> <span data-ttu-id="f5a5f-107">たとえば、プロジェクトには、要素をグループ化するのを助けるフォルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-107">For example, the project can have folders that help you group the elements.</span></span> <span data-ttu-id="f5a5f-108">Visual Studio ソリューションは、複数のプロジェクトを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-108">A Visual Studio solution can contain multiple projects.</span></span> <span data-ttu-id="f5a5f-109">プロジェクトには重要な制約が 1 つあります。これは、1 つのモデルからの要素のみを含むことができます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-109">There is one important constraint for a project: it can contain elements from only one model.</span></span> <span data-ttu-id="f5a5f-110">異なるモデルの要素を処理する必要がある場合、Visual Studio ソリューションで複数のプロジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-110">If you must work with elements from different models, you must use multiple projects in your Visual Studio solution.</span></span>

## <a name="create-a-new-project"></a><span data-ttu-id="f5a5f-111">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="f5a5f-111">Create a new project</span></span>
<span data-ttu-id="f5a5f-112">新しい空のプロジェクトを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-112">To create a new, empty project, follow these steps.</span></span>

1.  <span data-ttu-id="f5a5f-113">**ファイル**メニューで、**新規**をポイントし、**プロジェクト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-113">On the **File** menu, point to **New**, and then click **Project**.</span></span>
2.  <span data-ttu-id="f5a5f-114">テンプレート タイプの一覧で、**インストール済み**のノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-114">In the list of template types, expand the **Installed** node.</span></span>
3.  <span data-ttu-id="f5a5f-115">**テンプレート**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-115">Expand the **Templates** node.</span></span>
4.  <span data-ttu-id="f5a5f-116">**Finance and Operations** カテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-116">Select the **Finance and Operations** category.</span></span>
5.  <span data-ttu-id="f5a5f-117">**業務プロジェクト** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-117">Select the **Operations Project** template.</span></span>
6.  <span data-ttu-id="f5a5f-118">新規プロジェクトの名前および場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-118">Enter the name and location for the new project.</span></span>
7.  <span data-ttu-id="f5a5f-119">新しいソリューションを作成するのか、現在のソリューションにプロジェクトを追加するのかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-119">Specify whether you want to create a new solution or add the project to the current solution.</span></span>
8.  <span data-ttu-id="f5a5f-120">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-120">Click **OK**.</span></span>

<span data-ttu-id="f5a5f-121">すべてのプロジェクトには、いくつかの重要なプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-121">Every project has several important properties.</span></span> <span data-ttu-id="f5a5f-122">プロジェクトのプロパティを設定するには、ソリューション エクスプ ローラーでプロジェクトを右クリックし、**プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-122">To set the properties for a project, right-click the project in Solution Explorer, and then click **Properties**.</span></span> <span data-ttu-id="f5a5f-123">次のテーブルにこれらのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-123">The following table describes these properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f5a5f-124">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f5a5f-124">Property</span></span></th>
<th><span data-ttu-id="f5a5f-125">説明</span><span class="sxs-lookup"><span data-stu-id="f5a5f-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f5a5f-126">スタートアップ オブジェクトの種類</span><span class="sxs-lookup"><span data-stu-id="f5a5f-126">Startup Object type</span></span></td>
<td><span data-ttu-id="f5a5f-127">プロジェクトの実行時にスタートアップ オブジェクトとして使用されるオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-127">The type of object that will be used as the Startup Object when the project is run.</span></span> <span data-ttu-id="f5a5f-128">次のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-128">The following types are available:</span></span>
<ul>
<li><span data-ttu-id="f5a5f-129">フォーム</span><span class="sxs-lookup"><span data-stu-id="f5a5f-129">Form</span></span></li>
<li><span data-ttu-id="f5a5f-130">クラス</span><span class="sxs-lookup"><span data-stu-id="f5a5f-130">Class</span></span></li>
<li><span data-ttu-id="f5a5f-131">出力メニュー項目</span><span class="sxs-lookup"><span data-stu-id="f5a5f-131">Output menu item</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5a5f-132">スタートアップ オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f5a5f-132">Startup Object</span></span></td>
<td><span data-ttu-id="f5a5f-133">プロジェクトの実行時に呼び出されるオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-133">The object that will be invoked when the project is run.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5a5f-134">法人</span><span class="sxs-lookup"><span data-stu-id="f5a5f-134">Company</span></span></td>
<td><span data-ttu-id="f5a5f-135">プロジェクトの実行時に使用される既定の会社。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-135">The default company that will be used when the project is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5a5f-136">パーティション</span><span class="sxs-lookup"><span data-stu-id="f5a5f-136">Partition</span></span></td>
<td><span data-ttu-id="f5a5f-137">プロジェクトの実行時に使用されるパーティション。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-137">The partition that will be used when the project is run.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5a5f-138">プロジェクト ファイル</span><span class="sxs-lookup"><span data-stu-id="f5a5f-138">Project File</span></span></td>
<td><span data-ttu-id="f5a5f-139">プロジェクトに関する情報を含むファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-139">The name of the file that contains information about the project.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5a5f-140">プロジェクト フォルダー</span><span class="sxs-lookup"><span data-stu-id="f5a5f-140">Project Folder</span></span></td>
<td><span data-ttu-id="f5a5f-141">プロジェクトの場所。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-141">The location of the project.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5a5f-142">モデル</span><span class="sxs-lookup"><span data-stu-id="f5a5f-142">Model</span></span></td>
<td><span data-ttu-id="f5a5f-143">プロジェクトが関連付けられているモデル。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-143">The model that the project is associated with.</span></span> <span data-ttu-id="f5a5f-144">プロジェクト内のすべての要素は選択されたモデルにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-144">All elements in the project must be in the selected model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5a5f-145">モデル発行元</span><span class="sxs-lookup"><span data-stu-id="f5a5f-145">Model Publisher</span></span></td>
<td><span data-ttu-id="f5a5f-146">モデルの発行元を示す読み取り専用の値。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-146">A read-only value that indicates the publisher of the model.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f5a5f-147">レイヤー</span><span class="sxs-lookup"><span data-stu-id="f5a5f-147">Layer</span></span></td>
<td><span data-ttu-id="f5a5f-148">モデルが配置されているアプリケーション レイヤーを示す読み取り専用の値。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-148">A read-only value that indicates the application layer that the model is located in.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f5a5f-149">ビルド上にデータベースを同期</span><span class="sxs-lookup"><span data-stu-id="f5a5f-149">Synchronize database on build</span></span></td>
<td><span data-ttu-id="f5a5f-150">プロジェクトのビルド アクションが実行されたときにテーブルの同期操作が実行されるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-150">A value that indicates whether the synchronize operation for tables will be performed when the build action is performed for the project.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f5a5f-151">これらのプロパティの中で、**モデル**プロパティが特に重要です。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-151">Of these properties, the **Model** property is particularly important.</span></span> <span data-ttu-id="f5a5f-152">プロジェクトに関連付けられているモデルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-152">You must specify which model the project is associated with.</span></span> <span data-ttu-id="f5a5f-153">作成またはプロジェクトに追加されるすべての要素はこのモデルの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-153">All the elements that you create or add to the project must be part of this model.</span></span> <span data-ttu-id="f5a5f-154">**スタートアップ オブジェクト タイプ** および **スタートアップ オブジェクト** プロパティは、アプリケーションをテストしてデバッグする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-154">The **Startup Object type** and **Startup Object** properties are useful when you test and debug your application.</span></span> <span data-ttu-id="f5a5f-155">プロジェクトを起動すると (デバッグの場合は F5 キー、デバッグなしの場合は Ctrl+F5 キーを押します)、指定のフォームが読み込まれるか、または指定されたクラスの **main()** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-155">When you start your project (by pressing F5 for debugging or Ctrl+F5 for no debugging), the specified form will be loaded, or the **main()** method from the specified class will be run.</span></span> <span data-ttu-id="f5a5f-156">このメソッドには、次の署名が必要です。public static void Main(Args \_args)</span><span class="sxs-lookup"><span data-stu-id="f5a5f-156">The method must have the following signature: public static void main(Args \_args)</span></span>

## <a name="add-elements-to-a-project"></a><span data-ttu-id="f5a5f-157">プロジェクトへの要素の追加</span><span class="sxs-lookup"><span data-stu-id="f5a5f-157">Add elements to a project</span></span>
<span data-ttu-id="f5a5f-158">既存の要素をプロジェクトに追加する方法はいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-158">There are several ways to add existing elements to a project.</span></span> <span data-ttu-id="f5a5f-159">最も一般的なものを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-159">Here are the most typical:</span></span>

-   <span data-ttu-id="f5a5f-160">ソリューション エクスプ ローラーでプロジェクトを選択した後、アプリケーション エクスプローラーで要素を見つけ、右クリックし、次に**プロジェクトに追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-160">After you select the project in Solution Explorer, you can find the element in Application Explorer, right-click it, and then click **Add to Project**.</span></span> <span data-ttu-id="f5a5f-161">これは最も簡単なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-161">This is the simplest method.</span></span>
-   <span data-ttu-id="f5a5f-162">ドラッグ アンド ドロップ操作を使用して、アプリケーション エクスプ ローラーからプロジェクトに要素を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-162">You can use drag-and-drop operations to add an element from Application Explorer to a project.</span></span>
-   <span data-ttu-id="f5a5f-163">検索結果を単一のモデルに限定する場合は、アプリケーションのエクスプローラーでフィルターの結果をプロジェクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-163">If you're limiting your search results to a single model, you can add the results of a filter in Application Explorer to a project.</span></span>

<span data-ttu-id="f5a5f-164">要素を追加した後、ソリューション エクスプローラーを使用してフォルダーをグループ化することによりそれらを簡単に見つけることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-164">After you've added the elements, you might want to use Solution Explorer to group them into folders, so that they are easier to find.</span></span> <span data-ttu-id="f5a5f-165">プロジェクト ファイルとプロジェクトで作成するフォルダーの場所は、モデル要素を表す XML ファイルの場所には影響しません。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-165">The location of the project file and the folders that you create in the project don’t affect the location of the XML files that represent the model elements.</span></span> <span data-ttu-id="f5a5f-166">モデル要素は、常にモデル ストア内の適切なフォルダーに格納されます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-166">The model elements are always stored in the appropriate folder in the model store.</span></span> <span data-ttu-id="f5a5f-167">要素をフォルダにまとめるには、**要素タイプ別にプロジェクトを整理する** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-167">To organize elements into folders, select the **Organize projects by element type** option.</span></span> <span data-ttu-id="f5a5f-168">**Dynamics 365** メニューで、**オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-168">On the **Dynamics 365** menu, click **Options**.</span></span> <span data-ttu-id="f5a5f-169">**プロジェクト** カテゴリを選択して、このオプションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-169">Select the **Projects** category to see this option.</span></span> <span data-ttu-id="f5a5f-170">このオプションが選択されているときは、新規または既存のプロジェクトに追加される要素 (アプリケーション エクスプ ローラーの検索結果がプロジェクトに追加されるときなど) は、要素タイプ名に基づいて、フォルダーにグループ分けされます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-170">When this option is selected, elements that are added to a new or existing project (such as when search results in Application Explorer are added to a project) are grouped into folders, based on the element type name.</span></span> <span data-ttu-id="f5a5f-171">プロジェクトの新しい要素を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-171">To create a new element for a project, follow these steps.</span></span>

1.  <span data-ttu-id="f5a5f-172">ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-172">In Solution Explorer, right-click the project, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="f5a5f-173">**Operations コンポーネント** リストで、作成する要素のカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-173">In the **Operations Artifacts** list, select the category of element to create.</span></span>
3.  <span data-ttu-id="f5a5f-174">特定の要素タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-174">Select the specific element type.</span></span>
4.  <span data-ttu-id="f5a5f-175">要素名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-175">Enter a name for the element.</span></span>
5.  <span data-ttu-id="f5a5f-176">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-176">Click **Add**.</span></span> <span data-ttu-id="f5a5f-177">要素がプロジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-177">The element will be added to the project.</span></span> <span data-ttu-id="f5a5f-178">プロジェクトが関連付けられているモデル ストアのモデルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-178">It will also be added to the model in the model store that the project is associated with.</span></span>

<span data-ttu-id="f5a5f-179">新しい要素を追加した後、ソリューション エクスプローラーを使用してプロジェクト内のフォルダに移動することにより簡単に見つけることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-179">After you've added the new element, you might want to use Solution Explorer to move it into a folder in the project, so that it's easier to find.</span></span>

## <a name="export-a-projects-as-an-axpp-file"></a><span data-ttu-id="f5a5f-180">プロジェクトを .axpp ファイルとしてエクスポート</span><span class="sxs-lookup"><span data-stu-id="f5a5f-180">Export a projects as an .axpp file</span></span>
<span data-ttu-id="f5a5f-181">要素を別のインストールに転送するには、プロジェクト パッケージ ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-181">To transfer elements to a different installation, you can use a project package file.</span></span> <span data-ttu-id="f5a5f-182">プロジェクト パッケージ ファイルは、.axpp ファイル名拡張子を持ちます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-182">Project package files have the .axpp file name extension.</span></span> <span data-ttu-id="f5a5f-183">プロジェクト パッケージには、プロジェクトからのすべての要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-183">A project package contains all the elements from the project.</span></span> <span data-ttu-id="f5a5f-184">プロジェクトをエクスポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-184">To export a project, follow these steps.</span></span>

1.  <span data-ttu-id="f5a5f-185">ソリューション エクスプローラーで、エクスポートするプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-185">In Solution Explorer, select the project to export.</span></span>
2.  <span data-ttu-id="f5a5f-186">**プロジェクト**メニューで、**プロジェクトのエクスポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-186">On the **Project** menu, click **Export Project**.</span></span> <span data-ttu-id="f5a5f-187">(メニューのコマンドは、選択したプロジェクトの名前が含みます。)</span><span class="sxs-lookup"><span data-stu-id="f5a5f-187">(The command on the menu will contain the name of the selected project.)</span></span>
3.  <span data-ttu-id="f5a5f-188">プロジェクト パッケージ ファイル名を入力し、場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-188">Enter a name for the project package file, and select a location.</span></span>
4.  <span data-ttu-id="f5a5f-189">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-189">Click **Save**.</span></span>

## <a name="import-an-axpp-file"></a><span data-ttu-id="f5a5f-190">.axpp ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="f5a5f-190">Import an .axpp file</span></span>
<span data-ttu-id="f5a5f-191">プロジェクト パッケージ ファイルの内容を使用するには、.axpp ファイルをインストールにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-191">To use the contents of a project package file, you must import the .axpp file into an installation.</span></span> <span data-ttu-id="f5a5f-192">プロジェクト パッケージ ファイルの要素は、エクスポートされたものと同じモデルにインポートされます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-192">The elements from the project package file will be imported into the same model that they were exported from.</span></span> <span data-ttu-id="f5a5f-193">インストールにそのモデルが存在しない場合は、インポート処理中に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-193">If that model doesn’t exist in the installation, it will be created during the import process.</span></span> <span data-ttu-id="f5a5f-194">プロジェクト パッケージ ファイルをインポートするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-194">To import a project package file, follow these steps.</span></span>

1.  <span data-ttu-id="f5a5f-195">**Dynamics 365**  メニューで、**プロジェクトのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-195">On the **Dynamics 365** menu, click **Import Project**.</span></span>
2.  <span data-ttu-id="f5a5f-196">**プロジェクトのインポート** ダイアログ ボックスで、インポートするプロジェクト パッケージ (.axpp) ファイルの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-196">In the **Import Project** dialog box, specify the location of the project package (.axpp) file to import.</span></span>
3.  <span data-ttu-id="f5a5f-197">プロジェクト パッケージ ファイルの要素により、既存の要素が上書きされる場合は、**要素の上書き**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-197">If you want elements from the project package file to overwrite any existing elements, select **Overwrite Elements**.</span></span>
4.  <span data-ttu-id="f5a5f-198">プロジェクトを現在の選択で開くのか、新しいソリューションで開くのか、まったく開かないのかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-198">Specify whether you want to open the project in the current selection, in a new solution, or not at all.</span></span>
5.  <span data-ttu-id="f5a5f-199">**詳細**フィールドで、インポートされる要素を確認します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-199">In the **Details** field, review the elements that will be imported.</span></span> <span data-ttu-id="f5a5f-200">インポートしない任意の要素の横にあるチェック ボックスをクリアすることができます。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-200">You can clear the check box next to any elements that you don't want to import.</span></span> <span data-ttu-id="f5a5f-201">[![17\_DevoToolsConcept](./media/17_devotoolsconcept.png)](./media/17_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="f5a5f-201">[![17\_DevoToolsConcept](./media/17_devotoolsconcept.png)](./media/17_devotoolsconcept.png)</span></span>
6.  <span data-ttu-id="f5a5f-202">**OK** をクリックしてインポート プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="f5a5f-202">Click **OK** to complete the import process.</span></span>




