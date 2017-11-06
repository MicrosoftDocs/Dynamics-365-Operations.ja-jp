--- 
title: "仕入先請求ポリシーを設定します"
description: "[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f51c117da75a0382a38e75154ecef758f9a5d6c1
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="68e8e-103">仕入先請求ポリシーを設定します</span><span class="sxs-lookup"><span data-stu-id="68e8e-103">Set up vendor invoice policies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68e8e-104">[仕入先請求ポリシー] は、[仕入先請求書] ページを使用して仕入先請求書を転記するか、仕入先請求書の [ポリシー違反] ページを開いたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="68e8e-105">また、ワークフローに請求書を送信するたびに、仕入先請求書ワークフローを構成して仕入先請求書ポリシーを実行できます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="68e8e-106">仕入先請求ポリシーは仕入帳や請求仕訳帳で作成した請求書には適用しません。</span><span class="sxs-lookup"><span data-stu-id="68e8e-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="68e8e-107">請求書照合の検証は、仕入先請求ポリシーを使用せず、[買掛金管理パラメーター] ページで設定します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="68e8e-108">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="68e8e-109">買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="68e8e-110">始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="68e8e-111">仕入先請求書ポリシーの作成準備</span><span class="sxs-lookup"><span data-stu-id="68e8e-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="68e8e-112">[買掛金勘定] > [設定] > [買掛金勘定パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="68e8e-113">[請求書検証] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="68e8e-114">[請求書ヘッダーの状態を自動的に更新] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="68e8e-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-115">Click OK.</span></span>
5. <span data-ttu-id="68e8e-116">[不一致のある請求書を転記] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="68e8e-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-117">Close the page.</span></span>
7. <span data-ttu-id="68e8e-118">[買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="68e8e-119">[パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-119">Click Parameters.</span></span>
9. <span data-ttu-id="68e8e-120">[btnAdd] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-120">Click btnAdd.</span></span>
10. <span data-ttu-id="68e8e-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="68e8e-122">仕入先請求書のポリシー ルール タイプの作成</span><span class="sxs-lookup"><span data-stu-id="68e8e-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="68e8e-123">[買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー ルール タイプ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="68e8e-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-124">Click New.</span></span>
3. <span data-ttu-id="68e8e-125">[ルール名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="68e8e-126">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="68e8e-127">[クエリ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="68e8e-128">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="68e8e-129">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="68e8e-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-130">Click Save.</span></span>
9. <span data-ttu-id="68e8e-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="68e8e-132">仕入先請求書ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="68e8e-133">[買掛金勘定] > [ポリシー設定] > [仕入先請求ポリシー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="68e8e-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-134">Click New.</span></span>
3. <span data-ttu-id="68e8e-135">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="68e8e-136">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="68e8e-137">[ポリシーの組織] のセクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="68e8e-138">ツリーで、「Contoso Entertainment System USA」を選択します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="68e8e-139">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-139">Click Add.</span></span>
8. <span data-ttu-id="68e8e-140">[ポリシー ルール] のセクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="68e8e-141">[ポリシー ルールの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="68e8e-142">[ポリシー ルールの説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="68e8e-143">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-143">Click Filter.</span></span>
12. <span data-ttu-id="68e8e-144">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-144">Click Add.</span></span>
13. <span data-ttu-id="68e8e-145">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="68e8e-146">[テーブル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="68e8e-147">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="68e8e-148">[派生テーブル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="68e8e-149">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="68e8e-150">[フィールド] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="68e8e-151">[フィールド] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="68e8e-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-152">Close the page.</span></span>
21. <span data-ttu-id="68e8e-153">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="68e8e-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="68e8e-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-154">Click OK.</span></span>
23. <span data-ttu-id="68e8e-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="68e8e-155">Click OK.</span></span>
24. <span data-ttu-id="68e8e-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-156">Close the page.</span></span>
25. <span data-ttu-id="68e8e-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="68e8e-157">Close the page.</span></span>

