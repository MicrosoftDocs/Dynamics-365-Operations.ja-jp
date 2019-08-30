---
title: モデルの作成、およびデータモデル要素の作成についての概要
description: このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、フリート管理チュートリアルという名前の新しいモデルを作成します。 また、新しいモデルの要素を作成および編集します。
author: RobinARH
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 23421
ms.assetid: 1b7789f4-12c1-480b-bb39-c354b5b03276
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31bc2e2b553e565da168b9f6dc6d05d86ca9ad52
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864251"
---
# <a name="create-models-and-data-model-elements-overview"></a><span data-ttu-id="e593a-104">モデルの作成、およびデータモデル要素の作成についての概要</span><span class="sxs-lookup"><span data-stu-id="e593a-104">Create models and data model elements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e593a-105">このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、Microsoft Dynamics 365 for Finance and Operations でフリート管理チュートリアルという名前の新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e593a-105">In this tutorial, you'll use Visual Studio's Dynamics 365 menu to create a new model named Fleet Management tutorial in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e593a-106">また、新しいモデルの要素を作成および編集します。</span><span class="sxs-lookup"><span data-stu-id="e593a-106">You'll also create and edit new model elements.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e593a-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="e593a-107">Prerequisites</span></span>

<span data-ttu-id="e593a-108">このチュートリアルでは、Finance and Operations 環境にアクセスし、管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e593a-108">This tutorial requires that you have access to a Finance and Operations environment, and that you be provisioned as an administrator</span></span>

## <a name="keywords"></a><span data-ttu-id="e593a-109">キーワード</span><span class="sxs-lookup"><span data-stu-id="e593a-109">Keywords</span></span>
- <span data-ttu-id="e593a-110">**モデル** - 他の 2 つのモデルを参照するモデルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e593a-110">**Model** - You configure your model to refer to two other models.</span></span> <span data-ttu-id="e593a-111">これにより、モデルは他のパッケージにあるメタデータとコード要素を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e593a-111">This enables your model to reference metadata and code elements that are in other packages.</span></span>
- <span data-ttu-id="e593a-112">**プロジェクト** -**Unified Operations** プロジェクトを作成し、プロジェクトを新しいモデルに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="e593a-112">**Project** - You create a **Unified Operations** project, and you associate your project to your new model.</span></span> <span data-ttu-id="e593a-113">要素をプロジェクトに追加します。これはモデルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="e593a-113">You add elements to your project, which are also added to your model.</span></span> <span data-ttu-id="e593a-114">具体的には、拡張データ型 (EDT) を追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-114">Specifically, you add an extended data type (EDT).</span></span> <span data-ttu-id="e593a-115">また、フィールドおよびメソッドで入力するテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-115">You also add a table that you populate with fields and a method.</span></span>
- <span data-ttu-id="e593a-116">**デザイナー** - プロジェクトに品目を追加するたびに、選択した品目タイプに合わせたデザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e593a-116">**Designer** - Each time you add an item to your project, a designer is displayed that is tailored to the item type you selected.</span></span> <span data-ttu-id="e593a-117">**プロパティ** ウィンドウは、デザイナーの異なるノードが強調表示されるたびに調整されます。</span><span class="sxs-lookup"><span data-stu-id="e593a-117">The **Properties** window adjusts each time a different node of the designer is highlighted.</span></span> <span data-ttu-id="e593a-118">デザイナーおよび **プロパティ** ウィンドウで更新を行います。</span><span class="sxs-lookup"><span data-stu-id="e593a-118">You make updates in the designers and in the **Properties** window.</span></span>
- <span data-ttu-id="e593a-119">**EDT** - 拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="e593a-119">**EDT** - Extended data type.</span></span>

