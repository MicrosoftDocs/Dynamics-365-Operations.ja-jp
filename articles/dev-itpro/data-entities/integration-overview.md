---
title: データ統合方法 (インポート/エクスポート) の選択
description: このトピックは、設計者と開発者が Microsoft Dynamics 365 for Finance and Operations の統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2189b0488d9b65c410b3febefff1041c101b13c
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2019
ms.locfileid: "1689037"
---
# <a name="choose-a-data-integration-importexport-strategy"></a><span data-ttu-id="a8c3b-103">データ統合方法 (インポート/エクスポート) の選択</span><span class="sxs-lookup"><span data-stu-id="a8c3b-103">Choose a data integration (import/export) strategy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8c3b-104">このトピックは、設計者と開発者が Microsoft Dynamics 365 for Finance and Operations の統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-104">This topic is intended to help architects and developers make sound design decisions when they implement integration scenarios for Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a8c3b-105">このトピックでは、統合パターン、統合シナリオ、統合ソリューション、Finance and Operations のベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-105">The topic describes integration patterns, integration scenarios, and integration solutions and best practices for Finance and Operations.</span></span> <span data-ttu-id="a8c3b-106">ただし、すべての統合パターンを使用または設定する方法に関する技術詳細は含まれません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-106">However, it doesn't include technical details about how to use or set up every integration pattern.</span></span> <span data-ttu-id="a8c3b-107">また、サンプル統合コードも含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-107">It also doesn't include sample integration code.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c3b-108">パターンを選択にあたってガイダンスを示し、シナリオについて説明する際には、データのボリューム番号について言及されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-108">When providing guidance and discussing scenarios for choosing a pattern, data volume numbers are mentioned.</span></span> <span data-ttu-id="a8c3b-109">これらの番号は、パターンを測定するためだけに使用されるものであり、ハードシステムの機能限界を意味するものではありません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-109">These numbers must be only used to gauge the pattern and must not be considered as hard system limits.</span></span> <span data-ttu-id="a8c3b-110">絶対数は、実稼働環境ではさまざまな要因によって変わってきます。コンフィギュレーションはこのシナリオにおけるただ1つの側面に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-110">The absolute numbers will vary in real production environments due to various factors, configurations are only one aspect of this scenario.</span></span> 

<span data-ttu-id="a8c3b-111">次のテーブルに、Finance and Operations で使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-111">The following table lists the integration patterns that are available for Finance and Operations.</span></span>

| <span data-ttu-id="a8c3b-112">パターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-112">Pattern</span></span>                       | <span data-ttu-id="a8c3b-113">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="a8c3b-113">Documentation</span></span> |
|-------------------------------|---------------|
| <span data-ttu-id="a8c3b-114">OData</span><span class="sxs-lookup"><span data-stu-id="a8c3b-114">OData</span></span>                         | [<span data-ttu-id="a8c3b-115">OData</span><span class="sxs-lookup"><span data-stu-id="a8c3b-115">OData</span></span>](odata.md) |
| <span data-ttu-id="a8c3b-116">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="a8c3b-116">Batch data API</span></span>                | [<span data-ttu-id="a8c3b-117">定期統合</span><span class="sxs-lookup"><span data-stu-id="a8c3b-117">Recurring integrations</span></span>](recurring-integrations.md)<br>[<span data-ttu-id="a8c3b-118">データ パッケージ API</span><span class="sxs-lookup"><span data-stu-id="a8c3b-118">Data package API</span></span>](data-management-api.md) |
| <span data-ttu-id="a8c3b-119">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="a8c3b-119">Custom service</span></span>                | [<span data-ttu-id="a8c3b-120">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="a8c3b-120">Custom services</span></span>](custom-services.md) |
| <span data-ttu-id="a8c3b-121">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="a8c3b-121">Consume external web services</span></span> | [<span data-ttu-id="a8c3b-122">外部 Web サービスの使用</span><span class="sxs-lookup"><span data-stu-id="a8c3b-122">Consuming external web services</span></span>](consume-external-web-service.md) |
| <span data-ttu-id="a8c3b-123">Excel 統合</span><span class="sxs-lookup"><span data-stu-id="a8c3b-123">Excel integration</span></span>             | [<span data-ttu-id="a8c3b-124">Office 統合</span><span class="sxs-lookup"><span data-stu-id="a8c3b-124">Office integration</span></span>](../office-integration/office-integration.md) |

> [!NOTE]
> <span data-ttu-id="a8c3b-125">オンプレミス配置の場合、唯一サポートされる API は[データ パッケージ API](data-management-api.md) です。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-125">For on premise deployments, the only supported API is the [Data package API](data-management-api.md).</span></span> <span data-ttu-id="a8c3b-126">これは、7.2、platform update 12 ビルド 7.0.4709.41184 で現在利用可能です。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-126">This is currently available on 7.2, platform update 12 build 7.0.4709.41184.</span></span>

