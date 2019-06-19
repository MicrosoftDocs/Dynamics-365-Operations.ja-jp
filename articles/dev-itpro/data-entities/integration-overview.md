---
title: データ統合方法 (インポート/エクスポート) の選択
description: このトピックは、設計者と開発者が Microsoft Dynamics 365 for Finance and Operations の統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/10/2018
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
ms.openlocfilehash: d59e8e6a703dab0e0ccdbb9f7fcbf7994535646c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544268"
---
# <a name="choose-a-data-integration-importexport-strategy"></a><span data-ttu-id="97967-103">データ統合方法 (インポート/エクスポート) の選択</span><span class="sxs-lookup"><span data-stu-id="97967-103">Choose a data integration (import/export) strategy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97967-104">このトピックは、設計者と開発者が Microsoft Dynamics 365 for Finance and Operations の統合シナリオを実装する際に意思決定を適切に行えるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="97967-104">This topic is intended to help architects and developers make sound design decisions when they implement integration scenarios for Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="97967-105">このトピックでは、統合パターン、統合シナリオ、統合ソリューション、Finance and Operations のベストプラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="97967-105">The topic describes integration patterns, integration scenarios, and integration solutions and best practices for Finance and Operations.</span></span> <span data-ttu-id="97967-106">ただし、すべての統合パターンを使用または設定する方法に関する技術詳細は含まれません。</span><span class="sxs-lookup"><span data-stu-id="97967-106">However, it doesn't include technical details about how to use or set up every integration pattern.</span></span> <span data-ttu-id="97967-107">また、サンプル統合コードも含まれていません。</span><span class="sxs-lookup"><span data-stu-id="97967-107">It also doesn't include sample integration code.</span></span>

<span data-ttu-id="97967-108">次のテーブルに、Finance and Operations で使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="97967-108">The following table lists the integration patterns that are available for Finance and Operations.</span></span>

| <span data-ttu-id="97967-109">パターン</span><span class="sxs-lookup"><span data-stu-id="97967-109">Pattern</span></span>                       | <span data-ttu-id="97967-110">ドキュメント</span><span class="sxs-lookup"><span data-stu-id="97967-110">Documentation</span></span> |
|-------------------------------|---------------|
| <span data-ttu-id="97967-111">OData</span><span class="sxs-lookup"><span data-stu-id="97967-111">OData</span></span>                         | [<span data-ttu-id="97967-112">OData</span><span class="sxs-lookup"><span data-stu-id="97967-112">OData</span></span>](odata.md) |
| <span data-ttu-id="97967-113">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="97967-113">Batch data API</span></span>                | [<span data-ttu-id="97967-114">定期統合</span><span class="sxs-lookup"><span data-stu-id="97967-114">Recurring integrations</span></span>](recurring-integrations.md)<br>[<span data-ttu-id="97967-115">データ パッケージ API</span><span class="sxs-lookup"><span data-stu-id="97967-115">Data package API</span></span>](data-management-api.md) |
| <span data-ttu-id="97967-116">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="97967-116">Custom service</span></span>                | [<span data-ttu-id="97967-117">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="97967-117">Custom services</span></span>](custom-services.md) |
| <span data-ttu-id="97967-118">外部 Web サービスの消費</span><span class="sxs-lookup"><span data-stu-id="97967-118">Consume external web services</span></span> | [<span data-ttu-id="97967-119">外部 Web サービスの使用</span><span class="sxs-lookup"><span data-stu-id="97967-119">Consuming external web services</span></span>](consume-external-web-service.md) |
| <span data-ttu-id="97967-120">Excel 統合</span><span class="sxs-lookup"><span data-stu-id="97967-120">Excel integration</span></span>             | [<span data-ttu-id="97967-121">Office 統合</span><span class="sxs-lookup"><span data-stu-id="97967-121">Office integration</span></span>](../office-integration/office-integration.md) |

> [!NOTE]
> <span data-ttu-id="97967-122">オンプレミス配置の場合、唯一サポートされる API は[データ パッケージ API](data-management-api.md) です。</span><span class="sxs-lookup"><span data-stu-id="97967-122">For on premise deployments, the only supported API is the [Data package API](data-management-api.md).</span></span> <span data-ttu-id="97967-123">これは、7.2、platform update 12 ビルド 7.0.4709.41184 で現在利用可能です。</span><span class="sxs-lookup"><span data-stu-id="97967-123">This is currently available on 7.2, platform update 12 build 7.0.4709.41184.</span></span>

## <a name="synchronous-vs-asynchronous-integration-patterns"></a><span data-ttu-id="97967-124">同期および非同期の統合パターン</span><span class="sxs-lookup"><span data-stu-id="97967-124">Synchronous vs. asynchronous integration patterns</span></span>

<span data-ttu-id="97967-125">処理は、同期または非同期にすることができます。</span><span class="sxs-lookup"><span data-stu-id="97967-125">Processing can be either synchronous or asynchronous.</span></span> <span data-ttu-id="97967-126">多くの場合、使用すべき処理タイプは、選択した統合パターンによって決まります。</span><span class="sxs-lookup"><span data-stu-id="97967-126">Often, the type of processing that you must use determines the integration pattern that you choose.</span></span>

