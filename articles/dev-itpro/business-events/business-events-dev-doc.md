---
title: ビジネス イベント開発者ドキュメント
description: このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/21/2019
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
ms.openlocfilehash: b580541fe66b4a25088dfede4b947a82b0e3acc8
ms.sourcegitcommit: 2e727bb651cf4dfa65d624f45f0dcdc1e7e8287c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "719407"
---
# <a name="business-events-developer-documentation"></a><span data-ttu-id="5a130-103">ビジネス イベント開発者ドキュメント</span><span class="sxs-lookup"><span data-stu-id="5a130-103">Business events developer documentation</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="5a130-104">このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a130-104">This topic walks you through the development process and best practices for implementing business events.</span></span>

## <a name="what-is-a-business-event-and-what-is-not-a-business-event"></a><span data-ttu-id="5a130-105">何がビジネス イベントで、何がビジネス イベントではないか。</span><span class="sxs-lookup"><span data-stu-id="5a130-105">What is a business event and what is not a business event?</span></span>
<span data-ttu-id="5a130-106">ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。</span><span class="sxs-lookup"><span data-stu-id="5a130-106">This question comes up every time we start to think about use cases where business events can help.</span></span> <span data-ttu-id="5a130-107">仕入先の作成はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="5a130-107">Is creation of a vendor a business event?</span></span> <span data-ttu-id="5a130-108">または、発注書の確認はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="5a130-108">Or is confirming a purchase order a business event?</span></span> <span data-ttu-id="5a130-109">テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="5a130-109">Is it a business event if you capture the event at the table level?</span></span> <span data-ttu-id="5a130-110">または、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="5a130-110">Or should business events only be captured at the business logic level in a business process?</span></span> <span data-ttu-id="5a130-111">これらは有効な質問であるだけでなく、統合のソリューションを計画および構築するときに考察するキー トピックです。</span><span class="sxs-lookup"><span data-stu-id="5a130-111">These are not only valid questions, but also a key topic of discussion when planning and architecting a solution for integration.</span></span> <span data-ttu-id="5a130-112">次のガイドラインは、この思考過程および決定作業を支援するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-112">The following guidelines can be used to help with this thought process and decision making.</span></span>

<a name="intent"></a><span data-ttu-id="5a130-113">目的</span><span class="sxs-lookup"><span data-stu-id="5a130-113">Intent</span></span>
------

<span data-ttu-id="5a130-114">ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-114">The intent behind capturing the business event must be clearly understood.</span></span> <span data-ttu-id="5a130-115">つまり、ビジネス イベントをキャプチャする理由および受信者が使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="5a130-115">In other words, what is the reason for capturing the business event and how it is going to be used by the recipient.</span></span>

<span data-ttu-id="5a130-116">ビジネス イベントをキャプチャする目的が、Finance and Operations で発生したビジネス イベントに応答して Finance and Operations 外でビジネス アクションを実行することである場合は、これはビジネス イベントをキャプチャする有効な目的です。</span><span class="sxs-lookup"><span data-stu-id="5a130-116">If the intent for capturing a business event is to take a business action outside of Finance and Operations in response to the business event happening in Finance and Operations, then this is a valid intent to capture the business event.</span></span> <span data-ttu-id="5a130-117">ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文を作成するなどのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-117">The business action that is taken in response to the business event can be to notify users about the business event and/or to call into another business application to take a business action like, creating a sales order.</span></span> <span data-ttu-id="5a130-118">ビジネス アクションを、実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。</span><span class="sxs-lookup"><span data-stu-id="5a130-118">It is important to look at the business action generically and not base the need for a business event on the type of business action that will be taken.</span></span>

<span data-ttu-id="5a130-119">ビジネス イベントをキャプチャする目的がデータを他の受信者に転送して、事実上データ エクスポート シナリオを実現することである場合、これはビジネス イベントを使用するための良いユース ケースではありません。</span><span class="sxs-lookup"><span data-stu-id="5a130-119">If the intent of capturing the business event is to transfer data to the recipient and in effect, realizing a data export scenario, then this will not be a good use case for using business events.</span></span> <span data-ttu-id="5a130-120">実際、データ転送ユース ケースのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用となります。</span><span class="sxs-lookup"><span data-stu-id="5a130-120">In fact, the use of business events for data transfer use cases will be a misuse of the business events framework.</span></span>
<span data-ttu-id="5a130-121">このようなシナリオでは、データ管理で既に使用可能なデータ エクスポート メカニズムを使用し続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-121">Such scenarios must continue to use data export mechanisms already available in data management.</span></span>

