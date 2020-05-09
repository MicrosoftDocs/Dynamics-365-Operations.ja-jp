---
title: Commerce 環境での複数の B2C テナントのコンフィギュレーション
description: このトピックでは、専用の Dynamics 365 Commerce 環境で、複数のチャネルごとの Microsoft Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントの設定時期と方法について説明します。
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6ca48badbe15b7e1bf543716a9b0e3da31477a20
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096514"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="add3b-103">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="add3b-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="add3b-104">このトピックでは、専用の Dynamics 365 Commerce 環境で、複数の Microsoft Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントをチャネルごとに設定する時期と方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="add3b-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="add3b-105">概要</span><span class="sxs-lookup"><span data-stu-id="add3b-105">Overview</span></span>

<span data-ttu-id="add3b-106">Dynamics 365 Commerce では Azure AD B2C クラウド ID サービスを使用して、ユーザーの資格情報と認証フローをサポートします。</span><span class="sxs-lookup"><span data-stu-id="add3b-106">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="add3b-107">ユーザーは認証フローを使用して、パスワードの登録、ログイン、およびリセットを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="add3b-107">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="add3b-108">Azure AD B2C では、ユーザー名やパスワードなどの機密性の高い認証情報を保存します。</span><span class="sxs-lookup"><span data-stu-id="add3b-108">Azure AD B2C stores a user's sensitive authentication information, such as his or her user name and password.</span></span> <span data-ttu-id="add3b-109">ユーザー レコードは、各 B2C テナントに固有であり、ユーザー名 (電子メールアドレス) またはソーシャル ID プロバイダーの資格情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="add3b-109">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="add3b-110">多くの場合、単一の Azure AD B2C テナントは Commerce 環境で使用されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-110">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="add3b-111">その後、Commerce の顧客は同じ Commerce 環境で複数のサイトを作成および公開することができ、それらのサイトで同じ顧客の資格情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-111">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="add3b-112">ただし環境内のサイトを別のブランドとして扱う必要があり、ユーザーには別のビジネスとして表示される場合、B2C テナントはサイトまたはブランドの分離に使用されるチャネルに対してコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="add3b-112">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="add3b-113">チャネルごとに複数の B2C テナントを設定する場合の考慮事項</span><span class="sxs-lookup"><span data-stu-id="add3b-113">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="add3b-114">各チャネルまたはサイトが個別のビジネスとして扱われる場合、Commerce のユーザー認証フローに関する最適なオプションは異なる法人エンティティを使用することです。</span><span class="sxs-lookup"><span data-stu-id="add3b-114">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="add3b-115">ただし、同じ環境と法人各チャネルまたはサイトを保持しながら各サイトの個別ユーザー認証を使用する場合は、先に進む前に次の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-115">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="add3b-116">ユーザーは、チャネルまたはサイトごとに個別の資格情報を持つことになります。</span><span class="sxs-lookup"><span data-stu-id="add3b-116">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="add3b-117">各アカウントはそれぞれ別の B2C テナントに一意のエントリになるので、同じ人がチャネルまたはサイトごとに 2 つのアカウントを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="add3b-117">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="add3b-118">Microsoft Dynamics 環境では、グローバル レコードの検索に対して個別の顧客レコードが返されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-118">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="add3b-119">ユーザーがチャネルまたはサイト間で同じ電子メールアドレスを使用している場合、グローバル顧客検索ではチャネルまたはサイトごとに結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-119">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="add3b-120">(チャネル インジケータが表示されます。)</span><span class="sxs-lookup"><span data-stu-id="add3b-120">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="add3b-121">アドレス帳を使用して、ユーザーをグループ化し、チャネルごとに追跡できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="add3b-121">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="add3b-122">チャンネルごとの顧客レコード数が増加し、この増加がグローバル顧客検索のパフォーマンスに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-122">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="add3b-123">B2C テナントは顧客が誤ったテナントにサイン アップする状況を防止するために、チャネルに注意深くマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-123">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="add3b-124">そうしないと、混乱や追跡の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-124">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="add3b-125">次の図は、Commerce 環境における複数の B2C テナントを示しています。</span><span class="sxs-lookup"><span data-stu-id="add3b-125">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Commerce 環境での B2C テナントを複数化](media/MultiB2C_In_Environment.png)

<span data-ttu-id="add3b-127">同じ Commerce 環境にあるチャネルごとに個別の B2C テナントが必要であると判断した場合は、次のセクションの手順を実行し、この機能を要求します。</span><span class="sxs-lookup"><span data-stu-id="add3b-127">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a><span data-ttu-id="add3b-128">お客様の環境でチャネルごとの B2C を有効にすることを要求</span><span class="sxs-lookup"><span data-stu-id="add3b-128">Request that B2C per channel be enabled in your environment</span></span>

