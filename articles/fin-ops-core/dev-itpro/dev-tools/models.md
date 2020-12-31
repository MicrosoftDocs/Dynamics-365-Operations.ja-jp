---
title: モデルとパッケージ
description: このトピックでは、モデルとパッケージの概念について説明します。 また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。
author: jorisdg
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83351
ms.assetid: 66a32ee2-8c4f-4ae5-b022-ad1bb4f97e59
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d06551d2c72d972fa09cdfe100d094235cb426c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408681"
---
# <a name="models-and-packages"></a><span data-ttu-id="e81b2-104">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="e81b2-104">Models and packages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e81b2-105">このトピックでは、モデルとパッケージの概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-105">This topic describes the concept of models and packages.</span></span> <span data-ttu-id="e81b2-106">また、新しいモデルを作成するために Microsoft Visual Studio の開発ツールを使用する方法、既存のモデルのパラメーターを更新する方法、およびモデル間の依存関係を表示する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-106">It also explains how to use the development tools in Microsoft Visual Studio to create new models, how to update the parameters of existing models, and how to visualize dependencies between models.</span></span>

<span data-ttu-id="e81b2-107">モデル ストアのモデルを操作するには、Microsoft Visual Studio のツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-107">To work with models in the model store, you use tools in Microsoft Visual Studio.</span></span> <span data-ttu-id="e81b2-108">新しいモデルを作成、および既存のモデルのパラメータを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-108">You can create new models and change parameters for existing models.</span></span>

## <a name="conceptual-overview"></a><span data-ttu-id="e81b2-109">概念に関する概要</span><span class="sxs-lookup"><span data-stu-id="e81b2-109">Conceptual overview</span></span>
<span data-ttu-id="e81b2-110">モデルは、通常、配布可能なソフトウェア ソリューションを構成するメタデータとソース ファイルなどの要素のグループであり、既存のソリューションのカスタマイズを含みます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-110">A model is a group of elements, such as metadata and source files, that typically constitute a distributable software solution and includes customizations of an existing solution.</span></span> <span data-ttu-id="e81b2-111">モデルは、倉庫管理モデルやプロジェクト会計モデルなどのデザイン時概念です。</span><span class="sxs-lookup"><span data-stu-id="e81b2-111">A model is a design-time concept, for example a warehouse management model or a project accounting model.</span></span> <span data-ttu-id="e81b2-112">モデルは、常に 1 つのパッケージに属しています。</span><span class="sxs-lookup"><span data-stu-id="e81b2-112">A model always belongs to a package.</span></span> <span data-ttu-id="e81b2-113">パッケージは、1 つまたは複数のモデルの配置およびコンパイル単位です。</span><span class="sxs-lookup"><span data-stu-id="e81b2-113">A package is a deployment and compilation unit of one or more models.</span></span> <span data-ttu-id="e81b2-114">これには、モデル メタデータ、バイナリ、およびその他の関連するリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-114">It includes model metadata, binaries, and other associated resources.</span></span> <span data-ttu-id="e81b2-115">1 つ以上のパッケージは、ランタイム環境の配置に使用する車両の配置可能パッケージにパッケージすることができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-115">One or more packages can be packaged into a deployable package, which is the vehicle used for deployment on runtime environments.</span></span>

## <a name="creating-a-new-model"></a><span data-ttu-id="e81b2-116">新しいモデルを作成しています</span><span class="sxs-lookup"><span data-stu-id="e81b2-116">Creating a new model</span></span>
<span data-ttu-id="e81b2-117">**モデルの作成** ウィザードを使用して、新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-117">You use the **Create model** wizard to create new models.</span></span> <span data-ttu-id="e81b2-118">このウィザードには **Dynamics 365** メニューの **モデル管理** からアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-118">You can access this wizard from **Model Management** on the **Dynamics 365** menu.</span></span> <span data-ttu-id="e81b2-119">モデルは 2 種類作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-119">You can create two types of models:</span></span>

