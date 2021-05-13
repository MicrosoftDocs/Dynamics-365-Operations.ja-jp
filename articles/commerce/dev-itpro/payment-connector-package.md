---
title: Finance and Operations 配置用コマース支払パッケージの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の Finance and Operations 配置用に支払コネクタをパッケージ化する方法について説明します。
author: mugunthanm
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 869f7a86991c8befc3cfd3db55d1a96f4b350d75
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5959985"
---
# <a name="create-commerce-payment-packaging-for-finance-and-operations-deployment"></a><span data-ttu-id="e48cf-103">Finance and Operations のデプロイのための Commerce 支払パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="e48cf-103">Create Commerce payment packaging for Finance and Operations deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e48cf-104">このトピックでは、Microsoft Dynamics 365 Commerce の Finance and Operations 配置用に支払コネクタをパッケージ化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-104">This topic explains how to package a payment connector for Finance and Operations deployment in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e48cf-105">10.0.10 より前のリリースでは、コマース ソフトウェア開発キット (SDK) を使用して支払コネクタ パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-105">In releases that are earlier than 10.0.10, you use the Commerce software development kit (SDK) to create a payment connector package.</span></span> <span data-ttu-id="e48cf-106">(以前は Commerce SDK は Retail SDK と呼ばれていました。) 10.0.10 リリース以降では、Visual Studio のみを使用して Application Object Server (AOS) 支払コネクタ パッケージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-106">(The Commerce SDK was previously known as the Retail SDK.) In the 10.0.10 release and later, you can use only Visual Studio to create an Application Object Server (AOS) payment connector package.</span></span> <span data-ttu-id="e48cf-107">この方法を使用して作成したパッケージは、[オールイン ワンパッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md) を使用して、以前の展開とセルフサービス配置の両方に展開できます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-107">Packages that you create by using this approach can be deployed for both earlier deployments and self-service deployments by using [all-in-one packages](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="e48cf-108">10.0.10 以前のリリースでは、単一の支払パッケージを作成し、それをアプリケーション エクスプローラーとコマース チャネルおよびクラウド コンポーネント (Commerce Scale Unit) の両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-108">In releases that are earlier than 10.0.10, you can create a single payment package and use it both for Application Explorer and for the commerce channel and cloud components (Commerce Scale unit).</span></span> <span data-ttu-id="e48cf-109">10.0.10 リリースでは、2 つのパッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e48cf-109">In the 10.0.10 release, you must create two packages.</span></span> <span data-ttu-id="e48cf-110">1 つのパッケージはアプリケーション エクスプローラー用で、Dynamics 365 パッケージング モデルを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-110">One package is for Application Explorer, and you create it by using the Dynamics 365 packaging model.</span></span> <span data-ttu-id="e48cf-111">もう 1 つのパッケージは、コマース チャネルとクラウド コンポーネント用で、コマース SDK を使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-111">The other package is for the commerce channel and cloud components, and you create it by using the Commerce SDK.</span></span> <span data-ttu-id="e48cf-112">コマース SDK を使用してアプリケーション エクスプローラー支払パッケージを作成した以前の方法は、10.0.10 リリースの時点で廃止 (非推奨) となります。</span><span class="sxs-lookup"><span data-stu-id="e48cf-112">The previous approach, where the Commerce SDK is used to create Application Explorer payment packaging, is obsolete (deprecated) as of the 10.0.10 release.</span></span>

<span data-ttu-id="e48cf-113">配置できる支払パッケージを作成するには、次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e48cf-113">To create a payment package that you can deploy, follow the steps in the next section.</span></span>

> [!NOTE]
> <span data-ttu-id="e48cf-114">コマース チャネルとクラウド コンポーネント用パッケージを作成するため、コマース SDK を使用する手順は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="e48cf-114">The steps for using the Commerce SDK to create the package for the commerce channel and cloud components haven't changed.</span></span> <span data-ttu-id="e48cf-115">詳細については、「[コネクタの作成と配置](deploy-payment-connector.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cf-115">For more information, see [Create and deploy connector](deploy-payment-connector.md).</span></span>

## <a name="create-an-aos-payment-package-in-the-10010-release"></a><span data-ttu-id="e48cf-116">10.0.10 リリースでの AOS 支払パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="e48cf-116">Create an AOS payment package in the 10.0.10 release</span></span>

