---
title: データベース ログの構成と管理
description: データベース ログを使用すると、Dynamics 365 Human Resources のテーブルとフィールドに対する変更を追跡できます。
author: andreabichsel
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae974436469c00a3df6fd40d9d60521a0883a917
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054815"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="3c8b3-103">データベース ログの構成と管理</span><span class="sxs-lookup"><span data-stu-id="3c8b3-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3c8b3-104">データベース ログを使用すると、Dynamics 365 Human Resources のテーブルとフィールドに対する変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="3c8b3-105">このトピックでは、次の方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-105">This topic describes how to:</span></span>

- <span data-ttu-id="3c8b3-106">データベース ログのセキュリティとパフォーマンスの管理</span><span class="sxs-lookup"><span data-stu-id="3c8b3-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="3c8b3-107">データベース ログの設定</span><span class="sxs-lookup"><span data-stu-id="3c8b3-107">Set up database logging</span></span>
- <span data-ttu-id="3c8b3-108">データベース ログのクリーン アップ</span><span class="sxs-lookup"><span data-stu-id="3c8b3-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="3c8b3-109">データベース ログの概要</span><span class="sxs-lookup"><span data-stu-id="3c8b3-109">Overview of database logging</span></span>

<span data-ttu-id="3c8b3-110">データベース ログは、Microsoft Dynamics 365 Human Resources のテーブルとフィールドに対する特定の変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="3c8b3-111">これらの変更には、挿入、更新、または削除が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="3c8b3-112">データベース ログは、データベース ログ テーブルにテーブルまたはフィールドの変更の記録を保存します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="3c8b3-113">データベース ログのビジネス用途は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="3c8b3-114">機密情報を含む特定のテーブルへの変更の監査記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="3c8b3-115">単一のトランザクションを追跡する。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-115">Tracking single transactions.</span></span> <span data-ttu-id="3c8b3-116">データベース ログは、バッチ ジョブで実行される自動トランザクションを追跡するためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="3c8b3-117">データベース ログのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="3c8b3-117">Security for database logging</span></span>

<span data-ttu-id="3c8b3-118">データベース ログには機密データが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="3c8b3-119">ログ データへのアクセスを必要とするセキュリティ ロールのみを含めるようにアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="3c8b3-120">データベース ログとパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="3c8b3-120">Database logging and performance</span></span>

<span data-ttu-id="3c8b3-121">業務の観点からは価値がありますが、データベース ログはリソースの使用と管理に費用がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="3c8b3-122">データベース ログのパフォーマンスへの影響は次のものがあります:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="3c8b3-123">データベース ログのテーブルは急速に増大し、データベースのサイズが増加する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="3c8b3-124">増加は、保持すると決めたログ データ量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="3c8b3-125">既定では、データベース ログ テーブルは 30 日分のログ データのみを保持します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="3c8b3-126">データベース ログは、実行時間の長いデータ インポートなど、長時間の自動化プロセスに悪い影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="3c8b3-127">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="3c8b3-127">Best practices</span></span>

<span data-ttu-id="3c8b3-128">パフォーマンスを向上させるには、テーブル全体ではなく、ログに記録する特定のフィールドを選択してログ エントリを制限します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="3c8b3-129">全体的なパフォーマンスを維持するために、データベース ログは 20 テーブルに制限されています。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="3c8b3-130">個々のフィールドでは、更新処理のログのみを記録できます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="3c8b3-131">データベース ログの設定</span><span class="sxs-lookup"><span data-stu-id="3c8b3-131">Set up database logging</span></span>

<span data-ttu-id="3c8b3-132">**ログ データベースの変更** ウィザードを使用して、データベースのログを設定できます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="3c8b3-133">ウィザードでは、テーブルやフィールドのログを柔軟に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="3c8b3-134">**システム管理 > リンク > データベース > データベース ログの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="3c8b3-135">**新規** を選択して、**ログ データベースの変更** ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="3c8b3-136">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-136">Select **Next**.</span></span> 
3. <span data-ttu-id="3c8b3-137">ウィザードの **テーブルとフィールド** ページで、データベース ログを有効にするテーブルとフィールドを選択して、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-137">On the **Tables and fields** page of the wizard, select the the tables and fields on which you want to enable database logging, and select **Next**.</span></span>

   > [!Note]
   > <span data-ttu-id="3c8b3-138">データベース ログは、Human Resources データベースの全テーブルで使用できません。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-138">Database logging is not available on all tables in the Human Resources database.</span></span> <span data-ttu-id="3c8b3-139">一覧の下の **すべてのテーブルを表示** を選択すると、テーブルおよびフィールドの一覧が展開され、データベース ログが使用できるすべてのデータベース テーブルが表示されますが、これはデータベース テーブルの完全リストのサブセットになります。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-139">Selecting **Show all tables** below the list expands the list of tables and fields to show all database tables for which database logging is available, but this will be a subset of the full list of database tables.</span></span>

