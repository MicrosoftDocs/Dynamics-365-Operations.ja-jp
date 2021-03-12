---
title: クロスチャンネル共有の有効化と使用
description: このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのクロスチャンネル共有機能を有効にし、使用する方法について説明します。
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973134"
---
# <a name="enable-and-use-cross-channel-sharing"></a><span data-ttu-id="83e95-103">クロスチャンネル共有の有効化と使用</span><span class="sxs-lookup"><span data-stu-id="83e95-103">Enable and use cross-channel sharing</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83e95-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーのクロスチャンネル共有機能を有効にし、使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83e95-104">This topic describes how to enable and use the cross-channel sharing feature of Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="83e95-105">概要</span><span class="sxs-lookup"><span data-stu-id="83e95-105">Overview</span></span>

<span data-ttu-id="83e95-106">クロスチャンネル共有により、小売業者はサイトの複数のチャンネル間でコンテンツを再利用し、共有することができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-106">Cross-channel sharing lets retailers reuse and share content among multiple channels of a site.</span></span> <span data-ttu-id="83e95-107">この機能は、サイトチャンネルに互換性のある基本言語が設定されている場合や、多数のコンテンツ項目が共通である場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="83e95-107">This capability is useful when the site channels have a compatible base language, or when they have numerous content items in common.</span></span>

<span data-ttu-id="83e95-108">クロスチャンネル共有では、要求されたコンテンツのチャンネル固有のバージョンが見つからない場合に、使用可能なコンテンツを検索するための既定のチャンネルが有効になります。</span><span class="sxs-lookup"><span data-stu-id="83e95-108">Cross-channel sharing works by enabling a default channel that will be searched for available content when a channel-specific version of the requested content isn't found.</span></span> <span data-ttu-id="83e95-109">チャンネルで共有する予定のコンテンツは、既定のチャンネルで作成されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-109">Content that is intended to be shared among channels is created in the default channel.</span></span> <span data-ttu-id="83e95-110">そのコンテンツは、任意のサイトチャンネルで使用されるすべてのロケールに対してローカライズできます。</span><span class="sxs-lookup"><span data-stu-id="83e95-110">That content can be localized for any locale that is used on any site channel.</span></span>

## <a name="when-to-use-cross-channel-sharing"></a><span data-ttu-id="83e95-111">いつクロスチャンネル共有を使用するか</span><span class="sxs-lookup"><span data-stu-id="83e95-111">When to use cross-channel sharing</span></span>

<span data-ttu-id="83e95-112">1 つのサイトの複数のチャンネルでコンテンツを共有できる場合は、クロスチャネル共有が便利です。</span><span class="sxs-lookup"><span data-stu-id="83e95-112">Cross-channel sharing is useful when multiple channels on a single site can share content.</span></span> <span data-ttu-id="83e95-113">たとえば、1 つのサイトでグループ化された複数のブランドとストアフロントを持つ小売業者は、一部またはすべてのストアフロントの一部のコンテンツを共有できます。</span><span class="sxs-lookup"><span data-stu-id="83e95-113">For example, a retailer that has multiple brands and storefronts that are grouped under a single site can share some content among some or all of the storefronts.</span></span> <span data-ttu-id="83e95-114">この共有コンテンツには、契約条件、支払条件、出荷方法、およびよく寄せられる質問 (FAQ) などのページを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-114">This shared content can include pages for terms and conditions, payment terms, shipment methods, and frequently asked questions (FAQ).</span></span>

<span data-ttu-id="83e95-115">クロスチャンネル共有でもフラグメントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="83e95-115">Cross-channel sharing also supports fragments.</span></span> <span data-ttu-id="83e95-116">したがって、チャンネル固有のフラグメントを含むコンテンツ ページは、クロスチャネル コンテンツとして作成できます。</span><span class="sxs-lookup"><span data-stu-id="83e95-116">Therefore, a content page that contains channel-specific fragments can be created as cross-channel content.</span></span> <span data-ttu-id="83e95-117">この場合、コンテンツのほとんどはチャンネル間で共有されますが、クロスチャンネル ページ上のチャンネル固有のフラグメントは、対応する店頭チャンネルから要求された場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-117">In this case, although most of the content will be shared among channels, channel-specific fragments on a cross-channel page will be rendered only when they are requested from the corresponding storefront channel.</span></span>

