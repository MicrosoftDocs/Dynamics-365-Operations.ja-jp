---
title: Attract での拡張性
description: このトピックでは、Microsoft Power Platform を使用して Microsoft Dynamics 365 for Talent - Attract を拡張する方法について説明します。
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305135"
---
# <a name="extensibility-in-attract"></a><span data-ttu-id="099e0-103">Attract での拡張性</span><span class="sxs-lookup"><span data-stu-id="099e0-103">Extensibility in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="099e0-104">Microsoft Dynamics 365 for Talent は、アプリ プラットフォームの Common Data Service (CDS) の上に構築され、Microsoft Power Platform および Common Data Service for Apps が提供する機能を使用してさまざまな方法で拡張できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-104">Microsoft Dynamics 365 for Talent is built on top of the Common Data Service (CDS) for Apps platform, and can be extended in various ways by using the Microsoft Power Platform and the capabilities that Common Data Service for Apps offers.</span></span> <span data-ttu-id="099e0-105">したがって、Microsoft PowerApps および Microsoft Flow を使用して、システムをコンフィギュレーションおよびカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="099e0-105">Therefore, you can configure and personalize the system by using Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="099e0-106">Microsoft Power BI を使用して、人々に関する追加の分析を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="099e0-106">You can also get additional analytics about people by using Microsoft Power BI.</span></span> <span data-ttu-id="099e0-107">さらに、PowerApps および Web コンテンツ (iframe) 活動などの新しいカスタム活動は、採用プロセスをこれまで以上に適応しやすくします。</span><span class="sxs-lookup"><span data-stu-id="099e0-107">Furthermore, new custom activities, such as the PowerApps and Web content (iframe) activities, make the hiring process more adaptable than ever.</span></span> <span data-ttu-id="099e0-108">これらの活動を使用することにより、採用プロセスをビジネス ニーズとプロセスに合わせることができ、採用チームと候補者の両方にシームレスでカスタマイズされた経験があることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-108">By using these activities, you can tailor the hiring process to your business needs and processes, and can make sure that both the hiring team and candidates have a seamless, customized experience.</span></span>

## <a name="take-advantage-of-the-microsoft-power-platform"></a><span data-ttu-id="099e0-109">Microsoft Power Platform を活用</span><span class="sxs-lookup"><span data-stu-id="099e0-109">Take advantage of the Microsoft Power platform</span></span> 

<span data-ttu-id="099e0-110">Attract からのすべてのデータは Common Data Service for Apps に存在するため、Microsoft Power Platform からのツールを使用して Attract に固有のビジネス ニーズを組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-110">Because all the data from Attract resides in Common Data Service for Apps, you can use tools from the Microsoft Power platform to incorporate your unique business needs into Attract.</span></span>

### <a name="powerapps"></a><span data-ttu-id="099e0-111">PowerApps</span><span class="sxs-lookup"><span data-stu-id="099e0-111">PowerApps</span></span>

<span data-ttu-id="099e0-112">PowerApps を使用して、Attract データに接続し、Microsoft Excel の式のような式を使用してロジックを追加するアプリを簡単に構築できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-112">You can use PowerApps to easily build apps that connect to your Attract data, and that use expressions like the expressions in Microsoft Excel to add logic.</span></span> <span data-ttu-id="099e0-113">PowerApps を使用して構築するアプリは、Web、Apple iOS、Google Android デバイスで実行できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-113">Apps that you build by using PowerApps can run on the web, and on Apple iOS and Google Android devices.</span></span>

<span data-ttu-id="099e0-114">たとえば、履歴書をスキャンして候補者を Attract の位置にフィードする軽量アプリを構築することで、採用者にとって大学のキャリアフェアを簡単にすることができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-114">For example, you can make university career fairs easier for recruiters by building a lightweight app that lets them scan resumes and feed candidates to a position in Attract.</span></span> <span data-ttu-id="099e0-115">または、組織のコンプライアンスのニーズを満たすのに役立つアプリを構築できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-115">Alternatively, you can build an app that helps meet your organization's compliance needs.</span></span> <span data-ttu-id="099e0-116">PowerApps およびアプリの構築にそれを使用する方法の詳細については、[Common Data Service for Apps へデータを統合](https://docs.microsoft.com/en-us/powerapps) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099e0-116">For more information about PowerApps and how to use it to build apps, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).</span></span>

### <a name="microsoft-flow"></a><span data-ttu-id="099e0-117">Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="099e0-117">Microsoft Flow</span></span> 

