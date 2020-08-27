---
title: サブスクリプション、LCS プロジェクト、Azure Active Directory テナントに関するよく寄せられる質問
description: このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 08/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: a4647afbab926b954de9283b58fb00827e0ae9ae
ms.sourcegitcommit: 47d77535aca36b9f98801cb00e5ad2ae1386b3b9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686581"
---
# <a name="subscriptions-lcs-projects-and-azure-active-directory-tenants-faq"></a><span data-ttu-id="ad2fa-103">サブスクリプション、LCS プロジェクト、Azure Active Directory テナントに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ad2fa-103">Subscriptions, LCS projects, and Azure Active Directory tenants FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad2fa-104">顧客が Microsoft ボリューム ライセンス契約または Microsoft クラウド ソリューション プロバイダー (CSP) 契約を通じて加入すると、通常、Microsoft Azure Active Directory (Azure AD) テナント、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクト、および任意の数のサンドボックス環境とがあります。それらは顧客が選択した 1 つのデータ センターおよび 1 つの実稼働環境に展開されています。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-104">When customers subscribe through a Microsoft Volume Licensing agreement or a Microsoft Cloud Solution Provider (CSP) agreement, they usually have one Microsoft Azure Active Directory (Azure AD) tenant, one Microsoft Dynamics Lifecycle Services (LCS) Implementation project and any number of sandbox environments that are deployed to one data center of the customer's choice, and one production environment.</span></span> <span data-ttu-id="ad2fa-105">これらのコア概念の詳細については、[Finance and Operations アプリケーション アーキテクチャ](../imp-lifecycle/architecture-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-105">For more information about these core concepts, see [Finance and Operations application architecture](../imp-lifecycle/architecture-overview.md).</span></span> <span data-ttu-id="ad2fa-106">この設定は、ほとんどのプロジェクトで適切に動作しますが、さらに高度なシナリオが必要な場合もあります。または、導入ライフサイクル中の変更に対応する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-106">Although this setup works well for most projects, more advanced scenarios are sometimes required, or changes during the implementation lifecycle must be accommodated.</span></span>

<span data-ttu-id="ad2fa-107">このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-107">This topic provides answers to frequently asked questions about subscriptions and licenses, Azure AD tenants, and LCS Implementation projects.</span></span>

<span data-ttu-id="ad2fa-108">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-108">For more information, see the following topics:</span></span>

- [<span data-ttu-id="ad2fa-109">データ センター間で環境を移動する</span><span class="sxs-lookup"><span data-stu-id="ad2fa-109">Move environments between data centers</span></span>](move-environments-data-center.md)
- [<span data-ttu-id="ad2fa-110">契約タイプ間でライセンスを移動する</span><span class="sxs-lookup"><span data-stu-id="ad2fa-110">Move licenses between agreement types</span></span>](move-licenses-between-agreement-types.md)
- [<span data-ttu-id="ad2fa-111">LCS 実装プロジェクトを別の Azure AD テナントに移動する</span><span class="sxs-lookup"><span data-stu-id="ad2fa-111">Move LCS implementation projects to different Azure AD tenants</span></span>](move-lcs-implementation-project-tenant.md)
- [<span data-ttu-id="ad2fa-112">1 つの Azure AD テナントにおける複数の LCS プロジェクトおよび実稼働環境</span><span class="sxs-lookup"><span data-stu-id="ad2fa-112">Multiple LCS projects and production environments on one Azure AD tenant</span></span>](implement-multiple-projects-aad-tenant.md)

## <a name="do-i-have-to-move-azure-ad-tenants-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="ad2fa-113">CSP 契約からボリューム ライセンス契約に移行する際、Azure AD テナントを移行する必要がありますか？</span><span class="sxs-lookup"><span data-stu-id="ad2fa-113">Do I have to move Azure AD tenants when I move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="ad2fa-114">一連番号</span><span class="sxs-lookup"><span data-stu-id="ad2fa-114">No.</span></span> <span data-ttu-id="ad2fa-115">既存の Azure AD テナントを維持できますが、ボリューム ライセンスのサブスクリプションは CSP サブスクリプションと同じ Azure AD テナントに対して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-115">You can keep the existing Azure AD tenant, but you must make sure that the Volume Licensing subscriptions are purchased against the same Azure AD tenant as the CSP subscriptions.</span></span>