<a name="fidelity"></a><span data-ttu-id="5a130-122">忠実性</span><span class="sxs-lookup"><span data-stu-id="5a130-122">Fidelity</span></span>
--------

<span data-ttu-id="5a130-123">目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために必要なアプローチを評価することです。</span><span class="sxs-lookup"><span data-stu-id="5a130-123">When the intent is clear and a legitimate need for a business event is established, the next step is to evaluate the approach that must be taken to capture the business event.</span></span> <span data-ttu-id="5a130-124">次のセクションでは、評価する必要があるアプローチを要約します。</span><span class="sxs-lookup"><span data-stu-id="5a130-124">The following section summarizes the approach that must be evaluated.</span></span>

<span data-ttu-id="5a130-125">どのアプローチを採用するかに関わらず、ビジネス イベントの忠実性のためには以下の点を考慮することが重要で、結果として、ビジネス イベントを実装するためのデザイン選択に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="5a130-125">Regardless of which approach is taken, the fidelity of business events is significant to ensure the following aspects are taken care of and as a result, must influence the design choice for implementing the business event.</span></span> <span data-ttu-id="5a130-126">ただし、ビジネス イベントを実装するためのデザイン選択がビジネス イベントのコンセプトには影響を与えないようにします。選択されたデザインは、それがビジネス イベントであるか決定するための決定ツールとして使用すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="5a130-126">However, the design choice that you take to implement a business event must not influence the concept of business events--the chosen design must not be used as a decision-making tool to determine if it is a business event.</span></span> <span data-ttu-id="5a130-127">このような決定には、事前に考慮された目的を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-127">The intent discussed previously must be used for such decisions.</span></span>

-   <span data-ttu-id="5a130-128">**堅牢なビジネス イベント** - 間違ったビジネス イベントを受信者に送信するべきではありません。</span><span class="sxs-lookup"><span data-stu-id="5a130-128">**Durable business events** - There should be no false business events sent to the recipient.</span></span> <span data-ttu-id="5a130-129">発注書確認ビジネス イベントが送信済みの場合、受取人はその発注書が確認済みであることを信用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-129">If a purchase order confirmation business event was sent out, then the recipient must trust that the purchase order was indeed confirmed.</span></span> <span data-ttu-id="5a130-130">デザイン選択はこの取引の性質を保証する必要があり、この予想に反するデザイン選択を採用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="5a130-130">The design choice must ensure this transactional nature and hence must not take a design choice that would violate this expectation.</span></span>

-   <span data-ttu-id="5a130-131">**目標** - ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-131">**Targeted** - Business events must be designed to optimize the consumption story for the recipient.</span></span> <span data-ttu-id="5a130-132">つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にします。</span><span class="sxs-lookup"><span data-stu-id="5a130-132">In other words, make it as easy as possible for the recipient to consume business events.</span></span> <span data-ttu-id="5a130-133">このため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-133">Hence, business events must be as specific as possible and targeted to a specific use case.</span></span> <span data-ttu-id="5a130-134">そのためビジネス イベントは一般的なものではなく、コンシューマーがペイロードを理解するよう試みてビジネス イベントが何であったか判断させるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="5a130-134">Business events must not be generic thereby, leaving the consumer to determine what the business event was for by trying to understand the payload.</span></span> <span data-ttu-id="5a130-135">実行されたデザイン選択は、これが順守されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-135">The design choice made must allow for this to be preserved.</span></span>

