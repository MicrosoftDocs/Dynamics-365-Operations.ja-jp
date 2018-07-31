---
title: "ビルド操作"
description: "このトピックでは、プロジェクトのビルド プロセスとモデル パッケージの完全なビルドについて説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 76764
ms.assetid: f061b6cf-16f7-440e-94b9-f40666dd7431
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 87928ab631c346d2c379c6fe977b5606985a5ba6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="build-operations"></a><span data-ttu-id="26af9-103">ビルド操作</span><span class="sxs-lookup"><span data-stu-id="26af9-103">Build operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26af9-104">このトピックでは、プロジェクトのビルド プロセスとモデル パッケージの完全なビルドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="26af9-104">This topic reviews the process to build projects and full build of model packages.</span></span>

<span data-ttu-id="26af9-105">モデルの要素は、アプリケーションで使用できるように構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-105">The elements of a model must be built so that they can be used by the application.</span></span> <span data-ttu-id="26af9-106">要素をプロジェクト内にビルドすることができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-106">You can build the elements in a project.</span></span> <span data-ttu-id="26af9-107">また、モデル内のすべての要素をビルドすることもできます。</span><span class="sxs-lookup"><span data-stu-id="26af9-107">You can also build all the elements in a model.</span></span> <span data-ttu-id="26af9-108">ビルド操作中に次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-108">The following actions are performed during a build operation:</span></span>

-   <span data-ttu-id="26af9-109">メタデータの検証</span><span class="sxs-lookup"><span data-stu-id="26af9-109">Metadata validation</span></span>
-   <span data-ttu-id="26af9-110">X++ コードの検証</span><span class="sxs-lookup"><span data-stu-id="26af9-110">X++ code validation</span></span>
-   <span data-ttu-id="26af9-111">推奨チェック</span><span class="sxs-lookup"><span data-stu-id="26af9-111">Best practice checks</span></span>
-   <span data-ttu-id="26af9-112">レポート RDL の生成</span><span class="sxs-lookup"><span data-stu-id="26af9-112">Report RDL generation</span></span>
-   <span data-ttu-id="26af9-113">コンパイル、IL 生成、および .NET アセンブリの作成</span><span class="sxs-lookup"><span data-stu-id="26af9-113">Compilation, IL generation, and creation of the .NET assemblies</span></span>
-   <span data-ttu-id="26af9-114">ラベル アセンブリの生成および他のリソース ファイルの配置</span><span class="sxs-lookup"><span data-stu-id="26af9-114">Label assembly generation and deployment of other resource files</span></span>
-   <span data-ttu-id="26af9-115">データベース同期</span><span class="sxs-lookup"><span data-stu-id="26af9-115">Database synchronization</span></span>

## <a name="build-a-project"></a><span data-ttu-id="26af9-116">プロジェクトのビルド</span><span class="sxs-lookup"><span data-stu-id="26af9-116">Build a project</span></span>

<span data-ttu-id="26af9-117">プロジェクトを作成するときは、新規の要素か、変更された要素のみが作成されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-117">When you build a project, only those elements that are new or that have changed are built.</span></span> <span data-ttu-id="26af9-118">プロジェクトをビルドするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="26af9-118">To build a project, follow these steps.</span></span>

1.  <span data-ttu-id="26af9-119">ソリューション エクスプローラーで、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="26af9-119">In Solution Explorer, select the project.</span></span>
2.  <span data-ttu-id="26af9-120">**ビルド**メニューで、**ビルド&lt;プロジェクト名&gt;** をクリックして、ビルド プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="26af9-120">On the **Build** menu, click **Build &lt;project name&gt;** to start the build process.</span></span> <span data-ttu-id="26af9-121">または、ソリューション エクスプローラーでプロジェクトを右クリックし、その後**ビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26af9-121">Alternatively, right-click the project in Solution Explorer, and then click **Build**.</span></span>

