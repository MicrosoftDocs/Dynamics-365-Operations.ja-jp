---
title: データ統合戦略の選択
description: このトピックは、設計者と開発者が統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。
author: Sunil-Garg
manager: AnnBe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 178c0528c9139b607412e9d95366e539c4703cad
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112227"
---
# <a name="choose-a-data-integration-strategy"></a><span data-ttu-id="12e1e-103">データ統合戦略の選択</span><span class="sxs-lookup"><span data-stu-id="12e1e-103">Choose a data integration strategy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12e1e-104">このトピックは、設計者と開発者が統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-104">This topic is intended to help architects and developers make sound design decisions when they implement integration scenarios.</span></span>

<span data-ttu-id="12e1e-105">このトピックでは、統合パターン、統合シナリオ、統合ソリューション、およびベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-105">The topic describes integration patterns, integration scenarios, and integration solutions and best practices.</span></span> <span data-ttu-id="12e1e-106">ただし、すべての統合パターンを使用または設定する方法に関する技術詳細は含まれません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-106">However, it doesn't include technical details about how to use or set up every integration pattern.</span></span> <span data-ttu-id="12e1e-107">また、サンプル統合コードも含まれていません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-107">It also doesn't include sample integration code.</span></span>

> [!NOTE]
> <span data-ttu-id="12e1e-108">パターンを選択にあたってガイダンスを示し、シナリオについて説明する際には、データのボリューム番号について言及されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-108">When providing guidance and discussing scenarios for choosing a pattern, data volume numbers are mentioned.</span></span> <span data-ttu-id="12e1e-109">これらの番号は、パターンを測定するためだけに使用する必要があり、ハードシステムの限界を意味するものではありません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-109">These numbers must be used only to gauge the pattern and must not be considered as hard system limits.</span></span> <span data-ttu-id="12e1e-110">絶対数は、実稼働環境ではさまざまな要因によって変わってきます。コンフィギュレーションはこのシナリオにおけるただ1つの側面に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-110">The absolute numbers will vary in real production environments due to various factors, configurations are only one aspect of this scenario.</span></span> 

<span data-ttu-id="12e1e-111">次のテーブルに、使用可能な統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-111">The following table lists the integration patterns that are available.</span></span>

| <span data-ttu-id="12e1e-112">パターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-112">Pattern</span></span>                       | <span data-ttu-id="12e1e-113">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="12e1e-113">Documentation</span></span> |
|-------------------------------|---------------|
| <span data-ttu-id="12e1e-114">二重書き込み</span><span class="sxs-lookup"><span data-stu-id="12e1e-114">Dual-write</span></span>                    | [<span data-ttu-id="12e1e-115">二重書き込みの概要</span><span class="sxs-lookup"><span data-stu-id="12e1e-115">Dual-write overview</span></span>](dual-write/dual-write-home-page.md) |
| <span data-ttu-id="12e1e-116">クラシック データの統合</span><span class="sxs-lookup"><span data-stu-id="12e1e-116">Classic data integration</span></span>      | [<span data-ttu-id="12e1e-117">クラシック データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="12e1e-117">Classic data integration overview</span></span>](data-integration-cds.md) |
| <span data-ttu-id="12e1e-118">OData</span><span class="sxs-lookup"><span data-stu-id="12e1e-118">OData</span></span>                         | [<span data-ttu-id="12e1e-119">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="12e1e-119">Open Data Protocol (OData)</span></span>](odata.md) |
| <span data-ttu-id="12e1e-120">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="12e1e-120">Batch data API</span></span>                | [<span data-ttu-id="12e1e-121">定期統合</span><span class="sxs-lookup"><span data-stu-id="12e1e-121">Recurring integrations</span></span>](recurring-integrations.md)<br>[<span data-ttu-id="12e1e-122">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="12e1e-122">Data management package REST API</span></span>](data-management-api.md) |
| <span data-ttu-id="12e1e-123">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="12e1e-123">Custom service</span></span>                | [<span data-ttu-id="12e1e-124">顧客サービスの開発</span><span class="sxs-lookup"><span data-stu-id="12e1e-124">Custom service development</span></span>](custom-services.md) |
| <span data-ttu-id="12e1e-125">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="12e1e-125">Consume external web services</span></span> | [<span data-ttu-id="12e1e-126">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="12e1e-126">Consume external web services</span></span>](consume-external-web-service.md) |
| <span data-ttu-id="12e1e-127">Excel 統合</span><span class="sxs-lookup"><span data-stu-id="12e1e-127">Excel integration</span></span>             | [<span data-ttu-id="12e1e-128">Office 統合の概要</span><span class="sxs-lookup"><span data-stu-id="12e1e-128">Office integration overview</span></span>](../office-integration/office-integration.md) |

> [!NOTE]
> <span data-ttu-id="12e1e-129">オンプレミス配置の場合、唯一サポートされる API は [データ管理パッケージ REST API](data-management-api.md) です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-129">For on premise deployments, the only supported API is the [Data management package REST API](data-management-api.md).</span></span> <span data-ttu-id="12e1e-130">これは、7.2、platform update 12 ビルド 7.0.4709.41184 で現在利用可能です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-130">This is currently available on 7.2, platform update 12 build 7.0.4709.41184.</span></span>

## <a name="dual-write-vs-classic-data-integration-patterns"></a><span data-ttu-id="12e1e-131">二重書き込み と クラシック データ統合のパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-131">Dual-write vs. classic data integration patterns</span></span>

<span data-ttu-id="12e1e-132">二重書き込みにより、Dynamics 365 と Finance and Operations アプリケーションのモデル駆動型アプリケーション間で、同期、双方向、ほぼリアルタイムのエクスペリエンスが可能です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-132">Dual-write provides synchronous, bi-directional, near-real time experience between model-driven applications in Dynamics 365 and Finance and Operations applications.</span></span> <span data-ttu-id="12e1e-133">データ同期は、ほとんどまたはまったく介入を伴うことなく行われ、エンティティに対する作成、更新、および削除アクションによってトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-133">Data synchronization happens with little or no intervention and is triggered by create, update and delete actions on an entity.</span></span> <span data-ttu-id="12e1e-134">二重書き込みは、Dynamics 365 アプリケーションにまたがる対話型業務シナリオに適しています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-134">Dual-write is suitable for interactive business scenarios that span across Dynamics 365 applications.</span></span>

