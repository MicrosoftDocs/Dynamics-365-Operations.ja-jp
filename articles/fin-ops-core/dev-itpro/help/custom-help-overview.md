---
title: カスタム ヘルプの概要
description: このトピックでは、ソリューションを反映するために Microsoft ヘルプ システムを拡張し、コンテンツを [ヘルプ] ウィンドウに接続する方法について説明します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: a681307c00cf027e7633e16b12334688e15f3a8d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752758"
---
# <a name="custom-help-overview"></a><span data-ttu-id="62b3a-103">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="62b3a-103">Custom Help overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62b3a-104">Finance and Operationsアプリは、多くの場合、組織のニーズに合わせてカスタマイズおよび拡張されます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-104">Finance and Operations apps are often customized and extended to fit an organization's needs.</span></span> <span data-ttu-id="62b3a-105">ソリューションが Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、または Dynamics 365 Commerce に基づいている場合、ソリューション固有および顧客固有のヘルプ コンテンツを Finance and Operations クライアントの [ヘルプ ウィンドウ](../../fin-ops/get-started/help-overview.md#in-product-help) に接続できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-105">If your solution is based on Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, or Dynamics 365 Commerce, you can connect solution-specific and customer-specific Help content to the [Help pane](../../fin-ops/get-started/help-overview.md#in-product-help) in the Finance and Operations client.</span></span> <span data-ttu-id="62b3a-106">このトピックでは、主要な手順と決定ポイントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-106">This topic describes the main steps and decision points.</span></span>

