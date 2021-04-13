---
title: Finance and Operations アプリの開発と管理
description: このページは、開発者と IT プロが Finance and Operations の使用を開始するのに役に立ちます。
author: robinarh
ms.date: 06/20/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: rhaertle
ms.custom: 62303
ms.assetid: 3d7dfc2a-4be2-4fdc-ac35-cc96868f56ab
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b55e8a83fe7dd2e1d7978d2170ede47fe2162d97
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748125"
---
# <a name="development-and-administration-for-finance-and-operations-apps"></a><span data-ttu-id="355a8-103">Finance and Operations アプリの開発と管理</span><span class="sxs-lookup"><span data-stu-id="355a8-103">Development and administration for Finance and Operations apps</span></span>

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="355a8-104">Finance and Operations アプリの開発と管理には次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="355a8-104">Development and administration for Finance and Operations apps includes:</span></span>

- <span data-ttu-id="355a8-105">管理者エクスペリエンスと Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="355a8-105">Administrator experience and Lifecycle Services</span></span>
- <span data-ttu-id="355a8-106">開発者エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="355a8-106">Developer experience</span></span>
- <span data-ttu-id="355a8-107">インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="355a8-107">Intelligence</span></span>
- <span data-ttu-id="355a8-108">モバイル アプリ</span><span class="sxs-lookup"><span data-stu-id="355a8-108">Mobile apps</span></span>
- <span data-ttu-id="355a8-109">データ管理とデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="355a8-109">Data management and data entities</span></span> 
- <span data-ttu-id="355a8-110">Office 統合</span><span class="sxs-lookup"><span data-stu-id="355a8-110">Office integration</span></span>

## <a name="developer-experience"></a><span data-ttu-id="355a8-111">開発者エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="355a8-111">Developer experience</span></span>
<span data-ttu-id="355a8-112">開発者エクスペリエンスは、Visual Studio と .NET コンポーネントを使用する最新のツールに基づいています。</span><span class="sxs-lookup"><span data-stu-id="355a8-112">The developer experience is based on modern tooling using Visual Studio and .NET components.</span></span>
-   <span data-ttu-id="355a8-113">開発ツールは実行中の環境から切り離されます。すなわち、オンライン データベースではなく、ローカルの XML ベース ファイル対して開発を行います。</span><span class="sxs-lookup"><span data-stu-id="355a8-113">The development tools are decoupled from any running environment, which means that you develop against local, XML-based files, not the online database.</span></span>
-   <span data-ttu-id="355a8-114">Microsoft Visual Studio が開発環境です。</span><span class="sxs-lookup"><span data-stu-id="355a8-114">Microsoft Visual Studio is the development environment.</span></span> <span data-ttu-id="355a8-115">Finance and Operations は Visual Studio 環境をカスタマイズして、円滑で慣れ親しんだエクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="355a8-115">Finance and Operations customizes the Visual Studio environment to provide you with a smooth and familiar experience.</span></span>
-   <span data-ttu-id="355a8-116">X++ コンパイラは、すべての機能に対して一般的な中間的な言語 (CIL) を生成します。</span><span class="sxs-lookup"><span data-stu-id="355a8-116">The X++ compiler generates Common Intermediate Language (CIL) for all features.</span></span> <span data-ttu-id="355a8-117">CIL は、C# プログラミング言語など、他の .NET ベース (マネージド) 言語で使用されるものと同じ中間言語です。</span><span class="sxs-lookup"><span data-stu-id="355a8-117">CIL is the same intermediate language used by other .NET-based (managed) languages, such as the C# programming language.</span></span>
-   <span data-ttu-id="355a8-118">ブラウザー ベースのクライアントとフォームのデザイン パターンを活用して、改善されたエンドユーザー エクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="355a8-118">You can leverage the browser-based client and design patterns for forms to provide an improved end-user experience.</span></span>
-   <span data-ttu-id="355a8-119">Application Lifecycle Management (ALM) システムは、ビルドの自動化、テストの自動化、およびクラウドへのモデルの配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="355a8-119">The Application Lifecycle Management (ALM) system supports build automation, test automation, and deployment of models to the cloud.</span></span>

