---
title: アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのインポート
description: この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了する必要があります。
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd7a07d041373b266103f313df1bf2810e9c858
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182350"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="190b9-103">アプリケーション データを含むドキュメントを生成するためのコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="190b9-103">Import configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="190b9-104">この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="190b9-104">To complete the steps in this procedure, you must first complete the procedure, “ER Create a configuration provider and mark it as active”.</span></span>

<span data-ttu-id="190b9-105">この手順のステップでは、電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="190b9-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="190b9-106">この手順では、サンプル会社 Litware, Inc. 用に作成した必要な ER コンフィギュレーションをインポートし、それを使用して電子ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="190b9-106">In this procedure, you will import the required ER configurations that have been created for the sample company, Litware, Inc. and use them to generate electronic documents.</span></span> <span data-ttu-id="190b9-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="190b9-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="190b9-108">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="190b9-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="190b9-109">始める前に、ヘルプ トピック「電子申告ツールを使用して電子ドキュメントを生成し、アプリケーション データを更新」 (generate-electronic-documents-update-application-data/) に一覧表示されたファイルをダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="190b9-109">Before you begin, download and save the files listed in the Help topic, “Generate electronic documents and update application data with ER tool” (generate-electronic-documents-update-application-data/).</span></span> <span data-ttu-id="190b9-110">ファイルは、イントラスタット (モデル) .xml、イントラスタット (マッピング) .xml、およびイントラスタット (形式) .xml です。</span><span class="sxs-lookup"><span data-stu-id="190b9-110">The files are Intrastat (model).xml, Intrastat (mapping).xml, and Intrastat (format).xml.</span></span>

1. <span data-ttu-id="190b9-111">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="190b9-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="190b9-112">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="190b9-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="190b9-113">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="190b9-113">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
    * <span data-ttu-id="190b9-114">この手順のステップでは、ER 機能を使用してアプリケーション データの更新を完了する方法、およびイントラスタット レポートを生成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="190b9-114">The steps in this procedure show how to use ER capabilities to complete an application data update and how to generate an Intrastat report.</span></span> <span data-ttu-id="190b9-115">レポート処理の詳細は、アプリケーション テーブルにアーカイブされます。</span><span class="sxs-lookup"><span data-stu-id="190b9-115">The details of the reporting process are archived in the application tables.</span></span> <span data-ttu-id="190b9-116">現時点では、[イントラスタット] フォームからイントラスタット レポート処理が有効化されると、既存のソース コードでプログラムされたロジックに基づいてアーカイブがなされます。</span><span class="sxs-lookup"><span data-stu-id="190b9-116">Currently, when the Intrastat reporting process is activated from the Intrastat form, archiving is done based on the logic programmed in the existing source code.</span></span> <span data-ttu-id="190b9-117">この手順では、ER フレームワークのみを使用して、類似しているものの簡略化されたアプリケーション データのロジックを構成します。</span><span class="sxs-lookup"><span data-stu-id="190b9-117">In this procedure, you will configure a similar yet simplified logic of application data using only the ER framework.</span></span> <span data-ttu-id="190b9-118">ソース コードには、変更は行われません。</span><span class="sxs-lookup"><span data-stu-id="190b9-118">No changes will be made to the source code.</span></span>   

## <a name="import-er-configurations"></a><span data-ttu-id="190b9-119">ER コンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="190b9-119">Import ER configurations</span></span>
1. <span data-ttu-id="190b9-120">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-120">Click Reporting configurations.</span></span>
2. <span data-ttu-id="190b9-121">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-121">Click Exchange.</span></span>
3. <span data-ttu-id="190b9-122">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-122">Click Load from XML file.</span></span>
    * <span data-ttu-id="190b9-123">イントラスタット レポートを生成するためにデータ ソースとして使用するように設計されたデータ モデルを含む、ER モデル コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="190b9-123">Import the ER model configuration that contains the data model that is designed to be used as the data source for generating the Intrastat report.</span></span> <span data-ttu-id="190b9-124">後で、このデータ モデルの定義を拡張して、アプリケーション データ更新がイントラスタット レポート処理の詳細をアーカイブするのに使用します。</span><span class="sxs-lookup"><span data-stu-id="190b9-124">Later, you will extend this data model definition to use it for an application data update to archive details of the Intrastat reporting process.</span></span>   
    * <span data-ttu-id="190b9-125">[参照] をクリックして、イントラスタット (モデル) .xml ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-125">Click Browse and select the Intrastat (model).xml file.</span></span>  