<span data-ttu-id="97967-127">*同期*パターンは、ブロック要求と応答パターンであり、呼び出し先が実行を終了して応答を返すまで呼び出し元がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="97967-127">A *synchronous* pattern is a blocking request and response pattern, where the caller is blocked until the callee has finished running and gives a response.</span></span> <span data-ttu-id="97967-128">*非同期*パターンは非ブロック パターンで、呼び出し元が要求を送信して応答を待たずに続行します。</span><span class="sxs-lookup"><span data-stu-id="97967-128">An *asynchronous* pattern is a non-blocking pattern, where the caller submits the request and then continues without waiting for a response.</span></span>

<span data-ttu-id="97967-129">次のテーブルに、使用可能な受信統合パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="97967-129">The following table lists the inbound integration patterns that are available.</span></span>

| <span data-ttu-id="97967-130">パターン</span><span class="sxs-lookup"><span data-stu-id="97967-130">Pattern</span></span>        | <span data-ttu-id="97967-131">タイミング</span><span class="sxs-lookup"><span data-stu-id="97967-131">Timing</span></span>       | <span data-ttu-id="97967-132">バッチ</span><span class="sxs-lookup"><span data-stu-id="97967-132">Batch</span></span> |
|----------------|--------------|-------|
| <span data-ttu-id="97967-133">OData</span><span class="sxs-lookup"><span data-stu-id="97967-133">OData</span></span>          | <span data-ttu-id="97967-134">同期</span><span class="sxs-lookup"><span data-stu-id="97967-134">Synchronous</span></span>  | <span data-ttu-id="97967-135">無</span><span class="sxs-lookup"><span data-stu-id="97967-135">No</span></span>    |
| <span data-ttu-id="97967-136">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="97967-136">Batch data API</span></span> | <span data-ttu-id="97967-137">非同期</span><span class="sxs-lookup"><span data-stu-id="97967-137">Asynchronous</span></span> | <span data-ttu-id="97967-138">有</span><span class="sxs-lookup"><span data-stu-id="97967-138">Yes</span></span>   |

<span data-ttu-id="97967-139">同期と非同期パターンを比較する前に、Finance and Operations が提供するすべての REST および SOAP 統合アプリケーション プログラミング インターフェイス (API) を同期または非同期で呼び出すことができるので注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="97967-139">Before you compare synchronous and asynchronous patterns, you should be aware that all the REST and SOAP integration application programming interfaces (APIs) that Finance and Operations provides can be invoked either synchronously or asynchronously.</span></span>

<span data-ttu-id="97967-140">次の例は、このポイントを示しています。</span><span class="sxs-lookup"><span data-stu-id="97967-140">The following examples illustrate this point.</span></span> <span data-ttu-id="97967-141">オープン データ プロトコル (OData) が統合のために使用される場合、呼び出し元がブロックされるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="97967-141">You can't assume that the caller will be blocked when the Open Data Protocol (OData) is used for integration.</span></span> <span data-ttu-id="97967-142">通話の仕方によっては、呼び出し元がブロックされない場合があります。</span><span class="sxs-lookup"><span data-stu-id="97967-142">The caller might not be blocked, depending on how a call is made.</span></span>

| <span data-ttu-id="97967-143">パターン</span><span class="sxs-lookup"><span data-stu-id="97967-143">Pattern</span></span>        | <span data-ttu-id="97967-144">同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="97967-144">Synchronous programming paradigm</span></span>    | <span data-ttu-id="97967-145">非同期式のプログラミング パラダイム</span><span class="sxs-lookup"><span data-stu-id="97967-145">Asynchronous programming paradigm</span></span> |
|----------------|-------------------------------------|-----------------------------------|
| <span data-ttu-id="97967-146">OData</span><span class="sxs-lookup"><span data-stu-id="97967-146">OData</span></span>          | <span data-ttu-id="97967-147">DbResourceContextaveChanges</span><span class="sxs-lookup"><span data-stu-id="97967-147">DbResourceContextaveChanges</span></span>         | <span data-ttu-id="97967-148">DbResourceContextaveChangesAsync</span><span class="sxs-lookup"><span data-stu-id="97967-148">DbResourceContextaveChangesAsync</span></span> |
| <span data-ttu-id="97967-149">顧客サービス</span><span class="sxs-lookup"><span data-stu-id="97967-149">Custom service</span></span> | <span data-ttu-id="97967-150">httpRequestetResponse</span><span class="sxs-lookup"><span data-stu-id="97967-150">httpRequestetResponse</span></span>               | <span data-ttu-id="97967-151">httpRequesteginGetResponse</span><span class="sxs-lookup"><span data-stu-id="97967-151">httpRequesteginGetResponse</span></span> |
| <span data-ttu-id="97967-152">SOAP</span><span class="sxs-lookup"><span data-stu-id="97967-152">SOAP</span></span>           | <span data-ttu-id="97967-153">UserSessionServiceetUserSessionInfo</span><span class="sxs-lookup"><span data-stu-id="97967-153">UserSessionServiceetUserSessionInfo</span></span> | <span data-ttu-id="97967-154">UserSessionServiceetUserSessionInfoAsync</span><span class="sxs-lookup"><span data-stu-id="97967-154">UserSessionServiceetUserSessionInfoAsync</span></span> |
| <span data-ttu-id="97967-155">バッチ データ API</span><span class="sxs-lookup"><span data-stu-id="97967-155">Batch data API</span></span> | <span data-ttu-id="97967-156">ImportFromPackage</span><span class="sxs-lookup"><span data-stu-id="97967-156">ImportFromPackage</span></span>                   | [<span data-ttu-id="97967-157">BeginInvoke</span><span class="sxs-lookup"><span data-stu-id="97967-157">BeginInvoke</span></span>](/dotnet/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously) |

