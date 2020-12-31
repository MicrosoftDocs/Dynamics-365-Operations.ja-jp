---
title: URL リダイレクトの一括アップロード
description: このトピックでは、Microsoft Dynamics 365 Commerce でリダイレクトのコンマ区切り値 (csv) ファイルをアップロードすることによって、URL リダイレクトを一括して実装する方法について説明します。
author: BrianShook
manager: annbe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8268045832a95d6a2413a6e82d86d4b48a14bb76
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517344"
---
# <a name="upload-url-redirects-in-bulk"></a><span data-ttu-id="3ba17-103">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="3ba17-103">Upload URL redirects in bulk</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ba17-104">このトピックでは、Microsoft Dynamics 365 Commerce でリダイレクトのコンマ区切り値 (csv) ファイルをアップロードすることによって、URL リダイレクトを一括して実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-104">This topic describes how to implement URL redirects in bulk by uploading a redirect comma-separate values (CSV) file in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3ba17-105">概要</span><span class="sxs-lookup"><span data-stu-id="3ba17-105">Overview</span></span>

<span data-ttu-id="3ba17-106">Dynamics 365 Commerce で新しい電子商取引サイトの作成が完了し、稼動する準備ができたら、古いサイトから新しいサイトにドメイン名システム (DNS) スイッチを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-106">After you've finished creating a new e-commerce site in Dynamics 365 Commerce, and it's ready to go live, you must make the Domain Name System (DNS) switch from your old site to your new site.</span></span> <span data-ttu-id="3ba17-107">このスイッチを設定すると、新しいサイトの URL が古いサイトの URL とは異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-107">After you make this switch, the URLs for the new site will likely differ from the URLs for the old site.</span></span> <span data-ttu-id="3ba17-108">特定の URL の場合は、古い URL を使用するトラフィックを新しい URL にリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-108">For specific URLs, traffic that uses the old URL can be redirected to the new URL.</span></span> <span data-ttu-id="3ba17-109">このようにして、サイトの訪問者が目的の場所にアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-109">In this way, you ensure that site visitors reach the desired location.</span></span> <span data-ttu-id="3ba17-110">リダイレクトすることにより、顧客のリンク切れを防ぐことができます。また、確立された検索エンジン最適化 (SEO) の結果を管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-110">Redirects help prevent broken links for your customers and help you maintain your established search engine optimization (SEO) results.</span></span>

<span data-ttu-id="3ba17-111">個々のリンクのリダイレクトを DNS に手動で構成することもできますが、複数のリンクをリダイレクトする必要がある場合は手動による構成を行う方が手間がかかります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-111">Although redirects for individual links can be manually configured in DNS, manual configuration becomes tedious if multiple links must be redirected.</span></span> <span data-ttu-id="3ba17-112">リダイレクト プロセスを効率化するために、Commerce では、サイトの一括リダイレクト マップを含むデータ ファイルをアップロードする機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="3ba17-112">To streamline the redirect process, Commerce provides the capability to upload a data file that contains bulk redirect mappings for your site.</span></span> <span data-ttu-id="3ba17-113">Commerce サイト ビルダーのサイト設定では、システム管理者が、URL の一括リダイレクトを処理する CSV ファイルをアップロードして公開することができます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-113">In the site settings in Commerce site builder, your system admin can upload and publish a CSV file that handles bulk URL redirects.</span></span>

## <a name="redirect-csv-file"></a><span data-ttu-id="3ba17-114">CSV ファイルのリダイレクト</span><span class="sxs-lookup"><span data-stu-id="3ba17-114">Redirect CSV file</span></span>

<span data-ttu-id="3ba17-115">URL リダイレクトを処理するために、Commerce では、単純ですが、特定の CSV ファイルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3ba17-115">To handle URL redirects, Commerce supports a simple but specific CSV file.</span></span> <span data-ttu-id="3ba17-116">このファイルでは、次のスキーマを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-116">This file uses the following schema:</span></span>

`source URL, target URL, redirect type, case sensitivity`

<span data-ttu-id="3ba17-117">このスキーマの要素の説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-117">Here is an explanation of the elements of this schema:</span></span>