<span data-ttu-id="12e1e-135">クラシック データ統合により、Dynamics 365 と Dynamics 365 Finance and Operations アプリケーションのモデル駆動型アプリケーションの間で非同期および単一方向のデータ同期エクスペリエンスが可能です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-135">Classic data integration provides asynchronous and uni-directional data synchronization experience between model-driven applications in Dynamics 365 and Dynamics 365 Finance and Operations applications.</span></span> <span data-ttu-id="12e1e-136">IT管理者主導のエクスペリエンスであり、データ同期ジョブを特定の頻度で実行するようにスケジュールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-136">It's an IT-administrator led experience and you must schedule the data sync jobs to run on a specific cadence.</span></span> <span data-ttu-id="12e1e-137">クラシック データの統合は、Dynamics 365アプリケーション間で大量のデータの入出力を伴う業務シナリオに適しています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-137">Classic data integration is suitable for business scenarios that involves bulk ingress/egress of data across Dynamics 365 applications.</span></span>

| <span data-ttu-id="12e1e-138">パターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-138">Pattern</span></span>                       | <span data-ttu-id="12e1e-139">タイミング</span><span class="sxs-lookup"><span data-stu-id="12e1e-139">Timing</span></span>                        | <span data-ttu-id="12e1e-140">バッチ</span><span class="sxs-lookup"><span data-stu-id="12e1e-140">Batch</span></span> | <span data-ttu-id="12e1e-141">テクノロジ</span><span class="sxs-lookup"><span data-stu-id="12e1e-141">Technology</span></span> | <span data-ttu-id="12e1e-142">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="12e1e-142">Finance and Operations app</span></span> | <span data-ttu-id="12e1e-143">Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="12e1e-143">Model-driven apps in Dynamics 365</span></span> |
|-------------------------------|-------------------------------|-------|---|
| <span data-ttu-id="12e1e-144">二重書き込み</span><span class="sxs-lookup"><span data-stu-id="12e1e-144">Dual-write</span></span>             | <span data-ttu-id="12e1e-145">同期</span><span class="sxs-lookup"><span data-stu-id="12e1e-145">Synchronous</span></span><br><span data-ttu-id="12e1e-146">双方向</span><span class="sxs-lookup"><span data-stu-id="12e1e-146">Bi-directional</span></span>   | <span data-ttu-id="12e1e-147">無</span><span class="sxs-lookup"><span data-stu-id="12e1e-147">No</span></span>    | <span data-ttu-id="12e1e-148">OData</span><span class="sxs-lookup"><span data-stu-id="12e1e-148">OData</span></span> | <span data-ttu-id="12e1e-149">Finance</span><span class="sxs-lookup"><span data-stu-id="12e1e-149">Finance</span></span><br><span data-ttu-id="12e1e-150">サプライ チェーン</span><span class="sxs-lookup"><span data-stu-id="12e1e-150">Supply Chain</span></span><br><span data-ttu-id="12e1e-151">Commerce</span><span class="sxs-lookup"><span data-stu-id="12e1e-151">Commerce</span></span><br><span data-ttu-id="12e1e-152">サービス業</span><span class="sxs-lookup"><span data-stu-id="12e1e-152">Service Industry</span></span><br><span data-ttu-id="12e1e-153">CoreHR</span><span class="sxs-lookup"><span data-stu-id="12e1e-153">CoreHR</span></span> | <span data-ttu-id="12e1e-154">Sales</span><span class="sxs-lookup"><span data-stu-id="12e1e-154">Sales</span></span><br><span data-ttu-id="12e1e-155">マーケティング</span><span class="sxs-lookup"><span data-stu-id="12e1e-155">Marketing</span></span><br><span data-ttu-id="12e1e-156">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="12e1e-156">Customer Service</span></span><br><span data-ttu-id="12e1e-157">Field Service</span><span class="sxs-lookup"><span data-stu-id="12e1e-157">Field Service</span></span><br><span data-ttu-id="12e1e-158">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12e1e-158">Project Service Automation</span></span><br><span data-ttu-id="12e1e-159">人材</span><span class="sxs-lookup"><span data-stu-id="12e1e-159">Talent</span></span> | 
| <span data-ttu-id="12e1e-160">クラシック データの統合</span><span class="sxs-lookup"><span data-stu-id="12e1e-160">Classic data integration</span></span> | <span data-ttu-id="12e1e-161">非同期、単一方向</span><span class="sxs-lookup"><span data-stu-id="12e1e-161">Asynchronous, uni-directional</span></span> | <span data-ttu-id="12e1e-162">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-162">Yes</span></span>   | <span data-ttu-id="12e1e-163">DIXF</span><span class="sxs-lookup"><span data-stu-id="12e1e-163">DIXF</span></span> | <span data-ttu-id="12e1e-164">Finance</span><span class="sxs-lookup"><span data-stu-id="12e1e-164">Finance</span></span><br><span data-ttu-id="12e1e-165">サプライ チェーン</span><span class="sxs-lookup"><span data-stu-id="12e1e-165">Supply Chain</span></span><br><span data-ttu-id="12e1e-166">Commerce</span><span class="sxs-lookup"><span data-stu-id="12e1e-166">Commerce</span></span><br><span data-ttu-id="12e1e-167">サービス業</span><span class="sxs-lookup"><span data-stu-id="12e1e-167">Service Industry</span></span><br><span data-ttu-id="12e1e-168">CoreHR</span><span class="sxs-lookup"><span data-stu-id="12e1e-168">CoreHR</span></span> | <span data-ttu-id="12e1e-169">Sales</span><span class="sxs-lookup"><span data-stu-id="12e1e-169">Sales</span></span><br><span data-ttu-id="12e1e-170">マーケティング</span><span class="sxs-lookup"><span data-stu-id="12e1e-170">Marketing</span></span><br><span data-ttu-id="12e1e-171">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="12e1e-171">Customer Service</span></span><br><span data-ttu-id="12e1e-172">Field Service</span><span class="sxs-lookup"><span data-stu-id="12e1e-172">Field Service</span></span><br><span data-ttu-id="12e1e-173">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="12e1e-173">Project Service Automation</span></span><br><span data-ttu-id="12e1e-174">人材</span><span class="sxs-lookup"><span data-stu-id="12e1e-174">Talent</span></span> |


## <a name="synchronous-vs-asynchronous-integration-patterns"></a><span data-ttu-id="12e1e-175">同期および非同期の統合パターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-175">Synchronous vs. asynchronous integration patterns</span></span>

