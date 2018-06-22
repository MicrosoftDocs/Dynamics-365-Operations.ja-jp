---
title: "フリート管理のサンプル アプリケーション"
description: "このチュートリアルでは、フリート管理のサンプル アプリケーションがサポートするように設計されたエンド ツー エンドのシナリオを説明します。"
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 10254
ms.assetid: e289504e-a1d9-44b7-8f84-f99f330321d6
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7999982b42bbdc0c3ce72b00ca81b904de65769e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="fleet-management-sample-application"></a><span data-ttu-id="382e9-103">フリート管理のサンプル アプリケーション</span><span class="sxs-lookup"><span data-stu-id="382e9-103">Fleet Management sample application</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="382e9-104">このチュートリアルでは、フリート管理のサンプル アプリケーションがサポートするように設計されたエンド ツー エンドのシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="382e9-104">This tutorial walks you through an end-to-end scenario that the Fleet Management sample application is designed to support.</span></span>

<span data-ttu-id="382e9-105">このチュートリアルでは、フリート管理サンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="382e9-105">In this tutorial, you’ll take a tour of the Fleet Management sample.</span></span> <span data-ttu-id="382e9-106">このチュートリアルの概要では、背景知識とコンテキスト情報を提供しています。</span><span class="sxs-lookup"><span data-stu-id="382e9-106">The overviews in this tutorial provide some background knowledge and contextual info.</span></span> <span data-ttu-id="382e9-107">このサンプル アプリケーションのサポートの目的のエンド ツー エンドのシナリオを検討します。</span><span class="sxs-lookup"><span data-stu-id="382e9-107">You’ll walk through an end-to-end scenario that this sample application is designed to support.</span></span> <span data-ttu-id="382e9-108">これは、他のチュートリアルに進む前に知っておくべき情報です。</span><span class="sxs-lookup"><span data-stu-id="382e9-108">This is information that you should have before proceeding to other tutorials.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="382e9-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="382e9-109">Prerequisite</span></span>
-   <span data-ttu-id="382e9-110">このチュートリアルを開始する前に、エンド ユーザーとして最初にプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-110">You must first be provisioned as an end user before you start this tutorial.</span></span>
-   <span data-ttu-id="382e9-111">このチュートリアルでは主に、FleetManagement に移行したプロジェクトとそれによって構築されるアプリケーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="382e9-111">This tutorial mainly explores the FleetManagement Migrated project and the application that it builds.</span></span>

## <a name="installing-the-demo-data"></a><span data-ttu-id="382e9-112">デモ データのインストール</span><span class="sxs-lookup"><span data-stu-id="382e9-112">Installing the demo data</span></span>
<span data-ttu-id="382e9-113">サンプルを操作するには、提供されているデモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-113">To work with the sample, you must install the provided demo data.</span></span>

