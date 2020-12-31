---
title: セキュリティ アークテクチャ
description: このトピックでは、Finance and Operations のセキュリティ アーキテクチャの概要を提供します。
author: Peakerbl
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysSecConfiguration, SysUserGroupInfo, SysSecRoleExcludeUsers
audience: IT Pro
ms.reviewer: sericks
ms.custom: 15441
ms.assetid: bea829b3-38ce-463c-a7e3-c9393b79d559
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34997cf31ca2d0b4b628d71e3960bd3511246a65
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686307"
---
# <a name="security-architecture"></a><span data-ttu-id="16bde-103">セキュリティ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="16bde-103">Security architecture</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="16bde-104">このトピックでは、Finance and Operations のセキュリティ アーキテクチャの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="16bde-104">This topic provides an overview of the security architecture of Finance and Operations.</span></span>

<span data-ttu-id="16bde-105">セキュリティ アーキテクチャを理解すると、業務の要件に合わせてセキュリティを容易にカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="16bde-105">When you understand the security architecture, you can more easily customize security to fit the requirements of your business.</span></span> <span data-ttu-id="16bde-106">次の図は、セキュリティ アーキテクチャの高レベルな概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="16bde-106">The following diagram provides a high-level overview of the security architecture.</span></span> 

<span data-ttu-id="16bde-107">[![セキュリティ アークテクチャの概要を示す図](./media/security-architecture.png)](./media/security-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="16bde-107">[![Diagram showing overview of security architecture](./media/security-architecture.png)](./media/security-architecture.png)</span></span>

## <a name="authentication"></a><span data-ttu-id="16bde-108">認証</span><span class="sxs-lookup"><span data-stu-id="16bde-108">Authentication</span></span>
<span data-ttu-id="16bde-109">既定では、ユーザー権利を持つ認証済みユーザーのみが接続を確立できます。</span><span class="sxs-lookup"><span data-stu-id="16bde-109">By default, only authenticated users who have user rights can establish a connection.</span></span> 

<span data-ttu-id="16bde-110">Microsoft Azure Active Directory (AAD) は主要な ID プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="16bde-110">Microsoft Azure Active Directory (AAD) is a primary identity provider.</span></span> <span data-ttu-id="16bde-111">システムにアクセスするには、ユーザーは Finance and Operations インスタンスにプロビジョニングされ、認可されたテナントに有効な AAD アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="16bde-111">To access the system, users must be provisioned into a Finance and Operations instance and should have a valid AAD account in an authorized tenant.</span></span>

## <a name="authorization"></a><span data-ttu-id="16bde-112">認証</span><span class="sxs-lookup"><span data-stu-id="16bde-112">Authorization</span></span>
<span data-ttu-id="16bde-113">承認とは、Finance and Operations アプリケーションへのアクセスを制御することです。</span><span class="sxs-lookup"><span data-stu-id="16bde-113">Authorization is the control of access to Finance and Operations applications.</span></span> <span data-ttu-id="16bde-114">セキュリティ アクセス許可は、メニュー、メニュー項目、アクションおよびコマンド ボタン、レポート、サービス操作、Web URL のメニュー項目、Web コントロール、および Finance and Operations クライアントのフィールドなどのプログラムの個々の要素へのアクセスを制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-114">Security permissions are used to control access to individual elements of the program: menus, menu items, action and command buttons, reports, service operations, web URL menu items, web controls, and fields in the Finance and Operations client.</span></span> 

<span data-ttu-id="16bde-115">個別のセキュリティ アクセス許可は特権に、特権は職務に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="16bde-115">Individual security permissions are combined into privileges, and privileges are combined into duties.</span></span> <span data-ttu-id="16bde-116">管理者は、セキュリティ ロールに職務権限と権限を割り当てることにより、これらのセキュリティ ロールへのアクセス許可をプログラムに付与します。</span><span class="sxs-lookup"><span data-stu-id="16bde-116">The administrator grants security roles access to the program by assigning duties and privileges to those roles.</span></span> 

<span data-ttu-id="16bde-117">コンテキスト ベースのセキュリティは、セキュリティ設定が可能なオブジェクトへのアクセスをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="16bde-117">Context-based security controls access to securable objects.</span></span> <span data-ttu-id="16bde-118">特権がエントリ ポイント (メニュー項目またはサービス操作など) に関連付けられているとき、**読み取り** または **削除** などのアクセス レベルが指定されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-118">When a privilege is associated with an entry point (such as a menu item or a service operation), a level of access, such as **Read** or **Delete**, is specified.</span></span> <span data-ttu-id="16bde-119">承認サブシステムは、そのエントリ ポイントにアクセスがあると実行時にアクセスを検出し、エントリ ポイントが導かれるセキュリティ保護可能なオブジェクトに指定したレベルのアクセスを適用します。</span><span class="sxs-lookup"><span data-stu-id="16bde-119">The authorization subsystem detects the access at run time, when that entry point is accessed, and applies the specified level of access to the securable object that the entry point leads to.</span></span> <span data-ttu-id="16bde-120">この機能は、過剰なアクセス権がないことを保証し、開発者が意図したアクセス権を得るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="16bde-120">This functionality helps to ensure that there is no over-permissioning, and the developer gets the access that was intended.</span></span> 

<span data-ttu-id="16bde-121">詳細については、[ロールベース セキュリティ](role-based-security.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16bde-121">For more information, see [Role-based security](role-based-security.md).</span></span>

## <a name="data-security"></a><span data-ttu-id="16bde-122">データ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="16bde-122">Data security</span></span>
<span data-ttu-id="16bde-123">承認はプログラムの要素へのアクセスを許可するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-123">Authorization is used to grant access to elements of the program.</span></span> <span data-ttu-id="16bde-124">対照的に、データ セキュリティはデータベース内のテーブル、フィールド、および行へのアクセスを拒否するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-124">By contrast, data security is used to deny access to tables, fields, and rows in the database.</span></span>

<span data-ttu-id="16bde-125">拡張可能なデータ セキュリティ フレームワークを使用してセキュリティ ポリシーに基づいてテーブル レコードへのアクセスを制限することにより、ロールベースのセキュリティを補うことができます。</span><span class="sxs-lookup"><span data-stu-id="16bde-125">Use the extensible data security framework to supplement role-based security by restricting access to table records based on security policies.</span></span> <span data-ttu-id="16bde-126">セキュリティ アクセス許可がユーザー ロールの一部である場合、ユーザーがデータにアクセスできる割合が高くなりますが、セキュリティ ポリシーによってデータへのアクセスが減少します。</span><span class="sxs-lookup"><span data-stu-id="16bde-126">A security permission, as part of a user role, increases the access a user has to data, while a security policy decreases access to data.</span></span>

<span data-ttu-id="16bde-127">詳細については、[拡張可能なデータ セキュリティ ポリシー](extensible-data-security-policies.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16bde-127">For more information, see [Extensible data security policies](extensible-data-security-policies.md).</span></span>

<span data-ttu-id="16bde-128">また、テーブル アクセス許可フレームワークは、一部のデータを保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="16bde-128">Additionally, the Table Permissions Framework helps protect some data.</span></span> <span data-ttu-id="16bde-129">特定のテーブルのデータ セキュリティは、Application Object Server (AOS) によって適用されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-129">Data security for specific tables is enforced by Application Object Server (AOS).</span></span>

## <a name="auditing"></a><span data-ttu-id="16bde-130">監査</span><span class="sxs-lookup"><span data-stu-id="16bde-130">Auditing</span></span>
<span data-ttu-id="16bde-131">ユーザー サインインとサインアウトの監査が有効になります。つまり、ユーザーがアプリケーションからサインインまたはサインアウトするときにシステムに記録されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="16bde-131">Auditing of user sign in and sign out is enabled, which means that the system logs when a user signs in or out of the application.</span></span> <span data-ttu-id="16bde-132">ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。</span><span class="sxs-lookup"><span data-stu-id="16bde-132">A sign out is logged even if the user's session expires or ends.</span></span>

<span data-ttu-id="16bde-133">システム管理者またはセキュリティー管理者は、**ユーザー ログ** ページ (**システム管理** > **照会** > **ユーザー ログ**) に移動して監査ログにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="16bde-133">A system administrator or security administrator can access the audit logs by going to  the **User log** page (**System administration** > **Inquiries** > **User log**).</span></span>
