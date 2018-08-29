---
title: "現代レポートのデザイン テンプレートのインストール"
description: "このトピックでは、最新のレポート デザイン テンプレートをアプリケーション スイートにインストールする方法について説明します。 これらのサンプルを使用すると、ヘッダーとフッターに柔軟なブランドのあるグラフィックの豊富なビジネス ドキュメントを作成することができます。"
author: tjvass
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PrintMgmtSetupUIMain
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 82783
ms.assetid: 96676acf-a86b-4296-81db-b6ad6b4a46fb
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 3b296d1951e8909f0f55951e8aa9bde68f0308a0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="install-modern-report-design-templates"></a><span data-ttu-id="5a44d-104">現代レポートのデザイン テンプレートのインストール</span><span class="sxs-lookup"><span data-stu-id="5a44d-104">Install modern report design templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a44d-105">このトピックでは、最新のレポート デザイン テンプレートをアプリケーション スイートにインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-105">This topic explains how to install the modern report design templates in the application suite.</span></span> <span data-ttu-id="5a44d-106">これらのサンプルを使用すると、ヘッダーとフッターに柔軟なブランドのあるグラフィックの豊富なビジネス ドキュメントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-106">You can use these samples to create graphically rich business documents that have flexible branding in the header and footer.</span></span>

## <a name="introduction"></a><span data-ttu-id="5a44d-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="5a44d-107">Introduction</span></span>

<span data-ttu-id="5a44d-108">アプリケーション スイートの複数の主要なビジネス ドキュメント用のレポート デザインの形式を取る、新しい一連の開発者ツールを利用できます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-108">A new set of developer tools is available that takes the form of report designs for several core business documents in the application suite.</span></span> <span data-ttu-id="5a44d-109">これらのレポート デザインは、Microsoft Dynamics 365 for Finance and Operations で取引が生成されたときに、一般向けのドキュメントのヘッダーとフッターに柔軟なブランディングが表示されるように再設計されました。</span><span class="sxs-lookup"><span data-stu-id="5a44d-109">These report designs have been re-imagined so that flexible branding appears in the header and footer of public-facing documents when transactions are generated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="5a44d-110">次の図は、売上請求書の初期設計が最新の売上請求書の設計とどのように異なるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="5a44d-110">The following illustration shows how an earlier design for a sales invoice differs from a modern sales invoice design.</span></span>

<span data-ttu-id="5a44d-111">[![初期の売上請求書デザインおよび最新の売上請求書のデザインの例](./media/design-comparison-1024x653.png)](./media/design-comparison.png)</span><span class="sxs-lookup"><span data-stu-id="5a44d-111">[![Examples of an earlier sales invoice design and a modern sales invoice design](./media/design-comparison-1024x653.png)](./media/design-comparison.png)</span></span>

<span data-ttu-id="5a44d-112">インストールの完了後に、組み込みのブランド管理ツールを使用してアプリケーション ビジネス ドキュメントの最新のデザインに適用するブランド設定を定義できます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-112">After you complete the installation, you can use the built-in brand management tools to define brand settings that should be applied to the modern designs for application business documents.</span></span> <span data-ttu-id="5a44d-113">ブランド管理ツールは、**組織管理** &gt; **設定** &gt; **ドキュメント ブランド** &gt; **ブランドの詳細** で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="5a44d-113">The brand management tools are available at **Organization administration** &gt; **Setup** &gt; **Document branding** &gt; **Branding details**.</span></span>

## <a name="why-arent-these-designs-the-default-designs-for-the-application-suite-reports"></a><span data-ttu-id="5a44d-114">これらのデザインがアプリケーション スイート レポートの既定のデザインでないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="5a44d-114">Why aren't these designs the default designs for the application suite reports?</span></span>

<span data-ttu-id="5a44d-115">次の 2 つの主な理由か、Finance and Operations のレガシ ソリューションを維持しています。</span><span class="sxs-lookup"><span data-stu-id="5a44d-115">We are maintaining the legacy solutions for Finance and Operations for two primary reasons:</span></span>

