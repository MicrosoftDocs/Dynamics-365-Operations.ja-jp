---
title: "環境の更新"
description: "このトピックでは、セルフ サービス配置エクスペリエンスを使用して配置された環境を更新する方法について説明します。"
author: manado
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 61aee27fce705231c0ac89cc596bb19b95426608
ms.openlocfilehash: 9ec1db4f5c3a01300cc2678d4371eab7392c6223
ms.contentlocale: ja-jp
ms.lasthandoff: 12/14/2018

---

# <a name="update-an-environment"></a><span data-ttu-id="fc051-103">環境の更新</span><span class="sxs-lookup"><span data-stu-id="fc051-103">Update an environment</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="fc051-104">このトピックでは、[セルフサービス配置](infrastructure-stack.md)エクスペリエンスを使用して配置した Dynamics 365 for Finance and Operations 環境に更新を適用するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fc051-104">This topic walks through the process of applying updates to a Dynamics 365 for Finance and Operations environment that was deployed using the [self-service deployment](infrastructure-stack.md) experience.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc051-105">次世代のインフラストラクチャでは、現在のフローとは異なる方法で更新が適用されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-105">With the next generation infrastructure, updates are applied differently from the current flow.</span></span> <span data-ttu-id="fc051-106">**パッケージで提供されているものはすべて環境に適用され、既に環境に存在するものは上書きされます**。</span><span class="sxs-lookup"><span data-stu-id="fc051-106">**Whatever is supplied in the package is applied to the environment and it OVERWRITES what is already present in the environment**.</span></span> <span data-ttu-id="fc051-107">つまり、ビルド環境からのすべてのカスタマイズおよび ISV ソリューションを含む 1 つの配置可能パッケージを作成する**必要があります**。</span><span class="sxs-lookup"><span data-stu-id="fc051-107">This means that you **must** create a single deployable package that contains all customizations and ISV solutions from your build environment.</span></span> <span data-ttu-id="fc051-108">環境上にあるものと、パッケージに含まれるものの間でモデルの一覧に差異がある場合、更新を適用する前に警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-108">If there is a difference in the list of models between what is on the environment and what is in the package, you will be warned before applying the update.</span></span> <span data-ttu-id="fc051-109">1 つのパッケージを作成する方法については、[ソース コントロールを使用することでサード パーティ モデルとランタイム パッケージを管理する](../dev-tools/manage-runtime-packages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc051-109">For details about creating a single package, see [Manage third-party models and runtime packages by using source control](../dev-tools/manage-runtime-packages.md).</span></span>

## <a name="supported-package-types"></a><span data-ttu-id="fc051-110">サポートされているパッケージの種類</span><span class="sxs-lookup"><span data-stu-id="fc051-110">Supported package types</span></span>
<span data-ttu-id="fc051-111">[セルフ サービス展開](infrastructure-stack.md)エクスペリエンスを使用して展開された環境は 8.1 以降にあるため、次のパッケージ タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="fc051-111">Because environments deployed using the [self-service deployment](infrastructure-stack.md) experience will be on 8.1 and later, we support the following package types:</span></span>

- <span data-ttu-id="fc051-112">**AOT の配置可能パッケージ** - アプリケーション メタデータおよびソース コードから生成される配置可能なパッケージ。</span><span class="sxs-lookup"><span data-stu-id="fc051-112">**AOT deployable package** - A deployable package that is generated from application metadata and source code.</span></span> <span data-ttu-id="fc051-113">この展開可能なパッケージは、**ビルド**環境で作成されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-113">This deployable package is created in a **build** environment.</span></span>
- <span data-ttu-id="fc051-114">**バイナリ更新プログラム パッケージ** - ダイナミックリンク ライブラリ (DLL)と、プラットフォームとアプリケーションが依存するその他のバイナリとメタデータを含む配置可能パッケージ。</span><span class="sxs-lookup"><span data-stu-id="fc051-114">**Binary update package** - A deployable package that contains dynamic-link libraries (DLLs) and other binaries and metadata that the platform and application depend on.</span></span> <span data-ttu-id="fc051-115">これは、Microsoft によってリリースされたパッケージです。</span><span class="sxs-lookup"><span data-stu-id="fc051-115">This is a package released by Microsoft.</span></span>