<span data-ttu-id="97967-158">これらの API が呼び出されると、すぐにビジネス ロジックが Finance and Operations で実行されるため、OData とカスタム サービスの両方は同期統合パターンです。</span><span class="sxs-lookup"><span data-stu-id="97967-158">Both OData and custom services are synchronous integration patterns, because when these APIs are called, business logic is immediately run in Finance and Operations.</span></span> <span data-ttu-id="97967-159">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="97967-159">Here are some examples:</span></span>

- <span data-ttu-id="97967-160">OData を使用して製品レコードを挿入すると、レコードはすぐに OData 呼び出しの一部として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="97967-160">If OData is used to insert product records, the records are immediately inserted as part of the OData call.</span></span>
- <span data-ttu-id="97967-161">手持ちの在庫を検索するためにカスタム サービスを使用すると、ビジネス ロジックが JSON/SOAP 呼び出しの一部としてすぐに実行され、在庫総額がすぐに返されます。</span><span class="sxs-lookup"><span data-stu-id="97967-161">If a custom service is used to look up on-hand inventory, business logic is immediately run as part of the JSON/SOAP call, and an inventory sum number is immediately returned.</span></span>

<span data-ttu-id="97967-162">これらの API が呼び出されると、バッチ モードでデータがインポートまたはエクスポートされるため、バッチ データ API は非同期統合パターンと見なされます。</span><span class="sxs-lookup"><span data-stu-id="97967-162">Batch data APIs are considered asynchronous integration patterns, because when these APIs are called, data is imported or exported in batch mode.</span></span> <span data-ttu-id="97967-163">たとえば、ImportFromPackage API への呼び出しは、同期することができます。</span><span class="sxs-lookup"><span data-stu-id="97967-163">For example, calls to the ImportFromPackage API can be synchronous.</span></span> <span data-ttu-id="97967-164">ただし、API は、特定のデータ パッケージのみをインポートするバッチ ジョブをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="97967-164">However, the API schedules a batch job to import only a specific data package.</span></span> <span data-ttu-id="97967-165">スケジューリング ジョブはすぐに戻され、後でバッチ ジョブで処理されます。</span><span class="sxs-lookup"><span data-stu-id="97967-165">The scheduling job is quickly returned, and the work is done later in a batch job.</span></span> <span data-ttu-id="97967-166">したがって、バッチ データ API は非同期として分類されます。</span><span class="sxs-lookup"><span data-stu-id="97967-166">Therefore, batch data APIs are categorized as asynchronous.</span></span>

<span data-ttu-id="97967-167">バッチ データ API は大量のデータのインポートとエクスポートを処理するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="97967-167">Batch data APIs are designed to handle large-volume data imports and exports.</span></span> <span data-ttu-id="97967-168">大量である条件を正確に定義することは困難です。</span><span class="sxs-lookup"><span data-stu-id="97967-168">It's difficult to define what exactly qualifies as a large volume.</span></span> <span data-ttu-id="97967-169">回答は、エンティティによって、およびインポートまたはエクスポート中に実行されるビジネス ロジックの量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="97967-169">The answer depends on the entity, and on the amount of business logic that is run during import or export.</span></span> <span data-ttu-id="97967-170">ただし、経験則を次に示します: 容量が数十万レコード以上の場合は、統合のバッチ データ API を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-170">However, here is a rule of thumb: If the volume is more than a few hundred thousand records, you should use the batch data API for integrations.</span></span>

<span data-ttu-id="97967-171">一般に、統合パターンを選択しようとしている場合、次の質問を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="97967-171">In general, when you're trying to choose an integration pattern, we recommend that you consider the following questions:</span></span>

- <span data-ttu-id="97967-172">統合をリアルタイムで行う必要がある業務要件がありますか。</span><span class="sxs-lookup"><span data-stu-id="97967-172">Is there a business requirement that the integration should be in real time?</span></span>
- <span data-ttu-id="97967-173">ピーク時のデータ量の要件は何ですか ?</span><span class="sxs-lookup"><span data-stu-id="97967-173">What is the requirement for the peak data volume?</span></span>
- <span data-ttu-id="97967-174">頻度はどのくらいですか ?</span><span class="sxs-lookup"><span data-stu-id="97967-174">What is the frequency?</span></span>

### <a name="error-handling"></a><span data-ttu-id="97967-175">エラー処理</span><span class="sxs-lookup"><span data-stu-id="97967-175">Error handling</span></span> 