<span data-ttu-id="83e95-118">1 つのチャンネルのみを含むサイト、またはコンテンツを共有できない複数のチャンネルを持つサイトは、クロスチャンネル共有の恩恵を受けることができません。</span><span class="sxs-lookup"><span data-stu-id="83e95-118">Sites that have only one channel, or sites that have multiple channels that can't share content, won't benefit from cross-channel sharing.</span></span>

## <a name="enable-cross-channel-sharing"></a><span data-ttu-id="83e95-119">クロスチャンネル共有の有効化</span><span class="sxs-lookup"><span data-stu-id="83e95-119">Enable cross-channel sharing</span></span>

<span data-ttu-id="83e95-120">クロスチャンネル共有は、サイト レベルで有効になります。</span><span class="sxs-lookup"><span data-stu-id="83e95-120">Cross-channel sharing is enabled at the site level.</span></span> <span data-ttu-id="83e95-121">この操作は一方向です。</span><span class="sxs-lookup"><span data-stu-id="83e95-121">This operation is one-way.</span></span> <span data-ttu-id="83e95-122">つまり、クロスチャンネル共有が有効になっていると、無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="83e95-122">In other words, after cross-channel sharing is enabled, it can't be disabled.</span></span>

<span data-ttu-id="83e95-123">コマース サイト ビルダーでクロスチャネル共有を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83e95-123">To enable cross-channel sharing in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="83e95-124">**サイト設定 \> 機能** に移動します。</span><span class="sxs-lookup"><span data-stu-id="83e95-124">Go to **Site settings \> Features**.</span></span>
1. <span data-ttu-id="83e95-125">**クロス チャンネル** 機能のオプションを **オン** にします。</span><span class="sxs-lookup"><span data-stu-id="83e95-125">Set the option for the **Cross Channel** feature to **On**.</span></span>

    ![クロス チャンネル オプションをコマース サイト ビルダーでオンに設定](./media/enabling-cross-channel-sharing.png)

<span data-ttu-id="83e95-127">クロスチャンネル共有を有効にした後、次の図に示す例のように、クロスチャンネルの情報は **サイト設定 \> 機能** で、**チャンネル** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-127">After you enable cross-channel sharing, cross-channel information will appear in the **Channels** section at **Site settings \> Features**, as the example in the following illustration shows.</span></span>

![クロスチャンネル共有が有効になった後、チャンネル情報は表示されます](./media/channels-cross-channel.png)

<span data-ttu-id="83e95-129">さらにクロスチャンネル共有を有効にすると、コマース サイト ビルダーの右上隅の **チャンネル** フィールドでは、次の図で示すように、クロスチャンネル コンテンツを管理するために使用できる **クロス チャンネル オンライン サイト** オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="83e95-129">Additionally, after you enable cross-channel sharing, the **Channel** field in the upper right of Commerce site builder will include a **Cross Channel Online Store** option that you can use to manage cross-channel content, as shown in the following illustration.</span></span>

