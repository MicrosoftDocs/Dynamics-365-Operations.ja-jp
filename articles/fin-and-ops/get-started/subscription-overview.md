---
title: "サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問"
description: "このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。"
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: e3a5eda1f219a9e1c0ee448864ec3763f9fe155f
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="subscriptions-lcs-projects-and-azure-active-directory-tenants-faq"></a><span data-ttu-id="c29d8-103">サブスクリプション、LCS プロジェクト、および Azure Active Directory テナントに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c29d8-103">Subscriptions, LCS projects, and Azure Active Directory tenants FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c29d8-104">顧客は、マイクロソフト ボリューム ライセンス契約またはマイクロソフト クラウド ソリューション プロバイダー (CSP) 契約を通じて、 Microsoft Dynamics 365 for Finance and Operations に加入すると、Microsoft Azure Active Directory (Azure AD) テナント、Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトと、顧客が選択した 1 つのデータ センターに配備された任意の数のサンドボックス環境と、Finance and Operations の 1 つの実働インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="c29d8-104">When customers subscribe to Microsoft Dynamics 365 for Finance and Operations through a Microsoft Volume Licensing agreement or a Microsoft Cloud Solution Provider (CSP) agreement, they usually have one Microsoft Azure Active Directory (Azure AD) tenant, one Microsoft Dynamics Lifecycle Services (LCS) Implementation project and any number of sandbox environments that are deployed to one data center of the customer's choice, and one production instance of Finance and Operations.</span></span> <span data-ttu-id="c29d8-105">これらのコア概念の詳細については、[Finance and operations アーキテクチャの概要](../imp-lifecycle/architecture-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c29d8-105">For more information about these core concepts, see [Finance and operations architecture overview](../imp-lifecycle/architecture-overview.md).</span></span> <span data-ttu-id="c29d8-106">この設定は、ほとんどのプロジェクトで適切に動作しますが、さらに高度なシナリオが必要な場合もあります。または、導入ライフサイクル中の変更に対応する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-106">Although this setup works well for most projects, more advanced scenarios are sometimes required, or changes during the implementation lifecycle must be accommodated.</span></span>

<span data-ttu-id="c29d8-107">このトピックでは、定期売買およびライセンス、Azure AD テナントおよび LCS 実装プロジェクトに関するよく寄せられる質問に対する回答を提供します。</span><span class="sxs-lookup"><span data-stu-id="c29d8-107">This topic provides answers to frequently asked questions about subscriptions and licenses, Azure AD tenants, and LCS Implementation projects.</span></span>

<span data-ttu-id="c29d8-108">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c29d8-108">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c29d8-109">データ センター間で環境を移動する</span><span class="sxs-lookup"><span data-stu-id="c29d8-109">Move environments between data centers</span></span>](move-environments-data-center.md)
- [<span data-ttu-id="c29d8-110">契約タイプ間でライセンスを移動する</span><span class="sxs-lookup"><span data-stu-id="c29d8-110">Move licenses between agreement types</span></span>](move-licenses-between-agreement-types.md)
- [<span data-ttu-id="c29d8-111">LCS 実装プロジェクトを別の Azure Active Directory テナントに移動する</span><span class="sxs-lookup"><span data-stu-id="c29d8-111">Move an LCS Implementation project to another Azure Active Directory tenant</span></span>](move-lcs-implementation-project-tenant.md)
- [<span data-ttu-id="c29d8-112">複数の LCS プロジェクトと本番環境を同じ Azure Active Directory テナント上に実装する</span><span class="sxs-lookup"><span data-stu-id="c29d8-112">Implement multiple LCS projects and production environments on the same Azure Active Directory tenant</span></span>](implement-multiple-projects-aad-tenant.md)

## <a name="do-i-have-to-move-azure-ad-tenants-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="c29d8-113">CSP 契約からボリューム ライセンス契約に移行する際、Azure AD テナントを移行する必要がありますか？</span><span class="sxs-lookup"><span data-stu-id="c29d8-113">Do I have to move Azure AD tenants when I move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="c29d8-114">一連番号</span><span class="sxs-lookup"><span data-stu-id="c29d8-114">No.</span></span> <span data-ttu-id="c29d8-115">既存の Azure AD テナントを維持できますが、ボリューム ライセンスのサブスクリプションは CSP サブスクリプションと同じ Azure AD テナントに対して行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-115">You can keep the existing Azure AD tenant, but you must make sure that the Volume Licensing subscriptions are purchased against the same Azure AD tenant as the CSP subscriptions.</span></span>