## <a name="synchronous-vs-asynchronous-integration-patterns"></a><span data-ttu-id="a8c3b-127">同期および非同期の統合パターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-127">Synchronous vs. asynchronous integration patterns</span></span>

<span data-ttu-id="a8c3b-128">処理は、同期または非同期にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-128">Processing can be either synchronous or asynchronous.</span></span> <span data-ttu-id="a8c3b-129">多くの場合、使用すべき処理タイプは、選択した統合パターンによって決まります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-129">Often, the type of processing that you must use determines the integration pattern that you choose.</span></span>

<span data-ttu-id="a8c3b-130">*同期*パターンは、ブロック要求と応答パターンであり、呼び出し先が実行を終了して応答を返すまで呼び出し元がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-130">A *synchronous* pattern is a blocking request and response pattern, where the caller is blocked until the callee has finished running and gives a response.</span></span> <span data-ttu-id="a8c3b-131">*非同期*パターンは非ブロック パターンで、呼び出し元が要求を送信して応答を待たずに続行します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-131">An *asynchronous* pattern is a non-blocking pattern, where the caller submits the request and then continues without waiting for a response.</span></span>

<span data-ttu-id="a8c3b-132">次のテーブルに、使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-132">The following table lists the inbound integration patterns that are available.</span></span>

| <span data-ttu-id="a8c3b-133">パターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-133">Pattern</span></span>        | <span data-ttu-id="a8c3b-134">タイミング</span><span class="sxs-lookup"><span data-stu-id="a8c3b-134">Timing</span></span>       | <span data-ttu-id="a8c3b-135">バッチ</span><span class="sxs-lookup"><span data-stu-id="a8c3b-135">Batch</span></span> |
|----------------|--------------|-------|
| <span data-ttu-id="a8c3b-136">OData</span><span class="sxs-lookup"><span data-stu-id="a8c3b-136">OData</span></span>          | <span data-ttu-id="a8c3b-137">同期</span><span class="sxs-lookup"><span data-stu-id="a8c3b-137">Synchronous</span></span>  | <span data-ttu-id="a8c3b-138">無</span><span class="sxs-lookup"><span data-stu-id="a8c3b-138">No</span></span>    |
| <span data-ttu-id="a8c3b-139">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="a8c3b-139">Batch data API</span></span> | <span data-ttu-id="a8c3b-140">非同期</span><span class="sxs-lookup"><span data-stu-id="a8c3b-140">Asynchronous</span></span> | <span data-ttu-id="a8c3b-141">有</span><span class="sxs-lookup"><span data-stu-id="a8c3b-141">Yes</span></span>   |

<span data-ttu-id="a8c3b-142">同期と非同期パターンを比較する前に、Finance and Operations が提供するすべての REST および SOAP 統合アプリケーション プログラミング インターフェイス (API) を同期または非同期で呼び出すことができるので注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-142">Before you compare synchronous and asynchronous patterns, you should be aware that all the REST and SOAP integration application programming interfaces (APIs) that Finance and Operations provides can be invoked either synchronously or asynchronously.</span></span>

<span data-ttu-id="a8c3b-143">次の例は、このポイントを示しています。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-143">The following examples illustrate this point.</span></span> <span data-ttu-id="a8c3b-144">オープン データ プロトコル (OData) が統合のために使用される場合、呼び出し元がブロックされるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-144">You can't assume that the caller will be blocked when the Open Data Protocol (OData) is used for integration.</span></span> <span data-ttu-id="a8c3b-145">通話の仕方によっては、呼び出し元がブロックされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-145">The caller might not be blocked, depending on how a call is made.</span></span>

