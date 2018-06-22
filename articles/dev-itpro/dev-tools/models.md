---
title: "モデル"
description: "この記事では、モデルとパッケージの概念について説明します。 また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。"
author: robadawy
manager: AnnBe
ms.date: 05/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 83351
ms.assetid: 66a32ee2-8c4f-4ae5-b022-ad1bb4f97e59
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 80683d2b8b93d4d7973141a8605a9bf391eca20e
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="models"></a><span data-ttu-id="d0971-104">モデル</span><span class="sxs-lookup"><span data-stu-id="d0971-104">Models</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d0971-105">この記事では、モデルとパッケージの概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="d0971-105">This article describes the concept of models and packages.</span></span> <span data-ttu-id="d0971-106">また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="d0971-106">It also explains how to use the development tools in Microsoft Visual Studio to create new models, how to update the parameters of existing models, and how to visualize dependencies between models.</span></span>

<span data-ttu-id="d0971-107">モデル ストアのモデルを操作するには、Microsoft Visual Studio のツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0971-107">To work with models in the model store, you use tools in Microsoft Visual Studio.</span></span> <span data-ttu-id="d0971-108">新しいモデルを作成、および既存のモデルのパラメータを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-108">You can create new models and change parameters for existing models.</span></span>

## <a name="conceptual-overview"></a><span data-ttu-id="d0971-109">概念に関する概要</span><span class="sxs-lookup"><span data-stu-id="d0971-109">Conceptual overview</span></span>
<span data-ttu-id="d0971-110">モデルは、通常、配布可能なソフトウェア ソリューションを構成するメタデータとソース ファイルなどの要素のグループであり、既存のソリューションのカスタマイズを含みます。</span><span class="sxs-lookup"><span data-stu-id="d0971-110">A model is a group of elements, such as metadata and source files, that typically constitute a distributable software solution and includes customizations of an existing solution.</span></span> <span data-ttu-id="d0971-111">モデルは、倉庫管理モデルやプロジェクト会計モデルなどのデザイン時概念です。</span><span class="sxs-lookup"><span data-stu-id="d0971-111">A model is a design-time concept, for example a warehouse management model or a project accounting model.</span></span> <span data-ttu-id="d0971-112">モデルは、常に 1 つのパッケージに属しています。</span><span class="sxs-lookup"><span data-stu-id="d0971-112">A model always belongs to a package.</span></span> <span data-ttu-id="d0971-113">パッケージは、1 つまたは複数のモデルの配置およびコンパイル単位です。</span><span class="sxs-lookup"><span data-stu-id="d0971-113">A package is a deployment and compilation unit of one or more models.</span></span> <span data-ttu-id="d0971-114">これには、モデル メタデータ、バイナリ、およびその他の関連するリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d0971-114">It includes model metadata, binaries, and other associated resources.</span></span> <span data-ttu-id="d0971-115">1 つ以上のパッケージは、ランタイム環境の配置に使用する車両の配置可能パッケージにパッケージすることができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-115">One or more packages can be packaged into a deployable package, which is the vehicle used for deployment on runtime environments.</span></span>

