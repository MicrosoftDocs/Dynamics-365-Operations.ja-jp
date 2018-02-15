--- 
title: "電子申告 (ER) (Part 1) 用の画像が埋め込まれた Microsoft Office 形式のレポートを生成するためのコンフィギュレーションを設計する"
description: "このトピックの手順は、Microsoft Office (Excel および Word) の埋め込み画像を含む電子ドキュメントを生成する、電子レポート (ER) コンフィギュレーションの設計方法に関する情報を提供します。"
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.sourcegitcommit: 9cb9343028acacc387370e1cdd2202b84919185e
ms.openlocfilehash: 844d8de1d5a1958457eaab1d434bef015f92e33c
ms.contentlocale: ja-jp
ms.lasthandoff: 01/23/2018

---
# <a name="design-configurations-to-generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er-part-1"></a><span data-ttu-id="8e43c-103">電子申告 (ER) (Part 1) 用の画像が埋め込まれた Microsoft Office 形式のレポートを生成するためのコンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="8e43c-103">Design configurations to generate reports in Microsoft Office formats with embedded images for electronic reporting (ER) (Part 1)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e43c-104">この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="8e43c-105">この手順では、電子レポート (ER) コンフィギュレーションを設計して、埋め込み画像を含む Microsoft Excel または Word の電子ドキュメントを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="8e43c-106">この手順では、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。USMF データセットを使用してこれらの手順を完了できます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="8e43c-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="8e43c-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="8e43c-108">始める前に、ヘルプ トピック [電子申告ツールで生成されるビジネス ドキュメントへの画像と図形の埋め込み](../electronic-reporting-embed-images-shapes.md) に一覧表示されたファイルをダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="8e43c-109">ファイルは cheques.xml のモデル、format.xml を印刷する小切手、会社の logo.png、署名 image.png、署名画像 2.png、および小切手テンプレート Word.docx です。</span><span class="sxs-lookup"><span data-stu-id="8e43c-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="8e43c-110">前提条件の確認</span><span class="sxs-lookup"><span data-stu-id="8e43c-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="8e43c-111">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="8e43c-112">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="8e43c-113">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e43c-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="8e43c-114">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="8e43c-115">新しい ER モデル コンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="8e43c-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="8e43c-116">新しいモデルを作成する代わりに、以前に保存した ER モデル コンフィギュレーション ファイル (cheques.xml のモデル) を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="8e43c-117">このファイルには、支払小切手のサンプル データ モデルおよび Dynamics 365 for Operations アプリケーションのデータ コンポーネントへのデータ モデルのマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="8e43c-118">[バージョン] クイック タブで、[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="8e43c-119">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="8e43c-120">[参照] をクリックし、cheques.xml のモデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="8e43c-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-121">Click OK.</span></span>  
 6. <span data-ttu-id="8e43c-122">読み込まれたモデルは、Excel と Word で画像を含むドキュメントを生成するための情報のデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="8e43c-123">新しい ER 形式コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="8e43c-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="8e43c-124">新しい形式を作成する代わりに、以前に保存した ER 形式コンフィギュレーション ファイル (format.xml を印刷する小切手) を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="8e43c-125">このファイルには、事前に印刷されたフォームを使用して小切手を印刷する形式のサンプル レイアウトと、「小切手のモデル」データ モデルへのこの形式のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8e43c-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="8e43c-126">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="8e43c-127">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="8e43c-128">[参照] をクリックして、format.xml ファイルを印刷する小切手を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="8e43c-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-129">Click OK.</span></span>  
 6. <span data-ttu-id="8e43c-130">ツリーで、「小切手のモデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="8e43c-131">ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="8e43c-132">読み込まれた形式は、Excel と Word で画像を含むドキュメントを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="8e43c-133">ER ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e43c-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="8e43c-134">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="8e43c-135">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="8e43c-136">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="8e43c-137">「ドラフトの実行」フラグをオンにして、完了したドラフト バージョンではなく、選択した形式のドラフト バージョンを開始します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="8e43c-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="8e43c-139">現金 & 銀行管理パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e43c-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="8e43c-140">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="8e43c-141">クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="8e43c-142">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="8e43c-143">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-143">Click Check.</span></span>  
 5. <span data-ttu-id="8e43c-144">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="8e43c-145">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-145">Click Edit.</span></span>  
 7. <span data-ttu-id="8e43c-146">[会社のロゴ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="8e43c-147">[会社のロゴ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="8e43c-148">[変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-148">Click Change.</span></span>  
 10. <span data-ttu-id="8e43c-149">[参照] をクリックして、以前にダウンロードしたファイル、会社の logo.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="8e43c-150">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-150">Click Save.</span></span>  
 12. <span data-ttu-id="8e43c-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-151">Close the page.</span></span>  
 13. <span data-ttu-id="8e43c-152">[署名] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="8e43c-153">[最初の署名を印刷] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="8e43c-154">[変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-154">Click Change.</span></span>  
 16. <span data-ttu-id="8e43c-155">[参照] をクリックして、以前にダウンロードしたファイル、署名 image.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="8e43c-156">[コピー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="8e43c-157">[透かし] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="8e43c-158">[一般的な電子エクスポート形式] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="8e43c-159">[小切手の印刷フォーム] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="8e43c-160">これで、小切手を印刷するのに、選択された ER 形式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="8e43c-161">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-161">Click Attach.</span></span>  
 23. <span data-ttu-id="8e43c-162">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-162">Click New.</span></span>  
 24. <span data-ttu-id="8e43c-163">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-163">Click File.</span></span>  
 25. <span data-ttu-id="8e43c-164">[参照] をクリックして、以前にダウンロードしたファイル、署名画像 2.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="8e43c-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-165">Close the page.</span></span>  
 27. <span data-ttu-id="8e43c-166">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-166">Close the page.</span></span>  
 28. <span data-ttu-id="8e43c-167">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-167">Close the page.</span></span>  
 29. <span data-ttu-id="8e43c-168">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="8e43c-169">[無効な銀行口座での事前通知の作成を許容] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e43c-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="8e43c-170">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e43c-170">Click Save.</span></span>  
 32. <span data-ttu-id="8e43c-171">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8e43c-171">Close the page.</span></span>  

