---
title: コール センター注文の作成
description: この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dce2fdd9d91c2bd867f0455573733aefb0796fa7
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107355"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="7ae2c-103">コール センター注文の作成</span><span class="sxs-lookup"><span data-stu-id="7ae2c-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ae2c-104">この手順では、顧客の検索、新しい注文の作成、製品の検索、および顧客から支払を回収する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="7ae2c-105">この手順では、デモ データの会社 USRT を使用して、販売注文の担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="7ae2c-106">前提条件: 手順を完了するユーザーが、コール センター ユーザーとして設定され、Fabrikam Semi-Annual Catalog が少なくとも 1 つのソースコードと共に公開されています。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="7ae2c-107">**Retail と Commerce \> 顧客 \> 顧客サービス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="7ae2c-108">**検索文字列** には、顧客を検索するための検索条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-108">For **SearchText** , enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="7ae2c-109">この手順の例では、「Karen」を入力し、 **タブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="7ae2c-110">検索 を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-110">Select Search.</span></span>
    * <span data-ttu-id="7ae2c-111">デモ データに「Karen」という名前の顧客が 1 人だけいるため、それが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="7ae2c-112">**新しい販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="7ae2c-113">**販売注文** ヘッダー セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="7ae2c-114">カタログのソース コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="7ae2c-115">有効なソース・コードがない場合、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="7ae2c-116">**明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-116">Select **Add line**.</span></span>
8. <span data-ttu-id="7ae2c-117">**品目番号** では、品目の検索用語を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-117">For **Item number** , enter the item search term.</span></span>
    * <span data-ttu-id="7ae2c-118">このサンプルの手順については、品目番号の一部の「8111」を入力し、タブをクリックします。すると、品目の検索ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="7ae2c-119">販売注文に追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="7ae2c-120">販売数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="7ae2c-121">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-121">Select **Create**.</span></span>
12. <span data-ttu-id="7ae2c-122">顧客支払を取得するために、 **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="7ae2c-123">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-123">Select **Add**.</span></span>
    * <span data-ttu-id="7ae2c-124">[追加] リンクは、[支払] タブにあります。[支払] タブが折りたたまれている場合、展開します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="7ae2c-125">支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-125">Select the payment method.</span></span>
    * <span data-ttu-id="7ae2c-126">この手順では、支払方法は現金を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="7ae2c-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-127">Close the page.</span></span>
16. <span data-ttu-id="7ae2c-128">金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-128">Enter the amount.</span></span>
    * <span data-ttu-id="7ae2c-129">この手順では、販売注文の概要ページに表示される注文の残高と同じ金額を、金額フィールドの左側に入力します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="7ae2c-130">全額支払われるように注文を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="7ae2c-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-131">Select **OK**.</span></span>
18. <span data-ttu-id="7ae2c-132">**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ae2c-132">Select **Submit**.</span></span>

