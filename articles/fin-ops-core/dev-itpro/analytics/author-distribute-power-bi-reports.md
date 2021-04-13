---
title: Power BI Desktop を使用した分析レポートの作成
description: このトピックでは、ローカルの Entity Store データベースを使用して Power BI レポートを作成するプロセスについて説明します。
author: MilindaV2
ms.date: 01/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 265864
ms.assetid: e253a57a-979b-4ca5-8e09-2bfce97395a5
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: a689c3ebedab53fda3b47a731bc48d555dcccd37
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754534"
---
# <a name="create-analytical-reports-by-using-power-bi-desktop"></a><span data-ttu-id="469ab-103">Power BI Desktop を使用した分析レポートの作成</span><span class="sxs-lookup"><span data-stu-id="469ab-103">Create analytical reports by using Power BI Desktop</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="469ab-104">ユーザーが power user またはビジネス アナリストである場合は、自分の組織のために多くのレポートを作成している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="469ab-104">If you're a power user or a business analyst, you probably create many reports for your organization.</span></span> <span data-ttu-id="469ab-105">他のユーザーと共有する前に、データの書式設定と関連付けによって、Microsoft Excel でこれらのレポートを作成する場合があります。</span><span class="sxs-lookup"><span data-stu-id="469ab-105">You might create these reports in Microsoft Excel by formatting and relating data before you share it with other people.</span></span> <span data-ttu-id="469ab-106">レポートへの変更が必要な場合、組織内のユーザーから連絡が来る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="469ab-106">People in your organization might even come to you when they require modifications to the report.</span></span> <span data-ttu-id="469ab-107">このソリューションを使用すると、リッチでインタラクティブなレポートを簡単に作成できます。</span><span class="sxs-lookup"><span data-stu-id="469ab-107">This solution offers an easy way to create rich, interactive reports.</span></span> <span data-ttu-id="469ab-108">レポート ライターは、Microsoft Power BI Desktop をレポート ツールとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-108">As a report writer, you can use Microsoft Power BI Desktop as the reporting tool.</span></span> <span data-ttu-id="469ab-109">作成したレポートは、PowerBI.com に公開することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-109">The reports that you create can then be published to PowerBI.com.</span></span> <span data-ttu-id="469ab-110">Power BI Desktop の詳細については、[Power BI Desktop で魅力的なレポートとビジュアライゼーションを作成する](https://powerbi.microsoft.com/desktop)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="469ab-110">For more information about Power BI Desktop, see [Create stunning reports and visualizations with Power BI Desktop](https://powerbi.microsoft.com/desktop).</span></span>

## <a name="accessing-the-local-entity-store-by-using-directquery"></a><span data-ttu-id="469ab-111">DirectQuery を使用してローカル エンティティ ストアへのアクセス</span><span class="sxs-lookup"><span data-stu-id="469ab-111">Accessing the local Entity Store by using DirectQuery</span></span>
<span data-ttu-id="469ab-112">データ エンティティを介して公開されるオープン データ プロトコル (OData) エンドポイントを使用して、Microsoft Power BI レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-112">You can create Microsoft Power BI reports by using Open Data Protocol (OData) endpoints that are exposed via data entities.</span></span> <span data-ttu-id="469ab-113">このアプローチの限界にもかかわらず、エンティティ格納はレガシ ソリューションでもエンティティ格納をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="469ab-113">Despite the limitations of this approach, the Entity Store still supports it for legacy solutions.</span></span> <span data-ttu-id="469ab-114">ただし、DirectQuery は、解析ソリューションのソース データに推奨されるメソッドになりました。</span><span class="sxs-lookup"><span data-stu-id="469ab-114">However, DirectQuery is now the preferred method for sourcing data for analytical solutions.</span></span> <span data-ttu-id="469ab-115">DirectQuery の利点および制限の詳細については、[Power BI Desktop で DirectQuery の使用](https://powerbi.microsoft.com/documentation/powerbi-desktop-use-directquery/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="469ab-115">For more information about the benefits and limitations of DirectQuery, see [Use DirectQuery in Power BI Desktop](https://powerbi.microsoft.com/documentation/powerbi-desktop-use-directquery/).</span></span>

<span data-ttu-id="469ab-116">Power BI Desktop を使用すると、ローカルのエンティティ格納データベースに直接接続することによって、開発またはテスト環境でレポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-116">When you use Power BI Desktop, you can create a report in your development or test environment by connecting directly to the local Entity Store database.</span></span> <span data-ttu-id="469ab-117">レポートに問題がなければ、管理者は、ユーザーがそれを実稼働環境に移行する支援をすることができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-117">When you're satisfied with the report, your administrator can help you migrate it to your production environment.</span></span> <span data-ttu-id="469ab-118">このセクションの残りの部分では、このプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="469ab-118">The rest of this section walks you through this process.</span></span>

