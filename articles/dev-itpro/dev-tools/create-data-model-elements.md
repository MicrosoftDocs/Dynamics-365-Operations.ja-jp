---
title: "モデルとデータ モデル要素の作成"
description: "このチュートリアルでは、Visual Studio の Dynamics AX メニューを使用してフリート管理チュートリアルという名前の新しいモデルを作成します。 また、新しいモデルの要素を作成および編集します。"
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
ms.custom: 23421
ms.assetid: 1b7789f4-12c1-480b-bb39-c354b5b03276
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 094276b95403cb25bd54d59f19b5df81d68be056
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-model-and-data-model-elements"></a><span data-ttu-id="5ea10-104">モデルとデータ モデル要素の作成</span><span class="sxs-lookup"><span data-stu-id="5ea10-104">Create a model and data model elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ea10-105">このチュートリアルでは、Visual Studio の Dynamics AX メニューを使用してフリート管理チュートリアルという名前の新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-105">In this tutorial, you'll use Visual Studio's Dynamics AX menu to create a new model named Fleet Management tutorial.</span></span> <span data-ttu-id="5ea10-106">また、新しいモデルの要素を作成および編集します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-106">You'll also create and edit new model elements.</span></span>

<a name="prerequisites"></a><span data-ttu-id="5ea10-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="5ea10-107">Prerequisites</span></span>
-------------

<span data-ttu-id="5ea10-108">このチュートリアルでは、リモート デスクトップを使用して Dynamics AX 環境にアクセスし、Dynamics AX インスタンスの管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ea10-108">This tutorial requires you to access the Dynamics AX environment using Remote Desktop, and that you be provisioned as an administrator on the Dynamics AX instance.</span></span>

## <a name="keywords"></a><span data-ttu-id="5ea10-109">キーワード</span><span class="sxs-lookup"><span data-stu-id="5ea10-109">Keywords</span></span>
- <span data-ttu-id="5ea10-110">**モデル** - 他の 2 つのモデルを参照するモデルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-110">**Model** - You configure your model to refer to two other models.</span></span> <span data-ttu-id="5ea10-111">これにより、モデルは他のパッケージにあるメタデータとコード要素を参照できます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-111">This enables your model to reference metadata and code elements that are in other packages.</span></span>
- <span data-ttu-id="5ea10-112">**プロジェクト** - **Dynamics AX** プロジェクトを作成し、プロジェクトを新しいモデルに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-112">**Project** - You create a **Dynamics AX** project, and you associate your project to your new model.</span></span> <span data-ttu-id="5ea10-113">要素をプロジェクトに追加します。これはモデルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-113">You add elements to your project, which are also added to your model.</span></span> <span data-ttu-id="5ea10-114">具体的には、拡張データ型 (EDT) を追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-114">Specifically, you add an extended data type (EDT).</span></span> <span data-ttu-id="5ea10-115">また、フィールドおよびメソッドで入力するテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-115">You also add a table that you populate with fields and a method.</span></span>
- <span data-ttu-id="5ea10-116">**デザイナー** - プロジェクトに品目を追加するたびに、選択した品目タイプに合わせたデザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-116">**Designer** - Each time you add an item to your project, a designer is displayed that is tailored to the item type you choose.</span></span> <span data-ttu-id="5ea10-117">**プロパティ** ウィンドウは、デザイナーの異なるノードが強調表示されるたびに調整されます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-117">The **Properties** window adjusts each time a different node of the designer is highlighted.</span></span> <span data-ttu-id="5ea10-118">デザイナーおよび **プロパティ** ウィンドウで更新を行います。</span><span class="sxs-lookup"><span data-stu-id="5ea10-118">You make updates in the designers and in the **Properties** window.</span></span>
- <span data-ttu-id="5ea10-119">**EDT** - 拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="5ea10-119">**EDT** - Extended data type.</span></span>