1. <span data-ttu-id="e48cf-117">Visual Studio の、**Dynamics 365** メニューで、**モデル管理 \> モデルの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e48cf-117">In Visual Studio, on the **Dynamics 365** menu, select **Model Management \> Create model**.</span></span>
2. <span data-ttu-id="e48cf-118">モデル名、モデル発行元、およびその他の必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-118">Enter the model name, the model publisher, and other required details.</span></span> <span data-ttu-id="e48cf-119">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-119">Then select **Next**.</span></span>

    <span data-ttu-id="e48cf-120">モデル名には、**RetailPaymentConnectors** の接頭語を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e48cf-120">The model name must be prefixed with (that is, start with) **RetailPaymentConnectors**.</span></span> <span data-ttu-id="e48cf-121">この接頭語の後に、カスタム モデル名に関する情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-121">After this prefix, add information about the custom model name.</span></span> <span data-ttu-id="e48cf-122">たとえば、作成するモデルには **RetailPaymentConnectorsCustomConnector** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-122">For example, the model that you create might be named **RetailPaymentConnectorsCustomConnector**.</span></span> <span data-ttu-id="e48cf-123">**RetailPaymentConnectors** の接頭語で始まるモデル名のみが、コマース支払コネクタ オプションに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-123">Only model names that begin with the **RetailPaymentConnectors** prefix will be loaded in the Commerce payment connector options.</span></span>

    ![モデルの作成ウィザードでのパラメーター ページの追加](./media/CreateModel.png)

3. <span data-ttu-id="e48cf-125">**新しいパッケージの作成** オプションを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-125">Select the **Create new package** option, and then select **Next**.</span></span>
4. <span data-ttu-id="e48cf-126">必要な参照パッケージを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-126">Select the required referenced package, and then select **Next**.</span></span>
5. <span data-ttu-id="e48cf-127">**完了** を選択して、モデルの作成を終了します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-127">Select **Finish** to finish creating the model.</span></span>
6. <span data-ttu-id="e48cf-128">ソリューション エクスプローラーで、プロジェクトを選択し、**参照** を右クリックしてから、**参照の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-128">In Solution Explorer, select the project, right-click **References**, and then select **Add Reference**.</span></span>
7. <span data-ttu-id="e48cf-129">すべての支払コネクタ アセンブリとその依存関係を、プロジェクトに参照として追加します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-129">Add all the payment connector assemblies and their dependencies to the project as references.</span></span>

    ![参照ダイアログ ボックスの追加](./media/Reference.png)
    
[!NOTE]
> <span data-ttu-id="e48cf-131">すべての支払いコネクタ dll は移動可能である必要があります。移動可能および移動不可の支払いコネクタ dll があると、コネクタの読み取り時に問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-131">All payment connector dll’s must be portable, having portable and non-portable payment connector dll’s will cause issues when loading the connector.</span></span>

8. <span data-ttu-id="e48cf-132">拡張機能を実装するのに HTML と CSS ファイルが必要な場合 、それらをリソース ファイルとしてプロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-132">If your extension needs an HTML and CSS file for the implementation, then add them as a resource file to your project.</span></span> <span data-ttu-id="e48cf-133">配置中は、HTML ファイルが AosService\WebRoot\Resources\Html フォルダーにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-133">During deployment, the HTML files will be copied to the AosService\WebRoot\Resources\Html folder.</span></span> <span data-ttu-id="e48cf-134">CSS ファイルは AosService\WebRoot\Resources\Styles フォルダーにコピーされ、次の URL 形式を使用してアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-134">The CSS files will be copied to the AosService\WebRoot\Resources\Styles folder, then accessed with the following URL format.</span></span>

<span data-ttu-id="e48cf-135">例: GetPaymentAcceptPoint の実装は、必要に応じてこの URL を返す更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e48cf-135">Ex: GetPaymentAcceptPoint implementation should be updated to return this URL, if required.</span></span>