> [!NOTE]
> <span data-ttu-id="469ab-119">分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が独自の定期売買またはローカル コンピューターで実行している開発環境を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="469ab-119">To develop or extend analytical workspaces and reports in the application suite, customers must use a development environment running in their own subscription or on local machines.</span></span> <span data-ttu-id="469ab-120">Microsoft が提供するレベル 1 環境では、埋め込まれた分析レポートを開発または拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="469ab-120">You won’t be able to develop or extend embedded analytical reports in Microsoft-provided Tier-1 environments.</span></span> <span data-ttu-id="469ab-121">Power BI Desktop をインストールするには管理者権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="469ab-121">You need administrator rights to install Power BI Desktop.</span></span>

> <span data-ttu-id="469ab-122">レベル 1環境には、Power BI Desktop のサービス互換性があるバージョンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="469ab-122">Tier-1 environments now include a service compatible version of Power BI Desktop.</span></span> <span data-ttu-id="469ab-123">分析ワークスペースとレポートをアプリケーション スイートで開発または拡張するには、顧客が開発環境にプレインストールした Power BI Desktop を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-123">To develop or extend analytical workspaces and reports in the application suite, customers can use the Power BI Desktop application pre-installed on the development environment.</span></span> <span data-ttu-id="469ab-124">または、Power BI Desktop の最新の互換性があるリリースを使用し、プレビュー機能をオフにして、Finance and Operations アプリの分析レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="469ab-124">Alternatively, you can use the latest compatible release of Power BI Desktop with Preview features turned off to author analytical reports for Finance and Operations apps.</span></span> <span data-ttu-id="469ab-125">[Power BI Desktop の前の月次更新](https://docs.microsoft.com/power-bi/fundamentals/desktop-latest-update-archive#power-bi-desktop-monthly-update-video-3) で Power BI Desktop の 2020 年 8 月の更新プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="469ab-125">Download the August 2020 Update of Power BI Desktop at [Previous monthly updates to Power BI Desktop](https://docs.microsoft.com/power-bi/fundamentals/desktop-latest-update-archive#power-bi-desktop-monthly-update-video-3).</span></span>

### <a name="step-1-populate-the-local-entity-store-database"></a><span data-ttu-id="469ab-126">手順 1: ローカル エンティティ格納データベースに入力する</span><span class="sxs-lookup"><span data-stu-id="469ab-126">Step 1: Populate the local Entity Store database</span></span>
<span data-ttu-id="469ab-127">この例では、ローカルのエンティティ ストアでコマース 分析ソリューションが消費する集計モデルをステージングします。</span><span class="sxs-lookup"><span data-stu-id="469ab-127">For this example, we will stage the aggregate models that the Commerce analytical solution consumes in the local Entity Store.</span></span> <span data-ttu-id="469ab-128">アプリケーションが使用するモデルは、RetailCube 集計測定で定義されています。</span><span class="sxs-lookup"><span data-stu-id="469ab-128">The models that the application uses are defined in the RetailCube aggregate measurement.</span></span> 

1. <span data-ttu-id="469ab-129">クライアントで **エンティティ格納** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="469ab-129">In the client, open the **Entity Store** page.</span></span> <span data-ttu-id="469ab-130">(**システム管理** \> **設定** \> **エンティティ格納** の順に選択します。)</span><span class="sxs-lookup"><span data-stu-id="469ab-130">(Select **System administration** \> **Setup** \> **Entity Store**.)</span></span> 
2. <span data-ttu-id="469ab-131">**RetailCube** 集計測定を選択し、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-131">Select the **RetailCube** aggregate measurement, and then select **Refresh**.</span></span> 
3. <span data-ttu-id="469ab-132">バック グラウンドで実行されるジョブ名を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-132">Enter a name for the job that will be run in the background, and then select **OK**.</span></span>

<span data-ttu-id="469ab-133">次の図は、集計モデルの更新頻度を設定するために使用する管理者ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="469ab-133">The following illustration shows the administrator dialog box that is used to configure the frequency of updates for the aggregate model.</span></span>

![更新ダイアログ ボックスのコンフィギュレーション](media/Configure-refresh.png)

<span data-ttu-id="469ab-135">データをステージングするジョブの進行状況を監視するには、バッチ ジョブ監視ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="469ab-135">To monitor the progress of the job that stages the data, you can use the batch job monitoring page.</span></span> <span data-ttu-id="469ab-136">(**システム管理** \> **データベース** \> **バッチ ジョブ** の順に選択します。) デモ データを使用している場合、ジョブは 1 分ほどかかります。</span><span class="sxs-lookup"><span data-stu-id="469ab-136">(Select **System administration** \> **Database** \> **Batch jobs**.) If you're using demo data, the job should take about a minute.</span></span> <span data-ttu-id="469ab-137">データがエンティティ格納に格納された後、レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="469ab-137">After the data is in the Entity Store, you can write reports.</span></span> 

