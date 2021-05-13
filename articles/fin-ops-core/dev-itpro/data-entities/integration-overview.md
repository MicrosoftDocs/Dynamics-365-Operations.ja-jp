---
title: データ統合戦略の選択
description: このトピックは、設計者と開発者が統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。
author: Sunil-Garg
ms.date: 11/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8097b8d3601b182059022b22d9459d0064fd12e
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941182"
---
# <a name="choose-a-data-integration-strategy"></a><span data-ttu-id="c6d34-103">データ統合戦略の選択</span><span class="sxs-lookup"><span data-stu-id="c6d34-103">Choose a data integration strategy</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c6d34-104">このトピックは、設計者と開発者が統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-104">This topic is intended to help architects and developers make sound design decisions when they implement integration scenarios.</span></span>

<span data-ttu-id="c6d34-105">このトピックでは、統合パターン、統合シナリオ、統合ソリューション、およびベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-105">The topic describes integration patterns, integration scenarios, and integration solutions and best practices.</span></span> <span data-ttu-id="c6d34-106">ただし、すべての統合パターンを使用または設定する方法に関する技術詳細は含まれません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-106">However, it doesn't include technical details about how to use or set up every integration pattern.</span></span> <span data-ttu-id="c6d34-107">また、サンプル統合コードも含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-107">It also doesn't include sample integration code.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d34-108">パターンを選択にあたってガイダンスを示し、シナリオについて説明する際には、データのボリューム番号について言及されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-108">When providing guidance and discussing scenarios for choosing a pattern, data volume numbers are mentioned.</span></span> <span data-ttu-id="c6d34-109">これらの番号は、パターンを測定するためだけに使用する必要があり、ハードシステムの限界を意味するものではありません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-109">These numbers must be used only to gauge the pattern and must not be considered as hard system limits.</span></span> <span data-ttu-id="c6d34-110">絶対数は、実稼働環境ではさまざまな要因によって変わってきます。コンフィギュレーションはこのシナリオにおけるただ1つの側面に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-110">The absolute numbers will vary in real production environments due to various factors, configurations are only one aspect of this scenario.</span></span> 

<span data-ttu-id="c6d34-111">次のテーブルに、使用可能な統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-111">The following table lists the integration patterns that are available.</span></span>