<span data-ttu-id="26af9-122">ビルド プロセス中に、ビルドされている要素の一部がプロジェクトの一部ではないことに気付くかもしれません。</span><span class="sxs-lookup"><span data-stu-id="26af9-122">During the build process, you might notice that some elements that are built aren't part of the project.</span></span> <span data-ttu-id="26af9-123">この動作は、アセンブリの作成方法のために必要です。</span><span class="sxs-lookup"><span data-stu-id="26af9-123">This behavior is required because of the way that assemblies are created.</span></span> <span data-ttu-id="26af9-124">要素を作成するときは、実際には、要素が組み込まれる .NET モジュールを作成します。</span><span class="sxs-lookup"><span data-stu-id="26af9-124">When you build an element, you’re actually building the .NET module that the element is included in.</span></span> <span data-ttu-id="26af9-125">1 つの .NET モジュールには、複数のモデル要素が含まれ、1 つのアセンブリには、複数の .NET モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="26af9-125">A single .NET module contains multiple model elements, and a single assembly contains multiple .NET modules.</span></span> <span data-ttu-id="26af9-126">アセンブリ内のすべての .NET モジュールが構築されており、最新の状態である場合にのみ、アセンブリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-126">The assembly can be created only if all the .NET modules in the assembly have been built and are up to date.</span></span> <span data-ttu-id="26af9-127">アセンブリの .NET モジュール内の要素がビルドされていないまたは最新の状態になっていない場合は、現在のプロジェクトに含まれていない場合でもビルドされます。</span><span class="sxs-lookup"><span data-stu-id="26af9-127">If any elements in any of the .NET modules for an assembly haven’t been built or aren't up to date, they will be built, even if they aren’t included in the current project.</span></span> 

> [!NOTE]
> <span data-ttu-id="26af9-128">プロジェクトから要素を削除する場合は、削除を有効にする前にプロジェクトを再構築するか、モデルで完全なビルドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-128">If you delete an element from a project, you must rebuild the project or perform a full build on the model before the deletion takes effect.</span></span>

## <a name="rebuild-a-project"></a><span data-ttu-id="26af9-129">プロジェクトのリビルド</span><span class="sxs-lookup"><span data-stu-id="26af9-129">Rebuild a project</span></span>

<span data-ttu-id="26af9-130">変更したかどうかに関係なく、プロジェクトにすべての要素を作成する場合は、再構築処理を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-130">If you want to build all the elements in a project, regardless of whether they have changed, you must perform a rebuild operation.</span></span> <span data-ttu-id="26af9-131">プロジェクトをリビルドするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="26af9-131">To rebuild a project, follow these steps.</span></span>

1.  <span data-ttu-id="26af9-132">ソリューション エクスプローラーで、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="26af9-132">In Solution Explorer, select the project.</span></span>
2.  <span data-ttu-id="26af9-133">**ビルド**ニューで、**再構築&lt;プロジェクト名&gt;** をクリックして、再構築プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="26af9-133">On the **Build** menu, click **Rebuild &lt;project name&gt;** to start the rebuild process.</span></span> <span data-ttu-id="26af9-134">または、ソリューション エクスプローラーでプロジェクトを右クリックし、その後**再構築**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26af9-134">Alternatively, right-click the project in Solution Explorer, and then click **Rebuild**.</span></span>

## <a name="synchronizing-the-database-at-each-build"></a><span data-ttu-id="26af9-135">ビルドごとにデータベースを同期</span><span class="sxs-lookup"><span data-stu-id="26af9-135">Synchronizing the database at each build</span></span>

<span data-ttu-id="26af9-136">プロジェクトのプロパティを使用して、プロジェクトをビルドするたびにデータベースの同期操作を実行するように指定できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-136">A project property lets you specify that the synchronize operation for the database should be performed every time that you build the project.</span></span> <span data-ttu-id="26af9-137">これは、アプリケーションのテーブル構造を変更する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="26af9-137">This can be useful when you’re making changes to the table structure for an application.</span></span> <span data-ttu-id="26af9-138">ビルドを実行するたびに、データベースはプロジェクトで定義されているテーブルと同期されていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="26af9-138">Each time that you build, you will know that the database is synchronized with the tables as they are defined in the project.</span></span> <span data-ttu-id="26af9-139">プロジェクト プロパティの設定方法の詳細については、[プロジェクト](projects.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="26af9-139">For information about how to set project properties, see [Projects](projects.md).</span></span> <span data-ttu-id="26af9-140">アプリケーションに多数のテーブルがあり、アプリケーションをまだテストしていない場合、**ビルドでデータベースの同期**プロパティを **false** に設定できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-140">If your application has a large number of tables, and you aren’t yet testing the application, you can set the **Synchronize database on build** property to **false**.</span></span> <span data-ttu-id="26af9-141">この変更により、プロジェクトのビルドに必要な時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-141">This change will reduce the time that is required to build the project.</span></span> <span data-ttu-id="26af9-142">次にテストを開始するときは、必ずこのプロパティを **true** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="26af9-142">Then, when you begin testing, be sure to set this property back to **true**.</span></span> <span data-ttu-id="26af9-143">プロジェクトに含まれるテーブルを手動で同期する必要がある場合は、ソリューション エクスプローラーで、プロジェクトを右クリックし、**同期 &lt; プロジェクト名 &gt; データベース**をクリックできます。</span><span class="sxs-lookup"><span data-stu-id="26af9-143">If you must manually synchronize the tables in a project, you can right-click the project in Solution Explorer and then click **Synchronize &lt;project name&gt; with database**.</span></span> <span data-ttu-id="26af9-144">**Dynamics 365** メニューでプロセス (長いプロセスとなる可能性がある) データベース全体を同期させるには、**データベースの同期** をクリックします。します。</span><span class="sxs-lookup"><span data-stu-id="26af9-144">To synchronize the entire database, which can be a long process, on the **Dynamics 365** menu, click **Synchronize database**.</span></span>

