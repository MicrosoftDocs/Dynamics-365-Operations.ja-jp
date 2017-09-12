--- 
title: "電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を変更して実行する"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58e79f4d969e8bf0c7f150fd307f9f48334d6405
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="43f76-103">電子申告 (ER) 用の形式出力でドキュメント管理ファイルを使用するための形式を変更して実行する</span><span class="sxs-lookup"><span data-stu-id="43f76-103">Modify and run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43f76-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="43f76-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="43f76-105">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="43f76-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="43f76-106">これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート4：フォーマットの実行）」の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43f76-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="43f76-107">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="43f76-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="43f76-108">バイナリ形式のメッセージの生成に添付ファイルを設定するフォーマットを変更します。</span><span class="sxs-lookup"><span data-stu-id="43f76-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="43f76-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="43f76-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="43f76-110">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="43f76-111">ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="43f76-112">ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="43f76-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-113">Click Designer.</span></span>
    * <span data-ttu-id="43f76-114">UNICODEエンコードを使用し、XMLファイルとして生成される出力の請求書メッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="43f76-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="43f76-115">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="43f76-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="43f76-116">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="43f76-117">[名称] フィールドに、「Xmlメッセージ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="43f76-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="43f76-118">Xml メッセージ</span><span class="sxs-lookup"><span data-stu-id="43f76-118">Xml message</span></span>  
9. <span data-ttu-id="43f76-119">[エンコード] フィールドに、「UTF-8」と入力します。</span><span class="sxs-lookup"><span data-stu-id="43f76-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="43f76-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="43f76-120">UTF-8</span></span>  
10. <span data-ttu-id="43f76-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-121">Click OK.</span></span>
    * <span data-ttu-id="43f76-122">ZIPファイルとして生成される出力を設定します。</span><span class="sxs-lookup"><span data-stu-id="43f76-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="43f76-123">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="43f76-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="43f76-124">ツリーで、「Common\Folder」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="43f76-125">[名称] フィールドに、「Zip出力」と入力します。</span><span class="sxs-lookup"><span data-stu-id="43f76-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="43f76-126">Zip 出力</span><span class="sxs-lookup"><span data-stu-id="43f76-126">Zip output</span></span>  
14. <span data-ttu-id="43f76-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-127">Click OK.</span></span>
15. <span data-ttu-id="43f76-128">ツリーで、「Zip output」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="43f76-129">元名称と拡張子を含むファイルとして生成されるZIPファイルに添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="43f76-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="43f76-130">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="43f76-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="43f76-131">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="43f76-132">[名称] フィールドで、「添付ファイル」を入力します。</span><span class="sxs-lookup"><span data-stu-id="43f76-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="43f76-133">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="43f76-133">Attached file</span></span>  
19. <span data-ttu-id="43f76-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-134">Click OK.</span></span>
20. <span data-ttu-id="43f76-135">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="43f76-136">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="43f76-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="43f76-137">ツリーで、「'Text\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="43f76-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="43f76-139">新規フォーマットエレメントをデータ モデルにマッピングする</span><span class="sxs-lookup"><span data-stu-id="43f76-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="43f76-140">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="43f76-141">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="43f76-142">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="43f76-143">ツリーで、「Zip output\Attached file\Base64を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="43f76-144">ツリーで、「model\Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="43f76-145">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-145">Click Bind.</span></span>
7. <span data-ttu-id="43f76-146">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="43f76-147">[ファイル名の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-147">Click Edit filename.</span></span>
9. <span data-ttu-id="43f76-148">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="43f76-149">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="43f76-150">ツリーで、「model\Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="43f76-151">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-151">Click Add data source.</span></span>
13. <span data-ttu-id="43f76-152">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-152">Click Save.</span></span>
14. <span data-ttu-id="43f76-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="43f76-153">Close the page.</span></span>
15. <span data-ttu-id="43f76-154">ツリーで、「model\Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="43f76-155">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-155">Click Bind.</span></span>
17. <span data-ttu-id="43f76-156">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-156">Click Save.</span></span>
18. <span data-ttu-id="43f76-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="43f76-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="43f76-158">選択した請求書についてデザインされたレポートを実行する</span><span class="sxs-lookup"><span data-stu-id="43f76-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="43f76-159">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-159">Click Run.</span></span>
2. <span data-ttu-id="43f76-160">() セクションを含む記録を展開します。</span><span class="sxs-lookup"><span data-stu-id="43f76-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="43f76-161">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-161">Click Filter.</span></span>
4. <span data-ttu-id="43f76-162">顧客請求書仕訳および販売注文のフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="43f76-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="43f76-163">[基準] フィールドの基準[販売注文」フィールドで、注文番号 000148 を入力します。</span><span class="sxs-lookup"><span data-stu-id="43f76-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="43f76-164">000148</span><span class="sxs-lookup"><span data-stu-id="43f76-164">000148</span></span>  
6. <span data-ttu-id="43f76-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-165">Click OK.</span></span>
7. <span data-ttu-id="43f76-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="43f76-166">Click OK.</span></span>
    * <span data-ttu-id="43f76-167">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="43f76-167">Review the generated output.</span></span> <span data-ttu-id="43f76-168">XML形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意していください。</span><span class="sxs-lookup"><span data-stu-id="43f76-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="43f76-169">添付ファイルは、バイナリ形式のZIP出力で設定されます。</span><span class="sxs-lookup"><span data-stu-id="43f76-169">The attachment files are populated with the zipped output in binary format.</span></span>  


