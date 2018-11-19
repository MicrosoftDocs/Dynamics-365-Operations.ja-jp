---
title: "Finance and Operations のヘルプ システム"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のヘルプ システム コンポーネントの概要が示されます。 また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。"
author: margoc
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 75be5c5f675885aececb8ac0b25e699882ea77ab
ms.openlocfilehash: dc2a3d49041acf42814149eb71d4cc021bdad838
ms.contentlocale: ja-jp
ms.lasthandoff: 10/17/2018

---

# <a name="finance-and-operations-help-system"></a><span data-ttu-id="8c0e1-104">Finance and Operations のヘルプ システム</span><span class="sxs-lookup"><span data-stu-id="8c0e1-104">Finance and Operations Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c0e1-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のヘルプ システム コンポーネントの概要が示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-105">This topic provides an overview of the components of the Microsoft Dynamics 365 for Finance and Operations Help system.</span></span> <span data-ttu-id="8c0e1-106">また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-106">It also explains how you can provide custom documentation and training to your organization.</span></span> 

> [!NOTE] 
> <span data-ttu-id="8c0e1-107">次の製品間には密接な関係があります: Dynamics 365 for Finance and Operations、Dynamics 365 for Retail、および Dynamics 365 for Talent。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-107">The following products are closely related: Dynamics 365 for Finance and Operations; Dynamics 365 for Retail; and Dynamics 365 for Talent.</span></span> <span data-ttu-id="8c0e1-108">すべての 3 つの製品上に同じ機能が表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-108">The same functionality may appear in all 3 products.</span></span> <span data-ttu-id="8c0e1-109">結果として、主に [Retail] に関連するトピックでの製品名は Dynamics 365 for Retail、主に [Talent] に関連するトピックでの製品名は Dynamics 365 for Talent、コア製品に関連するトピックでの製品名は、Dynamics 365 for Finance and Operations となります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-109">As a result, in topics that are primarily related to Retail, the product name will be Dynamics 365 for Retail; in topics that are primarily related to Talent, the product name will be Dynamics 365 for Talent; and in topics that are related to the core product, the product name will be Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="8c0e1-110">1 つの製品で記述されているトピックは、関連する製品の同じ機能にも当てはまる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-110">Topics that are written for one product may apply to the same functionality in a related product.</span></span>

<span data-ttu-id="8c0e1-111">ヘルプ システムは、次の製品により共有されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-111">The Help system is shared by the following products:</span></span>
- <span data-ttu-id="8c0e1-112">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8c0e1-112">Dynamics 365 for Finance and Operations</span></span>
- <span data-ttu-id="8c0e1-113">Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="8c0e1-113">Dynamics 365 for Retail</span></span>
- <span data-ttu-id="8c0e1-114">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="8c0e1-114">Dynamics 365 for Talent</span></span>

<span data-ttu-id="8c0e1-115">Finance and Operations には、2 つの主要なコンポーネントに基づくまったく新しいヘルプ システムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-115">Finance and Operations includes a Help system that is based on two main components:</span></span>

-   <span data-ttu-id="8c0e1-116">ドキュメント サイト</span><span class="sxs-lookup"><span data-stu-id="8c0e1-116">A documentation site</span></span>
-   <span data-ttu-id="8c0e1-117">タスク ガイド</span><span class="sxs-lookup"><span data-stu-id="8c0e1-117">Task guides</span></span>

<span data-ttu-id="8c0e1-118">使用している製品のヘルプ ウィンドウからヘルプを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-118">You can access help from the Help pane in whichever product you are using.</span></span> <span data-ttu-id="8c0e1-119">次のスクリーンショットは、Finance and Operations を示します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-119">The following screenshot shows Finance and Operations.</span></span>

![[ヘルプ] ウィンドウ](./media/help-pane-ops-task-guides.png)

<span data-ttu-id="8c0e1-121">このトピックは、ヘルプ システムについて説明し、組織のカスタム ドキュメントおよびトレーニング リソースを作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-121">This topic describes the Help system, and explains how you can create custom documentation and training resources for your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c0e1-122">**タスク ガイド**は、Retail または Talent のヘルプ ウィンドウで現在使用できません (いくつかのタスク ガイドは、Talent のはじめにウィンドウで使用できます)。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-122">**Task guides** are not currently available for Retail, or in the Help pane for Talent (a few task guides are available in the Getting Started pane for Talent).</span></span> <span data-ttu-id="8c0e1-123">Retail および Talent 両方の手順を追ったヘルプは、docs.microsoft.com サイト上 ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-123">Procedural help is available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

