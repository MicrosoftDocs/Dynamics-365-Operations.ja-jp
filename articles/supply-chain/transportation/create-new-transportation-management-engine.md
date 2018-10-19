---
title: "新しい輸送管理エンジンの作成"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations の新しい輸送管理エンジンを作成する方法について説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSGenericEngine
audience: Developer
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9755a74cf05d6674f065e36dc224599eb1fed91e
ms.openlocfilehash: 745aaac9c69b885d9893a6a4bdb9c6ef33240dae
ms.contentlocale: ja-jp
ms.lasthandoff: 09/13/2018

---

# <a name="create-a-new-transportation-management-engine"></a><span data-ttu-id="e57eb-103">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="e57eb-103">Create a new transportation management engine</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e57eb-104">この記事では、Microsoft Dynamics 365 for Finance and Operations の新しい輸送管理エンジンを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-104">This article describes how to create a new transportation management engine in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="e57eb-105">輸送管理 (TMS) エンジンは、輸送管理で配送率を生成およびプロセスするために使用するロジックを定義します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-105">Transportation management (TMS) engines define the logic that is used to generate and process transportation rates in Transportation management.</span></span> <span data-ttu-id="e57eb-106">Microsoft Dynamics 365 for Finance and Operations には、レート、輸送時間、および輸送中に越えるゾーンの数などのさまざまなパラメーターを計算する複数の異なるエンジン タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-106">Microsoft Dynamics 365 for Finance and Operations provides several different engine types that calculate different parameters, such as rates, transit times, and the number of zones that will be crossed during transit.</span></span> <span data-ttu-id="e57eb-107">この記事では、Microsoft Visual Studio 開発環境と Finance and Operations 開発ツールを使用して新しい TMS エンジンを作成して展開する方法と、次に Operations でエンジンを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-107">This article explains how to use the Microsoft Visual Studio development environment together with Finance and Operations development tools to create and deploy a new TMS engine, and then how to set up the engine in Operations.</span></span> <span data-ttu-id="e57eb-108">Finance and Operations が提供するエンジンの詳細については、[輸送管理エンジン](transportation-management-engines.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e57eb-108">For more information about the engines that Finance and Operations provides, see [Transportation management engines](transportation-management-engines.md).</span></span>

## <a name="create-a-new-tms-engine"></a><span data-ttu-id="e57eb-109">新しい TMS エンジンを作成する</span><span class="sxs-lookup"><span data-stu-id="e57eb-109">Create a new TMS engine</span></span>
<span data-ttu-id="e57eb-110">このセクションでは、TMS エンジン実装を持つクラス ライブラリを作成する方法と、Finance and Operations モデルからクラス ライブラリを参照する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-110">This section explains how to create a class library that has a TMS engine implementation, and how to reference it from a Finance and Operations model.</span></span>

