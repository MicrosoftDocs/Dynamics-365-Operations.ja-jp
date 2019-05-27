---
title: 財務諸表
description: Finance および Operations の財務報告では、財務およびビジネスのプロフェッショナルが財務諸表を作成、管理、展開、および表示できます。 効率的にさまざまな種類のレポートをデザインするために従来のレポートの制約を超えて移動します。
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae2087cf142fc2670bda3c542b336f12978178a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553905"
---
# <a name="financial-reporting"></a><span data-ttu-id="cf33b-104">財務諸表</span><span class="sxs-lookup"><span data-stu-id="cf33b-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf33b-105">Finance および Operations の財務報告では、財務およびビジネスのプロフェッショナルが財務諸表を作成、管理、展開、および表示できます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="cf33b-106">効率的にさまざまな種類のレポートをデザインするために従来のレポートの制約を超えて移動します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="cf33b-107">財務報告書には、分析コードのサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="cf33b-108">したがって、勘定区分または分析コードは、すぐに使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="cf33b-109">その他のツールや構成手順を実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf33b-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="cf33b-110">財務諸表の設定</span><span class="sxs-lookup"><span data-stu-id="cf33b-110">Financial reporting setup</span></span>
<span data-ttu-id="cf33b-111">**財務諸表の設定** ページには、システムのすべての財務分析コードの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="cf33b-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="cf33b-112">**一般会計** \> **元帳の設定** \> **財務諸表の設定**。</span><span class="sxs-lookup"><span data-stu-id="cf33b-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="cf33b-113">**財務諸表の設定** ページには、財務諸表でレポートするデータを特定する 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="cf33b-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="cf33b-114">**分析コード** - 異なる会社がさまざまな分析コードや勘定構造を使用するため、レポートでユーザーがすべての財務分析コードを表示する順序を特定する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="cf33b-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="cf33b-115">このページでは、財務分析コードを財務諸表でレポートを作成および表示する際に表示する順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="cf33b-116">**属性タブ**は、**仕入先**および**顧客**をフィルタリングおよびレポートデザインの属性として使用するかどうかを選択できる場所です。</span><span class="sxs-lookup"><span data-stu-id="cf33b-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="cf33b-117">トランザクションを転記する際に、複数の仕入先または顧客を単一伝票に入力しない場合、仕入先および顧客に関するレポートのみが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="cf33b-118">仕入先または顧客を選択すると、統合にさらに時間が追加されます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="cf33b-119">財務報告書のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="cf33b-119">Financial reporting components</span></span>
<span data-ttu-id="cf33b-120">財務報告書の次のコンポーネントで、レポートの作成、表示、およびスケジュールが簡単にできます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="cf33b-121">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="cf33b-121">Component</span></span>        | <span data-ttu-id="cf33b-122">関数</span><span class="sxs-lookup"><span data-stu-id="cf33b-122">Functions</span></span> | <span data-ttu-id="cf33b-123">追加情報</span><span class="sxs-lookup"><span data-stu-id="cf33b-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="cf33b-124">レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="cf33b-124">Report Designer</span></span>  | <span data-ttu-id="cf33b-125">レポートを定義して生成するために、組み合わせるレポートの構成要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="cf33b-126">レポート ウィザードで、デザイン プロセスの経験が少ないユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf33b-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="cf33b-127">上級者になると、新しいレポートの構成要素を作成したり、要求に合わせて既存の構成要素を変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="cf33b-128">レポート スケジューラ</span><span class="sxs-lookup"><span data-stu-id="cf33b-128">Report schedules</span></span> | <span data-ttu-id="cf33b-129">1 つのレポートまたはレポートのグループをスケジュールして、定期的に生成されるようにします。</span><span class="sxs-lookup"><span data-stu-id="cf33b-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="cf33b-130">財務諸表の生成</span><span class="sxs-lookup"><span data-stu-id="cf33b-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="cf33b-131">機能</span><span class="sxs-lookup"><span data-stu-id="cf33b-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="cf33b-132">機能</span><span class="sxs-lookup"><span data-stu-id="cf33b-132">Feature</span></span></th>
<th><span data-ttu-id="cf33b-133">説明</span><span class="sxs-lookup"><span data-stu-id="cf33b-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cf33b-134">レポート デザインの柔軟性</span><span class="sxs-lookup"><span data-stu-id="cf33b-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="cf33b-135">レポート デザイナーでは、レポートをデザインする際に次のレポート オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="cf33b-136">分析コードの組み合わせを保存し、複数のレポートの分析コードを再利用します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="cf33b-137">分析コードの説明を書式設定して表示する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="cf33b-138">レポートの構成要素から除外した勘定または分析コードを識別します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="cf33b-139">ローリング予測のヘッダー書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="cf33b-140">財務諸表のコラボレーション</span><span class="sxs-lookup"><span data-stu-id="cf33b-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="cf33b-141">次の機能は、レポートの生成および配布の管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="cf33b-142">レポートをスケジュールして、毎日、毎週、月単位、または年単位基準で自動的に生成されるようにします。</span><span class="sxs-lookup"><span data-stu-id="cf33b-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="cf33b-143">読み取り専用 XPS 形式にエクスポートして、デジタル署名でドキュメントのセキュリティを向上します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="cf33b-144">Microsoft Excel ワークシートにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="cf33b-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="cf33b-145">レポートを共有するために、レポートへのリンクを含む電子メール メッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="cf33b-146">対話型レポートの表示</span><span class="sxs-lookup"><span data-stu-id="cf33b-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="cf33b-147">対話型機能で、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="cf33b-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="cf33b-148">表示しているレポートのレポートの日付を変更します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="cf33b-149">表示しているレポートの通貨を変更します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="cf33b-150">概要ビューまたは詳細ビューのいずれかでレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="cf33b-151">レポート コンテンツに特定の分析コードまたは分析コードの組み合わせを制限するのには、分析コード フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="cf33b-152">レポート コンテンツに特定の属性または属性の組み合わせを制限するのには、属性フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="cf33b-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="cf33b-153">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="cf33b-153">Additional resources</span></span>
[<span data-ttu-id="cf33b-154">財務諸表の生成</span><span class="sxs-lookup"><span data-stu-id="cf33b-154">Generate a financial report</span></span>](generate-financial-report.md)
