---
title: 画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン
description: このトピックでは、埋め込み画像を含む Excel と Word 形式で電子ドキュメントを生成するコンフィギュレーションをデザインする方法について説明します。
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944560"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="fefe3-103">画像が埋め込まれた Office 形式でレポートを生成するコンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="fefe3-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fefe3-104">この手順にあるステップを完了するには、まず 「ER 構成プロバイダを作成し、アクティブとしてマークする」 に記載の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="fefe3-105">この手順では、電子申告 (ER) コンフィギュレーションを設計して、埋め込み画像を含む Microsoft Excel または Word の電子ドキュメントを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="fefe3-106">この手順では、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。USMF データセットを使用してこれらの手順を完了できます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="fefe3-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="fefe3-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="fefe3-108">開始する前に、次のファイルをダウンロードして保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fefe3-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="fefe3-109">説明</span><span class="sxs-lookup"><span data-stu-id="fefe3-109">Description</span></span>                                          | <span data-ttu-id="fefe3-110">ファイル名</span><span class="sxs-lookup"><span data-stu-id="fefe3-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="fefe3-111">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="fefe3-111">ER data model configuration</span></span>                          | [<span data-ttu-id="fefe3-112">cheques.xml 用のモデル</span><span class="sxs-lookup"><span data-stu-id="fefe3-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="fefe3-113">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="fefe3-113">ER format configuration</span></span>                              | [<span data-ttu-id="fefe3-114">format.xml を印刷する小切手</span><span class="sxs-lookup"><span data-stu-id="fefe3-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="fefe3-115">会社のロゴ画像</span><span class="sxs-lookup"><span data-stu-id="fefe3-115">Company logo image</span></span>                                   | [<span data-ttu-id="fefe3-116">会社の logo.png</span><span class="sxs-lookup"><span data-stu-id="fefe3-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="fefe3-117">署名の画像</span><span class="sxs-lookup"><span data-stu-id="fefe3-117">Signature image</span></span>                                      | [<span data-ttu-id="fefe3-118">Signature image.png</span><span class="sxs-lookup"><span data-stu-id="fefe3-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="fefe3-119">代替署名画像</span><span class="sxs-lookup"><span data-stu-id="fefe3-119">Alternative signature image</span></span>                          | [<span data-ttu-id="fefe3-120">Signature image 2.png</span><span class="sxs-lookup"><span data-stu-id="fefe3-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="fefe3-121">小切手印刷用の Microsoft Word テンプレート</span><span class="sxs-lookup"><span data-stu-id="fefe3-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="fefe3-122">小切手テンプレート Word.docx</span><span class="sxs-lookup"><span data-stu-id="fefe3-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="fefe3-123">前提条件の確認</span><span class="sxs-lookup"><span data-stu-id="fefe3-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="fefe3-124">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="fefe3-125">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="fefe3-126">この構成プロバイダーが表示されない場合は、「構成プロバイダーを作成し、アクティブとしてマークする」 に記載の手順を完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="fefe3-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="fefe3-127">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="fefe3-128">新しい ER モデル コンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="fefe3-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="fefe3-129">新しいモデルを作成する代わりに、以前に保存した ER モデル コンフィギュレーション ファイル (cheques.xml のモデル) を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="fefe3-130">このファイルには、支払小切手のサンプル データ モデルおよび Dynamics 365 for Operations アプリケーションのデータ コンポーネントへのデータ モデルのマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="fefe3-131">[バージョン] クイック タブで、[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="fefe3-132">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="fefe3-133">[参照] をクリックし、cheques.xml のモデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="fefe3-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-134">Click OK.</span></span>  
 6. <span data-ttu-id="fefe3-135">読み込まれたモデルは、Excel と Word で画像を含むドキュメントを生成するための情報のデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="fefe3-136">新しい ER 形式コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="fefe3-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="fefe3-137">新しい形式を作成する代わりに、以前に保存した ER 形式コンフィギュレーション ファイル (format.xml を印刷する小切手) を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="fefe3-138">このファイルには、事前に印刷されたフォームを使用して小切手を印刷する形式のサンプル レイアウトと、データ モデル 「小切手のモデル」 にマッピングしたものが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fefe3-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="fefe3-139">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="fefe3-140">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="fefe3-141">[参照] をクリックして、format.xml ファイルを印刷する小切手を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="fefe3-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-142">Click OK.</span></span>  
 6. <span data-ttu-id="fefe3-143">ツリーで、「小切手のモデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="fefe3-144">ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="fefe3-145">読み込まれた形式は、Excel と Word で画像を含むドキュメントを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="fefe3-146">ER ユーザー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="fefe3-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="fefe3-147">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="fefe3-148">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="fefe3-149">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="fefe3-150">「ドラフトを実行する」 フラグをオンにして、選択した形式のドラフト バージョンを開始します。完了したドラフト バージョンではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fefe3-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="fefe3-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="fefe3-152">現金 & 銀行管理パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="fefe3-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="fefe3-153">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="fefe3-154">クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="fefe3-155">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="fefe3-156">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-156">Click Check.</span></span>  
 5. <span data-ttu-id="fefe3-157">[設定] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="fefe3-158">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-158">Click Edit.</span></span>  
 7. <span data-ttu-id="fefe3-159">[会社のロゴ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="fefe3-160">[会社のロゴ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="fefe3-161">[変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-161">Click Change.</span></span>  
 10. <span data-ttu-id="fefe3-162">[参照] をクリックして、以前にダウンロードしたファイル、会社の logo.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="fefe3-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-163">Click Save.</span></span>  
 12. <span data-ttu-id="fefe3-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-164">Close the page.</span></span>  
 13. <span data-ttu-id="fefe3-165">[署名] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="fefe3-166">[最初の署名を印刷] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="fefe3-167">[変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-167">Click Change.</span></span>  
 16. <span data-ttu-id="fefe3-168">[参照] をクリックして、以前にダウンロードしたファイル、署名 image.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="fefe3-169">[コピー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="fefe3-170">[透かし] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="fefe3-171">[一般的な電子エクスポート形式] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="fefe3-172">[小切手の印刷フォーム] コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="fefe3-173">これで、小切手を印刷するのに、選択された ER 形式が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="fefe3-174">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-174">Click Attach.</span></span>  
 23. <span data-ttu-id="fefe3-175">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-175">Click New.</span></span>  
 24. <span data-ttu-id="fefe3-176">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-176">Click File.</span></span>  
 25. <span data-ttu-id="fefe3-177">[参照] をクリックして、以前にダウンロードしたファイル、署名画像 2.png を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="fefe3-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-178">Close the page.</span></span>  
 27. <span data-ttu-id="fefe3-179">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-179">Close the page.</span></span>  
 28. <span data-ttu-id="fefe3-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-180">Close the page.</span></span>  
 29. <span data-ttu-id="fefe3-181">[現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="fefe3-182">[無効な銀行口座での事前通知の作成を許容] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fefe3-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="fefe3-183">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fefe3-183">Click Save.</span></span>  
 32. <span data-ttu-id="fefe3-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fefe3-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
