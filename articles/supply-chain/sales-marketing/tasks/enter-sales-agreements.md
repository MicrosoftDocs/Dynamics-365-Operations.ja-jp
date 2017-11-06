--- 
title: "販売契約書の入力"
description: "この手順では、一定期間に特別割引で、同意した金額の製品を購入するよう顧客の 1 人にコミットする販売契約書を作成する方法を示します。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="411fc-103">販売契約書の入力</span><span class="sxs-lookup"><span data-stu-id="411fc-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="411fc-104">この手順では、一定期間に特別割引で、同意した金額の製品を購入するよう顧客の 1 人にコミットする</span><span class="sxs-lookup"><span data-stu-id="411fc-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="411fc-105">販売契約書を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="411fc-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="411fc-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="411fc-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="411fc-107">販売契約書ヘッダーの設定</span><span class="sxs-lookup"><span data-stu-id="411fc-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="411fc-108">[販売とマーケティング] > [販売契約書] > [販売契約書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="411fc-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="411fc-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-109">Click New.</span></span>
3. <span data-ttu-id="411fc-110">[顧客口座] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="411fc-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="411fc-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="411fc-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="411fc-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="411fc-113">[販売契約書の分類] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="411fc-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="411fc-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="411fc-115">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="411fc-115">Expand the General section.</span></span>
9. <span data-ttu-id="411fc-116">[既定の確約] フィールドで、[製品価値確約] を選択します。</span><span class="sxs-lookup"><span data-stu-id="411fc-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="411fc-117">確約タイプは、契約が満了する方法を定義する契約に割り当てる必要がある必須の基準です。</span><span class="sxs-lookup"><span data-stu-id="411fc-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="411fc-118">4 つの定義済みのタイプにより、数量または値として表現される、顧客の確約のターゲットを設定できます。</span><span class="sxs-lookup"><span data-stu-id="411fc-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="411fc-119">数量の確約タイプは特定の製品にのみ適用されますが、値ベース タイプは特定および不特定の製品の両方の販売に適用されます。</span><span class="sxs-lookup"><span data-stu-id="411fc-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="411fc-120">[有効期限] フィールドで、契約の期限が切れる将来の日付を設定します。</span><span class="sxs-lookup"><span data-stu-id="411fc-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="411fc-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="411fc-122">製品価値確約明細行の設定</span><span class="sxs-lookup"><span data-stu-id="411fc-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="411fc-123">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-123">Click Add line.</span></span>
2. <span data-ttu-id="411fc-124">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="411fc-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="411fc-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="411fc-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="411fc-126">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="411fc-127">契約のために選択した確約のタイプは、契約項目に入力できる情報の種類に影響します。</span><span class="sxs-lookup"><span data-stu-id="411fc-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="411fc-128">たとえば、値ベースの契約の場合は、顧客が商品を購入するためにコミットする合計正味金額 (合意された通貨で) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="411fc-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="411fc-129">この例では、顧客が製品の特定の値を購入する契約を作成しているため、明細行の [数量] および [単位] フィールドは使用できません。</span><span class="sxs-lookup"><span data-stu-id="411fc-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="411fc-130">[正味金額] フィールドに、顧客が購入することを確定した金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="411fc-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="411fc-131">[割引率] フィールドでは、この契約にリンクされている顧客の販売注文明細行に適用されるパーセンテージ値を入力します。</span><span class="sxs-lookup"><span data-stu-id="411fc-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="411fc-132">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="411fc-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="411fc-133">[最大値の適用] フィールドで [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="411fc-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="411fc-134">[最大値の適用] の選択は、確約の特別価格を使用するすべての販売注文明細行の合計金額を意味し、割引や支払条件は確約で指定された金額を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="411fc-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="411fc-135">最小および最大のリリースの金額は、選択した契約を使用する各販売注文で販売する必要がある値の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="411fc-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="411fc-136">[販売契約書ヘッダー] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="411fc-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="411fc-137">契約のステータスが [有効] に設定されていない限り、販売注文はその契約に関連付けることはできません。したがって販売注文は、その契約のフルフィルメントに使用されません。</span><span class="sxs-lookup"><span data-stu-id="411fc-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="411fc-138">ステータスをこの段階で手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="411fc-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="411fc-139">ただし、ステータスは通常、顧客の契約を確認するときに変更されます。</span><span class="sxs-lookup"><span data-stu-id="411fc-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="411fc-140">[アクション ペイン] で、[販売契約書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="411fc-141">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-141">Click Confirmation.</span></span>
    * <span data-ttu-id="411fc-142">[契約を有効としてマークします] オプションが [はい] に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="411fc-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="411fc-143">[レポートの印刷] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="411fc-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="411fc-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="411fc-144">Click OK.</span></span>
14. <span data-ttu-id="411fc-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="411fc-145">Close the page.</span></span>
    * <span data-ttu-id="411fc-146">契約は現在有効であり、顧客の注文を契約にリンクすることを開始して、確定済ターゲットに対して相殺できます。</span><span class="sxs-lookup"><span data-stu-id="411fc-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  

