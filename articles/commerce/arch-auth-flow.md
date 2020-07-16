---
title: Dynamics 365 Commerce 認証フロー
description: このトピックでは、Microsoft Dynamics 365 Commerce のさまざまな認証フローの概要を示します。
author: samjarawan
manager: AnnBe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: samjar
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 37329d3a32cc29963a8e5e6507728f5c51629b62
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527730"
---
# <a name="dynamics-365-commerce-authentication-flows"></a><span data-ttu-id="7200a-103">Dynamics 365 Commerce 認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-103">Dynamics 365 Commerce authentication flows</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7200a-104">このトピックでは、Microsoft Dynamics 365 Commerce のさまざまな認証フローの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="7200a-104">This topic provides an overview of the various authentication flows in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="7200a-105">Dynamics 365 Commerce ソリューションは現在、複数の認証シナリオとフローをサポートしていますが、Commerce Scale Unit (ヘッドレス コマース エンジンとも呼ばれる) のコア認証インフラストラクチャは、完全に [OpenID connect](https://openid.net/connect/) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="7200a-105">Although the Dynamics 365 Commerce solution currently supports several authentication scenarios and flows, the core authentication infrastructure of the Commerce Scale Unit (also known as the headless commerce engine) is fully based on [OpenID Connect](https://openid.net/connect/).</span></span>

## <a name="authentication-methods"></a><span data-ttu-id="7200a-106">認証方法</span><span class="sxs-lookup"><span data-stu-id="7200a-106">Authentication methods</span></span>

<span data-ttu-id="7200a-107">Commerce Scale Unit の各アプリケーション プログラミング インターフェイス (API) へのアクセスは、次の 1 つ以上の役割によってネイティブに制限されます。</span><span class="sxs-lookup"><span data-stu-id="7200a-107">Access to each of the application programming interfaces (APIs) on the Commerce Scale Unit is natively restricted by one or more of the following roles:</span></span>

- <span data-ttu-id="7200a-108">**従業員** – このロールに関連付けられている API にアクセスするには、販売時点管理 (POS) デバイスの有効化 (デバイス トークン) と認証済従業員が必要です。</span><span class="sxs-lookup"><span data-stu-id="7200a-108">**Employee** – Access to APIs associated with this role requires point of sale (POS) device activation (a device token) and an authenticated employee.</span></span>
- <span data-ttu-id="7200a-109">**顧客** – このロールに関連付けられている API へのアクセスには、認証済顧客が必要です。</span><span class="sxs-lookup"><span data-stu-id="7200a-109">**Customer** – Access to APIs associated with this role requires an authenticated customer.</span></span> <span data-ttu-id="7200a-110">通常、E コマース サイトでは、これらの API を使用して、注文履歴の取得や顧客の詳細の変更などの操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7200a-110">E-Commerce sites generally use these APIs for operations such as retrieving order history and changing customer details.</span></span>
- <span data-ttu-id="7200a-111">**アプリケーション** – このロールに関連付けられている API にアクセスするには、Azure Active Directory (Azure AD) サービスとサービス間認証などのアプリケーション レベルの認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="7200a-111">**Application** – Access to APIs associated with this role requires application-level authentication, such as Azure Active Directory (Azure AD) service-to-service authentication.</span></span>
- <span data-ttu-id="7200a-112">**匿名** – このロールに関連付けられている API は、主にユーザー認証を行わずに E コマース サイトによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="7200a-112">**Anonymous** – APIs associated with this role are primarily used by e-Commerce sites without user authentication.</span></span>
- <span data-ttu-id="7200a-113">**カスタムされた API** – このロールに関連付けられている API へのアクセスを制限するには、POS デバイスの有効化、顧客認証、匿名認証などの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="7200a-113">**Customized APIs** – Access to APIs associated with this role can be restricted using any of the methods described above such as POS device activation, customer authentication, and anonymous authentication.</span></span>