-   <span data-ttu-id="5a130-136">**ノイズレス** - デザイン内でノイズを除外するための努力が最小になるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-136">**Noiseless** - There should be very little effort in the design to filter out the noise.</span></span> <span data-ttu-id="5a130-137">ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルタ ロジックの記述を避けます。</span><span class="sxs-lookup"><span data-stu-id="5a130-137">To make business events very specific, avoid writing filtering logic to filter out conditions that do not match the expected business event.</span></span> <span data-ttu-id="5a130-138">選択したアプローチは、ビジネス イベントがコードで実装されるポイントが、ノイズのフィルター処理が必要ないほど明確である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-138">The chosen approach must be such that the point at which the business event is implemented in code is specific enough to avoid the need for any filtering of noise.</span></span> <span data-ttu-id="5a130-139">ロジックの追加によってノイズをフィルター処理する試みはパフォーマンスの負荷になるだけでなく、特定のユース ケースに基づき複雑になる機能性があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-139">Any attempt to filter the noise by adding logic can not only be taxing on performance but, it may also get complicated based on specific use cases.</span></span>

| <span data-ttu-id="5a130-140">**ビジネス ロジック レベルでのキャプチャ**</span><span class="sxs-lookup"><span data-stu-id="5a130-140">**Capturing at business logic level**</span></span>                                                                                    | <span data-ttu-id="5a130-141">**テーブル レベルでのキャプチャ**</span><span class="sxs-lookup"><span data-stu-id="5a130-141">**Capturing at table level**</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a130-142">トランザクション内に置いて堅牢性を確保する</span><span class="sxs-lookup"><span data-stu-id="5a130-142">Ensures durability by being in the transaction</span></span>                                                                           | <span data-ttu-id="5a130-143">トランザクション内に置いて堅牢性を確保します。</span><span class="sxs-lookup"><span data-stu-id="5a130-143">Ensures durability by being in the transaction.</span></span>                                                                      |
| <span data-ttu-id="5a130-144">対象となるビジネス イベントを許可します。</span><span class="sxs-lookup"><span data-stu-id="5a130-144">Allows for targeted business events.</span></span>                                                                                     | <span data-ttu-id="5a130-145">イベントのキャプチャが低レベルであるため対象となるビジネス イベントを有効にすることが困難です。</span><span class="sxs-lookup"><span data-stu-id="5a130-145">Difficult to enable targeted business events due to the lower level capturing of events.</span></span>                             |
| <span data-ttu-id="5a130-146">簡単にノイズレスのままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-146">Makes it easy to remain noiseless.</span></span>                                                                                       | <span data-ttu-id="5a130-147">ノイズを除去するためのサウンド ロジックを導入する追加作業が行われるまで、ノイズレスのままにすることは困難です。</span><span class="sxs-lookup"><span data-stu-id="5a130-147">Difficult to remain noiseless unless additional effort is taken to put sound logic in place to filter out the noise.</span></span> |
| <span data-ttu-id="5a130-148">堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-148">Provides additional context of the business process, which can significantly improve the durability and the quality of payload.</span></span> | <span data-ttu-id="5a130-149">イベントのキャプチャが低レベルであると、ビジネス プロセスのコンテキストが失われる可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="5a130-149">Business process context is most likely lost due to the lower level capturing of events.</span></span>                             |


## <a name="implementing-a-business-event"></a><span data-ttu-id="5a130-150">ビジネス イベントの実装</span><span class="sxs-lookup"><span data-stu-id="5a130-150">Implementing a business event</span></span>

<span data-ttu-id="5a130-151">ビジネス イベントを実装して送信することは非常に簡単なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="5a130-151">Implementing a business event and sending it is a fairly straightforward process:</span></span>
1. <span data-ttu-id="5a130-152">契約を構築します。</span><span class="sxs-lookup"><span data-stu-id="5a130-152">Build the contract.</span></span>
2. <span data-ttu-id="5a130-153">イベントを構築します。</span><span class="sxs-lookup"><span data-stu-id="5a130-153">Build the event.</span></span>
3. <span data-ttu-id="5a130-154">イベントを送信するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5a130-154">Add code to send the event.</span></span> 

<span data-ttu-id="5a130-155">以下の 2 つのクラスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-155">Two classes must be implemented:</span></span>

- <span data-ttu-id="5a130-156">**ビジネス イベント** - このクラスは **BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a130-156">**Business event** – This class extends the **BusinessEventsBase** class.</span></span> <span data-ttu-id="5a130-157">ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-157">It provides support for constructing the business event, building the payload, and sending the business event.</span></span>
- <span data-ttu-id="5a130-158">**ビジネス イベント契約** - このクラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a130-158">**Business event contract** – This class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="5a130-159">ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="5a130-159">It defines the payload of the business event and allows for population of the contract at runtime.</span></span> 

