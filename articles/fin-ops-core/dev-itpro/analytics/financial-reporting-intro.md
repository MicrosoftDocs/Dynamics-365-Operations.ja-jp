---
title: 財務諸表
description: 財務報告では、財務およびビジネスのプロフェッショナルが財務諸表を作成、管理、展開、および表示できます。
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b1db953165bd745a00f68048767a2b19fcc2f38
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093954"
---
# <a name="financial-reporting"></a><span data-ttu-id="d1f6a-103">財務報告</span><span class="sxs-lookup"><span data-stu-id="d1f6a-103">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1f6a-104">アプリケーションの財務報告では、財務およびビジネスのプロフェッショナルが財務諸表を作成、管理、展開、および表示できます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-104">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="d1f6a-105">効率的にさまざまな種類のレポートをデザインするために従来のレポートの制約を超えて移動します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-105">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="d1f6a-106">財務報告書には、分析コードのサポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-106">Financial reporting includes dimension support.</span></span> <span data-ttu-id="d1f6a-107">したがって、勘定区分または分析コードは、すぐに使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-107">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="d1f6a-108">その他のツールや構成手順を実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-108">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="d1f6a-109">財務諸表の設定</span><span class="sxs-lookup"><span data-stu-id="d1f6a-109">Financial reporting setup</span></span>
<span data-ttu-id="d1f6a-110">**財務諸表の設定** ページには、システムのすべての財務分析コードの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-110">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="d1f6a-111">**一般会計** \> **元帳の設定** \> **財務諸表の設定**。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-111">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="d1f6a-112">**財務諸表の設定** ページには、財務諸表でレポートするデータを特定する 2 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-112">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="d1f6a-113">**分析コード** - 異なる会社がさまざまな分析コードや勘定構造を使用するため、レポートでユーザーがすべての財務分析コードを表示する順序を特定する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-113">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="d1f6a-114">このページでは、財務分析コードを財務諸表でレポートを作成および表示する際に表示する順序を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-114">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="d1f6a-115">**属性タブ** は、**仕入先** および **顧客** をフィルタリングおよびレポートデザインの属性として使用するかどうかを選択できる場所です。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-115">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="d1f6a-116">トランザクションを転記する際に、複数の仕入先または顧客を単一伝票に入力しない場合、仕入先および顧客に関するレポートのみが役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-116">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="d1f6a-117">仕入先または顧客を選択すると、統合にさらに時間が追加されます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-117">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="d1f6a-118">財務報告書のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="d1f6a-118">Financial reporting components</span></span>
<span data-ttu-id="d1f6a-119">財務報告書の次のコンポーネントで、レポートの作成、表示、およびスケジュールが簡単にできます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-119">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="d1f6a-120">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d1f6a-120">Component</span></span>        | <span data-ttu-id="d1f6a-121">関数</span><span class="sxs-lookup"><span data-stu-id="d1f6a-121">Functions</span></span> | <span data-ttu-id="d1f6a-122">追加情報</span><span class="sxs-lookup"><span data-stu-id="d1f6a-122">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="d1f6a-123">レポート デザイナー</span><span class="sxs-lookup"><span data-stu-id="d1f6a-123">Report Designer</span></span>  | <span data-ttu-id="d1f6a-124">レポートを定義して生成するために、組み合わせるレポートの構成要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-124">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="d1f6a-125">レポート ウィザードで、デザイン プロセスの経験が少ないユーザーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-125">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="d1f6a-126">上級者になると、新しいレポートの構成要素を作成したり、要求に合わせて既存の構成要素を変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-126">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="d1f6a-127">レポート スケジューラ</span><span class="sxs-lookup"><span data-stu-id="d1f6a-127">Report schedules</span></span> | <span data-ttu-id="d1f6a-128">1 つのレポートまたはレポートのグループをスケジュールして、定期的に生成されるようにします。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-128">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="d1f6a-129">財務諸表の生成</span><span class="sxs-lookup"><span data-stu-id="d1f6a-129">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="d1f6a-130">機能</span><span class="sxs-lookup"><span data-stu-id="d1f6a-130">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="d1f6a-131">機能</span><span class="sxs-lookup"><span data-stu-id="d1f6a-131">Feature</span></span></th>
<th><span data-ttu-id="d1f6a-132">説明</span><span class="sxs-lookup"><span data-stu-id="d1f6a-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d1f6a-133">レポート デザインの柔軟性</span><span class="sxs-lookup"><span data-stu-id="d1f6a-133">Report design flexibility</span></span></td>
<td><span data-ttu-id="d1f6a-134">レポート デザイナーでは、レポートをデザインする際に次のレポート オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-134">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="d1f6a-135">分析コードの組み合わせを保存し、複数のレポートの分析コードを再利用します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-135">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="d1f6a-136">分析コードの説明を書式設定して表示する方法を制御します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-136">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="d1f6a-137">レポートの構成要素から除外した勘定または分析コードを識別します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-137">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="d1f6a-138">ローリング予測のヘッダー書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-138">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d1f6a-139">財務諸表のコラボレーション</span><span class="sxs-lookup"><span data-stu-id="d1f6a-139">Financial report collaboration</span></span></td>
<td><span data-ttu-id="d1f6a-140">次の機能は、レポートの生成および配布の管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-140">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="d1f6a-141">レポートをスケジュールして、毎日、毎週、月単位、または年単位基準で自動的に生成されるようにします。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-141">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="d1f6a-142">読み取り専用 XPS 形式にエクスポートして、デジタル署名でドキュメントのセキュリティを向上します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-142">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="d1f6a-143">Microsoft Excel ワークシートにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-143">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="d1f6a-144">レポートを共有するために、レポートへのリンクを含む電子メール メッセージを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-144">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d1f6a-145">対話型レポートの表示</span><span class="sxs-lookup"><span data-stu-id="d1f6a-145">Interactive report viewing</span></span></td>
<td><span data-ttu-id="d1f6a-146">対話型機能で、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-146">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="d1f6a-147">表示しているレポートのレポートの日付を変更します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-147">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="d1f6a-148">表示しているレポートの通貨を変更します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-148">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="d1f6a-149">概要ビューまたは詳細ビューのいずれかでレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-149">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="d1f6a-150">レポート コンテンツに特定の分析コードまたは分析コードの組み合わせを制限するのには、分析コード フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-150">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="d1f6a-151">レポート コンテンツに特定の属性または属性の組み合わせを制限するのには、属性フィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="d1f6a-151">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="d1f6a-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d1f6a-152">Additional resources</span></span>
[<span data-ttu-id="d1f6a-153">財務諸表の生成</span><span class="sxs-lookup"><span data-stu-id="d1f6a-153">Generate financial reports</span></span>](generate-financial-report.md)
