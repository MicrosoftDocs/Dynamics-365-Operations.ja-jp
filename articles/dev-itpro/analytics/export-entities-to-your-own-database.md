---
title: "自分のデータベースの持ち込み"
description: "このトピックでは、エンティティを 独自の Azure SQL データベースにエクスポートする方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8b72aca3893254c1bf53048f2d6931ded82d3942
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="bring-your-own-database"></a><span data-ttu-id="cab70-103">自分のデータベースの持ち込み</span><span class="sxs-lookup"><span data-stu-id="cab70-103">Bring your own database</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="cab70-104">このトピックでは、管理者がデータ エンティティを Microsoft Dynamics 365 for Finance and Operations から 独自の Microsoft Azure SQL データベースにエクスポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cab70-104">This topic explains how administrators can export data entities from Microsoft Dynamics 365 for Finance and Operations into their own Microsoft Azure SQL database.</span></span> <span data-ttu-id="cab70-105">この機能は、*自分のデータベースの持ち込み* (BYOD) とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="cab70-105">This feature is also known as *bring your own database* (BYOD).</span></span> <span data-ttu-id="cab70-106">BYOD 機能は、Microsoft Dynamics AX でプラットフォーム更新プログラム 2 (2016 年 8 月) によってリリースされました。</span><span class="sxs-lookup"><span data-stu-id="cab70-106">The BYOD feature was released in Microsoft Dynamics AX with platform update 2 (August 2016).</span></span> <span data-ttu-id="cab70-107">マイナーな改良およびバグ修正は、後続のプラットフォーム更新プログラムに含まれています。</span><span class="sxs-lookup"><span data-stu-id="cab70-107">Minor improvements and bug fixes have been included in subsequent platform updates.</span></span>

<span data-ttu-id="cab70-108">BYOD 機能により、管理者は、独自のデータベースを構成し、Finance and Operations で使用できる 1 つまたは複数のデータ エンティティをそこにエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="cab70-108">The BYOD feature lets administrators configure their own database, and then export one or more data entities that are available in Finance and Operations into it.</span></span> <span data-ttu-id="cab70-109">(現時点では、1,700 以上のデータ エンティティが使用可能です。) 具体的には、この機能により次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-109">(Currently, more than 1,700 data entities are available.) Specifically, this feature lets you complete these tasks:</span></span>

- <span data-ttu-id="cab70-110">エンティティ データを Finance and Operations からエクスポートできる 1 つ以上の SQL データベースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cab70-110">Define one or more SQL databases that you can export entity data from Finance and Operations into.</span></span>
- <span data-ttu-id="cab70-111">すべてのレコード (*完全にプッシュ*) または変更されたレコードのみ (*差分プッシュ*) を、エキスポートします。</span><span class="sxs-lookup"><span data-stu-id="cab70-111">Export either all the records (*full push*) or only the records that have changed (*incremental push*).</span></span>
- <span data-ttu-id="cab70-112">定期的なエクスポートを有効にするには、Finance and Operations バッチ フレームワークの豊富なスケジューリング機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="cab70-112">Use the rich scheduling capabilities of the Finance and Operations batch framework to enable periodic exports.</span></span>
- <span data-ttu-id="cab70-113">トランザクション SQL (T-SQL) を使用してエンティティ データベースにアクセスし、さらにテーブルを追加してデータベースを拡張します。</span><span class="sxs-lookup"><span data-stu-id="cab70-113">Access the entity database by using Transact-SQL (T-SQL), and even extend the database by adding more tables.</span></span>


## <a name="entity-store-or-byod"></a><span data-ttu-id="cab70-114">エンティティ格納または BYOD か</span><span class="sxs-lookup"><span data-stu-id="cab70-114">Entity store or BYOD?</span></span>

<span data-ttu-id="cab70-115">「[Microsoft Power BI 統合についてのブログ投稿](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)」のシリーズに従った場合、エンティティ格納に馴染み深くなります。</span><span class="sxs-lookup"><span data-stu-id="cab70-115">If you followed the series of [blog posts about Microsoft Power BI integration](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/), you will be familiar with Entity store.</span></span> <span data-ttu-id="cab70-116">エンティティ格納は、Finance and Operations に含まれている運用データ ウェアハウスです。</span><span class="sxs-lookup"><span data-stu-id="cab70-116">Entity store is the operational data warehouse that is included with Finance and Operations.</span></span> <span data-ttu-id="cab70-117">エンティティ格納では、Power BI の実稼働レポートの組み込み統合を提供します。</span><span class="sxs-lookup"><span data-stu-id="cab70-117">Entity store provides built-in integration of operational reports with Power BI.</span></span> <span data-ttu-id="cab70-118">Finance and Operations に組み込まれている既存のレポートと分析ワークスペースは、エンティティ格納を使用します。</span><span class="sxs-lookup"><span data-stu-id="cab70-118">Ready-made reports and analytical workspaces that are built into Finance and Operations use Entity store.</span></span> <span data-ttu-id="cab70-119">Finance and Operations の環境のデータを使用して Power BI レポートを作成する場合は、エンティティ格納を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-119">If you write Power BI reports by using data in your Finance and Operations environment, you should use Entity store.</span></span>