## <a name="development-application-lifecycle-management-alm-flow"></a><span data-ttu-id="fc051-116">開発アプリケーション ライフ サイクル管理 (ALM) フロー</span><span class="sxs-lookup"><span data-stu-id="fc051-116">Development Application Lifecycle Management (ALM) flow</span></span>
<span data-ttu-id="fc051-117">コード カスタマイズをサンドボックスおよび製造環境に適用するには、ビルド環境から配置可能なコード パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc051-117">To apply code customizations to your sandbox and production environments, you need to create a deployable code package from your build environment.</span></span> <span data-ttu-id="fc051-118">これを行う方法の詳細については、[モデルの配置可能なパッケージを作成](create-apply-deployable-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc051-118">For details on how to do this, see [Create deployable packages of models](create-apply-deployable-package.md).</span></span>

## <a name="microsoft-updates"></a><span data-ttu-id="fc051-119">Microsoft の更新プログラム</span><span class="sxs-lookup"><span data-stu-id="fc051-119">Microsoft updates</span></span>
<span data-ttu-id="fc051-120">Microsoft の更新プログラムへのアクセスを取得するには、環境の環境詳細ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="fc051-120">To get access to Microsoft updates, go to the environment details page for your environment.</span></span> <span data-ttu-id="fc051-121">すべてのアプリケーションとプラットフォーム修正の累積的なバイナリ更新を示す **1 つのタイル** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-121">You will see a **single tile** that shows a cumulative, binary update of all the application and platform fixes.</span></span> <span data-ttu-id="fc051-122">この更新プログラムを適用するには、パッケージを選択して **パッケージの保存** を選択し、プロジェクト資産ライブラリに Microsoft の更新プログラムを保存します。</span><span class="sxs-lookup"><span data-stu-id="fc051-122">To apply this update, select the package and select **Save Package** to save the Microsoft update to the project asset library.</span></span>

## <a name="apply-updates"></a><span data-ttu-id="fc051-123">更新プログラムの適用</span><span class="sxs-lookup"><span data-stu-id="fc051-123">Apply updates</span></span>

### <a name="tier-1-sandboxdevelop-and-testdemobuild-environments"></a><span data-ttu-id="fc051-124">レベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境</span><span class="sxs-lookup"><span data-stu-id="fc051-124">Tier 1 Sandbox/Develop and Test/Demo/Build environments</span></span>