### <a name="businesseventsbase-extension"></a><span data-ttu-id="5a130-160">BusinessEventsBase 拡張機能</span><span class="sxs-lookup"><span data-stu-id="5a130-160">BusinessEventsBase extension</span></span>

#### <a name="naming-convention"></a><span data-ttu-id="5a130-161">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="5a130-161">Naming convention</span></span>

<span data-ttu-id="5a130-162">ビジネス イベントの名前は以下のパターンに従う必要があります: <名詞/名詞句><past tense action>BusinessEvent</span><span class="sxs-lookup"><span data-stu-id="5a130-162">The names of business events should follow this pattern: <noun/noun phrase><past tense action>BusinessEvent</span></span>

<span data-ttu-id="5a130-163">**例**</span><span class="sxs-lookup"><span data-stu-id="5a130-163">**Examples**</span></span>

- <span data-ttu-id="5a130-164">VendorInvoicePostedBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="5a130-164">VendorInvoicePostedBusinessEvent</span></span>
- <span data-ttu-id="5a130-165">CollectionLetterSentBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="5a130-165">CollectionLetterSentBusinessEvent</span></span>

<span data-ttu-id="5a130-166">名前の <名詞/名詞句> パートは、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-166">The <noun/noun phrase> part of the name should comply with existing definitions for application area prefixes.</span></span>

#### <a name="implementation"></a><span data-ttu-id="5a130-167">実装</span><span class="sxs-lookup"><span data-stu-id="5a130-167">Implementation</span></span>

<span data-ttu-id="5a130-168">**BusinessEventsBase** 拡張機能を実装するプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="5a130-168">The process of implementing a **BusinessEventsBase** extension is straightforward.</span></span> <span data-ttu-id="5a130-169">**BusinessEventsBase** クラスの拡張、および静的コンストラクター メソッドの実装、プライベート **新規** メソッド、内部状態を保持するメソッド、および **buildContract** メソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a130-169">It involves extending the **BusinessEventsBase** class, and implementing a static constructor method, a private **new** method, methods to maintain internal state, and the **buildContract** method.</span></span>

1. <span data-ttu-id="5a130-170">**BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a130-170">Extend the **BusinessEventsBase** class.</span></span>

    ```
    [BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
    "AccountsReceivable:SalesOrderInvoicePostedBusinessEventName","AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription",ModuleAxapta::SalesOrder)]
    public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
    ```

    <span data-ttu-id="5a130-171">**BusinessEvents** 属性に注意してください。</span><span class="sxs-lookup"><span data-stu-id="5a130-171">Note the **BusinessEvents** attribute.</span></span> <span data-ttu-id="5a130-172">この属性は、ビジネス イベントの契約、名前、説明、および含まれるモジュールに関する情報を含む、ビジネス イベント フレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-172">This attribute provides the business events framework with information about the business event's contract, name, and description, and also the module that it's part of.</span></span> <span data-ttu-id="5a130-173">ラベルは、名前と説明の引数に定義する必要がありますが、ローカライズされたデータの保存を避けるため、「@」記号なしで参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-173">Labels must be defined for the name and description arguments, but should be referenced without the '@' symbol to avoid storing localized data.</span></span>

2. <span data-ttu-id="5a130-174">静的 **newFrom<my_buffer>** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-174">Implement a static **newFrom<my_buffer>** method.</span></span> <span data-ttu-id="5a130-175">メソッド名の <my_buffer> パートは通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。</span><span class="sxs-lookup"><span data-stu-id="5a130-175">The <my_buffer> part of the method name is typically the table buffer that is used to initialize the business event contract.</span></span>

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

3. <span data-ttu-id="5a130-176">プライベート **新規** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-176">Implement a private **new** method.</span></span> <span data-ttu-id="5a130-177">このメソッドは静的コンストラクター メソッドからのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5a130-177">This method is called only from the static constructor method.</span></span>

    ```
    private void new()
    {
    }
    ```

