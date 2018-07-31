---
title: "Power BI Desktop を使用して分析レポートを作成する"
description: "このトピックでは、ローカルの Entity Store データベースを使用して Power BI レポートを作成するプロセスについて説明します。"
author: MilindaV2
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: BIMeasurementDeployManagementEntityStore
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265864
ms.assetid: e253a57a-979b-4ca5-8e09-2bfce97395a5
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.translationtype: HT
ms.sourcegitcommit: 8779134ef16a828635dfe0179881843076926bbe
ms.openlocfilehash: e9d43cf4225839305685a7b6129130c106380707
ms.contentlocale: ja-jp
ms.lasthandoff: 05/09/2018

---

# <a name="author-analytical-reports-by-using-power-bi-desktop"></a><span data-ttu-id="641b1-103">Power BI Desktop を使用して分析レポートを作成する</span><span class="sxs-lookup"><span data-stu-id="641b1-103">Author analytical reports by using Power BI Desktop</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="641b1-104">ユーザーが power user またはビジネス アナリストである場合は、自分の組織のために多くのレポートを作成している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="641b1-104">If you're a power user or a business analyst, you probably create many reports for your organization.</span></span> <span data-ttu-id="641b1-105">他のユーザーと共有する前に、データの書式設定と関連付けによって、Microsoft Excel でこれらのレポートを作成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="641b1-105">You might create these reports in Microsoft Excel by formatting and relating data before you share it with other people.</span></span> <span data-ttu-id="641b1-106">レポートへの変更が必要な場合、組織内のユーザーから連絡が来る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="641b1-106">People in your organization might even come to you when they require modifications to the report.</span></span> <span data-ttu-id="641b1-107">このソリューションを使用すると、リッチでインタラクティブなレポートを簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="641b1-107">This solution offers an easy way to create rich, interactive reports.</span></span> <span data-ttu-id="641b1-108">レポート ライターは、 Microsoft Power BI デスクトップをレポート ツールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="641b1-108">As a report writer, you can use Microsoft Power BI Desktop as the reporting tool.</span></span> <span data-ttu-id="641b1-109">その後、作成したレポートを PowerBI.com に公開できます。Power BI Desktop について詳しくは、「[Power BI Desktop で魅力的なレポートとビジュアライゼーションを作成する](https://powerbi.microsoft.com/en-us/desktop)」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="641b1-109">The reports that you create can then be published to PowerBI.com. For more information about Power BI Desktop, see [Create stunning reports and visualizations with Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop).</span></span>

