---
title: C# および X++ ソース コードを使用したビジネス ロジックを記述する
description: このチュートリアルの主な目的は、Microsoft Dynamics AX での C# と X++ 間で相互運用性について説明することです。 このチュートリアルでは、C# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。
author: pvillads
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26821
ms.assetid: 78f3c89c-2035-486d-9fba-35dd3c121d7d
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ca270b12d17c0ed863068b19595506e786acaf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191655"
---
# <a name="write-business-logic-by-using-c-and-x-source-code"></a><span data-ttu-id="d86a7-104">C# および X++ ソース コードを使用したビジネス ロジックを記述する</span><span class="sxs-lookup"><span data-stu-id="d86a7-104">Write business logic by using C# and X++ source code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d86a7-105">このチュートリアルの主な目的は、 C# と X++ 間で相互運用性について説明することです。</span><span class="sxs-lookup"><span data-stu-id="d86a7-105">The primary goal of this tutorial is to illustrate the interoperability between C# and X++.</span></span> <span data-ttu-id="d86a7-106">このチュートリアルでは、C# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-106">In this tutorial, you’ll write business logic in C# source code and in X++ source code.</span></span> 

<span data-ttu-id="d86a7-107">このチュートリアルでは、C\# ソース コードおよび X++ ソース コードでビジネス ロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-107">In this tutorial, you’ll write business logic in C\# source code and in X++ source code.</span></span> <span data-ttu-id="d86a7-108">以下の経験が得られます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-108">You'll get experience with the following:</span></span>

-   <span data-ttu-id="d86a7-109">Visual Studio の新しいツール。</span><span class="sxs-lookup"><span data-stu-id="d86a7-109">New tools in Visual Studio.</span></span>
-   <span data-ttu-id="d86a7-110">C\# でのイベント処理です。</span><span class="sxs-lookup"><span data-stu-id="d86a7-110">The handling of events in C\#.</span></span>
-   <span data-ttu-id="d86a7-111">C\# の言語統合クエリ (LINQ) を使用してデータをフェッチする。</span><span class="sxs-lookup"><span data-stu-id="d86a7-111">The use of Language Integrated Query (LINQ) in C\# to fetch data.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="d86a7-112">前提条件</span><span class="sxs-lookup"><span data-stu-id="d86a7-112">Prerequisite</span></span>
<span data-ttu-id="d86a7-113">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-113">This tutorial requires that you access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="d86a7-114">**注記**: **ソリューション内の項目に対してのみシンボルを読み込む**チェック ボックスがオンになっている場合、\#C プロジェクトのデバッグサポートは機能しません。</span><span class="sxs-lookup"><span data-stu-id="d86a7-114">**Note**: Debugging support for the C\# project does not work if the **Load symbols only for items in the solution** check box is selected.</span></span> <span data-ttu-id="d86a7-115">このオプションが既定で選択されているため、演習を実行する前に変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-115">Since this option is selected by default, it must be changed prior to running the lab.</span></span> <span data-ttu-id="d86a7-116">Visual Studio で、 **Dynamics 365** &gt; **オプション** をクリックし、 **ソリューション内の項目に対してのみシンボルを読み込む** チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-116">In Visual Studio, click **Dynamics 365** &gt; **Options**, and clear the **Load symbols only for items in the solution** check box.</span></span>

