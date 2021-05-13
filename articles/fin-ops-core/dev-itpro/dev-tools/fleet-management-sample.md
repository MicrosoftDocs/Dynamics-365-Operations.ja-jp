---
title: フリート管理のサンプル アプリケーションのエンド ツー エンドのシナリオ
description: このチュートリアルでは、フリート管理のサンプル アプリケーションがサポートするように設計されたエンド ツー エンドのシナリオを説明します。
author: RobinARH
ms.date: 07/08/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10254
ms.assetid: e289504e-a1d9-44b7-8f84-f99f330321d6
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84b1dfb305d9999d61d1c6aeb50ce56905cc38c
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866336"
---
# <a name="end-to-end-scenario-for-the-fleet-management-sample-application"></a><span data-ttu-id="6a9e9-103">フリート管理のサンプル アプリケーションのエンド ツー エンドのシナリオ</span><span class="sxs-lookup"><span data-stu-id="6a9e9-103">End-to-end scenario for the Fleet Management sample application</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a9e9-104">このチュートリアルでは、フリート管理のサンプル アプリケーションがサポートするように設計されたエンド ツー エンドのシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-104">This tutorial walks you through an end-to-end scenario that the Fleet Management sample application is designed to support.</span></span>

<span data-ttu-id="6a9e9-105">このチュートリアルでは、フリート管理サンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-105">In this tutorial, you’ll take a tour of the Fleet Management sample.</span></span> <span data-ttu-id="6a9e9-106">このチュートリアルの概要では、背景知識とコンテキスト情報を提供しています。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-106">The overviews in this tutorial provide some background knowledge and contextual info.</span></span> <span data-ttu-id="6a9e9-107">このサンプル アプリケーションのサポートの目的のエンド ツー エンドのシナリオを検討します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-107">You’ll walk through an end-to-end scenario that this sample application is designed to support.</span></span> <span data-ttu-id="6a9e9-108">これは、他のチュートリアルに進む前に知っておくべき情報です。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-108">This is information that you should have before proceeding to other tutorials.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="6a9e9-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="6a9e9-109">Prerequisite</span></span>

-   <span data-ttu-id="6a9e9-110">このチュートリアルを開始する前に、エンド ユーザーとして最初にプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-110">You must first be provisioned as an end user before you start this tutorial.</span></span>
-   <span data-ttu-id="6a9e9-111">このチュートリアルでは主に、FleetManagement に移行したプロジェクトとそれによって構築されるアプリケーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-111">This tutorial mainly explores the FleetManagement Migrated project and the application that it builds.</span></span>

## <a name="installing-the-demo-data"></a><span data-ttu-id="6a9e9-112">デモ データのインストール</span><span class="sxs-lookup"><span data-stu-id="6a9e9-112">Installing the demo data</span></span>
<span data-ttu-id="6a9e9-113">サンプルを操作するには、提供されているデモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-113">To work with the sample, you must install the provided demo data.</span></span>