4. <span data-ttu-id="3c8b3-140">ウィザードの **変更のタイプ** ページで、各テーブルおよびフィールドの変更を追跡するデータ操作を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-140">On the **Types of change** page of the wizard, select the data operations for which you want to track changes for each of the tables and fields, and select **Next**.</span></span> <span data-ttu-id="3c8b3-141">ログできるデータ操作の説明については、下の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-141">See the table below for a description of the data operations that are available for logging.</span></span>
5. <span data-ttu-id="3c8b3-142">**完了** ページで変更を確認し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-142">On the **Finish** page, review the changes that will be made, and select **Finish**.</span></span>

| <span data-ttu-id="3c8b3-143">操作</span><span class="sxs-lookup"><span data-stu-id="3c8b3-143">Operation</span></span> | <span data-ttu-id="3c8b3-144">説明</span><span class="sxs-lookup"><span data-stu-id="3c8b3-144">Description</span></span> |
| -- | -- |
| <span data-ttu-id="3c8b3-145">新しいトランザクションの追跡</span><span class="sxs-lookup"><span data-stu-id="3c8b3-145">Track new transactions</span></span> | <span data-ttu-id="3c8b3-146">テーブルに作成される新しいレコードのログを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-146">Create a log for new records that are created in the table.</span></span> |
| <span data-ttu-id="3c8b3-147">Update</span><span class="sxs-lookup"><span data-stu-id="3c8b3-147">Update</span></span> | <span data-ttu-id="3c8b3-148">テーブル レコードの更新またはテーブル内で個別に選択されたフィールドに対して、更新のログを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-148">Create a log for updates to table records, or updates to individually selected fields in the table.</span></span> <span data-ttu-id="3c8b3-149">テーブルの更新のログを選択すると、テーブル上のすべてのレコードのフィールドが更新されるたびにログ レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-149">If you select to log updates for the table, then a log record is created each time an update is made to any field of any record on the table.</span></span> <span data-ttu-id="3c8b3-150">特定のフィールドの更新をログする場合は、テーブル レコードのそれらのフィールドが更新された場合にのみログ レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-150">If you select to log updates for specific fields, then a log record is created only when updates are made to those fields of table records.</span></span> |
| <span data-ttu-id="3c8b3-151">消去</span><span class="sxs-lookup"><span data-stu-id="3c8b3-151">Delete</span></span> | <span data-ttu-id="3c8b3-152">テーブルから削除されたレコードのログを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-152">Create a log for records deleted from the table.</span></span> |
| <span data-ttu-id="3c8b3-153">キーの名前変更</span><span class="sxs-lookup"><span data-stu-id="3c8b3-153">Rename key</span></span> | <span data-ttu-id="3c8b3-154">テーブル キーの名前が変更された場合にログ レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-154">Create a log record when a table key is renamed.</span></span> |


## <a name="clean-up-database-logs"></a><span data-ttu-id="3c8b3-155">データベース ログのクリーン アップ</span><span class="sxs-lookup"><span data-stu-id="3c8b3-155">Clean up database logs</span></span>

<span data-ttu-id="3c8b3-156">次のオプションを使用して、データベース ログの全部または一部を削除できます:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-156">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="3c8b3-157">特定のテーブルのすべてのログを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-157">Select all logs for a particular table.</span></span>
- <span data-ttu-id="3c8b3-158">特定のタイプのデータベース ログを選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-158">Select specific types of database log.</span></span>
- <span data-ttu-id="3c8b3-159">ログが作成された日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-159">Select a date and time that a log was created.</span></span>

<span data-ttu-id="3c8b3-160">データベース ログのクリーンアップを設定するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-160">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="3c8b3-161">**システム管理 > リンク > データベース > データベース ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-161">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="3c8b3-162">**ログのクリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-162">Select **Clean up log**.</span></span>

2. <span data-ttu-id="3c8b3-163">次のいずれかのオプションを入力して、削除するログを選択する方法を選択します:</span><span class="sxs-lookup"><span data-stu-id="3c8b3-163">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="3c8b3-164">テーブル ID</span><span class="sxs-lookup"><span data-stu-id="3c8b3-164">Table ID</span></span>
   - <span data-ttu-id="3c8b3-165">ログのタイプ</span><span class="sxs-lookup"><span data-stu-id="3c8b3-165">Type of log</span></span>
   - <span data-ttu-id="3c8b3-166">作成日時</span><span class="sxs-lookup"><span data-stu-id="3c8b3-166">Created date and time</span></span>

3. <span data-ttu-id="3c8b3-167">**データベース ログのクリーンアップ** タブを使用して、ログのクリーンアップ タスクをいつ実行するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-167">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="3c8b3-168">既定では、データベース ログは 30 日間使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c8b3-168">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
