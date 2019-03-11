---
title: フリート管理のサンプル アプリケーション
description: このトピックは、フリート管理のサンプル アプリケーションについての概要です。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 79892
ms.assetid: 999b43b2-f149-4145-9d85-e2a62cd8da1e
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8225d1d40739819bef8a268b0d911f04f6f013
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369987"
---
# <a name="fleet-management-sample-application"></a><span data-ttu-id="98c26-103">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="98c26-103">Fleet Management sample application</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98c26-104">このトピックは、フリート管理のサンプル アプリケーションについての概要です。</span><span class="sxs-lookup"><span data-stu-id="98c26-104">This topic is an overview of the Fleet Management sample application.</span></span>

<span data-ttu-id="98c26-105">フリート管理サンプル アプリケーションは、開発および基板機能を示すために用意されています。</span><span class="sxs-lookup"><span data-stu-id="98c26-105">The Fleet Management sample application has been provided to showcase development and foundation capabilities.</span></span> <span data-ttu-id="98c26-106">フリート管理は、ISV が車のレンタル機関用に作成するかもしれないソリューションを表します。</span><span class="sxs-lookup"><span data-stu-id="98c26-106">Fleet Management represents a solution that an ISV might create for a car-rental agency.</span></span> <span data-ttu-id="98c26-107">フリート管理データには、レンタルに使用できる車両、レンタルしてこれらの車両を戻すことができる顧客が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98c26-107">Fleet Management data includes vehicles which are available for renting, and customers who can rent and return these vehicles.</span></span> <span data-ttu-id="98c26-108">従業員は、車両でメンテナンス ワークフローを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="98c26-108">Employees can also run a maintenance workflow on these vehicles.</span></span> <span data-ttu-id="98c26-109">**メモ**</span><span class="sxs-lookup"><span data-stu-id="98c26-109">**Note**</span></span>

<span data-ttu-id="98c26-110">一部のチュートリアルについては、コンピュータにない場合、FleetManagement ソリューションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98c26-110">For some tutorials, you will need to create the FleetManagement solution if it is not on your computer.</span></span> <span data-ttu-id="98c26-111">作成手順は「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="98c26-111">The steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>

<span data-ttu-id="98c26-112">一部のチュートリアルについては、フリート管理チュートリアル コードおよび <https://github.com/Microsoft/FMLab> から他のコンポーネントをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="98c26-112">For some tutorials, you must download the Fleet Management tutorial code and other artifacts from <https://github.com/Microsoft/FMLab>.</span></span>

<span data-ttu-id="98c26-113">フリート管理は、以下のようにプラットフォーム機能を示す Visual Studio ソリューションとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="98c26-113">Fleet Management is provided as a Visual Studio solution that demonstrates platform capabilities, such as:</span></span>

-   <span data-ttu-id="98c26-114">フォーム</span><span class="sxs-lookup"><span data-stu-id="98c26-114">Forms</span></span>
-   <span data-ttu-id="98c26-115">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="98c26-115">Workflow</span></span>
-   <span data-ttu-id="98c26-116">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="98c26-116">Security</span></span>
-   <span data-ttu-id="98c26-117">ラベル</span><span class="sxs-lookup"><span data-stu-id="98c26-117">Labels</span></span>
-   <span data-ttu-id="98c26-118">リソース</span><span class="sxs-lookup"><span data-stu-id="98c26-118">Resources</span></span>
-   <span data-ttu-id="98c26-119">データ</span><span class="sxs-lookup"><span data-stu-id="98c26-119">Data</span></span>
-   <span data-ttu-id="98c26-120">ビジネス インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="98c26-120">Business Intelligence</span></span>
-   <span data-ttu-id="98c26-121">拡張子</span><span class="sxs-lookup"><span data-stu-id="98c26-121">Extensions</span></span>

