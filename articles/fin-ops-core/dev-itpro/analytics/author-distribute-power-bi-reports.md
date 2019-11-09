---
title: Power BI Desktop を使用した分析レポートの作成
description: このトピックでは、ローカルの Entity Store データベースを使用して Power BI レポートを作成するプロセスについて説明します。
author: MilindaV2
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265864
ms.assetid: e253a57a-979b-4ca5-8e09-2bfce97395a5
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 16ca0284fe442e40476bbf61bca070cfc0dc3f92
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174580"
---
# <a name="create-analytical-reports-by-using-power-bi-desktop"></a><span data-ttu-id="57e13-103">Power BI Desktop を使用した分析レポートの作成</span><span class="sxs-lookup"><span data-stu-id="57e13-103">Create analytical reports by using Power BI Desktop</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57e13-104">ユーザーが power user またはビジネス アナリストである場合は、自分の組織のために多くのレポートを作成している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="57e13-104">If you're a power user or a business analyst, you probably create many reports for your organization.</span></span> <span data-ttu-id="57e13-105">他のユーザーと共有する前に、データの書式設定と関連付けによって、Microsoft Excel でこれらのレポートを作成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="57e13-105">You might create these reports in Microsoft Excel by formatting and relating data before you share it with other people.</span></span> <span data-ttu-id="57e13-106">レポートへの変更が必要な場合、組織内のユーザーから連絡が来る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="57e13-106">People in your organization might even come to you when they require modifications to the report.</span></span> <span data-ttu-id="57e13-107">このソリューションを使用すると、リッチでインタラクティブなレポートを簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="57e13-107">This solution offers an easy way to create rich, interactive reports.</span></span> <span data-ttu-id="57e13-108">レポート ライターは、Microsoft Power BI Desktop をレポート ツールとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-108">As a report writer, you can use Microsoft Power BI Desktop as the reporting tool.</span></span> <span data-ttu-id="57e13-109">作成したレポートは、PowerBI.com に公開することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-109">The reports that you create can then be published to PowerBI.com.</span></span> <span data-ttu-id="57e13-110">Power BI Desktop の詳細については、[Power BI Desktop で魅力的なレポートとビジュアライゼーションを作成する](https://powerbi.microsoft.com/desktop)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57e13-110">For more information about Power BI Desktop, see [Create stunning reports and visualizations with Power BI Desktop](https://powerbi.microsoft.com/desktop).</span></span>

## <a name="accessing-the-local-entity-store-by-using-directquery"></a><span data-ttu-id="57e13-111">DirectQuery を使用してローカル エンティティ ストアへのアクセス</span><span class="sxs-lookup"><span data-stu-id="57e13-111">Accessing the local Entity Store by using DirectQuery</span></span>
<span data-ttu-id="57e13-112">データ エンティティを介して公開されるオープン データ プロトコル (OData) エンドポイントを使用して、Microsoft Power BI レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-112">You can create Microsoft Power BI reports by using Open Data Protocol (OData) endpoints that are exposed via data entities.</span></span><span data-ttu-id="57e13-113">このアプローチの限界にもかかわらず、エンティティ格納は従来のソリューションでもエンティティ格納をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="57e13-113"> Despite the limitations of this approach, the Entity Store still supports it for legacy solutions.</span></span> <span data-ttu-id="57e13-114">ただし、DirectQuery は、解析ソリューションのソース データに推奨されるメソッドになりました。</span><span class="sxs-lookup"><span data-stu-id="57e13-114">However, DirectQuery is now the preferred method for sourcing data for analytical solutions.</span></span> <span data-ttu-id="57e13-115">DirectQuery の利点および制限の詳細については、[Power BI Desktop で DirectQuery の使用](https://powerbi.microsoft.com/documentation/powerbi-desktop-use-directquery/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57e13-115">For more information about the benefits and limitations of DirectQuery, see [Use DirectQuery in Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-use-directquery/).</span></span>

<span data-ttu-id="57e13-116">Power BI Desktop を使用すると、ローカルのエンティティ格納データベースに直接接続することによって、開発またはテスト環境でレポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-116">When you use Power BI Desktop, you can create a report in your development or test environment by connecting directly to the local Entity Store database.</span></span> <span data-ttu-id="57e13-117">レポートに問題がなければ、管理者は、ユーザーがそれを実稼働環境に移行する支援をすることができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-117">When you're satisfied with the report, your administrator can help you migrate it to your production environment.</span></span> <span data-ttu-id="57e13-118">このセクションの残りの部分では、このプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="57e13-118">The rest of this section walks you through this process.</span></span>