- <span data-ttu-id="5a44d-116">**最新のデザインには、コードが含まれていません。**</span><span class="sxs-lookup"><span data-stu-id="5a44d-116">**Modern designs don't include code.**</span></span> <span data-ttu-id="5a44d-117">レガシ ソリューションはコンフィギュレーション キーを認識し、地域によって異なる規制に関する要件を遵守する埋め込み Microsoft Visual Basic (VB) コードを使用することができますが、最新のレポート デザインでは柔軟性がはるかに少ないです。</span><span class="sxs-lookup"><span data-stu-id="5a44d-117">Although the legacy solutions use embedded Microsoft Visual Basic (VB) code to recognize configuration keys and honor regulatory requirements that vary by region, the modern report designs offer much less flexibility.</span></span> <span data-ttu-id="5a44d-118">最小限のコードが使用されている単純な設計によるメリットはありますが、各地域にわたる再利用性はありません。</span><span class="sxs-lookup"><span data-stu-id="5a44d-118">The benefit of a simple design that has minimal code behind it comes at the expense of reusability across regions.</span></span>
- <span data-ttu-id="5a44d-119">**最新のデザインは、すべてのビジネス ドキュメントで使用できるわけではありません。**</span><span class="sxs-lookup"><span data-stu-id="5a44d-119">**Modern designs aren't available for all business documents.**</span></span> <span data-ttu-id="5a44d-120">サポートされているビジネス ドキュメントと最新のレポート設計の可用性との間にはギャップがあります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-120">There is a gap between the supported business documents and the availability of modern report designs.</span></span> <span data-ttu-id="5a44d-121">レガシ デザインは審美的に満足できるものではありませんが、一貫性のある感覚を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-121">Although the legacy designs aren't as aesthetically pleasing, they provide a sense of consistency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a44d-122">シンプルで現代的なデザインが**推奨されない**展開もあります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-122">The simple modern designs are **not** recommended for all types of deployments.</span></span> <span data-ttu-id="5a44d-123">これは、顧客が実行時に、既存のアプリケーション構成設定を通じてドキュメントのレイアウトを制御する必要がない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-123">They are intended for cases where the customer doesn't require runtime control over the layout of the document through existing application configuration settings.</span></span>

## <a name="apply-the-modern-designs"></a><span data-ttu-id="5a44d-124">最新のデザインを適用</span><span class="sxs-lookup"><span data-stu-id="5a44d-124">Apply the modern designs</span></span>

<span data-ttu-id="5a44d-125">最新のレポート デザインは、モデル ファイルにバンドルされ、Microsoft Dynamics Lifecycle Services (LCS) に転記されました。</span><span class="sxs-lookup"><span data-stu-id="5a44d-125">The modern report designs have been bundled into a model file and posted to Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5a44d-126">したがって、既存のサブスクリプションから簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-126">Therefore, you can easily access them from your existing subscription.</span></span> <span data-ttu-id="5a44d-127">最新のレポート設計ソリューションを取得し、ローカルの開発環境にインストールするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-127">Use the following procedure to obtain the modern report design solutions and install them in your local development environment.</span></span> <span data-ttu-id="5a44d-128">その後、最新のレポート デザインを適切なシナリオに組み込むために、何らかのカスタマイズを適用してください。</span><span class="sxs-lookup"><span data-stu-id="5a44d-128">You must then apply some customizations to incorporate the modern report designs into the appropriate scenarios.</span></span>

<span data-ttu-id="5a44d-129">アプリケーション スイートに最新のレポート デザインをインストールするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5a44d-129">Follow these steps to install the modern report designs for the application suite.</span></span>

