---
title: オールインワン配置可能パッケージ
description: このトピックでは、オールインワンの配置可能なパッケージの概念とその使用方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 969b76d03a123259c3a1ff95fd44b975d17769e4
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374785"
---
# <a name="all-in-one-deployable-packages"></a><span data-ttu-id="5a00d-103">オールインワン配置可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="5a00d-103">All-in-one deployable packages</span></span>

<span data-ttu-id="5a00d-104">お客様は、ソフトウェア配置可能パッケージを適用することにより、各自の環境内のソフトウェアを更新できます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-104">Customers can update the software in their environments by applying software deployable packages.</span></span> <span data-ttu-id="5a00d-105">これらのパッケージは、お客様自身がカスタマイズの形で作成できます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-105">These packages can originate from the customers themselves in the form of customizations.</span></span> <span data-ttu-id="5a00d-106">また、パートナーや独立系ソフトウェア ベンダー (ISV) によって提供されることもあります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-106">They can also be provided by partners and independent software vendors (ISVs).</span></span> <span data-ttu-id="5a00d-107">Microsoft では、これらのさまざまなパッケージを 1 つのパッケージにまとめてから、環境に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5a00d-107">Microsoft recommends that customers combine all these various packages into a single package before they apply them to an environment.</span></span> <span data-ttu-id="5a00d-108">セルフサービス環境をお持ちのお客様にとって、このアプローチは難しい要件です。</span><span class="sxs-lookup"><span data-stu-id="5a00d-108">For customers who have self-service environments, this approach is a hard requirement.</span></span>

<span data-ttu-id="5a00d-109">このトピックでは、オールインワン配備可能パッケージを作成および管理するためのベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a00d-109">This topic outlines the best practices for creating and managing an all-in-one deployable package.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="5a00d-110">オールインワン配置可能パッケージでは **ない** 配置可能パッケージのサポートは、2020 年 10 月 31 日に終了します。</span><span class="sxs-lookup"><span data-stu-id="5a00d-110">Support for deployable packages that are **not** all-in-one deployable packages will end October 31, 2020.</span></span>
> - <span data-ttu-id="5a00d-111">現在、支払コネクタが環境に配置されている場合、[支払コネクタ パッケージを作成](../../../commerce/dev-itpro/payment-connector-package.md) して、オールインワン配置可能パッケージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-111">If a payment connector is currently deployed in your environment, you will have to [create a payment connector package](../../../commerce/dev-itpro/payment-connector-package.md) and include it in the all-in-one deployable package.</span></span>
> - <span data-ttu-id="5a00d-112">現在、小売販売時点管理で Microsoft Dynamics 365 Commerce 機能を使用している場合は、[セルフサービス インストーラーを同期](../../../commerce/dev-itpro/Synchronize-installers.md) する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-112">If you currently use Microsoft Dynamics 365 Commerce functionality for the retail point of sale, you will also have to [synchronize self-service installers](../../../commerce/dev-itpro/Synchronize-installers.md).</span></span>

## <a name="what-is-an-all-in-one-deployable-package"></a><span data-ttu-id="5a00d-113">オールインワン配置可能パッケージとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="5a00d-113">What is an all-in-one deployable package?</span></span>

<span data-ttu-id="5a00d-114">オールインワン配置可能パッケージは、現在環境内にあるすべてのモデルとバイナリを含むソフトウェア配置可能パッケージです。</span><span class="sxs-lookup"><span data-stu-id="5a00d-114">An all-in-one deployable is a software deployable package that contains all the models and binaries that you currently have in an environment.</span></span> <span data-ttu-id="5a00d-115">これは、環境内の Microsoft 以外のすべてのソフトウェアを表す単一のパッケージと考えてください。</span><span class="sxs-lookup"><span data-stu-id="5a00d-115">Think of it as a single package that represents all the non-Microsoft software in an environment.</span></span>

<span data-ttu-id="5a00d-116">たとえば、**SandboxTest** と **SandboxPreProd** という 2 つの環境があるとします。</span><span class="sxs-lookup"><span data-stu-id="5a00d-116">For example, you have two environments: **SandboxTest** and **SandboxPreProd**.</span></span>

<img src="media/AIO_PKG.png" width="500px" alt="All-in-one deployable package comparison" />

<span data-ttu-id="5a00d-117">ソフトウェア配置可能パッケージに CustomizationA、CustomizationB、ISV1 が含まれている場合、それは SandboxTest 環境用の完全に配置可能なパッケージです。</span><span class="sxs-lookup"><span data-stu-id="5a00d-117">If your software deployable package contains CustomizationA, CustomizationB, and ISV1, it's a fully deployable package for the SandboxTest environment.</span></span> <span data-ttu-id="5a00d-118">これは、モデルの一覧と完全に一致するためです。</span><span class="sxs-lookup"><span data-stu-id="5a00d-118">This is because it exactly matches the model list.</span></span> <span data-ttu-id="5a00d-119">また、インストールされているすべてのモデルに加えて CustomizationB が含まれているため、SandboxPreProd 環境用の完全に配置可能なパッケージでもあります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-119">It's also a fully deployable package for the SandboxPreProd environment because it has all the models that are installed, plus CustomizationB.</span></span>