- <span data-ttu-id="3ba17-118">**ソース URL** : リダイレクトが必要な元の URL。</span><span class="sxs-lookup"><span data-stu-id="3ba17-118">**Source URL**: The original URL that must be redirected.</span></span>
- <span data-ttu-id="3ba17-119">**対象 URL** 元の URL に移動するときにユーザーに対してリダイレクトされる URL。</span><span class="sxs-lookup"><span data-stu-id="3ba17-119">**Target URL**: The URL that users will be redirected to when they try to go to the source URL.</span></span>
- <span data-ttu-id="3ba17-120">**リダイレクト タイプ** : リダイレクトのタイプに応じて、この値を **301** または **302** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-120">**Redirect type**: Set this value to **301** or **302**, depending on the type of redirect that you want to use.</span></span>

    - <span data-ttu-id="3ba17-121">**301** リダイレクト タイプは、恒久的なリダイレクトを表し、最も頻繁に使用されるリダイレクト タイプです。</span><span class="sxs-lookup"><span data-stu-id="3ba17-121">The **301** redirect type represents permanent redirects and is the most frequently used redirect type.</span></span> <span data-ttu-id="3ba17-122">検索エンジンの最適化 (SEO) のランク付けを保守する必要がある場合は、このオプションをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3ba17-122">It's the best option when you must maintain search engine optimization (SEO) rankings.</span></span>
    - <span data-ttu-id="3ba17-123">**302** リダイレクト タイプは一時的なリダイレクトを表し、あまり使用されることはありません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-123">The **302** redirect type represents temporary redirects and is less frequently used.</span></span> <span data-ttu-id="3ba17-124">一時メンテナンスまたはその他の非永続的なシナリオにおいてリンクの対象を保守する必要がある場合は、このオプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3ba17-124">It's the best option when you must maintain link targeting during temporary maintenance or other non-permanent scenarios.</span></span>

- <span data-ttu-id="3ba17-125">**大文字と小文字を区別する** : ソース URL パスが大文字と小文字を区別する場合は、この値を **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-125">**Case sensitivity**: Set this value to **true** if your source URL paths are case-sensitive.</span></span> <span data-ttu-id="3ba17-126">これにより、ソース URL パスに対して大文字と小文字を区別することができます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-126">Case sensitivity will then be honored for the source URL paths.</span></span> <span data-ttu-id="3ba17-127">大文字と小文字を区別する必要がない場合は、この値を **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-127">Set this value to **false** if case sensitivity isn't required.</span></span> <span data-ttu-id="3ba17-128">この値を空白のままにすると、規定値の **false** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-128">If you leave this value blank, the default value of **false** is used.</span></span>

<span data-ttu-id="3ba17-129">次の例では、リダイレクトされた CSV ファイルのリダイレクト行セットを示します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-129">The following example shows a set of redirect rows in a redirect CSV file.</span></span>

```plaintext
https://www.contoso.com/shop, https://www.fabrikam.com/allstores, 301, true

https://www.contoso.com/news, https://www.fabrikam.com/updates, 301, false

https://www.contoso.com/news, https://www.fabrikam.com/updates, 301
```

> [!IMPORTANT]
> <span data-ttu-id="3ba17-130">次のルールに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-130">The following rules must be followed.</span></span> <span data-ttu-id="3ba17-131">それ以外の場合、バルク URL リダイレクトは正常に機能しません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-131">Otherwise, the bulk URL redirects won't work correctly.</span></span>
>
> - <span data-ttu-id="3ba17-132">**CSV ファイルでヘッダーを使用することはできません** : 最初の行または最上位の行は、最初のリダイレクト行で開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-132">**No header is allowed in the CSV file**: The first or topmost row must start with the first redirect row.</span></span>
> - <span data-ttu-id="3ba17-133">**循環するエントリはありません** : 行内のソース URL を対象 URL として同じ行に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-133">**There must be no circular entries**: The source URL in a row must not be used as the target URL in the same row.</span></span> <span data-ttu-id="3ba17-134">また、CSV ファイルの別の行または DNS リダイレクトのいずれかで、対象 URL がリンク元 URL としてリンクされている実装を回避する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-134">You must also avoid implementations where a target URL is linked back as a source URL, either in a different row of the CSV file or in a DNS redirect.</span></span>
> - <span data-ttu-id="3ba17-135">**ソースと対象の URL は、有効な URL 形式である必要があります** : スペースまたは無効な文字を URL で使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-135">**Source and target URLs must be in valid URL format**: No spaces or invalid characters can be used in URLs.</span></span>
> - <span data-ttu-id="3ba17-136">**クエリ文字列 URL はサポートされません** : ソースまたは対象 URL として指定されたクエリ文字列は実行されません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-136">**No query string URLs are supported**: Commerce won't run query strings that are provided as source or target URLs.</span></span>
> - <span data-ttu-id="3ba17-137">**CSV ファイルは有効な CSV 形式にする必要があります** : CSV ファイルには、コンマ区切り値、リダイレクトごとに1行ずつ、およびファイル形式が有効である必要があります。また、ヘッダーを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3ba17-137">**The CSV file must be in valid CSV format**: The CSV file must have comma-separated values, a separate line for each redirect, and valid file formatting, and it must have no header.</span></span>