## <a name="help-on-docsmicrosoftcom"></a><span data-ttu-id="8c0e1-124">docs.microsoft.com のヘルプ</span><span class="sxs-lookup"><span data-stu-id="8c0e1-124">Help on docs.microsoft.com</span></span>

<span data-ttu-id="8c0e1-125">docs.microsoft.com サイト ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) が Finance and Operations の製品ドキュメントの基本ソースです。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-125">The docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) is the primary source of product documentation for Finance and Operations.</span></span> <span data-ttu-id="8c0e1-126">サイトには次のような機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-126">The site offers the following features:</span></span>

-   <span data-ttu-id="8c0e1-127">**最新のコンテンツへのアクセス** – サイトは、製品のドキュメントのより速い、より柔軟な作成、出荷、および更新方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-127">**Access to the most up-to-date content** – The site gives us a faster and more flexible way to create, deliver, and update product documentation.</span></span> <span data-ttu-id="8c0e1-128">したがって、最新の技術情報にアクセスできることを確実にするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-128">Therefore, it helps to ensure that you have access to the latest technical information.</span></span>
-   <span data-ttu-id="8c0e1-129">**専門家が記述した内容** – サイトは Microsoft 内外のコミュニティ メンバーによって拡張できる豊富な製品ドキュメントのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-129">**Content that is written by experts** – The site provides a richer set of product documentation that can be enhanced by community members both inside and outside Microsoft.</span></span>
-   <span data-ttu-id="8c0e1-130">**異なるタイプのコンテンツへのアクセス**– サイトにより、タスク ガイド、ビデオ、トピックなど、Finance and Operations に関する異なる内容にすばやくアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-130">**Access to different types of content** – The site lets you quickly access different types of content about Finance and Operations, such as task guides, videos, and topics.</span></span>
-   <span data-ttu-id="8c0e1-131">**業務プロセスをサポートするコンテンツ** – サイトには Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) を活用する、業務プロセス指向のコンテンツが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-131">**Content that supports your business processes** – The site includes business process–focused content that takes advantage of the Business Process Modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="searching-on-docsmicrosoftcom"></a><span data-ttu-id="8c0e1-132">docs.microsoft.com での検索</span><span class="sxs-lookup"><span data-stu-id="8c0e1-132">Searching on docs.microsoft.com</span></span>
<span data-ttu-id="8c0e1-133">コンテンツを検索する方法について多くの質問が寄せられています。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-133">We get a lot of questions about how to search for our content.</span></span> <span data-ttu-id="8c0e1-134">当サイトでは、Finance and Operations に関するページから始めると、検索の範囲は Finance and Operations のコンテンツに限定されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-134">On our site, if you start from a page about Finance and Operations, we scope your search to just be for Finance and Operations content.</span></span> <span data-ttu-id="8c0e1-135">範囲を解除するには、検索ボックスの Unified Operations の横にある X をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-135">You can remove the scoping by clicking the X next to Unified Operations in the search box.</span></span> 

![検索](./media/search-scope-2.png)

<span data-ttu-id="8c0e1-137">任意の検索エンジンを使ってコンテンツを探すこともできます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-137">You can also find our content with any search engine.</span></span> <span data-ttu-id="8c0e1-138">最適な結果を得るには、次のようなサイト検索を使用することをお勧めします: site:docs.microsoft.com dynamics 365 "検索用語"。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-138">We recommend that for best results, you use a site search, such as site:docs.microsoft.com dynamics 365 "search term".</span></span>  

### <a name="the-docsmicrosoftcom-table-of-contents"></a><span data-ttu-id="8c0e1-139">docs.microsoft.com の目次</span><span class="sxs-lookup"><span data-stu-id="8c0e1-139">The docs.microsoft.com table of contents</span></span>
<span data-ttu-id="8c0e1-140">Finance and Operations、および Retail のすべては docs サイトの 単一の目次を共有し、顧客がトピックのコンテキストを確認できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-140">Finance and Operations and Retail all share a single table of contents on the docs site, which enables customers to see the context of the topic they are in.</span></span> <span data-ttu-id="8c0e1-141">また、目次上のフィルタコントロールを使用して、探しているトピックを検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-141">It also enables you to use the Filter control above the table of contents to find topics that you are looking for.</span></span> 

