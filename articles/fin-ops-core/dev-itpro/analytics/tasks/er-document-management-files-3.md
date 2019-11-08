---
title: ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用
description: 次の手順では、システム管理者または電子申告開発者のロールに指定されたユーザーが、ER 出力のドキュメント管理ファイルを使用するために電子申告の形式をコンフィギュレーションする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 618fabc96bdfeb0c2b577aa686702d9f1257ed70
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550720"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="85c97-103">ER 形式の出力 (パート 3 - 形式の作成) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="85c97-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85c97-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="85c97-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="85c97-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="85c97-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="85c97-106">これらの手順を完了するには、まず「フォーマット出力のドキュメント管理ファイルをER使用する (パート2：データモデルを拡張）」の作業ガイドの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85c97-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="85c97-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="85c97-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="85c97-108">請求書を処理するフォーマットを作成する</span><span class="sxs-lookup"><span data-stu-id="85c97-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="85c97-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="85c97-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="85c97-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="85c97-111">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="85c97-112">ツリーで、「Customer invoice model\Customer invoice model (custom)]を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="85c97-113">販売注文に添付されるファイル情報がある電子メッセージを生成するにはフォーマットを作成します。当該ファイルは電子処理請求書に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="85c97-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="85c97-114">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="85c97-115">[新規] フィールドで、「データモデル・顧客請求書モデル（カスタム）に基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="85c97-116">[名称] フィールドに、「電子請求書サンプル メッセージ」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="85c97-117">電子請求書のサンプル メッセージ</span><span class="sxs-lookup"><span data-stu-id="85c97-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="85c97-118">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="85c97-119">顧客への請求</span><span class="sxs-lookup"><span data-stu-id="85c97-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="85c97-120">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="85c97-121">添付ファイルをMIME形式のメッセージにする設定のフォーマットをデザインする</span><span class="sxs-lookup"><span data-stu-id="85c97-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="85c97-122">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-122">Click Designer.</span></span>
2. <span data-ttu-id="85c97-123">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="85c97-124">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="85c97-125">[名称] フィールドに、「Invoice」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="85c97-126">請求書</span><span class="sxs-lookup"><span data-stu-id="85c97-126">Invoice</span></span>  
5. <span data-ttu-id="85c97-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-127">Click OK.</span></span>
6. <span data-ttu-id="85c97-128">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="85c97-129">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="85c97-130">[名称] フィールドに、「SalesOrder」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="85c97-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="85c97-131">SalesOrder</span></span>  
9. <span data-ttu-id="85c97-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-132">Click OK.</span></span>
10. <span data-ttu-id="85c97-133">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="85c97-134">[名称] フィールドで、「InvoiceNumber」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="85c97-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="85c97-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="85c97-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-136">Click OK.</span></span>
13. <span data-ttu-id="85c97-137">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="85c97-138">[名称] フィールドに、「'InvoiceAmount」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="85c97-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="85c97-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="85c97-140">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-140">Click OK.</span></span>
16. <span data-ttu-id="85c97-141">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="85c97-142">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="85c97-143">[名称] フィールドに、「EnclosedDocs」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="85c97-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="85c97-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="85c97-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-145">Click OK.</span></span>
20. <span data-ttu-id="85c97-146">ツリーで、「Invoice\EnclosedDocs」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="85c97-147">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-147">Click Add Element.</span></span>
22. <span data-ttu-id="85c97-148">[名前] フィールドで、「Document」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="85c97-149">書類</span><span class="sxs-lookup"><span data-stu-id="85c97-149">Document</span></span>  
23. <span data-ttu-id="85c97-150">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-150">Click OK.</span></span>
24. <span data-ttu-id="85c97-151">ツリーで、「Invoice\EnclosedDocs\Document」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="85c97-152">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="85c97-153">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="85c97-154">[名称] フィールドで、「FileName」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="85c97-155">FileName</span><span class="sxs-lookup"><span data-stu-id="85c97-155">FileName</span></span>  
28. <span data-ttu-id="85c97-156">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-156">Click OK.</span></span>
29. <span data-ttu-id="85c97-157">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="85c97-158">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="85c97-159">[名称] フィールドで、「FileContent」を入力します。</span><span class="sxs-lookup"><span data-stu-id="85c97-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="85c97-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="85c97-160">FileContent</span></span>  
32. <span data-ttu-id="85c97-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-161">Click OK.</span></span>
33. <span data-ttu-id="85c97-162">ツリーで、「Invoice\EnclosedDocs\Document\FileContent」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="85c97-163">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="85c97-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="85c97-164">ツリーで、「'Text\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="85c97-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="85c97-166">フォーマットエレメントをデータソースとしてデータ モデルにマッピングする</span><span class="sxs-lookup"><span data-stu-id="85c97-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="85c97-167">ツリーで、「Invoice\SalesOrder」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="85c97-168">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="85c97-169">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="85c97-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="85c97-170">ツリーで、「model\Sales order number(SalesId)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="85c97-171">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-171">Click Bind.</span></span>
6. <span data-ttu-id="85c97-172">ツリーで、「Invoice\InvoiceNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="85c97-173">ツリーで、「model\Base invoice(InvoiceBase)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="85c97-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="85c97-174">ツリーで、「model\Base invoice(InvoiceBase)\Invoice number(Id)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="85c97-175">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-175">Click Bind.</span></span>
10. <span data-ttu-id="85c97-176">ツリーで、「Invoice\InvoiceAmount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="85c97-177">ツリーで、「model\Base invoice(InvoiceBase)\Invoice amount(Amount)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="85c97-178">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-178">Click Bind.</span></span>
13. <span data-ttu-id="85c97-179">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="85c97-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="85c97-180">ツリーで、「model\Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="85c97-181">ツリーで、「Invoice\EnclosedDocs\Document\FileContent\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="85c97-182">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-182">Click Bind.</span></span>
17. <span data-ttu-id="85c97-183">ツリーで、「model\Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="85c97-184">ツリーで、「Invoice\EnclosedDocs\Document\FileName」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="85c97-185">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-185">Click Bind.</span></span>
20. <span data-ttu-id="85c97-186">ツリーで、「model\Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="85c97-187">ツリーで、「Invoice\EnclosedDocs\Document」を選択します。</span><span class="sxs-lookup"><span data-stu-id="85c97-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="85c97-188">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-188">Click Bind.</span></span>
23. <span data-ttu-id="85c97-189">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85c97-189">Click Save.</span></span>
24. <span data-ttu-id="85c97-190">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="85c97-190">Close the page.</span></span>

