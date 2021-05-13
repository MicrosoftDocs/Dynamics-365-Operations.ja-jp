---
title: 'POS 拡張機能を開始する '
description: このトピックでは、POS 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 3194f598b3585a1738101e11ffbe33714127b665
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960153"
---
# <a name="getting-started-with-pos-extensions"></a><span data-ttu-id="23b67-103">POS 拡張機能を開始する </span><span class="sxs-lookup"><span data-stu-id="23b67-103">Getting started with POS extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23b67-104">このトピックでは、POS 拡張機能の開発環境を作成する方法および POS 拡張機能を開始する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="23b67-104">This topic explains how to create a POS extension development environment and get started with POS extensions.</span></span> <span data-ttu-id="23b67-105">このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="23b67-105">This topic applies to Retail software development kit (SDK) version 10.0.18 and later.</span></span>

## <a name="independent-pos-extension-model"></a><span data-ttu-id="23b67-106">独立した POS 拡張モデル</span><span class="sxs-lookup"><span data-stu-id="23b67-106">Independent POS extension model</span></span>

<span data-ttu-id="23b67-107">POS では、独立して拡張機能の開発、配置およびサービスを行える SDK による拡張機能を許可します。</span><span class="sxs-lookup"><span data-stu-id="23b67-107">POS allows extension through the SDK that lets you independently develop, deploy, and service the extension.</span></span> <span data-ttu-id="23b67-108">拡張機能を作成した後、拡張機能はインストーラー パッケージを使用して拡張機能インストーラーを作成し、拡張機能を配置できます。</span><span class="sxs-lookup"><span data-stu-id="23b67-108">After an extension is created, the extension can use the installer package to create the extension installer to deploy the extensions.</span></span> <span data-ttu-id="23b67-109">インストーラーは、拡張機能に対する変更または拡張が行われた後はべき等になります。</span><span class="sxs-lookup"><span data-stu-id="23b67-109">The installer is idempotent after any changes or enhancements are made to the extension.</span></span> <span data-ttu-id="23b67-110">インストーラーを作成し、それを実行して拡張機能を配置するだけです。</span><span class="sxs-lookup"><span data-stu-id="23b67-110">Just create the installer and run it to deploy the extensions.</span></span>

<span data-ttu-id="23b67-111">拡張機能インストーラーは、コア POS インストーラーから独立しています。</span><span class="sxs-lookup"><span data-stu-id="23b67-111">Extension installers are independent from the core POS installer.</span></span> <span data-ttu-id="23b67-112">これらは別個のもので、異なる方法でパッケージ化されます。</span><span class="sxs-lookup"><span data-stu-id="23b67-112">They are separate and are packaged differently.</span></span> <span data-ttu-id="23b67-113">利点は、拡張機能およびコア POS のサービスを個別に提供できることです。</span><span class="sxs-lookup"><span data-stu-id="23b67-113">The advantage is that extensions and the core POS can be independently serviced.</span></span> <span data-ttu-id="23b67-114">また、POS フレームワークでは複数の拡張機能インストーラーがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="23b67-114">Also, the POS framework supports multiple extension installers.</span></span> <span data-ttu-id="23b67-115">ISV、パートナー、および顧客からの拡張機能は、すべて個別にインストールしてサービスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="23b67-115">Extensions from ISVs, partners, and customers can all be independently installed and serviced.</span></span>

<span data-ttu-id="23b67-116">独立した POS 拡張モデルは Dynamics 365 Commerce アプリケーションのバージョン 10.0.18 以降でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="23b67-116">The independent POS extension model is supported ny Dynamics 365 Commerce application version 10.0.18 and later.</span></span> <span data-ttu-id="23b67-117">以前のバージョンでは、拡張機能とコア POS コードが 1 つのインストーラーとしてパッケージ化され、まとめてサービスが提供されており、したがって、拡張機能とコア POS の変更を個別に配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="23b67-117">In earlier versions, extensions and the core POS code are packaged as one installer and serviced together, therefore, you can’t independently deploy extension and core POS changes.</span></span>

<span data-ttu-id="23b67-118">POS の独立した拡張モデルは、CPOS の MPOS および POS 拡張フレームワーク用の Windows Optional パッケージ フレームワークを使用して、既成のコンポーネントから拡張されます。</span><span class="sxs-lookup"><span data-stu-id="23b67-118">The POS independent extension model isolates the extension from the out-of-box component using the Windows Optional package framework for MPOS and POS extension framework for CPOS.</span></span> <span data-ttu-id="23b67-119">Microsoft Dynamics 365 Commerce の Store Commerce アプリ、Hybrid iOS アプリ、および Android アプリは CPOS をホストするシェル (ラッパー) なので、他のアプリ タイプでは CPOS 拡張機能モデルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="23b67-119">The other app types use the CPOS extension model because the Store Commerce app in Microsoft Dynamics 365 Commerce, Hybrid iOS app, and Android app are shells (wrapper) that host the CPOS.</span></span>

