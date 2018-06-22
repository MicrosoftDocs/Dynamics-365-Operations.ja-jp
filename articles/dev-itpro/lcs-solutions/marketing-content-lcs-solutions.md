---
title: "LCS ソリューションのステージングおよび発行"
description: "このトピックでは、LCS ソリューション パッケージのマーケティング コンテンツを Azure Publishing Portal にアップロードする方法、およびソリューションを準備して発行する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196873
ms.assetid: 80b0cc44-ffbe-400e-b902-60518a930b0d
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a67616bb026b54b18deee358e6a0199c77e5e183
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="stage-and-publish-an-lcs-solution"></a><span data-ttu-id="dd47b-103">LCS ソリューションのステージングおよび発行</span><span class="sxs-lookup"><span data-stu-id="dd47b-103">Stage and publish an LCS solution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd47b-104">このトピックでは、LCS ソリューション パッケージのマーケティング コンテンツを Azure Publishing Portal にアップロードする方法、およびソリューションを準備して発行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-104">This topic explains how to upload the marketing content for your LCS solution package to the Azure Publishing Portal, and how to stage and publish your solution.</span></span>

<span data-ttu-id="dd47b-105">LCS ソリューション パッケージのマーケティング コンテンツを Microsoft Azure Publishing Portal に公開する前に、Microsoft に開発者センターのアカウントを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd47b-105">Before you can publish the marketing content for your LCS solution package to the Microsoft Azure Publishing Portal, you must set up a Developer Center account with Microsoft.</span></span> <span data-ttu-id="dd47b-106">アカウントを作成した後、マーケティング コンテンツをアップロード、およびアプリケーションのライフ サイクルを通じてコンテンツを管理できます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-106">After you've set up an account, you can upload your marketing content and then manage the content through the lifecycle of application.</span></span> <span data-ttu-id="dd47b-107">開発者センターのアカウントを設定する方法の詳細については、[Microsoft 開発者アカウントの作成](https://azure.microsoft.com/en-us/documentation/articles/marketplace-publishing-accounts-creation-registration/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd47b-107">For information about how to set up a Developer Center account, see [Create a Microsoft Developer account](https://azure.microsoft.com/en-us/documentation/articles/marketplace-publishing-accounts-creation-registration/).</span></span>

## <a name="upload-marketing-materials-set-up-legal-information-and-identify-the-support-team"></a><span data-ttu-id="dd47b-108">マーケティング資料のアップロード、法的情報の設定、サポート チームの特定</span><span class="sxs-lookup"><span data-stu-id="dd47b-108">Upload marketing materials, set up legal information, and identify the support team</span></span>
<span data-ttu-id="dd47b-109">マーケティングの概要、ソリューションの説明、および他のマーケティング資料をアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-109">You can upload a marketing summary, a description of your solution, and other marketing materials.</span></span>

