---
title: データベース ログの構成と管理
description: このトピックでは、データベース ログの管理について説明します。 データベース ログの設定方法、セキュリティとパフォーマンスの管理方法、およびデータベース ログのクリーンア ップ方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 03/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 57201
ms.assetid: 22a56b7d-4e07-4161-8416-0cac4a0b65a2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9db0cd6829c606b34dac1b0bc5c4db359e9108a7
ms.sourcegitcommit: 8bd87814d32dc4941a84b696d821960455265709
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117058"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="6ac86-104">データベース ログの構成と管理</span><span class="sxs-lookup"><span data-stu-id="6ac86-104">Configure and manage database logging</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ac86-105">データベース ログを使用すると、Finance and Operations アプリで、テーブルとフィールドに対する特定のタイプの変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-105">Database logging provides a way to track specific types of changes to the tables and fields in Finance and Operation apps.</span></span> <span data-ttu-id="6ac86-106">追跡可能な変更には、挿入、更新、削除、名前変更の各キー操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-106">Changes that can be tracked include insert, update, delete, and rename key operations.</span></span> <span data-ttu-id="6ac86-107">テーブルまたはフィールドのログを設定すると、そのテーブルまたはフィールドに対するすべての変更のレコードが、環境データベースのデータベース ログ テーブル **sysdatabaselog** に格納されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-107">When you configure logging for a table or field, a record of every change to that table or field is stored in the database log table, **sysdatabaselog**, in the environment database.</span></span>

<span data-ttu-id="6ac86-108">データベース ログは、次の目的で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-108">Database logging can be used for these purposes:</span></span>

- <span data-ttu-id="6ac86-109">機密情報を含む特定のテーブルへの変更を監査可能な形で生成します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-109">Create an auditable record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="6ac86-110">電子署名の使用を監視します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-110">Monitor the use of electronic signatures.</span></span> <span data-ttu-id="6ac86-111">既定では、電子署名を使用して署名されたすべての取引が記録されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-111">By default, all transactions that have been signed by using electronic signatures are logged.</span></span>

<span data-ttu-id="6ac86-112">データベース ログは、個々の取引を追跡することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="6ac86-112">Database logging is intended to track individual transactions.</span></span> <span data-ttu-id="6ac86-113">バッチ ジョブが実行する、自動化された取引を追跡するためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="6ac86-113">It isn't intended to track automated transactions that are run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="6ac86-114">データベース ログのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="6ac86-114">Security for database logging</span></span>

<span data-ttu-id="6ac86-115">データベース ログには機密データが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-115">Database logs can contain sensitive data.</span></span> <span data-ttu-id="6ac86-116">既定では、データベースへのアクセス権を持つユーザーは、X ++ やは警告を使用するか、データベースを直接照会することにより、データベース ログのテーブルは、 (**sysdatabaselog**) を照会できます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-116">By default, any user who has database access can query the database log table (**sysdatabaselog**) by using X++ or alerts, or by querying the database directly.</span></span> <span data-ttu-id="6ac86-117">データを保護するには、オンプレミス配置で使用する **sysdatabaselog** テーブルのアクセス権限を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-117">To help protect data, you should restrict permissions on the **sysdatabaselog** table for on-premises deployments.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="6ac86-118">データベース ログとパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="6ac86-118">Database logging and performance</span></span>

<span data-ttu-id="6ac86-119">データベースのログは業務の観点から見ると便利ですが、リソースの使用と管理に関しては費用がかさむ場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-119">Although database logging can be valuable from a business perspective, it can be expensive with regard to resource use and management.</span></span> <span data-ttu-id="6ac86-120">ここでは、データベース ログのパフォーマンスにがおよぼす影響について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-120">Here are some of the performance implications of database logging:</span></span>

