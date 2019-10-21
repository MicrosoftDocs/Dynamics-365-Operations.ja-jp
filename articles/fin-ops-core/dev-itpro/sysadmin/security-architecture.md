---
title: セキュリティ アークテクチャ
description: このトピックでは、Finance and Operations のセキュリティ アーキテクチャの概要を示します。
author: sarvanisathish
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysSecConfiguration, SysUserGroupInfo, SysSecRoleExcludeUsers
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15441
ms.assetid: bea829b3-38ce-463c-a7e3-c9393b79d559
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aea02328d187a1d0804871f59ef46a3ead7bd4f9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191794"
---
# <a name="security-architecture"></a><span data-ttu-id="2de8a-103">セキュリティ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="2de8a-103">Security architecture</span></span>
[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="2de8a-104">このトピックでは、Finance and Operations のセキュリティ アーキテクチャの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="2de8a-104">This topic provides an overview of the security architecture of Finance and Operations.</span></span>

<span data-ttu-id="2de8a-105">セキュリティ アーキテクチャを理解すると、業務の要件に合わせてセキュリティを容易にカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-105">When you understand the security architecture, you can more easily customize security to fit the requirements of your business.</span></span> <span data-ttu-id="2de8a-106">次の図は、セキュリティ アーキテクチャの高レベルな概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="2de8a-106">The following diagram provides a high-level overview of the security architecture.</span></span> 

<span data-ttu-id="2de8a-107">[![security-architecture](./media/security-architecture.png)](./media/security-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="2de8a-107">[![security-architecture](./media/security-architecture.png)](./media/security-architecture.png)</span></span>

## <a name="authentication"></a><span data-ttu-id="2de8a-108">認証</span><span class="sxs-lookup"><span data-stu-id="2de8a-108">Authentication</span></span>
<span data-ttu-id="2de8a-109">既定では、ユーザー権利を持つ認証済みユーザーのみが接続を確立できます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-109">By default, only authenticated users who have user rights can establish a connection.</span></span> 

<span data-ttu-id="2de8a-110">Microsoft Azure Active Directory (AAD) は主要な ID プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="2de8a-110">Microsoft Azure Active Directory (AAD) is a primary identity provider.</span></span> <span data-ttu-id="2de8a-111">システムにアクセスするには、ユーザーは Finance and Operations インスタンスにプロビジョニングされ、認可されたテナントに有効な AAD アカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="2de8a-111">To access the system, users must be provisioned into a Finance and Operations instance and should have a valid AAD account in an authorized tenant.</span></span>

## <a name="authorization"></a><span data-ttu-id="2de8a-112">承認</span><span class="sxs-lookup"><span data-stu-id="2de8a-112">Authorization</span></span>
<span data-ttu-id="2de8a-113">承認は Finance and Operations アプリケーションへのアクセスをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="2de8a-113">Authorization is the control of access to Finance and Operations applications.</span></span> <span data-ttu-id="2de8a-114">セキュリティ アクセス許可は、プログラムの個々の要素へのアクセスを制御するために使用されます: メニュー、メニュー項目、アクションおよびコマンド ボタン、レポート、サービス操作、Web URL のメニュー項目、Web コントロール、および Finance and Operations クライアントのフィールド。</span><span class="sxs-lookup"><span data-stu-id="2de8a-114">Security permissions are used to control access to individual elements of the program: menus, menu items, action and command buttons, reports, service operations, web URL menu items, web controls, and fields in the Finance and Operations client.</span></span> 

<span data-ttu-id="2de8a-115">個別のセキュリティ アクセス許可は特権に、特権は職務に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="2de8a-115">Individual security permissions are combined into privileges, and privileges are combined into duties.</span></span> <span data-ttu-id="2de8a-116">管理者は、セキュリティ ロールに職務権限と権限を割り当てることにより、これらのセキュリティ ロールへのアクセス許可をプログラムに付与します。</span><span class="sxs-lookup"><span data-stu-id="2de8a-116">The administrator grants security roles access to the program by assigning duties and privileges to those roles.</span></span> 

<span data-ttu-id="2de8a-117">コンテキスト ベースのセキュリティは、セキュリティ設定が可能なオブジェクトへのアクセスをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="2de8a-117">Context-based security controls access to securable objects.</span></span> <span data-ttu-id="2de8a-118">特権がエントリ ポイント (メニュー項目またはサービス操作など) に関連付けられているとき、**読み取り** または **削除** などのアクセス レベルが指定されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-118">When a privilege is associated with an entry point (such as a menu item or a service operation), a level of access, such as **Read** or **Delete**, is specified.</span></span> <span data-ttu-id="2de8a-119">承認サブシステムは、そのエントリ ポイントにアクセスがあると実行時にアクセスを検出し、エントリ ポイントが導かれるセキュリティ保護可能なオブジェクトに指定したレベルのアクセスを適用します。</span><span class="sxs-lookup"><span data-stu-id="2de8a-119">The authorization subsystem detects the access at run time, when that entry point is accessed, and applies the specified level of access to the securable object that the entry point leads to.</span></span> <span data-ttu-id="2de8a-120">この機能は、過剰なアクセス権がないことを保証し、開発者が意図したアクセス権を得るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-120">This functionality helps to ensure that there is no over-permissioning, and the developer gets the access that he or she intended.</span></span> 

<span data-ttu-id="2de8a-121">詳細については、[ロールベース セキュリティ](role-based-security.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2de8a-121">For more information, see [Role-based security](role-based-security.md).</span></span>

## <a name="data-security"></a><span data-ttu-id="2de8a-122">データ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="2de8a-122">Data security</span></span>
<span data-ttu-id="2de8a-123">承認はプログラムの要素へのアクセスを許可するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-123">Authorization is used to grant access to elements of the program.</span></span> <span data-ttu-id="2de8a-124">対照的に、データ セキュリティはデータベース内のテーブル、フィールド、および行へのアクセスを拒否するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-124">By contrast, data security is used to deny access to tables, fields, and rows in the database.</span></span> 

<span data-ttu-id="2de8a-125">拡張可能なデータ セキュリティ フレームワークを使用して、データ セキュリティ ポリシーをセキュリティ ロールに割り当てることにより、トランザクション データへのアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="2de8a-125">Use the extensible data security framework to control access to transactional data by assigning data security policies to security roles.</span></span> <span data-ttu-id="2de8a-126">データ セキュリティ ポリシーは、有効な日付または営業担当地域や組織などのユーザー データに基づいて、データへのアクセスを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-126">Data security policies can restrict access to data, based on either the effective date or user data, such as the sales territory or organization.</span></span> 

<span data-ttu-id="2de8a-127">レコード レベル セキュリティ (Dynamics AX 2012 以前のバージョンのデータを保護するためのメカニズム) が古くなっています。</span><span class="sxs-lookup"><span data-stu-id="2de8a-127">Record-level security, which was a mechanism for securing data in Dynamics AX 2012 and earlier versions, is obsolete.</span></span> <span data-ttu-id="2de8a-128">プログラム内のデータを保護またはフィルター処理するには、拡張可能なデータ セキュリティが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-128">Extensible data security is the recommended mechanism for securing or filtering data in the program.</span></span> 

<span data-ttu-id="2de8a-129">また、テーブル アクセス許可フレームワークは、一部のデータを保護するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-129">Additionally, the Table Permissions Framework helps protect some data.</span></span> <span data-ttu-id="2de8a-130">特定のテーブルのデータ セキュリティは、Application Object Server (AOS) によって適用されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-130">Data security for specific tables is enforced by Application Object Server (AOS).</span></span>

## <a name="auditing"></a><span data-ttu-id="2de8a-131">監査</span><span class="sxs-lookup"><span data-stu-id="2de8a-131">Auditing</span></span>
<span data-ttu-id="2de8a-132">ユーザー サインインとサインアウトの監査が有効になります。つまり、ユーザーがアプリケーションからサインインまたはサインアウトするときにシステムに記録されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2de8a-132">Auditing of user sign in and sign out is enabled, which means that the system logs when a user signs in or out of the application.</span></span> <span data-ttu-id="2de8a-133">ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-133">A sign out is logged even if the user's session expires or ends.</span></span>

<span data-ttu-id="2de8a-134">システム管理者またはセキュリティー管理者は、**ユーザー ログ** ページ (**システム管理** > **照会** > **ユーザー ログ**) に移動して監査ログにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2de8a-134">A system administrator or security administrator can access the audit logs by going to  the **User log** page (**System administration** > **Inquiries** > **User log**).</span></span>
