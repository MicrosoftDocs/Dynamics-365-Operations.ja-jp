---
title: カスタム モデルの開発とオンプレミス環境への配置
description: このトピックでは、カスタマイズと拡張機能を開発し、オンプレミス環境に展開するプロセスについて説明します。
author: kfend
manager: AnnBe
ms.date: 06/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 107013
ms.assetid: ''
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8181af97392d58304bc3520fa4d783acc492f567
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368520"
---
# <a name="develop-and-deploy-custom-models-to-on-premises-environments"></a><span data-ttu-id="0aa16-103">カスタム モデルの開発とオンプレミス環境への配置</span><span class="sxs-lookup"><span data-stu-id="0aa16-103">Develop and deploy custom models to on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aa16-104">このトピックでは、カスタマイズと拡張機能を開発してオンプレミス環境に配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-104">This topic describes how to develop customizations and extensions, and deploy them to an on-premises environment.</span></span> <span data-ttu-id="0aa16-105">オンプレミス配置は、ローカル ビジネス データ (LBD) 環境とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-105">On-premises environments are also referred to as local business data (LBD) environments.</span></span> <span data-ttu-id="0aa16-106">。このトピックでは、このプロセスがライタイムのクラウド環境でのプロセスと異なる点について説明します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-106">This topic focuses on the ways that this process differs from the process in a run-time cloud environment.</span></span>

<span data-ttu-id="0aa16-107">このプロセスには、次の主要ステップが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0aa16-107">The process has the following main steps:</span></span>

1. <span data-ttu-id="0aa16-108">開発環境とビルド環境の配置をします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-108">Deploy your development and build environments.</span></span>
2. <span data-ttu-id="0aa16-109">コードとカスタマイズの展開可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-109">Create a deployable package of your code and customizations.</span></span>
3. <span data-ttu-id="0aa16-110">展開可能パッケージを Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-110">Upload the deployable package to your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
4. <span data-ttu-id="0aa16-111">配置可能なパッケージを含むオンプレミスのランタイム環境をコンフィギュレーションし、配置します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-111">Configure and deploy an on-premises runtime environment that includes your deployable package.</span></span> <span data-ttu-id="0aa16-112">この環境は、サンドボックス環境または実稼働環境のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="0aa16-112">This environment can be either a sandbox environment or a production environment.</span></span>

<span data-ttu-id="0aa16-113">次のセクションでは、このプロセスの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-113">The following sections provide more information about this process.</span></span>

## <a name="development-tools-and-platform"></a><span data-ttu-id="0aa16-114">開発ツールおよびプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="0aa16-114">Development tools and platform</span></span>
<span data-ttu-id="0aa16-115">クラウド アプリケーションまたはオンプレミス アプリケーションの開発、拡張、またカスタマイズに関係なく、開発プラットフォーム、ツール、および環境 (仮想マシン [VM]) は同じです。</span><span class="sxs-lookup"><span data-stu-id="0aa16-115">Whether you're developing, extending, or customizing cloud applications or on-premises applications, the development platform, tools, and environments (virtual machines [VMs]) are the same.</span></span> <span data-ttu-id="0aa16-116">ターゲットのランタイム環境がクラウド環境またはオンプレミス環境にあるかどうかに関係なく、カスタム コードは同じ開発用 VM 上で開発されます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-116">Your custom code is developed on the same development VMs, regardless of whether your target runtime environments are in a cloud environment or an on-premises environment.</span></span>

