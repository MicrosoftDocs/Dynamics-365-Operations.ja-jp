--- 
title: "電子申告 (ER) 用の形式コンフィギュレーションを使用して支払の電子ドキュメントを生成する"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、支払処理の電子ドキュメントを生成する新しい電子申告 (ER) 形式のコンフィギュレーションを使用する方法を説明します。"
author: NickSelin
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
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="2d800-103">電子申告 (ER) 用の形式コンフィギュレーションを使用して支払の電子ドキュメントを生成する</span><span class="sxs-lookup"><span data-stu-id="2d800-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d800-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、支払処理の電子ドキュメントを生成する新しい電子申告 (ER) 形式のコンフィギュレーションを使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2d800-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="2d800-105">これらのステップは GBSI サンプル会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="2d800-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="2d800-106">これらの手順を完了するには、先に「支払ドキュメントの形式でコンフィギュレーションの作成」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d800-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="2d800-107">電子支払方法のコンフィギュレーションの変更</span><span class="sxs-lookup"><span data-stu-id="2d800-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="2d800-108">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d800-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="2d800-109">必要に応じて、[ファイル形式] セクションを切り替えて展開します。</span><span class="sxs-lookup"><span data-stu-id="2d800-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="2d800-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="2d800-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2d800-111">たとえば、[支払い方法] フィールドに値「電子」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="2d800-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="2d800-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-112">Click Edit.</span></span>
5. <span data-ttu-id="2d800-113">[一般的な電子申告] フィールドを [はい] に設定します。</span><span class="sxs-lookup"><span data-stu-id="2d800-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="2d800-114">支払ファイル生成の一般的な電子申告パターンを使用するには [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="2d800-115">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d800-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2d800-116">BACS (英国企業) 形式のコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="2d800-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-117">Click Save.</span></span>
9. <span data-ttu-id="2d800-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2d800-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="2d800-119">生成された支払ファイルの形式のテスト</span><span class="sxs-lookup"><span data-stu-id="2d800-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="2d800-120">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d800-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="2d800-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-121">Click New.</span></span>
3. <span data-ttu-id="2d800-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="2d800-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2d800-123">[名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d800-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2d800-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d800-125">VendPay を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-125">Select VendPay.</span></span>  
6. <span data-ttu-id="2d800-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-126">Click Save.</span></span>
7. <span data-ttu-id="2d800-127">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-127">Click Lines.</span></span>
8. <span data-ttu-id="2d800-128">[会社] フィールドで、「DEMF」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2d800-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="2d800-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="2d800-129">DEMF</span></span>  
9. <span data-ttu-id="2d800-130">[口座] フィールドで、「DE-01001」という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d800-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="2d800-131">DE-01001</span><span class="sxs-lookup"><span data-stu-id="2d800-131">DE-01001</span></span>  
10. <span data-ttu-id="2d800-132">[説明] フィールドで「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2d800-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="2d800-133">支払</span><span class="sxs-lookup"><span data-stu-id="2d800-133">Payment</span></span>  
11. <span data-ttu-id="2d800-134">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d800-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="2d800-135">1000</span><span class="sxs-lookup"><span data-stu-id="2d800-135">1000</span></span>  
12. <span data-ttu-id="2d800-136">[支払] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="2d800-137">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d800-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="2d800-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2d800-139">電子の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="2d800-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="2d800-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-141">Click Save.</span></span>
17. <span data-ttu-id="2d800-142">[支払の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-142">Click Generate payments.</span></span>
18. <span data-ttu-id="2d800-143">[支払方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d800-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="2d800-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2d800-145">電子の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="2d800-146">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d800-147">電子の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="2d800-148">[ファイル名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d800-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="2d800-149">たとえば、「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2d800-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="2d800-150">[銀行口座] フィールドで、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d800-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="2d800-151">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d800-152">GBSI OPER 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d800-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="2d800-153">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-153">Click OK.</span></span>
25. <span data-ttu-id="2d800-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d800-154">Click OK.</span></span>
    * <span data-ttu-id="2d800-155">XML 形式で作成した支払ファイルを分析します。</span><span class="sxs-lookup"><span data-stu-id="2d800-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="2d800-156">設計されたドキュメント レイアウトおよび定義された支払トランザクションの属性と比較します。</span><span class="sxs-lookup"><span data-stu-id="2d800-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