| <span data-ttu-id="a8c3b-146">パターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-146">Pattern</span></span>        | <span data-ttu-id="a8c3b-147">同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="a8c3b-147">Synchronous programming paradigm</span></span>    | <span data-ttu-id="a8c3b-148">非同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="a8c3b-148">Asynchronous programming paradigm</span></span> |
|----------------|-------------------------------------|-----------------------------------|
| <span data-ttu-id="a8c3b-149">OData</span><span class="sxs-lookup"><span data-stu-id="a8c3b-149">OData</span></span>          | <span data-ttu-id="a8c3b-150">DbResourceContextaveChanges</span><span class="sxs-lookup"><span data-stu-id="a8c3b-150">DbResourceContextaveChanges</span></span>         | <span data-ttu-id="a8c3b-151">DbResourceContextaveChangesAsync</span><span class="sxs-lookup"><span data-stu-id="a8c3b-151">DbResourceContextaveChangesAsync</span></span> |
| <span data-ttu-id="a8c3b-152">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="a8c3b-152">Custom service</span></span> | <span data-ttu-id="a8c3b-153">httpRequestetResponse</span><span class="sxs-lookup"><span data-stu-id="a8c3b-153">httpRequestetResponse</span></span>               | <span data-ttu-id="a8c3b-154">httpRequesteginGetResponse</span><span class="sxs-lookup"><span data-stu-id="a8c3b-154">httpRequesteginGetResponse</span></span> |
| <span data-ttu-id="a8c3b-155">SOAP</span><span class="sxs-lookup"><span data-stu-id="a8c3b-155">SOAP</span></span>           | <span data-ttu-id="a8c3b-156">UserSessionServiceetUserSessionInfo</span><span class="sxs-lookup"><span data-stu-id="a8c3b-156">UserSessionServiceetUserSessionInfo</span></span> | <span data-ttu-id="a8c3b-157">UserSessionServiceetUserSessionInfoAsync</span><span class="sxs-lookup"><span data-stu-id="a8c3b-157">UserSessionServiceetUserSessionInfoAsync</span></span> |
| <span data-ttu-id="a8c3b-158">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="a8c3b-158">Batch data API</span></span> | <span data-ttu-id="a8c3b-159">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="a8c3b-159">ImportFromPackage</span></span>                   | [<span data-ttu-id="a8c3b-160">BeginInvoke</span><span class="sxs-lookup"><span data-stu-id="a8c3b-160">BeginInvoke</span></span>](/dotnet/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously) |

<span data-ttu-id="a8c3b-161">これらの API が呼び出されると、すぐにビジネス ロジックが Finance and Operations で実行されるため、OData とカスタム サービスの両方は同期統合パターンです。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-161">Both OData and custom services are synchronous integration patterns, because when these APIs are called, business logic is immediately run in Finance and Operations.</span></span> <span data-ttu-id="a8c3b-162">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-162">Here are some examples:</span></span>

- <span data-ttu-id="a8c3b-163">OData を使用して製品レコードを挿入すると、レコードはすぐに OData 呼び出しの一部として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-163">If OData is used to insert product records, the records are immediately inserted as part of the OData call.</span></span>
- <span data-ttu-id="a8c3b-164">手持ちの在庫を検索するためにカスタム サービスを使用すると、ビジネス ロジックが JSON/SOAP 呼び出しの一部としてすぐに実行され、在庫総額がすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-164">If a custom service is used to look up on-hand inventory, business logic is immediately run as part of the JSON/SOAP call, and an inventory sum number is immediately returned.</span></span>

<span data-ttu-id="a8c3b-165">これらの API が呼び出されると、バッチ モードでデータがインポートまたはエクスポートされるため、バッチ データ API は非同期統合パターンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-165">Batch data APIs are considered asynchronous integration patterns, because when these APIs are called, data is imported or exported in batch mode.</span></span> <span data-ttu-id="a8c3b-166">たとえば、ImportFromPackage API への呼び出しは、同期することができます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-166">For example, calls to the ImportFromPackage API can be synchronous.</span></span> <span data-ttu-id="a8c3b-167">ただし、API は、特定のデータ パッケージのみをインポートするバッチ ジョブをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-167">However, the API schedules a batch job to import only a specific data package.</span></span> <span data-ttu-id="a8c3b-168">スケジューリング ジョブはすぐに戻され、後でバッチ ジョブで処理されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-168">The scheduling job is quickly returned, and the work is done later in a batch job.</span></span> <span data-ttu-id="a8c3b-169">したがって、バッチ データ API は非同期として分類されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-169">Therefore, batch data APIs are categorized as asynchronous.</span></span>

<span data-ttu-id="a8c3b-170">バッチ データ API は大量のデータのインポートとエクスポートを処理するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-170">Batch data APIs are designed to handle large-volume data imports and exports.</span></span> <span data-ttu-id="a8c3b-171">大量である条件を正確に定義することは困難です。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-171">It's difficult to define what exactly qualifies as a large volume.</span></span> <span data-ttu-id="a8c3b-172">回答は、エンティティによって、およびインポートまたはエクスポート中に実行されるビジネス ロジックの量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-172">The answer depends on the entity, and on the amount of business logic that is run during import or export.</span></span> <span data-ttu-id="a8c3b-173">ただし、経験則を次に示します: 容量が数十万レコード以上の場合は、統合のバッチ データ API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-173">However, here is a rule of thumb: If the volume is more than a few hundred thousand records, you should use the batch data API for integrations.</span></span>