4. <span data-ttu-id="5a130-178">内部状態を維持するプライベート **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-178">Implement private **parm** methods to maintain internal state.</span></span>

    ```
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour = custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    ```

5. <span data-ttu-id="5a130-179">**buildContract** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-179">Implement the **buildContract** method.</span></span> <span data-ttu-id="5a130-180">このステップには EventContract スタブが必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5a130-180">Note that you'll need an EventContract stub for this step.</span></span>

    ```
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return
        SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
    ```

    <span data-ttu-id="5a130-181">拡張機能のために、**buildContract** メソッドは **Wrappable(true)** および **Replaceable(true)** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-181">For extensibility, the **buildContract** method must be attributed with the **Wrappable(true)** and **Replaceable(true)** attributes.</span></span> <span data-ttu-id="5a130-182">**buildContract** メソッドは会社のためにビジネス イベントが有効にされるときにのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5a130-182">The **buildContract** method will be called only when a business event is enabled for a company.</span></span>

<span data-ttu-id="5a130-183">これは、「転記された販売注文請求書」ビジネス イベントの完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="5a130-183">Here is the complete implementation of the "Sales order invoice posted" business event.</span></span>

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

### <a name="businesseventscontract-extension"></a><span data-ttu-id="5a130-184">BusinessEventsContract 拡張機能</span><span class="sxs-lookup"><span data-stu-id="5a130-184">BusinessEventsContract extension</span></span>

<span data-ttu-id="5a130-185">ビジネス イベント契約クラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a130-185">A business event contract class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="5a130-186">ビジネス イベントのペイロードを定義および入力します。</span><span class="sxs-lookup"><span data-stu-id="5a130-186">It defines and populates the payload of the business event.</span></span> <span data-ttu-id="5a130-187">ビジネス イベントには一部の変動がありますが、ビジネス イベント契約の基本構造は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="5a130-187">Although there is some variation across business events, the basic structure of the business event contract is consistent.</span></span>

<span data-ttu-id="5a130-188">ビジネス イベント契約の実装プロセスには、**BusinessEventContract** クラスの拡張、内部状態の定義、初期化メソッドの実装、静的コンストラクター メソッドの実装、および契約状態にアクセスするための **parm** メソッドの実装が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a130-188">The process of implementing a business event contract involves extending the **BusinessEventContract** class, defining internal state, implementing an initialization method, implementing a static constructor method, and implementing **parm** methods to access the contract state.</span></span>

1. <span data-ttu-id="5a130-189">**BusinessEventContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5a130-189">Extend the **BusinessEventContract** class.</span></span>

    ```
    [DataContract]
    public final class SalesInvoicePostedBusinessEventContract extends
    BusinessEventsContract
    ```

    <span data-ttu-id="5a130-190">クラスは **DataContract** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-190">The class must be attributed with the **DataContract** attribute.</span></span>

2. <span data-ttu-id="5a130-191">契約状態を保持するプライベート変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="5a130-191">Add private variables to hold the contract state.</span></span>

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

3. <span data-ttu-id="5a130-192">プライベート初期化メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-192">Implement a private initialization method.</span></span>

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

    <span data-ttu-id="5a130-193">**初期化** メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="5a130-193">The **initialize** method is responsible for setting the business event contract class's private state, based on data that is provided through the static constructor method.</span></span>

4. <span data-ttu-id="5a130-194">静的コンストラクター メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-194">Implement a static constructor method.</span></span>

    ```
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    ```

    <span data-ttu-id="5a130-195">静的コンストラクター メソッドはプライベート **初期化** メソッドを呼び出して、プライベート クラス状態を初期化します。</span><span class="sxs-lookup"><span data-stu-id="5a130-195">The static constructor method calls a private **initialize** method to initialize the private class state.</span></span>