<span data-ttu-id="12e1e-176">処理は、同期または非同期にすることができます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-176">Processing can be either synchronous or asynchronous.</span></span> <span data-ttu-id="12e1e-177">多くの場合、使用すべき処理タイプは、選択した統合パターンによって決まります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-177">Often, the type of processing that you must use determines the integration pattern that you choose.</span></span>

<span data-ttu-id="12e1e-178">*同期*パターンは、ブロック要求と応答パターンであり、呼び出し先が実行を終了して応答を返すまで呼び出し元がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-178">A *synchronous* pattern is a blocking request and response pattern, where the caller is blocked until the callee has finished running and gives a response.</span></span> <span data-ttu-id="12e1e-179">*非同期*パターンは非ブロック パターンで、呼び出し元が要求を送信して応答を待たずに続行します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-179">An *asynchronous* pattern is a non-blocking pattern, where the caller submits the request and then continues without waiting for a response.</span></span>

<span data-ttu-id="12e1e-180">次のテーブルに、使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-180">The following table lists the inbound integration patterns that are available.</span></span>

| <span data-ttu-id="12e1e-181">パターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-181">Pattern</span></span>        | <span data-ttu-id="12e1e-182">タイミング</span><span class="sxs-lookup"><span data-stu-id="12e1e-182">Timing</span></span>       | <span data-ttu-id="12e1e-183">バッチ</span><span class="sxs-lookup"><span data-stu-id="12e1e-183">Batch</span></span> |
|----------------|--------------|-------|
| <span data-ttu-id="12e1e-184">OData</span><span class="sxs-lookup"><span data-stu-id="12e1e-184">OData</span></span>          | <span data-ttu-id="12e1e-185">同期</span><span class="sxs-lookup"><span data-stu-id="12e1e-185">Synchronous</span></span>  | <span data-ttu-id="12e1e-186">無</span><span class="sxs-lookup"><span data-stu-id="12e1e-186">No</span></span>    |
| <span data-ttu-id="12e1e-187">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="12e1e-187">Batch data API</span></span> | <span data-ttu-id="12e1e-188">非同期</span><span class="sxs-lookup"><span data-stu-id="12e1e-188">Asynchronous</span></span> | <span data-ttu-id="12e1e-189">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-189">Yes</span></span>   |

<span data-ttu-id="12e1e-190">同期と非同期パターンを比較する前に、すべての REST および SOAP 統合アプリケーション プログラミング インターフェイス (API) を同期または非同期で呼び出すことができるので注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-190">Before you compare synchronous and asynchronous patterns, you should be aware that all the REST and SOAP integration application programming interfaces (APIs) can be invoked either synchronously or asynchronously.</span></span>

<span data-ttu-id="12e1e-191">次の例は、このポイントを示しています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-191">The following examples illustrate this point.</span></span> <span data-ttu-id="12e1e-192">オープン データ プロトコル (OData) が統合のために使用される場合、呼び出し元がブロックされるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-192">You can't assume that the caller will be blocked when the Open Data Protocol (OData) is used for integration.</span></span> <span data-ttu-id="12e1e-193">通話の仕方によっては、呼び出し元がブロックされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-193">The caller might not be blocked, depending on how a call is made.</span></span>

| <span data-ttu-id="12e1e-194">パターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-194">Pattern</span></span>        | <span data-ttu-id="12e1e-195">同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="12e1e-195">Synchronous programming paradigm</span></span>    | <span data-ttu-id="12e1e-196">非同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="12e1e-196">Asynchronous programming paradigm</span></span> |
|----------------|-------------------------------------|-----------------------------------|
| <span data-ttu-id="12e1e-197">OData</span><span class="sxs-lookup"><span data-stu-id="12e1e-197">OData</span></span>          | <span data-ttu-id="12e1e-198">DbResourceContextSaveChanges</span><span class="sxs-lookup"><span data-stu-id="12e1e-198">DbResourceContextSaveChanges</span></span>         | <span data-ttu-id="12e1e-199">DbResourceContextSaveChangesAsync</span><span class="sxs-lookup"><span data-stu-id="12e1e-199">DbResourceContextSaveChangesAsync</span></span> |
| <span data-ttu-id="12e1e-200">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="12e1e-200">Custom service</span></span> | <span data-ttu-id="12e1e-201">httpRequestGetResponse</span><span class="sxs-lookup"><span data-stu-id="12e1e-201">httpRequestGetResponse</span></span>               | <span data-ttu-id="12e1e-202">httpRequestBeginGetResponse</span><span class="sxs-lookup"><span data-stu-id="12e1e-202">httpRequestBeginGetResponse</span></span> |
| <span data-ttu-id="12e1e-203">SOAP</span><span class="sxs-lookup"><span data-stu-id="12e1e-203">SOAP</span></span>           | <span data-ttu-id="12e1e-204">UserSessionServiceGetUserSessionInfo</span><span class="sxs-lookup"><span data-stu-id="12e1e-204">UserSessionServiceGetUserSessionInfo</span></span> | <span data-ttu-id="12e1e-205">UserSessionServiceGetUserSessionInfoAsync</span><span class="sxs-lookup"><span data-stu-id="12e1e-205">UserSessionServiceGetUserSessionInfoAsync</span></span> |
| <span data-ttu-id="12e1e-206">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="12e1e-206">Batch data API</span></span> | <span data-ttu-id="12e1e-207">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="12e1e-207">ImportFromPackage</span></span>                   | [<span data-ttu-id="12e1e-208">BeginInvoke</span><span class="sxs-lookup"><span data-stu-id="12e1e-208">BeginInvoke</span></span>](/dotnet/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously) |

<span data-ttu-id="12e1e-209">これらの API が呼び出されると、すぐにビジネス ロジックが実行されるため、OData とカスタム サービスの両方は同期統合パターンです。</span><span class="sxs-lookup"><span data-stu-id="12e1e-209">Both OData and custom services are synchronous integration patterns, because when these APIs are called, business logic is immediately run.</span></span> <span data-ttu-id="12e1e-210">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-210">Here are some examples:</span></span>

- <span data-ttu-id="12e1e-211">OData を使用して製品レコードを挿入すると、レコードはすぐに OData 呼び出しの一部として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-211">If OData is used to insert product records, the records are immediately inserted as part of the OData call.</span></span>
- <span data-ttu-id="12e1e-212">手持ちの在庫を検索するためにカスタム サービスを使用すると、ビジネス ロジックが JSON/SOAP 呼び出しの一部としてすぐに実行され、在庫総額がすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-212">If a custom service is used to look up on-hand inventory, business logic is immediately run as part of the JSON/SOAP call, and an inventory sum number is immediately returned.</span></span>