1. <span data-ttu-id="e57eb-111">新しいエンジンを配置するには、エンジンを含む財務および工程のモデルが必要です。新しいエンジンを展開するには、エンジンを含む Finance and Operations モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="e57eb-111">To deploy your new engines, you must have a Finance and Operations model that will contain the engines.</span></span> <span data-ttu-id="e57eb-112">**Dynamics 365**&gt; **モデル管理**メニューで、**モデルの作成**をクリックして、新しいモデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-112">On the **Dynamics 365** &gt; **Model Management** menu, click **Create model** to create a new model.</span></span> <span data-ttu-id="e57eb-113">**モデルの作成**ウィザードの最初のページで、モデル名を **TMSEngines** にします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-113">On the first page of the **Create model** wizard, name the model **TMSEngines**.</span></span> 

   <span data-ttu-id="e57eb-114">[![モデルの作成](./media/012.png)](./media/012.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-114">[![Creating a model](./media/012.png)](./media/012.png)</span></span>

2. <span data-ttu-id="e57eb-115">次のページで、**新しいパッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-115">On the next page, select **Create new package**.</span></span> 

   <span data-ttu-id="e57eb-116">[![新規パッケージの作成](./media/021.png)](./media/021.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-116">[![Creating a new package](./media/021.png)](./media/021.png)</span></span>

3. <span data-ttu-id="e57eb-117">次のページで、参照する **ApplicationSuite** モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-117">On the next page, select the **ApplicationSuite** model to reference.</span></span> <span data-ttu-id="e57eb-118">(**ApplicationPlatform** モデルが事前に選択されています)。</span><span class="sxs-lookup"><span data-stu-id="e57eb-118">(The **ApplicationPlatform** model is preselected.)</span></span> 

   <span data-ttu-id="e57eb-119">[![参照するモデルの選択](./media/032.png)](./media/032.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-119">[![Selecting the model to reference](./media/032.png)](./media/032.png)</span></span>

4. <span data-ttu-id="e57eb-120">次のページで、**完了**をクリックして新しいモデルの作成を確認します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-120">On the next page, click **Finish** to confirm the creation of a new model.</span></span> 

   <span data-ttu-id="e57eb-121">[![モデル作成の完了](./media/042.png)](./media/042.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-121">[![Completing model creation](./media/042.png)](./media/042.png)</span></span>

5. <span data-ttu-id="e57eb-122">新しいソリューションで、新しい Finance and Operations プロジェクトを作成し、**TMSThirdParty** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-122">In a new solution, create a new Finance and Operations project, and name it **TMSThirdParty**.</span></span> <span data-ttu-id="e57eb-123">プロジェクト プロパティで、プロジェクトのモデルを **TMSEngines** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-123">In the project properties, set the project's model to **TMSEngines**.</span></span>
6. <span data-ttu-id="e57eb-124">ソリューションに新しい C\# クラス ライブラリを追加し、**ThirdPartyTMSEngines** という名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-124">Add a new C\# class library to your solution, and name it **ThirdPartyTMSEngines**.</span></span>
7. <span data-ttu-id="e57eb-125">ThirdPartyTMSEngines プロジェクトで、Finance and Operations 固有のアセンブリへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-125">In the ThirdPartyTMSEngines project, add references to Finance and Operations–specific assemblies:</span></span>
   -   <span data-ttu-id="e57eb-126">X++ タイプの参照を有効にするアプリケーション アセンブリ。</span><span class="sxs-lookup"><span data-stu-id="e57eb-126">Application assemblies that enable X++ types to be referenced.</span></span> <span data-ttu-id="e57eb-127">これらのアセンブリは、次の場所にあります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-127">These assemblies can be found in the following locations.</span></span> <span data-ttu-id="e57eb-128">\[パッケージ ルート\] は、C:\\パッケージなど、配置された Dynamics 365 for Finance and Operations アセンブリが配置されている場所のバスです。</span><span class="sxs-lookup"><span data-stu-id="e57eb-128">\[Packages root\] is the path of the location where all the deployed Dynamics 365 for Finance and Operations assemblies are placed, such as C:\\Packages.</span></span>

           [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
           [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
           [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll

   -   <span data-ttu-id="e57eb-129">データ、LINQ、および補助機能へのアクセスを有効にするフレームワーク アセンブリ。</span><span class="sxs-lookup"><span data-stu-id="e57eb-129">Framework assemblies that enable access to data, LINQ, and auxiliary functions.</span></span> <span data-ttu-id="e57eb-130">これらすべてのアセンブリは \[パッケージ ルート\]\\ 在庫置場で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-130">All these assembles can be found in \[Packages root\]\\bin.</span></span>

           Microsoft.Dynamics.ApplicationPlatform.Environment.dll
           Microsoft.Dynamics.AX.Data.Core.dll
           Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
           Microsoft.Dynamics.AX.Framework.Linq.Data.dll
           Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
           Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
           Microsoft.Dynamics.AX.Server.Core.dll
           Microsoft.Dynamics.AX.Xpp.AxShared.dll
           Microsoft.Dynamics.AX.Xpp.Support.dll

   -   <span data-ttu-id="e57eb-131">コア TMS アセンブリ (エンジンを含む) と TMS ベース アセンブリ (ヘルパー、定数、データ転送クラス定義などを含む)</span><span class="sxs-lookup"><span data-stu-id="e57eb-131">The core TMS assembly (which contains engines) and the TMS base assembly (which contains helpers, constants, data transfer class definitions, and so on).</span></span> <span data-ttu-id="e57eb-132">これらのアセンブリは、次の場所にあります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-132">These assemblies can be found in the following locations.</span></span>

           [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
           [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll

8. <span data-ttu-id="e57eb-133">ThirdPartyTMSEngines プロジェクトで生成された C\# クラスの名前を **SampleRatingEngine** に変更します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-133">Rename the C\# class that is automatically generated in the ThirdPartyTMSEngines project to **SampleRatingEngine**.</span></span>
9. <span data-ttu-id="e57eb-134">エンジンを実装します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-134">Implement the engine.</span></span> <span data-ttu-id="e57eb-135">この例ではレート エンジンを作成しているため、レート エンジンの基本クラスを継承しています。</span><span class="sxs-lookup"><span data-stu-id="e57eb-135">Because we are creating a rate engine in this example, we inherit from the base class for rate engines.</span></span> <span data-ttu-id="e57eb-136">基本クラスは、レート エンジン インターフェイス (**TMSFwkIRateEngine**) のほとんどを実装します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-136">The base class implements most of the rate engine interface (**TMSFwkIRateEngine**).</span></span> <span data-ttu-id="e57eb-137">レート法の実装が必要なだけです。</span><span class="sxs-lookup"><span data-stu-id="e57eb-137">We just have to implement the rate method.</span></span> <span data-ttu-id="e57eb-138">この例を単純にするために、このメソッドではハードコーディングされたレートを 100 として登録します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-138">To keep this example simple, we will make this method register a hard-coded rate of 100.</span></span> <span data-ttu-id="e57eb-139">**TMSFwkIAccessorialEngine** などの、任意のエンジン インターフェイスを実装するエンジンを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-139">You can create engines that implement any of the engine interfaces, such as **TMSFwkIAccessorialEngine**.</span></span> <span data-ttu-id="e57eb-140">すべてのエンジン インターフェイスは X++ で定義されます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-140">All the engine interfaces are defined in X++.</span></span>

       namespace ThirdPartyTMSEngines
       {
           using Dynamics.AX.Application;
           using Microsoft.Dynamics.Ax.Tms.Base.Data;
           using Microsoft.Dynamics.Ax.Tms.Base.Utility;
           using Microsoft.Dynamics.Ax.Tms.Bll;
           using System.Xml.Linq;
           public class SampleRatingEngine : BaseRateEngine
           {
               public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
               {
                   XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
                   re.AddRate(TmsRateType.Rate, 100);
                   return this.RatingDto;
               }
           }
       }

10. <span data-ttu-id="e57eb-141">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-141">Build the solution.</span></span>
11. <span data-ttu-id="e57eb-142">TMSThirdParty プロジェクトに新しい参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-142">Add a new reference to the TMSThirdParty project.</span></span> <span data-ttu-id="e57eb-143">参照は、ThirdPartyTMSEngines プロジェクトを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-143">The reference should point to the ThirdPartyTMSEngines project.</span></span> <span data-ttu-id="e57eb-144">完了したら、ソリューションは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-144">When you've finished, your solution should look like this.</span></span> 

    <span data-ttu-id="e57eb-145">[![TMSThirdParty プロジェクトへの参照を含むソリューション](./media/052.png)](./media/052.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-145">[![The solution, which includes a reference to the TMSThirdParty project](./media/052.png)](./media/052.png)</span></span>

12. <span data-ttu-id="e57eb-146">ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-146">Build the solution.</span></span> <span data-ttu-id="e57eb-147">アプリケーション エクスプ ローラーの **参照** ノードに新しいライブラリが表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-147">Verify that the new library appears in the **References** node in Application Explorer.</span></span> 

    <span data-ttu-id="e57eb-148">[![アプリケーション エクスプ ローラーの参照ノード内の新しいライブラリ](./media/061.png)](./media/061.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-148">[![The new library in Application Explorer’s References node](./media/061.png)](./media/061.png)</span></span>

## <a name="deploy-the-tms-engine-as-a-package"></a><span data-ttu-id="e57eb-149">TMS エンジンをパッケージとして配置する</span><span class="sxs-lookup"><span data-stu-id="e57eb-149">Deploy the TMS engine as a package</span></span>
<span data-ttu-id="e57eb-150">サードパーティの TMS エンジンを配置する 1 つの方法は、配置パッケージを介することです。</span><span class="sxs-lookup"><span data-stu-id="e57eb-150">One way to deploy third-party TMS engines is through a deployment package.</span></span> <span data-ttu-id="e57eb-151">実稼働環境では、この方法をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-151">This approach is recommended in a production environment.</span></span> <span data-ttu-id="e57eb-152">開発環境では、次のセクション「Finance and Operations で TMS エンジンを設定する」で説明するように手動でアセンブリをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-152">In a development environment, you can manually copy the assemblies, as described in the next section, "Set up a TMS engine in Finance and Operations."</span></span> <span data-ttu-id="e57eb-153">エンジンをパッケージとして展開するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-153">To deploy the engine as a package, follow these steps.</span></span>

1. <span data-ttu-id="e57eb-154">**Dynamics 365** &gt; **配置** メニューで、<strong>配置パッケージの作成</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-154">On the **Dynamics 365** &gt; **Deploy** menu, click <strong>Create Deployment Package</strong>.</span></span>
2. <span data-ttu-id="e57eb-155">**配置パッケージの作成**ダイアログ ボックスで、TMSEngines モデルを選択し、パッケージ ファイルを格納する場所のパスを入力します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-155">In the **Create Deployment Package** dialog box, select the TMSEngines model, and enter the path where you want to store your package files.</span></span> 

   <span data-ttu-id="e57eb-156">[![TMSEngines モデルの選択](./media/071.png)](./media/071.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-156">[![Selecting the TMSEngines model ](./media/071.png)](./media/071.png)</span></span>

3. <span data-ttu-id="e57eb-157">パッケージをターゲット環境に展開することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e57eb-157">You can now deploy the package to the target environment.</span></span> <span data-ttu-id="e57eb-158">チュートリアルについては、[配置可能パッケージのインストール](../../dev-itpro/deployment/install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e57eb-158">For a tutorial, see [Install a deployable package](../../dev-itpro/deployment/install-deployable-package.md).</span></span>

## <a name="set-up-the-tms-engine-in-finance-and-operations"></a><span data-ttu-id="e57eb-159">Finance and Operations で TMS エンジンを設定</span><span class="sxs-lookup"><span data-stu-id="e57eb-159">Set up the TMS engine in Finance and Operations</span></span>
<span data-ttu-id="e57eb-160">このセクションでは、TMS エンジンを使用するために Finance and Operations を設定する方法と、作成した新しいエンジンをレート ショッピングに使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-160">This section explains how to set up Finance and Operations to use a TMS engine, and shows how the new engine that we have created is used in rate shopping.</span></span> <span data-ttu-id="e57eb-161">このセクションの例では、USMF デモ データ会社を使用しています。</span><span class="sxs-lookup"><span data-stu-id="e57eb-161">The example in this section uses the USMF demo data company.</span></span>

1. <span data-ttu-id="e57eb-162">「新しい TMS エンジンの作成」の説明に従って、新しいエンジンを作成します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-162">Create a new engine as described in the "Create a new TMS engine" section.</span></span>
2. <span data-ttu-id="e57eb-163">ソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-163">Build your solution.</span></span>
3. <span data-ttu-id="e57eb-164">結果のアセンブリを Finance and Operations サーバーのバイナリの場所、\[AOSWebRoot\]bin にコピーします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-164">Copy the resulting assembly into the binary location of the Finance and Operations server, \[AOSWebRoot\]bin.</span></span> <span data-ttu-id="e57eb-165">**注記:** このステップは、開発環境にのみ関連します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-165">**Note:** This step is relevant only in a development environment.</span></span> <span data-ttu-id="e57eb-166">実稼働環境では、配置パッケージを介して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-166">In a production environment, you should deploy through a deployment package.</span></span> <span data-ttu-id="e57eb-167">手順については、前のセクションの「パッケージとして TMS エンジンを配置する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e57eb-167">For instructions, see the previous section, "Deploy the TMS engine as a package."</span></span>
4. <span data-ttu-id="e57eb-168">Finance and Operations では、**レート エンジン** ページで新しい評価エンジンを作成します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-168">In Finance and Operations, on the **Rate engines** page, create a new rating engine.</span></span> <span data-ttu-id="e57eb-169">エンジンは、実装したエンジン クラス ライブラリとエンジン クラスを作成して生成されたエンジン アセンブリを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-169">The engine should point to the engine assembly that is produced by building the engine class library and the engine class that you implemented.</span></span> 

   <span data-ttu-id="e57eb-170">[![レート エンジン ページで新規評価エンジンの作成](./media/081.png)](./media/081.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-170">[![Creating a new rating engine on the Rate engines page](./media/081.png)](./media/081.png)</span></span>

5. <span data-ttu-id="e57eb-171">サンプル レート エンジンを使用する配送業者を作成します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-171">Create a shipping carrier that uses the Sample rate engine.</span></span> <span data-ttu-id="e57eb-172">当社のエンジンは Finance and Operations においていかなるデータも使用しないため、レート マスターを割り当てる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e57eb-172">Because our engine doesn't use any data in Finance and Operations, you don’t have to assign a rate master.</span></span> 

   <span data-ttu-id="e57eb-173">[![新規出荷の配送業者の作成](./media/092.png)](./media/092.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-173">[![Creating a new shipping carrier ](./media/092.png)](./media/092.png)</span></span>

6. <span data-ttu-id="e57eb-174">**工順ワークベンチの評価**ページで、**レート ショップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e57eb-174">On the **Rate route workbench** page, click **Rate shop**.</span></span> <span data-ttu-id="e57eb-175">次のスクリーン ショットに示すように、SampleCarrier から 100.00 のレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-175">You should see a rate of 100.00 from SampleCarrier, as shown in the following screen shot.</span></span> <span data-ttu-id="e57eb-176">この例では、倉庫 24 から顧客 US-004 へのルートの輸送料を検索しています。</span><span class="sxs-lookup"><span data-stu-id="e57eb-176">In this example, we are rate shopping for a route from warehouse 24 to customer US-004.</span></span> <span data-ttu-id="e57eb-177">ただし、料金がハードコーディングされているために、100.00 の料金が常に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-177">However, but because the rate is hard-coded, you will always see a rate of 100.00.</span></span> 

   <span data-ttu-id="e57eb-178">[![工順ワークベンチの評価](./media/101.png)](./media/101.png)</span><span class="sxs-lookup"><span data-stu-id="e57eb-178">[![Rate route workbench](./media/101.png)](./media/101.png)</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="e57eb-179">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="e57eb-179">Tips and tricks</span></span>
-   <span data-ttu-id="e57eb-180">Finance and Operations の開発ツールを使用している場合、ソリューションに新しい Finance and Operations プロジェクトを追加すると便利です。</span><span class="sxs-lookup"><span data-stu-id="e57eb-180">If you’re using development tools for Finance and Operations, it's useful to add a new Finance and Operations project to your solution.</span></span> <span data-ttu-id="e57eb-181">このプロジェクトをスタートアップ プロジェクトとして設定した場合、デバッグ セッションを開始すると、同じデバッグ セッションで X++ と C\# コードの両方のコードをデバッグできます。</span><span class="sxs-lookup"><span data-stu-id="e57eb-181">If you set this project as your startup project and start a debugging session, you can debug both X++ and C\# code in the same debugging session.</span></span>
-   <span data-ttu-id="e57eb-182">ThirdPartyTMSEngines プロジェクトを変更して再コンパイルするたびに、アセンブリの結果を Finance and Operations バイナリの場所に手動でコピーするか、展開パッケージを通じて展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-182">Every time that you change and recompile your ThirdPartyTMSEngines project, you must manually copy the resulting assembly to the Finance and Operations binary location or deploy through a deployment package.</span></span> <span data-ttu-id="e57eb-183">それ以外の場合、古いアセンブリを使用して実行される場合があります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-183">Otherwise, you might run by using a stale assembly.</span></span>
-   <span data-ttu-id="e57eb-184">Finance and Operations で TMS 固有の操作を実行した後、Internet Information Services (IIS) ワーカー プロセスによって ThirdPartyTMSEngines アセンブリが、ロックされアセンブリを更新することができなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="e57eb-184">After you execute TMS-specific operations in Finance and Operations, the Internet Information Services (IIS) worker process might lock the ThirdPartyTMSEngines assembly so that the assembly can’t be updated.</span></span> <span data-ttu-id="e57eb-185">この場合、w3svc プロセスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="e57eb-185">In this case, restart the w3svc process.</span></span>





