--- 
title: "製品コンフィギュレーション モデルの承認"
description: "この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。"
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa4548d3017246cbe49e2613f8990df6ea1c368b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="3976c-103">製品コンフィギュレーション モデルの承認</span><span class="sxs-lookup"><span data-stu-id="3976c-103">Approve a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3976c-104">この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="3976c-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="3976c-105">この手順では、デモ データの会社 USMF の [ハイエンド スピーカー] モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="3976c-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="3976c-106">このモデルは既に承認済ですが、手順は、プロセス全体について説明します。</span><span class="sxs-lookup"><span data-stu-id="3976c-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="3976c-107">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3976c-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3976c-108">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3976c-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="3976c-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3976c-110">この手順の [ハイエンド スピーカー] モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="3976c-111">[バージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3976c-111">Click Versions.</span></span>
5. <span data-ttu-id="3976c-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3976c-112">Click New.</span></span>
6. <span data-ttu-id="3976c-113">[製品番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="3976c-114">製品への参照は、製品コンフィギュレーション モデルのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="3976c-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="3976c-115">制約ベースのコンフィギュレーション テクノロジがある製品マスターのみこの一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3976c-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="3976c-116">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3976c-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="3976c-117">製品モデル バージョンがある場合選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="3976c-118">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3976c-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3976c-119">この製品モデル バージョンの有効期限が切れる場合は終了日を、または [なし] を選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="3976c-120">[承認] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3976c-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="3976c-121">[承認者] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="3976c-122">工程の使用のために製品モデルの承認を担当する個人を選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="3976c-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3976c-123">Click OK.</span></span>
12. <span data-ttu-id="3976c-124">[価格決定方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3976c-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="3976c-125">製品モデルのバージョンを有効化します。</span><span class="sxs-lookup"><span data-stu-id="3976c-125">Activate the product model version.</span></span> <span data-ttu-id="3976c-126">1 度に、1 つの製品モデルに対して、1 つの製品のみ有効にできます。</span><span class="sxs-lookup"><span data-stu-id="3976c-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="3976c-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3976c-127">Close the page.</span></span>