- <span data-ttu-id="6ac86-121">データベース ログのテーブルは、データ量が増大するペースが速く、データベースのサイズが増大する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-121">The database log table can grow quickly and can increase the size of the database.</span></span> <span data-ttu-id="6ac86-122">増加の程度は、保持するログに記録されたデータ量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-122">The amount of growth depends on the amount of logged data that you decide to retain.</span></span>
- <span data-ttu-id="6ac86-123">取引タイプのログの記録がオンになっている場合、当該取引タイプの各インスタンスが Microsoft SQL Server のトランザクション ログファイルに複数のレコードを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-123">When logging is turned on for a transaction type, each instance of that transaction type causes multiple records to be written to the Microsoft SQL Server transaction log file.</span></span> <span data-ttu-id="6ac86-124">具体的には、最初の取引に対して 1 つのレコードを書き込み、また別のレコードがデータベース ログのテーブルに取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-124">Specifically, one record is written for the initial transaction, and one record logs the transaction in the database log table.</span></span> <span data-ttu-id="6ac86-125">したがって、取引のログ ファイルはより速く増大し、追加の保守作業が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-125">Therefore, the transaction log file will grow more quickly and might require additional maintenance.</span></span>
- <span data-ttu-id="6ac86-126">データベースのログは、在庫の原価計算、部品表 (BOMs)、マスタープラン、長期にわたるデータ インポートなどの時間がかかる自動化プロセスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6ac86-126">Database logging can adversely affect long-running automated processes, such as inventory close, calculations for bills of materials (BOMs), master planning, and long-running data imports.</span></span>
- <span data-ttu-id="6ac86-127">テーブルのログがオンになっている場合、すべてのセットベースのデータベース操作は、行ベースの操作へとダウン グレードされます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-127">When logging is turned on for a table, all set-based database operations are downgraded to row-based operations.</span></span> <span data-ttu-id="6ac86-128">たとえば、テーブルへの挿入処理のログを記録している場合、各挿入は行ベースの挿入として実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-128">For example, if you're logging inserts for a table, each insert is done as a row-based insert.</span></span>

<span data-ttu-id="6ac86-129">ここでは、マイクロソフトが推奨するいくつかの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-129">Here are some practices that Microsoft recommends:</span></span>

- <span data-ttu-id="6ac86-130">ログに記録されたデータを保持する期間、およびデータをアーカイブまたは削除方法に関する計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-130">Create a plan for how long you will retain logged data, and how you will archive or delete data.</span></span>
- <span data-ttu-id="6ac86-131">ログのエントリを制限し、パフォーマンスを改善するには、テーブル全体ではなく、ログを記録するフィールドを個別に選択します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-131">Limit log entries, and help improve performance by selecting specific fields to log instead of whole tables.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ac86-132">個々のフィールドでは、更新処理のログのみを記録できます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-132">Only updates can be logged for individual fields.</span></span>

- <span data-ttu-id="6ac86-133">データベース ログの構成後は、SQL Server の取引ログのバックアップ頻度を増やすことを検討してください。</span><span class="sxs-lookup"><span data-stu-id="6ac86-133">After you configure database logging, consider increasing the frequency of backups of the SQL Server transaction log.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6ac86-134">この推奨事項は、SQL Server のローカル インスタンスを持つオンプレミス型の展開にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-134">This recommendation applies only to on-premises deployments that have a local instance of SQL Server.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="6ac86-135">データベース ログの設定</span><span class="sxs-lookup"><span data-stu-id="6ac86-135">Set up database logging</span></span>

<span data-ttu-id="6ac86-136">**ログ データベースの変更**ウィザードを使用して、データベースのログを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-136">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="6ac86-137">このウィザードを使用すると、テーブルやフィールドのログを柔軟に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-137">This wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="6ac86-138">**システム管理** \> **設定** \> **データベース** \> **データベース ログの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-138">Go to **System administration** \> **Setup** \> **Database** \> **Database log setup**.</span></span>
2. <span data-ttu-id="6ac86-139">**新規** を選択して、**ログ データベースの変更** ウィザードを開きます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-139">Select **New** to open the **Logging database changes** wizard.</span></span>
3. <span data-ttu-id="6ac86-140">ウィザードの操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-140">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="6ac86-141">データベース ログのクリーン アップ</span><span class="sxs-lookup"><span data-stu-id="6ac86-141">Clean up database logs</span></span>