<span data-ttu-id="98c26-122">フリート管理ソリューションには、2 つの独立したプロジェクト (基本モデル用のプロジェクトと、基本モデルに拡張するためのプロジェクト)。</span><span class="sxs-lookup"><span data-stu-id="98c26-122">The Fleet Management solution includes two separate projects: one for the base model and the other one for extensions to the base model.</span></span> <span data-ttu-id="98c26-123">FleetManagement Migrated という名前のプロジェクトは、Dynamics AX 2012 からコードを移行した後に、移行されたアプリケーションがどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="98c26-123">The project named FleetManagement Migrated demonstrates how a migrated application might appear after migrating code from Dynamics AX 2012.</span></span> <span data-ttu-id="98c26-124">このバージョンでは、Microsoft Dynamics AX 2012 R3 から移行されたフォームが Web クライアント上でどのように動作するかが示されます。</span><span class="sxs-lookup"><span data-stu-id="98c26-124">This version shows how forms that have been migrated from Microsoft Dynamics AX 2012 R3 work on a web client.</span></span> <span data-ttu-id="98c26-125">これらのフォームは、自動化された移行ツールおよび Visual Studio でのその他の手動移行手順を使用して作成されています。</span><span class="sxs-lookup"><span data-stu-id="98c26-125">These forms have been created using automated migration tools and some other manual migration steps in Visual Studio.</span></span> <span data-ttu-id="98c26-126">これらのフォームは X++ テーブルにバインドし、X++ プログラミング モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="98c26-126">These forms bind to X++ tables and use the X++ programming model.</span></span> <span data-ttu-id="98c26-127">FleetManagement Discounts (または FleetManagementExtension) という名前のプロジェクトは、拡張子を使用してアプリケーションをカスタマイズする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="98c26-127">The project named FleetManagement Discounts (or FleetManagementExtension) demonstrates how to use extensions to customize an application.</span></span> <span data-ttu-id="98c26-128">このプロジェクトは、コントロールとテーブルを拡張し、データイ ベントを処理し、プラグインを使用してビジネス ロジックを置き換えることで、フリート管理のサンプルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="98c26-128">This project extends the Fleet Management sample by extending controls and tables, handling data events, and replacing business logic using a plug-in.</span></span> <span data-ttu-id="98c26-129">この記事に添付されているチュートリアルでは、Fleet Management のサンプルを詳しく見ていきます。</span><span class="sxs-lookup"><span data-stu-id="98c26-129">The tutorials that accompany this article provide a more-detailed look at the Fleet Management sample.</span></span> <span data-ttu-id="98c26-130">これらには、フリート管理のチュートリアル「[フリート管理のサンプルを使用する](fleet-management-sample.md)」、拡張機能を説明するチュートリアル、「[拡張機能を使用してモデル要素をカスタマイズする](../extensibility/customize-model-elements-extensions.md)」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98c26-130">These include a Fleet Management tutorial, [Using the Fleet Management sample](fleet-management-sample.md), and a tutorial that walks through extensions, [Customize model elements using Extensions](../extensibility/customize-model-elements-extensions.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="98c26-131">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="98c26-131">Additional resources</span></span>
--------

[<span data-ttu-id="98c26-132">フリート管理のサンプルを使用する</span><span class="sxs-lookup"><span data-stu-id="98c26-132">Using the Fleet Management sample</span></span>](fleet-management-sample.md)

[<span data-ttu-id="98c26-133">拡張機能を使用してモデル要素をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="98c26-133">Customize model elements using extensions</span></span>](../extensibility/customize-model-elements-extensions.md)

[<span data-ttu-id="98c26-134">開発者ホーム ページ</span><span class="sxs-lookup"><span data-stu-id="98c26-134">Developer Home Page</span></span>](developer-home-page.md)

[<span data-ttu-id="98c26-135">FMLab サンプル コードをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="98c26-135">Download the FMLab sample code</span></span>](https://github.com/Microsoft/FMLab)

[<span data-ttu-id="98c26-136">FleetManagement ソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="98c26-136">Create the FleetManagement solution</span></span>](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)



