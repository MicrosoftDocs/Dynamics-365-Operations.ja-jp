---
title: Service Fabric 配置でアプリケーション エクスプローラーの支払パッケージの作成
description: このトピックでは、アプリケーション エクスプローラーの支払パッケージを作成して、Dynamics 365 Commerce の Microsoft Azure Service Fabric 環境に配置する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a518d3ec50876164adfcbc18dd4dfdf1a18ab282
ms.sourcegitcommit: 1e181db51abbf70bbf1f9af8ad6d8c67bafe5adb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/25/2020
ms.locfileid: "3082099"
---
# <a name="create-payment-packaging-for-application-explorer-in-service-fabric-deployments"></a><span data-ttu-id="400e3-103">Service Fabric 配置でアプリケーション エクスプローラーの支払パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="400e3-103">Create payment packaging for Application Explorer in Service Fabric deployments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="400e3-104">このトピックでは、アプリケーション エクスプローラーの支払パッケージを作成して、Dynamics 365 Commerce の Microsoft Azure Service Fabric 環境に配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="400e3-104">This topic explains how to create payment packaging for Application Explorer and deploy it in Microsoft Azure Service Fabric environments for Dynamics 365 Commerce.</span></span>

<span data-ttu-id="400e3-105">10.0.10 以前のリリースでは、コマース ソフトウェア開発キット (SDK) を使用して支払パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="400e3-105">In releases that are earlier than 10.0.10, you use the Commerce software development kit (SDK) to create payment packaging.</span></span> <span data-ttu-id="400e3-106">(以前は Commerce SDK は Retail SDK と呼ばれていました。) 10.0.10 リリース以降では、Visual Studio のみを使用して Application Object Server (AOS) 支払パッケージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-106">(The Commerce SDK was previously known as the Retail SDK.) In the 10.0.10 release and later, you can use only Visual Studio to create Application Object Server (AOS) payment packaging.</span></span> <span data-ttu-id="400e3-107">この方法を使用して作成するパッケージは、Service Fabric 環境およびサービスとしてのインフラストラクチャ (IaaS) 環境の両方に配置できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-107">Packages that you create by using this approach can be deployed in both Service Fabric environments and infrastructure as a service (IaaS) environments.</span></span>

> [!NOTE]
> <span data-ttu-id="400e3-108">10.0.10 以前のリリースでは、単一の支払パッケージを作成し、それをアプリケーション エクスプローラーとコマース チャネルおよびクラウド コンポーネント (Commerce Scale Unit) の両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="400e3-108">In releases that are earlier than 10.0.10, you can create a single payment package and use it both for Application Explorer and for the commerce channel and cloud components (Commerce Scale unit).</span></span> <span data-ttu-id="400e3-109">10.0.10 リリースでは、2 つのパッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-109">In the 10.0.10 release, you must create two packages.</span></span> <span data-ttu-id="400e3-110">1 つのパッケージはアプリケーション エクスプローラー用で、Dynamics 365 パッケージング モデルを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="400e3-110">One package is for Application Explorer, and you create it by using the Dynamics 365 packaging model.</span></span> <span data-ttu-id="400e3-111">もう 1 つのパッケージは、コマース チャネルとクラウド コンポーネント用で、コマース SDK を使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="400e3-111">The other package is for the commerce channel and cloud components, and you create it by using the Commerce SDK.</span></span> <span data-ttu-id="400e3-112">コマース SDK を使用してアプリケーション エクスプローラー支払パッケージを作成した以前の方法は、10.0.10 リリースの時点で廃止 (非推奨) となります。</span><span class="sxs-lookup"><span data-stu-id="400e3-112">The previous approach, where the Commerce SDK is used to create Application Explorer payment packaging, is obsolete (deprecated) as of the 10.0.10 release.</span></span>

<span data-ttu-id="400e3-113">Commerce Service Fabric 配置で配置できる支払パッケージを作成するには、次のセクションの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="400e3-113">To create a payment package that you can deploy in Commerce Service Fabric deployments, follow the steps in the next section.</span></span>

> [!NOTE]
> <span data-ttu-id="400e3-114">コマース チャネルとクラウド コンポーネント用パッケージを作成するため、コマース SDK を使用する手順は変更されていません。</span><span class="sxs-lookup"><span data-stu-id="400e3-114">The steps for using the Commerce SDK to create the package for the commerce channel and cloud components haven't changed.</span></span> <span data-ttu-id="400e3-115">詳細については、「[コネクタの作成と配置](deploy-payment-connector.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="400e3-115">For more information, see [Create and deploy connector](deploy-payment-connector.md).</span></span>

## <a name="create-an-aos-payment-package-in-the-10010-release"></a><span data-ttu-id="400e3-116">10.0.10 リリースでの AOS 支払パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="400e3-116">Create an AOS payment package in the 10.0.10 release</span></span>