<span data-ttu-id="12e1e-213">これらの API が呼び出されると、バッチ モードでデータがインポートまたはエクスポートされるため、バッチ データ API は非同期統合パターンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-213">Batch data APIs are considered asynchronous integration patterns, because when these APIs are called, data is imported or exported in batch mode.</span></span> <span data-ttu-id="12e1e-214">たとえば、ImportFromPackage API への呼び出しは、同期することができます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-214">For example, calls to the ImportFromPackage API can be synchronous.</span></span> <span data-ttu-id="12e1e-215">ただし、API は、特定のデータ パッケージのみをインポートするバッチ ジョブをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-215">However, the API schedules a batch job to import only a specific data package.</span></span> <span data-ttu-id="12e1e-216">スケジューリング ジョブはすぐに戻され、後でバッチ ジョブで処理されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-216">The scheduling job is quickly returned, and the work is done later in a batch job.</span></span> <span data-ttu-id="12e1e-217">したがって、バッチ データ API は非同期として分類されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-217">Therefore, batch data APIs are categorized as asynchronous.</span></span>

<span data-ttu-id="12e1e-218">バッチ データ API は大量のデータのインポートとエクスポートを処理するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-218">Batch data APIs are designed to handle large-volume data imports and exports.</span></span> <span data-ttu-id="12e1e-219">大量である条件を正確に定義することは困難です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-219">It's difficult to define what exactly qualifies as a large volume.</span></span> <span data-ttu-id="12e1e-220">回答は、エンティティによって、およびインポートまたはエクスポート中に実行されるビジネス ロジックの量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-220">The answer depends on the entity, and on the amount of business logic that is run during import or export.</span></span> <span data-ttu-id="12e1e-221">ただし、経験則を次に示します: 容量が数十万レコード以上の場合は、統合のバッチ データ API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-221">However, here is a rule of thumb: If the volume is more than a few hundred thousand records, you should use the batch data API for integrations.</span></span>

<span data-ttu-id="12e1e-222">一般に、統合パターンを選択しようとしている場合、次の質問を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-222">In general, when you're trying to choose an integration pattern, we recommend that you consider the following questions:</span></span>

- <span data-ttu-id="12e1e-223">統合をリアルタイムで行う必要がある業務要件がありますか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-223">Is there a business requirement that the integration should be in real time?</span></span>
- <span data-ttu-id="12e1e-224">ピーク時のデータ量の要件は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="12e1e-224">What is the requirement for the peak data volume?</span></span>
- <span data-ttu-id="12e1e-225">頻度はどのくらいですか ?</span><span class="sxs-lookup"><span data-stu-id="12e1e-225">What is the frequency?</span></span>

### <a name="error-handling"></a><span data-ttu-id="12e1e-226">エラー処理</span><span class="sxs-lookup"><span data-stu-id="12e1e-226">Error handling</span></span> 

<span data-ttu-id="12e1e-227">同期パターンを使用するときは、呼び出し元に成功または失敗の応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-227">When you use a synchronous pattern, success or failure responses are returned to the caller.</span></span> <span data-ttu-id="12e1e-228">たとえば、OData 呼び出しが販売注文を挿入するために使用される場合、販売注文明細行に存在しない製品への無効な参照があると、呼び出し元が受信する応答には、エラー メッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-228">For example, when an OData call is used to insert sales orders, if a sales order line has a bad reference to a product that doesn't exist, the response that the caller receives contains an error message.</span></span> <span data-ttu-id="12e1e-229">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-229">The caller is responsible for handling any errors in the response.</span></span>

<span data-ttu-id="12e1e-230">非同期パターンを使用するときは、呼び出し元には、スケジューリング呼び出しが成功したかどうかを示す応答がすぐ表示されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-230">When you use an asynchronous pattern, the caller receives an immediate response that indicates whether the scheduling call was successful.</span></span> <span data-ttu-id="12e1e-231">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-231">The caller is responsible for handling any errors in the response.</span></span> <span data-ttu-id="12e1e-232">スケジューリングが完了したら、データのインポートまたはエクスポートのステータスは、呼び出し元にプッシュされません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-232">After scheduling is done, the status of the data import or export isn't pushed to the caller.</span></span> <span data-ttu-id="12e1e-233">呼び出し元は、対応するインポートまたはエクスポート処理の結果をポーリングし、それに応じてエラーを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-233">The caller must poll for the result of the corresponding import or export process, and must handle any errors accordingly.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-dual-write"></a><span data-ttu-id="12e1e-234">二重書き込みを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-234">Typical scenarios and patterns that use dual-write</span></span> 

<span data-ttu-id="12e1e-235">二重書き込みを使用する一般的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-235">Here are some typical scenarios that use dual-write.</span></span>

### <a name="enable-customer-service-representative-to-facilitate-change-of-address-for-finance-and-operations-customers"></a><span data-ttu-id="12e1e-236">顧客サービス担当者が Finance and Operations の顧客の住所変更を容易にできるようにする</span><span class="sxs-lookup"><span data-stu-id="12e1e-236">Enable customer service representative to facilitate change of address for Finance and Operations customers</span></span>

<span data-ttu-id="12e1e-237">顧客が移転し、請求先住所と送付先住所の情報を変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-237">A customer relocates and wishes to change their billing and shipping address information.</span></span> <span data-ttu-id="12e1e-238">この顧客は、顧客サポート担当者に連絡して、住所の変更を依頼します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-238">This customer contacts the customer support representative and requests a change of address.</span></span> <span data-ttu-id="12e1e-239">顧客サポート担当者が電話を受け、顧客の請求先住所と送付先住所を変更します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-239">The customer support representative takes the call and changes the billing and shipping address information of the customer.</span></span>

| <span data-ttu-id="12e1e-240">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-240">Decision</span></span>                    | <span data-ttu-id="12e1e-241">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-241">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="12e1e-242">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-242">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-243">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-243">Yes</span></span>                      |
| <span data-ttu-id="12e1e-244">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-244">Peak data volume</span></span>            |                          |
| <span data-ttu-id="12e1e-245">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-245">Frequency</span></span>                   | <span data-ttu-id="12e1e-246">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-246">Ad hoc</span></span>                   |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-247">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-247">Recommended solution</span></span>
<span data-ttu-id="12e1e-248">このほぼリアルタイムのデータ同期のシナリオでは、二重書き込みで実装するのが最適です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-248">This scenario of near-real time data synchronization is best implemented by dual-write.</span></span>

