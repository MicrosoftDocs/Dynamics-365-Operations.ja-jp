---
title: ビジネス イベント開発者ドキュメント
description: このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 05/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: b8cc984908e6acfcb65684234337c67de23e1411
ms.sourcegitcommit: f7e1720ffa3e34c787ca0f93d561cb75cbbb540a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/23/2019
ms.locfileid: "1605761"
---
# <a name="business-events-developer-documentation"></a><span data-ttu-id="9f945-103">ビジネス イベント開発者ドキュメント</span><span class="sxs-lookup"><span data-stu-id="9f945-103">Business events developer documentation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9f945-104">このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9f945-104">This topic walks you through the development process and best practices for implementing business events.</span></span>

## <a name="what-is-a-business-event-and-what-is-not-a-business-event"></a><span data-ttu-id="9f945-105">何がビジネス イベントで、何がビジネス イベントではないか。</span><span class="sxs-lookup"><span data-stu-id="9f945-105">What is a business event and what is not a business event?</span></span>
<span data-ttu-id="9f945-106">ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。</span><span class="sxs-lookup"><span data-stu-id="9f945-106">This question comes up every time we start to think about use cases where business events can help.</span></span> <span data-ttu-id="9f945-107">仕入先の作成はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="9f945-107">Is creation of a vendor a business event?</span></span> <span data-ttu-id="9f945-108">または、発注書の確認はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="9f945-108">Or is confirming a purchase order a business event?</span></span> <span data-ttu-id="9f945-109">テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="9f945-109">Is it a business event if you capture the event at the table level?</span></span> <span data-ttu-id="9f945-110">または、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="9f945-110">Or should business events only be captured at the business logic level in a business process?</span></span> <span data-ttu-id="9f945-111">これらは有効な質問であるだけでなく、統合のソリューションを計画および構築するときに考察するキー トピックです。</span><span class="sxs-lookup"><span data-stu-id="9f945-111">These are not only valid questions, but also a key topic of discussion when planning and architecting a solution for integration.</span></span> <span data-ttu-id="9f945-112">次のガイドラインは、この思考過程および決定作業を支援するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9f945-112">The following guidelines can be used to help with this thought process and decision making.</span></span>

<a name="intent"></a><span data-ttu-id="9f945-113">目的</span><span class="sxs-lookup"><span data-stu-id="9f945-113">Intent</span></span>
------

<span data-ttu-id="9f945-114">ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-114">The intent behind capturing the business event must be clearly understood.</span></span> <span data-ttu-id="9f945-115">つまり、ビジネス イベントをキャプチャする理由および受信者が使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="9f945-115">In other words, what is the reason for capturing the business event and how it is going to be used by the recipient.</span></span>

<span data-ttu-id="9f945-116">ビジネス イベントをキャプチャする目的が、Finance and Operations で発生したビジネス イベントに応答して Finance and Operations 外でビジネス アクションを実行することである場合は、これはビジネス イベントをキャプチャする有効な目的です。</span><span class="sxs-lookup"><span data-stu-id="9f945-116">If the intent for capturing a business event is to take a business action outside of Finance and Operations in response to the business event happening in Finance and Operations, then this is a valid intent to capture the business event.</span></span> <span data-ttu-id="9f945-117">ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文を作成するなどのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-117">The business action that is taken in response to the business event can be to notify users about the business event and/or to call into another business application to take a business action like, creating a sales order.</span></span> <span data-ttu-id="9f945-118">ビジネス アクションを、実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。</span><span class="sxs-lookup"><span data-stu-id="9f945-118">It is important to look at the business action generically and not base the need for a business event on the type of business action that will be taken.</span></span>

<span data-ttu-id="9f945-119">ビジネス イベントをキャプチャする目的がデータを他の受信者に転送して、事実上データ エクスポート シナリオを実現することである場合、これはビジネス イベントを使用するための良いユース ケースではありません。</span><span class="sxs-lookup"><span data-stu-id="9f945-119">If the intent of capturing the business event is to transfer data to the recipient and in effect, realizing a data export scenario, then this will not be a good use case for using business events.</span></span> <span data-ttu-id="9f945-120">実際、データ転送ユース ケースのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用となります。</span><span class="sxs-lookup"><span data-stu-id="9f945-120">In fact, the use of business events for data transfer use cases will be a misuse of the business events framework.</span></span>
<span data-ttu-id="9f945-121">このようなシナリオでは、データ管理で既に使用可能なデータ エクスポート メカニズムを使用し続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-121">Such scenarios must continue to use data export mechanisms already available in data management.</span></span>

<a name="fidelity"></a><span data-ttu-id="9f945-122">忠実性</span><span class="sxs-lookup"><span data-stu-id="9f945-122">Fidelity</span></span>
--------

<span data-ttu-id="9f945-123">目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために必要なアプローチを評価することです。</span><span class="sxs-lookup"><span data-stu-id="9f945-123">When the intent is clear and a legitimate need for a business event is established, the next step is to evaluate the approach that must be taken to capture the business event.</span></span> <span data-ttu-id="9f945-124">次のセクションでは、評価する必要があるアプローチを要約します。</span><span class="sxs-lookup"><span data-stu-id="9f945-124">The following section summarizes the approach that must be evaluated.</span></span>

<span data-ttu-id="9f945-125">どのアプローチを採用するかに関わらず、ビジネス イベントの忠実性のためには以下の点を考慮することが重要で、結果として、ビジネス イベントを実装するためのデザイン選択に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="9f945-125">Regardless of which approach is taken, the fidelity of business events is significant to ensure the following aspects are taken care of and as a result, must influence the design choice for implementing the business event.</span></span> <span data-ttu-id="9f945-126">ただし、ビジネス イベントを実装するためのデザイン選択がビジネス イベントのコンセプトには影響を与えないようにします。選択されたデザインは、それがビジネス イベントであるか決定するための決定ツールとして使用すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9f945-126">However, the design choice that you take to implement a business event must not influence the concept of business events--the chosen design must not be used as a decision-making tool to determine if it is a business event.</span></span> <span data-ttu-id="9f945-127">このような決定には、事前に考慮された目的を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-127">The intent discussed previously must be used for such decisions.</span></span>

-   <span data-ttu-id="9f945-128">**堅牢なビジネス イベント** - 間違ったビジネス イベントを受信者に送信するべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9f945-128">**Durable business events** - There should be no false business events sent to the recipient.</span></span> <span data-ttu-id="9f945-129">発注書確認ビジネス イベントが送信済みの場合、受取人はその発注書が確認済みであることを信用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-129">If a purchase order confirmation business event was sent out, then the recipient must trust that the purchase order was indeed confirmed.</span></span> <span data-ttu-id="9f945-130">デザイン選択はこの取引の性質を保証する必要があり、この予想に反するデザイン選択を採用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="9f945-130">The design choice must ensure this transactional nature and hence must not take a design choice that would violate this expectation.</span></span>

