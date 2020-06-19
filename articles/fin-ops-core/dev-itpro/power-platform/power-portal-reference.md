---
title: Power Apps ポータルと Finance and Operations
description: このトピックでは、Power Apps ポータルを Finance and Operations で使用する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 40b13941d0f471a0aa1682d262c0c336a966716b
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416542"
---
# <a name="power-apps-portals-with-finance-and-operations"></a><span data-ttu-id="96943-103">Power Apps ポータルと Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="96943-103">Power Apps portals with Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="96943-104">この機能を使用するには、Common Data Service のサービス更新プログラム 189 が必要です。</span><span class="sxs-lookup"><span data-stu-id="96943-104">This functionality requires service update 189 for Common Data Service.</span></span> <span data-ttu-id="96943-105">Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。</span><span class="sxs-lookup"><span data-stu-id="96943-105">The release information for Common Data Service is published on the [latest version availability page](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability).</span></span>

<span data-ttu-id="96943-106">Power Apps ポータルでは、Common Data Service の仮想エンティティとして使用できる Finance and Operations エンティティに対して、作成、更新、および削除 (CRUD) 操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="96943-106">Power Apps portals will enable create, update, and delete (CRUD) operations to Finance and Operations entities that are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="96943-107">このトピックでは、Finance and Operations アプリの Power Apps ポータルに実装されているシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96943-107">This topic explains the scenarios that are implemented in Power Apps portals for Finance and Operations apps.</span></span>

## <a name="anonymous-access-from-power-apps-portals"></a><span data-ttu-id="96943-108">Power Apps ポータルからの匿名アクセス</span><span class="sxs-lookup"><span data-stu-id="96943-108">Anonymous access from Power Apps portals</span></span>

<span data-ttu-id="96943-109">Finance and Operations の入札やオンボードなどの業務プロセスのコラボレーション シナリオは、外部ユーザーが Finance and Operations アプリのユーザーではない場合でも、Power Apps ポータルからの参加を要求します。</span><span class="sxs-lookup"><span data-stu-id="96943-109">Collaboration scenarios in business processes such as bidding or onboarding of prospects in Finance and Operations require that external users participate from the Power Apps portal, even though they aren't users in Finance and Operations apps.</span></span> <span data-ttu-id="96943-110">匿名アクセスは、Finance and Operations アプリ ユーザーではないユーザーがログインしなくてもよいので、このような状況では匿名アクセスのシンプルさが魅力的です。</span><span class="sxs-lookup"><span data-stu-id="96943-110">The simplicity of anonymous access is appealing in these types of scenarios because the users, who might not be Finance and Operations apps users, don't have to sign in.</span></span> <span data-ttu-id="96943-111">ただし、業務プロセス内の意味のあるタスクを完了するために、Finance and Operations で CRUD 処理を実行することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="96943-111">However, they are expected to perform CRUD operations in Finance and Operations to complete any meaningful tasks in the business processes.</span></span>

<span data-ttu-id="96943-112">必要なエンティティのみが匿名アクセスに対して有効になるようにするには、Finance and Operations のユーザーが匿名アクセスに使用するユーザーとして指定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="96943-112">To ensure that only the required entities are enabled for anonymous access, a user in Finance and Operations must be designated as the user who is used for anonymous access.</span></span> <span data-ttu-id="96943-113">この指定は、**システム パラメーター** ページ (**システム管理 \> システム パラメーター**) の **仮想エンティティ** タブにある **匿名ポータルのアクセス ユーザー ID** フィールドで構成します。</span><span class="sxs-lookup"><span data-stu-id="96943-113">This designation is configured in the **Anonymous portal access user ID** field on the **Virtual entity** tab on the **System parameters** page (**System administration \> System parameters**).</span></span> <span data-ttu-id="96943-114">指定されたユーザーを職務とセキュリティ ロールに割り当てて、Power Portal から匿名でやりとりするすべてのユーザーが使用できるようにする必要がある特定のデータへのアクセスを制御することができます。</span><span class="sxs-lookup"><span data-stu-id="96943-114">The designated user can then be assigned to duties and security roles to control access to specific data that must be made available to all users who will interact anonymously from the Power Portal.</span></span>