4. <span data-ttu-id="190b9-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-126">Click OK.</span></span>
5. <span data-ttu-id="190b9-127">ツリーで、「イントラスタット (モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-127">In the tree, select 'Intrastat (model)'.</span></span>
6. <span data-ttu-id="190b9-128">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-128">Click Designer.</span></span>
7. <span data-ttu-id="190b9-129">ツリーで、「送信ドキュメント用」を展開します。</span><span class="sxs-lookup"><span data-stu-id="190b9-129">In the tree, expand 'For outgoing document'.</span></span>
8. <span data-ttu-id="190b9-130">ツリーで、「送信ドキュメント用\トランザクション」を展開します。</span><span class="sxs-lookup"><span data-stu-id="190b9-130">In the tree, expand 'For outgoing document\Transactions'.</span></span>
    * <span data-ttu-id="190b9-131">インポートされたデータ モデルの構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="190b9-131">Review the structure of the imported data model.</span></span> <span data-ttu-id="190b9-132">「送信ドキュメント用」ルート項目が、アプリケーションからデータを取得し、それをデータ ソースとして使用してイントラスタット レポートを生成するためのデータ フローを指定するよう定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="190b9-132">Note that the root item ‘For outgoing document’ is defined to specify the data flow for getting data from the application and using it as data source to generate the Intrastat report.</span></span> <span data-ttu-id="190b9-133">「トランザクション (レコード リスト)」を使用して、レポートする必要のあるイントラスタット トランザクションの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="190b9-133">The ‘Transactions (Record list)’ is used to represent the list of Intrastat transactions that must be reported.</span></span> <span data-ttu-id="190b9-134">レポートされた商品コードをアーカイブするため、このデータ フローには単一の商品コードの一意の識別子「商品 rec id (Int64)」が必要です。</span><span class="sxs-lookup"><span data-stu-id="190b9-134">Because you will archive reported commodity codes, the unique identifier of a single commodity code ‘Commodity rec id (Int64)’ is needed in this data flow.</span></span>   
9. <span data-ttu-id="190b9-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="190b9-135">Close the page.</span></span>
10. <span data-ttu-id="190b9-136">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-136">Click Exchange.</span></span>
11. <span data-ttu-id="190b9-137">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-137">Click Load from XML file.</span></span>
    * <span data-ttu-id="190b9-138">アプリケーションからデータを取得し、その後それを使用してイントラスタット レポートを生成するためのデータ フローを指定する、ER マッピング コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="190b9-138">Import the ER mapping configuration that specifies the data flow for getting data from the application and then using it to generate the Intrastat report.</span></span> <span data-ttu-id="190b9-139">後で、このモデル マッピングの定義を拡張してイントラスタット レポートからデータを取得し、それをアプリケーション データの更新に使用してイントラスタット レポート プロセスの詳細をアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="190b9-139">Later, you will extend this model mapping definition to get data from the Intrastat report and use it for the application data update to archive details of Intrastat reporting process.</span></span>   
    * <span data-ttu-id="190b9-140">[参照] をクリックして、イントラスタット (マッピング) .xml ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-140">Click Browse and select the Intrastat (mapping).xml file.</span></span>  
12. <span data-ttu-id="190b9-141">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-141">Click OK.</span></span>
13. <span data-ttu-id="190b9-142">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="190b9-142">In the tree, expand 'Intrastat (model)'.</span></span>
14. <span data-ttu-id="190b9-143">ツリーで、「イントラスタット (モデル)\イントラスタット (マッピング)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-143">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
15. <span data-ttu-id="190b9-144">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-144">Click Designer.</span></span>
    * <span data-ttu-id="190b9-145">現在のモデル マッピングには、[方向] フィールドに「モデルへ」という値が含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="190b9-145">Note that the current model mapping contains the value ‘To model’ in the Direction field.</span></span> <span data-ttu-id="190b9-146">つまり、このモデル マッピングは、アプリケーションからデータを取得してデータ モデルに保存するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="190b9-146">This means that this model mapping has been designed for getting data from the application and storing it in the data model.</span></span>  
16. <span data-ttu-id="190b9-147">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-147">Click Designer.</span></span>
17. <span data-ttu-id="190b9-148">ツリーで、「リスト」を展開します。</span><span class="sxs-lookup"><span data-stu-id="190b9-148">In the tree, expand 'List'.</span></span>
18. <span data-ttu-id="190b9-149">ツリーで、「トランザクション = リスト」を展開します。</span><span class="sxs-lookup"><span data-stu-id="190b9-149">In the tree, expand 'Transactions= List'.</span></span>
    * <span data-ttu-id="190b9-150">「送信ドキュメント用」というルート項目に基づいてフィルター処理されたデータ モデルを使用するモデル マッピングの構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="190b9-150">Review the structure of the model mapping that uses the data model that is filtered based on the root item, ‘For outgoing document.’</span></span> <span data-ttu-id="190b9-151">「リスト」という追加されたデータ ソースは、イントラスタット テーブルからのレコードのリストである必要なアプリケーション データへのアクセス許可を提供することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="190b9-151">Note that the added data source, ‘List’ provides access to the required application data, which is the list of records from the Intrastat table.</span></span>  
19. <span data-ttu-id="190b9-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="190b9-152">Close the page.</span></span>
20. <span data-ttu-id="190b9-153">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="190b9-153">Close the page.</span></span>
21. <span data-ttu-id="190b9-154">[交換] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-154">Click Exchange.</span></span>
22. <span data-ttu-id="190b9-155">[XML ファイルから読み込む] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-155">Click Load from XML file.</span></span>
    * <span data-ttu-id="190b9-156">イントラスタット レポートのレイアウトおよびレポートへのデータ登録のプロセスを指定する ER 形式コンフィギュレーションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="190b9-156">Import the ER format configuration that specifies the layout of the Intrastat report and the process of populating data to the report.</span></span> <span data-ttu-id="190b9-157">後で、この形式の定義を拡張してイントラスタット レポートのデータをデータ モデルに格納し、アプリケーション データを更新してイントラスタット レポート プロセスの詳細をアーカイブするために使用します。</span><span class="sxs-lookup"><span data-stu-id="190b9-157">Later, you will extend this format definition to put data from the Intrastat report in to the data model and then use it to update application data to archive the details of Intrastat reporting process.</span></span>   
    * <span data-ttu-id="190b9-158">[参照] をクリックして、イントラスタット (形式) .xml ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-158">Click Browse and select the Intrastat (format).xml file.</span></span>  
23. <span data-ttu-id="190b9-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-159">Click OK.</span></span>
24. <span data-ttu-id="190b9-160">ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-160">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
25. <span data-ttu-id="190b9-161">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-161">Click Designer.</span></span>
26. <span data-ttu-id="190b9-162">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-162">Click Expand/collapse.</span></span>
27. <span data-ttu-id="190b9-163">ツリーで、「ファイル\申告」を選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-163">In the tree, select 'File\Declaration'.</span></span>
28. <span data-ttu-id="190b9-164">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="190b9-164">Click the Mapping tab.</span></span>
29. <span data-ttu-id="190b9-165">ツリーで、「ファイル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="190b9-165">In the tree, select 'File'.</span></span>
    * <span data-ttu-id="190b9-166">イントラスタット レポートを生成するために使用されている形式の構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="190b9-166">Review the structure of the format used to generate the Intrastat report.</span></span> <span data-ttu-id="190b9-167">「送信ドキュメント用」というルート項目に基づいたデータ モデルからデータを設定することによって XML ファイルを生成するよう設計されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="190b9-167">Note that it is designed to generate an XML file by populating data from the data model, which is based on the root item ‘For outgoing document’.</span></span> <span data-ttu-id="190b9-168">生成されたファイルの名前が、ユーザー ダイアログ フォームで定義されていることを確認します (「fn」データ ソースがそのために使用されます)。</span><span class="sxs-lookup"><span data-stu-id="190b9-168">Verify that the name for generated file is defined on the user dialog form (‘fn’ data source is used for that).</span></span>   
30. <span data-ttu-id="190b9-169">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="190b9-169">Close the page.</span></span>