-   <span data-ttu-id="9f945-131">**目標** - ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-131">**Targeted** - Business events must be designed to optimize the consumption story for the recipient.</span></span> <span data-ttu-id="9f945-132">つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にします。</span><span class="sxs-lookup"><span data-stu-id="9f945-132">In other words, make it as easy as possible for the recipient to consume business events.</span></span> <span data-ttu-id="9f945-133">このため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-133">Hence, business events must be as specific as possible and targeted to a specific use case.</span></span> <span data-ttu-id="9f945-134">そのためビジネス イベントは一般的なものではなく、コンシューマーがペイロードを理解するよう試みてビジネス イベントが何であったか判断させるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9f945-134">Business events must not be generic thereby, leaving the consumer to determine what the business event was for by trying to understand the payload.</span></span> <span data-ttu-id="9f945-135">実行されたデザイン選択は、これが順守されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-135">The design choice made must allow for this to be preserved.</span></span>

-   <span data-ttu-id="9f945-136">**ノイズレス** - デザイン内でノイズを除外するための努力が最小になるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-136">**Noiseless** - There should be very little effort in the design to filter out the noise.</span></span> <span data-ttu-id="9f945-137">ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルタ ロジックの記述を避けます。</span><span class="sxs-lookup"><span data-stu-id="9f945-137">To make business events very specific, avoid writing filtering logic to filter out conditions that do not match the expected business event.</span></span> <span data-ttu-id="9f945-138">選択したアプローチは、ビジネス イベントがコードで実装されるポイントが、ノイズのフィルター処理が必要ないほど明確である必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-138">The chosen approach must be such that the point at which the business event is implemented in code is specific enough to avoid the need for any filtering of noise.</span></span> <span data-ttu-id="9f945-139">ロジックの追加によってノイズをフィルター処理する試みはパフォーマンスの負荷になるだけでなく、特定のユース ケースに基づき複雑になる機能性があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-139">Any attempt to filter the noise by adding logic can not only be taxing on performance but, it may also get complicated based on specific use cases.</span></span>

| <span data-ttu-id="9f945-140">**ビジネス ロジック レベルでのキャプチャ**</span><span class="sxs-lookup"><span data-stu-id="9f945-140">**Capturing at business logic level**</span></span>                                                                                    | <span data-ttu-id="9f945-141">**テーブル レベルでのキャプチャ**</span><span class="sxs-lookup"><span data-stu-id="9f945-141">**Capturing at table level**</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f945-142">トランザクション内に置いて堅牢性を確保する</span><span class="sxs-lookup"><span data-stu-id="9f945-142">Ensures durability by being in the transaction</span></span>                                                                           | <span data-ttu-id="9f945-143">トランザクション内に置いて堅牢性を確保します。</span><span class="sxs-lookup"><span data-stu-id="9f945-143">Ensures durability by being in the transaction.</span></span>                                                                      |
| <span data-ttu-id="9f945-144">対象となるビジネス イベントを許可します。</span><span class="sxs-lookup"><span data-stu-id="9f945-144">Allows for targeted business events.</span></span>                                                                                     | <span data-ttu-id="9f945-145">イベントのキャプチャが低レベルであるため対象となるビジネス イベントを有効にすることが困難です。</span><span class="sxs-lookup"><span data-stu-id="9f945-145">Difficult to enable targeted business events due to the lower level capturing of events.</span></span>                             |
| <span data-ttu-id="9f945-146">簡単にノイズレスのままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="9f945-146">Makes it easy to remain noiseless.</span></span>                                                                                       | <span data-ttu-id="9f945-147">ノイズを除去するためのサウンド ロジックを導入する追加作業が行われるまで、ノイズレスのままにすることは困難です。</span><span class="sxs-lookup"><span data-stu-id="9f945-147">Difficult to remain noiseless unless additional effort is taken to put sound logic in place to filter out the noise.</span></span> |
| <span data-ttu-id="9f945-148">堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-148">Provides additional context of the business process, which can significantly improve the durability and the quality of payload.</span></span> | <span data-ttu-id="9f945-149">イベントのキャプチャが低レベルであると、ビジネス プロセスのコンテキストが失われる可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="9f945-149">Business process context is most likely lost due to the lower level capturing of events.</span></span>                             |


## <a name="implementing-a-business-event"></a><span data-ttu-id="9f945-150">ビジネス イベントの実装</span><span class="sxs-lookup"><span data-stu-id="9f945-150">Implementing a business event</span></span>

<span data-ttu-id="9f945-151">ビジネス イベントを実装して送信することは非常に簡単なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="9f945-151">Implementing a business event and sending it is a fairly straightforward process:</span></span>
1. <span data-ttu-id="9f945-152">契約を構築します。</span><span class="sxs-lookup"><span data-stu-id="9f945-152">Build the contract.</span></span>
2. <span data-ttu-id="9f945-153">イベントを構築します。</span><span class="sxs-lookup"><span data-stu-id="9f945-153">Build the event.</span></span>
3. <span data-ttu-id="9f945-154">イベントを送信するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9f945-154">Add code to send the event.</span></span> 

<span data-ttu-id="9f945-155">以下の 2 つのクラスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-155">Two classes must be implemented:</span></span>

- <span data-ttu-id="9f945-156">**ビジネス イベント** - このクラスは **BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9f945-156">**Business event** – This class extends the **BusinessEventsBase** class.</span></span> <span data-ttu-id="9f945-157">ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-157">It provides support for constructing the business event, building the payload, and sending the business event.</span></span>
- <span data-ttu-id="9f945-158">**ビジネス イベント契約** - このクラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9f945-158">**Business event contract** – This class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="9f945-159">ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="9f945-159">It defines the payload of the business event and allows for population of the contract at runtime.</span></span> 

### <a name="businesseventsbase-extension"></a><span data-ttu-id="9f945-160">BusinessEventsBase 拡張機能</span><span class="sxs-lookup"><span data-stu-id="9f945-160">BusinessEventsBase extension</span></span>

#### <a name="naming-convention"></a><span data-ttu-id="9f945-161">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="9f945-161">Naming convention</span></span>

<span data-ttu-id="9f945-162">ビジネス イベントの名前は以下のパターンに従う必要があります: <名詞/名詞句><past tense action>BusinessEvent</span><span class="sxs-lookup"><span data-stu-id="9f945-162">The names of business events should follow this pattern: <noun/noun phrase><past tense action>BusinessEvent</span></span>

<span data-ttu-id="9f945-163">**例**</span><span class="sxs-lookup"><span data-stu-id="9f945-163">**Examples**</span></span>

- <span data-ttu-id="9f945-164">VendorInvoicePostedBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="9f945-164">VendorInvoicePostedBusinessEvent</span></span>
- <span data-ttu-id="9f945-165">CollectionLetterSentBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="9f945-165">CollectionLetterSentBusinessEvent</span></span>

<span data-ttu-id="9f945-166">名前の <名詞/名詞句> パートは、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-166">The <noun/noun phrase> part of the name should comply with existing definitions for application area prefixes.</span></span>

#### <a name="implementation"></a><span data-ttu-id="9f945-167">実装</span><span class="sxs-lookup"><span data-stu-id="9f945-167">Implementation</span></span>

