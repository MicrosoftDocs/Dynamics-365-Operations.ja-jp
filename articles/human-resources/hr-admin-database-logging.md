---
title: データベース ログの構成と管理
description: データベース ログを使用すると、Dynamics 365 Human Resources のテーブルとフィールドに対する変更を追跡できます。
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8057ebd0bc061c6bf78d8674c45e0885ffce681c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467652"
---
# <a name="configure-and-manage-database-logging"></a><span data-ttu-id="0845b-103">データベース ログの構成と管理</span><span class="sxs-lookup"><span data-stu-id="0845b-103">Configure and manage database logging</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0845b-104">データベース ログを使用すると、Dynamics 365 Human Resources のテーブルとフィールドに対する変更を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0845b-104">You can track changes to tables and fields in Dynamics 365 Human Resources with database logging.</span></span> <span data-ttu-id="0845b-105">このトピックでは、次の方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="0845b-105">This topic describes how to:</span></span>

- <span data-ttu-id="0845b-106">データベース ログのセキュリティとパフォーマンスの管理</span><span class="sxs-lookup"><span data-stu-id="0845b-106">Manage security and performance for database logging</span></span>
- <span data-ttu-id="0845b-107">データベース ログの設定</span><span class="sxs-lookup"><span data-stu-id="0845b-107">Set up database logging</span></span>
- <span data-ttu-id="0845b-108">データベース ログのクリーン アップ</span><span class="sxs-lookup"><span data-stu-id="0845b-108">Clean up database logs</span></span>

## <a name="overview-of-database-logging"></a><span data-ttu-id="0845b-109">データベース ログの概要</span><span class="sxs-lookup"><span data-stu-id="0845b-109">Overview of database logging</span></span>

<span data-ttu-id="0845b-110">データベース ログは、Microsoft Dynamics 365 Human Resources のテーブルとフィールドに対する特定の変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="0845b-110">Database logging tracks specific changes to Microsoft Dynamics 365 Human Resources tables and fields.</span></span> <span data-ttu-id="0845b-111">これらの変更には、挿入、更新、または削除が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0845b-111">These changes include inserting, updating, or deleting.</span></span> <span data-ttu-id="0845b-112">データベース ログは、データベース ログ テーブルにテーブルまたはフィールドの変更の記録を保存します。</span><span class="sxs-lookup"><span data-stu-id="0845b-112">Database logging stores a record of changes to tables or fields in the database log table.</span></span>

<span data-ttu-id="0845b-113">データベース ログのビジネス用途は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="0845b-113">The business uses of database logging include:</span></span>

- <span data-ttu-id="0845b-114">機密情報を含む特定のテーブルへの変更の監査記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="0845b-114">Creating an audit record of changes to specific tables that contain sensitive information.</span></span>
- <span data-ttu-id="0845b-115">単一のトランザクションを追跡する。</span><span class="sxs-lookup"><span data-stu-id="0845b-115">Tracking single transactions.</span></span> <span data-ttu-id="0845b-116">データベース ログは、バッチ ジョブで実行される自動トランザクションを追跡するためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="0845b-116">Database logging isn't intended for tracking automated transactions that run in batch jobs.</span></span>

## <a name="security-for-database-logging"></a><span data-ttu-id="0845b-117">データベース ログのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="0845b-117">Security for database logging</span></span>

<span data-ttu-id="0845b-118">データベース ログには機密データが含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="0845b-118">Database logs can contain sensitive data.</span></span> <span data-ttu-id="0845b-119">ログ データへのアクセスを必要とするセキュリティ ロールのみを含めるようにアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="0845b-119">Limit access to include only security roles that need access to the log data.</span></span>

## <a name="database-logging-and-performance"></a><span data-ttu-id="0845b-120">データベース ログとパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="0845b-120">Database logging and performance</span></span>

<span data-ttu-id="0845b-121">業務の観点からは価値がありますが、データベース ログはリソースの使用と管理に費用がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0845b-121">While valuable from a business perspective, database logging can be expensive in resource use and management.</span></span> <span data-ttu-id="0845b-122">データベース ログのパフォーマンスへの影響は次のものがあります:</span><span class="sxs-lookup"><span data-stu-id="0845b-122">The performance implications of database logging include:</span></span>

- <span data-ttu-id="0845b-123">データベース ログのテーブルは急速に増大し、データベースのサイズが増加する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0845b-123">The database log table can grow quickly and cause an increase in the size of the database.</span></span> <span data-ttu-id="0845b-124">増加は、保持すると決めたログ データ量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="0845b-124">Growth depends on the amount of logged data that you decide to keep.</span></span> <span data-ttu-id="0845b-125">既定では、データベース ログ テーブルは 30 日分のログ データのみを保持します。</span><span class="sxs-lookup"><span data-stu-id="0845b-125">By default, the database log table maintains only 30 days of log data.</span></span> 

