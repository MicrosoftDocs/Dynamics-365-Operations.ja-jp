---
title: Dynamics 365 Commerce での実験
description: 実験により、サイト ビルダーでのページ レイアウトの作成、編集、管理、およびコンテンツの処理が可能になります。 エンド ツー エンドの実験サポートは、E コマース ページおよびページ内のエンティティに対して有効になります。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413892"
---
# <a name="experimentation-in-dynamics-365-commerce"></a><span data-ttu-id="79aa3-104">Dynamics 365 Commerce での実験</span><span class="sxs-lookup"><span data-stu-id="79aa3-104">Experimentation in Dynamics 365 Commerce</span></span>
<span data-ttu-id="79aa3-105">Dynamics 365 Commerce での実験を使用して、E コマース ページの有効性についての仮想を検証し、データ駆動型信頼とともに決定を行います。</span><span class="sxs-lookup"><span data-stu-id="79aa3-105">Use experimentation in Dynamics 365 Commerce to validate hypotheses about the effectiveness of your e-Commerce pages and make decisions with data-driven confidence.</span></span> <span data-ttu-id="79aa3-106">Commerce では、ページ、モジュール、およびフラグメントの A/B テストをサポートしており、Web サイトに提案された変更の影響を測定できます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-106">Commerce supports A/B testing on pages, modules, and fragments and enables you to measure the impact of proposed changes to your website.</span></span>

<span data-ttu-id="79aa3-107">コマース サイト ビルダーでは、ページの作成、編集、管理および **バリエーション** と呼ばれるコンテンツの処理を行なえます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-107">You can create, edit, and manage page and content treatments known as **variations** in Commerce site builder.</span></span> <span data-ttu-id="79aa3-108">Commerce は、実験や処理の割り当てを作成するために使用できるサード パーティ サービスと統合します。</span><span class="sxs-lookup"><span data-stu-id="79aa3-108">Commerce integrates with third-party services that you can use to create experiments and treatment assignments.</span></span> <span data-ttu-id="79aa3-109">Commerce でキャプチャされた Real-time イベント ストリームは、サード パーティ サービスで実験結果を定義する分析を有効にします。</span><span class="sxs-lookup"><span data-stu-id="79aa3-109">Real-time event streams captured in Commerce enable the analytics that define the experiment results in the third-party service.</span></span> <span data-ttu-id="79aa3-110">その後、仮想のサポートまたは反論を支援するために、これらの分析を活用できます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-110">You can then leverage these analytics to help support or refute your hypothesis.</span></span>