## <a name="upload-a-redirect-csv-file"></a><span data-ttu-id="3ba17-138">リダイレクト CSV ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="3ba17-138">Upload a redirect CSV file</span></span>

<span data-ttu-id="3ba17-139">リダイレクト用の CSV ファイルは、Commerce サイト ビルダーを使用してアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-139">Redirect CSV files can be uploaded by using Commerce site builder.</span></span> <span data-ttu-id="3ba17-140">リダイレクト用の CSV ファイルをサイトにアップロードするユーザーは、そのサイトの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ba17-140">The person who uploads a redirect CSV file to a site must be an admin for that site.</span></span>

<span data-ttu-id="3ba17-141">リダイレクト CSV ファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-141">To upload a redirect CSV file, follow these steps.</span></span>

1. <span data-ttu-id="3ba17-142">Commerce サイトビルダーで、一括 URL リダイレクトを受信するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-142">In Commerce site builder, go to the site that will receive the bulk URL redirects.</span></span>
1. <span data-ttu-id="3ba17-143">**サイト 設定 \> 一般** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-143">Go to **Site settings \> General**.</span></span>
1. <span data-ttu-id="3ba17-144">**URL リダイレクト マッピング** で **アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-144">Under **URL Redirect Mapping**, select **Upload**.</span></span>
1. <span data-ttu-id="3ba17-145">ファイル エクスプローラーで、CSV ファイルを検索して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-145">In File Explorer, browse to your CSV file, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="3ba17-146">**URL リダイレクト マッピング** で、リダイレクトを有効にするにはこのオプションを **ON** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-146">Under **URL Redirect Mapping**, set the option to **On** to activate the redirects.</span></span>
1. <span data-ttu-id="3ba17-147">コマンド バーで、**保存と発行** を選択し、この変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="3ba17-147">On the command bar, select **Save and Publish** to commit the changes.</span></span> <span data-ttu-id="3ba17-148">リダイレクトが有効になるまで最大 15 分間待ちます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-148">Allow up to 15 minutes for the redirects to take effect.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ba17-149">一度に読み込むことができるのはサイトごとに 1 つのバルクリダイレクト CSV ファイルのみです。</span><span class="sxs-lookup"><span data-stu-id="3ba17-149">Only one bulk redirect CSV file can be loaded and active per site at any time.</span></span>

## <a name="update-an-uploaded-redirect-csv-file"></a><span data-ttu-id="3ba17-150">アップロードされたリダイレクト CSV ファイルの更新</span><span class="sxs-lookup"><span data-stu-id="3ba17-150">Update an uploaded redirect CSV file</span></span>

<span data-ttu-id="3ba17-151">以前にアップロードされたリダイレクト用 CSV ファイルをダウンロードして参照することができます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-151">A previously uploaded redirect CSV file can be downloaded for reference.</span></span> <span data-ttu-id="3ba17-152">また、ファイルをダウンロードした後に、ファイルを編集してからアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-152">Alternatively, after the file is downloaded, it can be edited and then uploaded again.</span></span>

<span data-ttu-id="3ba17-153">アップロードされたリダイレクト CSV ファイルをアップロードするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-153">To update an uploaded redirect CSV file, follow these steps.</span></span>