1.  <span data-ttu-id="382e9-114">VM で、Internet Explorer を開き、アプリケーションのベース URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-114">In the VM, open Internet Explorer and navigate to the application's base URL.</span></span>
2.  <span data-ttu-id="382e9-115">サインインします。</span><span class="sxs-lookup"><span data-stu-id="382e9-115">Sign in.</span></span>
3.  <span data-ttu-id="382e9-116">ダッシュ ボードで、ナビゲーション ウィンドウを開き、**フリート管理 &gt; 設定 &gt; フリート設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-116">On the dashboard, open the navigation pane and go to **Fleet Management &gt; Setup &gt; Fleet setup**.</span></span> 

    <span data-ttu-id="382e9-117">[![フリート設定](./media/fleetsetup1_introfleetmgmt1.png)](./media/fleetsetup1_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-117">[![Fleet Setup](./media/fleetsetup1_introfleetmgmt1.png)](./media/fleetsetup1_introfleetmgmt1.png)</span></span>

4.  <span data-ttu-id="382e9-118">**デモ データの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-118">Click **Setup Demo Data**.</span></span> 

    <span data-ttu-id="382e9-119">[![デモ データの読み込み](./media/loaddemodata_introfleetmgmt1.png)](./media/loaddemodata_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-119">[![Load Demo Data](./media/loaddemodata_introfleetmgmt1.png)](./media/loaddemodata_introfleetmgmt1.png)</span></span>

5.  <span data-ttu-id="382e9-120">デモ データの再読み込みを促すメッセージが表示されたら、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-120">If you're prompted to reload the demo data, click **Yes**.</span></span>
6.  <span data-ttu-id="382e9-121">データが読み込みを完了したら、**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-121">When the data is finished loading, click **Close**.</span></span>

## <a name="use-the-fleet-management-application-to-rent-a-vehicle"></a><span data-ttu-id="382e9-122">車両をレンタルするには、フリート管理アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="382e9-122">Use the Fleet Management application to rent a vehicle</span></span>
<span data-ttu-id="382e9-123">このセクションで移行したアプリで作業していることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="382e9-123">Keep in mind that you’re working with the migrated app in this section.</span></span> <span data-ttu-id="382e9-124">表示されるフォームは、Microsoft Dynamics AX 2012 バージョンのサンプルから直接ポートされます。</span><span class="sxs-lookup"><span data-stu-id="382e9-124">The forms that you see are directly ported from the Microsoft Dynamics AX 2012 version of the sample.</span></span> <span data-ttu-id="382e9-125">変更および再編成されていますが、再考されてはいません。</span><span class="sxs-lookup"><span data-stu-id="382e9-125">Although they have been modified and restyled, they have not been reimagined.</span></span>

1.  <span data-ttu-id="382e9-126">Internet Explorer を開き、Microsoft Dynamics 365 for Finance and Operations にサインインします。</span><span class="sxs-lookup"><span data-stu-id="382e9-126">Open Internet Explorer, and sign into Microsoft Dynamics 365 for Finance and Operations.</span></span>
2.  <span data-ttu-id="382e9-127">**ダッシュ ボード**に戻るには、ページの左上隅にある Microsoft Dynamics ロゴをクリックします。[![ダッシュに戻る](./media/returntodash_introfleetmgmt.png)](./media/returntodash_introfleetmgmt.png) ダッシュボードは主要なハブです。</span><span class="sxs-lookup"><span data-stu-id="382e9-127">To return to the **Dashboard**, click the Microsoft Dynamics logo in the top-left corner of the page.[![Return to Dash](./media/returntodash_introfleetmgmt.png)](./media/returntodash_introfleetmgmt.png) The dashboard is the main working hub.</span></span> <span data-ttu-id="382e9-128">セクションに分類され、アプリケーションの一部になる、様々なタイルを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="382e9-128">You can see the various tiles, organized into sections, which lead to parts of the application.</span></span> <span data-ttu-id="382e9-129">ダッシュボードは、水平スクロール用に設計されています。これは、最新のデバイスでうまく動作するための最適化です。</span><span class="sxs-lookup"><span data-stu-id="382e9-129">The dashboard is designed for horizontal scrolling, which is an optimization for working well on modern devices.</span></span> <span data-ttu-id="382e9-130">ダッシュボードの右側にあるボタンにはナビゲーションバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-130">The button to the right of the dashboard shows the navigation bar.</span></span>
3.  <span data-ttu-id="382e9-131">ダッシュ ボードから、ナビゲーション バーを開いて**フリート管理** &gt; **共通** &gt; **顧客** &gt; **顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-131">From the Dashboard, open the navigation bar and go to **Fleet Management** &gt; **Common** &gt; **Customers** &gt; **Customer**.</span></span> 

    <span data-ttu-id="382e9-132">[[![顧客](./media/customers_introfleetmgmt.png)](./media/customers_introfleetmgmt.png)]</span><span class="sxs-lookup"><span data-stu-id="382e9-132">[![Customers](./media/customers_introfleetmgmt.png)](./media/customers_introfleetmgmt.png)</span></span> 

    <span data-ttu-id="382e9-133">[![新規顧客](./media/newcustomer_introfleetmgmt1.png)](./media/newcustomer_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-133">[![New Customer](./media/newcustomer_introfleetmgmt1.png)](./media/newcustomer_introfleetmgmt1.png)</span></span>

4.  <span data-ttu-id="382e9-134">アクション ウィンドウで、Microsoft Office ロゴをクリックし、**Excel にエクスポート**の下の**顧客**をクリックして、グリッド ビューの情報を Microsoft Excel スプレッドシートに送信します。</span><span class="sxs-lookup"><span data-stu-id="382e9-134">On the Action Pane, click the Microsoft Office logo, then click on **Customers** under **Export to Excel **to send the information in the grid view to a Microsoft Excel spreadsheet.</span></span> <span data-ttu-id="382e9-135">この操作には少し時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-135">This operation can take some time.</span></span>

    <span data-ttu-id="382e9-136">[![Excel にエクスポート](./media/exporttoexcel.jpg)](./media/exporttoexcel.jpg)</span><span class="sxs-lookup"><span data-stu-id="382e9-136">[![Export to excel](./media/exporttoexcel.jpg)](./media/exporttoexcel.jpg)</span></span>

5.  <span data-ttu-id="382e9-137">要求するメッセージが表示されたら、**開く** をクリックして Excel でデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="382e9-137">When prompted, click **Open** to view the data in Excel.</span></span>
6.  <span data-ttu-id="382e9-138">Excel を閉じます。</span><span class="sxs-lookup"><span data-stu-id="382e9-138">Close Excel.</span></span>
7.  <span data-ttu-id="382e9-139">**詳細** ビューに切り替えるには、**名** 列の値をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-139">To switch to the **Details** view, click on a value in the **First Name** column.</span></span> 

    <span data-ttu-id="382e9-140">[![名](./media/customer.jpg)](./media/customer.jpg)このビューには、単一の顧客の詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-140">[![First name](./media/customer.jpg)](./media/customer.jpg) This view shows detailed information for a single customer.</span></span>

8.  <span data-ttu-id="382e9-141">**リストを表示**をクリックすると、ナビゲーション リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-141">Click **Show list** to show the navigation list.</span></span> 

    <span data-ttu-id="382e9-142">[![ナビゲーション リスト](./media/listnav_introfleetmgmt1.png)](./media/listnav_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-142">[![Navigation list](./media/listnav_introfleetmgmt1.png)](./media/listnav_introfleetmgmt1.png)</span></span>

9.  <span data-ttu-id="382e9-143">作業ウィンドウのナビゲーション リストでさまざまな顧客名をクリックし、各顧客の変更に関する詳細情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="382e9-143">Click the various customer names in the navigation list in the side pane, and watch as the detailed information about each customer changes.</span></span>
10. <span data-ttu-id="382e9-144">顧客 **Phil Spencer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="382e9-144">Select the customer **Phil Spencer**.</span></span> <span data-ttu-id="382e9-145">Phil の過去のレンタルの好みを示すために、グラフが更新されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="382e9-145">You'll notice the charts update to indicate Phil's previous rental preferences.</span></span>
11. <span data-ttu-id="382e9-146">詳細を表示する円のスライスをポイントします。</span><span class="sxs-lookup"><span data-stu-id="382e9-146">Hover over the pie slices to see the details.</span></span> <span data-ttu-id="382e9-147">Phil が、過去に、赤い SUV をよくレンタルしていたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="382e9-147">You'll notice that, in the past, Phil has often rented red SUVs.</span></span> <span data-ttu-id="382e9-148">これにより、次回の Phil の予約時に、販売員が利用可能な赤い SUV を探す手がかりを与えるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="382e9-148">This might give the sales clerk a cue to look for available red SUVs the next time Phil makes a reservation.</span></span> <span data-ttu-id="382e9-149">これは、積極的にインサイトを提供する簡単な例です。</span><span class="sxs-lookup"><span data-stu-id="382e9-149">This is a simple example of proactively providing insights.</span></span>
12. <span data-ttu-id="382e9-150">顧客として自分自身を追加します。</span><span class="sxs-lookup"><span data-stu-id="382e9-150">Add yourself as a customer.</span></span>
    -   <span data-ttu-id="382e9-151">アクション ウィンドウで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-151">On the Action Pane, click **New**.</span></span> 

        <span data-ttu-id="382e9-152">[![ユーザー自身を追加](./media/addyourself_introfleetmgmt1.png)](./media/addyourself_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-152">[![Add yourself](./media/addyourself_introfleetmgmt1.png)](./media/addyourself_introfleetmgmt1.png)</span></span>

    -   <span data-ttu-id="382e9-153">顧客として自身を追加するため、フォームに入力します。</span><span class="sxs-lookup"><span data-stu-id="382e9-153">Fill in the form to add yourself as a customer.</span></span> <span data-ttu-id="382e9-154">最低限、名前、クレジット カード フィールドの 16 桁の数字、住所情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="382e9-154">Make sure that you provide your name, a 16-digit number in the credit card field, and address information, at a minimum.</span></span> <span data-ttu-id="382e9-155">**注記**: 新しいレコードを保存するためのアクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="382e9-155">**Note**: You don't have to take any action to save a new record.</span></span>

13. <span data-ttu-id="382e9-156">新しいレンタルを作成します。</span><span class="sxs-lookup"><span data-stu-id="382e9-156">Create a new rental.</span></span>
    1.  <span data-ttu-id="382e9-157">ナビゲーション バーで、**フリート管理** &gt; **レンタル** &gt;**レンタル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-157">On the navigation bar, go to **Fleet management** &gt; **Rentals** &gt; **Rental**.</span></span>
    2.  <span data-ttu-id="382e9-158">**レンタル** フォームで、アクション ウィンドウの**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-158">In the **Rental** form, on the Action Pane, click **New.**</span></span>
    3.  <span data-ttu-id="382e9-159">**車両**フィールドで車両を選択します。</span><span class="sxs-lookup"><span data-stu-id="382e9-159">In the **Vehicle** field, select a vehicle.</span></span>
    4.  <span data-ttu-id="382e9-160">**顧客**フィールドで、自分の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="382e9-160">In the **Customer** field, select your name.</span></span>
    5.  <span data-ttu-id="382e9-161">**終了**フィールドで、終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="382e9-161">In the **To** field, pick an end date.</span></span>
    6.  <span data-ttu-id="382e9-162">**開始**フィールドに、「35,000」と入力します。</span><span class="sxs-lookup"><span data-stu-id="382e9-162">In the **Start** field, enter “35,000”.</span></span>
    7.  <span data-ttu-id="382e9-163">**ピックアップ** フィールドに、フルと入力します。</span><span class="sxs-lookup"><span data-stu-id="382e9-163">In the **Pickup** field, enter Full.</span></span>
    8.  <span data-ttu-id="382e9-164">作業が終了したら、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-164">When you are done, click **Save**.</span></span>

14. <span data-ttu-id="382e9-165">レンタル期間を開始します。</span><span class="sxs-lookup"><span data-stu-id="382e9-165">Start the rental period.</span></span>
    1.  <span data-ttu-id="382e9-166">アクション ウィンドウで、**レンタル開始**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-166">On the Action Pane, click **Start rental**.</span></span>
    2.  <span data-ttu-id="382e9-167">ダイアログ ボックスで、フィールドの値を確認して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-167">In the dialog box, verify the values in the fields and click **OK**.</span></span>

## <a name="use-fleet-management-to-run-a-workflow"></a><span data-ttu-id="382e9-168">フリート マネージメントを使用してワークフローを実行</span><span class="sxs-lookup"><span data-stu-id="382e9-168">Use Fleet Management to run a workflow</span></span>
1.  <span data-ttu-id="382e9-169">Dynamics アイコンをクリックして、ダッシュボードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="382e9-169">Click the Dynamics icon to return to the dashboard.</span></span>
2.  <span data-ttu-id="382e9-170">**予約管理**タイルを検索し、予約管理ワークスペースを開くためそれをクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-170">Find the **Reservation Management** tile and click on it to open the Reservation Management workspace.</span></span>
3.  <span data-ttu-id="382e9-171">**現在のレンタル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-171">Click **Current rentals**.</span></span>
4.  <span data-ttu-id="382e9-172">**レンタル**フォームで、レンタルの ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-172">On the **Rentals** form, click the ID of your rental.</span></span>
5.  <span data-ttu-id="382e9-173">**レンタル**フォームの詳細ビューにあるアクション ウィンドウで、**レンタルの完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-173">On the Details view of the **Rentals** form, on the Action Pane, click **Complete rental**.</span></span>
6.  <span data-ttu-id="382e9-174">**新しいマイレージ** フィールドに、40,000 と入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-174">In the **New mileage** field, enter 40,000, and then click **OK**.</span></span>
7.  <span data-ttu-id="382e9-175">Dynamics アイコンをクリックして、ダッシュボードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="382e9-175">Click the Dynamics icon to return to the dashboard.</span></span>
8.  <span data-ttu-id="382e9-176">ナビゲーション バーで、**フリート管理** &gt;**車両** &gt; **車両メンテナンス**に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-176">On the navigation bar, navigate to **Fleet management** &gt; **Vehicles** &gt; **Vehicle Maintenance**.</span></span> 

    <span data-ttu-id="382e9-177">[![車両メンテナンス](./media/vehiclemaintenance_introfleetmgmt.png)](./media/vehiclemaintenance_introfleetmgmt.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-177">[![Vehicle Maintenance](./media/vehiclemaintenance_introfleetmgmt.png)](./media/vehiclemaintenance_introfleetmgmt.png)</span></span> 

    <span data-ttu-id="382e9-178">**車両メンテナンス** フォームでは、**ステータス** フィールドでレンタルがサービス部門によって検査待ちであることが示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-178">In the **Vehicle Maintenance** form, the **Status** field shows that your rental is awaiting examination by the service department.</span></span> <span data-ttu-id="382e9-179">**注記**: バッチ フレームワークが車両の状態を変更するまで、最大で 2 分待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-179">**Note**: You might need to wait up to two minutes for the batch framework to change the status of the vehicle.</span></span> <span data-ttu-id="382e9-180">アクション ウィンドウで、**更新**をクリックしステータスの変更が表示されるまで、ビューを定期的に更新します。</span><span class="sxs-lookup"><span data-stu-id="382e9-180">On the Action Pane, click **Refresh** periodically to update the view, until you see the status change.</span></span> <span data-ttu-id="382e9-181">別の人がワークフローの各ステップを通常処理することに留意してください。バッチ フレームワークによって生じる多少の遅延は、実際のアプリケーションでは問題ありません。</span><span class="sxs-lookup"><span data-stu-id="382e9-181">Keep in mind that a different person usually handles each step in a workflow; the brief delay introduced by the batch framework is not an issue in a real-world application.</span></span>
9.  <span data-ttu-id="382e9-182">レンタルを含む行を選択します。</span><span class="sxs-lookup"><span data-stu-id="382e9-182">Select the row that contains your rental.</span></span> <span data-ttu-id="382e9-183">アクション ウィンドウで、**ワークフロー**をクリックし、**検査完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-183">On the Action Pane, click **Workflow**, and then click **Examination complete**.</span></span> <span data-ttu-id="382e9-184">**注記**: ワークフローでフルセットのオプションを取得するには、ページを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-184">**Note**: You may need to refresh the page to get the full set of options under Workflow.</span></span>
10. <span data-ttu-id="382e9-185">コメントを入力し、**検査完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-185">Enter a comment, and then click **Examination complete**.</span></span>
11. <span data-ttu-id="382e9-186">バッチ フレームワークが変更を処理するまで、最大で 2 分再度待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-186">You might again need to wait up to two minutes for the batch framework to process the change.</span></span> <span data-ttu-id="382e9-187">アクション ウィンドウで、**ステータス**フィールドの変更が表示されるまで、**更新**を定期的にクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-187">On the Action Pane, click **Refresh** periodically, until you see the **Status** field change.</span></span> <span data-ttu-id="382e9-188">車両が**サービス待ち**の状態であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="382e9-188">Notice that the vehicle now has a status of **Awaiting Service**.</span></span>
12. <span data-ttu-id="382e9-189">必要に応じて、このワークフロー手順を引き続き繰り返して、車両にサービスおよびクリーニング フェーズを実行できます。</span><span class="sxs-lookup"><span data-stu-id="382e9-189">Optionally, you can continue to repeat these workflow steps to take the vehicle through the service and cleaning phases.</span></span> <span data-ttu-id="382e9-190">クリーニングが完了した後、最終状態は、**実行**になります。</span><span class="sxs-lookup"><span data-stu-id="382e9-190">After cleaning is completed, the final status is **Done**.</span></span>
13. <span data-ttu-id="382e9-191">**ワークフロー**、**履歴の表示**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-191">Click **Workflow**, and then click **View history**.</span></span> <span data-ttu-id="382e9-192">**ワークフロー履歴** フォームは、車両ワークフローに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="382e9-192">The **Workflow history** form provides information about the vehicle workflow.</span></span>
14. <span data-ttu-id="382e9-193">**追跡の詳細**をクリックして活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="382e9-193">Click **Tracking details** to see the activities.</span></span> <span data-ttu-id="382e9-194">[![追跡の詳細](./media/workflow.jpg)](./media/workflow.jpg)</span><span class="sxs-lookup"><span data-stu-id="382e9-194">[![Tracking details](./media/workflow.jpg)](./media/workflow.jpg)</span></span>

### <a name="to-view-the-setup-behind-the-workflow"></a><span data-ttu-id="382e9-195">ワークフローの背後に設定を表示するには</span><span class="sxs-lookup"><span data-stu-id="382e9-195">To view the setup behind the workflow</span></span>

1.  <span data-ttu-id="382e9-196">ダッシュ ボードで、**フリート管理** &gt; **設定** &gt; **ワークフローの設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-196">On the dashboard, navigate to **Fleet Management** &gt; **Setup** &gt; **Workflow setup**.</span></span> <span data-ttu-id="382e9-197">**ワークフロー セットアップ** ページには、ワークフローの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-197">The **Workflow Setup** page shows the list of workflows.</span></span> 

    <span data-ttu-id="382e9-198">[![ワークフローの設定](./media/workflowsetup.jpg)](./media/workflowsetup.jpg)</span><span class="sxs-lookup"><span data-stu-id="382e9-198">[![Workflow setup](./media/workflowsetup.jpg)](./media/workflowsetup.jpg)</span></span>

2.  <span data-ttu-id="382e9-199">**ワークフロー ID** 列に、車両メンテナンス ワークフローの ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-199">In the **Workflow ID** column, click the ID of your vehicle maintenance workflow.</span></span>
3.  <span data-ttu-id="382e9-200">コードを実行するアクセス許可を求めるプロンプトを承認します。</span><span class="sxs-lookup"><span data-stu-id="382e9-200">Accept any prompts that ask you for permission to run code.</span></span> <span data-ttu-id="382e9-201">短い待機の後、ワークフロー エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="382e9-201">After a short wait, the workflow editor opens.</span></span> <span data-ttu-id="382e9-202">**注記:** このステップは、クラウドではなく 1 ボックス環境で動作します。</span><span class="sxs-lookup"><span data-stu-id="382e9-202">**Note:** This step works on the one-box environment, but not in the cloud.</span></span> <span data-ttu-id="382e9-203">ワークフロー エディターでは、ワークフロー図を表示できます。</span><span class="sxs-lookup"><span data-stu-id="382e9-203">You can view the workflow diagram in the workflow editor.</span></span> <span data-ttu-id="382e9-204">次の図はワークフローを示します。</span><span class="sxs-lookup"><span data-stu-id="382e9-204">The following illustration shows the workflow.</span></span>

    <span data-ttu-id="382e9-205">[![ワークフロー ダイアグラム](./media/workflow_introfleetmgmt.png)](./media/workflow_introfleetmgmt.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-205">[![Workflow diagram](./media/workflow_introfleetmgmt.png)](./media/workflow_introfleetmgmt.png)</span></span>

4.  <span data-ttu-id="382e9-206">完了したら、**ワークフロー** ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="382e9-206">When you are done, close the **Workflow** window.</span></span>

## <a name="create-a-new-kpi-definition"></a><span data-ttu-id="382e9-207">新しい KPI 定義を作成する</span><span class="sxs-lookup"><span data-stu-id="382e9-207">Create a new KPI definition</span></span>
<span data-ttu-id="382e9-208">Web クライアントを使用すると、適切な権限を持つユーザーが、開発者がモデル化して展開した KPI 定義を変更できます。</span><span class="sxs-lookup"><span data-stu-id="382e9-208">The web client enables users who have appropriate permissions to modify KPI definitions that have been modeled and deployed by developers.</span></span> <span data-ttu-id="382e9-209">ユーザーは、クライアントに新しい KPI 定義を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="382e9-209">Users also have the ability to create new KPI definitions in the client.</span></span> <span data-ttu-id="382e9-210">このチュートリアルでは、クライアントで新しい KPI の定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="382e9-210">In this walkthrough, you create a new KPI definition in the client.</span></span>

1.  <span data-ttu-id="382e9-211">**予約管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="382e9-211">Open the **Reservation Management** workspace.</span></span> <span data-ttu-id="382e9-212">ナビゲーション バーで、**フリート管理**&gt;** ワークスペース&gt;予約管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="382e9-212">On the navigation bar, go to** Fleet Management **&gt;** Workspaces &gt; Reservation Management**.</span></span>
2.  <span data-ttu-id="382e9-213">ワークスペースの左下に表示されている総収益 KPI タイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="382e9-213">Notice the Total revenue KPI tile shown on the bottom left of the workspace.</span></span> <span data-ttu-id="382e9-214">**総収益 KPI** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-214">Click the **Total Revenue KPI** tile.</span></span> <span data-ttu-id="382e9-215">総収益 KPI タイルの詳細と共に収益の上位および下位貢献者を示すチャートが画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-215">Details of the total revenue KPI tile along with charts indicating top and bottom contributors to revenue will be shown on screen.</span></span>
3.  <span data-ttu-id="382e9-216">次に、レンタルの数を監視する新しい KPI を定義します。</span><span class="sxs-lookup"><span data-stu-id="382e9-216">Next, you will define a new KPI to monitor the number of rentals.</span></span>
4.  <span data-ttu-id="382e9-217">アクション ウィンドウで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-217">On the Action Pane, click **New**.</span></span> <span data-ttu-id="382e9-218">**新しい KPI** ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="382e9-218">The **New KPI** dialog will open.</span></span>
5.  <span data-ttu-id="382e9-219">新しい KPI 定義に次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="382e9-219">Enter following values for the new KPI definition.</span></span>

    | <span data-ttu-id="382e9-220">**フィールド**</span><span class="sxs-lookup"><span data-stu-id="382e9-220">**Field**</span></span>         | <span data-ttu-id="382e9-221">**値**</span><span class="sxs-lookup"><span data-stu-id="382e9-221">**Value**</span></span>               |
    |-------------------|-------------------------|
    | <span data-ttu-id="382e9-222">**名前**</span><span class="sxs-lookup"><span data-stu-id="382e9-222">**Name**</span></span>          | <span data-ttu-id="382e9-223">レンタルの数</span><span class="sxs-lookup"><span data-stu-id="382e9-223">Number of Rentals</span></span>       |
    | <span data-ttu-id="382e9-224">**測定**</span><span class="sxs-lookup"><span data-stu-id="382e9-224">**Measurement**</span></span>   | <span data-ttu-id="382e9-225">FMAggregateMeasurements</span><span class="sxs-lookup"><span data-stu-id="382e9-225">FMAggregateMeasurements</span></span> |
    | <span data-ttu-id="382e9-226">**メジャー グループ**</span><span class="sxs-lookup"><span data-stu-id="382e9-226">**Measure Group**</span></span> | <span data-ttu-id="382e9-227">FmRentalCharges</span><span class="sxs-lookup"><span data-stu-id="382e9-227">FmRentalCharges</span></span>         |
    | <span data-ttu-id="382e9-228">**基準**</span><span class="sxs-lookup"><span data-stu-id="382e9-228">**Measure**</span></span>       | <span data-ttu-id="382e9-229">NoRentals</span><span class="sxs-lookup"><span data-stu-id="382e9-229">NoRentals</span></span>               |
    | <span data-ttu-id="382e9-230">**目標は**</span><span class="sxs-lookup"><span data-stu-id="382e9-230">**Goal is**</span></span>       | <span data-ttu-id="382e9-231">固定値</span><span class="sxs-lookup"><span data-stu-id="382e9-231">Fixed Value</span></span>             |
    | <span data-ttu-id="382e9-232">**目標値**</span><span class="sxs-lookup"><span data-stu-id="382e9-232">**Goal Value**</span></span>    | <span data-ttu-id="382e9-233">30</span><span class="sxs-lookup"><span data-stu-id="382e9-233">30</span></span>                      |


6.  <span data-ttu-id="382e9-234">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-234">Click **Save**.</span></span> 

    <span data-ttu-id="382e9-235">[![新規 KPI](./media/newkpi_introfleetmgmt1.png)](./media/newkpi_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-235">[![New KPI](./media/newkpi_introfleetmgmt1.png)](./media/newkpi_introfleetmgmt1.png)</span></span> 

    <span data-ttu-id="382e9-236">**注記:** **新しい KPI** ダイアログ ボックスで、**保存**ボタンが表示されない場合、より高い画面解像度を使用するとダイアログ全体を表示できます。</span><span class="sxs-lookup"><span data-stu-id="382e9-236">**Note:** If the **Save** button isn’t visible in the **New KPI** dialog box, use a higher screen resolution so that you can see the entire dialog.</span></span> <span data-ttu-id="382e9-237">作成した KPI に関する詳細を含む、KPI 詳細ページを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="382e9-237">You can see the KPI details page that contains details about the KPI that you created.</span></span> <span data-ttu-id="382e9-238">**詳細** セクションで変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="382e9-238">You can make changes in the **Details** section.</span></span> <span data-ttu-id="382e9-239">値が目標の 90% 未満の場合は KPI が赤く表示され、値が目標の 110% を超える場合は KPI が緑で表示されるように、既定のしきい値を変更します。</span><span class="sxs-lookup"><span data-stu-id="382e9-239">You will modify the default threshold values so that if the value is less than 90% of the goal, the KPI will show red and if the value is over 110% of the goal, the KPI will show green.</span></span>
7.  <span data-ttu-id="382e9-240">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-240">Click **Edit**.</span></span>
8.  <span data-ttu-id="382e9-241">画面の右にスクロールし、次のようにしきい値フィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="382e9-241">Scroll to the right of the screen, and modify the values in the thresholds fields as follows.</span></span>

    | <span data-ttu-id="382e9-242">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="382e9-242">**Property**</span></span>           | <span data-ttu-id="382e9-243">**値**</span><span class="sxs-lookup"><span data-stu-id="382e9-243">**Value**</span></span> |
    |------------------------|-----------|
    | <span data-ttu-id="382e9-244">**次の値未満の場合に赤**</span><span class="sxs-lookup"><span data-stu-id="382e9-244">**Red if less than**</span></span>   | <span data-ttu-id="382e9-245">90</span><span class="sxs-lookup"><span data-stu-id="382e9-245">90</span></span>        |
    | <span data-ttu-id="382e9-246">**次の値を超えた場合に緑:**</span><span class="sxs-lookup"><span data-stu-id="382e9-246">**Green if more than**</span></span> | <span data-ttu-id="382e9-247">110</span><span class="sxs-lookup"><span data-stu-id="382e9-247">110</span></span>       |


9.  <span data-ttu-id="382e9-248">アプリケーション バーで、**保存をクリックします</span><span class="sxs-lookup"><span data-stu-id="382e9-248">In the application bar, click **Save</span></span> 

    <span data-ttu-id="382e9-249">[![KPI グラフ](./media/kpigraph_introfleetmgmt.png)](./media/kpigraph_introfleetmgmt.png)**</span><span class="sxs-lookup"><span data-stu-id="382e9-249">[![KPI Graph](./media/kpigraph_introfleetmgmt.png)](./media/kpigraph_introfleetmgmt.png)**</span></span>

10. <span data-ttu-id="382e9-250">グリッド ビューに戻るには、フォーム キャプションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-250">Click the form caption to return to the grid view.</span></span>
11. <span data-ttu-id="382e9-251">**名**列ヘッダーをクリックし、フィルター演算子を**部分一致**に変更し、フィルター フィールド値を**番号**に更新します。</span><span class="sxs-lookup"><span data-stu-id="382e9-251">Click the **Name** column header, change the filter operator to **contains**, and update the filter field value to **Number**.</span></span> <span data-ttu-id="382e9-252">新しい KPI をリストで使用できることが分かります。</span><span class="sxs-lookup"><span data-stu-id="382e9-252">You will see the new KPI is available in the list.</span></span>

    <span data-ttu-id="382e9-253">[![KPI List](./media/kpilist_introfleetmgmt1.png)](./media/kpilist_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-253">[![KPI List](./media/kpilist_introfleetmgmt1.png)](./media/kpilist_introfleetmgmt1.png)</span></span>

## <a name="launch-an-operational-report"></a><span data-ttu-id="382e9-254">運用レポートの起動</span><span class="sxs-lookup"><span data-stu-id="382e9-254">Launch an operational report</span></span>
<span data-ttu-id="382e9-255">このチュートリアルでは、現在車両をレンタルしている顧客の一覧を含む運用レポートを開始します。</span><span class="sxs-lookup"><span data-stu-id="382e9-255">In this tutorial, you’ll launch an operational report that contains a list of customers who are currently renting vehicles.</span></span>

1.  <span data-ttu-id="382e9-256">ダッシュボードを使用して、**予約管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="382e9-256">Use the dashboard to open the **Reservation management** workspace.</span></span>
2.  <span data-ttu-id="382e9-257">**顧客レポート** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-257">Click the **Customers report** tile.</span></span> <span data-ttu-id="382e9-258">**顧客グループ**のパラメーターでは、何も入力しないでください。</span><span class="sxs-lookup"><span data-stu-id="382e9-258">Do not enter anything in the parameter for **Customer group**.</span></span> 

    <span data-ttu-id="382e9-259">[![顧客リスト](./media/customerlist_introfleetmgmt1.png)](./media/customerlist_introfleetmgmt1.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-259">[![Customer List](./media/customerlist_introfleetmgmt1.png)](./media/customerlist_introfleetmgmt1.png)</span></span>

3.  <span data-ttu-id="382e9-260">**OK** をクリックしてダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="382e9-260">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="382e9-261">レポートが表示され、顧客リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="382e9-261">The report will be rendered and show the list of customers.</span></span> <span data-ttu-id="382e9-262">レポートを表示するのに、数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="382e9-262">The report may take a minute to render.</span></span>

## <a name="secure-access-using-the-role-based-security-system"></a><span data-ttu-id="382e9-263">ロールベースのセキュリティ システムを使用してアクセスを保護</span><span class="sxs-lookup"><span data-stu-id="382e9-263">Secure access using the role-based security system</span></span>
<span data-ttu-id="382e9-264">このチュートリアルでは、さまざまなセキュリティ ロールが割り当てられているユーザーとしてシステムにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="382e9-264">In this tutorial, you’ll access the system as a user that has been assigned a different security role.</span></span> <span data-ttu-id="382e9-265">このチュートリアルでは、少なくとも 1 人の追加エンド ユーザーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="382e9-265">This tutorial requires that you have created at least one additional end user.</span></span>

1.  <span data-ttu-id="382e9-266">ダッシュ ボードの、**システム管理**セクションで、**ユーザー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-266">On the dashboard, in the **System administration** section, click **Users**.</span></span>
2.  <span data-ttu-id="382e9-267">アクション ウィンドウで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-267">On the Action Pane, click **New**.</span></span>
3.  <span data-ttu-id="382e9-268">以下のフィールド情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="382e9-268">Enter the following field information.</span></span>

    | <span data-ttu-id="382e9-269">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="382e9-269">**Property**</span></span>        | <span data-ttu-id="382e9-270">**値**</span><span class="sxs-lookup"><span data-stu-id="382e9-270">**Value**</span></span>                                                                                 |
    |---------------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="382e9-271">**ユーザー ID**</span><span class="sxs-lookup"><span data-stu-id="382e9-271">**User ID**</span></span>         | <span data-ttu-id="382e9-272">8 文字の固有 ID</span><span class="sxs-lookup"><span data-stu-id="382e9-272">Eight character unique ID</span></span>                                                                 |
    | <span data-ttu-id="382e9-273">**ユーザー名**</span><span class="sxs-lookup"><span data-stu-id="382e9-273">**User name**</span></span>       | <span data-ttu-id="382e9-274">ユーザーの最初の名前</span><span class="sxs-lookup"><span data-stu-id="382e9-274">The first name of the user</span></span>                                                                |
    | <span data-ttu-id="382e9-275">**ネットワーク ドメイン**</span><span class="sxs-lookup"><span data-stu-id="382e9-275">**Network domain**</span></span>  | <span data-ttu-id="382e9-276">urn:Federation:MicrosoftOnline</span><span class="sxs-lookup"><span data-stu-id="382e9-276">urn:Federation:MicrosoftOnline</span></span>                                                            |
    | <span data-ttu-id="382e9-277">**エイリアス**</span><span class="sxs-lookup"><span data-stu-id="382e9-277">**Alias**</span></span>           | <span data-ttu-id="382e9-278"><tim@lucernepublishers.ccsctp.net> (組織アカウントの電子メール アドレスに置き換えてください。)</span><span class="sxs-lookup"><span data-stu-id="382e9-278"><tim@lucernepublishers.ccsctp.net> (Replace with the organization account email address.)</span></span> |
    | <span data-ttu-id="382e9-279">**既定の会社**</span><span class="sxs-lookup"><span data-stu-id="382e9-279">**Default Company**</span></span> | <span data-ttu-id="382e9-280">DAT</span><span class="sxs-lookup"><span data-stu-id="382e9-280">DAT</span></span>                                                                                       |
    | <span data-ttu-id="382e9-281">**有効**</span><span class="sxs-lookup"><span data-stu-id="382e9-281">**Enabled**</span></span>         | <span data-ttu-id="382e9-282">このスライダーが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="382e9-282">Verify that this slider is set to **Yes**.</span></span>                                                |

4.  <span data-ttu-id="382e9-283">**ロールの割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-283">Click **Assign Roles**.</span></span> 

    <span data-ttu-id="382e9-284">[![ロールの割り当て](./media/assignroles_introfleetmgmt.png)](./media/assignroles_introfleetmgmt.png)</span><span class="sxs-lookup"><span data-stu-id="382e9-284">[![Assign Roles](./media/assignroles_introfleetmgmt.png)](./media/assignroles_introfleetmgmt.png)</span></span>

5.  <span data-ttu-id="382e9-285">**フリート管理ブランチ マネージャー** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-285">Select **Fleet management branch manager**, and then click **OK**.</span></span>
6.  <span data-ttu-id="382e9-286">右上のユーザー名をクリックしてから、**サインアウト**をクリックします。サインイン ページにリダイレクトされます</span><span class="sxs-lookup"><span data-stu-id="382e9-286">Click the user name on the top right, and then click **Sign Out**. You’ll be redirected back to the sign-n page</span></span>
7.  <span data-ttu-id="382e9-287">上記の手順でセキュリティ ロールを割り当てたユーザーの資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="382e9-287">Sign in using the credentials for the user who you assigned the security role to in the steps above.</span></span>
8.  <span data-ttu-id="382e9-288">ダッシュボードで、このユーザーはセキュリティ ロールに関連する項目のみ確認できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="382e9-288">Notice that in the dashboard, this user can see only items that are related to his security role.</span></span> <span data-ttu-id="382e9-289">システム管理者が確認できる項目は非表示になります。</span><span class="sxs-lookup"><span data-stu-id="382e9-289">Items that system administrators can see are now hidden.</span></span>
9.  <span data-ttu-id="382e9-290">セッションをサインアウトするには、**サインアウト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="382e9-290">Click **Sign out** to sign out of the session.</span></span>





