---
title: 需要予測を計算するときに、トランザクション履歴データから異常値を削除します。
description: この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。 異常値を除外すると、予測の精度が向上します。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44be713a1049e90618392d028c81e974841b348
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886826"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="aa064-104">需要予測を計算するときに、トランザクション履歴データから異常値を削除します。</span><span class="sxs-lookup"><span data-stu-id="aa064-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa064-105">この記事では、需要予測の計算に使用される履歴データから異常値を除外する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aa064-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="aa064-106">異常値を除外すると、予測の精度が向上します。</span><span class="sxs-lookup"><span data-stu-id="aa064-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="aa064-107">異常値を除外すると、予測の精度が向上します。</span><span class="sxs-lookup"><span data-stu-id="aa064-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="aa064-108">これはオプションのタスクです。</span><span class="sxs-lookup"><span data-stu-id="aa064-108">This is an optional task.</span></span> <span data-ttu-id="aa064-109">次にプロセスの概要について示します。</span><span class="sxs-lookup"><span data-stu-id="aa064-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="aa064-110">**マスター プラン** &gt; **設定** &gt; **需要予測** &gt; **異常値の削除** の順にクリックして、クエリを使用して除外するトランザクションを選択できる **異常値の削除** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="aa064-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="aa064-111">クエリを適用する会社を選択し、名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="aa064-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="aa064-112">**クエリの日付** フィールドには、現在の日付が自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="aa064-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="aa064-113">**有効** チェック ボックスをオンにし、クエリによって検索されたトランザクションを履歴データから除外します。</span><span class="sxs-lookup"><span data-stu-id="aa064-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="aa064-114">この設定は、ベースライン予測を作成するときに適用されます。</span><span class="sxs-lookup"><span data-stu-id="aa064-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="aa064-115">**異常値削除クエリ** ページで、ベースライン予測を計算するときに、除外するトランザクションを定義する基準を追加、削除、および選択できます。</span><span class="sxs-lookup"><span data-stu-id="aa064-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="aa064-116">たとえば、除外する特定の品目または注文トランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="aa064-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="aa064-117">**トランザクションの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa064-117">Click **Display transactions**.</span></span> <span data-ttu-id="aa064-118">**異常値トランザクション** ページに、クエリで定義した条件を満たし、需要予測の計算時に履歴データから除外されるトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa064-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="aa064-119">**注記:** 既存のクエリに基づいたクエリの作成もできます。</span><span class="sxs-lookup"><span data-stu-id="aa064-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="aa064-120">コピーするクエリを選択してから **重複** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa064-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="aa064-121">**クエリ日付** フィールドがバージョンを識別します。</span><span class="sxs-lookup"><span data-stu-id="aa064-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="aa064-122">クエリをそのまま使用するか、**クエリの編集** をクリックして基準を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="aa064-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="aa064-123">必要に応じて新しいクエリの名前と説明を変更できます。</span><span class="sxs-lookup"><span data-stu-id="aa064-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="aa064-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aa064-124">Additional resources</span></span>
--------

[<span data-ttu-id="aa064-125">需要予測の概要</span><span class="sxs-lookup"><span data-stu-id="aa064-125">Demand forecasting overview</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="aa064-126">予測精度の監視</span><span class="sxs-lookup"><span data-stu-id="aa064-126">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