-   <span data-ttu-id="e81b2-120">**固有のパッケージに配置されているモデル** - このタイプのモデルを使用して、新しいモデル要素を作成し、参照モデルのメタデータとビジネス ロジックを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-120">**A model that is deployed in its own package** – You can use this type of model to create new model elements, and extend the metadata and business logic of referenced models.</span></span> <span data-ttu-id="e81b2-121">このウィザードでは、参照モデルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-121">The wizard lets you select the referenced models.</span></span> <span data-ttu-id="e81b2-122">このタイプのモデルは、独自のアセンブリとバイナリにコンパイルされるため、一般的なアップグレード、展開、アプリケーション ライフサイクル管理のコストが削減され、簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-122">This type of model is compiled into its own assembly and binaries, and will simplify and reduce the cost of upgrades, deployment, and application lifecycle management in general.</span></span>
-   <span data-ttu-id="e81b2-123">**既存のパッケージの一部であるモデル** - このタイプのモデルを使用して、ソース コードおよびメタデータのオーバーレイなどの高度なカスタマイズを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-123">**A model that is a part of an existing package** – You can use this type of model to perform advanced customizations, such as overlayering source code and metadata.</span></span>

<span data-ttu-id="e81b2-124">**モデルの作成** ウィザードで、レイヤーの **usr** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-124">In the **Create model** wizard, select **usr** for the layer.</span></span> <span data-ttu-id="e81b2-125">このレイヤーには、ユーザーのカスタマイズが保存されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-125">This layer will store user customizations.</span></span> <span data-ttu-id="e81b2-126">必要に応じて、**usp** レイヤーを使用してカスタマイズをパッチできます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-126">If needed, you can patch your customizations using the **usp** layer.</span></span> <span data-ttu-id="e81b2-127">異なるレイヤーに同じオブジェクトの複数のバージョンがある場合は、最上位のレイヤーが優先され、使用されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-127">If there are multiple versions of the same object in different layers, then the top layer will take precedence and will be used.</span></span>

<span data-ttu-id="e81b2-128">**モデルの作成** ウィザードが完了したとき、新しいプロジェクトの作成を選択した場合、名前とその場所を指定するための入力を要求されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-128">When the **Create model** wizard is completed, if you chose to create a new project, you will be prompted to specify a name and location for it.</span></span>

## <a name="updating-model-parameters"></a><span data-ttu-id="e81b2-129">モード パラメーターの更新</span><span class="sxs-lookup"><span data-stu-id="e81b2-129">Updating model parameters</span></span>
<span data-ttu-id="e81b2-130">モデルのパラメーターを変更する必要がある場合は、**更新モデル パラメーター** ダイアログ ボックスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-130">If you must change the parameters for a model, you can use the **Update model parameters** dialog box.</span></span>

1.  <span data-ttu-id="e81b2-131">**Dynamics 365** メニューで、**モデル管理** をポイントし、**モデルのパラメーターの更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-131">On the **Dynamics 365** menu, point to **Model Management**, and then click **Update model parameters**.</span></span>
2.  <span data-ttu-id="e81b2-132">**モデル名** フィールドで、パラメーターを更新するモデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-132">In the **Model name** field, select the model to update parameters for.</span></span>
3.  <span data-ttu-id="e81b2-133">必要に応じてパラメーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-133">Update the parameters as you require.</span></span>
4.  <span data-ttu-id="e81b2-134">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-134">Click **Next**.</span></span>
5.  <span data-ttu-id="e81b2-135">変更が必要な場合は、現在のモデルの依存関係情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-135">Update the dependency information for the current model, if changes are required.</span></span>
6.  <span data-ttu-id="e81b2-136">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-136">Click **Next**.</span></span> <span data-ttu-id="e81b2-137">モデルの要約情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-137">The summary information for the model is displayed.</span></span>
7.  <span data-ttu-id="e81b2-138">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-138">Click **Finish**.</span></span>

<span data-ttu-id="e81b2-139">更新されたモデル パラメーターは、Visual Studio を再起動した後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="e81b2-139">The updated model parameters become effective only after you restart Visual Studio.</span></span>

