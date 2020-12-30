---
title: 展開のトレースを使用する
description: この記事は、注文の展開結果の背後にある原因を参照して追跡する方法について説明します。
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88e777d69c9da8a19c186bca3ca591e59af232f0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431737"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="9121c-103">展開のトレースを使用する</span><span class="sxs-lookup"><span data-stu-id="9121c-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9121c-104">この記事は、注文の展開結果の背後にある原因を参照して追跡する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9121c-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="9121c-105">追跡を有効にすることで、特定の注文の展開結果に関与する要因を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9121c-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="9121c-106">次の例は、追跡情報の使用方法です。</span><span class="sxs-lookup"><span data-stu-id="9121c-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="9121c-107">サプライ チェーンおよび在庫引当を最適化する、計画オーダーのアクション間の関係を表示します。</span><span class="sxs-lookup"><span data-stu-id="9121c-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="9121c-108">既に承認された注文との関係を表示します。</span><span class="sxs-lookup"><span data-stu-id="9121c-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="9121c-109">自動的に確定する派生要求を絞り込み、より正確にオーダーの優先順位付けをします。</span><span class="sxs-lookup"><span data-stu-id="9121c-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="9121c-110">計画のパラメーターが最適であるかどうか、プランの結果をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="9121c-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="9121c-111">注文の生産日付、量、および優先順位などの情報を決定した方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="9121c-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="9121c-112">選択した注文の将来およびアクションに関する詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9121c-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="9121c-113">**展開** ページにある上部ウィンドウの **説明** タブで追跡情報を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9121c-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="9121c-114">追跡はオーダーを展開するときに発生します。</span><span class="sxs-lookup"><span data-stu-id="9121c-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="9121c-115">オーダーの追跡を開始するには、**更新** をクリックし、**トレースの有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9121c-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="9121c-116">特定の情報のログを検索するには **テキストの検索** フィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9121c-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="9121c-117">検索結果はツリーで強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="9121c-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9121c-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9121c-118">Additional resources</span></span>
--------

[<span data-ttu-id="9121c-119">マスター プランの概要</span><span class="sxs-lookup"><span data-stu-id="9121c-119">Master plans overview</span></span>](master-plans.md)