<span data-ttu-id="97967-176">同期パターンを使用するときは、呼び出し元に成功または失敗の応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="97967-176">When you use a synchronous pattern, success or failure responses are returned to the caller.</span></span> <span data-ttu-id="97967-177">たとえば、OData 呼び出しが販売注文を挿入するために使用される場合、販売注文明細行に存在しない製品への無効な参照があると、呼び出し元が受信する応答には、エラー メッセージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="97967-177">For example, when an OData call is used to insert sales orders, if a sales order line has a bad reference to a product that doesn't exist, the response that the caller receives contains an error message.</span></span> <span data-ttu-id="97967-178">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="97967-178">The caller is responsible for handling any errors in the response.</span></span>

<span data-ttu-id="97967-179">非同期パターンを使用するときは、呼び出し元には、スケジューリング呼び出しが成功したかどうかを示す応答がすぐ表示されます。</span><span class="sxs-lookup"><span data-stu-id="97967-179">When you use an asynchronous pattern, the caller receives an immediate response that indicates whether the scheduling call was successful.</span></span> <span data-ttu-id="97967-180">呼び出し元は、応答内のエラーを処理します。</span><span class="sxs-lookup"><span data-stu-id="97967-180">The caller is responsible for handling any errors in the response.</span></span> <span data-ttu-id="97967-181">スケジューリングが完了したら、データのインポートまたはエクスポートのステータスは、呼び出し元にプッシュされません。</span><span class="sxs-lookup"><span data-stu-id="97967-181">After scheduling is done, the status of the data import or export isn't pushed to the caller.</span></span> <span data-ttu-id="97967-182">呼び出し元は、対応するインポートまたはエクスポート処理の結果をポーリングし、それに応じてエラーを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-182">The caller must poll for the result of the corresponding import or export process, and must handle any errors accordingly.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-odata-integrations"></a><span data-ttu-id="97967-183">OData 統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="97967-183">Typical scenarios and patterns that use OData integrations</span></span>

<span data-ttu-id="97967-184">OData 統合を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="97967-184">Here are some typical scenarios that use OData integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="97967-185">Power BI レポートの OData の使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="97967-185">Use of OData for Power BI reports is discouraged.</span></span> <span data-ttu-id="97967-186">このような状況ではエンティティ格納を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="97967-186">Using entity store for such scenarios is encouraged.</span></span>

### <a name="create-and-update-product-information"></a><span data-ttu-id="97967-187">製品情報の作成および更新</span><span class="sxs-lookup"><span data-stu-id="97967-187">Create and update product information</span></span>

<span data-ttu-id="97967-188">あるメーカーでは、Finance and Operations を実行しますが、その製品は、オンプレミスでホストされているサード パーティ製アプリケーションを使用して定義および構成されます。</span><span class="sxs-lookup"><span data-stu-id="97967-188">A manufacturer runs Finance and Operations, but defines and configures its product by using a third-party application that is hosted on-premises.</span></span> <span data-ttu-id="97967-189">この製造元は、生産情報をオンプレミス アプリケーションから Finance and Operations に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-189">This manufacturer wants to move its production information from the on-premises application to Finance and Operations.</span></span> <span data-ttu-id="97967-190">製品が定義されるとき、またはオンプレミス アプリケーションで変更されるとき、ユーザーは、同じ変更を Finance and Operations でリアルタイムに確認できます。</span><span class="sxs-lookup"><span data-stu-id="97967-190">When a product is defined, or when it's changed in the on-premises application, the user should see the same change, in real time, in Finance and Operations.</span></span>

| <span data-ttu-id="97967-191">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-191">Decision</span></span>                    | <span data-ttu-id="97967-192">情報</span><span class="sxs-lookup"><span data-stu-id="97967-192">Information</span></span>              |
|-----------------------------|--------------------------|
| <span data-ttu-id="97967-193">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-193">Is real-time data required?</span></span> | <span data-ttu-id="97967-194">有</span><span class="sxs-lookup"><span data-stu-id="97967-194">Yes</span></span>                      |
| <span data-ttu-id="97967-195">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-195">Peak data volume</span></span>            | <span data-ttu-id="97967-196">時間当たり 1,000 レコード\*</span><span class="sxs-lookup"><span data-stu-id="97967-196">1,000 records per hour\*</span></span> |
| <span data-ttu-id="97967-197">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-197">Frequency</span></span>                   | <span data-ttu-id="97967-198">アドホック</span><span class="sxs-lookup"><span data-stu-id="97967-198">Ad hoc</span></span>                   |

<span data-ttu-id="97967-199">\* 場合によっては、新しいまたは変更された生産コンフィギュレーションが短時間に多く発生します。</span><span class="sxs-lookup"><span data-stu-id="97967-199">\* Occasionally, many new or modified production configurations will occur in a short time.</span></span>

#### <a name="recommended-solution"></a><span data-ttu-id="97967-200">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-200">Recommended solution</span></span>

<span data-ttu-id="97967-201">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で製品情報を作成および更新することによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="97967-201">This scenario is best implemented by using the OData service endpoints to create and update product information in Finance and Operations.</span></span>

