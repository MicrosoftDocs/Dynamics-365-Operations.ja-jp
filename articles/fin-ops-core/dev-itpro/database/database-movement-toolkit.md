---
title: データベース移動ツールキット
description: このトピックでは、データベース移動ツールキットをダウンロードして使用する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: d818b9690ade862756c8b25e95b892662c7c0314
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5126991"
---
# <a name="database-movement-toolkit"></a><span data-ttu-id="7ec67-103">データベース移動ツールキット</span><span class="sxs-lookup"><span data-stu-id="7ec67-103">Database movement toolkit</span></span>

<span data-ttu-id="7ec67-104">データベース移動ツールキットは、Microsoft Dynamics Lifecycle Services (LCS) にホストされる ZIP ファイルです。</span><span class="sxs-lookup"><span data-stu-id="7ec67-104">The Database movement toolkit is a ZIP file hosted in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7ec67-105">このツールキットをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="7ec67-105">This toolkit is available for download.</span></span> <span data-ttu-id="7ec67-106">開発環境とサンドボックス環境との間でのデータ移動に関するカスタマー エクスペリエンスを高める一連のスクリプトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ec67-106">It contains a series of scripts that enhance the customer experience for movement of data between developer environments and sandbox environments.</span></span> <span data-ttu-id="7ec67-107">このトピックでは、ツールキットのコンポーネント、ダウンロード方法、および最近の変更点について説明します。</span><span class="sxs-lookup"><span data-stu-id="7ec67-107">This topic explains the components of the toolkit, how to download it, and any recent changes.</span></span>

## <a name="download-the-latest-version"></a><span data-ttu-id="7ec67-108">最新バージョンのダウンロード</span><span class="sxs-lookup"><span data-stu-id="7ec67-108">Download the latest version</span></span>

<span data-ttu-id="7ec67-109">ツールキットは、LCS 共有アセット ライブラリの **モデル** セクションで入手できます。</span><span class="sxs-lookup"><span data-stu-id="7ec67-109">The toolkit is available in the LCS Shared Asset Library under the **Models** section.</span></span>  <span data-ttu-id="7ec67-110">**データベース移動ツールキット** というタイトルのエントリを検索し、Tier1 DevTest 環境にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="7ec67-110">Search for the entry titled **Database Movement Toolkit** and then download it to your Tier1 DevTest environment.</span></span>  

## <a name="toolkit-components"></a><span data-ttu-id="7ec67-111">ツールキット コンポーネント</span><span class="sxs-lookup"><span data-stu-id="7ec67-111">Toolkit components</span></span>

<span data-ttu-id="7ec67-112">このツールキットには、次の主要コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ec67-112">The toolkit contains the following primary components:</span></span>

- <span data-ttu-id="7ec67-113">**Sqlpackage.exe** - このツールは Microsoft Azure SQL データベース、および Tier1 DevTest にホストされている SQL Server データベースに対して、抽出および公開アクションを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="7ec67-113">**Sqlpackage.exe** - This tool is used to perform extract and publish actions against Microsoft Azure SQL databases, as well as SQL Server databases hosted on Tier1 DevTest environments.</span></span>  
- <span data-ttu-id="7ec67-114">**PowerShell 7.0** - これは、並列処理機能を含む PowerShell の自己完結型バージョンであり、環境間でのデータ転送のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="7ec67-114">**PowerShell 7.0** - This is a self-contained version of PowerShell that includes capabilities for parallelism, which increases the performance of transferring data between environments.</span></span>  
- <span data-ttu-id="7ec67-115">**PowerShell スクリプト** - AX 2012 データのアップグレードのようなシナリオでのエクスペリエンスを向上させ、自動化するためのスクリプトがいくつか用意されています。</span><span class="sxs-lookup"><span data-stu-id="7ec67-115">**PowerShell script** - There are several scripts included to provide an enhanced and more automated experience for scenarios such as AX 2012 data upgrade.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="7ec67-116">サポートされているシナリオ</span><span class="sxs-lookup"><span data-stu-id="7ec67-116">Supported scenarios</span></span>

<span data-ttu-id="7ec67-117">現在、このツールキットは次のシナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7ec67-117">The toolkit currently supports the following scenarios.</span></span> <span data-ttu-id="7ec67-118">今後、さらに追加される予定です。</span><span class="sxs-lookup"><span data-stu-id="7ec67-118">More will be added over time.</span></span>  

* [<span data-ttu-id="7ec67-119">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="7ec67-119">Upgrade from AX 2012 - Data upgrade in sandbox environments</span></span>](../migration-upgrade/upgrade-data-sandbox-dacpac.md)

## <a name="versions"></a><span data-ttu-id="7ec67-120">バージョン</span><span class="sxs-lookup"><span data-stu-id="7ec67-120">Versions</span></span>

