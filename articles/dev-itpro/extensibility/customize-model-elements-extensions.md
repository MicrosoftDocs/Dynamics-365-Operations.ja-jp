---
title: 拡張機能によってモデル要素をカスタマイズする
description: このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。 Dynamics AX の拡張機能を示すために、このモデルにはフリート管理アプリケーションの機能を拡張する要素が含まれています。
author: robadawy
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 11184
ms.assetid: 3190f6e2-698a-4cfa-9a2d-a6c57354920a
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 739033a750925d948039e3ed52eee33336d2e56e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368307"
---
# <a name="customize-model-elements-through-extension"></a><span data-ttu-id="5b791-104">拡張機能によってモデル要素をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="5b791-104">Customize model elements through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b791-105">このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。</span><span class="sxs-lookup"><span data-stu-id="5b791-105">In this tutorial, you’ll become familiar with the Fleet Management Extension model.</span></span> <span data-ttu-id="5b791-106">このモデルには、フリート管理アプリケーションの機能を拡張する要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b791-106">This model contains elements that extend the functionality of the Fleet Management application.</span></span> <span data-ttu-id="5b791-107">*拡張機能* を作成することにより、モデル要素をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-107">You can customize model elements by creating *extensions*.</span></span> <span data-ttu-id="5b791-108">Microsoft Dynamics AX 2012 の オーバーレイ機能とは異なり、拡張機能はベースライン モデル要素をオーバーレイしません。</span><span class="sxs-lookup"><span data-stu-id="5b791-108">Unlike the overlayering capabilities of Microsoft Dynamics AX 2012, extensions don’t overlay the baseline model elements.</span></span> <span data-ttu-id="5b791-109">代わりに、拡張機能はモデルと関連付けられているビジネス ロジックに追加またはカスタマイズする別のアセンブリとしてコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="5b791-109">Instead, extensions are compiled as a separate assembly that adds to or customizes the model and the associated business logic.</span></span> <span data-ttu-id="5b791-110">テーブルにフィールドを追加、またはフォームにコントロールを追加することなどによりメタデータを拡張、およびイベント ハンドラおよびプラグイン クラスを定義することによりビジネス ロジックを拡張またはカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-110">You can extend metadata, for example, by adding a field to a table or adding a control to a form, and also extend or customize business logic by defining event handlers and plug-in classes.</span></span> <span data-ttu-id="5b791-111">テーブル、フォーム、フォーム データ ソース、フォーム コントロール、およびその他を使用して、様々な定義済みイベントでイベント ハンドラーを作成することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5b791-111">You can now author event handlers on several pre-defined events on tables, forms, form data sources, form controls, and others.</span></span> <span data-ttu-id="5b791-112">プラグインは、アプリケーションのビジネス ロジックを交換または拡張するできるようにする新しい機能拡張の概念でもあります。</span><span class="sxs-lookup"><span data-stu-id="5b791-112">Plug-ins are also a new extensibility concept that enables replacing or extending the business logic of the application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b791-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="5b791-113">Prerequisites</span></span>
<span data-ttu-id="5b791-114">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b791-114">This tutorial requires you to access the environment using Remote Desktop, and that you be provisioned as an administrator on the instance.</span></span>

## <a name="understanding-the-fleet-management-model"></a><span data-ttu-id="5b791-115">フリート管理モデルを理解する</span><span class="sxs-lookup"><span data-stu-id="5b791-115">Understanding the Fleet Management model</span></span>
<span data-ttu-id="5b791-116">フリート管理アプリケーションは、車両、顧客、および車両予約を管理するためのシステムをレンタル自動車会社に提供します。</span><span class="sxs-lookup"><span data-stu-id="5b791-116">The Fleet Management application provides a rental car company a system for managing vehicles, customers and vehicle reservations.</span></span> <span data-ttu-id="5b791-117">アプリケーションは、フリート係とフリート マネージャの役割で使用されるよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-117">The application is designed for use by the Fleet Clerk and Fleet Manager personas.</span></span>

### <a name="fleet-clerk"></a><span data-ttu-id="5b791-118">フリート係</span><span class="sxs-lookup"><span data-stu-id="5b791-118">Fleet Clerk</span></span>

<span data-ttu-id="5b791-119">担当者は、顧客との対面または電話でのやり取りを処理する受付従業員です。</span><span class="sxs-lookup"><span data-stu-id="5b791-119">The Clerk is the front desk employee who handles the face-to-face and over-the-phone interactions with customers.</span></span> <span data-ttu-id="5b791-120">担当者は主に、アプリケーションに顧客情報を入力する、顧客の車両予約を作成する、車両アクセサリをオファーすることで予約をアップセルする、車両レンタルの終了時に車両の返却を処理することに関心を持っています。</span><span class="sxs-lookup"><span data-stu-id="5b791-120">The Clerk is primarily concerned with entering customer information into the application, creating vehicle reservations for customers, upselling the reservation by offering vehicle accessories, and processing vehicle returns upon completion of a vehicle rental.</span></span> <span data-ttu-id="5b791-121">担当者は、各自のニーズを予測し、楽しくて印象的なエクスペリエンスを提供しながら、顧客とやり取りすることにより、**フリート管理ワークスペース**を使用して顧客とのやり取りを準備することに大部分の時間を費やします。</span><span class="sxs-lookup"><span data-stu-id="5b791-121">The Clerk spends the vast majority of their time using the **Fleet Management Workspace** to prepare for interactions with customers by anticipating their needs and providing a pleasant and memorable experience, while interacting with the customer.</span></span>

### <a name="fleet-manager"></a><span data-ttu-id="5b791-122">フリート マネージャー</span><span class="sxs-lookup"><span data-stu-id="5b791-122">Fleet Manager</span></span>

<span data-ttu-id="5b791-123">マネージャーは、業務要件とプロセスの設定を処理するバック オフィス従業員です。</span><span class="sxs-lookup"><span data-stu-id="5b791-123">The Manager is the back office employee who handles setting business requirements and processes.</span></span> <span data-ttu-id="5b791-124">マネージャーは、車両の情報を入力する、使用可能な車両アクセサを定義する、車両メンテナンス、価格を決定する、および収益、アップセルの成功などのビジネス パフォーマンス測定を分析することに主に関心を持っています。</span><span class="sxs-lookup"><span data-stu-id="5b791-124">The Manager is primarily concerned with entering vehicle information, defining the available vehicle accessories, vehicle maintenance, determining pricing, and analyzing business performance measures such as revenue, upsell success, and so on.</span></span> <span data-ttu-id="5b791-125">アプリケーションのビジネス ロジックは、次の 3 つの主なエンティティとそれらの間の関係を中心に展開されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-125">The application's business logic revolves around the following three primary entities and the relationships between them.</span></span>

### <a name="customers"></a><span data-ttu-id="5b791-126">顧客</span><span class="sxs-lookup"><span data-stu-id="5b791-126">Customers</span></span>

<span data-ttu-id="5b791-127">顧客は、車両の予約を行い、車両のアクセサリを選択し、車両をチェックアウトおよび返却をし、車両のレンタル料を支払うためにフリート係に連絡します。</span><span class="sxs-lookup"><span data-stu-id="5b791-127">Customers contact the Fleet Clerk to make vehicle reservations, choose vehicle accessories, check out and return vehicles, and pay for vehicle rentals.</span></span> <span data-ttu-id="5b791-128">顧客関連の情報は、**FMCustomer** というテーブルに保管されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-128">Customer-related information is stored in the table named **FMCustomer**.</span></span>

### <a name="vehicles"></a><span data-ttu-id="5b791-129">車両及び運搬具</span><span class="sxs-lookup"><span data-stu-id="5b791-129">Vehicles</span></span>

<span data-ttu-id="5b791-130">車両は主として価格が異なり、車両の*クラス*に比例します。</span><span class="sxs-lookup"><span data-stu-id="5b791-130">Vehicles vary primarily in their price, which is proportional to the vehicle *class*.</span></span> <span data-ttu-id="5b791-131">車両に関する情報を格納するテーブルの名前は、「FMVehicle」で始まります。\*\*</span><span class="sxs-lookup"><span data-stu-id="5b791-131">The names of tables that store information about vehicles begin with "FMVehicle".\*\*</span></span>

### <a name="reservations-and-rentals"></a><span data-ttu-id="5b791-132">引当とレンタル</span><span class="sxs-lookup"><span data-stu-id="5b791-132">Reservations and rentals</span></span>