## <a name="getting-started-with-pos-extension"></a><span data-ttu-id="23b67-120">POS 拡張機能を開始する </span><span class="sxs-lookup"><span data-stu-id="23b67-120">Getting started with POS extension</span></span>

<span data-ttu-id="23b67-121">ストア内トポロジに応じて、POS アプリケーション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="23b67-121">Depending on your store topology, choose the POS application type.</span></span> <span data-ttu-id="23b67-122">1 つの POS アプリケーション タイプに対して開発された拡張機能は、他の POS アプリケーション タイプで使用できます。</span><span class="sxs-lookup"><span data-stu-id="23b67-122">The extension developed for one POS app type can be used in other POS app types.</span></span> <span data-ttu-id="23b67-123">拡張機能が POS アプリケーション タイプに依存している場合は、別のアプリケーション タイプでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="23b67-123">If your extension has a dependency on the POS application type, then it can’t be used in another application type.</span></span> <span data-ttu-id="23b67-124">拡張機能の開発中にこのような依存関係を回避することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="23b67-124">We recommend that you try to avoid such dependencies during extension development.</span></span>

## <a name="set-up-the-pos-development-environment"></a><span data-ttu-id="23b67-125">POS 開発環境の設定</span><span class="sxs-lookup"><span data-stu-id="23b67-125">Set up the POS development environment</span></span>

### <a name="prerequisites"></a><span data-ttu-id="23b67-126">必要条件</span><span class="sxs-lookup"><span data-stu-id="23b67-126">Prerequisites</span></span>

