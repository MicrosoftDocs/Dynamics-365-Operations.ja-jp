---
title: E コマース ユーザーとロールの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトの作成環境へのアクセスをユーザーに許可する方法について説明します。
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b02f262136c0d970ca9eee3e5e63ef6dc8ccb7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794286"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="556c6-103">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="556c6-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="556c6-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトの作成環境へのアクセスをユーザーに許可する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="556c6-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="556c6-105">ユーザーのアクセスを制御し、特定のタスクを実行するためのアクセス許可をユーザーに付与するために、サイトの作成環境では、Microsoft Azure Active Directory (Azure AD) で作成したセキュリティ グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="556c6-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="556c6-106">最初に、Azure AD の新規または既存のセキュリティ グループを作成環境の各ロールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="556c6-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="556c6-107">その後、個々のユーザーを適切なセキュリティ グループに追加するか、そこから削除することにより、個々のユーザーにアクセス許可を付与または削除することができます。</span><span class="sxs-lookup"><span data-stu-id="556c6-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="556c6-108">作成環境でのロールの概要</span><span class="sxs-lookup"><span data-stu-id="556c6-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="556c6-109">Dynamics 365 for Commerce 作成環境では、次のロールがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="556c6-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="556c6-110">役割</span><span class="sxs-lookup"><span data-stu-id="556c6-110">Role</span></span>                 | <span data-ttu-id="556c6-111">説明</span><span class="sxs-lookup"><span data-stu-id="556c6-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="556c6-112">システム管理者</span><span class="sxs-lookup"><span data-stu-id="556c6-112">System Administrator</span></span> | <span data-ttu-id="556c6-113">このロールを持つユーザーには、すべてのツール、および評価とレビューに対する権限が与えられます。</span><span class="sxs-lookup"><span data-stu-id="556c6-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="556c6-114">また、サイトを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="556c6-114">They can also create sites.</span></span> |
| <span data-ttu-id="556c6-115">管理者</span><span class="sxs-lookup"><span data-stu-id="556c6-115">Administrator</span></span>   | <span data-ttu-id="556c6-116">このロールを持つユーザーは、特定のサイト構造内のすべてのツールおよび RnR に対する権限が与えられます。</span><span class="sxs-lookup"><span data-stu-id="556c6-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="556c6-117">Web プロデューサー</span><span class="sxs-lookup"><span data-stu-id="556c6-117">Web Producer</span></span>         | <span data-ttu-id="556c6-118">このロールを持つユーザーは、ページ、フラグメント、テンプレートを作成し、資産をアップロードおよび管理し、製品とカテゴリを拡充することができます。</span><span class="sxs-lookup"><span data-stu-id="556c6-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="556c6-119">リーダー</span><span class="sxs-lookup"><span data-stu-id="556c6-119">Reader</span></span>               | <span data-ttu-id="556c6-120">このロールを持つユーザーは、ページ、テンプレート、資産、フラグメント、レイアウト、および設定を表示できますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="556c6-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="556c6-121">RnR モデレーター</span><span class="sxs-lookup"><span data-stu-id="556c6-121">RnR Moderator</span></span>        | <span data-ttu-id="556c6-122">このロールを持つユーザーは、製品レビューを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="556c6-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="556c6-123">システム管理者ロール</span><span class="sxs-lookup"><span data-stu-id="556c6-123">System Administrator role</span></span>

<span data-ttu-id="556c6-124">Microsoft Dynamics Lifecycle Services (LCS) 環境で Dynamics 365 Commerce をプロビジョニングする場合、**システム管理者** ロールのセキュリティ グループを提供するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="556c6-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="556c6-125">このロールは、構成している環境で作成したすべてのサイトに自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="556c6-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="556c6-126">このロールのセキュリティ グループは、LCS でのみ更新できます。</span><span class="sxs-lookup"><span data-stu-id="556c6-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="556c6-127">すべてのサイトの **サイトの管理** ページで読み取り専用として表示され、情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="556c6-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="556c6-128">管理者ロール</span><span class="sxs-lookup"><span data-stu-id="556c6-128">Administrator role</span></span>

<span data-ttu-id="556c6-129">コマースで新しいサイトを作成すると、**管理者** ロールのセキュリティ グループを提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="556c6-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="556c6-130">このロールが付与するアクセス許可の概要については、このトピックの前の部分で示した表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="556c6-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="556c6-131">セキュリティグループの追加または更新</span><span class="sxs-lookup"><span data-stu-id="556c6-131">Add or update security groups</span></span>

<span data-ttu-id="556c6-132">サイトの作成後、**システム管理者** および **管理者** のロールに関連付けられているセキュリティ グループ内のユーザーのみが、そのサイトの作成環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="556c6-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="556c6-133">ユーザーを **Web プロデューサー**、**RnR モデレーター**、および **リーダー** のロールに割り当てるには、これらのロールにセキュリティ グループを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="556c6-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="556c6-134">セキュリティ グループをロールに追加したり、ロールに現在割り当てられているセキュリティ グループを更新したりするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="556c6-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="556c6-135">更新するサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="556c6-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="556c6-136">**サイト管理** で、**セキュリティ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="556c6-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="556c6-137">変更するロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="556c6-137">Select the role to modify.</span></span>
1. <span data-ttu-id="556c6-138">セキュリティ グループをロールに追加するか、ロールからセキュリティ グループを削除します。</span><span class="sxs-lookup"><span data-stu-id="556c6-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="556c6-139">追加リソース</span><span class="sxs-lookup"><span data-stu-id="556c6-139">Additional resources</span></span>

[<span data-ttu-id="556c6-140">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="556c6-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="556c6-141">サイトにおける検索エンジン最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="556c6-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="556c6-142">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="556c6-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]