<span data-ttu-id="97967-202">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-202">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-203">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="97967-203">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="97967-204">OData サービス エンドポイントが同じエンティティのセットに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-204">Make sure that the OData service endpoints are available for the same set of entities.</span></span>

<span data-ttu-id="97967-205">サード パーティ製アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="97967-205">In the third-party application:</span></span>

- <span data-ttu-id="97967-206">製品情報がサード パーティ製アプリケーションで作成または変更されるときは、同じ変更を加えるために Finance and Operations への OData 呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="97967-206">When product information is created or modified in the third-party application, an OData call is made to Finance and Operations to make the same change.</span></span>

### <a name="read-the-status-of-customer-orders"></a><span data-ttu-id="97967-207">客注文のステータスを読み取る</span><span class="sxs-lookup"><span data-stu-id="97967-207">Read the status of customer orders</span></span>

<span data-ttu-id="97967-208">会社は、Finance and Operations を実行しますが、顧客が注文の状況を確認できる自己ホストの顧客ポータルを持っています。</span><span class="sxs-lookup"><span data-stu-id="97967-208">A company runs Finance and Operations but has a self-hosted customer portal where customers can check the status of their orders.</span></span> <span data-ttu-id="97967-209">注文ステータス情報は、Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="97967-209">Order status information is maintained in Finance and Operations.</span></span>

| <span data-ttu-id="97967-210">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-210">Decision</span></span>                    | <span data-ttu-id="97967-211">情報</span><span class="sxs-lookup"><span data-stu-id="97967-211">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="97967-212">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-212">Is real-time data required?</span></span> | <span data-ttu-id="97967-213">有</span><span class="sxs-lookup"><span data-stu-id="97967-213">Yes</span></span>                    |
| <span data-ttu-id="97967-214">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-214">Peak data volume</span></span>            | <span data-ttu-id="97967-215">時間当たり 5,000 レコード</span><span class="sxs-lookup"><span data-stu-id="97967-215">5,000 records per hour</span></span> |
| <span data-ttu-id="97967-216">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-216">Frequency</span></span>                   | <span data-ttu-id="97967-217">アドホック</span><span class="sxs-lookup"><span data-stu-id="97967-217">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="97967-218">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-218">Recommended solution</span></span>

<span data-ttu-id="97967-219">このシナリオは、OData サービス エンドポイントを使用して、Finance and Operations で注文のステータスを読み取ることによって最適に実装されます。</span><span class="sxs-lookup"><span data-stu-id="97967-219">This scenario is best implemented by using the OData service endpoints to read order status information from Finance and Operations.</span></span>

<span data-ttu-id="97967-220">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-220">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-221">注文のステータス情報を読むために必要なエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="97967-221">Determine the entity that is required in order to read order status information.</span></span>
- <span data-ttu-id="97967-222">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-222">Make sure that the OData service endpoint is available for the entity.</span></span>

<span data-ttu-id="97967-223">顧客のポータル サイトで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="97967-223">On the customer portal site:</span></span>

- <span data-ttu-id="97967-224">顧客は注文のステータスをチェックするとき、対応する注文を読み取ってそのステータスを取得するために、Finance and Operations にリアルタイムの OData 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="97967-224">When a customer checks the status of an order, make a real-time OData call to Finance and Operations to read the corresponding order and retrieve its status.</span></span>

### <a name="approve-boms"></a><span data-ttu-id="97967-225">BOM の承認</span><span class="sxs-lookup"><span data-stu-id="97967-225">Approve BOMs</span></span>

<span data-ttu-id="97967-226">会社は、Finance and Operations を実行しますが、オンプレミスでホストされている製品ライフサイクル管理 (PLM) システムを使用しています。</span><span class="sxs-lookup"><span data-stu-id="97967-226">A company runs Finance and Operations but uses a product lifecycle management (PLM) system that is hosted on-premises.</span></span> <span data-ttu-id="97967-227">PLM システムには、承認のために Finance and Operations に完成した部品表 (BOM) 情報を送信するワークフローがあります。</span><span class="sxs-lookup"><span data-stu-id="97967-227">The PLM system has a workflow that sends the finished bill of materials (BOM) information to Finance and Operations for approval.</span></span>

| <span data-ttu-id="97967-228">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-228">Decision</span></span>                    | <span data-ttu-id="97967-229">情報</span><span class="sxs-lookup"><span data-stu-id="97967-229">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="97967-230">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-230">Is real-time data required?</span></span> | <span data-ttu-id="97967-231">有</span><span class="sxs-lookup"><span data-stu-id="97967-231">Yes</span></span>                    |
| <span data-ttu-id="97967-232">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-232">Peak data volume</span></span>            | <span data-ttu-id="97967-233">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="97967-233">1,000 records per hour</span></span> |
| <span data-ttu-id="97967-234">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-234">Frequency</span></span>                   | <span data-ttu-id="97967-235">アドホック</span><span class="sxs-lookup"><span data-stu-id="97967-235">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="97967-236">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-236">Recommended solution</span></span>

