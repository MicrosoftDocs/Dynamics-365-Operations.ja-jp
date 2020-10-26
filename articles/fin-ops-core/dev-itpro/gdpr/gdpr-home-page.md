---
title: GDPRデータの要求リソースに応答する
description: このトピックでは、Finance and Operations アプリ、およびその他の Dynamics 365 製品を使用する顧客として、一般データ保護規則 (GDPR) に基づくデータ権利要求への対応に役立つ情報へのリンクを提供します。
author: rschloma
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 10031
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53cc1c827d19f4da779eaef8c5f294d3b291bd8d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979654"
---
# <a name="respond-to-gdpr-data-requests-resources"></a><span data-ttu-id="e47bb-103">GDPR データ要求への応答のリソース</span><span class="sxs-lookup"><span data-stu-id="e47bb-103">Respond to GDPR data requests resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e47bb-104">このトピックでは、Dynamics 365 Finance、Supply Chain Management、コマース、人事管理、および Microsoft Dynamics AX 2012 を使用する顧客として、一般データ保護規制 (GDPR) に基づくデータ権利要求への対応に役立つ情報へのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="e47bb-104">This topic provides links to information that can help you respond to a request for information under the General Data Protection Regulation (GDPR) as a customer using Dynamics 365 Finance, Supply Chain Management, Commerce, Human Resources, and Microsoft Dynamics AX 2012.</span></span> 

<span data-ttu-id="e47bb-105">データの要求に応答する最初のステップは、通常、個人検索レポートを使用して、要求されるデータを特定することです。</span><span class="sxs-lookup"><span data-stu-id="e47bb-105">Your first step in responding to a request for data will usually be to use the Person search report to locate the data that's requested.</span></span> <span data-ttu-id="e47bb-106">場合によっては、他のレポートを使用したり、使用している製品で特定のページにアクセスしたり、個人検索レポートを拡張したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e47bb-106">In some cases, you might need to use other reports, access specific pages in the product that you're using, or extend the Person search report.</span></span> <span data-ttu-id="e47bb-107">(レポートは現在 Microsoft Dynamics AX 2012 では使用できません。) このトピックでは、これらのタスクを完了するのに役立つコンテンツを示しています。</span><span class="sxs-lookup"><span data-stu-id="e47bb-107">(The report is currently not available for Microsoft Dynamics AX 2012.) This topic points to content that will help you complete those tasks.</span></span>

## <a name="overview"></a><span data-ttu-id="e47bb-108">概要</span><span class="sxs-lookup"><span data-stu-id="e47bb-108">Overview</span></span>

- [<span data-ttu-id="e47bb-109">一般データ保護規則の概要</span><span class="sxs-lookup"><span data-stu-id="e47bb-109">General Data Protection Regulation overview</span></span>](gdpr-guide.md)
- [<span data-ttu-id="e47bb-110">個人検索レポート</span><span class="sxs-lookup"><span data-stu-id="e47bb-110">Person search report</span></span>](gdpr-person-search-report.md)
- [<span data-ttu-id="e47bb-111">個人検索レポートの拡張</span><span class="sxs-lookup"><span data-stu-id="e47bb-111">Extend the Person search report</span></span>](gdpr-extend-person-search-report.md)
- [<span data-ttu-id="e47bb-112">機密データへのアクセスを管理</span><span class="sxs-lookup"><span data-stu-id="e47bb-112">Manage access to sensitive data</span></span>](gdpr-auditing-sensitive-data.md)


## <a name="product-specific-considerations"></a><span data-ttu-id="e47bb-113">製品固有の考慮事項</span><span class="sxs-lookup"><span data-stu-id="e47bb-113">Product-specific considerations</span></span>

- [<span data-ttu-id="e47bb-114">AX 2012 の個人データ要求への対応</span><span class="sxs-lookup"><span data-stu-id="e47bb-114">Respond to requests for personal data in AX 2012</span></span>](gdpr-ax2012.md)
- [<span data-ttu-id="e47bb-115">人事管理の個人データ要求への対応</span><span class="sxs-lookup"><span data-stu-id="e47bb-115">Respond to requests for personal data in Human Resources</span></span>](respond-dsr-request-talent.md)
- [<span data-ttu-id="e47bb-116">一般データ保護規則の概要</span><span class="sxs-lookup"><span data-stu-id="e47bb-116">General Data Protection Regulation overview</span></span>](gdpr-guide.md)
- [<span data-ttu-id="e47bb-117">Lifecycle Services (LCS) に対する GDPR データ要求</span><span class="sxs-lookup"><span data-stu-id="e47bb-117">GDPR data requests for Lifecycle Services (LCS)</span></span>](gdpr-lcs.md)