1.  <span data-ttu-id="dd47b-110">[Azure Publishing ポータル](https://publish.windowsazure.com/workspace/)で、ソリューションを開いてから、左ウィンドウで**マーケティング**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-110">In the [Azure Publishing Portal](https://publish.windowsazure.com/workspace/), open your solution, and then, in the left pane, click **Marketing**.</span></span>
2.  <span data-ttu-id="dd47b-111">**Url** セクションの**識別子**フィールドに、サービスに関する特定のマーケティング ページにリンクする URL で使用する 短い URL にしやすい識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-111">In the **Url** section, in the **Identifier** field, enter a short, URL-friendly identifier to use in the URLs that link to the specific marketing pages for your offer.</span></span>
3.  <span data-ttu-id="dd47b-112">**言語**セクションで**英語**を選択してから、**説明**セクションにソリューションのタイトル、要約、長い要約、および説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-112">In the **Languages** section, select **English**, and then, in the **Description** section, enter the title, summary, long summary, and description of your solution.</span></span>
4.  <span data-ttu-id="dd47b-113">**ロゴ** セクションで、アップロードするグラフィックのサイズに対応する**画像のアップロード** リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-113">In the **Logos** section, click the **Upload Image** link for the graphic size that corresponds to the graphic size that you want to upload.</span></span> <span data-ttu-id="dd47b-114">**注記:** すべてのグラフィックスは各イメージに与えられているサイズに従う必要があり、PNG 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd47b-114">**Note:** All graphics must follow the sizes that are given for each image, and they must be in a PNG format.</span></span>
5.  <span data-ttu-id="dd47b-115">プラス記号 (**+**) をクリックすると、1 つまたは複数のリンクを追加のリソースに追加できます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-115">Click the plus sign (**+**) to add one or more links to additional resources.</span></span>
6.  <span data-ttu-id="dd47b-116">オプション: 左ウィンドウで、**サンプル イメージ** をクリックして、ソリューションを説明またはレベル上げする追加画像をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-116">Optional: In the left pane, click **Sample Images** to upload any additional images that describe or promote your solution.</span></span> <span data-ttu-id="dd47b-117">**注記:** すべてのグラフィックスは各イメージに与えられているサイズに従う必要があり、PNG 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd47b-117">**Note:** All graphics must follow the sizes that are given for each image, and they must be in a PNG format.</span></span>
7.  <span data-ttu-id="dd47b-118">左のナビゲーション ウィンドウで、**プラン**をクリックしてから、**プラン** セクションに、タイトル、概要、および顧客がソリューションを購入した場合に受け取る内容の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-118">In the left navigation pane, click **Plans**, and then, in the **Plans** section, enter the title, summary, and description of what customers will receive when they purchase your solution.</span></span> <span data-ttu-id="dd47b-119">**重要:** 現時点では、この情報は、Microsoft Dynamics 365 for Finance and Operations には適用されません。</span><span class="sxs-lookup"><span data-stu-id="dd47b-119">**Important:** Currently, this information doesn't apply to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="dd47b-120">ただし、それは将来に使用されるもので、ソリューションが公開される前に含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd47b-120">However, it will be used in the future and must be included before your solution can be published.</span></span> <span data-ttu-id="dd47b-121">この情報はいつでも更新することができます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-121">You can update this information at any time.</span></span>
8.  <span data-ttu-id="dd47b-122">左のナビゲーション ウィンドウで、**リーガル**をクリックしてから、**リーガル** セクションにプライバシー ポリシーの URL とソリューションの使用条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-122">In the left navigation pane, click **Legal**, and then, in the **Legal** section, enter the URLs of the privacy policy and the terms of use for your solution.</span></span> <span data-ttu-id="dd47b-123">お客様は、ソリューションを購入する際に、これらのポリシーを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-123">Customers will be able to view these policies when they purchase your solution.</span></span>
9.  <span data-ttu-id="dd47b-124">左のナビゲーション ウィンドウで、**サポート**をクリックしてから、組織のエンジニアリングの連絡先と顧客サポート情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-124">In the left navigation pane, click **Support**, and then enter the engineering contact and customer support information for your organization.</span></span> <span data-ttu-id="dd47b-125">この情報は、マイクロソフトでは、ソリューションに関する質問の問い合わせ窓口として使用されます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-125">This information will be used as a single point of contact if Microsoft has a question about your solution.</span></span> <span data-ttu-id="dd47b-126">この情報は顧客サポートにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-126">The information will also be used for customer support.</span></span>
10. <span data-ttu-id="dd47b-127">左のナビゲーション ウィンドウで、**カテゴリ**をクリックしてから**ビジネス アプリケーション** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-127">In the left navigation pane, click **Categories**, and then select the **Business Application** check box.</span></span>

## <a name="stage-and-publish-your-solution"></a><span data-ttu-id="dd47b-128">ソリューションのステージングおよび発行</span><span class="sxs-lookup"><span data-stu-id="dd47b-128">Stage and publish your solution</span></span>
<span data-ttu-id="dd47b-129">前の手順を完了した後は、ソリューションを実施および公開できます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-129">After you've completed the previous procedure, you can stage and publish your solution.</span></span>

1.  <span data-ttu-id="dd47b-130">左のナビゲーション ウィンドウで、**ステージング**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-130">In the left navigation pane, click **Staging**.</span></span>
2.  <span data-ttu-id="dd47b-131">**ステージング** グループで、**ステージングにプッシュ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-131">In the **Staging** group, click **Push to staging**.</span></span> <span data-ttu-id="dd47b-132">訂正が必要な場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-132">If any corrections are required, you receive an error message.</span></span>
3.  <span data-ttu-id="dd47b-133">メッセージ内の各エラーについては、問題を修正するためリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-133">For each error in the message, click the link to fix the issue.</span></span>
4.  <span data-ttu-id="dd47b-134">すべてのエラーを修正した後、Azure サブスクリプション ID を入力するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-134">After you've fixed all the errors, you will be prompted to enter your Azure subscription ID.</span></span> <span data-ttu-id="dd47b-135">LCS 内のこの ID は、**プロジェクト設定** &gt; **Azure コネクタ** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-135">You can find this ID in LCS, at **Project Settings** &gt; **Azure Connectors**.</span></span> <span data-ttu-id="dd47b-136">Azure サブスクリプション ID を入力し、チェック マークをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-136">Enter your Azure subscription ID, and then click the check mark.</span></span> <span data-ttu-id="dd47b-137">**ステージング** ページに戻ります。ここではアプリケーションのステージング プロセスを追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-137">You are returned to the **Staging** page, where you can track the staging process of your application.</span></span>
5.  <span data-ttu-id="dd47b-138">ステージングが完了した場合、**生産** グループで、**生産にプッシュする承認要求** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd47b-138">When staging is completed, in the **Production** group, click **Request Approval to Push to Production**.</span></span> <span data-ttu-id="dd47b-139">Microsoft はソリューションやマーケティング文書の検証を開始します。</span><span class="sxs-lookup"><span data-stu-id="dd47b-139">Microsoft will begin to validate your solution and marketing materials.</span></span> <span data-ttu-id="dd47b-140">レビュー中に質問や問題が発生した場合、Microsoft は、会社が提供したエンジニアリングの担当者に問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="dd47b-140">If any questions or concerns arise during the review, Microsoft will contact the engineering contacts that your company provided.</span></span> <span data-ttu-id="dd47b-141">承認後、ソリューションは Azure マーケットプレースで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="dd47b-141">After approval, your solution will be available in the Azure marketplace.</span></span>


<a name="additional-resources"></a><span data-ttu-id="dd47b-142">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="dd47b-142">Additional resources</span></span>
--------

[<span data-ttu-id="dd47b-143">AppSource 向け LCS ソリューション ホームページ</span><span class="sxs-lookup"><span data-stu-id="dd47b-143">LCS Solutions for AppSource home page</span></span>](lcs-solutions-app-source.md)




