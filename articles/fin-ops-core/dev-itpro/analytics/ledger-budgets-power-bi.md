---
title: 実績対予算 Power BI コンテンツ
description: このトピックでは、実績対予算 Power BI コンテンツについて説明します。 レポートへのアクセス方法およびデータ モデルに関する情報を提供します。
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568576"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="68b81-104">実績対予算 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="68b81-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68b81-105">このトピックでは、**実績対予算** Microsoft Power BI コンテンツについて説明します。</span><span class="sxs-lookup"><span data-stu-id="68b81-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="68b81-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="68b81-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="68b81-107">概要</span><span class="sxs-lookup"><span data-stu-id="68b81-107">Overview</span></span>

<span data-ttu-id="68b81-108">**実績対予算** Power BI コンテンツは、組織内で実績対予算パフォーマンスの監視を担当する各個人に対して作成されました。</span><span class="sxs-lookup"><span data-stu-id="68b81-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="68b81-109">**実績対予算** Power BI コンテンツは、予算差異の可視性を提供します。</span><span class="sxs-lookup"><span data-stu-id="68b81-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="68b81-110">勘定カテゴリ、予算コード、主勘定、主勘定の説明、または差異の原因をより良く理解するための会計年度期間ごとに、今年度の予算を分析できます。</span><span class="sxs-lookup"><span data-stu-id="68b81-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="68b81-111">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="68b81-111">Accessing the Power BI content</span></span>
<span data-ttu-id="68b81-112">**実績対予算** Power BI コンテンツからのレポートは、**元帳予算と予測**、および **CFO** ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="68b81-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="68b81-113">Power BI コンテンツに含まれるレポート</span><span class="sxs-lookup"><span data-stu-id="68b81-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="68b81-114">次の表は、**実績対予算** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="68b81-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="68b81-115">レポート </span><span class="sxs-lookup"><span data-stu-id="68b81-115">Report</span></span>                      | <span data-ttu-id="68b81-116">メトリックス</span><span class="sxs-lookup"><span data-stu-id="68b81-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="68b81-117">経費 - 実績対予算</span><span class="sxs-lookup"><span data-stu-id="68b81-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="68b81-118">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="68b81-118">Total expenses this year</span></span></li><li><span data-ttu-id="68b81-119">今年度の合計経費予算</span><span class="sxs-lookup"><span data-stu-id="68b81-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="68b81-120">収益 - 実績対予算</span><span class="sxs-lookup"><span data-stu-id="68b81-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="68b81-121">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="68b81-121">Total revenue this year</span></span></li><li><span data-ttu-id="68b81-122">今年度の予算の総収益</span><span class="sxs-lookup"><span data-stu-id="68b81-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="68b81-123">支出</span><span class="sxs-lookup"><span data-stu-id="68b81-123">Expense</span></span>                     | <ul><li><span data-ttu-id="68b81-124">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="68b81-124">Total expenses this year</span></span></li><li><span data-ttu-id="68b81-125">予算に基づく経費目標</span><span class="sxs-lookup"><span data-stu-id="68b81-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="68b81-126">収益</span><span class="sxs-lookup"><span data-stu-id="68b81-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="68b81-127">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="68b81-127">Total revenue this year</span></span></li><li><span data-ttu-id="68b81-128">予算に基づく収益目標</span><span class="sxs-lookup"><span data-stu-id="68b81-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="68b81-129">純利益</span><span class="sxs-lookup"><span data-stu-id="68b81-129">Net income</span></span>                  | <ul><li><span data-ttu-id="68b81-130">今年度の純利益</span><span class="sxs-lookup"><span data-stu-id="68b81-130">Net income this year</span></span></li><li><span data-ttu-id="68b81-131">予算に基づく目標純利益</span><span class="sxs-lookup"><span data-stu-id="68b81-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="68b81-132">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="68b81-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="68b81-133">エンティティ</span><span class="sxs-lookup"><span data-stu-id="68b81-133">Entity</span></span>                    | <span data-ttu-id="68b81-134">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="68b81-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="68b81-135">総勘定元帳アクティビティ</span><span class="sxs-lookup"><span data-stu-id="68b81-135">General Ledger Activities</span></span> | <span data-ttu-id="68b81-136">総勘定元帳のトランザクション金額</span><span class="sxs-lookup"><span data-stu-id="68b81-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="68b81-137">予算アクティビティ</span><span class="sxs-lookup"><span data-stu-id="68b81-137">Budget Activities</span></span>         | <span data-ttu-id="68b81-138">予算登録のトランザクション金額</span><span class="sxs-lookup"><span data-stu-id="68b81-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="68b81-139">主勘定</span><span class="sxs-lookup"><span data-stu-id="68b81-139">Main Accounts</span></span>             | <span data-ttu-id="68b81-140">レポートをフィルター処理する主勘定</span><span class="sxs-lookup"><span data-stu-id="68b81-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="68b81-141">会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="68b81-141">Fiscal Calendars</span></span>          | <span data-ttu-id="68b81-142">レポートをフィルター処理する会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="68b81-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="68b81-143">元帳</span><span class="sxs-lookup"><span data-stu-id="68b81-143">Ledgers</span></span>                   | <span data-ttu-id="68b81-144">現在の元帳へのレポートをフィルター処理するために使用される元帳</span><span class="sxs-lookup"><span data-stu-id="68b81-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="68b81-145">予算コード</span><span class="sxs-lookup"><span data-stu-id="68b81-145">Budget Codes</span></span>              | <span data-ttu-id="68b81-146">レポートをフィルター処理する予算コード</span><span class="sxs-lookup"><span data-stu-id="68b81-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="68b81-147">法人</span><span class="sxs-lookup"><span data-stu-id="68b81-147">Legal Entities</span></span>            | <span data-ttu-id="68b81-148">現在の法人へのレポートをフィルター処理するために使用される法人</span><span class="sxs-lookup"><span data-stu-id="68b81-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]