## <a name="do-i-get-a-new-lcs-implementation-project-when-i-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="c29d8-116">CSP 契約からボリューム ライセンス契約に移行した際、新しい LCS 実装プロジェクトを取得しますか？</span><span class="sxs-lookup"><span data-stu-id="c29d8-116">Do I get a new LCS Implementation project when I move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="c29d8-117">一連番号</span><span class="sxs-lookup"><span data-stu-id="c29d8-117">No.</span></span> <span data-ttu-id="c29d8-118">LCS プロジェクトは変わりません。</span><span class="sxs-lookup"><span data-stu-id="c29d8-118">The LCS project remains the same.</span></span>

## <a name="can-i-keep-the-existing-lcs-implementation-project-when-i-move-to-different-azure-ad-tenant"></a><span data-ttu-id="c29d8-119">異なる Azure AD テナントに移動する際、既存の LCS 実装プロジェクトを維持することはできますか？</span><span class="sxs-lookup"><span data-stu-id="c29d8-119">Can I keep the existing LCS Implementation project when I move to different Azure AD tenant?</span></span>

<span data-ttu-id="c29d8-120">一連番号</span><span class="sxs-lookup"><span data-stu-id="c29d8-120">No.</span></span> <span data-ttu-id="c29d8-121">新しい LCS プロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c29d8-121">A new LCS project will be created.</span></span>

## <a name="how-long-does-it-take-to-move-from-a-csp-agreement-to-a-volume-licensing-agreement"></a><span data-ttu-id="c29d8-122">CSP 契約からボリューム ライセンス契約に移行するには、どのくらいの時間がかかりますか？</span><span class="sxs-lookup"><span data-stu-id="c29d8-122">How long does it take to move from a CSP agreement to a Volume Licensing agreement?</span></span>

<span data-ttu-id="c29d8-123">ボリューム ライセンスの購入では、注文の処理と定期売買の有効化に数日かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-123">For a Volume Licensing purchase, it can take a few days for the order to be processed and the subscriptions to be activated.</span></span> <span data-ttu-id="c29d8-124">アドオン環境の再配置には、2 営業日のサービス レベル契約 (SLA) があります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-124">Redeployment of add-on environments has a service level agreement (SLA) of two business days.</span></span> <span data-ttu-id="c29d8-125">古いアドオン環境を割り当て解除し削除するには数時間かかります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-125">It takes a few hours to deallocate and delete old add-on environments.</span></span>

## <a name="what-if-i-forget-to-delete-the-existing-environments-before-i-suspend-the-existing-subscription"></a><span data-ttu-id="c29d8-126">既存のサブスクリプションを一時停止する前に既存の環境を削除するのを忘れた場合はどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="c29d8-126">What if I forget to delete the existing environments before I suspend the existing subscription?</span></span>

<span data-ttu-id="c29d8-127">サブスクリプションを中断する前に、既存の環境の割り当てを解除して削除しないと、環境は**配置済み**状態のままになります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-127">If you don't deallocate and delete the existing environments before you suspend the subscriptions, the environments will remain in a **Deployed** state.</span></span> <span data-ttu-id="c29d8-128">ただし、これらの環境の全詳細にアクセスしようとすると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c29d8-128">However, if you try to access the full details of these environments, you will receive an error message.</span></span>

## <a name="can-i-have-a-csp-agreement-and-a-volume-licensing-agreement-in-parallel"></a><span data-ttu-id="c29d8-129">CSP 契約とボリューム ライセンス契約を並行して締結することはできますか？</span><span class="sxs-lookup"><span data-stu-id="c29d8-129">Can I have a CSP agreement and a Volume Licensing agreement in parallel?</span></span>

<span data-ttu-id="c29d8-130">はい。</span><span class="sxs-lookup"><span data-stu-id="c29d8-130">Yes.</span></span> <span data-ttu-id="c29d8-131">ただし、各プログラムで必要なライセンスの最低限の数を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c29d8-131">However, you must maintain the minimum required number of licenses under each program.</span></span>

