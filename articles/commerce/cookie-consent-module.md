---
title: Cookie の同意モジュール
description: このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
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
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796006"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="5c0e1-103">Cookie の同意モジュール</span><span class="sxs-lookup"><span data-stu-id="5c0e1-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c0e1-104">このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5c0e1-105">Cookie の同意モジュールは、ブラウザのクッキーを追跡する機能やモジュールに対し、サイトの利用者に向けて明示的にクッキーの同意を促すものです。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="5c0e1-106">サイトの利用者が新しいブラウザ セッションでサイトを初めて閲覧する際には、この同意が必要となります。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="5c0e1-107">同意が得られて場合は、追跡されるため、サイトの利用者は再び同意を求められることはありません。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="5c0e1-108">詳細については、[Cookie に関するコンプライアンス](cookie-compliance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="5c0e1-109">サイト利用者のクッキーの同意が得られない場合、クッキーの同意が必要となる機能やモジュールはページ上に表示されません。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="5c0e1-110">たとえば、精算モジュール、ソーシャル共有モジュール、優先保管機能にはすべて、cookie の同意が必要となり、サイト利用者の同意が得られれない場合は表示されません。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="5c0e1-111">Cookie の同意モジュールは、ページの読み込み時に適用できるよう、ページのヘッダー フラグメントに構成可能です。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="5c0e1-112">cookie 同意モジュールは、サイト上での cookie の使用についてサイト利用者に通知する明示的ななメッセージを含み、かつサイトのプライバシー ページへのリンクを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="5c0e1-113">以下の図は、サイト ページのヘッダーに表示される、サイトの [プライバシーポリシー] ページへのリンクを含む cookie 同意メッセージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="5c0e1-114">![Cookie 同意モジュールの例](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="5c0e1-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="5c0e1-115">Cookie 同意モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="5c0e1-115">Cookie consent module properties</span></span>

| <span data-ttu-id="5c0e1-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5c0e1-116">Property name</span></span>             | <span data-ttu-id="5c0e1-117">先頭値</span><span class="sxs-lookup"><span data-stu-id="5c0e1-117">Value</span></span>                 | <span data-ttu-id="5c0e1-118">説明</span><span class="sxs-lookup"><span data-stu-id="5c0e1-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5c0e1-119">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="5c0e1-119">Rich Text</span></span>                  | <span data-ttu-id="5c0e1-120">リッチ テキスト</span><span class="sxs-lookup"><span data-stu-id="5c0e1-120">Rich Text</span></span> | <span data-ttu-id="5c0e1-121">サイトがブラウザの Cookie を使用していること、およびサイトが完全に機能するためには Cookie の使用に同意する必要があることをサイト利用者に通知するリッチテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="5c0e1-122">リンク</span><span class="sxs-lookup"><span data-stu-id="5c0e1-122">Links</span></span> | <span data-ttu-id="5c0e1-123">URL</span><span class="sxs-lookup"><span data-stu-id="5c0e1-123">URL</span></span> | <span data-ttu-id="5c0e1-124">サイトで追跡されている cookie の種類を説明するサイトのプライバシー ページに、1つ以上のリンクを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="5c0e1-125">サイト ページへの cookie 同意モジュールを追加する</span><span class="sxs-lookup"><span data-stu-id="5c0e1-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="5c0e1-126">Cookie 同意モジュールを複数のサイト ページに効率的に追加するには、共有ページ ヘッダーのフラグメントに追加します。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="5c0e1-127">ヘッダー フラグメントをすべてのサイトのページに追加すると、サイトの利用者がサイトのページに最初に移動した際に、cookie の同意を通知するメッセージが自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="5c0e1-128">ヘッダーのフラグメントとモジュールの詳細については、[ヘッダー モジュール](author-header-module.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="5c0e1-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c0e1-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5c0e1-129">Additional resources</span></span>

[<span data-ttu-id="5c0e1-130">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="5c0e1-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5c0e1-131">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="5c0e1-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="5c0e1-132">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="5c0e1-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]