<span data-ttu-id="97967-237">このシナリオは、OData アクションを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="97967-237">This scenario can be implemented by using an OData action.</span></span>

<span data-ttu-id="97967-238">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-238">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-239">統合に必要なエンティティを決定する</span><span class="sxs-lookup"><span data-stu-id="97967-239">Determine the entity that is required for the integration.</span></span>
- <span data-ttu-id="97967-240">OData サービス エンドポイントがエンティティに対して使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-240">Make sure that the OData service endpoints are available for the entity.</span></span>
- <span data-ttu-id="97967-241">エンティティで、必要なビジネス ロジックを実行するアクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="97967-241">On the entity, create an action to run the required business logic.</span></span>

<span data-ttu-id="97967-242">PLM ソリューション:</span><span class="sxs-lookup"><span data-stu-id="97967-242">In the PLM solution:</span></span>

- <span data-ttu-id="97967-243">PLM システムで、BOM を承認する OData アクションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97967-243">Make the PLM system invoke the OData action to approve the BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="97967-244">このタイプの OData アクションは **BOMBillOfMaterialsHeaderEntity::approve** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="97967-244">You can find an example of this type of OData action in **BOMBillOfMaterialsHeaderEntity::approve**.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-a-custom-service"></a><span data-ttu-id="97967-245">カスタム サービスを使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="97967-245">Typical scenarios and patterns that use a custom service</span></span>

<span data-ttu-id="97967-246">カスタム サービスを使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="97967-246">Here are some typical scenarios that use a custom service.</span></span>

### <a name="look-up-on-hand-inventory"></a><span data-ttu-id="97967-247">手持在庫の検索</span><span class="sxs-lookup"><span data-stu-id="97967-247">Look up on-hand inventory</span></span>

<span data-ttu-id="97967-248">エネルギー会社にはヒーターのインストール ジョブをスケジュールするフィールド作業者がいます。</span><span class="sxs-lookup"><span data-stu-id="97967-248">An energy company has field workers who schedule installation jobs for heaters.</span></span> <span data-ttu-id="97967-249">この会社はバック オフィスとサード パーティのサービスとしてのソフトウェア (SaaS) のために Finance and Operations を使用して予定をスケジューリングします。</span><span class="sxs-lookup"><span data-stu-id="97967-249">This company uses Finance and Operations for the back office and third-party software as a service (SaaS) to schedule appointments.</span></span> <span data-ttu-id="97967-250">現場作業員が予定をスケジュールするときは、ジョブに使用できるインストール パーツがあることを確認するために、引当可能在庫数を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-250">When field workers schedule appointments, they must look up inventory availability to make sure that installation parts are available for the job.</span></span>

| <span data-ttu-id="97967-251">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-251">Decision</span></span>                    | <span data-ttu-id="97967-252">情報</span><span class="sxs-lookup"><span data-stu-id="97967-252">Information</span></span>            |
|-----------------------------|------------------------|
| <span data-ttu-id="97967-253">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-253">Is real-time data required?</span></span> | <span data-ttu-id="97967-254">有</span><span class="sxs-lookup"><span data-stu-id="97967-254">Yes</span></span>                    |
| <span data-ttu-id="97967-255">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-255">Peak data volume</span></span>            | <span data-ttu-id="97967-256">時間当たり 1,000 レコード</span><span class="sxs-lookup"><span data-stu-id="97967-256">1,000 records per hour</span></span> |
| <span data-ttu-id="97967-257">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-257">Frequency</span></span>                   | <span data-ttu-id="97967-258">アドホック</span><span class="sxs-lookup"><span data-stu-id="97967-258">Ad hoc</span></span>                 |

#### <a name="recommended-solution"></a><span data-ttu-id="97967-259">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-259">Recommended solution</span></span>

<span data-ttu-id="97967-260">このシナリオは、カスタム サービスを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="97967-260">This scenario can be implemented by using a custom service.</span></span>

<span data-ttu-id="97967-261">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-261">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-262">特定のアイテムの現物手持在庫を計算するカスタム サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="97967-262">Create a custom service to calculate the physical on-hand inventory for a given item.</span></span>

<span data-ttu-id="97967-263">スケジューリング アプリケーション:</span><span class="sxs-lookup"><span data-stu-id="97967-263">In the scheduling application:</span></span>

- <span data-ttu-id="97967-264">選択した品目の在庫情報を取得するために、SOAP または REST を通じてカスタム サービス エンドポイントへのリアルタイムな呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="97967-264">Make a real-time call to a custom service endpoint, through either SOAP or REST, to retrieve inventory information for the selected item.</span></span>

> [!NOTE]
> <span data-ttu-id="97967-265">このタイプのカスタム サービスの例は、Retail Real Time Services が実装された **RetailTransactionServiceInventory::inventoryLookup** で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="97967-265">You can find an example of this type of custom service in the Retail Real Time Services implementation: **RetailTransactionServiceInventory::inventoryLookup**.</span></span>

