---
title: ER 出力でドキュメント管理ファイルを使用するための形式の実行
description: 次の手順では、システム管理者または電子申告開発者のロールに指定されたユーザーが、ER 出力のドキュメント管理ファイルを使用するために電子申告の形式をコンフィギュレーションする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185017"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a><span data-ttu-id="d7a8c-103">ER 形式の出力 (パート 4: 形式の実行) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="d7a8c-103">ER Use Document Management files in format outputs (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7a8c-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="d7a8c-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="d7a8c-106">これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート3：フォーマットの作成）」の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="d7a8c-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="d7a8c-108">単一請求書の販売注文に必要な添付ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="d7a8c-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="d7a8c-109">[売掛金勘定] > [請求書] > [未処理の顧客請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="d7a8c-110">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d7a8c-111">たとえば、「CIV-000148」の値を含む請求書フィールドでフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="d7a8c-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="d7a8c-112">CIV-000148</span></span>  
3. <span data-ttu-id="d7a8c-113">クリックして選択した請求書のリンク先に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="d7a8c-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="d7a8c-114">CIV-000148</span></span>  
4. <span data-ttu-id="d7a8c-115">クリックして、[販売注文] フィールドのリンク先に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="d7a8c-116">000148</span><span class="sxs-lookup"><span data-stu-id="d7a8c-116">000148</span></span>  
5. <span data-ttu-id="d7a8c-117">明細行またはヘッダーのフィールドで、ヘッダーのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="d7a8c-118">ヘッダーを選択して、これが添付の追加先であることを示します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="d7a8c-119">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-119">Click Attach.</span></span>
    * <span data-ttu-id="d7a8c-120">この販売注文の添付ファイルとしていくつかのファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="d7a8c-121">ドキュメント管理がサポートするドキュメント タイプのファイルを使用します (ファイル拡張子DOCX、DPF、XML、JPGなど)。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="d7a8c-122">ER電子メッセージに関連する請求書に添付され、さらに処理されるファイルを閲覧、選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="d7a8c-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-123">Click New.</span></span>
8. <span data-ttu-id="d7a8c-124">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-124">Click File.</span></span>
9. <span data-ttu-id="d7a8c-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-125">Click New.</span></span>
10. <span data-ttu-id="d7a8c-126">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-126">Click File.</span></span>
11. <span data-ttu-id="d7a8c-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-127">Close the page.</span></span>
12. <span data-ttu-id="d7a8c-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-128">Close the page.</span></span>
13. <span data-ttu-id="d7a8c-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-129">Close the page.</span></span>
14. <span data-ttu-id="d7a8c-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="d7a8c-131">選択した請求書についてデザインされたレポートを実行する</span><span class="sxs-lookup"><span data-stu-id="d7a8c-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="d7a8c-132">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d7a8c-133">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="d7a8c-134">ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="d7a8c-135">ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="d7a8c-136">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-136">Click Run.</span></span>
6. <span data-ttu-id="d7a8c-137">() セクションを含む記録を展開します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="d7a8c-138">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-138">Click Filter.</span></span>
8. <span data-ttu-id="d7a8c-139">顧客請求書仕訳および販売注文のフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="d7a8c-140">[基準] フィールドで、「000148」と入力します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="d7a8c-141">基準「販売注文」フィールドで、「注文番号000148」を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="d7a8c-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-142">Click OK.</span></span>
11. <span data-ttu-id="d7a8c-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-143">Click OK.</span></span>
    * <span data-ttu-id="d7a8c-144">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-144">Review the generated output.</span></span> <span data-ttu-id="d7a8c-145">各添付ファイルに対して単一のXMLノードが作成されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="d7a8c-146">添付ファイルのコンテンツは、MIME (base64) のテキスト形式のXML出力に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7a8c-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