## <a name="scenario"></a><span data-ttu-id="d86a7-117">シナリオ</span><span class="sxs-lookup"><span data-stu-id="d86a7-117">Scenario</span></span>
<span data-ttu-id="d86a7-118">危険な運転習慣の経歴を持つ運転手に、余りにも多くの車がレンタルされています。</span><span class="sxs-lookup"><span data-stu-id="d86a7-118">Too many cars have been rented to drivers who have a history of unsafe driving habits.</span></span> <span data-ttu-id="d86a7-119">フリート管理レンタル会社は、外部ソースからドライブ レコードを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-119">The Fleet Management rental company needs to check driving records from external sources.</span></span> <span data-ttu-id="d86a7-120">上級管理職は、運転免許とその関連情報を管理する法人である運輸省 (DOT) が運用するサービスに加入することに決まりました。</span><span class="sxs-lookup"><span data-stu-id="d86a7-120">Upper management has decided to subscribe to a service that is hosted by the Department of Transportation (DOT), which is the legal entity that manages drivers’ licenses and associated information.</span></span> <span data-ttu-id="d86a7-121">このサービスは、指定された一意のライセンス番号の引用数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-121">This service retrieves the number of citations for the given unique license number.</span></span> <span data-ttu-id="d86a7-122">X++ ソース コードから直接外部サービスを呼び出すことは容易ではありません。</span><span class="sxs-lookup"><span data-stu-id="d86a7-122">It’s not easy to call external services directly from X++ source code.</span></span> <span data-ttu-id="d86a7-123">Visual Studio にはサービスを呼び出す「コードビハインド」を (C\# で) 生成するツールがあり、これらのツールにより開発作業が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-123">Visual Studio has tools for generating the “code-behind” (in C\#) that calls the services, and these tools make the development effort easy.</span></span> <span data-ttu-id="d86a7-124">Visual Studio を活用してコードを記述することが当然の選択です。</span><span class="sxs-lookup"><span data-stu-id="d86a7-124">The obvious choice would be to leverage Visual Studio to write the code.</span></span> <span data-ttu-id="d86a7-125">ただし、このチュートリアルでは物流が簡単なラボ環境の範囲を超えているため、コードは実際に外部サービスを呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="d86a7-125">However, in this tutorial your code won’t actually call an external service, because the logistics are beyond the scope of the simple lab environment.</span></span> <span data-ttu-id="d86a7-126">代わりに、サービス コールのモック実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-126">Instead, we provide a mock implementation of a service call.</span></span> <span data-ttu-id="d86a7-127">このチュートリアルの目標は、C\# の現在の状態と X++ との相互運用性の理解について教えることです。</span><span class="sxs-lookup"><span data-stu-id="d86a7-127">The goal of this tutorial is to teach an understanding of the current state of C\# and of interoperability with X++.</span></span>

## <a name="create-a-c-class-library"></a><span data-ttu-id="d86a7-128">C\# クラス ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="d86a7-128">Create a C\# class library</span></span>
<span data-ttu-id="d86a7-129">プロジェクトから、 C\# クラス ライブラリ、またはアセンブリを生成する C\# プロジェクトの別のタイプへの参照を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-129">You can create a reference from a project to the C\# class library, or to any other type of C\# project that generates an assembly.</span></span> <span data-ttu-id="d86a7-130">このような参照は、ビルド順序に影響します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-130">Such references affect the build order.</span></span> <span data-ttu-id="d86a7-131">C\# プロジェクトは、それを参照して依存するプロジェクトより前にビルドされます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-131">The C\# project is built before the project that references and depends on it.</span></span> <span data-ttu-id="d86a7-132">インフラストラクチャは参照を理解し、 C\# アセンブリが実行前にクラウドに正しく配置されるようにします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-132">The infrastructure understands the references, and will make sure that the C\# assemblies are deployed correctly to the cloud before execution.</span></span> <span data-ttu-id="d86a7-133">フリート管理ソリューションで C\# クラス ライブラリを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d86a7-133">Follow these steps to create a C\# class library in the Fleet Management solution:</span></span>

1.  <span data-ttu-id="d86a7-134">Visual Studio で、**ファイル** &gt; **プロジェクト/ソリューションを開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-134">In Visual Studio, click **File** &gt; **Open project/solution**.</span></span>
2.  <span data-ttu-id="d86a7-135">**プロジェクトを開く**ダイアログ ボックスの**ファイル名**テキスト ボックスに次のパスを入力してから **Enter** キーを押します - *C:\\users\\public\\desktop\\FleetManagement*。</span><span class="sxs-lookup"><span data-stu-id="d86a7-135">In the **Open Project** dialog box, in the **File name** text box, type the following path, and then press **Enter** - *C:\\users\\public\\desktop\\FleetManagement*.</span></span>
3.  <span data-ttu-id="d86a7-136">FleetManagement.sln というファイルを選択し、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-136">Select the file named FleetManagement.sln, and then click **Open**.</span></span> <span data-ttu-id="d86a7-137">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。[![OpenProject\_LinqC](./media/openproject_linqc2.png)](./media/openproject_linqc2.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-137">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).[![OpenProject\_LinqC](./media/openproject_linqc2.png)](./media/openproject_linqc2.png)</span></span>
4.  <span data-ttu-id="d86a7-138">**FleetManagement** ソリューションを右クリックし、**追加** &gt; **新しいプロジェクト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-138">Right-click the **FleetManagement** solution, and then click **Add** &gt; **New Project**.</span></span> <span data-ttu-id="d86a7-139">**新しいプロジェクトの追加** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-139">The **Add New Project** dialog is displayed.</span></span>
5.  <span data-ttu-id="d86a7-140">左ウィンドウで、**Visual C\#** をクリックしてから、中央ウィンドウで**クラス ライブラリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-140">In the left pane, click **Visual C\#**, and then in the middle pane, click **Class Library**.</span></span>
6.  <span data-ttu-id="d86a7-141">**名前**テキスト ボックスの下部に **DriversLicenseEvaluator** という名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-141">At the bottom in the **Name** text box, type the name **DriversLicenseEvaluator**.</span></span>
7.  <span data-ttu-id="d86a7-142">**場所**テキスト ボックスに、*C:\\users\\public\\desktop\\FleetManagement* というディレクトリ パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-142">In the **Location** text box, type the following directory path: *C:\\users\\public\\desktop\\FleetManagement*.</span></span>
8.  <span data-ttu-id="d86a7-143">上部にあるドロップダウン リストで、プロジェクトが ".NET Framework 4.5" に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-143">Verify that your project is set to “.NET Framework 4.5” in the drop-down list at the top.</span></span>
9.  <span data-ttu-id="d86a7-144">プロジェクトを作成するには、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-144">Click **OK** to create the project.</span></span> <span data-ttu-id="d86a7-145">[![AddNewProject\_LinqC](./media/addnewproject_linqc2.png)](./media/addnewproject_linqc2.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-145">[![AddNewProject\_LinqC](./media/addnewproject_linqc2.png)](./media/addnewproject_linqc2.png)</span></span>
10. <span data-ttu-id="d86a7-146">**ソリューション エクスプローラー**の DriversLicenseEvaluator プロジェクトで、ファイル名 Class1.cs を右クリックして DriversLicenseChecker.cs に名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-146">In **Solution Explorer**, under the DriversLicenseEvaluator project, right-click the file name Class1.cs and rename it DriversLicenseChecker.cs.</span></span>
11. <span data-ttu-id="d86a7-147">クラスへのすべての参照の名前を変更するか、確認するメッセージが表示されたら、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-147">Click **Yes**, when prompted to rename all references to the class.</span></span> <span data-ttu-id="d86a7-148">[![RenameClass\_LinqC](./media/renameclass_linqc1.png)](./media/renameclass_linqc1.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-148">[![RenameClass\_LinqC](./media/renameclass_linqc1.png)](./media/renameclass_linqc1.png)</span></span>