> [!NOTE]
> <span data-ttu-id="57e13-119">分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が独自の定期売買またはローカル コンピューターで実行している開発環境を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e13-119">To develop or extend analytical workspaces and reports in the application suite, customers must use a development environment running in their own subscription or on local machines.</span></span> <span data-ttu-id="57e13-120">Microsoft が提供するレベル 1 環境では、埋め込まれた分析レポートを開発または拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="57e13-120">You won’t be able to develop or extend embedded analytical reports in Microsoft-provided, Tier-1 environments.</span></span> <span data-ttu-id="57e13-121">Power BI Desktop をインストールするには管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="57e13-121">You need administrator rights to install Power BI Desktop.</span></span>

### <a name="step-1-populate-the-local-entity-store-database"></a><span data-ttu-id="57e13-122">手順 1: ローカル エンティティ格納データベースに入力する</span><span class="sxs-lookup"><span data-stu-id="57e13-122">Step 1: Populate the local Entity Store database</span></span>
<span data-ttu-id="57e13-123">この例では、ローカルのエンティティ ストアで Retail 分析ソリューションが消費する集計モデルをステージングします。</span><span class="sxs-lookup"><span data-stu-id="57e13-123">For this example, we will stage the aggregate models that the Retail analytical solution consumes in the local Entity Store.</span></span> <span data-ttu-id="57e13-124">Retail アプリケーションが使用するモデルは、RetailCube 集計測定で定義されています。</span><span class="sxs-lookup"><span data-stu-id="57e13-124">The models that the Retail application uses are defined in the RetailCube aggregate measurement.</span></span> 

1. <span data-ttu-id="57e13-125">クライアントで**エンティティ格納**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="57e13-125">In the client, open the **Entity Store** page.</span></span> <span data-ttu-id="57e13-126">(**システム管理** \> **設定** \> **エンティティ格納**の順に選択します。)</span><span class="sxs-lookup"><span data-stu-id="57e13-126">(Select **System administration** \> **Setup** \> **Entity Store**.)</span></span> 
2. <span data-ttu-id="57e13-127">**RetailCube** 集計測定を選択し、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-127">Select the **RetailCube** aggregate measurement, and then select **Refresh**.</span></span> 
3. <span data-ttu-id="57e13-128">バック グラウンドで実行されるジョブ名を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-128">Enter a name for the job that will be run in the background, and then select **OK**.</span></span>

<span data-ttu-id="57e13-129">次の図は、集計モデルの更新頻度を設定するために使用する管理者ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="57e13-129">The following illustration shows the administrator dialog box that is used to configure the frequency of updates for the aggregate model.</span></span>

![更新ダイアログ ボックスのコンフィギュレーション](media/Configure-refresh.png)

<span data-ttu-id="57e13-131">データをステージングするジョブの進行状況を監視するには、バッチ ジョブ監視ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="57e13-131">To monitor the progress of the job that stages the data, you can use the batch job monitoring page.</span></span> <span data-ttu-id="57e13-132">(**システム管理** \> **データベース** \> **バッチ ジョブ**の順に選択します。) デモ データを使用している場合、ジョブは 1 分ほどかかります。</span><span class="sxs-lookup"><span data-stu-id="57e13-132">(Select **System administration** \> **Database** \> **Batch jobs**.) If you're using demo data, the job should take about a minute.</span></span> <span data-ttu-id="57e13-133">データがエンティティ格納に格納された後、レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="57e13-133">After the data is in the Entity Store, you can write reports.</span></span> 

### <a name="step-2-connect-to-the-local-entity-store-database"></a><span data-ttu-id="57e13-134">手順 2: ローカル エンティティ格納データベースに接続する</span><span class="sxs-lookup"><span data-stu-id="57e13-134">Step 2: Connect to the local Entity Store database</span></span>
1. <span data-ttu-id="57e13-135">Power BI Desktop を起動します。</span><span class="sxs-lookup"><span data-stu-id="57e13-135">Start Power BI Desktop.</span></span> <span data-ttu-id="57e13-136">Power BI Desktop のアップデートが使用可能な場合は、それらをダウンロードし、適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57e13-136">If any updates are available for Power BI Desktop, you might have to download and apply them.</span></span> 
2. <span data-ttu-id="57e13-137">Power BI **ようこそ** ページで、**データの取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-137">On the Power BI **Welcome** page, select **Get data**.</span></span> 

    <span data-ttu-id="57e13-138">または、Power BI Desktop が開始するとき、**データの取得** \> **SQL Server** を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-138">Alternatively, when Power BI Desktop starts, you can select **Get Data** \> **SQL Server**.</span></span> 

    ![Power BI Desktop でデータ メニューを取得する](media/Power-BI-Desktop-Get-Data.png)

