---
title: データベース移動ツールキット
description: このトピックでは、データベース移動ツールキット (開発環境環境とサンドボックス環境との間でデータを移動するためのカスタマー エクスペリエンスを高める一連のスクリプト) をダウンロードして使用する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: 2cd828a8a5874f9e26c27097e210a43336c561de
ms.sourcegitcommit: 42dbebced4a99dfe703689b7e38c3c5caecd12e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949238"
---
# <a name="database-movement-toolkit"></a><span data-ttu-id="924ee-103">データベース移動ツールキット</span><span class="sxs-lookup"><span data-stu-id="924ee-103">Database movement toolkit</span></span>

<span data-ttu-id="924ee-104">データベース移動ツールキットは、Microsoft Dynamics Lifecycle Services (LCS) にホストされる ZIP ファイルです。</span><span class="sxs-lookup"><span data-stu-id="924ee-104">The Database movement toolkit is a ZIP file hosted in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="924ee-105">このツールキットをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="924ee-105">This toolkit is available for download.</span></span> <span data-ttu-id="924ee-106">開発環境とサンドボックス環境との間でのデータ移動に関するカスタマー エクスペリエンスを高める一連のスクリプトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="924ee-106">It contains a series of scripts that enhance the customer experience for movement of data between developer environments and sandbox environments.</span></span> <span data-ttu-id="924ee-107">このトピックでは、ツールキットのコンポーネント、ダウンロード方法、および最近の変更点について説明します。</span><span class="sxs-lookup"><span data-stu-id="924ee-107">This topic explains the components of the toolkit, how to download it, and any recent changes.</span></span>

## <a name="download-the-latest-version"></a><span data-ttu-id="924ee-108">最新バージョンのダウンロード</span><span class="sxs-lookup"><span data-stu-id="924ee-108">Download the latest version</span></span>

<span data-ttu-id="924ee-109">ツールキットは、LCS 共有アセット ライブラリの**モデル** セクションで入手できます。</span><span class="sxs-lookup"><span data-stu-id="924ee-109">The toolkit is available in the LCS Shared Asset Library under the **Models** section.</span></span>  <span data-ttu-id="924ee-110">**データベース移動ツールキット**というタイトルのエントリを検索し、Tier1 DevTest 環境にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="924ee-110">Search for the entry titled **Database Movement Toolkit** and then download it to your Tier1 DevTest environment.</span></span>  

## <a name="toolkit-components"></a><span data-ttu-id="924ee-111">ツールキット コンポーネント</span><span class="sxs-lookup"><span data-stu-id="924ee-111">Toolkit components</span></span>

<span data-ttu-id="924ee-112">このツールキットには、次の主要コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="924ee-112">The toolkit contains the following primary components:</span></span>

- <span data-ttu-id="924ee-113">**Sqlpackage.exe** - このツールは Microsoft Azure SQL データベース、および Tier1 DevTest にホストされている SQL Server データベースに対して、抽出および公開アクションを実行するために使用します。</span><span class="sxs-lookup"><span data-stu-id="924ee-113">**Sqlpackage.exe** - This tool is used to perform extract and publish actions against Microsoft Azure SQL databases, as well as SQL Server databases hosted on Tier1 DevTest environments.</span></span>  
- <span data-ttu-id="924ee-114">**PowerShell 7.0** - これは、並列処理機能を含む PowerShell の自己完結型バージョンであり、環境間でのデータ転送のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="924ee-114">**PowerShell 7.0** - This is a self-contained version of PowerShell that includes capabilities for parallelism, which increases the performance of transferring data between environments.</span></span>  
- <span data-ttu-id="924ee-115">**PowerShell スクリプト** - AX 2012 データのアップグレードのようなシナリオでのエクスペリエンスを向上させ、自動化するためのスクリプトがいくつか用意されています。</span><span class="sxs-lookup"><span data-stu-id="924ee-115">**PowerShell script** - There are several scripts included to provide an enhanced and more automated experience for scenarios such as AX 2012 data upgrade.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="924ee-116">サポートされているシナリオ</span><span class="sxs-lookup"><span data-stu-id="924ee-116">Supported scenarios</span></span>

<span data-ttu-id="924ee-117">現在、このツールキットは次のシナリオをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="924ee-117">The toolkit currently supports the following scenarios.</span></span> <span data-ttu-id="924ee-118">今後、さらに追加される予定です。</span><span class="sxs-lookup"><span data-stu-id="924ee-118">More will be added over time.</span></span>  

* [<span data-ttu-id="924ee-119">AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="924ee-119">Upgrade from AX 2012 - Data upgrade in sandbox environments</span></span>](../migration-upgrade/upgrade-data-sandbox-dacpac.md)

## <a name="versions"></a><span data-ttu-id="924ee-120">バージョン</span><span class="sxs-lookup"><span data-stu-id="924ee-120">Versions</span></span>

### <a name="version-1"></a><span data-ttu-id="924ee-121">Version 1</span><span class="sxs-lookup"><span data-stu-id="924ee-121">Version 1</span></span>
| <span data-ttu-id="924ee-122">機能</span><span class="sxs-lookup"><span data-stu-id="924ee-122">Feature</span></span> | <span data-ttu-id="924ee-123">細目</span><span class="sxs-lookup"><span data-stu-id="924ee-123">Details</span></span> |
| :------ | :------ |
| <span data-ttu-id="924ee-124">初期</span><span class="sxs-lookup"><span data-stu-id="924ee-124">Initial</span></span> | <span data-ttu-id="924ee-125">ツールキットは LCS 共有 アセット ライブラリにアップロード済み。</span><span class="sxs-lookup"><span data-stu-id="924ee-125">Toolkit uploaded to LCS Shared Asset Library.</span></span>|