- <span data-ttu-id="12e1e-249">顧客情報は、Finance and Operations アプリから取得されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-249">The customer's information is sourced in a Finance and Operations app.</span></span>
- <span data-ttu-id="12e1e-250">顧客が顧客サポートに電話し、請求先住所と送付先住所の情報を変更するよう依頼します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-250">A customer calls customer support and asks to change their billing and shipping address information.</span></span>
- <span data-ttu-id="12e1e-251">顧客サポート担当者は、Dynamics 365 Customer Service の顧客レコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-251">A customer support representative retrieves the customer’s record in Dynamics 365 Customer Service.</span></span>
- <span data-ttu-id="12e1e-252">顧客サポート担当者は、請求先住所と送付先住所を更新してデータを保存します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-252">The customer support representative updates the billing and shipping address and saves the data.</span></span>
- <span data-ttu-id="12e1e-253">新しい請求先住所と送付先住所は、リアルタイムで Finance and Operations アプリに同期されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-253">The new billing and shipping address syncs back to the Finance and Operations app in real-time.</span></span>

### <a name="sales-representatives-can-change-customer-credit-limits-without-logging-into-a-finance-and-operations-app"></a><span data-ttu-id="12e1e-254">販売担当者は、Finance and Operations アプリにログインすることなく、顧客の与信限度額を変更できます</span><span class="sxs-lookup"><span data-stu-id="12e1e-254">Sales representatives can change customer credit limits without logging into a Finance and Operations app</span></span>

<span data-ttu-id="12e1e-255">顧客には $2,000 の与信限度額があり、$5,000 に引き上げたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-255">A customer has a credit limit of $2,000 and wants to increase it to $5,000.</span></span> <span data-ttu-id="12e1e-256">この顧客は、顧客サポートに電話し、増加を依頼します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-256">This customer calls the customer support and requests the increase.</span></span> <span data-ttu-id="12e1e-257">チケットが、販売部門に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-257">The ticket is assigned to the sales department.</span></span> <span data-ttu-id="12e1e-258">販売責任者は、依頼を検討し、顧客の支払履歴を確認し、顧客が与信限度額の増加の資格があると判断します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-258">The head of sales reviews the request, checks the customer's payment history, and determines that the customer is eligible for an increased credit limit.</span></span> <span data-ttu-id="12e1e-259">販売責任者は依頼を承認し、チケットに応答します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-259">The head of sales approves the request and responds to the ticket.</span></span> <span data-ttu-id="12e1e-260">顧客は与信限度額 $5,000 の承認を通知する電子メールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-260">The customer receives an email informing the approval of $5,000 credit limit.</span></span>

| <span data-ttu-id="12e1e-261">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-261">Decision</span></span>                    | <span data-ttu-id="12e1e-262">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-262">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="12e1e-263">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-263">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-264">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-264">Yes</span></span>                      |
| <span data-ttu-id="12e1e-265">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-265">Peak data volume</span></span>            |                          |
| <span data-ttu-id="12e1e-266">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-266">Frequency</span></span>                   | <span data-ttu-id="12e1e-267">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-267">Ad hoc</span></span>                   |


#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-268">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-268">Recommended solution</span></span>

<span data-ttu-id="12e1e-269">このシナリオでは、二重書き込みで実装するのが最適です。</span><span class="sxs-lookup"><span data-stu-id="12e1e-269">This scenario is best implemented by dual-write.</span></span>

- <span data-ttu-id="12e1e-270">顧客は顧客サポートに電話し、与信限度額を $2,000 から $5,000 に引き上げたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-270">A customer calls customer support and wants to increase their credit limit from $2,000 to $5,000.</span></span>
- <span data-ttu-id="12e1e-271">顧客サポート担当者が Dynamics 365 Customer Service でチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-271">A customer support representative creates a ticket in Dynamics 365 Customer Service.</span></span>
- <span data-ttu-id="12e1e-272">このチケットが、販売部門に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-272">This ticket is assigned to the sales unit.</span></span>
- <span data-ttu-id="12e1e-273">販売部門の販売担当者が依頼を確認して、承認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-273">A sales representative from the sales unit reviews and approves the request.</span></span>
- <span data-ttu-id="12e1e-274">この結果、Dynamics 365 Sales で顧客の与信限度額が $5,000 に引き上げられました。</span><span class="sxs-lookup"><span data-stu-id="12e1e-274">This result is the increase of credit limit of the customer to $5,000 in Dynamics 365 Sales.</span></span> 
- <span data-ttu-id="12e1e-275">Finance and Operations アプリの与信限度額が $5,000 に更新されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-275">The credit limit in the Finance and operations app is updated to $5,000.</span></span>
- <span data-ttu-id="12e1e-276">販売担当者は、チケットに応答して解決します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-276">The sales representative responds to the ticket and resolves it.</span></span> 
- <span data-ttu-id="12e1e-277">顧客は、与信限度額の引き上げに関する電子メールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-277">The customer receives an email about the increased credit limit.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-odata-integrations"></a><span data-ttu-id="12e1e-278">OData 統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-278">Typical scenarios and patterns that use OData integrations</span></span>

<span data-ttu-id="12e1e-279">OData 統合を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-279">Here are some typical scenarios that use OData integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="12e1e-280">Power BI レポートの OData の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="12e1e-280">Use of OData for Power BI reports is discouraged.</span></span> <span data-ttu-id="12e1e-281">このような状況ではエンティティ格納を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-281">Using entity store for such scenarios is encouraged.</span></span>

### <a name="create-and-update-product-information"></a><span data-ttu-id="12e1e-282">製品情報の作成および更新</span><span class="sxs-lookup"><span data-stu-id="12e1e-282">Create and update product information</span></span>

<span data-ttu-id="12e1e-283">あるメーカーでは、その製品をオンプレミスでホストされているサード パーティ製アプリケーションを使用して、定義および構成します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-283">A manufacturer defines and configures its product by using a third-party application that is hosted on-premises.</span></span> <span data-ttu-id="12e1e-284">このメーカーは、生産情報をオンプレミス アプリケーションから Finance and Operations に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-284">This manufacturer wants to move its production information from the on-premises application to Finance and Operations.</span></span> <span data-ttu-id="12e1e-285">製品が定義されるとき、またはオンプレミス アプリケーションで変更されるとき、ユーザーは、同じ変更をリアルタイムに確認できます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-285">When a product is defined, or when it's changed in the on-premises application, the user should see the same change, in real time.</span></span>