<span data-ttu-id="9f945-168">**BusinessEventsBase** 拡張機能を実装するプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="9f945-168">The process of implementing a **BusinessEventsBase** extension is straightforward.</span></span> <span data-ttu-id="9f945-169">**BusinessEventsBase** クラスの拡張、および静的コンストラクター メソッドの実装、プライベート **新規** メソッド、内部状態を保持するメソッド、および **buildContract** メソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9f945-169">It involves extending the **BusinessEventsBase** class, and implementing a static constructor method, a private **new** method, methods to maintain internal state, and the **buildContract** method.</span></span>

1. <span data-ttu-id="9f945-170">静的 **newFrom<my_buffer>** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-170">Implement a static **newFrom<my_buffer>** method.</span></span> <span data-ttu-id="9f945-171">メソッド名の <my_buffer> パートは通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。</span><span class="sxs-lookup"><span data-stu-id="9f945-171">The <my_buffer> part of the method name is typically the table buffer that is used to initialize the business event contract.</span></span>

    ```
    static public SalesInvoicePostedBusinessEvent
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        SalesInvoicePostedBusinessEvent businessEvent = new
        SalesInvoicePostedBusinessEvent();
        businessEvent.parmCustInvoiceJour(_custInvoiceJour);
        return businessEvent;
    }
    ```

2. <span data-ttu-id="9f945-172">**BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9f945-172">Extend the **BusinessEventsBase** class.</span></span>

    ```
    [BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
    "AccountsReceivable:SalesOrderInvoicePostedBusinessEventName","AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription",ModuleAxapta::SalesOrder)]
    public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
    ```

    <span data-ttu-id="9f945-173">**BusinessEvents** 属性に注意してください。</span><span class="sxs-lookup"><span data-stu-id="9f945-173">Note the **BusinessEvents** attribute.</span></span> <span data-ttu-id="9f945-174">この属性は、ビジネス イベントの契約、名前、説明、および含まれるモジュールに関する情報を含む、ビジネス イベント フレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-174">This attribute provides the business events framework with information about the business event's contract, name, and description, and also the module that it's part of.</span></span> <span data-ttu-id="9f945-175">ラベルは、名前と説明の引数に定義する必要がありますが、ローカライズされたデータの保存を避けるため、「@」記号なしで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-175">Labels must be defined for the name and description arguments, but should be referenced without the '@' symbol to avoid storing localized data.</span></span>

3. <span data-ttu-id="9f945-176">プライベート **新規** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-176">Implement a private **new** method.</span></span> <span data-ttu-id="9f945-177">このメソッドは静的コンストラクター メソッドからのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-177">This method is called only from the static constructor method.</span></span>

    ```
    private void new()
    {
    }
    ```

4. <span data-ttu-id="9f945-178">内部状態を維持するプライベート **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-178">Implement private **parm** methods to maintain internal state.</span></span>

    ```
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour = custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    ```

5. <span data-ttu-id="9f945-179">**buildContract** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-179">Implement the **buildContract** method.</span></span> <span data-ttu-id="9f945-180">このステップには EventContract スタブが必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9f945-180">Note that you'll need an EventContract stub for this step.</span></span>

    ```
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return
        SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
    ```

    <span data-ttu-id="9f945-181">拡張機能のために、**buildContract** メソッドは **Wrappable(true)** および **Replaceable(true)** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-181">For extensibility, the **buildContract** method must be attributed with the **Wrappable(true)** and **Replaceable(true)** attributes.</span></span> <span data-ttu-id="9f945-182">**buildContract** メソッドは会社のためにビジネス イベントが有効にされるときにのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-182">The **buildContract** method will be called only when a business event is enabled for a company.</span></span>

<span data-ttu-id="9f945-183">これは、「転記された販売注文請求書」ビジネス イベントの完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="9f945-183">Here is the complete implementation of the "Sales order invoice posted" business event.</span></span>

```
/// <summary>
/// Sales order invoice posted business event.
/// </summary>
[BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
'AccountsReceivable:SalesOrderInvoicePostedBusinessEventName',
'AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription',
ModuleAxapta::SalesOrder)]
public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
{
    private CustInvoiceJour custInvoiceJour;
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour =
    custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    /// <summary\>
    /// Creates a SalesInvoicePostedBusinessEvent from a CustInvoiceJour record.
    /// <summary>
    /// param name = "_custInvoiceJour"> CustInvoiceJour record <param>
    /// <returns>A SalesInvoicePostedBusinessEvent </returns>
    static public SalesInvoicePostedBusinessEvent
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        SalesInvoicePostedBusinessEvent businessEvent = new
        SalesInvoicePostedBusinessEvent();
        businessEvent.parmCustInvoiceJour(_custInvoiceJour);
        return businessEvent;
    }
    private void new()
    {
    }
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
}
```

### <a name="businesseventscontract-extension"></a><span data-ttu-id="9f945-184">BusinessEventsContract 拡張機能</span><span class="sxs-lookup"><span data-stu-id="9f945-184">BusinessEventsContract extension</span></span>

<span data-ttu-id="9f945-185">ビジネス イベント契約クラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9f945-185">A business event contract class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="9f945-186">ビジネス イベントのペイロードを定義および入力します。</span><span class="sxs-lookup"><span data-stu-id="9f945-186">It defines and populates the payload of the business event.</span></span> <span data-ttu-id="9f945-187">ビジネス イベントには一部の変動がありますが、ビジネス イベント契約の基本構造は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="9f945-187">Although there is some variation across business events, the basic structure of the business event contract is consistent.</span></span>

<span data-ttu-id="9f945-188">ビジネス イベント契約の実装プロセスには、**BusinessEventContract** クラスの拡張、内部状態の定義、初期化メソッドの実装、静的コンストラクター メソッドの実装、および契約状態にアクセスするための **parm** メソッドの実装が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9f945-188">The process of implementing a business event contract involves extending the **BusinessEventContract** class, defining internal state, implementing an initialization method, implementing a static constructor method, and implementing **parm** methods to access the contract state.</span></span>

1. <span data-ttu-id="9f945-189">**BusinessEventContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9f945-189">Extend the **BusinessEventContract** class.</span></span>

    ```
    [DataContract]
    public final class SalesInvoicePostedBusinessEventContract extends
    BusinessEventsContract
    ```

    <span data-ttu-id="9f945-190">クラスは **DataContract** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-190">The class must be attributed with the **DataContract** attribute.</span></span>

2. <span data-ttu-id="9f945-191">契約状態を保持するプライベート変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="9f945-191">Add private variables to hold the contract state.</span></span>

    ```
    private CustInvoiceAccount invoiceAccount;
    private CustInvoiceId invoiceId;
    private SalesIdBase salesId;
    private TransDate invoiceDate;
    private DueDate invoiceDueDate;
    private AmountMST invoiceAmount;
    private TaxAmount invoiceTaxAmount;
    private LegalEntityDataAreaId legalEntity;
    ```

