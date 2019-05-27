---
title: 返品品目の受取の登録
description: 着荷の概要フォームまたは登録フォームを使用して、返品品目の受取を登録することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571078"
---
# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="d0821-103">返品品目の受取の登録</span><span class="sxs-lookup"><span data-stu-id="d0821-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d0821-104">返品品目の入庫を登録するための 2 種類の方法があります。</span><span class="sxs-lookup"><span data-stu-id="d0821-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="d0821-105">最初の方法は、**着荷の概要**フォームを使用する倉庫の入庫プロセスです。</span><span class="sxs-lookup"><span data-stu-id="d0821-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="d0821-106">もう 1 つの方法は、**登録**フォームを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0821-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="d0821-107">返品品目の入庫を着荷の概要フォームで登録</span><span class="sxs-lookup"><span data-stu-id="d0821-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="d0821-108">**着荷の概要**フォームを使用すれば、返品確認 (RMA) 番号によって返品荷物を識別できます。</span><span class="sxs-lookup"><span data-stu-id="d0821-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="d0821-109">仕訳帳名が **設定**タブで定義され、**着荷の概要**フォームで選択された明細行に対応する仕訳帳明細行がある場合、**着荷開始**をクリックすると、新しい仕訳帳ヘッダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d0821-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="d0821-110">**在庫管理** \> **定期処理** \> **着荷の概要**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="d0821-111">**設定名**フィールドで、**返品注文**をクリックし、次に**更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="d0821-112">検索結果を絞り込むには、<STRONG>範囲</STRONG>フィールドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d0821-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="d0821-113">正確な結果を得るためには、<STRONG>RMA 番号</STRONG>フィールドで RMA 番号を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d0821-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="d0821-114">どの入庫の到着が表示されるかを制限する、フィルターのセットを定義し保存するには、<STRONG>設定</STRONG>タブをクリックします。使用可能なフィルターには、タイプ、倉庫、およびドックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d0821-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="d0821-115"><STRONG>着荷の概要</STRONG>フォームでは、返品注文は他の着荷タイプと混合することはできません。</span><span class="sxs-lookup"><span data-stu-id="d0821-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="d0821-116">したがって、参照は常に販売注文ですが、販売注文 ID が仕訳帳ヘッダー上で指定されません。</span><span class="sxs-lookup"><span data-stu-id="d0821-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="d0821-117">**入庫**グリッドで、返品される品目に一致する明細行を特定し、**着荷に関する選択**列のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="d0821-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="d0821-118">返品荷物に含まれていない元の注文の品目など、返品入庫から特定の明細行を除外するには、フォームの下部の**明細行**テーブルにある、対応する**着荷に関する選択**チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="d0821-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="d0821-119">**着荷開始**ボタンをクリックして、着荷仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="d0821-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d0821-120">複数の返品注文を選択し、単一着荷プロセスにそのすべてを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d0821-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="d0821-121">各返品注文明細行は、対応する着荷仕訳帳明細行にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d0821-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="d0821-122"><STRONG>品目到着</STRONG>フォームを使用して、着荷仕訳帳を手動で作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="d0821-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="d0821-123">**在庫管理** \> **仕訳帳** \> **品目到着** \> **品目到着**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="d0821-124">作成した着荷仕訳帳を選択し、**明細行**をクリックして、**仕訳帳明細行、場所** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d0821-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="d0821-125">**一般** タブで、必要に応じて、**数量**フィールドの番号を調整し、**廃棄コード**フィールドに廃棄コードを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d0821-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="d0821-126">あるいは、**検査管理**チェック ボックスをオンにして、検査指示のコンテキストで、検査プロセスによって、返品品目を送付させることもできます。</span><span class="sxs-lookup"><span data-stu-id="d0821-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d0821-127">検査によって返品品目を送付する場合、廃棄コードを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d0821-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="d0821-128">**検証**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="d0821-129">検証プロセスにエラーがない場合は、**転記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="d0821-130">返品品目の入庫を登録フォームに登録</span><span class="sxs-lookup"><span data-stu-id="d0821-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="d0821-131">**着荷の概要**フォームを使用する代わりに、**登録**フォームを使用して、返品品目の着荷を登録することができます。</span><span class="sxs-lookup"><span data-stu-id="d0821-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="d0821-132">**販売とマーケティング** \> **共通** \> **返品注文** \> **すべての返品注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="d0821-133">新しい返品注文を作成するか、リストから返品注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="d0821-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="d0821-134">**明細行**クイック タブで、返品注文行を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0821-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="d0821-135">**明細行の更新** クリックし、**登録** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="d0821-136">**廃棄コード**フィールドに廃棄コードを割り当て、**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="d0821-137">検査品目を、<STRONG>登録</STRONG>フォームを使用して、検査指示として送付することはできません。</span><span class="sxs-lookup"><span data-stu-id="d0821-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="d0821-138">**トランザクション**グリッドで、登録するトランザクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0821-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="d0821-139">**今回登録**グリッドで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="d0821-140">すべての返品品目が**今回登録**グリッドに表示されるまで、前の 2 つのステップを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="d0821-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="d0821-141">**すべて転記**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d0821-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0821-142">参照</span><span class="sxs-lookup"><span data-stu-id="d0821-142">See also</span></span>

<span data-ttu-id="d0821-143">[着荷の概要 (フォーム)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="d0821-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  