### <a name="version-5"></a><span data-ttu-id="7ec67-121">バージョン 5</span><span class="sxs-lookup"><span data-stu-id="7ec67-121">Version 5</span></span>
| <span data-ttu-id="7ec67-122">機能</span><span class="sxs-lookup"><span data-stu-id="7ec67-122">Feature</span></span> | <span data-ttu-id="7ec67-123">細目</span><span class="sxs-lookup"><span data-stu-id="7ec67-123">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="7ec67-124">スキーマの発行</span><span class="sxs-lookup"><span data-stu-id="7ec67-124">Schema publish</span></span> | <span data-ttu-id="7ec67-125">CleanupSource および Cleanupsource スクリプトが追加されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-125">Added CleanupSource and CleanupTarget scripts.</span></span>|
| <span data-ttu-id="7ec67-126">データ転送</span><span class="sxs-lookup"><span data-stu-id="7ec67-126">Data transfer</span></span> | <span data-ttu-id="7ec67-127">移動時間をキャプチャするためのタイマーが追加されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-127">Added timer to capture transfer time.</span></span>|

### <a name="version-4"></a><span data-ttu-id="7ec67-128">バージョン 4</span><span class="sxs-lookup"><span data-stu-id="7ec67-128">Version 4</span></span>
| <span data-ttu-id="7ec67-129">機能</span><span class="sxs-lookup"><span data-stu-id="7ec67-129">Feature</span></span> | <span data-ttu-id="7ec67-130">細目</span><span class="sxs-lookup"><span data-stu-id="7ec67-130">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="7ec67-131">スキーマの発行</span><span class="sxs-lookup"><span data-stu-id="7ec67-131">Schema publish</span></span> | <span data-ttu-id="7ec67-132">マイナーな改良。</span><span class="sxs-lookup"><span data-stu-id="7ec67-132">Minor improvements.</span></span>|

### <a name="version-3"></a><span data-ttu-id="7ec67-133">バージョン 3</span><span class="sxs-lookup"><span data-stu-id="7ec67-133">Version 3</span></span>
| <span data-ttu-id="7ec67-134">機能</span><span class="sxs-lookup"><span data-stu-id="7ec67-134">Feature</span></span> | <span data-ttu-id="7ec67-135">細目</span><span class="sxs-lookup"><span data-stu-id="7ec67-135">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="7ec67-136">スキーマの発行</span><span class="sxs-lookup"><span data-stu-id="7ec67-136">Schema publish</span></span> | <span data-ttu-id="7ec67-137">PublishDiag.log にエラーを出力するようにスクリプトが修正されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-137">Fixed the scripts to output errors in PublishDiag.log.</span></span>|

### <a name="version-2"></a><span data-ttu-id="7ec67-138">Version 2</span><span class="sxs-lookup"><span data-stu-id="7ec67-138">Version 2</span></span>
| <span data-ttu-id="7ec67-139">機能</span><span class="sxs-lookup"><span data-stu-id="7ec67-139">Feature</span></span> | <span data-ttu-id="7ec67-140">細目</span><span class="sxs-lookup"><span data-stu-id="7ec67-140">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="7ec67-141">スキーマの発行</span><span class="sxs-lookup"><span data-stu-id="7ec67-141">Schema publish</span></span> | <span data-ttu-id="7ec67-142">Sqlpackage ディレクトリで現在のディレクトリ参照を使用するようにスクリプトが修正されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-142">Fixed the scripts to use current directory reference to Sqlpackage directory.</span></span>|
| <span data-ttu-id="7ec67-143">スキーマの発行</span><span class="sxs-lookup"><span data-stu-id="7ec67-143">Schema publish</span></span> | <span data-ttu-id="7ec67-144">ソース データベースからローカル ユーザーを削除し、環境固有のテーブルを整理するようにスクリプトが修正されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-144">Fixed the scripts to delete local users from the source database, and tidy up environment-specific tables.</span></span>|
| <span data-ttu-id="7ec67-145">データ転送</span><span class="sxs-lookup"><span data-stu-id="7ec67-145">Data transfer</span></span> | <span data-ttu-id="7ec67-146">欠落している PowerShell モジュールをインストールするようにスクリプトが修正されました。</span><span class="sxs-lookup"><span data-stu-id="7ec67-146">Fixed the scripts to install missing PowerShell modules.</span></span>|

### <a name="version-1"></a><span data-ttu-id="7ec67-147">Version 1</span><span class="sxs-lookup"><span data-stu-id="7ec67-147">Version 1</span></span>
| <span data-ttu-id="7ec67-148">機能</span><span class="sxs-lookup"><span data-stu-id="7ec67-148">Feature</span></span> | <span data-ttu-id="7ec67-149">細目</span><span class="sxs-lookup"><span data-stu-id="7ec67-149">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="7ec67-150">初期</span><span class="sxs-lookup"><span data-stu-id="7ec67-150">Initial</span></span> | <span data-ttu-id="7ec67-151">ツールキットは LCS 共有 アセット ライブラリにアップロード済み。</span><span class="sxs-lookup"><span data-stu-id="7ec67-151">Toolkit uploaded to LCS Shared Asset Library.</span></span>|