<span data-ttu-id="97967-266">また、inventorySiteOnHand エンティティを使用して同じ結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="97967-266">You can also use the inventorySiteOnHand entity to achieve the same result.</span></span> <span data-ttu-id="97967-267">場合によっては、複数のメソッドを使用して、Finance and Operations で同じデータとビジネス ロジックを公開できます。すべてのメソッドが同じように有効になり、効果を持ちます。</span><span class="sxs-lookup"><span data-stu-id="97967-267">Sometimes, you can use multiple methods to expose the same data and business logic in Finance and Operations, and all the methods are equally valid and effective.</span></span> <span data-ttu-id="97967-268">この場合、特定のシナリオを最適に機能して、開発者が最も使いやすいメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="97967-268">In this case, choose the method that works best for a given scenario and that a developer is most comfortable with.</span></span>

## <a name="typical-scenarios-and-patterns-that-use-batch-data-integrations"></a><span data-ttu-id="97967-269">バッチ データ統合を使用する一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="97967-269">Typical scenarios and patterns that use batch data integrations</span></span>

<span data-ttu-id="97967-270">バッチ データ API を使用する典型的なシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="97967-270">Here are some typical scenarios that use batch data APIs.</span></span>

### <a name="import-large-volumes-of-sales-orders"></a><span data-ttu-id="97967-271">大量の販売注文のインポート</span><span class="sxs-lookup"><span data-stu-id="97967-271">Import large volumes of sales orders</span></span>

<span data-ttu-id="97967-272">会社は、オンプレミスを実行するフロント エンド システムから大量の販売注文を受信します。</span><span class="sxs-lookup"><span data-stu-id="97967-272">A company receives a large volume of sales orders from a front-end system that runs on-premises.</span></span> <span data-ttu-id="97967-273">これらの注文は、定期的に処理、管理するために Finance and Operations に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-273">These orders must periodically be sent to Finance and Operations for processing and management.</span></span>

| <span data-ttu-id="97967-274">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-274">Decision</span></span>                    | <span data-ttu-id="97967-275">情報</span><span class="sxs-lookup"><span data-stu-id="97967-275">Information</span></span>                 |
|-----------------------------|-----------------------------|
| <span data-ttu-id="97967-276">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-276">Is real-time data required?</span></span> | <span data-ttu-id="97967-277">無</span><span class="sxs-lookup"><span data-stu-id="97967-277">No</span></span>                          |
| <span data-ttu-id="97967-278">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-278">Peak data volume</span></span>            | <span data-ttu-id="97967-279">時間当たり 200,000 レコード</span><span class="sxs-lookup"><span data-stu-id="97967-279">200,000 records per hour</span></span>    |
| <span data-ttu-id="97967-280">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-280">Frequency</span></span>                   | <span data-ttu-id="97967-281">5 分間隔で 1 回</span><span class="sxs-lookup"><span data-stu-id="97967-281">One time every five minutes</span></span> |

#### <a name="recommended-solution"></a><span data-ttu-id="97967-282">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-282">Recommended solution</span></span>

<span data-ttu-id="97967-283">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="97967-283">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="97967-284">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-284">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-285">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="97967-285">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="97967-286">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-286">Make sure that data management is enabled for the entities.</span></span>

<span data-ttu-id="97967-287">オンプレミスシステム:</span><span class="sxs-lookup"><span data-stu-id="97967-287">In the on-premises system:</span></span>

- <span data-ttu-id="97967-288">Finance and Operations にファイルをインポートするには、REST バッチ データ API を使用します。</span><span class="sxs-lookup"><span data-stu-id="97967-288">Use the REST batch data API to import files into Finance and Operations.</span></span>

### <a name="export-large-volumes-of-purchase-orders"></a><span data-ttu-id="97967-289">大量の発注書をエクスポート</span><span class="sxs-lookup"><span data-stu-id="97967-289">Export large volumes of purchase orders</span></span>

<span data-ttu-id="97967-290">会社は、Finance and Operations で大量の発注書を生成し、オンプレミス在庫管理システムを使用して製品を入庫します。</span><span class="sxs-lookup"><span data-stu-id="97967-290">A company generates a large volume of purchase orders in Finance and Operations and uses an on-premises inventory management system to receive products.</span></span> <span data-ttu-id="97967-291">発注書は、Finance and Operations からオンプレミス インベントリ システムに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-291">Purchase orders must be moved from Finance and Operations to the on-premises inventory system.</span></span>

| <span data-ttu-id="97967-292">意思決定</span><span class="sxs-lookup"><span data-stu-id="97967-292">Decision</span></span>                    | <span data-ttu-id="97967-293">情報</span><span class="sxs-lookup"><span data-stu-id="97967-293">Information</span></span>               |
|-----------------------------|---------------------------|
| <span data-ttu-id="97967-294">リアルタイムな日付が必要ですか。</span><span class="sxs-lookup"><span data-stu-id="97967-294">Is real-time data required?</span></span> | <span data-ttu-id="97967-295">無</span><span class="sxs-lookup"><span data-stu-id="97967-295">No</span></span>                        |
| <span data-ttu-id="97967-296">ピーク データ量</span><span class="sxs-lookup"><span data-stu-id="97967-296">Peak data volume</span></span>            | <span data-ttu-id="97967-297">時間当たり 300,000 レコード</span><span class="sxs-lookup"><span data-stu-id="97967-297">300,000 records per hour</span></span>  |
| <span data-ttu-id="97967-298">頻度</span><span class="sxs-lookup"><span data-stu-id="97967-298">Frequency</span></span>                   | <span data-ttu-id="97967-299">1 時間あたり 1 回</span><span class="sxs-lookup"><span data-stu-id="97967-299">One time per hour</span></span>         |

