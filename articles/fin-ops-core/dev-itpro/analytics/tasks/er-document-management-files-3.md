---
title: ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用
description: このトピックでは、ER 出力でドキュメント管理ファイルを使用するために電子申告形式を構成する方法について説明します。 (パート 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755013"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="a62f6-104">ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="a62f6-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a62f6-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a62f6-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a62f6-107">これらの手順を完了するには、まず 「フォーマット出力のドキュメント管理ファイルを ER 使用する（パート2：データモデルを拡張）」作業ガイドに記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62f6-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="a62f6-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="a62f6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="a62f6-109">請求書を処理するフォーマットを作成する</span><span class="sxs-lookup"><span data-stu-id="a62f6-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="a62f6-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a62f6-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a62f6-112">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="a62f6-113">ツリーで、[Customer invoice model\Customer invoice model (custom)]を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="a62f6-114">販売注文に添付されるファイル情報がある電子メッセージを生成するにはフォーマットを作成します。当該ファイルは電子処理請求書に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="a62f6-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="a62f6-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="a62f6-116">[新規] フィールドで、「データモデル・顧客請求書モデル（カスタム）に基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="a62f6-117">[名称] フィールドに、「電子請求書サンプル メッセージ」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="a62f6-118">電子請求書のサンプル メッセージ</span><span class="sxs-lookup"><span data-stu-id="a62f6-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="a62f6-119">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="a62f6-120">顧客への請求</span><span class="sxs-lookup"><span data-stu-id="a62f6-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="a62f6-121">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="a62f6-122">添付ファイルをMIME形式のメッセージにする設定のフォーマットをデザインする</span><span class="sxs-lookup"><span data-stu-id="a62f6-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="a62f6-123">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-123">Click Designer.</span></span>
2. <span data-ttu-id="a62f6-124">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="a62f6-125">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="a62f6-126">[名称] フィールドに、「Invoice」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="a62f6-127">請求書</span><span class="sxs-lookup"><span data-stu-id="a62f6-127">Invoice</span></span>  
5. <span data-ttu-id="a62f6-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-128">Click OK.</span></span>
6. <span data-ttu-id="a62f6-129">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="a62f6-130">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="a62f6-131">[名称] フィールドに、「SalesOrder」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="a62f6-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="a62f6-132">SalesOrder</span></span>  
9. <span data-ttu-id="a62f6-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-133">Click OK.</span></span>
10. <span data-ttu-id="a62f6-134">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="a62f6-135">[名称] フィールドで、「InvoiceNumber」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="a62f6-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="a62f6-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="a62f6-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-137">Click OK.</span></span>
13. <span data-ttu-id="a62f6-138">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="a62f6-139">[名称] フィールドに、「'InvoiceAmount」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="a62f6-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="a62f6-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="a62f6-141">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-141">Click OK.</span></span>
16. <span data-ttu-id="a62f6-142">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="a62f6-143">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="a62f6-144">[名称] フィールドに、「EnclosedDocs」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="a62f6-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="a62f6-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="a62f6-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-146">Click OK.</span></span>
20. <span data-ttu-id="a62f6-147">ツリーで、「Invoice\EnclosedDocs」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="a62f6-148">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-148">Click Add Element.</span></span>
22. <span data-ttu-id="a62f6-149">[名前] フィールドで、「Document」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="a62f6-150">書類</span><span class="sxs-lookup"><span data-stu-id="a62f6-150">Document</span></span>  
23. <span data-ttu-id="a62f6-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-151">Click OK.</span></span>
24. <span data-ttu-id="a62f6-152">ツリーで、「Invoice\EnclosedDocs\Document」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="a62f6-153">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="a62f6-154">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="a62f6-155">[名称] フィールドで、「FileName」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="a62f6-156">FileName</span><span class="sxs-lookup"><span data-stu-id="a62f6-156">FileName</span></span>  
28. <span data-ttu-id="a62f6-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-157">Click OK.</span></span>
29. <span data-ttu-id="a62f6-158">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="a62f6-159">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="a62f6-160">[名称] フィールドで、「FileContent」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="a62f6-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="a62f6-161">FileContent</span></span>  
32. <span data-ttu-id="a62f6-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-162">Click OK.</span></span>
33. <span data-ttu-id="a62f6-163">ツリーで、「Invoice\EnclosedDocs\Document\FileContent」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="a62f6-164">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="a62f6-165">ツリーで、「'Text\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="a62f6-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="a62f6-167">フォーマットエレメントをデータソースとしてデータ モデルにマッピングする</span><span class="sxs-lookup"><span data-stu-id="a62f6-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="a62f6-168">ツリーで、「Invoice\SalesOrder」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="a62f6-169">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="a62f6-170">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="a62f6-171">ツリーで、「model\Sales order number(SalesId)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="a62f6-172">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-172">Click Bind.</span></span>
6. <span data-ttu-id="a62f6-173">ツリーで、「Invoice\InvoiceNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="a62f6-174">ツリーで、「model\Base invoice(InvoiceBase)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="a62f6-175">ツリーで、「model\Base invoice(InvoiceBase)\Invoice number(Id)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="a62f6-176">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-176">Click Bind.</span></span>
10. <span data-ttu-id="a62f6-177">ツリーで、「Invoice\InvoiceAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="a62f6-178">ツリーで、「model\Base invoice(InvoiceBase)\Invoice amount(Amount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="a62f6-179">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-179">Click Bind.</span></span>
13. <span data-ttu-id="a62f6-180">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="a62f6-181">ツリーで、「model\Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="a62f6-182">ツリーで、「Invoice\EnclosedDocs\Document\FileContent\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="a62f6-183">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-183">Click Bind.</span></span>
17. <span data-ttu-id="a62f6-184">ツリーで、「model\Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="a62f6-185">ツリーで、「Invoice\EnclosedDocs\Document\FileName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="a62f6-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-186">Click Bind.</span></span>
20. <span data-ttu-id="a62f6-187">ツリーで、「model\Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="a62f6-188">ツリーで、「Invoice\EnclosedDocs\Document」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62f6-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="a62f6-189">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-189">Click Bind.</span></span>
23. <span data-ttu-id="a62f6-190">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62f6-190">Click Save.</span></span>
24. <span data-ttu-id="a62f6-191">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a62f6-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]