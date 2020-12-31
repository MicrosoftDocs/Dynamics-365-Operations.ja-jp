---
title: Lifecycle Services (LCS) のセキュリティの構成
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のセキュリティが、組織レベルとプロジェクト レベルの両方で制御される方法について説明します。
author: AngelMarshall
manager: AnnBe
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.assetid: 79396ff8-538f-4f6f-80d0-898fc5618fb5
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf02ea673a550a7ac257008e3e67277025d13506
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679254"
---
# <a name="configure-lifecycle-services-lcs-security"></a><span data-ttu-id="c64fc-103">Lifecycle Services (LCS) のセキュリティの構成</span><span class="sxs-lookup"><span data-stu-id="c64fc-103">Configure Lifecycle Services (LCS) security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c64fc-104">Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-104">Security in Microsoft Dynamics Lifecycle Services (LCS) is controlled at both the organization level and the project level.</span></span> <span data-ttu-id="c64fc-105">組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c64fc-105">Not all members of an organization have access to all projects.</span></span> <span data-ttu-id="c64fc-106">また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c64fc-106">Additionally, the members of a project might not all be members of the same organization.</span></span> <br>

<span data-ttu-id="c64fc-107">現在、サインアップ時に [Microsoft 365 ポータル](https://go.microsoft.com/fwlink/?LinkID=324287)で作成した Microsoft Azure Active Directory (Azure AD) 資格情報を使用してサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-107">Currently, users can sign in by using the Microsoft Azure Active Directory (Azure AD) credentials that they created in the [Microsoft 365 portal](https://go.microsoft.com/fwlink/?LinkID=324287) when they signed up.</span></span> <span data-ttu-id="c64fc-108">Azure AD の組織の管理者になっているユーザーは、Lifecycle Services (LCS) の管理者になります。</span><span class="sxs-lookup"><span data-stu-id="c64fc-108">Users who are administrators for their organization in Azure AD will be administrators in Lifecycle Services (LCS).</span></span> <br> 

<span data-ttu-id="c64fc-109">Microsoft Dynamics AX 2012 では、LCS への組織レベルのアクセスは、個人の Microsoft ID と CustomerSource または PartnerSource の組織との関連付けによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-109">For Microsoft Dynamics AX 2012, organization-level access to LCS is controlled by the association of a person’s Microsoft ID with an organization in CustomerSource or PartnerSource.</span></span> <span data-ttu-id="c64fc-110">したがって、CustomerSource または PartnerSource のユーザーは、LCS の組織のワークスペースに自動的にアクセスし、参加するように招待されたすべてのプロジェクトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-110">Therefore, users of CustomerSource or PartnerSource automatically have access to their organization’s workspace in LCS, and can view all projects that they have been invited to participate in.</span></span> <span data-ttu-id="c64fc-111">CustomerSource および PartnerSource の組織の管理者になっているユーザーは LCS の管理者になります。</span><span class="sxs-lookup"><span data-stu-id="c64fc-111">Users who are administrators for their organization in CustomerSource and PartnerSource will be administrators in LCS.</span></span> <br>

<span data-ttu-id="c64fc-112">管理者は CustomerSource または PartnerSource の資格情報を持っていないユーザーを LCS の組織のメンバーに招待できますが、この方法はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="c64fc-112">Although an administrator can invite users who don’t have CustomerSource or PartnerSource credentials to be members of an organization in LCS, we don't recommend this approach.</span></span> <span data-ttu-id="c64fc-113">LCS 組織のメンバーとなるよう招待されたユーザーには、CustomerSource または PartnerSource での資格情報が提供されません。</span><span class="sxs-lookup"><span data-stu-id="c64fc-113">Users who are invited to be members of an LCS organization aren't provided with credentials in CustomerSource or PartnerSource.</span></span> <br> 

<span data-ttu-id="c64fc-114">LCS へのプロジェクト レベル アクセスは、招待によって行われます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-114">Project-level access to LCS is by invitation.</span></span> <span data-ttu-id="c64fc-115">プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-115">You can invite members of your organization to be project owners and team members.</span></span> <span data-ttu-id="c64fc-116">また、組織のメンバーではなく、Azure AD、CustomerSource、または PartnerSource のアカンウントを持たないユーザーをチーム メンバーに招待できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-116">Additionally, you can invite users who aren't part of your organization, and who don't have accounts in Azure AD or CustomerSource or PartnerSource, to be team members.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c64fc-117">会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c64fc-117">We strongly recommend that you manage all users within your company at the organization level.</span></span> <span data-ttu-id="c64fc-118">この方法で、組織との関係が CustomerSource、PartnerSource、および Azure AD で正しいことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-118">In that way, you help ensure that their relationship with your organization is correct in CustomerSource, PartnerSource, and Azure AD.</span></span> <span data-ttu-id="c64fc-119">また、ユーザーが組織で利用できる福利厚生にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-119">Additionally, you help ensure that users can access the benefits that are available to your organization.</span></span>

## <a name="manage-lcs-organization-users"></a><span data-ttu-id="c64fc-120">LCS 組織のユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="c64fc-120">Manage LCS organization users</span></span>
<span data-ttu-id="c64fc-121">管理者のみユーザーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-121">Only an administrator can manage users.</span></span> <span data-ttu-id="c64fc-122">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-122">Follow these steps.</span></span>

1.  <span data-ttu-id="c64fc-123">CustomerSource、PartnerSource、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-123">In CustomerSource, PartnerSource, or Azure AD, associate all the users in your organization who require access to LCS with your organization.</span></span> <span data-ttu-id="c64fc-124">ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="c64fc-124">Users might have to wait up to two business days before they can sign in to LCS.</span></span>
2.  <span data-ttu-id="c64fc-125">LCS の適切なプロジェクトに、ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-125">Add your users to the appropriate projects in LCS.</span></span>

### <a name="invite-a-user-to-an-lcs-project"></a><span data-ttu-id="c64fc-126">LCS プロジェクトへのユーザーの招待</span><span class="sxs-lookup"><span data-stu-id="c64fc-126">Invite a user to an LCS project</span></span>

1.  <span data-ttu-id="c64fc-127">[LCS](https://lcs.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="c64fc-127">Sign in to [LCS](https://lcs.dynamics.com/).</span></span>
2.  <span data-ttu-id="c64fc-128">プロジェクトを選択してユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-128">Select the project to add the user to.</span></span>
3.  <span data-ttu-id="c64fc-129">**プロジェクト ユーザー** タイルを選択し、**プロジェクト ユーザー** ページで、プラス記号 (**+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-129">Select the **Project users** tile, and then, on the **Project users** page, select the plus sign (**+**).</span></span>
4.  <span data-ttu-id="c64fc-130">ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、**招待** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-130">Enter the user’s email address, select the correct security role, and then select **Invite**.</span></span>

> [!NOTE]
> <span data-ttu-id="c64fc-131">実装プロジェクトで、招待されたユーザーの実装ロールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-131">For implementation projects, you can select the implementation role for the invited user.</span></span> <span data-ttu-id="c64fc-132">**FastTrack からの連絡を許可する** を **はい** に設定した場合、Microsoft FastTrack チームは実装ロールと実装プロジェクトのステージに基づいてご連絡を差し上げる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c64fc-132">If you set **Allow FastTrack to contact** to **Yes**, then Microsoft FastTrack team may reach out to you based on your implementation role and the stages of the implementation project.</span></span>   

## <a name="working-with-customersource-and-partnersource"></a><span data-ttu-id="c64fc-133">CustomerSource および PartnerSource での作業</span><span class="sxs-lookup"><span data-stu-id="c64fc-133">Working with CustomerSource and PartnerSource</span></span>
<span data-ttu-id="c64fc-134">このセクションの情報は、CustomerSource または PartnerSource へのアクセスを支援することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="c64fc-134">The information in this section is intended to help you access CustomerSource or PartnerSource.</span></span>

### <a name="signing-in-to-customersource-or-partnersource"></a><span data-ttu-id="c64fc-135">CustomerSource または PartnerSource へのサインイン</span><span class="sxs-lookup"><span data-stu-id="c64fc-135">Signing in to CustomerSource or PartnerSource</span></span>

<span data-ttu-id="c64fc-136">[CustomerSource サインイン ページ](https://mbs.microsoft.com/customersource/)に移動し、Microsoft アカウント (以前は Windows Live ID と呼ばれる) のユーザー名とパスワードを入力してサイトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c64fc-136">Visit the [CustomerSource sign-in page](https://mbs.microsoft.com/customersource/), and enter the user name and password for your Microsoft account (previously known as Windows Live ID) to access the site.</span></span> <span data-ttu-id="c64fc-137">組織の CustomerSource 勘定へのアクセスがない場合、「[CustomerSource](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource) にログインする方法」ページに従います。</span><span class="sxs-lookup"><span data-stu-id="c64fc-137">If you don't have access to your organization’s CustomerSource account, follow the steps on the [How to sign in to CustomerSource](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource) page.</span></span>

### <a name="determining-the-administrator-for-your-organization-in-customersource-or-partnersource"></a><span data-ttu-id="c64fc-138">CustomerSource または PartnerSource で組織の管理者を決定する</span><span class="sxs-lookup"><span data-stu-id="c64fc-138">Determining the administrator for your organization in CustomerSource or PartnerSource</span></span>

<span data-ttu-id="c64fc-139">CustomerSource の管理者がわからない場合、または組織に CustomerSource 管理者がいない場合は、電子メールを [itmbssup@microsoft.com](mailto:itmbssup@microsoft.com) に送信してお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="c64fc-139">If you don’t know your CustomerSource administrator, or if your organization doesn’t have a CustomerSource administrator, send an email to [itmbssup@microsoft.com](mailto:itmbssup@microsoft.com) for assistance.</span></span>

## <a name="configuring-project-security"></a><span data-ttu-id="c64fc-140">プロジェクト セキュリティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c64fc-140">Configuring project security</span></span>
<span data-ttu-id="c64fc-141">プロジェクトにユーザーとして参加するように、組織の内外からユーザーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-141">You can invite users from inside or outside your organization to join your project as users.</span></span> <span data-ttu-id="c64fc-142">次のテーブルに、ユーザーが使用可能なロールを示します。</span><span class="sxs-lookup"><span data-stu-id="c64fc-142">The following table describes the roles that are available for users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c64fc-143">役割</span><span class="sxs-lookup"><span data-stu-id="c64fc-143">Role</span></span></th>
<th><span data-ttu-id="c64fc-144">説明</span><span class="sxs-lookup"><span data-stu-id="c64fc-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c64fc-145">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="c64fc-145">Project owner</span></span></td>
<td><span data-ttu-id="c64fc-146">このロールのメンバーは LCS のすべてのツールにアクセスでき、他のユーザーを任意のロールに追加することや、プロジェクトを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-146">Members of this role have access to all tools in LCS, can add other users in any role, and can delete the project.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c64fc-147">環境マネージャー</span><span class="sxs-lookup"><span data-stu-id="c64fc-147">Environment manager</span></span></td>
<td><span data-ttu-id="c64fc-148">このロールのメンバーは LCS のすべてのツールにアクセスでき、クラウド ホスト環境を管理できます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-148">Members of this role have access to all tools in LCS and can manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c64fc-149">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="c64fc-149">Project team member</span></span></td>
<td><span data-ttu-id="c64fc-150">このロールのメンバーは LCS のすべてのツールにアクセスできますが、クラウド ホスト環境を管理できません。</span><span class="sxs-lookup"><span data-stu-id="c64fc-150">Members of this role have access to all tools in LCS but can&#39;t manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c64fc-151">プロジェクト チーム メンバー (見込顧客)</span><span class="sxs-lookup"><span data-stu-id="c64fc-151">Project team member (prospect)</span></span></td>
<td><span data-ttu-id="c64fc-152">このロールのメンバーは LCS プロジェクトのすべてのツールに制限付きでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-152">Members of this role have limited access to all tools in an LCS project.</span></span> <span data-ttu-id="c64fc-153">見込顧客は、プロジェクトに追加されましたが、VOICE または Azure AD にアカウントを持っていないユーザーです。</span><span class="sxs-lookup"><span data-stu-id="c64fc-153">Prospects are users who have been added to a project, but who don&#39;t have an account in VOICE or an Azure AD account.</span></span> <span data-ttu-id="c64fc-154"><strong>見込み顧客</strong>が組織として一覧表示されるため、ユーザーが見込み顧客であることを識別することができます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-154">You can identify that a user is a prospect, because <strong>prospect</strong> is listed as the organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c64fc-155">Operations user</span><span class="sxs-lookup"><span data-stu-id="c64fc-155">Operations user</span></span></td>
<td><span data-ttu-id="c64fc-156">このロールのメンバーは LCS の次のツールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-156">Members of this role have access to the following tools in LCS:</span></span>
<ul>
<li><span data-ttu-id="c64fc-157">システム診断</span><span class="sxs-lookup"><span data-stu-id="c64fc-157">System diagnostics</span></span></li>
<li><span data-ttu-id="c64fc-158">問題検索</span><span class="sxs-lookup"><span data-stu-id="c64fc-158">Issue search</span></span></li>
<li><span data-ttu-id="c64fc-159">クラウドを利用したサポート</span><span class="sxs-lookup"><span data-stu-id="c64fc-159">Cloud-powered support</span></span></li>
<li><span data-ttu-id="c64fc-160">更新</span><span class="sxs-lookup"><span data-stu-id="c64fc-160">Updates</span></span></li>
<li><span data-ttu-id="c64fc-161">クラウド ホスト環境</span><span class="sxs-lookup"><span data-stu-id="c64fc-161">Cloud-hosted environments</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c64fc-162">1 つのプロジェクトのセキュリティをコンフィギュレーションした後は、別のプロジェクトにユーザーをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-162">After you've configured security for one project, you can import the users to another project.</span></span>

## <a name="configure-implementation-roles"></a><span data-ttu-id="c64fc-163">実装ロールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c64fc-163">Configure implementation roles</span></span> 
<span data-ttu-id="c64fc-164">実装プロジェクトがある場合、プロジェクト ユーザーの実装ロールを指定するためのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c64fc-164">If you have an implementation project, you will have the option to specify project user's implementation roles.</span></span> <span data-ttu-id="c64fc-165">詳細については、[Dynamics 365 実装のロール](https://docs.microsoft.com/learn/modules/get-started-implementation-project/01-2-roles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c64fc-165">For more information, see [Roles in a Dynamics 365 implementation](https://docs.microsoft.com/learn/modules/get-started-implementation-project/01-2-roles).</span></span>


