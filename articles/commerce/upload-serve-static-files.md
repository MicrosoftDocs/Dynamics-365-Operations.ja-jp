---
title: 静的ファイルのアップロードと提供
description: このトピックでは、静的ファイルを Microsoft Dynamics 365 Commerce サイト ビルダーにアップロードする方法と、そのファイルを要求するために使用できるカスタム URL およびファイル名の作成方法について説明します。
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211022"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="c1495-103">静的ファイルのアップロードと提供</span><span class="sxs-lookup"><span data-stu-id="c1495-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1495-104">このトピックでは、静的ファイルを Microsoft Dynamics 365 Commerce サイト ビルダーにアップロードする方法と、そのファイルを要求するために使用できるカスタム URL およびファイル名の作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c1495-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="c1495-105">サードパーティの一部のコネクタでは、電子商取引サイトからファイルをホストし、提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1495-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="c1495-106">これらのコネクタは、特定のコールバック URL パスとファイル名への要求によってファイルが返されることを予期しています。</span><span class="sxs-lookup"><span data-stu-id="c1495-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="c1495-107">したがって、このトピックでは、Dynamics 365 Commerce 電子商取引サイト上にユーザー定義可能な URL とファイル名を持つ静的ファイルをアップロードして提供する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c1495-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="c1495-108">静的ファイルを返すサイト URL の作成</span><span class="sxs-lookup"><span data-stu-id="c1495-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="c1495-109">Commerce サイト ビルダーで静的ファイルを返すサイトの URL を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1495-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c1495-110">サイトのメディア ライブラリに移動し、定義する URL に要求によって提供する必要があるファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="c1495-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="c1495-111">ファイルが既にアップロードされている場合は、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="c1495-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="c1495-112">サイトの **URL** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c1495-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="c1495-113">**新規 \> 新しい URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="c1495-114">**新しい URL** ダイアログ ボックスで、**メディア ライブラリ アセット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="c1495-115">**URL パス** フィールドに URL パスを入力します。</span><span class="sxs-lookup"><span data-stu-id="c1495-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="c1495-116">パスにファイル名を含めます。</span><span class="sxs-lookup"><span data-stu-id="c1495-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="c1495-117">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-117">Select **Next**.</span></span> <span data-ttu-id="c1495-118">メディア ライブラリが開き、アップロードされた **ドキュメント** タイプのすべてのメディア アセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1495-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="c1495-119">手順 5 で定義した URL への要求に対して提供するファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="c1495-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-120">Select **Save**.</span></span>

<span data-ttu-id="c1495-121">この時点で、作成した URL はドラフト状態になっています。</span><span class="sxs-lookup"><span data-stu-id="c1495-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="c1495-122">URL をポイントしたファイルは、URL を発行するまで返されません。</span><span class="sxs-lookup"><span data-stu-id="c1495-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="c1495-123">URL を発行する前に、適切なデータを返すかどうかを検証できます。</span><span class="sxs-lookup"><span data-stu-id="c1495-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="c1495-124">URL の検証と発行</span><span class="sxs-lookup"><span data-stu-id="c1495-124">Validate and publish a URL</span></span>

<span data-ttu-id="c1495-125">発行前に URL を検証するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1495-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="c1495-126">サイトの **URL** に移動し、プレビューする URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="c1495-127">右側のプロパティ ウィンドウで、**編集** ボタンの下にある適切な URL リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="c1495-128">新しいブラウザー ウィンドウが開き、404 エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c1495-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="c1495-129">URL に **?preview=inprogress** クエリ文字列を追加し (例: `https://yoursite.com/callback.html?preview=inprogress`)、ページを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="c1495-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="c1495-130">メディア ライブラリにアップロードしたファイルが応答に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1495-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="c1495-131">URL を検証したら、それを公開できます。</span><span class="sxs-lookup"><span data-stu-id="c1495-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="c1495-132">サイトの **URL** に移動し、URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="c1495-133">コマンド バーで **発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="c1495-134">URL がポイントするファイルの更新</span><span class="sxs-lookup"><span data-stu-id="c1495-134">Update the file that a URL points to</span></span>

<span data-ttu-id="c1495-135">URL が発行されたら、それを更新して、別のファイルを指すようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="c1495-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="c1495-136">または、次のセクションで説明するように、異なるタイプのリソースをポイントするように URL を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="c1495-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="c1495-137">たとえば、URL を内部ページまたはリダイレクトにポイントすることができます。</span><span class="sxs-lookup"><span data-stu-id="c1495-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="c1495-138">URL で指定されているファイルを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1495-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="c1495-139">サイトの **URL** に移動し、更新する URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="c1495-140">右側のプロパティ ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="c1495-141">**URL の割り当て** で、**ステップ 2** ボックスをオンにし、メディア ライブラリから新しいドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="c1495-142">**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="c1495-143">URL がポイントするアセット タイプの更新</span><span class="sxs-lookup"><span data-stu-id="c1495-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="c1495-144">URL を更新して、内部ページまたはリダイレクトなどの別のタイプのアセット (リソース) をポイントするようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c1495-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="c1495-145">URL で指定されているアセット タイプを更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c1495-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="c1495-146">サイトの **URL** に移動し、更新する URL を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="c1495-147">右側のプロパティ ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="c1495-148">**URL の割り当て** の **ステップ 1** で、別のアセット タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="c1495-149">**ステップ 2** ボックスをオンにし、新しいアセットを選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="c1495-150">**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="c1495-151">URL パスの変更</span><span class="sxs-lookup"><span data-stu-id="c1495-151">Change the URL path</span></span>

<span data-ttu-id="c1495-152">URL が作成された後は、パスを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="c1495-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="c1495-153">ファイルまたはその他の種類のリソースに対応する URL パスを変更する必要がある場合は、新しい URL を作成し、既存のファイルまたはその他のリソースにマップしてから、古い URL を発行解除して削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1495-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="c1495-154">URL パスを変更するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c1495-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="c1495-155">新しい URL を作成して既存のファイルまたは別のリソースにマップするには、このトピックの前の[静的ファイルを返すサイト URL を作成する](#create-a-site-url-that-returns-a-static-file)セクションの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c1495-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="c1495-156">新しい URL を選択し、コマンド バーの **発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="c1495-157">新しい URL が発行されます。</span><span class="sxs-lookup"><span data-stu-id="c1495-157">The new URL is published.</span></span>
1. <span data-ttu-id="c1495-158">古い URL の発行を解除するには、URL を選択し、コマンド バーの **発行取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1495-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="c1495-159">古い URL を必要に応じて削除できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c1495-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1495-160">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c1495-160">Additional resources</span></span>

[<span data-ttu-id="c1495-161">デジタル資産管理の概要</span><span class="sxs-lookup"><span data-stu-id="c1495-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c1495-162">画像のアップロード</span><span class="sxs-lookup"><span data-stu-id="c1495-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c1495-163">ビデオのアップロード</span><span class="sxs-lookup"><span data-stu-id="c1495-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="c1495-164">画像とビデオ以外のファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="c1495-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="c1495-165">画像のトリミング</span><span class="sxs-lookup"><span data-stu-id="c1495-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c1495-166">画像の中心のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c1495-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]