## <a name="write-a-c-method-named-checkdriverslicense"></a><span data-ttu-id="d86a7-149">CheckDriversLicense という名前で C\# メソッドを記述</span><span class="sxs-lookup"><span data-stu-id="d86a7-149">Write a C\# method named CheckDriversLicense</span></span>
<span data-ttu-id="d86a7-150">このセクションでは、CheckDriversLicense という名前のメソッドの C\# コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-150">In this section, you add C\# code for a method named CheckDriversLicense.</span></span> <span data-ttu-id="d86a7-151">このメソッドでは、運転免許証を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-151">The method must validate the driver’s license.</span></span> <span data-ttu-id="d86a7-152">これを行うには、メソッドは顧客テーブルに格納されている運転免許証番号を取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-152">To do this, the method must retrieve the driver’s license number, which is stored in the customer table.</span></span> <span data-ttu-id="d86a7-153">このメソッドには、メソッドで必要な情報が含まれている顧客レコードの RecId値が与えられます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-153">The method is given the RecId value for the customer record that contains the information required by the method.</span></span> <span data-ttu-id="d86a7-154">C\# コードは、 LINQ プロバイダーを使用して、顧客テーブルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-154">Your C\# code uses the LINQ provider to read from the customer table.</span></span> <span data-ttu-id="d86a7-155">LINQ が作動するためには、最初に LINQ アセンブリを指定している参照を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-155">For LINQ to work, you must first add references pointing to the LINQ assemblies.</span></span> <span data-ttu-id="d86a7-156">これらの参照を DriversLicenseEvaluator という名前の C\# プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-156">You add these references to the C\# project named DriversLicenseEvaluator.</span></span>

1.  <span data-ttu-id="d86a7-157">**ソリューション エクスプローラー**で、DriversLicenseEvaluator プロジェクト ノードを展開し、**参照**を右クリックしてから**参照の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-157">In **Solution Explorer**, expand the DriversLicenseEvaluator project node, right-click **References**, and then click **Add Reference**.</span></span>
2.  <span data-ttu-id="d86a7-158">**参照**をクリックし、次のパスを入力します: C:\\Packages\\bin</span><span class="sxs-lookup"><span data-stu-id="d86a7-158">Click **Browse** and then enter the following path: C:\\Packages\\bin</span></span>
    -   <span data-ttu-id="d86a7-159">*一部の環境では、パッケージ フォルダーの場所はその c: ドライブにはありません。*</span><span class="sxs-lookup"><span data-stu-id="d86a7-159">*In some environments, the location of the packages folder is not on the c: drive.*</span></span>