5. <span data-ttu-id="5a130-196">契約状態にアクセスするための **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5a130-196">Implement **parm** methods to access the contract state.</span></span>

    ```
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    ```

    <span data-ttu-id="5a130-197">**parm** メソッドは **DataMember('<name>')** および **BusinessEventsDataMember('<description>')** 属性に帰属する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-197">The **parm** methods should be attributed with the **DataMember('<name>')** and **BusinessEventsDataMember('<description>')** attributes.</span></span> <span data-ttu-id="5a130-198">属性で提供する名前 (たとえば、 **'InvoiceAccount'**) はデータ契約消費者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a130-198">The name that you provide on the attribute (for example **'InvoiceAccount'**) will be visible to data contract consumers.</span></span> <span data-ttu-id="5a130-199">BusinessEventsDataMember で指定された説明は、この契約のデータ メンバーを記述するときにビジネス イベント カタログ UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5a130-199">The description provided in the BusinessEventsDataMember will be visible in the Business Events catalog UI when describing this contract's data members.</span></span>

> [!NOTE]
> - <span data-ttu-id="5a130-200">**RecId** 値はビジネス イベント ペイロードの一部にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5a130-200">**RecId** values should not be part of a business event payload.</span></span> <span data-ttu-id="5a130-201">代わりに代替キー (AK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="5a130-201">Use the alternate key (AK) instead.</span></span>
> - <span data-ttu-id="5a130-202">列挙型 (enum) 値は、公開する前にそのシンボル値に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-202">Enumeration (enum) values must be converted to their symbol value before they can be published.</span></span> <span data-ttu-id="5a130-203">**enum2Symbol** メソッドを使用して列挙型の値をシンボル文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="5a130-203">Use the **enum2Symbol** method to convert an enum's value to the symbol string.</span></span> <span data-ttu-id="5a130-204">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5a130-204">Here is an example:</span></span>
>
>    ```
>    status = enum2Symbol(enumNum(CustVendDisputeStatus), _custDispute.Status);
>    ```

<span data-ttu-id="5a130-205">場合によっては、データ契約の内部状態の投入のために、追加の取得メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-205">In some cases, population of the data contract's internal state will require that you implement additional retrieval methods.</span></span> <span data-ttu-id="5a130-206">これらの取得メソッドはプライベート メソッドとして実装し、**初期化** メソッドから呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-206">These retrieval methods should be implemented as private methods, and they should be called from the **initialize** method.</span></span>

<span data-ttu-id="5a130-207">これは、「転記された販売注文請求書」ビジネス イベント契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="5a130-207">Here is the complete implementation of the "Sales order invoice posted" business event contract.</span></span>

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

## <a name="sending-a-business-event"></a><span data-ttu-id="5a130-208">ビジネス イベントの送信</span><span class="sxs-lookup"><span data-stu-id="5a130-208">Sending a business event</span></span>

<span data-ttu-id="5a130-209">適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-209">You must modify application code so that it sends the business event at the appropriate point.</span></span> <span data-ttu-id="5a130-210">多くの場合、フレームワーク内の共通ポイントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-210">Often, you can use a common point within a framework.</span></span> <span data-ttu-id="5a130-211">**SourceDocument** を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="5a130-211">Documents that extend **SourceDocument** have a common point for creating and sending a business event.</span></span> <span data-ttu-id="5a130-212">詳細については、以下をサポートする元伝票フレームワークのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a130-212">For more information, see the section on source document framework support below.</span></span>

<span data-ttu-id="5a130-213">また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-213">Other frameworks also provide common points for sending business events.</span></span> <span data-ttu-id="5a130-214">たとえば、AOT 内の **CustVendVoucher** クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、**転記** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="5a130-214">For example, the **CustVendVoucher** class hierarchy in AOT has a **post** method that is used to send business events that are related to posting customer or vendor vouchers.</span></span> <span data-ttu-id="5a130-215">基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-215">Overrides of the base class implementation provide specialization of the logic for sending business events.</span></span> <span data-ttu-id="5a130-216">例については、AOT の **CustVoucher.createBusinessEvent** または **VendVoucher.createBusinessEvent** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a130-216">For an example, see **CustVoucher.createBusinessEvent** or **VendVoucher.createBusinessEvent** in AOT.</span></span>

