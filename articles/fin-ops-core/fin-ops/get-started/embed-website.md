---
title: サードパーティ製アプリの埋め込み
description: このトピックでは、サードパーティー製アプリを埋め込んで、製品の機能を拡張する方法について説明します。
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d348683e0a2ed35f26830a6ce05c0bf9ca5970bd
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944844"
---
# <a name="embed-third-party-apps"></a><span data-ttu-id="f9a23-103">サードパーティ製アプリの埋め込み</span><span class="sxs-lookup"><span data-stu-id="f9a23-103">Embed third-party apps</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="f9a23-104">多くの顧客は、さまざまなアプリケーションを使用して業務を行っています。</span><span class="sxs-lookup"><span data-stu-id="f9a23-104">Many customers use a range of applications to run their business.</span></span> <span data-ttu-id="f9a23-105">これらのアプリケーションの一部は、Finance and Operations アプリと連携して動作するサードパーティの Web アプリです。</span><span class="sxs-lookup"><span data-stu-id="f9a23-105">Some of those applications are third-party web apps that work in conjunction with Finance and Operations apps.</span></span> <span data-ttu-id="f9a23-106">よりシームレスなユーザー エクスペリエンスを提供するには、**(プレビュー) フル ページ アプリ** 機能を使用して、それらのサードパーティ製アプリを Finance and Operations アプリに直接埋め込むことができます (サードパーティ製アプリが埋め込みを許可している場合)。</span><span class="sxs-lookup"><span data-stu-id="f9a23-106">To provide a more seamless user experience, you can use the **(Preview) Full page apps** feature to embed those third-party apps directly into your Finance and Operations apps (provided that the third-party apps allow themselves to be embedded).</span></span> <span data-ttu-id="f9a23-107">これにより、ユーザーはタブやウィンドウを切り替えることなく、必要な Web サイトやアプリにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-107">In this way, users can access the websites and apps that they require without having to switch tabs or windows.</span></span>

<span data-ttu-id="f9a23-108">サードパーティ製アプリを製品に組み込む前に、機能管理で **(プレビュー) フル ページ アプリ** 機能をオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-108">Before you can embed third-party apps into the product, you must turn on the **(Preview) Full page apps** feature in Feature management.</span></span> <span data-ttu-id="f9a23-109">その後、次のいずれかの方法でサードパーティ製アプリまたは Web サイトを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-109">You can then use one of the following methods to embed a third-party app or website.</span></span> <span data-ttu-id="f9a23-110">これらの方法は、Microsoft Power Apps のキャンバス アプリを Finance and Operations のアプリに組み込む際に使用される方法と類似しています。</span><span class="sxs-lookup"><span data-stu-id="f9a23-110">These methods are analogous to the methods that are used to embed canvas apps from Microsoft Power Apps into Finance and Operations apps.</span></span>

- <span data-ttu-id="f9a23-111">既存のページに、アプリまたは Web サイトを新しいタブ ページ (ピボット タブ、クイック タブ、ブレード、またはワークスペースのセクション) として埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-111">Embed the app or website on an existing page as a new tab page (pivot tab, FastTab, blade, or workspace section).</span></span>
- <span data-ttu-id="f9a23-112">ダッシュボードから、アプリまたは Web サイトの新しいフル ページ エクスペリエンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-112">Create a new full-page experience for the app or website from the dashboard.</span></span>

## <a name="embed-a-website-on-an-existing-page"></a><span data-ttu-id="f9a23-113">既存のページに Web サイトを埋め込む</span><span class="sxs-lookup"><span data-stu-id="f9a23-113">Embed a website on an existing page</span></span>

<span data-ttu-id="f9a23-114">システム内の既存のページを埋め込みアプリで補完する場合は、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-114">Use this procedure if you want to supplement an existing page in the system with an embedded app.</span></span>

1. <span data-ttu-id="f9a23-115">アプリを埋め込むページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-115">Open the page where you want to embed the app.</span></span>
2. <span data-ttu-id="f9a23-116">**アプリを追加** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-116">Open the **Add an app** pane:</span></span>

    1. <span data-ttu-id="f9a23-117">**設定** を選択してから **個人用設定** を選択して、**個人用設定** ツールバーを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-117">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
    2. <span data-ttu-id="f9a23-118">**詳細 \>アプリを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-118">Select **More \> Add an app**.</span></span>

