---
title: Visual Studio の開発ツール
description: Visual Studio 2015 は、開発用の単一統合開発環境 (IDE) です。
author: robadawy
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 23401
ms.assetid: ''
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76a4c8d985396747c35b94e3a3ea4421b642b3cd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191690"
---
# <a name="development-tools-in-visual-studio"></a><span data-ttu-id="b3594-103">Visual Studio の開発ツール</span><span class="sxs-lookup"><span data-stu-id="b3594-103">Development tools in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

## <a name="what-are-the-development-tools"></a><span data-ttu-id="b3594-104">開発ツールとは</span><span class="sxs-lookup"><span data-stu-id="b3594-104">What are the development tools?</span></span>
<span data-ttu-id="b3594-105">Microsoft Dynamics AX 2012 からの注意すべき変更は、Finance and Operations アプリケーションにはリッチ クライアント アプリケーション (ax32.exe) が含まれていないことです。</span><span class="sxs-lookup"><span data-stu-id="b3594-105">A notable change from Microsoft Dynamics AX 2012 is that the Finance and Operations applications do not include a rich-client application (ax32.exe).</span></span> <span data-ttu-id="b3594-106">開発の観点では、Microsoft Dynamics AX 2012 の開発環境、MorphX が使用されなくなることを意味します。</span><span class="sxs-lookup"><span data-stu-id="b3594-106">From a development perspective, this means that the Microsoft Dynamics AX 2012 development environment, MorphX, is no longer used.</span></span> <span data-ttu-id="b3594-107">代わりに、アプリケーション開発は Visual Studio でのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3594-107">In its place, the application development is carried out exclusively in Visual Studio.</span></span> <span data-ttu-id="b3594-108">開発ツールは、デバッグおよびローカル テストのシナリオを含むすべての開発タスクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="b3594-108">The development tools support all of the development tasks, including debugging and local testing scenarios.</span></span> <span data-ttu-id="b3594-109">開発経験の主なゴールは、使い慣れた Microsoft Dynamics AX 2012 の概念を保持しながら、Visual Studio のフレームワークにシームレスに順応することです。</span><span class="sxs-lookup"><span data-stu-id="b3594-109">A primary goal of the development experience is to keep familiar Microsoft Dynamics AX 2012 concepts, and seamlessly adapt them to the Visual Studio framework and paradigms.</span></span>

<span data-ttu-id="b3594-110">Visual Studio 2015 は、開発用の単一統合開発環境 (IDE) です。</span><span class="sxs-lookup"><span data-stu-id="b3594-110">Visual Studio 2015 is the exclusive integrated development environment (IDE) for development.</span></span> <span data-ttu-id="b3594-111">すべてのアプリケーション開発作業がそのアプリケーションで実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3594-111">All of your application development work will be performed with it.</span></span> <span data-ttu-id="b3594-112">このセクションでは、開発ツールのインストール時に Visual Studio に追加される主な機能の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="b3594-112">This section is an overview of the main features that are added to Visual Studio when the development tools are installed.</span></span>

### <a name="application-explorer"></a><span data-ttu-id="b3594-113">アプリケーション エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="b3594-113">Application Explorer</span></span>
<span data-ttu-id="b3594-114">Visual Studio で、モデル ストアはアプリケーション エクスプローラーで表されます。</span><span class="sxs-lookup"><span data-stu-id="b3594-114">In Visual Studio, the model store is represented by the Application Explorer.</span></span> <span data-ttu-id="b3594-115">**表示**メニューで、**アプリケーション** **エクスプローラー**をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="b3594-115">On the **View** menu, click **Application** **Explorer** to open it.</span></span> <span data-ttu-id="b3594-116">アプリケーション エクスプローラーは、Microsoft Dynamics AX 2012 でよく使われているアプリケーション オブジェクト ツリー (AOT) に対応します。</span><span class="sxs-lookup"><span data-stu-id="b3594-116">The Application Explorer corresponds to the Application Object Tree (AOT) that you may be familiar with in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="b3594-117">アプリケーション エクスプローラーを使用して、アプリケーションを定義するモデル ストア内の要素を参照および操作します。</span><span class="sxs-lookup"><span data-stu-id="b3594-117">Use the Application Explorer to browse and interact with the elements in the model store that define the applications.</span></span> <span data-ttu-id="b3594-118">次の図は、アプリケーション エクスプローラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3594-118">The following illustration shows the Application Explorer.</span></span> <span data-ttu-id="b3594-119">詳細については、[アプリケーション エクスプローラー](application-explorer.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3594-119">For more details, see [Application Explorer](application-explorer.md).</span></span>

