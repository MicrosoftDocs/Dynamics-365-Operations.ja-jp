---
title: Lifecycle Services (LCS) のセキュリティの構成
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) のセキュリティが、組織レベルとプロジェクト レベルの両方で制御される方法について説明します。
author: AngelMarshall
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6154
ms.assetid: 79396ff8-538f-4f6f-80d0-898fc5618fb5
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19c33dd33b90317c03bae71fa940a38b53261866
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924118"
---
# <a name="configure-lifecycle-services-lcs-security"></a><span data-ttu-id="b04f3-103">Lifecycle Services (LCS) のセキュリティの構成</span><span class="sxs-lookup"><span data-stu-id="b04f3-103">Configure Lifecycle Services (LCS) security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b04f3-104">Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-104">Security in Microsoft Dynamics Lifecycle Services (LCS) is controlled at both the organization level and the project level.</span></span> <span data-ttu-id="b04f3-105">組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b04f3-105">Not all members of an organization have access to all projects.</span></span> <span data-ttu-id="b04f3-106">また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b04f3-106">Additionally, the members of a project might not all be members of the same organization.</span></span> <br>

<span data-ttu-id="b04f3-107">現在、サインアップ時に Microsoft 365 ポータルで作成した Microsoft Azure Active Directory (Azure AD) 資格情報を使用してサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-107">Currently, users can sign in by using the Microsoft Azure Active Directory (Azure AD) credentials that they created in the Microsoft 365 portal when they signed up.</span></span> <span data-ttu-id="b04f3-108">Azure AD の組織の管理者になっているユーザーは、Lifecycle Services (LCS) の管理者になります。</span><span class="sxs-lookup"><span data-stu-id="b04f3-108">Users who are administrators for their organization in Azure AD will be administrators in Lifecycle Services (LCS).</span></span> 

<span data-ttu-id="b04f3-109">LCS へのプロジェクト レベル アクセスは、招待によって行われます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-109">Project-level access to LCS is by invitation.</span></span> <span data-ttu-id="b04f3-110">プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-110">You can invite members of your organization to be project owners and team members.</span></span> <span data-ttu-id="b04f3-111">また、組織のメンバーではなく、Azure AD のアカンウントを持たないユーザーをチーム メンバーに招待できます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-111">Additionally, you can invite users who aren't part of your organization, and who don't have accounts in Azure AD to be team members.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b04f3-112">会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b04f3-112">We strongly recommend that you manage all users within your company at the organization level.</span></span> <span data-ttu-id="b04f3-113">また、ユーザーが組織で利用できる福利厚生にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-113">Additionally, you help ensure that users can access the benefits that are available to your organization.</span></span>

## <a name="manage-lcs-organization-users"></a><span data-ttu-id="b04f3-114">LCS 組織のユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="b04f3-114">Manage LCS organization users</span></span>
<span data-ttu-id="b04f3-115">管理者のみユーザーを管理できます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-115">Only an administrator can manage users.</span></span> <span data-ttu-id="b04f3-116">以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-116">Follow these steps.</span></span>

1.  <span data-ttu-id="b04f3-117">PartnerSource ビジネス センター (PSBC)、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-117">In PartnerSource Business Center (PSBC) or Azure AD, associate all the users in your organization who require access to LCS with your organization.</span></span> <span data-ttu-id="b04f3-118">ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b04f3-118">Users might have to wait up to two business days before they can sign in to LCS.</span></span>
2.  <span data-ttu-id="b04f3-119">LCS の適切なプロジェクトに、ユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-119">Add your users to the appropriate projects in LCS.</span></span>

### <a name="invite-a-user-to-an-lcs-project"></a><span data-ttu-id="b04f3-120">LCS プロジェクトへのユーザーの招待</span><span class="sxs-lookup"><span data-stu-id="b04f3-120">Invite a user to an LCS project</span></span>