<span data-ttu-id="cab70-120">ただし、次のシナリオでは BYOD 機能をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cab70-120">However, the BYOD feature is recommended for the following scenarios:</span></span>

- <span data-ttu-id="cab70-121">Finance and Operations からご自身のデータ ウェアハウスにデータをエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-121">You must export data from Finance and Operations into your own data warehouse.</span></span>
- <span data-ttu-id="cab70-122">Power BI 以外の分析ツールを使用し、これらのツールはデータに対して T-SQL アクセスを必要とします。</span><span class="sxs-lookup"><span data-stu-id="cab70-122">You use analytical tools other than Power BI, and those tools require T-SQL access to data.</span></span>
- <span data-ttu-id="cab70-123">他のシステムとのバッチ統合を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-123">You must perform batch integration with other systems.</span></span>

> [!NOTE]
> <span data-ttu-id="cab70-124">Finance and Operations には、生産データベースへの T-SQL 接続を使用できません。</span><span class="sxs-lookup"><span data-stu-id="cab70-124">Finance and Operations doesn't allow T-SQL connections to the production database.</span></span> <span data-ttu-id="cab70-125">Finance and Operations の以前のバージョンをアップグレードする場合、データベースへの直接的な T-SQL アクセスを必要とする統合ソリューションがある場合は、BYOD は推奨するアップグレード パスになります。</span><span class="sxs-lookup"><span data-stu-id="cab70-125">If you're upgrading from a previous version of Finance and Operations, and you have integration solutions that require direct T-SQL access to the database, BYOD is the recommended upgrade path.</span></span>

<span data-ttu-id="cab70-126">Finance and Operations の顧客は、エンティティ格納または BYOD のいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-126">As a customer of Finance and Operations, you can use either Entity store or BYOD.</span></span> <span data-ttu-id="cab70-127">使用可能な既定の操作レポートは、埋め込み Power BI とエンティティ格納を利用します。</span><span class="sxs-lookup"><span data-stu-id="cab70-127">The default operational reports that are available take advantage of embedded Power BI and Entity store.</span></span> <span data-ttu-id="cab70-128">最初の選択として、既定の業務レポートを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cab70-128">We recommend that you use our default operational reports as your first choice.</span></span> <span data-ttu-id="cab70-129">また、要件に合わせて、既成のオペレーション レポートを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-129">You can also extend the ready-made operational reports to meet your requirements.</span></span> <span data-ttu-id="cab70-130">BYOD を必要に応じて利用する補足的なオプションと見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-130">You should consider BYOD a complementary option that you use as you require.</span></span>

## <a name="creating-a-sql-database"></a><span data-ttu-id="cab70-131">SQL データベースを作成しています</span><span class="sxs-lookup"><span data-stu-id="cab70-131">Creating a SQL database</span></span>

<span data-ttu-id="cab70-132">エンティティのエクスポート オプションをコンフィギュレーションして BYOD 機能を使用する前に、Azure ポータルを使用して SQL データベースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-132">Before you can configure the entity export option and use the BYOD feature, you must create a SQL database by using Azure portal.</span></span>

<span data-ttu-id="cab70-133">1 ボックス開発環境では、ローカルの Microsoft SQL Server データベースでデータベースを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-133">For one-box development environments, you can create a database in the local Microsoft SQL Server database.</span></span> <span data-ttu-id="cab70-134">ただし、このデータベースは、開発およびテスト目的でのみ使用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-134">However, this database should be used only for development and testing purposes.</span></span> <span data-ttu-id="cab70-135">実稼働環境については、SQL データベースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-135">For production environments, you must create a SQL database.</span></span>