![クロスチャンネル共有の有効後、チャンネル フィールドのクロス チャンネル オンライン ストアのオプション](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a><span data-ttu-id="83e95-131">クロスチャンネル コンテンツの作成および使用</span><span class="sxs-lookup"><span data-stu-id="83e95-131">Create and use cross-channel content</span></span>

<span data-ttu-id="83e95-132">複数の方法でチャンネル間のコンテンツを作成および使用することができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-132">You can create and use cross-channel content in multiple ways.</span></span> <span data-ttu-id="83e95-133">たとえば、クロスチャンネル フラグメントを作成したり、クロスチャンネルやチャネル固有のコンテンツを使用するクロスチャンネル ページを作成したり、チャンネル固有のフラグメントに対してクロスチャンネル フラグメントを上書きしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-133">For example, you can create cross-channel fragments, create cross-channel pages that use cross-channel and channel-specific content, and override cross-channel fragments with channel-specific versions of fragments.</span></span>

### <a name="create-a-cross-channel-fragment"></a><span data-ttu-id="83e95-134">クロスチャンネル フラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="83e95-134">Create a cross-channel fragment</span></span>

<span data-ttu-id="83e95-135">コマース サイト ビルダーでクロスチャンネル フラグメントを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83e95-135">To create a cross-channel fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="83e95-136">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="83e95-136">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="83e95-137">**新しいフラグメント** ダイアログ ボックスで、**プロモーション バナー** モジュールを選択し、**フラグメント名** に名前を入力します (たとえば、**クロスチャンネル バナー** など)。</span><span class="sxs-lookup"><span data-stu-id="83e95-137">In the **New fragment** dialog box, select the **Promo banner** module, and then, under **Fragment name**, enter a name (for example, **Cross-channel banner**).</span></span> <span data-ttu-id="83e95-138">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-138">Then select **OK**.</span></span>
1. <span data-ttu-id="83e95-139">**プロモーション バナー** モジュールのプロパティ ペインで 、**メッセージの追加** を選び、**メッセージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-139">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="83e95-140">**メッセージ** ダイアログ ボックスの **テキスト** で、**クロスチャンネル** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-140">In the **Message** dialog box, under **Text**, enter **Cross-channel**, and the select **OK**.</span></span> 
1. <span data-ttu-id="83e95-141">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="83e95-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="83e95-142">このクロスチャンネル フラグメントは、任意のサイト チャンネルで作成されたクロスチャンネルまたはチャンネル固有のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="83e95-142">This cross-channel fragment can be used on cross-channel or channel-specific pages that are created on any site channel.</span></span>

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a><span data-ttu-id="83e95-143">クロスチャンネル コンテンツを使用するクロスチャンネル ページの作成</span><span class="sxs-lookup"><span data-stu-id="83e95-143">Create a cross-channel page that uses cross-channel content</span></span>

<span data-ttu-id="83e95-144">サイトのすべてのチャンネルで、クロスチャンネル ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="83e95-144">Cross-channel pages can be used on any channel of your site.</span></span> <span data-ttu-id="83e95-145">したがって、共有コンテンツ ページを一度作成した後に、その後の更新を 1 か所で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-145">Therefore, you can create a shared content page one time and make any subsequent updates in a single place.</span></span> <span data-ttu-id="83e95-146">たとえば、URL `/toc` を含むクロスチャンネルの **使用条件** ページは、サイトのすべてのチャンネル間で共有できます。</span><span class="sxs-lookup"><span data-stu-id="83e95-146">For example, a cross-channel **Terms and conditions** page that has the URL `/toc` can be shared among all the channels of a site.</span></span> <span data-ttu-id="83e95-147">サイト チャンネルのベース URL が `www.fabrikam.com/brand1` および `www.fabrikam.com/brand2` である場合、同じクロスチャンネル、共有の **使用条件** ページが `www.fabrikam.com/brand1/toc` および `www.fabrikam.com/brand2/toc` で、両方のサイト チャンネルの URL からを使用でき ます。</span><span class="sxs-lookup"><span data-stu-id="83e95-147">If the base URLs for the site channels are `www.fabrikam.com/brand1` and `www.fabrikam.com/brand2`, the same cross-channel, shared **Terms and conditions** page will be available from both site channel URLs, at `www.fabrikam.com/brand1/toc` and `www.fabrikam.com/brand2/toc`, respectively.</span></span> <span data-ttu-id="83e95-148">**使用条件** ページを後で更新する必要がある場合は、単一の共有ページのみを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83e95-148">If the **Terms and conditions** page must be updated later, you have to update only the single, shared page.</span></span>

<span data-ttu-id="83e95-149">クロスチャンネル コンテンツを使用するコマース サイト ビルダーでクロスチャンネル ページを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83e95-149">To create a cross-channel page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="83e95-150">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="83e95-150">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="83e95-151">**テンプレートの選択** ダイアログ ボックスで、**マーケティング** などのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-151">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="83e95-152">**ページ名** に、そのページの名前 (たとえば、**クロスチャンネル ページ**) を入力します。</span><span class="sxs-lookup"><span data-stu-id="83e95-152">Under **Page name**, enter a name for the page (for example, **Cross-channel page**).</span></span>
1. <span data-ttu-id="83e95-153">**ページ URL** で、ページの URL を入力し (たとえば、**examplepage**)、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-153">Under **Page URL**, enter a page URL (for example, **examplepage**), and then select **OK**.</span></span>
1. <span data-ttu-id="83e95-154">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-154">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="83e95-155">**フラグメントの追加** ダイアログ ボックスで、キャンペーンのバナーを持つ前に作成したクロスチャンネル フラグメントを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-155">In the **Add fragment** dialog box, select the cross-channel fragment that you created earlier that has a promo banner, and then select **OK**.</span></span>
1. <span data-ttu-id="83e95-156">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="83e95-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="83e95-157">「クロスチャンネル」という内容のキャンペーン バナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-157">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="83e95-158">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="83e95-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a><span data-ttu-id="83e95-159">チャンネル固有のコンテンツを使用するクロスチャンネル ページの作成</span><span class="sxs-lookup"><span data-stu-id="83e95-159">Create a channel-specific page that uses cross-channel content</span></span>

<span data-ttu-id="83e95-160">チャンネル固有のページ上にあるクロスチャンネル コンテンツを使用することにより、共有コンテンツ フラグメントを一度作成した後に、チャンネル固有のページで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="83e95-160">By using cross-channel content on channel-specific pages, you can create a shared content fragment one time and then use it on channel-specific pages.</span></span> <span data-ttu-id="83e95-161">この「単一ソーシング」は、契約条件、支払条件、連絡先情報などの共有コンテンツに適しています。</span><span class="sxs-lookup"><span data-stu-id="83e95-161">This "single sourcing" is useful for shared content such as terms and conditions, payment terms, or contact information.</span></span>

<span data-ttu-id="83e95-162">クロスチャンネル コンテンツを使用するコマース サイト ビルダーでチャンネル固有のページを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83e95-162">To create a channel-specific page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="83e95-163">**Fabrikam 拡張オンライン ストア** などの特定のチャンネル内から、**ページ** へ移動し、**新規** を選択して新しいページを作成します。</span><span class="sxs-lookup"><span data-stu-id="83e95-163">From within a specific channel, such as **Fabrikam extended online store**, go to **Pages**, and then select **New** to create a new page.</span></span>
1. <span data-ttu-id="83e95-164">**テンプレートの選択** ダイアログ ボックスで、**マーケティング** などのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-164">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="83e95-165">**ページ名** に、そのページの名前 (たとえば、**チャンネル固有のページ**) を入力します。</span><span class="sxs-lookup"><span data-stu-id="83e95-165">Under **Page name**, enter a name for the page (for example, **Channel-specific page**).</span></span>
1. <span data-ttu-id="83e95-166">**ページ URL** で、ページの URL を入力し (たとえば、**channelspecificpage**)、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-166">Under **Page URL**, enter a page URL (for example, **channelspecificpage**), and then select **OK**.</span></span>
1. <span data-ttu-id="83e95-167">新規ページの **メイン** スロットで、省略記号ボタン (**...**) を選択してから、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-167">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="83e95-168">**フラグメントの追加** ダイアログ ボックスの **チャンネル** で、**クロス チャンネル オンライン ストア** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-168">In the **Add fragment** dialog box, under **Channel**, select **Cross Channel Online Store**.</span></span> <span data-ttu-id="83e95-169">前に作成したクロスチャンネル フラグメントが一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-169">The cross-channel fragment that you created earlier should appear in the list.</span></span> <span data-ttu-id="83e95-170">それを選び、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-170">Select it, and then select **OK**.</span></span>
1. <span data-ttu-id="83e95-171">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="83e95-171">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="83e95-172">「クロスチャンネル」という内容のキャンペーン バナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-172">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="83e95-173">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="83e95-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a><span data-ttu-id="83e95-174">クロスチャンネル ページのチャンネル固有のバージョンを作成</span><span class="sxs-lookup"><span data-stu-id="83e95-174">Create a channel-specific version of a cross-channel page</span></span>

<span data-ttu-id="83e95-175">クロスチャンネル共有では、クロスチャンネル コンテンツの上書きがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="83e95-175">Cross-channel sharing supports overrides of cross-channel content.</span></span> <span data-ttu-id="83e95-176">たとえば、サイトチャンネルの 1 つを除くすべてが、同じコンテンツを共有します。</span><span class="sxs-lookup"><span data-stu-id="83e95-176">For example, all but one of your site channels share the same piece of content.</span></span> <span data-ttu-id="83e95-177">1 つのサイトチャンネルに異なるコンテンツが必要です。</span><span class="sxs-lookup"><span data-stu-id="83e95-177">That one site channel requires different content.</span></span> <span data-ttu-id="83e95-178">そのため異なるコンテンツを実装するには、クロスチャンネルページのチャンネル固有のバージョンを作成して、チャンネル固有のコンテンツを含むクロスチャンネルのコンテンツを上書きします。</span><span class="sxs-lookup"><span data-stu-id="83e95-178">To implement the different content for it, you override the cross-channel content with channel-specific content by creating a channel-specific version of the cross-channel page.</span></span>

<span data-ttu-id="83e95-179">コマース サイト ビルダーでクロスチャンネル ページのチャンネル固有のバージョンを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83e95-179">To create a channel-specific version of a cross-channel page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="83e95-180">右上にある **チャンネル** フィールドで、**クロス チャンネル オンライン ストア** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-180">In the **Channel** field in the upper right, select **Cross Channel Online Store**.</span></span>
1. <span data-ttu-id="83e95-181">以前作成したクロスチャンネル ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="83e95-181">Open the cross-channel page that you created earlier.</span></span>
1. <span data-ttu-id="83e95-182">右上の **チャンネル** フィールドで、特定のコンテンツを持つチャンネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-182">In the **Channel** field in the upper right, select the channel that should have specific content.</span></span> <span data-ttu-id="83e95-183">ページ エディターに、新しいページ バリアントを作成するかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-183">The page editor shows a message that prompts you to create a new page variant.</span></span>
1. <span data-ttu-id="83e95-184">**ページ バリアントを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-184">Select **Create page variant**.</span></span>
1. <span data-ttu-id="83e95-185">ページ バリアントの **メイン** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-185">In the **Main** slot of the page variant, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="83e95-186">**モジュールの追加** ダイアログ ボックスで、**キャンペーン バナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-186">In the **Add Module** dialog box, select the **Promo banner** module, and then select **OK**.</span></span>
1. <span data-ttu-id="83e95-187">**プロモーション バナー** モジュールのプロパティ ペインで 、**メッセージの追加** を選び、**メッセージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-187">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="83e95-188">**メッセージ** ダイアログ ボックスの **テキスト** で、**チャンネル固有** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83e95-188">In the **Message** dialog box, under **Text**, enter **Channel-specific**, and the select **OK**.</span></span>
1. <span data-ttu-id="83e95-189">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="83e95-189">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="83e95-190">「チャンネル固有」という内容のキャンペーン バナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-190">You should see the promo banner that says, "Channel-specific."</span></span>
1. <span data-ttu-id="83e95-191">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="83e95-191">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="83e95-192">これで、チャンネルのベース URL を使用して、そのサイト上のクロスチャンネル ページの URL に移動すると、クロスチャンネル コンテンツの代わりに、チャンネル固有のコンテンツが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83e95-192">Now, if you use the base URL of the channel and go to the URL of the cross-channel page on that site, you will see the channel-specific content instead of the cross-channel content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83e95-193">追加リソース</span><span class="sxs-lookup"><span data-stu-id="83e95-193">Additional resources</span></span>

[<span data-ttu-id="83e95-194">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="83e95-194">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="83e95-195">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="83e95-195">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="83e95-196">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="83e95-196">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="83e95-197">公開グループの作業</span><span class="sxs-lookup"><span data-stu-id="83e95-197">Work with publish groups</span></span>](publish-groups.md)