<span data-ttu-id="5a130-217">ビジネス イベントの送信は、基になる取引のコミットにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="5a130-217">The sending of a business event is linked to the commit of the underlying transaction.</span></span> <span data-ttu-id="5a130-218">基になる取引が中止される場合、ビジネス イベントは送信されません。</span><span class="sxs-lookup"><span data-stu-id="5a130-218">If the underlying transaction is aborted, the business event won't be sent.</span></span> <span data-ttu-id="5a130-219">そのため、アプリケーションはペイロード情報が使用可能なポイントでビジネス イベントを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-219">Therefore, applications can send the business event at the point where the payload information is available.</span></span>

<span data-ttu-id="5a130-220">ビジネス イベント フレームワークは、ビジネス イベントが消費者に公開されるかどうか決定します。</span><span class="sxs-lookup"><span data-stu-id="5a130-220">The business events framework determines whether a business event is published to a consumer.</span></span> <span data-ttu-id="5a130-221">一般的なルールとして、ビジネス イベントが有効かどうかに関わらず、アプリケーションはビジネス イベントを常に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-221">As a general rule, applications should always send a business event, regardless of whether the business event is enabled.</span></span> <span data-ttu-id="5a130-222">重要な追加ロジックが必要な場合、またはビジネス イベントを送信するためのロジックがパフォーマンスに影響する場合は、ビジネス イベントの送信に関連付けられたビジネス ロジックを実行する前に、アプリケーションは特定のビジネス イベントが有効化されているかどうか確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-222">If significant additional logic is required, or if the logic for sending a business event has a performance impact, an application can check whether a specific business event is enabled before it runs business logic that is associated with sending business events.</span></span> <span data-ttu-id="5a130-223">この確認は **BusinessEventsConfigurationReader::isBusinessEventEnabled** メソッドを介して実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a130-223">This check is done through the **BusinessEventsConfigurationReader::isBusinessEventEnabled** method.</span></span>