## <a name="create-the-fleet-management-tutorial-model"></a><span data-ttu-id="5ea10-120">フリート管理チュートリアル モデルを作成する</span><span class="sxs-lookup"><span data-stu-id="5ea10-120">Create the Fleet Management tutorial model</span></span>
1.  <span data-ttu-id="5ea10-121">**管理者として実行** を使用して Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-121">Start Visual Studio using **Run as administrator**.</span></span>
2.  <span data-ttu-id="5ea10-122">**Dynamics AX** ウィンドウから、**モデル管理 &gt; モデルの作成**を選択し、**モデルの作成**ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-122">From the **Dynamics AX** window, select **Model Management &gt; Create model** to open the **Create model** wizard.</span></span>
3.  <span data-ttu-id="5ea10-123">モデル パラメーターの以下の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-123">Enter the following values for model parameters.</span></span>

    | <span data-ttu-id="5ea10-124">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5ea10-124">**Property**</span></span>           | <span data-ttu-id="5ea10-125">**値**</span><span class="sxs-lookup"><span data-stu-id="5ea10-125">**Value**</span></span>                                                                                                                |
    |------------------------|--------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5ea10-126">**モデル名**</span><span class="sxs-lookup"><span data-stu-id="5ea10-126">**Model name**</span></span>         | <span data-ttu-id="5ea10-127">FleetMgmntTutorial</span><span class="sxs-lookup"><span data-stu-id="5ea10-127">FleetMgmntTutorial</span></span>                                                                                                       |
    | <span data-ttu-id="5ea10-128">**モデル発行元**</span><span class="sxs-lookup"><span data-stu-id="5ea10-128">**Model publisher**</span></span>    | <span data-ttu-id="5ea10-129">Microsoft Corp</span><span class="sxs-lookup"><span data-stu-id="5ea10-129">Microsoft Corp</span></span>                                                                                                           |
    | <span data-ttu-id="5ea10-130">**レイヤー**</span><span class="sxs-lookup"><span data-stu-id="5ea10-130">**Layer**</span></span>              | <span data-ttu-id="5ea10-131">isv</span><span class="sxs-lookup"><span data-stu-id="5ea10-131">isv</span></span>                                                                                                                      |
    | <span data-ttu-id="5ea10-132">**モデルの説明**</span><span class="sxs-lookup"><span data-stu-id="5ea10-132">**Model description**</span></span>  | <span data-ttu-id="5ea10-133">このチュートリアルでは、Microsoft Dynamics AX の開発ツールを使用して、フリート管理 アプリケーションを構築する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-133">This tutorial shows how to build the Fleet Management application by using the Microsoft Dynamics AX  development tools.</span></span> |
    | <span data-ttu-id="5ea10-134">**モデルの表示名**</span><span class="sxs-lookup"><span data-stu-id="5ea10-134">**Model display name**</span></span> | <span data-ttu-id="5ea10-135">フリート管理のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="5ea10-135">Fleet Management Tutorial</span></span>                                                                                                |

    <span data-ttu-id="5ea10-136">**注記**: モデルの名前は **FleetMgmntTutorial** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ea10-136">**Note**: Your model name must be **FleetMgmntTutorial**.</span></span> <span data-ttu-id="5ea10-137">他の名前は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5ea10-137">Don't use any other name.</span></span> <span data-ttu-id="5ea10-138">その他のチュートリアルでは、プロジェクトをインポートすることでこのモデル内のモデル要素を上書きします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-138">In other tutorials, you'll overwrite model elements in this model by importing a project.</span></span> <span data-ttu-id="5ea10-139">このチュートリアルで作成したモデルに **FleetMgmntTutorial** という名前が付けられていない場合、その他のチュートリアルでプロジェクトが正しくインポートできない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5ea10-139">If the model you create in this tutorial isn't named **FleetMgmntTutorial**, you may not be able to correctly import the project in other tutorials.</span></span>