3. <span data-ttu-id="f9a23-119">アプリを追加するページの地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-119">Select the region of the page where you want to add the app.</span></span> <span data-ttu-id="f9a23-120">この地域は、ピボット タブ、クイック タブ、ブレード、またはワークスペース セクションの *タブ コンテナー* である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-120">This region must be a *tab container* for a pivot tab, FastTab, blade, or workspace section.</span></span>
4. <span data-ttu-id="f9a23-121">**Web サイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-121">Select **Website**.</span></span>
5. <span data-ttu-id="f9a23-122">埋め込み型アプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-122">Configure the embedded app:</span></span>

    - <span data-ttu-id="f9a23-123">**名前** – 埋め込みアプリを含むタブに表示するテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-123">**Name** – Enter the text that should be shown for the tab that contains the embedded app.</span></span> <span data-ttu-id="f9a23-124">多くの場合、アプリの名前をこのテキストに設定します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-124">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="f9a23-125">**URL** – アプリの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-125">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="f9a23-126">セキュリティ上の理由から、URL にはハイパーテキスト転送プロトコル セキュア (HTTPS) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-126">For security reasons, the URL must use Hypertext Transfer Protocol Secure (HTTPS).</span></span>
    > - <span data-ttu-id="f9a23-127">埋め込むアプリまたは Web サイトは埋め込みを許可するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-127">The app or website must be configured to allow itself to be embedded.</span></span>

