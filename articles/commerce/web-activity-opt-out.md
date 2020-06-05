---
title: Web アクティビティ イベント コレクションのオプトアウト
description: このトピックでは、web サイトへの訪問者に対して、Microsoft Dynamics 365 Commerce の Web アクティビティ イベント コレクションをオプトアウトする方法について説明します。
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 8058db089b8768076ff1250be77d42a6e2b3f570
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378995"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="db799-103">Web アクティビティ イベント コレクションのオプトアウト</span><span class="sxs-lookup"><span data-stu-id="db799-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="db799-104">このトピックでは、Microsoft Dynamics 365 Commerce で Web アクティビティ イベント コレクションを顧客にオプトアウトさせる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="db799-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db799-105">概要</span><span class="sxs-lookup"><span data-stu-id="db799-105">Overview</span></span>

<span data-ttu-id="db799-106">Dynamics 365 Commerce では、サイト管理者が自社の e コマース サイトのユーザーのウェブ アクティビティ の分析をすることが可能となります。</span><span class="sxs-lookup"><span data-stu-id="db799-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="db799-107">そうすることで、自身のサイトがどのように使われているかをより理解することができ、ユーザー エクスペリエンスを向上させ、ビジネスの目標を達成するためにサイトを最適化することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="db799-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="db799-108">管理者がオプトアウト エクスペリエンスを実装する方法</span><span class="sxs-lookup"><span data-stu-id="db799-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="db799-109">管理者がオプトアウト エクスペリエンスを実装する方法は、3 つあります。</span><span class="sxs-lookup"><span data-stu-id="db799-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="db799-110">ユーザーに代わってオプト アウトする</span><span class="sxs-lookup"><span data-stu-id="db799-110">Opt out on behalf of users</span></span>

<span data-ttu-id="db799-111">Commerce 本部のアカウント管理では、管理者はユーザーに代わってオプト アウトを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="db799-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="db799-112">HQ クライアントで **すべての顧客** ページで、顧客を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="db799-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="db799-113">[顧客の詳細] ページにて、 **小売** クイックタブの **プライバシー** セクションで、**アクティビティの追跡をしない** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="db799-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![プライバシー設定](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="db799-115">**保存**を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="db799-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="db799-116">モジュールベースのオプトアウト エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="db799-116">Module-based opt-out experience</span></span>

<span data-ttu-id="db799-117">管理者は、認証されたユーザーが自分で Web アクティビティ イベント コレクションをオプトアウトを選択させることができます。</span><span class="sxs-lookup"><span data-stu-id="db799-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="db799-118">このオプトアウト エクスペリエンスを提供するには、顧客アカウント プロファイル ページにユーザーのオプトアウト モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="db799-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="db799-119">カスタムの拡張機能</span><span class="sxs-lookup"><span data-stu-id="db799-119">Custom extensions</span></span>

<span data-ttu-id="db799-120">管理者は、ユーザーのオプトアウト エクスペリエンスを管理するの独自の拡張機能を作成できます。</span><span class="sxs-lookup"><span data-stu-id="db799-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="db799-121">詳細については、[Retail サーバー API](e-commerce-extensibility/call-retail-server-apis.md) および [オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="db799-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