| <span data-ttu-id="12e1e-286">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-286">Decision</span></span>                    | <span data-ttu-id="12e1e-287">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-287">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="12e1e-288">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-288">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-289">はい</span><span class="sxs-lookup"><span data-stu-id="12e1e-289">Yes</span></span>                      |
| <span data-ttu-id="12e1e-290">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-290">Peak data volume</span></span>            | <span data-ttu-id="12e1e-291">時間当たり 1,000 レコード\*</span><span class="sxs-lookup"><span data-stu-id="12e1e-291">1,000 records per hour\*</span></span> |
| <span data-ttu-id="12e1e-292">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-292">Frequency</span></span>                   | <span data-ttu-id="12e1e-293">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-293">Ad hoc</span></span>                   |

<span data-ttu-id="12e1e-294">\* 場合によっては、新しいまたは変更された生産コンフィギュレーションが短時間に多く発生します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-294">\* Occasionally, many new or modified production configurations will occur in a short time.</span></span>

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-295">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-295">Recommended solution</span></span>

<span data-ttu-id="12e1e-296">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で製品情報を作成および更新することによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-296">This scenario is best implemented by using the OData service endpoints to create and update product information in Finance and Operations.</span></span>

<span data-ttu-id="12e1e-297">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-297">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-298">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-298">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="12e1e-299">OData サービス エンドポイントが同じエンティティのセットに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-299">Make sure that the OData service endpoints are available for the same set of entities.</span></span>

<span data-ttu-id="12e1e-300">サード パーティ製アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="12e1e-300">In the third-party application:</span></span>

- <span data-ttu-id="12e1e-301">製品情報がサード パーティ製アプリケーションで作成または変更されるときは、同じ変更を加えるために Finance and Operations に対して OData 呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-301">When product information is created or modified in the third-party application, an OData call is made to Finance and Operations to make the same change.</span></span>

### <a name="read-the-status-of-customer-orders"></a><span data-ttu-id="12e1e-302">客注文のステータスを読み取る</span><span class="sxs-lookup"><span data-stu-id="12e1e-302">Read the status of customer orders</span></span>

<span data-ttu-id="12e1e-303">会社は、顧客が注文の状況を確認できる自己ホストの顧客ポータルを持っています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-303">A company has a self-hosted customer portal where customers can check the status of their orders.</span></span> <span data-ttu-id="12e1e-304">注文ステータス情報は、アプリケーションで管理されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-304">Order status information is maintained in the application.</span></span>

| <span data-ttu-id="12e1e-305">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-305">Decision</span></span>                    | <span data-ttu-id="12e1e-306">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-306">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="12e1e-307">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-307">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-308">はい</span><span class="sxs-lookup"><span data-stu-id="12e1e-308">Yes</span></span>                    |
| <span data-ttu-id="12e1e-309">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-309">Peak data volume</span></span>            | <span data-ttu-id="12e1e-310">時間当たり 5,000 レコード</span><span class="sxs-lookup"><span data-stu-id="12e1e-310">5,000 records per hour</span></span> |
| <span data-ttu-id="12e1e-311">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-311">Frequency</span></span>                   | <span data-ttu-id="12e1e-312">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-312">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-313">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-313">Recommended solution</span></span>

<span data-ttu-id="12e1e-314">このシナリオは、OData サービス エンドポイントを使用して、注文ステータス情報を読み取ることによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-314">This scenario is best implemented by using the OData service endpoints to read order status information.</span></span>

<span data-ttu-id="12e1e-315">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-315">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-316">注文のステータス情報を読むために必要なエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-316">Determine the entity that is required in order to read order status information.</span></span>
- <span data-ttu-id="12e1e-317">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-317">Make sure that the OData service endpoint is available for the entity.</span></span>

<span data-ttu-id="12e1e-318">顧客のポータル サイトで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="12e1e-318">On the customer portal site:</span></span>

- <span data-ttu-id="12e1e-319">顧客は注文のステータスをチェックするとき、対応する注文を読み取ってそのステータスを取得するために、Finance and Operations にリアルタイムの OData 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="12e1e-319">When a customer checks the status of an order, make a real-time OData call to Finance and Operations to read the corresponding order and retrieve its status.</span></span>

### <a name="approve-boms"></a><span data-ttu-id="12e1e-320">BOM の承認</span><span class="sxs-lookup"><span data-stu-id="12e1e-320">Approve BOMs</span></span>

<span data-ttu-id="12e1e-321">会社は、オンプレミスでホストされている製品ライフサイクル管理 (PLM) システムを使用しています。</span><span class="sxs-lookup"><span data-stu-id="12e1e-321">A company uses a product lifecycle management (PLM) system that is hosted on-premises.</span></span> <span data-ttu-id="12e1e-322">PLM システムには、承認のためにアプリケーションに完成した部品表 (BOM) 情報を送信するワークフローがあります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-322">The PLM system has a workflow that sends the finished bill of materials (BOM) information to the application for approval.</span></span>

| <span data-ttu-id="12e1e-323">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-323">Decision</span></span>                    | <span data-ttu-id="12e1e-324">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-324">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="12e1e-325">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-325">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-326">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-326">Yes</span></span>                    |
| <span data-ttu-id="12e1e-327">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-327">Peak data volume</span></span>            | <span data-ttu-id="12e1e-328">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="12e1e-328">1,000 records per hour</span></span> |
| <span data-ttu-id="12e1e-329">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-329">Frequency</span></span>                   | <span data-ttu-id="12e1e-330">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-330">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-331">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-331">Recommended solution</span></span>

<span data-ttu-id="12e1e-332">このシナリオは、OData アクションを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-332">This scenario can be implemented by using an OData action.</span></span>

<span data-ttu-id="12e1e-333">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-333">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-334">統合に必要なエンティティを決定する</span><span class="sxs-lookup"><span data-stu-id="12e1e-334">Determine the entity that is required for the integration.</span></span>
- <span data-ttu-id="12e1e-335">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-335">Make sure that the OData service endpoints are available for the entity.</span></span>
- <span data-ttu-id="12e1e-336">エンティティで、必要なビジネス ロジックを実行するアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-336">On the entity, create an action to run the required business logic.</span></span>