<span data-ttu-id="5a00d-120">ただし、ソフトウェア配置可能パッケージに CustomizationA のみが含まれている場合は、どちらの環境にも完全に配置できません。</span><span class="sxs-lookup"><span data-stu-id="5a00d-120">However, if your software deployable package contains only CustomizationA, it isn't fully deployable for either environment.</span></span> <span data-ttu-id="5a00d-121">パッケージには、既にインストールされている一部のモデルが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5a00d-121">The package is missing some of the models that are already installed.</span></span>

## <a name="how-do-i-create-an-all-in-one-deployable-package"></a><span data-ttu-id="5a00d-122">オールインワン配備可能パッケージをどのように作成しますか?</span><span class="sxs-lookup"><span data-stu-id="5a00d-122">How do I create an all-in-one deployable package?</span></span>

<span data-ttu-id="5a00d-123">オールインワン配置可能パッケージを作成するには、主に次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-123">There are two primary methods for creating an all-in-one deployable package:</span></span>

- <span data-ttu-id="5a00d-124">継続的インテグレーション/継続的配置モデルを使用している場合は、既にオールインワン配置可能パッケージを作成しています。</span><span class="sxs-lookup"><span data-stu-id="5a00d-124">If you're using the continuous integration/continuous deployment model, you're already creating all-in-one deployable packages.</span></span>
- <span data-ttu-id="5a00d-125">ビルド環境がない場合は、Microsoft Visual Studio でパッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-125">If you don't have a build environment, you can create a package in Microsoft Visual Studio.</span></span> <span data-ttu-id="5a00d-126">詳細については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a00d-126">For more information, see [Create deployable packages of models](../deployment/create-apply-deployable-package.md).</span></span>

## <a name="what-if-my-isv-packages-dont-contain-source-code"></a><span data-ttu-id="5a00d-127">ISV パッケージにソース コードが含まれていない場合どうなりますか?</span><span class="sxs-lookup"><span data-stu-id="5a00d-127">What if my ISV packages don't contain source code?</span></span>

<span data-ttu-id="5a00d-128">ISV はソース コードを共有するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-128">ISVs can choose whether to share their source code with you.</span></span> <span data-ttu-id="5a00d-129">共有しない場合は、バイナリのみのパッケージを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a00d-129">If they don't share it, they will provide a binary-only package.</span></span> <span data-ttu-id="5a00d-130">このパッケージは、オールインワン配置可能パッケージで簡単に管理できます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-130">This package can easily be managed into an all-in-one deployable package.</span></span> <span data-ttu-id="5a00d-131">手順については、[ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理](manage-runtime-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a00d-131">For instructions, see [Manage third-party models and runtime packages by using source control](manage-runtime-packages.md).</span></span>

## <a name="why-are-these-packages-important"></a><span data-ttu-id="5a00d-132">これらのパッケージはなぜ重要なのですか?</span><span class="sxs-lookup"><span data-stu-id="5a00d-132">Why are these packages important?</span></span>

<span data-ttu-id="5a00d-133">完全に配置可能なパッケージを使用するベスト プラクティスは、特定の環境に適用されるパッケージの複雑さと数を減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-133">The best practice of using fully deployable packages helps reduce the complexity and number of packages that are applied to a given environment.</span></span> <span data-ttu-id="5a00d-134">場合によっては、異なるパッケージをインストールすると、環境の動作が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="5a00d-134">In some circumstances, installation of different packages can change the behavior of your environment.</span></span> <span data-ttu-id="5a00d-135">たとえば、ModelB の後に ModelA をインストールするのではなく、ModelA の後に ModelB をインストールするとします。</span><span class="sxs-lookup"><span data-stu-id="5a00d-135">For example, if you install ModelA and then ModelB instead of ModelB and then ModelA.</span></span>

<span data-ttu-id="5a00d-136">さらに、このアプローチはセルフサービス環境にとって、難しい要件です。</span><span class="sxs-lookup"><span data-stu-id="5a00d-136">In addition, this approach is a hard requirement for self-service environments.</span></span> <span data-ttu-id="5a00d-137">これは、これらの環境ではコンテナー詰めテクノロジを使用して、パッケージを適用するたびに、新しい環境を構築するためです。</span><span class="sxs-lookup"><span data-stu-id="5a00d-137">This is because those environments use containerization technology and build a brand-new environment every time that you apply a package.</span></span> <span data-ttu-id="5a00d-138">今日 ModelA を適用し、明日 ModelB のみを適用すると、ModelA を効果的にアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="5a00d-138">If you apply ModelA today and then apply only ModelB tomorrow, you will effectively uninstall ModelA.</span></span>