<span data-ttu-id="6ac86-142">データベース ログは必要に応じて削除できます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-142">You can delete database logs as required.</span></span> <span data-ttu-id="6ac86-143">特定のテーブルのログを削除したり、特定のタイプのデータベース ログを削除するなど、作成された日時に基づいてログを削除したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-143">You can delete logs for specific tables, delete specific types of database logs, or delete logs based on the date and time when they were created.</span></span>

> [!NOTE]
> <span data-ttu-id="6ac86-144">電子署名されたレコードは、ログから削除できません。</span><span class="sxs-lookup"><span data-stu-id="6ac86-144">Records that have been electronically signed can't be deleted from logs.</span></span>

1. <span data-ttu-id="6ac86-145">**システム管理** \> **問い合わせ** \> **設定** \> **データベース ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-145">Go to **System administration** \> **Inquiries** \> **Database** \> **Database log**.</span></span>
2. <span data-ttu-id="6ac86-146">**ログのクリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-146">Select **Clean up log**.</span></span>
3. <span data-ttu-id="6ac86-147">削除するログを選択するにあたって使用するメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-147">Select the method that should be used to select the logs that are deleted.</span></span> <span data-ttu-id="6ac86-148">ログの参照先のテーブル ID、ログのタイプ、作成日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-148">Enter the table ID that the logs refer to, the type of log, or the creation date and time.</span></span>
4. <span data-ttu-id="6ac86-149">**データベース ログのクリーンアップ** タブを使用して、ログのクリーンアップ タスクを実行するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-149">Use the **Database log cleanup** tab to specify when the log cleanup task should be run.</span></span>

## <a name="consistency-check-for-database-log-triggers"></a><span data-ttu-id="6ac86-150">データベース ログ トリガーの整合性チェック</span><span class="sxs-lookup"><span data-stu-id="6ac86-150">Consistency check for database log triggers</span></span>

<span data-ttu-id="6ac86-151">プラットフォーム更新プログラム 34 では、整合性チェックをする機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="6ac86-151">In Platform update 34, functionality for a consistency check was added.</span></span> <span data-ttu-id="6ac86-152">整合性チェックは、**データベースログ** ウィザードの一環として実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-152">The consistency check is run as part of the **Database log** wizard.</span></span> <span data-ttu-id="6ac86-153">**完了** を選択した後、**データベース ログの設定** ページの**整合性チェック** を選択した後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-153">It's run after you select **Finish** or after you select **Consistency check** on the **Database log setup** page.</span></span>

<span data-ttu-id="6ac86-154">整合性チェックでは、不足しているデータベース ログのトリガーが再作成されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-154">The consistency check will re-create any missing database log triggers.</span></span> <span data-ttu-id="6ac86-155">また、対応する構成が見つからない孤立したデータベース ログのトリガーも削除されます。</span><span class="sxs-lookup"><span data-stu-id="6ac86-155">It will also drop any "orphaned" database log triggers that no corresponding configuration is found for.</span></span> <span data-ttu-id="6ac86-156">整合性チェックでは、このように現在の構成と、ログ機能の実装に使用するデータベース トリガーとの間に不整合がある場合は、ただちにそれを検出して修正します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-156">In this way, the consistency check quickly detects and fixes any inconsistencies between the current configuration and the database triggers that are used to implement the logging functionality.</span></span>

1. <span data-ttu-id="6ac86-157">**システム管理** \> **問い合わせ** \> **設定** \> **データベース ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-157">Go to **System administration** \> **Inquiries** \> **Database** \> **Database log**.</span></span>
2. <span data-ttu-id="6ac86-158">**データベース ログ** のページで、 **整合性チェック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ac86-158">On the **Database log** page, select **Consistency check**.</span></span>