1. <span data-ttu-id="400e3-117">Visual Studio の、**Dynamics 365** メニューで、**モデル管理 \> モデルの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="400e3-117">In Visual Studio, on the **Dynamics 365** menu, select **Model Management \> Create model**.</span></span>
2. <span data-ttu-id="400e3-118">モデル名、モデル発行元、およびその他の必要な詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="400e3-118">Enter the model name, the model publisher, and other required details.</span></span> <span data-ttu-id="400e3-119">その後、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-119">Then select **Next**.</span></span>

    <span data-ttu-id="400e3-120">モデル名には、**RetailPaymentConnectors** の接頭語を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="400e3-120">The model name must be prefixed with (that is, start with) **RetailPaymentConnectors**.</span></span> <span data-ttu-id="400e3-121">この接頭語の後に、カスタム モデル名に関する情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="400e3-121">After this prefix, add information about the custom model name.</span></span> <span data-ttu-id="400e3-122">たとえば、作成するモデルには **RetailPaymentConnectorsCustomConnector** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="400e3-122">For example, the model that you create might be named **RetailPaymentConnectorsCustomConnector**.</span></span> <span data-ttu-id="400e3-123">**RetailPaymentConnectors** の接頭語で始まるモデル名のみが、コマース支払コネクタ オプションに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="400e3-123">Only model names that begin with the **RetailPaymentConnectors** prefix will be loaded in the Commerce payment connector options.</span></span>

    ![モデルの作成ウィザードでのパラメーター ページの追加](./media/CreateModel.png)

3. <span data-ttu-id="400e3-125">**新しいパッケージの作成**オプションを選択し、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-125">Select the **Create new package** option, and then select **Next**.</span></span>
4. <span data-ttu-id="400e3-126">必要な参照パッケージを選択し、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-126">Select the required referenced package, and then select **Next**.</span></span>
5. <span data-ttu-id="400e3-127">**完了**を選択して、モデルの作成を終了します。</span><span class="sxs-lookup"><span data-stu-id="400e3-127">Select **Finish** to finish creating the model.</span></span>
6. <span data-ttu-id="400e3-128">ソリューション エクスプローラーで、プロジェクトを選択し、**参照**を右クリックしてから、**参照の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-128">In Solution Explorer, select the project, right-click **References**, and then select **Add Reference**.</span></span>
7. <span data-ttu-id="400e3-129">すべての支払コネクタ アセンブリとその依存関係を、プロジェクトに参照として追加します。</span><span class="sxs-lookup"><span data-stu-id="400e3-129">Add all the payment connector assemblies and their dependencies to the project as references.</span></span>

    ![参照ダイアログ ボックスの追加](./media/Reference.png)

8. <span data-ttu-id="400e3-131">支払コネクタに関連付けられているその他の支払 X++ 拡張機能がない場合、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="400e3-131">If you don't have any other payment X++ extensions that are related to the payment connector, build the solution.</span></span>
9. <span data-ttu-id="400e3-132">配備可能なパッケージを作成するには、**Dynamics 365** メニューで、**配置 \> 配置パッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-132">To create the deployable package, on the **Dynamics 365** menu, select **Deploy \> Create Deployment Package**.</span></span>
10. <span data-ttu-id="400e3-133">以前に作成したモデルを選択し、パッケージ ファイルの場所を指定してから、**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-133">Select the model that you created earlier, specify the location of the package file, and then select **Create**.</span></span>

    ![配置パッケージ ダイアログ ボックスの作成](./media/Create.png)

    <span data-ttu-id="400e3-135">Visual Studio はモデルをビルドし、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="400e3-135">Visual Studio builds the model and creates the deployable package.</span></span>

10. <span data-ttu-id="400e3-136">配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインしてから、LCS プロジェクトで、**資産ライブラリ** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="400e3-136">After the deployable package has been created, sign in to Microsoft Dynamics Lifecycle Services (LCS), and then, in your LCS project, select the **Asset Library** tile.</span></span>
11. <span data-ttu-id="400e3-137">作成した展開可能なパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="400e3-137">Upload the deployable package that you created.</span></span>

## <a name="apply-a-deployable-package"></a><span data-ttu-id="400e3-138">配置可能パッケージの適用</span><span class="sxs-lookup"><span data-stu-id="400e3-138">Apply a deployable package</span></span>

<span data-ttu-id="400e3-139">配置可能パッケージの環境への適用方法については、 [クラウド環境への更新プログラムの適用](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="400e3-139">For information about how to apply a deployable package to an environment, see [Apply updates to cloud environments](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md).</span></span>

## <a name="remove-a-deployable-package"></a><span data-ttu-id="400e3-140">配置可能パッケージの削除</span><span class="sxs-lookup"><span data-stu-id="400e3-140">Remove a deployable package</span></span>

<span data-ttu-id="400e3-141">環境から配置可能パッケージをアンインストールまたは削除する方法についての詳細は、[パッケージのアンインストール](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="400e3-141">For information about how to uninstall or remove a deployable package from an environment, see [Uninstall a package](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md).</span></span>
