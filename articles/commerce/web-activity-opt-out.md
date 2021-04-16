---
title: Web アクティビティ イベント コレクションのオプトアウト
description: このトピックでは、web サイトへの訪問者に対して、Microsoft Dynamics 365 Commerce の Web アクティビティ イベント コレクションをオプトアウトする方法について説明します。
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791560"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="89222-103">Web アクティビティ イベント コレクションのオプトアウト</span><span class="sxs-lookup"><span data-stu-id="89222-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="89222-104">このトピックでは、Microsoft Dynamics 365 Commerce で Web アクティビティ イベント コレクションを顧客にオプトアウトさせる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89222-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="89222-105">Dynamics 365 Commerce では、サイト管理者が自社の e コマース サイトのユーザーのウェブ アクティビティ の分析をすることが可能となります。</span><span class="sxs-lookup"><span data-stu-id="89222-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="89222-106">そうすることで、自身のサイトがどのように使われているかをより理解することができ、ユーザー エクスペリエンスを向上させ、ビジネスの目標を達成するためにサイトを最適化することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="89222-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="89222-107">管理者がオプトアウト エクスペリエンスを実装する方法</span><span class="sxs-lookup"><span data-stu-id="89222-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="89222-108">管理者がオプトアウト エクスペリエンスを実装する方法は、3 つあります。</span><span class="sxs-lookup"><span data-stu-id="89222-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="89222-109">ユーザーに代わってオプト アウトする</span><span class="sxs-lookup"><span data-stu-id="89222-109">Opt out on behalf of users</span></span>

<span data-ttu-id="89222-110">Commerce 本部のアカウント管理では、管理者はユーザーに代わってオプト アウトを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="89222-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="89222-111">HQ クライアントで **すべての顧客** ページで、顧客を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="89222-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="89222-112">[顧客の詳細] ページにて、 **小売** クイックタブの **プライバシー** セクションで、**アクティビティの追跡をしない** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="89222-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![プライバシー設定](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="89222-114">**保存** を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="89222-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="89222-115">モジュールベースのオプトアウト エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="89222-115">Module-based opt-out experience</span></span>

<span data-ttu-id="89222-116">管理者は、認証されたユーザーが自分で Web アクティビティ イベント コレクションをオプトアウトを選択させることができます。</span><span class="sxs-lookup"><span data-stu-id="89222-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="89222-117">このオプトアウト エクスペリエンスを提供するには、顧客アカウント プロファイル ページにユーザーのオプトアウト モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="89222-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="89222-118">カスタムの拡張機能</span><span class="sxs-lookup"><span data-stu-id="89222-118">Custom extensions</span></span>

<span data-ttu-id="89222-119">管理者は、ユーザーのオプトアウト エクスペリエンスを管理するの独自の拡張機能を作成できます。</span><span class="sxs-lookup"><span data-stu-id="89222-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="89222-120">詳細については、[Retail サーバー API](e-commerce-extensibility/call-retail-server-apis.md) および [オンライン チャネルの拡張性](e-commerce-extensibility/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89222-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