<span data-ttu-id="5b791-133">引当は、顧客および車両間の関係を処理します。</span><span class="sxs-lookup"><span data-stu-id="5b791-133">Reservations handle the relationship between customers and vehicles.</span></span> <span data-ttu-id="5b791-134">引当情報には、引当日、顧客情報、車両の選択と価格、およびアクセサリや手数料などの追加の雑費が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5b791-134">Reservation information includes reservation dates, customer information, vehicle selection and price, and additional charges such as accessories or fees.</span></span> <span data-ttu-id="5b791-135">引当やレンタル情報は、**FMRental** および **FMRentalCharge** テーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-135">Reservation and rental information is stored in the **FMRental** and **FMRentalCharge** tables.</span></span> <span data-ttu-id="5b791-136">計算エンジンは、車両予約の価格決定に関連するトランザクションの情報を処理します。</span><span class="sxs-lookup"><span data-stu-id="5b791-136">A calculation engine handles the transactional information related to the pricing of vehicle reservations.</span></span> <span data-ttu-id="5b791-137">このデータ モデルを使用すると、フリート管理アプリケーションは基本的な自動車レンタル経験を提供します。</span><span class="sxs-lookup"><span data-stu-id="5b791-137">Using this data model the Fleet Management application provides a basic car rental experience.</span></span>

## <a name="extending-the-fleet-management-model"></a><span data-ttu-id="5b791-138">フリート管理モデルを拡張</span><span class="sxs-lookup"><span data-stu-id="5b791-138">Extending the Fleet Management model</span></span>
<span data-ttu-id="5b791-139">基本的なフリート管理アプリケーションは、追加機能でカスタマイズされています。これらの機能によりレンタカー会社は、割引を使用して顧客に価格インセンティブを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-139">The basic Fleet Management application has been customized with additional capabilities that enable a rental car company to provide pricing incentives to its customers through discounts.</span></span> <span data-ttu-id="5b791-140">これらの割引機能を使用可能にする追加のビジネス ロジックおよびデータは、フリート管理拡張モデルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-140">The additional business logic and data that enables these discount capabilities is stored in the Fleet Management Extension model.</span></span> <span data-ttu-id="5b791-141">割引機能は、3 つの主要なカスタマイズを介してフリート管理アプリケーションに価値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b791-141">The discount capabilities add value to the Fleet management application through three primary customizations.</span></span>

### <a name="the-fleet-management-extension-data-model"></a><span data-ttu-id="5b791-142">フリート管理拡張モデル</span><span class="sxs-lookup"><span data-stu-id="5b791-142">The Fleet Management Extension data model</span></span>

<span data-ttu-id="5b791-143">割引に関連する情報を格納する 2 つの新しいテーブルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="5b791-143">Two new tables have been added that store discount-related information.</span></span> <span data-ttu-id="5b791-144">**FEDiscounts** には、すべての割引とその料金のリストが保存されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-144">**FEDiscounts** stores the list of all discounts and their rates.</span></span> <span data-ttu-id="5b791-145">**FERentalDiscountRelationTable** は割引が適用される引当を追跡します。</span><span class="sxs-lookup"><span data-stu-id="5b791-145">**FERentalDiscountRelationTable** keeps track of the reservations that the discounts are applied to.</span></span> <span data-ttu-id="5b791-146">既存のテーブルは、価格設定スキームへの割引口座に拡張されました。</span><span class="sxs-lookup"><span data-stu-id="5b791-146">Existing tables have been extended to account for the addition of discounts to the pricing scheme.</span></span> <span data-ttu-id="5b791-147">**FMRental** という特定の予約の車両料金を追跡するテーブルは、車両料金の割引に対応するように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="5b791-147">The table that keeps track of the vehicle rate for a particular reservation, named **FMRental**, has been extended to accommodate discounts to the vehicle rate.</span></span> <span data-ttu-id="5b791-148">**FMRentalCharge** という予約のアクセサリーを追跡しているテーブルは、アクセサリーに適用される割引に対応するために拡張されました。</span><span class="sxs-lookup"><span data-stu-id="5b791-148">The table that keeps track of the accessories for a reservation, named **FMRentalCharge**, has been extended to accommodate discounts applied to accessories.</span></span>

### <a name="the-fleet-management-extension-calculation-engine"></a><span data-ttu-id="5b791-149">フリート管理拡張計算エンジン</span><span class="sxs-lookup"><span data-stu-id="5b791-149">The Fleet Management Extension Calculation Engine</span></span>

<span data-ttu-id="5b791-150">基本的な計算エンジンには、カスタマイズにより、新しい割引によって定義されたさまざまな価格決定スキーマが追加されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-150">The basic calculation engine has been customized to add the various pricing schemes defined by the new discounts.</span></span> <span data-ttu-id="5b791-151">プラグイン クラスによって、基本計算エンジンの機能が置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="5b791-151">A plug-in class has replaced the functionality of the base calculation engine.</span></span> <span data-ttu-id="5b791-152">車両の予約が 7 日間を超えるときは、車両フリート管理モデルが、車両の 1 日当たりの料金とより低い 1 週間あたりの料金との差に基づいて、節約を計算します。</span><span class="sxs-lookup"><span data-stu-id="5b791-152">When a vehicle is reserved for more than 7 days, the vehicle Fleet Management model calculates savings based on the difference between a vehicle's daily rate and a lower weekly rate.</span></span> <span data-ttu-id="5b791-153">プラグインは、同じ動作を割引を使用して実現できるため、1 週間あたりの料金の計算を削除します。</span><span class="sxs-lookup"><span data-stu-id="5b791-153">The plug-in removes the weekly-rate calculation because this same behavior can be accomplished by using discounts.</span></span>

### <a name="the-fleet-management-user-interface-extensions"></a><span data-ttu-id="5b791-154">フリート管理ユーザー インターフェイス拡張</span><span class="sxs-lookup"><span data-stu-id="5b791-154">The Fleet Management User Interface Extensions</span></span>

<span data-ttu-id="5b791-155">**FMRental** という名前のフォームに組み込まれている Rental は、担当者が予約に割引を適用できるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-155">The Rental, which is contained by the form named **FMRental**, has been extended to enable the Clerk to apply discounts to a reservation.</span></span> <span data-ttu-id="5b791-156">画面上の価格の概要は、予約に関連する車両およびアクセサリに適用可能な割引に関する貯蓄情報によってリアルタイムで更新されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-156">The on-screen price summary is updated in real time with savings information related to discounts that can be applied to vehicles and accessories related to the reservation.</span></span> <span data-ttu-id="5b791-157">次の手順では、フリート管理拡張モデルでのカスタマイズを調べて、自分でカスタマイズの一部を再実装します。</span><span class="sxs-lookup"><span data-stu-id="5b791-157">In the following steps, you'll explore the customizations that have been made in the Fleet management Extension model, as well as re-implement a portion of the customizations for yourself.</span></span>

## <a name="setup"></a><span data-ttu-id="5b791-158">段取り</span><span class="sxs-lookup"><span data-stu-id="5b791-158">Setup</span></span>
<span data-ttu-id="5b791-159">前のチュートリアルでフリート管理ソリューションを開いていない場合は、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5b791-159">If you haven't opened the Fleet Management Solution in a previous tutorial, follow these steps.</span></span> <span data-ttu-id="5b791-160">フリート管理ソリューション ファイルは、Dynamics AX のダウンロード可能な VM で利用できます。</span><span class="sxs-lookup"><span data-stu-id="5b791-160">The fleet management solution file is available on the Dynamics AX downloadable VM.</span></span>

1.  <span data-ttu-id="5b791-161">**デスクトップ**で、**Visual Studio** ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-161">On the **Desktop**, double-click the **Visual Studio** shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="5b791-162">**FleetManagement** ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-162">Open the **FleetManagement** solution.</span></span> <span data-ttu-id="5b791-163">**ファイル**メニューで、**開く**をポイントし、**プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-163">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
3.  <span data-ttu-id="5b791-164">デスクトップを参照し、**FleetManagement** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-164">Browse to the desktop and open the **FleetManagement** folder.</span></span> <span data-ttu-id="5b791-165">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-165">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
4.  <span data-ttu-id="5b791-166">**FleetManagement** という名前のソリューション ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b791-166">Select the solution file named **FleetManagement**.</span></span> <span data-ttu-id="5b791-167">表示されるファイル タイプは Microsoft Visual Studio Solution です。</span><span class="sxs-lookup"><span data-stu-id="5b791-167">The file type listed is Microsoft Visual Studio Solution.</span></span>
5.  <span data-ttu-id="5b791-168">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-168">Click **Open**.</span></span> <span data-ttu-id="5b791-169">ソリューションを開くには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5b791-169">The solution may take some time to open.</span></span>



### <a name="installing-the-demo-data"></a><span data-ttu-id="5b791-170">デモ データのインストール</span><span class="sxs-lookup"><span data-stu-id="5b791-170">Installing the demo data</span></span>

<span data-ttu-id="5b791-171">デモ データを既にインストールしている場合、次のセクションに進めます。</span><span class="sxs-lookup"><span data-stu-id="5b791-171">If you've already installed the demo data, you can skip to the next section.</span></span>