## <a name="do-i-get-a-new-lcs-implementation-project-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="ad2fa-116">CSP 契約からボリューム ライセンス契約に移行した際、新しい LCS 実装プロジェクトを取得しますか？</span><span class="sxs-lookup"><span data-stu-id="ad2fa-116">Do I get a new LCS Implementation project when I move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="ad2fa-117">一連番号</span><span class="sxs-lookup"><span data-stu-id="ad2fa-117">No.</span></span> <span data-ttu-id="ad2fa-118">LCS プロジェクトは変わりません。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-118">The LCS project remains the same.</span></span>

## <a name="can-i-keep-the-existing-lcs-implementation-project-when-i-move-to-different-azure-ad-tenant"></a><span data-ttu-id="ad2fa-119">異なる Azure AD テナントに移動する際、既存の LCS 実装プロジェクトを維持することはできますか？</span><span class="sxs-lookup"><span data-stu-id="ad2fa-119">Can I keep the existing LCS Implementation project when I move to different Azure AD tenant?</span></span>

<span data-ttu-id="ad2fa-120">一連番号</span><span class="sxs-lookup"><span data-stu-id="ad2fa-120">No.</span></span> <span data-ttu-id="ad2fa-121">新しい LCS プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-121">A new LCS project will be created.</span></span>

## <a name="how-long-does-it-take-to-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="ad2fa-122">CSP 契約からボリューム ライセンス契約に移行するには、どのくらいの時間がかかりますか？</span><span class="sxs-lookup"><span data-stu-id="ad2fa-122">How long does it take to move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="ad2fa-123">ボリューム ライセンスの購入では、注文の処理と定期売買の有効化に数日かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-123">For a Volume Licensing purchase, it can take a few days for the order to be processed and the subscriptions to be activated.</span></span> <span data-ttu-id="ad2fa-124">アドオン環境の再配置には、2 営業日のサービス レベル契約 (SLA) があります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-124">Redeployment of add-on environments has a service level agreement (SLA) of two business days.</span></span> <span data-ttu-id="ad2fa-125">古いアドオン環境を割り当て解除し削除するには数時間かかります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-125">It takes a few hours to deallocate and delete old add-on environments.</span></span>

## <a name="what-if-i-forget-to-delete-the-existing-environments-before-i-suspend-the-existing-subscription"></a><span data-ttu-id="ad2fa-126">既存のサブスクリプションを一時停止する前に既存の環境を削除するのを忘れた場合はどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-126">What if I forget to delete the existing environments before I suspend the existing subscription?</span></span>

<span data-ttu-id="ad2fa-127">サブスクリプションを中断する前に、既存の環境の割り当てを解除して削除しないと、環境は**配置済み**状態のままになります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-127">If you don't deallocate and delete the existing environments before you suspend the subscriptions, the environments will remain in a **Deployed** state.</span></span> <span data-ttu-id="ad2fa-128">ただし、これらの環境の全詳細にアクセスしようとすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-128">However, if you try to access the full details of these environments, you will receive an error message.</span></span>

## <a name="can-i-have-a-csp-agreement-and-a-volume-licensing-agreement-in-parallel"></a><span data-ttu-id="ad2fa-129">CSP 契約とボリューム ライセンス契約を並行して締結することはできますか？</span><span class="sxs-lookup"><span data-stu-id="ad2fa-129">Can I have a CSP agreement and a Volume Licensing agreement in parallel?</span></span>

<span data-ttu-id="ad2fa-130">はい。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-130">Yes.</span></span> <span data-ttu-id="ad2fa-131">ただし、各プログラムで必要なライセンスの最低限の数を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-131">However, you must maintain the minimum required number of licenses under each program.</span></span>