3. <span data-ttu-id="57e13-140">**SQL Server データベース** ダイアログ ボックスに **.** と入力します。</span><span class="sxs-lookup"><span data-stu-id="57e13-140">In the **SQL Server Database** dialog box, enter **.**</span></span> <span data-ttu-id="57e13-141">サーバー名として、および **AxDW** をデータベースとして。</span><span class="sxs-lookup"><span data-stu-id="57e13-141">as the server name and **AxDW** as the database name.</span></span> <span data-ttu-id="57e13-142">その後、**DirectQuery** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-142">Then select the **DirectQuery** option.</span></span> 

    <span data-ttu-id="57e13-143">次の図は、Power BI Desktop がローカルのエンティティ格納データベースにアクセスするための設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="57e13-143">The following illustration shows the settings that enable Power BI Desktop to access the local Entity Store database.</span></span>

    ![ローカル エンティティ格納データベースにアクセスするための設定](media/Connect-to-SQL-Database.png)

    > [!NOTE]
    > <span data-ttu-id="57e13-145">**インポート** オプションは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="57e13-145">The **Import** option isn't currently supported.</span></span>

4. <span data-ttu-id="57e13-146">**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-146">Select **OK**.</span></span> 

    <span data-ttu-id="57e13-147">**ナビゲーター** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="57e13-147">The **Navigator** dialog box appears.</span></span> <span data-ttu-id="57e13-148">このダイアログ ボックスを使用して、レポートの対象となるテーブルとビューをエンティティ格納から選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-148">You use this dialog box to select which tables and views from the Entity Store you want to report on.</span></span> 

5. <span data-ttu-id="57e13-149">検索ボックスで、**Retail** と入力して RetailCube 集計測定に関連するエンティティについてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="57e13-149">In the search box, enter **Retail** to filter for entities that are related to the RetailCube aggregate measurement.</span></span>
6. <span data-ttu-id="57e13-150">ナビゲーターに表示された **RetailCube\_RetailTransDetailsView** テーブルを選択し、**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="57e13-150">Select the **RetailCube\_RetailTransDetailsView** table that is shown in the navigator, and then select **Load**.</span></span> 

<span data-ttu-id="57e13-151">レポートを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="57e13-151">You can now create a report.</span></span> <span data-ttu-id="57e13-152">測定およびフィールドはキャンバスにドラッグして、データおよび傾向を対話的に参照することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-152">You can drag measures and fields to the canvas, and can explore data and trends interactively.</span></span>

<span data-ttu-id="57e13-153">次の図は、ローカルの Entity Store データベースをソースとして使用する基本レポートを示しています。</span><span class="sxs-lookup"><span data-stu-id="57e13-153">The following illustration shows a basic report that uses the local Entity Store database as its source.</span></span>

![Power BI Desktop レポート](media/Power-BI-Desktop-Report.png)

<span data-ttu-id="57e13-155">Power BI Desktop でも計算の作成がサポートされ、複数の集計測定のデータを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-155">Power BI Desktop also supports the creation of calculations and lets you combine data from multiple aggregate measurements.</span></span> <span data-ttu-id="57e13-156">数分で、ローカルの開発環境でデータを使用することにより分析レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-156">Within minutes, you can create analytical reports by using data in the local development environment.</span></span> <span data-ttu-id="57e13-157">レポートに問題がなければ、それを実稼働環境に移行できます。これにより、ユーザーは、そのレポートを使用して、実稼働データにかかわることができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-157">When you're satisfied with the report, you can migrate it to the production environment, so that users can use the report to interact with production data.</span></span>

## <a name="validating-reports-in-a-demo-environment"></a><span data-ttu-id="57e13-158">デモ環境でのレポートの検証</span><span class="sxs-lookup"><span data-stu-id="57e13-158">Validating reports in a demo environment</span></span>

<span data-ttu-id="57e13-159">レポートにはデベロッパー環境のデモまたはテスト データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="57e13-159">The report shows the demo or test data in your developer environment.</span></span> <span data-ttu-id="57e13-160">デモ環境にレポートを統合する場合は、引き続きこのレポートを PowerBI.com アカウントに公開し、クライアントに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="57e13-160">If you want to integrate the report into a demo environment, you can continue to publish this report to your PowerBI.com account and pin it to the client.</span></span> 