6. <span data-ttu-id="f9a23-128">**保存** を選択して、アプリをページに埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-128">Select **Save** to embed the app on the page.</span></span> <span data-ttu-id="f9a23-129">アプリがグループの最後のタブまたはセクションとして追加されます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-129">The app is added as the last tab or section in the group.</span></span>
7. <span data-ttu-id="f9a23-130">アプリが予定通り表示されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-130">Confirm that the app appears as expected.</span></span> <span data-ttu-id="f9a23-131">アプリが表示されない場合は、このトピックの後半の[トラブルシューティング](#troubleshooting) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-131">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>
8. <span data-ttu-id="f9a23-132">ビュー セレクターを開き、**保存** (アプリを現在のビューに関連付ける場合) または **名前を付けて保存** (アプリを別のビューに保存する場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-132">Open the view selector, and select either **Save** (if the app should be associated with the current view) or **Save as** (to save the app to a different view).</span></span>

    <span data-ttu-id="f9a23-133">ページにビュー セレクターがない場合 (たとえば、ページがダイアログ ボックスまたはワークスペースの場合)、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-133">If the page doesn't have a view selector (for example, if the page is a dialog box or a workspace), you can skip this step.</span></span>

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a><span data-ttu-id="f9a23-134">ダッシュボードからのフル ページ エクスペリエンスとして Web サイトを埋め込む</span><span class="sxs-lookup"><span data-stu-id="f9a23-134">Embed a website as a full-page experience from the dashboard</span></span>

<span data-ttu-id="f9a23-135">埋め込むアプリが既存のページに関連していない場合や、Finance and Operations アプリ内のアプリでフル ページ エクスペリエンスが必要な場合は、この手順を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-135">Use this procedure if the app that you want to embed isn't related to an existing page, or if you just want a full-page experience for the app inside the Finance and Operations app.</span></span>

1. <span data-ttu-id="f9a23-136">ダッシュボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-136">Open the dashboard.</span></span>
2. <span data-ttu-id="f9a23-137">ページを選択したまま (または右クリック) にしてから、**個人設定** を選択して、**ページを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-137">Select and hold (or right-click) the page, select **Personalize**, and then select **Add a page**.</span></span>
3. <span data-ttu-id="f9a23-138">**ページを追加** ウィンドウで **Web サイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-138">In the **Add a page** pane, select **Website**.</span></span>
4. <span data-ttu-id="f9a23-139">埋め込み型アプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-139">Configure the embedded app:</span></span>

    - <span data-ttu-id="f9a23-140">**名前** – 埋め込みアプリ用にダッシュボードに追加されるタイルに表示されるテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-140">**Name** – Enter the text that should be shown on the tile that is added for the embedded app on the dashboard.</span></span> <span data-ttu-id="f9a23-141">多くの場合、アプリの名前をこのテキストに設定します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-141">Often, you will want this text to be the name of the app.</span></span>
    - <span data-ttu-id="f9a23-142">**URL** – アプリの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-142">**URL** – Specify the location of the app.</span></span>

    > [!IMPORTANT]
    > - <span data-ttu-id="f9a23-143">セキュリティ上の理由から、URL では HTTPS を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-143">For security reasons, the URL must use HTTPS.</span></span>
    > - <span data-ttu-id="f9a23-144">埋め込むアプリまたは Web サイトは埋め込みを許可するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-144">The app or website must be configured to allow itself to be embedded.</span></span>

5. <span data-ttu-id="f9a23-145">**保存** を選択して、アプリを新しいタイルとしてダッシュボードに追加します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-145">Select **Save** to add the app to the dashboard as a new tile.</span></span>
6. <span data-ttu-id="f9a23-146">ダッシュボードの新しいタイルを選択し、アプリが予定通り表示されるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-146">Select the new tile on the dashboard, and confirm that the app appears as expected.</span></span> <span data-ttu-id="f9a23-147">アプリが表示されない場合は、このトピックの後半の[トラブルシューティング](#troubleshooting) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-147">If the app isn't rendered, see the [Troubleshooting](#troubleshooting) section later in this topic.</span></span>

## <a name="sharing-embedded-apps"></a><span data-ttu-id="f9a23-148">埋め込まれたアプリの共有</span><span class="sxs-lookup"><span data-stu-id="f9a23-148">Sharing embedded apps</span></span>

<span data-ttu-id="f9a23-149">前のセクションで説明した方法のいずれかを使用してアプリを埋め込んだ後に、システム内の他のユーザーとビューを共有することができます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-149">After you've embedded an app by using one of the methods that are described in the previous sections, you might want to share the view with other users in the system.</span></span> <span data-ttu-id="f9a23-150">埋め込みアプリを共有するには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-150">To share an embedded app, use one of the following methods:</span></span>

- <span data-ttu-id="f9a23-151">**ビューを公開する (推奨):** 埋め込みアプリがビューに保存されている場合、ビューを共有するための推奨される方法は、適切なセキュリティ ロールを持つユーザーにビューを公開することです。</span><span class="sxs-lookup"><span data-stu-id="f9a23-151">**Publish the view (Recommended):** If the embedded app has been saved to a view, the recommended and preferred way to share it is to publish the view to users who have the appropriate security roles.</span></span> <span data-ttu-id="f9a23-152">その後、公開されたビューの対象となるセキュリティ ロールを持つすべてのユーザーが Finance and Operations アプリでアプリを確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-152">Then, all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> <span data-ttu-id="f9a23-153">公開方法の詳細については、「[ビューを公開する](saved-views.md#publishing-views)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-153">For more information about how to publish a view, see [Publishing views](saved-views.md#publishing-views).</span></span>

    <span data-ttu-id="f9a23-154">ダッシュボードからフル ページ エクスペリエンスとして埋め込まれたアプリを公開することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-154">You can also publish an app that has been embedded as a full-page experience from the dashboard.</span></span> <span data-ttu-id="f9a23-155">ダッシュボードで、アプリに関連付けられているタイルを選択したまま (または右クリック) にして、**個人用設定** を選択してから、**ページを公開する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-155">On the dashboard, select and hold (or right-click) the tile that is associated with the app, select **Personalize**, and then select **Publish page**.</span></span> <span data-ttu-id="f9a23-156">現在、セキュリティ ロールのみにビューを公開できます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-156">Currently, you can publish only to security roles.</span></span> <span data-ttu-id="f9a23-157">ただし、法人に公開する機能は、機能が一般に利用できる状態になる前に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-157">However, the capability to publish to legal entities will be added before the feature becomes generally available.</span></span>

- <span data-ttu-id="f9a23-158">**個人用設定をコピーする :** ビューがサポートしないページ (ダイアログ ボックスやワークスペースなど)、またはフル ページ アプリ エクスペリエンスの場合は、個人用設定を適切なユーザーにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-158">**Copy the personalization:** For pages that don't support views (for example, dialog boxes or workspaces), or for the full-page app experience, you can copy the personalization to the appropriate users.</span></span> <span data-ttu-id="f9a23-159">詳細については、[個人用設定の共有](personalize-user-experience.md#sharing-personalizations)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-159">For more information, see [Sharing personalizations](personalize-user-experience.md#sharing-personalizations).</span></span>

## <a name="viewing-embedded-apps"></a><span data-ttu-id="f9a23-160">埋め込まれたアプリの表示</span><span class="sxs-lookup"><span data-stu-id="f9a23-160">Viewing embedded apps</span></span>

<span data-ttu-id="f9a23-161">Finance and Operations アプリのページに埋め込みアプリを表示するには、埋め込みアプリがあるページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-161">To view an embedded app on a page in Finance and Operations apps, open the page that has the embedded app.</span></span> <span data-ttu-id="f9a23-162">いくつかのページでは、標準アクション ペインの **Power Apps** ボタンを使用して埋め込みアプリにアクセスできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f9a23-162">Remember that, on some pages, embedded apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="f9a23-163">または、新しいタブ、クイック タブ、ブレードとして、またはワークスペースの新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-163">Alternatively, they might appear directly on the page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

## <a name="editing-or-removing-embedded-apps"></a><span data-ttu-id="f9a23-164">埋め込みアプリの編集または削除</span><span class="sxs-lookup"><span data-stu-id="f9a23-164">Editing or removing embedded apps</span></span>

<span data-ttu-id="f9a23-165">ページにアプリを埋め込んだ後に、アプリの構成を編集する必要がある場合があります (セクション ラベルや URL を変更するなど)。</span><span class="sxs-lookup"><span data-stu-id="f9a23-165">After an app has been embedded on a page, you might have to edit its configuration (for example, by changing the section label or the URL).</span></span> <span data-ttu-id="f9a23-166">または、ページから削除する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-166">Alternatively, you might have to remove it from the page.</span></span> <span data-ttu-id="f9a23-167">埋め込みアプリの構成を編集したり、完全に削除したりするには、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f9a23-167">Use one of the following procedures to edit the configuration of an embedded app or remove it completely.</span></span>

### <a name="apps-that-are-embedded-on-existing-pages"></a><span data-ttu-id="f9a23-168">既存のページに埋め込まれているアプリ</span><span class="sxs-lookup"><span data-stu-id="f9a23-168">Apps that are embedded on existing pages</span></span>

1. <span data-ttu-id="f9a23-169">アプリが埋め込まれているページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-169">Open the page where the app is embedded.</span></span>
2. <span data-ttu-id="f9a23-170">**設定** を選択してから **個人用設定** を選択して、**個人用設定** ツールバーを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-170">Select **Settings** and then **Personalize** to open the **Personalization** toolbar.</span></span>
3. <span data-ttu-id="f9a23-171">**選択** ツールを選択し、埋め込みアプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-171">Select the **Select** tool, and then select the embedded app.</span></span>
4. <span data-ttu-id="f9a23-172">アプリを編集するには、必要に応じて構成を変更し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-172">To edit the app, make the required changes to its configuration, and then select **Save**.</span></span>

    <span data-ttu-id="f9a23-173">または、アプリを削除するには、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-173">Alternatively, to remove the app, select **Delete**.</span></span>

5. <span data-ttu-id="f9a23-174">ビューを再保存または再公開します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-174">Re-save or republish the view.</span></span> <span data-ttu-id="f9a23-175">ビューを明示的に保存せずにページを離れる場合、**Web サイトの編集** ウィンドウで実行したアクションは維持されません。</span><span class="sxs-lookup"><span data-stu-id="f9a23-175">Note that if you leave the page without explicitly saving the view, none of the actions that you performed in the **Edit website** pane will be maintained.</span></span>

### <a name="apps-that-are-embedded-from-the-dashboard"></a><span data-ttu-id="f9a23-176">ダッシュボードに埋め込まれているアプリ</span><span class="sxs-lookup"><span data-stu-id="f9a23-176">Apps that are embedded from the dashboard</span></span>

1. <span data-ttu-id="f9a23-177">ダッシュボードを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-177">Open the dashboard.</span></span>
2. <span data-ttu-id="f9a23-178">埋め込みアプリに関連付けられているタイルを選択したまま (または右クリック) にして、**個人用設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-178">Select and hold (or right-click) the tile that is associated with the embedded app, and then select **Personalize**.</span></span>
3. <span data-ttu-id="f9a23-179">**ページの編集** を選択してアプリを編集します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-179">To edit the app, select **Edit page**.</span></span> <span data-ttu-id="f9a23-180">**Web サイトの編集** ウィンドウで、必要に応じてアプリ構成を変更してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-180">In the **Edit website** pane, make the required changes to the app configuration, and then select **Save**.</span></span>

    <span data-ttu-id="f9a23-181">または、アプリを削除するには、**ページの削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-181">Alternatively, to remove the app, select **Remove page**.</span></span>

## <a name="appendix"></a><span data-ttu-id="f9a23-182">付録</span><span class="sxs-lookup"><span data-stu-id="f9a23-182">Appendix</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="f9a23-183">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f9a23-183">Troubleshooting</span></span>

<span data-ttu-id="f9a23-184">Finance and Operation アプリに Web サイトを埋め込んでも正しく表示されない場合や、「URL の接続が拒否されました」というエラー メッセージが表示される場合は、その Web サイトが iFrame に埋め込まれないように設定されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-184">If a website isn't rendered correctly after it's embedded in a Finance and Operation app, or if you receive an error message that states that the URL was denied a connection, the website is probably configured to prevent itself from being embedded in an iframe.</span></span> <span data-ttu-id="f9a23-185">次の手順に従って、Web サイトを埋め込むかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-185">Follow these steps to determine whether the website can be embedded.</span></span>

1. <span data-ttu-id="f9a23-186">使用しているブラウザー用の開発者ツールを開きます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-186">Open the developer tools for the browser that you're using.</span></span>
2. <span data-ttu-id="f9a23-187">**ネットワーク** タブで、埋め込みサイトからの応答を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-187">On the **Network** tab, find and select the response from the embedded site.</span></span>
3. <span data-ttu-id="f9a23-188">**ヘッダー** タブの **応答ヘッダー** で、**X-Frame-Options** を検索します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-188">On the **Headers** tab, under **Response Headers**, look for **x-frame-options**.</span></span> <span data-ttu-id="f9a23-189">応答ヘッダーに **X-Frame-Options** が存在し、値が **DENY** または **SAMEORIGIN** の場合、Web サイトは現時点では埋め込むことができません。</span><span class="sxs-lookup"><span data-stu-id="f9a23-189">If **x-frame-options** exists in the response headers, and has a value of **DENY** or **SAMEORIGIN**, the website can't currently be embedded.</span></span> <span data-ttu-id="f9a23-190">アプリを安全に埋め込むには、アプリの所有者と連携する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a23-190">You will have to work with the owner of the app to enable it to be safely embedded.</span></span>

### <a name="developer-modeling-a-website-on-a-form"></a><span data-ttu-id="f9a23-191">[開発者] フォーム上の Web サイトをモデル化する</span><span class="sxs-lookup"><span data-stu-id="f9a23-191">[Developer] Modeling a website on a form</span></span>

<span data-ttu-id="f9a23-192">このトピックでは個人用設定によるサードパーティ製アプリまたは Web サイトの埋め込みに焦点を当てていますが、開発者は Visual Studio 開発経験を利用してフォームに埋め込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="f9a23-192">Although this topic is focused on embedding third-party apps or websites through personalization, developers can also embed them in a form by using the Visual Studio development experience.</span></span> <span data-ttu-id="f9a23-193">フォームに **WebsiteHostControl** コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-193">Just add a **WebsiteHostControl** control to the form.</span></span> <span data-ttu-id="f9a23-194">コントロールで使用できるメタデータ プロパティは、個人用設定のエクスペリエンスと同じ機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="f9a23-194">The metadata properties that are available for the control provide the same capabilities as the personalization experience.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