3.  <span data-ttu-id="d86a7-160">**ファイル名**フィールドに、パターン \*LINQ\*.dll を入力してから **Enter** を押します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-160">In the **File name** field, type the pattern \*LINQ\*.dll and then press **Enter**.</span></span> <span data-ttu-id="d86a7-161">LINQ という名前が入っている、アセンブリの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-161">You'll see a list of assemblies with the name LINQ in them.</span></span> <span data-ttu-id="d86a7-162">その一覧から、次のファイルを選択し、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-162">From that list, select the following files, and then click **Add**:</span></span>
    -   <span data-ttu-id="d86a7-163">Microsoft.Dynamics.AX.Framework.Linq.Data.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-163">Microsoft.Dynamics.AX.Framework.Linq.Data.dll</span></span>
    -   <span data-ttu-id="d86a7-164">Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-164">Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll</span></span>
    -   <span data-ttu-id="d86a7-165">Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-165">Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll</span></span>

    <span data-ttu-id="d86a7-166">[![SelectReferences\_LinqC](./media/selectreferences_linqc1.png)](./media/selectreferences_linqc1.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-166">[![SelectReferences\_LinqC](./media/selectreferences_linqc1.png)](./media/selectreferences_linqc1.png)</span></span>
4.  <span data-ttu-id="d86a7-167">以下のコードで使用する共通タイプを含むサポート アセンブリも追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-167">You must also add the support assemblies that contain the Common type that you'll use in the code below.</span></span> <span data-ttu-id="d86a7-168">**参照**をもう一度クリックし、フィールドに次のファイル名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-168">Click **Browse** again, and then type the following file name into the field:</span></span>
    -   <span data-ttu-id="d86a7-169">Microsoft.Dynamics.AX.Xpp.Support.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-169">Microsoft.Dynamics.AX.Xpp.Support.dll</span></span>
    -   <span data-ttu-id="d86a7-170">Microsoft.Dynamics.AX.Data.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-170">Microsoft.Dynamics.AX.Data.Core.dll</span></span>

5.  <span data-ttu-id="d86a7-171">**追加**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-171">Click **Add**, and then click **OK**.</span></span> <span data-ttu-id="d86a7-172">アセンブリが、プロジェクトの参照ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-172">The assemblies now appear under the references node in the project.</span></span>
6.  <span data-ttu-id="d86a7-173">**参照の追加** プロセスを繰り返します。ただし、今回は以下の DLL ファイルを指定されたパスから追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-173">Repeat the **Add Reference** process, except this time, add the following DLL file from the indicated path:</span></span>
    -   <span data-ttu-id="d86a7-174">C:\\Packages\\FleetManagement\\bin 内の Dynamics.Ax.FleetManagement.dll</span><span class="sxs-lookup"><span data-stu-id="d86a7-174">Dynamics.Ax.FleetManagement.dll, in C:\\Packages\\FleetManagement\\bin</span></span>

7.  <span data-ttu-id="d86a7-175">**ソリューション エクスプローラー**で、Dynamics.Ax.FleetManagement.dll の参照を選択し、プロパティ **Copy Local = False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-175">In **Solution Explorer**, select the reference Dynamics.Ax.FleetManagement.dll reference and set the property **Copy Local = False**.</span></span>
8.  <span data-ttu-id="d86a7-176">**ソリューション エクスプローラー**で、**DriversLicenseChecker.cs** を右クリックしてから、**コードの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-176">In **Solution Explorer**, right-click **DriversLicenseChecker.cs**, and then click **View Code**.</span></span>
9.  <span data-ttu-id="d86a7-177">**DriversLicenseEvaluator** 名前空間に、次の使用する 3 つのステートメントを追加し、外部クラスを参照するコードの冗長性を減らします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-177">Add the following three using statements to the **DriversLicenseEvaluator** namespace, to reduce the verbosity of code that references external classes.</span></span> <span data-ttu-id="d86a7-178">Dynamics.AX.Application の使用。Microsoft.Dynamics.AX.Framework.Linq.Data の使用。Microsoft.Dynamics.AX.Xpp の使用。ユーザーの C\# コードは以下の例のように見えるはずです。</span><span class="sxs-lookup"><span data-stu-id="d86a7-178">using Dynamics.AX.Application; using Microsoft.Dynamics.AX.Framework.Linq.Data; using Microsoft.Dynamics.AX.Xpp; Your C\# code should now look something like the following example.</span></span>

        using System;
        using System.Collections.Generic;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;

        namespace DriversLicenseEvaluator
        {
          using Dynamics.AX.Application;
          using Microsoft.Dynamics.AX.Framework.Linq.Data;
          using Microsoft.Dynamics.Ax.Xpp;

          public class DriversLicenseChecker
          {
          }
        }

10. <span data-ttu-id="d86a7-179">クラス CheckDriversLicense を次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-179">Replace the class CheckDriversLicense with the following code.</span></span> <span data-ttu-id="d86a7-180">**ヒント**: C:\\FMLab ディレクトリ内の DriversLicenseChecker.cs ファイルからコードに貼り付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-180">**Tip**: If you prefer, you can paste in the code from the DriversLicenseChecker.cs file in the C:\\FMLab directory.</span></span>

          public class DriversLicenseChecker
          {
            public static bool CheckDriversLicense(long customerId)
            {
              // Use LINQ to get back to the information about the license number
              FMCustomer customer;
              QueryProvider provider = new AXQueryProvider(null);
              var customers = new QueryCollection<FMCustomer>(provider);

              // Build the query (but do not execute it)
              var query = from c in customers 
                    where c.RecId == customerId 
                    select c;

              // Execute the query:
              customer = query.FirstOrDefault();
              if (customer == null)
              {
                throw new ArgumentException
                  ("The customerId does not designate a customer");
              }

              if (string.IsNullOrEmpty(customer.DriverLicense))
              {
                // No driver's license was recorded. Veto the rental.
                return false;
              }

              // Call the DOT web service to validate the license number.
              // This is not practical for this lab, because all the service providers
              // charge for this service. Instead, just assume that any license number
              // that contains the sequence "89" is valid.
              // In the demo data, this is true for Adrian Lannin,
              // but not for Phil Spencer.
              return customer.DriverLicense.Contains("89");
            }
          }

### <a name="understand-the-linq-code"></a><span data-ttu-id="d86a7-181">LINQ コードを理解する</span><span class="sxs-lookup"><span data-stu-id="d86a7-181">Understand the LINQ code</span></span>

<span data-ttu-id="d86a7-182">さらに C\# コードに進む前に、追加した LINQ コードを理解していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d86a7-182">Before proceeding with more C\# code, verify that you understand the LINQ code you just added.</span></span> <span data-ttu-id="d86a7-183">LINQ の詳細については、[技術概念ガイド](developer-home-page.md)で説明されているため、以下では基本のみを説明します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-183">More details about LINQ are provided in the [Technical Concepts Guide](developer-home-page.md), so only the basics are described below.</span></span>

-   <span data-ttu-id="d86a7-184">最初に、*プロバイダー*を作成します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-184">First, a *provider* is created.</span></span> <span data-ttu-id="d86a7-185">すべてのテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-185">It provides access to all the tables.</span></span>
-   <span data-ttu-id="d86a7-186">次に、すべての顧客の*コレクション*が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-186">Next, a *collection* of all customers is created.</span></span> <span data-ttu-id="d86a7-187">利息のある顧客はこのコレクションから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-187">The customer of interest is retrieved from this collection.</span></span>
-   <span data-ttu-id="d86a7-188">次に、**RecId** によって要求された顧客を指定する where 句で*クエリ*が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-188">Then, a *query* is created with a where clause that designates the requested customer by **RecId**.</span></span>
-   <span data-ttu-id="d86a7-189">FirstOrDefault メソッドを呼び出すと、クエリが強制的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-189">The call to the FirstOrDefault method forces execution of the query.</span></span>
-   <span data-ttu-id="d86a7-190">このメソッドは、一致する単一の顧客を顧客変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-190">The method assigns the single matching customer to the customer variable.</span></span> <span data-ttu-id="d86a7-191">(RecId 値が顧客と一致しない場合は、Null が割り当てられます。)</span><span class="sxs-lookup"><span data-stu-id="d86a7-191">(Null is assigned if the RecId value matches no customer.)</span></span>
-   <span data-ttu-id="d86a7-192">最後に、関連付けられている運転免許証が有効かどうかを確認するため、顧客データをテストします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-192">Finally, the customer data is tested to see if the associated driver's license is valid.</span></span> <span data-ttu-id="d86a7-193">(ライセンスに「89」は含まれていますか。)</span><span class="sxs-lookup"><span data-stu-id="d86a7-193">(Does the license contain "89"?)</span></span>

## <a name="handle-the-event-when-a-record-is-added"></a><span data-ttu-id="d86a7-194">レコードが追加されると、イベントが処理されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-194">Handle the event when a record is added</span></span>
<span data-ttu-id="d86a7-195">次のサブセクションでは、次の項目について説明します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-195">The following subsections provide the following:</span></span>

-   <span data-ttu-id="d86a7-196">次のコード品目および総合関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-196">Explain the upcoming code items and their inter-relationships.</span></span>
-   <span data-ttu-id="d86a7-197">イベント ハンドラーのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-197">Show the code for an event handler.</span></span>
-   <span data-ttu-id="d86a7-198">ハンドラーをイベントの発生に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-198">Associate the handler with the event occurrences.</span></span>

### <a name="preparatory-overview"></a><span data-ttu-id="d86a7-199">準備の概要</span><span class="sxs-lookup"><span data-stu-id="d86a7-199">Preparatory overview</span></span>

<span data-ttu-id="d86a7-200">テーブルにレコードを追加しようとすると、そのレコードがデータベースに書き込まれる前に、OnValidateWrite イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-200">When an attempt is made to add a record to a table, the OnValidateWrite event is raised before the record is written to the database.</span></span> <span data-ttu-id="d86a7-201">FMRental テーブルに対して OnValidateWrite イベントが発生するたびに、CheckDriversLicense メソッドが呼び出されることを必要とします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-201">You want your CheckDriversLicense method to be called each time on the OnValidateWrite event is raised for the FMRental table.</span></span> <span data-ttu-id="d86a7-202">これを行うには、イベントによって呼び出され、checkDriversLicense メソッドを呼び出す C\# メソッドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-202">To do this, you now need to write a C\# method that is invoked by the event, and which calls your checkDriversLicense method.</span></span> <span data-ttu-id="d86a7-203">つまり、CheckDriversLicense メソッドを呼び出すイベント ハンドラーを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-203">In other words, you need to write an event handler that calls your CheckDriversLicense method.</span></span> <span data-ttu-id="d86a7-204">イベント ハンドラー メソッドは、型のパラメーター、DataEventArgsを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-204">The event handler method receives a parameter of the type, DataEventArgs.</span></span> <span data-ttu-id="d86a7-205">イベント ハンドラーは、レコードを承認または拒否するかを DataEventArgs 構造の値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-205">The event handler can set a value in the DataEventArgs structure to accept or reject the record.</span></span> <span data-ttu-id="d86a7-206">イベント ハンドラー メソッドを書き込んだ後は、イベントに割り当てて接続するか、または FMRental テーブルのメンバーである OnValidatedWrite をデリゲートして追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-206">After you write your event handler method, you connect it to the event by assigning, or adding it to the OnValidatedWrite delegate that is a member of the FMRental table.</span></span> <span data-ttu-id="d86a7-207">FMRental フォームのデータ ソースの init メソッドにこの割り当てを記述します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-207">You write this assignment in the init method of the data source of the FMRental form.</span></span> <span data-ttu-id="d86a7-208">デリゲートへのこの割り当ては奇妙に思える場合があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-208">This assignment to a delegate might seem odd.</span></span> <span data-ttu-id="d86a7-209">結局のところ、既存のコード (FMRental) を変更して、ハンドラーを追加します。これはイベントが提供する予定の疎結合の主な価値提案と矛盾しています。</span><span class="sxs-lookup"><span data-stu-id="d86a7-209">After all, we're modifying existing code (FMRental) to add handlers, which contradicts the main value proposition of loose coupling that eventing is supposed to offer.</span></span> <span data-ttu-id="d86a7-210">この割り当てステップは一時的です。</span><span class="sxs-lookup"><span data-stu-id="d86a7-210">This assignment step is temporary.</span></span> <span data-ttu-id="d86a7-211">最終的に、X++ の場合と同じストーリーが C\# でも発生します。属性は、デリゲートとハンドアラーを結合するメカニズムとして、C\# イベント ハンドラーに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-211">We'll eventually have the same story in C\# as we do in X++, where an attribute is applied to the C\# event handler as the mechanism that ties the delegate to the handler.</span></span> <span data-ttu-id="d86a7-212">**注記**: フォームが開かれると、データソースの init メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-212">**Note**: The data source init method is called when the form is opened.</span></span> <span data-ttu-id="d86a7-213">技術的には、init メソッドは FormDataSource クラスから継承されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-213">Technically, the init method is inherited from the FormDataSource class.</span></span>

### <a name="write-an-event-handler-method"></a><span data-ttu-id="d86a7-214">イベント ハンドラー メソッドの記述</span><span class="sxs-lookup"><span data-stu-id="d86a7-214">Write an event handler method</span></span>

<span data-ttu-id="d86a7-215">C\# では、次のイベント ハンドラー メソッドを記述して DriversLicenseChecker クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-215">In C\#, write the following event handler method and add it to the DriversLicenseChecker class.</span></span>

      public static void OnValidatedWriteHandler(Common table, DataEventArgs args)
      {
        var validateEventArgs = args as ValidateEventArgs;

        // Do not check if already rejected.
        if (validateEventArgs.parmValidateResult())
        {
          var rentalTable = table as FMRental;
          if (rentalTable == null)
          {
            throw new ArgumentNullException("table");
          }

          var result = CheckDriversLicense(rentalTable.Customer);
          validateEventArgs.parmValidateResult(result);
        }
      }

<span data-ttu-id="d86a7-216">プロジェクト ノードを右クリックしてから**ビルド**をクリックし、DriversLicenseEvaluator プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-216">Build the DriversLicenseEvaluator project by right-clicking the project node and then clicking **Build**.</span></span>

### <a name="add-a-reference-pointing-to-the-driverslicenseevaluator-project"></a><span data-ttu-id="d86a7-217">DriversLIcenseEvaluator プロジェクトを指定する参照の追加</span><span class="sxs-lookup"><span data-stu-id="d86a7-217">Add a reference pointing to the DriversLIcenseEvaluator project</span></span>

<span data-ttu-id="d86a7-218">次の手順を実行し、**移行されたフリート管理**という名前の X++ プロジェクトから **DriversLicenseEvaluator** という名前の C\# プロジェクトへの参照を作成します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-218">Create a reference from the X++ project named **FleetManagement Migrated** to the C\# project named **DriversLicenseEvaluator**, by completing the following steps.</span></span>

1.  <span data-ttu-id="d86a7-219">FleetManagement Migrated プロジェクトを右クリックし、**追加** をクリックして **参照** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-219">Right-click the FleetManagement Migrated project, click **Add**, and then click **Reference**.</span></span> <span data-ttu-id="d86a7-220">**プロジェクト** 参照タブで DriversLicenseEvaluator プロジェクトの行を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-220">Select the row for the DriversLicenseEvaluator project in the **Projects** references tab, and then click **OK**.</span></span> <span data-ttu-id="d86a7-221">[![AddReference\_LinqC](./media/addreference_linqc1.png)](./media/addreference_linqc1.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-221">[![AddReference\_LinqC](./media/addreference_linqc1.png)](./media/addreference_linqc1.png)</span></span>
2.  <span data-ttu-id="d86a7-222">FleetManagement Migrated プロジェクトで、**References** ノードを展開すると、**DriversLicenseEvaluator** プロジェクトへの新しい参照が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-222">Under the FleetManagement Migrated project, expand the **References** node, and there you see new reference to the **DriversLicenseEvaluator** project.</span></span>

<span data-ttu-id="d86a7-223">[![SolutionExplorerReferences\_LinqC](./media/solutionexplorerreferences_linqc2.png)](./media/solutionexplorerreferences_linqc2.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-223">[![SolutionExplorerReferences\_LinqC](./media/solutionexplorerreferences_linqc2.png)](./media/solutionexplorerreferences_linqc2.png)</span></span> 

#### <a name="build-sequence"></a><span data-ttu-id="d86a7-224">ビルド順序</span><span class="sxs-lookup"><span data-stu-id="d86a7-224">Build sequence</span></span>

<span data-ttu-id="d86a7-225">C\# DriversLicenseEvaluator プロジェクトは、 FleetManagement Migrated プロジェクトのビルド前にビルドされます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-225">Your C\# DriversLicenseEvaluator project will be built before the FleetManagement Migrated project is built.</span></span> <span data-ttu-id="d86a7-226">これは、追加された参照によって、フリート プロジェクトがプロジェクトに依存するためです。</span><span class="sxs-lookup"><span data-stu-id="d86a7-226">This is because the added reference makes the Fleet project dependent on your project.</span></span> <span data-ttu-id="d86a7-227">ビルド シーケンスを簡単に確認するには、FleetManagement ソリューションを右クリックし、 **プロジェクト ビルド順序** をクリックして、 **相互関係** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-227">The build sequence is easy to see if you right-click the FleetManagement solution, click **Project Build Order**, and then click **Dependencies**.</span></span>

<span data-ttu-id="d86a7-228">[![ProjectDependencies1\_LinqC](./media/projectdependencies1_linqc2.png)](./media/projectdependencies1_linqc2.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-228">[![ProjectDependencies1\_LinqC](./media/projectdependencies1_linqc2.png)](./media/projectdependencies1_linqc2.png)</span></span>

<span data-ttu-id="d86a7-229">[![ProjectDependencies2\_LinqC](./media/projectdependencies2_linqc1.png)](./media/projectdependencies2_linqc1.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-229">[![ProjectDependencies2\_LinqC](./media/projectdependencies2_linqc1.png)](./media/projectdependencies2_linqc1.png)</span></span>

### <a name="add-your-event-handler-to-a-delegate"></a><span data-ttu-id="d86a7-230">委任へのイベント ハンドラーの追加</span><span class="sxs-lookup"><span data-stu-id="d86a7-230">Add your event handler to a delegate</span></span>

1.  <span data-ttu-id="d86a7-231">**ソリューション エクスプローラー**で、**移行された FleetManagement &gt; ユーザー インターフェイス &gt; フォーム &gt; FMRental** に進みます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-231">In **Solution Explorer**, navigate to **FleetManagement Migrated &gt; User Interface &gt; Forms &gt; FMRental**.</span></span>
2.  <span data-ttu-id="d86a7-232">**FMRental** フォームをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-232">Double-click the **FMRental** form.</span></span> <span data-ttu-id="d86a7-233">Visual Studio デザイナーは、このフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-233">The Visual Studio designer opens to the form.</span></span>
3.  <span data-ttu-id="d86a7-234">フォームで使われるデータ ソースを表示するには、**データ ソース**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-234">Expand the **Data Sources** node to show the data sources used in the form.</span></span>
4.  <span data-ttu-id="d86a7-235">**FMRental** データ ソースおよび**メソッド**ノードを展開し、データ ソースで定義されたメソッドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-235">Expand the **FMRental** data source, and then the **Methods** node to list the methods defined on the data source.</span></span>
5.  <span data-ttu-id="d86a7-236">**メソッド** を右クリックし、**オーバーライド &gt; メソッド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-236">Right-click **Methods**, and then click **Override &gt; init**.</span></span> <span data-ttu-id="d86a7-237">リストには、まだ上書きされていないデータ ソース上のすべてのメソッドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-237">The list displays all of the methods on the data source that haven't yet been overridden.</span></span> <span data-ttu-id="d86a7-238">**init** を選択すると、**FMRental.xpp** ファイルが X++ コード エディタ内に開き、カーソルが init メソッドのテンプレートの近くに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-238">When you select **init**, this opens the file **FMRental.xpp** in the X++ code editor with the cursor near the template for the init method.</span></span>
6.  <span data-ttu-id="d86a7-239">**初期化**メソッド本体の最後に、+= 演算子を使用してデリゲートに 1 つの割り当てを追加します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-239">At the end of the **init** method body, use the += operator to add one assignment to a delegate.</span></span>

          FMRental.onValidatedWrite += eventhandler
           (DriversLicenseEvaluator.DriversLicenseChecker::OnValidatedWriteHandler);

7.  <span data-ttu-id="d86a7-240">クリックして保存し、ソリューション全体を構築します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-240">Click to save, and then build the entire solution.</span></span>

## <a name="final-test"></a><span data-ttu-id="d86a7-241">最終テスト</span><span class="sxs-lookup"><span data-stu-id="d86a7-241">Final test</span></span>
<span data-ttu-id="d86a7-242">このセクションでは、ブレークポイントを設定し、Visual Studio デバッガーでフリート アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-242">In this section, you set breakpoints and run the Fleet application under the Visual Studio debugger.</span></span> <span data-ttu-id="d86a7-243">これにより、次のことを証明できます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-243">This enables you to prove the following:</span></span>

-   <span data-ttu-id="d86a7-244">LINQ クエリは、OnValidateWrite イベントが発生したときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-244">Your LINQ query runs when the OnValidateWrite event is raised.</span></span>
-   <span data-ttu-id="d86a7-245">LINQ クエリが、顧客のデータの取得に成功します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-245">Your LINQ query successfully retrieves the data for one customer.</span></span>

### <a name="prepare-the-test"></a><span data-ttu-id="d86a7-246">テストの準備</span><span class="sxs-lookup"><span data-stu-id="d86a7-246">Prepare the test</span></span>

1.  <span data-ttu-id="d86a7-247">**ソリューション エクスプローラー**で、**移行された FleetManagement &gt; ユーザー インターフェイス &gt; フォーム**に進みます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-247">In **Solution Explorer**, navigate to **FleetManagement Migrated &gt; User Interface &gt; Forms.**</span></span>
2.  <span data-ttu-id="d86a7-248">**FMRental** を右クリックし、**スタートアップ オブジェクトとして設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-248">Right-click **FMRental**, and then click **Set as Startup Object**.</span></span>
3.  <span data-ttu-id="d86a7-249">DriversLicenseChecker.cs のコード エディターで、OnValidateWriteHandler メソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-249">In the code editor for DriversLicenseChecker.cs, find the OnValidateWriteHandler method.</span></span> <span data-ttu-id="d86a7-250">次のコード行を検索します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-250">Find the following line of code.</span></span>

        var result = CheckDriversLicense(rentalTable.Customer);

4.  <span data-ttu-id="d86a7-251">このコード行にブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-251">Set a breakpoint on that line of code.</span></span> <span data-ttu-id="d86a7-252">その線の左余白をクリックすると、これが行なわれます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-252">You do this by clicking in the left margin at that line.</span></span> <span data-ttu-id="d86a7-253">ブレークポイントが設定されている場合は、赤いドットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-253">A red dot displays when the breakpoint is set.</span></span>
5.  <span data-ttu-id="d86a7-254">CheckDriversLicense メソッドでは、次の行で別のブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-254">In the CheckDriversLicense method, set another breakpoint at the following line.</span></span>

        if (string.IsNullOrEmpty(customer.DriverLicense))

### <a name="run-the-test"></a><span data-ttu-id="d86a7-255">テストの実行</span><span class="sxs-lookup"><span data-stu-id="d86a7-255">Run the test</span></span>

<span data-ttu-id="d86a7-256">このテストでは、書き込んだ C\# コードをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-256">For this test, we'll be debugging the C\# code that we've written.</span></span> <span data-ttu-id="d86a7-257">これを行うには、Visual Studio に C\# コードを含むアセンブリのシンボルを読み込むように通知する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d86a7-257">To do this, we need to inform Visual Studio to load the symbols for the assembly that contains the C\# code.</span></span> <span data-ttu-id="d86a7-258">**Dynamics 365 &gt; オプション &gt; デバッグ** の順に移動し、 **ソリューション内の項目に対してのみシンボルを読み込む** チェック ボックスが選択されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-258">Go to **Dynamics 365 &gt; Options &gt; Debugging** and verify that the **Load symbols only for items in the solution** check box is not selected.</span></span> <span data-ttu-id="d86a7-259">[![Options\_LinqC](./media/options_linqc2.png)](./media/options_linqc2.png) **ヒント**: C\# コードでブレークポイントに到達できない場合、**モジュール**ウィンドウ (**デバッグ&gt;ウィンドウ&gt;モジュール**) で開けて、C\# モジュールを検索し、明示的に読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-259">[![Options\_LinqC](./media/options_linqc2.png)](./media/options_linqc2.png) **Tip**: If you're unable to get to the breakpoint in the C\# code, you may want to open the **Modules** window (**Debug &gt; Windows &gt; Modules**), find the C\# module and load it explicitly.</span></span>

1.  <span data-ttu-id="d86a7-260">**デバッグ &gt; デバッグを開始**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-260">Click **Debug &gt; Start Debugging**.</span></span> <span data-ttu-id="d86a7-261">これにより、フリート アプリケーションが開始され、**FMRental** フォームのブラウザー ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-261">This starts the Fleet application, and a browser window with the **FMRental** form is displayed.</span></span>
2.  <span data-ttu-id="d86a7-262">**車両レンタル ID** をクリックすると詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-262">Click on any **Vehicle rental ID** to view details.</span></span>
3.  <span data-ttu-id="d86a7-263">フォームの左上隅にある**編集**アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-263">Click the **Edit** icon near the top left of the form.</span></span> <span data-ttu-id="d86a7-264">アイコンは鉛筆のように見えます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-264">The icon looks like a pencil.</span></span>
4.  <span data-ttu-id="d86a7-265">**レンタル** セクションの**終了**フィールドで、1 日ごとに日付を増加させます。[![FMRentalDetails](./media/fmrental.jpg)](./media/fmrental.jpg)</span><span class="sxs-lookup"><span data-stu-id="d86a7-265">In the **To** field of the **Rental** section, increase the date by one day.[![FMRentalDetails](./media/fmrental.jpg)](./media/fmrental.jpg)</span></span>
5.  <span data-ttu-id="d86a7-266">**保存**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-266">Click the **Save** button.</span></span> <span data-ttu-id="d86a7-267">これにより、強調表示されたブレークポイントで Visual Studio にフォーカスが移動します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-267">This causes the focus to shift to Visual Studio at your highlighted breakpoint.</span></span> <span data-ttu-id="d86a7-268">この行は、OnValidatedWrite イベントが発生し、ハンドラー メソッド が呼び出されたことを示しています。</span><span class="sxs-lookup"><span data-stu-id="d86a7-268">This line shows that the OnValidatedWrite event was raised, and that your handler method was called.</span></span>
6.  <span data-ttu-id="d86a7-269">**F5** キーを押して実行を続行します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-269">Press **F5** to continue the run.</span></span> <span data-ttu-id="d86a7-270">すぐに、その他のブレークポイントが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="d86a7-270">Instantly, your other breakpoint becomes highlighted.</span></span>
7.  <span data-ttu-id="d86a7-271">ブレークポイントの数行上で、変数の顧客を検索します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-271">Find the variable customer a few lines above your breakpoint.</span></span>
8.  <span data-ttu-id="d86a7-272">顧客変数を右クリックし、**QuickWatch** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d86a7-272">Right-click the customer variable, and then click **QuickWatch**.</span></span> <span data-ttu-id="d86a7-273">長整数値は、LINQ クエリが機能していることを証明します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-273">Any long integer value proves that your LINQ query worked.</span></span> <span data-ttu-id="d86a7-274">[![QuickWatch\_LinqC](./media/quickwatch_linqc2.png)](./media/quickwatch_linqc2.png)</span><span class="sxs-lookup"><span data-stu-id="d86a7-274">[![QuickWatch\_LinqC](./media/quickwatch_linqc2.png)](./media/quickwatch_linqc2.png)</span></span>
9.  <span data-ttu-id="d86a7-275">**F5** キーを押して**保存**操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="d86a7-275">Press **F5** to complete the **Save** operation.</span></span>