<span data-ttu-id="a8c3b-174">一般に、統合パターンを選択しようとしている場合、次の質問を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-174">In general, when you're trying to choose an integration pattern, we recommend that you consider the following questions:</span></span>

- <span data-ttu-id="a8c3b-175">統合をリアルタイムで行う必要がある業務要件がありますか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-175">Is there a business requirement that the integration should be in real time?</span></span>
- <span data-ttu-id="a8c3b-176">ピーク時のデータ量の要件は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="a8c3b-176">What is the requirement for the peak data volume?</span></span>
- <span data-ttu-id="a8c3b-177">頻度はどのくらいですか ?</span><span class="sxs-lookup"><span data-stu-id="a8c3b-177">What is the frequency?</span></span>

### <a name="error-handling"></a><span data-ttu-id="a8c3b-178">エラー処理</span><span class="sxs-lookup"><span data-stu-id="a8c3b-178">Error handling</span></span> 

<span data-ttu-id="a8c3b-179">同期パターンを使用するときは、呼び出し元に成功または失敗の応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-179">When you use a synchronous pattern, success or failure responses are returned to the caller.</span></span> <span data-ttu-id="a8c3b-180">たとえば、OData 呼び出しが販売注文を挿入するために使用される場合、販売注文明細行に存在しない製品への無効な参照があると、呼び出し元が受信する応答には、エラー メッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-180">For example, when an OData call is used to insert sales orders, if a sales order line has a bad reference to a product that doesn't exist, the response that the caller receives contains an error message.</span></span> <span data-ttu-id="a8c3b-181">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-181">The caller is responsible for handling any errors in the response.</span></span>

<span data-ttu-id="a8c3b-182">非同期パターンを使用するときは、呼び出し元には、スケジューリング呼び出しが成功したかどうかを示す応答がすぐ表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-182">When you use an asynchronous pattern, the caller receives an immediate response that indicates whether the scheduling call was successful.</span></span> <span data-ttu-id="a8c3b-183">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-183">The caller is responsible for handling any errors in the response.</span></span> <span data-ttu-id="a8c3b-184">スケジューリングが完了したら、データのインポートまたはエクスポートのステータスは、呼び出し元にプッシュされません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-184">After scheduling is done, the status of the data import or export isn't pushed to the caller.</span></span> <span data-ttu-id="a8c3b-185">呼び出し元は、対応するインポートまたはエクスポート処理の結果をポーリングし、それに応じてエラーを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-185">The caller must poll for the result of the corresponding import or export process, and must handle any errors accordingly.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-odata-integrations"></a><span data-ttu-id="a8c3b-186">OData 統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-186">Typical scenarios and patterns that use OData integrations</span></span>

<span data-ttu-id="a8c3b-187">OData 統合を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-187">Here are some typical scenarios that use OData integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c3b-188">Power BI レポートの OData の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-188">Use of OData for Power BI reports is discouraged.</span></span> <span data-ttu-id="a8c3b-189">このような状況ではエンティティ格納を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-189">Using entity store for such scenarios is encouraged.</span></span>

### <a name="create-and-update-product-information"></a><span data-ttu-id="a8c3b-190">製品情報の作成および更新</span><span class="sxs-lookup"><span data-stu-id="a8c3b-190">Create and update product information</span></span>

<span data-ttu-id="a8c3b-191">あるメーカーでは、Finance and Operations を実行しますが、その製品は、オンプレミスでホストされているサード パーティ製アプリケーションを使用して定義および構成されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-191">A manufacturer runs Finance and Operations, but defines and configures its product by using a third-party application that is hosted on-premises.</span></span> <span data-ttu-id="a8c3b-192">この製造元は、生産情報をオンプレミス アプリケーションから Finance and Operations に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-192">This manufacturer wants to move its production information from the on-premises application to Finance and Operations.</span></span> <span data-ttu-id="a8c3b-193">製品が定義されるとき、またはオンプレミス アプリケーションで変更されるとき、ユーザーは、同じ変更を Finance and Operations でリアルタイムに確認できます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-193">When a product is defined, or when it's changed in the on-premises application, the user should see the same change, in real time, in Finance and Operations.</span></span>

| <span data-ttu-id="a8c3b-194">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-194">Decision</span></span>                    | <span data-ttu-id="a8c3b-195">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-195">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="a8c3b-196">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-196">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-197">有</span><span class="sxs-lookup"><span data-stu-id="a8c3b-197">Yes</span></span>                      |
| <span data-ttu-id="a8c3b-198">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-198">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-199">時間当たり 1,000 レコード\*</span><span class="sxs-lookup"><span data-stu-id="a8c3b-199">1,000 records per hour\*</span></span> |
| <span data-ttu-id="a8c3b-200">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-200">Frequency</span></span>                   | <span data-ttu-id="a8c3b-201">アドホック</span><span class="sxs-lookup"><span data-stu-id="a8c3b-201">Ad hoc</span></span>                   |

