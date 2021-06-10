---
title: POS 拡張機能の使用を開始する
description: このトピックでは、販売時点管理 (POS) 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 53b39eec04b8e775471245f4e00d57a639ae656e
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093896"
---
# <a name="getting-started-with-pos-extensions"></a><span data-ttu-id="7281f-103">POS 拡張機能の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="7281f-103">Getting started with POS extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7281f-104">このトピックでは、販売時点管理 (POS) 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7281f-104">This topic explains how to create a Point of Sale (POS) extension development environment and get started with POS extensions.</span></span> <span data-ttu-id="7281f-105">Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="7281f-105">It applies to version 10.0.18 and later of the Retail software development kit (SDK).</span></span>

## <a name="independent-pos-extension-model"></a><span data-ttu-id="7281f-106">独立した POS 拡張モデル</span><span class="sxs-lookup"><span data-stu-id="7281f-106">Independent POS extension model</span></span>

<span data-ttu-id="7281f-107">POS により SDK を使用した拡張機能が可能になります。</span><span class="sxs-lookup"><span data-stu-id="7281f-107">POS allows for extension through the SDK.</span></span> <span data-ttu-id="7281f-108">そのため、開発、配置、およびサービス拡張機能を独自に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="7281f-108">Therefore, you can independently develop, deploy, and service extensions.</span></span> <span data-ttu-id="7281f-109">拡張機能を作成した後、インストーラー パッケージを使用し、拡張機能を配置する拡張機能インストーラーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7281f-109">After an extension is created, it can use the installer package to create the extension installer that deploys the extensions.</span></span> <span data-ttu-id="7281f-110">インストーラーは、拡張機能に対する変更または拡張が行われた後はべき等になります。</span><span class="sxs-lookup"><span data-stu-id="7281f-110">The installer is idempotent after any changes or enhancements are made to the extension.</span></span> <span data-ttu-id="7281f-111">インストーラーを作成し、それを実行して拡張機能を配置するだけです。</span><span class="sxs-lookup"><span data-stu-id="7281f-111">Just create the installer, and then run it to deploy the extensions.</span></span>

<span data-ttu-id="7281f-112">拡張機能インストーラーは、コア POS インストーラーには依存しません。</span><span class="sxs-lookup"><span data-stu-id="7281f-112">Extension installers are independent of the core POS installer.</span></span> <span data-ttu-id="7281f-113">これらは別個のもので、異なる方法でパッケージ化されます。</span><span class="sxs-lookup"><span data-stu-id="7281f-113">They are separate and are packaged differently.</span></span> <span data-ttu-id="7281f-114">利点は、拡張機能およびコア POS のサービスを個別に提供できることです。</span><span class="sxs-lookup"><span data-stu-id="7281f-114">The advantage is that extensions and the core POS can be independently serviced.</span></span> <span data-ttu-id="7281f-115">また、POS フレームワークでは複数の拡張機能インストーラーがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7281f-115">Additionally, the POS framework supports multiple extension installers.</span></span> <span data-ttu-id="7281f-116">独立系ソフトウェア ベンダー (ISV)、パートナー、および顧客からの拡張機能は、すべて個別にインストールしてサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="7281f-116">Extensions from independent software vendors (ISVs), partners, and customers can be independently installed and serviced.</span></span>

<span data-ttu-id="7281f-117">独立した POS 拡張モデルは Microsoft Dynamics 365 Commerce アプリケーションのバージョン 10.0.18 以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7281f-117">The independent POS extension model is supported by Microsoft Dynamics 365 Commerce application version 10.0.18 and later.</span></span> <span data-ttu-id="7281f-118">以前のバージョンでは、拡張機能とコア POS コードは 1 つのインストーラーとしてパッケージ化され、まとめてサービスが提供されています。</span><span class="sxs-lookup"><span data-stu-id="7281f-118">In earlier versions, extensions and the core POS code are packaged as one installer and serviced together.</span></span> <span data-ttu-id="7281f-119">したがって、拡張機能の変更やコア POS の変更を個別に配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="7281f-119">Therefore, you can't independently deploy extension changes and core POS changes.</span></span>

<span data-ttu-id="7281f-120">POS の独立した拡張モデルは、Modern POS (MPOS) および Cloud POS (CPOS) の POS 拡張フレームワーク用の Windows Optional パッケージ フレームワークを使用して、既成のコンポーネントから拡張されます。</span><span class="sxs-lookup"><span data-stu-id="7281f-120">The POS independent extension model isolates an extension from the out-of-box component by using the Windows Optional package framework for Modern POS (MPOS) and the POS extension framework for Cloud POS (CPOS).</span></span> <span data-ttu-id="7281f-121">Dynamics 365 Commerce の Store Commerce アプリ、iOS Hybrid アプリ、および Android Hybrid アプリは CPOS をホストするシェル (ラッパー) なので、他のアプリ タイプでは CPOS 拡張機能モデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7281f-121">The other app types use the CPOS extension model, because the Store Commerce app in Dynamics 365 Commerce, the iOS hybrid app, and the Android hybrid app are shells (wrappers) that host CPOS.</span></span>

