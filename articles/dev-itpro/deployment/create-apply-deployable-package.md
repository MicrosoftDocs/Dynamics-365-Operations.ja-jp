---
title: "モデルの配置可能パッケージを作成する"
description: "このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。"
author: robadawy
manager: AnnBe
ms.date: 10/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 702e7eac1dbbc2aee54f581ebdf24217c867ffe6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="create-deployable-packages-of-models"></a><span data-ttu-id="96b97-103">モデルの配置可能パッケージを作成する</span><span class="sxs-lookup"><span data-stu-id="96b97-103">Create deployable packages of models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96b97-104">AOT パッケージは、Microsoft Dynamics 365 for Finance and Operations 環境または Retail 環境の Microsoft Dynamics 365 に適用できる 1 つまたは複数のモデルの配置およびコンパイル単位です。</span><span class="sxs-lookup"><span data-stu-id="96b97-104">An AOT package is a deployment and compilation unit of one or more models that can be applied to a Microsoft Dynamics 365 for Finance and Operations environment, or a Microsoft Dynamics 365 for Retail environment.</span></span> <span data-ttu-id="96b97-105">これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96b97-105">It includes model metadata, binaries, reports and other associated resources.</span></span> <span data-ttu-id="96b97-106">1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。</span><span class="sxs-lookup"><span data-stu-id="96b97-106">One or more AOT packages can be packaged into a deployable package, which is the vehicle used for deployment of code (and customizations) on demo, sandbox and production environments.</span></span> <span data-ttu-id="96b97-107">この記事では、展開可能なパッケージの作成と適用のプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96b97-107">This article guides you through the process of creating and applying a deployable package.</span></span> 

## <a name="overview-of-the-process"></a><span data-ttu-id="96b97-108">プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="96b97-108">Overview of the process</span></span>

<span data-ttu-id="96b97-109">ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b97-109">In order to deploy your code and customizations to a runtime environment (Demo, Sandbox or Production), you must create deployable packages of your solution or implementation.</span></span> <span data-ttu-id="96b97-110">**Visual Studio 開発ツール**、ビルド環境で有効な**ビルドの自動化プロセス**で配置可能パッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="96b97-110">Deployable packages can be created using the **Visual Studio dev tools**, or by the **build automation process** that are available on build environments.</span></span> <span data-ttu-id="96b97-111">これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="96b97-111">These deployable packages are referred to as Application Deployable Packages or AOT Deployable Packages.</span></span> <span data-ttu-id="96b97-112">以下のイメージはプロセスの概要です。</span><span class="sxs-lookup"><span data-stu-id="96b97-112">The image below is an overview of the process.</span></span> <span data-ttu-id="96b97-113">配置可能パッケージが作成されたら、LCS プロジェクトの資産ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b97-113">Once a deployable package is created, it must be uploaded to the LCS project's asset library.</span></span> <span data-ttu-id="96b97-114">管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用**ツールを使用してランタイム環境にパッケージを適用できます。</span><span class="sxs-lookup"><span data-stu-id="96b97-114">An administrator can then go to the LCS environment page and apply the package to a runtime environment using the **Maintain &gt; Apply updates** tool.</span></span> 

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> <span data-ttu-id="96b97-116">アプリケーション配置可能パッケージにはソース コードが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="96b97-116">Application Deployable Packages do not contain source code.</span></span>

## <a name="create-a-deployable-package"></a><span data-ttu-id="96b97-117">配置可能パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="96b97-117">Create a deployable package</span></span>
<span data-ttu-id="96b97-118">開発ステージを完了すると、以下の手順に従って Visual Studio から配置可能パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="96b97-118">After you have completed the development stage, follow these steps to create a deployable package from Visual Studio.</span></span>

1.  <span data-ttu-id="96b97-119">Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="96b97-119">In Microsoft Visual Studio, select **Dynamics 365** &gt; **Deploy** &gt; **Create Deployment Package**.</span></span>
<span data-ttu-id="96b97-120">![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)</span><span class="sxs-lookup"><span data-stu-id="96b97-120">![Create deployment package](./media/createdeploymentpackage-986x1024.png)</span></span>

2.  <span data-ttu-id="96b97-121">モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="96b97-121">Select the packages that contain your models, and then select a location in which to create the deployable package.</span></span> 
<span data-ttu-id="96b97-122">![場所の選択](./media/pack4.png)</span><span class="sxs-lookup"><span data-stu-id="96b97-122">![Select a location](./media/pack4.png)</span></span>

3.  <span data-ttu-id="96b97-123">配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、LCS プロジェクトで、**資産ライブラリ** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="96b97-123">After a deployable package is created, sign in to Microsoft Dynamics Lifecycle Services (LCS), and then, in your LCS project, click the **Asset Library** tile.</span></span>

4.  <span data-ttu-id="96b97-124">先ほど作成した展開可能なパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="96b97-124">Upload the deployable package that you created earlier.</span></span>

## <a name="apply-a-deployable-package"></a><span data-ttu-id="96b97-125">配置可能パッケージの適用</span><span class="sxs-lookup"><span data-stu-id="96b97-125">Apply a deployable package</span></span>
<span data-ttu-id="96b97-126">展開可能なパッケージを環境に適用する方法については、[[展開可能なパッケージの適用](apply-deployable-package-system.md)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96b97-126">To apply a deployable package to an environment, see the article [Apply a deployable package](apply-deployable-package-system.md).</span></span>

## <a name="remove-a-deployable-package"></a><span data-ttu-id="96b97-127">配置可能パッケージの削除</span><span class="sxs-lookup"><span data-stu-id="96b97-127">Remove a deployable package</span></span>
<span data-ttu-id="96b97-128">環境から配置可能パッケージをアンインストールしたり、削除したりするには、[モジュール (パッケージ) のアンインストール (削除)](uninstall-deployable-package.md)の記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96b97-128">To uninstall or remove a deployable package from an environment, see the article [Uninstall (remove) a module (package)](uninstall-deployable-package.md).</span></span>

