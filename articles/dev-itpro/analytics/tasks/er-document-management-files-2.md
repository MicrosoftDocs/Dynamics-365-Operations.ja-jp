--- 
title: "ER 出力でドキュメント管理ファイルを使用するためのデータ モデルの拡張"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="3b795-103">ER 出力でドキュメント管理ファイルを使用するためのデータ モデルの拡張</span><span class="sxs-lookup"><span data-stu-id="3b795-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3b795-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="3b795-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="3b795-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="3b795-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3b795-106">これらの手順を完了するには、まず「フォーマット出力のドキュメント管理ファイルをER使用する (パート1：データモデルを作成）」の作業ガイドの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b795-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="3b795-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="3b795-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="3b795-108">データモデルを拡張して、そのモデルにあるドキュメント管理ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="3b795-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="3b795-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b795-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3b795-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3b795-111">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="3b795-112">ツリーで、「Customer invoice model\Customer invoice model (custom)]を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="3b795-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-113">Click Designer.</span></span>
6. <span data-ttu-id="3b795-114">ツリーで、「Customer invoice(InvoiceCustomer)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="3b795-115">このデータ モデルを拡張して、販売注文に添付されたファイルに適用させます。この販売注文は電子的処理の請求書に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="3b795-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="3b795-116">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b795-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="3b795-117">[名称] フィールドで、「添付請求書」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="3b795-118">添付請求書</span><span class="sxs-lookup"><span data-stu-id="3b795-118">Invoice attachments</span></span>  
9. <span data-ttu-id="3b795-119">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="3b795-120">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-120">Click Add.</span></span>
11. <span data-ttu-id="3b795-121">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b795-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="3b795-122">[名称] フィールドで、「ファイルコンテンツ」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="3b795-123">ファイルの内容</span><span class="sxs-lookup"><span data-stu-id="3b795-123">File content</span></span>  
13. <span data-ttu-id="3b795-124">[品目タイプ] フィールドで、「コンテナー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="3b795-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-125">Click Add.</span></span>
15. <span data-ttu-id="3b795-126">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3b795-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="3b795-127">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="3b795-128">ファイル名</span><span class="sxs-lookup"><span data-stu-id="3b795-128">File name</span></span>  
17. <span data-ttu-id="3b795-129">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="3b795-130">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="3b795-131">新規データ モデル・エレメントを Dynamics 365 for Finance and Operations データ ソースにマッピングします</span><span class="sxs-lookup"><span data-stu-id="3b795-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="3b795-132">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="3b795-133">クイック フィルターを使用し、 「InvoiceCustomer」の値により「定義」フィールドでフィルターします。</span><span class="sxs-lookup"><span data-stu-id="3b795-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="3b795-134">顧客への請求</span><span class="sxs-lookup"><span data-stu-id="3b795-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="3b795-135">新規モデルエレメントを該当するデータソースにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="3b795-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="3b795-136">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-136">Click Designer.</span></span>
4. <span data-ttu-id="3b795-137">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="3b795-138">ツリーで、「Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="3b795-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="3b795-139">ツリーで、「Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="3b795-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-140">Click Edit.</span></span>
8. <span data-ttu-id="3b795-141">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="3b795-142">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="3b795-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="3b795-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-143">Click Save.</span></span>
10. <span data-ttu-id="3b795-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-144">Close the page.</span></span>
11. <span data-ttu-id="3b795-145">ツリーで、「Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="3b795-146">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-146">Click Edit.</span></span>
13. <span data-ttu-id="3b795-147">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="3b795-148">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="3b795-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="3b795-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-149">Click Save.</span></span>
15. <span data-ttu-id="3b795-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-150">Close the page.</span></span>
16. <span data-ttu-id="3b795-151">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b795-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="3b795-152">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-152">Click Edit.</span></span>
18. <span data-ttu-id="3b795-153">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents」を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b795-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="3b795-154">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'</span><span class="sxs-lookup"><span data-stu-id="3b795-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="3b795-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-155">Click Save.</span></span>
20. <span data-ttu-id="3b795-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-156">Close the page.</span></span>
21. <span data-ttu-id="3b795-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-157">Click Save.</span></span>
22. <span data-ttu-id="3b795-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-158">Close the page.</span></span>
23. <span data-ttu-id="3b795-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-159">Close the page.</span></span>
24. <span data-ttu-id="3b795-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3b795-160">Close the page.</span></span>
25. <span data-ttu-id="3b795-161">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-161">Click Change status.</span></span>
26. <span data-ttu-id="3b795-162">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-162">Click Complete.</span></span>
27. <span data-ttu-id="3b795-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b795-163">Click OK.</span></span>


