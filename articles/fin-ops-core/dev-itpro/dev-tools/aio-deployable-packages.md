---
title: オールインワン配置可能パッケージ
description: このトピックでは、オールインワンの配置可能なパッケージの概念とその使用方法について説明します。
author: laneswenka
ms.date: 05/20/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: e1167aa3705bd9d7965c52f7bee4aec9d96cb027
ms.sourcegitcommit: 273903b7b73ac726d447c50f7086e6d8b0f0f74e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2021
ms.locfileid: "6086977"
---
# <a name="all-in-one-deployable-packages"></a><span data-ttu-id="f61fd-103">オールインワン配置可能パッケージ</span><span class="sxs-lookup"><span data-stu-id="f61fd-103">All-in-one deployable packages</span></span>

<span data-ttu-id="f61fd-104">お客様は、ソフトウェア配置可能パッケージを適用することにより、各自の環境内のソフトウェアを更新できます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-104">Customers can update the software in their environments by applying software deployable packages.</span></span> <span data-ttu-id="f61fd-105">これらのパッケージは、お客様自身がカスタマイズの形で作成できます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-105">These packages can originate from the customers themselves in the form of customizations.</span></span> <span data-ttu-id="f61fd-106">また、パートナーや独立系ソフトウェア ベンダー (ISV) によって提供されることもあります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-106">They can also be provided by partners and independent software vendors (ISVs).</span></span> <span data-ttu-id="f61fd-107">Microsoft では、これらのさまざまなパッケージを 1 つのパッケージにまとめてから、環境に適用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f61fd-107">Microsoft recommends that customers combine all these various packages into a single package before they apply them to an environment.</span></span> <span data-ttu-id="f61fd-108">セルフサービス環境をお持ちのお客様にとって、このアプローチは難しい要件です。</span><span class="sxs-lookup"><span data-stu-id="f61fd-108">For customers who have self-service environments, this approach is a hard requirement.</span></span>

<span data-ttu-id="f61fd-109">このトピックでは、オールインワン配備可能パッケージを作成および管理するためのベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f61fd-109">This topic outlines the best practices for creating and managing an all-in-one deployable package.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="f61fd-110">オール イン ワン パッケージの適用は、フェーズで行われます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-110">The enforcement of all-in-one packages will be done in phases.</span></span> <span data-ttu-id="f61fd-111">オールインワン配置可能パッケージでは **ない** 配置可能パッケージに対するサポートを拡張する要求は、2020 年 10 月 31 日に終了しました。</span><span class="sxs-lookup"><span data-stu-id="f61fd-111">Requests to extend the support for deployable packages that are **not** all-in-one deployable packages ended on October 31, 2020.</span></span>
> - <span data-ttu-id="f61fd-112">現在、支払コネクタが環境に配置されている場合、[支払コネクタ パッケージを作成](../../../commerce/dev-itpro/payment-connector-package.md) して、オールインワン配置可能パッケージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-112">If a payment connector is currently deployed in your environment, you will have to [create a payment connector package](../../../commerce/dev-itpro/payment-connector-package.md) and include it in the all-in-one deployable package.</span></span>
> - <span data-ttu-id="f61fd-113">現在、小売販売時点管理で Microsoft Dynamics 365 Commerce 機能を使用している場合は、[セルフサービス インストーラーを同期](../../../commerce/dev-itpro/Synchronize-installers.md) する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-113">If you currently use Microsoft Dynamics 365 Commerce functionality for the retail point of sale, you will also have to [synchronize self-service installers](../../../commerce/dev-itpro/Synchronize-installers.md).</span></span>

## <a name="what-is-an-all-in-one-deployable-package"></a><span data-ttu-id="f61fd-114">オールインワン配置可能パッケージとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="f61fd-114">What is an all-in-one deployable package?</span></span>

