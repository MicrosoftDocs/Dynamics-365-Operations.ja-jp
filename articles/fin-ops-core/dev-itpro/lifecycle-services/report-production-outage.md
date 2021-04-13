---
title: 稼働停止のレポート
description: このトピックでは、Lifecycle Services (LCS) を通じて生産停止を報告する方法について説明します。
author: angelmarshall
ms.date: 05/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 46b489d3219eb3699ce38e8cb6c4c29c0e09b201
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749610"
---
# <a name="report-a-production-outage"></a><span data-ttu-id="55897-103">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="55897-103">Report a production outage</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="55897-104">Lifecycle Services (LCS) には、**レポート生産停止** と呼ばれる機能があります。</span><span class="sxs-lookup"><span data-stu-id="55897-104">Lifecycle Services (LCS) has a feature called **Report production outage**.</span></span> <span data-ttu-id="55897-105">この機能は、1 つ以上の Dynamics 365 Finance and Operations アプリを購入し、LCS に配置された実稼働環境の実装プロジェクトを持つすべての顧客が利用できます。</span><span class="sxs-lookup"><span data-stu-id="55897-105">This feature is available to all customers who have purchased one or more Dynamics 365 Finance and Operations apps and have implementation projects with a production environment deployed in LCS.</span></span> <span data-ttu-id="55897-106">この機能は、実稼動環境のサービスが低下または使用不可能になった場合、Microsoft サポートに問題をエスカレートを迅速かつ有効なチャンネルを提供します。</span><span class="sxs-lookup"><span data-stu-id="55897-106">This feature provides a quick and effective channel to escalate issues to Microsoft Support in the event that the services in a production environment are degraded or become unavailable.</span></span>

<span data-ttu-id="55897-107">相互に包括的な条件に従って、稼働停止は、複数のユーザーに影響を与え、ビジネスの日常業務遂行を妨げる実稼働環境における 1 つ以上のシステム全体の問題として定義できます。</span><span class="sxs-lookup"><span data-stu-id="55897-107">Following mutually inclusive conditions, a production outage can be defined as one or more system-wide issues on a live production environment that impact multiple users and prevent your business from performing daily operations.</span></span>

## <a name="reporting-flow"></a><span data-ttu-id="55897-108">レポート フロー</span><span class="sxs-lookup"><span data-stu-id="55897-108">Reporting flow</span></span>
<span data-ttu-id="55897-109">次のリストは、問題を処理する順序を示します。</span><span class="sxs-lookup"><span data-stu-id="55897-109">The following list shows the order in which an issue should be handled:</span></span>

1. <span data-ttu-id="55897-110">実稼働環境で、顧客は稼働停止やその他の業務を続行できない状況が発生します。</span><span class="sxs-lookup"><span data-stu-id="55897-110">In a live production environment, a customer experiences an outage or other situation with prevents business from continuing.</span></span>
2. <span data-ttu-id="55897-111">顧客は、LCS サポート ポータルを使用して稼働停止の問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="55897-111">The customer reports a production outage issue by using the LCS Support portal.</span></span>
3. <span data-ttu-id="55897-112">顧客は稼働停止の問題を選択し、追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="55897-112">The customer selects a production outage issue and provides additional information.</span></span>
4. <span data-ttu-id="55897-113">Microsoft のサポート エンジニアは、送信の 30 分以内に生産停止チケットを確認し、問題を調査し解決するために利害関係者とすぐに連携を取ります。</span><span class="sxs-lookup"><span data-stu-id="55897-113">A Microsoft support engineer acknowledges the production outage ticket within 30 minutes of submission and begins to immediately collaborate with stakeholders to investigate and resolve the issue.</span></span>
5. <span data-ttu-id="55897-114">サポート エンジニアが顧客に連絡してステータス更新を提供します。</span><span class="sxs-lookup"><span data-stu-id="55897-114">A support engineer contacts the customer to provide a status update.</span></span>