1.  <span data-ttu-id="5b791-172">VM で、Internet Explorer を開き、アプリケーションのベース URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b791-172">In the VM, open Internet Explorer and navigate to the application's base URL.</span></span>
2.  <span data-ttu-id="5b791-173">サインインします。</span><span class="sxs-lookup"><span data-stu-id="5b791-173">Sign in.</span></span>
3.  <span data-ttu-id="5b791-174">ダッシュ ボードで、ナビゲーション ウィンドウを開き、**フリート管理 &gt; 設定 &gt; フリート設定**に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b791-174">On the dashboard, open the navigation pane and navigate to **Fleet Management &gt; Setup &gt; Fleet Setup**.</span></span> <span data-ttu-id="5b791-175">[![フリート設定 > カスタマイズ モデル](./media/fleetsetup_customizemodel.png)](./media/fleetsetup_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-175">[![Fleet setup > Customize model](./media/fleetsetup_customizemodel.png)](./media/fleetsetup_customizemodel.png)</span></span>
4.  <span data-ttu-id="5b791-176">**デモ データの設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-176">Click **Setup Demo Data**.</span></span> 

    <span data-ttu-id="5b791-177">[![コンフィギュレーション > モデルをカスタマイズする](./media/configuration_customizemodel.png)](./media/configuration_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-177">[![Configuration > Customize Model](./media/configuration_customizemodel.png)](./media/configuration_customizemodel.png)</span></span>

5.  <span data-ttu-id="5b791-178">デモ データの再読み込みを促すメッセージが表示されたら、**はい**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-178">If you're prompted to reload the demo data, click **Yes**.</span></span>
6.  <span data-ttu-id="5b791-179">データが読み込みを完了したら、**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-179">When the data is finished loading, click **Close**.</span></span>
7.  <span data-ttu-id="5b791-180">ダッシュ ボードで、ナビゲーション バーを開き、**システム管理 &gt; 共通 &gt; 集計の測定を維持**に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b791-180">On the dashboard, open the navigation bar and navigate to **System Administration &gt; Common &gt; Maintain aggregate measurements**.</span></span> <span data-ttu-id="5b791-181">(手順 7 ～ 9 は、新しいリリースでは適用できません)</span><span class="sxs-lookup"><span data-stu-id="5b791-181">(Steps 7 to 9 are not applicable on newer releases)</span></span>
8.  <span data-ttu-id="5b791-182">**FMAggregateMeasurements** を選択し、アクション ペインで **今すぐ更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-182">Select **FMAggregateMeasurements**, and on the Action Pane, click **Refresh now**.</span></span>
9.  <span data-ttu-id="5b791-183">処理が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="5b791-183">Wait until the processing completes.</span></span> <span data-ttu-id="5b791-184">進行中の処理は、一連の移動するドットによってページの上部に示されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-184">The ongoing processing is indicated at the top of the page by a series of moving dots.</span></span> <span data-ttu-id="5b791-185">インジケータが消えて、**前回処理時刻** フィールドが更新されると、処理が完了します。</span><span class="sxs-lookup"><span data-stu-id="5b791-185">The processing is completed when the indicator disappears and the **Time Last Processed** field is updated.</span></span>

## <a name="open-the-fmrental-form-on-the-one-box-environment"></a><span data-ttu-id="5b791-186">1 ボックス環境で FMRental フォームを開く</span><span class="sxs-lookup"><span data-stu-id="5b791-186">Open the FMRental form on the one-box environment</span></span>
1.  <span data-ttu-id="5b791-187">VM で、Internet Explorer を開き、Dynamics AX アプリケーションのベース URL に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b791-187">In the VM, open Internet Explorer and navigate to the base URL of your Dynamics AX application.</span></span> <span data-ttu-id="5b791-188">詳細については、「[Microsoft Dynamics AX インスタンスにアクセス ](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b791-188">For more information, see [Access Microsoft Dynamics AX Instances](../dev-tools/access-instances.md).</span></span>
2.  <span data-ttu-id="5b791-189">求められた場合にログインします。</span><span class="sxs-lookup"><span data-stu-id="5b791-189">Sign in, if prompted.</span></span>
3.  <span data-ttu-id="5b791-190">**予約管理**タイルを検索し、予約管理ワークスペースを開くためそれをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-190">Find the **Reservation Management** tile and click to open the Reservation Management workspace.</span></span> 

    <span data-ttu-id="5b791-191">[![予約管理タイル](./media/reservationmanagementtile.jpg)](./media/reservationmanagementtile.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b791-191">[![Reservation management tile](./media/reservationmanagementtile.jpg)](./media/reservationmanagementtile.jpg)</span></span>

4.  <span data-ttu-id="5b791-192">**予約管理** ワークスペースが開いたら、**現在のレンタル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-192">When the **Reservation Management** workspace opens, click **Current rentals**.</span></span> 

    <span data-ttu-id="5b791-193">[![現在のレンタル](./media/reservationmanagementworkspace.jpg)](./media/reservationmanagementworkspace.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b791-193">[![Current rentals](./media/reservationmanagementworkspace.jpg)](./media/reservationmanagementworkspace.jpg)</span></span>

5.  <span data-ttu-id="5b791-194">これにより、グリッド ビューで **レンタル** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-194">This will open the **Rental** form in grid view.</span></span> 

    <span data-ttu-id="5b791-195">[![レンタル フォーム](./media/rentalform_customizemodel.png)](./media/rentalform_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-195">[![Rental form](./media/rentalform_customizemodel.png)](./media/rentalform_customizemodel.png)</span></span>

6.  <span data-ttu-id="5b791-196">**レンタル** フォームを実行した後、**オプション &gt; ビューの変更 &gt; ヘッダー** をクリックして、**ヘッダーの表示**を開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-196">After the **Rental** form loads, click **Options &gt; Change view &gt; Header** to open the **Header view**.</span></span>

    <span data-ttu-id="5b791-197">[![ヘッダーの表示](./media/headerview_customizemodel.png)](./media/headerview_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-197">[![Header view](./media/headerview_customizemodel.png)](./media/headerview_customizemodel.png)</span></span>

7.  <span data-ttu-id="5b791-198">**ヘッダーの表示**フォームを読み込んだら、下までスクロールし、**割引** タブを展開します。このタブはフリート管理モデルに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5b791-198">When the **Header view** form loads, scroll to the bottom and expand the **Discounts** tab. This tab isn't part of the Fleet Management model.</span></span> <span data-ttu-id="5b791-199">これは、**FMRental** フォームに対する拡張機能としてフリート管理拡張モデルでモデリングされています。</span><span class="sxs-lookup"><span data-stu-id="5b791-199">It has been modeled in the Fleet Management Extension Model as an extension to the **FMRental** form.</span></span>

    <span data-ttu-id="5b791-200">[![割引](./media/discounts_customizemodel.png)](./media/discounts_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-200">[![Discounts](./media/discounts_customizemodel.png)](./media/discounts_customizemodel.png)</span></span>

8.  <span data-ttu-id="5b791-201">割引を追加するために**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-201">Click **Add** to add a discount.</span></span>
9.  <span data-ttu-id="5b791-202">**得意先** 割引を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-202">Select the **Frequent Customer** discount, and then click **OK**.</span></span> <span data-ttu-id="5b791-203">選択した割引が **割引** グリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-203">The selected discount is added to the **Discounts** grid.</span></span> 

    <span data-ttu-id="5b791-204">[![得意先割引](./media/fcdiscount_customizemodel.png)](./media/fcdiscount_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-204">[![Frequent customer discount](./media/fcdiscount_customizemodel.png)](./media/fcdiscount_customizemodel.png)</span></span>

10. <span data-ttu-id="5b791-205">FactBox を開くには、ショートカット キー **Alt+F2** を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b791-205">Use the shortcut key, **Alt+F2** to open the FactBox.</span></span>
11. <span data-ttu-id="5b791-206">右側の**レンタル合計**情報ボックスを展開し、適用されるディスカウントの割引を表示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-206">Expand the **Rental total** FactBox on the right and view the discount savings that are applied.</span></span> 

    <span data-ttu-id="5b791-207">[![レンタル合計](./media/rentaltotal_customizemodel.png)](./media/rentaltotal_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-207">[![Rental total](./media/rentaltotal_customizemodel.png)](./media/rentaltotal_customizemodel.png)</span></span>

## <a name="overview-of-the-fleet-management-discount-extension-project"></a><span data-ttu-id="5b791-208">フリート管理割引の拡張プロジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="5b791-208">Overview of the Fleet management discount extension project</span></span>
<span data-ttu-id="5b791-209">このチュートリアルでは、**FleetManagementDiscounts** プロジェクトに**フリート管理拡張**という名前のモデルに属しているモデルの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5b791-209">In this tutorial, the **FleetManagementDiscounts** Project contains the model elements that belong to the model named **Fleet Management Extension**.</span></span> <span data-ttu-id="5b791-210">ここで、プロジェクト要素について調べ、学びます。</span><span class="sxs-lookup"><span data-stu-id="5b791-210">Here, you'll explore and learn about the project elements.</span></span>

### <a name="navigate-to-fmrentalextension-in-the-tree-designer"></a><span data-ttu-id="5b791-211">ツリー デザイナーで FMRental.Extension に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b791-211">Navigate to FMRental.Extension in the Tree Designer</span></span>

1.  <span data-ttu-id="5b791-212">Visual Studio の**ソリューション エクスプローラー**の **FleetManagement 割引**プロジェクトで、**ユーザー インターフェイス &gt; フォーム機能拡張**と展開します。</span><span class="sxs-lookup"><span data-stu-id="5b791-212">In the Visual Studio, in **Solution Explorer**, in the **FleetManagement Discounts** project, expand **User Interface &gt; Form Extensions**.</span></span> 

    <span data-ttu-id="5b791-213">[![ソリューション エクスプローラー](./media/solutionexplorer1_customizemodel.png)](./media/solutionexplorer1_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-213">[![Solution explorer](./media/solutionexplorer1_customizemodel.png)](./media/solutionexplorer1_customizemodel.png)</span></span>

    <span data-ttu-id="5b791-214">**FMRental.Extension** 要素は、2 つの新しいデータ ソースと新しいタブ コントロールを追加することによって **FMRental** フォームの機能を拡張する拡張要素です。</span><span class="sxs-lookup"><span data-stu-id="5b791-214">The **FMRental.Extension** element is an extension element that extends the functionality of the **FMRental** form by adding two new data sources and a new tab control.</span></span>
2.  <span data-ttu-id="5b791-215">**ソリューション エクスプローラー**で、**FMRental.Extension** をダブルクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-215">In **Solution Explorer**, double-click **FMRental.Extension** to open the designer.</span></span> <span data-ttu-id="5b791-216">次のイメージに示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-216">As the following image shows:</span></span>
    -   <span data-ttu-id="5b791-217">*斜体*のテキストで示されているデータ ソースはベースライン フォームで定義されているデータ ソースです。</span><span class="sxs-lookup"><span data-stu-id="5b791-217">The data sources shown in *italic* text are data sources defined in the baseline form.</span></span>
    -   <span data-ttu-id="5b791-218">**太字**で示されているデータ ソースは現在の拡張子で定義されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-218">The data sources shown in **bold** are the ones defined in the current extension.</span></span>

    <span data-ttu-id="5b791-219">デザイナーは、その拡張機能を含めて、モデル要素の統合ビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-219">The designer presents an integrated view of the model element, including its extensions.</span></span> <span data-ttu-id="5b791-220">読み取り専用ノードは斜体で表示さえｒますが、現在の拡張機能に属するノードはカスタマイズの種類を示す他の視覚的な記号と共に太字で表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-220">Read-only nodes are shown in italic text, while nodes that belong to the current extension are shown in bold, with other visual cues that indicate the type of customization.</span></span> 

    <span data-ttu-id="5b791-221">[![FMRentalExt\_CustomizeModel](./media/fmrentalext_customizemodel.png)](./media/fmrentalext_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-221">[![FMRentalExt\_CustomizeModel](./media/fmrentalext_customizemodel.png)](./media/fmrentalext_customizemodel.png)</span></span>

3.  <span data-ttu-id="5b791-222">デザイナーの検索ボックスに、次の図に示すように「e:」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b791-222">In the designer's search box, type 'e:' as shown in the image below.</span></span> <span data-ttu-id="5b791-223">現在のデザイナーがフィルター処理され、現在の拡張に属するノードのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-223">This filters the current designer to only show nodes that belong to the current extension.</span></span> 

    <span data-ttu-id="5b791-224">[![現在の拡張機能](./media/rentalext-e_customizemodel.png)](./media/rentalext-e_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-224">[![Current extension](./media/rentalext-e_customizemodel.png)](./media/rentalext-e_customizemodel.png)</span></span>

4.  <span data-ttu-id="5b791-225">また、'e:LineViewDiscounts' と入力してデザイナーをフィルター処理し、**LineViewDiscounts** という名前と一致し現在の拡張子に属するノードを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-225">You can also type 'e:LineViewDiscounts' to filter the designer to show nodes that match the name **LineViewDiscounts** and that belong to the current extension.</span></span> 

    <span data-ttu-id="5b791-226">[![LineViewDiscounts](./media/lineviewdiscounts_customizemodel.png)](./media/lineviewdiscounts_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-226">[![LineViewDiscounts](./media/lineviewdiscounts_customizemodel.png)](./media/lineviewdiscounts_customizemodel.png)</span></span>

5.  <span data-ttu-id="5b791-227">内容を確認するには、**LineViewDiscounts** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5b791-227">Expand the **LineViewDiscounts** node to see its contents.</span></span> 

    <span data-ttu-id="5b791-228">[![LineViewDiscounts ノードの展開](./media/expandlvdnode_customizemodel.png)](./media/expandlvdnode_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-228">[![Expand LineViewDiscounts node](./media/expandlvdnode_customizemodel.png)](./media/expandlvdnode_customizemodel.png)</span></span>

### <a name="open-the-fmrentalextension-xml-file-to-view-the-metadata"></a><span data-ttu-id="5b791-229">FMRental.Extension XML ファイルを開いてメタデータを表示</span><span class="sxs-lookup"><span data-stu-id="5b791-229">Open the FMRental.Extension XML file to view the metadata</span></span>

1.  <span data-ttu-id="5b791-230">**ソリューション エクスプローラー**で、FMRental.Extension フォーム拡張子をクリックしてから**プログラムから開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-230">In the **Solution Explorer**, right-click FMRental.Extension form extension, and then click **Open with**.</span></span>
2.  <span data-ttu-id="5b791-231">**プログラムから開く**ダイアログ ボックスで、**XML (テキスト) エディター**を選択してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-231">In the **Open with** dialog box, select **XML (Text) Editor**, and then click **OK**.</span></span>
3.  <span data-ttu-id="5b791-232">デザイナーを閉じるように求めるメッセージが表示されたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-232">When prompted to close the designer, click **Yes**.</span></span>
4.  <span data-ttu-id="5b791-233">対応するマイナス記号をクリックすると、**制御**および**データ ソース** ノードの子ノードが折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="5b791-233">Click the corresponding minus signs to collapse the child nodes of the **Controls** and **DataSources** nodes.</span></span> <span data-ttu-id="5b791-234">正しい結果については次の図を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b791-234">Refer to the following image for the correct result.</span></span> 

    <span data-ttu-id="5b791-235">[![レンタル コード](./media/fmrentalcode_customizemodel.png)](./media/fmrentalcode_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-235">[![Rental code](./media/fmrentalcode_customizemodel.png)](./media/fmrentalcode_customizemodel.png)</span></span> 

    <span data-ttu-id="5b791-236">XML ファイルには、**FMRental.Extension** 要素に関連付けられているメタデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5b791-236">The XML file contains the metadata associated with the **FMRental.Extension** element.</span></span> <span data-ttu-id="5b791-237">このファイルに、拡張機能の一部である 1 つのみのタブ ページ コントロールおよび 2 つのデータ ソースを説明するメタデータが含まれることがわかります。</span><span class="sxs-lookup"><span data-stu-id="5b791-237">You can see that this file contains metadata that describes only one tab page control and two data sources that are part of the extension.</span></span> <span data-ttu-id="5b791-238">基本フォームからのメタデータが含まれていないことを確認することもできます。</span><span class="sxs-lookup"><span data-stu-id="5b791-238">You can also see that it doesn't contain any metadata from the base form.</span></span>

### <a name="view-other-elements-in-the-fleet-management-discount-extension-project"></a><span data-ttu-id="5b791-239">フリート管理割引の拡張プロジェクトのその他の要素の表示</span><span class="sxs-lookup"><span data-stu-id="5b791-239">View other elements in the Fleet Management discount extension project</span></span>

<span data-ttu-id="5b791-240">**FleetManagement Discounts** プロジェクトには 2 つの新しいテーブル **FEDiscount** および **FERentalDiscountRelationTable** と、既存のフリート管理テーブル **FMRental** および **FMRentalCharge** への 2 つの拡張が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b791-240">The **FleetManagement Discounts** project contains two new tables, **FEDiscount** and **FERentalDiscountRelationTable**, and two extensions to existing Fleet Management tables, **FMRental** and **FMRentalCharge**.</span></span>

1.  <span data-ttu-id="5b791-241">**ソリューション エクスプローラー**の FleetManagement 割引で**データ モデル &gt; テーブル拡張機能 &gt; FMRental.Extension** をダブルクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-241">In **Solution Explorer**, in FleetManagement Discounts, double-click **Data Model &gt; Table Extensions &gt; FMRental.Extension** to open the designer.</span></span>
2.  <span data-ttu-id="5b791-242">**フィールド**ノードを展開し、拡張子に追加されたフィールド FEVehicleRateDiscount がベース FMRental テーブルに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b791-242">Expand the **Fields** node to see that this extension contains one added field, FEVehicleRateDiscount, to the base FMRental table.</span></span> 

    <span data-ttu-id="5b791-243">[![FEVehicleRateDiscount](./media/nodes_customizemodel.png)](./media/nodes_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-243">[![FEVehicleRateDiscount](./media/nodes_customizemodel.png)](./media/nodes_customizemodel.png)</span></span>

3.  <span data-ttu-id="5b791-244">同様に、デザイナーで **FMRentalChange.Extension** 要素を開いて、その内容を調べます。</span><span class="sxs-lookup"><span data-stu-id="5b791-244">Similarly, open the **FMRentalChange.Extension** element in the designer to explore its contents.</span></span>

### <a name="inspect-the-data-event-handlers"></a><span data-ttu-id="5b791-245">データ イベント ハンドラーの検査</span><span class="sxs-lookup"><span data-stu-id="5b791-245">Inspect the data event handlers</span></span>

<span data-ttu-id="5b791-246">**ソリューション エクスプローラー**の FleetManagement 割引プロジェクトで、**コード &gt; クラス &gt; FMRentalCharge\_Extension** をダブルクリックしてコード エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-246">In **Solution Explorer**, in the FleetManagement Discounts project, double-click **Code &gt; Classes &gt; FMRentalCharge\_Extension** to open the code editor.</span></span> 

<span data-ttu-id="5b791-247">[![FMRentalChargeCode](./media/fmrentalchargecode_customizemodel.png)](./media/fmrentalchargecode_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-247">[![FMRentalChargeCode](./media/fmrentalchargecode_customizemodel.png)](./media/fmrentalchargecode_customizemodel.png)</span></span> 

<span data-ttu-id="5b791-248">このクラスには、**FMRentalCharge** テーブルの**更新**および**挿入**イベントに登録するイベント ハンドラーの実装が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5b791-248">This class contains event handler implementations that subscribe to the **Updating** and **Inserting** events of the **FMRentalCharge** table.</span></span> <span data-ttu-id="5b791-249">Microsoft Dynamics AX では、テーブルおよび他の種類で発生する可能性のあるデータ イベントが導入されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-249">Microsoft Dynamics AX introduces data events that can occur on tables and other types.</span></span> <span data-ttu-id="5b791-250">基本 X++ コードをオーバーレイせずにビジネス ロジックを拡張するアプリケーションを有効にする、テーブルのデータ イベントを申し込むことができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-250">You can subscribe to data events of a table, enabling your application to extend business logic without overlayering base X++ code.</span></span> <span data-ttu-id="5b791-251">このチュートリアルの後半で、簡単にテーブル イベントをサブスクライブする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b791-251">Later in this tutorial, you'll see how easy it is to subscribe to table events.</span></span> <span data-ttu-id="5b791-252">**注記:** このクラスが拡張クラス (\_拡張子の接尾辞によって示される) であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b791-252">**Note:** Notice that this class is an extension class (indicated by the \_Extension suffix).</span></span> <span data-ttu-id="5b791-253">任意のクラスでイベント ハンドラーを作成することができます。このクラスは拡張クラスである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5b791-253">You can author event handlers in any class, this class does not need to be an extension class.</span></span> <span data-ttu-id="5b791-254">拡張子クラスは、拡張メソッドを作成するために必要です。</span><span class="sxs-lookup"><span data-stu-id="5b791-254">Extension classes are needed in order to create extension methods.</span></span> <span data-ttu-id="5b791-255">拡張メソッドの詳細については、[X++ デバッガーの機能](../dev-tools/new-x-debugger-features.md) 記事の「拡張メソッド」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5b791-255">For more details on extension methods, refer to the "Extension methods" section of the [X++ debugger features](../dev-tools/new-x-debugger-features.md) article.</span></span>

### <a name="view-the-plug-in-classes"></a><span data-ttu-id="5b791-256">プラグイン クラスの表示</span><span class="sxs-lookup"><span data-stu-id="5b791-256">View the plug-in classes</span></span>

<span data-ttu-id="5b791-257">前のセクションに示された **FMRentalCharge\_Extension** クラスのイベント ハンドラー コードでは、両方のイベント ハンドラーが **FMTotalsEngineBase::GetInstance** を呼び出してフリート管理計算エンジンの現在のインスタンスを取得することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5b791-257">In the event handler code of the **FMRentalCharge\_Extension** class shown in the previous section, notice that both event handlers call **FMTotalsEngineBase::GetInstance** to retrieve the current instance of the Fleet Management calculation engine.</span></span> <span data-ttu-id="5b791-258">計算エンジンは、プラグイン クラスを使用して実装されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-258">The calculation engines are implemented by using plug-in classes.</span></span> <span data-ttu-id="5b791-259">クラス ファクトリは、コンフィギュレーションまたはビジネス データに基づくプラグイン クラスの適切なインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b791-259">A class factory creates the appropriate instances of a plug-in class based on configuration or business data.</span></span>

1.  <span data-ttu-id="5b791-260">FMRentalCharge\_Extension.xpp を表示するコード エディター ウィンドウで、**GetInstance** を右クリックしてから**定義に移動**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-260">In the code editor window that displays FMRentalCharge\_Extension.xpp, right-click **GetInstance**, and then click **Go To Definition**.</span></span> <span data-ttu-id="5b791-261">これにより、抽象クラス **FMTotalsEngineBase** のコードが開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-261">This will open the code of the abstract class **FMTotalsEngineBase**.</span></span> <span data-ttu-id="5b791-262">この抽象クラスは**プラグインポイント**と呼ばれ、属性 \[Microsoft.Dynamics.AX.Platform.Extensibility.ExportInterfaceAttribute()\] に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="5b791-262">This abstract class is called a **plugin point** and it's associated with the following attribute: \[Microsoft.Dynamics.AX.Platform.Extensibility.ExportInterfaceAttribute()\]</span></span> 

    <span data-ttu-id="5b791-263">[![定義に移動](./media/godefinition_customizemodel.png)](./media/godefinition_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-263">[![Go to Definition](./media/godefinition_customizemodel.png)](./media/godefinition_customizemodel.png)</span></span> 

    <span data-ttu-id="5b791-264">プラグイン クラスは、抽象クラスやインターフェイスの拡張機能または実装を表します。</span><span class="sxs-lookup"><span data-stu-id="5b791-264">Plug-in classes represent extensions or implementations of abstract classes or interfaces.</span></span> <span data-ttu-id="5b791-265">プラグイン クラスは、そのメタデータとプラグイン ポイントを定義する属性に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5b791-265">Plug-in classes are associated with attributes defining their metadata and the plug-in point.</span></span> <span data-ttu-id="5b791-266">この例では、**FMTotalsEngineBase** プラグイン ポイントに関連付けられている 2 つのプラグイン クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="5b791-266">In this example, there are two plug-in classes associated with the **FMTotalsEngineBase** plug-in point.</span></span> <span data-ttu-id="5b791-267">基本計算エンジンは、プラグイン クラス **FMTotalsEngine** によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-267">The base calculation engine is defined by the plug-in class **FMTotalsEngine**.</span></span> <span data-ttu-id="5b791-268">プロジェクト **移行されたフリート管理 &gt; コード &gt; クラス** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-268">You can find it in the project **FleetManagement Migrated &gt; Code &gt; Classes**.</span></span> 

    <span data-ttu-id="5b791-269">[![FMTotalsEngineBase](./media/code1_customizemodel.png)](./media/code1_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-269">[![FMTotalsEngineBase](./media/code1_customizemodel.png)](./media/code1_customizemodel.png)</span></span> 

    <span data-ttu-id="5b791-270">割引計算エンジンは、プラグイン クラス **FEDiscountEngine** によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-270">The discount calculation engine is defined by the plug-in class **FEDiscountEngine**.</span></span> <span data-ttu-id="5b791-271">プロジェクト **フリート管理割引 &gt; コード &gt; クラス** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-271">You can find it in the project **FleetManagement Discounts &gt; Code &gt; Classes**.</span></span> 

    <span data-ttu-id="5b791-272">[![FEDiscountEngine](./media/code2_customizemodel.png)](./media/code2_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-272">[![FEDiscountEngine](./media/code2_customizemodel.png)](./media/code2_customizemodel.png)</span></span>

2.  <span data-ttu-id="5b791-273">**GetInstance** メソッドを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b791-273">Look at the **GetInstance** method.</span></span> <span data-ttu-id="5b791-274">このメソッドは、プラグイン ファクトリ **SysPluginFactory::Instance** を使用して、現在のプラグイン メタデータに基づいて現在の計算エンジンのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b791-274">It uses the plug-in factory **SysPluginFactory::Instance** to instantiate the current calculation engine based on current plug-in metadata.</span></span> <span data-ttu-id="5b791-275">プラグイン メタデータは、グローバル構成テーブルの **FMParameters** で指定されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-275">The plug-in metadata is specified in the global configuration table, **FMParameters**.</span></span> 

    <span data-ttu-id="5b791-276">[![FMParameters](./media/code3_customizemodel.png)](./media/code3_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-276">[![FMParameters](./media/code3_customizemodel.png)](./media/code3_customizemodel.png)</span></span> 

    <span data-ttu-id="5b791-277">Dynamics AX は、コンフィギュレーション可能なプラグイン クラスもサポートします。このクラスでは、クラスに関連付けられているプラグイン メタデータは開発時は未知であり、管理者がランタイム時にコンフィギュレーション可能です。</span><span class="sxs-lookup"><span data-stu-id="5b791-277">Dynamics AX also supports configurable plug-in classes where the plug-in metadata associate with the class isn't known at development time and is configurable at runtime by an administrator.</span></span> <span data-ttu-id="5b791-278">これは、このチュートリアルの対象ではありません。</span><span class="sxs-lookup"><span data-stu-id="5b791-278">This isn't in the scope of this tutorial.</span></span>

## <a name="create-additional-fleet-management-extensions"></a><span data-ttu-id="5b791-279">追加のフリート管理拡張子を作成する</span><span class="sxs-lookup"><span data-stu-id="5b791-279">Create additional Fleet Management extensions</span></span>
<span data-ttu-id="5b791-280">このセクションでは、Visual Studio ツールを使用して拡張機能を作成して操作する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-280">This section shows how you can use the Visual Studio tools to create and interact with extensions.</span></span>

### <a name="extend-the-fmvehicle-table"></a><span data-ttu-id="5b791-281">FMVehicle テーブルを拡張</span><span class="sxs-lookup"><span data-stu-id="5b791-281">Extend the FMVehicle Table</span></span>

1.  <span data-ttu-id="5b791-282">**ソリューション エクスプローラー**で、**FleetManagement 割引**プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b791-282">In **Solution Explorer**, select the **FleetManagement Discounts** project.</span></span>
2.  <span data-ttu-id="5b791-283">Visual studio の**アプリケーション エクスプローラー**で、**表示 &gt; アプリケーション エクスプローラー**をクリックして、FMVehicle という名前のテーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="5b791-283">In Visual studio, in **Application Explorer,** click **View &gt; Application Explorer**, and search for the table named FMVehicle.</span></span> <span data-ttu-id="5b791-284">フィルター バーに "FMVehicle type:Table" と入力し、**Enter** を押します。</span><span class="sxs-lookup"><span data-stu-id="5b791-284">Type "FMVehicle type:Table" in the filter bar and press **Enter**.</span></span> 

    <span data-ttu-id="5b791-285">[![FMVehicle の AppExplore 検索](./media/appexplorersmall_customizemodel.png)](./media/appexplorersmall_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-285">[![AppExplorer search for FMVehicle](./media/appexplorersmall_customizemodel.png)](./media/appexplorersmall_customizemodel.png)</span></span>

3.  <span data-ttu-id="5b791-286">**FMVehicle** を右クリックし、**拡張子の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-286">Right-click **FMVehicle**, and then click **Create extension**.</span></span> 

    <span data-ttu-id="5b791-287">[![AppExplorer 拡張機能の作成](./media/appexplorerlarge1_customizemodel.png)](./media/appexplorerlarge1_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-287">[![AppExplorer Create extension](./media/appexplorerlarge1_customizemodel.png)](./media/appexplorerlarge1_customizemodel.png)</span></span>

    <span data-ttu-id="5b791-288">これにより、**FMVehicle.Extension** という名前の **FleetManagement Discounts** プロジェクトに **FMVehicle** テーブルの拡張が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-288">This will create an extension of the **FMVehicle** table in the **FleetManagement Discounts** project named **FMVehicle.Extension**.</span></span> 

    <span data-ttu-id="5b791-289">[![FMVehicle.Extension](./media/expanddiscountsnode2_customizemodel.png)](./media/expanddiscountsnode2_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-289">[![FMVehicle.Extension](./media/expanddiscountsnode2_customizemodel.png)](./media/expanddiscountsnode2_customizemodel.png)</span></span>

4.  <span data-ttu-id="5b791-290">**ソリューション エクスプローラー**で、**FMVehicle.Extension** を右クリックしてから**プログラムから開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-290">In **Solution Explorer**, right-click **FMVehicle.Extension**, and then click **Open with**.</span></span> <span data-ttu-id="5b791-291">ダイアログ ボックスで **XML (テキスト) エディター**を選択してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-291">In the dialog box, select **XML (Text) Editor**, and then click **OK**.</span></span> <span data-ttu-id="5b791-292">**注記**: この拡張子ファイルは、データベースの **FMVehicle** テーブルのメタデータを含まない簡単なテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="5b791-292">**Note**: This extension file is simply a template that doesn't contain metadata from the base **FMVehicle** table.</span></span> <span data-ttu-id="5b791-293">拡張ファイルには拡張を定義するメタデータのみが常に含まれ、基本モデル要素からは何もありません。</span><span class="sxs-lookup"><span data-stu-id="5b791-293">An extension file will always contain only the metadata that defines the extension and nothing from the base model element.</span></span> 

    <span data-ttu-id="5b791-294">[![FMVehicle](./media/code4_customizemodel.png)](./media/code4_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-294">[![FMVehicle](./media/code4_customizemodel.png)](./media/code4_customizemodel.png)</span></span>

5.  <span data-ttu-id="5b791-295">XML エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b791-295">Close the XML editor.</span></span>
6.  <span data-ttu-id="5b791-296">**ソリューション エクスプローラー**で、**FMVehicle.Extension** をダブルクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-296">In **Solution Explorer**, double-click **FMVehicle.Extension** to open the designer.</span></span>
7.  <span data-ttu-id="5b791-297">**フィールド** を右クリックし、新しい整数型フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5b791-297">Right-click **Fields** and add a new integer field.</span></span> <span data-ttu-id="5b791-298">フィールドの名前を **NumberOfCylinders** に変更します。</span><span class="sxs-lookup"><span data-stu-id="5b791-298">Change the name of the field to **NumberOfCylinders**.</span></span>
8.  <span data-ttu-id="5b791-299">**プロパティ** ウィンドウで、新しいフィールドの**ラベル** プロパティを **NumberofCylinders** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5b791-299">In the **Properties** window, set the **Label** property of the new field to **NumberofCylinders**.</span></span>
9.  <span data-ttu-id="5b791-300">**NumberOfCylinders** フィールドを **AutoReport** フィールド グループにドラッグ アンド ドロップし、ベース テーブルのフィールド グループに展開します。</span><span class="sxs-lookup"><span data-stu-id="5b791-300">Drag-and-drop the **NumberOfCylinders** field into the **AutoReport** field group to extend the field group of the base table.</span></span> 

    <span data-ttu-id="5b791-301">[![NumberOfCylinders\_CustomizeModel](./media/numberofcylinders_customizemodel.png)](./media/numberofcylinders_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-301">[![NumberOfCylinders\_CustomizeModel](./media/numberofcylinders_customizemodel.png)](./media/numberofcylinders_customizemodel.png)</span></span>

10. <span data-ttu-id="5b791-302">FMVehicle.Extension を保存します。</span><span class="sxs-lookup"><span data-stu-id="5b791-302">Save FMVehicle.Extension.</span></span>
11. <span data-ttu-id="5b791-303">**イベント**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5b791-303">Expand the **Events** node.</span></span> <span data-ttu-id="5b791-304">**イベント** ノードには、テーブルが公開するすべてのイベントが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-304">The **Events** node lists all events that the table exposes.</span></span> <span data-ttu-id="5b791-305">これには、フレームワークによって定義されたイベントと、アプリケーション開発者によって定義されたデリゲート メソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5b791-305">This includes events that are defined by the framework, and delegate methods that are defined by application developers.</span></span> 

    <span data-ttu-id="5b791-306">[![イベント ノード](./media/eventsnode_customizemodel.png)](./media/eventsnode_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-306">[![Events node](./media/eventsnode_customizemodel.png)](./media/eventsnode_customizemodel.png)</span></span>

    <span data-ttu-id="5b791-307">**注記**: テーブルのイベント、フォームイベント、フォーム データ ソース イベント、フォーム コントロール イベントなど、異なるフレームワーク イベントが、さまざまなタイプの要素とサブ要素のデザイナーに公開されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-307">**Note**: Different framework events are exposed on the designers of many types of element and sub-elements, like table events, form events, form data source events, and form control events.</span></span>
12. <span data-ttu-id="5b791-308">onValidatedWrite を右クリックし、**イベント ハンドラー メソッドをコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b791-308">Right-click onValidatedWrite, and then select **Copy event handler method**.</span></span> 

    <span data-ttu-id="5b791-309">[![onValidateWrite](./media/onvalidatewrite_customizemodel.png)](./media/onvalidatewrite_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-309">[![onValidateWrite](./media/onvalidatewrite_customizemodel.png)](./media/onvalidatewrite_customizemodel.png)</span></span> 

    <span data-ttu-id="5b791-310">このステップは、イベント ハンドラー メソッドのシグネチャをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="5b791-310">This step copies the event handler method signature to the clipboard.</span></span>
13. <span data-ttu-id="5b791-311">**FMVehicleEventHandlers** という名前の新しいクラスを **FleetManagement Discounts** プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="5b791-311">Add a new class named **FMVehicleEventHandlers** to the **FleetManagement Discounts** project.</span></span>
14. <span data-ttu-id="5b791-312">**ソリューション エクスプローラー**で、**FEVehicleEventHandlers** をダブルクリックしてコード エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="5b791-312">In **Solution Explorer**, double-click **FEVehicleEventHandlers** to open the code editor.</span></span>
15. <span data-ttu-id="5b791-313">右クリックし、手順 12 にコピーしたイベント ハンドラー メソッドを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="5b791-313">Right-click and paste the event handler method that you copied in step 12.</span></span>

        Class FMVehicleEventHandlers
        {
            /// <summary>
            ///
            /// </summary>
            /// <param name="sender"></param>
            /// <param name="e"></param>
            [DataEventHandler(tableStr(FMVehicle), DataEventType::ValidatedWrite)]
            public static void FMVehicle_onValidatedWrite(Common sender, DataEventArgs e)
            {
            }
        }



16. <span data-ttu-id="5b791-314">次のコードを **FMVehicle\_onValidatedWrite** イベント ハンドラーに挿入します。</span><span class="sxs-lookup"><span data-stu-id="5b791-314">Insert the following code into the **FMVehicle\_onValidatedWrite** event handler.</span></span> <span data-ttu-id="5b791-315">このコードは、シリンダの数が 8 を超えることができないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="5b791-315">This code validates that the number of cylinders can't be greater than 8.</span></span>

           [DataEventHandler(tableStr(FMVehicle), DataEventType::ValidatedWrite)]
            public static void FMVehicle_onValidatedWrite(Common sender, DataEventArgs e)
            {
                ValidateEventArgs validateArgs = e as ValidateEventArgs;
                FMVehicle vehicle = sender as FMVehicle;
                boolean result = validateArgs.parmValidateResult();

                if (vehicle.NumberOfCylinders > 8)
                {
                    result = checkFailed("Invalid number of cylinders.");
                    validateArgs.parmValidateResult(result);
                }
            }

17. <span data-ttu-id="5b791-316">FMVehicleEventHandlers クラスを保存 **ヒント**: モデルの任意のクラスで、イベント ハンドラーを貼り付けて定義できます。</span><span class="sxs-lookup"><span data-stu-id="5b791-316">Save FMVehicleEventHandlers class **Tip**: You can paste and define your event handlers in any class of your model.</span></span> <span data-ttu-id="5b791-317">クラス FMVehicleEventHandlers は、例としてのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-317">The class FMVehicleEventHandlers is used only as an example.</span></span>

### <a name="extend-the-fmvehicle-form"></a><span data-ttu-id="5b791-318">FMVehicle フォームを拡張</span><span class="sxs-lookup"><span data-stu-id="5b791-318">Extend the FMVehicle Form</span></span>

<span data-ttu-id="5b791-319">次に、**FleetManagement 割引**プロジェクトの **FMVehicle** フォーム拡張機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b791-319">Next, add an extension to the **FMVehicle** form in the **FleetManagement Discounts** project.</span></span> <span data-ttu-id="5b791-320">最初に、**ソリューション エクスプローラー**でこのプロジェクトを選択することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b791-320">First, be sure to select this project in **Solution Explorer**.</span></span>

1.  <span data-ttu-id="5b791-321">**アプリケーション エクスプローラー**を使用して **FMVehicle** という名前のフォームを検索するには、**アプリケーション エクスプローラー**のフィルタ バーに *FMVehicle タイプ:フォーム* を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b791-321">Use **Application Explorer** to find the form named **FMVehicle**, and in the **Application Explorer** filter bar, enter the *FMVehicle type:form*.</span></span>
2.  <span data-ttu-id="5b791-322">フォームを右クリックし、**拡張子の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-322">Right-click the form, and then click **Create extension**.</span></span>
3.  <span data-ttu-id="5b791-323">下に示すように、**NumberOfCylinders** という名前の新しい整数コントロールを **Attributes2** グループ コントロールに追加します。</span><span class="sxs-lookup"><span data-stu-id="5b791-323">Add a new integer control named **NumberOfCylinders** to the **Attributes2** group control as shown below.</span></span> <span data-ttu-id="5b791-324">このコントロールは、**デザイン&gt; タブ &gt; TabPageDetails &gt; TabHeader &gt; DetailsDetails &gt; Attributes2** を展開すると見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5b791-324">You can find this control by expanding **Design &gt; Tab &gt; TabPageDetails &gt; TabHeader &gt; DetailsDetails &gt; Attributes2**.</span></span> 

    <span data-ttu-id="5b791-325">[![シリンダの数](./media/numcylinteger_customizemodel.png)](./media/numcylinteger_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-325">[![Number of Cylinders](./media/numcylinteger_customizemodel.png)](./media/numcylinteger_customizemodel.png)</span></span>

4.  <span data-ttu-id="5b791-326">次のように新しいコントロールをプロパティ ウィンドウの **NumberOfCylinders** データ フィールドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="5b791-326">Bind the new control to the **NumberOfCylinders** data field in the properties window as follows.</span></span> 

    <span data-ttu-id="5b791-327">[![バインド コントロール](./media/datafield_customizemodel.png)](./media/datafield_customizemodel.png)</span><span class="sxs-lookup"><span data-stu-id="5b791-327">[![Bind control](./media/datafield_customizemodel.png)](./media/datafield_customizemodel.png)</span></span>

5.  <span data-ttu-id="5b791-328">FMVehicle.Extension を保存し、プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b791-328">Save FMVehicle.Extension and build the project.</span></span>

### <a name="test-your-extensions"></a><span data-ttu-id="5b791-329">拡張機能をテスト</span><span class="sxs-lookup"><span data-stu-id="5b791-329">Test your extensions</span></span>

1.  <span data-ttu-id="5b791-330">**ソリューション エクスプローラー**で、**FleetManagement 割引**を右クリックしてから、**スタートアップ プロジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-330">In **Solution Explorer**, right-click **FleetManagement Discounts**, and then click **Set as StartUp project**.</span></span>
2.  <span data-ttu-id="5b791-331">同様に、FleetManagement 割引で、スタートアップ オブジェクトとして **FMVehicle.Extension** フォームを設定します。</span><span class="sxs-lookup"><span data-stu-id="5b791-331">Similarly, in FleetManagement Discounts, set the **FMVehicle.Extension** form as the startup object.</span></span>
3.  <span data-ttu-id="5b791-332">**Ctrl+F5** キーを押してデバッグなしで開始するか、**デバッグ** メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="5b791-332">Press **Ctrl+F5** to start without debugging, or use the **Debug** menu.</span></span>
4.  <span data-ttu-id="5b791-333">**車両**フォームが開いた後、車両を選択して詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-333">After the **Vehicles** form opens, select a vehicle to view its details.</span></span>
5.  <span data-ttu-id="5b791-334">**詳細**タブを展開し、新しい**シリンダ番号**フィールドを通知します。</span><span class="sxs-lookup"><span data-stu-id="5b791-334">Expand the **Details** tab and notice the new **Number of Cylinders** field.</span></span> 

    <span data-ttu-id="5b791-335">[![シリンダー数の詳細](./media/nbofcyls.jpg)](./media/nbofcyls.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b791-335">[![Details with number of cylinders](./media/nbofcyls.jpg)](./media/nbofcyls.jpg)</span></span>

6.  <span data-ttu-id="5b791-336">アクション ウィンドウで、**編集**をクリックして**シリンダの数**フィールドの値を 12 に変更します。</span><span class="sxs-lookup"><span data-stu-id="5b791-336">In the Action Pane, click **Edit**, and change the value in the **Number of cylinders** field to 12.</span></span>
7.  <span data-ttu-id="5b791-337">アクション ウィンドウで、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-337">In the Action Pane, click **Save**.</span></span>
8.  <span data-ttu-id="5b791-338">検証エラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="5b791-338">Notice the validation error.</span></span>
9.  <span data-ttu-id="5b791-339">有効なシリンダ数を 9 より小さく入力し、次に新しい値を保存します。</span><span class="sxs-lookup"><span data-stu-id="5b791-339">Enter a valid number of cylinders, less than 9, and then save the new value.</span></span>

## <a name="experiment-with-event-handlers-on-form-controls"></a><span data-ttu-id="5b791-340">フォーム コントロールでのイベント ハンドラーを試す</span><span class="sxs-lookup"><span data-stu-id="5b791-340">Experiment with event handlers on form controls</span></span>
<span data-ttu-id="5b791-341">これは、既存のコントロールにイベント ハンドラー メソッドを追加する例です。</span><span class="sxs-lookup"><span data-stu-id="5b791-341">This is an example of adding event handler methods on existing controls.</span></span>

1.  <span data-ttu-id="5b791-342">**FMRental** フォーム デザイナーで **AddLine** コマンド ボタン コントロールを検索し、**OnClicked** イベントを右クリックし、次に選択**イベント ハンドラーのメソッドをコピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b791-342">Find the **AddLine** command button control in the **FMRental** form designer, right-click the **OnClicked** event, and select **Copy event handler method**.</span></span>

    <span data-ttu-id="5b791-343">[![明細行 OnClicked イベントを追加します。](./media/addlineonclickedevent.jpg)](./media/addlineonclickedevent.jpg)</span><span class="sxs-lookup"><span data-stu-id="5b791-343">[![Add line OnClicked event](./media/addlineonclickedevent.jpg)](./media/addlineonclickedevent.jpg)</span></span>

2.  <span data-ttu-id="5b791-344">フリート管理拡張モデルのクラスでイベント ハンドラー メソッドを貼り付け、X++ コードを追加して実装します。</span><span class="sxs-lookup"><span data-stu-id="5b791-344">Paste the event handler method in a class of the Fleet Management Extension model and add X++ code to implement it.</span></span>

<!-- -->

    /// <summary>
    ///
    /// </summary>
    /// <param name="sender"></param>
    /// <param name="e"></param>
    [FormControlEventHandler(formControlStr(FMRental, AddLine), FormControlEventType::Clicked)]
    public static void AddLine_OnClicked(FormControl sender, FormControlEventArgs e)
    {
    }

-   <span data-ttu-id="5b791-345">AddLine\_OnClicked イベント ハンドラーを実装すると、**sender** パラメーターを使用して、ボタン コントロール インスタンスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5b791-345">When implementing the AddLine\_OnClicked event handler, you can access the button control instance using the **sender** parameter.</span></span>

<!-- -->

    FormButtonControl button = sender as FormButtonControl;

-   <span data-ttu-id="5b791-346">親フォームや、変数のいずれかにアクセスする場合は、この例では、**FormRun** インスタンスとデータ ソースのいずれかにアクセスする方法が示されています。</span><span class="sxs-lookup"><span data-stu-id="5b791-346">If you need to access the parent form or any of its variables, this example shows how to access the **FormRun** instance and one of its data sources.</span></span>

<!-- -->

    FormRun fr;
    fr = sender.formRun();
    var frDs = fr.dataSource("FMRental");

## <a name="experiment-with-event-handlers-on-form-data-sources"></a><span data-ttu-id="5b791-347">フォーム データ ソースでのイベント ハンドラーを試す</span><span class="sxs-lookup"><span data-stu-id="5b791-347">Experiment with event handlers on form data sources</span></span>
<span data-ttu-id="5b791-348">テーブル、フォーム コントロールおよびその他の要素タイプと同じように、フォーム データ ソースとフォーム データ ソース フィールドはフレームワーク レベルのイベントを提供します。</span><span class="sxs-lookup"><span data-stu-id="5b791-348">Just like tables, form controls and other element types, form data sources and form data source fields provide framework-level events.</span></span> <span data-ttu-id="5b791-349">次の例は、フォーム データ ソースの ValidatingWrite イベントまたはフォーム データ ソースの検証イベントを使用して FMRental フォームのユーザー入力を検証する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5b791-349">The following example shows how you can use the ValidatingWrite event on a form data source or the Validating event on a form data source field to validate user input on the FMRental form.</span></span> <span data-ttu-id="5b791-350">この機能は、Platform Update 7 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="5b791-350">This functionality is available as of Platform Update 7.</span></span>

```
    /// <summary>
    /// When saving a new rental, prevent setting the start mileage on the FMRental form to a value that is equal to 1
    /// </summary>
    [FormDataSourceEventHandler(formDataSourceStr(FMRental, FMRental), FormDataSourceEventType::ValidatingWrite)]
    public static void FMRental_OnValidatingWrite(FormDataSource sender, FormDataSourceEventArgs e)
    {
        var datasource = sender as FormDataSource;
        var args = e as FormDataSourceCancelEventArgs;
        if (args != null && datasource != null)
        {
            FMRental record = datasource.cursor() as FMRental;
            if (record.recId == 0)
            {
                if(record.startmileage == 1)
                {
                    boolean doCancel = !checkFailed("Start Mileage = 1 is not allowed");
                    args.cancel(doCancel);
                }
            }
        }
    }
```
```
    /// <summary>
    /// Prevent changing the start mileage field on the FMRental form to a value that is equal to 1
    /// </summary>
    [FormDataFieldEventHandler(formDataFieldStr(FMRental, FMRental, StartMileage), FormDataFieldEventType::Validating)]
    public static void StartMileage_OnValidating(FormDataObject sender, FormDataFieldEventArgs e)
    {
        var dataObject = sender as FormDataObject;
        var args = e as FormDataFieldCancelEventArgs;
        if (args != null && dataObject != null)
        {
            var datasource = dataObject.datasource() as FormDataSource;
            if (datasource != null)
            {
                FMRental record = datasource.cursor() as FMRental;
                if (record.RecId > 0)
                {
                    if (record.StartMileage == 1 )
                    {
                        boolean doCancel = !checkFailed("Start Mileage = 1 is not allowed");
                        args.cancel(doCancel);
                    }
                }
            }
        }
    }
```
## <a name="experiment-with-table-extension-display-and-edit-methods"></a><span data-ttu-id="5b791-351">テーブル 拡張子ディスプレイを試し、メソッドを編集</span><span class="sxs-lookup"><span data-stu-id="5b791-351">Experiment with table extension display and edit methods</span></span>
<span data-ttu-id="5b791-352">拡張メソッドを使用すると、新しい表示を作成してテーブルを拡張し、オーバーレイ X++ コード無しでテーブルのメソッドを編集します (拡張メソッドは、\_ 拡張子の接尾語という名のクラスに属する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="5b791-352">Extension methods enable you to extend tables by creating new display and edit methods on these tables without over-layering X++ code (Extension method must belong to a class named with an \_Extension suffix).</span></span> <span data-ttu-id="5b791-353">たとえば、このクラスは、CupHoldersDisplay と呼ばれる拡張表示メソッドを使用して、FMVehicle テーブルを拡張する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="5b791-353">For example, this class shows how you can extend the FMVehicle table with an extension display method named CupHoldersDisplay.</span></span>

    public static class FMVehicle_Extension
    {
       public static display int CupHoldersDisplay(FMVehicle vehicle)
       {
         return 7;
       }
    }

<span data-ttu-id="5b791-354">フォームまたはフォームの拡張機能では、以下の画像に示すように、「Data Source = FMVehicle」および「Data method ="FMVehicle\_Extension::CupHoldersDisplay」を設定することによってこの表示メソッドにコントロールをバインドできます。</span><span class="sxs-lookup"><span data-stu-id="5b791-354">On a form or form extension, you can bind a control to this display method by setting "Data Source = FMVehicle" and "Data method = "FMVehicle\_Extension::CupHoldersDisplay" as the image below shows.</span></span>

![拡張表示メソッド](./media/extensiondisplaymethod.jpg)

## <a name="create-a-fleet-extension-package-for-deployment"></a><span data-ttu-id="5b791-356">展開のためのフリート拡張パッケージを作成する</span><span class="sxs-lookup"><span data-stu-id="5b791-356">Create a Fleet extension package for deployment</span></span>
<span data-ttu-id="5b791-357">拡張機能をテスト環境、運用前環境、運用環境などの別の環境に展開するには、展開パッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b791-357">To deploy your extension to another environment, for example, a test, pre-production or production environment, you must create a deployment package.</span></span>

1.  <span data-ttu-id="5b791-358">Visual Studio の **Dynamics AX** メニューで、**配置**をポイントしてから、**配置パッケージの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-358">In Visual Studio, on the **Dynamics AX** menu, point to **Deploy**, and then click **Create Deployment Package**.</span></span> 

    ![配置パッケージの作成](./media/createdeploymentpackage_customizemodel.png)

2.  <span data-ttu-id="5b791-360">**フリート管理拡張** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5b791-360">Select the **Fleet Management Extension** check box.</span></span>
3.  <span data-ttu-id="5b791-361">**パッケージ ファイルの場所**テキスト ボックスに、「c:\FMLab」と入力します。</span><span class="sxs-lookup"><span data-stu-id="5b791-361">In the **Package file location** text box, enter "c:\FMLab".</span></span>
4.  <span data-ttu-id="5b791-362">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b791-362">Click **Create**.</span></span> <span data-ttu-id="5b791-363">これにより、フリート管理拡張パッケージを含む展開パッケージが作成されます。</span><span class="sxs-lookup"><span data-stu-id="5b791-363">This will create a deployment package that contains the Fleet management Extension package.</span></span>


<a name="additional-resources"></a><span data-ttu-id="5b791-364">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5b791-364">Additional resources</span></span>
--------

[<span data-ttu-id="5b791-365">FMLab サンプル コードをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="5b791-365">Download FMLab sample code</span></span>](https://github.com/Microsoft/FMLab)



