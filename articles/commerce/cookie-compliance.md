---
title: Cookie のコンプライアンス
description: このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796030"
---
# <a name="cookie-compliance"></a><span data-ttu-id="30e17-103">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="30e17-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30e17-104">このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="30e17-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="30e17-105">eコマースの顧客に影響を与える追跡技術が使用される場合は、プライバシーが重要な要素になります。</span><span class="sxs-lookup"><span data-stu-id="30e17-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="30e17-106">欧州連合 (EU) の一般データ保護規則 (GDPR) などのプライバシー コンプライアンス基準により、現在有効な任意のサイトでは電子プライバシー ガイドラインを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30e17-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="30e17-107">多くの E コマース サイトは既定でグローバルにアクセスできるため、E コマース サイトのコンプライアンス基準を確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="30e17-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="30e17-108">Microsoft が Cookie のコンプライアンスに使用する基本原則の詳細については、[Microsoft Trust Center](https://www.microsoft.com/trust-center) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30e17-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="30e17-109">そのサイトでは、コンプライアンスおよびプライバシーの領域に関する詳細情報も取得できます。</span><span class="sxs-lookup"><span data-stu-id="30e17-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="30e17-110">次の表に、Dynamics 365 Commerce サイトによって配置された Cookie の現在の参照一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="30e17-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="30e17-111">Cookie 名</span><span class="sxs-lookup"><span data-stu-id="30e17-111">Cookie name</span></span>                               | <span data-ttu-id="30e17-112">使用状況</span><span class="sxs-lookup"><span data-stu-id="30e17-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="30e17-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="30e17-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="30e17-114">シングルサインオン (SSO) 用の Microsoft Azure Active Directory (Azure AD) の認証 Cookie を保存します。</span><span class="sxs-lookup"><span data-stu-id="30e17-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="30e17-115">暗号化されたユーザー プリンシパル情報 (名前、姓、メール) を保存します。</span><span class="sxs-lookup"><span data-stu-id="30e17-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="30e17-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="30e17-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="30e17-117">カート インスタンスに追加された製品の一覧を取得するために使用される店舗カート ID。</span><span class="sxs-lookup"><span data-stu-id="30e17-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="30e17-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="30e17-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="30e17-119">Cookie 準拠の承認追跡。</span><span class="sxs-lookup"><span data-stu-id="30e17-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="30e17-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="30e17-120">ai_session</span></span>                                  | <span data-ttu-id="30e17-121">アプリの特定のページと機能を含むユーザー アクティビティのセッション数が検出されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="30e17-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="30e17-122">ai_user</span></span>                                     | <span data-ttu-id="30e17-123">アプリとその機能を使用した人の数が検出されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="30e17-124">ユーザーは匿名 ID を使用してカウントされます。</span><span class="sxs-lookup"><span data-stu-id="30e17-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="30e17-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="30e17-125">b2cru</span></span>                                       | <span data-ttu-id="30e17-126">リダイレクト URL を動的に格納します。</span><span class="sxs-lookup"><span data-stu-id="30e17-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="30e17-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="30e17-127">JSESSIONID</span></span>                                  | <span data-ttu-id="30e17-128">ユーザー セッションを保存するために支払コネクタ Adyen によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="30e17-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="30e17-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="30e17-130">認証</span><span class="sxs-lookup"><span data-stu-id="30e17-130">Authentication</span></span>                                               |
| <span data-ttu-id="30e17-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="30e17-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="30e17-132">要求の状態を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="30e17-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="30e17-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="30e17-134">CRSF から保護するためにクロスサイト リクエスト フォージェリ (CRSF) トークンが使用されています。</span><span class="sxs-lookup"><span data-stu-id="30e17-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="30e17-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="30e17-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="30e17-136">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="30e17-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="30e17-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="30e17-138">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="30e17-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="30e17-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="30e17-140">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="30e17-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="30e17-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="30e17-142">SSO セッションを維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30e17-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="30e17-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="30e17-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="30e17-144">現在のトランザクションなど、トランザクションを追跡するために使用されます (企業からコンシューマー (B2C) サイトに対して認証されている開いたタブの数)。</span><span class="sxs-lookup"><span data-stu-id="30e17-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="30e17-145">電子商取引サイトにおけるサイト利用者向け cookie の同意</span><span class="sxs-lookup"><span data-stu-id="30e17-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="30e17-146">電子商取引サイトの機能、またはモジュールが必須ではない Cookie を使用している場合は、サイト利用者の同意を取得してから、cookie を追跡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30e17-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="30e17-147">サイト利用者が電子商取引サイトで cookie の同意を得られるようにするには、サイトの作成者が、ページのヘッダーモジュールに cookie の同意モジュールを追加および構成して、cookie の同意を要求し、同意を得られたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30e17-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="30e17-148">イト利用者の同意は、非必須の cookie を使用した機能、またはモジュールがサイトのページに表示される前に得なければなりません。</span><span class="sxs-lookup"><span data-stu-id="30e17-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30e17-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="30e17-149">Additional resources</span></span>

[<span data-ttu-id="30e17-150">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="30e17-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="30e17-151">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="30e17-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="30e17-152">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="30e17-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="30e17-153">追跡しているコンテンツの変更に関連付いたユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="30e17-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="30e17-154">Cookie の同意モジュール</span><span class="sxs-lookup"><span data-stu-id="30e17-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="30e17-155">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="30e17-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