<span data-ttu-id="a8c3b-202">\* 場合によっては、新しいまたは変更された生産コンフィギュレーションが短時間に多く発生します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-202">\* Occasionally, many new or modified production configurations will occur in a short time.</span></span>

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-203">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-203">Recommended solution</span></span>

<span data-ttu-id="a8c3b-204">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で製品情報を作成および更新することによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-204">This scenario is best implemented by using the OData service endpoints to create and update product information in Finance and Operations.</span></span>

<span data-ttu-id="a8c3b-205">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-205">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-206">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-206">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="a8c3b-207">OData サービス エンドポイントが同じエンティティのセットに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-207">Make sure that the OData service endpoints are available for the same set of entities.</span></span>

<span data-ttu-id="a8c3b-208">サード パーティ製アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-208">In the third-party application:</span></span>

- <span data-ttu-id="a8c3b-209">製品情報がサード パーティ製アプリケーションで作成または変更されるときは、同じ変更を加えるために Finance and Operations への OData 呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-209">When product information is created or modified in the third-party application, an OData call is made to Finance and Operations to make the same change.</span></span>

### <a name="read-the-status-of-customer-orders"></a><span data-ttu-id="a8c3b-210">客注文のステータスを読み取る</span><span class="sxs-lookup"><span data-stu-id="a8c3b-210">Read the status of customer orders</span></span>

<span data-ttu-id="a8c3b-211">会社は、Finance and Operations を実行しますが、顧客が注文の状況を確認できる自己ホストの顧客ポータルを持っています。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-211">A company runs Finance and Operations but has a self-hosted customer portal where customers can check the status of their orders.</span></span> <span data-ttu-id="a8c3b-212">注文ステータス情報は、Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-212">Order status information is maintained in Finance and Operations.</span></span>

| <span data-ttu-id="a8c3b-213">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-213">Decision</span></span>                    | <span data-ttu-id="a8c3b-214">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-214">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="a8c3b-215">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-215">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-216">有</span><span class="sxs-lookup"><span data-stu-id="a8c3b-216">Yes</span></span>                    |
| <span data-ttu-id="a8c3b-217">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-217">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-218">時間当たり 5,000 レコード</span><span class="sxs-lookup"><span data-stu-id="a8c3b-218">5,000 records per hour</span></span> |
| <span data-ttu-id="a8c3b-219">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-219">Frequency</span></span>                   | <span data-ttu-id="a8c3b-220">アドホック</span><span class="sxs-lookup"><span data-stu-id="a8c3b-220">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-221">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-221">Recommended solution</span></span>

<span data-ttu-id="a8c3b-222">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で注文のステータスを読み取ることによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-222">This scenario is best implemented by using the OData service endpoints to read order status information from Finance and Operations.</span></span>

<span data-ttu-id="a8c3b-223">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-223">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-224">注文のステータス情報を読むために必要なエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-224">Determine the entity that is required in order to read order status information.</span></span>
- <span data-ttu-id="a8c3b-225">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-225">Make sure that the OData service endpoint is available for the entity.</span></span>

<span data-ttu-id="a8c3b-226">顧客のポータル サイトで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-226">On the customer portal site:</span></span>

- <span data-ttu-id="a8c3b-227">顧客は注文のステータスをチェックするとき、対応する注文を読み取ってそのステータスを取得するために、Finance and Operations にリアルタイムの OData 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-227">When a customer checks the status of an order, make a real-time OData call to Finance and Operations to read the corresponding order and retrieve its status.</span></span>

### <a name="approve-boms"></a><span data-ttu-id="a8c3b-228">BOM の承認</span><span class="sxs-lookup"><span data-stu-id="a8c3b-228">Approve BOMs</span></span>

<span data-ttu-id="a8c3b-229">会社は、Finance and Operations を実行しますが、オンプレミスでホストされている製品ライフサイクル管理 (PLM) システムを使用しています。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-229">A company runs Finance and Operations but uses a product lifecycle management (PLM) system that is hosted on-premises.</span></span> <span data-ttu-id="a8c3b-230">PLM システムには、承認のために Finance and Operations に完成した部品表 (BOM) 情報を送信するワークフローがあります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-230">The PLM system has a workflow that sends the finished bill of materials (BOM) information to Finance and Operations for approval.</span></span>

