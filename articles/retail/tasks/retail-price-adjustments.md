--- 
title: "小売価格調整の作成"
description: "この手順では、小売価格調整の作成を説明します。"
author: josaw1
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 6dd4e12008838460c0bb0ade907ea78d06c80fed
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-retail-price-adjustments"></a><span data-ttu-id="10387-103">小売価格調整の作成</span><span class="sxs-lookup"><span data-stu-id="10387-103">Create retail price adjustments</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="10387-104">この手順では、小売価格調整の作成を説明します。</span><span class="sxs-lookup"><span data-stu-id="10387-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="10387-105">小売の価格調整では、品目の販売価格を直接設定できます。また、基準販売価格、あるいは売買契約の販売価格を変更できます。</span><span class="sxs-lookup"><span data-stu-id="10387-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="10387-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="10387-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="10387-107">[価格設定および割引の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="10387-108">[価格調整] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="10387-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-109">Click New.</span></span>
    * <span data-ttu-id="10387-110">ここで、小売割引、小売価格調整、売買契約仕訳帳、およびカテゴリの価格決定ルールを含む、よく使用する価格および割引ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="10387-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="10387-111">[価格調整] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="10387-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="10387-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="10387-113">[明細行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="10387-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="10387-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-114">Click Add.</span></span>
    * <span data-ttu-id="10387-115">この例の場合、[製品] フィールドに「81126」と入力します。</span><span class="sxs-lookup"><span data-stu-id="10387-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="10387-116">次に、[割引率] フィールドに「10.0」を入力します。</span><span class="sxs-lookup"><span data-stu-id="10387-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="10387-117">割引率のタイプの価格調整では、基準販売価格または売買契約の販売価格を削減します。</span><span class="sxs-lookup"><span data-stu-id="10387-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="10387-118">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-118">Click Add.</span></span>
    * <span data-ttu-id="10387-119">この例の場合、[製品] フィールドに「81125」と入力します。</span><span class="sxs-lookup"><span data-stu-id="10387-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="10387-120">その後、[割引方法] フィールドで [現金割引金額] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10387-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="10387-121">最後に、[現金割引金額] フィールドに「5.0」を入力します。</span><span class="sxs-lookup"><span data-stu-id="10387-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="10387-122">[現金割引金額] 割引タイプは、基準価格または売買契約の価格から差し引かれる金額です。</span><span class="sxs-lookup"><span data-stu-id="10387-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="10387-123">[価格グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-123">Click Price groups.</span></span>
    * <span data-ttu-id="10387-124">[価格グループ] フィールドで [RP-Houston] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10387-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="10387-125">これにより、ヒューストン店舗に価格調整が関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="10387-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="10387-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-126">Click Save.</span></span>
11. <span data-ttu-id="10387-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="10387-127">Close the page.</span></span>
12. <span data-ttu-id="10387-128">[ステータス] フィールドで [有効] を選択します。</span><span class="sxs-lookup"><span data-stu-id="10387-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="10387-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="10387-129">Click Save.</span></span>
14. <span data-ttu-id="10387-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="10387-130">Close the page.</span></span>
15. <span data-ttu-id="10387-131">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="10387-131">Refresh the page.</span></span>