<span data-ttu-id="96943-115">このシナリオには匿名アクセスが含まれるため、セキュリティの観点から、**匿名ポータルのアクセス ユーザー ID** フィールドで指定されているユーザーにのみ、重要なユーザー コンテキストがあります。</span><span class="sxs-lookup"><span data-stu-id="96943-115">Note that because this scenario involves anonymous access, the only user context that matters, from a security perspective, is the user who is designated in the **Anonymous portal access user ID** field.</span></span>

## <a name="authenticated-access-from-power-apps-portals"></a><span data-ttu-id="96943-116">Power Apps ポータルからの認証済みアクセス</span><span class="sxs-lookup"><span data-stu-id="96943-116">Authenticated access from Power Apps portals</span></span>

<span data-ttu-id="96943-117">Power Apps ポータルから Finance and Operations へのユーザーアクセスを完全に認証することによって、Finance and Operations のユーザーが Power Apps ポータルからも操作できるようにします。</span><span class="sxs-lookup"><span data-stu-id="96943-117">Fully authenticated user access from Power Apps portals to Finance and Operations lets users in Finance and Operations also interact from Power Apps portals.</span></span> <span data-ttu-id="96943-118">Power Apps ポータルにサインインするユーザーは、適切なセキュリティ ロールを持つ Finance and Operations のユーザーであることもわかっています。</span><span class="sxs-lookup"><span data-stu-id="96943-118">A user who signs in to the Power Apps portal is also a known user in Finance and Operations who has appropriate security roles.</span></span> <span data-ttu-id="96943-119">Finance and Operations の業務プロセスにおける既存の役割は、Power Portal でこのタイプの認証されたユーザーに対するセキュリティ アクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="96943-119">The existing roles from the business process in Finance and Operations govern the security access for this type of authenticated user in the Power Portal.</span></span>

<span data-ttu-id="96943-120">Power Apps ポータル認証は Common Data Service の連絡先エンティティにリンクされているため、Common Data Service の連絡先と Finance and Operations の対応するユーザーの間にマッピングを確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96943-120">Because Power Apps portals authentication is linked to the Contacts entity in Common Data Service, a mapping must be established between the Common Data Service contact and the corresponding user in Finance and Operations.</span></span> <span data-ttu-id="96943-121">このマッピングは、エントリを **msdyn\_externalportalusermapping** エンティティに追加することによって実行できます。</span><span class="sxs-lookup"><span data-stu-id="96943-121">This mapping can be done by adding entries to the **msdyn\_externalportalusermapping** entity.</span></span> <span data-ttu-id="96943-122">セキュリティの観点から、認証されたユーザーが使用できる仮想エンティティの範囲は、Power Apps ポータルで **グローバル** としてコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96943-122">From a security perspective, the scope of virtual entities that are made available to authenticated users must be configured as **Global** in the Power Apps portal.</span></span>

<span data-ttu-id="96943-123">別のテナントから認証されたユーザーをユーザーとして Finance and Operations に追加する必要がある場合、Finance and Operations で[新しいユーザーの作成](../sysadmin/tasks/create-new-users.md)プロセスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96943-123">When authenticated users from a different tenant need to be added to Finance and Operations as users, you must use the [Create new user](../sysadmin/tasks/create-new-users.md) process in Finance and Operations.</span></span> <span data-ttu-id="96943-124">このプロセスにより、Microsoft Azure Active Directory (Azure AD) 企業間 (B2B) ゲスト ユーザーとして、テナント間のユーザーが追加されます。</span><span class="sxs-lookup"><span data-stu-id="96943-124">This process adds cross-tenant users as Microsoft Azure Active Directory (Azure AD) business-to-business (B2B) guest users.</span></span>
