---
title: モデルの作成、およびデータモデル要素の作成についての概要
description: このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、フリート管理チュートリアルという名前の新しいモデルを作成します。
author: RobinARH
ms.date: 07/23/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 23421
ms.assetid: 1b7789f4-12c1-480b-bb39-c354b5b03276
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5b63d0cd0c995e06f42ce998893ad8f38ab61e
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866005"
---
# <a name="create-models-and-data-model-elements-overview"></a><span data-ttu-id="2014d-103">モデルとデータ モデル要素の作成の概要</span><span class="sxs-lookup"><span data-stu-id="2014d-103">Create models and data model elements overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2014d-104">このチュートリアルでは、Visual Studio の Dynamics 365 メニューを使用して、**フリート管理チュートリアル** という名前の新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="2014d-104">In this tutorial, you'll use Visual Studio's Dynamics 365 menu to create a new model named **Fleet Management tutorial**.</span></span> <span data-ttu-id="2014d-105">また、新しいモデルの要素を作成および編集します。</span><span class="sxs-lookup"><span data-stu-id="2014d-105">You'll also create and edit new model elements.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2014d-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="2014d-106">Prerequisites</span></span>

<span data-ttu-id="2014d-107">このチュートリアルでは、プロビジョニングする環境に管理者としてアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2014d-107">This tutorial requires that you have access to an environment, and that you be provisioned as an administrator</span></span>

## <a name="keywords"></a><span data-ttu-id="2014d-108">キーワード</span><span class="sxs-lookup"><span data-stu-id="2014d-108">Keywords</span></span>

- <span data-ttu-id="2014d-109">**モデル** - 他の 2 つのモデルを参照するモデルをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2014d-109">**Model** - You configure your model to refer to two other models.</span></span> <span data-ttu-id="2014d-110">これにより、モデルは他のパッケージにあるメタデータとコード要素を参照できます。</span><span class="sxs-lookup"><span data-stu-id="2014d-110">This enables your model to reference metadata and code elements that are in other packages.</span></span>
- <span data-ttu-id="2014d-111">**プロジェクト** - プロジェクトを作成し、次に新しいモデルにプロジェクトを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="2014d-111">**Project** - You create a project and then associate your project to your new model.</span></span> <span data-ttu-id="2014d-112">要素をプロジェクトに追加します。これはモデルにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="2014d-112">You add elements to your project, which are also added to your model.</span></span> <span data-ttu-id="2014d-113">具体的には、拡張データ型 (EDT) を追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-113">Specifically, you add an extended data type (EDT).</span></span> <span data-ttu-id="2014d-114">また、フィールドおよびメソッドで入力するテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-114">You also add a table that you populate with fields and a method.</span></span>
- <span data-ttu-id="2014d-115">**デザイナー** - プロジェクトに品目を追加するたびに、選択した品目タイプに合わせたデザイナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2014d-115">**Designer** - Each time you add an item to your project, a designer is displayed that is tailored to the item type you selected.</span></span> <span data-ttu-id="2014d-116">**プロパティ** ウィンドウは、デザイナーの異なるノードが強調表示されるたびに調整されます。</span><span class="sxs-lookup"><span data-stu-id="2014d-116">The **Properties** window adjusts each time a different node of the designer is highlighted.</span></span> <span data-ttu-id="2014d-117">デザイナーおよび **プロパティ** ウィンドウで更新を行います。</span><span class="sxs-lookup"><span data-stu-id="2014d-117">You make updates in the designers and in the **Properties** window.</span></span>
- <span data-ttu-id="2014d-118">**EDT** - 拡張データ型。</span><span class="sxs-lookup"><span data-stu-id="2014d-118">**EDT** - Extended data type.</span></span>

## <a name="create-the-fleet-management-tutorial-model"></a><span data-ttu-id="2014d-119">フリート管理チュートリアル モデルを作成する</span><span class="sxs-lookup"><span data-stu-id="2014d-119">Create the Fleet Management tutorial model</span></span>