> [!NOTE]
> <span data-ttu-id="62b3a-107">Finance and Operations アプリのユーザーは、カスタム タスク ガイドを作成して、ソリューションの機能を説明する概念コンテンツを補うことができます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-107">Users of Finance and Operations apps can create custom task guides to supplement conceptual content that describes the functionality of their solution.</span></span> <span data-ttu-id="62b3a-108">これらの概念的な説明は、ヘルプとも呼ばれ、Microsoft、パートナー、および組織自体が提供できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-108">These conceptual descriptions are also referred to as Help and can be provided by Microsoft, partners, and an organization itself.</span></span> <span data-ttu-id="62b3a-109">詳細については、[ヘルプ システム](../../fin-ops/get-started/help-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-109">For more information, see [Help system](../../fin-ops/get-started/help-overview.md).</span></span>

<span data-ttu-id="62b3a-110">次の図およびこのトピック一般では、*ヘルプ* という用語を使用して、ハウツー ガイドを含めるか除外するかを概念的に説明します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-110">The following illustration, and this topic in general, use the term *Help* for conceptual descriptions that either include or exclude how-to guides.</span></span> <span data-ttu-id="62b3a-111">*タスク ガイド* という用語は、製品内のタスク ガイドを指します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-111">The term *task guides* refers to in-product task guides.</span></span>

![カスタマイズされたヘルプ ソリューションと [ヘルプ] ウィンドウ](../../fin-ops/get-started/media/help-architecture.png)

## <a name="custom-help-content"></a><span data-ttu-id="62b3a-113">カスタム ヘルプ コンテンツ</span><span class="sxs-lookup"><span data-stu-id="62b3a-113">Custom Help content</span></span>

<span data-ttu-id="62b3a-114">通常、カスタム ヘルプ コンテンツは、次の 3 つのソースのいずれかから生成されます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-114">Custom Help content typically originates from one of three sources:</span></span>

- <span data-ttu-id="62b3a-115">Microsoft ドキュメント リポジトリ</span><span class="sxs-lookup"><span data-stu-id="62b3a-115">Microsoft documentation repositories (repos)</span></span>

    <span data-ttu-id="62b3a-116">カスタム ヘルプ ツールキットの [HTMLFromRepoGenerator](custom-help-toolkit-HtmlFromRepoGenerator.md) ツールを使用して、任意の Finance and Operations リポジトリからコンテンツを複製し、対応する HTML ファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-116">You can use the [HTMLFromRepoGenerator](custom-help-toolkit-HtmlFromRepoGenerator.md) tool from the Custom Help Toolkit to clone content from any of the Finance and Operations repositories and generate corresponding HTML files.</span></span> <span data-ttu-id="62b3a-117">これらのファイルは、ソリューションに固有のコンテンツで更新できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-117">Those files can then be updated with content that is specific to your solution.</span></span>

- <span data-ttu-id="62b3a-118">既存のカスタマイズされた Dynamics AX コンテンツ</span><span class="sxs-lookup"><span data-stu-id="62b3a-118">Existing customized Dynamics AX content</span></span>

    <span data-ttu-id="62b3a-119">[Dynamics AX カスタム ヘルプ コンテンツを変換して、Dynamics 365 で使用できるようにする](migrate-dynamicsax2012.md) ことができます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-119">You can [convert Dynamics AX custom Help content so that it can be used in Dynamics 365](migrate-dynamicsax2012.md).</span></span>

- <span data-ttu-id="62b3a-120">ソリューションに対して特別に作成された HTML ファイル</span><span class="sxs-lookup"><span data-stu-id="62b3a-120">HTML files that are created specifically for your solution</span></span>

    <span data-ttu-id="62b3a-121">[メタデータの詳細](preparing-content.md#metadata) は、状況依存ヘルプと検索が正しく機能するために HTML ファイルに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b3a-121">[Learn more about the metadata](preparing-content.md#metadata) that must be added to your HTML files for context-sensitive Help and search to work correctly.</span></span>

## <a name="process"></a><span data-ttu-id="62b3a-122">処理</span><span class="sxs-lookup"><span data-stu-id="62b3a-122">Process</span></span>

<span data-ttu-id="62b3a-123">エンドツーエンド プロセスは、実際の顧客ソリューションとユーザーの期待によって異なります。</span><span class="sxs-lookup"><span data-stu-id="62b3a-123">The end-to-end process depends on the actual customer solution and the users' expectations.</span></span> <span data-ttu-id="62b3a-124">標準的なプロセスには、次の手順が含まれます:</span><span class="sxs-lookup"><span data-stu-id="62b3a-124">A typical process involves the following steps:</span></span>

1. <span data-ttu-id="62b3a-125">カスタム ヘルプ コンテンツを作成します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-125">Create the custom Help content.</span></span>
2. <span data-ttu-id="62b3a-126">コンテンツを Web サイト に公開します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-126">Publish the content on a website.</span></span>
3. <span data-ttu-id="62b3a-127">検索サービスを使用してコンテンツにインデックスを付けます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-127">Index the content by using a search service.</span></span>
4. <span data-ttu-id="62b3a-128">カスタム **ヘルプ** ウィンドウを Web サイト と検索サービスに接続します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-128">Connect the custom **Help** pane to the website and the search service.</span></span>

<span data-ttu-id="62b3a-129">Microsoft は、Microsoft Help リポジトリから HTML ファイルを生成し、検索サービス用の JavaScript Object Notation (JSON) ファイルを生成して、HTML ファイルのロケールを変更し、ソリューションのロケールに一致するようにする [ツールキット](custom-help-toolkit.md) を提供します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-129">Microsoft provides a [toolkit](custom-help-toolkit.md) that can help you generate HTML files from the Microsoft Help repositories, generate JavaScript Object Notation (JSON) files for search services, and change the locale of HTML files so that it matches the locale of your solution.</span></span>

<span data-ttu-id="62b3a-130">ページ下部のリンクからこのドキュメントに寄稿するか、[Dynamics 365 コミュニティ](https://community.dynamics.com/) に参加して、知識を共有してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-130">You're welcome to share your knowledge by contributing to this documentation through the link at the bottom of the page or by joining the [Dynamics 365 community](https://community.dynamics.com/).</span></span>

<span data-ttu-id="62b3a-131">次の表は、ヘルプ エクスペリエンスを構成するために管理者が通常持つ主な目的の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-131">The following table outlines the main objectives that admins typically have for configuring the Help experience.</span></span>

| <span data-ttu-id="62b3a-132">目標</span><span class="sxs-lookup"><span data-stu-id="62b3a-132">Objective</span></span> | <span data-ttu-id="62b3a-133">詳細情報</span><span class="sxs-lookup"><span data-stu-id="62b3a-133">Learn more</span></span> |
|-----------|------------|
| <span data-ttu-id="62b3a-134">実際のソリューションを反映した、カスタマイズされた製品内ヘルプ エクスペリエンスをユーザーに提供したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-134">I want to give my users a customized in-product Help experience that reflects their actual solution.</span></span> | <span data-ttu-id="62b3a-135">このトピックの [カスタム ヘルプ Web サイト](#custom-help-sites) セクションと、[タスク レコーダーを使用したドキュメントやトレーニングの作成](../user-interface/task-recorder-training-docs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-135">See the [Custom Help websites](#custom-help-sites) section of this topic and [Create documentation or training with Task Recorder](../user-interface/task-recorder-training-docs.md).</span></span> |
| <span data-ttu-id="62b3a-136">Microsoft Help コンテンツをソリューションに固有の Help コンテンツのベースラインとして使用したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-136">I want to use the Microsoft Help content as a baseline for Help content that is specific to my solution.</span></span> | <span data-ttu-id="62b3a-137">[カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール](custom-help-toolkit-HtmlFromRepoGenerator.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-137">See [Custom Help Toolkit: The HtmlFromRepoGenerator tool](custom-help-toolkit-HtmlFromRepoGenerator.md).</span></span> |
| <span data-ttu-id="62b3a-138">Microsoft Help コンテンツに寄稿したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-138">I want to contribute to the Microsoft Help content.</span></span> | <span data-ttu-id="62b3a-139">[ヘルプの拡張、カスタマイズ、および共同作業](contributor-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-139">See [Extend, customize, and collaborate on the Help](contributor-guide.md).</span></span> |
| <span data-ttu-id="62b3a-140">既存の Dynamics AX コンテンツを再利用したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-140">I want to reuse my existing Dynamics AX content.</span></span> | <span data-ttu-id="62b3a-141">[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-141">See [Convert Dynamics AX custom Help for use in Dynamics 365](migrate-dynamicsax2012.md).</span></span> |
| <span data-ttu-id="62b3a-142">ヘルプ コンテンツの Web サイト を設定したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-142">I want to set up a website for my Help content.</span></span> | <span data-ttu-id="62b3a-143">このトピックの [カスタム ヘルプ Web サイト](#custom-help-sites) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-143">See the [Custom Help websites](#custom-help-sites) section of this topic.</span></span> |
| <span data-ttu-id="62b3a-144">コンテンツを **ヘルプ** ウィンドウに追加したい。</span><span class="sxs-lookup"><span data-stu-id="62b3a-144">I want to add my content to the **Help** pane.</span></span> | <span data-ttu-id="62b3a-145">[カスタム ヘルプ Web サイトを ヘルプ ウィンドウに接続する](connect-help-pane.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-145">See [Connect a custom Help website to the Help pane](connect-help-pane.md).</span></span> |
| <span data-ttu-id="62b3a-146">テクニカル ライターは、以前のコンテンツを Markdown に変換して、Microsoft コンテンツをカスタマイズしやすくするためのガイダンスを必要としています。</span><span class="sxs-lookup"><span data-stu-id="62b3a-146">Our technical writers want guidance that will help them convert our earlier content into Markdown so that it becomes easier for them to customize the Microsoft content.</span></span> | <span data-ttu-id="62b3a-147">[Markdown への移行](migrate-dynamicsax2012.md#moving-to-markdown) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-147">See [Moving to Markdown](migrate-dynamicsax2012.md#moving-to-markdown).</span></span> |

## <a name="custom-help-websites"></a><a name="custom-help-sites"></a><span data-ttu-id="62b3a-148">カスタム ヘルプ Web サイト</span><span class="sxs-lookup"><span data-stu-id="62b3a-148">Custom Help websites</span></span>

<span data-ttu-id="62b3a-149">製品がヘルプ コンテンツに接続する前に、製品内の **ヘルプ** ウィンドウをカスタマイズして、コンテンツが表示されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b3a-149">Before the product can connect to your Help content, you must customize the in-product **Help** pane so that it shows your content.</span></span> <span data-ttu-id="62b3a-150">次の条件を満たす必要があります:</span><span class="sxs-lookup"><span data-stu-id="62b3a-150">The following conditions must be met:</span></span>

- <span data-ttu-id="62b3a-151">コンテンツは Web サイト で入手可能である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b3a-151">Your content must be available on a website.</span></span>

    <span data-ttu-id="62b3a-152">コンテンツを既存の Web サイト に展開するか、コンテンツをホストする専用の Web サイト を設定できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-152">You can deploy your content to an existing website, or you can set up a dedicated website to host your content.</span></span> <span data-ttu-id="62b3a-153">Web サイトは非公開でも公開でもかまいませんが、ユーザーがコンテンツにアクセスするためサインインする必要は **ない** ことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="62b3a-153">The website can be private or public, but we recommend that users **not** be required to sign in to access your content.</span></span>

- <span data-ttu-id="62b3a-154">コンテンツには、検索サービスでインデックス付けされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b3a-154">Your content must be indexed by a search service.</span></span>

    <span data-ttu-id="62b3a-155">状況依存ヘルプの [カスタム ヘルプ ツールキット](custom-help-toolkit.md) の一部である [AzureSearchCustomHelp](walkthrough-help-azure.md) ソリューションを使用する場合、**ヘルプ** ウィンドウは、検索サービスのインデックスに対して実行する必要があるクエリを生成します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-155">If you use the [AzureSearchCustomHelp](walkthrough-help-azure.md) solution that is part of the [Custom Help Toolkit](custom-help-toolkit.md) for context-sensitive Help, the **Help** pane will generate a query that must be run against the search service's index.</span></span> <span data-ttu-id="62b3a-156">クエリは、ヘルプ トピックの特定のメタデータに依存します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-156">The query depends on specific metadata in the Help topics.</span></span> <span data-ttu-id="62b3a-157">詳細については、[カスタム ヘルプ トピックのメタデータ要件](preparing-content.md#metadata) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-157">For more information, see [Metadata requirements for custom Help topics](preparing-content.md#metadata).</span></span>

<span data-ttu-id="62b3a-158">[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md) トピックでは、Azure でコンテンツをホストするためのアプローチについて説明します。</span><span class="sxs-lookup"><span data-stu-id="62b3a-158">The [Deploy custom Help to Azure](walkthrough-help-azure.md) topic describes an approach for hosting content on Azure.</span></span> <span data-ttu-id="62b3a-159">製品内の **ヘルプ** ウィンドウで検索できるように、コンテンツにインデックス付けする検索サービスの設定方法に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62b3a-159">It includes information about how to set up a search service that indexes your content so that it can be found by the in-product **Help** pane.</span></span> <span data-ttu-id="62b3a-160">[Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing) をお持ちでない場合は、始める前にアカウントを作成してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-160">If you don't have an [Azure subscription](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing), create an account before you begin.</span></span> <span data-ttu-id="62b3a-161">12 か月間は無料のアカウントで開始できます。</span><span class="sxs-lookup"><span data-stu-id="62b3a-161">You can start with a free account for 12 months.</span></span> <span data-ttu-id="62b3a-162">詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b3a-162">For more information, see [Create your Azure free account today](https://azure.microsoft.com/free/).</span></span>

## <a name="see-also"></a><span data-ttu-id="62b3a-163">参照</span><span class="sxs-lookup"><span data-stu-id="62b3a-163">See also</span></span>

<span data-ttu-id="62b3a-164">[カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する](connect-help-pane.md)</span><span class="sxs-lookup"><span data-stu-id="62b3a-164">[Connect a custom Help website to the Help pane](connect-help-pane.md)</span></span>  
[<span data-ttu-id="62b3a-165">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="62b3a-165">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
[<span data-ttu-id="62b3a-166">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="62b3a-166">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="62b3a-167">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="62b3a-167">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="62b3a-168">Finance and Operations アプリのヘルプ エクスペリエンスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="62b3a-168">Configure the Help experience for Finance and Operations apps</span></span>](../../fin-ops/get-started/help-connect.md)  
[<span data-ttu-id="62b3a-169">ヘルプ システム</span><span class="sxs-lookup"><span data-stu-id="62b3a-169">Help system</span></span>](../../fin-ops/get-started/help-overview.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]