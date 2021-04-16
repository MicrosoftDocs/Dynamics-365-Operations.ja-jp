---
title: robots.txt ファイルの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794238"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="bc76d-103">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="bc76d-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bc76d-104">このトピックでは、Microsoft Dynamics 365 Commerce の robots.txt ファイルを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bc76d-105">ロボット除外標準または robots.txt は、Web サイトが Web ロボットと通信するために使用する標準です。</span><span class="sxs-lookup"><span data-stu-id="bc76d-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="bc76d-106">参照すべきではない Web サイトのすべての領域について、Web ロボットに指示します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="bc76d-107">多くの場合、検索エンジンはロボットを使用して Web サイトをインデックス化します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="bc76d-108">サーバーからロボットを除外するには、サーバー上にファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="bc76d-109">このファイルでは、ロボットのアクセス ポリシーを指定します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="bc76d-110">ファイルは、ローカル URL **/robots.txt** で HTTP 経由でアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc76d-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="bc76d-111">robots.txt ファイルは、検索エンジンがサイトのコンテンツをインデックス化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="bc76d-112">Dynamics 365 Commerce では、ドメインの robots.txt ファイルをアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="bc76d-113">コマース環境内のドメインごとに、robots.txt ファイルを 1 つアップロードして、そのドメインに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="bc76d-114">robots.txt ファイルの詳細については、[Web ロボット ページ](https://www.robotstxt.org/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc76d-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="bc76d-115">robots.txt ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="bc76d-115">Upload a robots.txt file</span></span>

<span data-ttu-id="bc76d-116">[ロボットの除外標準](https://www.robotstxt.org/orig.html)に従って robots.txt ファイルを作成しおよび編集した後に、コマース作成ツールを使用するコンピュータでそのファイルにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="bc76d-117">ファイル名は、**robots.txt** である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc76d-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="bc76d-118">最適な結果を得るには、標準に記載されている形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc76d-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="bc76d-119">各コマースの顧客は、robots.txt ファイルの内容を検証および維持する責任があります。</span><span class="sxs-lookup"><span data-stu-id="bc76d-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="bc76d-120">robots.txt ファイルをアップロードするには、システム管理者としてコマースにログインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc76d-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="bc76d-121">コマースで robots.txt ファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bc76d-122">システム管理者として Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="bc76d-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="bc76d-123">左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="bc76d-124">**テナントの設定** で、**robots.txt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="bc76d-125">環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="bc76d-126">**管理** を選択して、環境内ドメインの robots.txt ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="bc76d-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="bc76d-127">右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **アップロード** ボタン (上向き矢印) を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="bc76d-128">ファイル参照ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="bc76d-129">ダイアログボックスで、関連付けられたドメインにアップロードする robots.txt ファイルを参照して選択し、**開く** を選択してアップロードを完了します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="bc76d-130">アップロード中に、コマースはファイルがテキスト ファイルであることを検証しますが、ファイルの内容は検証しません。</span><span class="sxs-lookup"><span data-stu-id="bc76d-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="bc76d-131">robots.txt ファイルのダウンロード</span><span class="sxs-lookup"><span data-stu-id="bc76d-131">Download a robots.txt file</span></span>

<span data-ttu-id="bc76d-132">コマースで robots.txt ファイルをダウンロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bc76d-133">システム管理者として Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="bc76d-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="bc76d-134">左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="bc76d-135">**テナントの設定** で、**robots.txt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="bc76d-136">環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="bc76d-137">**管理** を選択して、環境内ドメインの robots.txt ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="bc76d-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="bc76d-138">右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **ダウンロード** ボタン (下向き矢印) を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="bc76d-139">ファイル参照ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="bc76d-140">ダイアログ ボックスで、ローカル ドライブの目的の場所に移動し、ファイル名を確認するか入力して **保存** を選択してダウンロードを完了します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="bc76d-141">この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="bc76d-142">robots.txt ファイルの削除</span><span class="sxs-lookup"><span data-stu-id="bc76d-142">Delete a robots.txt file</span></span>

<span data-ttu-id="bc76d-143">コマースで robots.txt ファイルを削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="bc76d-144">システム管理者として Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="bc76d-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="bc76d-145">左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="bc76d-146">**テナントの設定** で、**robots.txt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="bc76d-147">環境に関連付けられているすべてのドメインのリストが、ウィンドウの主要部分に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="bc76d-148">**管理** を選択して、環境内ドメインの robots.txt ファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="bc76d-149">右側のメニューで、robots.txt ファイルに関連づけられているドメインの横にある **削除** ボタン (ごみ箱記号) を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="bc76d-150">ファイル ブラウザー ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-150">A file browser window appears.</span></span>
6. <span data-ttu-id="bc76d-151">ファイル ブラウザー ウィンドウで、ドメインから削除する robots.txt ファイルを参照して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="bc76d-152">警告のメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-152">A warning message box appears.</span></span>
7. <span data-ttu-id="bc76d-153">メッセージ ボックスで、**削除** を選択して robots.txt ファイルの削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="bc76d-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="bc76d-154">この手順を使用して、コマース作成ツールを介して以前にアップロードされた robots.txt ファイルのみを削除できます。</span><span class="sxs-lookup"><span data-stu-id="bc76d-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc76d-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bc76d-155">Additional resources</span></span>

[<span data-ttu-id="bc76d-156">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bc76d-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="bc76d-157">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="bc76d-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="bc76d-158">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="bc76d-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="bc76d-159">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="bc76d-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="bc76d-160">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="bc76d-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="bc76d-161">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="bc76d-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="bc76d-162">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="bc76d-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="bc76d-163">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bc76d-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="bc76d-164">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="bc76d-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="bc76d-165">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="bc76d-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