1. <span data-ttu-id="2014d-120">**管理者として実行** を使用して Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="2014d-120">Start Visual Studio using **Run as administrator**.</span></span>
2. <span data-ttu-id="2014d-121">**Dynamics 365** メニューから、**モデル管理 &gt; モデルの作成** を選択して、**モデルの作成** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="2014d-121">From the **Dynamics 365** menu, select **Model Management &gt; Create model** to open the **Create model** wizard.</span></span>
3. <span data-ttu-id="2014d-122">モデル パラメーターの以下の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2014d-122">Enter the following values for model parameters.</span></span>

    | <span data-ttu-id="2014d-123">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2014d-123">Property</span></span>               | <span data-ttu-id="2014d-124">Value</span><span class="sxs-lookup"><span data-stu-id="2014d-124">Value</span></span>                                                                                                                    |
    |------------------------|--------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="2014d-125">**モデル名**</span><span class="sxs-lookup"><span data-stu-id="2014d-125">**Model name**</span></span>         | <span data-ttu-id="2014d-126">FleetMgmntTutorial</span><span class="sxs-lookup"><span data-stu-id="2014d-126">FleetMgmntTutorial</span></span>                                                                                                       |
    | <span data-ttu-id="2014d-127">**モデル発行元**</span><span class="sxs-lookup"><span data-stu-id="2014d-127">**Model publisher**</span></span>    | <span data-ttu-id="2014d-128">Microsoft Corp</span><span class="sxs-lookup"><span data-stu-id="2014d-128">Microsoft Corp</span></span>                                                                                                           |
    | <span data-ttu-id="2014d-129">**レイヤー**</span><span class="sxs-lookup"><span data-stu-id="2014d-129">**Layer**</span></span>              | <span data-ttu-id="2014d-130">isv</span><span class="sxs-lookup"><span data-stu-id="2014d-130">isv</span></span>                                                                                                                      |
    | <span data-ttu-id="2014d-131">**モデルの説明**</span><span class="sxs-lookup"><span data-stu-id="2014d-131">**Model description**</span></span>  | <span data-ttu-id="2014d-132">このチュートリアルでは、Microsoft Dynamics AX の開発ツールを使用して、フリート管理 アプリケーションを構築する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2014d-132">This tutorial shows how to build the Fleet Management application by using the Microsoft Dynamics AX  development tools.</span></span> |
    | <span data-ttu-id="2014d-133">**モデルの表示名**</span><span class="sxs-lookup"><span data-stu-id="2014d-133">**Model display name**</span></span> | <span data-ttu-id="2014d-134">フリート管理のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="2014d-134">Fleet Management Tutorial</span></span>                                                                                                |

    > [!NOTE]
    > <span data-ttu-id="2014d-135">モデルの名前は **FleetMgmntTutorial** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2014d-135">Your model name must be **FleetMgmntTutorial**.</span></span> <span data-ttu-id="2014d-136">他の名前は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2014d-136">Don't use any other name.</span></span> <span data-ttu-id="2014d-137">その他のチュートリアルでは、プロジェクトをインポートすることでこのモデル内のモデル要素を上書きします。</span><span class="sxs-lookup"><span data-stu-id="2014d-137">In other tutorials, you'll overwrite model elements in this model by importing a project.</span></span> <span data-ttu-id="2014d-138">このチュートリアルで作成したモデルに **FleetMgmntTutorial** という名前が付けられていない場合、その他のチュートリアルでプロジェクトが正しくインポートできない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2014d-138">If the model you create in this tutorial isn't named **FleetMgmntTutorial**, you may not be able to correctly import the project in other tutorials.</span></span>