3. <span data-ttu-id="9f945-192">プライベート初期化メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-192">Implement a private initialization method.</span></span>

    ```
    private void initialize(CustInvoiceJour _custInvoiceJour)
    {
        invoiceAccount = _custInvoiceJour.InvoiceAccount;
        invoiceId = _custInvoiceJour.InvoiceId;
        salesId = _custInvoiceJour.SalesId;
        invoiceDate = _custInvoiceJour.InvoiceDate;
        invoiceDueDate = _custInvoiceJour.DueDate;
        invoiceAmount = _custInvoiceJour.InvoiceAmountMST;
        invoiceTaxAmount = _custInvoiceJour.SumTaxMST;
        legalEntity = _custInvoiceJour.DataAreaId;
    }
    ```

    <span data-ttu-id="9f945-193">**初期化** メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="9f945-193">The **initialize** method is responsible for setting the business event contract class's private state, based on data that is provided through the static constructor method.</span></span>

4. <span data-ttu-id="9f945-194">静的コンストラクター メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-194">Implement a static constructor method.</span></span>

    ```
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    ```

    <span data-ttu-id="9f945-195">静的コンストラクター メソッドはプライベート **初期化** メソッドを呼び出して、プライベート クラス状態を初期化します。</span><span class="sxs-lookup"><span data-stu-id="9f945-195">The static constructor method calls a private **initialize** method to initialize the private class state.</span></span>

5. <span data-ttu-id="9f945-196">契約状態にアクセスするための **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="9f945-196">Implement **parm** methods to access the contract state.</span></span>

    ```
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    ```

    <span data-ttu-id="9f945-197">**parm** メソッドは **DataMember('<name>')** および **BusinessEventsDataMember('<description>')** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-197">The **parm** methods should be attributed with the **DataMember('<name>')** and **BusinessEventsDataMember('<description>')** attributes.</span></span> <span data-ttu-id="9f945-198">属性で提供する名前 (たとえば、 **'InvoiceAccount'**) はデータ契約消費者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-198">The name that you provide on the attribute (for example **'InvoiceAccount'**) will be visible to data contract consumers.</span></span> <span data-ttu-id="9f945-199">BusinessEventsDataMember で指定された説明は、この契約のデータ メンバーを記述するときにビジネス イベント カタログ UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-199">The description provided in the BusinessEventsDataMember will be visible in the Business Events catalog UI when describing this contract's data members.</span></span>