## <a name="get-started-with-pos-extensions"></a><span data-ttu-id="7281f-122">POS 拡張機能の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="7281f-122">Get started with POS extensions</span></span>

<span data-ttu-id="7281f-123">ストア内トポロジに応じて、POS アプリ タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7281f-123">Depending on your store topology, select the POS app type.</span></span> <span data-ttu-id="7281f-124">一般に、1 つの POS アプリ タイプに対して開発された拡張機能は、他の POS アプリ タイプで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7281f-124">In general, an extension that was developed for one POS app type can be used for other POS app types.</span></span> <span data-ttu-id="7281f-125">ただし、拡張機能が POS アプリ タイプに依存している場合は、別の POS アプリ タイプでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7281f-125">However, if your extension has a dependency on the POS app type, it can't be used for another POS app type.</span></span> <span data-ttu-id="7281f-126">拡張機能の開発中にこのタイプの依存関係を回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7281f-126">We recommend that you try to avoid dependencies of this type during extension development.</span></span>

## <a name="set-up-the-pos-development-environment"></a><span data-ttu-id="7281f-127">POS 開発環境の設定</span><span class="sxs-lookup"><span data-stu-id="7281f-127">Set up the POS development environment</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7281f-128">必要条件</span><span class="sxs-lookup"><span data-stu-id="7281f-128">Prerequisites</span></span>