#### <a name="recommended-solution"></a><span data-ttu-id="97967-300">推奨される解決策</span><span class="sxs-lookup"><span data-stu-id="97967-300">Recommended solution</span></span>

<span data-ttu-id="97967-301">このシナリオは、バッチ データ API を使用すると最もよく実装されます。</span><span class="sxs-lookup"><span data-stu-id="97967-301">This scenario is best implemented by using batch data APIs.</span></span>

<span data-ttu-id="97967-302">Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="97967-302">In Finance and Operations:</span></span>

- <span data-ttu-id="97967-303">統合に必要なすべてのエンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="97967-303">Determine all the entities that are required for the integration.</span></span>
- <span data-ttu-id="97967-304">エンティティに対してデータ管理が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-304">Make sure that data management is enabled for the entities.</span></span>
- <span data-ttu-id="97967-305">差分プッシュする必要がある場合は、エンティティの変更履歴を有効にできるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="97967-305">If incremental push is required, make sure that change tracking can be enabled on the entities.</span></span>

<span data-ttu-id="97967-306">オンプレミス在庫システム:</span><span class="sxs-lookup"><span data-stu-id="97967-306">In the on-premises inventory system:</span></span>

- <span data-ttu-id="97967-307">REST バッチ データ API を使用して、Finance and Operations からファイルをエクスポートし、在庫システムにインポートします。</span><span class="sxs-lookup"><span data-stu-id="97967-307">Use the REST batch data API to export the file from Finance and Operations and import it into the inventory system.</span></span>

## <a name="typical-scenarios-and-patterns-that-call-external-web-services"></a><span data-ttu-id="97967-308">外部の Web サービスを呼び出す一般的なシナリオとパターン</span><span class="sxs-lookup"><span data-stu-id="97967-308">Typical scenarios and patterns that call external web services</span></span>

<span data-ttu-id="97967-309">通常、Finance and Operations はオンプレミスまたは別の SaaS プロバイダーによってホストされている外部 Web サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97967-309">It's typical that Finance and Operations calls out to an external web service that is hosted either on-premises or by another SaaS provider.</span></span> <span data-ttu-id="97967-310">この場合、Finance and Operations は統合クライアントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="97967-310">In this case, Finance and Operations acts as the integration client.</span></span> <span data-ttu-id="97967-311">Finance and Operation の統合クライアントを作成するときは、他のアプリケーションの統合クライアントを作成するときと同じベスト プラクティスおよびガイドラインのセットに従ってください。</span><span class="sxs-lookup"><span data-stu-id="97967-311">When you write an integration client for Finance and Operations, you should follow the same set of best practices and guidelines that you follow when you write an integration client for any other application.</span></span> <span data-ttu-id="97967-312">単純な例として、[外部 Web サービスの使用](consume-external-web-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="97967-312">For a simple example, see [Consuming external web services](consume-external-web-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97967-313">セキュリティ要件のため、Finance and Operations の生産とサンドボックス環境では、トランスポート層セキュリティ (TLS) 1.2 以降を使用するセキュリティ保護された通信のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="97967-313">Because of security requirements, Finance and Operations production and sandbox environments support only secured communication that uses Transport Layer Security (TLS) 1.2 or later.</span></span> <span data-ttu-id="97967-314">つまり、Finance and Operations が呼び出すターゲットの Web サービス エンドポイントは、TLS 1.2 以降をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="97967-314">In other words, the target web service endpoint that Finance and Operations calls out to must support TLS 1.2 or later.</span></span> <span data-ttu-id="97967-315">ターゲット サービス エンドポイントがこの要件を満たしていない場合、Finance and Operations からの呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="97967-315">If the target service endpoint doesn't meet this requirement, calls from Finance and Operations fail.</span></span> <span data-ttu-id="97967-316">例外エラー メッセージは、次のメッセージのようになります。</span><span class="sxs-lookup"><span data-stu-id="97967-316">The exception error message resembles the following message:</span></span>
>
> <span data-ttu-id="97967-317">*「転送接続からデータを読み取ることができません: 既存の接続がリモート ホストによって強制的に切断されました。」*</span><span class="sxs-lookup"><span data-stu-id="97967-317">*Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.*</span></span>
>
> <span data-ttu-id="97967-318">TLS 1.2 またはそれ以降のバージョンを使用することが原因で対象サービスを変更できない場合は、次の図に示すように、ブローカー サービスを導入して 2 ホップ コールを行うことでこの問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="97967-318">If you can't modify the target service so that it uses TLS 1.2 or later, you can work around this issue by introducing a broker service and making a two-hop call, as shown in the following illustration.</span></span>
>
> ![TLS の要件](./media/integration-tls.png)
