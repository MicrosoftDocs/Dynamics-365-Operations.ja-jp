---
title: Visual Studio 開発ツールの更新
description: このトピックでは、開発ツールを更新する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 33571
ms.assetid: bd24d864-6915-4d17-9ebb-d1619b7d4311
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0dbe4329ad97c4812c85cc15c06eab632fc9f895
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544125"
---
# <a name="update-the-visual-studio-development-tools"></a><span data-ttu-id="657e9-103">Visual Studio 開発ツールの更新</span><span class="sxs-lookup"><span data-stu-id="657e9-103">Update the Visual Studio development tools</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="657e9-104">このトピックでは、開発ツールを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="657e9-104">This topic explains how to update the development tools.</span></span>

<span data-ttu-id="657e9-105">このチュートリアルを使用して、Visual Studio 開発ツールを新しいバージョンに更新します。</span><span class="sxs-lookup"><span data-stu-id="657e9-105">Use this tutorial to update your Visual Studio development tools with a new version.</span></span> <span data-ttu-id="657e9-106">既存の Visual Studio 開発ツールをアンインストールして、新しい拡張機能をインストールする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="657e9-106">It explains how to uninstall your existing Visual Studio development tools and install the new extension.</span></span> <span data-ttu-id="657e9-107">新しい拡張機能は、インストール可能な VSIX ファイルの形式です。</span><span class="sxs-lookup"><span data-stu-id="657e9-107">The new extension is in the form of an installable VSIX file.</span></span> <span data-ttu-id="657e9-108">このファイルは、Dynamics Lifecycle Services (LCS) のサイトで使用可能なバイナリ修正プログラムの一部です。</span><span class="sxs-lookup"><span data-stu-id="657e9-108">This file is a part of the binary hotfix available on the Dynamics Lifecycle Services (LCS) site.</span></span> <span data-ttu-id="657e9-109">VSIX ファイルは、バイナリ修正プログラム パッケージの **DevToolsService\\Scripts** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="657e9-109">The VSIX file is located in the **DevToolsService\\Scripts** folder of the binary hotfix package.</span></span> 

> [!NOTE]
> <span data-ttu-id="657e9-110">Finance and Operations プラットフォーム (Dynamics 365 Unified Operations プラットフォームとも呼ばれます) をプラットフォーム更新プログラム 4 以降にアップグレードする場合は、この記事の手順に従う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="657e9-110">You do not need to follow the instructions in this article if you are upgrading your Finance and Operations platform (also known as the Dynamics 365 Unified Operations platform) to Platform update 4 or newer.</span></span> <span data-ttu-id="657e9-111">プラットフォームのアップグレード プロセスの一部である自動のステップです。</span><span class="sxs-lookup"><span data-stu-id="657e9-111">It is an automatic step that is part of the platform upgrade process.</span></span>

## <a name="uninstall-the-existing-visual-studio-extension"></a><span data-ttu-id="657e9-112">既存の Visual Studio 拡張機能をアンインストールする</span><span class="sxs-lookup"><span data-stu-id="657e9-112">Uninstall the existing Visual Studio extension</span></span>
<span data-ttu-id="657e9-113">開発ツールの新しいバージョンをインストールするには、最初に既存のバージョンをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="657e9-113">In order to install a new version of the development tools, you'll need to uninstall the existing version first.</span></span> <span data-ttu-id="657e9-114">インストールされている開発ツールのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="657e9-114">Verify the version of the development tools that you have installed.</span></span> <span data-ttu-id="657e9-115">インストールしていない場合は、このセクションを省略できます。</span><span class="sxs-lookup"><span data-stu-id="657e9-115">If you don't have it installed, you can skip this section.</span></span>

### <a name="verify-your-current-version-of-the-visual-studio-extension"></a><span data-ttu-id="657e9-116">Visual Studio 拡張機能の現在のバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="657e9-116">Verify your current version of the Visual Studio extension</span></span>

1.  <span data-ttu-id="657e9-117">Visual Studio の**ヘルプ&gt; About Microsoft Visual Studio** ダイアログを開いて、**Finance and Operations 開発者ツール**を表示します。</span><span class="sxs-lookup"><span data-stu-id="657e9-117">Open the Visual Studio **Help &gt; About Microsoft Visual Studio** dialog and find **Finance and Operations Developer Tools**.</span></span>
2.  <span data-ttu-id="657e9-118">選択して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="657e9-118">Select it and click **OK**.</span></span>

### <a name="uninstall-the-extension"></a><span data-ttu-id="657e9-119">拡張機能をアンインストールする</span><span class="sxs-lookup"><span data-stu-id="657e9-119">Uninstall the extension</span></span>

1.  <span data-ttu-id="657e9-120">Visual Studio の**ツール&gt;拡張子と更新**ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="657e9-120">Open the Visual Studio **Tools &gt; Extensions and Updates** dialog.</span></span>
2.  <span data-ttu-id="657e9-121">**Finance and Operations Visual Studio ツール**を選択し、**アンインストール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="657e9-121">Select **Finance and Operations Visual Studio Tools** and click **Uninstall**.</span></span>
3.  <span data-ttu-id="657e9-122">拡張機能がアンインストールされると、Visual Studio を終了します。</span><span class="sxs-lookup"><span data-stu-id="657e9-122">When the extension is uninstalled, exit Visual Studio.</span></span>

## <a name="install-a-new-version-of-the-extension"></a><span data-ttu-id="657e9-123">拡張機能の新しいバージョンのインストール</span><span class="sxs-lookup"><span data-stu-id="657e9-123">Install a new version of the extension</span></span>
1.  <span data-ttu-id="657e9-124">Visual Studio が実行されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="657e9-124">Make sure Visual Studio is not running.</span></span>
2.  <span data-ttu-id="657e9-125">新しいバージョンの VSIX ファイルをダブルクリック (または右クリックと**未処理**) します。</span><span class="sxs-lookup"><span data-stu-id="657e9-125">Double-click (or right-click and **Open**) the VSIX file of the new version.</span></span>
3.  <span data-ttu-id="657e9-126">インストールの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="657e9-126">Follow the installation instructions.</span></span>
4.  <span data-ttu-id="657e9-127">インストールが完了したら、Visual Studio を起動して、アプリケーションの開発を開始できます。</span><span class="sxs-lookup"><span data-stu-id="657e9-127">When installation is complete, you can start Visual Studio and start developing your application.</span></span>