| <span data-ttu-id="a8c3b-231">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-231">Decision</span></span>                    | <span data-ttu-id="a8c3b-232">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-232">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="a8c3b-233">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-233">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-234">有</span><span class="sxs-lookup"><span data-stu-id="a8c3b-234">Yes</span></span>                    |
| <span data-ttu-id="a8c3b-235">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-235">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-236">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="a8c3b-236">1,000 records per hour</span></span> |
| <span data-ttu-id="a8c3b-237">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-237">Frequency</span></span>                   | <span data-ttu-id="a8c3b-238">アドホック</span><span class="sxs-lookup"><span data-stu-id="a8c3b-238">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-239">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-239">Recommended solution</span></span>

<span data-ttu-id="a8c3b-240">このシナリオは、OData アクションを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-240">This scenario can be implemented by using an OData action.</span></span>

<span data-ttu-id="a8c3b-241">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-241">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-242">統合に必要なエンティティを決定する</span><span class="sxs-lookup"><span data-stu-id="a8c3b-242">Determine the entity that is required for the integration.</span></span>
- <span data-ttu-id="a8c3b-243">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-243">Make sure that the OData service endpoints are available for the entity.</span></span>
- <span data-ttu-id="a8c3b-244">エンティティで、必要なビジネス ロジックを実行するアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-244">On the entity, create an action to run the required business logic.</span></span>

<span data-ttu-id="a8c3b-245">PLM ソリューション:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-245">In the PLM solution:</span></span>

- <span data-ttu-id="a8c3b-246">PLM システムで、BOM を承認する OData アクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-246">Make the PLM system invoke the OData action to approve the BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c3b-247">このタイプの OData アクションは **BOMBillOfMaterialsHeaderEntity::approve** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-247">You can find an example of this type of OData action in **BOMBillOfMaterialsHeaderEntity::approve**.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-a-custom-service"></a><span data-ttu-id="a8c3b-248">カスタム サービスを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-248">Typical scenarios and patterns that use a custom service</span></span>

<span data-ttu-id="a8c3b-249">カスタム サービスを使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-249">Here are some typical scenarios that use a custom service.</span></span>

### <a name="look-up-on-hand-inventory"></a><span data-ttu-id="a8c3b-250">手持在庫の検索</span><span class="sxs-lookup"><span data-stu-id="a8c3b-250">Look up on-hand inventory</span></span>

<span data-ttu-id="a8c3b-251">エネルギー会社にはヒーターのインストール ジョブをスケジュールするフィールド作業者がいます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-251">An energy company has field workers who schedule installation jobs for heaters.</span></span> <span data-ttu-id="a8c3b-252">この会社はバック オフィスとサード パーティのサービスとしてのソフトウェア (SaaS) のために Finance and Operations を使用して予定をスケジューリングします。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-252">This company uses Finance and Operations for the back office and third-party software as a service (SaaS) to schedule appointments.</span></span> <span data-ttu-id="a8c3b-253">現場作業員が予定をスケジュールするときは、ジョブに使用できるインストール パーツがあることを確認するために、引当可能在庫数を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-253">When field workers schedule appointments, they must look up inventory availability to make sure that installation parts are available for the job.</span></span>

| <span data-ttu-id="a8c3b-254">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-254">Decision</span></span>                    | <span data-ttu-id="a8c3b-255">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-255">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="a8c3b-256">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-256">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-257">有</span><span class="sxs-lookup"><span data-stu-id="a8c3b-257">Yes</span></span>                    |
| <span data-ttu-id="a8c3b-258">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-258">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-259">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="a8c3b-259">1,000 records per hour</span></span> |
| <span data-ttu-id="a8c3b-260">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-260">Frequency</span></span>                   | <span data-ttu-id="a8c3b-261">アドホック</span><span class="sxs-lookup"><span data-stu-id="a8c3b-261">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-262">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-262">Recommended solution</span></span>

<span data-ttu-id="a8c3b-263">このシナリオは、カスタム サービスを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-263">This scenario can be implemented by using a custom service.</span></span>

<span data-ttu-id="a8c3b-264">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-264">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-265">特定のアイテムの現物手持在庫を計算するカスタム サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-265">Create a custom service to calculate the physical on-hand inventory for a given item.</span></span>

<span data-ttu-id="a8c3b-266">スケジューリング アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-266">In the scheduling application:</span></span>

- <span data-ttu-id="a8c3b-267">選択した品目の在庫情報を取得するために、SOAP または REST を通じてカスタム サービス エンドポイントへのリアルタイムな呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-267">Make a real-time call to a custom service endpoint, through either SOAP or REST, to retrieve inventory information for the selected item.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c3b-268">このタイプのカスタム サービスの例は、Retail Real Time Services が実装された **RetailTransactionServiceInventory::inventoryLookup** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-268">You can find an example of this type of custom service in the Retail Real Time Services implementation: **RetailTransactionServiceInventory::inventoryLookup**.</span></span>