<span data-ttu-id="cab70-136">また、データベースにサインインするには、SQL ユーザー アカウントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-136">You should also create a SQL user account for sign-in to the database.</span></span> <span data-ttu-id="cab70-137">サーバー名、データベース名、および SQL ユーザー ID とパスワードを記述します。</span><span class="sxs-lookup"><span data-stu-id="cab70-137">Write down the server name, database name, and the SQL user ID and password.</span></span> <span data-ttu-id="cab70-138">この情報は、次のセクションで、エンティティのエクスポート オプションをコンフィギュレーションするときに使用します。</span><span class="sxs-lookup"><span data-stu-id="cab70-138">You will use this information when you configure the entity export option in the next section.</span></span>

<span data-ttu-id="cab70-139">ビジネス インテリジェンス (BI) ツールとの統合に BYOD 機能を使用している場合、SQL プレミアム データベースの作成を検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-139">If you're using the BYOD feature for integration with a business intelligence (BI) tool, you should consider creating a SQL premium database.</span></span> <span data-ttu-id="cab70-140">Premium データベースでは、クラスター化された縦棒ストア インデックス (CCI) がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="cab70-140">Premium databases support clustered columnstore indexes (CCIs).</span></span> <span data-ttu-id="cab70-141">CCI は、分析およびレポートのワークロードで一般的な読取りクエリのパフォーマンスを向上させるメモリ内インデックスです。</span><span class="sxs-lookup"><span data-stu-id="cab70-141">CCIs are in-memory indexes that improve the performance of read queries that are typical in analytical and reporting workloads.</span></span> <span data-ttu-id="cab70-142">ステージング データベースへのデータのエクスポート、または一般的な統合目的で BYOD 機能を使用している場合、標準的なデータベースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-142">If you're using the BYOD feature to export data into a staging database or for general integration purposes, you can use a standard database.</span></span>

## <a name="configuring-the-entity-export-option"></a><span data-ttu-id="cab70-143">エンティティのエクスポート オプションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cab70-143">Configuring the entity export option</span></span>

1. <span data-ttu-id="cab70-144">Finance and Operations クライアントを起動し、**データの管理** ワークスペースで、**データベースへのエンティティ エクスポートの構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="cab70-144">Start the Finance and Operations client, and then, in the **Data management** workspace, select the **Configure Entity export to database** tile.</span></span>
2. <span data-ttu-id="cab70-145">いくつかのデータベースを構成した場合、一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-145">If you've configured any databases, a list is shown.</span></span> <span data-ttu-id="cab70-146">それ以外の場合、新しいデータベースをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-146">Otherwise, you must configure a new database.</span></span> <span data-ttu-id="cab70-147">この場合、**新規**を選択して、新しいデータベースに一意の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="cab70-147">In this case, select **New**, and then enter a unique name and a description for the new database.</span></span> <span data-ttu-id="cab70-148">複数のデータベースにエンティティをエクスポートできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cab70-148">Note that you can export entities into multiple databases.</span></span>
3. <span data-ttu-id="cab70-149">次の形式で、接続文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="cab70-149">Enter the connection string in the following format:</span></span>

    <span data-ttu-id="cab70-150">データ ソース =&lt; 論理サーバー名 &gt;、1433。最初のカタログ =&lt; DB名 &gt;。統合セキュリティ = False。ユーザー ID =&lt; SQL ユーザー ID &gt; 。パスワード =&lt; パスワード &gt;</span><span class="sxs-lookup"><span data-stu-id="cab70-150">Data Source=&lt;logical server name&gt;,1433; Initial Catalog=&lt;your DB name&gt;; Integrated Security=False; User ID=&lt;SQL user ID&gt;; Password=&lt;password&gt;</span></span>

    <span data-ttu-id="cab70-151">この接続文字列では、論理サーバー名を **nnnn.database.windows.net** のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-151">In this connection string, the logical server name should resemble **nnnn.database.windows.net**.</span></span> <span data-ttu-id="cab70-152">Azure ポータル内の論理サーバー名を検索できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-152">You should be able to find the logical server name in Azure portal.</span></span> <span data-ttu-id="cab70-153">次の図は、接続文字列の例を示します。</span><span class="sxs-lookup"><span data-stu-id="cab70-153">The following illustration shows an example of a connection string.</span></span>
    
    ![新しいレコード ページの接続文字列](media/NewRecord.png)

