---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 5 部 - 形式の変更および実行)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23e91b6aee62157da9141cc7b6c4fae39c19ce32
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544682"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5-modify-and-run-format"></a><span data-ttu-id="16ccf-103">ER 形式の出力 (パート 5: 形式の変更と実行) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="16ccf-103">ER Use Document Management files in format outputs (Part 5: Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16ccf-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="16ccf-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="16ccf-106">これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート4：フォーマットの実行）」の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16ccf-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="16ccf-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="16ccf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="16ccf-108">バイナリ形式のメッセージの生成に添付ファイルを設定するフォーマットを変更します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="16ccf-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="16ccf-110">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="16ccf-111">ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="16ccf-112">ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="16ccf-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-113">Click Designer.</span></span>
    * <span data-ttu-id="16ccf-114">UNICODEエンコードを使用し、XMLファイルとして生成される出力の請求書メッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="16ccf-115">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="16ccf-116">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="16ccf-117">[名称] フィールドに、「Xmlメッセージ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="16ccf-118">Xml メッセージ</span><span class="sxs-lookup"><span data-stu-id="16ccf-118">Xml message</span></span>  
9. <span data-ttu-id="16ccf-119">[エンコード] フィールドに、「UTF-8」と入力します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="16ccf-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="16ccf-120">UTF-8</span></span>  
10. <span data-ttu-id="16ccf-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-121">Click OK.</span></span>
    * <span data-ttu-id="16ccf-122">ZIPファイルとして生成される出力を設定します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="16ccf-123">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="16ccf-124">ツリーで、「Common\Folder」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="16ccf-125">[名称] フィールドに、「Zip出力」と入力します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="16ccf-126">Zip 出力</span><span class="sxs-lookup"><span data-stu-id="16ccf-126">Zip output</span></span>  
14. <span data-ttu-id="16ccf-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-127">Click OK.</span></span>
15. <span data-ttu-id="16ccf-128">ツリーで、「Zip output」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="16ccf-129">元名称と拡張子を含むファイルとして生成されるZIPファイルに添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="16ccf-130">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="16ccf-131">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="16ccf-132">[名称] フィールドで、「添付ファイル」を入力します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="16ccf-133">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="16ccf-133">Attached file</span></span>  
19. <span data-ttu-id="16ccf-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-134">Click OK.</span></span>
20. <span data-ttu-id="16ccf-135">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="16ccf-136">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="16ccf-137">ツリーで、「'Text\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="16ccf-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="16ccf-139">新規フォーマットエレメントをデータ モデルにマッピングする</span><span class="sxs-lookup"><span data-stu-id="16ccf-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="16ccf-140">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="16ccf-141">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="16ccf-142">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="16ccf-143">ツリーで、「Zip output\Attached file\Base64を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="16ccf-144">ツリーで、「model\Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="16ccf-145">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-145">Click Bind.</span></span>
7. <span data-ttu-id="16ccf-146">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="16ccf-147">[ファイル名の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-147">Click Edit filename.</span></span>
9. <span data-ttu-id="16ccf-148">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="16ccf-149">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="16ccf-150">ツリーで、「model\Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="16ccf-151">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-151">Click Add data source.</span></span>
13. <span data-ttu-id="16ccf-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-152">Click Save.</span></span>
14. <span data-ttu-id="16ccf-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-153">Close the page.</span></span>
15. <span data-ttu-id="16ccf-154">ツリーで、「model\Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="16ccf-155">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-155">Click Bind.</span></span>
17. <span data-ttu-id="16ccf-156">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-156">Click Save.</span></span>
18. <span data-ttu-id="16ccf-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="16ccf-158">選択した請求書についてデザインされたレポートを実行する</span><span class="sxs-lookup"><span data-stu-id="16ccf-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="16ccf-159">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-159">Click Run.</span></span>
2. <span data-ttu-id="16ccf-160">() セクションを含む記録を展開します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="16ccf-161">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-161">Click Filter.</span></span>
4. <span data-ttu-id="16ccf-162">顧客請求書仕訳および販売注文のフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="16ccf-163">[基準] フィールドの基準[販売注文」フィールドで、注文番号 000148 を入力します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="16ccf-164">000148</span><span class="sxs-lookup"><span data-stu-id="16ccf-164">000148</span></span>  
6. <span data-ttu-id="16ccf-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-165">Click OK.</span></span>
7. <span data-ttu-id="16ccf-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16ccf-166">Click OK.</span></span>
    * <span data-ttu-id="16ccf-167">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="16ccf-167">Review the generated output.</span></span> <span data-ttu-id="16ccf-168">XML形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意していください。</span><span class="sxs-lookup"><span data-stu-id="16ccf-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="16ccf-169">添付ファイルは、バイナリ形式のZIP出力で設定されます。</span><span class="sxs-lookup"><span data-stu-id="16ccf-169">The attachment files are populated with the zipped output in binary format.</span></span>  