4. <span data-ttu-id="2014d-139">**次へ** をクリックして次のページに移動し、次に **新しいパッケージの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-139">Click **Next** to advance to the next page, and then select **Create New Package**.</span></span> <span data-ttu-id="2014d-140">作成しているモデルは独自のパッケージを持ち、独自の .NET アセンブリを構築します。</span><span class="sxs-lookup"><span data-stu-id="2014d-140">The model you're creating will have its own package and build its own .NET assembly.</span></span>

    <span data-ttu-id="2014d-141">[![パッケージを選択](./media/package_datamodel.png)](./media/package_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-141">[![Select package](./media/package_datamodel.png)](./media/package_datamodel.png)</span></span>

5. <span data-ttu-id="2014d-142">**次へ** をクリックし、**参照モデルを選択** ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="2014d-142">Click **Next** to advance to the **Select referenced models** step.</span></span>
6. <span data-ttu-id="2014d-143">参照されるモデルとして **アプリケーション プラットフォーム** および **アプリケーション基盤** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-143">Select **Application Platform** and **Application Foundation** as referenced models.</span></span>

    <span data-ttu-id="2014d-144">[![参照モデルを選択](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-144">[![Select referenced models](./media/referencemodels_datamodel.png)](./media/referencemodels_datamodel.png)</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="2014d-145">正しい参照モデルを選択していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2014d-145">Verify that you've selected the correct referenced models.</span></span>

7. <span data-ttu-id="2014d-146">**次へ** をクリックし、**概要** ステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="2014d-146">Click **Next** to advance to the **Summary** step.</span></span>
8. <span data-ttu-id="2014d-147">概要ページの情報を確認してから、**新規プロジェクトの作成** および **これを新規プロジェクトの自分の既定のモデルにする** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-147">Verify the information on the summary page, and then select the **Create new project** and **Make this my default model for new projects** check boxes.</span></span>

    <span data-ttu-id="2014d-148">[![データ モデルの概要](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-148">[![Summary of data model](./media/summary_datamodel.png)](./media/summary_datamodel.png)</span></span>

9. <span data-ttu-id="2014d-149">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-149">Click **Finish**.</span></span> <span data-ttu-id="2014d-150">**新しいプロジェクト** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="2014d-150">The **New Project** dialog box opens.</span></span>
10. <span data-ttu-id="2014d-151">**テンプレート** で、**Dynamics 365** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-151">Under **Templates**, select **Dynamics 365**.</span></span>
11. <span data-ttu-id="2014d-152">**Unified Operations** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-152">Select the **Unified Operations** template.</span></span>
12. <span data-ttu-id="2014d-153">ダイアログ ボックスのフィールドに次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2014d-153">Enter the following values in the fields in the dialog box.</span></span>

    | <span data-ttu-id="2014d-154">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2014d-154">Property</span></span>     | <span data-ttu-id="2014d-155">Value</span><span class="sxs-lookup"><span data-stu-id="2014d-155">Value</span></span>           |
    |--------------|-----------------|
    | <span data-ttu-id="2014d-156">**名前**</span><span class="sxs-lookup"><span data-stu-id="2014d-156">**Name**</span></span>     | <span data-ttu-id="2014d-157">FMTDataModel</span><span class="sxs-lookup"><span data-stu-id="2014d-157">FMTDataModel</span></span>    |
    | <span data-ttu-id="2014d-158">**保管場所**</span><span class="sxs-lookup"><span data-stu-id="2014d-158">**Location**</span></span> | <span data-ttu-id="2014d-159">C:\\FMLab</span><span class="sxs-lookup"><span data-stu-id="2014d-159">C:\\FMLab</span></span>       |
    | <span data-ttu-id="2014d-160">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="2014d-160">**Solution**</span></span> | <span data-ttu-id="2014d-161">ソリューションへの追加</span><span class="sxs-lookup"><span data-stu-id="2014d-161">Add to solution</span></span> |

    <span data-ttu-id="2014d-162">[![新しいプロジェクト ダイアログ](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-162">[![New project dialog](./media/newproject_datamodel.png)](./media/newproject_datamodel.png)</span></span>

13. <span data-ttu-id="2014d-163">プロジェクトを作成するには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-163">Click **OK** to create the project.</span></span>

## <a name="create-the-fmtaddress-extended-data-type"></a><span data-ttu-id="2014d-164">FMTAddress の拡張データ型を作成します。</span><span class="sxs-lookup"><span data-stu-id="2014d-164">Create the FMTAddress extended data type</span></span>

1. <span data-ttu-id="2014d-165">**ソリューション エクスプローラー** で、**FMTDataModel** を右クリックして **追加** をポイントしてから **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-165">In **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **New Item**.</span></span>
2. <span data-ttu-id="2014d-166">**Dynamics 365 品目** で、**データ型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-166">Under **Dynamics 365 Items**, select **Data Types**.</span></span>
3. <span data-ttu-id="2014d-167">**EDT 文字列** をクリックし、を新しい項目の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-167">Click **EDT String** to select the new item type.</span></span>
4. <span data-ttu-id="2014d-168">**名前** フィールドに、**FMTAddress** と入力してから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-168">In the **Name** field, enter **FMTAddress**, and then click **Add**.</span></span>

    <span data-ttu-id="2014d-169">[![新しいデータ タイプの追加](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-169">[![Add a new data type](./media/newitem_datamodel.png)](./media/newitem_datamodel.png)</span></span>

    <span data-ttu-id="2014d-170">これにより、新しい EDT モデル要素をプロジェクトに追加され、次の図に示すように、新しい要素の EDT デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="2014d-170">This adds a new EDT model element to the project, and opens the EDT designer for the new element, as shown in the following illustration.</span></span>

    <span data-ttu-id="2014d-171">[![追加されたFMTAddress](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-171">[![FMTAddress added](./media/edtelement_datamodel.png)](./media/edtelement_datamodel.png)</span></span>

5. <span data-ttu-id="2014d-172">デザイナーで **FMTAddress** ルート ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-172">Select the root node of **FMTAddress** in the designer.</span></span>
6. <span data-ttu-id="2014d-173">**プロパティ** ウィンドウの **外観セクション** で、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2014d-173">In the **Properties** window, in the **Appearance section**, set the following properties.</span></span>

    | <span data-ttu-id="2014d-174">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2014d-174">Property</span></span>        | <span data-ttu-id="2014d-175">先頭値</span><span class="sxs-lookup"><span data-stu-id="2014d-175">Value</span></span>              |
    |-----------------|--------------------|
    | <span data-ttu-id="2014d-176">**ヘルプ テキスト**</span><span class="sxs-lookup"><span data-stu-id="2014d-176">**Help Text**</span></span>   | <span data-ttu-id="2014d-177">オンライン ヘルプをチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="2014d-177">Check online help.</span></span> |
    | <span data-ttu-id="2014d-178">**ラベル**</span><span class="sxs-lookup"><span data-stu-id="2014d-178">**Label**</span></span>       | <span data-ttu-id="2014d-179">住所</span><span class="sxs-lookup"><span data-stu-id="2014d-179">Address</span></span>            |
    | <span data-ttu-id="2014d-180">**文字列サイズ**</span><span class="sxs-lookup"><span data-stu-id="2014d-180">**String Size**</span></span> | <span data-ttu-id="2014d-181">75</span><span class="sxs-lookup"><span data-stu-id="2014d-181">75</span></span>                 |

    <span data-ttu-id="2014d-182">[![FMTAddress のプロパティ ウィンドウ](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-182">[![Properties window for FMTAddress](./media/edtproperty_datamodel.png)](./media/edtproperty_datamodel.png)</span></span>

7. <span data-ttu-id="2014d-183">**Ctrl+S** キーを押して EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="2014d-183">Press **Ctrl+S** to save the EDT.</span></span>

## <a name="add-existing-model"></a><span data-ttu-id="2014d-184">既存のモデルの追加</span><span class="sxs-lookup"><span data-stu-id="2014d-184">Add existing model</span></span>

<span data-ttu-id="2014d-185">現在のモデルとプロジェクトに他の必要なモデル要素ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-185">Add the other required model element files to the current model and project.</span></span> <span data-ttu-id="2014d-186">**既存の品目を追加** フィーチャーを使用することにより、これを素早く実行することができます。</span><span class="sxs-lookup"><span data-stu-id="2014d-186">You can do this quickly by using the **Add existing item** feature.</span></span>

1. <span data-ttu-id="2014d-187">**ソリューション エクスプローラー** で、**FMTDataModel** を右クリックして **追加** をポイントしてから **既存の項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-187">In the **Solution Explorer**, right-click **FMTDataModel**, point to **Add**, and then click **Existing Item**.</span></span>
2. <span data-ttu-id="2014d-188">C:\\FMLab\\EDT\\ を参照します。</span><span class="sxs-lookup"><span data-stu-id="2014d-188">Browse to C:\\FMLab\\EDT\\.</span></span>

    <span data-ttu-id="2014d-189">[![既存の品目を追加](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-189">[![Add existing items](./media/existingitem_datamodel.png)](./media/existingitem_datamodel.png)</span></span>

3. <span data-ttu-id="2014d-190">**Ctrl+A** を押してすべてのファイルを選択し、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-190">Press **Ctrl+A** to select all of the files, and then click **Add**.</span></span>

## <a name="create-the-fmtcustomer-table"></a><span data-ttu-id="2014d-191">FMTCustomer テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="2014d-191">Create the FMTCustomer table</span></span>

1. <span data-ttu-id="2014d-192">**ソリューション エクスプローラー** で、**FMTDataModel** を右クリックしてから **追加 &gt; 新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-192">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Add &gt; New Item**.</span></span>
2. <span data-ttu-id="2014d-193">左ウィンドウで、**インストール済み** を展開し、**Dynamics 365 品目** を展開してから、**データ モデル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-193">In the left pane, expand **Installed**, expand **Dynamics 365 Items** and then click **Data Model**.</span></span>
3. <span data-ttu-id="2014d-194">アーティファクトの一覧で **テーブル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-194">In the list of artifacts, select **Table**.</span></span>
4. <span data-ttu-id="2014d-195">**名前** フィールドに、**FMTCustomer** と入力してから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-195">In the **Name** field, enter **FMTCustomer**, and then click **Add**.</span></span> <span data-ttu-id="2014d-196">テーブル デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="2014d-196">The table designer opens.</span></span>

   <span data-ttu-id="2014d-197">[![データ モデルにテーブルを追加](./media/add_datamodel.png)](./media/add_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-197">[![Add table to data model](./media/add_datamodel.png)](./media/add_datamodel.png)</span></span>

### <a name="add-fields-to-the-fmtcustomer-table"></a><span data-ttu-id="2014d-198">FMTCustomer テーブルへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="2014d-198">Add fields to the FMTCustomer table</span></span>

<span data-ttu-id="2014d-199">FMTCustomer のテーブル デザイナーで、テーブルに複数のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-199">In the table designer for FMTCustomer, you now add several fields to the table.</span></span>

<span data-ttu-id="2014d-200">[![テーブルにフィールドを追加](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-200">[![Add fields to table](./media/addfields_datamodel.png)](./media/addfields_datamodel.png)</span></span>

1. <span data-ttu-id="2014d-201">各フィールドを追加するには、**フィールド** を右クリックし、**新規** をクリックして、タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-201">To add each field, right-click **Fields**, click **New**, and then select a type.</span></span> <span data-ttu-id="2014d-202">各フィールドを追加すると、次の表に示すように、**プロパティ** ウィンドウでフィールド名とその他の特定の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2014d-202">As you add each field, you must specify the field name and certain other values in the **Properties** window, as described in the following table.</span></span>

    | <span data-ttu-id="2014d-203">型</span><span class="sxs-lookup"><span data-stu-id="2014d-203">Type</span></span>       | <span data-ttu-id="2014d-204">フィールド名</span><span class="sxs-lookup"><span data-stu-id="2014d-204">Field name</span></span>     | <span data-ttu-id="2014d-205">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="2014d-205">Property values</span></span>                                                             |
    |------------|----------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="2014d-206">**日付**</span><span class="sxs-lookup"><span data-stu-id="2014d-206">**Date**</span></span>   | <span data-ttu-id="2014d-207">CCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="2014d-207">CCExpiryDate</span></span>   | <span data-ttu-id="2014d-208">拡張データ型 = FMTCCExpiryDate</span><span class="sxs-lookup"><span data-stu-id="2014d-208">Extended Data Type = FMTCCExpiryDate</span></span>                                        |
    | <span data-ttu-id="2014d-209">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-209">**String**</span></span> | <span data-ttu-id="2014d-210">アドレス</span><span class="sxs-lookup"><span data-stu-id="2014d-210">Address</span></span>        | <span data-ttu-id="2014d-211">拡張データ型 = FMTAddressHelp テキスト = アドレス フィールドのヘルプ テキスト。</span><span class="sxs-lookup"><span data-stu-id="2014d-211">Extended Data Type = FMTAddressHelp Text = Help text for the address field.</span></span> |
    | <span data-ttu-id="2014d-212">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-212">**String**</span></span> | <span data-ttu-id="2014d-213">CellPhone</span><span class="sxs-lookup"><span data-stu-id="2014d-213">CellPhone</span></span>      | <span data-ttu-id="2014d-214">拡張データ型 = 電話</span><span class="sxs-lookup"><span data-stu-id="2014d-214">Extended Data Type = Phone</span></span>                                                  |
    | <span data-ttu-id="2014d-215">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-215">**String**</span></span> | <span data-ttu-id="2014d-216">CreditCardNum</span><span class="sxs-lookup"><span data-stu-id="2014d-216">CreditCardNum</span></span>  | <span data-ttu-id="2014d-217">拡張データ型 = FMTCreditCardNum</span><span class="sxs-lookup"><span data-stu-id="2014d-217">Extended Data Type = FMTCreditCardNum</span></span>                                       |
    | <span data-ttu-id="2014d-218">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-218">**String**</span></span> | <span data-ttu-id="2014d-219">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="2014d-219">DriversLicense</span></span> | <span data-ttu-id="2014d-220">拡張データ型 = FMTDriversLicense</span><span class="sxs-lookup"><span data-stu-id="2014d-220">Extended Data Type = FMTDriversLicense</span></span>                                      |
    | <span data-ttu-id="2014d-221">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-221">**String**</span></span> | <span data-ttu-id="2014d-222">電子メール</span><span class="sxs-lookup"><span data-stu-id="2014d-222">Email</span></span>          | <span data-ttu-id="2014d-223">文字列サイズ = 80Label = 電子メール</span><span class="sxs-lookup"><span data-stu-id="2014d-223">String Size = 80Label = Email</span></span>                                               |
    | <span data-ttu-id="2014d-224">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-224">**String**</span></span> | <span data-ttu-id="2014d-225">名</span><span class="sxs-lookup"><span data-stu-id="2014d-225">FirstName</span></span>      | <span data-ttu-id="2014d-226">拡張データ型 = FirstName</span><span class="sxs-lookup"><span data-stu-id="2014d-226">Extended Data Type = FirstName</span></span>                                              |
    | <span data-ttu-id="2014d-227">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-227">**String**</span></span> | <span data-ttu-id="2014d-228">姓</span><span class="sxs-lookup"><span data-stu-id="2014d-228">LastName</span></span>       | <span data-ttu-id="2014d-229">拡張データ型 = LastName</span><span class="sxs-lookup"><span data-stu-id="2014d-229">Extended Data Type = LastName</span></span>                                               |
    | <span data-ttu-id="2014d-230">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-230">**String**</span></span> | <span data-ttu-id="2014d-231">ライセンス</span><span class="sxs-lookup"><span data-stu-id="2014d-231">License</span></span>        | <span data-ttu-id="2014d-232">文字列サイズ = 100Label = ライセンス</span><span class="sxs-lookup"><span data-stu-id="2014d-232">String Size = 100Label = License</span></span>                                            |
    | <span data-ttu-id="2014d-233">**文字列**</span><span class="sxs-lookup"><span data-stu-id="2014d-233">**String**</span></span> | <span data-ttu-id="2014d-234">縮小版</span><span class="sxs-lookup"><span data-stu-id="2014d-234">Thumbnail</span></span>      | <span data-ttu-id="2014d-235">文字列サイズ = 100Label = サムネイル</span><span class="sxs-lookup"><span data-stu-id="2014d-235">String Size = 100Label = Thumbnail</span></span>                                          |

    > [!TIP]
    > <span data-ttu-id="2014d-236">EDT を参照するテーブル内のすべての新しいフィールドでは、**ソリューション エクスプローラー** または **アプリケーション エクスプローラー** から EDT エレメントをドラッグし、デザイナーの **FMTCustomer** テーブルの **フィールド** ノードをドロップするだけで、フィールドを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2014d-236">For all new fields in the table that reference an EDT, you can create the field by simply dragging the EDT element from **Solution Explorer** or **Application Explorer** and dropping it on the **Fields** node of the **FMTCustomer** table in the designer.</span></span>

    <span data-ttu-id="2014d-237">[![データ モデルを使用したソリューション エクスプローラー](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-237">[![Solution Explorer with data model](./media/administratorarrow_datamodel.png)](./media/administratorarrow_datamodel.png)</span></span>

2. <span data-ttu-id="2014d-238">**Ctrl+S** キーを押して、テーブルに新しいフィールドを保存します。</span><span class="sxs-lookup"><span data-stu-id="2014d-238">Press **Ctrl+S** to save the new fields on the table.</span></span>

### <a name="add-fields-to-field-groups"></a><span data-ttu-id="2014d-239">フィールド グループへのフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="2014d-239">Add fields to field groups</span></span>

1. <span data-ttu-id="2014d-240">次の一覧のフィールドを選択して、一部の不フィールドを **AutoSummary** フィールド グループに追加する準備をします。</span><span class="sxs-lookup"><span data-stu-id="2014d-240">Prepare to add some of the fields to the **AutoSummary** field group by selecting the fields in the following list.</span></span> <span data-ttu-id="2014d-241">複数のフィールドを選択するには、Ctrl キーを押しながら各フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-241">To select multiple fields, hold down the Ctrl key while you click each field:</span></span>
    - <span data-ttu-id="2014d-242">**住所**</span><span class="sxs-lookup"><span data-stu-id="2014d-242">**Address**</span></span>
    - <span data-ttu-id="2014d-243">**CCExpiryDate**</span><span class="sxs-lookup"><span data-stu-id="2014d-243">**CCExpiryDate**</span></span>
    - <span data-ttu-id="2014d-244">**CellPhone**</span><span class="sxs-lookup"><span data-stu-id="2014d-244">**CellPhone**</span></span>
    - <span data-ttu-id="2014d-245">**CreditCardNum**</span><span class="sxs-lookup"><span data-stu-id="2014d-245">**CreditCardNum**</span></span>
    - <span data-ttu-id="2014d-246">**DriversLicense**</span><span class="sxs-lookup"><span data-stu-id="2014d-246">**DriversLicense**</span></span>
    - <span data-ttu-id="2014d-247">**電子メール**</span><span class="sxs-lookup"><span data-stu-id="2014d-247">**Email**</span></span>
    - <span data-ttu-id="2014d-248">**名**</span><span class="sxs-lookup"><span data-stu-id="2014d-248">**FirstName**</span></span>
    - <span data-ttu-id="2014d-249">**姓**</span><span class="sxs-lookup"><span data-stu-id="2014d-249">**LastName**</span></span>

2. <span data-ttu-id="2014d-250">**フィールド グループ** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="2014d-250">Expand the **Field Groups** node.</span></span>
3. <span data-ttu-id="2014d-251">選択したフィールドを **AutoSummary** ノードにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="2014d-251">Drag the selected fields to the **AutoSummary** node</span></span>
4. <span data-ttu-id="2014d-252">同じ方法を使用して、**氏名**、**姓**、および **携帯** フィールドを **自動レポート** フィールド グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-252">Use the same technique to add the fields **FirstName**, **LastName**, and **CellPhone** to the **AutoReport** field group.</span></span>
5. <span data-ttu-id="2014d-253">テーブルを保存します。</span><span class="sxs-lookup"><span data-stu-id="2014d-253">Save the table.</span></span>

### <a name="add-a-method"></a><span data-ttu-id="2014d-254">メソッドの追加</span><span class="sxs-lookup"><span data-stu-id="2014d-254">Add a method</span></span>

1. <span data-ttu-id="2014d-255">**Methods** ノードを右クリックし、**New Method** をクリックして、**FMTCustomer** テーブルに **fullName** という名前の X++ メソッドを 追加します。</span><span class="sxs-lookup"><span data-stu-id="2014d-255">Add the X++ method named **fullName** to the **FMTCustomer** table by right-clicking the **Methods** node, and then clicking **New Method**.</span></span>
2. <span data-ttu-id="2014d-256">コード エディターで、既定のメソッドのコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2014d-256">In the code editor, replace the default method code with the following code.</span></span>

    > [!TIP]
    > <span data-ttu-id="2014d-257">「this.」を入力するとき、IntelliSense リストからフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-257">When you type “this.”, choose the field from the IntelliSense list.</span></span>

    ```xpp
    public display FMTName fullName()
    {
        return this.FirstName + ' ' + this.LastName;
    }
    ```

3. <span data-ttu-id="2014d-258">コードを保存します。</span><span class="sxs-lookup"><span data-stu-id="2014d-258">Save the code.</span></span>

## <a name="update-the-fmtaddress-edt"></a><span data-ttu-id="2014d-259">FMTAddress EDT の更新</span><span class="sxs-lookup"><span data-stu-id="2014d-259">Update the FMTAddress EDT</span></span>

1. <span data-ttu-id="2014d-260">**ソリューション エクスプローラー** で **FMTDataModel** プロジェクトを展開します。</span><span class="sxs-lookup"><span data-stu-id="2014d-260">In **Solution Explorer**, expand the **FMTDataModel** project.</span></span>
2. <span data-ttu-id="2014d-261">**FMTAddress** を右クリックしてから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-261">Right-click **FMTAddress**, and then click **Open**.</span></span> <span data-ttu-id="2014d-262">**EDT デザイナー** が開きます。</span><span class="sxs-lookup"><span data-stu-id="2014d-262">The **EDT designer** opens.</span></span>
3. <span data-ttu-id="2014d-263">**EDT デザイナー** で、**FMTAddress** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-263">In the **EDT designer**, select **FMTAddress**.</span></span>
4. <span data-ttu-id="2014d-264">**プロパティ** ウィンドウの **参照テーブル** フィールドで、**FMTCustomer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-264">In the **Properties** window, in the **Reference Table** field, select **FMTCustomer**.</span></span> <span data-ttu-id="2014d-265">**ヒント:** ドロップダウン リストをクリックし、検索ボックスに、接頭語「FMT」を入力します。</span><span class="sxs-lookup"><span data-stu-id="2014d-265">**Tip:** Click the drop-down list, and then type the prefix "FMT" in the search box.</span></span> <span data-ttu-id="2014d-266">これにより、名前に「FMT」が含まれている表のみが表示されるように、ドロップダウン リストがフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="2014d-266">This filters the drop-down list to only show tables that contain "FMT" in their name.</span></span> <span data-ttu-id="2014d-267">フィルター処理されたエントリの一覧から **FMTCustomer** テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-267">Select the **FMTCustomer** table from the list of filtered entries.</span></span>

    <span data-ttu-id="2014d-268">[![プロパティ ウィンドウで FMTAddress EDT を更新する](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span><span class="sxs-lookup"><span data-stu-id="2014d-268">[![Update the FMTAddress EDT in the Properties window](./media/searchfmt_datamodel.png)](./media/searchfmt_datamodel.png)</span></span>

5. <span data-ttu-id="2014d-269">EDT を保存します。</span><span class="sxs-lookup"><span data-stu-id="2014d-269">Save the EDT.</span></span>

## <a name="build-the-fmtdatamodel-project-and-the-fleet-management-tutorial-model"></a><span data-ttu-id="2014d-270">FMTDataModel プロジェクトと フリート管理チュートリアル モデルの構築</span><span class="sxs-lookup"><span data-stu-id="2014d-270">Build the FMTDataModel project and the Fleet Management tutorial model</span></span>

1. <span data-ttu-id="2014d-271">**ソリューション エクスプローラー** で、**FMTDataModel** を右クリックしてから **リビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-271">In **Solution Explorer**, right-click **FMTDataModel**, and then click **Rebuild**.</span></span>
2. <span data-ttu-id="2014d-272">モデル全体の完全なビルドを行うには、**Dynamics 365** メニューで、**モデルをビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-272">To do a full build of the entire model, on the **Dynamics 365** menu, click **Build models**.</span></span>
3. <span data-ttu-id="2014d-273">**フリート管理チュートリアル** 以外のすべてのモデルのチェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="2014d-273">Clear the check box for all models except for **Fleet Management Tutorial**.</span></span>
4. <span data-ttu-id="2014d-274">**オプション** タブで、**推奨チェックの実行** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="2014d-274">On the **Options** tab, select the **Run Best practice checks** check box.</span></span> <span data-ttu-id="2014d-275">使用可能なその他のオプションに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2014d-275">Note that other options available.</span></span>
5. <span data-ttu-id="2014d-276">**モデル** タブで、**ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-276">On the **Models** tab, click **Build**.</span></span>
6. <span data-ttu-id="2014d-277">ダイアログ ボックスで **閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2014d-277">Click **Close**  in the dialog box.</span></span>
7. <span data-ttu-id="2014d-278">**ウィンドウ** メニューで、**すべてのドキュメントを閉じる** をクリックして、開いているすべてのドキュメントを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2014d-278">On the **Window** menu, click **Close All Documents**, to close all open documents.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