4. <span data-ttu-id="cab70-155">**検証** を選択し、接続が正常に行われたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="cab70-155">Select **Validate**, and make sure that the connection is successful.</span></span>

    - <span data-ttu-id="cab70-156">**クラスター化された列ストア インデックスを作成** オプションは、Finance and Operations からコピーされるエンティティの CCI を定義することで選択したクエリの出力先データベースを最適化します。</span><span class="sxs-lookup"><span data-stu-id="cab70-156">The **Create clustered column store indexes** option optimizes the destination database for selected queries by defining CCIs for entities that are copied from Finance and Operations.</span></span> <span data-ttu-id="cab70-157">ただし、CCI は現在 SQL プレミアム データベースでのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="cab70-157">However, CCIs are currently supported only on SQL premium databases.</span></span> <span data-ttu-id="cab70-158">したがって、このオプションを有効にするには、SQL プレミアム データベースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-158">Therefore, to enable this option, you must create a SQL premium database.</span></span>
    - <span data-ttu-id="cab70-159">**ターゲット データベースでトリガーを有効にする** オプションは、ターゲット データベースで SQL トリガーを有効にするためにエクスポート ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="cab70-159">The **Enable triggers in target database** option sets export jobs to enable SQL triggers in the target database.</span></span> <span data-ttu-id="cab70-160">このオプションを使用すると、レコードを挿入した後に開始する必要がある操作を調整するために、ダウンストリーム プロセスをトリガーにフックできます。</span><span class="sxs-lookup"><span data-stu-id="cab70-160">This option lets you hook downstream processes into the trigger to orchestrate actions that must be started after records have been inserted.</span></span> <span data-ttu-id="cab70-161">1 つのトリガーは一括挿入の操作ごとにサポートされています。</span><span class="sxs-lookup"><span data-stu-id="cab70-161">One trigger is supported per bulk insert operation.</span></span> <span data-ttu-id="cab70-162">一括挿入のサイズは、データ管理フレームワークの **Maximum insert commit size** パラメーターによって決まります。</span><span class="sxs-lookup"><span data-stu-id="cab70-162">The size of the bulk insert is determined by the **Maximum insert commit size** parameter in the Data management framework.</span></span> 

<span data-ttu-id="cab70-163">BYOD からデータを読み取るレポート システムのシナリオでは、Finance and Operations からの同期の実行中に、レポート システムが BYOD から一貫したデータを取得することを確認するという課題が常にあります。</span><span class="sxs-lookup"><span data-stu-id="cab70-163">For scenarios in which reporting systems read data from BYOD, there is always the challenge of ensuring that the reporting systems get consistent data from BYOD while the sync from Finance and Operations is in progress.</span></span> <span data-ttu-id="cab70-164">BYOD プロセスで作成されたステージング テーブルから報告システムが直接読み取りしないようにすることにより、この結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-164">You can achieve this result by not having the reporting systems read directly from the staging tables created by the BYOD process.</span></span> <span data-ttu-id="cab70-165">ステージング テーブルは、データが Finance and Operations インスタンスから同期されている間データを保持するため、常に変化します。</span><span class="sxs-lookup"><span data-stu-id="cab70-165">The staging tables hold the data while data is being synced from the Finance and Operations instance and hence will be constantly changing.</span></span> <span data-ttu-id="cab70-166">SQL トリガー機能を使用して、Finance and Operations からのデータ同期が完了した時点を判断し、下流のレポーティング システムに通知します。</span><span class="sxs-lookup"><span data-stu-id="cab70-166">Use the SQL trigger feature to determine when the data sync from Finance and Operations has been completed, and then hydrate the downstream reporting systems .</span></span>

<span data-ttu-id="cab70-167">検証に合格すると、次の図に示すように、エンティティのエクスポートに向けてコンフィギュレーションされたデータベースがデータベースのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-167">When the validation is passed, the database that you configured for entity export appears in lists of databases, as shown in the following illustration.</span></span>

   ![エンティティ エクスポートのデータベース](media/e3bcecdb0ff1532d890915903b378c60.png)

<span data-ttu-id="cab70-169">メニュー上で **公開** オプションを選択することにより、1 つまたは複数のエンティティを新しいデータベースに公開することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="cab70-169">You can now publish one or more entities to the new database by selecting the **Publish** option on the menu.</span></span>

### <a name="publishing-the-entity-schema-to-the-database"></a><span data-ttu-id="cab70-170">エンティティ スキーマをデータベースに公開</span><span class="sxs-lookup"><span data-stu-id="cab70-170">Publishing the entity schema to the database</span></span>

<span data-ttu-id="cab70-171">**発行** ページは、いくつかのシナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="cab70-171">The **Publish** page enables several scenarios:</span></span>

