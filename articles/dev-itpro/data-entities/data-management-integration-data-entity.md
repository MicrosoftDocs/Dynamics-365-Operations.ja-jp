---
title: "データ エンティティを使用したデータ管理と統合"
description: "このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 26441
ms.assetid: 8aa25787-5920-4277-acff-7011200133f4
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: bf70cb93ed39c869aad7cb10e397731765c6db81
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="data-management-and-integration-by-using-data-entities"></a><span data-ttu-id="e0238-103">データ エンティティを使用したデータ管理と統合</span><span class="sxs-lookup"><span data-stu-id="e0238-103">Data management and integration by using data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0238-104">このトピックでは、同期と非同期の統合の仕組みについて簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="e0238-104">This topic provides a brief overview of the mechanics of synchronous and asynchronous integration.</span></span>

<a name="synchronous-services"></a><span data-ttu-id="e0238-105">同期サービス</span><span class="sxs-lookup"><span data-stu-id="e0238-105">Synchronous services</span></span>
--------------------

<span data-ttu-id="e0238-106">同期統合では、比較的簡単です。</span><span class="sxs-lookup"><span data-stu-id="e0238-106">Synchronous integrations are relatively straightforward.</span></span> <span data-ttu-id="e0238-107"><strong>パブリック</strong>が有効なすべてのエンティティは、次の URL: https://\[BaseURL\]/Data/&lt;&lt; データ エンティティ パブリック コレクション名&gt;&gt;のサービス アプリケーション プログラミング インターフェイス (API) として自動的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0238-107">Any entity that has <strong>Is public</strong> enabled is automatically available as a service application programming interface (API) in the following URL: https://\[BaseURL\]/Data/&lt;&lt;Data Entity Public Collection Name&gt;&gt;.</span></span>

<span data-ttu-id="e0238-108">現在、OData プロトコルは、すべての公開可能エンティティが相互作用できるエンドポイントを公開するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e0238-108">Currently, OData protocol is used to expose endpoints where all public-enabled entities can be interacted with.</span></span> <span data-ttu-id="e0238-109"><strong>サポートされているプロトコル:</strong>OData V4.0 <strong>データ形式:</strong>JSON <strong>メタデータ URL:</strong> https://\[BaseURL\]/Data/$metadata</span><span class="sxs-lookup"><span data-stu-id="e0238-109"><strong>Supported protocol:</strong> OData V4.0 <strong>Data format:</strong> JSON <strong>Metadata URL:</strong> https://\[BaseURL\]/Data/$metadata</span></span>

## <a name="data-importexport-and-recurring-integration-scenarios"></a><span data-ttu-id="e0238-110">データのインポート/エクスポートと定期的な統合のシナリオ</span><span class="sxs-lookup"><span data-stu-id="e0238-110">Data import/export and recurring integration scenarios</span></span>
<span data-ttu-id="e0238-111">データ管理プラットフォームを通じた統合では、エンティティを介したデータの挿入/抽出に関するより多くの機能と高度なスループットが提供されます。</span><span class="sxs-lookup"><span data-stu-id="e0238-111">Integration through the data management platform provides more capabilities and higher throughput for inserting/extracting data through entities.</span></span> <span data-ttu-id="e0238-112">この統合シナリオでは通常、データは次の 3 つのフェーズに分かれています。</span><span class="sxs-lookup"><span data-stu-id="e0238-112">Typically, data goes through three phases in this integration scenario:</span></span>

-   <span data-ttu-id="e0238-113">**ソース** – これらは、受信データ ファイルまたはキュー内のメッセージです。</span><span class="sxs-lookup"><span data-stu-id="e0238-113">**Source** – These are inbound data files or messages in the queue.</span></span> <span data-ttu-id="e0238-114">一般的なデータ形式には、CSV、XML、タブ区切りなどがあります。</span><span class="sxs-lookup"><span data-stu-id="e0238-114">Typical data formats include CSV, XML, and tab-delimited.</span></span>
-   <span data-ttu-id="e0238-115">**ステージング** – これらは、データ エンティティに密接にマップして自動的に生成されたテーブルです。</span><span class="sxs-lookup"><span data-stu-id="e0238-115">**Staging** – These are automatically generated tables that map closely to the data entity.</span></span> <span data-ttu-id="e0238-116">**データ管理の有効化** が **true** のときは、中間記憶を提供するステージング テーブルが生成されます。</span><span class="sxs-lookup"><span data-stu-id="e0238-116">When **Data management enabled** is **true**, staging tables are generated to provide intermediary storage.</span></span> <span data-ttu-id="e0238-117">これにより、フレームワークは大量のファイルの解析、変換、およびいくつかの検証を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e0238-117">This enables the framework to do high-volume file parsing, transformation, and some validations.</span></span>
-   <span data-ttu-id="e0238-118">**ターゲット** – これは、データをインポートするデータ エンティティです。</span><span class="sxs-lookup"><span data-stu-id="e0238-118">**Target** – This is the data entity where data will be imported.</span></span>

<span data-ttu-id="e0238-119">次の図は、着信フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="e0238-119">The following diagram shows an inbound flow.</span></span> ![受信フロー](./media/over6.png)

## <a name="known-limitations-in-data-importexport"></a><span data-ttu-id="e0238-121">データのインポート/エクスポートにおける既知の制限</span><span class="sxs-lookup"><span data-stu-id="e0238-121">Known limitations in data import/export</span></span>
<span data-ttu-id="e0238-122">テキスト ファイルをインポートするとき、文字列サイズは 32,768 文字に限定されます。</span><span class="sxs-lookup"><span data-stu-id="e0238-122">When you import text files, string sizes are limited to 32,768 characters.</span></span> <span data-ttu-id="e0238-123">文字列がこれより大きい場合は、インポートされた文字列が切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="e0238-123">If there is a string larger than this, the imported string will be truncated.</span></span> <span data-ttu-id="e0238-124">これは、基本的な実装の制限であり、SQL Server Integration Services (SSIS) によるものです。</span><span class="sxs-lookup"><span data-stu-id="e0238-124">This is a limitation in the underlying implementation and is due to SQL Server Integration Services (SSIS).</span></span>  

<span data-ttu-id="e0238-125">32,768 文字を超える文字列をインポートする必要がある場合は、コンテナー エンティティ フィールドを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0238-125">If you need to import strings that are larger than 32,768 characters, we suggest that you use container entity fields.</span></span>


<span data-ttu-id="e0238-126">詳細については、FastTrack 技術解説のビデオ: [Dynamics 365 for Operations – 技術解説: 統合](https://www.youtube.com/watch?v=fooBvQhIo6I}をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="e0238-126">For more information, watch the FastTrack Tech Talk video: [Dynamics 365 for Operations – Tech Talk: Integration](https://www.youtube.com/watch?v=fooBvQhIo6I}.</span></span>


