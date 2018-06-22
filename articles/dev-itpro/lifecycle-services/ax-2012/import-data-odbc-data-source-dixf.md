---
title: "ODBC データ ソースからのデータのインポート (AX 2012)"
description: "Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、ODBC データ ソースからのデータを Microsoft Dynamics AX 2012 にインポートすることができます。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18821
ms.assetid: 3eb200bd-666e-424c-8bd0-9528da4ba880
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b74c99fbfb2b6bb19808c7bd12c04a74ba9e5a9a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="import-data-from-an-odbc-data-source-ax-2012"></a><span data-ttu-id="d93a5-103">ODBC データ ソースからのデータのインポート (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="d93a5-103">Import data from an ODBC data source (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d93a5-104">Microsoft Dynamics AX 2012 のデータのインポート/エクスポート フレームワークを使用すると、ODBC データ ソースからのデータを Microsoft Dynamics AX 2012 にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-104">You can use the Microsoft Dynamics AX 2012 Data Import/Export Framework to import data from an ODBC data source into Microsoft Dynamics AX 2012.</span></span> 

<span data-ttu-id="d93a5-105">このチュートリアルでは、次の作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-105">This walkthrough illustrates the following tasks:</span></span>

-   <span data-ttu-id="d93a5-106">SQL Server ソース データを作成する</span><span class="sxs-lookup"><span data-stu-id="d93a5-106">Create a SQL Server data source</span></span>
-   <span data-ttu-id="d93a5-107">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="d93a5-107">Define the format of your source data</span></span>
-   <span data-ttu-id="d93a5-108">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="d93a5-108">Define a processing group</span></span>
-   <span data-ttu-id="d93a5-109">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="d93a5-109">Process data from source to staging</span></span>
-   <span data-ttu-id="d93a5-110">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="d93a5-110">Validate the data in staging</span></span>
-   <span data-ttu-id="d93a5-111">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="d93a5-111">Process data from staging to target</span></span>
-   <span data-ttu-id="d93a5-112">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="d93a5-112">Validate the data in target</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d93a5-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="d93a5-113">Prerequisites</span></span>
<span data-ttu-id="d93a5-114">このチュートリアルを完了するには、次のものが必要です。</span><span class="sxs-lookup"><span data-stu-id="d93a5-114">To complete this walkthrough you will need:</span></span>

-   <span data-ttu-id="d93a5-115">Microsoft Dynamics AX 2012、Microsoft Dynamics AX 2012 R2、または Microsoft Dynamics AX 2012 R3。</span><span class="sxs-lookup"><span data-stu-id="d93a5-115">Microsoft Dynamics AX 2012, Microsoft Dynamics AX 2012 R2, or Microsoft Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="d93a5-116">データのインポート/エクスポート フレームワーク</span><span class="sxs-lookup"><span data-stu-id="d93a5-116">Data Import/Export Framework</span></span>

## <a name="create-a-sql-server-data-source"></a><span data-ttu-id="d93a5-117">SQL Server ソース データを作成する</span><span class="sxs-lookup"><span data-stu-id="d93a5-117">Create a SQL Server data source</span></span>
1.  <span data-ttu-id="d93a5-118">Microsoft SQL Server Management Studio を開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-118">Open Microsoft SQL Server Management Studio.</span></span>
2.  <span data-ttu-id="d93a5-119">次のクエリを実行し、データベースの作成 (DMFLEgacyDB)、テーブルの作成 (VendorEntity)、テーブルへのデータ入力を行います。</span><span class="sxs-lookup"><span data-stu-id="d93a5-119">Run the following query to create a database (DMFLEgacyDB), create a table (VendorEntity), and populate the table.</span></span>

         USE [master] GO /****** Database [DMFLegacyDB] ******/ CREATE DATABASE [DMFLegacyDB]GOUSE [DMFLegacyDB]
        GO
         /****** Table [dbo].[VendorEntity] ******/
         CREATE TABLE [dbo].[VendorEntity]
        (
         [ACCOUNTNUM][nvarchar](20)default(N'') NOT NULL,
         [FIRSTNAME][nvarchar](25)default(N'') NOT NULL,
         [MIDDLENAME][nvarchar](25)default(N'') NOT NULL,
         [LASTNAME][nvarchar](25)default(N'') NOT NULL,
         [LANGUAGEID][nvarchar](7)NOT NULL,
         [VENDGROUP][nvarchar](20)NULL,
         [CURRENCY][nvarchar](10)NULL,
         [PartyType][nvarchar](10)NULL
         ) 
        ON [PRIMARY]
        GO
        INSERT [dbo].[VendorEntity] ([ACCOUNTNUM], [FIRSTNAME], [MIDDLENAME], [LANGUAGEID], [LASTNAME], [VENDGROUP], [CURRENCY], [PartyType])
         VALUES (N'V001', N'001 first', N'001 middle', N'en-us', N'001 last', N'10', N'USD', N'Person')
        INSERT [dbo].[VendorEntity] ([ACCOUNTNUM], [FIRSTNAME], [MIDDLENAME], [LANGUAGEID], [LASTNAME], [VENDGROUP], [CURRENCY], [PartyType])
         VALUES (N'V002', N'002 first', N'002 middle', N'en-us', N'002 last', N'20', N'USD', N'Person')

## <a name="create-an-odbc-data-source-to-connect-to-the-sql-server-database"></a><span data-ttu-id="d93a5-120">SQL Server データベースを作成して、ODBC データ ソース に接続する</span><span class="sxs-lookup"><span data-stu-id="d93a5-120">Create an ODBC data source to connect to the SQL Server database</span></span>
1.  <span data-ttu-id="d93a5-121">Microsoft Dynamics AX を実行しているコンピューターで、**管理ツール** &gt; **データ ソース (ODBC)** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-121">On the computer that is running Microsoft Dynamics AX, open **Administrative Tools** &gt; **Data Source (ODBC)**.</span></span>
2.  <span data-ttu-id="d93a5-122">SQL Server のユーザー DSN を作成し、名前を **DMFLegacyDB DSN** にして、データベースの作成に使用した SQL Server のインスタンスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-122">Create a User DSN for SQL Server, name it **DMFLegacyDB-DSN**, and select the instance of SQL Server that you used to create the database.</span></span>
3.  <span data-ttu-id="d93a5-123">**次へ**をクリックし、適切な値を選択して SQL Server インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-123">Click **Next**, and select the appropriate values to connect to the SQL Server instance.</span></span> <span data-ttu-id="d93a5-124">一般に、データのインポート/エクスポート フレームワーク サービスを実行しているアカウントと接続することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-124">In general, we recommend that you connect with the account that you are running the Data Import/Export Framework service as.</span></span> <span data-ttu-id="d93a5-125">詳細については、[データ ソースの管理](http://msdn.microsoft.com/en-us/library/windows/desktop/ms712362(v=vs.85).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d93a5-125">For more information, see [Managing Data Sources](http://msdn.microsoft.com/en-us/library/windows/desktop/ms712362(v=vs.85).aspx).</span></span>
4.  <span data-ttu-id="d93a5-126">**次へ**をクリックし、既定のデータベースの **DMFLegacyDB** を選択し、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-126">Click **Next**, select **DMFLegacyDB** for the default database, and then click **Finish**.</span></span>

## <a name="define-the-format-of-your-source-data"></a><span data-ttu-id="d93a5-127">ソース データのフォーマットを形式する</span><span class="sxs-lookup"><span data-stu-id="d93a5-127">Define the format of your source data</span></span>
1.  <span data-ttu-id="d93a5-128">**データのインポート/エクスポート フレームワーク** &gt; **設定** &gt; **ソース データ形式**を開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-128">Open **Data Import/Export Framework** &gt; **Setup** &gt; **Source data formats**.</span></span>
2.  <span data-ttu-id="d93a5-129">**新規**をクリックし、名前と説明を入力します。次に、**タイプ** フィールドの **ODBC** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-129">Click **New**, enter a name and description, and then in the **Type** field, select **ODBC**.</span></span>
3.  <span data-ttu-id="d93a5-130">**一般**タブの、**DSN** タイプで、**ユーザー DSN** を選択し、**DSN 場所**の場合は、**クライアント**を選択し、**DMFLegacyDB-DSN** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-130">On the **General** tab, for **DSN** type, select **User DSN**, for **DSN location**, select **Client**, and then select **DMFLegacyDB-DSN**.</span></span> <span data-ttu-id="d93a5-131">接続文字列が入力されます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-131">The connection string will populate.</span></span>
4.  <span data-ttu-id="d93a5-132">**検証**をクリックして、ログオンしているアカウントが ODBC 接続にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-132">Click **Validate** to verify that the account that you are logged on as has access to the ODBC connection.</span></span>

## <a name="define-a-processing-group"></a><span data-ttu-id="d93a5-133">処理グループの定義</span><span class="sxs-lookup"><span data-stu-id="d93a5-133">Define a processing group</span></span>
1.  <span data-ttu-id="d93a5-134">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、**新規**をクリックして新しい処理グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-134">In **Data Import/Export Framework** &gt; **Common** &gt; **Processing group**, click **New** to create a new processing group.</span></span>
2.  <span data-ttu-id="d93a5-135">グループの名前と説明を設定します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-135">Set the group name and description.</span></span>
3.  <span data-ttu-id="d93a5-136">処理グループに含めるエンティティを選択するには、**エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-136">Click **Entities** to select the entities to include in the processing group.</span></span>
4.  <span data-ttu-id="d93a5-137">**処理グループのエンティティの選択**フォームで、**新規**をクリックしてから、**エンティティ**に対して**仕入先**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-137">In the **Select entities for processing group** form, click **New**, and then, for **Entity name**, select **Vendor**.</span></span>
5.  <span data-ttu-id="d93a5-138">**エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-138">Click **Entities**.</span></span> <span data-ttu-id="d93a5-139">**処理グループのエンティティの選択** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-139">The **Select entities for processing group** dialog box opens.</span></span>
6.  <span data-ttu-id="d93a5-140">**クエリ** ボックスに次のクエリを入力します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-140">In the **Query** box, enter the following query:</span></span>

        select * from VendorEntity

7.  <span data-ttu-id="d93a5-141">**ソース マッピングの生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-141">Click **Generate source mapping**.</span></span> <span data-ttu-id="d93a5-142">オプション: マッピングを必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-142">Optional: Modify the mapping as needed.</span></span>
8.  <span data-ttu-id="d93a5-143">**検証**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-143">Click **Validate**.</span></span>
9.  <span data-ttu-id="d93a5-144">**ソース ファイルのプレビュー**をクリックし、**処理グループのエンティティの選択**フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-144">Click **Preview source file**, and then close the **Select entities for processing group** form.</span></span>

## <a name="process-data-from-source-to-staging"></a><span data-ttu-id="d93a5-145">ソースからステージングにデータを処理</span><span class="sxs-lookup"><span data-stu-id="d93a5-145">Process data from source to staging</span></span>
1.  <span data-ttu-id="d93a5-146">**処理グループ** フォームで、作成した仕入先グループを選択して**ステージング データの取得**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-146">In the **Processing group** form, select the vendor group that you created, and click **Get staging data**.</span></span> <span data-ttu-id="d93a5-147">**ステージング データ ジョブに対するジョブ ID の作成** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-147">The **Create a job ID for the staging data job** dialog box opens.</span></span>
2.  <span data-ttu-id="d93a5-148">既定では、ジョブの ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-148">By default, an ID for the job is generated.</span></span> <span data-ttu-id="d93a5-149">必要に応じて、IDを変更して説明を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-149">You can optionally modify the ID and add a description.</span></span> <span data-ttu-id="d93a5-150">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-150">Click **OK**.</span></span>
3.  <span data-ttu-id="d93a5-151">**ステージング データ実行** フォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-151">The **Staging data execution** form opens.</span></span>
4.  <span data-ttu-id="d93a5-152">**ソースからステージングにデータを取得**フォームで、**OK** をクリックしてすぐに実行します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-152">In the **Get data from source to staging** form, click **OK** to run immediately.</span></span> <span data-ttu-id="d93a5-153">ソース データはステージング テーブルにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-153">The source data is copied to the staging tables.</span></span>

## <a name="validate-the-data-in-staging"></a><span data-ttu-id="d93a5-154">ステージングのデータの検証</span><span class="sxs-lookup"><span data-stu-id="d93a5-154">Validate the data in staging</span></span>
1.  <span data-ttu-id="d93a5-155">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、**実行履歴**をクリックして実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-155">In **Data Import/Export Framework** &gt; **Common** &gt; **Processing group**, click **Execution history**, and select the job that ran.</span></span>
2.  <span data-ttu-id="d93a5-156">**ステージング データの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-156">Click **View staging data**.</span></span>
3.  <span data-ttu-id="d93a5-157">ODBC ソースと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-157">Review the staging data to validate that it matches the ODBC source.</span></span>
4.  <span data-ttu-id="d93a5-158">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-158">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>

## <a name="process-data-from-staging-to-target"></a><span data-ttu-id="d93a5-159">ステージングからターゲットにデータを処理</span><span class="sxs-lookup"><span data-stu-id="d93a5-159">Process data from staging to target</span></span>
1.  <span data-ttu-id="d93a5-160">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**で、操作する処理グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-160">In **Data Import/Export Framework** &gt; **Common** &gt; **Processing group**, select the processing group to work with.</span></span>
2.  <span data-ttu-id="d93a5-161">**データをターゲットにコピー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-161">Click **Copy data to target**.</span></span> <span data-ttu-id="d93a5-162">**実行するジョブ ID を選択** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-162">The **Select a job ID to run** dialog box opens.</span></span>
3.  <span data-ttu-id="d93a5-163">ジョブを選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-163">Select a job and click **OK**.</span></span> <span data-ttu-id="d93a5-164">**ターゲット データ実行** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-164">The **Target data execution** dialog box opens.</span></span>
4.  <span data-ttu-id="d93a5-165">**実行**をクリックし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d93a5-165">Click **Run**, and then click **OK**.</span></span> <span data-ttu-id="d93a5-166">データはターゲット エンティティにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d93a5-166">The data is copied to the target entities.</span></span>

## <a name="validate-the-data-in-target"></a><span data-ttu-id="d93a5-167">ターゲットのデータの検証</span><span class="sxs-lookup"><span data-stu-id="d93a5-167">Validate the data in target</span></span>
<span data-ttu-id="d93a5-168">ODBC ソースからの顧客仕入先データが次のいずれかの方法で表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-168">Verify that the vendor data from the ODBC source is displayed in either of the following ways:</span></span>

-   <span data-ttu-id="d93a5-169">ステージング データの表示:</span><span class="sxs-lookup"><span data-stu-id="d93a5-169">View staging data:</span></span>
    1.  <span data-ttu-id="d93a5-170">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **処理グループ**、**実行履歴**、**ステージング データの表示**とクリックしてから実行したジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-170">**Data Import/Export Framework** &gt; **Common** &gt; **Processing group**, click **Execution history**, click **View staging data** and then select the job that ran.</span></span>
    2.  <span data-ttu-id="d93a5-171">ODBC ソースと一致することを検証するステージング データを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-171">Review the staging data to validate that it matches the ODBC source.</span></span>
    3.  <span data-ttu-id="d93a5-172">**すべて検証**をクリックして、関連するすべての参照データが正しくシステムに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-172">Click **Validate all** to verify that all the related reference data is correct and present in the system.</span></span>
-   <span data-ttu-id="d93a5-173">ODBC ソースからの顧客データが **買掛金勘定** &gt; **共通** &gt; **仕入先** &gt; **すべての仕入先** フォームに表示されるようになったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93a5-173">Verify that the customer data from the ODBC source is now displayed in **Accounts payable** &gt; **Common** &gt; **Vendor** &gt; **All Vendors** form.</span></span>





