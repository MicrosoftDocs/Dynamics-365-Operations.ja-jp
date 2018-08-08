--- 
title: "品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録"
description: "この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。"
author: ShylaThompson
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1dab4ba973f5a9d3a2d8f1b5a5afcdd821d1a6d0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="b6cc2-103">品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録</span><span class="sxs-lookup"><span data-stu-id="b6cc2-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6cc2-104">この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="b6cc2-105">これは通常、入荷係により行われます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="b6cc2-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="b6cc2-107">このガイドを開始する前に、未処理の発注書明細行と共に確認済の発注書が必要です。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="b6cc2-108">明細行の品目は在庫がある必要があり、製品バリアントの使用および追跡用分析コードの保有はできません。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="b6cc2-109">その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="b6cc2-110">使用される倉庫は、倉庫管理プロセスに対して有効化されている必要があり、また受入場所は、ライセンス プレートにより制御されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="b6cc2-111">USMF を使用している場合、会社コード 1001、倉庫 51、品目 M9200 を使用して発注書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="b6cc2-112">作成した発注書の数をメモし、品目番号と購買注文明細行に使用したサイトもメモします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="b6cc2-113">着荷仕訳帳ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="b6cc2-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="b6cc2-114">[品目到着] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="b6cc2-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-115">Click New.</span></span>
3. <span data-ttu-id="b6cc2-116">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-117">USMF を使用している場合、「WHS」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="b6cc2-118">他のデータを使用している場合、ユーザーが名前を選択した仕訳帳は次のプロパティを必要とします。[ピッキング場所の確認] は [いいえ] に設定し、[検査管理] は [いいえ] に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="b6cc2-119">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="b6cc2-120">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-121">購買注文明細行に使用されているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="b6cc2-122">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b6cc2-123">USMF で倉庫 51 を使用した場合、サイト 5 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="b6cc2-124">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-125">選択したサイトの有効な倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="b6cc2-126">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b6cc2-127">USMF のサンプル値を使用している場合、51 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="b6cc2-128">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-129">選択した倉庫の有効な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="b6cc2-130">場所は、ライセンス プレートにより制御されている、位置プロファイルと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="b6cc2-131">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b6cc2-132">USMF のサンプル値を使用している場合、Bulk-008 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="b6cc2-133">[ライセンス プレート] フィールドのドロップダウン矢印を右クリックし、[詳細の表示] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="b6cc2-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-134">Click New.</span></span>
10. <span data-ttu-id="b6cc2-135">[ライセンス プレート] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-136">値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="b6cc2-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-137">Click Save.</span></span>
12. <span data-ttu-id="b6cc2-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-138">Close the page.</span></span>
13. <span data-ttu-id="b6cc2-139">[ライセンス プレート] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-140">作成したライセンス プレートの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="b6cc2-141">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="b6cc2-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="b6cc2-143">明細行の追加</span><span class="sxs-lookup"><span data-stu-id="b6cc2-143">Add a line</span></span>
1. <span data-ttu-id="b6cc2-144">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-144">Click Add line.</span></span>
2. <span data-ttu-id="b6cc2-145">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b6cc2-146">購買注文明細行で使用した品目番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="b6cc2-147">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b6cc2-148">登録する数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="b6cc2-149">[日付] フィールドは、この品目の手持在庫数量が在庫に登録される日付を決定します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="b6cc2-150">ロット ID は、提供された情報から一意に識別される場合に、システムによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="b6cc2-151">それ以外の場合は手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="b6cc2-152">これは、特定の元伝票明細行にこの登録をリンクする必須のフィールドです。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="b6cc2-153">登録の完了</span><span class="sxs-lookup"><span data-stu-id="b6cc2-153">Complete the registration</span></span>
1. <span data-ttu-id="b6cc2-154">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-154">Click Validate.</span></span>
    * <span data-ttu-id="b6cc2-155">これは、仕訳帳が転記できる状態かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="b6cc2-156">検証が失敗する場合、仕訳帳を転記する前にエラーを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="b6cc2-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-157">Click OK.</span></span>
    * <span data-ttu-id="b6cc2-158">[OK] をクリックしてから、メッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="b6cc2-159">仕訳帳が OK である、というメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="b6cc2-160">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-160">Click Post.</span></span>
4. <span data-ttu-id="b6cc2-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-161">Click OK.</span></span>
    * <span data-ttu-id="b6cc2-162">[OK] をクリックしてから、メッセージ バーを確認します。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="b6cc2-163">操作完了というメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="b6cc2-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6cc2-164">Close the page.</span></span>