<span data-ttu-id="add3b-129">現在、チャネルごとに個別の B2C テナントを同じ Commerce 環境で使用できるようにするには、Dynamics 365 Commerce に要求を提出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-129">Currently, if you want distinct B2C tenants per channel to be available in the same Commerce environment, you must submit a request to Dynamics 365 Commerce.</span></span> <span data-ttu-id="add3b-130">詳細については、[Lifecycle Services (LCS) のサポートを受ける](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照するか、または Commerce ソリューションへ連絡し相談してください。</span><span class="sxs-lookup"><span data-stu-id="add3b-130">For more information, see [Get support for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), or discuss this issue with your Commerce solutions contact.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="add3b-131">お客様の環境での B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="add3b-131">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="add3b-132">使用している環境で B2C テナントをコンフィギュレーションするには、このセクションの該当する手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="add3b-132">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="add3b-133">Azure AD B2C テナントの追加</span><span class="sxs-lookup"><span data-stu-id="add3b-133">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="add3b-134">Azure AD B2C テナントをお客様の環境に追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="add3b-134">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="add3b-135">システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-135">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="add3b-136">左のナビゲーション ウィンドウで、**テナント設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="add3b-136">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="add3b-137">**B2C 設定**を選択し、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-137">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="add3b-138">**B2C アプリケーションを追加**を選択し、以下の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-138">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="add3b-139">**アプリケーション名**: Commerce で管理するコンテキストのアプリケーションで使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-139">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="add3b-140">Azure ポータルの Azure AD B2C アプリケーションを設定する際に、選択したアプリケーション名の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="add3b-140">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="add3b-141">このようにして、Commerce の B2C テナントを管理する際に混乱を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="add3b-141">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="add3b-142">**テナント名**: Azure ポータルに表示される B2C テナント名を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-142">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="add3b-143">**Password Policy ID 忘れた**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-143">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="add3b-144">**Signin Policy ID をサインアップ**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-144">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="add3b-145">**クライアント GUID**: Azure ポータルに表示されるとおりに Azure AD B2C テナント ID (B2C テナントのアプリケーション ID ではない) を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-145">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="add3b-146">**Profile Policy ID を編集**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="add3b-146">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="add3b-147">情報の入力が完了したら、**承認**を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="add3b-147">When you've finished entering this information, select **OK** to save your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="add3b-148">Dynamics 365 Commerce チームがそれらを設定するよう指示しない限り、**スコープ**、**Non Interactive Policy ID**、**Non Interactive Client ID**、**Custom Domain をログイン**および **Policy ID をサインアップ**ブランクなどのフィールドを残す必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-148">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>
<span data-ttu-id="add3b-149">新しい Azure AD B2C テナントが、**B2C Applications の管理**下の一覧に表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="add3b-149">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="add3b-150">Azure AD B2C テナントの管理または削除</span><span class="sxs-lookup"><span data-stu-id="add3b-150">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="add3b-151">システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-151">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="add3b-152">左のナビゲーション ウィンドウで、**テナント設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="add3b-152">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="add3b-153">**B2C 設定**を選択し、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-153">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="add3b-154">B2C テナントを編集するには、その横にある鉛筆の記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-154">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="add3b-155">B2C テナントを削除するには、その横のごみ箱アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-155">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="add3b-156">**保存**を選び、**発行**を選択して変更をアクティブにします。</span><span class="sxs-lookup"><span data-stu-id="add3b-156">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="add3b-157">ライブまたは公開サイトに対して B2C テナントをコンフィギュレーションすると、ユーザーはテナントに存在するアカウントを使用してサインアップした可能性があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-157">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="add3b-158">**テナントの設定 \> B2C テナント**メニュー上でコンフィギュレーションされたテナントを削除する場合、テナントのチャネルに関連付けられているサイトから B2C テナントのアソシエーションを削除することになります。</span><span class="sxs-lookup"><span data-stu-id="add3b-158">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="add3b-159">この場合、ユーザーは自分のアカウントにログインできなくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-159">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="add3b-160">したがって、コンフィギュレーション済のテナントを削除する場合は細心の注意を払ってください。</span><span class="sxs-lookup"><span data-stu-id="add3b-160">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="add3b-161">コンフィギュレーションされたテナントを削除すると、B2C テナントとレコードが引き続き維持されますが、そのテナントの Commerce システム コンフィギュレーションは変更または削除されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-161">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="add3b-162">サイトへサイン アップまたはサイト インを試みるユーザーは、サイトのチャネルに対してコンフィギュレーションされた既定または新しく関連付けられた B2C テナントに新しいアカウント レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="add3b-162">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>
## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="add3b-163">B2C テナントでのチャネルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="add3b-163">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="add3b-164">システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-164">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="add3b-165">左のナビゲーション ウィンドウで、**サイト設定**を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="add3b-165">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="add3b-166">**チャネル**を選択し、コンフィギュレーションするチャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-166">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="add3b-167">右側のプロパティ ウィンドウの **B2C アプリケーションの選択**フィールドで、このチャネルに使用されるコンフィギュレーション済み Azure AD B2C テナントを選択します。</span><span class="sxs-lookup"><span data-stu-id="add3b-167">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="add3b-168">コマンド バーで**保存と発行**を選択し、新規または更新されたコンフィギュレーションをコミットします。</span><span class="sxs-lookup"><span data-stu-id="add3b-168">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="add3b-169">チャネルに割り当てられている B2C アプリケーションを変更すると、その環境に既にサイン アップしているすべてのユーザーに対して確立されている現在の参照を削除することになります。</span><span class="sxs-lookup"><span data-stu-id="add3b-169">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="add3b-170">この場合、現在割り当てられている B2C アプリケーションに関連付けられている資格情報は、ユーザーに使用できません。</span><span class="sxs-lookup"><span data-stu-id="add3b-170">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="add3b-171">したがって、チャネルを初めて設定するときにユーザーが登録できなかった場合にのみ、チャネル Azure AD B2C コンフィギュレーションを変更してください。</span><span class="sxs-lookup"><span data-stu-id="add3b-171">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="add3b-172">そうしないと、新しい Azure AD B2C テナントのレコードを確立するために、ユーザーが再度サイン アップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="add3b-172">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="add3b-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="add3b-173">Additional resources</span></span>

[<span data-ttu-id="add3b-174">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="add3b-174">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="add3b-175">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="add3b-175">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="add3b-176">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="add3b-176">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="add3b-177">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="add3b-177">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="add3b-178">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="add3b-178">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="add3b-179">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="add3b-179">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="add3b-180">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="add3b-180">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="add3b-181">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="add3b-181">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="add3b-182">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="add3b-182">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="add3b-183">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="add3b-183">Enable location-based store detection</span></span>](enable-store-detection.md)