1. <span data-ttu-id="5a44d-130">[LCS](https://lcs.dynamics.com/) にサインインして展開ダッシュボードにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5a44d-130">Sign in to [LCS](https://lcs.dynamics.com/) to access the deployment dashboard.</span></span> <span data-ttu-id="5a44d-131">その後、**共有アセット ライブラリ** ページで、**モデル** アセット タイプを選択し、**ApplicationSuiteModernDesigns** モデル ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="5a44d-131">Then, on the **Shared asset library** page, select the **Model** asset type, and download the **ApplicationSuiteModernDesigns** model file.</span></span> <span data-ttu-id="5a44d-132">モデル ファイルを、開発環境からアクセスできる場所に保存します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-132">Save the model file to a location that is accessible from the development environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a44d-133">使用しているアプリケーションのバージョンに適切なモデル ファイルを選択してください。</span><span class="sxs-lookup"><span data-stu-id="5a44d-133">Be sure to select the appropriate model file for the version of the application that you're using.</span></span>

2. <span data-ttu-id="5a44d-134">ローカルの開発環境にモデル ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5a44d-134">Import the model file into your local development environment.</span></span> <span data-ttu-id="5a44d-135">Finance and Operations 開発環境でモデル ファイルをインストールするには、ModelUtil.exe ツールと **-import** ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-135">To install a model file in a Finance and Operations development environment, use the ModelUtil.exe tool and the **-import** directive.</span></span> <span data-ttu-id="5a44d-136">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-136">Here is an example.</span></span>

    ```
    ModelUtil.exe -import -metadatastorepath=[path of the metadata store] -file=[full path of the file to import]
    ```

3. <span data-ttu-id="5a44d-137">**J:\\AOSService\\PackagesLocalDirectory\\bin** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-137">Navigate to the **J:\\AOSService\\PackagesLocalDirectory\\bin** folder.</span></span>
4. <span data-ttu-id="5a44d-138">次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-138">Run the following command.</span></span>

    ```
    ModelUtil.exe -import -metadatastorepath=J:\AOSService\PackagesLocalDirectory -file="E:\Test\AppSuiteModernDesigns.axmodel"
    ```

    <span data-ttu-id="5a44d-139">モデル ファイルをインポートする方法の詳細については、[モデルの配分: モデルをエクスポートおよびインポートする方法](../dev-tools/models-export-import.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a44d-139">For more information about how to import model files, see [Distribution of models: How to export and import a model](../dev-tools/models-export-import.md).</span></span> <span data-ttu-id="5a44d-140">モデル ファイルをインポートした後は、Microsoft Visual Studio 2015 を開始します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-140">After you've imported the model file, start Microsoft Visual Studio 2015.</span></span> <span data-ttu-id="5a44d-141">アプリケーション エクスプローラーで、**アプリケーション スイート - 最新のデザイン** コレクションが **AOT** ノードの下に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-141">In Application Explorer, verify that the **Application Suite - Modern Designs** collection appears under the **AOT** node.</span></span>

<span data-ttu-id="5a44d-142">アプリケーション スイート最新デザイン モデルを正常にインポートしたので、アプリケーション スイートをリビルドしてメタデータ要素を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-142">Now that you've successfully imported the Application Suite Modern Designs model, you must to rebuild the application suite to update the metadata elements.</span></span>

## <a name="build-the-application-suite"></a><span data-ttu-id="5a44d-143">アプリケーション スイートの構築</span><span class="sxs-lookup"><span data-stu-id="5a44d-143">Build the application suite</span></span>

<span data-ttu-id="5a44d-144">Application Suite Modern Designs モデルは、Application Suite モデルの拡張です。</span><span class="sxs-lookup"><span data-stu-id="5a44d-144">The Application Suite Modern Designs model is an extension of the Application Suite model.</span></span> <span data-ttu-id="5a44d-145">すべてのアプリケーション参照がモデル拡張を対象とするように更新されるようにするには、Microsoft Visual Studio を使用してアプリケーション スイート モデルを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-145">To help guarantee that all application references are updated so that they target the model extensions, you must build the Application Suite model by using Microsoft Visual Studio.</span></span>

1. <span data-ttu-id="5a44d-146">Visual Studio 2015 を起動するか、既存のインスタンスを使用します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-146">Start Visual Studio 2015, or use the existing instance.</span></span>
2. <span data-ttu-id="5a44d-147">**Dynamics 365** メニューで、**モデルのビルド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-147">On the **Dynamics 365** menu, select **Build models**.</span></span>
3. <span data-ttu-id="5a44d-148">一覧で、**ApplicationSuite** パッケージのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5a44d-148">In the list, select the check box for the **ApplicationSuite** package.</span></span>

    <span data-ttu-id="5a44d-149">[![Visual Studio 2015 の中の完全なビルド ダイアログ ボックス](./media/BuildAppSuite.png)](./media/BuildAppSuite.png)</span><span class="sxs-lookup"><span data-stu-id="5a44d-149">[![Full build dialog box in Visual Studio 2015](./media/BuildAppSuite.png)](./media/BuildAppSuite.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="5a44d-150">アプリケーション スイート最新デザイン モデルがパッケージ定義に含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-150">You will see that the Application Suite Modern Designs model is included in the package definition.</span></span>

4. <span data-ttu-id="5a44d-151">**ビルド** を選択し、アプリケーション スイートの完全なビルドを実行します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-151">Select **Build** to do a full build of the application suite.</span></span>

<span data-ttu-id="5a44d-152">このプロセスは、マシンの規模によっては最大 20 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-152">This process may take up to 20 minutes, depending on the size of your machine.</span></span>

## <a name="deploy-the-modern-designs-one-box-environments"></a><span data-ttu-id="5a44d-153">最新のデザインを配置する (ワンボックス環境)</span><span class="sxs-lookup"><span data-stu-id="5a44d-153">Deploy the modern designs (one-box environments)</span></span>

<span data-ttu-id="5a44d-154">最新のレポート デザイン テンプレートを含むアプリケーション スイートをコンパイルした後、ローカルで変更を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-154">After you've compiled the application suite that includes the modern report design templates, you should verify the changes locally.</span></span> <span data-ttu-id="5a44d-155">変更を確認するには、ローカルで実行されている Microsoft SQL Server Reporting Services (SSRS) のインスタンスに新しい最新のレポート デザイン ソリューションを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-155">To verify the changes, you must deploy the new modern report design solutions to the instance of Microsoft SQL Server Reporting Services (SSRS) that is running locally.</span></span>

<span data-ttu-id="5a44d-156">最新のレポート デザインを既存のアプリケーション スイート レポートに反映させるには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5a44d-156">Follow these steps to incorporate the modern report design into an existing application suite report.</span></span>

1. <span data-ttu-id="5a44d-157">アプリケーション スイート レポートを含むプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-157">Create a project that contains the application suite report.</span></span> <span data-ttu-id="5a44d-158">アプリケーション エクスプローラーの**アプリケーション スイートの最新のデザイン** モデルで、**レポート** ノードを展開してから**レポート** サブノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-158">In Application Explorer, under the **Application Suite Modern Designs** model, expand the **Reports** node, and then expand the **Reports** subnode.</span></span> <span data-ttu-id="5a44d-159">フォルダーですべての品目を選択して右クリックし、**新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-159">Select all the items in the folder, right-click, and then select **Add to new project**.</span></span>
2. <span data-ttu-id="5a44d-160">**新しいプロジェクト** ウィザードの操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-160">Complete the **New Project** wizard.</span></span> <span data-ttu-id="5a44d-161">すべての既定値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-161">Accept all default values.</span></span>
3. <span data-ttu-id="5a44d-162">ソリューション エクスプローラーで、プロジェクトを選択し、右クリックしてから、**レポートを配置する**を選択してビルドを配置し、ローカルにレポートを配置します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-162">In Solution Explorer, select the project, right-click, and then select **Deploy reports** to deploy the build and deploy the reports locally.</span></span>

<span data-ttu-id="5a44d-163">既存のレポートに最新のレポート デザインを追加するとき、パラメータ処理と、標準のソリューションで使用されるデータ プロバイダーの両方を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-163">When you add the modern report design to an existing report, you can reuse both the parameter handling and the data provider that the out-of-box solution uses.</span></span>

## <a name="update-print-management-settings"></a><span data-ttu-id="5a44d-164">印刷管理の設定を更新</span><span class="sxs-lookup"><span data-stu-id="5a44d-164">Update Print management settings</span></span>

<span data-ttu-id="5a44d-165">この時点で、アプリケーションから最新のレポート デザインにアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-165">At this point, you should be able to access the modern report designs from the application.</span></span> <span data-ttu-id="5a44d-166">実稼働環境に配置する前に、現代レポートのデザイン テンプレートに関するテスト検証を行うことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-166">Make sure that you do thorough test validations on the modern report design templates before you deploy them to production environments.</span></span> <span data-ttu-id="5a44d-167">テスト検証を行うには、アプリケーション ビジネス プロセスの最新のレポート デザインをアクティブにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a44d-167">To do test validations, you must activate the modern report designs for the application business process.</span></span>

<span data-ttu-id="5a44d-168">最新のレポート デザイン ソリューションを既定のレポート デザインとして選択することにより、顧客の販売注文の印刷管理設定を更新するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5a44d-168">Follow these steps to update the Print management settings for customer sales orders by selecting the modern report design solution as the default report design.</span></span>

1. <span data-ttu-id="5a44d-169">モジュールの**フォームの設定**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-169">Open the **Form setup** page for the module.</span></span> <span data-ttu-id="5a44d-170">たとえば、売掛金勘定に対して、**売掛金勘定** &gt; **設定** &gt; **フォーム** &gt; **フォーム設定**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-170">For example, for Accounts receivable, select **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form Setup**.</span></span>
2. <span data-ttu-id="5a44d-171">**印刷管理** を選択して **印刷管理設定** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-171">Select **Print management** to open the **Print management setup** page.</span></span>
3. <span data-ttu-id="5a44d-172">ツリーを展開し、**販売済注文確認書**ドキュメントの設定を見つけます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-172">Expand the tree, and find the settings for the **Sales order confirmation** document.</span></span>
4. <span data-ttu-id="5a44d-173">**元 &lt; 既定 &gt;** を選択し、既定のドキュメントの工順の変更を開始します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-173">Select **Original &lt;Default&gt;** to begin to modify the default document routing.</span></span>
5. <span data-ttu-id="5a44d-174">**レポート形式**リストで、**SalesConfirmModern.Report** を選択して現代レポートのデザイン ソリューションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5a44d-174">In the **Report format** list, select **SalesConfirmModern.Report** to enable the modern report design solution.</span></span>

    <span data-ttu-id="5a44d-175">[![最新のデザインを選択するために使用される印刷管理の設定ページ](./media/UpdatePrintMgtSettings.png)](./media/UpdatePrintMgtSettings.png)</span><span class="sxs-lookup"><span data-stu-id="5a44d-175">[![Print management settings page that is used to select the modern design](./media/UpdatePrintMgtSettings.png)](./media/UpdatePrintMgtSettings.png)</span></span>

6. <span data-ttu-id="5a44d-176">別のページを開きます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-176">Open another page.</span></span> <span data-ttu-id="5a44d-177">このステップでは、保存操作が強制的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a44d-177">This step forces a save operation to occur.</span></span>
7. <span data-ttu-id="5a44d-178">アプリケーションで最新のデザインを表示するために販売注文を転記します。</span><span class="sxs-lookup"><span data-stu-id="5a44d-178">Post a sales order to view the modern design in the application.</span></span>