<span data-ttu-id="12e1e-337">PLM ソリューション:</span><span class="sxs-lookup"><span data-stu-id="12e1e-337">In the PLM solution:</span></span>

- <span data-ttu-id="12e1e-338">PLM システムで、BOM を承認する OData アクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-338">Make the PLM system invoke the OData action to approve the BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="12e1e-339">このタイプの OData アクションは **BOMBillOfMaterialsHeaderEntity::approve** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-339">You can find an example of this type of OData action in **BOMBillOfMaterialsHeaderEntity::approve**.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-a-custom-service"></a><span data-ttu-id="12e1e-340">カスタム サービスを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-340">Typical scenarios and patterns that use a custom service</span></span>

<span data-ttu-id="12e1e-341">カスタム サービスを使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-341">Here are some typical scenarios that use a custom service.</span></span>

### <a name="look-up-on-hand-inventory"></a><span data-ttu-id="12e1e-342">手持在庫の検索</span><span class="sxs-lookup"><span data-stu-id="12e1e-342">Look up on-hand inventory</span></span>

<span data-ttu-id="12e1e-343">エネルギー会社にはヒーターのインストール ジョブをスケジュールするフィールド作業者がいます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-343">An energy company has field workers who schedule installation jobs for heaters.</span></span> <span data-ttu-id="12e1e-344">この会社はバック オフィスとサード パーティのサービスとしてのソフトウェア (SaaS) のためにアプリケーションを使用して予定をスケジューリングします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-344">This company uses the application for the back office and third-party software as a service (SaaS) to schedule appointments.</span></span> <span data-ttu-id="12e1e-345">現場作業員が予定をスケジュールするときは、ジョブに使用できるインストール パーツがあることを確認するために、引当可能在庫数を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-345">When field workers schedule appointments, they must look up inventory availability to make sure that installation parts are available for the job.</span></span>

| <span data-ttu-id="12e1e-346">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-346">Decision</span></span>                    | <span data-ttu-id="12e1e-347">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-347">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="12e1e-348">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-348">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-349">有</span><span class="sxs-lookup"><span data-stu-id="12e1e-349">Yes</span></span>                    |
| <span data-ttu-id="12e1e-350">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-350">Peak data volume</span></span>            | <span data-ttu-id="12e1e-351">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="12e1e-351">1,000 records per hour</span></span> |
| <span data-ttu-id="12e1e-352">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-352">Frequency</span></span>                   | <span data-ttu-id="12e1e-353">アドホック</span><span class="sxs-lookup"><span data-stu-id="12e1e-353">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-354">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-354">Recommended solution</span></span>

<span data-ttu-id="12e1e-355">このシナリオは、カスタム サービスを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-355">This scenario can be implemented by using a custom service.</span></span>

<span data-ttu-id="12e1e-356">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-356">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-357">特定のアイテムの現物手持在庫を計算するカスタム サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-357">Create a custom service to calculate the physical on-hand inventory for a given item.</span></span>

<span data-ttu-id="12e1e-358">スケジューリング アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="12e1e-358">In the scheduling application:</span></span>

- <span data-ttu-id="12e1e-359">選択した品目の在庫情報を取得するために、SOAP または REST を通じてカスタム サービス エンドポイントへのリアルタイムな呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="12e1e-359">Make a real-time call to a custom service endpoint, through either SOAP or REST, to retrieve inventory information for the selected item.</span></span>

> [!NOTE]
> <span data-ttu-id="12e1e-360">このタイプのカスタム サービスの例は、Retail Real Time Services が実装された **RetailTransactionServiceInventory::inventoryLookup** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-360">You can find an example of this type of custom service in the Retail Real Time Services implementation: **RetailTransactionServiceInventory::inventoryLookup**.</span></span>

<span data-ttu-id="12e1e-361">また、inventorySiteOnHand エンティティを使用して同じ結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-361">You can also use the inventorySiteOnHand entity to achieve the same result.</span></span> <span data-ttu-id="12e1e-362">場合によっては、複数のメソッドを使用して同じデータとビジネス ロジックを公開でき、すべてのメソッドが同じように有効になり効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-362">Sometimes, you can use multiple methods to expose the same data and business logic, and all the methods are equally valid and effective.</span></span> <span data-ttu-id="12e1e-363">この場合、特定のシナリオを最適に機能して、開発者が最も使いやすいメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-363">In this case, choose the method that works best for a given scenario and that a developer is most comfortable with.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-batch-data-integrations"></a><span data-ttu-id="12e1e-364">バッチ データ統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-364">Typical scenarios and patterns that use batch data integrations</span></span>

<span data-ttu-id="12e1e-365">バッチ データ API を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-365">Here are some typical scenarios that use batch data APIs.</span></span>

### <a name="import-large-volumes-of-sales-orders"></a><span data-ttu-id="12e1e-366">大量の販売注文のインポート</span><span class="sxs-lookup"><span data-stu-id="12e1e-366">Import large volumes of sales orders</span></span>

<span data-ttu-id="12e1e-367">会社は、オンプレミスを実行するフロント エンド システムから大量の販売注文を受信します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-367">A company receives a large volume of sales orders from a front-end system that runs on-premises.</span></span> <span data-ttu-id="12e1e-368">これらの注文は、定期的に処理、管理するためにアプリケーションに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-368">These orders must periodically be sent to the application for processing and management.</span></span>

| <span data-ttu-id="12e1e-369">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-369">Decision</span></span>                    | <span data-ttu-id="12e1e-370">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-370">Information</span></span>                 |
|-----------------------------|-----------------------------|
| <span data-ttu-id="12e1e-371">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-371">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-372">無</span><span class="sxs-lookup"><span data-stu-id="12e1e-372">No</span></span>                          |
| <span data-ttu-id="12e1e-373">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-373">Peak data volume</span></span>            | <span data-ttu-id="12e1e-374">時間当たり 200,000 レコード</span><span class="sxs-lookup"><span data-stu-id="12e1e-374">200,000 records per hour</span></span>    |
| <span data-ttu-id="12e1e-375">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-375">Frequency</span></span>                   | <span data-ttu-id="12e1e-376">5 分間隔で 1 回</span><span class="sxs-lookup"><span data-stu-id="12e1e-376">One time every five minutes</span></span> |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-377">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-377">Recommended solution</span></span>

<span data-ttu-id="12e1e-378">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-378">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="12e1e-379">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-379">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-380">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-380">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="12e1e-381">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-381">Make sure that data management is enabled for the entities.</span></span>

