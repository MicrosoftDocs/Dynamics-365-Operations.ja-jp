---
title: Cookie の同意モジュール
description: このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 842096c6e3045e434aced9642c86690e2ff7483a
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761405"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="8aea7-103">Cookie の同意モジュール</span><span class="sxs-lookup"><span data-stu-id="8aea7-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8aea7-104">このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8aea7-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8aea7-105">概要</span><span class="sxs-lookup"><span data-stu-id="8aea7-105">Overview</span></span>

<span data-ttu-id="8aea7-106">Cookie の同意モジュールは、ブラウザのクッキーを追跡する機能やモジュールに対し、サイトの利用者に向けて明示的にクッキーの同意を促すものです。</span><span class="sxs-lookup"><span data-stu-id="8aea7-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="8aea7-107">サイトの利用者が新しいブラウザ セッションでサイトを初めて閲覧する際には、この同意が必要となります。</span><span class="sxs-lookup"><span data-stu-id="8aea7-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="8aea7-108">同意が得られて場合は、追跡されるため、サイトの利用者は再び同意を求められることはありません。</span><span class="sxs-lookup"><span data-stu-id="8aea7-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="8aea7-109">詳細については、[Cookie に関するコンプライアンス](cookie-compliance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8aea7-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="8aea7-110">サイト利用者のクッキーの同意が得られない場合、クッキーの同意が必要となる機能やモジュールはページ上に表示されません。</span><span class="sxs-lookup"><span data-stu-id="8aea7-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="8aea7-111">たとえば、精算モジュール、ソーシャル共有モジュール、優先保管機能にはすべて、cookie の同意が必要となり、サイト利用者の同意が得られれない場合は表示されません。</span><span class="sxs-lookup"><span data-stu-id="8aea7-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="8aea7-112">Cookie の同意モジュールは、ページの読み込み時に適用できるよう、ページのヘッダー フラグメントに構成可能です。</span><span class="sxs-lookup"><span data-stu-id="8aea7-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="8aea7-113">cookie 同意モジュールは、サイト上での cookie の使用についてサイト利用者に通知する明示的ななメッセージを含み、かつサイトのプライバシー ページへのリンクを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8aea7-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="8aea7-114">以下の図は、サイト ページのヘッダーに表示される、サイトの [プライバシーポリシー] ページへのリンクを含む cookie 同意メッセージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8aea7-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="8aea7-115">![Cookie 同意モジュールの例](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="8aea7-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="8aea7-116">Cookie 同意モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="8aea7-116">Cookie consent module properties</span></span>

| <span data-ttu-id="8aea7-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="8aea7-117">Property name</span></span>             | <span data-ttu-id="8aea7-118">先頭値</span><span class="sxs-lookup"><span data-stu-id="8aea7-118">Value</span></span>                 | <span data-ttu-id="8aea7-119">説明</span><span class="sxs-lookup"><span data-stu-id="8aea7-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8aea7-120">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="8aea7-120">Rich Text</span></span>                  | <span data-ttu-id="8aea7-121">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="8aea7-121">Rich Text</span></span> | <span data-ttu-id="8aea7-122">サイトがブラウザの Cookie を使用していること、およびサイトが完全に機能するためには Cookie の使用に同意する必要があることをサイト利用者に通知するリッチテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="8aea7-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="8aea7-123">リンク</span><span class="sxs-lookup"><span data-stu-id="8aea7-123">Links</span></span> | <span data-ttu-id="8aea7-124">URL</span><span class="sxs-lookup"><span data-stu-id="8aea7-124">URL</span></span> | <span data-ttu-id="8aea7-125">サイトで追跡されている cookie の種類を説明するサイトのプライバシー ページに、1つ以上のリンクを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8aea7-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="8aea7-126">サイト ページへの cookie 同意モジュールを追加する</span><span class="sxs-lookup"><span data-stu-id="8aea7-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="8aea7-127">Cookie 同意モジュールを複数のサイト ページに効率的に追加するには、共有ページ ヘッダーのフラグメントに追加します。</span><span class="sxs-lookup"><span data-stu-id="8aea7-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="8aea7-128">ヘッダー フラグメントをすべてのサイトのページに追加すると、サイトの利用者がサイトのページに最初に移動した際に、cookie の同意を通知するメッセージが自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8aea7-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="8aea7-129">ヘッダーのフラグメントとモジュールの詳細については、[ヘッダー モジュール](author-header-module.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="8aea7-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8aea7-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8aea7-130">Additional resources</span></span>

[<span data-ttu-id="8aea7-131">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="8aea7-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8aea7-132">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="8aea7-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="8aea7-133">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="8aea7-133">Cookie compliance</span></span>](cookie-compliance.md)