## <a name="viewing-package-dependencies"></a><span data-ttu-id="e81b2-140">パッケージの依存関係の表示</span><span class="sxs-lookup"><span data-stu-id="e81b2-140">Viewing package dependencies</span></span>
<span data-ttu-id="e81b2-141">どのパッケージとそのモデルに他のパッケージへの依存関係があるかを示す、グラフィック表現を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-141">You can create a graphical representation that shows which packages and their models have dependencies on other packages.</span></span> <span data-ttu-id="e81b2-142">**Dynamics 365** メニューで、**モデル管理** をポイントし、**パッケージの依存関係の表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-142">On the **Dynamics 365** menu, point to **Model Management**, and then click **View package dependencies**.</span></span> <span data-ttu-id="e81b2-143">現在のパッケージとそのモデルについて、有向グラフ マークアップ言語 (DGML) 図が生成されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-143">A Directed Graph Markup Language (DGML) diagram will be generated for the current packages and their models.</span></span> <span data-ttu-id="e81b2-144">この図は、それぞれがパッケージを表す相互依存ノードの集合です。</span><span class="sxs-lookup"><span data-stu-id="e81b2-144">This diagram is a collection of interdependent nodes, each of which represents a package.</span></span> <span data-ttu-id="e81b2-145">各ノードでは、パッケージに属するすべてのモデルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-145">Each node lists all the models that belong to that package.</span></span> <span data-ttu-id="e81b2-146">追加のツールは、強化または図を簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-146">Additional tools let you enhance or simplify the diagram.</span></span> <span data-ttu-id="e81b2-147">たとえば、コメントを追加したり、ノードをあちこちに移動したり、またはノードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-147">For example, you can add comments, move nodes around, or remove nodes.</span></span> <span data-ttu-id="e81b2-148">また、次の手順で、単一モデルのパッケージ依存関係を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-148">You can also view package dependencies of a single model by following these steps:</span></span>

1.  <span data-ttu-id="e81b2-149">アプリケーション エクスプローラーがモデル ビューになっていることを確認します。AOT ノードを右クリックし、**モデル ビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-149">Make sure the Application Explorer is in Model view: Right-click the AOT node and select **Model view**.</span></span>
2.  <span data-ttu-id="e81b2-150">任意のモデルを右クリックし、**パッケージの依存関係を表示** > **送信参照を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-150">Right-click on any model and select **View package dependencies** > **View outgoing references.**</span></span>

<span data-ttu-id="e81b2-151">選択したモデルが依存するすべてのパッケージのグラフが生成されます。</span><span class="sxs-lookup"><span data-stu-id="e81b2-151">This will generate a graph of all packages that the selected model depends on.</span></span> 

![ビューの相互関係](./media/viewdependencies2.png) 

![ディレクトリ依存関係](./media/directorydependencies.png)

## <a name="deleting-a-model"></a><span data-ttu-id="e81b2-154">モデルの削除</span><span class="sxs-lookup"><span data-stu-id="e81b2-154">Deleting a model</span></span>
<span data-ttu-id="e81b2-155">開発またはテスト環境では、次の手順に従ってモデルを削除します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-155">In a development or test environment, follow these steps to delete a model.</span></span>

<span data-ttu-id="e81b2-156">次の手順では、ローカル モデル ストア フォルダーが C:\AOSService\PackagesLocalDirectory であり、モデルの名前が MyModel1 であると想定しています。</span><span class="sxs-lookup"><span data-stu-id="e81b2-156">The following steps assume the local model store folder is C:\AOSService\PackagesLocalDirectory and your model is named MyModel1.</span></span>

<span data-ttu-id="e81b2-157">モデルが独自のパッケージに属している場合。</span><span class="sxs-lookup"><span data-stu-id="e81b2-157">If your model belongs to its own package.</span></span> <span data-ttu-id="e81b2-158">たとえば、パッケージに他のモデルが含まれていない拡張パッケージ。</span><span class="sxs-lookup"><span data-stu-id="e81b2-158">For example an extension package with no other models in the package.</span></span>