<span data-ttu-id="f61fd-115">オールインワン配置可能パッケージは、現在環境内にあるすべてのモデルとバイナリを含むソフトウェア配置可能パッケージです。</span><span class="sxs-lookup"><span data-stu-id="f61fd-115">An all-in-one deployable is a software deployable package that contains all the models and binaries that you currently have in an environment.</span></span> <span data-ttu-id="f61fd-116">これは、環境内の Microsoft 以外のすべてのソフトウェアを表す単一のパッケージと考えてください。</span><span class="sxs-lookup"><span data-stu-id="f61fd-116">Think of it as a single package that represents all the non-Microsoft software in an environment.</span></span>

<span data-ttu-id="f61fd-117">たとえば、**SandboxTest** と **SandboxPreProd** という 2 つの環境があるとします。</span><span class="sxs-lookup"><span data-stu-id="f61fd-117">For example, you have two environments: **SandboxTest** and **SandboxPreProd**.</span></span>

<img src="media/AIO_PKG.png" width="500px" alt="All-in-one deployable package comparison" />

<span data-ttu-id="f61fd-118">ソフトウェア配置可能パッケージに CustomizationA、CustomizationB、ISV1 が含まれている場合、それは SandboxTest 環境用の完全に配置可能なパッケージです。</span><span class="sxs-lookup"><span data-stu-id="f61fd-118">If your software deployable package contains CustomizationA, CustomizationB, and ISV1, it's a fully deployable package for the SandboxTest environment.</span></span> <span data-ttu-id="f61fd-119">これは、モデルの一覧と完全に一致するためです。</span><span class="sxs-lookup"><span data-stu-id="f61fd-119">This is because it exactly matches the model list.</span></span> <span data-ttu-id="f61fd-120">また、インストールされているすべてのモデルに加えて CustomizationB が含まれているため、SandboxPreProd 環境用の完全に配置可能なパッケージでもあります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-120">It's also a fully deployable package for the SandboxPreProd environment because it has all the models that are installed, plus CustomizationB.</span></span>

<span data-ttu-id="f61fd-121">ただし、ソフトウェア配置可能パッケージに CustomizationA のみが含まれている場合は、どちらの環境にも完全に配置できません。</span><span class="sxs-lookup"><span data-stu-id="f61fd-121">However, if your software deployable package contains only CustomizationA, it isn't fully deployable for either environment.</span></span> <span data-ttu-id="f61fd-122">パッケージには、既にインストールされている一部のモデルが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f61fd-122">The package is missing some of the models that are already installed.</span></span>

## <a name="how-do-i-create-an-all-in-one-deployable-package"></a><span data-ttu-id="f61fd-123">オールインワン配備可能パッケージをどのように作成しますか?</span><span class="sxs-lookup"><span data-stu-id="f61fd-123">How do I create an all-in-one deployable package?</span></span>

<span data-ttu-id="f61fd-124">オールインワン配置可能パッケージを作成するには、主に次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-124">There are two primary methods for creating an all-in-one deployable package:</span></span>

- <span data-ttu-id="f61fd-125">継続的インテグレーション/継続的配置モデルを使用している場合は、既にオールインワン配置可能パッケージを作成しています。</span><span class="sxs-lookup"><span data-stu-id="f61fd-125">If you're using the continuous integration/continuous deployment model, you're already creating all-in-one deployable packages.</span></span>
- <span data-ttu-id="f61fd-126">ビルド環境がない場合は、Microsoft Visual Studio でパッケージを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-126">If you don't have a build environment, you can create a package in Microsoft Visual Studio.</span></span> <span data-ttu-id="f61fd-127">詳細については、[配置可能パッケージの作成](../deployment/create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f61fd-127">For more information, see [Create deployable packages of models](../deployment/create-apply-deployable-package.md).</span></span>

## <a name="what-if-my-isv-packages-dont-contain-source-code"></a><span data-ttu-id="f61fd-128">ISV パッケージにソース コードが含まれていない場合どうなりますか?</span><span class="sxs-lookup"><span data-stu-id="f61fd-128">What if my ISV packages don't contain source code?</span></span>