<span data-ttu-id="8c0e1-142">他の Dynamics 365 製品を検索するか、またはサイトの階層リンクをクリックしてハブ ページにアクセスすることでヘルプを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-142">You can get help on other Dynamics 365 products by searching for them, or by clicking Dynamics 365 in the site breadcrumb to get to our hub page.</span></span> 

### <a name="use-an-rss-feed"></a><span data-ttu-id="8c0e1-143">RSS フィードを使用します</span><span class="sxs-lookup"><span data-stu-id="8c0e1-143">Use an RSS feed</span></span>
<span data-ttu-id="8c0e1-144">Unified Operations のコンテンツへのすべての更新の RSS フィードを購読するには、Internet Explorer や RSS フィード マネージャなどの RSS フィードをサポートするブラウザから次のリンクを使用します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-144">To subscribe to an RSS feed of all updates to the Unified Operations content, use the following link from a browser that supports RSS feeds, such as Internet Explorer, or an RSS feed manager:</span></span> 

<span data-ttu-id="8c0e1-145">[RSS フィード](https://docs.microsoft.com/api/search/rss?locale=en-us&$filter=scopes%2Fany(t%3A%20t%20eq%20%27Unified%20Operations%27))</span><span class="sxs-lookup"><span data-stu-id="8c0e1-145">[RSS feed](https://docs.microsoft.com/api/search/rss?locale=en-us&$filter=scopes%2Fany(t%3A%20t%20eq%20%27Unified%20Operations%27))</span></span>

### <a name="give-feedback"></a><span data-ttu-id="8c0e1-146">フィードバックを送る</span><span class="sxs-lookup"><span data-stu-id="8c0e1-146">Give feedback</span></span> 
<span data-ttu-id="8c0e1-147">お客様からのフィードバックをぜひいただきたいです。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-147">We really like customer feedback.</span></span> <span data-ttu-id="8c0e1-148">GitHub を通じて、コメントを投稿したり、コンテンツへの変更を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-148">You can either comment or suggest changes to our content through GitHub.</span></span> <span data-ttu-id="8c0e1-149">フィードバック システムの詳細については、[このブログ投稿](https://docs.microsoft.com/teamblog/a-new-feedback-system-is-coming-to-docs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-149">For more information about our feedback system, see [this blog post](https://docs.microsoft.com/teamblog/a-new-feedback-system-is-coming-to-docs).</span></span>

##### <a name="leave-us-feedback"></a><span data-ttu-id="8c0e1-150">フィードバックをお送りください</span><span class="sxs-lookup"><span data-stu-id="8c0e1-150">Leave us feedback</span></span> 
<span data-ttu-id="8c0e1-151">フィードバックまたはトピックに関するご質問がある場合は、ページ下部にコメントを記入してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-151">If you have feedback or questions about a topic, leave us a comment at the bottom of the page.</span></span>  

1. <span data-ttu-id="8c0e1-152">**フィードバック**をクリックしてページ下部のコメントに移動し、**製品のフィードバック**、または**サインインしてフィードバックを送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-152">Click **Feedback** to get to the comments at the bottom of the page, and then click either **Product feedback**, or **Sign in to give documentation feedback**.</span></span>

![フィードバック](./media/comments.png)

2. <span data-ttu-id="8c0e1-154">コメントを入力して、**フィードバックを送信**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-154">Start typing your comments, and then click **Submit feedback**.</span></span>

![コメントを投稿](./media/feedback.png)



##### <a name="suggest-a-change-or-contribute-content-through-github"></a><span data-ttu-id="8c0e1-156">GitHub を通じてコンテンツの変更や提案を投稿する</span><span class="sxs-lookup"><span data-stu-id="8c0e1-156">Suggest a change or contribute content through GitHub</span></span>
<span data-ttu-id="8c0e1-157">変更を提案するには、GitHub アカウントを所有し、コントリビューター ライセンス契約に署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-157">To suggest a change, you'll need to have a GitHub account, and sign a Contributor License Agreement.</span></span>  <span data-ttu-id="8c0e1-158">プル要求が送信された後、提案された変更が確認されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-158">After you submit a pull request, we'll review your proposed changes.</span></span> <span data-ttu-id="8c0e1-159">必要に応じて、内部的に検討してから返答します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-159">If necessary, we'll discuss them internally, and then get back to you.</span></span>  

<span data-ttu-id="8c0e1-160">開始するには、トピックの**編集** (鉛筆) ボタンをクリック、または https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public にあるリポジトリへ移動します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-160">To get started, click the **Edit** (pencil) button on a topic, or go to our repo at https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public.</span></span> 

<span data-ttu-id="8c0e1-161">詳細については、https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/live/CONTRIBUTING.md にある寄稿者のガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-161">For more information, please refer to our contributor's guide: https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/live/CONTRIBUTING.md.</span></span> 


> [!NOTE]
> <span data-ttu-id="8c0e1-162">現時点では英語のコンテンツ セットへの寄稿のみを受け付けています。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-162">We only accept contributions to our English content set at this time.</span></span>  


## <a name="task-guides"></a><span data-ttu-id="8c0e1-163">タスク ガイド</span><span class="sxs-lookup"><span data-stu-id="8c0e1-163">Task guides</span></span>
<span data-ttu-id="8c0e1-164">タスク ガイドは、制御された、ガイド付きでインタラクティブな方法による、タスクまたは業務プロセスの手順の説明です。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-164">A Task guide is a controlled, guided, interactive experience that leads you through the steps of a task, or business process.</span></span> <span data-ttu-id="8c0e1-165">[ヘルプ] ウィンドウからタスク ガイドを開く (再生する) ことができます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-165">You can open (play) a Task guide from the Help pane.</span></span> <span data-ttu-id="8c0e1-166">最初にタスク ガイドをクリックすると、[ヘルプ] ウィンドウには、タスクのステップ バイ ステップの手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-166">When you first click a Task guide, the Help pane will show the step-by-step instructions for the task.</span></span> <span data-ttu-id="8c0e1-167">ローカライズされたタスク ガイドが利用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-167">Localized Task guides are now available.</span></span> 

<span data-ttu-id="8c0e1-168">Microsoftは、 2017 年 12 月 までの Finance and Operations のリリースのタスク ガイド ライブラリを出荷しました。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-168">Microsoft shipped task guide libraries for releases through December 2017 for Finance and Operations.</span></span> <span data-ttu-id="8c0e1-169">[ヘルプ ウィンドウからタスク ガイドへのアクセス](help-overview.md#accessing-task-guides-from-the-help-pane)セクションでは、製品の正しいタスク ガイドを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-169">The section [Accessing Task guides from the Help pane](help-overview.md#accessing-task-guides-from-the-help-pane) describes how to find the correct task guides for your product.</span></span> 

![タスク ガイドの読み取りビュー](./media/task-guide-ops.png)

<span data-ttu-id="8c0e1-171">ガイドのあるインタラクティブな経験を開始するには、[ヘルプ] ページ下部の **タスク ガイドの開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-171">To begin the guided, interactive experience, click **Start task guide** at the bottom of the Help pane.</span></span> <span data-ttu-id="8c0e1-172">黒のポインタが、実行する必要があるアクションを開いて、表示します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-172">A black pointer opens and indicates the action that you must perform.</span></span> <span data-ttu-id="8c0e1-173">UI に表示される指示に従い、指示されたデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-173">Follow the directions that appear in the UI, and enter data as directed.</span></span> 

![タスク ガイドの手順書](./media/task-guide-step-1-ops.png)

> [!IMPORTANT] 
> <span data-ttu-id="8c0e1-175">タスク ガイドの再生時には、実際のデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-175">The data that you enter when you play a task guide is real.</span></span> <span data-ttu-id="8c0e1-176">実稼働環境である場合、データは現在使用している会社で入力されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-176">If you're in a production environment, the data will be entered in the company that you’re currently using.</span></span>

### <a name="it-all-begins-with-task-recorder"></a><span data-ttu-id="8c0e1-177">すべてタスク レコーダーから始まります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-177">It all begins with Task Recorder</span></span>

<span data-ttu-id="8c0e1-178">タスク ガイドは、タスク レコーダーを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-178">Task guides are created by using Task Recorder.</span></span> <span data-ttu-id="8c0e1-179">タスク レコーダーを使用すると、Finance and Operations UI で実行するアクション (メニューのクリック、設定の変更、データの入力) はすべて記録されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-179">When you use Task Recorder, all the actions that you perform in the Finance and Operations UI (such as clicking menus, changing settings, and entering data) are recorded.</span></span> <span data-ttu-id="8c0e1-180">記録する手順は、[タスク記録] と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-180">The steps that you record are collectively called a task recording.</span></span> <span data-ttu-id="8c0e1-181">前のセクションで説明したように、タスク記録は [ヘルプ] ウィンドウに表示され、タスク ガイドとして再生できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-181">As we explained in the previous section, task recordings can be displayed in the Help pane and played as task guides.</span></span> <span data-ttu-id="8c0e1-182">ただし、タスク記録を使用できるそのほかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-182">However, there are other ways that you can use task recordings:</span></span>

-   <span data-ttu-id="8c0e1-183">**タスク記録を BPM に保存** – LCS の BPM ライブラリの階層の明細行にタスク記録を保存できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-183">**Save task recordings to BPM** – You can save a task recording to a line of a hierarchy in a BPM library in LCS.</span></span> <span data-ttu-id="8c0e1-184">BPM にタスク記録を保存すると、フローチャートの図が生成され、記録のステップとともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-184">When you save a task recording to BPM, a flowchart diagram is generated and displayed, together with the steps of the recording.</span></span> 

    > [!Note]
    > <span data-ttu-id="8c0e1-185">Finance and Operations のヘルプ ウィンドウに表示させてタスク ガイドとして再生するには、記録を BPM ライブラリに保存します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-185">To display a task recording in the Finance and Operations Help pane and play it as a task guide, you'll have to save the recording to a BPM library.</span></span>
    
-   <span data-ttu-id="8c0e1-186">**タスク記録をWord文書として保存** – Microsoft Word文書としてタスク記録を保存すると、組織の印刷可能なトレーニング ガイドを簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-186">**Save task recordings as Word documents** – By saving a task recording as a Microsoft Word document, you can easily produce printable training guides for your organization.</span></span>

<span data-ttu-id="8c0e1-187">タスク レコーダーの詳細については、「[Finance and Operations のタスク レコーダー](../../dev-itpro/user-interface/task-recorder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-187">For more information about Task Recorder, see [Task recorder in Finance and Operations](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="creating-customized-task-recordings"></a><span data-ttu-id="8c0e1-188">カスタマイズされたタスク記録の作成</span><span class="sxs-lookup"><span data-stu-id="8c0e1-188">Creating customized task recordings</span></span>

<span data-ttu-id="8c0e1-189">独自のタスク記録を作成するか、Microsoft の提供するタスク記録をダウンロードしてカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-189">You can create your own task recordings, or you can download and customize task recording that Microsoft provides.</span></span> <span data-ttu-id="8c0e1-190">したがって、固有の Finance and Operations の実装を反映する、組織のカスタマイズされたヘルプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-190">Therefore, you can create customized Help for your organization that reflects your specific Finance and Operations implementation.</span></span> <span data-ttu-id="8c0e1-191">Finance and Operations の [ヘルプ] ウィンドウに表示させてタスク ガイドとして再生するには、LCD で記録を BPM ライブラリに保存します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-191">To display a task recording in the Finance and Operations Help pane and play it as a Task guide, you'll have to save the recording to a BPM library in LCS.</span></span> <span data-ttu-id="8c0e1-192">パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-192">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="8c0e1-193">詳細な手順については、「[ドキュメントとトレーニングの作成にタスク記録を使用](../../dev-itpro/user-interface/task-recorder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-193">For complete instructions, see [Using task recordings to create documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

## <a name="in-product-help"></a><span data-ttu-id="8c0e1-194">製品内ヘルプ</span><span class="sxs-lookup"><span data-stu-id="8c0e1-194">In-product Help</span></span>
<span data-ttu-id="8c0e1-195">Finance and Operations 内のヘルプ コンテンツにアクセスするには、**ヘルプ** (**?**) アイコンをクリックしてからヘルプを選択するか、Ctrl + Shift + ? を押します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-195">To access Help content within Finance and Operations, either click the **Help** (**?**) icon and then choose Help or press Ctrl+Shift+?.</span></span> <span data-ttu-id="8c0e1-196">どちらの場合も、[ヘルプ] ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-196">In both cases, the Help pane opens.</span></span> <span data-ttu-id="8c0e1-197">[ヘルプ] ウィンドウから記事またはタスク ガイドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-197">From the Help pane, you can access articles or task guides.</span></span> 

![[ヘルプ] ウィンドウ](./media/help-pane-wiki.png)

### <a name="accessing-help-topics-from-the-help-pane"></a><span data-ttu-id="8c0e1-199">ヘルプ ウィンドウからヘルプ トピックへのアクセス</span><span class="sxs-lookup"><span data-stu-id="8c0e1-199">Accessing help topics from the Help pane</span></span>

<span data-ttu-id="8c0e1-200">[ヘルプ] ウィンドウから、Finance and Operations クライアントに適用する記事にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-200">From the Help pane, you can access articles that apply to the Finance and Operations client.</span></span> <span data-ttu-id="8c0e1-201">最初にヘルプ ウィンドウを開いてから**ヘルプ**タブをクリックすると、Finance and Operations の現在のページに対応する記事が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-201">When you first open the Help pane and click the **Help** tab, you’ll see the articles that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="8c0e1-202">記事がない場合は、検索するキーワードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-202">If no articles are found, you can enter keywords to refine your search.</span></span> <span data-ttu-id="8c0e1-203">[ヘルプ] ウィンドウで記事をクリックすると、ブラウザで新しいタブが開いて記事を表示します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-203">When you click an article in the Help pane, a new tab opens in your browser and displays the article.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8c0e1-204">このセクションは、Dynamics 365 for Talent には適用されません。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-204">This section does not apply to Dynamics 365 for Talent.</span></span> <span data-ttu-id="8c0e1-205">[Talent] のヘルプ システムは、製品のタスクのガイドに自動的に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-205">The Help system for Talent is automatically connected to Task guides for the product.</span></span> <span data-ttu-id="8c0e1-206">さらに、[Talent] のカスタム タスク ガイドを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-206">Also, you cannot create custom Task guides for Talent.</span></span> 

### <a name="accessing-task-guides-from-the-help-pane"></a><span data-ttu-id="8c0e1-207">ヘルプ ウィンドウからタスク ガイドへのアクセス</span><span class="sxs-lookup"><span data-stu-id="8c0e1-207">Accessing Task guides from the Help pane</span></span>

<span data-ttu-id="8c0e1-208">[ヘルプ] ウィンドウからタスク ガイドにアクセスできるようになる前に、システム管理者が Finance and Operations の **システム パラメーター** ページに進み、設定をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-208">Before you can access Task guides from the Help pane, a System administrator has to go to the **System parameters** page in Finance and Operations and configure some settings.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="8c0e1-209">ヘルプを設定するには、Finance and Operations を導入したテナントと同じテナントのアカウントを使用してサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-209">In order to configure help, you must be signed in with an account in the same tenant as the tenant in which Finance and Operations is deployed.</span></span>
> -   <span data-ttu-id="8c0e1-210">ローカル仮想ハード ドライブ (VHD) で実行されている Finance and Operations のインスタンスから、LCS ライブラリに接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-210">It is not possible to connect to an LCS library from an instance of Finance and Operations running in a local virtual hard drive (VHD).</span></span>

![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)

<span data-ttu-id="8c0e1-212">**システム パラメーター** ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-212">On the **System parameters** page, follow these steps:</span></span>

1.  <span data-ttu-id="8c0e1-213">**重要:** ヘルプ タブを初めて開く際には、Lifecycle Services に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-213">**Important:** The first time that you open the Help tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="8c0e1-214">フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、**OK** をクリックしてパラメーター フォームを取得します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-214">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the parameters form.</span></span>

![LCS に接続](./media/connect-to-lcs-crop-1024x365.png)

2.  <span data-ttu-id="8c0e1-216">接続する Lifecycle Services プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-216">Select the Lifecycle Services project to connect to.</span></span>
3.  <span data-ttu-id="8c0e1-217">タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-217">Select BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="8c0e1-218">Finance and Operations、Microsoft のコンテンツ用に、Microsoft Dynamics 365 for Finance and Operations の「2017 年 2 月 QPC 統合ライブラリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-218">For Finance and Operations, for Microsoft content, select the February 2017 QPC Unified Library for Microsoft Dynamics 365 for Finance and Operations.</span></span> 
    - <span data-ttu-id="8c0e1-219">[Retail] 用に、7 月にライブラリをリリースする予定です。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-219">For Retail, we will be releasing a library in July.</span></span> 
    - <span data-ttu-id="8c0e1-220">[Talent] のライブラリを選択する必要はありません。適切なライブラリへの接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-220">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

4.  <span data-ttu-id="8c0e1-221">BPM ライブラリの表示順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-221">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="8c0e1-222">これにより、ライブラリからのタスク記録が [ヘルプ] ウィンドウに表示される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-222">This determines the order in which task recordings from the libraries will appear in the Help pane.</span></span>

<span data-ttu-id="8c0e1-223">システム管理者がこれらのステップを完了したのちに、ヘルプ ウィンドウを開いて **タスク ガイド** タブをクリックできます。Finance and Operations の現在のページに対応するタスク ガイドが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-223">After a System administrator has completed these steps, you can open the Help pane and click the **Task guides** tab. You'll now see the Task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="8c0e1-224">タスク ガイドがない場合は、検索するキーワードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-224">If no Task guides are found, you can enter keywords to refine your search.</span></span> <span data-ttu-id="8c0e1-225">[ヘルプ] ウィンドウでタスク ガイドをクリックした後、[ヘルプ] ウィンドウにはステップ バイ ステップの手順が表示され、タスク ガイドが再生できます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-225">After you click a Task guide in the Help pane, the Help pane shows the step-by-step instructions, and you can play the task guide.</span></span> 

![タスク ガイドの読み取りビュー](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides-for-microsoft-libraries"></a><span data-ttu-id="8c0e1-227">Microsoft ライブラリの翻訳されたタスク ガイドはどこにありますか。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-227">Where are the translated Task guides for Microsoft libraries?</span></span>

<span data-ttu-id="8c0e1-228">翻訳されたタスク ガイドは、タイトルの「すべての言語」を持つライブラリでリリースされます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-228">Translated Task guides are released in libraries with "All languages" in the title.</span></span> <span data-ttu-id="8c0e1-229">Finance and Operations でローカライズされたタスク ガイドのヘルプを参照するには、適切なライブラリに接続できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-229">In Finance and Operations, to see localized Task guide help, make sure that you are connected to an appropriate library.</span></span> <span data-ttu-id="8c0e1-230">タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の [言語の設定] でユーザーごとに制御されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-230">The language that a Task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 
-   <span data-ttu-id="8c0e1-231">タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-231">If a Task guide has been translated, when you open that Task guide all the text of the Task guide will appear in your selected language.</span></span>
-   <span data-ttu-id="8c0e1-232">タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-232">If a Task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c0e1-233">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="8c0e1-233">Additional resources</span></span>

- [<span data-ttu-id="8c0e1-234">Finance and Operations のヘルプ システム (ダウンロード可能なファクト シート)</span><span class="sxs-lookup"><span data-stu-id="8c0e1-234">Finance and Operations help system (downloadable fact sheet)</span></span>](https://mbs.microsoft.com/customersource/global/AX/learning/fact-sheets/msdaxhelpsystemfactsheet)
- [<span data-ttu-id="8c0e1-235">タスク レコーダー</span><span class="sxs-lookup"><span data-stu-id="8c0e1-235">Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder.md)
- [<span data-ttu-id="8c0e1-236">タスク記録を使用してドキュメントやトレーニングを作成</span><span class="sxs-lookup"><span data-stu-id="8c0e1-236">Create documentation or training using Task recordings</span></span>](../../dev-itpro/user-interface/task-recorder.md)

<span data-ttu-id="8c0e1-237">次の表に Web サイトの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-237">The following table lists our websites.</span></span> <span data-ttu-id="8c0e1-238">名前の横にアスタリスク (\*) のあるサイトには、サービス計画と関連付けられたアカウントでサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-238">Sites that have an asterisk (\*) next to the name require that you sign in by using an account that is associated with a service plan.</span></span>

| <span data-ttu-id="8c0e1-239">サイト</span><span class="sxs-lookup"><span data-stu-id="8c0e1-239">Site</span></span>                                                                     | <span data-ttu-id="8c0e1-240">説明</span><span class="sxs-lookup"><span data-stu-id="8c0e1-240">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c0e1-241">Docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="8c0e1-241">Docs.microsoft.com</span></span>](/dynamics365/) | <span data-ttu-id="8c0e1-242">Dynamics 365 のすべての製品ドキュメントのホストまたはリンクです。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-242">Hosts or links to all product documentation for Dynamics 365.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="8c0e1-243">Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="8c0e1-243">Microsoft Learn</span></span>](https://docs.microsoft.com/learn/) | <span data-ttu-id="8c0e1-244">Microsoft の無料 e ラーニング サイトです。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-244">Microsoft's free eLearning site.</span></span>                                                                                                                                                               |
| <span data-ttu-id="8c0e1-245">[Lifecycle Services](https://lcs.dynamics.com/en/)\*</span><span class="sxs-lookup"><span data-stu-id="8c0e1-245">[Lifecycle Services](https://lcs.dynamics.com/en/)\*</span></span>                      | <span data-ttu-id="8c0e1-246">事前販売からの実装および工程にいたるまで Dynamics 365 for Finance and Operations のプロジェクトを管理するのに、顧客とパートナーが使用できるクラウドベースの共同ワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-246">Provides a cloud-based collaborative workspace that customers and partners can use to manage Dynamics 365 for Finance and Operations projects from pre-sales to implementation and operations.</span></span> <span data-ttu-id="8c0e1-247">このサイトは、実装のすべてのフェーズに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-247">This site is useful in all phases of an implementation.</span></span> |
| [<span data-ttu-id="8c0e1-248">サポート ブログ</span><span class="sxs-lookup"><span data-stu-id="8c0e1-248">Support blog</span></span>](http://aka.ms/AXSupportBlog)                              | <span data-ttu-id="8c0e1-249">Dynamics 365 for Finance and Operations のサポート チームによって投稿されるヒントおよび秘訣を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-249">Provides tips and tricks that are posted by the Dynamics 365 for Finance and Operations Support team.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="8c0e1-250">Docs.microsoft.com/previous versions</span><span class="sxs-lookup"><span data-stu-id="8c0e1-250">Docs.microsoft.com/previous versions</span></span>](https://docs.microsoft.com/en-us/previous-versions/dynamics/)                                             | <span data-ttu-id="8c0e1-251">以前のリリースのコンテンツをホストします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-251">Hosts content from previous releases.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="8c0e1-252">Dynamics コミュニティ</span><span class="sxs-lookup"><span data-stu-id="8c0e1-252">Dynamics Community</span></span>](https://community.dynamics.com/)                  | <span data-ttu-id="8c0e1-253">ブログ、フォーラムおよびビデオをホストします。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-253">Hosts blogs, forums, and videos.</span></span>                                                                                                                                                                                                           |
| [<span data-ttu-id="8c0e1-254">Microsoft.com/dynamics365/</span><span class="sxs-lookup"><span data-stu-id="8c0e1-254">Microsoft.com/dynamics365/</span></span>](https://www.microsoft.com/en-us/dynamics365/home)                 | <span data-ttu-id="8c0e1-255">評価と販売情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-255">Provides evaluation and sales information.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="8c0e1-256">[CustomerSource](https://mbs.microsoft.com/customersource/)\*</span><span class="sxs-lookup"><span data-stu-id="8c0e1-256">[CustomerSource](https://mbs.microsoft.com/customersource/)\*</span></span>                      | <span data-ttu-id="8c0e1-257">Finance and Operations、ダウンロード可能なレポート、およびホワイト ペーパーの一部のトレーニング リソースをホストする、サービス計画保持者の主なサポート サイトです。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-257">Hosts some training resources for Finance and Operations,  downloadable reports and white papers, and is the primary support site for service plan holders.</span></span> <span data-ttu-id="8c0e1-258">サイトのいくつかのリソースにアクセスするためには、サービス計画が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="8c0e1-258">May require a service plan to access some resources on the site.</span></span>     |