<span data-ttu-id="a8c3b-269">また、inventorySiteOnHand エンティティを使用して同じ結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-269">You can also use the inventorySiteOnHand entity to achieve the same result.</span></span> <span data-ttu-id="a8c3b-270">場合によっては、複数のメソッドを使用して、Finance and Operations で同じデータとビジネス ロジックを公開できます。すべてのメソッドが同じように有効になり、効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-270">Sometimes, you can use multiple methods to expose the same data and business logic in Finance and Operations, and all the methods are equally valid and effective.</span></span> <span data-ttu-id="a8c3b-271">この場合、特定のシナリオを最適に機能して、開発者が最も使いやすいメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-271">In this case, choose the method that works best for a given scenario and that a developer is most comfortable with.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-batch-data-integrations"></a><span data-ttu-id="a8c3b-272">バッチ データ統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-272">Typical scenarios and patterns that use batch data integrations</span></span>

<span data-ttu-id="a8c3b-273">バッチ データ API を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-273">Here are some typical scenarios that use batch data APIs.</span></span>

### <a name="import-large-volumes-of-sales-orders"></a><span data-ttu-id="a8c3b-274">大量の販売注文のインポート</span><span class="sxs-lookup"><span data-stu-id="a8c3b-274">Import large volumes of sales orders</span></span>

<span data-ttu-id="a8c3b-275">会社は、オンプレミスを実行するフロント エンド システムから大量の販売注文を受信します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-275">A company receives a large volume of sales orders from a front-end system that runs on-premises.</span></span> <span data-ttu-id="a8c3b-276">これらの注文は、定期的に処理、管理するために Finance and Operations に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-276">These orders must periodically be sent to Finance and Operations for processing and management.</span></span>

| <span data-ttu-id="a8c3b-277">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-277">Decision</span></span>                    | <span data-ttu-id="a8c3b-278">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-278">Information</span></span>                 |
|-----------------------------|-----------------------------|
| <span data-ttu-id="a8c3b-279">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-279">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-280">無</span><span class="sxs-lookup"><span data-stu-id="a8c3b-280">No</span></span>                          |
| <span data-ttu-id="a8c3b-281">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-281">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-282">時間当たり 200,000 レコード</span><span class="sxs-lookup"><span data-stu-id="a8c3b-282">200,000 records per hour</span></span>    |
| <span data-ttu-id="a8c3b-283">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-283">Frequency</span></span>                   | <span data-ttu-id="a8c3b-284">5 分間隔で 1 回</span><span class="sxs-lookup"><span data-stu-id="a8c3b-284">One time every five minutes</span></span> |

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-285">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-285">Recommended solution</span></span>

<span data-ttu-id="a8c3b-286">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-286">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="a8c3b-287">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-287">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-288">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-288">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="a8c3b-289">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-289">Make sure that data management is enabled for the entities.</span></span>

<span data-ttu-id="a8c3b-290">オンプレミスシステム:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-290">In the on-premises system:</span></span>

- <span data-ttu-id="a8c3b-291">Finance and Operations にファイルをインポートするには、REST バッチ データ API を使用します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-291">Use the REST batch data API to import files into Finance and Operations.</span></span>

### <a name="export-large-volumes-of-purchase-orders"></a><span data-ttu-id="a8c3b-292">大量の発注書をエクスポート</span><span class="sxs-lookup"><span data-stu-id="a8c3b-292">Export large volumes of purchase orders</span></span>

<span data-ttu-id="a8c3b-293">会社は、Finance and Operations で大量の発注書を生成し、オンプレミス在庫管理システムを使用して製品を入庫します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-293">A company generates a large volume of purchase orders in Finance and Operations and uses an on-premises inventory management system to receive products.</span></span> <span data-ttu-id="a8c3b-294">発注書は、Finance and Operations からオンプレミス インベントリ システムに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-294">Purchase orders must be moved from Finance and Operations to the on-premises inventory system.</span></span>