- <span data-ttu-id="cab70-172">データベースに新しいエンティティを公開します。</span><span class="sxs-lookup"><span data-stu-id="cab70-172">Publish new entities to the database.</span></span>
- <span data-ttu-id="cab70-173">以前に公開されたエンティティをデータベースから削除します。</span><span class="sxs-lookup"><span data-stu-id="cab70-173">Delete previously published entities from the database.</span></span> <span data-ttu-id="cab70-174">(たとえば、スキーマを再作成することができます。)</span><span class="sxs-lookup"><span data-stu-id="cab70-174">(For example, you might want to re-create the schema.)</span></span>
- <span data-ttu-id="cab70-175">Finance and Operations における公開されたエンティティとエンティティ スキーマとを比較する。</span><span class="sxs-lookup"><span data-stu-id="cab70-175">Compare published entities with the entity schema in Finance and Operations.</span></span> <span data-ttu-id="cab70-176">(たとえば、新しいフィールドを後で Finance and Operations に追加する場合、フィールドをデータベース スキーマと比較できます。)</span><span class="sxs-lookup"><span data-stu-id="cab70-176">(For example, if new fields are added to Finance and Operations later, you can compare the fields with your database schema.)</span></span>
- <span data-ttu-id="cab70-177">データの差分更新を可能にする変更追跡機能をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="cab70-177">Configure change tracking functionality that enables incremental updates of your data.</span></span>

<span data-ttu-id="cab70-178">次のセクションでは、各オプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cab70-178">The following sections discuss each option.</span></span>

#### <a name="publish"></a><span data-ttu-id="cab70-179">パブリッシュ</span><span class="sxs-lookup"><span data-stu-id="cab70-179">Publish</span></span>

<span data-ttu-id="cab70-180">**発行** オプションは、ターゲット データベースにエンティティ データベース スキーマを定義します。</span><span class="sxs-lookup"><span data-stu-id="cab70-180">The **Publish** option defines the entity database schema on the destination database.</span></span> <span data-ttu-id="cab70-181">1 つまたは複数のエンティティを選択してから、**公開** オプションを選択すると、バッチ ジョブが開始します。</span><span class="sxs-lookup"><span data-stu-id="cab70-181">When you select one or more entities, and then select the **Publish** option, a batch job is started.</span></span> <span data-ttu-id="cab70-182">このジョブは、出力先データベースにエンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="cab70-182">This job creates the entities in the destination database.</span></span> <span data-ttu-id="cab70-183">データベース定義ジョブが完了すると、メッセージが表示されます。このメッセージには、右上のベル記号を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="cab70-183">When the database definition job is completed, you receive a message, which you can access by using the bell symbol in the upper right.</span></span>

<span data-ttu-id="cab70-184">実際のデータの更新は、データをエクスポートするときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-184">The actual data update occurs when you export data.</span></span> <span data-ttu-id="cab70-185">この時点では、スキーマを作成するだけです。</span><span class="sxs-lookup"><span data-stu-id="cab70-185">At this point, you're just creating the schema.</span></span>

#### <a name="drop-entity"></a><span data-ttu-id="cab70-186">エンティティの削除</span><span class="sxs-lookup"><span data-stu-id="cab70-186">Drop entity</span></span>

<span data-ttu-id="cab70-187">**エンティティを削除** オプションは、出力先のデータベースからデータとエンティティ定義を削除します。</span><span class="sxs-lookup"><span data-stu-id="cab70-187">The **Drop entity** option deletes the data and the entity definition from the destination database.</span></span>

#### <a name="compare-source-names"></a><span data-ttu-id="cab70-188">ソース名の比較</span><span class="sxs-lookup"><span data-stu-id="cab70-188">Compare source names</span></span>

<span data-ttu-id="cab70-189">**ソース名を比較** オプションでは、ターゲットのエンティティ スキーマを Finance and Operations 内のエンティティ スキーマと比較することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-189">The **Compare source names** option lets you compare the entity schema in the destination with the entity schema in Finance and Operations.</span></span> <span data-ttu-id="cab70-190">このオプションは、バージョン管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-190">This option is used for version management.</span></span> <span data-ttu-id="cab70-191">また、出力先テーブルから不要な列を削除するためにこのオプションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-191">You can also use this option to remove any unwanted columns from the destination table.</span></span>

#### <a name="configure-change-tracking"></a><span data-ttu-id="cab70-192">変更追跡のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cab70-192">Configure change tracking</span></span>

