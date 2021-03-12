---
title: 4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d21ce20b2c7ac8c656a718749dabd76f33893da8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991468"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="34b16-103">4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成</span><span class="sxs-lookup"><span data-stu-id="34b16-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34b16-104">このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="34b16-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34b16-105">概要</span><span class="sxs-lookup"><span data-stu-id="34b16-105">Overview</span></span>

<span data-ttu-id="34b16-106">要求が成功しなかった場合、サーバーは HTTP ステータス コード エラーの応答を発行します。</span><span class="sxs-lookup"><span data-stu-id="34b16-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="34b16-107">ページが見つからない場合は、404 ステータス コードがキャプチャされて返され、サーバー エラーが発生した場合は 500 ステータス コードがキャプチャされて返されます。</span><span class="sxs-lookup"><span data-stu-id="34b16-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="34b16-108">Dynamics 365 Commerce では、アプリケーション ユーザーは、これらのステータス コード エラーの応答について、ユーザーに対して表示されるカスタム ステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34b16-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="34b16-109">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="34b16-109">Build a status code error response page</span></span>

<span data-ttu-id="34b16-110">ステータス コード エラーの応答ページの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34b16-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34b16-111">優先的に使用する Web ブラウザーで、Dynamics 365 Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="34b16-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="34b16-112">4xx/5xx ステータス コード エラーの応答ページを構築するサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="34b16-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="34b16-113">テンプレートの構築</span><span class="sxs-lookup"><span data-stu-id="34b16-113">Build the template</span></span>

<span data-ttu-id="34b16-114">ステータス コード エラーの応答ページのテンプレートの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34b16-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34b16-115">**テンプレート** に移動する。</span><span class="sxs-lookup"><span data-stu-id="34b16-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="34b16-116">**新規** を選択して、ページのテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="34b16-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="34b16-117">**テンプレート名** 配下の **新規テンプレート** ダイアログ ボックスに、新規テンプレートの名称を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34b16-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="34b16-118">ステータス コード エラーの応答ページに含める構造に基づいて、テンプレートを構築します。</span><span class="sxs-lookup"><span data-stu-id="34b16-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="34b16-119">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="34b16-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="34b16-120">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="34b16-120">Build the status code error response page</span></span>

<span data-ttu-id="34b16-121">ステータス コード エラーの応答ページを構築するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34b16-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34b16-122">**ページ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="34b16-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="34b16-123">**新規** を選択して、ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="34b16-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="34b16-124">**テンプレートの選択** ダイアログボックスでテンプレートを選択し、**ページ名** に、[ステータスコードのエラー応答] ページの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="34b16-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="34b16-125">**ページの URL** フィールドは空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="34b16-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="34b16-126">ページを構築します。</span><span class="sxs-lookup"><span data-stu-id="34b16-126">Build the page.</span></span>
1. <span data-ttu-id="34b16-127">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="34b16-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="34b16-128">4xx および 5xx ステータス コード エラー用に個別のステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34b16-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="34b16-129">または、両方のエラー カテゴリに同じ一般的なステータス コード エラーの応答ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="34b16-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="34b16-130">ステータス コード エラーの応答ページのリダイレクトを設定する</span><span class="sxs-lookup"><span data-stu-id="34b16-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="34b16-131">ステータス コード エラーの応答ページのリダイレクトを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34b16-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34b16-132">**URL \> 新規 \> 新しいエイリアス** に移動して、構築したステータス コード エラーの応答ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="34b16-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="34b16-133">**エイリアス** フィールドに、リダイレクトを設定するステータス コード エラーの応答ページに応じて、**default-4xx** または **default-5xx** のいずれかを入力します。</span><span class="sxs-lookup"><span data-stu-id="34b16-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="34b16-134">これらのエイリアスは公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34b16-134">These aliases must be published.</span></span> <span data-ttu-id="34b16-135">そうしない場合、リダイレクトは機能しません。</span><span class="sxs-lookup"><span data-stu-id="34b16-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="34b16-136">**OK** を選択してリンクをコミットします。</span><span class="sxs-lookup"><span data-stu-id="34b16-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="34b16-137">両方のエラー カテゴリに対して単一のステータス コード エラー の応答ページを使用している場合は、この手順を繰り返して、もう一方のエラー カテゴリのエイリアスを同じページにリンクします。</span><span class="sxs-lookup"><span data-stu-id="34b16-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34b16-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="34b16-138">Additional resources</span></span>

[<span data-ttu-id="34b16-139">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="34b16-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="34b16-140">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="34b16-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="34b16-141">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="34b16-141">Create a page URL</span></span>](create-page-url.md)