<span data-ttu-id="099e0-118">Microsoft Flow を使用して、Attract データの上で実行するワークフローを自動作成できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-118">You can use Microsoft Flow to create automated workflows that run on top of Attract data.</span></span> <span data-ttu-id="099e0-119">コードの書き込みなしで、数百の人気のアプリおよびサービスに簡単に接続できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-119">You can easily connect to hundreds of popular apps and services without having to write code.</span></span> <span data-ttu-id="099e0-120">Common Data Service for Apps で Attract ジョブ、候補者、アプリケーション エンティティとやりとりするフローを構築することで、さまざまな活動を自動化できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-120">By building flows that interact with the Attract Job, Candidate, and Application entities in Common Data Service for Apps, you can automate various actions.</span></span> <span data-ttu-id="099e0-121">たとえば、候補者がオファーを受け入れると、オンボード チームに通知を送信でき、または Twitter にニュースが発表されます。</span><span class="sxs-lookup"><span data-stu-id="099e0-121">For example, when a candidate accepts an offer, a notification can be sent to an onboarding team, or the news can be announced on Twitter.</span></span> <span data-ttu-id="099e0-122">フローの詳細については、[Microsoft Flow の開発者ドキュメント](https://docs.microsoft.com/en-us/flow/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099e0-122">For more information about flows, see the [Microsoft Flow documentation](https://docs.microsoft.com/en-us/flow/).</span></span>

### <a name="power-bi"></a><span data-ttu-id="099e0-123">Power BI</span><span class="sxs-lookup"><span data-stu-id="099e0-123">Power BI</span></span>

<span data-ttu-id="099e0-124">Power BI を使用すると、Attract データへのより深い洞察を与えるカスタム レポートおよびダッシュボードを構築し表示できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-124">Power BI lets you build and view custom reports and dashboards that give you deeper insight into your Attract data.</span></span> <span data-ttu-id="099e0-125">Power BI および対話型レポートとダッシュボードの作成方法の詳細については、[Power BI ドキュメント](https://docs.microsoft.com/en-us/power-bi/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099e0-125">For more information about Power BI and how to build interactive reports and dashboards, see the [Power BI documentation](https://docs.microsoft.com/en-us/power-bi/).</span></span>

### <a name="custom-activities"></a><span data-ttu-id="099e0-126">カスタム活動</span><span class="sxs-lookup"><span data-stu-id="099e0-126">Custom activities</span></span> 

<span data-ttu-id="099e0-127">職務プロセス テンプレートのレベルで、または新しいジョブを作成している間に、PowerApps アプリおよび Web コンテンツ (iframe) 活動などのカスタム活動を追加できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-127">You can add custom activities, such as the PowerApps apps and Web content (iframe) activities, at the level of the job process template or while you're creating a new job.</span></span> <span data-ttu-id="099e0-128">これらの活動を使用すると、採用プロセスをカスタマイズしたり、組織に固有のビジネス ロジックを Attract にもたらすことができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-128">These activities let you customize the hiring process and bring business logic that is unique to your organization into Attract.</span></span>

#### <a name="powerapps-activity"></a><span data-ttu-id="099e0-129">PowerApps 活動</span><span class="sxs-lookup"><span data-stu-id="099e0-129">PowerApps activity</span></span> 

<span data-ttu-id="099e0-130">PowerApps 活動では、職務または職務プロセス テンプレートの作成者が採用フローを PowerApps アプリに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-130">The PowerApps activity lets the creator of a job or job process template embed a PowerApps app in the hiring flow.</span></span> <span data-ttu-id="099e0-131">アプリを作成し公開した後、活動コンフィギュレーションで、アプリ ID を入力できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-131">After you create and publish the app, you can enter its app ID in the activity configurations.</span></span> <span data-ttu-id="099e0-132">PowerApps アプリを使用すると、Common Data Service for Apps へのデータの読み取りおよび書き込みができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-132">By using a PowerApps app, you can read and write data into Common Data Service for Apps.</span></span> <span data-ttu-id="099e0-133">アプリがフローするようにリンクもできます。</span><span class="sxs-lookup"><span data-stu-id="099e0-133">You can even link the app to a flow.</span></span> <span data-ttu-id="099e0-134">たとえば、採用担当者が電話面接の実施中に、フォームに入力するために使用するアプリがあります。</span><span class="sxs-lookup"><span data-stu-id="099e0-134">For example, you have an app that recruiters use to fill in a form while they conduct phone interviews.</span></span> <span data-ttu-id="099e0-135">この場合、申請者が職務アプリ プロセスでさらに進めることができるかどうかを評価するフローにアプリをリンクできます。</span><span class="sxs-lookup"><span data-stu-id="099e0-135">In this case, you can link the app to a flow that evaluates whether an applicant can be advanced further in the job application process.</span></span> <span data-ttu-id="099e0-136">このタイプの活動は、採用チームのメンバーでのみ表示できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-136">This type of activity can be viewed only by members of the hiring team.</span></span> <span data-ttu-id="099e0-137">PowerApps 活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099e0-137">For more information about how to configure the PowerApps activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="099e0-138">PowerApps 活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-138">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

#### <a name="web-content-iframe-activity"></a><span data-ttu-id="099e0-139">Web コンテンツ (iframe) 活動</span><span class="sxs-lookup"><span data-stu-id="099e0-139">Web content (iframe) activity</span></span>

<span data-ttu-id="099e0-140">Web コンテンツ (iframe) 活動を使用して、採用プロセスまたは候補者のポータルに構築したカスタム Web ソリューションを組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-140">The Web content (iframe) activity lets you embed a custom web solution that you've built in the hiring process or the Candidate portal.</span></span> <span data-ttu-id="099e0-141">Common Data Service for Apps から直接データの読み取りおよび書き込みができます。</span><span class="sxs-lookup"><span data-stu-id="099e0-141">You can read and write data directly from Common Data Service for Apps.</span></span> <span data-ttu-id="099e0-142">フローをトリガーし、または Microsoft Azure 機能を利用できるように、ソリューションをカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="099e0-142">You can also customize the solution so that it triggers flows or takes advantage of Microsoft Azure functions.</span></span> <span data-ttu-id="099e0-143">Web コンテンツ活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="099e0-143">For more information about how to configure the Web content activity, see [Activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="099e0-144">Web コンテンツ活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="099e0-144">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>
