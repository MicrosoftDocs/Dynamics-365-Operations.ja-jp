---
title: RFQ のスコア方法の作成
description: この手順では、スコア方法を作成する方法を示します。
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8657098519391ee488025e175e1499c58a55ce
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204657"
---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="2a384-103">RFQ のスコア方法の作成</span><span class="sxs-lookup"><span data-stu-id="2a384-103">Create a scoring method for RFQs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a384-104">この手順では、スコア方法を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2a384-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="2a384-105">スコア方法は、見積依頼 (RFQ) の回答として送信する入札を比較するために使用できる一連の基準です。</span><span class="sxs-lookup"><span data-stu-id="2a384-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="2a384-106">たとえば、仕入先の過去のパフォーマンスを評価、環境に優しい会社かどうか、良い協力者であるかを評価、または価格に基づく入札の比較をする場合があります。</span><span class="sxs-lookup"><span data-stu-id="2a384-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="2a384-107">入札タイプの RFQs の規定のスコア方法として、スコア方法を入札タイプと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2a384-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="2a384-108">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="2a384-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="2a384-109">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="2a384-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="2a384-110">[調達] > [設定] > [見積依頼] > [スコア方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a384-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="2a384-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a384-111">Click New.</span></span>
3. <span data-ttu-id="2a384-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2a384-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2a384-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a384-114">Click Save.</span></span>
6. <span data-ttu-id="2a384-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a384-115">Click New.</span></span>
7. <span data-ttu-id="2a384-116">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="2a384-117">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="2a384-118">この説明は、スコア方法が RFQ に対して選択された場合、スコア方法の名前とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a384-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="2a384-119">[範囲の開始] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="2a384-120">調達担当者がスコアとして入力できる範囲を制限します。</span><span class="sxs-lookup"><span data-stu-id="2a384-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="2a384-121">RFQ に複数のスコア基準がある場合、入力した基準が相互に追加され、さらに入札が比較できるよう合計が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="2a384-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="2a384-122">[範囲の終了] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="2a384-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2a384-123">Click New.</span></span>
12. <span data-ttu-id="2a384-124">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="2a384-125">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="2a384-126">[範囲の開始] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="2a384-127">[範囲の終了] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a384-127">In the Range to field, enter a number.</span></span>