<span data-ttu-id="f61fd-129">ISV はソース コードを共有するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-129">ISVs can choose whether to share their source code with you.</span></span> <span data-ttu-id="f61fd-130">共有しない場合は、バイナリのみのパッケージを提供します。</span><span class="sxs-lookup"><span data-stu-id="f61fd-130">If they don't share it, they will provide a binary-only package.</span></span> <span data-ttu-id="f61fd-131">このパッケージは、オールインワン配置可能パッケージで簡単に管理できます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-131">This package can easily be managed into an all-in-one deployable package.</span></span> <span data-ttu-id="f61fd-132">手順については、[ソース コントロールを使用してサード パーティ モデルとランタイム パッケージを管理](manage-runtime-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f61fd-132">For instructions, see [Manage third-party models and runtime packages by using source control](manage-runtime-packages.md).</span></span>

## <a name="how-can-i-deploy-isv-licenses"></a><span data-ttu-id="f61fd-133">ISV ライセンスはどのように配置できますか?</span><span class="sxs-lookup"><span data-stu-id="f61fd-133">How can I deploy ISV licenses?</span></span>

<span data-ttu-id="f61fd-134">ISV はライセンスの配置可能パッケージを送信し、ライセンスを提供または更新することができます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-134">ISVs can send license deployable packages to provide or update a license.</span></span> <span data-ttu-id="f61fd-135">ただし、セルフサービス環境では、ライセンスはすべてオールインワン配置可能パッケージに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-135">However, for self-service environments licenses should also be included in an all-in-one deployable package.</span></span> <span data-ttu-id="f61fd-136">ビルド パイプラインまたはリリース パイプラインにタスクを追加して、配置可能なパッケージに対して所有するライセンスを追加できます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-136">You can add a task to your build or release pipelines to add any licenses you have to a deployable package.</span></span> <span data-ttu-id="f61fd-137">詳細については [Azure Pipelines にある配置可能パッケージへのライセンス ファイルの追加](pipeline-add-license-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f61fd-137">For more information, see [Add license files to a deployable package in Azure Pipelines](pipeline-add-license-package.md).</span></span>

## <a name="why-are-these-packages-important"></a><span data-ttu-id="f61fd-138">これらのパッケージはなぜ重要なのですか?</span><span class="sxs-lookup"><span data-stu-id="f61fd-138">Why are these packages important?</span></span>

<span data-ttu-id="f61fd-139">完全に配置可能なパッケージを使用するベスト プラクティスは、特定の環境に適用されるパッケージの複雑さと数を減らすのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-139">The best practice of using fully deployable packages helps reduce the complexity and number of packages that are applied to a given environment.</span></span> <span data-ttu-id="f61fd-140">場合によっては、異なるパッケージをインストールすると、環境の動作が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f61fd-140">In some circumstances, installation of different packages can change the behavior of your environment.</span></span> <span data-ttu-id="f61fd-141">たとえば、ModelB の後に ModelA をインストールするのではなく、ModelA の後に ModelB をインストールするとします。</span><span class="sxs-lookup"><span data-stu-id="f61fd-141">For example, if you install ModelA and then ModelB instead of ModelB and then ModelA.</span></span>

<span data-ttu-id="f61fd-142">さらに、このアプローチはセルフサービス環境にとって、難しい要件です。</span><span class="sxs-lookup"><span data-stu-id="f61fd-142">In addition, this approach is a hard requirement for self-service environments.</span></span> <span data-ttu-id="f61fd-143">これは、これらの環境ではコンテナー詰めテクノロジを使用して、パッケージを適用するたびに、新しい環境を構築するためです。</span><span class="sxs-lookup"><span data-stu-id="f61fd-143">This is because those environments use containerization technology and build a brand-new environment every time that you apply a package.</span></span> <span data-ttu-id="f61fd-144">今日 ModelA を適用し、明日 ModelB のみを適用すると、ModelA を効果的にアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="f61fd-144">If you apply ModelA today and then apply only ModelB tomorrow, you will effectively uninstall ModelA.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