1. <span data-ttu-id="e81b2-159">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス。</span><span class="sxs-lookup"><span data-stu-id="e81b2-159">Stop the following services: AOS web service and Batch Management service.</span></span>
2. <span data-ttu-id="e81b2-160">パッケージ フォルダー C:\AOSService\PackagesLocalDirectory\MyModel1 を削除します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-160">Delete the package folder C:\AOSService\PackagesLocalDirectory\MyModel1.</span></span>
3. <span data-ttu-id="e81b2-161">手順 1 で停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-161">Restart the services that were stopped in step 1.</span></span>
4. <span data-ttu-id="e81b2-162">Visual Studio を実行している場合、モデルを更新します (**Visual Studio > Dynamics 365 > モデル管理 > モデルの更新**)</span><span class="sxs-lookup"><span data-stu-id="e81b2-162">If Visual Studio is running, refresh your models (**Visual Studio > Dynamics 365 > Model management > Refresh models**)</span></span>
5. <span data-ttu-id="e81b2-163">Visual Studio で、完全なデータベース同期を実行します (**Visual Studio > Dynamics 365 > データベースの同期**)。</span><span class="sxs-lookup"><span data-stu-id="e81b2-163">In Visual Studio, perform a full database synchronization (**Visual Studio > Dynamics 365 > Synchronize database**).</span></span>

<span data-ttu-id="e81b2-164">モデルが複数のモデルを含むパッケージに属している場合。</span><span class="sxs-lookup"><span data-stu-id="e81b2-164">If your model belongs to a package with multiple models.</span></span> <span data-ttu-id="e81b2-165">たとえば、MyModel1 は、アプリケーションスイートをオーバーレイします。</span><span class="sxs-lookup"><span data-stu-id="e81b2-165">For example, the MyModel1 overlays Application Suite.</span></span>

1. <span data-ttu-id="e81b2-166">次のサービスを停止: AOS Web サービスおよびバッチ管理サービス。</span><span class="sxs-lookup"><span data-stu-id="e81b2-166">Stop the following services: AOS web service and  Batch Management service.</span></span>
2. <span data-ttu-id="e81b2-167">モデル フォルダー C:\AOSService\PackagesLocalDirectory\<PackageName>\MyModel1 を削除します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-167">Delete the model folder C:\AOSService\PackagesLocalDirectory\<PackageName>\MyModel1.</span></span> <span data-ttu-id="e81b2-168">この例の場合。</span><span class="sxs-lookup"><span data-stu-id="e81b2-168">In this example.</span></span> <span data-ttu-id="e81b2-169">PackageName=ApplicationSuite。</span><span class="sxs-lookup"><span data-stu-id="e81b2-169">PackageName=ApplicationSuite.</span></span>
3. <span data-ttu-id="e81b2-170">手順 1 で停止したサービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="e81b2-170">Restart the services that were stopped in step 1.</span></span>
4. <span data-ttu-id="e81b2-171">Visual Studio で、モデルを更新します (**Visual Studio > Dynamics 365 > モデル管理 > モデルの更新**)。</span><span class="sxs-lookup"><span data-stu-id="e81b2-171">In Visual Studio, refresh your models (**Visual Studio > Dynamics 365 > Model management > Refresh models**).</span></span>
5. <span data-ttu-id="e81b2-172">Visual Studio で、削除したモデルが属しているパッケージをビルドします (**Visual Studio > Dynamics 365 > モデルをビルド**)。</span><span class="sxs-lookup"><span data-stu-id="e81b2-172">In Visual Studio, build the package that the deleted models belonged to (**Visual Studio > Dynamics 365 > Build models**).</span></span>
6. <span data-ttu-id="e81b2-173">Visual Studio で、完全なデータベース同期を実行します (**Visual Studio > Dynamics 365 > データベースの同期**)。</span><span class="sxs-lookup"><span data-stu-id="e81b2-173">In Visual Studio, perform a full database synchronization (**Visual Studio > Dynamics 365 > Synchronize database**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e81b2-174">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e81b2-174">Additional resources</span></span>

[<span data-ttu-id="e81b2-175">Visual Studioの開発ツール</span><span class="sxs-lookup"><span data-stu-id="e81b2-175">Development tools in Visual Studio</span></span>](development-tools-overview.md)

[<span data-ttu-id="e81b2-176">開発およびカスタマイズのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="e81b2-176">Develop and customize home page</span></span>](developer-home-page.md)

[<span data-ttu-id="e81b2-177">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="e81b2-177">Export and import models</span></span>](models-export-import.md)
