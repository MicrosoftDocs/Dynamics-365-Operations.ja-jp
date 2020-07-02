---
title: Cookie のコンプライアンス
description: このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446916"
---
# <a name="cookie-compliance"></a><span data-ttu-id="31501-103">Cookie のコンプライアンス</span><span class="sxs-lookup"><span data-stu-id="31501-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="31501-104">このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="31501-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31501-105">概要</span><span class="sxs-lookup"><span data-stu-id="31501-105">Overview</span></span>

<span data-ttu-id="31501-106">eコマースの顧客に影響を与える追跡技術が使用される場合は、プライバシーが重要な要素になります。</span><span class="sxs-lookup"><span data-stu-id="31501-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="31501-107">欧州連合 (EU) の一般データ保護規則 (GDPR) などのプライバシー コンプライアンス基準により、現在有効な任意のサイトでは電子プライバシー ガイドラインを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31501-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="31501-108">多くの E コマース サイトは既定でグローバルにアクセスできるため、E コマース サイトのコンプライアンス基準を確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="31501-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="31501-109">Microsoft が Cookie のコンプライアンスに使用する基本原則の詳細については、[Microsoft Trust Center](https://www.microsoft.com/trust-center) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31501-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="31501-110">そのサイトでは、コンプライアンスおよびプライバシーの領域に関する詳細情報も取得できます。</span><span class="sxs-lookup"><span data-stu-id="31501-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="31501-111">次の表に、Dynamics 365 Commerce サイトによって配置された Cookie の現在の参照一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="31501-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="31501-112">Cookie 名</span><span class="sxs-lookup"><span data-stu-id="31501-112">Cookie name</span></span>                               | <span data-ttu-id="31501-113">使用状況</span><span class="sxs-lookup"><span data-stu-id="31501-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="31501-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="31501-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="31501-115">シングルサインオン (SSO) 用の Microsoft Azure Active Directory (Azure AD) の認証 Cookie を保存します。</span><span class="sxs-lookup"><span data-stu-id="31501-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="31501-116">暗号化されたユーザー プリンシパル情報 (名前、姓、メール) を保存します。</span><span class="sxs-lookup"><span data-stu-id="31501-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="31501-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="31501-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="31501-118">カート インスタンスに追加された製品の一覧を取得するために使用される店舗カート ID。</span><span class="sxs-lookup"><span data-stu-id="31501-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="31501-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="31501-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="31501-120">Cookie 準拠の承認追跡。</span><span class="sxs-lookup"><span data-stu-id="31501-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="31501-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="31501-121">ai_session</span></span>                                  | <span data-ttu-id="31501-122">アプリの特定のページと機能を含むユーザー アクティビティのセッション数が検出されます。</span><span class="sxs-lookup"><span data-stu-id="31501-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="31501-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="31501-123">ai_user</span></span>                                     | <span data-ttu-id="31501-124">アプリとその機能を使用した人の数が検出されます。</span><span class="sxs-lookup"><span data-stu-id="31501-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="31501-125">ユーザーは匿名 ID を使用してカウントされます。</span><span class="sxs-lookup"><span data-stu-id="31501-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="31501-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="31501-126">b2cru</span></span>                                       | <span data-ttu-id="31501-127">リダイレクト URL を動的に格納します。</span><span class="sxs-lookup"><span data-stu-id="31501-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="31501-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="31501-128">JSESSIONID</span></span>                                  | <span data-ttu-id="31501-129">ユーザー セッションを保存するために支払コネクタ Adyen によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="31501-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="31501-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="31501-131">認証</span><span class="sxs-lookup"><span data-stu-id="31501-131">Authentication</span></span>                                               |
| <span data-ttu-id="31501-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="31501-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="31501-133">要求の状態を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="31501-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="31501-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="31501-135">CRSF から保護するためにクロスサイト リクエスト フォージェリ (CRSF) トークンが使用されています。</span><span class="sxs-lookup"><span data-stu-id="31501-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="31501-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="31501-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="31501-137">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31501-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="31501-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="31501-139">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31501-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="31501-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="31501-141">適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="31501-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="31501-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="31501-143">SSO セッションを維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31501-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="31501-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="31501-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="31501-145">現在のトランザクションなど、トランザクションを追跡するために使用されます (企業からコンシューマー (B2C) サイトに対して認証されている開いたタブの数)。</span><span class="sxs-lookup"><span data-stu-id="31501-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="31501-146">追加リソース</span><span class="sxs-lookup"><span data-stu-id="31501-146">Additional resources</span></span>

[<span data-ttu-id="31501-147">ユーザー補助機能</span><span class="sxs-lookup"><span data-stu-id="31501-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="31501-148">コンプライアンスの概要</span><span class="sxs-lookup"><span data-stu-id="31501-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="31501-149">プライバシー ポリシー ページの追加</span><span class="sxs-lookup"><span data-stu-id="31501-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="31501-150">追跡しているコンテンツの変更に関連付けられたユーザー ID の置換</span><span class="sxs-lookup"><span data-stu-id="31501-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