<span data-ttu-id="12e1e-382">オンプレミスシステム:</span><span class="sxs-lookup"><span data-stu-id="12e1e-382">In the on-premises system:</span></span>

- <span data-ttu-id="12e1e-383">REST バッチ データ API を使用して、ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-383">Use the REST batch data API to import files.</span></span>

### <a name="export-large-volumes-of-purchase-orders"></a><span data-ttu-id="12e1e-384">大量の発注書をエクスポート</span><span class="sxs-lookup"><span data-stu-id="12e1e-384">Export large volumes of purchase orders</span></span>

<span data-ttu-id="12e1e-385">会社は、Finance and Operations で大量の発注書を生成し、オンプレミス在庫管理システムを使用して製品を入庫します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-385">A company generates a large volume of purchase orders in Finance and Operations and uses an on-premises inventory management system to receive products.</span></span> <span data-ttu-id="12e1e-386">発注書は、Finance and Operations からオンプレミス インベントリ システムに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-386">Purchase orders must be moved from Finance and Operations to the on-premises inventory system.</span></span>

| <span data-ttu-id="12e1e-387">意思決定</span><span class="sxs-lookup"><span data-stu-id="12e1e-387">Decision</span></span>                    | <span data-ttu-id="12e1e-388">情報</span><span class="sxs-lookup"><span data-stu-id="12e1e-388">Information</span></span>               |
|-----------------------------|---------------------------|
| <span data-ttu-id="12e1e-389">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="12e1e-389">Is real-time data required?</span></span> | <span data-ttu-id="12e1e-390">無</span><span class="sxs-lookup"><span data-stu-id="12e1e-390">No</span></span>                        |
| <span data-ttu-id="12e1e-391">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="12e1e-391">Peak data volume</span></span>            | <span data-ttu-id="12e1e-392">時間当たり 300,000 レコード</span><span class="sxs-lookup"><span data-stu-id="12e1e-392">300,000 records per hour</span></span>  |
| <span data-ttu-id="12e1e-393">頻度</span><span class="sxs-lookup"><span data-stu-id="12e1e-393">Frequency</span></span>                   | <span data-ttu-id="12e1e-394">1 時間あたり 1 回</span><span class="sxs-lookup"><span data-stu-id="12e1e-394">One time per hour</span></span>         |

#### <a name="recommended-solution"></a><span data-ttu-id="12e1e-395">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="12e1e-395">Recommended solution</span></span>

<span data-ttu-id="12e1e-396">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-396">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="12e1e-397">Finance and Operations の場合:</span><span class="sxs-lookup"><span data-stu-id="12e1e-397">In Finance and Operations:</span></span>

- <span data-ttu-id="12e1e-398">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-398">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="12e1e-399">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-399">Make sure that data management is enabled for the entities.</span></span>
- <span data-ttu-id="12e1e-400">差分プッシュする必要がある場合は、エンティティの変更履歴を有効にできるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-400">If incremental push is required, make sure that change tracking can be enabled on the entities.</span></span>

<span data-ttu-id="12e1e-401">オンプレミス在庫システム:</span><span class="sxs-lookup"><span data-stu-id="12e1e-401">In the on-premises inventory system:</span></span>

- <span data-ttu-id="12e1e-402">REST バッチ データ API を使用して、Finance and Operations からファイルをエクスポートし、在庫システムにインポートします。</span><span class="sxs-lookup"><span data-stu-id="12e1e-402">Use the REST batch data API to export the file from Finance and Operations and import it into the inventory system.</span></span>

## <a name="typical-scenarios-and-patterns-that-call-external-web-services"></a><span data-ttu-id="12e1e-403">外部の Web サービスを呼び出す一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="12e1e-403">Typical scenarios and patterns that call external web services</span></span>

<span data-ttu-id="12e1e-404">通常、アプリケーションはオンプレミスまたは別の SaaS プロバイダーによってホストされている外部 Web サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-404">It's typical that the application calls out to an external web service that is hosted either on-premises or by another SaaS provider.</span></span> <span data-ttu-id="12e1e-405">この場合、アプリケーションは統合クライアントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-405">In this case, the application acts as the integration client.</span></span> <span data-ttu-id="12e1e-406">統合クライアントを作成するときは、他のアプリケーションの統合クライアントを作成するときと同じベスト プラクティスおよびガイドラインのセットに従ってください。</span><span class="sxs-lookup"><span data-stu-id="12e1e-406">When you write an integration client, you should follow the same set of best practices and guidelines that you follow when you write an integration client for any other application.</span></span> <span data-ttu-id="12e1e-407">単純な例として、 [外部 Web サービスの使用](consume-external-web-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12e1e-407">For a simple example, see [Consume external web services](consume-external-web-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12e1e-408">セキュリティ要件のため、運用およびサンドボックス環境では、トランスポート層セキュリティ (TLS) 1.2 以降を使用するセキュリティ保護された通信のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-408">Because of security requirements, production and sandbox environments support only secured communication that uses Transport Layer Security (TLS) 1.2 or later.</span></span> <span data-ttu-id="12e1e-409">つまり、アプリケーションが呼び出すターゲットの Web サービス エンドポイントは、TLS 1.2 以降をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-409">In other words, the target web service endpoint that the application calls out to must support TLS 1.2 or later.</span></span> <span data-ttu-id="12e1e-410">ターゲット サービス エンドポイントがこの要件を満たしていない場合、呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="12e1e-410">If the target service endpoint doesn't meet this requirement, calls fail.</span></span> <span data-ttu-id="12e1e-411">例外エラー メッセージは、次のメッセージのようになります。</span><span class="sxs-lookup"><span data-stu-id="12e1e-411">The exception error message resembles the following message:</span></span>
>
> <span data-ttu-id="12e1e-412">*「転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。」*</span><span class="sxs-lookup"><span data-stu-id="12e1e-412">*Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.*</span></span>
>
> <span data-ttu-id="12e1e-413">TLS 1.2 またはそれ以降のバージョンを使用することが原因で対象サービスを変更できない場合は、次の図に示すように、ブローカー サービスを導入して 2 ホップ コールを行うことでこの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="12e1e-413">If you can't modify the target service so that it uses TLS 1.2 or later, you can work around this issue by introducing a broker service and making a two-hop call, as shown in the following illustration.</span></span>
>
> ![TLS の要件](./media/integration-tls.png)