## <a name="create-the-fleet-management-tutorial-model"></a><span data-ttu-id="e593a-120">フリート管理チュートリアル モデルを作成する</span><span class="sxs-lookup"><span data-stu-id="e593a-120">Create the Fleet Management tutorial model</span></span>
1.  <span data-ttu-id="e593a-121">**管理者として実行** を使用して Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="e593a-121">Start Visual Studio using **Run as administrator**.</span></span>
2.  <span data-ttu-id="e593a-122">**Dynamics 365** ウィンドウから、**モデル管理 &gt; モデルの作成**を選択して、**モデルの作成**ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="e593a-122">From the **Dynamics 365** window, select **Model Management &gt; Create model** to open the **Create model** wizard.</span></span>
3.  <span data-ttu-id="e593a-123">モデル パラメーターの以下の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e593a-123">Enter the following values for model parameters.</span></span>

    | <span data-ttu-id="e593a-124">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="e593a-124">**Property**</span></span>           | <span data-ttu-id="e593a-125">**値**</span><span class="sxs-lookup"><span data-stu-id="e593a-125">**Value**</span></span>                                                                                                                |
    |------------------------|--------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e593a-126">**モデル名**</span><span class="sxs-lookup"><span data-stu-id="e593a-126">**Model name**</span></span>         | <span data-ttu-id="e593a-127">FleetMgmntTutorial</span><span class="sxs-lookup"><span data-stu-id="e593a-127">FleetMgmntTutorial</span></span>                                                                                                       |
    | <span data-ttu-id="e593a-128">**モデル発行元**</span><span class="sxs-lookup"><span data-stu-id="e593a-128">**Model publisher**</span></span>    | <span data-ttu-id="e593a-129">Microsoft Corp</span><span class="sxs-lookup"><span data-stu-id="e593a-129">Microsoft Corp</span></span>                                                                                                           |
    | <span data-ttu-id="e593a-130">**レイヤー**</span><span class="sxs-lookup"><span data-stu-id="e593a-130">**Layer**</span></span>              | <span data-ttu-id="e593a-131">isv</span><span class="sxs-lookup"><span data-stu-id="e593a-131">isv</span></span>                                                                                                                      |
    | <span data-ttu-id="e593a-132">**モデルの説明**</span><span class="sxs-lookup"><span data-stu-id="e593a-132">**Model description**</span></span>  | <span data-ttu-id="e593a-133">このチュートリアルでは、Microsoft Dynamics AX の開発ツールを使用して、フリート管理 アプリケーションを構築する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e593a-133">This tutorial shows how to build the Fleet Management application by using the Microsoft Dynamics AX  development tools.</span></span> |
    | <span data-ttu-id="e593a-134">**モデルの表示名**</span><span class="sxs-lookup"><span data-stu-id="e593a-134">**Model display name**</span></span> | <span data-ttu-id="e593a-135">フリート管理のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="e593a-135">Fleet Management Tutorial</span></span>                                                                                                |

    > [!NOTE]
    > <span data-ttu-id="e593a-136">モデルの名前は **FleetMgmntTutorial** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e593a-136">Your model name must be **FleetMgmntTutorial**.</span></span> <span data-ttu-id="e593a-137">他の名前は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="e593a-137">Don't use any other name.</span></span> <span data-ttu-id="e593a-138">その他のチュートリアルでは、プロジェクトをインポートすることでこのモデル内のモデル要素を上書きします。</span><span class="sxs-lookup"><span data-stu-id="e593a-138">In other tutorials, you'll overwrite model elements in this model by importing a project.</span></span> <span data-ttu-id="e593a-139">このチュートリアルで作成したモデルに **FleetMgmntTutorial** という名前が付けられていない場合、その他のチュートリアルでプロジェクトが正しくインポートできない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e593a-139">If the model you create in this tutorial isn't named **FleetMgmntTutorial**, you may not be able to correctly import the project in other tutorials.</span></span>
 