<span data-ttu-id="d0971-116">[パッケージ、モデル、およびプロジェクト](https://mix.office.com/watch/ies6lyit6773) Office Mix は、モデルとパッケージおよび相互にどのように関連しているかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d0971-116">The [Packages, models, and projects](https://mix.office.com/watch/ies6lyit6773) Office Mix describes models and packages and how they relate to each other.</span></span>

## <a name="creating-a-new-model"></a><span data-ttu-id="d0971-117">新しいモデルを作成しています</span><span class="sxs-lookup"><span data-stu-id="d0971-117">Creating a new model</span></span>
<span data-ttu-id="d0971-118">**モデルの作成** ウィザードを使用して、新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0971-118">You use the **Create model** wizard to create new models.</span></span> <span data-ttu-id="d0971-119">このウィザードには **Dynamics 365** メニューの **モデル管理** からアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-119">You can access this wizard from **Model Management** on the **Dynamics 365**menu.</span></span> <span data-ttu-id="d0971-120">モデルは 2 種類作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-120">You can create two types of models:</span></span>

-   <span data-ttu-id="d0971-121">**固有のパッケージに配置されているモデル** - このタイプのモデルを使用して、新しいモデル要素を作成し、参照モデルのメタデータとビジネス ロジックを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-121">**A model that is deployed in its own package** – You can use this type of model to create new model elements, and extend the metadata and business logic of referenced models.</span></span> <span data-ttu-id="d0971-122">このウィザードでは、参照モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d0971-122">The wizard lets you select the referenced models.</span></span> <span data-ttu-id="d0971-123">このタイプのモデルは、独自のアセンブリとバイナリにコンパイルされるため、一般的なアップグレード、展開、アプリケーション ライフサイクル管理のコストが削減され、簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="d0971-123">This type of model is compiled into its own assembly and binaries, and will simplify and reduce the cost of upgrades, deployment, and application lifecycle management in general.</span></span>
-   <span data-ttu-id="d0971-124">**既存のパッケージの一部であるモデル** - このタイプのモデルを使用して、ソース コードおよびメタデータのオーバーレイなどの高度なカスタマイズを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-124">**A model that is a part of an existing package** – You can use this type of model to perform advanced customizations, such as overlayering source code and metadata.</span></span>

<span data-ttu-id="d0971-125">**モデルの作成** ウィザードが完了したとき、新しいプロジェクトの作成を選択した場合、名前とその場所を指定するための入力を要求されます。</span><span class="sxs-lookup"><span data-stu-id="d0971-125">When the **Create model** wizard is completed, if you chose to create a new project, you will be prompted to specify a name and location for it.</span></span>

## <a name="updating-model-parameters"></a><span data-ttu-id="d0971-126">モード パラメーターの更新</span><span class="sxs-lookup"><span data-stu-id="d0971-126">Updating model parameters</span></span>
<span data-ttu-id="d0971-127">モデルのパラメーターを変更する必要がある場合は、**更新モデル パラメーター** ダイアログ ボックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0971-127">If you must change the parameters for a model, you can use the **Update model parameters** dialog box.</span></span>

1.  <span data-ttu-id="d0971-128">**Dynamics 365** メニューで、**モデル管理**をポイントし、**モデルのパラメーターの更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0971-128">On the **Dynamics 365** menu, point to **Model Management**, and then click **Update model parameters**.</span></span>
2.  <span data-ttu-id="d0971-129">**モデル名**フィールドで、パラメーターを更新するモデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0971-129">In the **Model name** field, select the model to update parameters for.</span></span>
3.  <span data-ttu-id="d0971-130">必要に応じてパラメーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="d0971-130">Update the parameters as you require.</span></span>
4.  <span data-ttu-id="d0971-131">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0971-131">Click **Next**.</span></span>
5.  <span data-ttu-id="d0971-132">変更が必要な場合は、現在のモデルの依存関係情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="d0971-132">Update the dependency information for the current model, if changes are required.</span></span>
6.  <span data-ttu-id="d0971-133">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0971-133">Click **Next**.</span></span> <span data-ttu-id="d0971-134">モデルの要約情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d0971-134">The summary information for the model is displayed.</span></span>
7.  <span data-ttu-id="d0971-135">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0971-135">Click **Finish**.</span></span>

<span data-ttu-id="d0971-136">更新されたモデル パラメーターは、Visual Studio を再起動した後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="d0971-136">The updated model parameters become effective only after you restart Visual Studio.</span></span>

## <a name="viewing-package-dependencies"></a><span data-ttu-id="d0971-137">パッケージの依存関係の表示</span><span class="sxs-lookup"><span data-stu-id="d0971-137">Viewing package dependencies</span></span>
<span data-ttu-id="d0971-138">どのパッケージとそのモデルに他のパッケージへの依存関係があるかを示す、グラフィック表現を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d0971-138">You can create a graphical representation that shows which packages and their models have dependencies on other packages.</span></span> <span data-ttu-id="d0971-139">**Dynamics 365** メニューで、**モデル管理**をポイントし、**パッケージの依存関係の表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0971-139">On the **Dynamics 365** menu, point to **Model Management**, and then click **View package dependencies**.</span></span> <span data-ttu-id="d0971-140">現在のパッケージとそのモデルについて、有向グラフ マークアップ言語 (DGML) 図が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d0971-140">A Directed Graph Markup Language (DGML) diagram will be generated for the current packages and their models.</span></span> <span data-ttu-id="d0971-141">この図は、それぞれがパッケージを表す相互依存ノードの集合です。</span><span class="sxs-lookup"><span data-stu-id="d0971-141">This diagram is a collection of interdependent nodes, each of which represents a package.</span></span> <span data-ttu-id="d0971-142">各ノードでは、パッケージに属するすべてのモデルを表示します。</span><span class="sxs-lookup"><span data-stu-id="d0971-142">Each node lists all the models that belong to that package.</span></span> <span data-ttu-id="d0971-143">追加のツールは、強化または図を簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="d0971-143">Additional tools let you enhance or simplify the diagram.</span></span> <span data-ttu-id="d0971-144">たとえば、コメントを追加したり、ノードをあちこちに移動したり、またはノードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="d0971-144">For example, you can add comments, move nodes around, or remove nodes.</span></span> <span data-ttu-id="d0971-145">また、次の手順で、単一モデルのパッケージ依存関係を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="d0971-145">You can also view package dependencies of a single model by following these steps:</span></span>

1.  <span data-ttu-id="d0971-146">アプリケーション エクスプローラーがモデル ビューになっていることを確認します。AOT ノードを右クリックし、モデル ビューを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0971-146">Make sure the Application Explorer is in Model view: Right-click on the AOT node and select Model view.</span></span>
2.  <span data-ttu-id="d0971-147">任意のモデルを右クリックし、**パッケージの依存関係を表示** > **送信参照を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0971-147">Right-click on any model and select **View package dependencies** > **View outgoing references.**</span></span>

<span data-ttu-id="d0971-148">選択したモデルが依存するすべてのパッケージのグラフが生成されます。</span><span class="sxs-lookup"><span data-stu-id="d0971-148">This will generate a graph of all packages that the selected model depends on.</span></span> 

![ビューの相互関係](./media/viewdependencies2.png) 

![ディレクトリ依存関係](./media/directorydependencies.png)

## <a name="deleting-a-model"></a><span data-ttu-id="d0971-151">モデルの削除</span><span class="sxs-lookup"><span data-stu-id="d0971-151">Deleting a model</span></span>
<span data-ttu-id="d0971-152">開発またはテスト環境では、次の手順に従ってモデルを削除します。</span><span class="sxs-lookup"><span data-stu-id="d0971-152">On a development or test environment, follow these steps to delete a model.</span></span>

<span data-ttu-id="d0971-153">次の手順では、ローカル モデル ストア フォルダーが C:\AOSService\PackagesLocalDirectory であり、モデルの名前が MyModel1 であると想定しています。</span><span class="sxs-lookup"><span data-stu-id="d0971-153">The following steps assume the local model store folder is C:\AOSService\PackagesLocalDirectory and your model is named MyModel1.</span></span>

<span data-ttu-id="d0971-154">モデルがそれ自身のパッケージに属している場合 (たとえば: パッケージに他のモデルがない拡張機能パッケージ):</span><span class="sxs-lookup"><span data-stu-id="d0971-154">If your model belongs to its own package (For example: An extension package with no other models in the package):</span></span>
1. <span data-ttu-id="d0971-155">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="d0971-155">Stop the following services: The AOS web service and the Batch Management Service</span></span>
2. <span data-ttu-id="d0971-156">パッケージ フォルダー  C:\AOSService\PackagesLocalDirectory\MyModel1 を削除します</span><span class="sxs-lookup"><span data-stu-id="d0971-156">Delete the package folder  C:\AOSService\PackagesLocalDirectory\MyModel1</span></span>
3. <span data-ttu-id="d0971-157">手順 1 からサービスを再開</span><span class="sxs-lookup"><span data-stu-id="d0971-157">Restart the services from step 1</span></span>
4. <span data-ttu-id="d0971-158">Visual Studio を実行している場合、モデルを更新します (Visual Studio > Dynamics 365 > モデル管理 > モデルの更新)</span><span class="sxs-lookup"><span data-stu-id="d0971-158">If Visual Studio is running, refresh your models (Visual Studio > Dynamics 365 > Model management > Refresh models)</span></span>
5. <span data-ttu-id="d0971-159">Visual Studio で、完全なデータベース同期を実行します (Visual Studio > Dynamics 365 > データベースの同期...)</span><span class="sxs-lookup"><span data-stu-id="d0971-159">In Visual Studio, perform a full database synchronization (Visual Studio > Dynamics 365 > Synchronize database...)</span></span>

<span data-ttu-id="d0971-160">モデルが、複数のモデルを持つパッケージに属している場合 (MyModel1 がアプリケーション スイートにオーバーレイする場合など):</span><span class="sxs-lookup"><span data-stu-id="d0971-160">If your model belongs to a package with multiple models (For example, MyModel1 overlays Application Suite):</span></span>
1. <span data-ttu-id="d0971-161">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス</span><span class="sxs-lookup"><span data-stu-id="d0971-161">Stop the following services: The AOS web service and the Batch Management Service</span></span>
2. <span data-ttu-id="d0971-162">モデル フォルダー  C:\AOSService\PackagesLocalDirectory\<PackageName>\MyModel1 (In this example PackageName=ApplicationSuite) を削除します</span><span class="sxs-lookup"><span data-stu-id="d0971-162">Delete the model folder  C:\AOSService\PackagesLocalDirectory\<PackageName>\MyModel1 (In this example PackageName=ApplicationSuite)</span></span>
3. <span data-ttu-id="d0971-163">手順 1 からサービスを再開</span><span class="sxs-lookup"><span data-stu-id="d0971-163">Restart the services from step 1</span></span>
4. <span data-ttu-id="d0971-164">Visual Studio で、モデルを更新します (Visual Studio > Dynamics 365 > モデル管理 > モデルの更新)。</span><span class="sxs-lookup"><span data-stu-id="d0971-164">In Visual Studio, refresh your models (Visual Studio > Dynamics 365 > Model management > Refresh models)</span></span>
5. <span data-ttu-id="d0971-165">Visual Studio で、削除したモデルが属しているパッケージをビルドします (Visual Studio > Dynamics 365 > モデルをビルド...)</span><span class="sxs-lookup"><span data-stu-id="d0971-165">In Visual Studio, build the package that the deleted models belonged to (Visual Studio > Dynamics 365 > Build models...)</span></span>
6. <span data-ttu-id="d0971-166">Visual Studio で、完全なデータベース同期を実行します (Visual Studio > Dynamics 365 > データベースの同期...)</span><span class="sxs-lookup"><span data-stu-id="d0971-166">In Visual Studio, perform a full database synchronization (Visual Studio > Dynamics 365 > Synchronize database...)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0971-167">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d0971-167">Additional resources</span></span>

[<span data-ttu-id="d0971-168">開発ツールの概要</span><span class="sxs-lookup"><span data-stu-id="d0971-168">Development tools overview</span></span>](development-tools-overview.md)

[<span data-ttu-id="d0971-169">開発者ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="d0971-169">Developer home page</span></span>](developer-home-page.md)

[<span data-ttu-id="d0971-170">モデルの配分: モデル ファイルをエクスポートおよびインポートする方法</span><span class="sxs-lookup"><span data-stu-id="d0971-170">Distribution of models: How to export and import model files</span></span>](models-export-import.md)