> [!NOTE]
> - <span data-ttu-id="9f945-200">**RecId** 値はビジネス イベント ペイロードの一部にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="9f945-200">**RecId** values should not be part of a business event payload.</span></span> <span data-ttu-id="9f945-201">代わりに代替キー (AK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="9f945-201">Use the alternate key (AK) instead.</span></span>
> - <span data-ttu-id="9f945-202">列挙型 (enum) 値は、公開する前にそのシンボル値に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-202">Enumeration (enum) values must be converted to their symbol value before they can be published.</span></span> <span data-ttu-id="9f945-203">**enum2Symbol** メソッドを使用して列挙型の値をシンボル文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="9f945-203">Use the **enum2Symbol** method to convert an enum's value to the symbol string.</span></span> <span data-ttu-id="9f945-204">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="9f945-204">Here is an example:</span></span>
>
>    ```
>    status = enum2Symbol(enumNum(CustVendDisputeStatus), _custDispute.Status);
>    ```

<span data-ttu-id="9f945-205">場合によっては、データ契約の内部状態の投入のために、追加の取得メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-205">In some cases, population of the data contract's internal state will require that you implement additional retrieval methods.</span></span> <span data-ttu-id="9f945-206">これらの取得メソッドはプライベート メソッドとして実装し、**初期化** メソッドから呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-206">These retrieval methods should be implemented as private methods, and they should be called from the **initialize** method.</span></span>

<span data-ttu-id="9f945-207">これは、「転記された販売注文請求書」ビジネス イベント契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="9f945-207">Here is the complete implementation of the "Sales order invoice posted" business event contract.</span></span>

```
/// <summary>
/// The data contract for a SalesInvoicePostedBusinessEvent
/// </summary>
[DataContract]
public final class SalesInvoicePostedBusinessEventContract extends
BusinessEventsContract
{
    private CustInvoiceAccount invoiceAccount;
    private CustInvoiceId invoiceId;
    private SalesIdBase salesId;
    private TransDate invoiceDate;
    private DueDate invoiceDueDate;
    private AmountMST invoiceAmount;
    private TaxAmount invoiceTaxAmount;
    private LegalEntityDataAreaId legalEntity;
    /// <summary>
    /// Creates a SalesInvoicePostedBusinessEventContract from a CustInvoiceJour record.
    /// </summary>
    /// <param name = "_custInvoiceJour"> CustInvoiceJour record</param>
    /// <returns>A SalesInvoicePostedBusinessEventContract </returns>
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    private void initialize(CustInvoiceJour _custInvoiceJour)
    {
        invoiceAccount = _custInvoiceJour.InvoiceAccount;
        invoiceId = _custInvoiceJour.InvoiceId;
        salesId = _custInvoiceJour.SalesId;
        invoiceDate = _custInvoiceJour.InvoiceDate;
        invoiceDueDate = _custInvoiceJour.DueDate;
        invoiceAmount = _custInvoiceJour.InvoiceAmountMST;
        invoiceTaxAmount = _custInvoiceJour.SumTaxMST;
        legalEntity = _custInvoiceJour.DataAreaId;
    }
    private void new()
    {
    }
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
    = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    [DataMember('InvoiceId'), BusinessEventsDataMember("@AccountsReceivable:BusinessEventInvoiceId")]
    public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId = invoiceId)
    {
    invoiceId = _invoiceId;
    return invoiceId;
    }
    [DataMember('SalesOrderId'), BusinessEventsDataMember("@AccountsReceivable:SalesOrderId")]
    public SalesIdBase parmSaleOrderId(SalesIdBase _salesId = salesId)
    {
        salesId = _salesId;
        return salesId;
    }
    [DataMember('InvoiceDate'), BusinessEventsDataMember("@AccountsReceivable:BusinessEventInvoiceDate")]
    public TransDate parmInvoiceDate(TransDate _invoiceDate = invoiceDate)
    {
        invoiceDate = _invoiceDate;
        return invoiceDate;
    }
    [DataMember('InvoiceDueDate'), BusinessEventsDataMember("@AccountsReceivable:InvoiceDueDate")]
    public DueDate parmInvoiceDueDate(DueDate _invoiceDueDate = invoiceDueDate)
    {
        invoiceDueDate = _invoiceDueDate;
        return invoiceDueDate;
    }
    [DataMember('InvoiceAmountInAccountingCurrency'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAmountInAccountingCurrency")]
    public AmountMST parmInvoiceAmount(AmountMST _invoiceAmount = invoiceAmount)
    {
        invoiceAmount = _invoiceAmount;
        return invoiceAmount;
    }
    [DataMember('InvoiceTaxAmount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceTaxAmount")]
    public TaxAmount parmInvoiceTaxAmount(TaxAmount _invoiceTaxAmount =
    invoiceTaxAmount)
    {
        invoiceTaxAmount = _invoiceTaxAmount;
        return invoiceTaxAmount;
    }
    [DataMember('LegalEntity'), BusinessEventsDataMember("@AccountsReceivable:LegalEntity")]
    public LegalEntityDataAreaId parmLegalEntity(LegalEntityDataAreaId _legalEntity
    = legalEntity)
    {
        legalEntity = _legalEntity;
        return legalEntity;
    }
}
```

## <a name="sending-a-business-event"></a><span data-ttu-id="9f945-208">ビジネス イベントの送信</span><span class="sxs-lookup"><span data-stu-id="9f945-208">Sending a business event</span></span>

<span data-ttu-id="9f945-209">適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-209">You must modify application code so that it sends the business event at the appropriate point.</span></span> <span data-ttu-id="9f945-210">多くの場合、フレームワーク内の共通ポイントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9f945-210">Often, you can use a common point within a framework.</span></span> <span data-ttu-id="9f945-211">**SourceDocument** を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-211">Documents that extend **SourceDocument** have a common point for creating and sending a business event.</span></span> <span data-ttu-id="9f945-212">詳細については、以下をサポートする元伝票フレームワークのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f945-212">For more information, see the section on source document framework support below.</span></span>

<span data-ttu-id="9f945-213">また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-213">Other frameworks also provide common points for sending business events.</span></span> <span data-ttu-id="9f945-214">たとえば、AOT 内の **CustVendVoucher** クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、**転記** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-214">For example, the **CustVendVoucher** class hierarchy in AOT has a **post** method that is used to send business events that are related to posting customer or vendor vouchers.</span></span> <span data-ttu-id="9f945-215">基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-215">Overrides of the base class implementation provide specialization of the logic for sending business events.</span></span> <span data-ttu-id="9f945-216">例については、AOT の **CustVoucher.createBusinessEvent** または **VendVoucher.createBusinessEvent** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f945-216">For an example, see **CustVoucher.createBusinessEvent** or **VendVoucher.createBusinessEvent** in AOT.</span></span>

<span data-ttu-id="9f945-217">ビジネス イベントの送信は、基になる取引のコミットにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="9f945-217">The sending of a business event is linked to the commit of the underlying transaction.</span></span> <span data-ttu-id="9f945-218">基になる取引が中止される場合、ビジネス イベントは送信されません。</span><span class="sxs-lookup"><span data-stu-id="9f945-218">If the underlying transaction is aborted, the business event won't be sent.</span></span> <span data-ttu-id="9f945-219">そのため、アプリケーションはペイロード情報が使用可能なポイントでビジネス イベントを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="9f945-219">Therefore, applications can send the business event at the point where the payload information is available.</span></span>

<span data-ttu-id="9f945-220">ビジネス イベント フレームワークは、ビジネス イベントが消費者に公開されるかどうか決定します。</span><span class="sxs-lookup"><span data-stu-id="9f945-220">The business events framework determines whether a business event is published to a consumer.</span></span> <span data-ttu-id="9f945-221">一般的なルールとして、ビジネス イベントが有効かどうかに関わらず、アプリケーションはビジネス イベントを常に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-221">As a general rule, applications should always send a business event, regardless of whether the business event is enabled.</span></span> <span data-ttu-id="9f945-222">重要な追加ロジックが必要な場合、またはビジネス イベントを送信するためのロジックがパフォーマンスに影響する場合は、ビジネス イベントの送信に関連付けられたビジネス ロジックを実行する前に、アプリケーションは特定のビジネス イベントが有効化されているかどうか確認することができます。</span><span class="sxs-lookup"><span data-stu-id="9f945-222">If significant additional logic is required, or if the logic for sending a business event has a performance impact, an application can check whether a specific business event is enabled before it runs business logic that is associated with sending business events.</span></span> <span data-ttu-id="9f945-223">この確認は **BusinessEventsConfigurationReader::isBusinessEventEnabled** メソッドを介して実行されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-223">This check is done through the **BusinessEventsConfigurationReader::isBusinessEventEnabled** method.</span></span>

```
if (BusinessEventsConfigurationReader::isBusinessEventEnabled(classStr(CollectionStatusUpdatedBusinessEvent)))
{
    while select dispute
    where dispute.Status == CustVendDisputeStatus::PromiseToPay
    && dispute.FollowUpDate _currentDate
    exists join custTrans
    where custTrans.RecId == dispute.CustTrans
    && !custTrans.Closed
    exists join _tmpCustAging
    where _tmpCustAging.AccountNum == custTrans.AccountNum
    {
        CollectionStatusUpdatedBusinessEvent::newFromCustDispute(dispute).send();
    }
}
```

## <a name="source-document-framework-support"></a><span data-ttu-id="9f945-224">ソース ドキュメント フレームワークのサポート</span><span class="sxs-lookup"><span data-stu-id="9f945-224">Source document framework support</span></span>

<span data-ttu-id="9f945-225">元伝票フレームワークは、ドキュメントのプロセス内状態から完了状態への移行の一部として、ビジネス イベントの自動送信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9f945-225">The source document framework supports sending business events automatically as part of the transition from an in-process state to a completed state for the document.</span></span> <span data-ttu-id="9f945-226">この機能を活用するには、元伝票フレームワークを拡張するドキュメントが **SourceDocumentStateInProcess.getBusinessEvent** メソッドの拡張機能を実装して、正確な **BusinessEventsBase** 拡張子タイプを作成して戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-226">To take advantage of this capability, documents that extend the source document framework must implement an extension of the **SourceDocumentStateInProcess.getBusinessEvent** method to create and return the correct **BusinessEventsBase** extension type.</span></span>

## <a name="extending-a-business-event-payload"></a><span data-ttu-id="9f945-227">ビジネス イベント ペイロードの拡張</span><span class="sxs-lookup"><span data-stu-id="9f945-227">Extending a business event payload</span></span>

<span data-ttu-id="9f945-228">ビジネス イベントのペイロードの一部として、追加情報を公開する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-228">You might want to publish additional information as part of the payload of a business event.</span></span> <span data-ttu-id="9f945-229">この追加情報を送信するには、ビジネス イベントの標準ペイロードを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-229">To send this additional information, you must extend the business event's standard payload.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="9f945-230">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="9f945-230">Example scenario</span></span>

<span data-ttu-id="9f945-231">この例では、**CustFreeTextInvoicePostedBusinessEventContract** を拡張して顧客の分類を含める方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9f945-231">This example shows how to extend the **CustFreeTextInvoicePostedBusinessEventContract** class so that it includes a customer classification.</span></span> <span data-ttu-id="9f945-232">この顧客分類は業界に基づくカスタム分類です。</span><span class="sxs-lookup"><span data-stu-id="9f945-232">This customer classification is an industry-based custom classification.</span></span>

#### <a name="step-1-create-an-extended-business-event-contract"></a><span data-ttu-id="9f945-233">ステップ 1: 拡張されたビジネス イベント契約の作成</span><span class="sxs-lookup"><span data-stu-id="9f945-233">Step 1: Create an extended business event contract</span></span>

<span data-ttu-id="9f945-234">標準的なビジネス イベント契約、およびペイロードに含める必要がある追加情報で構成される契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="9f945-234">Create a contract that consists of the standard business event contract plus any additional information that must be included in the payload.</span></span>

    ```
    [DataContract]
    public class CustFreeTextInvoicePostedBusinessEventExtendedContract
    extends BusinessEventsContract
    {
        // standard contract
        private CustFreeTextInvoicePostedBusinessEventContract
        custFreeTextInvoicePostedBusinessEventContract;
        // contract extensions
        private str customerClassification;
    }
    ```

#### <a name="step-2-create-an-initialize-method"></a><span data-ttu-id="9f945-235">ステップ 2: 初期化メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="9f945-235">Step 2: Create an initialize method</span></span>

<span data-ttu-id="9f945-236">プライベート契約の値を初期化する **初期化** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f945-236">Create an **initialize** method that initializes the value of the private contract.</span></span>

    ```
    private void initialize(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        custFreeTextInvoicePostedBusinessEventContract =
        _custFreeTextInvoicePostedBusinessEventContract;
    }
    ```

#### <a name="step-3-create-a-static-newfrom-method"></a><span data-ttu-id="9f945-237">ステップ 3: 静的 newFrom メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="9f945-237">Step 3: Create a static newFrom method</span></span>

<span data-ttu-id="9f945-238">標準契約を引数として取得し **初期化** メソッドを呼び出す、静的 **newFrom** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="9f945-238">Create a static **newFrom** method that takes the standard contract as an argument and calls the **initialize** method.</span></span>

    ```
    public static CustFreeTextInvoicePostedBusinessEventExtendedContract
    newFromCustFreeTextInvoicePostedBusinessEventContract(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        var contract = new CustFreeTextInvoicePostedBusinessEventExtendedContract();
        contract.initialize(_custFreeTextInvoicePostedBusinessEventContract);
        return contract;
    }
    ```

#### <a name="step-4-map-parm-methods"></a><span data-ttu-id="9f945-239">ステップ 4: parm メソッドのマッピング</span><span class="sxs-lookup"><span data-stu-id="9f945-239">Step 4: Map parm methods</span></span>

<span data-ttu-id="9f945-240">**parm** メソッドを標準データ コントラクトからコピーして、クラスの標準契約インスタンス内で値を取得およびセットするように各メソッドを修正します。</span><span class="sxs-lookup"><span data-stu-id="9f945-240">Copy the **parm** methods from the standard data contract, and modify each method so that it gets and sets values in the class's standard contract instance.</span></span>

```
[DataMember('InvoiceAccount')]
public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
= custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount())
{
    return
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount(_invoiceAccount);
}
[DataMember('InvoiceId')]
public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId =
custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId())
{
    return custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId(_invoiceId);
}
```

#### <a name="step-5-add-parms-methods-for-additional-payload-data"></a><span data-ttu-id="9f945-241">ステップ 5: 追加ペイロード データのために parm メソッドを追加する</span><span class="sxs-lookup"><span data-stu-id="9f945-241">Step 5: Add parms methods for additional payload data</span></span>

```
[DataMember('CustomerClassification')]
public CustomerClassification parmCustomerClassification(CustomerClassification
_customerClassification = customerClassification)
{
    customerClassification = _customerClassification;
    return customerClassification;
}
```

<span data-ttu-id="9f945-242">これは拡張ビジネス契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="9f945-242">Here is the complete implementation of the extended business contract.</span></span>

```
[DataContract]
public class CustFreeTextInvoicePostedBusinessEventExtendedContract
extends BusinessEventsContract
{
    // standard contract
    private CustFreeTextInvoicePostedBusinessEventContract
    custFreeTextInvoicePostedBusinessEventContract;
    // contract extensions
    private str customerClassification;
    public static CustFreeTextInvoicePostedBusinessEventExtendedContract
    newFromCustFreeTextInvoicePostedBusinessEventContract(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        var contract = new CustFreeTextInvoicePostedBusinessEventExtendedContract();
        contract.initialize(_custFreeTextInvoicePostedBusinessEventContract);
        return contract;
    }
    private void initialize(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        custFreeTextInvoicePostedBusinessEventContract =
        _custFreeTextInvoicePostedBusinessEventContract;
    }
    private void new()
    {
    }
    [DataMember('InvoiceAccount')]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount
    = custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAccount(_invoiceAccount);
    }
    [DataMember('InvoiceId')]
    public CustInvoiceId parmInvoiceId(CustInvoiceId _invoiceId =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId())
    {
        return custFreeTextInvoicePostedBusinessEventContract.parmInvoiceId(_invoiceId);
    }
    [DataMember('InvoiceDate')]
    public TransDate parmInvoiceDate(TransDate _invoiceDate =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDate())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDate(_invoiceDate);
    }
    [DataMember('InvoiceDueDate')]
    public DueDate parmInvoiceDueDate(DueDate _invoiceDueDate =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDueDate())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceDueDate(_invoiceDueDate);
    }
    [DataMember('InvoiceAmountInAccountingCurrency')]
    public AmountMST parmInvoiceAmount(AmountMST _invoiceAmount =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAmount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceAmount(_invoiceAmount);
    }
    [DataMember('InvoiceTaxAmount')]
    public TaxAmount parmInvoiceTaxAmount(TaxAmount _invoiceTaxAmount =
    custFreeTextInvoicePostedBusinessEventContract.parmInvoiceTaxAmount())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmInvoiceTaxAmount(_invoiceTaxAmount);
    }
    [DataMember('LegalEntity')]
    public LegalEntityDataAreaId parmLegalEntity(LegalEntityDataAreaId _legalEntity
    = custFreeTextInvoicePostedBusinessEventContract.parmLegalEntity())
    {
        return
        custFreeTextInvoicePostedBusinessEventContract.parmLegalEntity(_legalEntity);
    }
    // contract extensions
    [DataMember('CustomerClassification')]
    public CustomerClassification parmCustomerClassification(CustomerClassification
    _customerClassification = customerClassification)
    {
        customerClassification = _customerClassification;
        return customerClassification;
    }
}
```

#### <a name="step-6-wrap-the-buildcontract-method"></a><span data-ttu-id="9f945-243">ステップ 6: buildContract メソッドをラップします。</span><span class="sxs-lookup"><span data-stu-id="9f945-243">Step 6: Wrap the buildContract method</span></span>

<span data-ttu-id="9f945-244">標準ビジネス イベント契約をロードしてペイロード拡張機能を投入する **next** を呼び出す、ビルド契約の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-244">Provide a build contract implementation that calls **next** to load the standard business event contract and populates any payload extensions.</span></span> <span data-ttu-id="9f945-245">これは完全なクラスです。</span><span class="sxs-lookup"><span data-stu-id="9f945-245">Here is the complete class.</span></span>

```
[ExtensionOf(classStr(CustFreeTextInvoicePostedBusinessEvent))]
public final class FreeTextInvoicePostedBusinessEventContract_Extension
{
    public BusinessEventsContract buildContract()
    {
        var businessEventContract =
        CustFreeTextInvoicePostedBusinessEventExtendedContract::newFromCustFreeTextInvoicePostedBusinessEventContract(next
        buildContract());
        businessEventContract.parmCustomerClassification(CustomerClassifier::deriveCustomerClassification(businessEventContract.parmInvoiceAccount()));
        return businessEventContract;
    }
}
```

## <a name="extending-filters-to-have-custom-fields-if-supported-by-the-middleware"></a><span data-ttu-id="9f945-246">カスタム フィールドを持つようにフィルターを拡張する (ミドルウェアによってサポートされている場合)</span><span class="sxs-lookup"><span data-stu-id="9f945-246">Extending filters to have custom fields (if supported by the middleware)</span></span>

<span data-ttu-id="9f945-247">一部のミドルウェア システムはイベントのフィルター処理を許可します。</span><span class="sxs-lookup"><span data-stu-id="9f945-247">Some middleware systems allow for filtering of the events.</span></span> <span data-ttu-id="9f945-248">たとえば、Azure Service Bus にはキーと値のペアを設定できるプロパティ バッグがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-248">For example, Azure Service Bus has a property bag that can be populated with key-value pairs.</span></span> <span data-ttu-id="9f945-249">これらのキーと値のペアは、Azure Service Bus のキューやトピックからの読み込み時にイベントをフィルター処理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f945-249">These key-value pairs can be used for filtering events when reading from the Azure Service Bus Queue or Topic.</span></span> <span data-ttu-id="9f945-250">また、Azure イベント グリッドには件名、イベント タイプ、ID などのフィルター処理されたメッセージ プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-250">Additionally, Azure Event Grid has filterable message properties like Subject, Event Type, and ID.</span></span> <span data-ttu-id="9f945-251">さまざまなシステムに対してこれらの異なるプロパティをサポートするために、ビジネス イベント フレームワークは PayloadContext と呼ばれる概念を使用しており、さまざまなイベント システムによるフィルター処理に対してカスタム フィールドを含むように拡張できます。</span><span class="sxs-lookup"><span data-stu-id="9f945-251">To support these different properties for the different systems, the Business Events framework uses a concept called PayloadContext, which can be extended to include custom fields for filtering by the different eventing systems.</span></span>

### <a name="payload-context"></a><span data-ttu-id="9f945-252">ペイロード コンテキスト</span><span class="sxs-lookup"><span data-stu-id="9f945-252">Payload context</span></span>

<span data-ttu-id="9f945-253">ビジネス イベント フレームワークは *ペイロード コンテキスト* の概念をサポートしており、フレームワークによって送信されたメッセージをペイロードに関するコンテキストで修飾する手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f945-253">The Business Events framework supports a concept of *payload context*, which provides a means for decorating messages sent by the framework with context about the payload.</span></span> <span data-ttu-id="9f945-254">シナリオによっては、エンドポイントにメッセージを送信するときに追加のコンテキストが必要になることがあります。そのため、フレームワークにはコンテキストの上書きやアダプタのカスタマイズができるフックポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-254">In some scenarios, additional context may be required when sending messages to endpoints, so the framework has hookpoints where the context can be overwritten and the adapters can be customized.</span></span>

### <a name="adding-a-custom-payload-context"></a><span data-ttu-id="9f945-255">カスタム ペイロード コンテキストの追加</span><span class="sxs-lookup"><span data-stu-id="9f945-255">Adding a custom payload context</span></span>

<span data-ttu-id="9f945-256">カスタム ペイロード コンテキストは BusinessEventsCommitLogPayloadContext クラスから拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-256">A custom payload context must extend from the class BusinessEventsCommitLogPayloadContext.</span></span>

```
class CustomCommitLogPayloadContext extends
BusinessEventsCommitLogPayloadContext

{

private utcdatetime eventTime;

public utcdatetime parmEventTime(utcdatetime \_eventTime = eventTime)

{

eventTime = \_eventTime;

return eventTime;

}

}  
```

### <a name="constructing-the-custom-payload-context"></a><span data-ttu-id="9f945-257">カスタム ペイロード コンテキストの構築</span><span class="sxs-lookup"><span data-stu-id="9f945-257">Constructing the custom payload context</span></span>

<span data-ttu-id="9f945-258">新しいペイロード コンテキスト タイプを作成するには、BusinessEventsSender.buildPayloadContext メソッドに対してコマンド チェーン (CoC) 拡張機能を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-258">A Chain of Command (CoC) extension will need to be written for the BusinessEventsSender.buildPayloadContext method to construct the new payload context type.</span></span>

```
[ExtensionOf(classStr(BusinessEventsSender))]

public final class CustomPayloadContextBusinessEventsSender_Extension

{

protected BusinessEventsCommitLogPayloadContext
buildPayloadContext(BusinessEventsCommitLogEntry \_commitLogEntry)

{

BusinessEventsCommitLogPayloadContext payloadContext = next
buildPayloadContext(_commitLogEntry);

CustomCommitLogPayloadContext customPayloadContext = new
CustomCommitLogPayloadContext();

customPayloadContext.initFromBusinessEventsCommitLogEntry(_commitLogEntry);

customPayloadContext.parmEventTime(_commitLogEntry.parmEventTime());

return customPayloadContext;

}

}  
```

### <a name="consuming-the-custom-payload-context-from-an-adapter"></a><span data-ttu-id="9f945-259">アダプターからカスタム ペイロード コンテキストを使用する</span><span class="sxs-lookup"><span data-stu-id="9f945-259">Consuming the custom payload context from an adapter</span></span>

<span data-ttu-id="9f945-260">ペイロード コンテキストを使用するアダプターは、CoC メソッドを公開して新しいペイロード コンテキストを使用できるように記述されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-260">Adapters that consume payload context are written in such a way that they expose CoC methods to allow consuming new payload contexts.</span></span> <span data-ttu-id="9f945-261">次の例では、サービス バス アダプターの一般的なプロパティ バッグを持ち、サービス バスの消費者によってフィルター処理できるサービス バス アダプターの外観について説明します。</span><span class="sxs-lookup"><span data-stu-id="9f945-261">The following example explores what this looks like for the Service Bus adapter, which has a generic property bag that can be filtered on by the consumers of the Service Bus.</span></span>

<span data-ttu-id="9f945-262">BusinessEventsServiceBusAdapter には addProperties という CoC メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="9f945-262">The BusinessEventsServiceBusAdapter has the CoC method called addProperties.</span></span>

```
[ExtensionOf(classStr(BusinessEventsServiceBusAdapter))]

public final class CustomBusinessEventsServiceBusAdapter_Extension

{

protected void addProperties(BrokeredMessage \_message,
BusinessEventsEndpointPayloadContext \_context)

{

if (_context is CustomCommitLogPayloadContext)

{

CustomCommitLogPayloadContext customPayloadContext = \_context as
CustomCommitLogPayloadContext;

var propertyBag = \_message.Properties;

propertyBag.Add('EventId', customPayloadContext.parmEventId());

propertyBag.Add('BusinessEventId', customPayloadContext.parmBusinessEventId());

*// Convert the enum to string to be able to serialize the property.*

propertyBag.Add('BusinessEventCategory', enum2Symbol(enumNum(ModuleAxapta),
customPayloadContext.parmBusinessEventCategory()));

propertyBag.Add('LegalEntity', customPayloadContext.parmLegalEntity());

propertyBag.Add('EventTime', customPayloadContext.parmEventTime());

}

}

}  
```

## <a name="adding-a-custom-endpoint-type"></a><span data-ttu-id="9f945-263">カスタム エンドポイント タイプの追加</span><span class="sxs-lookup"><span data-stu-id="9f945-263">Adding a custom endpoint type</span></span>
<span data-ttu-id="9f945-264">ビジネス イベント フレームワークは出荷時のものに加え、新しいエンドポイント タイプの追加をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9f945-264">The Business Events framework supports adding new endpoint types in addition to the ones that ship out of the box.</span></span> <span data-ttu-id="9f945-265">この方法の例は以下の説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f945-265">An example of how to do this is describe with the below.</span></span>

### <a name="add-new-endpoint-type"></a><span data-ttu-id="9f945-266">新しいエンドポイント タイプの追加</span><span class="sxs-lookup"><span data-stu-id="9f945-266">Add new endpoint type</span></span>

<span data-ttu-id="9f945-267">各エンドポイント タイプは、列挙 BusinessEventsEndpointType によって表されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-267">Each endpoint type is represented by the enum BusinessEventsEndpointType.</span></span> <span data-ttu-id="9f945-268">新しいエンドポイントの追加は、次のセクションで示すように、この列挙を拡張して開始されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-268">Adding a new endpoint starts by extending this enum, as shown in the following section.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint1.png)