<span data-ttu-id="7200a-114">Commerce Scale Unit API とそのアクセス制限の完全な一覧については、[Commerce Scale Unit 顧客およびコンシューマー API](/dev-itpro/retail-server-customer-consumer-api.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7200a-114">For the full list of Commerce Scale Unit APIs and their access restrictions, see [Commerce Scale Unit customer and consumer APIs](/dev-itpro/retail-server-customer-consumer-api.md).</span></span>

### <a name="supported-authentication-methods"></a><span data-ttu-id="7200a-115">サポートされている認証方法</span><span class="sxs-lookup"><span data-stu-id="7200a-115">Supported authentication methods</span></span>

<span data-ttu-id="7200a-116">次の表では、デバイス トークンを生成する POS デバイスの有効化、またはユーザー トークンを生成するユーザー認証のいずれかを必要とする API に対して、サポートされている認証方法のセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7200a-116">The following table describes the set of supported authentication methods for APIs that require either POS device activation that generates a device token or user authentication that generates a user token.</span></span>

| <span data-ttu-id="7200a-117">API カテゴリ</span><span class="sxs-lookup"><span data-stu-id="7200a-117">API category</span></span> | <span data-ttu-id="7200a-118">シナリオ</span><span class="sxs-lookup"><span data-stu-id="7200a-118">Scenario</span></span> | <span data-ttu-id="7200a-119">サポートされている認証方法</span><span class="sxs-lookup"><span data-stu-id="7200a-119">Supported authentication method</span></span> | <span data-ttu-id="7200a-120">必要な設定</span><span class="sxs-lookup"><span data-stu-id="7200a-120">Required setup</span></span> | <span data-ttu-id="7200a-121">追加の詳細</span><span class="sxs-lookup"><span data-stu-id="7200a-121">Additional details</span></span> |
|----------|-----------|------------|------------|------------|
| <span data-ttu-id="7200a-122">従業員</span><span class="sxs-lookup"><span data-stu-id="7200a-122">Employee</span></span> | <span data-ttu-id="7200a-123">Dynamics 365 POS 認証フロー\*</span><span class="sxs-lookup"><span data-stu-id="7200a-123">Dynamics 365 POS authentication flows\*</span></span> | <span data-ttu-id="7200a-124">単純レジ担当者のユーザー名とパスワード</span><span class="sxs-lookup"><span data-stu-id="7200a-124">Simple cashier user name and password</span></span> | <span data-ttu-id="7200a-125">Dynamics 365 Commerce 本社で、作業者のユーザー名とパスワードをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-125">In Dynamics 365 Commerce headquarters, configure a user name and password for a worker.</span></span> | [<span data-ttu-id="7200a-126">作業者を作成</span><span class="sxs-lookup"><span data-stu-id="7200a-126">Create a worker</span></span>](retail-modern-pos-device-activation.md#create-a-worker) |
| <span data-ttu-id="7200a-127">従業員</span><span class="sxs-lookup"><span data-stu-id="7200a-127">Employee</span></span> | <span data-ttu-id="7200a-128">Dynamics 365 POS 認証フロー\*</span><span class="sxs-lookup"><span data-stu-id="7200a-128">Dynamics 365 POS authentication flows\*</span></span> | <span data-ttu-id="7200a-129">Azure AD 資格情報</span><span class="sxs-lookup"><span data-stu-id="7200a-129">Azure AD credentials</span></span> | <span data-ttu-id="7200a-130">Commerce 本社で、Azure AD の資格情報にマップされる作業者をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-130">In Commerce headquarters, configure a worker that is mapped to Azure AD credentials.</span></span> | [<span data-ttu-id="7200a-131">POS サインインの Azure Active Directory 認証を有効にする</span><span class="sxs-lookup"><span data-stu-id="7200a-131">Enable Azure Active Directory authentication for POS sign-in</span></span>](aad-pos-logon.md) |
| <span data-ttu-id="7200a-132">従業員</span><span class="sxs-lookup"><span data-stu-id="7200a-132">Employee</span></span> | <span data-ttu-id="7200a-133">Dynamics 365 POS 認証フロー\*</span><span class="sxs-lookup"><span data-stu-id="7200a-133">Dynamics 365 POS authentication flows\*</span></span> | <span data-ttu-id="7200a-134">拡張サインイン資格情報 (たとえば、バーコードまたは磁気ストライプリーダー \[MSR\] を使用)</span><span class="sxs-lookup"><span data-stu-id="7200a-134">Extended sign-in credentials (for example, by using a bar code or a magnetic stripe reader \[MSR\])</span></span> | <span data-ttu-id="7200a-135">Commerce 本社で、拡張サインインの作業者をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-135">In Commerce headquarters, configure a worker for extended sign-in.</span></span> | [<span data-ttu-id="7200a-136">MPOS および Cloud POS の拡張ログオン機能の設定</span><span class="sxs-lookup"><span data-stu-id="7200a-136">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md) |
| <span data-ttu-id="7200a-137">顧客</span><span class="sxs-lookup"><span data-stu-id="7200a-137">Customer</span></span> | <span data-ttu-id="7200a-138">Dynamics 365 Commerce 認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-138">Dynamics 365 Commerce authentication flows</span></span> | <span data-ttu-id="7200a-139">Azure AD B2C を使用したサイトユーザー認証</span><span class="sxs-lookup"><span data-stu-id="7200a-139">Site user authentication by using Azure AD B2C</span></span> | <ol><li><span data-ttu-id="7200a-140">Azure AD 企業と顧客間 (B2C) アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="7200a-140">Create an Azure AD business-to-consumer (B2C) application.</span></span></li><li><span data-ttu-id="7200a-141">Commerce 本社で、Azure AD B2C アプリケーションを、ID プロバイダーの承認済みリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="7200a-141">In Commerce headquarters, add the Azure AD B2C application to the accepted list of identity providers.</span></span></li><li><span data-ttu-id="7200a-142">Commerce サイト ビルダー で Azure AD B2C アプリケーションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-142">In Commerce site builder, configure the Azure AD B2C application.</span></span></li></ol> | [<span data-ttu-id="7200a-143">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-143">Set up a B2C tenant in Commerce</span></span>](set-up-b2c-tenant.md)<p>[<span data-ttu-id="7200a-144">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-144">Set up custom pages for user sign-ins</span></span>](custom-pages-user-logins.md)</p> |
| <span data-ttu-id="7200a-145">顧客</span><span class="sxs-lookup"><span data-stu-id="7200a-145">Customer</span></span> | <span data-ttu-id="7200a-146">Dynamics 365 Commerce 認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-146">Dynamics 365 Commerce authentication flows</span></span> | <span data-ttu-id="7200a-147">OpenID Connect をサポートする外部 ID プロバイダーを使用したサイト ユーザー認証</span><span class="sxs-lookup"><span data-stu-id="7200a-147">Site user authentication by using an external identity provider that supports OpenID Connect</span></span> | <ol><li><span data-ttu-id="7200a-148">Azure AD B2C アプリケーションを作成し、外部 ID プロバイダーをサポートするようにコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-148">Create an Azure AD B2C application, and configure it to support external identity providers.</span></span></li><li><span data-ttu-id="7200a-149">Commerce 本社で、Azure AD B2C アプリケーションを、ID プロバイダーの承認済みリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="7200a-149">In Commerce headquarters, add the Azure AD B2C application to the accepted list of identity providers.</span></span></li><li><span data-ttu-id="7200a-150">Commerce サイト ビルダー で Azure AD B2C アプリケーションをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7200a-150">In Commerce site builder, configure the Azure AD B2C application.</span></span></li></ol> | [<span data-ttu-id="7200a-151">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-151">Set up a B2C tenant in Commerce</span></span>](set-up-b2c-tenant.md)<p>[<span data-ttu-id="7200a-152">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-152">Set up custom pages for user sign-ins</span></span>](custom-pages-user-logins.md)</p> |
| <span data-ttu-id="7200a-153">顧客</span><span class="sxs-lookup"><span data-stu-id="7200a-153">Customer</span></span> | <span data-ttu-id="7200a-154">サード パーティ E コマースの認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-154">Third-party e-Commerce authentication flows</span></span> | <span data-ttu-id="7200a-155">OpenID Connect をサポートする外部 ID プロバイダーを使用したサイト ユーザー認証</span><span class="sxs-lookup"><span data-stu-id="7200a-155">Site user authentication by using an external identity provider that supports OpenID Connect</span></span> | <span data-ttu-id="7200a-156">Commerce 本社で、外部 ID プロバイダーを ID プロバイダーの承認済みリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="7200a-156">In Commerce headquarters, add the external identity provider to the accepted list of identity providers.</span></span> | [<span data-ttu-id="7200a-157">認証プロバイダーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7200a-157">Configure authentication providers</span></span>](/dev-itpro/configure-authentication-providers.md) |
| <span data-ttu-id="7200a-158">応募</span><span class="sxs-lookup"><span data-stu-id="7200a-158">Application</span></span> | <span data-ttu-id="7200a-159">サード パーティ アプリまたはサービスの認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-159">Third-party app or service authentication flows</span></span> | <span data-ttu-id="7200a-160">Azure AD サービス間認証/アプリケーション認証</span><span class="sxs-lookup"><span data-stu-id="7200a-160">Azure AD service-to-service authentication/application authentication</span></span> | <span data-ttu-id="7200a-161">Commerce 本社で、外部 ID プロバイダーを ID プロバイダーの承認済みリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="7200a-161">In Commerce headquarters, add the external identity provider to the accepted list of identity providers.</span></span> | |