4.  <span data-ttu-id="e593a-140">**次へ**をクリックして次のページに移動し、次に**新しいパッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-140">Click **Next** to advance to the next page, and then select **Create New Package**.</span></span> <span data-ttu-id="e593a-141">作成しているモデルは独自のパッケージを持ち、独自の .NET アセンブリを構築します。</span><span class="sxs-lookup"><span data-stu-id="e593a-141">The model you're creating will have its own package and build its own .NET assembly.</span></span> 

    <span data-ttu-id="e593a-142">[![Package\_DataModel](./media/package_datamodel.png)](./media/package_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-142">[![Package\_DataModel](./media/package_datamodel.png)](./media/package_datamodel.png)</span></span>

5.  <span data-ttu-id="e593a-143">**次へ**をクリックし、**参照モデルを選択**ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="e593a-143">Click **Next** to advance to the **Select referenced models** step.</span></span>
6.  <span data-ttu-id="e593a-144">参照されるモデルとして **アプリケーション プラットフォーム** および **アプリケーション基盤** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-144">Select **Application Platform** and **Application Foundation** as referenced models.</span></span>

    <span data-ttu-id="e593a-145">[![ReferenceModels\_DataModel](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-145">[![ReferenceModels\_DataModel](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="e593a-146">正しい参照モデルを選択していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e593a-146">Verify that you've selected the correct referenced models.</span></span>
    
7.  <span data-ttu-id="e593a-147">**次へ**をクリックし、**概要**ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="e593a-147">Click **Next** to advance to the **Summary** step.</span></span>
8.  <span data-ttu-id="e593a-148">概要ページの情報を確認してから、**新規プロジェクトの作成** および **これを新規プロジェクトの自分の既定のモデルにする** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-148">Verify the information on the summary page, and then select the **Create new project** and **Make this my default model for new projects** check boxes.</span></span> 

    <span data-ttu-id="e593a-149">[![Summary\_DataModel](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-149">[![Summary\_DataModel](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span></span>

9.  <span data-ttu-id="e593a-150">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-150">Click **Finish**.</span></span> <span data-ttu-id="e593a-151">**新しいプロジェクト** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="e593a-151">The **New Project** dialog box opens.</span></span>
10. <span data-ttu-id="e593a-152">**テンプレート**で、**Dynamics 365** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-152">Under **Templates**, select **Dynamics 365**.</span></span>
11. <span data-ttu-id="e593a-153">**Unified Operations** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-153">Select the **Unified Operations** template.</span></span>
12. <span data-ttu-id="e593a-154">ダイアログ ボックスのフィールドに次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e593a-154">Enter the following values in the fields in the dialog box.</span></span>

    | <span data-ttu-id="e593a-155">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="e593a-155">**Property**</span></span> | <span data-ttu-id="e593a-156">**値**</span><span class="sxs-lookup"><span data-stu-id="e593a-156">**Value**</span></span>       |
    |--------------|-----------------|
    | <span data-ttu-id="e593a-157">**名前**</span><span class="sxs-lookup"><span data-stu-id="e593a-157">**Name**</span></span>     | <span data-ttu-id="e593a-158">FMTDataModel</span><span class="sxs-lookup"><span data-stu-id="e593a-158">FMTDataModel</span></span>    |
    | <span data-ttu-id="e593a-159">**保管場所**</span><span class="sxs-lookup"><span data-stu-id="e593a-159">**Location**</span></span> | <span data-ttu-id="e593a-160">C:\\FMLab</span><span class="sxs-lookup"><span data-stu-id="e593a-160">C:\\FMLab</span></span>       |
    | <span data-ttu-id="e593a-161">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="e593a-161">**Solution**</span></span> | <span data-ttu-id="e593a-162">ソリューションへの追加</span><span class="sxs-lookup"><span data-stu-id="e593a-162">Add to solution</span></span> |

    <span data-ttu-id="e593a-163">[![NewProject\_DataModel](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-163">[![NewProject\_DataModel](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span></span>

13. <span data-ttu-id="e593a-164">プロジェクトを作成するには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-164">Click **OK** to create the project.</span></span>

## <a name="create-the-fmtaddress-extended-data-type"></a><span data-ttu-id="e593a-165">FMTAddress の拡張データ型を作成します。</span><span class="sxs-lookup"><span data-stu-id="e593a-165">Create the FMTAddress extended data type</span></span>
1.  <span data-ttu-id="e593a-166">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-166">In **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="e593a-167">**Dynamics 365 品目**で、**データ型**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-167">Under **Dynamics 365 Items**, select **Data Types**.</span></span>
3.  <span data-ttu-id="e593a-168">**EDT 文字列**をクリックし、を新しい項目の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-168">Click **EDT String** to select the new item type.</span></span>
4.  <span data-ttu-id="e593a-169">**名前**フィールドに、**FMTAddress** と入力してから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-169">In the **Name** field, enter **FMTAddress**, and then click **Add**.</span></span> 

    <span data-ttu-id="e593a-170">[![NewItem\_DataModel](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-170">[![NewItem\_DataModel](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span></span> 

    <span data-ttu-id="e593a-171">これにより、新しい EDT モデル要素をプロジェクトに追加され、次の図に示すように、新しい要素の EDT デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e593a-171">This adds a new EDT model element to the project, and opens the EDT designer for the new element, as shown in the following illustration.</span></span> 

    <span data-ttu-id="e593a-172">[![EDTelement\_DataModel](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-172">[![EDTelement\_DataModel](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span></span>

5.  <span data-ttu-id="e593a-173">デザイナーで **FMTAddress** ルート ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-173">Select the root node of **FMTAddress** in the designer.</span></span>
6.  <span data-ttu-id="e593a-174">**プロパティ** ウィンドウの**外観セクション**で、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e593a-174">In the **Properties** window, in the **Appearance section**, set the following properties.</span></span>

    | <span data-ttu-id="e593a-175">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="e593a-175">**Property**</span></span>    | <span data-ttu-id="e593a-176">**値**</span><span class="sxs-lookup"><span data-stu-id="e593a-176">**Value**</span></span>          |
    |-----------------|--------------------|
    | <span data-ttu-id="e593a-177">**ヘルプ テキスト**</span><span class="sxs-lookup"><span data-stu-id="e593a-177">**Help Text**</span></span>   | <span data-ttu-id="e593a-178">オンライン ヘルプをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="e593a-178">Check online help.</span></span> |
    | <span data-ttu-id="e593a-179">**ラベル**</span><span class="sxs-lookup"><span data-stu-id="e593a-179">**Label**</span></span>       | <span data-ttu-id="e593a-180">アドレス</span><span class="sxs-lookup"><span data-stu-id="e593a-180">Address</span></span>            |
    | <span data-ttu-id="e593a-181">**文字列サイズ**</span><span class="sxs-lookup"><span data-stu-id="e593a-181">**String Size**</span></span> | <span data-ttu-id="e593a-182">75</span><span class="sxs-lookup"><span data-stu-id="e593a-182">75</span></span>                 |

    <span data-ttu-id="e593a-183">[![EDTProperty\_DataModel](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-183">[![EDTProperty\_DataModel](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span></span>

7.  <span data-ttu-id="e593a-184">**Ctrl+S** キーを押して EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="e593a-184">Press **Ctrl+S** to save the EDT.</span></span>

## <a name="add-existing-model"></a><span data-ttu-id="e593a-185">既存のモデルの追加</span><span class="sxs-lookup"><span data-stu-id="e593a-185">Add existing model</span></span>
<span data-ttu-id="e593a-186">現在のモデルとプロジェクトに他の必要なモデル要素ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-186">Add the other required model element files to the current model and project.</span></span> <span data-ttu-id="e593a-187">**既存の品目を追加** フィーチャーを使用することにより、これを素早く実行することができます。</span><span class="sxs-lookup"><span data-stu-id="e593a-187">You can do this quickly by using the **Add existing item** feature.</span></span>

1.  <span data-ttu-id="e593a-188">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**既存の項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-188">In the **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="e593a-189">C:\\FMLab\\EDT\\ を参照します。</span><span class="sxs-lookup"><span data-stu-id="e593a-189">Browse to C:\\FMLab\\EDT\\.</span></span> 

    <span data-ttu-id="e593a-190">[![ExistingItem\_DataModel](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-190">[![ExistingItem\_DataModel](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span></span>

3.  <span data-ttu-id="e593a-191">**Ctrl+A** を押してすべてのファイルを選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-191">Press **Ctrl+A** to select all of the files, and then click **Add**.</span></span>

## <a name="create-the-fmtcustomer-table"></a><span data-ttu-id="e593a-192">FMTCustomer テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e593a-192">Create the FMTCustomer table</span></span>
1. <span data-ttu-id="e593a-193">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**追加 &gt; 新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-193">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Add &gt; New Item**.</span></span>
2. <span data-ttu-id="e593a-194">左ウィンドウで、**インストール済み**を展開し、**Dynamics 365 品目**を展開してから、**データ モデル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-194">In the left pane, expand **Installed**, expand **Dynamics 365 Items** and then click **Data Model**.</span></span>
3. <span data-ttu-id="e593a-195">アーティファクトの一覧で**テーブル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-195">In the list of artifacts, select **Table**.</span></span>
4. <span data-ttu-id="e593a-196">**名前**フィールドに、**FMTCustomer** と入力してから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-196">In the **Name** field, enter **FMTCustomer**, and then click **Add**.</span></span> <span data-ttu-id="e593a-197">テーブル デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="e593a-197">The table designer opens.</span></span> 

   <span data-ttu-id="e593a-198">[![Add\_DataModel](./media/add_datamodel.png)](./media/add_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-198">[![Add\_DataModel](./media/add_datamodel.png)](./media/add_datamodel.png)</span></span>

### <a name="add-fields-to-the-fmtcustomer-table"></a><span data-ttu-id="e593a-199">FMTCustomer テーブルへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="e593a-199">Add fields to the FMTCustomer table</span></span>

<span data-ttu-id="e593a-200">FMTCustomer のテーブル デザイナーで、テーブルに複数のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-200">In the table designer for FMTCustomer, you now add several fields to the table.</span></span> 

<span data-ttu-id="e593a-201">[![AddFields\_DataModel](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-201">[![AddFields\_DataModel](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span></span>

1.  <span data-ttu-id="e593a-202">各フィールドを追加するには、**フィールド** を右クリックし、**新規** をクリックして、タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-202">To add each field, right-click **Fields**, click **New**, and then select a type.</span></span> <span data-ttu-id="e593a-203">各フィールドを追加すると、次の表に示すように、**プロパティ** ウィンドウでフィールド名とその他の特定の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e593a-203">As you add each field, you must specify the field name and certain other values in the **Properties** window, as described in the following table.</span></span>

    | <span data-ttu-id="e593a-204">**タイプ**</span><span class="sxs-lookup"><span data-stu-id="e593a-204">**Type**</span></span>   | <span data-ttu-id="e593a-205">**フィールド名**</span><span class="sxs-lookup"><span data-stu-id="e593a-205">**Field name**</span></span> | <span data-ttu-id="e593a-206">**プロパティ値**</span><span class="sxs-lookup"><span data-stu-id="e593a-206">**Property values**</span></span>                                                         |
    |------------|----------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="e593a-207">**日付**</span><span class="sxs-lookup"><span data-stu-id="e593a-207">**Date**</span></span>   | <span data-ttu-id="e593a-208">CCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="e593a-208">CCExpiryDate</span></span>   | <span data-ttu-id="e593a-209">拡張データ型 = FMTCCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="e593a-209">Extended Data Type = FMTCCExpiryDate</span></span>                                        |
    | <span data-ttu-id="e593a-210">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-210">**String**</span></span> | <span data-ttu-id="e593a-211">アドレス</span><span class="sxs-lookup"><span data-stu-id="e593a-211">Address</span></span>        | <span data-ttu-id="e593a-212">拡張データ型 = FMTAddressHelp テキスト = アドレス フィールドのヘルプ テキスト。</span><span class="sxs-lookup"><span data-stu-id="e593a-212">Extended Data Type = FMTAddressHelp Text = Help text for the address field.</span></span> |
    | <span data-ttu-id="e593a-213">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-213">**String**</span></span> | <span data-ttu-id="e593a-214">CellPhone</span><span class="sxs-lookup"><span data-stu-id="e593a-214">CellPhone</span></span>      | <span data-ttu-id="e593a-215">拡張データ型 = 電話</span><span class="sxs-lookup"><span data-stu-id="e593a-215">Extended Data Type = Phone</span></span>                                                  |
    | <span data-ttu-id="e593a-216">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-216">**String**</span></span> | <span data-ttu-id="e593a-217">CreditCardNum</span><span class="sxs-lookup"><span data-stu-id="e593a-217">CreditCardNum</span></span>  | <span data-ttu-id="e593a-218">拡張データ型 = FMTCreditCardNum</span><span class="sxs-lookup"><span data-stu-id="e593a-218">Extended Data Type = FMTCreditCardNum</span></span>                                       |
    | <span data-ttu-id="e593a-219">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-219">**String**</span></span> | <span data-ttu-id="e593a-220">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="e593a-220">DriversLicense</span></span> | <span data-ttu-id="e593a-221">拡張データ型 = FMTDriversLicense</span><span class="sxs-lookup"><span data-stu-id="e593a-221">Extended Data Type = FMTDriversLicense</span></span>                                      |
    | <span data-ttu-id="e593a-222">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-222">**String**</span></span> | <span data-ttu-id="e593a-223">電子メール</span><span class="sxs-lookup"><span data-stu-id="e593a-223">Email</span></span>          | <span data-ttu-id="e593a-224">文字列サイズ = 80Label = 電子メール</span><span class="sxs-lookup"><span data-stu-id="e593a-224">String Size = 80Label = Email</span></span>                                               |
    | <span data-ttu-id="e593a-225">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-225">**String**</span></span> | <span data-ttu-id="e593a-226">名</span><span class="sxs-lookup"><span data-stu-id="e593a-226">FirstName</span></span>      | <span data-ttu-id="e593a-227">拡張データ型 = FirstName</span><span class="sxs-lookup"><span data-stu-id="e593a-227">Extended Data Type = FirstName</span></span>                                              |
    | <span data-ttu-id="e593a-228">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-228">**String**</span></span> | <span data-ttu-id="e593a-229">姓</span><span class="sxs-lookup"><span data-stu-id="e593a-229">LastName</span></span>       | <span data-ttu-id="e593a-230">拡張データ型 = LastName</span><span class="sxs-lookup"><span data-stu-id="e593a-230">Extended Data Type = LastName</span></span>                                               |
    | <span data-ttu-id="e593a-231">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-231">**String**</span></span> | <span data-ttu-id="e593a-232">ライセンス</span><span class="sxs-lookup"><span data-stu-id="e593a-232">License</span></span>        | <span data-ttu-id="e593a-233">文字列サイズ = 100Label = ライセンス</span><span class="sxs-lookup"><span data-stu-id="e593a-233">String Size = 100Label = License</span></span>                                            |
    | <span data-ttu-id="e593a-234">**文字列**</span><span class="sxs-lookup"><span data-stu-id="e593a-234">**String**</span></span> | <span data-ttu-id="e593a-235">縮小版</span><span class="sxs-lookup"><span data-stu-id="e593a-235">Thumbnail</span></span>      | <span data-ttu-id="e593a-236">文字列サイズ = 100Label = サムネイル</span><span class="sxs-lookup"><span data-stu-id="e593a-236">String Size = 100Label = Thumbnail</span></span>                                          |


    > [!TIP]
    > <span data-ttu-id="e593a-237">EDT を参照するテーブル内のすべての新しいフィールドでは、**ソリューション エクスプローラー**または**アプリケーション エクスプローラー**から EDT エレメントをドラッグし、デザイナーの **FMTCustomer** テーブルの**フィールド**ノードをドロップするだけで、フィールドを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e593a-237">For all new fields in the table that reference an EDT, you can create the field by simply dragging the EDT element from **Solution Explorer** or **Application Explorer** and dropping it on the **Fields** node of the **FMTCustomer** table in the designer.</span></span> 

    <span data-ttu-id="e593a-238">[![AdministratorArrow\_DataModel](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-238">[![AdministratorArrow\_DataModel](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span></span>

2.  <span data-ttu-id="e593a-239">**Ctrl+S** キーを押して、テーブルに新しいフィールドを保存します。</span><span class="sxs-lookup"><span data-stu-id="e593a-239">Press **Ctrl+S** to save the new fields on the table.</span></span>

### <a name="add-fields-to-field-groups"></a><span data-ttu-id="e593a-240">フィールド グループへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="e593a-240">Add fields to field groups</span></span>

1.  <span data-ttu-id="e593a-241">次の一覧のフィールドを選択して、一部の不フィールドを **AutoSummary** フィールド グループに追加する準備をします。</span><span class="sxs-lookup"><span data-stu-id="e593a-241">Prepare to add some of the fields to the **AutoSummary** field group by selecting the fields in the following list.</span></span> <span data-ttu-id="e593a-242">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-242">To select multiple fields, hold down the Ctrl key while you click each field:</span></span>
    -   <span data-ttu-id="e593a-243">**住所**</span><span class="sxs-lookup"><span data-stu-id="e593a-243">**Address**</span></span>
    -   <span data-ttu-id="e593a-244">**CCExpiryDate**</span><span class="sxs-lookup"><span data-stu-id="e593a-244">**CCExpiryDate**</span></span>
    -   <span data-ttu-id="e593a-245">**CellPhone**</span><span class="sxs-lookup"><span data-stu-id="e593a-245">**CellPhone**</span></span>
    -   <span data-ttu-id="e593a-246">**CreditCardNum**</span><span class="sxs-lookup"><span data-stu-id="e593a-246">**CreditCardNum**</span></span>
    -   <span data-ttu-id="e593a-247">**DriversLicense**</span><span class="sxs-lookup"><span data-stu-id="e593a-247">**DriversLicense**</span></span>
    -   <span data-ttu-id="e593a-248">**電子メール**</span><span class="sxs-lookup"><span data-stu-id="e593a-248">**Email**</span></span>
    -   <span data-ttu-id="e593a-249">**名**</span><span class="sxs-lookup"><span data-stu-id="e593a-249">**FirstName**</span></span>
    -   <span data-ttu-id="e593a-250">**姓**</span><span class="sxs-lookup"><span data-stu-id="e593a-250">**LastName**</span></span>

2.  <span data-ttu-id="e593a-251">**フィールド グループ**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="e593a-251">Expand the **Field Groups** node.</span></span>
3.  <span data-ttu-id="e593a-252">選択したフィールドを **AutoSummary** ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="e593a-252">Drag the selected fields to the **AutoSummary** node</span></span>
4.  <span data-ttu-id="e593a-253">同じ方法を使用して、**氏名**、**姓**、および**携帯**フィールドを**自動レポート**フィールド グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-253">Use the same technique to add the fields **FirstName**, **LastName**, and **CellPhone** to the **AutoReport** field group.</span></span>
5.  <span data-ttu-id="e593a-254">テーブルを保存します。</span><span class="sxs-lookup"><span data-stu-id="e593a-254">Save the table.</span></span>

### <a name="add-a-method"></a><span data-ttu-id="e593a-255">メソッドの追加</span><span class="sxs-lookup"><span data-stu-id="e593a-255">Add a method</span></span>

1.  <span data-ttu-id="e593a-256">**Methods** ノードを右クリックし、**New Method** をクリックして、**FMTCustomer** テーブルに **fullName** という名前の X++ メソッドを 追加します。</span><span class="sxs-lookup"><span data-stu-id="e593a-256">Add the X++ method named **fullName** to the **FMTCustomer** table by right-clicking the **Methods** node, and then clicking **New Method**.</span></span>
2.  <span data-ttu-id="e593a-257">コード エディターで、既定のメソッドのコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="e593a-257">In the code editor, replace the default method code with the following code.</span></span> 
 
    > [!TIP]
    > <span data-ttu-id="e593a-258">「this.」を入力するとき、IntelliSense リストからフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-258">When you type “this.”, choose the field from the IntelliSense list.</span></span>

```
        public display FMTName fullName()
        {
            return this.FirstName + ' ' + this.LastName;
        }
```

3.  <span data-ttu-id="e593a-259">コードを保存します。</span><span class="sxs-lookup"><span data-stu-id="e593a-259">Save the code.</span></span>

## <a name="update-the-fmtaddress-edt"></a><span data-ttu-id="e593a-260">FMTAddress EDT の更新</span><span class="sxs-lookup"><span data-stu-id="e593a-260">Update the FMTAddress EDT</span></span>
1.  <span data-ttu-id="e593a-261">**ソリューション エクスプローラー**で **FMTDataModel** プロジェクトを展開します。</span><span class="sxs-lookup"><span data-stu-id="e593a-261">In **Solution Explorer**, expand the **FMTDataModel** project.</span></span>
2.  <span data-ttu-id="e593a-262">**FMTAddress** を右クリックしてから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-262">Right-click **FMTAddress**, and then click **Open**.</span></span> <span data-ttu-id="e593a-263">**EDT デザイナー**が開きます。</span><span class="sxs-lookup"><span data-stu-id="e593a-263">The **EDT designer** opens.</span></span>
3.  <span data-ttu-id="e593a-264">**EDT デザイナー**で、**FMTAddress** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-264">In the **EDT designer**, select **FMTAddress**.</span></span>
4.  <span data-ttu-id="e593a-265">**プロパティ** ウィンドウの**参照テーブル** フィールドで、**FMTCustomer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-265">In the **Properties** window, in the **Reference Table** field, select **FMTCustomer**.</span></span> <span data-ttu-id="e593a-266">**ヒント:** ドロップダウン リストをクリックし、検索ボックスに、接頭語「FMT」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e593a-266">**Tip:** Click the drop-down list, and then type the prefix "FMT" in the search box.</span></span> <span data-ttu-id="e593a-267">これにより、名前に「FMT」が含まれている表のみが表示されるように、ドロップダウン リストがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="e593a-267">This filters the drop-down list to only show tables that contain "FMT" in their name.</span></span> <span data-ttu-id="e593a-268">フィルター処理されたエントリの一覧から **FMTCustomer** テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-268">Select the **FMTCustomer** table from the list of filtered entries.</span></span> <span data-ttu-id="e593a-269">[![SearchFMT\_DataModel](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="e593a-269">[![SearchFMT\_DataModel](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span></span>
5.  <span data-ttu-id="e593a-270">EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="e593a-270">Save the EDT.</span></span>

## <a name="build-the-fmtdatamodel-project-and-the-fleet-management-tutorial-model"></a><span data-ttu-id="e593a-271">FMTDataModel プロジェクトと フリート管理チュートリアル モデルの構築</span><span class="sxs-lookup"><span data-stu-id="e593a-271">Build the FMTDataModel project and the Fleet Management tutorial model</span></span>
1. <span data-ttu-id="e593a-272">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**リビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-272">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Rebuild**.</span></span>
2. <span data-ttu-id="e593a-273">モデル全体の完全なビルドを行うには、**Dynamics 365** メニューで、**モデルをビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-273">To do a full build of the entire model, on the **Dynamics 365** menu, click **Build models**.</span></span>
3. <span data-ttu-id="e593a-274">**フリート管理チュートリアル**以外のすべてのモデルのチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="e593a-274">Clear the check box for all models except for **Fleet Management Tutorial**.</span></span>
4. <span data-ttu-id="e593a-275">**オプション**タブで、**推奨チェックの実行**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e593a-275">On the **Options** tab, select the **Run Best practice checks** check box.</span></span> <span data-ttu-id="e593a-276">使用可能なその他のオプションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e593a-276">Note that other options available.</span></span>
5. <span data-ttu-id="e593a-277">**モデル**タブで、**ビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-277">On the **Models** tab, click **Build**.</span></span>
6. <span data-ttu-id="e593a-278">ダイアログ ボックスで **閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e593a-278">Click **Close**  in the dialog box.</span></span>
7. <span data-ttu-id="e593a-279">**ウィンドウ**メニューで、**すべてのドキュメントを閉じる**をクリックして、開いているすべてのドキュメントを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e593a-279">On the **Window** menu, click **Close All Documents**, to close all open documents.</span></span>




