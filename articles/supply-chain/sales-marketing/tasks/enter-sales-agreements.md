---
title: 販売契約書の入力
description: このトピックでは、一定期間に特別割引で、同意した金額の製品を購入するよう顧客の 1 人にコミットする販売契約書を作成する方法を示します。
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06d251992c7facca471ac893e5a0fee333e0cbed
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148656"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="c82f6-103">販売契約書の入力</span><span class="sxs-lookup"><span data-stu-id="c82f6-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c82f6-104">このトピックでは、一定期間に特別割引で、同意した金額の製品を購入するよう顧客の 1 人にコミットする販売契約書を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="c82f6-105">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="c82f6-106">販売契約書ヘッダーの設定</span><span class="sxs-lookup"><span data-stu-id="c82f6-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="c82f6-107">ナビゲーション ウィンドウで、**モジュール > 販売とマーケティング > 販売契約書 > 販売契約書**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="c82f6-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-108">Select **New**.</span></span>
3. <span data-ttu-id="c82f6-109">**顧客アカウント** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="c82f6-110">**販売契約書の分類**フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="c82f6-111">**一般**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="c82f6-112">**既定の確約**フィールドで、**製品価値の確約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="c82f6-113">確約タイプは、契約が満了する方法を定義する契約に割り当てる必要がある必須の基準です。</span><span class="sxs-lookup"><span data-stu-id="c82f6-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="c82f6-114">4 つの定義済みのタイプにより、数量または値として表現される、顧客の確約のターゲットを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="c82f6-115">数量の確約タイプは特定の製品にのみ適用されますが、値ベース タイプは特定および不特定の製品の両方の販売に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="c82f6-116">**有効期限**フィールドで、契約期限が切れる将来の日付を設定します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="c82f6-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="c82f6-118">製品価値確約明細行の設定</span><span class="sxs-lookup"><span data-stu-id="c82f6-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="c82f6-119">**明細行の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-119">Select **Add line**.</span></span>
2. <span data-ttu-id="c82f6-120">**品目番号**フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="c82f6-121">契約のために選択した確約のタイプは、契約項目に入力できる情報の種類に影響します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="c82f6-122">たとえば、値ベースの契約の場合は、顧客が商品を購入するためにコミットする合計正味金額 (合意された通貨で) を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c82f6-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="c82f6-123">この例では、顧客が製品の特定の値を購入する契約を作成しているため、明細行の **数量** と **単位** のフィールドを使用できません。</span><span class="sxs-lookup"><span data-stu-id="c82f6-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="c82f6-124">**正味金額**フィールドに、顧客が購入することを確定した金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="c82f6-125">**割引率**フィールドでは、この契約にリンクされている顧客の販売注文明細行に適用されるパーセンテージ値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="c82f6-126">**行の詳細**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="c82f6-127">**最大値の適用**フィールドで、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="c82f6-128">**最大値の適用**の選択は、確約の特別価格を使用するすべての販売注文明細行の合計金額を意味し、割引や支払条件は確約で指定された金額を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="c82f6-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="c82f6-129">最小および最大のリリースの金額は、選択した契約を使用する各販売注文で販売する必要がある値の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="c82f6-130">**販売契約書ヘッダー**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="c82f6-131">契約のステータスが**有効**に設定されていない限り、販売注文はその契約に関連付けることはできません。したがって販売注文は、その契約のフルフィルメントに使用されません。</span><span class="sxs-lookup"><span data-stu-id="c82f6-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="c82f6-132">ステータスをこの段階で手動で変更できます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="c82f6-133">ただし、ステータスは通常、顧客の契約を確認するときに変更されます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="c82f6-134">アクション ペインで、**販売契約書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="c82f6-135">**確認**を確認します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-135">Select **Confirmation**.</span></span> <span data-ttu-id="c82f6-136">**契約を有効としてマークします**オプションが、**はい**に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c82f6-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="c82f6-137">**レポートの印刷**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="c82f6-138">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c82f6-138">Select **OK**.</span></span>
12. <span data-ttu-id="c82f6-139">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-139">Close the page.</span></span> <span data-ttu-id="c82f6-140">これで、契約は有効になります。</span><span class="sxs-lookup"><span data-stu-id="c82f6-140">The agreement is now effective.</span></span> <span data-ttu-id="c82f6-141">顧客の注文を契約にリンクすることを開始して、確定済ターゲットに対して相殺できます。</span><span class="sxs-lookup"><span data-stu-id="c82f6-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

