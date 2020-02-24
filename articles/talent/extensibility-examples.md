---
title: Power Apps および Power Automate を使用した Talent の拡張
description: この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent - Attract の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 1051fa4db16bb94cc9d60a91fc3637d7e5305cc2
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029914"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="759ca-103">Power Apps および Power Automate を使用した Talent の拡張</span><span class="sxs-lookup"><span data-stu-id="759ca-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="759ca-104">この記事では、Microsoft Power Apps および Microsoft Power Automate を使用する Microsoft Dynamics 365 Talent: Attract の拡張性シナリオのいくつかの例を説明します。</span><span class="sxs-lookup"><span data-stu-id="759ca-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="759ca-105">各例に関連付けられているソリューション パッケージを Power Apps 環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="759ca-106">次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="759ca-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="759ca-107">この記事で説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="759ca-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="759ca-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="759ca-108">Prerequisites</span></span>

- <span data-ttu-id="759ca-109">パッケージをインポートするには、ユーザーは**環境メーカー**のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="759ca-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="759ca-110">アプリをエクスポートまたはインポートするには、Power Apps プラン 2 ライセンスもしくは Power Apps プラン 2 試用版ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="759ca-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="759ca-111">Power Automate – フォーム コネクト</span><span class="sxs-lookup"><span data-stu-id="759ca-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="759ca-112">**Power Automate – フォーム コネクト** テンプレートは、Microsoft Forms からデータを読み込み、それを Common Data Service エンティティに格納することができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="759ca-113">このテンプレートは、他のシナリオに使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="759ca-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="759ca-114">Here are some examples:</span></span>

- <span data-ttu-id="759ca-115">候補評価をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="759ca-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="759ca-116">コースのアンケート結果をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="759ca-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="759ca-117">人事管理 (HR) の管理者向けの面接質問のライブラリを作成します。</span><span class="sxs-lookup"><span data-stu-id="759ca-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="759ca-118">面接プロセスの候補者の評価をキャプチャします</span><span class="sxs-lookup"><span data-stu-id="759ca-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="759ca-119">Microsoft Dynamics 365: Attract では、候補者が詳細を入力する候補者ポータルでフォームを使用できます。</span><span class="sxs-lookup"><span data-stu-id="759ca-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="759ca-120">フォームを職務テンプレートに活動としても埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="759ca-121">候補者がフォームを送信すると、Microsoft Power Automate はフォーム送信をキャプチャし、データを読み込み、Common Data Service エンティティに格納します。</span><span class="sxs-lookup"><span data-stu-id="759ca-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="759ca-122">**Power Automate – フォーム コネクト** テンプレートおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Power Automate – フォーム コネクト](https://go.microsoft.com/fwlink/?linkid=2081988) に移動します。</span><span class="sxs-lookup"><span data-stu-id="759ca-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="759ca-123">Power Automate – SharePoint 統合</span><span class="sxs-lookup"><span data-stu-id="759ca-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="759ca-124">**Power Automate – SharePoint 統合** テンプレートを使用すると、Microsoft SharePoint リストからデータを読み取り、そのリストを Common Data Service エンティティのフィールド値と比較し、その比較結果を通知電子メールとして送信できます。</span><span class="sxs-lookup"><span data-stu-id="759ca-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="759ca-125">組織では、一連のスキルが緊急に必要とされることがあるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="759ca-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="759ca-126">これらのスキルは、SharePoint に SharePoint リストとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="759ca-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="759ca-127">候補者が一連の必要なスキルがリストされている仕事に応募するときに、候補者のスキルと SharePoint に格納されているスキルに顕著な一致が見られる場合は、通知電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="759ca-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="759ca-128">これは、組織全体で採用担当者が候補者を採用するのに役立つため、緊急に必要なポジションをより迅速に埋めるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="759ca-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="759ca-129">このテンプレートは、SharePoint 統合を含むあらゆるシナリオで使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="759ca-130">**Power Automate  – SharePoint 統合** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [Power Automate – SharePoint 統合](https://go.microsoft.com/fwlink/?linkid=2082109) に移動します。</span><span class="sxs-lookup"><span data-stu-id="759ca-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="759ca-131">照会アプリ</span><span class="sxs-lookup"><span data-stu-id="759ca-131">Referral App</span></span>

<span data-ttu-id="759ca-132">照会アプリを使用すると、共有された人材プールに候補者を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="759ca-133">候補者を送信するときに、参照元に**名**、**姓**、**電子メール**、および **LinkedIn URL** を入力できます。</span><span class="sxs-lookup"><span data-stu-id="759ca-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="759ca-134">これにより、候補者のソース メタデータに、参照元の情報が設定されます。</span><span class="sxs-lookup"><span data-stu-id="759ca-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="759ca-135">このアプリは、参照を送信するための従業員セルフ サービスに埋め込むことも、社内ポータルでハイパーリンクとして使用してスタンドアロン アプリとして実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="759ca-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="759ca-136">**照会アプリ**をダウンロードするには、Microsoft ダウンロード センターの [Dynamics 365 Talent拡張機能ソリューション : 照会アプリ](https://www.microsoft.com/download/details.aspx?id=58497)に移動します。</span><span class="sxs-lookup"><span data-stu-id="759ca-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="759ca-137">このアプリをインポートしてカスタマイズし、機能を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="759ca-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="759ca-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="759ca-138">Additional resources</span></span>

[<span data-ttu-id="759ca-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="759ca-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="759ca-140">テナントと環境間でのアプリケーションの移行</span><span class="sxs-lookup"><span data-stu-id="759ca-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