## <a name="set-up-prerequisites"></a><span data-ttu-id="79aa3-111"> 前提条件の設定</span><span class="sxs-lookup"><span data-stu-id="79aa3-111">Set up prerequisites</span></span>
1. <span data-ttu-id="79aa3-112">**Commerce の適切なバージョンの入手** - モジュール ライブラリ、オンライン チャネル拡張ソフトウェア開発キット (SDK)、および Commerce Scale Unit を Commerce バージョン 10.0.13 以降にアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="79aa3-112">**Get the correct version of Commerce** - Upgrade your module library, online channel extensibility software development kit (SDK), and Commerce Scale Unit to Commerce version 10.0.13 or later.</span></span>
1. <span data-ttu-id="79aa3-113">**実験コネクタの設定** - 実験コネクタは、Commerce がサード パーティ サービスと接続して実験のリストを取得し、実験をユーザーに対して表示するタイミングを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-113">**Set up an experimentation connector** - An experimentation connector allows Commerce to connect with third-party services to retrieve the list of experiments and determine when to show an experiment to a user.</span></span> <span data-ttu-id="79aa3-114">サード パーティ コネクタは、[AppSource](https://appsource.microsoft.com) から購入できます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-114">You can purchase a third-party connector from [AppSource](https://appsource.microsoft.com).</span></span> <span data-ttu-id="79aa3-115">発行元が提供する設定手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="79aa3-115">Follow the setup instructions provided by the publisher.</span></span> <span data-ttu-id="79aa3-116">あるいは、Commerce からのサンプル テスト コネクタを使用して、外部サービスを構成する必要なく、実験ワークフローをテストすることもできます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-116">You can alternatively use the sample test connector from Commerce to test the experimentation workflow without needing to configure an external service.</span></span> <span data-ttu-id="79aa3-117">詳細については、[コネクタのコンフィギュレーションと有効化](e-commerce-extensibility/connectors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79aa3-117">For more information, see [Configure and enable connectors](e-commerce-extensibility/connectors.md).</span></span> 
1. <span data-ttu-id="79aa3-118">**Commerce で実験機能のフラグをオンにする** - テナント レベルでの実験を有効にするには、**テナントの設定 > 機能** または **サイト設定 > 機能** のサイト レベルに移動します。</span><span class="sxs-lookup"><span data-stu-id="79aa3-118">**Turn on the experimentation feature flags in Commerce** - You can enable experimentation at the tenant level by going to **Tenant Settings > Features** or at the site level at **Site Settings > Features**.</span></span>
    - <span data-ttu-id="79aa3-119">実験の一部ではない他のコンテンツに影響を与えたりコピーしたりせずに、ページ内にモジュールの実験バリエーションを作成するために **実験** フラグを有効にします。</span><span class="sxs-lookup"><span data-stu-id="79aa3-119">Enable the **Experimentation** flag to create experiment variations of modules within a page without affecting or copying other content that isn't part of the experiment.</span></span> <span data-ttu-id="79aa3-120">これにより、実験のライフサイクルの間、実験外で進行中のコンテンツの更新は確実に同期を維持します。</span><span class="sxs-lookup"><span data-stu-id="79aa3-120">This ensures that ongoing content updates outside the experiment stay in sync during the experiment lifecycle.</span></span> <span data-ttu-id="79aa3-121">このフラグを無効にすると、すべての実験がユーザーに表示されなくなり、サイト ビルダー内のすべての編集機能が削除されます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-121">Disabling this flag stops all experiments from being shown to users and removes all editing functions within site builder.</span></span>
    - <span data-ttu-id="79aa3-122">ページまたはフラグメントでの実験を実行するために、**ページまたはフラグメントでの実験** フラグを有効にします。</span><span class="sxs-lookup"><span data-stu-id="79aa3-122">Enable the **Experiment on pages or fragments** flag to run experiments on a page or fragment.</span></span> <span data-ttu-id="79aa3-123">これにより、ページまたはフラグメント内のページ全体のフル インスタンス コピーまたはすべてのモジュールのフラグメントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-123">This creates a full instance copy of the entire page or fragment for all modules within the page or fragment.</span></span> <span data-ttu-id="79aa3-124">包括的なコンテンツの変更をテストする場合、またはインスタンス間で進行中のコンテンツの変更を同期することが問題にならない場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="79aa3-124">Use this mode when you want to test comprehensive content changes, or where synchronizing ongoing content changes across instances isn't a concern.</span></span> <span data-ttu-id="79aa3-125">このフラグを無効にすると、ページおよびフラグメントの新しい実験を作成および編集ができなくなります。</span><span class="sxs-lookup"><span data-stu-id="79aa3-125">Disabling this flag prevents creation and editing of new experiments on pages and fragments.</span></span>
    > [!NOTE]
    > <span data-ttu-id="79aa3-126">**ページまたはフラグメントでの実験** 機能の実行には、**実験** フラグを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79aa3-126">The **Experimentation** flag must also be enabled for the **Experiment on pages or fragments** functionality to work.</span></span>
    
## <a name="experimentation-lifecycle"></a><span data-ttu-id="79aa3-127">実験ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="79aa3-127">Experimentation lifecycle</span></span>
<span data-ttu-id="79aa3-128">実験の設定、バリエーションの作成、および実験の実行は、反復プロセスです。</span><span class="sxs-lookup"><span data-stu-id="79aa3-128">Setting up an experiment, creating variations, and running an experiment is an iterative process.</span></span> <span data-ttu-id="79aa3-129">次の図は、Commerce およびサード パーティ サービスでの実験ライフサイクルを示しています。</span><span class="sxs-lookup"><span data-stu-id="79aa3-129">The diagram below illustrates the experimentation lifecycle in Commerce and the third-party service.</span></span> 

<span data-ttu-id="79aa3-130">[ ![実験ライフサイクル](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="79aa3-130">[ ![Experimentation lifecycle](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)</span></span>

<span data-ttu-id="79aa3-131">実験プロセスの各手順の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="79aa3-131">To learn more about each step in the experimentation process, refer to the following topics.</span></span>
- [<span data-ttu-id="79aa3-132">仮説を識別して実験のメトリックスを決定する</span><span class="sxs-lookup"><span data-stu-id="79aa3-132">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md)
- [<span data-ttu-id="79aa3-133">実験の設定</span><span class="sxs-lookup"><span data-stu-id="79aa3-133">Set up an experiment</span></span>](experimentation-setup.md)
- [<span data-ttu-id="79aa3-134">接続して実験を編集する</span><span class="sxs-lookup"><span data-stu-id="79aa3-134">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
- [<span data-ttu-id="79aa3-135">実験のプレビューと発行</span><span class="sxs-lookup"><span data-stu-id="79aa3-135">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
- [<span data-ttu-id="79aa3-136">実験の実行と監視</span><span class="sxs-lookup"><span data-stu-id="79aa3-136">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
- [<span data-ttu-id="79aa3-137">バリエーションのレベルを上げて実験を完了する</span><span class="sxs-lookup"><span data-stu-id="79aa3-137">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)

> [!NOTE]
> <span data-ttu-id="79aa3-138">実験がライフサイクルのどこにあるかを知るには、サイト ビルダーの左側ナビゲーション ペインにある **実験** を選択します。</span><span class="sxs-lookup"><span data-stu-id="79aa3-138">To learn where an experiment is in the lifecycle, select **Experiments** in the left navigation pane of site builder.</span></span> <span data-ttu-id="79aa3-139">実験のリストが、Commerce およびサード パーティ サービス両方の各実験のステータスと共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="79aa3-139">A list of experiments is displayed with the status of each experiment in both Commerce and the third-party service.</span></span> <span data-ttu-id="79aa3-140">詳細については、[実験のステータスを確認する](experimentation-status.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79aa3-140">For more information, see [Review the status of an experiment](experimentation-status.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="79aa3-141">次のステップ</span><span class="sxs-lookup"><span data-stu-id="79aa3-141">Next step</span></span>
[<span data-ttu-id="79aa3-142">仮想を識別して実験の成功メトリックを決定する</span><span class="sxs-lookup"><span data-stu-id="79aa3-142">Identify a hypothesis and determine success metrics for an experiment</span></span>](experimentation-identify.md) 