## <a name="how-can-i-find-the-tenant-name-and-tenant-id-within-lcs"></a><span data-ttu-id="ad2fa-132">LCS 内のテナント名とテナント ID をどのように見つけますか?</span><span class="sxs-lookup"><span data-stu-id="ad2fa-132">How can I find the Tenant name and Tenant ID within LCS?</span></span>
1. <span data-ttu-id="ad2fa-133">LCS のプロジェクト ホーム ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-133">Go to project home page in LCS.</span></span>
2. <span data-ttu-id="ad2fa-134">**環境**セクションで、**利用可能なサブスクリプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-134">In the **Environments** section, select **Subscriptions available**.</span></span>
3. <span data-ttu-id="ad2fa-135">**利用可能なサブスクリプション** ページで、**テナント名**および**テナント ID** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-135">On the **Subscriptions available** page, you will find the **Tenant name** and the **Tenant ID**.</span></span>

## <a name="how-can-i-find-the-subscription-status"></a><span data-ttu-id="ad2fa-136">サブスクリプションのステータスをどのように見つけますか?</span><span class="sxs-lookup"><span data-stu-id="ad2fa-136">How can I find the subscription status?</span></span>
1. <span data-ttu-id="ad2fa-137">LCS のプロジェクト ホーム ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-137">Go to the project home page in LCS.</span></span>
2. <span data-ttu-id="ad2fa-138">**環境**セクションで、**利用可能なサブスクリプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-138">In the **Environments** section, select **Subscriptions available**.</span></span>
3. <span data-ttu-id="ad2fa-139">**利用可能なサブスクリプション**ページで、テナントへが利用できるすべての**サービス プラン**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-139">On the **Subscriptions available** page, you’ll find all **Service plans** available to the tenant.</span></span>  
4. <span data-ttu-id="ad2fa-140">**割り当てられた日**は、サービス プランのステータスが変更された日付を示します。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-140">The **Assigned date** indicates the date that service plan status was changed.</span></span> 

## <a name="how-would-the-subscription-status-impact-the-environment"></a><span data-ttu-id="ad2fa-141">サブスクリプション ステータスは環境にどのように影響しますか?</span><span class="sxs-lookup"><span data-stu-id="ad2fa-141">How would the subscription status impact the environment?</span></span>
<span data-ttu-id="ad2fa-142">環境の操作の一部は、次のサブスクリプション ステータスにより影響を受ける可能性があります:</span><span class="sxs-lookup"><span data-stu-id="ad2fa-142">Some of the environment's operations may be impacted by the subscription status:</span></span>
- <span data-ttu-id="ad2fa-143">**有効** - サブスクリプションは稼働状態です。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-143">**Active** - Your subscription is in an operative state.</span></span> <span data-ttu-id="ad2fa-144">すべての環境操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-144">You should be able to perform all environment operations.</span></span> 
- <span data-ttu-id="ad2fa-145">**支払猶予期間** - サブスクリプションの期限が切れていますが、支払猶予期間内です。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-145">**In Grace Period** - Your subscription has expired, but is within the grace period.</span></span> <span data-ttu-id="ad2fa-146">今すぐサブスクリプションを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-146">You should renew your subscription soon.</span></span> <span data-ttu-id="ad2fa-147">サブスクリプション ステータスは、ライセンス数、新しい環境の展開機能、または環境操作の実行機能には影響しません。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-147">The subscription status won’t impact your license quantity, ability to deploy a new environment, or to perform environment operations.</span></span>
- <span data-ttu-id="ad2fa-148">**中断** - サブスクリプションが支払猶予期間を過ぎて期限切れになりました。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-148">**Suspended** - Your subscription has expired beyond the grace period.</span></span> <span data-ttu-id="ad2fa-149">このサブスクリプション ステータスはライセンス数を削減し、新しい環境の展開機能、または環境操作の実行機能に影響を与える場合があります。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-149">This subscription status may reduce the license quantity, impact your ability to deploy a new environment, or impact your ability to perform environment operations.</span></span> 
- <span data-ttu-id="ad2fa-150">**削除済** - サブスクリプションは削除されました。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-150">**Deleted** - Your subscription has been deleted.</span></span> <span data-ttu-id="ad2fa-151">これにより、新しい環境を展開したり環境操作を実行したりする機能に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="ad2fa-151">This will impact your ability to deploy a new environment or perform environment operations.</span></span>  