+ <span data-ttu-id="23b67-127">Windows 10 1809 以降または Modern POS 用の Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="23b67-127">Windows 10 1809 or newer or Windows Server 2019 for Modern POS.</span></span>
+ <span data-ttu-id="23b67-128">以下のワークロードとコンポーネントを使用する Visual Studio 2017 Community、Professional、または Enterprise。</span><span class="sxs-lookup"><span data-stu-id="23b67-128">Visual Studio 2017 Community, Professional, or Enterprise with the following workloads and components:</span></span>
+ <span data-ttu-id="23b67-129">Visual Studio ワークロード</span><span class="sxs-lookup"><span data-stu-id="23b67-129">Visual Studio workloads</span></span>
    + <span data-ttu-id="23b67-130">Visual Studioコア エディター (通常は既定で選択)</span><span class="sxs-lookup"><span data-stu-id="23b67-130">Visual Studio core editor (usually selected by default)</span></span>
    + <span data-ttu-id="23b67-131">.NET デスクトップ開発</span><span class="sxs-lookup"><span data-stu-id="23b67-131">.NET desktop development</span></span>
    + <span data-ttu-id="23b67-132"> C++ (POS) を使用したデスクトップ開発</span><span class="sxs-lookup"><span data-stu-id="23b67-132">Desktop development with C++ (POS)</span></span>
    + <span data-ttu-id="23b67-133">ユニバーサル Windows プラットフォーム開発 (POS)</span><span class="sxs-lookup"><span data-stu-id="23b67-133">Universal Windows Platform development (POS)</span></span>
    + <span data-ttu-id="23b67-134">[ASP.NET](http://asp.net/) および Web 開発</span><span class="sxs-lookup"><span data-stu-id="23b67-134">[ASP.NET](http://asp.net/)  and web development</span></span>
    + <span data-ttu-id="23b67-135">Azure 開発</span><span class="sxs-lookup"><span data-stu-id="23b67-135">Azure development</span></span>
    + <span data-ttu-id="23b67-136">Node.js 開発 (POS)</span><span class="sxs-lookup"><span data-stu-id="23b67-136">Node.js Development (POS)</span></span>
    + <span data-ttu-id="23b67-137">.NET Core クロスプラットフォーム開発</span><span class="sxs-lookup"><span data-stu-id="23b67-137">.NET Core cross-platform development</span></span>
+ <span data-ttu-id="23b67-138">Visual Studio のコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="23b67-138">Visual Studio components.</span></span> <span data-ttu-id="23b67-139">これらを Visual Studio インストール時に選択できます。</span><span class="sxs-lookup"><span data-stu-id="23b67-139">These can be selected during Visual Studio installation.</span></span>
    + <span data-ttu-id="23b67-140">C# Visual Basic および Roslyn コンパイラ</span><span class="sxs-lookup"><span data-stu-id="23b67-140">C# and Visual Basic Roslyn compilers</span></span>
    + <span data-ttu-id="23b67-141">MSBuild</span><span class="sxs-lookup"><span data-stu-id="23b67-141">MSBuild</span></span>
    + <span data-ttu-id="23b67-142">TypeScript 4.0 SDK</span><span class="sxs-lookup"><span data-stu-id="23b67-142">TypeScript 4.0 SDK</span></span>
    + <span data-ttu-id="23b67-143">VC++ バージョン 15.8 + 最新の v 141 ツール</span><span class="sxs-lookup"><span data-stu-id="23b67-143">VC++ version 15.8+ latest v141 tools</span></span>
    + <span data-ttu-id="23b67-144">Visual C++ ATL (x86 および x64 用)</span><span class="sxs-lookup"><span data-stu-id="23b67-144">Visual C++ ATL for x86 and x64</span></span>
    + <span data-ttu-id="23b67-145">Visual C++ MFC (x86 および x64 用)</span><span class="sxs-lookup"><span data-stu-id="23b67-145">Visual C++ MFC for x86 and x64</span></span>
    + <span data-ttu-id="23b67-146">Windows 10 SDK (10.0.17763.0)</span><span class="sxs-lookup"><span data-stu-id="23b67-146">Windows 10 SDK (10.0.17763.0)</span></span>
+ <span data-ttu-id="23b67-147">.NET Framework/SDK</span><span class="sxs-lookup"><span data-stu-id="23b67-147">.NET Framework/SDK</span></span>
    + [<span data-ttu-id="23b67-148">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="23b67-148">.NET Core 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet/3.1)
    + [<span data-ttu-id="23b67-149">.NET Framework 4.7.2</span><span class="sxs-lookup"><span data-stu-id="23b67-149">.NET Framework 4.7.2</span></span>](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net472-developer-pack-offline-installer) 
+ <span data-ttu-id="23b67-150">SQL Server Express 2016 の ローカル チャンネル データベース。</span><span class="sxs-lookup"><span data-stu-id="23b67-150">SQL Server Express 2016 local channel database.</span></span> <span data-ttu-id="23b67-151">(オフラインでの配置の場合のみ必須)。</span><span class="sxs-lookup"><span data-stu-id="23b67-151">(Required only for offline deployments).</span></span>
+ <span data-ttu-id="23b67-152">SQL Server Data Tools</span><span class="sxs-lookup"><span data-stu-id="23b67-152">SQL Server Data Tools</span></span>
+ <span data-ttu-id="23b67-153">Windows 用 Git (ソース コントロール管理)。</span><span class="sxs-lookup"><span data-stu-id="23b67-153">Git for Windows (Source control management).</span></span>

## <a name="develop-a-pos-extension"></a><span data-ttu-id="23b67-154">POS 拡張機能の開発</span><span class="sxs-lookup"><span data-stu-id="23b67-154">Develop a POS extension</span></span>

<span data-ttu-id="23b67-155">SDK およびサンプルのソース コードを [POS GitHub リポジトリ](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension) からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="23b67-155">Download the SDK and sample source code from the [POS GitHub repo](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample/Pos.Extension).</span></span>

<span data-ttu-id="23b67-156">最初の拡張機能を開発するには、GitHub から既存のサンプルを使用するか、または、ステップ バイ ステップ ガイドに従って拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="23b67-156">To develop your first extension, use the existing samples from GitHub or follow the step-by-step guide to create the extension.</span></span>

## <a name="github-sample"></a><span data-ttu-id="23b67-157">GitHub サンプル</span><span class="sxs-lookup"><span data-stu-id="23b67-157">GitHub sample</span></span>

<span data-ttu-id="23b67-158">このサンプルを使用するには、GitHub リポジトリから **リリース** 分岐サンプルを複製し、GitHub の readme ファイルの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="23b67-158">To use the sample, clone the **release** branch samples from the GitHub repo and follow the steps in the GitHub readme file.</span></span> <span data-ttu-id="23b67-159">コンパイル、ビルド、およびデバッグするには、POS 拡張機能のデバッグ セクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="23b67-159">To compile, build, and debug, follow the steps in Debug POS extension section.</span></span>

## <a name="custom-extensions"></a><span data-ttu-id="23b67-160">カスタムの拡張機能</span><span class="sxs-lookup"><span data-stu-id="23b67-160">Custom extensions</span></span>

<span data-ttu-id="23b67-161">独自の拡張機能を作成するには、[POS 拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="23b67-161">To create your own extension, follow the steps in [Create a POS extension package project](create-pos-extension-package.md).</span></span>

<span data-ttu-id="23b67-162">拡張機能をデバッグするには、[POS 拡張機能のデバッグ](debug-pos-extension.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="23b67-162">To debug your extension, follow the steps in [Debug a POS extension](debug-pos-extension.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