## <a name="compliance-manager"></a><span data-ttu-id="e47bb-118">コンプライアンス マネージャー</span><span class="sxs-lookup"><span data-stu-id="e47bb-118">Compliance Manager</span></span>
<span data-ttu-id="e47bb-119">コンプライアンス マネージャーは、組織が GDPR のような複雑なコンプライアンス責務を満たすのを支援するために設計された、クロス Microsoft クラウド サービス ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="e47bb-119">Compliance Manager is a cross–Microsoft Cloud services solution designed to help organizations meet complex compliance obligations like the GDPR.</span></span> <span data-ttu-id="e47bb-120">これにより、Microsoft クラウド サービスを使用する場合、推奨される操作およびステップ バイ ステップ ガイダンスと共に、データ保護規制に対するコンプライアンス方針を反映するリアルタイムのリスク評価が実行されます。</span><span class="sxs-lookup"><span data-stu-id="e47bb-120">It performs a real-time risk assessment that reflects your compliance posture against data protection regulations when using Microsoft Cloud services, along with recommended actions and step-by-step guidance.</span></span>

### <a name="compliance-manager"></a><span data-ttu-id="e47bb-121">コンプライアンス マネージャー</span><span class="sxs-lookup"><span data-stu-id="e47bb-121">Compliance Manager</span></span>
<span data-ttu-id="e47bb-122">[https://aka.ms/compliancemanager](https://aka.ms/compliancemanager) に移動して、自分でコンプライアンス マネージャーを試すことができます。</span><span class="sxs-lookup"><span data-stu-id="e47bb-122">You can try Compliance Manager yourself by visiting [https://aka.ms/compliancemanager](https://aka.ms/compliancemanager).</span></span>

### <a name="resources"></a><span data-ttu-id="e47bb-123">リソース</span><span class="sxs-lookup"><span data-stu-id="e47bb-123">Resources</span></span>
<span data-ttu-id="e47bb-124">コンプライアンス マネージャーの詳細と、複雑なコンプライアンス義務を満たすためにどのようにコンプライアンス マネージャーが役に立つかについて学習できるリソースは数多くあります。</span><span class="sxs-lookup"><span data-stu-id="e47bb-124">There are a number of resources to help you learn more about Compliance Manager and what it can do you help you meet complex compliance obligations.</span></span>

- <span data-ttu-id="e47bb-125">[Microsoft 365 - コンプライアンス マネージャー プレビュー](https://blogs.office.com/2017/11/16/microsoft-365-helps-businesses-increase-trust-and-innovation-through-compliance-with-compliance-manager-preview/) (Office、2017 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-125">[Microsoft 365 - Compliance Manager preview](https://blogs.office.com/2017/11/16/microsoft-365-helps-businesses-increase-trust-and-innovation-through-compliance-with-compliance-manager-preview/) (Office, November 2017)</span></span>

- <span data-ttu-id="e47bb-126">[コンプライアンス マネージャー プレビューが閲覧可能になりました](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Compliance-Manager-Preview-is-now-available/ba-p/124662) (Tech Community 2017 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-126">[Compliance Manager preview is now available](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Compliance-Manager-Preview-is-now-available/ba-p/124662) (Tech Community, November 2017)</span></span>

- <span data-ttu-id="e47bb-127">[新しいサービス信頼ポータルについて理解する](https://blogs.technet.microsoft.com/scottschnoll/2017/11/21/get-to-know-the-new-service-trust-portal/) (TechNet 2017 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-127">[Get to know the new Service Trust Portal](https://blogs.technet.microsoft.com/scottschnoll/2017/11/21/get-to-know-the-new-service-trust-portal/) (TechNet, November 2017)</span></span> 

- <span data-ttu-id="e47bb-128">[コンプライアンス マネージャーの発表](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Manage-Your-Compliance-from-One-Place-Announcing-Compliance/ba-p/106493) (Tech Community 2017 年 9 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-128">[Announcing Compliance Manager](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Manage-Your-Compliance-from-One-Place-Announcing-Compliance/ba-p/106493) (Tech Community, September 2017)</span></span>

- <span data-ttu-id="e47bb-129">[現代の職場に力を与えるために、インテリジェンス、管理、セキュリティを強化する](https://blogs.office.com/2017/09/25/advancing-intelligence-management-and-security-to-empower-the-modern-workplace/) (Office 2017 年 9 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-129">[Advancing intelligence, management, and security to empower the modern workplace](https://blogs.office.com/2017/09/25/advancing-intelligence-management-and-security-to-empower-the-modern-workplace/) (Office, September 2017)</span></span>

- <span data-ttu-id="e47bb-130">[GDPR コンプライアンス を迅速化する新しい Microsoft 365 機能](https://blogs.microsoft.com/microsoftsecure/2017/09/25/new-microsoft-365-features-to-accelerate-gdpr-compliance/) (Microsoft セキュリティ、2017 年 9 月)</span><span class="sxs-lookup"><span data-stu-id="e47bb-130">[New Microsoft 365 features to accelerate GDPR compliance](https://blogs.microsoft.com/microsoftsecure/2017/09/25/new-microsoft-365-features-to-accelerate-gdpr-compliance/) (Microsoft Secure, September 2017)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="e47bb-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e47bb-131">Additional resources</span></span>

<span data-ttu-id="e47bb-132">GDPR および組織がデータの要求に対して実行する必要があるアクションの詳細については、[Microsoft サービス信頼ポータル](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=77b002ad-06f7-4a9b-8493-e18e2cb0577f&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="e47bb-132">For more information about the GDPR and the actions that your organization might need to take in response to a request for data, visit the [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=77b002ad-06f7-4a9b-8493-e18e2cb0577f&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers).</span></span>