<span data-ttu-id="cab70-193">変更の追跡は、SQL Server および SQL データベースで提供される機能です。</span><span class="sxs-lookup"><span data-stu-id="cab70-193">Change tracking is a feature that is provided in SQL Server and SQL Database.</span></span> <span data-ttu-id="cab70-194">変更追跡を使用すると、データベースでテーブルに加えられた変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-194">Change tracking enables the database to track changes that are made on tables.</span></span> <span data-ttu-id="cab70-195">変更の追跡を使用して、Finance and Operations でトランザクションが実行されるときにテーブルに加えられた変更を識別します。</span><span class="sxs-lookup"><span data-stu-id="cab70-195">The system uses change tracking to identify changes that are made to tables as transactions are performed in Finance and Operations.</span></span>

<span data-ttu-id="cab70-196">**発行** ページの **変更の追跡** オプションでは、基になるエンティティの変更の追跡方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-196">The **Change tracking** option on the **Publish** page lets you configure how changes are tracked on the underlying entity.</span></span>

![基礎となるエンティティの変更追跡](media/8918ed89bcc966252727af5a1b75e0fb.png)

<span data-ttu-id="cab70-198">次のテーブルでは、使用可能な変更追跡オプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cab70-198">The following table describes the change tracking options that are available.</span></span>