### <a name="add-new-endpoint-table-to-the-hierarchy"></a><span data-ttu-id="9f945-270">新しいエンドポイント テーブルを階層に追加します</span><span class="sxs-lookup"><span data-stu-id="9f945-270">Add new endpoint table to the hierarchy</span></span>

<span data-ttu-id="9f945-271">すべてのエンドポイント データが階層テーブルに保管され、そのルートは BusinessEventsEndpoint です。</span><span class="sxs-lookup"><span data-stu-id="9f945-271">All endpoint data is stored in a hierarchy table, the root of which is BusinessEventsEndpoint.</span></span> <span data-ttu-id="9f945-272">新しいエンドポイント テーブルは、サポート継承プロパティ = Yes、拡張プロパティ = “BusinessEventsEndpoint” (または BusinessEventsEndpoint 階層内の他の任意のエンドポイント) を設定して、このルート テーブルを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-272">A new endpoint table must extend this root table by setting the Support Inheritance property = Yes, and the Extends property = “BusinessEventsEndpoint” (or any other endpoint in the BusinessEventsEndpoint hierarchy).</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint2.png)

<span data-ttu-id="9f945-274">その後、新しいテーブルに、このエンドポイントとの初期化とコード内での通信に必要なカスタム フィールドの定義が保持されます。</span><span class="sxs-lookup"><span data-stu-id="9f945-274">The new table will then hold the definition of the custom fields needed to initialize and communicate with this endpoint in code.</span></span> <span data-ttu-id="9f945-275">競合の可能性を回避するには、フィールド名を属している特定のエンドポイントに対して限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-275">To avoid the possibility of conflict, field names should be qualified to the specific endpoint where they belong.</span></span> <span data-ttu-id="9f945-276">たとえば、2 つのエンドポイントは "URL" フィールドの概念を持つことができますが、それらを区別するために "CustomURL" のようなカスタム エンドポイントに固有の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-276">For example, two endpoints can have the concept of a “URL” field, but to distinguish them, their names should be specific to the custom endpoint like “CustomURL”.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint3.png)