| <span data-ttu-id="c6d34-112">パターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-112">Pattern</span></span>                       | <span data-ttu-id="c6d34-113">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="c6d34-113">Documentation</span></span> |
|-------------------------------|---------------|
| <span data-ttu-id="c6d34-114">Power Platform 統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-114">Power Platform integration</span></span>    | [<span data-ttu-id="c6d34-115">Finance and Operations アプリと Microsoft Power Platform の統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-115">Microsoft Power Platform integration with Finance and Operations apps</span></span>](../power-platform/overview.md) |
| <span data-ttu-id="c6d34-116">二重書き込み</span><span class="sxs-lookup"><span data-stu-id="c6d34-116">Dual-write</span></span>                    | [<span data-ttu-id="c6d34-117">二重書き込みの概要</span><span class="sxs-lookup"><span data-stu-id="c6d34-117">Dual-write overview</span></span>](dual-write/dual-write-home-page.md) |
| <span data-ttu-id="c6d34-118">クラシック データの統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-118">Classic data integration</span></span>      | [<span data-ttu-id="c6d34-119">クラシック データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="c6d34-119">Classic data integration overview</span></span>](data-integration-cds.md) |
| <span data-ttu-id="c6d34-120">OData</span><span class="sxs-lookup"><span data-stu-id="c6d34-120">OData</span></span>                         | [<span data-ttu-id="c6d34-121">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="c6d34-121">Open Data Protocol (OData)</span></span>](odata.md) |
| <span data-ttu-id="c6d34-122">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="c6d34-122">Batch data API</span></span>                | [<span data-ttu-id="c6d34-123">定期統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-123">Recurring integrations</span></span>](recurring-integrations.md)<br>[<span data-ttu-id="c6d34-124">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="c6d34-124">Data management package REST API</span></span>](data-management-api.md) |
| <span data-ttu-id="c6d34-125">カスタム サービス</span><span class="sxs-lookup"><span data-stu-id="c6d34-125">Custom service</span></span>                | [<span data-ttu-id="c6d34-126">カスタム サービスの開発</span><span class="sxs-lookup"><span data-stu-id="c6d34-126">Custom service development</span></span>](custom-services.md) |
| <span data-ttu-id="c6d34-127">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="c6d34-127">Consume external web services</span></span> | [<span data-ttu-id="c6d34-128">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="c6d34-128">Consume external web services</span></span>](consume-external-web-service.md) |
| <span data-ttu-id="c6d34-129">Excel 統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-129">Excel integration</span></span>             | [<span data-ttu-id="c6d34-130">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="c6d34-130">Office integration overview</span></span>](../office-integration/office-integration.md) |

> [!NOTE]
> <span data-ttu-id="c6d34-131">オンプレミス配置の場合、唯一サポートされる API は [データ管理パッケージ REST API](data-management-api.md) です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-131">For on premise deployments, the only supported API is the [Data management package REST API](data-management-api.md).</span></span> <span data-ttu-id="c6d34-132">これは、7.2、platform update 12 ビルド 7.0.4709.41184 で現在利用可能です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-132">This is currently available on 7.2, platform update 12 build 7.0.4709.41184.</span></span>

## <a name="power-platform-integration"></a><span data-ttu-id="c6d34-133">Power Platform の統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-133">Power platform integration</span></span>
<span data-ttu-id="c6d34-134">Finance and Operations は、Dataverse の仮想データ ソースであり、Dataverse および Microsoft Power Platform からの完全な作成、読み取り、更新、削除 (CRUD) 操作を可能にし ます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-134">Finance and Operations is a virtual data source in Dataverse, and enables full create, read, update, delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="c6d34-135">定義上、仮想エンティティのデータは、Dataverse には存在しません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-135">By definition, the data for virtual entities doesn't reside in Dataverse.</span></span> <span data-ttu-id="c6d34-136">代わりに、Finance and Operations には引き続き存在します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-136">Instead, it continues to reside in Finance and Operations.</span></span> <span data-ttu-id="c6d34-137">Dataverse から Finance and Operations エンティティに対して CRUD 操作を有効にするには 、エンティティを Dataverse の仮想エンティティとして使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-137">To enable CRUD operations on Finance and Operations entities from Dataverse, entities must be made available as virtual entities in Dataverse.</span></span> <span data-ttu-id="c6d34-138">これにより、Finance and Operations アプリに存在するデータに対して、Dataverse と Microsoft Power Platform から CRUD 処理を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-138">This allows CRUD operations to be performed, from Dataverse and Microsoft Power Platform, on data that resides in Finance and Operations apps.</span></span> <span data-ttu-id="c6d34-139">詳細については、[Microsoft Power Platform 統合](../power-platform/overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6d34-139">For detailed information, see [Microsoft Power Platform integration](../power-platform/overview.md).</span></span>

## <a name="dual-write-vs-classic-data-integration-patterns-vs-virtual-entities"></a><span data-ttu-id="c6d34-140">二重書き込み対クラシック データ統合のパターン対仮想エンティティ</span><span class="sxs-lookup"><span data-stu-id="c6d34-140">Dual-write vs. classic data integration patterns vs. virtual entities</span></span>

<span data-ttu-id="c6d34-141">二重書き込みにより、Dynamics 365 と Finance and Operations アプリケーションのモデル駆動型アプリケーション間で、同期、双方向、ほぼリアルタイムのエクスペリエンスが可能です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-141">Dual-write provides synchronous, bi-directional, near-real time experience between model-driven applications in Dynamics 365 and Finance and Operations applications.</span></span> <span data-ttu-id="c6d34-142">データ同期は、ほとんどまたはまったく介入を伴うことなく行われ、エンティティに対する作成、更新、および削除アクションによってトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-142">Data synchronization happens with little or no intervention and is triggered by create, update and delete actions on an entity.</span></span> <span data-ttu-id="c6d34-143">二重書き込みは、Dynamics 365 アプリケーションにまたがる対話型業務シナリオに適しています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-143">Dual-write is suitable for interactive business scenarios that span across Dynamics 365 applications.</span></span>

<span data-ttu-id="c6d34-144">クラシック データ統合により、Customer Engagement アプリと Finance and Operations アプリの間で非同期および単一方向のデータ同期エクスペリエンスが可能です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-144">Classic data integration provides asynchronous and uni-directional data synchronization experience between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="c6d34-145">IT管理者主導のエクスペリエンスであり、データ同期ジョブを特定の頻度で実行するようにスケジュールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-145">It's an IT-administrator led experience and you must schedule the data sync jobs to run on a specific cadence.</span></span> <span data-ttu-id="c6d34-146">クラシック データの統合は、Dynamics 365アプリケーション間で大量のデータの入出力を伴う業務シナリオに適しています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-146">Classic data integration is suitable for business scenarios that involves bulk ingress/egress of data across Dynamics 365 applications.</span></span>

| <span data-ttu-id="c6d34-147">パターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-147">Pattern</span></span>                       | <span data-ttu-id="c6d34-148">タイミング</span><span class="sxs-lookup"><span data-stu-id="c6d34-148">Timing</span></span>                        | <span data-ttu-id="c6d34-149">バッチ</span><span class="sxs-lookup"><span data-stu-id="c6d34-149">Batch</span></span> | <span data-ttu-id="c6d34-150">テクノロジ</span><span class="sxs-lookup"><span data-stu-id="c6d34-150">Technology</span></span> | <span data-ttu-id="c6d34-151">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="c6d34-151">Finance and Operations app</span></span> | <span data-ttu-id="c6d34-152">Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="c6d34-152">Model-driven apps in Dynamics 365</span></span> |
|-------------------------------|-------------------------------|-------|---|------|------------|
| <span data-ttu-id="c6d34-153">二重書き込み</span><span class="sxs-lookup"><span data-stu-id="c6d34-153">Dual-write</span></span>             | <span data-ttu-id="c6d34-154">同期</span><span class="sxs-lookup"><span data-stu-id="c6d34-154">Synchronous</span></span><br><span data-ttu-id="c6d34-155">双方向</span><span class="sxs-lookup"><span data-stu-id="c6d34-155">Bi-directional</span></span>   | <span data-ttu-id="c6d34-156">無</span><span class="sxs-lookup"><span data-stu-id="c6d34-156">No</span></span>    | <span data-ttu-id="c6d34-157">OData</span><span class="sxs-lookup"><span data-stu-id="c6d34-157">OData</span></span> | <span data-ttu-id="c6d34-158">Finance</span><span class="sxs-lookup"><span data-stu-id="c6d34-158">Finance</span></span><br><span data-ttu-id="c6d34-159">サプライ チェーン</span><span class="sxs-lookup"><span data-stu-id="c6d34-159">Supply Chain</span></span><br><span data-ttu-id="c6d34-160">Commerce</span><span class="sxs-lookup"><span data-stu-id="c6d34-160">Commerce</span></span><br><span data-ttu-id="c6d34-161">サービス業</span><span class="sxs-lookup"><span data-stu-id="c6d34-161">Service Industry</span></span><br><span data-ttu-id="c6d34-162">CoreHR</span><span class="sxs-lookup"><span data-stu-id="c6d34-162">CoreHR</span></span> | <span data-ttu-id="c6d34-163">Sales</span><span class="sxs-lookup"><span data-stu-id="c6d34-163">Sales</span></span><br><span data-ttu-id="c6d34-164">マーケティング</span><span class="sxs-lookup"><span data-stu-id="c6d34-164">Marketing</span></span><br><span data-ttu-id="c6d34-165">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="c6d34-165">Customer Service</span></span><br><span data-ttu-id="c6d34-166">Field Service</span><span class="sxs-lookup"><span data-stu-id="c6d34-166">Field Service</span></span><br><span data-ttu-id="c6d34-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c6d34-167">Project Service Automation</span></span><br><span data-ttu-id="c6d34-168">人材</span><span class="sxs-lookup"><span data-stu-id="c6d34-168">Talent</span></span> | 
| <span data-ttu-id="c6d34-169">クラシック データの統合</span><span class="sxs-lookup"><span data-stu-id="c6d34-169">Classic data integration</span></span> | <span data-ttu-id="c6d34-170">非同期、単一方向</span><span class="sxs-lookup"><span data-stu-id="c6d34-170">Asynchronous, uni-directional</span></span> | <span data-ttu-id="c6d34-171">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-171">Yes</span></span>   | <span data-ttu-id="c6d34-172">DIXF</span><span class="sxs-lookup"><span data-stu-id="c6d34-172">DIXF</span></span> | <span data-ttu-id="c6d34-173">Finance</span><span class="sxs-lookup"><span data-stu-id="c6d34-173">Finance</span></span><br><span data-ttu-id="c6d34-174">サプライ チェーン</span><span class="sxs-lookup"><span data-stu-id="c6d34-174">Supply Chain</span></span><br><span data-ttu-id="c6d34-175">Commerce</span><span class="sxs-lookup"><span data-stu-id="c6d34-175">Commerce</span></span><br><span data-ttu-id="c6d34-176">サービス業</span><span class="sxs-lookup"><span data-stu-id="c6d34-176">Service Industry</span></span><br><span data-ttu-id="c6d34-177">CoreHR</span><span class="sxs-lookup"><span data-stu-id="c6d34-177">CoreHR</span></span> | <span data-ttu-id="c6d34-178">Sales</span><span class="sxs-lookup"><span data-stu-id="c6d34-178">Sales</span></span><br><span data-ttu-id="c6d34-179">マーケティング</span><span class="sxs-lookup"><span data-stu-id="c6d34-179">Marketing</span></span><br><span data-ttu-id="c6d34-180">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="c6d34-180">Customer Service</span></span><br><span data-ttu-id="c6d34-181">Field Service</span><span class="sxs-lookup"><span data-stu-id="c6d34-181">Field Service</span></span><br><span data-ttu-id="c6d34-182">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c6d34-182">Project Service Automation</span></span><br><span data-ttu-id="c6d34-183">人材</span><span class="sxs-lookup"><span data-stu-id="c6d34-183">Talent</span></span> |

<span data-ttu-id="c6d34-184">仮想エンティティは、データを Dataverse に物理的にコピーすることなく、Finance and Operations で Microsoft Power Platform を使用するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-184">Virtual entities provide a mechanism to use Microsoft Power Platform with Finance and Operations without having to physically copy data to Dataverse.</span></span> <span data-ttu-id="c6d34-185">このガイダンスは、要件に二重書き込みまたはデータ統合、または仮想エンティティが必要かどうかを判断するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-185">This guidance must be used to determine if the requirements will need dual-write or data integrator or virtual entities.</span></span> <span data-ttu-id="c6d34-186">仮想エンティティと二重書き込み/データ統合は、必要に応じて併用できる補完的なテクノロジです。</span><span class="sxs-lookup"><span data-stu-id="c6d34-186">Virtual entities and dual-write/data integrator are complementary technologies such that, they can be used together if required.</span></span>

## <a name="synchronous-vs-asynchronous-integration-patterns"></a><span data-ttu-id="c6d34-187">同期および非同期の統合パターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-187">Synchronous vs. asynchronous integration patterns</span></span>

<span data-ttu-id="c6d34-188">処理は、同期または非同期にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-188">Processing can be either synchronous or asynchronous.</span></span> <span data-ttu-id="c6d34-189">多くの場合、使用すべき処理タイプは、選択した統合パターンによって決まります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-189">Often, the type of processing that you must use determines the integration pattern that you choose.</span></span>

<span data-ttu-id="c6d34-190">*同期* パターンは、ブロック要求と応答パターンであり、呼び出し先が実行を終了して応答を返すまで呼び出し元がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-190">A *synchronous* pattern is a blocking request and response pattern, where the caller is blocked until the callee has finished running and gives a response.</span></span> <span data-ttu-id="c6d34-191">*非同期* パターンは非ブロック パターンで、呼び出し元が要求を送信して応答を待たずに続行します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-191">An *asynchronous* pattern is a non-blocking pattern, where the caller submits the request and then continues without waiting for a response.</span></span>

<span data-ttu-id="c6d34-192">次のテーブルに、使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-192">The following table lists the inbound integration patterns that are available.</span></span>

| <span data-ttu-id="c6d34-193">パターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-193">Pattern</span></span>        | <span data-ttu-id="c6d34-194">タイミング</span><span class="sxs-lookup"><span data-stu-id="c6d34-194">Timing</span></span>       | <span data-ttu-id="c6d34-195">バッチ</span><span class="sxs-lookup"><span data-stu-id="c6d34-195">Batch</span></span> |
|----------------|--------------|-------|
| <span data-ttu-id="c6d34-196">OData</span><span class="sxs-lookup"><span data-stu-id="c6d34-196">OData</span></span>          | <span data-ttu-id="c6d34-197">同期</span><span class="sxs-lookup"><span data-stu-id="c6d34-197">Synchronous</span></span>  | <span data-ttu-id="c6d34-198">無</span><span class="sxs-lookup"><span data-stu-id="c6d34-198">No</span></span>    |
| <span data-ttu-id="c6d34-199">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="c6d34-199">Batch data API</span></span> | <span data-ttu-id="c6d34-200">非同期</span><span class="sxs-lookup"><span data-stu-id="c6d34-200">Asynchronous</span></span> | <span data-ttu-id="c6d34-201">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-201">Yes</span></span>   |

<span data-ttu-id="c6d34-202">同期と非同期パターンを比較する前に、すべての REST および SOAP 統合アプリケーション プログラミング インターフェイス (API) を同期または非同期で呼び出すことができるので注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-202">Before you compare synchronous and asynchronous patterns, you should be aware that all the REST and SOAP integration application programming interfaces (APIs) can be invoked either synchronously or asynchronously.</span></span>

<span data-ttu-id="c6d34-203">次の例は、このポイントを示しています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-203">The following examples illustrate this point.</span></span> <span data-ttu-id="c6d34-204">オープン データ プロトコル (OData) が統合のために使用される場合、呼び出し元がブロックされるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-204">You can't assume that the caller will be blocked when the Open Data Protocol (OData) is used for integration.</span></span> <span data-ttu-id="c6d34-205">通話の仕方によっては、呼び出し元がブロックされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-205">The caller might not be blocked, depending on how a call is made.</span></span>

| <span data-ttu-id="c6d34-206">パターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-206">Pattern</span></span>        | <span data-ttu-id="c6d34-207">同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="c6d34-207">Synchronous programming paradigm</span></span>    | <span data-ttu-id="c6d34-208">非同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="c6d34-208">Asynchronous programming paradigm</span></span> |
|----------------|-------------------------------------|-----------------------------------|
| <span data-ttu-id="c6d34-209">OData</span><span class="sxs-lookup"><span data-stu-id="c6d34-209">OData</span></span>          | <span data-ttu-id="c6d34-210">DbResourceContextSaveChanges</span><span class="sxs-lookup"><span data-stu-id="c6d34-210">DbResourceContextSaveChanges</span></span>         | <span data-ttu-id="c6d34-211">DbResourceContextSaveChangesAsync</span><span class="sxs-lookup"><span data-stu-id="c6d34-211">DbResourceContextSaveChangesAsync</span></span> |
| <span data-ttu-id="c6d34-212">カスタム サービス</span><span class="sxs-lookup"><span data-stu-id="c6d34-212">Custom service</span></span> | <span data-ttu-id="c6d34-213">httpRequestGetResponse</span><span class="sxs-lookup"><span data-stu-id="c6d34-213">httpRequestGetResponse</span></span>               | <span data-ttu-id="c6d34-214">httpRequestBeginGetResponse</span><span class="sxs-lookup"><span data-stu-id="c6d34-214">httpRequestBeginGetResponse</span></span> |
| <span data-ttu-id="c6d34-215">SOAP</span><span class="sxs-lookup"><span data-stu-id="c6d34-215">SOAP</span></span>           | <span data-ttu-id="c6d34-216">UserSessionServiceGetUserSessionInfo</span><span class="sxs-lookup"><span data-stu-id="c6d34-216">UserSessionServiceGetUserSessionInfo</span></span> | <span data-ttu-id="c6d34-217">UserSessionServiceGetUserSessionInfoAsync</span><span class="sxs-lookup"><span data-stu-id="c6d34-217">UserSessionServiceGetUserSessionInfoAsync</span></span> |
| <span data-ttu-id="c6d34-218">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="c6d34-218">Batch data API</span></span> | <span data-ttu-id="c6d34-219">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="c6d34-219">ImportFromPackage</span></span>                   | [<span data-ttu-id="c6d34-220">BeginInvoke</span><span class="sxs-lookup"><span data-stu-id="c6d34-220">BeginInvoke</span></span>](/dotnet/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously) |

<span data-ttu-id="c6d34-221">これらの API が呼び出されると、すぐにビジネス ロジックが実行されるため、OData とカスタム サービスの両方は同期統合パターンです。</span><span class="sxs-lookup"><span data-stu-id="c6d34-221">Both OData and custom services are synchronous integration patterns, because when these APIs are called, business logic is immediately run.</span></span> <span data-ttu-id="c6d34-222">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-222">Here are some examples:</span></span>

- <span data-ttu-id="c6d34-223">OData を使用して製品レコードを挿入すると、レコードはすぐに OData 呼び出しの一部として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-223">If OData is used to insert product records, the records are immediately inserted as part of the OData call.</span></span>
- <span data-ttu-id="c6d34-224">手持ちの在庫を検索するためにカスタム サービスを使用すると、ビジネス ロジックが JSON/SOAP 呼び出しの一部としてすぐに実行され、在庫総額がすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-224">If a custom service is used to look up on-hand inventory, business logic is immediately run as part of the JSON/SOAP call, and an inventory sum number is immediately returned.</span></span>

<span data-ttu-id="c6d34-225">これらの API が呼び出されると、バッチ モードでデータがインポートまたはエクスポートされるため、バッチ データ API は非同期統合パターンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-225">Batch data APIs are considered asynchronous integration patterns, because when these APIs are called, data is imported or exported in batch mode.</span></span> <span data-ttu-id="c6d34-226">たとえば、ImportFromPackage API への呼び出しは、同期することができます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-226">For example, calls to the ImportFromPackage API can be synchronous.</span></span> <span data-ttu-id="c6d34-227">ただし、API は、特定のデータ パッケージのみをインポートするバッチ ジョブをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-227">However, the API schedules a batch job to import only a specific data package.</span></span> <span data-ttu-id="c6d34-228">スケジューリング ジョブはすぐに戻され、後でバッチ ジョブで処理されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-228">The scheduling job is quickly returned, and the work is done later in a batch job.</span></span> <span data-ttu-id="c6d34-229">したがって、バッチ データ API は非同期として分類されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-229">Therefore, batch data APIs are categorized as asynchronous.</span></span>

<span data-ttu-id="c6d34-230">バッチ データ API は大量のデータのインポートとエクスポートを処理するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-230">Batch data APIs are designed to handle large-volume data imports and exports.</span></span> <span data-ttu-id="c6d34-231">大量である条件を正確に定義することは困難です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-231">It's difficult to define what exactly qualifies as a large volume.</span></span> <span data-ttu-id="c6d34-232">回答は、エンティティによって、およびインポートまたはエクスポート中に実行されるビジネス ロジックの量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-232">The answer depends on the entity, and on the amount of business logic that is run during import or export.</span></span> <span data-ttu-id="c6d34-233">ただし、経験則を次に示します: 容量が数十万レコード以上の場合は、統合のバッチ データ API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-233">However, here is a rule of thumb: If the volume is more than a few hundred thousand records, you should use the batch data API for integrations.</span></span>

<span data-ttu-id="c6d34-234">一般に、統合パターンを選択しようとしている場合、次の質問を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-234">In general, when you're trying to choose an integration pattern, we recommend that you consider the following questions:</span></span>

- <span data-ttu-id="c6d34-235">統合をリアルタイムで行う必要がある業務要件がありますか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-235">Is there a business requirement that the integration should be in real time?</span></span>
- <span data-ttu-id="c6d34-236">ピーク時のデータ量の要件は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="c6d34-236">What is the requirement for the peak data volume?</span></span>
- <span data-ttu-id="c6d34-237">頻度はどのくらいですか ?</span><span class="sxs-lookup"><span data-stu-id="c6d34-237">What is the frequency?</span></span>

### <a name="error-handling"></a><span data-ttu-id="c6d34-238">エラー処理</span><span class="sxs-lookup"><span data-stu-id="c6d34-238">Error handling</span></span> 

<span data-ttu-id="c6d34-239">同期パターンを使用するときは、呼び出し元に成功または失敗の応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-239">When you use a synchronous pattern, success or failure responses are returned to the caller.</span></span> <span data-ttu-id="c6d34-240">たとえば、OData 呼び出しが販売注文を挿入するために使用される場合、販売注文明細行に存在しない製品への無効な参照があると、呼び出し元が受信する応答には、エラー メッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-240">For example, when an OData call is used to insert sales orders, if a sales order line has a bad reference to a product that doesn't exist, the response that the caller receives contains an error message.</span></span> <span data-ttu-id="c6d34-241">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-241">The caller is responsible for handling any errors in the response.</span></span>

<span data-ttu-id="c6d34-242">非同期パターンを使用するときは、呼び出し元には、スケジューリング呼び出しが成功したかどうかを示す応答がすぐ表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-242">When you use an asynchronous pattern, the caller receives an immediate response that indicates whether the scheduling call was successful.</span></span> <span data-ttu-id="c6d34-243">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-243">The caller is responsible for handling any errors in the response.</span></span> <span data-ttu-id="c6d34-244">スケジューリングが完了したら、データのインポートまたはエクスポートのステータスは、呼び出し元にプッシュされません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-244">After scheduling is done, the status of the data import or export isn't pushed to the caller.</span></span> <span data-ttu-id="c6d34-245">呼び出し元は、対応するインポートまたはエクスポート処理の結果をポーリングし、それに応じてエラーを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-245">The caller must poll for the result of the corresponding import or export process, and must handle any errors accordingly.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-dual-write"></a><span data-ttu-id="c6d34-246">二重書き込みを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-246">Typical scenarios and patterns that use dual-write</span></span> 

<span data-ttu-id="c6d34-247">二重書き込みを使用する一般的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-247">Here are some typical scenarios that use dual-write.</span></span>

### <a name="enable-customer-service-representative-to-facilitate-change-of-address-for-finance-and-operations-customers"></a><span data-ttu-id="c6d34-248">顧客サービス担当者が Finance and Operations の顧客の住所変更を容易にできるようにする</span><span class="sxs-lookup"><span data-stu-id="c6d34-248">Enable customer service representative to facilitate change of address for Finance and Operations customers</span></span>

<span data-ttu-id="c6d34-249">顧客が移転し、請求先住所と送付先住所の情報を変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-249">A customer relocates and wishes to change their billing and shipping address information.</span></span> <span data-ttu-id="c6d34-250">この顧客は、顧客サポート担当者に連絡して、住所の変更を依頼します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-250">This customer contacts the customer support representative and requests a change of address.</span></span> <span data-ttu-id="c6d34-251">顧客サポート担当者が電話を受け、顧客の請求先住所と送付先住所を変更します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-251">The customer support representative takes the call and changes the billing and shipping address information of the customer.</span></span>

| <span data-ttu-id="c6d34-252">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-252">Decision</span></span>                    | <span data-ttu-id="c6d34-253">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-253">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="c6d34-254">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-254">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-255">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-255">Yes</span></span>                      |
| <span data-ttu-id="c6d34-256">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-256">Peak data volume</span></span>            |                          |
| <span data-ttu-id="c6d34-257">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-257">Frequency</span></span>                   | <span data-ttu-id="c6d34-258">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-258">Ad hoc</span></span>                   |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-259">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-259">Recommended solution</span></span>
<span data-ttu-id="c6d34-260">このほぼリアルタイムのデータ同期のシナリオでは、二重書き込みで実装するのが最適です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-260">This scenario of near-real time data synchronization is best implemented by dual-write.</span></span>

- <span data-ttu-id="c6d34-261">顧客情報は、Finance and Operations アプリから取得されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-261">The customer's information is sourced in a Finance and Operations app.</span></span>
- <span data-ttu-id="c6d34-262">顧客が顧客サポートに電話し、請求先住所と送付先住所の情報を変更するよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-262">A customer calls customer support and asks to change their billing and shipping address information.</span></span>
- <span data-ttu-id="c6d34-263">顧客サポート担当者は、Dynamics 365 Customer Service の顧客レコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-263">A customer support representative retrieves the customer’s record in Dynamics 365 Customer Service.</span></span>
- <span data-ttu-id="c6d34-264">顧客サポート担当者は、請求先住所と送付先住所を更新してデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-264">The customer support representative updates the billing and shipping address and saves the data.</span></span>
- <span data-ttu-id="c6d34-265">新しい請求先住所と送付先住所は、リアルタイムで Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-265">The new billing and shipping address syncs back to the Finance and Operations app in real-time.</span></span>

### <a name="sales-representatives-can-change-customer-credit-limits-without-logging-into-a-finance-and-operations-app"></a><span data-ttu-id="c6d34-266">販売担当者は、Finance and Operations アプリにログインすることなく、顧客の与信限度額を変更できます</span><span class="sxs-lookup"><span data-stu-id="c6d34-266">Sales representatives can change customer credit limits without logging into a Finance and Operations app</span></span>

<span data-ttu-id="c6d34-267">顧客には $2,000 の与信限度額があり、$5,000 に引き上げたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-267">A customer has a credit limit of $2,000 and wants to increase it to $5,000.</span></span> <span data-ttu-id="c6d34-268">この顧客は、顧客サポートに電話し、増加を依頼します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-268">This customer calls the customer support and requests the increase.</span></span> <span data-ttu-id="c6d34-269">チケットが、販売部門に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-269">The ticket is assigned to the sales department.</span></span> <span data-ttu-id="c6d34-270">販売責任者は、依頼を検討し、顧客の支払履歴を確認し、顧客が与信限度額の増加の資格があると判断します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-270">The head of sales reviews the request, checks the customer's payment history, and determines that the customer is eligible for an increased credit limit.</span></span> <span data-ttu-id="c6d34-271">販売責任者は依頼を承認し、チケットに応答します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-271">The head of sales approves the request and responds to the ticket.</span></span> <span data-ttu-id="c6d34-272">顧客は与信限度額 $5,000 の承認を通知する電子メールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-272">The customer receives an email informing the approval of $5,000 credit limit.</span></span>

| <span data-ttu-id="c6d34-273">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-273">Decision</span></span>                    | <span data-ttu-id="c6d34-274">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-274">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="c6d34-275">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-275">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-276">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-276">Yes</span></span>                      |
| <span data-ttu-id="c6d34-277">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-277">Peak data volume</span></span>            |                          |
| <span data-ttu-id="c6d34-278">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-278">Frequency</span></span>                   | <span data-ttu-id="c6d34-279">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-279">Ad hoc</span></span>                   |


#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-280">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-280">Recommended solution</span></span>

<span data-ttu-id="c6d34-281">このシナリオでは、二重書き込みで実装するのが最適です。</span><span class="sxs-lookup"><span data-stu-id="c6d34-281">This scenario is best implemented by dual-write.</span></span>

- <span data-ttu-id="c6d34-282">顧客は顧客サポートに電話し、与信限度額を $2,000 から $5,000 に引き上げたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-282">A customer calls customer support and wants to increase their credit limit from $2,000 to $5,000.</span></span>
- <span data-ttu-id="c6d34-283">顧客サポート担当者が Dynamics 365 Customer Service でチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-283">A customer support representative creates a ticket in Dynamics 365 Customer Service.</span></span>
- <span data-ttu-id="c6d34-284">このチケットが、販売部門に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-284">This ticket is assigned to the sales unit.</span></span>
- <span data-ttu-id="c6d34-285">販売部門の販売担当者が依頼を確認して、承認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-285">A sales representative from the sales unit reviews and approves the request.</span></span>
- <span data-ttu-id="c6d34-286">この結果、Dynamics 365 Sales で顧客の与信限度額が $5,000 に引き上げられました。</span><span class="sxs-lookup"><span data-stu-id="c6d34-286">This result is the increase of credit limit of the customer to $5,000 in Dynamics 365 Sales.</span></span> 
- <span data-ttu-id="c6d34-287">Finance and Operations アプリの与信限度額が $5,000 に更新されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-287">The credit limit in the Finance and operations app is updated to $5,000.</span></span>
- <span data-ttu-id="c6d34-288">販売担当者は、チケットに応答して解決します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-288">The sales representative responds to the ticket and resolves it.</span></span> 
- <span data-ttu-id="c6d34-289">顧客は、与信限度額の引き上げに関する電子メールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-289">The customer receives an email about the increased credit limit.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-odata-integrations"></a><span data-ttu-id="c6d34-290">OData 統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-290">Typical scenarios and patterns that use OData integrations</span></span>

<span data-ttu-id="c6d34-291">OData 統合を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-291">Here are some typical scenarios that use OData integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d34-292">Power BI レポートの OData の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="c6d34-292">Use of OData for Power BI reports is discouraged.</span></span> <span data-ttu-id="c6d34-293">このような状況ではエンティティ格納を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-293">Using entity store for such scenarios is encouraged.</span></span>

### <a name="create-and-update-product-information"></a><span data-ttu-id="c6d34-294">製品情報の作成および更新</span><span class="sxs-lookup"><span data-stu-id="c6d34-294">Create and update product information</span></span>

<span data-ttu-id="c6d34-295">あるメーカーでは、その製品をオンプレミスでホストされているサード パーティ製アプリケーションを使用して、定義および構成します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-295">A manufacturer defines and configures its product by using a third-party application that is hosted on-premises.</span></span> <span data-ttu-id="c6d34-296">このメーカーは、生産情報をオンプレミス アプリケーションから Finance and Operations に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-296">This manufacturer wants to move its production information from the on-premises application to Finance and Operations.</span></span> <span data-ttu-id="c6d34-297">製品が定義されるとき、またはオンプレミス アプリケーションで変更されるとき、ユーザーは、同じ変更をリアルタイムに確認できます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-297">When a product is defined, or when it's changed in the on-premises application, the user should see the same change, in real time.</span></span>

| <span data-ttu-id="c6d34-298">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-298">Decision</span></span>                    | <span data-ttu-id="c6d34-299">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-299">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="c6d34-300">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-300">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-301">はい</span><span class="sxs-lookup"><span data-stu-id="c6d34-301">Yes</span></span>                      |
| <span data-ttu-id="c6d34-302">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-302">Peak data volume</span></span>            | <span data-ttu-id="c6d34-303">時間当たり 1,000 レコード\*</span><span class="sxs-lookup"><span data-stu-id="c6d34-303">1,000 records per hour\*</span></span> |
| <span data-ttu-id="c6d34-304">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-304">Frequency</span></span>                   | <span data-ttu-id="c6d34-305">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-305">Ad hoc</span></span>                   |

<span data-ttu-id="c6d34-306">\* 場合によっては、新しいまたは変更された生産コンフィギュレーションが短時間に多く発生します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-306">\* Occasionally, many new or modified production configurations will occur in a short time.</span></span>

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-307">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-307">Recommended solution</span></span>

<span data-ttu-id="c6d34-308">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で製品情報を作成および更新することによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-308">This scenario is best implemented by using the OData service endpoints to create and update product information in Finance and Operations.</span></span>

<span data-ttu-id="c6d34-309">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-309">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-310">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-310">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="c6d34-311">OData サービス エンドポイントが同じエンティティのセットに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-311">Make sure that the OData service endpoints are available for the same set of entities.</span></span>

<span data-ttu-id="c6d34-312">サード パーティ製アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="c6d34-312">In the third-party application:</span></span>

- <span data-ttu-id="c6d34-313">製品情報がサード パーティ製アプリケーションで作成または変更されるときは、同じ変更を加えるために Finance and Operations に対して OData 呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-313">When product information is created or modified in the third-party application, an OData call is made to Finance and Operations to make the same change.</span></span>

### <a name="read-the-status-of-customer-orders"></a><span data-ttu-id="c6d34-314">客注文のステータスを読み取る</span><span class="sxs-lookup"><span data-stu-id="c6d34-314">Read the status of customer orders</span></span>

<span data-ttu-id="c6d34-315">会社は、顧客が注文の状況を確認できる自己ホストの顧客ポータルを持っています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-315">A company has a self-hosted customer portal where customers can check the status of their orders.</span></span> <span data-ttu-id="c6d34-316">注文ステータス情報は、アプリケーションで管理されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-316">Order status information is maintained in the application.</span></span>

| <span data-ttu-id="c6d34-317">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-317">Decision</span></span>                    | <span data-ttu-id="c6d34-318">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-318">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="c6d34-319">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-319">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-320">はい</span><span class="sxs-lookup"><span data-stu-id="c6d34-320">Yes</span></span>                    |
| <span data-ttu-id="c6d34-321">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-321">Peak data volume</span></span>            | <span data-ttu-id="c6d34-322">時間当たり 5,000 レコード</span><span class="sxs-lookup"><span data-stu-id="c6d34-322">5,000 records per hour</span></span> |
| <span data-ttu-id="c6d34-323">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-323">Frequency</span></span>                   | <span data-ttu-id="c6d34-324">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-324">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-325">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-325">Recommended solution</span></span>

<span data-ttu-id="c6d34-326">このシナリオは、OData サービス エンドポイントを使用して、注文ステータス情報を読み取ることによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-326">This scenario is best implemented by using the OData service endpoints to read order status information.</span></span>

<span data-ttu-id="c6d34-327">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-327">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-328">注文のステータス情報を読むために必要なエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-328">Determine the entity that is required in order to read order status information.</span></span>
- <span data-ttu-id="c6d34-329">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-329">Make sure that the OData service endpoint is available for the entity.</span></span>

<span data-ttu-id="c6d34-330">顧客のポータル サイトで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c6d34-330">On the customer portal site:</span></span>

- <span data-ttu-id="c6d34-331">顧客は注文のステータスをチェックするとき、対応する注文を読み取ってそのステータスを取得するために、Finance and Operations にリアルタイムの OData 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="c6d34-331">When a customer checks the status of an order, make a real-time OData call to Finance and Operations to read the corresponding order and retrieve its status.</span></span>

### <a name="approve-boms"></a><span data-ttu-id="c6d34-332">BOM の承認</span><span class="sxs-lookup"><span data-stu-id="c6d34-332">Approve BOMs</span></span>

<span data-ttu-id="c6d34-333">会社は、オンプレミスでホストされている製品ライフサイクル管理 (PLM) システムを使用しています。</span><span class="sxs-lookup"><span data-stu-id="c6d34-333">A company uses a product lifecycle management (PLM) system that is hosted on-premises.</span></span> <span data-ttu-id="c6d34-334">PLM システムには、承認のためにアプリケーションに完成した部品表 (BOM) 情報を送信するワークフローがあります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-334">The PLM system has a workflow that sends the finished bill of materials (BOM) information to the application for approval.</span></span>

| <span data-ttu-id="c6d34-335">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-335">Decision</span></span>                    | <span data-ttu-id="c6d34-336">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-336">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="c6d34-337">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-337">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-338">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-338">Yes</span></span>                    |
| <span data-ttu-id="c6d34-339">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-339">Peak data volume</span></span>            | <span data-ttu-id="c6d34-340">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="c6d34-340">1,000 records per hour</span></span> |
| <span data-ttu-id="c6d34-341">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-341">Frequency</span></span>                   | <span data-ttu-id="c6d34-342">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-342">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-343">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-343">Recommended solution</span></span>

<span data-ttu-id="c6d34-344">このシナリオは、OData アクションを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-344">This scenario can be implemented by using an OData action.</span></span>

<span data-ttu-id="c6d34-345">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-345">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-346">統合に必要なエンティティを決定する</span><span class="sxs-lookup"><span data-stu-id="c6d34-346">Determine the entity that is required for the integration.</span></span>
- <span data-ttu-id="c6d34-347">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-347">Make sure that the OData service endpoints are available for the entity.</span></span>
- <span data-ttu-id="c6d34-348">エンティティで、必要なビジネス ロジックを実行するアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-348">On the entity, create an action to run the required business logic.</span></span>

<span data-ttu-id="c6d34-349">PLM ソリューション:</span><span class="sxs-lookup"><span data-stu-id="c6d34-349">In the PLM solution:</span></span>

- <span data-ttu-id="c6d34-350">PLM システムで、BOM を承認する OData アクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-350">Make the PLM system invoke the OData action to approve the BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d34-351">このタイプの OData アクションは **BOMBillOfMaterialsHeaderEntity::approve** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-351">You can find an example of this type of OData action in **BOMBillOfMaterialsHeaderEntity::approve**.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-a-custom-service"></a><span data-ttu-id="c6d34-352">カスタム サービスを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-352">Typical scenarios and patterns that use a custom service</span></span>

<span data-ttu-id="c6d34-353">カスタム サービスを使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-353">Here are some typical scenarios that use a custom service.</span></span>

### <a name="look-up-on-hand-inventory"></a><span data-ttu-id="c6d34-354">手持在庫の検索</span><span class="sxs-lookup"><span data-stu-id="c6d34-354">Look up on-hand inventory</span></span>

<span data-ttu-id="c6d34-355">エネルギー会社にはヒーターのインストール ジョブをスケジュールするフィールド作業者がいます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-355">An energy company has field workers who schedule installation jobs for heaters.</span></span> <span data-ttu-id="c6d34-356">この会社はバック オフィスとサード パーティのサービスとしてのソフトウェア (SaaS) のためにアプリケーションを使用して予定をスケジューリングします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-356">This company uses the application for the back office and third-party software as a service (SaaS) to schedule appointments.</span></span> <span data-ttu-id="c6d34-357">現場作業員が予定をスケジュールするときは、ジョブに使用できるインストール パーツがあることを確認するために、引当可能在庫数を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-357">When field workers schedule appointments, they must look up inventory availability to make sure that installation parts are available for the job.</span></span>

| <span data-ttu-id="c6d34-358">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-358">Decision</span></span>                    | <span data-ttu-id="c6d34-359">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-359">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="c6d34-360">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-360">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-361">有</span><span class="sxs-lookup"><span data-stu-id="c6d34-361">Yes</span></span>                    |
| <span data-ttu-id="c6d34-362">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-362">Peak data volume</span></span>            | <span data-ttu-id="c6d34-363">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="c6d34-363">1,000 records per hour</span></span> |
| <span data-ttu-id="c6d34-364">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-364">Frequency</span></span>                   | <span data-ttu-id="c6d34-365">アドホック</span><span class="sxs-lookup"><span data-stu-id="c6d34-365">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-366">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-366">Recommended solution</span></span>

<span data-ttu-id="c6d34-367">このシナリオは、カスタム サービスを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-367">This scenario can be implemented by using a custom service.</span></span>

<span data-ttu-id="c6d34-368">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-368">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-369">特定のアイテムの現物手持在庫を計算するカスタム サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-369">Create a custom service to calculate the physical on-hand inventory for a given item.</span></span>

<span data-ttu-id="c6d34-370">スケジューリング アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="c6d34-370">In the scheduling application:</span></span>

- <span data-ttu-id="c6d34-371">選択した品目の在庫情報を取得するために、SOAP または REST を通じてカスタム サービス エンドポイントへのリアルタイムな呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="c6d34-371">Make a real-time call to a custom service endpoint, through either SOAP or REST, to retrieve inventory information for the selected item.</span></span>

> [!NOTE]
> <span data-ttu-id="c6d34-372">このタイプのカスタム サービスの例は、Retail Real Time Services が実装された **RetailTransactionServiceInventory::inventoryLookup** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-372">You can find an example of this type of custom service in the Retail Real Time Services implementation: **RetailTransactionServiceInventory::inventoryLookup**.</span></span>

<span data-ttu-id="c6d34-373">また、inventorySiteOnHand エンティティを使用して同じ結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-373">You can also use the inventorySiteOnHand entity to achieve the same result.</span></span> <span data-ttu-id="c6d34-374">場合によっては、複数のメソッドを使用して同じデータとビジネス ロジックを公開でき、すべてのメソッドが同じように有効になり効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-374">Sometimes, you can use multiple methods to expose the same data and business logic, and all the methods are equally valid and effective.</span></span> <span data-ttu-id="c6d34-375">この場合、特定のシナリオを最適に機能して、開発者が最も使いやすいメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-375">In this case, choose the method that works best for a given scenario and that a developer is most comfortable with.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-batch-data-integrations"></a><span data-ttu-id="c6d34-376">バッチ データ統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-376">Typical scenarios and patterns that use batch data integrations</span></span>

<span data-ttu-id="c6d34-377">バッチ データ API を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-377">Here are some typical scenarios that use batch data APIs.</span></span>

### <a name="import-large-volumes-of-sales-orders"></a><span data-ttu-id="c6d34-378">大量の販売注文のインポート</span><span class="sxs-lookup"><span data-stu-id="c6d34-378">Import large volumes of sales orders</span></span>

<span data-ttu-id="c6d34-379">会社は、オンプレミスを実行するフロント エンド システムから大量の販売注文を受信します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-379">A company receives a large volume of sales orders from a front-end system that runs on-premises.</span></span> <span data-ttu-id="c6d34-380">これらの注文は、定期的に処理、管理するためにアプリケーションに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-380">These orders must periodically be sent to the application for processing and management.</span></span>

| <span data-ttu-id="c6d34-381">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-381">Decision</span></span>                    | <span data-ttu-id="c6d34-382">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-382">Information</span></span>                 |
|-----------------------------|-----------------------------|
| <span data-ttu-id="c6d34-383">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-383">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-384">無</span><span class="sxs-lookup"><span data-stu-id="c6d34-384">No</span></span>                          |
| <span data-ttu-id="c6d34-385">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-385">Peak data volume</span></span>            | <span data-ttu-id="c6d34-386">時間当たり 200,000 レコード</span><span class="sxs-lookup"><span data-stu-id="c6d34-386">200,000 records per hour</span></span>    |
| <span data-ttu-id="c6d34-387">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-387">Frequency</span></span>                   | <span data-ttu-id="c6d34-388">5 分間隔で 1 回</span><span class="sxs-lookup"><span data-stu-id="c6d34-388">One time every five minutes</span></span> |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-389">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-389">Recommended solution</span></span>

<span data-ttu-id="c6d34-390">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-390">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="c6d34-391">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-391">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-392">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-392">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="c6d34-393">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-393">Make sure that data management is enabled for the entities.</span></span>

<span data-ttu-id="c6d34-394">オンプレミスシステム:</span><span class="sxs-lookup"><span data-stu-id="c6d34-394">In the on-premises system:</span></span>

- <span data-ttu-id="c6d34-395">REST バッチ データ API を使用して、ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-395">Use the REST batch data API to import files.</span></span>

### <a name="export-large-volumes-of-purchase-orders"></a><span data-ttu-id="c6d34-396">大量の発注書をエクスポート</span><span class="sxs-lookup"><span data-stu-id="c6d34-396">Export large volumes of purchase orders</span></span>

<span data-ttu-id="c6d34-397">会社は、Finance and Operations で大量の発注書を生成し、オンプレミス在庫管理システムを使用して製品を入庫します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-397">A company generates a large volume of purchase orders in Finance and Operations and uses an on-premises inventory management system to receive products.</span></span> <span data-ttu-id="c6d34-398">発注書は、Finance and Operations からオンプレミス インベントリ システムに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-398">Purchase orders must be moved from Finance and Operations to the on-premises inventory system.</span></span>

| <span data-ttu-id="c6d34-399">意思決定</span><span class="sxs-lookup"><span data-stu-id="c6d34-399">Decision</span></span>                    | <span data-ttu-id="c6d34-400">情報</span><span class="sxs-lookup"><span data-stu-id="c6d34-400">Information</span></span>               |
|-----------------------------|---------------------------|
| <span data-ttu-id="c6d34-401">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="c6d34-401">Is real-time data required?</span></span> | <span data-ttu-id="c6d34-402">無</span><span class="sxs-lookup"><span data-stu-id="c6d34-402">No</span></span>                        |
| <span data-ttu-id="c6d34-403">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="c6d34-403">Peak data volume</span></span>            | <span data-ttu-id="c6d34-404">時間当たり 300,000 レコード</span><span class="sxs-lookup"><span data-stu-id="c6d34-404">300,000 records per hour</span></span>  |
| <span data-ttu-id="c6d34-405">頻度</span><span class="sxs-lookup"><span data-stu-id="c6d34-405">Frequency</span></span>                   | <span data-ttu-id="c6d34-406">1 時間あたり 1 回</span><span class="sxs-lookup"><span data-stu-id="c6d34-406">One time per hour</span></span>         |

#### <a name="recommended-solution"></a><span data-ttu-id="c6d34-407">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="c6d34-407">Recommended solution</span></span>

<span data-ttu-id="c6d34-408">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-408">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="c6d34-409">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="c6d34-409">In Finance and Operations:</span></span>

- <span data-ttu-id="c6d34-410">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-410">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="c6d34-411">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-411">Make sure that data management is enabled for the entities.</span></span>
- <span data-ttu-id="c6d34-412">差分プッシュする必要がある場合は、エンティティの変更履歴を有効にできるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-412">If incremental push is required, make sure that change tracking can be enabled on the entities.</span></span>

<span data-ttu-id="c6d34-413">オンプレミス在庫システム:</span><span class="sxs-lookup"><span data-stu-id="c6d34-413">In the on-premises inventory system:</span></span>

- <span data-ttu-id="c6d34-414">REST バッチ データ API を使用して、Finance and Operations からファイルをエクスポートし、在庫システムにインポートします。</span><span class="sxs-lookup"><span data-stu-id="c6d34-414">Use the REST batch data API to export the file from Finance and Operations and import it into the inventory system.</span></span>

## <a name="typical-scenarios-and-patterns-that-call-external-web-services"></a><span data-ttu-id="c6d34-415">外部の Web サービスを呼び出す一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="c6d34-415">Typical scenarios and patterns that call external web services</span></span>

<span data-ttu-id="c6d34-416">通常、アプリケーションはオンプレミスまたは別の SaaS プロバイダーによってホストされている外部 Web サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-416">It's typical that the application calls out to an external web service that is hosted either on-premises or by another SaaS provider.</span></span> <span data-ttu-id="c6d34-417">この場合、アプリケーションは統合クライアントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-417">In this case, the application acts as the integration client.</span></span> <span data-ttu-id="c6d34-418">統合クライアントを作成するときは、他のアプリケーションの統合クライアントを作成するときと同じベスト プラクティスおよびガイドラインのセットに従ってください。</span><span class="sxs-lookup"><span data-stu-id="c6d34-418">When you write an integration client, you should follow the same set of best practices and guidelines that you follow when you write an integration client for any other application.</span></span> <span data-ttu-id="c6d34-419">単純な例として、 [外部 Web サービスの使用](consume-external-web-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6d34-419">For a simple example, see [Consume external web services](consume-external-web-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6d34-420">セキュリティ要件のため、運用およびサンドボックス環境では、トランスポート層セキュリティ (TLS) 1.2 以降を使用するセキュリティ保護された通信のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-420">Because of security requirements, production and sandbox environments support only secured communication that uses Transport Layer Security (TLS) 1.2 or later.</span></span> <span data-ttu-id="c6d34-421">つまり、アプリケーションが呼び出すターゲットの Web サービス エンドポイントは、TLS 1.2 以降をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-421">In other words, the target web service endpoint that the application calls out to must support TLS 1.2 or later.</span></span> <span data-ttu-id="c6d34-422">ターゲット サービス エンドポイントがこの要件を満たしていない場合、呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="c6d34-422">If the target service endpoint doesn't meet this requirement, calls fail.</span></span> <span data-ttu-id="c6d34-423">例外エラー メッセージは、次のメッセージのようになります。</span><span class="sxs-lookup"><span data-stu-id="c6d34-423">The exception error message resembles the following message:</span></span>
>
> <span data-ttu-id="c6d34-424">*「転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。」*</span><span class="sxs-lookup"><span data-stu-id="c6d34-424">*Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.*</span></span>
>
> <span data-ttu-id="c6d34-425">TLS 1.2 またはそれ以降のバージョンを使用することが原因で対象サービスを変更できない場合は、次の図に示すように、ブローカー サービスを導入して 2 ホップ コールを行うことでこの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="c6d34-425">If you can't modify the target service so that it uses TLS 1.2 or later, you can work around this issue by introducing a broker service and making a two-hop call, as shown in the following illustration.</span></span>
>
> ![TLS の要件](./media/integration-tls.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]