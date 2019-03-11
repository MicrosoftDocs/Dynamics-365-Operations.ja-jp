---
title: データベース移動操作
description: このトピックでは、Lifecycle Services のデータベース移動機能の一部として使用可能な操作について説明します。
author: laneswenka
manager: AnnBe
ms.date: 10/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 103674f8eefce840e3c6064d4b922b1ae69d4012
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369150"
---
# <a name="database-movement-operations"></a><span data-ttu-id="15321-103">データベース移動操作</span><span class="sxs-lookup"><span data-stu-id="15321-103">Database Movement operations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/private-preview-banner.md)]

<span data-ttu-id="15321-104">このトピックでは、Lifecycle Services (LCS) のデータベース移動機能の一部として使用可能な操作について説明します。</span><span class="sxs-lookup"><span data-stu-id="15321-104">This topic describes the operations that are available as part of the Database Movement features in Lifecycle Services (LCS).</span></span>  

## <a name="sandbox-refresh"></a><span data-ttu-id="15321-105">サンドボックスの更新</span><span class="sxs-lookup"><span data-stu-id="15321-105">Sandbox refresh</span></span>
<span data-ttu-id="15321-106">実稼働環境をサンドボックス環境に、またはサンドボックス環境を別のサンドボックス環境に更新するときは、ターゲット環境にコピーされない特定のデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="15321-106">When refreshing a production environment to a sandbox environment, or a sandbox environment to another sandbox environment, there are certain elements of the database that are not copied over to the target environment.</span></span>  <span data-ttu-id="15321-107">これらの要素として次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="15321-107">These elements include:</span></span>
* <span data-ttu-id="15321-108">LogisticsElectronicAddress テーブル内の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="15321-108">Email addresses in the LogisticsElectronicAddress table.</span></span>
* <span data-ttu-id="15321-109">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。</span><span class="sxs-lookup"><span data-stu-id="15321-109">Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables.</span></span>
* <span data-ttu-id="15321-110">SysEmailSMTPPassword テーブルの SMTP パスワード。</span><span class="sxs-lookup"><span data-stu-id="15321-110">SMTP password in the SysEmailSMTPPassword table.</span></span>
* <span data-ttu-id="15321-111">SysEmailParameters テーブルの SMTP 中継サーバー。</span><span class="sxs-lookup"><span data-stu-id="15321-111">SMTP Relay server in the SysEmailParameters table.</span></span>
* <span data-ttu-id="15321-112">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。</span><span class="sxs-lookup"><span data-stu-id="15321-112">Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables.</span></span>
* <span data-ttu-id="15321-113">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。</span><span class="sxs-lookup"><span data-stu-id="15321-113">Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables.</span></span>
* <span data-ttu-id="15321-114">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="15321-114">Document attachments in the DocuValue table.</span></span>
* <span data-ttu-id="15321-115">管理者を除くすべてのユーザーが無効になります。</span><span class="sxs-lookup"><span data-stu-id="15321-115">All users except for the administrator are disabled.</span></span>
* <span data-ttu-id="15321-116">すべてのバッチ ジョブは、[保留] 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="15321-116">All batch jobs are set to Withhold status.</span></span>

## <a name="import"></a><span data-ttu-id="15321-117">インポート元</span><span class="sxs-lookup"><span data-stu-id="15321-117">Import</span></span>
<span data-ttu-id="15321-118">データベース バックアップをサンドボックス環境にインポートするときは、特定のアクティビティを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15321-118">When importing a database backup in to a sandbox environment, there are certain activities which must be performed.</span></span>  <span data-ttu-id="15321-119">コピーされるフィールドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="15321-119">These include:</span></span>
* <span data-ttu-id="15321-120">要件に従って、電子メール機能が正しく再設定または無効化されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="15321-120">Ensure email capabilities are properly reconfigured or disabled, per your requirements.</span></span>
* <span data-ttu-id="15321-121">AOS サーバーが必要なバッチ グループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="15321-121">AOS servers are added back to required batch groups.</span></span>
* <span data-ttu-id="15321-122">システム ヘルプとタスク ガイドに再接続されます。</span><span class="sxs-lookup"><span data-stu-id="15321-122">System Help and Task guides are reconnected.</span></span>
* <span data-ttu-id="15321-123">バッチ ジョブは、[待機中] 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="15321-123">Batch jobs are set to Waiting status.</span></span>
* <span data-ttu-id="15321-124">ユーザーは再度有効になります。</span><span class="sxs-lookup"><span data-stu-id="15321-124">Users are re-enabled.</span></span>

## <a name="export"></a><span data-ttu-id="15321-125">輸出</span><span class="sxs-lookup"><span data-stu-id="15321-125">Export</span></span>
<span data-ttu-id="15321-126">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされない特定のデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="15321-126">When exporting a database backup from an environment, there are certain elements of the database that are not exported in the backup file.</span></span>  <span data-ttu-id="15321-127">これらの要素として次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="15321-127">These elements include:</span></span>
* <span data-ttu-id="15321-128">LogisticsElectronicAddress テーブル内の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="15321-128">Email addresses in the LogisticsElectronicAddress table.</span></span>
* <span data-ttu-id="15321-129">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。</span><span class="sxs-lookup"><span data-stu-id="15321-129">Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables.</span></span>
* <span data-ttu-id="15321-130">SysEmailSMTPPassword テーブルの SMTP パスワード。</span><span class="sxs-lookup"><span data-stu-id="15321-130">SMTP password in the SysEmailSMTPPassword table.</span></span>
* <span data-ttu-id="15321-131">SysEmailParameters テーブルの SMTP 中継サーバー。</span><span class="sxs-lookup"><span data-stu-id="15321-131">SMTP Relay server in the SysEmailParameters table.</span></span>
* <span data-ttu-id="15321-132">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。</span><span class="sxs-lookup"><span data-stu-id="15321-132">Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables.</span></span>
* <span data-ttu-id="15321-133">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。</span><span class="sxs-lookup"><span data-stu-id="15321-133">Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables.</span></span>
* <span data-ttu-id="15321-134">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="15321-134">Document attachments in the DocuValue table.</span></span>
* <span data-ttu-id="15321-135">管理者を除くすべてのユーザーが無効になります。</span><span class="sxs-lookup"><span data-stu-id="15321-135">All users except for the administrator are disabled.</span></span>
* <span data-ttu-id="15321-136">すべてのバッチ ジョブは、[保留] 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="15321-136">All batch jobs are set to Withhold status.</span></span>
