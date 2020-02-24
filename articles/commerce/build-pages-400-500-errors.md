---
title: 4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001137"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="2c3f9-103">4xx/5xx ステータス コード エラーに対するカスタム応答ページの作成</span><span class="sxs-lookup"><span data-stu-id="2c3f9-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2c3f9-104">このトピックでは、Microsoft Dynamics 365 Commerce の作成ツールを使用して、4xx と 5xx のステータス コード エラーに対するカスタム応答ページを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2c3f9-105">概要</span><span class="sxs-lookup"><span data-stu-id="2c3f9-105">Overview</span></span>

<span data-ttu-id="2c3f9-106">要求が成功しなかった場合、サーバーは HTTP ステータス コード エラーの応答を発行します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="2c3f9-107">ページが見つからない場合は、404 ステータス コードがキャプチャされて返され、サーバー エラーが発生した場合は 500 ステータス コードがキャプチャされて返されます。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="2c3f9-108">Dynamics 365 Commerce では、アプリケーション ユーザーは、これらのステータス コード エラーの応答について、ユーザーに対して表示されるカスタム ステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="2c3f9-109">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="2c3f9-109">Build a status code error response page</span></span>

<span data-ttu-id="2c3f9-110">ステータス コード エラーの応答ページの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="2c3f9-111">優先的に使用する Web ブラウザーで、Dynamics 365 Commerce にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="2c3f9-112">4xx/5xx ステータス コード エラーの応答ページを構築するサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="2c3f9-113">テンプレートの構築</span><span class="sxs-lookup"><span data-stu-id="2c3f9-113">Build the template</span></span>

<span data-ttu-id="2c3f9-114">ステータス コード エラーの応答ページのテンプレートの構築を開始するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="2c3f9-115">**テンプレート \> 新しいテンプレート**に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="2c3f9-116">新しいテンプレートに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-116">Name the new template.</span></span>
1. <span data-ttu-id="2c3f9-117">ステータス コード エラーの応答ページに含める構造に基づいて、テンプレートを構築します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="2c3f9-118">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="2c3f9-119">ステータス コード エラーの応答ページの構築</span><span class="sxs-lookup"><span data-stu-id="2c3f9-119">Build the status code error response page</span></span>

<span data-ttu-id="2c3f9-120">ステータス コード エラーの応答ページを構築するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="2c3f9-121">**ページ \> 新しいページ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="2c3f9-122">ステータス コード エラーの応答ページに名前を付けますが、**URL** フィールドは設定**しない**でください。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="2c3f9-123">ページを構築します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-123">Build the page.</span></span>
1. <span data-ttu-id="2c3f9-124">ページをチェックインして、公開します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="2c3f9-125">4xx および 5xx ステータス コード エラー用に個別のステータス コード エラーの応答ページを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="2c3f9-126">または、両方のエラー カテゴリに同じ一般的なステータス コード エラーの応答ページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="2c3f9-127">ステータス コード エラーの応答ページのリダイレクトを設定する</span><span class="sxs-lookup"><span data-stu-id="2c3f9-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="2c3f9-128">ステータス コード エラーの応答ページのリダイレクトを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="2c3f9-129">**URL \> 新規 \> 新しいエイリアス**に移動して、構築したステータス コード エラーの応答ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="2c3f9-130">**エイリアス** フィールドに、リダイレクトを設定するステータス コード エラーの応答ページに応じて、**default-4xx** または **default-5xx** のいずれかを入力します。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="2c3f9-131">これらのエイリアスは公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-131">These aliases must be published.</span></span> <span data-ttu-id="2c3f9-132">そうしない場合、リダイレクトは機能しません。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="2c3f9-133">**OK** を選択してリンクをコミットします。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="2c3f9-134">両方のエラー カテゴリに対して単一のステータス コード エラー の応答ページを使用している場合は、この手順を繰り返して、もう一方のエラー カテゴリのエイリアスを同じページにリンクします。</span><span class="sxs-lookup"><span data-stu-id="2c3f9-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c3f9-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2c3f9-135">Additional resources</span></span>

[<span data-ttu-id="2c3f9-136">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="2c3f9-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="2c3f9-137">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="2c3f9-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2c3f9-138">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="2c3f9-138">Create a page URL</span></span>](create-page-url.md)