<span data-ttu-id="0aa16-117">開発の詳細については、[開発者ホーム ページ](../dev-tools/developer-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aa16-117">For detailed information about development, see the [Developer home page](../dev-tools/developer-home-page.md).</span></span> <span data-ttu-id="0aa16-118">拡張機能やカスタマイズの詳細については、[拡張機能のホーム ページ](../extensibility/extensibility-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aa16-118">For information about extensibility and customization, see the [Extensibility home page](../extensibility/extensibility-home-page.md).</span></span> <span data-ttu-id="0aa16-119">構築、テスト、および継続的な配信の詳細については、[継続的な配信ホームページ](../dev-tools/continuous-delivery-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aa16-119">For information about building, testing, and continuous delivery, see the [Continuous delivery homepage](../dev-tools/continuous-delivery-home-page.md).</span></span>

## <a name="deploy-development-and-build-environments"></a><span data-ttu-id="0aa16-120">開発環境とビルド環境の配備</span><span class="sxs-lookup"><span data-stu-id="0aa16-120">Deploy development and build environments</span></span>
<span data-ttu-id="0aa16-121">Azure サブスクリプションを使用することにより、オンプレミス LCS プロジェクトを使用し、Microsoft Azure 上にビルドおよび配置環境を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-121">You can use an on-premises LCS project to deploy build and development environments on Microsoft Azure by using your own Azure subscription.</span></span> <span data-ttu-id="0aa16-122">または、ローカル開発用の仮想ハード ディスク (VHD) をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-122">Alternatively, you can download a virtual hard disk (VHD) for local development.</span></span>

<span data-ttu-id="0aa16-123">Azure サブスクリプションに開発環境またはビルド環境を展開する場合、または開発 VHD をダウンロードする場合は、LCS の **クラウド ホスト環境** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-123">To deploy a development or build environment in your Azure subscription, or to download a development VHD, open the **Cloud-hosted environments** page in LCS.</span></span>

<span data-ttu-id="0aa16-124">[![クラウド ホスト環境のメニュー項目](./media/alm-flow-01.png)](./media/alm-flow-01.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-124">[![Cloud-hosted environment menu item](./media/alm-flow-01.png)](./media/alm-flow-01.png)</span></span>

<span data-ttu-id="0aa16-125">次に、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-125">Then follow these steps.</span></span>
    
1. <span data-ttu-id="0aa16-126">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-126">Click **Add**.</span></span> 

    <span data-ttu-id="0aa16-127">[![クラウド ホスト環境のボタンの追加](./media/alm-flow-02.png)](./media/alm-flow-02.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-127">[![Cloud-hosted environment Add button](./media/alm-flow-02.png)](./media/alm-flow-02.png)</span></span>
  
2. <span data-ttu-id="0aa16-128">**Azure** または **ローカル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-128">Select **Azure** or **Locally**.</span></span> <span data-ttu-id="0aa16-129">**ローカル** を選択した場合、開発 VHDを検索し、ダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-129">If you select **Locally**, find and download a development VHD.</span></span> <span data-ttu-id="0aa16-130">**Azure** を選択した場合、次の 3 つのトポロジー、**ビルドおよびテスト**、**デモ**または**開発**から 1 つを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-130">If you select **Azure**, you're prompted to select one of three topologies: **Build and Test**, **Demo**, or **Development**.</span></span>
3. <span data-ttu-id="0aa16-131">配置の手順を完了し、Azure サブスクリプションに VM を配置します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-131">Complete the deployment steps, and deploy a VM in your Azure subscription.</span></span>

<span data-ttu-id="0aa16-132">ローカルの開発 VHD をコンフィギュレーショする方法の詳細については、[アクセス インスタンス](../dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aa16-132">For more information about how to configure a local development VHD, see [Access instances](../dev-tools/access-instances.md#vm-that-is-running-on-premises).</span></span>

> [!NOTE]
> <span data-ttu-id="0aa16-133">独自の Azure サブスクリプションに環境を展開するには、少なくとも 1 つの Azure コネクタを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aa16-133">To deploy environments in your own Azure subscription, you must set up at least one Azure Connector.</span></span> <span data-ttu-id="0aa16-134">Azure コネクタを設定するには、LCS で **プロジェクト設定** ページを開き、**Azure コネクタ** タブをクリックします。 その後、指示に従って Azure コネクタを追加します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-134">To set up an Azure Connector, in LCS, open the **Project settings** page, and then click the **Azure connectors** tab. Then follow the instructions to add an Azure Connector.</span></span> <span data-ttu-id="0aa16-135">手順を完了するには、組織のテナント管理者でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0aa16-135">To complete the steps, you must be the tenant administrator of the organization.</span></span>  
> <span data-ttu-id="0aa16-136">[![プロジェクトの設定のメニュー項目](./media/alm-flow-03.png)](./media/alm-flow-03.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-136">[![Project settings menu item](./media/alm-flow-03.png)](./media/alm-flow-03.png)</span></span>

## <a name="create-and-upload-a-deployable-package-to-the-lcs-asset-library"></a><span data-ttu-id="0aa16-137">展開可能なパッケージを作成して LCS アセット ライブラリにアップロードする</span><span class="sxs-lookup"><span data-stu-id="0aa16-137">Create and upload a deployable package to the LCS Asset library</span></span>
<span data-ttu-id="0aa16-138">開発のフェーズを完了し、サンド ボックスまたは実稼働環境にコードを配置する準備ができたら、モデルからアプリケーション配置可能パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0aa16-138">When you complete a phase of development, and are ready to deploy your code to a sandbox or production on-premises environment, you must create an application deployable package from your models.</span></span> <span data-ttu-id="0aa16-139">このプロセスは、クラウド環境のプロセスと違いはありません。</span><span class="sxs-lookup"><span data-stu-id="0aa16-139">This process doesn't differ from the process for cloud environments.</span></span>

<span data-ttu-id="0aa16-140">自動ビルド (ビルド環境) を使用している場合、ビルド プロセスがアプリケーション配置可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-140">If you're using automated builds (a build environment), the build process creates an application deployable package for you.</span></span> <span data-ttu-id="0aa16-141">また、ユーザーの開発環境で、Microsoft Visual Studio からアプリケーション展開可能パッケージを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-141">You can also create an application deployable package from Microsoft Visual Studio in your development environment.</span></span> <span data-ttu-id="0aa16-142">開発環境で配置可能なパッケージのアプリケーションを作成する方法の詳細については、[配置可能なパッケージの作成と適用](../deployment/create-apply-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0aa16-142">For more information on how to create an application deployable package in your development environment, see [Create and apply a deployable package](../deployment/create-apply-deployable-package.md).</span></span>

<span data-ttu-id="0aa16-143">配置可能なパッケージの準備ができたら、以下の手順に従って、そのパッケージを LCS プロジェクトの資産ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-143">When your deployable package is ready, follow these steps to upload it to your LCS project’s Asset library.</span></span>

1. <span data-ttu-id="0aa16-144">**アセット ライブラリ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-144">Open the **Asset library** page.</span></span>

    <span data-ttu-id="0aa16-145">[![資産ライブラリのメニュー項目](./media/alm-flow-04.png)](./media/alm-flow-04.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-145">[![Asset library menu item](./media/alm-flow-04.png)](./media/alm-flow-04.png)</span></span>

2. <span data-ttu-id="0aa16-146">**ソフトウェア配置可能パッケージ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-146">Click the **Software deployable package** tab.</span></span>

    <span data-ttu-id="0aa16-147">[![ソフトウェア配置可能パッケージ ファイル](./media/alm-flow-05.png)](./media/alm-flow-05.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-147">[![Software deployable package files](./media/alm-flow-05.png)](./media/alm-flow-05.png)</span></span>

3. <span data-ttu-id="0aa16-148">展開可能なパッケージをアップロードするには、プラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-148">Click the plus sign (**+**) to upload the deployable package.</span></span> 

## <a name="configure-an-on-premises-runtime-environment-that-uses-your-code"></a><span data-ttu-id="0aa16-149">コードを使用するオンプレミスのランタイム環境をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="0aa16-149">Configure an on-premises runtime environment that uses your code</span></span>
<span data-ttu-id="0aa16-150">2017 年 7 月リリースの Microsoft Dynamics 365 for Finance and Operations (オンプレミス) では、サンボックスの配置または実稼動環境中にのみカスタマイズや拡張機能を適用できます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-150">As of the July 2017 release of Microsoft Dynamics 365 for Finance and Operations (on-premises), you can apply your customizations and extensions only during the deployment of a sandbox or production environment.</span></span>

1. <span data-ttu-id="0aa16-151">LCS プロジェクトで、**構成**をクリックして環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-151">In your LCS project, click **Configure** to deploy your environment.</span></span>

    <span data-ttu-id="0aa16-152">[![サンドボックス 構成ボタン](./media/alm-flow-06.png)](./media/alm-flow-06.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-152">[![Sandbox Configure button](./media/alm-flow-06.png)](./media/alm-flow-06.png)</span></span>

2. <span data-ttu-id="0aa16-153">配置ツールで、環境名を入力する必要がある場合、**詳細設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-153">In the deployment tool, when you must enter the environment name, click **Advanced settings**.</span></span>

    <span data-ttu-id="0aa16-154">[![オンプレミス トポロジの詳細設定ボタン](./media/alm-flow-07.png)](./media/alm-flow-07.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-154">[![On premise topology Advanced settings button](./media/alm-flow-07.png)](./media/alm-flow-07.png)</span></span>

3. <span data-ttu-id="0aa16-155">**ソリューション資産のカスタマイズ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0aa16-155">Click the **Customize solution assets** tab.</span></span> 

    <span data-ttu-id="0aa16-156">[![配置設定カスタマイズ ソリューション資産タブ](./media/alm-flow-08.png)](./media/alm-flow-08.png)</span><span class="sxs-lookup"><span data-stu-id="0aa16-156">[![Deployment settings Customize solution assets tab](./media/alm-flow-08.png)](./media/alm-flow-08.png)</span></span>

4. <span data-ttu-id="0aa16-157">**展開する AOT パッケージの選択**フィールドで、カスタマイズを含むアプリケーション (AOT) の展開可能パッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-157">In the **Select the AOT packages to be deployed** field, select the application (AOT) deployable package that contains your customizations.</span></span> <span data-ttu-id="0aa16-158">このフィールドには、アセット ライブラリのすべての AOT パッケージがリストされます。</span><span class="sxs-lookup"><span data-stu-id="0aa16-158">This field lists all the AOT packages in your Asset library.</span></span>
5. <span data-ttu-id="0aa16-159">**完了**をクリックして**配置設定**ページを閉じ、環境の展開プロセスを続行します。</span><span class="sxs-lookup"><span data-stu-id="0aa16-159">Click **Done** to close the **Deployment settings** page, and then continue with the environment deployment process.</span></span>