| <span data-ttu-id="cab70-199">オプション</span><span class="sxs-lookup"><span data-stu-id="cab70-199">Option</span></span>               | <span data-ttu-id="cab70-200">説明</span><span class="sxs-lookup"><span data-stu-id="cab70-200">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="cab70-201">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="cab70-201">Enable primary table</span></span> | <span data-ttu-id="cab70-202">エンティティは複数のテーブルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-202">An entity consists of several tables.</span></span> <span data-ttu-id="cab70-203">エンティティの主テーブルに加えられたすべての変更を追跡するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cab70-203">Select this option to track all changes that are made to the primary table of the entity.</span></span> <span data-ttu-id="cab70-204">プライマリ テーブルに変更を加えると、対応するレコードが出力先データベースに挿入されるか、またはそのデータベース内で更新されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-204">When changes are made to the primary table, the corresponding record is inserted into or updated in the destination database.</span></span> <span data-ttu-id="cab70-205">エンティティ全体からのデータは出力先テーブルに書き込まれますが、プライマリ テーブルが変更された場合にのみ、システムの挿入または更新オプションがトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="cab70-205">Although data from the whole entity is written to the destination table, the system triggers the insert or update option only when the primary table is modified.</span></span> |
| <span data-ttu-id="cab70-206">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="cab70-206">Enable entire entity</span></span> | <span data-ttu-id="cab70-207">エンティティのすべての変更を追跡するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cab70-207">Select this option to track all changes to the entity.</span></span> <span data-ttu-id="cab70-208">(これらの変更は、エンティティを構成するすべてのテーブルへの変更を含みます。) エンティティへの変更を加えるときに、対応する更新が宛先に対して行われます。</span><span class="sxs-lookup"><span data-stu-id="cab70-208">(These changes include changes to all the tables that make up the entity.) When changes are made to the entity, corresponding updates are made to the destination.</span></span> |
| <span data-ttu-id="cab70-209">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="cab70-209">Enable custom query</span></span>  | <span data-ttu-id="cab70-210">このオプションを使用すると、開発者は、システムが変更を評価するために実行するカスタム クエリを提供できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-210">This option lets a developer provide a custom query that the system runs to evaluate changes.</span></span> <span data-ttu-id="cab70-211">このオプションは、選択したフィールドのセットのみから変更を追跡するという複雑な要件がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="cab70-211">This option is useful when you have a complex requirement to track changes from only a selected set of fields.</span></span> <span data-ttu-id="cab70-212">エクスポートされるエンティティが入れ子になったビューの階層を使用して構築されたときも、このオプションを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-212">You can also select this option when the entities that will be exported were built by using a hierarchy of nested views.</span></span> <span data-ttu-id="cab70-213">詳細については、[カスタム クエリを使用してエンティティの変更追跡を有効にする](../data-entities/entity-change-track.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cab70-213">For more information, see [Enable change tracking for an entity by using a custom query](../data-entities/entity-change-track.md).</span></span> |

<span data-ttu-id="cab70-214">追跡変更機能の操作については、Finance and Operations データベース内の**変更追跡**オプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-214">For the change tracking functionality to work, you must enable the **Change tracking** option in the Finance and Operations database.</span></span> <span data-ttu-id="cab70-215">このオプションは、既定で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="cab70-215">This option is enabled by default.</span></span>

<span data-ttu-id="cab70-216">出力先のデータベースに存在するエンティティを再発行する場合、システムでは、既存のデータが新しい操作が原因で削除されることを警告されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-216">If you republish an entity that exists in the destination database, the system warns you that existing data will be deleted because of the new operation.</span></span>

<span data-ttu-id="cab70-217">発行操作を確認すると、システムがスキーマをデータベースに発行し、その操作が完了すると通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="cab70-217">When you confirm the publish operation, the system publishes the schema to the database, and you're notified when the operation is completed.</span></span>

<span data-ttu-id="cab70-218">**公開**ページで**公開済のみを表示**オプションを選択することにより、指定した出力先データベースに公開されたエンティティのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-218">By selecting the **Show published only** option on the **Publish** page, you can show only the entities that were published to a given destination database.</span></span> <span data-ttu-id="cab70-219">発行機能は、データベース内のエンティティ スキーマを作成します。</span><span class="sxs-lookup"><span data-stu-id="cab70-219">The Publish function creates the entity schema in the database.</span></span> <span data-ttu-id="cab70-220">データベースに移動して、対応するインデックスとともに、作成されたテーブル スキーマを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-220">You can navigate to the database and see the table schemas that were created, together with corresponding indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="cab70-221">現在、データベースに複合エンティティをエクスポートするのに BYOD を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="cab70-221">Currently, you can't use BYOD to export composite entities into a database.</span></span> <span data-ttu-id="cab70-222">複合エンティティの各エンティティをエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-222">You must export each entity in the composite entity.</span></span>

## <a name="exporting-data-into-your-database"></a><span data-ttu-id="cab70-223">データベースへのエクスポート データ</span><span class="sxs-lookup"><span data-stu-id="cab70-223">Exporting data into your database</span></span>

<span data-ttu-id="cab70-224">エンティティが宛先データベースに公開された後、**データ管理**ワークスペースのエクスポート機能を使用してデータを移動することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-224">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="cab70-225">エクスポート関数を使用すると、1 つまたは複数のエンティティが含まれるデータ移動ジョブを定義できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-225">The Export function lets you define a Data movement job that contains one or more entities.</span></span>

<span data-ttu-id="cab70-226">**エクスポート** ページを使用すると、Finance and Operations からのデータを、カンマで区切られた値 (CSV) 値などの多くのターゲット データ書式にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-226">You can use the **Export** page to export data from Finance and Operations into many target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="cab70-227">このページは、別の宛先として SQL データベースもサポートしています。</span><span class="sxs-lookup"><span data-stu-id="cab70-227">This page also supports SQL databases as another destination.</span></span>

![ページをエクスポート](media/091eb0da74bf94c620c3785bca92b41e.png)

<span data-ttu-id="cab70-229">データ エクスポートのエンティティを追加するとき、増分エクスポート (増分プッシュとも呼ばれます) またはフル プッシュをするかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="cab70-229">When you add an entity for data export, you can select to do an incremental export (which is also known as incremental push) or a full push.</span></span> <span data-ttu-id="cab70-230">作業する増分プッシュについては、このトピックで前述されているように、Finance and Operations データベースで**変更追跡**オプションを有効にし、適切な変更追跡オプションを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-230">For incremental push to work, you must enable the **Change tracking** option in the Finance and Operations database and specify an appropriate change tracking option, as described earlier in this topic.</span></span>

<span data-ttu-id="cab70-231">増分プッシュの実行を選択した場合、新しいレコードが挿入される、またはレコードが追加されるたびに、対応する変更が宛先エンティティに反映されます。</span><span class="sxs-lookup"><span data-stu-id="cab70-231">If you select to do an incremental push, whenever a new record is inserted, or a record is added, the corresponding change will be reflected in the destination entity.</span></span> <span data-ttu-id="cab70-232">プラットフォーム更新プログラム 8 による Microsoft Dynamics 365 for Finance and Operations, Enterprise edition では、ソースで削除されたレコードは出力先で更新されません。</span><span class="sxs-lookup"><span data-stu-id="cab70-232">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with platform update 8, records that are deleted in the source aren't updated in the destination.</span></span>

<span data-ttu-id="cab70-233">完全なプッシュは、選択したエンティティからのテーブルおよび挿入のすべてのレコードを切り詰めます。</span><span class="sxs-lookup"><span data-stu-id="cab70-233">Full push truncates the table and inserts all the records from the selected entity.</span></span>

<span data-ttu-id="cab70-234">複数のエンティティを持つデータ プロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-234">You can create a data project that has multiple entities.</span></span> <span data-ttu-id="cab70-235">Finance and Operations バッチ フレームワークを使用することにより、このデータ プロジェクトの実行をスケジュールすることができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-235">You can schedule this data project to run by using the Finance and Operations batch framework.</span></span> <span data-ttu-id="cab70-236">また、**バッチ処理でのエクスポート** オプションを選択することにより、データ エクスポート ジョブを定期的に実行するようにスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="cab70-236">You also schedule the data export job to run on a periodic basis by selecting the **Export in batch** option.</span></span>

### <a name="known-limitations"></a><span data-ttu-id="cab70-237">既知の制限</span><span class="sxs-lookup"><span data-stu-id="cab70-237">Known limitations</span></span>

<span data-ttu-id="cab70-238">BYOD 機能には、次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-238">The BYOD feature has the following limitations.</span></span>

#### <a name="there-should-be-no-active-sessions-on-your-database-during-synchronization"></a><span data-ttu-id="cab70-239">同期中、データベースにアクティブなセッションが存在してはいけません</span><span class="sxs-lookup"><span data-stu-id="cab70-239">There should be no active sessions on your database during synchronization</span></span>
<span data-ttu-id="cab70-240">BYOD は独自のデータベースであるため、Finance and Operations からデータが同期されているときは Azure SQL データベースにアクティブなセッションがないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-240">Because BYOD is your own database, you must ensure that there are no active sessions on your Azure SQL database when data is being synced from Finance and Operations.</span></span> <span data-ttu-id="cab70-241">同期中にデータベースの有効なセッションを実行すると、SQL ロックが発生し、書き込み速度が低下したり Azure SQL データベースへのエクスポートの完全な失敗につながる可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="cab70-241">Having active sessions on your database during synchronization can results in SQL locks which in turn can cause in slow writes or even complete failure of exports to your Azure SQL database.</span></span>

#### <a name="export-data-projects-are-specific-to-a-single-legal-entity"></a><span data-ttu-id="cab70-242">エクスポート データ プロジェクトは単一の法人に固有です。</span><span class="sxs-lookup"><span data-stu-id="cab70-242">Export data projects are specific to a single legal entity</span></span>

<span data-ttu-id="cab70-243">複数の法人間では、データをエクスポートする 1 つのジョブを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="cab70-243">You can't create a single job to export data across multiple legal entities.</span></span> <span data-ttu-id="cab70-244">データをエクスポートするデータ プロジェクトを作成するとき、このジョブは現在の法人からのデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="cab70-244">When you create a data project to export data, the job exports data from the current legal entity.</span></span> <span data-ttu-id="cab70-245">複数の法人からデータをエクスポートする必要がある場合は、法人を切り替えることにより、複数のデータ プロジェクトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-245">If you must export data from multiple legal entities, you must create multiple data projects by switching legal entities.</span></span>

#### <a name="you-cant-export-composite-entities-into-your-own-database"></a><span data-ttu-id="cab70-246">独自のデータベースに複合エンティティをエクスポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="cab70-246">You can't export composite entities into your own database</span></span>

<span data-ttu-id="cab70-247">現在、複合エンティティがサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cab70-247">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="cab70-248">複合エンティティを構成する個々 のエンティティをエクスポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-248">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="cab70-249">ただし、同じデータ プロジェクト内の両方のエンティティをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-249">However, you can export both the entities in the same data project.</span></span>

#### <a name="entities-that-dont-have-unique-keys-cant-be-exported-by-using-incremental-push"></a><span data-ttu-id="cab70-250">固有キーを持たないエンティティは、増分プッシュを使用してエクスポートすることは不可能</span><span class="sxs-lookup"><span data-stu-id="cab70-250">Entities that don't have unique keys can't be exported by using incremental push</span></span>

<span data-ttu-id="cab70-251">この制限は特に、数個の既製エンティティからレコードを段階的にエクスポートする場合に直面する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-251">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="cab70-252">これらのエンティティは Finance and Operations にデータをインポートできるように設計されているため、固有のキーはありません。</span><span class="sxs-lookup"><span data-stu-id="cab70-252">Because these entities were designed to enable the import of data into Finance and Operations, they don't have a unique key.</span></span> <span data-ttu-id="cab70-253">ただし、変更追跡を、固有のキーがあるエンティティに対してのみ有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cab70-253">However, you can enable change tracking only for entities that have a unique key.</span></span> <span data-ttu-id="cab70-254">したがって、増分プッシュには制限があります。</span><span class="sxs-lookup"><span data-stu-id="cab70-254">Therefore, there is a limitation on incremental push.</span></span> <span data-ttu-id="cab70-255">1 つの回避策は、必要なエンティティを拡張し、固有のキーを定義することです。</span><span class="sxs-lookup"><span data-stu-id="cab70-255">One workaround is to extend the required entity and define a unique key.</span></span>