4.  <span data-ttu-id="5ea10-140">**次へ**をクリックして次のページに移動し、次に**新しいパッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-140">Click **Next** to advance to the next page, and then select **Create New Package**.</span></span> <span data-ttu-id="5ea10-141">作成しているモデルは独自のパッケージを持ち、独自の .NET アセンブリを構築します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-141">The model you're creating will have its own package and build its own .NET assembly.</span></span> 

    <span data-ttu-id="5ea10-142">[![Package\_DataModel](./media/package_datamodel.png)](./media/package_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-142">[![Package\_DataModel](./media/package_datamodel.png)](./media/package_datamodel.png)</span></span>

5.  <span data-ttu-id="5ea10-143">**次へ**をクリックし、**参照モデルを選択**ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-143">Click **Next** to advance to the **Select referenced models** step.</span></span>
6.  <span data-ttu-id="5ea10-144">参照されるモデルとして **アプリケーション プラットフォーム** および **アプリケーション基盤** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-144">Select **Application Platform** and **Application Foundation** as referenced models.</span></span>

    <span data-ttu-id="5ea10-145">[![ReferenceModels\_DataModel](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-145">[![ReferenceModels\_DataModel](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span></span> 

    <span data-ttu-id="5ea10-146">**重要**: 正しい参照モデルを選択していることを確認ください。</span><span class="sxs-lookup"><span data-stu-id="5ea10-146">**Important**: Verify that you've selected the correct referenced models.</span></span>
7.  <span data-ttu-id="5ea10-147">**次へ**をクリックし、**概要**ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-147">Click **Next** to advance to the **Summary** step.</span></span>
8.  <span data-ttu-id="5ea10-148">概要ページの情報を確認してから、**新規プロジェクトの作成** および **これを新規プロジェクトの自分の既定のモデルにする** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-148">Verify the information on the summary page, and then select the **Create new project** and **Make this my default model for new projects** check boxes.</span></span> 

    <span data-ttu-id="5ea10-149">[![Summary\_DataModel](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-149">[![Summary\_DataModel](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span></span>

9.  <span data-ttu-id="5ea10-150">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-150">Click **Finish**.</span></span> <span data-ttu-id="5ea10-151">**新しいプロジェクト** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-151">The **New Project** dialog box opens.</span></span>
10. <span data-ttu-id="5ea10-152">**テンプレート** で、**Dynamics AX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-152">Under **Templates**, select **Dynamics AX**.</span></span>
11. <span data-ttu-id="5ea10-153">**Dynamics AX Project** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-153">Select the **Dynamics AX Project** template.</span></span>
12. <span data-ttu-id="5ea10-154">ダイアログ ボックスのフィールドに次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-154">Enter the following values in the fields in the dialog box.</span></span>

    | <span data-ttu-id="5ea10-155">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5ea10-155">**Property**</span></span> | <span data-ttu-id="5ea10-156">**値**</span><span class="sxs-lookup"><span data-stu-id="5ea10-156">**Value**</span></span>       |
    |--------------|-----------------|
    | <span data-ttu-id="5ea10-157">**名前**</span><span class="sxs-lookup"><span data-stu-id="5ea10-157">**Name**</span></span>     | <span data-ttu-id="5ea10-158">FMTDataModel</span><span class="sxs-lookup"><span data-stu-id="5ea10-158">FMTDataModel</span></span>    |
    | <span data-ttu-id="5ea10-159">**保管場所**</span><span class="sxs-lookup"><span data-stu-id="5ea10-159">**Location**</span></span> | <span data-ttu-id="5ea10-160">C:\\FMLab</span><span class="sxs-lookup"><span data-stu-id="5ea10-160">C:\\FMLab</span></span>       |
    | <span data-ttu-id="5ea10-161">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="5ea10-161">**Solution**</span></span> | <span data-ttu-id="5ea10-162">ソリューションへの追加</span><span class="sxs-lookup"><span data-stu-id="5ea10-162">Add to solution</span></span> |

    <span data-ttu-id="5ea10-163">[![NewProject\_DataModel](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-163">[![NewProject\_DataModel](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span></span>

13. <span data-ttu-id="5ea10-164">プロジェクトを作成するには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-164">Click **OK** to create the project.</span></span>

## <a name="create-the-fmtaddress-extended-data-type"></a><span data-ttu-id="5ea10-165">FMTAddress の拡張データ型を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-165">Create the FMTAddress extended data type</span></span>
1.  <span data-ttu-id="5ea10-166">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-166">In **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="5ea10-167">**AX アーティファクト**で、**データ型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-167">Under **AX Artifacts**, select **Data Types**.</span></span>
3.  <span data-ttu-id="5ea10-168">**EDT 文字列**をクリックし、を新しい項目の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-168">Click **EDT String** to select the new item type.</span></span>
4.  <span data-ttu-id="5ea10-169">**名前**フィールドに、**FMTAddress** と入力してから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-169">In the **Name** field, enter **FMTAddress**, and then click **Add**.</span></span> 

    <span data-ttu-id="5ea10-170">[![NewItem\_DataModel](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-170">[![NewItem\_DataModel](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span></span> 

    <span data-ttu-id="5ea10-171">これにより、新しい EDT モデル要素をプロジェクトに追加され、次の図に示すように、新しい要素の EDT デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-171">This adds a new EDT model element to the project, and opens the EDT designer for the new element, as shown in the following illustration.</span></span> 

    <span data-ttu-id="5ea10-172">[![EDTelement\_DataModel](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-172">[![EDTelement\_DataModel](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span></span>

5.  <span data-ttu-id="5ea10-173">デザイナーで **FMTAddress** ルート ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-173">Select the root node of **FMTAddress** in the designer.</span></span>
6.  <span data-ttu-id="5ea10-174">**プロパティ** ウィンドウの**外観セクション**で、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-174">In the **Properties** window, in the **Appearance section**, set the following properties.</span></span>

    | <span data-ttu-id="5ea10-175">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="5ea10-175">**Property**</span></span>    | <span data-ttu-id="5ea10-176">**値**</span><span class="sxs-lookup"><span data-stu-id="5ea10-176">**Value**</span></span>          |
    |-----------------|--------------------|
    | <span data-ttu-id="5ea10-177">**ヘルプ テキスト**</span><span class="sxs-lookup"><span data-stu-id="5ea10-177">**Help Text**</span></span>   | <span data-ttu-id="5ea10-178">オンライン ヘルプをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="5ea10-178">Check online help.</span></span> |
    | <span data-ttu-id="5ea10-179">**ラベル**</span><span class="sxs-lookup"><span data-stu-id="5ea10-179">**Label**</span></span>       | <span data-ttu-id="5ea10-180">アドレス</span><span class="sxs-lookup"><span data-stu-id="5ea10-180">Address</span></span>            |
    | <span data-ttu-id="5ea10-181">**文字列サイズ**</span><span class="sxs-lookup"><span data-stu-id="5ea10-181">**String Size**</span></span> | <span data-ttu-id="5ea10-182">75</span><span class="sxs-lookup"><span data-stu-id="5ea10-182">75</span></span>                 |

    <span data-ttu-id="5ea10-183">[![EDTProperty\_DataModel](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-183">[![EDTProperty\_DataModel](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span></span>

7.  <span data-ttu-id="5ea10-184">**Ctrl+S** キーを押して EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-184">Press **Ctrl+S** to save the EDT.</span></span>

## <a name="add-existing-model"></a><span data-ttu-id="5ea10-185">既存のモデルの追加</span><span class="sxs-lookup"><span data-stu-id="5ea10-185">Add existing model</span></span>
<span data-ttu-id="5ea10-186">現在のモデルとプロジェクトに他の必要なモデル要素ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-186">Add the other required model element files to the current model and project.</span></span> <span data-ttu-id="5ea10-187">**既存の品目を追加** フィーチャーを使用することにより、これを素早く実行することができます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-187">You can do this quickly by using the **Add existing item** feature.</span></span>

1.  <span data-ttu-id="5ea10-188">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックして**追加**をポイントしてから**既存の項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-188">In the **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="5ea10-189">C:\\FMLab\\EDT\\ を参照します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-189">Browse to C:\\FMLab\\EDT\\.</span></span> 

    <span data-ttu-id="5ea10-190">[![ExistingItem\_DataModel](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-190">[![ExistingItem\_DataModel](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span></span>

3.  <span data-ttu-id="5ea10-191">**Ctrl+A** を押してすべてのファイルを選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-191">Press **Ctrl+A** to select all of the files, and then click **Add**.</span></span>

## <a name="create-the-fmtcustomer-table"></a><span data-ttu-id="5ea10-192">FMTCustomer テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-192">Create the FMTCustomer table</span></span>
1. <span data-ttu-id="5ea10-193">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**追加 &gt; 新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-193">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Add &gt; New Item**.</span></span>
2. <span data-ttu-id="5ea10-194">左ウィンドウで、<strong>インストール済み</strong>を展開し、*<strong><em>AX アーティファクト</em>*</strong>を展開してから、*<strong><em>データ モデル</em>*</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-194">In the left pane, expand <strong>Installed</strong>, expand *<strong><em>AX Artifacts</em>*,</strong> and then click *<strong><em>Data Model</em>*.</strong></span></span>
3. <span data-ttu-id="5ea10-195">アーティファクトの一覧で**テーブル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-195">In the list of artifacts, select **Table**.</span></span>
4. <span data-ttu-id="5ea10-196">**名前**フィールドに、**FMTCustomer** と入力してから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-196">In the **Name** field, enter **FMTCustomer**, and then click **Add**.</span></span> <span data-ttu-id="5ea10-197">テーブル デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-197">The table designer opens.</span></span> 

   <span data-ttu-id="5ea10-198">[![Add\_DataModel](./media/add_datamodel.png)](./media/add_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-198">[![Add\_DataModel](./media/add_datamodel.png)](./media/add_datamodel.png)</span></span>

### <a name="add-fields-to-the-fmtcustomer-table"></a><span data-ttu-id="5ea10-199">FMTCustomer テーブルへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="5ea10-199">Add fields to the FMTCustomer table</span></span>

<span data-ttu-id="5ea10-200">FMTCustomer のテーブル デザイナーで、テーブルに複数のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-200">In the table designer for FMTCustomer, you now add several fields to the table.</span></span> 

<span data-ttu-id="5ea10-201">[![AddFields\_DataModel](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-201">[![AddFields\_DataModel](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span></span>

1.  <span data-ttu-id="5ea10-202">各フィールドを追加するには、**フィールド** を右クリックし、**新規** をクリックして、タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-202">To add each field, right-click **Fields**, click **New**, and then select a type.</span></span> <span data-ttu-id="5ea10-203">各フィールドを追加すると、次の表に示すように、**プロパティ** ウィンドウでフィールド名とその他の特定の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ea10-203">As you add each field, you must specify the field name and certain other values in the **Properties** window, as described in the following table.</span></span>

    | <span data-ttu-id="5ea10-204">**タイプ**</span><span class="sxs-lookup"><span data-stu-id="5ea10-204">**Type**</span></span>   | <span data-ttu-id="5ea10-205">**フィールド名**</span><span class="sxs-lookup"><span data-stu-id="5ea10-205">**Field name**</span></span> | <span data-ttu-id="5ea10-206">**プロパティ値**</span><span class="sxs-lookup"><span data-stu-id="5ea10-206">**Property values**</span></span>                                                         |
    |------------|----------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="5ea10-207">**日付**</span><span class="sxs-lookup"><span data-stu-id="5ea10-207">**Date**</span></span>   | <span data-ttu-id="5ea10-208">CCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="5ea10-208">CCExpiryDate</span></span>   | <span data-ttu-id="5ea10-209">拡張データ型 = FMTCCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="5ea10-209">Extended Data Type = FMTCCExpiryDate</span></span>                                        |
    | <span data-ttu-id="5ea10-210">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-210">**String**</span></span> | <span data-ttu-id="5ea10-211">アドレス</span><span class="sxs-lookup"><span data-stu-id="5ea10-211">Address</span></span>        | <span data-ttu-id="5ea10-212">拡張データ型 = FMTAddressHelp テキスト = アドレス フィールドのヘルプ テキスト。</span><span class="sxs-lookup"><span data-stu-id="5ea10-212">Extended Data Type = FMTAddressHelp Text = Help text for the address field.</span></span> |
    | <span data-ttu-id="5ea10-213">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-213">**String**</span></span> | <span data-ttu-id="5ea10-214">CellPhone</span><span class="sxs-lookup"><span data-stu-id="5ea10-214">CellPhone</span></span>      | <span data-ttu-id="5ea10-215">拡張データ型 = 電話</span><span class="sxs-lookup"><span data-stu-id="5ea10-215">Extended Data Type = Phone</span></span>                                                  |
    | <span data-ttu-id="5ea10-216">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-216">**String**</span></span> | <span data-ttu-id="5ea10-217">CreditCardNum</span><span class="sxs-lookup"><span data-stu-id="5ea10-217">CreditCardNum</span></span>  | <span data-ttu-id="5ea10-218">拡張データ型 = FMTCreditCardNum</span><span class="sxs-lookup"><span data-stu-id="5ea10-218">Extended Data Type = FMTCreditCardNum</span></span>                                       |
    | <span data-ttu-id="5ea10-219">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-219">**String**</span></span> | <span data-ttu-id="5ea10-220">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="5ea10-220">DriversLicense</span></span> | <span data-ttu-id="5ea10-221">拡張データ型 = FMTDriversLicense</span><span class="sxs-lookup"><span data-stu-id="5ea10-221">Extended Data Type = FMTDriversLicense</span></span>                                      |
    | <span data-ttu-id="5ea10-222">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-222">**String**</span></span> | <span data-ttu-id="5ea10-223">電子メール</span><span class="sxs-lookup"><span data-stu-id="5ea10-223">Email</span></span>          | <span data-ttu-id="5ea10-224">文字列サイズ = 80Label = 電子メール</span><span class="sxs-lookup"><span data-stu-id="5ea10-224">String Size = 80Label = Email</span></span>                                               |
    | <span data-ttu-id="5ea10-225">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-225">**String**</span></span> | <span data-ttu-id="5ea10-226">名</span><span class="sxs-lookup"><span data-stu-id="5ea10-226">FirstName</span></span>      | <span data-ttu-id="5ea10-227">拡張データ型 = FirstName</span><span class="sxs-lookup"><span data-stu-id="5ea10-227">Extended Data Type = FirstName</span></span>                                              |
    | <span data-ttu-id="5ea10-228">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-228">**String**</span></span> | <span data-ttu-id="5ea10-229">姓</span><span class="sxs-lookup"><span data-stu-id="5ea10-229">LastName</span></span>       | <span data-ttu-id="5ea10-230">拡張データ型 = LastName</span><span class="sxs-lookup"><span data-stu-id="5ea10-230">Extended Data Type = LastName</span></span>                                               |
    | <span data-ttu-id="5ea10-231">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-231">**String**</span></span> | <span data-ttu-id="5ea10-232">ライセンス</span><span class="sxs-lookup"><span data-stu-id="5ea10-232">License</span></span>        | <span data-ttu-id="5ea10-233">文字列サイズ = 100Label = ライセンス</span><span class="sxs-lookup"><span data-stu-id="5ea10-233">String Size = 100Label = License</span></span>                                            |
    | <span data-ttu-id="5ea10-234">**文字列**</span><span class="sxs-lookup"><span data-stu-id="5ea10-234">**String**</span></span> | <span data-ttu-id="5ea10-235">縮小版</span><span class="sxs-lookup"><span data-stu-id="5ea10-235">Thumbnail</span></span>      | <span data-ttu-id="5ea10-236">文字列サイズ = 100Label = サムネイル</span><span class="sxs-lookup"><span data-stu-id="5ea10-236">String Size = 100Label = Thumbnail</span></span>                                          |

    <span data-ttu-id="5ea10-237">**ヒント**: EDT を参照するテーブル内のすべての新しいフィールドのために、**ソリューション エクスプローラ**または**アプリケーション エクスプローラー**から EDT エレメントをドラッグし、デザイナーの **FMTCustomer** テーブルの**フィールド** ノードをドロップするだけで、フィールドを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-237">**Tip**: For all new fields in the table that reference an EDT, you can create the field by simply dragging the EDT element from **Solution Explorer** or **Application Explorer** and dropping it on the **Fields** node of the **FMTCustomer** table in the designer.</span></span> 

    <span data-ttu-id="5ea10-238">[![AdministratorArrow\_DataModel](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-238">[![AdministratorArrow\_DataModel](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span></span>

2.  <span data-ttu-id="5ea10-239">**Ctrl+S** キーを押して、テーブルに新しいフィールドを保存します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-239">Press **Ctrl+S** to save the new fields on the table.</span></span>

### <a name="add-fields-to-field-groups"></a><span data-ttu-id="5ea10-240">フィールド グループへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="5ea10-240">Add fields to field groups</span></span>

1.  <span data-ttu-id="5ea10-241">次の一覧のフィールドを選択して、一部の不フィールドを **AutoSummary** フィールド グループに追加する準備をします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-241">Prepare to add some of the fields to the **AutoSummary** field group by selecting the fields in the following list.</span></span> <span data-ttu-id="5ea10-242">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-242">To select multiple fields, hold down the Ctrl key while you click each field:</span></span>
    -   <span data-ttu-id="5ea10-243">**住所**</span><span class="sxs-lookup"><span data-stu-id="5ea10-243">**Address**</span></span>
    -   <span data-ttu-id="5ea10-244">**CCExpiryDate**</span><span class="sxs-lookup"><span data-stu-id="5ea10-244">**CCExpiryDate**</span></span>
    -   <span data-ttu-id="5ea10-245">**CellPhone**</span><span class="sxs-lookup"><span data-stu-id="5ea10-245">**CellPhone**</span></span>
    -   <span data-ttu-id="5ea10-246">**CreditCardNum**</span><span class="sxs-lookup"><span data-stu-id="5ea10-246">**CreditCardNum**</span></span>
    -   <span data-ttu-id="5ea10-247">**DriversLicense**</span><span class="sxs-lookup"><span data-stu-id="5ea10-247">**DriversLicense**</span></span>
    -   <span data-ttu-id="5ea10-248">**電子メール**</span><span class="sxs-lookup"><span data-stu-id="5ea10-248">**Email**</span></span>
    -   <span data-ttu-id="5ea10-249">**名**</span><span class="sxs-lookup"><span data-stu-id="5ea10-249">**FirstName**</span></span>
    -   <span data-ttu-id="5ea10-250">**姓**</span><span class="sxs-lookup"><span data-stu-id="5ea10-250">**LastName**</span></span>

2.  <span data-ttu-id="5ea10-251">**フィールド グループ**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-251">Expand the **Field Groups** node.</span></span>
3.  <span data-ttu-id="5ea10-252">選択したフィールドを **AutoSummary** ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-252">Drag the selected fields to the **AutoSummary** node</span></span>
4.  <span data-ttu-id="5ea10-253">同じ方法を使用して、**氏名**、**姓**、および**携帯**フィールドを**自動レポート**フィールド グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-253">Use the same technique to add the fields **FirstName**, **LastName**, and **CellPhone** to the **AutoReport** field group.</span></span>
5.  <span data-ttu-id="5ea10-254">テーブルを保存します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-254">Save the table.</span></span>

### <a name="add-a-method"></a><span data-ttu-id="5ea10-255">メソッドの追加</span><span class="sxs-lookup"><span data-stu-id="5ea10-255">Add a method</span></span>

1.  <span data-ttu-id="5ea10-256">**Methods** ノードを右クリックし、**New Method** をクリックして、**FMTCustomer** テーブルに **fullName** という名前の X++ メソッドを 追加します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-256">Add the X++ method named **fullName** to the **FMTCustomer** table by right-clicking the **Methods** node, and then clicking **New Method**.</span></span>
2.  <span data-ttu-id="5ea10-257">コード エディターで、既定のメソッドのコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-257">In the code editor, replace the default method code with the following code.</span></span> <span data-ttu-id="5ea10-258">**ヒント**: 「this.」を入力するとき、IntelliSense リストからフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-258">**Tip**: When you type “this.”, choose the field from the IntelliSense list.</span></span>

        public display FMTName fullName()
        {
            return this.FirstName + ' ' + this.LastName;
        }

3.  <span data-ttu-id="5ea10-259">コードを保存します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-259">Save the code.</span></span>

## <a name="update-the-fmtaddress-edt"></a><span data-ttu-id="5ea10-260">FMTAddress EDT の更新</span><span class="sxs-lookup"><span data-stu-id="5ea10-260">Update the FMTAddress EDT</span></span>
1.  <span data-ttu-id="5ea10-261">**ソリューション エクスプローラー**で **FMTDataModel** プロジェクトを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-261">In **Solution Explorer**, expand the **FMTDataModel** project.</span></span>
2.  <span data-ttu-id="5ea10-262">**FMTAddress** を右クリックしてから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-262">Right-click **FMTAddress**, and then click **Open**.</span></span> <span data-ttu-id="5ea10-263">**EDT デザイナー**が開きます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-263">The **EDT designer** opens.</span></span>
3.  <span data-ttu-id="5ea10-264">**EDT デザイナー**で、**FMTAddress** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-264">In the **EDT designer**, select **FMTAddress**.</span></span>
4.  <span data-ttu-id="5ea10-265">**プロパティ** ウィンドウの**参照テーブル** フィールドで、**FMTCustomer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-265">In the **Properties** window, in the **Reference Table** field, select **FMTCustomer**.</span></span> <span data-ttu-id="5ea10-266">**ヒント:** ドロップダウン リストをクリックし、検索ボックスに、接頭語「FMT」を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-266">**Tip:** Click the drop-down list, and then type the prefix "FMT" in the search box.</span></span> <span data-ttu-id="5ea10-267">これにより、名前に「FMT」が含まれている表のみが表示されるように、ドロップダウン リストがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-267">This filters the drop-down list to only show tables that contain "FMT" in their name.</span></span> <span data-ttu-id="5ea10-268">フィルター処理されたエントリの一覧から **FMTCustomer** テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-268">Select the **FMTCustomer** table from the list of filtered entries.</span></span> <span data-ttu-id="5ea10-269">[![SearchFMT\_DataModel](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="5ea10-269">[![SearchFMT\_DataModel](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span></span>
5.  <span data-ttu-id="5ea10-270">EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-270">Save the EDT.</span></span>

## <a name="build-the-fmtdatamodel-project-and-the-fleet-management-tutorial-model"></a><span data-ttu-id="5ea10-271">FMTDataModel プロジェクトと フリート管理チュートリアル モデルの構築</span><span class="sxs-lookup"><span data-stu-id="5ea10-271">Build the FMTDataModel project and the Fleet Management tutorial model</span></span>
1. <span data-ttu-id="5ea10-272">**ソリューション エクスプローラー**で、**FMTDataModel** を右クリックしてから**リビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-272">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Rebuild**.</span></span>
2. <span data-ttu-id="5ea10-273">モデル全体の完全なビルドを行うには、<strong>Dynamics AX **</strong> メニューで [モデルを**ビルド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-273">To do a full build of the entire model, on the <strong>Dynamics AX **menu, click **Build models.</strong></span></span>
3. <span data-ttu-id="5ea10-274">**フリート管理チュートリアル**以外のすべてのモデルのチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-274">Clear the check box for all models except for **Fleet Management Tutorial**.</span></span>
4. <span data-ttu-id="5ea10-275">**オプション**タブで、**推奨チェックの実行**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ea10-275">On the **Options** tab, select the **Run Best practice checks** check box.</span></span> <span data-ttu-id="5ea10-276">使用可能なその他のオプションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5ea10-276">Note that other options available.</span></span>
5. <span data-ttu-id="5ea10-277">**モデル**タブで、**ビルド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-277">On the **Models** tab, click **Build**.</span></span>
6. <span data-ttu-id="5ea10-278">ダイアログ ボックスで **閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ea10-278">Click **Close**  in the dialog box.</span></span>
7. <span data-ttu-id="5ea10-279">**ウィンドウ**メニューで、**すべてのドキュメントを閉じる**をクリックして、開いているすべてのドキュメントを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5ea10-279">On the **Window** menu, click **Close All Documents**, to close all open documents.</span></span>





