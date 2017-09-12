--- 
title: "コール センター注文の作成"
description: "この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 62f88cc2e28405a9d2eb43819fb09d83a64658b6
ms.contentlocale: ja-jp
ms.lasthandoff: 07/28/2017

---
# <a name="create-call-center-orders"></a><span data-ttu-id="88fea-103">コール センター注文の作成</span><span class="sxs-lookup"><span data-stu-id="88fea-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="88fea-104">この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88fea-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="88fea-105">この手順では、デモ データの会社 USRT を使用して、販売注文の担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="88fea-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="88fea-106">前提条件: 手順を完了するユーザーが、コール センター ユーザーとして設定され、Fabrikam Semi-Annual Catalog が少なくとも 1 つのソースコードと共に公開されています。</span><span class="sxs-lookup"><span data-stu-id="88fea-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="88fea-107">[小売りとコマース] > [顧客] > [顧客サービス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="88fea-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="88fea-108">[検索文字列] フィールドで、顧客を検索するための検索条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="88fea-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="88fea-109">この手順の例では、「開発者」を入力し、タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="88fea-110">[検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-110">Click Search.</span></span>
    * <span data-ttu-id="88fea-111">デモ データに開発者という名前の顧客が一人だけあるため、それが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="88fea-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="88fea-112">[新しい販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-112">Click New sales order.</span></span>
5. <span data-ttu-id="88fea-113">[販売注文ヘッダー] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="88fea-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="88fea-114">カタログのソース コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="88fea-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="88fea-115">有効なソース・コードがない場合、ソース フィールドを閉じ、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="88fea-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="88fea-116">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-116">Click Add line.</span></span>
8. <span data-ttu-id="88fea-117">[品目番号] フィールドで、品目の検索用語を入力します。</span><span class="sxs-lookup"><span data-stu-id="88fea-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="88fea-118">このサンプルの手順については、品目番号の一部の「8111」を入力し、タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-118">For this sample procedure enter a partial item number of '8111' and press tab.</span></span> <span data-ttu-id="88fea-119">品目の検索ウィンドウがポップアップ表示されます。</span><span class="sxs-lookup"><span data-stu-id="88fea-119">This will pop up the item search window.</span></span>  
9. <span data-ttu-id="88fea-120">販売注文に追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="88fea-120">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="88fea-121">販売数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="88fea-121">Enter the sales quantity.</span></span>
11. <span data-ttu-id="88fea-122">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-122">Click Create.</span></span>
12. <span data-ttu-id="88fea-123">顧客支払を取得するために、[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-123">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="88fea-124">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-124">Click Add.</span></span>
    * <span data-ttu-id="88fea-125">[追加] リンクは、[支払] タブにあります。</span><span class="sxs-lookup"><span data-stu-id="88fea-125">The Add link is in the Payments tab.</span></span> <span data-ttu-id="88fea-126">[支払] タブが折りたたまれている場合、展開します。</span><span class="sxs-lookup"><span data-stu-id="88fea-126">Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="88fea-127">支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="88fea-127">Select the payment method.</span></span>
    * <span data-ttu-id="88fea-128">この手順では、支払方法は現金を選択します。</span><span class="sxs-lookup"><span data-stu-id="88fea-128">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="88fea-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88fea-129">Close the page.</span></span>
16. <span data-ttu-id="88fea-130">金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="88fea-130">Enter the amount.</span></span>
    * <span data-ttu-id="88fea-131">この手順では、販売注文の概要ページに表示される注文の残高と同じ金額を、金額フィールドの左側に入力します。</span><span class="sxs-lookup"><span data-stu-id="88fea-131">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="88fea-132">全額支払われるように注文を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="88fea-132">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="88fea-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-133">Click OK.</span></span>
18. <span data-ttu-id="88fea-134">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88fea-134">Click Submit.</span></span>