```
if (BusinessEventsConfigurationReader::isBusinessEventEnabled(new
CollectionStatusUpdatedBusinessEvent()))
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

## <a name="source-document-framework-support"></a><span data-ttu-id="5a130-224">ソース ドキュメント フレームワークのサポート</span><span class="sxs-lookup"><span data-stu-id="5a130-224">Source document framework support</span></span>

<span data-ttu-id="5a130-225">元伝票フレームワークは、ドキュメントのプロセス内状態から完了状態への移行の一部として、ビジネス イベントの自動送信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5a130-225">The source document framework supports sending business events automatically as part of the transition from an in-process state to a completed state for the document.</span></span> <span data-ttu-id="5a130-226">この機能を活用するには、元伝票フレームワークを拡張するドキュメントが **SourceDocumentStateInProcess.getBusinessEvent** メソッドの拡張機能を実装して、正確な **BusinessEventsBase** 拡張子タイプを作成して戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-226">To take advantage of this capability, documents that extend the source document framework must implement an extension of the **SourceDocumentStateInProcess.getBusinessEvent** method to create and return the correct **BusinessEventsBase** extension type.</span></span>

## <a name="extending-a-business-event-payload"></a><span data-ttu-id="5a130-227">ビジネス イベント ペイロードの拡張</span><span class="sxs-lookup"><span data-stu-id="5a130-227">Extending a business event payload</span></span>

<span data-ttu-id="5a130-228">ビジネス イベントのペイロードの一部として、追加情報を公開する場合があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-228">You might want to publish additional information as part of the payload of a business event.</span></span> <span data-ttu-id="5a130-229">この追加情報を送信するには、ビジネス イベントの標準ペイロードを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a130-229">To send this additional information, you must extend the business event's standard payload.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="5a130-230">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="5a130-230">Example scenario</span></span>

<span data-ttu-id="5a130-231">この例では、**CustFreeTextInvoicePostedBusinessEventContract** を拡張して顧客の分類を含める方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5a130-231">This example shows how to extend the **CustFreeTextInvoicePostedBusinessEventContract** class so that it includes a customer classification.</span></span> <span data-ttu-id="5a130-232">この顧客分類は業界に基づくカスタム分類です。</span><span class="sxs-lookup"><span data-stu-id="5a130-232">This customer classification is an industry-based custom classification.</span></span>

#### <a name="step-1-create-an-extended-business-event-contract"></a><span data-ttu-id="5a130-233">ステップ 1: 拡張されたビジネス イベント契約の作成</span><span class="sxs-lookup"><span data-stu-id="5a130-233">Step 1: Create an extended business event contract</span></span>

<span data-ttu-id="5a130-234">標準的なビジネス イベント契約、およびペイロードに含める必要がある追加情報で構成される契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="5a130-234">Create a contract that consists of the standard business event contract plus any additional information that must be included in the payload.</span></span>

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

#### <a name="step-2-create-an-initialize-method"></a><span data-ttu-id="5a130-235">ステップ 2: 初期化メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="5a130-235">Step 2: Create an initialize method</span></span>

<span data-ttu-id="5a130-236">プライベート契約の値を初期化する **初期化** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a130-236">Create an **initialize** method that initializes the value of the private contract.</span></span>

    ```
    private void initialize(CustFreeTextInvoicePostedBusinessEventContract
    _custFreeTextInvoicePostedBusinessEventContract)
    {
        custFreeTextInvoicePostedBusinessEventContract =
        _custFreeTextInvoicePostedBusinessEventContract;
    }
    ```

#### <a name="step-3-create-a-static-newfrom-method"></a><span data-ttu-id="5a130-237">ステップ 3: 静的 newFrom メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="5a130-237">Step 3: Create a static newFrom method</span></span>

<span data-ttu-id="5a130-238">標準契約を引数として取得し **初期化** メソッドを呼び出す、静的 **newFrom** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="5a130-238">Create a static **newFrom** method that takes the standard contract as an argument and calls the **initialize** method.</span></span>

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

#### <a name="step-4-map-parm-methods"></a><span data-ttu-id="5a130-239">ステップ 4: parm メソッドのマッピング</span><span class="sxs-lookup"><span data-stu-id="5a130-239">Step 4: Map parm methods</span></span>

<span data-ttu-id="5a130-240">**parm** メソッドを標準データ コントラクトからコピーして、クラスの標準契約インスタンス内で値を取得およびセットするように各メソッドを修正します。</span><span class="sxs-lookup"><span data-stu-id="5a130-240">Copy the **parm** methods from the standard data contract, and modify each method so that it gets and sets values in the class's standard contract instance.</span></span>

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

#### <a name="step-5-add-parms-methods-for-additional-payload-data"></a><span data-ttu-id="5a130-241">ステップ 5: 追加ペイロード データのために parm メソッドを追加する</span><span class="sxs-lookup"><span data-stu-id="5a130-241">Step 5: Add parms methods for additional payload data</span></span>

```
[DataMember('CustomerClassification')]
public CustomerClassification parmCustomerClassification(CustomerClassification
_customerClassification = customerClassification)
{
    customerClassification = _customerClassification;
    return customerClassification;
}
```

<span data-ttu-id="5a130-242">これは拡張ビジネス契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="5a130-242">Here is the complete implementation of the extended business contract.</span></span>

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

#### <a name="step-6-wrap-the-buildcontract-method"></a><span data-ttu-id="5a130-243">ステップ 6: buildContract メソッドをラップします。</span><span class="sxs-lookup"><span data-stu-id="5a130-243">Step 6: Wrap the buildContract method</span></span>

<span data-ttu-id="5a130-244">標準ビジネス イベント契約をロードしてペイロード拡張機能を投入する **next** を呼び出す、ビルド契約の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="5a130-244">Provide a build contract implementation that calls **next** to load the standard business event contract and populates any payload extensions.</span></span> <span data-ttu-id="5a130-245">これは完全なクラスです。</span><span class="sxs-lookup"><span data-stu-id="5a130-245">Here is the complete class.</span></span>

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

## <a name="summary"></a><span data-ttu-id="5a130-246">集計</span><span class="sxs-lookup"><span data-stu-id="5a130-246">Summary</span></span>

<span data-ttu-id="5a130-247">標準ビジネス イベント契約を補うビジネス イベント契約を実装し、 **buildContract** メソッドの実装をラップするためにコマンド チェーン (CoC) を使用する拡張クラスを実装することにより、ビジネス イベントのペイロードを容易に拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="5a130-247">You can easily extend the payload of a business event by implementing a business event contract that supplements the standard business event contract, and an extension class that uses Chain of Command (CoC) to wrap the implementation of the **buildContract** method.</span></span>
