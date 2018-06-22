---
title: "Lifecycle Services のセキュリティのコンフィギュレーション"
description: "Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルおよびプロジェクト レベルの両方で制御されます。 組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。 また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 6154
ms.assetid: 79396ff8-538f-4f6f-80d0-898fc5618fb5
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ec4256ccb00a0d748469076dc8520257a8c4bd57
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-lifecycle-services-security"></a><span data-ttu-id="e3a5c-105">Lifecycle Services のセキュリティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e3a5c-105">Configure Lifecycle Services security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3a5c-106">Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルおよびプロジェクト レベルの両方で制御されます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-106">Security in Microsoft Dynamics Lifecycle Services (LCS) is controlled at both the organization level and the project level.</span></span> <span data-ttu-id="e3a5c-107">組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-107">Not all members of an organization have access to all projects.</span></span> <span data-ttu-id="e3a5c-108">また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-108">Additionally, the members of a project might not all be members of the same organization.</span></span>

<span data-ttu-id="e3a5c-109">Microsoft Dynamics 365 for Finance and Operations の現在のバージョンについては、ユーザーが登録する際に [Microsoft Office 365 ポータル](http://go.microsoft.com/fwlink/?LinkID=324287) で作成された Microsoft Azure Active Directory (Azure AD) 資格情報を使用して、サインインできます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-109">For the current version of Microsoft Dynamics 365 for Finance and Operations, users can sign in by using the Microsoft Azure Active Directory (Azure AD) credentials that they created in the [Microsoft Office 365 portal](http://go.microsoft.com/fwlink/?LinkID=324287) when they signed up.</span></span> <span data-ttu-id="e3a5c-110">Azure AD の組織の管理者になっているユーザーは、Microsoft Dynamics Lifecycle Services (LCS) の管理者になります。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-110">Users who are administrators for their organization in Azure AD will be administrators in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e3a5c-111">Microsoft Dynamics AX 2012 で、LCS への組織レベルのアクセスは、個人の Microsoft ID と CustomerSource または PartnerSource の組織との関連によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-111">For Microsoft Dynamics AX 2012, organization-level access to LCS is controlled by the association of a person’s Microsoft ID with an organization in CustomerSource or PartnerSource.</span></span> <span data-ttu-id="e3a5c-112">したがって、CustomerSource または PartnerSource のユーザーは、LCS の組織のワークスペースに自動的にアクセスし、参加するように招待されたすべてのプロジェクトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-112">Therefore, users of CustomerSource or PartnerSource automatically have access to their organization’s workspace in LCS, and can view all projects that they have been invited to participate in.</span></span> <span data-ttu-id="e3a5c-113">CustomerSource および PartnerSource の組織の管理者になっているユーザーは LCS の管理者になります。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-113">Users who are administrators for their organization in CustomerSource and PartnerSource will be administrators in LCS.</span></span> <span data-ttu-id="e3a5c-114">管理者は CustomerSource または PartnerSource の資格情報を持っていないユーザーを LCS の組織のメンバーに招待できますが、この方法はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-114">Although an administrator can invite people who don’t have CustomerSource or PartnerSource credentials to be members of an organization in LCS, we don't recommend this approach.</span></span> <span data-ttu-id="e3a5c-115">LCS 組織のメンバーとなるよう招待されたユーザーには、CustomerSource または PartnerSource での資格情報が提供されません。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-115">People who are invited to be members of an LCS organization aren't provided with credentials in CustomerSource or PartnerSource.</span></span> <span data-ttu-id="e3a5c-116">LCS へのプロジェクト レベル アクセスは、招待によって行われます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-116">Project-level access to LCS is by invitation.</span></span> <span data-ttu-id="e3a5c-117">プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-117">You can invite members of your organization to be project owners and team members.</span></span> <span data-ttu-id="e3a5c-118">また、組織のメンバーではなく、Azure AD、CustomerSource、または PartnerSource のアカンウントを持たないユーザーをチーム メンバーに招待できます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-118">Additionally, you can invite users who aren't part of your organization, and who don't have accounts in Azure AD or CustomerSource or PartnerSource, to be team members.</span></span> <span data-ttu-id="e3a5c-119">**重要:** 会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-119">**Important:** We strongly recommend that you manage all users within your company at the organization level.</span></span> <span data-ttu-id="e3a5c-120">この方法では、組織との関係が CustomerSource、PartnerSource、および Azure AD で正しいことを保証できます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-120">In that way, you help guarantee that their relationship with your organization is correct in CustomerSource, PartnerSource, and Azure AD.</span></span> <span data-ttu-id="e3a5c-121">また、ユーザーが組織で利用できる福利厚生にアクセスできることを保証します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-121">Additionally, you help guarantee that users can access the benefits that are available to your organization.</span></span>

## <a name="manage-lcs-organization-users"></a><span data-ttu-id="e3a5c-122">LCS 組織のユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="e3a5c-122">Manage LCS organization users</span></span>
<span data-ttu-id="e3a5c-123">管理者のみユーザーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-123">Only an administrator can manage users.</span></span> <span data-ttu-id="e3a5c-124">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-124">Follow these steps.</span></span>

1.  <span data-ttu-id="e3a5c-125">CustomerSource、PartnerSource、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-125">In CustomerSource, PartnerSource, or Azure AD, associate all the users in your organization who require access to LCS with your organization.</span></span> <span data-ttu-id="e3a5c-126">ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-126">Users might have to wait up to two business days before they can sign in to LCS.</span></span>
2.  <span data-ttu-id="e3a5c-127">LCS の適切なプロジェクトに、ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-127">Add your users to the appropriate projects in LCS.</span></span>

### <a name="invite-a-user-to-an-lcs-project"></a><span data-ttu-id="e3a5c-128">LCS プロジェクトへのユーザーの招待</span><span class="sxs-lookup"><span data-stu-id="e3a5c-128">Invite a user to an LCS project</span></span>

1.  <span data-ttu-id="e3a5c-129">[LCS](http://lcs.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-129">Sign in to [LCS](http://lcs.dynamics.com/).</span></span>
2.  <span data-ttu-id="e3a5c-130">プロジェクトをクリックしてユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-130">Click the project to add the user to.</span></span>
3.  <span data-ttu-id="e3a5c-131">**プロジェクト ユーザー** タイルをクリックし、**プロジェクト ユーザー** ページで、プラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-131">Click the **Project users** tile, and then, on the **Project users** page, click the plus sign (**+**).</span></span>
4.  <span data-ttu-id="e3a5c-132">ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、**招待**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-132">Enter the user’s email address, select the correct security role, and then click **Invite**.</span></span>

## <a name="working-with-customersource-and-partnersource"></a><span data-ttu-id="e3a5c-133">CustomerSource および PartnerSource での作業</span><span class="sxs-lookup"><span data-stu-id="e3a5c-133">Working with CustomerSource and PartnerSource</span></span>
<span data-ttu-id="e3a5c-134">このセクションの情報は、CustomerSource または PartnerSource へのアクセスを支援することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-134">The information in this section is intended to help you access CustomerSource or PartnerSource.</span></span>

### <a name="signing-in-to-customersource-or-partnersource"></a><span data-ttu-id="e3a5c-135">CustomerSource または PartnerSource にサインインしています</span><span class="sxs-lookup"><span data-stu-id="e3a5c-135">Signing in to CustomerSource or PartnerSource</span></span>

<span data-ttu-id="e3a5c-136">[CustomerSource サインイン ページ](https://mbs.microsoft.com/customersource/)に移動し、Microsoft アカウント (以前は Windows Live ID と呼ばれる) のユーザー名とパスワードを入力してサイトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-136">Visit the [CustomerSource sign-in page](https://mbs.microsoft.com/customersource/), and enter the user name and password for your Microsoft account (previously known as Windows Live ID) to access the site.</span></span> <span data-ttu-id="e3a5c-137">組織の CustomerSource 勘定へのアクセスがない場合、「[CustomerSource にログインする方法](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource)」ページに従います。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-137">If you don't have access to your organization’s CustomerSource account, follow the steps on the [How to sign in to CustomerSource](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource) page.</span></span>

### <a name="determining-the-administrator-for-your-organization-in-customersource-or-partnersource"></a><span data-ttu-id="e3a5c-138">CustomerSource または PartnerSource で組織の管理者を決定する</span><span class="sxs-lookup"><span data-stu-id="e3a5c-138">Determining the administrator for your organization in CustomerSource or PartnerSource</span></span>

<span data-ttu-id="e3a5c-139">CustomerSource の管理者がわからない場合、または組織に CustomerSource 管理者がいない場合は、ヘルプを表示するには、電子メール メッセージを [itmbssup@microsoft.com](http://itmbssup@microsoft.com) に送信します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-139">If you don’t know your CustomerSource administrator, or if your organization doesn’t have a CustomerSource administrator, send an email message to [itmbssup@microsoft.com](http://itmbssup@microsoft.com) for help.</span></span>

## <a name="configuring-project-security"></a><span data-ttu-id="e3a5c-140">プロジェクト セキュリティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e3a5c-140">Configuring project security</span></span>
<span data-ttu-id="e3a5c-141">プロジェクトにユーザーとして参加するように、組織の内外からユーザーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-141">You can invite users from inside or outside your organization to join your project as users.</span></span> <span data-ttu-id="e3a5c-142">次のテーブルに、ユーザーが使用可能なロールを示します。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-142">The following table describes the roles that are available for users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3a5c-143">役割</span><span class="sxs-lookup"><span data-stu-id="e3a5c-143">Role</span></span></th>
<th><span data-ttu-id="e3a5c-144">説明</span><span class="sxs-lookup"><span data-stu-id="e3a5c-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3a5c-145">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="e3a5c-145">Project owner</span></span></td>
<td><span data-ttu-id="e3a5c-146">このロールのメンバーは LCS のすべてのツールにアクセスでき、他のユーザーを任意のロールに追加することや、プロジェクトを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-146">Members of this role have access to all tools in LCS, can add other users in any role, and can delete the project.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5c-147">環境マネージャー</span><span class="sxs-lookup"><span data-stu-id="e3a5c-147">Environment manager</span></span></td>
<td><span data-ttu-id="e3a5c-148">このロールのメンバーは LCS のすべてのツールにアクセスでき、クラウド ホスト環境を管理できます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-148">Members of this role have access to all tools in LCS and can manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5c-149">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="e3a5c-149">Project team member</span></span></td>
<td><span data-ttu-id="e3a5c-150">このロールのメンバーは LCS のすべてのツールにアクセスできますが、クラウド ホスト環境を管理できません。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-150">Members of this role have access to all tools in LCS but can&#39;t manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3a5c-151">プロジェクト チーム メンバー (見込顧客)</span><span class="sxs-lookup"><span data-stu-id="e3a5c-151">Project team member (prospect)</span></span></td>
<td><span data-ttu-id="e3a5c-152">このロールのメンバーは LCS プロジェクトのすべてのツールに制限付きでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-152">Members of this role have limited access to all tools in an LCS project.</span></span> <span data-ttu-id="e3a5c-153">見込顧客は、プロジェクトに追加されたが、VOICE または Azure AD アカウントを持っていないユーザーです。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-153">Prospects are users who have been added to a project, but who don&#39;t have an account in VOICE or an Azure AD account.</span></span> <span data-ttu-id="e3a5c-154"><strong>見込み顧客</strong> がユーザーの組織として一覧表示されるため、ユーザーが見込み顧客であることを識別することができます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-154">You can identify that a user is a prospect, because <strong>prospect</strong> is listed as his or her organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3a5c-155">オペレーション ユーザー</span><span class="sxs-lookup"><span data-stu-id="e3a5c-155">Operations user</span></span></td>
<td><span data-ttu-id="e3a5c-156">このロールのメンバーは LCS の次のツールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-156">Members of this role have access to the following tools in LCS:</span></span>
<ul>
<li><span data-ttu-id="e3a5c-157">システム診断</span><span class="sxs-lookup"><span data-stu-id="e3a5c-157">System diagnostics</span></span></li>
<li><span data-ttu-id="e3a5c-158">問題検索</span><span class="sxs-lookup"><span data-stu-id="e3a5c-158">Issue search</span></span></li>
<li><span data-ttu-id="e3a5c-159">クラウドを利用したサポート</span><span class="sxs-lookup"><span data-stu-id="e3a5c-159">Cloud-powered support</span></span></li>
<li><span data-ttu-id="e3a5c-160">更新</span><span class="sxs-lookup"><span data-stu-id="e3a5c-160">Updates</span></span></li>
<li><span data-ttu-id="e3a5c-161">クラウド ホスト環境</span><span class="sxs-lookup"><span data-stu-id="e3a5c-161">Cloud-hosted environments</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e3a5c-162">1 つのプロジェクトのセキュリティをコンフィギュレーションした後は、別のプロジェクトにユーザーをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="e3a5c-162">After you've configured security for one project, you can import the users to another project.</span></span>