> [!NOTE]
> <span data-ttu-id="26af9-145">アセンブリを完全にコンパイルする前にデータベースを同期しようとすると、Visual Studio データベース同期ツールには、同期が正常に完了したことを示すメッセージが表示されますが、実際には同期は成功していません。</span><span class="sxs-lookup"><span data-stu-id="26af9-145">If you try to synchronize the database before you have fully compiled assemblies, the Visual Studio database synchronization tool will display a message that synchronization has completed successfully, when in fact, the synchronization was not successful.</span></span>

<span data-ttu-id="26af9-146">テーブルおよびビューは、完全にコンパイルするまでに、データベースに対して同期することはできません。</span><span class="sxs-lookup"><span data-stu-id="26af9-146">Tables and views cannot be synchronized against the database until they are fully compiled.</span></span> <span data-ttu-id="26af9-147">アプリケーション プラットフォーム、アプリケーション基準、およびアプリケーション スイートの完全なビルドを完了すると、Visual Studio での Dynamics 365 メニューからデータベース同期を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-147">After you complete a full build of the Application Platform, Application Foundation, and Application Suite, you can complete a Database Synchronization from the Dynamics 365 menu in Visual Studio.</span></span> 

## <a name="build-a-models-package"></a><span data-ttu-id="26af9-148">モデルのパッケージをビルドする</span><span class="sxs-lookup"><span data-stu-id="26af9-148">Build a model's package</span></span>

<span data-ttu-id="26af9-149">特定のモデル内のすべての要素を構築する場合があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-149">You might want to build all the elements in a specific model.</span></span> <span data-ttu-id="26af9-150">これを行うには、モデルが属するパッケージでフル ビルドを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-150">To do this, you must perform a full build on the package that the model belongs to.</span></span> <span data-ttu-id="26af9-151">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="26af9-151">Follow these steps.</span></span>

1.  <span data-ttu-id="26af9-152">**Dynamics 365** メニューで、**モデルをビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26af9-152">On the **Dynamics 365** menu, click **Build models**.</span></span>
2.  <span data-ttu-id="26af9-153">**パッケージ** リストで、ビルドするパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="26af9-153">In the **Packages** list, select the package(s) to build.</span></span>
    -   <span data-ttu-id="26af9-154">パッケージ名がアルファベット順に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-154">Package names are listed alphabetically.</span></span>
    -   <span data-ttu-id="26af9-155">パッケージに属するモデルはかっこ内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-155">Models belonging to the package are shown in brackets.</span></span>

3.  <span data-ttu-id="26af9-156">依存パッケージを最初に作成する場合は、**参照パッケージのビルド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="26af9-156">If you want to build the dependent packages first, select **Build referenced packages**.</span></span> <span data-ttu-id="26af9-157">構築する必要のある依存パッケージが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-157">Any dependent package that must be built will be listed.</span></span>

    <span data-ttu-id="26af9-158">[![モデル ダイアログを構築](./media/buildmodelsdialog.png)](./media/buildmodelsdialog.png)</span><span class="sxs-lookup"><span data-stu-id="26af9-158">[![Build models dialog](./media/buildmodelsdialog.png)](./media/buildmodelsdialog.png)</span></span>
    