## <a name="accessing-the-local-entity-store-by-using-directquery"></a><span data-ttu-id="641b1-110">DirectQuery を使用してローカル エンティティ ストアへのアクセス</span><span class="sxs-lookup"><span data-stu-id="641b1-110">Accessing the local Entity Store by using DirectQuery</span></span>
<span data-ttu-id="641b1-111">Microsoft Dynamics 365 for Finance and Operations では、データ エンティティで公開されるオープン データ プロトコル (OData) のエンドポイントを使用して Microsoft Power BI レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="641b1-111">In Microsoft Dynamics 365 for Finance and Operations, you can create Microsoft Power BI reports by using Open Data Protocol (OData) endpoints that are exposed via data entities.</span></span> <span data-ttu-id="641b1-112">このアプローチの限界にもかかわらず、エンティティ格納は従来のソリューションでもエンティティ格納をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="641b1-112">Despite the limitations of this approach, the Entity Store still supports it for legacy solutions.</span></span> <span data-ttu-id="641b1-113">ただし、DirectQuery は、解析ソリューションのソース データに推奨されるメソッドになりました。</span><span class="sxs-lookup"><span data-stu-id="641b1-113">However, DirectQuery is now the preferred method for sourcing data for analytical solutions.</span></span> <span data-ttu-id="641b1-114">DirectQuery の利点および制限の詳細については、[Power BI Desktop で DirectQuery の使用](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-use-directquery/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="641b1-114">For more information about the benefits and limitations of DirectQuery, see [Use DirectQuery in Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-use-directquery/).</span></span>

<span data-ttu-id="641b1-115">Power BI デスクトップを使用すると、ローカルのエンティティ格納データベースに直接接続することによって、開発またはテスト環境でレポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="641b1-115">When you use Power BI Desktop, you can create a report in your development or test environment by connecting directly to the local Entity Store database.</span></span> <span data-ttu-id="641b1-116">レポートに問題がなければ、管理者は、ユーザーがそれを実稼働環境に移行する支援をすることができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-116">When you're satisfied with the report, your administrator can help you migrate it to your production environment.</span></span> <span data-ttu-id="641b1-117">このセクションの残りの部分では、このプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="641b1-117">The rest of this section walks you through this process.</span></span>

> [!Note]
> <span data-ttu-id="641b1-118">分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が独自の定期売買またはローカル コンピューターで実行している開発環境を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="641b1-118">To develop or extend analytical workspaces and reports in the application suite, customers must use a development environment running in their own subscription or on local machines.</span></span> <span data-ttu-id="641b1-119">Microsoft が提供するレベル 1 環境では、埋め込まれた分析レポートを開発または拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="641b1-119">You won’t be able to develop or extend embedded analytical reports in Microsoft-provided, Tier-1 environments.</span></span> <span data-ttu-id="641b1-120">Power BI デスクトップをインストールするための管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="641b1-120">You need administrator rights to install Power BI Desktop.</span></span>

### <a name="step-1-populate-the-local-entity-store-database"></a><span data-ttu-id="641b1-121">手順 1: ローカル エンティティ格納データベースに入力する</span><span class="sxs-lookup"><span data-stu-id="641b1-121">Step 1: Populate the local Entity Store database</span></span>
<span data-ttu-id="641b1-122">この例では、ローカルのエンティティ ストアで Retail 分析ソリューションが消費する集計モデルをステージングします。</span><span class="sxs-lookup"><span data-stu-id="641b1-122">For this example, we will stage the aggregate models that the Retail analytical solution consumes in the local Entity Store.</span></span> <span data-ttu-id="641b1-123">Retail アプリケーションが使用するモデルは、RetailCube 集計測定で定義されています。</span><span class="sxs-lookup"><span data-stu-id="641b1-123">The models that the Retail application uses are defined in the RetailCube aggregate measurement.</span></span> 

1. <span data-ttu-id="641b1-124">Finance and Operations クライアントで**エンティティ格納**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="641b1-124">In the Finance and Operations client, open the **Entity Store** page.</span></span> <span data-ttu-id="641b1-125">(**システム管理** > **設定** > **エンティティ格納**の順に選択します。)</span><span class="sxs-lookup"><span data-stu-id="641b1-125">(Select **System administration** > **Setup** > **Entity Store**.)</span></span> 
2. <span data-ttu-id="641b1-126">**RetailCube** 集計測定を選択し、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-126">Select the **RetailCube** aggregate measurement, and then select **Refresh**.</span></span> 
3. <span data-ttu-id="641b1-127">バック グラウンドで実行されるジョブ名を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-127">Enter a name for the job that will be run in the background, and then select **OK**.</span></span>

<span data-ttu-id="641b1-128">次の図は、集計モデルの更新頻度を設定するために使用する管理者ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="641b1-128">The following illustration shows the administrator dialog box that is used to configure the frequency of updates for the aggregate model.</span></span>

![更新ダイアログ ボックスのコンフィギュレーション](media/Configure-refresh.png)

<span data-ttu-id="641b1-130">データをステージングするジョブの進行状況を監視するには、バッチ ジョブ監視ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="641b1-130">To monitor the progress of the job that stages the data, you can use the batch job monitoring page.</span></span> <span data-ttu-id="641b1-131">(**システム管理** > **データベース** > **バッチ ジョブ**の順に選択します。) デモ データを使用している場合、ジョブは 1 分ほどかかります。</span><span class="sxs-lookup"><span data-stu-id="641b1-131">(Select **System administration** > **Database** > **Batch jobs**.) If you're using demo data, the job should take about a minute.</span></span> <span data-ttu-id="641b1-132">データがエンティティ格納に格納された後、レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="641b1-132">After the data is in the Entity Store, you can write reports.</span></span> 

### <a name="step-2-connect-to-the-local-entity-store-database"></a><span data-ttu-id="641b1-133">手順 2: ローカル エンティティ格納データベースに接続する</span><span class="sxs-lookup"><span data-stu-id="641b1-133">Step 2: Connect to the local Entity Store database</span></span>
1. <span data-ttu-id="641b1-134">Power BI デスクトップを起動します。</span><span class="sxs-lookup"><span data-stu-id="641b1-134">Start Power BI Desktop.</span></span> <span data-ttu-id="641b1-135">Power BI デスクトップのアップデートがある場合は、それらをダウンロードし、適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="641b1-135">If any updates are available for Power BI Desktop, you might have to download and apply them.</span></span> 
2. <span data-ttu-id="641b1-136">Power BI **ようこそ**ページで、**データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="641b1-136">On the Power BI **Welcome** page, select **Get data**.</span></span> 

    <span data-ttu-id="641b1-137">または、Power BI デスクトップが開始すると、**データの取得** > **SQL Server** を選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-137">Alternatively, when Power BI Desktop starts, you can select **Get Data** > **SQL Server**.</span></span> 

    ![Power BI デスクトップ内でデータ メニューを取得します](media/Power-BI-Desktop-Get-Data.png)

3. <span data-ttu-id="641b1-139">**SQL Server データベース** ダイアログ ボックスに **.** と入力します。</span><span class="sxs-lookup"><span data-stu-id="641b1-139">In the **SQL Server Database** dialog box, enter **.**</span></span> <span data-ttu-id="641b1-140">サーバー名として、および **AxDW** をデータベースとして。</span><span class="sxs-lookup"><span data-stu-id="641b1-140">as the server name and **AxDW** as the database name.</span></span> <span data-ttu-id="641b1-141">その後、**DirectQuery** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-141">Then select the **DirectQuery** option.</span></span> 

    <span data-ttu-id="641b1-142">次の図は、Power BI デスクトップがローカルのエンティティ格納データベースにアクセスするための設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="641b1-142">The following illustration shows the settings that enable Power BI Desktop to access the local Entity Store database.</span></span>

    ![ローカル エンティティ格納データベースにアクセスするための設定](media/Connect-to-SQL-Database.png)

    > [!NOTE]
    > <span data-ttu-id="641b1-144">**インポート** オプションは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="641b1-144">The **Import** option isn't currently supported.</span></span>

4. <span data-ttu-id="641b1-145">**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-145">Select **OK**.</span></span> 

    <span data-ttu-id="641b1-146">**ナビゲーター** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="641b1-146">The **Navigator** dialog box appears.</span></span> <span data-ttu-id="641b1-147">このダイアログ ボックスを使用して、レポートの対象となるテーブルとビューをエンティティ格納から選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-147">You use this dialog box to select which tables and views from the Entity Store you want to report on.</span></span> 

5. <span data-ttu-id="641b1-148">検索ボックスで、**Retail** と入力して RetailCube 集計測定に関連するエンティティについてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="641b1-148">In the search box, enter **Retail** to filter for entities that are related to the RetailCube aggregate measurement.</span></span>
6. <span data-ttu-id="641b1-149">ナビゲーターに表示された **RetailCube_RetailTransDetailsView** テーブルを選択し、**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="641b1-149">Select the **RetailCube_RetailTransDetailsView** table that is shown in the navigator, and then select **Load**.</span></span> 

<span data-ttu-id="641b1-150">レポートを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="641b1-150">You can now create a report.</span></span> <span data-ttu-id="641b1-151">測定およびフィールドはキャンバスにドラッグして、データおよび傾向を対話的に参照することができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-151">You can drag measures and fields to the canvas, and can explore data and trends interactively.</span></span>

<span data-ttu-id="641b1-152">次の図は、ローカルの Entity Store データベースをソースとして使用する基本レポートを示しています。</span><span class="sxs-lookup"><span data-stu-id="641b1-152">The following illustration shows a basic report that uses the local Entity Store database as its source.</span></span>

![Power BI デスクトップ レポート](media/Power-BI-Desktop-Report.png)

<span data-ttu-id="641b1-154">Power BI デスクトップでも、計算の作成がサポートされ、複数の集計測定のデータを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-154">Power BI Desktop also supports the creation of calculations and lets you combine data from multiple aggregate measurements.</span></span> <span data-ttu-id="641b1-155">数分で、ローカルの開発環境でデータを使用することにより分析レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-155">Within minutes, you can create analytical reports by using data in the local development environment.</span></span> <span data-ttu-id="641b1-156">レポートに問題がなければ、それを実稼働環境に移行できます。これにより、ユーザーは、そのレポートを使用して、実稼働データにかかわることができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-156">When you're satisfied with the report, you can migrate it to the production environment, so that users can use the report to interact with production data.</span></span>

## <a name="validating-reports-in-a-demo-environment"></a><span data-ttu-id="641b1-157">デモ環境でのレポートの検証</span><span class="sxs-lookup"><span data-stu-id="641b1-157">Validating reports in a demo environment</span></span>

<span data-ttu-id="641b1-158">レポートにはデベロッパー環境のデモまたはテスト データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="641b1-158">The report shows the demo or test data in your developer environment.</span></span> <span data-ttu-id="641b1-159">デモ環境にレポートを統合する場合は、引き続きこのレポートを PowerBI.com アカウントに公開し、Finance and Operations クライアントに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="641b1-159">If you want to integrate the report into a demo environment, you can continue to publish this report to your PowerBI.com account and pin it to the Finance and Operations client.</span></span> 

