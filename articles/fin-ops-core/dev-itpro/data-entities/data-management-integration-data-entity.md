---
title: データ エンティティを使用したデータの管理と統合についての概要
description: このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 26441
ms.assetid: 8aa25787-5920-4277-acff-7011200133f4
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 466af74e10c5f980ad82e1fb3b6c2c3b31616416
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183429"
---
# <a name="data-management-and-integration-by-using-data-entities-overview"></a><span data-ttu-id="58fd5-103">データ エンティティを使用したデータの管理と統合についての概要</span><span class="sxs-lookup"><span data-stu-id="58fd5-103">Data management and integration by using data entities overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58fd5-104">このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="58fd5-104">This topic provides a brief overview of the mechanics of synchronous and asynchronous integration.</span></span>

## <a name="synchronous-services"></a><span data-ttu-id="58fd5-105">同期サービス</span><span class="sxs-lookup"><span data-stu-id="58fd5-105">Synchronous services</span></span>

<span data-ttu-id="58fd5-106">同期統合では、比較的簡単です。</span><span class="sxs-lookup"><span data-stu-id="58fd5-106">Synchronous integrations are relatively straightforward.</span></span> <span data-ttu-id="58fd5-107">**Is public** が有効なすべてのエンティティは、次の URL: `https://[BaseURL]/Data/<<Data Entity Public Collection Name>>` データ エンティティ パブリック コレクション名のサービス アプリケーション プログラミング インターフェイス (API) として自動的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-107">Any entity that has **Is public** enabled is automatically available as a service application programming interface (API) in the following URL: `https://[BaseURL]/Data/<<Data Entity Public Collection Name>>`.</span></span>

<span data-ttu-id="58fd5-108">現在、OData プロトコルは、すべての公開可能エンティティが相互作用できるエンドポイントを公開するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-108">Currently, OData protocol is used to expose endpoints where all public-enabled entities can be interacted with.</span></span>

<span data-ttu-id="58fd5-109">**サポートされているプロトコル:** OData V4.0</span><span class="sxs-lookup"><span data-stu-id="58fd5-109">**Supported protocol:** OData V4.0</span></span>

<span data-ttu-id="58fd5-110">**データ形式:** JSON</span><span class="sxs-lookup"><span data-stu-id="58fd5-110">**Data format:** JSON</span></span>

<span data-ttu-id="58fd5-111">**メタデータ URL:** `https://[BaseURL]/Data/$metadata`</span><span class="sxs-lookup"><span data-stu-id="58fd5-111">**Metadata URL:** `https://[BaseURL]/Data/$metadata`</span></span>

## <a name="data-importexport-and-recurring-integration-scenarios"></a><span data-ttu-id="58fd5-112">データのインポート/エクスポートと定期的な統合のシナリオ</span><span class="sxs-lookup"><span data-stu-id="58fd5-112">Data import/export and recurring integration scenarios</span></span>
<span data-ttu-id="58fd5-113">データ管理プラットフォームを通じた統合では、エンティティを介したデータの挿入/抽出に関するより多くの機能と高度なスループットが提供されます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-113">Integration through the data management platform provides more capabilities and higher throughput for inserting/extracting data through entities.</span></span> <span data-ttu-id="58fd5-114">この統合シナリオでは通常、データは次の 3 つのフェーズに分かれています。</span><span class="sxs-lookup"><span data-stu-id="58fd5-114">Typically, data goes through three phases in this integration scenario:</span></span>

- <span data-ttu-id="58fd5-115">**ソース** – これらは、受信データ ファイルまたはキュー内のメッセージです。</span><span class="sxs-lookup"><span data-stu-id="58fd5-115">**Source** – These are inbound data files or messages in the queue.</span></span> <span data-ttu-id="58fd5-116">一般的なデータ形式には、CSV、XML、タブ区切りなどがあります。</span><span class="sxs-lookup"><span data-stu-id="58fd5-116">Typical data formats include CSV, XML, and tab-delimited.</span></span>
- <span data-ttu-id="58fd5-117">**ステージング** – これらは、データ エンティティに密接にマップして自動的に生成されたテーブルです。</span><span class="sxs-lookup"><span data-stu-id="58fd5-117">**Staging** – These are automatically generated tables that map closely to the data entity.</span></span> <span data-ttu-id="58fd5-118">**データ管理の有効化** が **true** のときは、中間記憶を提供するステージング テーブルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-118">When **Data management enabled** is **true**, staging tables are generated to provide intermediary storage.</span></span> <span data-ttu-id="58fd5-119">これにより、フレームワークは大量のファイルの解析、変換、およびいくつかの検証を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-119">This enables the framework to do high-volume file parsing, transformation, and some validations.</span></span>
- <span data-ttu-id="58fd5-120">**ターゲット** – これは、データをインポートするデータ エンティティです。</span><span class="sxs-lookup"><span data-stu-id="58fd5-120">**Target** – This is the data entity where data will be imported.</span></span>

<span data-ttu-id="58fd5-121">次の図は、着信フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="58fd5-121">The following diagram shows an inbound flow.</span></span>

![受信フロー](./media/over6.png)

## <a name="known-limitations-in-data-importexport"></a><span data-ttu-id="58fd5-123">データのインポート/エクスポートにおける既知の制限</span><span class="sxs-lookup"><span data-stu-id="58fd5-123">Known limitations in data import/export</span></span>
<span data-ttu-id="58fd5-124">テキスト ファイルをインポートするとき、文字列サイズは 32,768 文字に限定されます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-124">When you import text files, string sizes are limited to 32,768 characters.</span></span> <span data-ttu-id="58fd5-125">文字列がこれより大きい場合は、インポートされた文字列が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="58fd5-125">If there is a string larger than this, the imported string will be truncated.</span></span> <span data-ttu-id="58fd5-126">これは、基本的な実装の制限であり、SQL Server Integration Services (SSIS) によるものです。</span><span class="sxs-lookup"><span data-stu-id="58fd5-126">This is a limitation in the underlying implementation and is due to SQL Server Integration Services (SSIS).</span></span>

<span data-ttu-id="58fd5-127">32,768 文字を超える文字列をインポートする必要がある場合は、コンテナー エンティティ フィールドを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="58fd5-127">If you need to import strings that are larger than 32,768 characters, we suggest that you use container entity fields.</span></span>

<span data-ttu-id="58fd5-128">詳細については、FastTrack 技術解説のビデオ: [Dynamics 365 for Operations – 技術解説: 統合](https://www.youtube.com/watch?v=fooBvQhIo6I)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="58fd5-128">For more information, watch the FastTrack Tech Talk video: [Dynamics 365 for Operations – Tech Talk: Integration](https://www.youtube.com/watch?v=fooBvQhIo6I).</span></span>