<span data-ttu-id="7200a-162">\* POS にサインインするには、デバイスごとにライセンス認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="7200a-162">\* Sign-in to POS requires device activation for each terminal.</span></span> <span data-ttu-id="7200a-163">詳細については、[販売時点管理 (POS) デバイスのライセンス認証](/dev-itpro/retail-device-activation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7200a-163">For more information, see [Point of Sale (POS) device activation](/dev-itpro/retail-device-activation.md).</span></span>

### <a name="unsupported-authentication-flows"></a><span data-ttu-id="7200a-164">サポートされていない認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-164">Unsupported authentication flows</span></span>

| <span data-ttu-id="7200a-165">シナリオ</span><span class="sxs-lookup"><span data-stu-id="7200a-165">Scenario</span></span> | <span data-ttu-id="7200a-166">サポートされていない認証方法</span><span class="sxs-lookup"><span data-stu-id="7200a-166">Unsupported authentication method</span></span> | <span data-ttu-id="7200a-167">詳細情報</span><span class="sxs-lookup"><span data-stu-id="7200a-167">Details</span></span> |
|----------|-----------|------------|
| <span data-ttu-id="7200a-168">Dynamics 365 POS 認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-168">Dynamics 365 POS authentication flows</span></span> | <span data-ttu-id="7200a-169">デバイスのライセンス認証を行わない (つまり、デバイストークンなし) 認証</span><span class="sxs-lookup"><span data-stu-id="7200a-169">Authentication without device activation (that is, without a device token)</span></span> | <span data-ttu-id="7200a-170">POS 関連の Commerce Scale Unit API では、認証のためのデバイス ライセンス認証トークンが必要です。</span><span class="sxs-lookup"><span data-stu-id="7200a-170">All POS-related Commerce Scale Unit APIs require a device activation token for authentication.</span></span> |

## <a name="dynamics-365-pos-employee-authentication-flows"></a><span data-ttu-id="7200a-171">Dynamics 365 POS 従業員認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-171">Dynamics 365 POS employee authentication flows</span></span>

<span data-ttu-id="7200a-172">次の図は、Commerce の POS 従業員認証フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="7200a-172">The following illustration shows POS employee authentication flows in Commerce.</span></span>

<span data-ttu-id="7200a-173"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-1.jpg" target="_blank">![Dynamics 365 POS 従業員認証フロー](./media/arch-auth-flow-1.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="7200a-173"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-1.jpg" target="_blank">![Dynamics 365 POS employee authentication flows](./media/arch-auth-flow-1.jpg)</a></span></span>

## <a name="dynamics-365-e-commerce-customer-authentication-flows"></a><span data-ttu-id="7200a-174">Dynamics 365 E コマース顧客認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-174">Dynamics 365 e-Commerce customer authentication flows</span></span>

<span data-ttu-id="7200a-175">次の図は、Commerce の E コマース フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="7200a-175">The following illustration shows e-Commerce customer authentication flows in Commerce.</span></span>

<span data-ttu-id="7200a-176"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-2.jpg" target="_blank">![Dynamics 365 E コマース顧客認証フロー](./media/arch-auth-flow-2.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="7200a-176"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-2.jpg" target="_blank">![Dynamics 365 e-Commerce customer authentication flows](./media/arch-auth-flow-2.jpg)</a></span></span>

## <a name="third-party-e-commerce-customer-authentication-flows"></a><span data-ttu-id="7200a-177">サード パーティ E コマースの顧客認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-177">Third-party e-Commerce customer authentication flows</span></span>

<span data-ttu-id="7200a-178">次の図は、Commerce のサード パーティ E コマースの顧客認証フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="7200a-178">The following illustration shows third-party e-Commerce customer authentication flows in Commerce.</span></span>

<span data-ttu-id="7200a-179"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-3.jpg" target="_blank">![サード パーティ E コマースの顧客認証フロー](./media/arch-auth-flow-3.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="7200a-179"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-3.jpg" target="_blank">![Third-party e-Commerce customer authentication flows](./media/arch-auth-flow-3.jpg)</a></span></span>

## <a name="third-party-application-authentication-flows"></a><span data-ttu-id="7200a-180">サード パーティ製アプリケーションの認証フロー</span><span class="sxs-lookup"><span data-stu-id="7200a-180">Third-party application authentication flows</span></span>

<span data-ttu-id="7200a-181">次の図は、Commerce のサード パーティ製アプリケーションの認証フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="7200a-181">The following illustration shows third-party application authentication flows in Commerce.</span></span>

<span data-ttu-id="7200a-182"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-4.jpg" target="_blank">![サード パーティ製アプリケーションの認証フロー](./media/arch-auth-flow-4.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="7200a-182"><a href="https://docs.microsoft.com/dynamics365/commerce/media/arch-auth-flow-4.jpg" target="_blank">![Third-party application authentication flows](./media/arch-auth-flow-4.jpg)</a></span></span>

## <a name="additional-resources"></a><span data-ttu-id="7200a-183">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7200a-183">Additional resources</span></span>

[<span data-ttu-id="7200a-184">Dynamics 365 Commerce アーキテクチャの概要</span><span class="sxs-lookup"><span data-stu-id="7200a-184">Dynamics 365 Commerce architecture overview</span></span>](commerce-architecture.md)

[<span data-ttu-id="7200a-185">Commerce Scale Unit の顧客およびコンシューマー API</span><span class="sxs-lookup"><span data-stu-id="7200a-185">Commerce Scale Unit customer and consumer APIs</span></span>](/dev-itpro/retail-server-customer-consumer-api.md)

[<span data-ttu-id="7200a-186">POS 作業者 ログオン</span><span class="sxs-lookup"><span data-stu-id="7200a-186">POS worker logon</span></span>](retail-modern-pos-device-activation.md#create-a-worker)

[<span data-ttu-id="7200a-187">POS サインインの Azure Active Directory 認証を有効にする</span><span class="sxs-lookup"><span data-stu-id="7200a-187">Enable Azure Active Directory authentication for POS sign-in</span></span>](aad-pos-logon.md)

[<span data-ttu-id="7200a-188">MPOS および Cloud POS の拡張ログオン機能の設定</span><span class="sxs-lookup"><span data-stu-id="7200a-188">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="7200a-189">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-189">Set up a B2C tenant in Commerce</span></span>](set-up-b2c-tenant.md)

[<span data-ttu-id="7200a-190">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="7200a-190">Set up custom pages for user sign-ins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7200a-191">認証プロバイダーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7200a-191">Configure authentication providers</span></span>](/dev-itpro/configure-authentication-providers.md)

[<span data-ttu-id="7200a-192">販売時点管理 (POS) デバイスのライセンス認証</span><span class="sxs-lookup"><span data-stu-id="7200a-192">Point of Sale (POS) device activation</span></span>](/dev-itpro/retail-device-activation.md)