<span data-ttu-id="fc051-125">Lifecycle Services (LCS) を通じて配置されたレベル 1 サンドボックス/開発およびテスト/デモ/ビルド環境に更新を適用するには、[クラウド環境に更新を適用する](apply-deployable-package-system.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fc051-125">To apply updates to a Tier 1 Sandbox/Develop and Test/Demo/Build environment deployed through Lifecycle Services (LCS), follow the steps in  [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

### <a name="tier-2-and-above-standard-acceptance-testsandbox-environments"></a><span data-ttu-id="fc051-126">レベル 2 以上の標準引受テスト/サンドボックス環境</span><span class="sxs-lookup"><span data-stu-id="fc051-126">Tier 2 and above Standard Acceptance Test/Sandbox environments</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc051-127">パッケージを適用するとシステムのダウンタイムが発生します。</span><span class="sxs-lookup"><span data-stu-id="fc051-127">Applying packages causes system downtime.</span></span> <span data-ttu-id="fc051-128">すべて関連するサービスを停止、およびパッケージを適用中のときには環境を使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="fc051-128">All relevant services will be stopped, and you won't be able to use your environments while the package is being applied.</span></span>

<span data-ttu-id="fc051-129">開始する前に、配置可能パッケージが LCS のプロジェクト アセット ライブラリにアップロードされていることと、検証が成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="fc051-129">Before you begin, verify that the deployable package has been uploaded to the project asset library in LCS and that validations have succeeded.</span></span>

<span data-ttu-id="fc051-130">このパッケージをプロジェクト資産ライブラリに置いたら、次の手順を使用して環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="fc051-130">After you have this package in the project asset library, use the following steps to update your environment:</span></span>

1. <span data-ttu-id="fc051-131">パッケージを適用する環境の**環境の詳細**ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc051-131">Open the **Environment details** view for the environment where you want to apply the package.</span></span>
2. <span data-ttu-id="fc051-132">**メンテナンス > 更新プログラムの適用**をクリックし、更新プログラムを適用します。</span><span class="sxs-lookup"><span data-stu-id="fc051-132">Click **Maintain > Apply updates** to apply an update.</span></span>
3. <span data-ttu-id="fc051-133">パッケージを選択して適用します。</span><span class="sxs-lookup"><span data-stu-id="fc051-133">Select the package to apply.</span></span> <span data-ttu-id="fc051-134">上部にあるフィルターを使用してパッケージを探します。</span><span class="sxs-lookup"><span data-stu-id="fc051-134">Use the filter at the top to find your package.</span></span> <span data-ttu-id="fc051-135">アプリケーションおよびプラットフォーム バイナリ パッケージと、一覧のアセット ライブラリから検証に合格したアプリケーションの配置可能なパッケージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-135">You will see application and platform binary packages and application deployable packages that have passed validation from the asset library in the list.</span></span>
4. <span data-ttu-id="fc051-136">**適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc051-136">Click **Apply**.</span></span>
5. <span data-ttu-id="fc051-137">**環境の詳細** ビューの右上隅のステータスが **キュー** から **サービス** に代わり、完了した後は **配置済み** に変わります。</span><span class="sxs-lookup"><span data-stu-id="fc051-137">The status in the upper-right corner of the **Environment details** view changes from **Queued** to **Servicing**, and then after completion it changes to **Deployed**.</span></span>
6. <span data-ttu-id="fc051-138">完了すると、**環境の詳細** ページにある **履歴 > 環境**の変更からアクセスできる環境履歴が更新され、配置済みの完了したパッケージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc051-138">After completion, the environment history accessible from **History > Environment** changes on the **Environment details** page is updated to show the completed package deployed.</span></span>
7. <span data-ttu-id="fc051-139">環境履歴ページからログをダウンロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fc051-139">You can also download the logs from the environment history page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc051-140">最新のインフラストラクチャ スタックに配置された環境では、サービスが失敗した場合、環境が自動的にロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="fc051-140">For environments deployed in the modern infrastructure stack, if servicing fails, the environment is automatically rolled back.</span></span> <span data-ttu-id="fc051-141">工程が失敗した理由を理解するため、上記の手順に示されているとおりに環境の履歴ページからログをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="fc051-141">To understand why the operation failed, you can download the logs from the environment history page as mentioned in the steps above.</span></span>

### <a name="production-environments"></a><span data-ttu-id="fc051-142">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="fc051-142">Production environments</span></span>
<span data-ttu-id="fc051-143">運用環境に更新プログラムを適用することは、まだ有効になっていません。</span><span class="sxs-lookup"><span data-stu-id="fc051-143">Applying updates to production has not been enabled yet.</span></span> <span data-ttu-id="fc051-144">運用環境に適用する更新の信頼性を向上させるため、このフローが有効になると、最新のコピーとサンドボックス環境の指定されたスナップショットのどちらを運用環境に移動するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="fc051-144">To improve the reliability of updates being applied to production, when this flow is enabled you have the option to move either the latest copy or a designated snapshot of the sandbox environment to production.</span></span> <span data-ttu-id="fc051-145">更新を選択して、それを運用環境に移動する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="fc051-145">There is no way to select an update and move that to production.</span></span> <span data-ttu-id="fc051-146">これにより、更新がもう一度適用されなくなり、サンドボックスのイメージが運用環境に昇格されるため、エクスペリエンスの信頼性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="fc051-146">This ensures a more reliable experience as the update will not be applied again; rather an image of the sandbox will be promoted to production.</span></span>

