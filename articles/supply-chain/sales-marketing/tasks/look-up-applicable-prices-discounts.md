---
title: 適用できる価格および割引の検索
description: この手順は、特定の顧客に対して現在有効な製品の価格や割引を、販売注文を作成せずに検索する方法を示します。
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37893b914f02f34071e1d8951a5df993e053f1b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255016"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="a2f4f-103">適用できる価格および割引の検索</span><span class="sxs-lookup"><span data-stu-id="a2f4f-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2f4f-104">この手順は、特定の顧客に対して現在有効な製品の価格や割引を、販売注文を作成せずに検索する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="a2f4f-105">この手順では、特定の例について説明します。必要な値を選択するには、USMF のデモ会社を使用したこの例に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="a2f4f-106">適用できる価格の検索</span><span class="sxs-lookup"><span data-stu-id="a2f4f-106">Find the applicable price</span></span>
1. <span data-ttu-id="a2f4f-107">[販売とマーケティング] > [価格と割引] > [価格の検索] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="a2f4f-108">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a2f4f-109">リストで、顧客 US-001 を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="a2f4f-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a2f4f-111">[品目番号] フィールドに、'T0004' を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="a2f4f-112">既定では、[数量] フィールドは 1 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="a2f4f-113">ただし、顧客が対象製品に対して予定している注文のサイズがわかっている場合は、代わりにこの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="a2f4f-114">この情報は、顧客との売買契約に数量の区分があるかどうかに関連しています。つまり、製品の価格は購買最小数量に依存します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="a2f4f-115">[日付] フィールドで、顧客が注文を発注する予定の日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="a2f4f-116">日付には、今日、または将来の任意の日付を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="a2f4f-117">指定された数量で選択した日付に選択した顧客によって購入された場合、システムは選択した製品で有効になる価格を返します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="a2f4f-118">この例では、今日、顧客 US-001 が製品 T0004 を 1 単位購入した場合、その製品は 1 単位 350 CAD に変更されます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="a2f4f-119">この価格は、既存で有効な、顧客との売買契約から取得されます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="a2f4f-120">ページの他のフィールドでは、(製品マスターで設定されている場合) 製品価格と製品原価、および計算される収益性に関する詳細情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="a2f4f-121">[関連製品バリアントの表示] オプションを選択した場合、製品バリアントに追加の売買契約があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="a2f4f-122">[関連製品バリアントの表示] チェック ボックスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="a2f4f-123">製品バリアントの一覧が、分析コードに関する情報とともに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="a2f4f-124">リストで、白色を表す明細行にマークを付けます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="a2f4f-125">製品価格は、分析コードごとに指定されていなかった場合、以前に表示されたものとは異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="a2f4f-126">[販売価格の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-126">Click View sales prices.</span></span>
    * <span data-ttu-id="a2f4f-127">[価格 (販売)] ページには、バリアントを含めた、製品に適用可能なすべての売買契約が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="a2f4f-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="a2f4f-129">適用できる割引の検索</span><span class="sxs-lookup"><span data-stu-id="a2f4f-129">Find the applicable discount</span></span>
<span data-ttu-id="a2f4f-130">[顧客口座] フィールドには顧客番号 US-001 が含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="a2f4f-131">[品目番号] フィールドに、'T0012' を入力します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="a2f4f-132">[数量] フィールドが 1 に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="a2f4f-133">製品 T0012 に表示される次の価格決定の詳細は、複数の売買契約から取得されます: 単価は 1,000 CAD で、割引率は 5 です。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="a2f4f-134">数量を '20' に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="a2f4f-135">注文数量の増加は、5 から 7% に変更予定の顧客に対する行割引によるものです。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="a2f4f-136">正味金額は、単価、割引、合計数量に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="a2f4f-137">[行割引の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-137">Click View line discount.</span></span>
    * <span data-ttu-id="a2f4f-138">製品 T0012 には、2 つの行割引契約があります。つまり、1 から 10 の注文明細行数量で 5% の割引が指定され、10 以上では注文数量が 7％ 割引されています。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="a2f4f-139">割引は、製品グループ、この例では、製品 T0012 が所属するグループ コード 01 に適用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="a2f4f-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2f4f-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]