1. <span data-ttu-id="3ba17-154">Commerce サイトビルダーで、一括 URL リダイレクトを受信するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-154">In Commerce site builder, go to the site that will receive the bulk URL redirects.</span></span>
1. <span data-ttu-id="3ba17-155">**サイト 設定 \> 一般** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-155">Go to **Site settings \> General**.</span></span>
1. <span data-ttu-id="3ba17-156">**URL リダイレクト マッピング** で **ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-156">Under **URL Redirect Mapping**, select **Download**.</span></span>
1. <span data-ttu-id="3ba17-157">ファイルをローカル コンピューターに保存します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-157">Save the file to your local computer.</span></span>
1. <span data-ttu-id="3ba17-158">必要に応じて CSV ファイルを編集し、保存します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-158">Edit the CSV file as appropriate, and then save it.</span></span>
1. <span data-ttu-id="3ba17-159">**URL リダイレクト マッピング** で **置換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-159">Under **URL Redirect Mapping**, select **Replace**.</span></span>
1. <span data-ttu-id="3ba17-160">ファイル エクスプローラーで、置換 CSV ファイルを検索して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-160">In File Explorer, browse to the replacement CSV file, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="3ba17-161">**URL リダイレクト マッピング** で、リダイレクトを有効にするにはこのオプションを **ON** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-161">Under **URL Redirect Mapping**, set the option to **On** to activate the redirects.</span></span>
1. <span data-ttu-id="3ba17-162">コマンド バーで、**保存と発行** を選択し、この変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="3ba17-162">On the command bar, select **Save and Publish** to commit the changes.</span></span> <span data-ttu-id="3ba17-163">リダイレクトが有効になるまで最大 15 分間待ちます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-163">Allow up to 15 minutes for the redirects to take effect.</span></span>

## <a name="turn-off-bulk-redirects"></a><span data-ttu-id="3ba17-164">一括リダイレクトをオフにする</span><span class="sxs-lookup"><span data-stu-id="3ba17-164">Turn off bulk redirects</span></span>

<span data-ttu-id="3ba17-165">アップロードされたリダイレクト CSV ファイルでの一括リダイレクトを無効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-165">To turn off the bulk redirects in an uploaded redirect CSV file, follow these steps.</span></span>

1. <span data-ttu-id="3ba17-166">有効であるが存在しない、ソースおよび対象 URL (`https://www.com,https://www.com,301`など) を持つ新しいCSVファイル を作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-166">Create and save a new CSV file that has valid but nonexistent source and target URLs (for example, `https://www.com,https://www.com,301`).</span></span>
1. <span data-ttu-id="3ba17-167">Commerce サイトビルダーで、一括 URL リダイレクトを受信するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-167">In Commerce site builder, go to the site that will receive the bulk URL redirects.</span></span>
1. <span data-ttu-id="3ba17-168">**サイト 設定 \> 一般** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-168">Go to **Site settings \> General**.</span></span>
1. <span data-ttu-id="3ba17-169">**URL リダイレクト マッピング** で **置換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-169">Under **URL Redirect Mapping**, select **Replace**.</span></span>
1. <span data-ttu-id="3ba17-170">ファイル エクスプローラーで、新しい CSV ファイルを検索して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-170">In File Explorer, browse to  your new CSV file, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="3ba17-171">**URL リダイレクト マッピング** で、リダイレクトを有効にするにはこのオプションを **ON** に設定します。</span><span class="sxs-lookup"><span data-stu-id="3ba17-171">Under **URL Redirect Mapping**, set the option to **On** to activate the redirects.</span></span> 
1. <span data-ttu-id="3ba17-172">コマンド バーで、**保存と発行** を選択し、この変更をコミットします。</span><span class="sxs-lookup"><span data-stu-id="3ba17-172">On the command bar, select **Save and Publish** to commit the changes.</span></span> <span data-ttu-id="3ba17-173">リダイレクトが機能しなくなるまで最大 15 分間待ちます。</span><span class="sxs-lookup"><span data-stu-id="3ba17-173">Allow up to 15 minutes for the redirects to stop working.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ba17-174">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3ba17-174">Additional resources</span></span>

[<span data-ttu-id="3ba17-175">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3ba17-175">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="3ba17-176">新しい E コマース テナントの配置</span><span class="sxs-lookup"><span data-stu-id="3ba17-176">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="3ba17-177">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="3ba17-177">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="3ba17-178">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="3ba17-178">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="3ba17-179">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="3ba17-179">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="3ba17-180">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="3ba17-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="3ba17-181">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="3ba17-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="3ba17-182">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3ba17-182">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="3ba17-183">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="3ba17-183">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="3ba17-184">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="3ba17-184">Enable location-based store detection</span></span>](enable-store-detection.md)