4.  <span data-ttu-id="26af9-159">**オプション**タブで、ビルド プロセスのオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="26af9-159">On the **Options** tab, review the options for the build process.</span></span> <span data-ttu-id="26af9-160">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-160">The following options are available.</span></span>

    | <span data-ttu-id="26af9-161">オプション</span><span class="sxs-lookup"><span data-stu-id="26af9-161">Option</span></span>                       | <span data-ttu-id="26af9-162">説明</span><span class="sxs-lookup"><span data-stu-id="26af9-162">Description</span></span>                                                                                                                                                                       |
    |------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="26af9-163">コンパイル済みのフォームをビルドする</span><span class="sxs-lookup"><span data-stu-id="26af9-163">Build Pre-Compiled Forms</span></span>     | <span data-ttu-id="26af9-164">静的 HTML は、ビルド プロセス中にフォームごとに生成されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-164">Static HTML is generated for each form during the build process.</span></span> <span data-ttu-id="26af9-165">これにより、実行時にフォームをより速くレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="26af9-165">This allows faster rendering of forms at run time.</span></span>                                                               |
    | <span data-ttu-id="26af9-166">ビルド レポート</span><span class="sxs-lookup"><span data-stu-id="26af9-166">Build Reports</span></span>                | <span data-ttu-id="26af9-167">レポートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-167">Reports are built.</span></span>                                                                                                                                                                |
    | <span data-ttu-id="26af9-168">集計の測定をビルドする</span><span class="sxs-lookup"><span data-stu-id="26af9-168">Build Aggregate Measurements</span></span> | <span data-ttu-id="26af9-169">集計の測定はビルドです。</span><span class="sxs-lookup"><span data-stu-id="26af9-169">Aggregate measurements are build.</span></span>                                                                                                                                                 |
    | <span data-ttu-id="26af9-170">ベスト プラクティス チェックを実行</span><span class="sxs-lookup"><span data-stu-id="26af9-170">Run Best Practice Checks</span></span>     | <span data-ttu-id="26af9-171">推奨チェックはビルド プロセス中に実行されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-171">Best practice checks are performed during the build process.</span></span>                                                                                                                      |
    | <span data-ttu-id="26af9-172">データベースの同期</span><span class="sxs-lookup"><span data-stu-id="26af9-172">Synchronize Database</span></span>         | <span data-ttu-id="26af9-173">SQL データベースのスキーマは、メタデータと一致するよう、(メタデータとソース コードのコンパイル後に) ビルド プロセス中に更新されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-173">The schema of the SQL database is updated during the build process (after compilation of the metadata and source code), so that it matches the metadata.</span></span>                          |
    | <span data-ttu-id="26af9-174">相互参照データのビルド</span><span class="sxs-lookup"><span data-stu-id="26af9-174">Build cross reference data</span></span>   | <span data-ttu-id="26af9-175">相互参照機能のデータは、ビルド処理中に更新されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-175">The data for the cross-reference feature is updated during the build process.</span></span> <span data-ttu-id="26af9-176">相互参照データを使用すると、開発時にコードやメタデータへの参照を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-176">Cross reference data enables developers to find references to code and metadata during development.</span></span> |

5.  <span data-ttu-id="26af9-177">**ビルド**をクリックし、ビルド プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="26af9-177">Click **Build** to start the build process.</span></span>
6.  <span data-ttu-id="26af9-178">ビルド プロセスの詳細をフォローするには、**詳細**タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="26af9-178">Expand the **Details** tab to follow details of the build process.</span></span>

## <a name="build-results"></a><span data-ttu-id="26af9-179">ビルドの結果</span><span class="sxs-lookup"><span data-stu-id="26af9-179">Build results</span></span>

<span data-ttu-id="26af9-180">ビルド操作が完了した後、Microsoft Visual Studio で結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-180">After a build operation is completed, you will see the results in Microsoft Visual Studio.</span></span> <span data-ttu-id="26af9-181">Visual Studio の **出力** ウィンドウには、ビルドのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-181">The **Output** pane in Visual Studio shows the status of the build.</span></span> <span data-ttu-id="26af9-182">**出力元の表示** フィールドを使用すると、標準的なビルド情報とビルド詳細を切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-182">You can use the **Show output from** field to switch between the standard build information and the build details.</span></span> 