+ <span data-ttu-id="7281f-129">Windows 10 1809 以降、または MPOS 用 Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="7281f-129">Windows 10 1809 or later, or Windows Server 2019 for MPOS</span></span>
+ <span data-ttu-id="7281f-130">以下のワークロードとコンポーネントがある Visual Studio 2017 Community、Professional、または Enterprise。</span><span class="sxs-lookup"><span data-stu-id="7281f-130">Visual Studio 2017 Community, Professional, or Enterprise that has the following workloads and components:</span></span>

    + <span data-ttu-id="7281f-131">Visual Studio ワークロード:</span><span class="sxs-lookup"><span data-stu-id="7281f-131">Visual Studio workloads:</span></span>

        + <span data-ttu-id="7281f-132">Visual Studioコア エディター (通常は既定で選択)</span><span class="sxs-lookup"><span data-stu-id="7281f-132">Visual Studio core editor (usually selected by default)</span></span>
        + <span data-ttu-id="7281f-133">.NET デスクトップ開発</span><span class="sxs-lookup"><span data-stu-id="7281f-133">.NET desktop development</span></span>
        + <span data-ttu-id="7281f-134"> C++ (POS) を使用したデスクトップ開発</span><span class="sxs-lookup"><span data-stu-id="7281f-134">Desktop development with C++ (POS)</span></span>
        + <span data-ttu-id="7281f-135">ユニバーサル Windows プラットフォーム (UWP) 開発 (POS)</span><span class="sxs-lookup"><span data-stu-id="7281f-135">Universal Windows Platform (UWP) development (POS)</span></span>
        + <span data-ttu-id="7281f-136">[ASP.NET](http://asp.net/) および Web 開発</span><span class="sxs-lookup"><span data-stu-id="7281f-136">[ASP.NET](http://asp.net/) and web development</span></span>
        + <span data-ttu-id="7281f-137">Azure 開発</span><span class="sxs-lookup"><span data-stu-id="7281f-137">Azure development</span></span>
        + <span data-ttu-id="7281f-138">Node.js 開発 (POS)</span><span class="sxs-lookup"><span data-stu-id="7281f-138">Node.js development (POS)</span></span>
        + <span data-ttu-id="7281f-139">.NET Core クロスプラットフォーム開発</span><span class="sxs-lookup"><span data-stu-id="7281f-139">.NET Core cross-platform development</span></span>

    + <span data-ttu-id="7281f-140">Visual Studio のコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="7281f-140">Visual Studio components.</span></span> <span data-ttu-id="7281f-141">これらのコンポーネントは Visual Studio インストール時に選択できます。</span><span class="sxs-lookup"><span data-stu-id="7281f-141">These components can be selected during Visual Studio installation.</span></span>

        + <span data-ttu-id="7281f-142">C# Visual Basic および Roslyn コンパイラ</span><span class="sxs-lookup"><span data-stu-id="7281f-142">C# and Visual Basic Roslyn compilers</span></span>
        + <span data-ttu-id="7281f-143">MSBuild</span><span class="sxs-lookup"><span data-stu-id="7281f-143">MSBuild</span></span>
        + <span data-ttu-id="7281f-144">TypeScript 4.0 SDK</span><span class="sxs-lookup"><span data-stu-id="7281f-144">TypeScript 4.0 SDK</span></span>
        + <span data-ttu-id="7281f-145">Visual C++ バージョン 15.8 + 最新の v141 ツール</span><span class="sxs-lookup"><span data-stu-id="7281f-145">Visual C++ version 15.8+ latest v141 tools</span></span>
        + <span data-ttu-id="7281f-146">Visual C++ ATL (x86 および x64 用)</span><span class="sxs-lookup"><span data-stu-id="7281f-146">Visual C++ ATL for x86 and x64</span></span>
        + <span data-ttu-id="7281f-147">Visual C++ MFC (x86 および x64 用)</span><span class="sxs-lookup"><span data-stu-id="7281f-147">Visual C++ MFC for x86 and x64</span></span>
        + <span data-ttu-id="7281f-148">Windows 10 SDK (10.0.17763.0)</span><span class="sxs-lookup"><span data-stu-id="7281f-148">Windows 10 SDK (10.0.17763.0)</span></span>

+ <span data-ttu-id="7281f-149">.NET Framework/SDK</span><span class="sxs-lookup"><span data-stu-id="7281f-149">The .NET Framework/SDK</span></span>

    + [<span data-ttu-id="7281f-150">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="7281f-150">.NET Core 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet/3.1)
    + [<span data-ttu-id="7281f-151">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="7281f-151">.NET Framework 4.7.2</span></span>](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net472-developer-pack-offline-installer)

+ <span data-ttu-id="7281f-152">SQL Server Express 2016 ローカル チャネル データベース (オフライン配置の場合のみ必要)</span><span class="sxs-lookup"><span data-stu-id="7281f-152">SQL Server Express 2016 local channel database (required only for offline deployments)</span></span>
+ <span data-ttu-id="7281f-153">SQL Server Data Tools</span><span class="sxs-lookup"><span data-stu-id="7281f-153">SQL Server Data Tools</span></span>
+ <span data-ttu-id="7281f-154">Windows 用 Git (ソース コントロール管理)</span><span class="sxs-lookup"><span data-stu-id="7281f-154">Git for Windows (source control management)</span></span>

## <a name="develop-a-pos-extension"></a><span data-ttu-id="7281f-155">POS 拡張機能の開発</span><span class="sxs-lookup"><span data-stu-id="7281f-155">Develop a POS extension</span></span>

<span data-ttu-id="7281f-156">SDK およびサンプルのソース コードを [POS GitHub リポジトリ (repo)](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7281f-156">Download the SDK and sample source code from the [POS GitHub repository (repo)](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension).</span></span>

<span data-ttu-id="7281f-157">最初の拡張機能を開発するには、GitHub から既存のサンプルを使用します。</span><span class="sxs-lookup"><span data-stu-id="7281f-157">To develop your first extension, use the existing samples from GitHub.</span></span> <span data-ttu-id="7281f-158">また、ステップ バイ ステップ ガイドに従って拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="7281f-158">Alternatively, follow the step-by-step guide to create the extension.</span></span>

## <a name="github-sample"></a><span data-ttu-id="7281f-159">GitHub サンプル</span><span class="sxs-lookup"><span data-stu-id="7281f-159">GitHub sample</span></span>

<span data-ttu-id="7281f-160">このサンプルを使用するには、GitHub リポジトリから **リリース** 分岐サンプルを複製し、GitHub の readme ファイルの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7281f-160">To use the sample, clone the **release** branch samples from the GitHub repo, and follow the steps in the GitHub readme file.</span></span>

## <a name="custom-extensions"></a><span data-ttu-id="7281f-161">カスタムの拡張機能</span><span class="sxs-lookup"><span data-stu-id="7281f-161">Custom extensions</span></span>

<span data-ttu-id="7281f-162">独自の拡張機能を作成するには、[POS 拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7281f-162">To create your own extension, follow the steps in [Create a POS extension package project](create-pos-extension-package.md).</span></span>

<span data-ttu-id="7281f-163">拡張機能をデバッグするには、[POS 拡張機能のデバッグ](debug-pos-extension.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7281f-163">To debug your extension, follow the steps in [Debug POS extensions](debug-pos-extension.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
