---
title: ソーシャル共有モジュール
description: このトピックでは、ソーシャル共有モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795360"
---
# <a name="social-share-module"></a><span data-ttu-id="48a31-103">ソーシャル共有モジュール</span><span class="sxs-lookup"><span data-stu-id="48a31-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="48a31-104">このトピックでは、ソーシャル共有モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="48a31-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="48a31-105">ソーシャル共有モジュールを使用すると、ユーザーは E コマース サイト ページの URL を Facebook、Twitter、Pinterest、LinkedIn などのソーシャルメディアで共有することができます。</span><span class="sxs-lookup"><span data-stu-id="48a31-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="48a31-106">サイトページの URL は、メールを使用して共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="48a31-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="48a31-107">ソーシャル共有モジュールは、製品の情報共有でユーザーを支援するために、製品の詳細ページ (PDF) 上で一般に使用されます。</span><span class="sxs-lookup"><span data-stu-id="48a31-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="48a31-108">各ソーシャル共有モジュールは、ソーシャル共有項目モジュールのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="48a31-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="48a31-109">個々のソーシャル共有項目モジュールは、特定のソーシャル メディア サイトを参照するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="48a31-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="48a31-110">Facebook、Twitter、LinkedIn、メールとの統合は、標準ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="48a31-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="48a31-111">サイト ユーザーがソーシャルメディア シンボルを選択すると、それぞれのソーシャルメディア サイトに対して HTML iFrame が起動されます。</span><span class="sxs-lookup"><span data-stu-id="48a31-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="48a31-112">iFrame 内では、ユーザーは自分が表示していたページコンテンツにサインインして投稿することができます。</span><span class="sxs-lookup"><span data-stu-id="48a31-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="48a31-113">各ソーシャルメディア プラットフォームで cookie が追跡される可能性があるため、このモジュールでは、サイトユーザーに対して cookie の同意を通知するメッセージを受け入れるように要求します。</span><span class="sxs-lookup"><span data-stu-id="48a31-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="48a31-114">Cookie の同意が受け入れられない場合、このモジュールはページで非表示になります。</span><span class="sxs-lookup"><span data-stu-id="48a31-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="48a31-115">詳細については、[Cookie に関するコンプライアンス](cookie-compliance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48a31-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="48a31-116">次の図は、製品の詳細ページで使用されるソーシャル共有モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="48a31-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![ソーシャル共有モジュールの例](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="48a31-118">ソーシャル共有モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="48a31-118">Social share module properties</span></span>

| <span data-ttu-id="48a31-119">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48a31-119">Property name</span></span>             | <span data-ttu-id="48a31-120">先頭値</span><span class="sxs-lookup"><span data-stu-id="48a31-120">Value</span></span>                 | <span data-ttu-id="48a31-121">説明</span><span class="sxs-lookup"><span data-stu-id="48a31-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="48a31-122">キャプション</span><span class="sxs-lookup"><span data-stu-id="48a31-122">Caption</span></span>                  | <span data-ttu-id="48a31-123">テキスト</span><span class="sxs-lookup"><span data-stu-id="48a31-123">Text</span></span> | <span data-ttu-id="48a31-124">このプロパティは、モジュールのキャプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="48a31-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="48a31-125">方向</span><span class="sxs-lookup"><span data-stu-id="48a31-125">Orientation</span></span> | <span data-ttu-id="48a31-126">**水平** または **垂直**</span><span class="sxs-lookup"><span data-stu-id="48a31-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="48a31-127">このプロパティは、ソーシャルメディア項目のレイアウトの方向を定義します。</span><span class="sxs-lookup"><span data-stu-id="48a31-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="48a31-128">ソーシャル共有項目モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="48a31-128">Social share item module properties</span></span>
| <span data-ttu-id="48a31-129">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="48a31-129">Property name</span></span>             | <span data-ttu-id="48a31-130">先頭値</span><span class="sxs-lookup"><span data-stu-id="48a31-130">Value</span></span>                 | <span data-ttu-id="48a31-131">説明</span><span class="sxs-lookup"><span data-stu-id="48a31-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="48a31-132">ソーシャル メディア</span><span class="sxs-lookup"><span data-stu-id="48a31-132">Social media</span></span>              | <span data-ttu-id="48a31-133">**Facebook**、**Twitter** 、**Pinterest**、**LinkedIn** 、**メール**</span><span class="sxs-lookup"><span data-stu-id="48a31-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="48a31-134">ソーシャルメディア プラットフォームの一覧を含むドロップダウン メニュー。</span><span class="sxs-lookup"><span data-stu-id="48a31-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="48a31-135">アイコン</span><span class="sxs-lookup"><span data-stu-id="48a31-135">Icon</span></span> |<span data-ttu-id="48a31-136">画像</span><span class="sxs-lookup"><span data-stu-id="48a31-136">Image</span></span>    | <span data-ttu-id="48a31-137">この画像は、それぞれのソーシャルメディアに対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="48a31-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="48a31-138">ベスト プラクティスとして、各プラットフォームに使用される推奨されるイメージについては、ソーシャルメディア プラットフォームの SDK を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48a31-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="48a31-139">ソーシャル共有モジュールを購入ボックス モジュールに追加する</span><span class="sxs-lookup"><span data-stu-id="48a31-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="48a31-140">ソーシャル共有モジュールを購入ボックス モジュールに追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="48a31-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="48a31-141">Fabrikam サイトで、**ページ** を選択し、**DefaultPDP** ページを選択すると、製品の詳細ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48a31-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="48a31-142">**Buybox (必須)** スロットで、省略ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48a31-143">**モジュールの追加** ダイアログ ボックスで、**ソーシャル共有** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48a31-144">**ソーシャル共有** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48a31-145">**モジュールの追加** ダイアログ ボックスで、**SocialShare** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48a31-146">**SocialShare** モジュールのプロパティ ウィンドウで、**方向** で **水平方向** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="48a31-147">必要に応じてキャプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="48a31-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="48a31-148">**SocialShare** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="48a31-149">**モジュールの追加** ダイアログ ボックスで、**SocialShareItem** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="48a31-150">**SocialShareItem** モジュールのプロパティ ペインで、**ソーシャルメディア** から **Facebook** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="48a31-151">**SocialShareItem** モジュールのプロパティ ペインで、**アイコン** から **+ イメージの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="48a31-152">**メディア ピッカー** ダイアログ ボックスで、Facebook のロゴ イメージを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48a31-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="48a31-153">Facebook のロゴ イメージが表示されない場合は、**新しいメディア項目をアップロード** を選択してアップロードします。</span><span class="sxs-lookup"><span data-stu-id="48a31-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="48a31-154">必要に応じて、追加の **SocialShareItem** モジュールを追加およびコンフィギュレーションし ます。</span><span class="sxs-lookup"><span data-stu-id="48a31-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="48a31-155">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="48a31-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="48a31-156">このページには、ソーシャル共有モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48a31-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="48a31-157">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="48a31-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48a31-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="48a31-158">Additional resources</span></span>

[<span data-ttu-id="48a31-159">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="48a31-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="48a31-160">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="48a31-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="48a31-161">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="48a31-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]