### <a name="add-new-endpointadapter-class-that-implements-ibusinesseventsendpoint"></a><span data-ttu-id="9f945-278">IBusinessEventsEndpoint を実装する新しい EndpointAdapter クラスを追加します</span><span class="sxs-lookup"><span data-stu-id="9f945-278">Add new EndpointAdapter class that implements IBusinessEventsEndpoint</span></span>

<span data-ttu-id="9f945-279">新しいエンドポイント アダプター クラスでは IBusinessEventsEndpoint インターフェイスを実装し、BusinessEventsEndpointAttribute 属性で修飾する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-279">The new endpoint adapter class must implement the IBusinessEventsEndpoint interface as well as be decorated with the BusinessEventsEndpointAttribute attribute.</span></span>

```

[BusinessEventsEndpoint(BusinessEventsEndpointType::CustomEndpoint)]

public class CustomEndpointAdapter implements IBusinessEventsEndpoint

{  
```

<span data-ttu-id="9f945-280">初期化メソッドを実装して、渡された BusinessEventsEndpoint バッファーのタイプを確認し、次に示すように、この新しいアダプターに対して適切な型である場合は初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-280">The initialize method should be implemented to check the type of the BusinessEventsEndpoint buffer that is passed in, and initialize when it is of the correct type for this new adapter, as shown below.</span></span>