![アプリケーション エクスプローラー](media/1_devotoolsconcept.png)

### <a name="the-project-template"></a><span data-ttu-id="b3594-121">プロジェクト テンプレート</span><span class="sxs-lookup"><span data-stu-id="b3594-121">The project template</span></span>
<span data-ttu-id="b3594-122">単純なアプリケーションであっても、そのモデルには多数の要素を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b3594-122">Even a simple application can have a large number of elements in its model.</span></span> <span data-ttu-id="b3594-123">モデルに使用する要素を整理および管理するために、**業務プロジェクト** テンプレートが Visual Studio に追加されました。</span><span class="sxs-lookup"><span data-stu-id="b3594-123">The **Operations Project** template has been added to Visual Studio to help you organize and manage the elements that you are working with for a model.</span></span> <span data-ttu-id="b3594-124">このプロジェクトを使用して、モデル要素の設計、作成、およびをテストをします。</span><span class="sxs-lookup"><span data-stu-id="b3594-124">You will use the project to design, build, and test model elements.</span></span> <span data-ttu-id="b3594-125">1 つの Visual Studio ソリューション内に複数のプロジェクトがあることが一般的です。</span><span class="sxs-lookup"><span data-stu-id="b3594-125">It’s common to have several projects within a single Visual Studio solution.</span></span><span data-ttu-id="b3594-126">次の図は、Visual Studio ソリューションの 3 つのプロジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3594-126"> The following illustration shows three projects in a Visual Studio solution.</span></span> <span data-ttu-id="b3594-127">詳細については、[プロジェクト](projects.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3594-127">For more details, see [Projects](projects.md).</span></span>

![ソリューション エクスプローラー](media/2_devotoolsconcept.png)

### <a name="element-designers"></a><span data-ttu-id="b3594-129">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="b3594-129">Element designers</span></span>
<span data-ttu-id="b3594-130">Visual Studio のツールには、アプリケーション内の要素の種類ごとのデザイナーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3594-130">The Visual Studio tools contain designers for each kind of element in the application.</span></span> <span data-ttu-id="b3594-131">要素を作成または変更するときは、これらのデザイナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="b3594-131">You will use these designers when you create or modify elements.</span></span> <span data-ttu-id="b3594-132">次の図は、フォーム要素の要素デザイナーを示しています。</span><span class="sxs-lookup"><span data-stu-id="b3594-132">The following illustration shows the element designer for a form element.</span></span> <span data-ttu-id="b3594-133">詳細については、[要素デザイナー](element-designers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3594-133">For more details, see [Element designers](element-designers.md).</span></span>

![要素デザイナー](media/3_devotoolsconcept.png)

### <a name="code-editor"></a><span data-ttu-id="b3594-135">コード エディター</span><span class="sxs-lookup"><span data-stu-id="b3594-135">Code editor</span></span>
<span data-ttu-id="b3594-136">X++ コードは、Visual Studio 用のコード エディターに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="b3594-136">The X++ code is written in the code editor for Visual Studio.</span></span> <span data-ttu-id="b3594-137">開発者がコード エディターに期待する標準機能がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b3594-137">The standard features that a developer expects from the code editor are supported.</span></span> <span data-ttu-id="b3594-138">たとえば、コードのセクションは折りたたみ可能です。</span><span class="sxs-lookup"><span data-stu-id="b3594-138">For example, sections of code are collapsible.</span></span> <span data-ttu-id="b3594-139">IntelliSense は、コードを書き込みまたは変更するガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3594-139">IntelliSense provides guidance as you write or modify code.</span></span> <span data-ttu-id="b3594-140">詳細については、[コード エディター](code-editor.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3594-140">For more details, see [Code editor](code-editor.md).</span></span>

![コード エディター](media/4_devotoolsconcept.png)

### <a name="dynamics-365-menu"></a><span data-ttu-id="b3594-142">Dynamics 365 メニュー</span><span class="sxs-lookup"><span data-stu-id="b3594-142">Dynamics 365 menu</span></span>
<span data-ttu-id="b3594-143">このツールは **Dynamics 365 メニュー** を Visual Studio に追加します。</span><span class="sxs-lookup"><span data-stu-id="b3594-143">The tools add the **Dynamics 365** menu to Visual Studio.</span></span> <span data-ttu-id="b3594-144">開発プロセス中に使用するいくつかのツールは、ここで入手できます。</span><span class="sxs-lookup"><span data-stu-id="b3594-144">Several tools that you will use during the development process are found here.</span></span> <span data-ttu-id="b3594-145">たとえば、モデルを管理するツールは、メニューからアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b3594-145">For example, the tools for managing models are accessed from the menu.</span></span>