- <span data-ttu-id="0845b-126">データベース ログは、実行時間の長いデータ インポートなど、長時間の自動化プロセスに悪い影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0845b-126">Database logging can adversely affect long-running automated processes, such as long-running data imports.</span></span>

### <a name="best-practices"></a><span data-ttu-id="0845b-127">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="0845b-127">Best practices</span></span>

<span data-ttu-id="0845b-128">パフォーマンスを向上させるには、テーブル全体ではなく、ログに記録する特定のフィールドを選択してログ エントリを制限します。</span><span class="sxs-lookup"><span data-stu-id="0845b-128">To improve performance, limit log entries by selecting specific fields to log instead of whole tables.</span></span> <span data-ttu-id="0845b-129">全体的なパフォーマンスを維持するために、データベース ログは 20 テーブルに制限されています。</span><span class="sxs-lookup"><span data-stu-id="0845b-129">To help maintain overall performance, database logging is limited to 20 tables.</span></span>

> [!NOTE]
> <span data-ttu-id="0845b-130">個々のフィールドでは、更新処理のログのみを記録できます。</span><span class="sxs-lookup"><span data-stu-id="0845b-130">Only updates can be logged for individual fields.</span></span>

## <a name="set-up-database-logging"></a><span data-ttu-id="0845b-131">データベース ログの設定</span><span class="sxs-lookup"><span data-stu-id="0845b-131">Set up database logging</span></span>

<span data-ttu-id="0845b-132">**ログ データベースの変更** ウィザードを使用して、データベースのログを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0845b-132">You can use the **Logging database changes** wizard to set up database logging.</span></span> <span data-ttu-id="0845b-133">ウィザードでは、テーブルやフィールドのログを柔軟に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0845b-133">The wizard provides a flexible way to set up logging for tables or fields.</span></span>

1. <span data-ttu-id="0845b-134">**システム管理 > リンク > データベース > データベース ログの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0845b-134">Go to **System administration > Links > Database > Database log setup**.</span></span> <span data-ttu-id="0845b-135">**新規** を選択して、**ログ データベースの変更** ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="0845b-135">Select **New** to start the **Logging database changes** wizard.</span></span>
2. <span data-ttu-id="0845b-136">ウィザードの操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="0845b-136">Complete the wizard.</span></span>

## <a name="clean-up-database-logs"></a><span data-ttu-id="0845b-137">データベース ログのクリーン アップ</span><span class="sxs-lookup"><span data-stu-id="0845b-137">Clean up database logs</span></span>

<span data-ttu-id="0845b-138">次のオプションを使用して、データベース ログの全部または一部を削除できます:</span><span class="sxs-lookup"><span data-stu-id="0845b-138">You can delete all or part of the database logs, using the following options:</span></span>

- <span data-ttu-id="0845b-139">特定のテーブルのすべてのログを選択します。</span><span class="sxs-lookup"><span data-stu-id="0845b-139">Select all logs for a particular table.</span></span>
- <span data-ttu-id="0845b-140">特定のタイプのデータベース ログを選択します。</span><span class="sxs-lookup"><span data-stu-id="0845b-140">Select specific types of database log.</span></span>
- <span data-ttu-id="0845b-141">ログが作成された日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="0845b-141">Select a date and time that a log was created.</span></span>

<span data-ttu-id="0845b-142">データベース ログのクリーンアップを設定するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="0845b-142">To set up database log cleanup, follow these steps:</span></span> 

1. <span data-ttu-id="0845b-143">**システム管理 > リンク > データベース > データベース ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0845b-143">Go to **System administration > Links > Database > Database log**.</span></span> <span data-ttu-id="0845b-144">**ログのクリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0845b-144">Select **Clean up log**.</span></span>

2. <span data-ttu-id="0845b-145">次のいずれかのオプションを入力して、削除するログを選択する方法を選択します:</span><span class="sxs-lookup"><span data-stu-id="0845b-145">Choose a method of selecting logs to delete by entering one of the following options:</span></span>

   - <span data-ttu-id="0845b-146">テーブル ID</span><span class="sxs-lookup"><span data-stu-id="0845b-146">Table ID</span></span>
   - <span data-ttu-id="0845b-147">ログのタイプ</span><span class="sxs-lookup"><span data-stu-id="0845b-147">Type of log</span></span>
   - <span data-ttu-id="0845b-148">作成日時</span><span class="sxs-lookup"><span data-stu-id="0845b-148">Created date and time</span></span>

3. <span data-ttu-id="0845b-149">**データベース ログのクリーンアップ** タブを使用して、ログのクリーンアップ タスクをいつ実行するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0845b-149">Use the **Database log cleanup** tab to determine when to run the log cleanup task.</span></span> <span data-ttu-id="0845b-150">既定では、データベース ログは 30 日間使用できます。</span><span class="sxs-lookup"><span data-stu-id="0845b-150">By default, database logs are available for 30 days.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]