```

if (!(_endpoint is CustomBusinessEventsEndpoint))

{

BusinessEventsEndpointManager::logUnknownEndpointRecord(tableStr(CustomBusinessEventsEndpoint),
\_endpoint.RecId);

}

CustomBusinessEventsEndpoint customBusinessEventsEndpoint = \_endpoint as
CustomBusinessEventsEndpoint;

customField = customBusinessEventsEndpoint.CustomField;

if (!customField)

{

throw warning(strFmt("\@BusinessEvents:MissingAdapterConstructorParameter",
classStr(CustomEndpointAdapter), varStr(customField)));

}

```

### <a name="extend-the-endpointconfiguration-form"></a><span data-ttu-id="9f945-281">EndpointConfiguration フォームの拡張</span><span class="sxs-lookup"><span data-stu-id="9f945-281">Extend the EndpointConfiguration form</span></span>

<span data-ttu-id="9f945-282">カスタム フィールド入力を保持するには FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ の下に新しいグループ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9f945-282">Add a new group control under FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ to hold your custom field input.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint4.png)

<span data-ttu-id="9f945-284">カスタム フィールドの入力は、前の手順で作成された新しいテーブルとフィールドにバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9f945-284">The custom field input should be bound to the new table and field created in the previous step.</span></span> <span data-ttu-id="9f945-285">次に示すように、BusinessEventsEndpointConfiguration フォームの getConcreteType と showOtherFields メソッドを拡張するクラス拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="9f945-285">Create a class extension to extend the getConcreteType and showOtherFields methods of BusinessEventsEndpointConfiguration form, as shown below.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint5.png)

```

[ExtensionOf(formStr(BusinessEventsEndpointConfiguration))]

final public class CustomBusinessEventsEndpointConfiguration_Extension

{

public TableName getConcreteTableType(BusinessEventsEndpointType \_endpointType)

{

TableName tableName = next getConcreteTableType(_endpointType);

if (_endpointType == BusinessEventsEndpointType::CustomEndpoint)

{

tableName = tableStr(CustomBusinessEventsEndpoint);

}

return tableName;

}

public void showOtherFields()

{

next showOtherFields();

BusinessEventsEndpointType selection =
any2Enum(EndpointTypeSelection.selection());

if (selection == BusinessEventsEndpointType::CustomEndpoint)

{

this.control(this.controlId(formControlStr(BusinessEventsEndpointConfiguration,
CustomFields))).visible(true);

}

}

}

```