```
https://AOSUrl/resources/html/Myhtml.html
https://AOSUrl/resources/styles/Mycss.css
```
> [!NOTE]
> <span data-ttu-id="e48cf-136">リソースとしてプロジェクトに追加された HTML および CSS ファイルは AosService\WebRoot\, にコピーされ、リソースとして追加された他のファイル形式は AosService\WebRoot\. にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="e48cf-136">Only HTML and CSS file formats added as Resources to the project will be copied to the AosService\WebRoot\, other file formats added as Resources will not be copied to AosService\WebRoot\.</span></span> <span data-ttu-id="e48cf-137">AosService\WebRoot\ フォルダーのファイルが必要な場合、HTML ファイル形式に移行するか、またはサポートされていないファイル形式を外部でホストします。</span><span class="sxs-lookup"><span data-stu-id="e48cf-137">If you need the file in AosService\WebRoot\ folder then migrate it to HTML file format or host the non-supported file formats externally.</span></span> <span data-ttu-id="e48cf-138">外部でホストされている場合、カスタマイズまたはパートナーがホスティングを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e48cf-138">IF hosted externally, hosting has to be managed by the custome or partner.</span></span>

9. <span data-ttu-id="e48cf-139">支払コネクタに関連付けられているその他の支払 X++ 拡張機能がない場合、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="e48cf-139">If you don't have any other payment X++ extensions that are related to the payment connector, build the solution.</span></span>

> [!NOTE]
> <span data-ttu-id="e48cf-140">他の拡張機能パッケージが存在しない場合は、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-140">If there are no other extensions package, then continue with these steps.</span></span> <span data-ttu-id="e48cf-141">追加の拡張機能パッケージがある場合は、すべてを 1 つの配置可能なパッケージに結合させます。</span><span class="sxs-lookup"><span data-stu-id="e48cf-141">If you have additional extensions packages, then combine all of them into  all-in-one deployable packages.</span></span> <span data-ttu-id="e48cf-142">これを行わないと、このパッケージは他のパッケージを上書きします。</span><span class="sxs-lookup"><span data-stu-id="e48cf-142">If you do not do this, this package will override other packages.</span></span> <span data-ttu-id="e48cf-143">詳細については、「[オールインワン配置可能パッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cf-143">For more information, see [All-in-one deployable packages](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md).</span></span>

10. <span data-ttu-id="e48cf-144">配備可能なパッケージを作成するには、**Dynamics 365** メニューで、**配置 \> 配置パッケージの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-144">To create the deployable package, on the **Dynamics 365** menu, select **Deploy \> Create Deployment Package**.</span></span>
11. <span data-ttu-id="e48cf-145">以前に作成したモデルを選択し、パッケージ ファイルの場所を指定してから、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-145">Select the model that you created earlier, specify the location of the package file, and then select **Create**.</span></span>


    ![配置パッケージ ダイアログ ボックスの作成](./media/Create.png)

    <span data-ttu-id="e48cf-147">Visual Studio はモデルをビルドし、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-147">Visual Studio builds the model and creates the deployable package.</span></span>

12. <span data-ttu-id="e48cf-148">配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインしてから、LCS プロジェクトで、**資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e48cf-148">After the deployable package has been created, sign in to Microsoft Dynamics Lifecycle Services (LCS), and then, in your LCS project, select the **Asset Library** tile.</span></span>
13. <span data-ttu-id="e48cf-149">作成した展開可能なパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e48cf-149">Upload the deployable package that you created.</span></span>

## <a name="apply-a-deployable-package"></a><span data-ttu-id="e48cf-150">配置可能パッケージの適用</span><span class="sxs-lookup"><span data-stu-id="e48cf-150">Apply a deployable package</span></span>

<span data-ttu-id="e48cf-151">配置可能パッケージの環境への適用方法については、 [クラウド環境への更新プログラムの適用](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cf-151">For information about how to apply a deployable package to an environment, see [Apply updates to cloud environments](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md).</span></span>

## <a name="remove-a-deployable-package"></a><span data-ttu-id="e48cf-152">配置可能パッケージの削除</span><span class="sxs-lookup"><span data-stu-id="e48cf-152">Remove a deployable package</span></span>

<span data-ttu-id="e48cf-153">環境から配置可能パッケージをアンインストールまたは削除する方法についての詳細は、[パッケージのアンインストール](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e48cf-153">For information about how to uninstall or remove a deployable package from an environment, see [Uninstall a package](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