| <span data-ttu-id="a8c3b-295">意思決定</span><span class="sxs-lookup"><span data-stu-id="a8c3b-295">Decision</span></span>                    | <span data-ttu-id="a8c3b-296">情報</span><span class="sxs-lookup"><span data-stu-id="a8c3b-296">Information</span></span>               |
|-----------------------------|---------------------------|
| <span data-ttu-id="a8c3b-297">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-297">Is real-time data required?</span></span> | <span data-ttu-id="a8c3b-298">無</span><span class="sxs-lookup"><span data-stu-id="a8c3b-298">No</span></span>                        |
| <span data-ttu-id="a8c3b-299">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="a8c3b-299">Peak data volume</span></span>            | <span data-ttu-id="a8c3b-300">時間当たり 300,000 レコード</span><span class="sxs-lookup"><span data-stu-id="a8c3b-300">300,000 records per hour</span></span>  |
| <span data-ttu-id="a8c3b-301">頻度</span><span class="sxs-lookup"><span data-stu-id="a8c3b-301">Frequency</span></span>                   | <span data-ttu-id="a8c3b-302">1 時間あたり 1 回</span><span class="sxs-lookup"><span data-stu-id="a8c3b-302">One time per hour</span></span>         |

#### <a name="recommended-solution"></a><span data-ttu-id="a8c3b-303">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="a8c3b-303">Recommended solution</span></span>

<span data-ttu-id="a8c3b-304">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-304">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="a8c3b-305">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-305">In Finance and Operations:</span></span>

- <span data-ttu-id="a8c3b-306">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-306">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="a8c3b-307">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-307">Make sure that data management is enabled for the entities.</span></span>
- <span data-ttu-id="a8c3b-308">差分プッシュする必要がある場合は、エンティティの変更履歴を有効にできるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-308">If incremental push is required, make sure that change tracking can be enabled on the entities.</span></span>

<span data-ttu-id="a8c3b-309">オンプレミス在庫システム:</span><span class="sxs-lookup"><span data-stu-id="a8c3b-309">In the on-premises inventory system:</span></span>

- <span data-ttu-id="a8c3b-310">REST バッチ データ API を使用して、Finance and Operations からファイルをエクスポートし、在庫システムにインポートします。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-310">Use the REST batch data API to export the file from Finance and Operations and import it into the inventory system.</span></span>

## <a name="typical-scenarios-and-patterns-that-call-external-web-services"></a><span data-ttu-id="a8c3b-311">外部の Web サービスを呼び出す一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="a8c3b-311">Typical scenarios and patterns that call external web services</span></span>

<span data-ttu-id="a8c3b-312">通常、Finance and Operations はオンプレミスまたは別の SaaS プロバイダーによってホストされている外部 Web サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-312">It's typical that Finance and Operations calls out to an external web service that is hosted either on-premises or by another SaaS provider.</span></span> <span data-ttu-id="a8c3b-313">この場合、Finance and Operations は統合クライアントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-313">In this case, Finance and Operations acts as the integration client.</span></span> <span data-ttu-id="a8c3b-314">Finance and Operation の統合クライアントを作成するときは、他のアプリケーションの統合クライアントを作成するときと同じベスト プラクティスおよびガイドラインのセットに従ってください。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-314">When you write an integration client for Finance and Operations, you should follow the same set of best practices and guidelines that you follow when you write an integration client for any other application.</span></span> <span data-ttu-id="a8c3b-315">単純な例として、[外部 Web サービスの使用](consume-external-web-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-315">For a simple example, see [Consuming external web services](consume-external-web-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8c3b-316">セキュリティ要件のため、Finance and Operations の生産とサンドボックス環境では、トランスポート層セキュリティ (TLS) 1.2 以降を使用するセキュリティ保護された通信のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-316">Because of security requirements, Finance and Operations production and sandbox environments support only secured communication that uses Transport Layer Security (TLS) 1.2 or later.</span></span> <span data-ttu-id="a8c3b-317">つまり、Finance and Operations が呼び出すターゲットの Web サービス エンドポイントは、TLS 1.2 以降をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-317">In other words, the target web service endpoint that Finance and Operations calls out to must support TLS 1.2 or later.</span></span> <span data-ttu-id="a8c3b-318">ターゲット サービス エンドポイントがこの要件を満たしていない場合、Finance and Operations からの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-318">If the target service endpoint doesn't meet this requirement, calls from Finance and Operations fail.</span></span> <span data-ttu-id="a8c3b-319">例外エラー メッセージは、次のメッセージのようになります。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-319">The exception error message resembles the following message:</span></span>
>
> <span data-ttu-id="a8c3b-320">*「転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。」*</span><span class="sxs-lookup"><span data-stu-id="a8c3b-320">*Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.*</span></span>
>
> <span data-ttu-id="a8c3b-321">TLS 1.2 またはそれ以降のバージョンを使用することが原因で対象サービスを変更できない場合は、次の図に示すように、ブローカー サービスを導入して 2 ホップ コールを行うことでこの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="a8c3b-321">If you can't modify the target service so that it uses TLS 1.2 or later, you can work around this issue by introducing a broker service and making a two-hop call, as shown in the following illustration.</span></span>
>
> ![TLS の要件](./media/integration-tls.png)