## <a name="access-and-availability"></a><span data-ttu-id="55897-115">アクセスおよび可用性</span><span class="sxs-lookup"><span data-stu-id="55897-115">Access and availability</span></span>
<span data-ttu-id="55897-116">顧客の実装プロジェクトに追加されたすべてのユーザーはこの機能にアクセスを許可できます。</span><span class="sxs-lookup"><span data-stu-id="55897-116">All users who have been added to a customer's implementation project have access to this feature.</span></span> <span data-ttu-id="55897-117">これには、プロジェクト オーナー、組織管理者、チームメンバー、および環境マネージャーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="55897-117">This includes project owners, organization admins, team members, and environment managers.</span></span>

<span data-ttu-id="55897-118">この機能は次で利用できます。</span><span class="sxs-lookup"><span data-stu-id="55897-118">This feature is available for:</span></span>
- <span data-ttu-id="55897-119">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="55897-119">Dynamics 365 Finance</span></span>
- <span data-ttu-id="55897-120">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="55897-120">Dynamics 365 Supply Chain Management</span></span>
- <span data-ttu-id="55897-121">Microsoft が管理する環境</span><span class="sxs-lookup"><span data-stu-id="55897-121">Environments that are managed by Microsoft</span></span>
- <span data-ttu-id="55897-122">LCS プロジェクトの実稼動環境</span><span class="sxs-lookup"><span data-stu-id="55897-122">A production environment in the LCS project</span></span>
- <span data-ttu-id="55897-123">すべてのサポート計画</span><span class="sxs-lookup"><span data-stu-id="55897-123">All support plans</span></span>

## <a name="report-a-production-outage"></a><span data-ttu-id="55897-124">稼働停止のレポート</span><span class="sxs-lookup"><span data-stu-id="55897-124">Report a production outage</span></span>
<span data-ttu-id="55897-125">生産停止を報告するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="55897-125">To report a production outage, follow these steps:</span></span>

1. <span data-ttu-id="55897-126">LCS プロジェクトにログインします。</span><span class="sxs-lookup"><span data-stu-id="55897-126">Log in to your LCS project.</span></span>  
2. <span data-ttu-id="55897-127">ハンバーガー メニューから **サポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-127">From the hamburger menu, click **Support**.</span></span> 

  ![サポートをクリック](media/click-support.png)
  
3. <span data-ttu-id="55897-129">**Microsoft に送信** タブで、**稼働停止のレポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-129">On the **Submitted To Microsoft** tab, click **Report production outage**.</span></span>

  ![サポートをクリック](media/report-production-outage.png)
  
4. <span data-ttu-id="55897-131">プロダクションの停止を確認し、ドロップダウン リストから停止シナリオを選択してから、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-131">Confirm the production outage, select the outage scenario from the drop-down list, and then click **Continue**.</span></span>
5. <span data-ttu-id="55897-132">停止に関するタイトルと詳細を追加して、**次** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-132">Add a title and details about the outage, and then click **Next**.</span></span>
6. <span data-ttu-id="55897-133">連絡先の情報を入力し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-133">Provide contact information, and then click **Next**.</span></span>
7. <span data-ttu-id="55897-134">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="55897-134">Click **Done**.</span></span> 

<span data-ttu-id="55897-135">LCS で稼働停止をレポートできない場合は [電話サポート](cloud-powered-support-lcs.md#phone-support) が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="55897-135">If you're unable to report a production outage in LCS, [phone support](cloud-powered-support-lcs.md#phone-support) is available.</span></span> 

> [!Note]
> <span data-ttu-id="55897-136">停止シナリオに状況が一覧表示されていない場合は、LCS を通じてサポート インシデントを入力します。</span><span class="sxs-lookup"><span data-stu-id="55897-136">If you don't see your situation listed in the outage scenarios, enter a support incident through LCS.</span></span> <span data-ttu-id="55897-137">Microsoft のサポート エンジニアによる最初の調査中に、状況が現在の稼働停止シナリオのリストに合っていないことがわかった場合、サポート インシデントが現在のサポート計画に基づいて正しいサポート チームおよびサービス レベル契約 (SLA)  に転送されます。</span><span class="sxs-lookup"><span data-stu-id="55897-137">During the initial investigation by a Microsoft support engineer, if it is found that the situation does not meet the current list of production outage scenarios, the support incident will be transferred to the correct support team and service-level agreement (SLA)  based on your current support plan.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]