### <a name="step-2-connect-to-the-local-entity-store-database"></a><span data-ttu-id="469ab-138">手順 2: ローカル エンティティ格納データベースに接続する</span><span class="sxs-lookup"><span data-stu-id="469ab-138">Step 2: Connect to the local Entity Store database</span></span>
1. <span data-ttu-id="469ab-139">Power BI Desktop を起動します。</span><span class="sxs-lookup"><span data-stu-id="469ab-139">Start Power BI Desktop.</span></span> <span data-ttu-id="469ab-140">Power BI Desktop のアップデートが使用可能な場合は、それらをダウンロードし、適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="469ab-140">If any updates are available for Power BI Desktop, you might have to download and apply them.</span></span> 
2. <span data-ttu-id="469ab-141">Power BI **ようこそ** ページで、**データの取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-141">On the Power BI **Welcome** page, select **Get data**.</span></span> 

    <span data-ttu-id="469ab-142">または、Power BI Desktop が開始するとき、**データの取得** \> **SQL Server** を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-142">Alternatively, when Power BI Desktop starts, you can select **Get Data** \> **SQL Server**.</span></span> 

    ![Power BI Desktop でデータ メニューを取得する](media/Power-BI-Desktop-Get-Data.png)

3. <span data-ttu-id="469ab-144">**SQL Server データベース** ダイアログ ボックスに **.** と入力します。</span><span class="sxs-lookup"><span data-stu-id="469ab-144">In the **SQL Server Database** dialog box, enter **.**</span></span> <span data-ttu-id="469ab-145">サーバー名として、および **AxDW** をデータベースとして。</span><span class="sxs-lookup"><span data-stu-id="469ab-145">as the server name and **AxDW** as the database name.</span></span> <span data-ttu-id="469ab-146">その後、**DirectQuery** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-146">Then select the **DirectQuery** option.</span></span> 

    <span data-ttu-id="469ab-147">次の図は、Power BI Desktop がローカルのエンティティ格納データベースにアクセスするための設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="469ab-147">The following illustration shows the settings that enable Power BI Desktop to access the local Entity Store database.</span></span>

    ![ローカル エンティティ格納データベースにアクセスするための設定](media/Connect-to-SQL-Database.png)

    > [!NOTE]
    > <span data-ttu-id="469ab-149">**インポート** オプションは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="469ab-149">The **Import** option isn't currently supported.</span></span>

4. <span data-ttu-id="469ab-150">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-150">Select **OK**.</span></span> 

    <span data-ttu-id="469ab-151">**ナビゲーター** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="469ab-151">The **Navigator** dialog box appears.</span></span> <span data-ttu-id="469ab-152">このダイアログ ボックスを使用して、レポートの対象となるテーブルとビューをエンティティ格納から選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-152">You use this dialog box to select which tables and views from the Entity Store you want to report on.</span></span> 

5. <span data-ttu-id="469ab-153">検索ボックスで、**Retail** と入力して RetailCube 集計測定に関連するエンティティについてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="469ab-153">In the search box, enter **Retail** to filter for entities that are related to the RetailCube aggregate measurement.</span></span>
6. <span data-ttu-id="469ab-154">ナビゲーターに表示された **RetailCube\_RetailTransDetailsView** テーブルを選択し、**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="469ab-154">Select the **RetailCube\_RetailTransDetailsView** table that is shown in the navigator, and then select **Load**.</span></span> 

<span data-ttu-id="469ab-155">レポートを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="469ab-155">You can now create a report.</span></span> <span data-ttu-id="469ab-156">測定およびフィールドはキャンバスにドラッグして、データおよび傾向を対話的に参照することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-156">You can drag measures and fields to the canvas, and can explore data and trends interactively.</span></span>

<span data-ttu-id="469ab-157">次の図は、ローカルの Entity Store データベースをソースとして使用する基本レポートを示しています。</span><span class="sxs-lookup"><span data-stu-id="469ab-157">The following illustration shows a basic report that uses the local Entity Store database as its source.</span></span>

![Power BI Desktop レポート](media/Power-BI-Desktop-Report.png)

<span data-ttu-id="469ab-159">Power BI Desktop でも計算の作成がサポートされ、複数の集計測定のデータを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-159">Power BI Desktop also supports the creation of calculations and lets you combine data from multiple aggregate measurements.</span></span> <span data-ttu-id="469ab-160">数分で、ローカルの開発環境でデータを使用することにより分析レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-160">Within minutes, you can create analytical reports by using data in the local development environment.</span></span> <span data-ttu-id="469ab-161">レポートに問題がなければ、それを実稼働環境に移行できます。これにより、ユーザーは、そのレポートを使用して、実稼働データにかかわることができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-161">When you're satisfied with the report, you can migrate it to the production environment, so that users can use the report to interact with production data.</span></span>

## <a name="validating-reports-in-a-demo-environment"></a><span data-ttu-id="469ab-162">デモ環境でのレポートの検証</span><span class="sxs-lookup"><span data-stu-id="469ab-162">Validating reports in a demo environment</span></span>

<span data-ttu-id="469ab-163">レポートにはデベロッパー環境のデモまたはテスト データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="469ab-163">The report shows the demo or test data in your developer environment.</span></span> <span data-ttu-id="469ab-164">デモ環境にレポートを統合する場合は、引き続きこのレポートを PowerBI.com アカウントに公開し、クライアントに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="469ab-164">If you want to integrate the report into a demo environment, you can continue to publish this report to your PowerBI.com account and pin it to the client.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]