1.  <span data-ttu-id="b04f3-121">[LCS](https://lcs.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="b04f3-121">Sign in to [LCS](https://lcs.dynamics.com/).</span></span>
2.  <span data-ttu-id="b04f3-122">プロジェクトを選択してユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-122">Select the project to add the user to.</span></span>
3.  <span data-ttu-id="b04f3-123">**プロジェクト ユーザー** タイルを選択し、**プロジェクト ユーザー** ページで、プラス記号 (**+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-123">Select the **Project users** tile, and then, on the **Project users** page, select the plus sign (**+**).</span></span>
4.  <span data-ttu-id="b04f3-124">ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、**招待** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-124">Enter the user’s email address, select the correct security role, and then select **Invite**.</span></span>

> [!NOTE]
> <span data-ttu-id="b04f3-125">実装プロジェクトで、招待されたユーザーの実装ロールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-125">For implementation projects, you can select the implementation role for the invited user.</span></span> <span data-ttu-id="b04f3-126">**FastTrack からの連絡を許可する** を **はい** に設定した場合、Microsoft FastTrack チームは実装ロールと実装プロジェクトのステージに基づいてご連絡を差し上げる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b04f3-126">If you set **Allow FastTrack to contact** to **Yes**, then Microsoft FastTrack team may reach out to you based on your implementation role and the stages of the implementation project.</span></span>   


## <a name="configuring-project-security"></a><span data-ttu-id="b04f3-127">プロジェクト セキュリティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b04f3-127">Configuring project security</span></span>
<span data-ttu-id="b04f3-128">プロジェクトにユーザーとして参加するように、組織の内外からユーザーを招待することができます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-128">You can invite users from inside or outside your organization to join your project as users.</span></span> <span data-ttu-id="b04f3-129">次のテーブルに、ユーザーが使用可能なロールを示します。</span><span class="sxs-lookup"><span data-stu-id="b04f3-129">The following table describes the roles that are available for users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b04f3-130">役割</span><span class="sxs-lookup"><span data-stu-id="b04f3-130">Role</span></span></th>
<th><span data-ttu-id="b04f3-131">説明</span><span class="sxs-lookup"><span data-stu-id="b04f3-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b04f3-132">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="b04f3-132">Project owner</span></span></td>
<td><span data-ttu-id="b04f3-133">このロールのメンバーは LCS のすべてのツールにアクセスでき、他のユーザーを任意のロールに追加することや、プロジェクトを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-133">Members of this role have access to all tools in LCS, can add other users in any role, and can delete the project.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b04f3-134">環境マネージャー</span><span class="sxs-lookup"><span data-stu-id="b04f3-134">Environment manager</span></span></td>
<td><span data-ttu-id="b04f3-135">このロールのメンバーは LCS のすべてのツールにアクセスでき、クラウド ホスト環境を管理できます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-135">Members of this role have access to all tools in LCS and can manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b04f3-136">プロジェクト チーム メンバー</span><span class="sxs-lookup"><span data-stu-id="b04f3-136">Project team member</span></span></td>
<td><span data-ttu-id="b04f3-137">このロールのメンバーは LCS のすべてのツールにアクセスできますが、クラウド ホスト環境を管理できません。</span><span class="sxs-lookup"><span data-stu-id="b04f3-137">Members of this role have access to all tools in LCS but can&#39;t manage cloud-hosted environments.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b04f3-138">プロジェクト チーム メンバー (見込顧客)</span><span class="sxs-lookup"><span data-stu-id="b04f3-138">Project team member (prospect)</span></span></td>
<td><span data-ttu-id="b04f3-139">このロールのメンバーは LCS プロジェクトのすべてのツールに制限付きでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-139">Members of this role have limited access to all tools in an LCS project.</span></span> <span data-ttu-id="b04f3-140">見込顧客は、プロジェクトに追加されましたが、VOICE または Azure AD にアカウントを持っていないユーザーです。</span><span class="sxs-lookup"><span data-stu-id="b04f3-140">Prospects are users who have been added to a project, but who don&#39;t have an account in VOICE or an Azure AD account.</span></span> <span data-ttu-id="b04f3-141"><strong>見込み顧客</strong>が組織として一覧表示されるため、ユーザーが見込み顧客であることを識別することができます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-141">You can identify that a user is a prospect, because <strong>prospect</strong> is listed as the organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b04f3-142">Operations user</span><span class="sxs-lookup"><span data-stu-id="b04f3-142">Operations user</span></span></td>
<td><span data-ttu-id="b04f3-143">このロールのメンバーは LCS の次のツールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-143">Members of this role have access to the following tools in LCS:</span></span>
<ul>
<li><span data-ttu-id="b04f3-144">システム診断</span><span class="sxs-lookup"><span data-stu-id="b04f3-144">System diagnostics</span></span></li>
<li><span data-ttu-id="b04f3-145">問題検索</span><span class="sxs-lookup"><span data-stu-id="b04f3-145">Issue search</span></span></li>
<li><span data-ttu-id="b04f3-146">クラウドを利用したサポート</span><span class="sxs-lookup"><span data-stu-id="b04f3-146">Cloud-powered support</span></span></li>
<li><span data-ttu-id="b04f3-147">更新</span><span class="sxs-lookup"><span data-stu-id="b04f3-147">Updates</span></span></li>
<li><span data-ttu-id="b04f3-148">クラウド ホスト環境</span><span class="sxs-lookup"><span data-stu-id="b04f3-148">Cloud-hosted environments</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b04f3-149">1 つのプロジェクトのセキュリティをコンフィギュレーションした後は、別のプロジェクトにユーザーをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-149">After you've configured security for one project, you can import the users to another project.</span></span>

## <a name="configure-implementation-roles"></a><span data-ttu-id="b04f3-150">実装ロールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b04f3-150">Configure implementation roles</span></span> 
<span data-ttu-id="b04f3-151">実装プロジェクトがある場合、プロジェクト ユーザーの実装ロールを指定するためのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b04f3-151">If you have an implementation project, you will have the option to specify project user's implementation roles.</span></span> <span data-ttu-id="b04f3-152">詳細については、[Dynamics 365 実装のロール](/learn/modules/get-started-implementation-project/01-2-roles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b04f3-152">For more information, see [Roles in a Dynamics 365 implementation](/learn/modules/get-started-implementation-project/01-2-roles).</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
