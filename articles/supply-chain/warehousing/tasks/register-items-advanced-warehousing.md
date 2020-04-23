---
title: 品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録
description: この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f8c39ade92b80c561c9e96220a59e7f222d77e6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216991"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="b7d07-103">品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録</span><span class="sxs-lookup"><span data-stu-id="b7d07-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7d07-104">この手順では、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="b7d07-105">これは通常、入荷係により行われます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="b7d07-106">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="b7d07-107">このガイドを開始する前に、未処理の発注書明細行と共に確認済の発注書が必要です。</span><span class="sxs-lookup"><span data-stu-id="b7d07-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="b7d07-108">明細行の品目は在庫がある必要があり、製品バリアントの使用および追跡用分析コードの保有はできません。</span><span class="sxs-lookup"><span data-stu-id="b7d07-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="b7d07-109">その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="b7d07-110">使用される倉庫は、倉庫管理プロセスに対して有効化されている必要があり、また受入に使う場所は、ライセンス プレートにより管理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="b7d07-111">USMF を使用している場合、会社口座 1001、倉庫 51、品目 M9200 を使用して発注書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="b7d07-112">作成した発注書の数をメモし、品目番号と購買注文明細行に使用したサイトもメモします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="b7d07-113">着荷仕訳帳ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="b7d07-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="b7d07-114">[品目到着] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="b7d07-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-115">Click New.</span></span>
3. <span data-ttu-id="b7d07-116">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b7d07-117">USMF を使用している場合、「WHS」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="b7d07-118">その他のデータを使用している場合、名前を選択した仕訳帳は次のプロパティを必要とします : ピッキング場所の確認 は いいえ に設定し、検査管理 は いいえ に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="b7d07-119">[数] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="b7d07-120">[サイト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="b7d07-121">購買注文明細行に使用されているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="b7d07-122">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b7d07-123">USMF で倉庫 51 を使用した場合、サイト 5 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="b7d07-124">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="b7d07-125">選択したサイトに対して有効な倉庫を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="b7d07-126">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b7d07-127">USMF で値の例を使用している場合、51 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="b7d07-128">[場所] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="b7d07-129">選択した倉庫の有効な場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="b7d07-130">場所は、ライセンス プレートにより制御されている、位置プロファイルと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="b7d07-131">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="b7d07-132">USMF で値の例を使用している場合は、Bulk-008 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="b7d07-133">[ライセンス プレート] フィールドのドロップダウン矢印を右クリックし、[詳細の表示] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="b7d07-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-134">Click New.</span></span>
10. <span data-ttu-id="b7d07-135">[ライセンス プレート] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="b7d07-136">値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="b7d07-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-137">Click Save.</span></span>
12. <span data-ttu-id="b7d07-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-138">Close the page.</span></span>
13. <span data-ttu-id="b7d07-139">[ライセンス プレート] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="b7d07-140">作成したライセンス プレートの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="b7d07-141">これは、仕訳帳のすべての明細行の既定値として使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="b7d07-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="b7d07-143">明細行の追加</span><span class="sxs-lookup"><span data-stu-id="b7d07-143">Add a line</span></span>
1. <span data-ttu-id="b7d07-144">[明細行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-144">Click Add line.</span></span>
2. <span data-ttu-id="b7d07-145">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b7d07-146">購買注文明細行で使用した品目番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="b7d07-147">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b7d07-148">登録する数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="b7d07-149">[日付] フィールドは、この品目の手持在庫数量が在庫に登録される日付を決定します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="b7d07-150">ロット ID は、提供された情報から一意に識別される場合に、システムによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="b7d07-151">それ以外の場合は手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="b7d07-152">これは、特定の元伝票明細行にこの登録をリンクする必須のフィールドです。</span><span class="sxs-lookup"><span data-stu-id="b7d07-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="b7d07-153">登録の完了</span><span class="sxs-lookup"><span data-stu-id="b7d07-153">Complete the registration</span></span>
1. <span data-ttu-id="b7d07-154">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-154">Click Validate.</span></span>
    * <span data-ttu-id="b7d07-155">これは、仕訳帳が転記できる状態かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="b7d07-156">検証が失敗する場合、仕訳帳を転記する前にエラーを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b7d07-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="b7d07-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-157">Click OK.</span></span>
    * <span data-ttu-id="b7d07-158">[OK] をクリックしてから、メッセージを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="b7d07-159">仕訳帳が OK である、というメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="b7d07-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="b7d07-160">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-160">Click Post.</span></span>
4. <span data-ttu-id="b7d07-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b7d07-161">Click OK.</span></span>
    * <span data-ttu-id="b7d07-162">[OK] をクリックしてから、メッセージ バーを確認します。</span><span class="sxs-lookup"><span data-stu-id="b7d07-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="b7d07-163">操作完了というメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="b7d07-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="b7d07-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b7d07-164">Close the page.</span></span>

