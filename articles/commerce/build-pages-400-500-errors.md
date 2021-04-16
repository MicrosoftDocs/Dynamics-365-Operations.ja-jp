---
title: 4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799653"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="790fa-103">4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成</span><span class="sxs-lookup"><span data-stu-id="790fa-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="790fa-104">このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="790fa-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="790fa-105">要求が成功しなかった場合、サーバーは HTTP ステータス コード エラーの応答を発行します。</span><span class="sxs-lookup"><span data-stu-id="790fa-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="790fa-106">ページが見つからない場合は、404 ステータス コードがキャプチャされて返され、サーバー エラーが発生した場合は 500 ステータス コードがキャプチャされて返されます。</span><span class="sxs-lookup"><span data-stu-id="790fa-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="790fa-107">Dynamics 365 Commerce では、アプリケーション ユーザーは、これらのステータス コード エラーの応答について、ユーザーに対して表示されるカスタム ステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="790fa-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="790fa-108">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="790fa-108">Build a status code error response page</span></span>

<span data-ttu-id="790fa-109">ステータス コード エラーの応答ページの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="790fa-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="790fa-110">優先的に使用する Web ブラウザーで、Dynamics 365 Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="790fa-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="790fa-111">4xx/5xx ステータス コード エラーの応答ページを構築するサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="790fa-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="790fa-112">テンプレートの構築</span><span class="sxs-lookup"><span data-stu-id="790fa-112">Build the template</span></span>

<span data-ttu-id="790fa-113">ステータス コード エラーの応答ページのテンプレートの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="790fa-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="790fa-114">**テンプレート** に移動する。</span><span class="sxs-lookup"><span data-stu-id="790fa-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="790fa-115">**新規** を選択して、ページのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="790fa-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="790fa-116">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、新規テンプレートの名称を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="790fa-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="790fa-117">ステータス コード エラーの応答ページに含める構造に基づいて、テンプレートを構築します。</span><span class="sxs-lookup"><span data-stu-id="790fa-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="790fa-118">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="790fa-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="790fa-119">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="790fa-119">Build the status code error response page</span></span>

<span data-ttu-id="790fa-120">ステータス コード エラーの応答ページを構築するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="790fa-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="790fa-121">**ページ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="790fa-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="790fa-122">**新規** を選択して、ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="790fa-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="790fa-123">**テンプレートの選択** ダイアログボックスでテンプレートを選択し、**ページ名** に、[ステータスコードのエラー応答] ページの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="790fa-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="790fa-124">**ページの URL** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="790fa-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="790fa-125">ページを構築します。</span><span class="sxs-lookup"><span data-stu-id="790fa-125">Build the page.</span></span>
1. <span data-ttu-id="790fa-126">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="790fa-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="790fa-127">4xx および 5xx ステータス コード エラー用に個別のステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="790fa-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="790fa-128">または、両方のエラー カテゴリに同じ一般的なステータス コード エラーの応答ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="790fa-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="790fa-129">ステータス コード エラーの応答ページのリダイレクトを設定する</span><span class="sxs-lookup"><span data-stu-id="790fa-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="790fa-130">ステータス コード エラーの応答ページのリダイレクトを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="790fa-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="790fa-131">**URL \> 新規 \> 新しいエイリアス** に移動して、構築したステータス コード エラーの応答ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="790fa-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="790fa-132">**エイリアス** フィールドに、リダイレクトを設定するステータス コード エラーの応答ページに応じて、**default-4xx** または **default-5xx** のいずれかを入力します。</span><span class="sxs-lookup"><span data-stu-id="790fa-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="790fa-133">これらのエイリアスは公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="790fa-133">These aliases must be published.</span></span> <span data-ttu-id="790fa-134">そうしない場合、リダイレクトは機能しません。</span><span class="sxs-lookup"><span data-stu-id="790fa-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="790fa-135">**OK** を選択してリンクをコミットします。</span><span class="sxs-lookup"><span data-stu-id="790fa-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="790fa-136">両方のエラー カテゴリに対して単一のステータス コード エラー の応答ページを使用している場合は、この手順を繰り返して、もう一方のエラー カテゴリのエイリアスを同じページにリンクします。</span><span class="sxs-lookup"><span data-stu-id="790fa-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="790fa-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="790fa-137">Additional resources</span></span>

[<span data-ttu-id="790fa-138">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="790fa-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="790fa-139">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="790fa-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="790fa-140">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="790fa-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