1.  <span data-ttu-id="6a9e9-114">仮想マシン (VM) で、Internet Explorer を開き、アプリケーションのベース URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-114">In the virtual machine (VM), open Internet Explorer and navigate to the application's base URL.</span></span>
2.  <span data-ttu-id="6a9e9-115">サインインします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-115">Sign in.</span></span>
3.  <span data-ttu-id="6a9e9-116">ダッシュ ボードで、ナビゲーション ウィンドウを開き、**フリート管理 \> 設定 \> フリート設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-116">On the dashboard, open the navigation pane and go to **Fleet Management \> Setup\> Fleet setup**.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-117">![フリート設定](media/fmt_setup_data.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-117">![Fleet setup](media/fmt_setup_data.png)</span></span>
    
4.  <span data-ttu-id="6a9e9-118">**データ設定** タブで、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-118">On the **Data setup** tab, select **Create**.</span></span> 
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-119">![デモ データの読み込み](media/fmt_data_setup_create.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-119">![Load Demo Data](media/fmt_data_setup_create.png)</span></span>

5.  <span data-ttu-id="6a9e9-120">デモ データの再読み込みを促すメッセージが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-120">If you're prompted to reload the demo data, click **Yes**.</span></span>
6.  <span data-ttu-id="6a9e9-121">データの読み込みが完了したら、 **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-121">When the data is finished loading, select **Close**.</span></span>

## <a name="use-the-fleet-management-application-to-rent-a-vehicle"></a><span data-ttu-id="6a9e9-122">車両をレンタルするには、フリート管理アプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-122">Use the Fleet Management application to rent a vehicle</span></span>
<span data-ttu-id="6a9e9-123">このセクションで移行したアプリで作業をしていることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-123">Remember that you’re working with the migrated app in this section.</span></span> <span data-ttu-id="6a9e9-124">表示されるフォームは、Microsoft Dynamics AX 2012 バージョンのサンプルから直接ポートされます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-124">The forms that you see are directly ported from the Microsoft Dynamics AX 2012 version of the sample.</span></span> <span data-ttu-id="6a9e9-125">変更および再編成されていますが、再考されてはいません。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-125">Although they have been modified and restyled, they have not been reimagined.</span></span>

1.  <span data-ttu-id="6a9e9-126">Internet Explorer を開き、Finance and Operations アプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-126">Open Internet Explorer, and sign into the Finance and Operations application.</span></span>
2.  <span data-ttu-id="6a9e9-127">**ダッシュボード** に戻るには、ページの左上隅にある製品名を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-127">To return to the **Dashboard**, select the product name in the top-left corner of the page.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-128">![ダッシュボードに戻る](media/fmt_logo.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-128">![Return to dashboard](media/fmt_logo.png)</span></span>
    
    <span data-ttu-id="6a9e9-129">ダッシュボードは主要な作業ハブです。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-129">The dashboard is the main working hub.</span></span> <span data-ttu-id="6a9e9-130">セクションに分類され、アプリケーションの一部になる、様々なタイルを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-130">You can see the various tiles, organized into sections, which lead to parts of the application.</span></span> <span data-ttu-id="6a9e9-131">ダッシュボードは、水平スクロール用に設計されています。これは、最新のデバイスでうまく動作するための最適化です。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-131">The dashboard is designed for horizontal scrolling, which is an optimization for working well on modern devices.</span></span> <span data-ttu-id="6a9e9-132">ダッシュボードの右側にあるボタンにはナビゲーションバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-132">The button to the right of the dashboard shows the navigation bar.</span></span>
3.  <span data-ttu-id="6a9e9-133">ダッシュ ボードから、ナビゲーション バーを開いて **フリート管理 \> 顧客 \> 顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-133">From the Dashboard, open the navigation bar and go to **Fleet Management \> Customers \> Customer**.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-134">![顧客リストに移動](media/fmt_customers_customer.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-134">![Navigate to customer list](media/fmt_customers_customer.png)</span></span>
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-135">![新しい顧客](media/fmt_new_customer.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-135">![New customer](media/fmt_new_customer.png)</span></span>

4.  <span data-ttu-id="6a9e9-136">**詳細** ビューに切り替えるには、 **名** 列の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-136">To switch to the **Details** view, select a value in the **First Name** column.</span></span> <span data-ttu-id="6a9e9-137">このビューには、単一の顧客の詳細情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-137">This view shows detailed information for a single customer.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-138">![詳細ビューの名](media/fmt_details_view.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-138">![First name to details view](media/fmt_details_view.png)</span></span>

5.  <span data-ttu-id="6a9e9-139">**リストを表示** をクリックすると、ナビゲーション リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-139">Click **Show list** to show the navigation list.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-140">![ナビゲーション リスト](media/fmt_show_list.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-140">![Navigation list](media/fmt_show_list.png)</span></span>

6.  <span data-ttu-id="6a9e9-141">作業ウィンドウのナビゲーション リストでさまざまな顧客名をクリックし、各顧客の変更に関する詳細情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-141">Click the various customer names in the navigation list in the side pane, and watch as the detailed information about each customer changes.</span></span>
7. <span data-ttu-id="6a9e9-142">顧客 **Eduardo Cobo** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-142">Select the customer **Eduardo Cobo**.</span></span> <span data-ttu-id="6a9e9-143">Eduardo の過去のレンタルの好みを示すために、グラフが更新されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-143">You'll notice the charts update to indicate Eduardo's previous rental preferences.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-144">![詳細ビュー](media/fmt_another_customer.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-144">![Details view](media/fmt_another_customer.png)</span></span>

8. <span data-ttu-id="6a9e9-145">詳細を表示する円のスライスをポイントします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-145">Hover over the pie slices to see the details.</span></span> <span data-ttu-id="6a9e9-146">Eduardo が、過去に、赤い SUV をよくレンタルしていたことがわかります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-146">You'll notice that, in the past, Eduardo has often rented red SUVs.</span></span> <span data-ttu-id="6a9e9-147">これにより、次回の Eduardo の予約時に、販売員が利用可能な赤い SUV を探す手がかりを与えるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-147">This might give the sales clerk a cue to look for available red SUVs the next time Eduardo makes a reservation.</span></span> <span data-ttu-id="6a9e9-148">これは、積極的にインサイトを提供する簡単な例です。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-148">This is a simple example of proactively providing insights.</span></span>
9. <span data-ttu-id="6a9e9-149">顧客として自分自身を追加します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-149">Add yourself as a customer.</span></span>
    -   <span data-ttu-id="6a9e9-150">アクション ウィンドウで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-150">On the Action Pane, click **New**.</span></span> 
        
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="6a9e9-151">![ユーザー自身を追加](media/fmt_add_new.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-151">![Add yourself](media/fmt_add_new.png)</span></span>

    -   <span data-ttu-id="6a9e9-152">顧客として自身を追加するため、フォームに入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-152">Fill in the form to add yourself as a customer.</span></span> <span data-ttu-id="6a9e9-153">最低限、名前、クレジット カード フィールドの 16 桁の数字、住所情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-153">Make sure that you provide your name, a 16-digit number in the credit card field, and address information, at a minimum.</span></span> <span data-ttu-id="6a9e9-154">**注記**: 新しいレコードを保存するためのアクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-154">**Note**: You don't have to take any action to save a new record.</span></span>

10. <span data-ttu-id="6a9e9-155">新しいレンタルを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-155">Create a new rental.</span></span>
    1.  <span data-ttu-id="6a9e9-156">ナビゲーション バーで、**フリート管理** \> **レンタル** \>**レンタル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-156">On the navigation bar, go to **Fleet management** \> **Rentals** \> **Rental**.</span></span>
    2.  <span data-ttu-id="6a9e9-157">**レンタル** フォームで、アクション ウィンドウの **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-157">In the **Rental** form, on the Action Pane, click **New.**</span></span>
    3.  <span data-ttu-id="6a9e9-158">**車両** フィールドで車両を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-158">In the **Vehicle** field, select a vehicle.</span></span>
    4.  <span data-ttu-id="6a9e9-159">**顧客** フィールドで、自分の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-159">In the **Customer** field, select your name.</span></span>
    5.  <span data-ttu-id="6a9e9-160">**終了** フィールドで、終了日を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-160">In the **To** field, pick an end date.</span></span>
    6.  <span data-ttu-id="6a9e9-161">**開始** フィールドに、**35,000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-161">In the **Start** field, enter **35,000**.</span></span>
    7.  <span data-ttu-id="6a9e9-162">**ピックアップ** フィールドに、**フル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-162">In the **Pickup** field, enter **Full**.</span></span>
    8.  <span data-ttu-id="6a9e9-163">作業が終了したら、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-163">When you are done, click **Save**.</span></span>

11. <span data-ttu-id="6a9e9-164">レンタル期間を開始します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-164">Start the rental period.</span></span>
    1.  <span data-ttu-id="6a9e9-165">アクション ウィンドウで、**レンタル開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-165">On the Action Pane, click **Start rental**.</span></span>
    2.  <span data-ttu-id="6a9e9-166">ダイアログ ボックスで、フィールドの値を確認して **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-166">In the dialog box, verify the values in the fields and click **OK**.</span></span>

## <a name="use-fleet-management-to-run-a-workflow"></a><span data-ttu-id="6a9e9-167">フリート マネージメントを使用してワークフローを実行</span><span class="sxs-lookup"><span data-stu-id="6a9e9-167">Use Fleet Management to run a workflow</span></span>
1. <span data-ttu-id="6a9e9-168">**ホーム** アイコンをクリックして、ダッシュボードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-168">Click the **Home** icon to return to the dashboard.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-169">![ホーム アイコン](media/fmt_home_icon.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-169">![Home icon](media/fmt_home_icon.png)</span></span>

2. <span data-ttu-id="6a9e9-170">**予約管理** タイルをクリックして予約管理ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-170">Find the **Reservation Management** tile and select it to open the Reservation Management workspace.</span></span>
3. <span data-ttu-id="6a9e9-171">**現在のレンタル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-171">Click **Current rentals**.</span></span>
4. <span data-ttu-id="6a9e9-172">**レンタル** フォームで、レンタルの ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-172">On the **Rentals** form, click the ID of your rental.</span></span>
5. <span data-ttu-id="6a9e9-173">**レンタル** フォームの詳細ビューにあるアクション ウィンドウで、**レンタルの完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-173">On the Details view of the **Rentals** form, on the Action Pane, click **Complete rental**.</span></span>
6. <span data-ttu-id="6a9e9-174">**新しいマイレージ** フィールドに、**40,000** と入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-174">In the **New mileage** field, enter **40,000**, and then click **OK**.</span></span>
7. <span data-ttu-id="6a9e9-175">**ホーム** アイコンをクリックして、ダッシュボードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-175">Click the **Home** icon to return to the dashboard.</span></span>
8. <span data-ttu-id="6a9e9-176">ナビゲーション バーで、**フリート管理** &gt;**車両** &gt; **車両メンテナンス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-176">On the navigation bar, navigate to **Fleet management** &gt; **Vehicles** &gt; **Vehicle Maintenance**.</span></span> <span data-ttu-id="6a9e9-177">**車両メンテナンス** フォームでは、**ステータス** フィールドでレンタルがサービス部門によって検査待ちであることが示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-177">In the **Vehicle Maintenance** form, the **Status** field shows that your rental is awaiting examination by the service department.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-178">![車両メンテナンス](media/fmt_vehicle_examination.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-178">![Vehicle mainenance](media/fmt_vehicle_examination.png)</span></span>
        
    > [!NOTE]
    > <span data-ttu-id="6a9e9-179">バッチ フレームワークが車両の状態を変更するまで、最大で 2分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-179">You might need to wait up to two minutes for the batch framework to change the status of the vehicle.</span></span> <span data-ttu-id="6a9e9-180">アクション ウィンドウで、**更新** をクリックしステータスの変更が表示されるまで、ビューを定期的に更新します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-180">On the Action Pane, click **Refresh** periodically to update the view, until you see the status change.</span></span> <span data-ttu-id="6a9e9-181">別の人がワークフローの各ステップを通常処理することに留意してください。バッチ フレームワークによって生じる多少の遅延は、実際のアプリケーションでは問題ありません。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-181">Keep in mind that a different person usually handles each step in a workflow; the brief delay introduced by the batch framework is not an issue in a real-world application.</span></span>

9.  <span data-ttu-id="6a9e9-182">レンタルを含む行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-182">Select the row that contains your rental.</span></span> <span data-ttu-id="6a9e9-183">アクション ウィンドウで、**ワークフロー** をクリックし、**検査完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-183">On the Action Pane, click **Workflow**, and then click **Examination complete**.</span></span> <span data-ttu-id="6a9e9-184">ワークフローでフルセットのオプションを取得するには、ページを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-184">You may need to refresh the page to get the full set of options under Workflow.</span></span>
10. <span data-ttu-id="6a9e9-185">コメントを入力し、**検査完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-185">Enter a comment, and then click **Examination complete**.</span></span>
11. <span data-ttu-id="6a9e9-186">バッチ フレームワークが変更を処理するまで、最大で 2 分再度待機することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-186">You might again need to wait up to two minutes for the batch framework to process the change.</span></span> <span data-ttu-id="6a9e9-187">アクション ウィンドウで、**ステータス** フィールドの変更が表示されるまで、**更新** を定期的にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-187">On the Action Pane, click **Refresh** periodically, until you see the **Status** field change.</span></span> <span data-ttu-id="6a9e9-188">車両が **サービス待ち** の状態であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-188">Notice that the vehicle now has a status of **Awaiting Service**.</span></span>
12. <span data-ttu-id="6a9e9-189">必要に応じて、このワークフロー手順を引き続き繰り返して、車両にサービスおよびクリーニング フェーズを実行できます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-189">Optionally, you can continue to repeat these workflow steps to take the vehicle through the service and cleaning phases.</span></span> <span data-ttu-id="6a9e9-190">クリーニングが完了した後、最終状態は、**実行** になります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-190">After cleaning is completed, the final status is **Done**.</span></span>
13. <span data-ttu-id="6a9e9-191">**ワークフロー**、**履歴の表示** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-191">Click **Workflow**, and then click **View history**.</span></span> <span data-ttu-id="6a9e9-192">**ワークフロー履歴** フォームは、車両ワークフローに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-192">The **Workflow history** form provides information about the vehicle workflow.</span></span>
14. <span data-ttu-id="6a9e9-193">**追跡の詳細** をクリックして活動を表示します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-193">Click **Tracking details** to see the activities.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-194">![追跡の詳細](media/fmt_workflow_history.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-194">![Tracking details](media/fmt_workflow_history.png)</span></span>

### <a name="to-view-the-setup-behind-the-workflow"></a><span data-ttu-id="6a9e9-195">ワークフローの背後に設定を表示するには</span><span class="sxs-lookup"><span data-stu-id="6a9e9-195">To view the setup behind the workflow</span></span>

1.  <span data-ttu-id="6a9e9-196">ダッシュ ボードで、**フリート管理** \> **設定** \> **ワークフローの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-196">On the dashboard, navigate to **Fleet Management** \> **Setup** \> **Workflow setup**.</span></span> <span data-ttu-id="6a9e9-197">**ワークフロー セットアップ** ページには、ワークフローの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-197">The **Workflow Setup** page shows the list of workflows.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-198">![ワークフローの設定](media/fmt_workflow_setup.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-198">![Workflow setup](media/fmt_workflow_setup.png)</span></span>
    
2.  <span data-ttu-id="6a9e9-199">**ワークフロー ID** 列に、車両メンテナンス ワークフローの ID をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-199">In the **Workflow ID** column, click the ID of your vehicle maintenance workflow.</span></span>
3.  <span data-ttu-id="6a9e9-200">コードを実行するアクセス許可を求めるプロンプトを承認します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-200">Accept any prompts that ask you for permission to run code.</span></span> <span data-ttu-id="6a9e9-201">短い待機の後、ワークフロー エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-201">After a short wait, the workflow editor opens.</span></span> <span data-ttu-id="6a9e9-202">このステップは、クラウドではなく 1 ボックス環境で動作します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-202">This step works on the one-box environment, but not in the cloud.</span></span> <span data-ttu-id="6a9e9-203">ワークフロー エディターでは、ワークフロー図を表示できます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-203">You can view the workflow diagram in the workflow editor.</span></span> <span data-ttu-id="6a9e9-204">次の図はワークフローを示します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-204">The following illustration shows the workflow.</span></span>
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-205">![ワークフロー エディター](media/fmt_workflow_editor.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-205">![Workflow editor](media/fmt_workflow_editor.png)</span></span>

4.  <span data-ttu-id="6a9e9-206">完了したら、**ワークフロー** ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-206">When you are done, close the **Workflow** window.</span></span>

## <a name="create-a-new-kpi-definition"></a><span data-ttu-id="6a9e9-207">新しい KPI 定義を作成する</span><span class="sxs-lookup"><span data-stu-id="6a9e9-207">Create a new KPI definition</span></span>
<span data-ttu-id="6a9e9-208">Web クライアントを使用すると、適切な権限を持つユーザーが、開発者がモデル化して展開した KPI 定義を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-208">The web client enables users who have appropriate permissions to modify KPI definitions that have been modeled and deployed by developers.</span></span> <span data-ttu-id="6a9e9-209">ユーザーは、クライアントに新しい KPI 定義を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-209">Users also have the ability to create new KPI definitions in the client.</span></span> <span data-ttu-id="6a9e9-210">このチュートリアルでは、クライアントで新しい KPI の定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-210">In this walkthrough, you create a new KPI definition in the client.</span></span>

1.  <span data-ttu-id="6a9e9-211">**予約管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-211">Open the **Reservation Management** workspace.</span></span> <span data-ttu-id="6a9e9-212">ナビゲーション バーで、 **フリート管理 &gt; ワークスペース &gt; 予約管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-212">On the navigation bar, go to **Fleet Management &gt; Workspaces &gt; Reservation Management**.</span></span>
2.  <span data-ttu-id="6a9e9-213">ワークスペースの左下に表示されている総収益 KPI タイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-213">Notice the Total revenue KPI tile shown on the bottom left of the workspace.</span></span> <span data-ttu-id="6a9e9-214">**総収益 KPI** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-214">Click the **Total Revenue KPI** tile.</span></span> <span data-ttu-id="6a9e9-215">総収益 KPI タイルの詳細と共に収益の上位および下位貢献者を示すチャートが画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-215">Details of the total revenue KPI tile along with charts indicating top and bottom contributors to revenue will be shown on screen.</span></span>
3.  <span data-ttu-id="6a9e9-216">次に、レンタルの数を監視する新しい KPI を定義します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-216">Next, you will define a new KPI to monitor the number of rentals.</span></span>
4.  <span data-ttu-id="6a9e9-217">アクション ウィンドウで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-217">On the Action Pane, click **New**.</span></span> <span data-ttu-id="6a9e9-218">**新しい KPI** ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-218">The **New KPI** dialog will open.</span></span>
5.  <span data-ttu-id="6a9e9-219">新しい KPI 定義に次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-219">Enter following values for the new KPI definition.</span></span>

    | <span data-ttu-id="6a9e9-220">フィールド</span><span class="sxs-lookup"><span data-stu-id="6a9e9-220">Field</span></span>         | <span data-ttu-id="6a9e9-221">先頭値</span><span class="sxs-lookup"><span data-stu-id="6a9e9-221">Value</span></span>               |
    |---------------|-------------------------|
    | <span data-ttu-id="6a9e9-222">氏名</span><span class="sxs-lookup"><span data-stu-id="6a9e9-222">Name</span></span>          | <span data-ttu-id="6a9e9-223">レンタルの数</span><span class="sxs-lookup"><span data-stu-id="6a9e9-223">Number of Rentals</span></span>       |
    | <span data-ttu-id="6a9e9-224">測定</span><span class="sxs-lookup"><span data-stu-id="6a9e9-224">Measurement</span></span>   | <span data-ttu-id="6a9e9-225">FMAggregateMeasurements</span><span class="sxs-lookup"><span data-stu-id="6a9e9-225">FMAggregateMeasurements</span></span> |
    | <span data-ttu-id="6a9e9-226">メジャー グループ</span><span class="sxs-lookup"><span data-stu-id="6a9e9-226">Measure group</span></span> | <span data-ttu-id="6a9e9-227">FmRentalCharges</span><span class="sxs-lookup"><span data-stu-id="6a9e9-227">FmRentalCharges</span></span>         |
    | <span data-ttu-id="6a9e9-228">基準</span><span class="sxs-lookup"><span data-stu-id="6a9e9-228">Measure</span></span>       | <span data-ttu-id="6a9e9-229">NoRentals</span><span class="sxs-lookup"><span data-stu-id="6a9e9-229">NoRentals</span></span>               |
    | <span data-ttu-id="6a9e9-230">KPI 目標タイプ</span><span class="sxs-lookup"><span data-stu-id="6a9e9-230">KPI Goal Type</span></span> | <span data-ttu-id="6a9e9-231">固定値</span><span class="sxs-lookup"><span data-stu-id="6a9e9-231">Fixed Value</span></span>             |
    | <span data-ttu-id="6a9e9-232">目標値</span><span class="sxs-lookup"><span data-stu-id="6a9e9-232">Goal value</span></span>    | <span data-ttu-id="6a9e9-233">30</span><span class="sxs-lookup"><span data-stu-id="6a9e9-233">30</span></span>                      |
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-234">![新規 KPI](media/fmt_new_kpi.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-234">![New KPI](media/fmt_new_kpi.png)</span></span>

6.  <span data-ttu-id="6a9e9-235">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-235">Click **Save**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="6a9e9-236">**新規 KPI** ダイアログ ボックスで、**保存** ボタンが表示されない場合、より高い画面解像度を使用するとダイアログ全体を表示できます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-236">If the **Save** button isn’t visible in the **New KPI** dialog box, use a higher screen resolution so that you can see the entire dialog.</span></span> <span data-ttu-id="6a9e9-237">作成した KPI に関する詳細を含む、KPI 詳細ページを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-237">You can see the KPI details page that contains details about the KPI that you created.</span></span> <span data-ttu-id="6a9e9-238">**詳細** セクションで変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-238">You can make changes in the **Details** section.</span></span> <span data-ttu-id="6a9e9-239">値が目標の 90% 未満の場合は KPI が赤く表示され、値が目標の 110% を超える場合は KPI が緑で表示されるように、既定のしきい値を変更します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-239">You will modify the default threshold values so that if the value is less than 90% of the goal, the KPI will show red and if the value is over 110% of the goal, the KPI will show green.</span></span>

7.  <span data-ttu-id="6a9e9-240">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-240">Click **Edit**.</span></span>

8.  <span data-ttu-id="6a9e9-241">画面の右にスクロールし、次のようにしきい値フィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-241">Scroll to the right of the screen, and modify the values in the thresholds fields as follows.</span></span>

    | <span data-ttu-id="6a9e9-242">プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a9e9-242">Property</span></span>           | <span data-ttu-id="6a9e9-243">先頭値</span><span class="sxs-lookup"><span data-stu-id="6a9e9-243">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="6a9e9-244">次の値未満の場合に不良: </span><span class="sxs-lookup"><span data-stu-id="6a9e9-244">Bad if less than</span></span>   | <span data-ttu-id="6a9e9-245">90</span><span class="sxs-lookup"><span data-stu-id="6a9e9-245">90</span></span>        |
    | <span data-ttu-id="6a9e9-246">次の値を超えた場合に良: </span><span class="sxs-lookup"><span data-stu-id="6a9e9-246">Good if more than</span></span>  | <span data-ttu-id="6a9e9-247">110</span><span class="sxs-lookup"><span data-stu-id="6a9e9-247">110</span></span>       |

9.  <span data-ttu-id="6a9e9-248">アプリケーション バーで、 **保存** をクリックします</span><span class="sxs-lookup"><span data-stu-id="6a9e9-248">In the application bar, click **Save**.</span></span> 
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-249">![KPI グラフ](media/fmt_kpi_value.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-249">![KPI graph](media/fmt_kpi_value.png)</span></span>

10. <span data-ttu-id="6a9e9-250">グリッド ビューに戻るには、フォーム キャプションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-250">Click the form caption to return to the grid view.</span></span>
11. <span data-ttu-id="6a9e9-251">**名** 列ヘッダーをクリックし、フィルター演算子を **部分一致** に変更し、フィルター フィールド値を **番号** に更新します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-251">Click the **Name** column header, change the filter operator to **contains**, and update the filter field value to **Number**.</span></span> <span data-ttu-id="6a9e9-252">新しい KPI をリストで使用できることが分かります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-252">You will see the new KPI is available in the list.</span></span>
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-253">![KPI リスト](media/fmt_kpi_list.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-253">![KPI list](media/fmt_kpi_list.png)</span></span>

## <a name="launch-an-operational-report"></a><span data-ttu-id="6a9e9-254">運用レポートの起動</span><span class="sxs-lookup"><span data-stu-id="6a9e9-254">Launch an operational report</span></span>
<span data-ttu-id="6a9e9-255">このチュートリアルでは、現在車両をレンタルしている顧客の一覧を含む運用レポートを開始します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-255">In this tutorial, you’ll launch an operational report that contains a list of customers who are currently renting vehicles.</span></span>

1.  <span data-ttu-id="6a9e9-256">ダッシュボードを使用して、**予約管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-256">Use the dashboard to open the **Reservation management** workspace.</span></span>
2.  <span data-ttu-id="6a9e9-257">ページの右側の **レポート** で **顧客リスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-257">On the right side of the page, under **Reports** click **Customer list**.</span></span> <span data-ttu-id="6a9e9-258">**顧客グループ** のパラメーターでは、何も入力しないでください。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-258">Do not enter anything in the parameter for **Customer group**.</span></span> 
    
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-259">![顧客リスト](media/fmt_customer_list_report.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-259">![Customer list](media/fmt_customer_list_report.png)</span></span>

3.  <span data-ttu-id="6a9e9-260">**OK** をクリックしてダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-260">Click **OK** to close the dialog box.</span></span> <span data-ttu-id="6a9e9-261">レポートが表示され、顧客リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-261">The report will be rendered and show the list of customers.</span></span> <span data-ttu-id="6a9e9-262">レポートを表示するのに、数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-262">The report may take a minute to render.</span></span>

## <a name="secure-access-using-the-role-based-security-system"></a><span data-ttu-id="6a9e9-263">ロールベースのセキュリティ システムを使用してアクセスを保護</span><span class="sxs-lookup"><span data-stu-id="6a9e9-263">Secure access using the role-based security system</span></span>
<span data-ttu-id="6a9e9-264">このチュートリアルでは、さまざまなセキュリティ ロールが割り当てられているユーザーとしてシステムにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-264">In this tutorial, you’ll access the system as a user that has been assigned a different security role.</span></span> <span data-ttu-id="6a9e9-265">このチュートリアルでは、少なくとも 1 人の追加エンド ユーザーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-265">This tutorial requires that you have created at least one additional end user.</span></span>

1.  <span data-ttu-id="6a9e9-266">ダッシュ ボードの **システム管理** セクションで、**ユーザー**、**ユーザー** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-266">On the dashboard, in the **System administration** section, click **Users** and then **Users**.</span></span>
2.  <span data-ttu-id="6a9e9-267">アクション ウィンドウで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-267">On the Action Pane, click **New**.</span></span>
3.  <span data-ttu-id="6a9e9-268">以下のフィールド情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-268">Enter the following field information.</span></span>

    | <span data-ttu-id="6a9e9-269">プロパティ</span><span class="sxs-lookup"><span data-stu-id="6a9e9-269">Property</span></span>        | <span data-ttu-id="6a9e9-270">先頭値</span><span class="sxs-lookup"><span data-stu-id="6a9e9-270">Value</span></span>                                                                                 |
    |-----------------|-------------------------------------------------------------------------------------------|
    | <span data-ttu-id="6a9e9-271">ユーザー ID</span><span class="sxs-lookup"><span data-stu-id="6a9e9-271">User ID</span></span>         | <span data-ttu-id="6a9e9-272">8 文字の固有 ID</span><span class="sxs-lookup"><span data-stu-id="6a9e9-272">Eight character unique ID</span></span>                                                                 |
    | <span data-ttu-id="6a9e9-273">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="6a9e9-273">User name</span></span>       | <span data-ttu-id="6a9e9-274">ユーザーの最初の名前</span><span class="sxs-lookup"><span data-stu-id="6a9e9-274">The first name of the user</span></span>                                                                |
    | <span data-ttu-id="6a9e9-275">プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6a9e9-275">Provider</span></span>        | `urn:Federation:MicrosoftOnline`                                                          |
    | <span data-ttu-id="6a9e9-276">電子メール</span><span class="sxs-lookup"><span data-stu-id="6a9e9-276">Email</span></span>           | <span data-ttu-id="6a9e9-277">テスト用にログインできる電子メール エイリアスを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-277">Use an email alias that you can login with for testing.</span></span>                                   |
    | <span data-ttu-id="6a9e9-278">法人</span><span class="sxs-lookup"><span data-stu-id="6a9e9-278">Company</span></span>         | `DAT`                                                                                     |
    | <span data-ttu-id="6a9e9-279">有効な機能</span><span class="sxs-lookup"><span data-stu-id="6a9e9-279">Enabled</span></span>         | <span data-ttu-id="6a9e9-280">このスライダーが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-280">Verify that this slider is set to **Yes**.</span></span>                                                |

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-281">![新しいユーザー レコード](media/fmt_new_user_record.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-281">![New user record](media/fmt_new_user_record.png)</span></span>

4.  <span data-ttu-id="6a9e9-282">**ロールの割り当て** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-282">Click **Assign Roles**.</span></span> 

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6a9e9-283">![ブランチ マネージャーの割り当て](media/fmt_branch_manager.png)</span><span class="sxs-lookup"><span data-stu-id="6a9e9-283">![Assign branch manager](media/fmt_branch_manager.png)</span></span>

5.  <span data-ttu-id="6a9e9-284">**フリート管理ブランチ マネージャー** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-284">Select **Fleet management branch manager**, and then click **OK**.</span></span>
6.  <span data-ttu-id="6a9e9-285">右上のユーザー名をクリックしてから、**サインアウト** をクリックします。サインイン ページにリダイレクトされます</span><span class="sxs-lookup"><span data-stu-id="6a9e9-285">Click the user name on the top right, and then click **Sign Out**. You’ll be redirected back to the sign-n page</span></span>
7.  <span data-ttu-id="6a9e9-286">上記の手順でセキュリティ ロールを割り当てたユーザーの資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-286">Sign in using the credentials for the user who you assigned the security role to in the steps above.</span></span>
8.  <span data-ttu-id="6a9e9-287">ダッシュボードで、このユーザーはランチ マネージャー セキュリティ ロールに関連する項目のみ確認できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-287">Notice that in the dashboard, this user can see only items that are related to the branch manager security role.</span></span> <span data-ttu-id="6a9e9-288">システム管理者が確認できる項目は非表示になります。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-288">Items that system administrators can see are now hidden.</span></span>
9.  <span data-ttu-id="6a9e9-289">セッションをサインアウトするには、**サインアウト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a9e9-289">Click **Sign out** to sign out of the session.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]