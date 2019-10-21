---
title: モデルの配置可能パッケージを作成する
description: このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。
author: robadawy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ccd4ef3b3d2ba83ef7325687ff2581439f0a035
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174582"
---
# <a name="create-deployable-packages-of-models"></a><span data-ttu-id="d297d-103">モデルの配置可能パッケージを作成する</span><span class="sxs-lookup"><span data-stu-id="d297d-103">Create deployable packages of models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d297d-104">AOT パッケージは、環境に適用することのできる、1 つまたは複数のモデルの配置およびコンパイル単位です。</span><span class="sxs-lookup"><span data-stu-id="d297d-104">An AOT package is a deployment and compilation unit of one or more models that can be applied to an environment.</span></span> <span data-ttu-id="d297d-105">これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d297d-105">It includes model metadata, binaries, reports and other associated resources.</span></span> <span data-ttu-id="d297d-106">1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。</span><span class="sxs-lookup"><span data-stu-id="d297d-106">One or more AOT packages can be packaged into a deployable package, which is the vehicle used for deployment of code (and customizations) on demo, sandbox and production environments.</span></span> <span data-ttu-id="d297d-107">この記事では、展開可能なパッケージの作成と適用のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d297d-107">This article guides you through the process of creating and applying a deployable package.</span></span> 

## <a name="overview-of-the-process"></a><span data-ttu-id="d297d-108">プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="d297d-108">Overview of the process</span></span>

<span data-ttu-id="d297d-109">ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d297d-109">In order to deploy your code and customizations to a runtime environment (Demo, Sandbox or Production), you must create deployable packages of your solution or implementation.</span></span> <span data-ttu-id="d297d-110">**Visual Studio 開発ツール**、またはビルド環境で使用可能な**ビルドの自動化プロセス**を使用して、配置可能パッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d297d-110">Deployable packages can be created using the **Visual Studio dev tools**, or by the **build automation process** that are available on build environments.</span></span> <span data-ttu-id="d297d-111">これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d297d-111">These deployable packages are referred to as Application Deployable Packages or AOT Deployable Packages.</span></span> <span data-ttu-id="d297d-112">以下のイメージはプロセスの概要です。</span><span class="sxs-lookup"><span data-stu-id="d297d-112">The image below is an overview of the process.</span></span> <span data-ttu-id="d297d-113">配置可能パッケージが作成されたら、LCS プロジェクトの資産ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d297d-113">Once a deployable package is created, it must be uploaded to the LCS project's asset library.</span></span> <span data-ttu-id="d297d-114">管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用**ツールを使用してランタイム環境にパッケージを適用できます。</span><span class="sxs-lookup"><span data-stu-id="d297d-114">An administrator can then go to the LCS environment page and apply the package to a runtime environment using the **Maintain &gt; Apply updates** tool.</span></span> 

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> <span data-ttu-id="d297d-116">アプリケーション配置可能パッケージにはソース コードが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d297d-116">Application Deployable Packages do not contain source code.</span></span>

> <span data-ttu-id="d297d-117">本番環境への移行を目的にした配置可能パッケージを作成するには、ビルド環境を使用することを常にお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d297d-117">It is always recommended to use a build environment to create deployable packages that are intended to go to production.</span></span>

## <a name="create-a-deployable-package"></a><span data-ttu-id="d297d-118">配置可能パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="d297d-118">Create a deployable package</span></span>
<span data-ttu-id="d297d-119">配置可能パッケージを作成するにはビルド環境を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d297d-119">We recommend using a build environment to create deployable packages.</span></span> <span data-ttu-id="d297d-120">開発環境で配置可能パッケージを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d297d-120">You can also create a deployable package on a development environment.</span></span> 

<span data-ttu-id="d297d-121">開発環境では、開発とテストを完了した後で、次の手順に従って Visual Studio で配置可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="d297d-121">On a development environment, after you have completed development and testing, follow these steps to create a deployable package in Visual Studio.</span></span>

1.  <span data-ttu-id="d297d-122">Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d297d-122">In Microsoft Visual Studio, select **Dynamics 365** &gt; **Deploy** &gt; **Create Deployment Package**.</span></span>
<span data-ttu-id="d297d-123">![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)</span><span class="sxs-lookup"><span data-stu-id="d297d-123">![Create deployment package](./media/createdeploymentpackage-986x1024.png)</span></span>

2.  <span data-ttu-id="d297d-124">モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="d297d-124">Select the packages that contain your models, and then select a location in which to create the deployable package.</span></span> 
<span data-ttu-id="d297d-125">![場所の選択](./media/pack4.png)</span><span class="sxs-lookup"><span data-stu-id="d297d-125">![Select a location](./media/pack4.png)</span></span>

3.  <span data-ttu-id="d297d-126">配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、LCS プロジェクトで、**資産ライブラリ**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d297d-126">After a deployable package is created, sign in to Microsoft Dynamics Lifecycle Services (LCS), and then, in your LCS project, click the **Asset Library** tile.</span></span>

4.  <span data-ttu-id="d297d-127">先ほど作成した展開可能なパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="d297d-127">Upload the deployable package that you created earlier.</span></span>

## <a name="apply-a-deployable-package"></a><span data-ttu-id="d297d-128">配置可能パッケージの適用</span><span class="sxs-lookup"><span data-stu-id="d297d-128">Apply a deployable package</span></span>
<span data-ttu-id="d297d-129">展開可能なパッケージを環境に適用する方法については、[[展開可能なパッケージの適用](apply-deployable-package-system.md)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d297d-129">To apply a deployable package to an environment, see the article [Apply a deployable package](apply-deployable-package-system.md).</span></span>

## <a name="remove-a-deployable-package"></a><span data-ttu-id="d297d-130">配置可能パッケージの削除</span><span class="sxs-lookup"><span data-stu-id="d297d-130">Remove a deployable package</span></span>
<span data-ttu-id="d297d-131">環境から配置可能パッケージをアンインストールしたり、削除したりするには、[モジュール (パッケージ) のアンインストール (削除)](uninstall-deployable-package.md)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d297d-131">To uninstall or remove a deployable package from an environment, see the article [Uninstall (remove) a module (package)](uninstall-deployable-package.md).</span></span>
