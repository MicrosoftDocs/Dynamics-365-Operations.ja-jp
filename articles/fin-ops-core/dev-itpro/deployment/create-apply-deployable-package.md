---
title: モデルの配置可能パッケージを作成する
description: このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。
author: jorisdg
manager: AnnBe
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d8d5a8ab2461c182e42e0608cc668f82a559fab
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680546"
---
# <a name="create-deployable-packages-of-models"></a><span data-ttu-id="cbaf7-103">モデルの配置可能パッケージを作成する</span><span class="sxs-lookup"><span data-stu-id="cbaf7-103">Create deployable packages of models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbaf7-104">AOT パッケージは、環境に適用することのできる、1 つまたは複数のモデルの配置およびコンパイル単位です。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-104">An AOT package is a deployment and compilation unit of one or more models that can be applied to an environment.</span></span> <span data-ttu-id="cbaf7-105">これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-105">It includes model metadata, binaries, reports and other associated resources.</span></span> <span data-ttu-id="cbaf7-106">1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-106">One or more AOT packages can be packaged into a deployable package, which is the vehicle used for deployment of code (and customizations) on demo, sandbox, and production environments.</span></span> <span data-ttu-id="cbaf7-107">このトピックでは、展開可能なパッケージの作成と適用のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-107">This topic guides you through the process of creating and applying a deployable package.</span></span> 

## <a name="overview-of-the-process"></a><span data-ttu-id="cbaf7-108">プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="cbaf7-108">Overview of the process</span></span>

<span data-ttu-id="cbaf7-109">ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-109">In order to deploy your code and customizations to a runtime environment (demo, sandbox, or production), you must create deployable packages of your solution or implementation.</span></span> <span data-ttu-id="cbaf7-110">**Visual Studio 開発ツール**、またはビルド環境で使用可能な **ビルドの自動化プロセス** を使用して、配置可能パッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-110">Deployable packages can be created by using **Visual Studio dev tools** or by using the **build automation process** that is available on build environments.</span></span> <span data-ttu-id="cbaf7-111">これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-111">These deployable packages are referred to as Application Deployable Packages or AOT Deployable Packages.</span></span> <span data-ttu-id="cbaf7-112">次の図は、プロセスの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-112">The following image shows an overview of the process.</span></span> <span data-ttu-id="cbaf7-113">配置可能パッケージが作成されたら、Lifecycle Services (LCS) プロジェクトの資産ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-113">After a deployable package is created, it must be uploaded to the Lifecycle Services (LCS) project's asset library.</span></span> <span data-ttu-id="cbaf7-114">管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用** ツールを使用してランタイム環境にパッケージを適用できます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-114">An administrator can then go to the LCS environment page and apply the package to a runtime environment using the **Maintain &gt; Apply updates** tool.</span></span> 

> [!NOTE]
> <span data-ttu-id="cbaf7-115">結合した AOT 配置可能パッケージを使用して、Commerce 用カスタム支払コネクタをパッケージ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-115">Custom payment connector for Commerce needs to be packaged using a combined AOT deployable package.</span></span> <span data-ttu-id="cbaf7-116">詳細については、[Service Fabric 配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-116">For more information, see [Create payment packaging for Application Explorer in Service Fabric deployments](../../../commerce/dev-itpro/payment-connector-package.md).</span></span>

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> <span data-ttu-id="cbaf7-118">アプリケーション配置可能パッケージにはソース コードが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-118">Application Deployable Packages do not contain source code.</span></span>

> <span data-ttu-id="cbaf7-119">本番環境への移行を目的にした配置可能パッケージを作成するには、ビルド環境を使用することを常にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-119">It is always recommended to use a build environment to create deployable packages that are intended to go to production.</span></span>

## <a name="create-a-deployable-package"></a><span data-ttu-id="cbaf7-120">配置可能パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="cbaf7-120">Create a deployable package</span></span>
<span data-ttu-id="cbaf7-121">配置可能パッケージを作成するにはビルド環境を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-121">We recommend using a build environment to create deployable packages.</span></span> <span data-ttu-id="cbaf7-122">開発環境で配置可能パッケージを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-122">You can also create a deployable package on a development environment.</span></span> 

<span data-ttu-id="cbaf7-123">開発環境では、開発とテストを完了した後で、次の手順に従って Visual Studio で配置可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-123">On a development environment, after you have completed development and testing, follow these steps to create a deployable package in Visual Studio.</span></span>

1.  <span data-ttu-id="cbaf7-124">Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-124">In Microsoft Visual Studio, select **Dynamics 365** &gt; **Deploy** &gt; **Create Deployment Package**.</span></span>
<span data-ttu-id="cbaf7-125">![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)</span><span class="sxs-lookup"><span data-stu-id="cbaf7-125">![Create deployment package](./media/createdeploymentpackage-986x1024.png)</span></span>

2.  <span data-ttu-id="cbaf7-126">モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-126">Select the packages that contain your models, and then select a location in which to create the deployable package.</span></span> 
<span data-ttu-id="cbaf7-127">![場所の選択](./media/pack4.png)</span><span class="sxs-lookup"><span data-stu-id="cbaf7-127">![Select a location](./media/pack4.png)</span></span>

3.  <span data-ttu-id="cbaf7-128">配置可能パッケージが作成された後、Lifecycle Services にサインインし、LCS プロジェクトで、**資産ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-128">After a deployable package is created, sign in to Lifecycle Services, and then, in your LCS project, click the **Asset Library** tile.</span></span>

4.  <span data-ttu-id="cbaf7-129">先ほど作成した展開可能なパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-129">Upload the deployable package that you created earlier.</span></span>

## <a name="apply-a-deployable-package"></a><span data-ttu-id="cbaf7-130">配置可能パッケージの適用</span><span class="sxs-lookup"><span data-stu-id="cbaf7-130">Apply a deployable package</span></span>
<span data-ttu-id="cbaf7-131">展開可能なパッケージを環境に適用する方法については、[クラウド環境に更新を適用する](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-131">To apply a deployable package to an environment, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

## <a name="remove-a-deployable-package"></a><span data-ttu-id="cbaf7-132">配置可能パッケージの削除</span><span class="sxs-lookup"><span data-stu-id="cbaf7-132">Remove a deployable package</span></span>
<span data-ttu-id="cbaf7-133">環境から配置可能パッケージをアンインストールしたり、削除したりするには、[パッケージ のアンインストール](uninstall-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cbaf7-133">To uninstall or remove a deployable package from an environment, see [Uninstall a package](uninstall-deployable-package.md).</span></span>