<span data-ttu-id="26af9-183">[![出力ウィンドウ](./media/27_devotoolsconcept.png)](./media/27_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="26af9-183">[![Output window](./media/27_devotoolsconcept.png)](./media/27_devotoolsconcept.png)</span></span> 

<span data-ttu-id="26af9-184">Visual Studio の **エラー一覧** ウィンドウには、ビルド プロセス中に発生したビルド エラーおよび警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-184">The **Error List** pane in Visual Studio shows the build errors and warning that occurred during the build process.</span></span> <span data-ttu-id="26af9-185">ビルド エラーが表示された場合は、それらを修正してから再ビルドし、アプリケーション用の有効なアセンブリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-185">If you see any build errors, you must fix them and then build again, so that valid assemblies can be created for the application.</span></span> <span data-ttu-id="26af9-186">**エラー一覧**ウィンドウに表示される警告の多くは、アプリケーション開発のベスト プラクティスに適合するように、アプリケーションに加える必要がある変更を通知する推奨チェックです。</span><span class="sxs-lookup"><span data-stu-id="26af9-186">Many of the warnings that appear in the **Error List** pane are best practice checks that inform you of revisions that you should make to your application so that it conforms to the best practices for application development.</span></span> <span data-ttu-id="26af9-187">原則的には、アプリケーションのすべてのベスト プラクティス警告に対処する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26af9-187">Ideally, you should address all the best practice warnings for an application.</span></span> 

<span data-ttu-id="26af9-188">[![エラー一覧](./media/28_devotoolsconcept.png)](./media/28_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="26af9-188">[![Error list](./media/28_devotoolsconcept.png)](./media/28_devotoolsconcept.png)</span></span> 

<span data-ttu-id="26af9-189">ほとんどのエラーや警告をダブルクリックして、問題の原因を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-189">You can double-click most errors and warnings to see the source of the issue.</span></span> <span data-ttu-id="26af9-190">要素デザイナーまたはコード エディターが開き、エラーまたは警告の原因となっているプロパティ設定やコードを確認できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-190">The element designer or code editor will open, where you can see what property setting or code is causing the error or warning.</span></span> <span data-ttu-id="26af9-191">Visual Studio の **タスク一覧** ウィンドウには、コード内ので "TODO" とフラグが付けられたタスクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-191">The **Task List** pane in Visual Studio shows tasks that have been flagged with "TODO" comments in code.</span></span> <span data-ttu-id="26af9-192">たとえば、次のコメントは、一部のオブジェクト参照がまだ検証を要求することを示します。</span><span class="sxs-lookup"><span data-stu-id="26af9-192">For example, the following comment indicates that some object references still require validation.</span></span>

    // TODO: validate object references

<span data-ttu-id="26af9-193">コードが作成されるとき、"TODO" コメントが **タスク一覧** ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="26af9-193">When the code is built, these "TODO" comments appear in the **Task List** pane.</span></span> <span data-ttu-id="26af9-194">**作業一覧**ウィンドウを表示するには、**表示** メニューで **作業一覧** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26af9-194">To view the **Task List** pane, on the **View** menu, click **Task List**.</span></span> 

<span data-ttu-id="26af9-195">[![作業リスト](./media/29_devotoolsconcept.png)](./media/29_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="26af9-195">[![Task list](./media/29_devotoolsconcept.png)](./media/29_devotoolsconcept.png)</span></span> 

<span data-ttu-id="26af9-196">解決を容易にするために、エラーまたはタスクの影響を受ける要素を現在のプロジェクトまたは新しいプロジェクトに追加できます。</span><span class="sxs-lookup"><span data-stu-id="26af9-196">To make resolution easier, you can add the elements that are affected by the error or task to the current project or to a new project.</span></span> <span data-ttu-id="26af9-197">**エラー一覧**ウィンドウまたは**タスク一覧**ウィンドウで、修正するエラーまたはタスクの行を選択して右クリックし、**プロジェクトに追加**または**新しいプロジェクトに追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="26af9-197">In the **Error List** pane or the **Task List** pane, select the rows for the errors or tasks that you want to fix, right-click, and then click **Add to project** or **Add to new project**.</span></span> <span data-ttu-id="26af9-198">これにより、影響を受ける要素をアプリケーションで見つける手間を省くことができます。</span><span class="sxs-lookup"><span data-stu-id="26af9-198">This saves you the effort of finding the affected elements in the application.</span></span> 

<span data-ttu-id="26af9-199">[![エラー一覧](./media/30_devotoolsconcept.png)](./media/30_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="26af9-199">[![Error list](./media/30_devotoolsconcept.png)](./media/30_devotoolsconcept.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26af9-200">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="26af9-200">Additional resources</span></span>

[<span data-ttu-id="26af9-201">開発ツールの概要</span><span class="sxs-lookup"><span data-stu-id="26af9-201">Development tools overview</span></span>](development-tools-overview.md)

[<span data-ttu-id="26af9-202">開発者ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="26af9-202">Developer home page</span></span>](developer-home-page.md)




