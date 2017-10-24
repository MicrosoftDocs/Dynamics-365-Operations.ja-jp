--- 
title: "購買契約書の作成"
description: "この手順では、購買契約書の作成方法について説明しています。"
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="d3cdb-103">購買契約書の作成</span><span class="sxs-lookup"><span data-stu-id="d3cdb-103">Create a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3cdb-104">この手順では、購買契約書の作成方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="d3cdb-105">これは通常、購買マネージャが行います。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="d3cdb-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d3cdb-107">開始する前に、購買契約書の分類を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="d3cdb-108">契約を作成すると、発注書の作成時にそれを使用できます。また、販売契約条件がヘッダーまたは任意の明細行に、その契約によって影響される順でコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="d3cdb-109">新しい購買契約の作成</span><span class="sxs-lookup"><span data-stu-id="d3cdb-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="d3cdb-110"> [調達] > [購買契約書] > [購買契約書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="d3cdb-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-111">Click New.</span></span>
3. <span data-ttu-id="d3cdb-112">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d3cdb-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d3cdb-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3cdb-115">[購買契約の分類] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d3cdb-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d3cdb-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d3cdb-118">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-118">Expand the General section.</span></span>
10. <span data-ttu-id="d3cdb-119">[有効期限] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="d3cdb-120">この有効期限は、すべての確約明細行の既定値であり、各特定の確約の有効期間を決定します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="d3cdb-121">[ドキュメント タイトル] フィールドに、購買契約書の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="d3cdb-122">[既定の確約] フィールドを、[製品数量確約] に設定したままにします (または、これに設定されていない場合は変更します)。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="d3cdb-123">確約の既定値により、契約項目のオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="d3cdb-124">契約項目を作成する際に新しい確約タイプが必要な場合は、ヘッダーの確約既定値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="d3cdb-125">確約には、次の 4 つのタイプがあります。製品数量確約 - 製品の特定数量のためのものです。製品価値確約 - 製品の特定の通貨金額のためのものです。製品カテゴリ価値確約 - 金額がカタログ品目またはカタログ以外の品目である、特定の通貨金額調達カテゴリのためのものです。価値確約 - すべての製品または調達カテゴリにより満たせる特定の通貨金額のためのものです。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="d3cdb-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="d3cdb-127">確約の追加</span><span class="sxs-lookup"><span data-stu-id="d3cdb-127">Add a commitment</span></span>
1. <span data-ttu-id="d3cdb-128">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-128">Click Add line.</span></span>
2. <span data-ttu-id="d3cdb-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d3cdb-130">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d3cdb-131">確約を追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="d3cdb-132">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d3cdb-133">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="d3cdb-134">これは、仕入先から購入することに合意した合計数量です。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="d3cdb-135">[単価] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="d3cdb-136">[明細行の詳細] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="d3cdb-137">[最大値の適用] オプションを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="d3cdb-138">[最大値の適用] オプションは、確約の使用を制限します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="d3cdb-139">購入できるのは、明細行の [数量] フィールドで指定された数量までです。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="d3cdb-140">[明細行の詳細] セクションを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="d3cdb-141">ヘッダー条件の追加</span><span class="sxs-lookup"><span data-stu-id="d3cdb-141">Add header conditions</span></span>
1. <span data-ttu-id="d3cdb-142">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="d3cdb-143">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-143">Click Change view.</span></span>
3. <span data-ttu-id="d3cdb-144">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-144">Click Header view.</span></span>
4. <span data-ttu-id="d3cdb-145">[条件] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="d3cdb-146">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3cdb-147">仕入先からの支払条件が既定によりここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="d3cdb-148">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d3cdb-149">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d3cdb-150">[荷渡方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d3cdb-151">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d3cdb-152">[配送条件] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d3cdb-153">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="d3cdb-154">契約の確認と有効化</span><span class="sxs-lookup"><span data-stu-id="d3cdb-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="d3cdb-155">アクション ウィンドウで、[購買契約] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="d3cdb-156">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-156">Click Confirmation.</span></span>
    * <span data-ttu-id="d3cdb-157">[契約を有効としてマークします] オプションに [はい] を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="d3cdb-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-158">Click OK.</span></span>
4. <span data-ttu-id="d3cdb-159">アクション ウィンドウで、[購買契約] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="d3cdb-160">[購買契約確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="d3cdb-161">[プレビュー/印刷] オプションにより、仕入先に印刷または送信する購買契約書のドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="d3cdb-162">契約を更新して後で再確認すると、両方のバージョンがここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="d3cdb-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3cdb-163">Close the page.</span></span>


