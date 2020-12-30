---
title: 購買契約書の作成
description: このトピックでは、購買契約書の作成方法について説明します。
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431906"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="c092f-103">購買契約書の作成</span><span class="sxs-lookup"><span data-stu-id="c092f-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c092f-104">このトピックでは、購買契約書の作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c092f-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="c092f-105">これは通常、購買マネージャが行います。</span><span class="sxs-lookup"><span data-stu-id="c092f-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="c092f-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="c092f-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c092f-107">開始する前に、購買契約書の分類を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c092f-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="c092f-108">契約を作成すると、発注書の作成時にそれを使用できます。また、販売契約条件がヘッダーまたは任意の明細行に、その契約によって影響される順でコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c092f-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="c092f-109">新しい購買契約の作成</span><span class="sxs-lookup"><span data-stu-id="c092f-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="c092f-110">**ナビゲーション ウィンドウ > モジュール > 調達 > 購買契約書 > 購買契約書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c092f-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="c092f-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c092f-111">Click **New**.</span></span>
3. <span data-ttu-id="c092f-112">**仕入先口座** フィールドで、ドロップダウン メニューを選択し、目的のレコードの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="c092f-113">**購買契約の分類** フィールドで、ドロップダウン メニューを選択し、目的のレコードの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="c092f-114">**概要** FastTab を展開します。</span><span class="sxs-lookup"><span data-stu-id="c092f-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="c092f-115">**有効期限** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c092f-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="c092f-116">この有効期限は、すべての確約明細行の既定値であり、各特定の確約の有効期間を決定します。</span><span class="sxs-lookup"><span data-stu-id="c092f-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="c092f-117">**ドキュメント タイトル** フィールドに、購買契約書の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c092f-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="c092f-118">**既定の確約** フィールドを、**製品数量確約** に設定したままにします (または、これに設定されていない場合は変更します)。</span><span class="sxs-lookup"><span data-stu-id="c092f-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="c092f-119">確約の既定値により、契約項目のオプションが決まります。</span><span class="sxs-lookup"><span data-stu-id="c092f-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="c092f-120">契約項目を作成する際に新しい確約タイプが必要な場合は、ヘッダーの確約既定値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c092f-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="c092f-121">確約には、次の 4 つのタイプがあります。**製品数量確約** - 製品の特定数量のためのものです。**製品価値確約** - 製品の特定の通貨金額のためのものです。**製品カテゴリ価値確約** - 金額がカタログ品目またはカタログ以外の品目である、特定の通貨金額調達カテゴリのためのものです。**価値確約** - すべての製品または調達カテゴリにより満たせる特定の通貨金額のためのものです。</span><span class="sxs-lookup"><span data-stu-id="c092f-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="c092f-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="c092f-123">確約の追加</span><span class="sxs-lookup"><span data-stu-id="c092f-123">Add a commitment</span></span>
1. <span data-ttu-id="c092f-124">**明細行の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-124">Select **Add line**.</span></span>
2. <span data-ttu-id="c092f-125">**品目番号** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="c092f-126">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c092f-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="c092f-127">これは、仕入先から購入することに合意した合計数量です。</span><span class="sxs-lookup"><span data-stu-id="c092f-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="c092f-128">**単価** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c092f-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="c092f-129">**行の詳細** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c092f-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="c092f-130">**最大値の適用** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c092f-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="c092f-131">**最大値の適用** オプションは、確約の使用を制限します。</span><span class="sxs-lookup"><span data-stu-id="c092f-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="c092f-132">購入できるのは、明細行の **数量** フィールドで指定された数量までです。</span><span class="sxs-lookup"><span data-stu-id="c092f-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="c092f-133">ヘッダー条件の追加</span><span class="sxs-lookup"><span data-stu-id="c092f-133">Add header conditions</span></span>
1. <span data-ttu-id="c092f-134">アクション ウィンドウで、**オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="c092f-135">**ビューの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-135">Select **Change view**.</span></span>
3. <span data-ttu-id="c092f-136">**ヘッダーの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-136">Select **Header view**.</span></span>
4. <span data-ttu-id="c092f-137">**条件** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c092f-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="c092f-138">**支払方法** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="c092f-139">仕入先からの支払条件が既定によりここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c092f-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="c092f-140">**荷渡方法** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="c092f-141">**配送条件** フィールドで、ドロップダウン ボタンを選択してルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c092f-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="c092f-142">契約の確認と有効化</span><span class="sxs-lookup"><span data-stu-id="c092f-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="c092f-143">アクション ウィンドウで、**購買契約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="c092f-144">**確認** を確認します。</span><span class="sxs-lookup"><span data-stu-id="c092f-144">Select **Confirmation**.</span></span> <span data-ttu-id="c092f-145">**契約を有効としてマークする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c092f-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="c092f-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-146">Select **OK**.</span></span>
4. <span data-ttu-id="c092f-147">アクション ウィンドウで、**購買契約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="c092f-148">**購買契約確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c092f-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="c092f-149">**プレビュー/印刷** オプションにより、仕入先に印刷または送信する購買契約書のドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="c092f-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="c092f-150">契約を更新して後で再確認すると、両方のバージョンがここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c092f-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="c092f-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c092f-151">Close the page.</span></span>