<span data-ttu-id="355a8-120">詳細については、 [開発およびカスタマイズのホーム ページ](dev-tools/developer-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="355a8-120">For more information, see [Develop and customize home page](dev-tools/developer-home-page.md).</span></span>

## <a name="administrator-experience-and-lifecycle-services"></a><span data-ttu-id="355a8-121">管理者エクスペリエンスと Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="355a8-121">Administrator experience and Lifecycle Services</span></span>
<span data-ttu-id="355a8-122">Finance、Supply Chain Management、およびコマースはクラウドでホストされます。</span><span class="sxs-lookup"><span data-stu-id="355a8-122">Finance, Supply Chain Management, and Commerce are cloud-hosted.</span></span> <span data-ttu-id="355a8-123">IT プロは、Dynamics Lifecycle Services (LCS) を使用して、環境を監視およびチューニングし、機能を配置し、最新の修正プログラムで最新の状態に維持することができます。</span><span class="sxs-lookup"><span data-stu-id="355a8-123">As an IT professional, you can use Dynamics Lifecycle Services (LCS) to monitor and tune your environments, deploy features, and stay up to date with recent hotfixes.</span></span> <span data-ttu-id="355a8-124">展開の範囲内で、セキュリティを構成し、プロセスをいつ実行するかを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="355a8-124">Within your deployment, you can configure security, and manage when processes run.</span></span> <span data-ttu-id="355a8-125">また、ビジネス インテリジェンスとレポート、モバイル アプリ、Office、およびその他の統合のサポートを要求されたとき、LCS を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="355a8-125">You can also use LCS when you are called on to support business intelligence and reporting, mobile apps, Office, and other integrations.</span></span> 

## <a name="bi--reporting"></a><span data-ttu-id="355a8-126">BI とレポート作成</span><span class="sxs-lookup"><span data-stu-id="355a8-126">BI & reporting</span></span>
<span data-ttu-id="355a8-127">Finance and Operations は、5 つの異なるレポート エクスペリエンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="355a8-127">Finance and Operations provides five distinct reporting experiences.</span></span> <span data-ttu-id="355a8-128">組織全体のさまざまな職務の複雑で多様なレポートのニーズを満たすために、専門のツールが用意されています。</span><span class="sxs-lookup"><span data-stu-id="355a8-128">Specialized tools are provided to meet the complex and diverse reporting needs of various functions throughout the organization.</span></span>
- <span data-ttu-id="355a8-129">操作ビュー: 特定のビジネス ペルソナの特定のニーズに対応するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="355a8-129">Operational views – Designed to address the specific needs of a given business persona.</span></span>
- <span data-ttu-id="355a8-130">ビジネス ドキュメント – 処理済みのビジネス データをキャプチャおよび交換するために使用される静的なドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="355a8-130">Business documents – Static documents used to capture and exchange processed business data.</span></span>
- <span data-ttu-id="355a8-131">分析ツールおよび視覚化 – ユーザーによるデータの検証を可能にする論理計算の個人用プレゼンテーションです。</span><span class="sxs-lookup"><span data-stu-id="355a8-131">Analytical tools and visualizations – Personalized presentations of logical calculations that allow the user to explore their data.</span></span>
- <span data-ttu-id="355a8-132">Electronic Reporting – 電子ドキュメントの形式の構成に使用されるツールです。</span><span class="sxs-lookup"><span data-stu-id="355a8-132">Electronic reporting – Tool used to configure formats for electronic documents.</span></span>
- <span data-ttu-id="355a8-133">Financial Reporting – 法人の財務活動の標準的な見解に基づいて、詳細な会計管理のツールを提供するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="355a8-133">Financial reporting – Designed to provide in-depth accounting management tools based on standard views of financial activities across legal entities.</span></span>

## <a name="mobile-apps"></a><span data-ttu-id="355a8-134">モバイル アプリ</span><span class="sxs-lookup"><span data-stu-id="355a8-134">Mobile apps</span></span>
<span data-ttu-id="355a8-135">Finance and Operations のモバイル アプリは、組織の業務プロセスをモバイル化するための力を組織に与えます。</span><span class="sxs-lookup"><span data-stu-id="355a8-135">The Finance and Operations mobile app empowers your organization to mobilize its business processes.</span></span> <span data-ttu-id="355a8-136">IT 管理者が組織のモバイル ワークスペース機能を有効にすると、ユーザーはアプリにサインインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。</span><span class="sxs-lookup"><span data-stu-id="355a8-136">After your IT admin enables the mobile workspaces feature for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="355a8-137">Dynamics 365 for Finance and Operations モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="355a8-137">The Dynamics 365 for Finance and Operations mobile app includes the following features that can help increase productivity:</span></span>
+ <span data-ttu-id="355a8-138">ネットワーク接続が断続的な場合やモバイル デバイスがオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。</span><span class="sxs-lookup"><span data-stu-id="355a8-138">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are offline.</span></span> <span data-ttu-id="355a8-139">デバイスがネットワーク接続を再確立する際に、オフライン データ操作は Finance and Operations と自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="355a8-139">When a device reestablishes a network connection, offline data operations are automatically synchronized with Finance and Operations.</span></span> 
+ <span data-ttu-id="355a8-140">IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。</span><span class="sxs-lookup"><span data-stu-id="355a8-140">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="355a8-141">このアプリは既存のコード資産を使用します。したがって、検証手順、ビジネス ロジック、またはセキュリティのコンフィギュレーションを再実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="355a8-141">The app uses your existing code assets, so you don’t have to re-implement your validation procedures, business logic, or security configuration.</span></span> 
+ <span data-ttu-id="355a8-142">IT 管理者または開発者は、Finance and Operations Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計できます。</span><span class="sxs-lookup"><span data-stu-id="355a8-142">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the Finance and Operations web client.</span></span> 
+ <span data-ttu-id="355a8-143">IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。</span><span class="sxs-lookup"><span data-stu-id="355a8-143">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="355a8-144">デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。</span><span class="sxs-lookup"><span data-stu-id="355a8-144">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don’t have constant network connectivity.</span></span> 

## <a name="data-management-and-data-entities"></a><span data-ttu-id="355a8-145">データ管理とデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="355a8-145">Data management and data entities</span></span>
<span data-ttu-id="355a8-146">Finance and Operations からのデータは、Dataverse、Power Apps、および Power BI を使用して、Microsoft のデータ ソースおよび Microsoft 以外のデータ ソースと簡単に統合することができます。</span><span class="sxs-lookup"><span data-stu-id="355a8-146">Data from Finance and Operations can easily be integrated with Microsoft and non-Microsoft data sources using Dataverse, Power Apps, and Power BI.</span></span> <span data-ttu-id="355a8-147">詳細については、 [データ エンティティの概要](data-entities/data-entities.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="355a8-147">For more information, see [Data entities overview](data-entities/data-entities.md).</span></span>

## <a name="office-integration"></a><span data-ttu-id="355a8-148">Office 統合</span><span class="sxs-lookup"><span data-stu-id="355a8-148">Office integration</span></span>
<span data-ttu-id="355a8-149">Microsoft Office の統合機能は、生産的環境を提供し、Office 製品を使用して作業を遂行するユーザーを支援します。</span><span class="sxs-lookup"><span data-stu-id="355a8-149">The Microsoft Office integration capabilities provide users with a productive environment that helps them get the job done by using Office products.</span></span> <span data-ttu-id="355a8-150">詳細については、 [Office 統合の概要](office-integration/office-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="355a8-150">For more information, see [Office integration overview](office-integration/office-integration.md).</span></span>

## <a name="elearning-courses"></a><span data-ttu-id="355a8-151">eLearning コース</span><span class="sxs-lookup"><span data-stu-id="355a8-151">eLearning courses</span></span>
<span data-ttu-id="355a8-152">オンライン コースおよびトレーニングについては、[Microsoft Learn の Dynamics 365 Finance and Operations ](https://docs.microsoft.com/learn/browse/?expanded=dynamics-365&products=dynamics-finance-operations&roles=administrator%2Cdeveloper) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="355a8-152">For online courses and training, check out [Dynamics 365 Finance and Operations on Microsoft Learn](https://docs.microsoft.com/learn/browse/?expanded=dynamics-365&products=dynamics-finance-operations&roles=administrator%2Cdeveloper).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]