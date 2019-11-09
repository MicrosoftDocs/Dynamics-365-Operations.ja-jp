---
title: ビジネス イベント開発者ドキュメント
description: このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 09/19/2019
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
ms.openlocfilehash: 6a405b2182f288de1cb79c92d5ab4b3365e6783c
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578254"
---
# <a name="business-events-developer-documentation"></a><span data-ttu-id="d2ca9-103">ビジネス イベント開発者ドキュメント</span><span class="sxs-lookup"><span data-stu-id="d2ca9-103">Business events developer documentation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d2ca9-104">このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-104">This topic walks you through the development process and best practices for implementing business events.</span></span>

## <a name="what-is-a-business-event-and-what-isnt-a-business-event"></a><span data-ttu-id="d2ca9-105">何がビジネス イベントで、何がビジネス イベントではないか。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-105">What is a business event, and what isn't a business event?</span></span>

<span data-ttu-id="d2ca9-106">ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-106">This question comes up every time that we start to think about use cases where business events can help.</span></span> <span data-ttu-id="d2ca9-107">仕入先の作成はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-107">Is the creation of a vendor a business event?</span></span> <span data-ttu-id="d2ca9-108">発注書の確認はビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-108">Is confirmation of a purchase order a business event?</span></span> <span data-ttu-id="d2ca9-109">テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-109">Is it a business event if you capture the event at the table level?</span></span> <span data-ttu-id="d2ca9-110">また、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-110">Or should business events be captured only at the business logic level in a business process?</span></span> <span data-ttu-id="d2ca9-111">これらの質問は無効であるだけでなく、統合のソリューションを計画および構築する時に考察するキー トピックです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-111">These questions aren't just valid, but they are also a key topic of discussion when a solution is planned and architected for integration.</span></span> <span data-ttu-id="d2ca9-112">次のガイドラインは、この思考過程および決定作業を支援するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-112">The following guidelines can help with this thought process and decision making.</span></span>

## <a name="intent"></a><span data-ttu-id="d2ca9-113">目的</span><span class="sxs-lookup"><span data-stu-id="d2ca9-113">Intent</span></span>

<span data-ttu-id="d2ca9-114">ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-114">The intent behind capturing a business event must be clearly understood.</span></span> <span data-ttu-id="d2ca9-115">つまり、ビジネス イベントをキャプチャする理由、および受信者が使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-115">In other words, what is the reason for capturing the business event, and how it will be used by the recipient?</span></span>

<span data-ttu-id="d2ca9-116">ビジネス イベントをキャプチャして、Finance and Operation で発生するビジネス イベントに応じて Dynamics 365 Finance and Operations アプリの外部でビジネス アクションを実行することを目的としている場合、ビジネスイベントの良いユース ケースがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-116">If your intent is to capture a business event so that you can take a business action outside Dynamics 365 Finance and Operations apps in response to a business event that occurs in Finance and Operations, you have a good use case for business events.</span></span> <span data-ttu-id="d2ca9-117">ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文の作成などのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-117">The business action that is taken in response to the business event can be to notify users about the business event and/or to call into another business application to take a business action, such as creation of a sales order.</span></span> <span data-ttu-id="d2ca9-118">ビジネス アクションを実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-118">It's important that you look at the business action generically and not base the need for a business event on the type of business action that will be taken.</span></span>

<span data-ttu-id="d2ca9-119">データを受信者に転送し、効果的にデータ エクスポート シナリオを実現することを目的としている場合、ビジネス イベントに対する良いユースケースはありません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-119">If your intent is to transfer data to a recipient and, in effect, realize a data export scenario, you don't have a good use case for business events.</span></span> <span data-ttu-id="d2ca9-120">実際、データ転送シナリオのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用になります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-120">In fact, the use of business events for data transfer scenarios is a misuse of the business events framework.</span></span> <span data-ttu-id="d2ca9-121">このようなシナリオでは、データ管理で既に使用可能であるデータ エクスポート メカニズムを使用し続ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-121">Such scenarios must continue to use data export mechanisms that are already available in data management.</span></span>

## <a name="fidelity"></a><span data-ttu-id="d2ca9-122">忠実性</span><span class="sxs-lookup"><span data-stu-id="d2ca9-122">Fidelity</span></span>

<span data-ttu-id="d2ca9-123">目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために使用する必要のあるアプローチを評価することです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-123">When the intent is clear, and a legitimate need for a business event is established, the next step is to evaluate the approach that must be used to capture the business event.</span></span> <span data-ttu-id="d2ca9-124">このセクションでは、評価する必要があるアプローチについて要約します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-124">This section summarizes the approach that must be evaluated.</span></span>

<span data-ttu-id="d2ca9-125">使用するアプローチに関係なく、次の部分が使用されることを保証するために、ビジネス イベントの再現性は重要です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-125">Regardless of the approach that is used, the fidelity of business events is significant, because it helps guarantee that the following aspects are taken care of.</span></span> <span data-ttu-id="d2ca9-126">そのため、ビジネス イベント実装の設計の選択に影響します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-126">Therefore, it must influence the design choice for implementing the business event.</span></span> <span data-ttu-id="d2ca9-127">ただし、ビジネス イベントを実装するための設計の選択は、ビジネス イベントの概念に影響しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-127">However, the design choice that you make to implement a business event must not influence the concept of business events.</span></span> <span data-ttu-id="d2ca9-128">つまり、選択した設計が、イベントがビジネス イベントかどうかを決定する意思決定ツールとして使用されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-128">In other words, the chosen design must not be used as a decision-making tool, to determine whether an event is a business event.</span></span> <span data-ttu-id="d2ca9-129">目的を考えてこれらの決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-129">The intent must be used to make those decisions.</span></span>

- <span data-ttu-id="d2ca9-130">**堅牢なビジネス イベント** - 間違ったビジネス イベントは受信者に送信されません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-130">**Durable business events** – No false business events should be sent to the recipient.</span></span> <span data-ttu-id="d2ca9-131">発注書確認のビジネス イベントが送信される場合、受取人はその発注書が確認済みであることを信用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-131">If a purchase order confirmation business event is sent out, the recipient expects and must trust that the purchase order was really confirmed.</span></span> <span data-ttu-id="d2ca9-132">この設計の選択は、このトランザクションの性質を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-132">The design choice must help guarantee this transactional nature.</span></span> <span data-ttu-id="d2ca9-133">そのため、受信者の期待に違反するデザインの選択を行わないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-133">Therefore, you must not make a design choice that violates the recipient's expectations.</span></span>
- <span data-ttu-id="d2ca9-134">**目標** – ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-134">**Targeted** – Business events must be designed to optimize the consumption story for the recipient.</span></span> <span data-ttu-id="d2ca9-135">つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-135">In other words, you should make it as easy as possible for the recipient to consume business events.</span></span> <span data-ttu-id="d2ca9-136">そのため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-136">Therefore, business events must be as specific as possible and must be targeted to specific use cases.</span></span> <span data-ttu-id="d2ca9-137">消費者がペイロードを理解するよう試みてビジネス イベントが何であったか判断する必要があるため、ビジネス イベントは一般的なものであるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-137">They must not be generic, so that the consumer has to determine what the business event is for by trying to understand the payload.</span></span> <span data-ttu-id="d2ca9-138">デザインの選択は、対象となるビジネス イベントの保持のために許可されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-138">The design choice must allow for preservation of targeted business events.</span></span>
- <span data-ttu-id="d2ca9-139">**ノイズレス** – デザインはノイズを除外するための努力が最小になるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-139">**Noiseless** – The design should include very little effort to filter out noise.</span></span> <span data-ttu-id="d2ca9-140">ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルター ロジックの記述を避けます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-140">To make business events very specific, avoid writing filtering logic to filter out conditions that don't match the expected business event.</span></span> <span data-ttu-id="d2ca9-141">選択したアプローチは、ノイズ除去が必要でないように、十分に特定された時点でビジネス イベントがコードで実装されていることを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-141">The chosen approach must help guarantee that the business event is implemented in code at a sufficiently specific point so that no filtering of noise is required.</span></span> <span data-ttu-id="d2ca9-142">ロジックの追加によるノイズ除去の試行すべてはパフォーマンスに影響し、また特定のユースケースが複雑になることがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-142">Any attempt to filter noise by adding logic can affect performance and might also become complicated in specific use cases.</span></span>

| <span data-ttu-id="d2ca9-143">ビジネス ロジック レベルでのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="d2ca9-143">Capture at the business logic level</span></span> | <span data-ttu-id="d2ca9-144">テーブル レベルでのキャプチャ</span><span class="sxs-lookup"><span data-stu-id="d2ca9-144">Capture at the table level</span></span> |
|-------------------------------------|----------------------------|
| <span data-ttu-id="d2ca9-145">このレベルでのキャプチャは、トランザクションで発生するため、持続性を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-145">Capture at this level helps guarantee durability because it occurs in the transaction.</span></span> | <span data-ttu-id="d2ca9-146">このレベルでのキャプチャは、トランザクションで発生するため、持続性を保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-146">Capture at this level helps guarantee durability because it occurs in the transaction.</span></span> |
| <span data-ttu-id="d2ca9-147">このレベルでのキャプチャは、対象となるビジネス イベントに対して許可されています。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-147">Capture at this level allows for targeted business events.</span></span> | <span data-ttu-id="d2ca9-148">イベントは下位レベルでキャプチャされるため、対象となるビジネス イベントを提供することは困難です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-148">Because events are captured at a lower level, it's difficult to provide targeted business events.</span></span> |
| <span data-ttu-id="d2ca9-149">ノイズレスのままにすることは簡単です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-149">It's easy to remain noiseless.</span></span> | <span data-ttu-id="d2ca9-150">ノイズを除去するためのサウンド ロジックを実装する追加作業が行われるまで、ノイズレスのままにすることは困難です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-150">It's difficult to remain noiseless unless additional effort is made to implement sound logic that filters out noise.</span></span> |
| <span data-ttu-id="d2ca9-151">このレベルでのキャプチャにより、堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストが提供されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-151">Capture at this level provides additional context for the business process, and can significantly improve the durability and quality of the payload.</span></span> | <span data-ttu-id="d2ca9-152">イベントは下位レベルでキャプチャされるため、ビジネス プロセス コンテキストが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-152">Because events are captured at a lower level, business process context is probably lost.</span></span> |

> [!NOTE]
> <span data-ttu-id="d2ca9-153">一般に、テーブル レベルでビジネス イベントを実装する場合、上記の表で説明した問題に加えて、他の課題に直面する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-153">In general, if you implement business events at the table level, you might face other challenges, in addition to the challenges that are described in the preceding table.</span></span> <span data-ttu-id="d2ca9-154">たとえば、基になるテーブルのデータを更新するストアド プロシージャを使用してビジネス ロジックを実行する場合、X++ のテーブル挿入メソッドでそのビジネス イベントが実装されているため、そのイベントは生成すらされないことがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-154">For example, if the business logic is run via a stored procedure that updates data in the underlying table, the business event might not even be generated, because it was implemented in the table insert method in X++.</span></span> <span data-ttu-id="d2ca9-155">特定のユース ケースでは、多くの課題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-155">You might encounter additional challenges in specific use cases.</span></span> <span data-ttu-id="d2ca9-156">そのため、テーブル レベルでビジネス イベントを実装することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-156">Therefore, we don't recommend that you implement business events at the table level.</span></span>

## <a name="implement-a-business-event"></a><span data-ttu-id="d2ca9-157">ビジネス イベントの実装</span><span class="sxs-lookup"><span data-stu-id="d2ca9-157">Implement a business event</span></span>

<span data-ttu-id="d2ca9-158">ビジネス イベントを実装して送信することは非常に簡単です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-158">The process for implementing a business event and sending it is fairly straightforward.</span></span>

1. <span data-ttu-id="d2ca9-159">契約を構築します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-159">Build the contract.</span></span>
2. <span data-ttu-id="d2ca9-160">イベントを構築します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-160">Build the event.</span></span>
3. <span data-ttu-id="d2ca9-161">イベントを送信するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-161">Add code to send the event.</span></span> 

<span data-ttu-id="d2ca9-162">以下の 2 つのクラスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-162">Two classes must be implemented:</span></span>

- <span data-ttu-id="d2ca9-163">**ビジネス イベント** - このクラスは **BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-163">**Business event** – This class extends the **BusinessEventsBase** class.</span></span> <span data-ttu-id="d2ca9-164">ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-164">It supports constructing the business event, building the payload, and sending the business event.</span></span>
- <span data-ttu-id="d2ca9-165">**ビジネス イベント契約** - このクラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-165">**Business event contract** – This class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="d2ca9-166">ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-166">It defines the payload of the business event and allows for population of the contract at runtime.</span></span> 

### <a name="businesseventsbase-extension"></a><span data-ttu-id="d2ca9-167">BusinessEventsBase 拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2ca9-167">BusinessEventsBase extension</span></span>

#### <a name="naming-convention"></a><span data-ttu-id="d2ca9-168">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="d2ca9-168">Naming convention</span></span>

<span data-ttu-id="d2ca9-169">ビジネス イベントの名前は、\<名詞/名詞句\>\<過去時制のアクション\>BusinessEvent のパターンに従う必要があります</span><span class="sxs-lookup"><span data-stu-id="d2ca9-169">The names of business events should follow the pattern \<noun or noun phrase\>\<past tense action\>BusinessEvent.</span></span> <span data-ttu-id="d2ca9-170">名前の \<名詞/名詞句\> の部分は、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-170">The \<noun or noun phrase\> part of the name should comply with existing definitions for application area prefixes.</span></span>

<span data-ttu-id="d2ca9-171">**例**</span><span class="sxs-lookup"><span data-stu-id="d2ca9-171">**Examples**</span></span>

- <span data-ttu-id="d2ca9-172">VendorInvoicePostedBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="d2ca9-172">VendorInvoicePostedBusinessEvent</span></span>
- <span data-ttu-id="d2ca9-173">CollectionLetterSentBusinessEvent</span><span class="sxs-lookup"><span data-stu-id="d2ca9-173">CollectionLetterSentBusinessEvent</span></span>

#### <a name="implementation"></a><span data-ttu-id="d2ca9-174">実装</span><span class="sxs-lookup"><span data-stu-id="d2ca9-174">Implementation</span></span>

<span data-ttu-id="d2ca9-175">**BusinessEventsBase** クラスの拡張機能を実装するプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-175">The process of implementing an extension of the **BusinessEventsBase** class is straightforward.</span></span> <span data-ttu-id="d2ca9-176">**BusinessEventsBase** クラスの拡張、および静的コンストラクター メソッドの実装、プライベート **新規** メソッド、内部状態を保持するメソッド、および **buildContract** メソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-176">It involves extending the **BusinessEventsBase** class, and implementing a static constructor method, a private **new** method, methods to maintain internal state, and the **buildContract** method.</span></span>

1. <span data-ttu-id="d2ca9-177">**newFrom\<my\_buffer\>** 静的メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-177">Implement a static **newFrom\<my\_buffer\>** method.</span></span> <span data-ttu-id="d2ca9-178">メソッド名の \<my\_buffer\> の部分は通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-178">The \<my\_buffer\> part of the method name is typically the table buffer that is used to initialize the business event contract.</span></span>

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

2. <span data-ttu-id="d2ca9-179">**BusinessEventsBase** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-179">Extend the **BusinessEventsBase** class.</span></span>

    ```
    [BusinessEvents(classStr(SalesInvoicePostedBusinessEventContract),
    "AccountsReceivable:SalesOrderInvoicePostedBusinessEventName","AccountsReceivable:SalesOrderInvoicePostedBusinessEventDescription",ModuleAxapta::SalesOrder)]
    public class SalesInvoicePostedBusinessEvent extends BusinessEventsBase
    ```

    <span data-ttu-id="d2ca9-180">**BusinessEvents** 属性に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-180">Note the **BusinessEvents** attribute.</span></span> <span data-ttu-id="d2ca9-181">この属性は、ビジネス イベントの契約、名前、説明に関する情報を含む、ビジネス イベント フレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-181">This attribute provides the business events framework with information about the business event's contract, name, and description.</span></span> <span data-ttu-id="d2ca9-182">また、ビジネス イベントが含まれるモジュールも提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-182">It also provides the module that the business event is part of.</span></span> <span data-ttu-id="d2ca9-183">名前および説明の引数のためにラベルを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-183">Labels must be defined for the name and description arguments.</span></span> <span data-ttu-id="d2ca9-184">ただし、このようなラベルは記号 (@) なしで参照して、ローカライズされたデータの保存を回避する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-184">However, these labels should be referenced without the at symbol (@) to avoid storing localized data.</span></span>

3. <span data-ttu-id="d2ca9-185">プライベート **新規** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-185">Implement a private **new** method.</span></span> <span data-ttu-id="d2ca9-186">このメソッドは静的コンストラクター メソッドからのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-186">This method is called only from the static constructor method.</span></span>

    ```
    private void new()
    {
    }
    ```

4. <span data-ttu-id="d2ca9-187">内部状態を維持するプライベート **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-187">Implement private **parm** methods to maintain internal state.</span></span>

    ```
    private CustInvoiceJour parmCustInvoiceJour(CustInvoiceJour _custInvoiceJour = custInvoiceJour)
    {
        custInvoiceJour = _custInvoiceJour;
        return custInvoiceJour;
    }
    ```

5. <span data-ttu-id="d2ca9-188">**buildContract** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-188">Implement the **buildContract** method.</span></span> <span data-ttu-id="d2ca9-189">このステップには **EventContract** スタブが必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-189">Note that you need an **EventContract** stub for this step.</span></span>

    ```
    [Wrappable(true), Replaceable(true)]
    public BusinessEventsContract buildContract()
    {
        return
        SalesInvoicePostedBusinessEventContract::newFromCustInvoiceJour(custInvoiceJour);
    }
    ```

    <span data-ttu-id="d2ca9-190">拡張機能のために、**buildContract** メソッドには **Wrappable(true)** および **Replaceable(true)** 属性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-190">For extensibility, the **buildContract** method must have the **Wrappable(true)** and **Replaceable(true)** attributes.</span></span> <span data-ttu-id="d2ca9-191">**buildContract** メソッドは会社のためにビジネス イベントが有効にされる時にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-191">The **buildContract** method is called only when a business event is enabled for a company.</span></span>

<span data-ttu-id="d2ca9-192">これは、「転記された販売注文請求書」ビジネス イベントの完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-192">Here is the complete implementation of the "Sales order invoice posted" business event.</span></span>

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

### <a name="businesseventscontract-extension"></a><span data-ttu-id="d2ca9-193">BusinessEventsContract 拡張機能</span><span class="sxs-lookup"><span data-stu-id="d2ca9-193">BusinessEventsContract extension</span></span>

<span data-ttu-id="d2ca9-194">ビジネス イベント契約クラスは **BusinessEventsContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-194">A business event contract class extends the **BusinessEventsContract** class.</span></span> <span data-ttu-id="d2ca9-195">ビジネス イベントのペイロードを定義および入力します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-195">It defines and populates the payload of the business event.</span></span> <span data-ttu-id="d2ca9-196">ビジネス イベントには一部の変動がありますが、ビジネス イベント契約の基本構造は一貫しています。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-196">Although there is some variation across business events, the basic structure of the business event contract is consistent.</span></span>

<span data-ttu-id="d2ca9-197">ビジネス イベント契約の実装プロセスには、**BusinessEventContract** クラスの拡張、内部状態の定義、初期化メソッドの実装、静的コンストラクター メソッドの実装、および契約状態にアクセスするための **parm** メソッドの実装が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-197">The process of implementing a business event contract involves extending the **BusinessEventContract** class, defining internal state, implementing an initialization method, implementing a static constructor method, and implementing **parm** methods to access the contract state.</span></span>

1. <span data-ttu-id="d2ca9-198">**BusinessEventContract** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-198">Extend the **BusinessEventContract** class.</span></span>

    ```
    [DataContract]
    public final class SalesInvoicePostedBusinessEventContract extends
    BusinessEventsContract
    ```

    <span data-ttu-id="d2ca9-199">このクラスには、**DataContract** 属性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-199">The class must have the **DataContract** attribute.</span></span>

2. <span data-ttu-id="d2ca9-200">契約状態を保持するプライベート変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-200">Add private variables to hold the contract state.</span></span>

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

3. <span data-ttu-id="d2ca9-201">プライベート初期化メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-201">Implement a private initialization method.</span></span>

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

    <span data-ttu-id="d2ca9-202">**初期化**メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-202">The **initialize** method is responsible for setting the private state of the business event contract class, based on data that is provided through the static constructor method.</span></span>

4. <span data-ttu-id="d2ca9-203">静的コンストラクター メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-203">Implement a static constructor method.</span></span>

    ```
    public static SalesInvoicePostedBusinessEventContract
    newFromCustInvoiceJour(CustInvoiceJour _custInvoiceJour)
    {
        var contract = new SalesInvoicePostedBusinessEventContract();
        contract.initialize(_custInvoiceJour);
        return contract;
    }
    ```

    <span data-ttu-id="d2ca9-204">静的コンストラクター メソッドはプライベート **初期化** メソッドを呼び出して、プライベート クラス状態を初期化します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-204">The static constructor method calls a private **initialize** method to initialize the private class state.</span></span>

5. <span data-ttu-id="d2ca9-205">契約状態にアクセスするための **parm** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-205">Implement **parm** methods to access the contract state.</span></span>

    ```
    [DataMember('InvoiceAccount'), BusinessEventsDataMember("@AccountsReceivable:InvoiceAccount")]
    public CustInvoiceAccount parmInvoiceAccount(CustInvoiceAccount _invoiceAccount = invoiceAccount)
    {
        invoiceAccount = _invoiceAccount;
        return invoiceAccount;
    }
    ```

    <span data-ttu-id="d2ca9-206">**parm** メソッドには **DataMember('\<名前\>')** および **BusinessEventsDataMember('\<説明\>')** 属性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-206">The **parm** methods should have the **DataMember('\<name\>')** and **BusinessEventsDataMember('\<description\>')** attributes.</span></span> <span data-ttu-id="d2ca9-207">**DataMember** 属性で提供する名前 (たとえば、**'InvoiceAccount'**) はデータ契約消費者に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-207">The name that you provide on the **DataMember** attribute (for example, **'InvoiceAccount'**) will be visible to data contract consumers.</span></span> <span data-ttu-id="d2ca9-208">**BusinessEventsDataMember** 属性で指定された説明は、ビジネス イベント カタログ UI に表示され、この契約のデータ メンバーを説明するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-208">The description that you provide in the **BusinessEventsDataMember** attribute will be visible in the Business Events catalog user interface (UI) and used to describe this contract's data members.</span></span>

> [!NOTE]
> - <span data-ttu-id="d2ca9-209">**RecId** 値はビジネス イベントのペイロードの一部にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-209">**RecId** values should not be part of a business event's payload.</span></span> <span data-ttu-id="d2ca9-210">代わりに代替キー (AK) を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-210">Use the alternate key (AK) instead.</span></span>
> - <span data-ttu-id="d2ca9-211">列挙型 (enum) 値は、公開する前にそのシンボル値に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-211">Enumeration (enum) values must be converted to their symbol value before they can be published.</span></span> <span data-ttu-id="d2ca9-212">**enum2Symbol** メソッドを使用して列挙型の値をシンボル文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-212">Use the **enum2Symbol** method to convert an enum's value to the symbol string.</span></span> <span data-ttu-id="d2ca9-213">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-213">Here is an example:</span></span>
>
>    ```
>    status = enum2Symbol(enumNum(CustVendDisputeStatus), _custDispute.Status);
>    ```

<span data-ttu-id="d2ca9-214">場合によっては、データ契約の内部状態の投入のために、追加の取得メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-214">In some cases, population of the data contract's internal state requires that you implement additional retrieval methods.</span></span> <span data-ttu-id="d2ca9-215">これらの取得メソッドはプライベート メソッドとして実装し、**初期化** メソッドから呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-215">These retrieval methods should be implemented as private methods, and they should be called from the **initialize** method.</span></span>

<span data-ttu-id="d2ca9-216">これは、「転記された販売注文請求書」ビジネス イベント契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-216">Here is the complete implementation of the "Sales order invoice posted" business event contract.</span></span>

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

## <a name="sending-a-business-event"></a><span data-ttu-id="d2ca9-217">ビジネス イベントの送信</span><span class="sxs-lookup"><span data-stu-id="d2ca9-217">Sending a business event</span></span>

<span data-ttu-id="d2ca9-218">適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-218">You must modify application code so that it sends the business event at the appropriate point.</span></span> <span data-ttu-id="d2ca9-219">多くの場合、フレームワークの共通ポイントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-219">Often, you can use a common point in a framework.</span></span> <span data-ttu-id="d2ca9-220">**SourceDocument** を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-220">Documents that extend **SourceDocument** have a common point for creating and sending a business event.</span></span> <span data-ttu-id="d2ca9-221">詳細については、このトピックの後半の [ソース ドキュメント フレームワークのサポート](#source-document-framework-support) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-221">For more information, see the [Source document framework support](#source-document-framework-support) section later in this topic.</span></span>

<span data-ttu-id="d2ca9-222">また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-222">Other frameworks also provide common points for sending business events.</span></span> <span data-ttu-id="d2ca9-223">たとえば、アプリケーション オブジェクト ツリー (AOT) 内の **CustVendVoucher** クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、**転記** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-223">For example, the **CustVendVoucher** class hierarchy in the Application Object Tree (AOT) has a **post** method that is used to send business events that are related to posting customer or vendor vouchers.</span></span> <span data-ttu-id="d2ca9-224">基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-224">Overrides of the base class implementation provide specialization of the logic for sending business events.</span></span> <span data-ttu-id="d2ca9-225">例については、AOT の **CustVoucher.createBusinessEvent** または **VendVoucher.createBusinessEvent** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-225">For an example, see **CustVoucher.createBusinessEvent** or **VendVoucher.createBusinessEvent** in the AOT.</span></span>

<span data-ttu-id="d2ca9-226">ビジネス イベントの送信は、基になる取引のコミットにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-226">The sending of a business event is linked to the commit of the underlying transaction.</span></span> <span data-ttu-id="d2ca9-227">基になる取引が中止される場合、ビジネス イベントは送信されません。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-227">If the underlying transaction is aborted, the business event won't be sent.</span></span> <span data-ttu-id="d2ca9-228">そのため、アプリケーションはペイロード情報が使用可能なポイントでビジネス イベントを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-228">Therefore, applications can send the business event at the point where the payload information is available.</span></span>

<span data-ttu-id="d2ca9-229">ビジネス イベント フレームワークは、ビジネス イベントが消費者に公開されるかどうか決定します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-229">The business events framework determines whether a business event is published to a consumer.</span></span> <span data-ttu-id="d2ca9-230">一般的なルールとして、ビジネス イベントが有効かどうかに関わらず、アプリケーションはビジネス イベントを常に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-230">As a general rule, applications should always send a business event, regardless of whether the business event is enabled.</span></span> <span data-ttu-id="d2ca9-231">重要な追加ロジックが必要な場合、またはビジネス イベントを送信するためのロジックがパフォーマンスに影響する場合は、ビジネス イベントの送信に関連付けられたビジネス ロジックを実行する前に、アプリケーションは特定のビジネス イベントが有効化されているかどうか確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-231">If significant additional logic is required, or if the logic for sending a business event has a performance impact, an application can check whether a specific business event is enabled before it runs business logic that is associated with sending business events.</span></span> <span data-ttu-id="d2ca9-232">この確認は **BusinessEventsConfigurationReader::isBusinessEventEnabled** メソッドを介して実行されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-232">This check is done through the **BusinessEventsConfigurationReader::isBusinessEventEnabled** method.</span></span>

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

## <a name="source-document-framework-support"></a><span data-ttu-id="d2ca9-233">ソース ドキュメント フレームワークのサポート</span><span class="sxs-lookup"><span data-stu-id="d2ca9-233">Source document framework support</span></span>

<span data-ttu-id="d2ca9-234">元伝票フレームワークは、ドキュメントのプロセス内状態から完了状態への移行の一部として、ビジネス イベントの自動送信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-234">The source document framework supports sending business events automatically as part of the transition from an in-process state to a completed state for the document.</span></span> <span data-ttu-id="d2ca9-235">この機能を活用するには、元伝票フレームワークを拡張するドキュメントが **SourceDocumentStateInProcess.getBusinessEvent** メソッドの拡張機能を実装して、正確な **BusinessEventsBase** 拡張子タイプを作成して戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-235">To take advantage of this capability, documents that extend the source document framework must implement an extension of the **SourceDocumentStateInProcess.getBusinessEvent** method to create and return the correct **BusinessEventsBase** extension type.</span></span>

## <a name="extending-a-business-event-payload"></a><span data-ttu-id="d2ca9-236">ビジネス イベント ペイロードの拡張</span><span class="sxs-lookup"><span data-stu-id="d2ca9-236">Extending a business event payload</span></span>

<span data-ttu-id="d2ca9-237">ビジネス イベントのペイロードの一部として、追加情報を公開する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-237">You might want to publish additional information as part of the payload of a business event.</span></span> <span data-ttu-id="d2ca9-238">この追加情報を送信するには、ビジネス イベントの標準ペイロードを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-238">To send this additional information, you must extend the business event's standard payload.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="d2ca9-239">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="d2ca9-239">Example scenario</span></span>

<span data-ttu-id="d2ca9-240">この例では、**CustFreeTextInvoicePostedBusinessEventContract** を拡張して顧客の分類を含める方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-240">This example shows how to extend the **CustFreeTextInvoicePostedBusinessEventContract** class so that it includes a customer classification.</span></span> <span data-ttu-id="d2ca9-241">この顧客分類は業界に基づくカスタム分類です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-241">This customer classification is an industry-based custom classification.</span></span>

#### <a name="step-1-create-an-extended-business-event-contract"></a><span data-ttu-id="d2ca9-242">ステップ 1: 拡張されたビジネス イベント契約の作成</span><span class="sxs-lookup"><span data-stu-id="d2ca9-242">Step 1: Create an extended business event contract</span></span>

<span data-ttu-id="d2ca9-243">標準的なビジネス イベント契約、およびペイロードに含める必要がある追加情報で構成される契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-243">Create a contract that consists of the standard business event contract plus any additional information that must be included in the payload.</span></span>

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

#### <a name="step-2-create-an-initialize-method"></a><span data-ttu-id="d2ca9-244">ステップ 2: 初期化メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="d2ca9-244">Step 2: Create an initialize method</span></span>

<span data-ttu-id="d2ca9-245">プライベート契約の値を初期化する **初期化** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-245">Create an **initialize** method that initializes the value of the private contract.</span></span>

```
private void initialize(CustFreeTextInvoicePostedBusinessEventContract
_custFreeTextInvoicePostedBusinessEventContract)
{
    custFreeTextInvoicePostedBusinessEventContract =
    _custFreeTextInvoicePostedBusinessEventContract;
}
```

#### <a name="step-3-create-a-static-newfrom-method"></a><span data-ttu-id="d2ca9-246">ステップ 3: 静的 newFrom メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="d2ca9-246">Step 3: Create a static newFrom method</span></span>

<span data-ttu-id="d2ca9-247">標準契約を引数として取得し **初期化** メソッドを呼び出す、静的 **newFrom** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-247">Create a static **newFrom** method that takes the standard contract as an argument and calls the **initialize** method.</span></span>

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

#### <a name="step-4-map-parm-methods"></a><span data-ttu-id="d2ca9-248">ステップ 4: parm メソッドのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2ca9-248">Step 4: Map parm methods</span></span>

<span data-ttu-id="d2ca9-249">**parm** メソッドを標準データ コントラクトからコピーして、クラスの標準契約インスタンス内で値を取得およびセットするように各メソッドを修正します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-249">Copy the **parm** methods from the standard data contract, and modify each method so that it gets and sets values in the class's standard contract instance.</span></span>

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

#### <a name="step-5-add-parm-methods-for-additional-payload-data"></a><span data-ttu-id="d2ca9-250">ステップ 5: 追加ペイロード データのために parm メソッドを追加する</span><span class="sxs-lookup"><span data-stu-id="d2ca9-250">Step 5: Add parm methods for additional payload data</span></span>

```
[DataMember('CustomerClassification')]
public CustomerClassification parmCustomerClassification(CustomerClassification
_customerClassification = customerClassification)
{
    customerClassification = _customerClassification;
    return customerClassification;
}
```

<span data-ttu-id="d2ca9-251">これは拡張ビジネス契約の完全な実装です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-251">Here is the complete implementation of the extended business contract.</span></span>

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

#### <a name="step-6-wrap-the-buildcontract-method"></a><span data-ttu-id="d2ca9-252">ステップ 6: buildContract メソッドをラップします。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-252">Step 6: Wrap the buildContract method</span></span>

<span data-ttu-id="d2ca9-253">標準ビジネス イベント契約をロードしてペイロード拡張機能を投入する **next** を呼び出す、ビルド契約の実装を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-253">Provide a build contract implementation that calls **next** to load the standard business event contract and populates any payload extensions.</span></span> <span data-ttu-id="d2ca9-254">これは完全なクラスです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-254">Here is the complete class.</span></span>

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

## <a name="extending-filters-so-that-they-have-custom-fields-if-the-middleware-supports-this-extension"></a><span data-ttu-id="d2ca9-255">カスタム フィールドを持つようにフィルターを拡張する (ミドルウェアがこの拡張機能をサポートしている場合)</span><span class="sxs-lookup"><span data-stu-id="d2ca9-255">Extending filters so that they have custom fields (if the middleware supports this extension)</span></span>

<span data-ttu-id="d2ca9-256">一部のミドルウェア システムはイベントのフィルター処理を許可します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-256">Some middleware systems allow for filtering of the events.</span></span> <span data-ttu-id="d2ca9-257">たとえば、Microsoft Azure Service Bus にはキーと値のペアを設定できるプロパティ バッグがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-257">For example, Microsoft Azure Service Bus has a property bag that can be populated with key-value pairs.</span></span> <span data-ttu-id="d2ca9-258">これらのキーと値のペアは、Service Bus のキューやトピックからの読み込み時にイベントをフィルター処理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-258">These key-value pairs can be used to filter events when reading from the Service Bus Queue or Topic.</span></span> <span data-ttu-id="d2ca9-259">また、Azure イベント グリッドには**件名**、**イベント タイプ**、および **ID** などのフィルター処理が可能なメッセージ プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-259">Additionally, Azure Event Grid has filterable message properties such as **Subject**, **Event Type**, and **ID**.</span></span> <span data-ttu-id="d2ca9-260">異なるシステムに対してこれら各種プロパティをサポートするために、ビジネス イベントのフレームワークは、*ペイロード コンテキスト*という名前の概念を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-260">To support these various properties for the different systems, the Business Events framework uses a concept that is named *payload context*.</span></span> <span data-ttu-id="d2ca9-261">この概念を拡張して、さまざまなイベント システムがフィルター処理のために使用できるカスタム フィールドを含めることができます</span><span class="sxs-lookup"><span data-stu-id="d2ca9-261">This concept can be extended so that it includes custom fields that the different eventing systems can use for filtering.</span></span>

### <a name="payload-context"></a><span data-ttu-id="d2ca9-262">ペイロード コンテキスト</span><span class="sxs-lookup"><span data-stu-id="d2ca9-262">Payload context</span></span>

<span data-ttu-id="d2ca9-263">ビジネス イベント フレームワークは、ペイロード コンテキストの概念をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-263">The Business Events framework supports the payload context concept.</span></span> <span data-ttu-id="d2ca9-264">ペイロード コンテキストは、フレームワークがペイロードに関するコンテキストと共に送信するメッセージを装飾する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-264">Payload context provides a way to decorate messages that the framework sends with context about the payload.</span></span> <span data-ttu-id="d2ca9-265">一部のシナリオでは、メッセージがエンドポイントに送信される時、追加のコンテキストが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-265">In some scenarios, additional context might be required when messages are sent to endpoints.</span></span> <span data-ttu-id="d2ca9-266">そのため、フレームワークにはコンテキストの上書きやアダプタのカスタマイズができるフックポイントがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-266">Therefore, the framework has hookpoints where the context can be overwritten and the adapters can be customized.</span></span>

### <a name="step-1-add-a-custom-payload-context"></a><span data-ttu-id="d2ca9-267">ステップ 1: カスタム ペイロード コンテキストを追加します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-267">Step 1: Add a custom payload context</span></span>

<span data-ttu-id="d2ca9-268">カスタム ペイロード コンテキストは **BusinessEventsCommitLogPayloadContext** クラスから拡張される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-268">A custom payload context must be extended from the **BusinessEventsCommitLogPayloadContext** class.</span></span>

```
class CustomCommitLogPayloadContext extends BusinessEventsCommitLogPayloadContext
{
    private utcdatetime eventTime;
    public utcdatetime parmEventTime(utcdatetime \_eventTime = eventTime)
    {
        eventTime = \_eventTime;
        return eventTime;
    }
}
```

### <a name="step-2-construct-the-custom-payload-context"></a><span data-ttu-id="d2ca9-269">ステップ 2: カスタム ペイロード コンテキストを構築します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-269">Step 2: Construct the custom payload context</span></span>

<span data-ttu-id="d2ca9-270">新しいペイロード コンテキスト タイプを構築するには、**BusinessEventsSender.buildPayloadContext** メソッドに対してコマンド チェーン (CoC) 拡張機能を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-270">A Chain of Command (CoC) extension must be written for the **BusinessEventsSender.buildPayloadContext** method, so that it can construct the new payload context type.</span></span>

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

### <a name="step-3-consume-the-custom-payload-context-from-an-adapter"></a><span data-ttu-id="d2ca9-271">ステップ 3: アダプターからカスタム ペイロード コンテキストを使用します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-271">Step 3: Consume the custom payload context from an adapter</span></span>

<span data-ttu-id="d2ca9-272">ペイロード コンテキストを使用するアダプターは、新しいペイロード コンテキストの使用を許可する CoC メソッドを公開するように記述されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-272">Adapters that consume payload context are written in such a way that they expose CoC methods that allow for the consumption of new payload contexts.</span></span> <span data-ttu-id="d2ca9-273">次の例は、サービス バス アダプターに対するこのステップの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-273">The following example shows what this step looks like for the Service Bus adapter.</span></span> <span data-ttu-id="d2ca9-274">このアダプターには、サービス バスの消費者がフィルター処理できる汎用のプロパティ バッグがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-274">This adapter has a generic property bag that Service Bus consumers can filter on.</span></span>

<span data-ttu-id="d2ca9-275">**BusinessEventsServiceBusAdapter** には **addProperties** という名前の CoC メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-275">The **BusinessEventsServiceBusAdapter** has the CoC method that is named **addProperties**.</span></span>

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
            // Convert the enum to string to be able to serialize the property.
            propertyBag.Add('BusinessEventCategory', enum2Symbol(enumNum(ModuleAxapta),
            customPayloadContext.parmBusinessEventCategory()));
            propertyBag.Add('LegalEntity', customPayloadContext.parmLegalEntity());
            propertyBag.Add('EventTime', customPayloadContext.parmEventTime());
        }
    }
}
```

## <a name="adding-a-custom-endpoint-type"></a><span data-ttu-id="d2ca9-276">カスタム エンドポイント タイプの追加</span><span class="sxs-lookup"><span data-stu-id="d2ca9-276">Adding a custom endpoint type</span></span>
<span data-ttu-id="d2ca9-277">ビジネス イベント フレームワークは、最初から用意されているエンドポイント タイプに加え、新しいエンドポイント タイプの追加物もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-277">The Business Events framework supports the addition of new endpoint types to the out-of-box endpoint types.</span></span> <span data-ttu-id="d2ca9-278">このセクションでは、新しいカスタム エンドポイント タイプの追加方法を示す例を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-278">This section provides an example that shows how to add new custom endpoint types.</span></span>

### <a name="step-1-add-a-new-endpoint-type"></a><span data-ttu-id="d2ca9-279">ステップ 1: 新しいエンドポイント タイプを追加します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-279">Step 1: Add a new endpoint type</span></span>

<span data-ttu-id="d2ca9-280">各エンドポイント タイプは、列挙 **BusinessEventsEndpointType** によって表されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-280">Each endpoint type is represented by the **BusinessEventsEndpointType** enum.</span></span> <span data-ttu-id="d2ca9-281">新しいエンドポイントを追加するプロセスの最初のステップは、次のセクションに示すように、この列挙を拡張することです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-281">The first step in the process of adding a new endpoint is to extend this enum, as shown in the following section.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint1.png)

### <a name="step-2-add-a-new-endpoint-table-to-the-hierarchy"></a><span data-ttu-id="d2ca9-283">ステップ 2: 新しいエンドポイント テーブルを階層に追加します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-283">Step 2: Add a new endpoint table to the hierarchy</span></span>

<span data-ttu-id="d2ca9-284">すべてのエンドポイント データは階層テーブルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-284">All endpoint data is stored in a hierarchy table.</span></span> <span data-ttu-id="d2ca9-285">このテーブルのルートは、BusinessEventsEndpoint テーブルです。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-285">The root of this table is the BusinessEventsEndpoint table.</span></span> <span data-ttu-id="d2ca9-286">新しいエンドポイント テーブルは、**サポート継承**プロパティを **Yes** に、**拡張**プロパティを **"BusinessEventsEndpoint"** (または BusinessEventsEndpoint 階層内の他の任意のエンドポイント) に設定して、このルート テーブルを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-286">A new endpoint table must extend this root table by setting the **Support Inheritance** property to **Yes** and the **Extends** property to **"BusinessEventsEndpoint"** (or any other endpoint in the BusinessEventsEndpoint hierarchy).</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint2.png)

<span data-ttu-id="d2ca9-288">その後、新しいテーブルに、初期化およびコード内でのエンドポイントとの通信に必要なカスタム フィールドの定義が保持されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-288">The new table then holds the definition of the custom fields that are required to initialize and communicate with the endpoint in code.</span></span> <span data-ttu-id="d2ca9-289">競合を回避するには、属している特定のエンドポイントに対してフィールド名を限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-289">To help avoid conflict, you should qualify field names to the specific endpoint where they belong.</span></span> <span data-ttu-id="d2ca9-290">たとえば、2 つのエンドポイントは、**URL** フィールドの概念を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-290">For example, two endpoints can have the concept of a **URL** field.</span></span> <span data-ttu-id="d2ca9-291">フィールドを区別するために、名前はカスタム エンドポイントに対して固有である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-291">To distinguish the fields, names should be specific to the custom endpoint.</span></span> <span data-ttu-id="d2ca9-292">たとえば、カスタム エンドポイントの **CustomURL** のフィールドに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-292">For example, name the field for the custom endpoint **CustomURL**.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint3.png)

### <a name="step-3-add-a-new-endpoint-adapter-class-that-implements-the-ibusinesseventsendpoint-interface"></a><span data-ttu-id="d2ca9-294">ステップ 3: IBusinessEventsEndpoint インターフェイスを実装する新しいエンドポイント アダプター クラスを追加します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-294">Step 3: Add a new endpoint adapter class that implements the IBusinessEventsEndpoint interface</span></span>

<span data-ttu-id="d2ca9-295">新しいエンドポイント アダプター クラスは、**IBusinessEventsEndpoint** インターフェイスを実装している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-295">The new endpoint adapter class must implement the **IBusinessEventsEndpoint** interface.</span></span> <span data-ttu-id="d2ca9-296">また、**BusinessEventsEndpointAttribute** 属性で装飾する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-296">It must also be decorated with the **BusinessEventsEndpointAttribute** attribute.</span></span>

```
[BusinessEventsEndpoint(BusinessEventsEndpointType::CustomEndpoint)]
public class CustomEndpointAdapter implements IBusinessEventsEndpoint
{
```

<span data-ttu-id="d2ca9-297">**初期化**メソッドを実装して、渡された **BusinessEventsEndpoint** バッファーのタイプを確認し、次の例が示すように、バッファーが適切な型である場合は初期化します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-297">The **initialize** method should be implemented to check the type of the **BusinessEventsEndpoint** buffer that is passed in, and then, if the buffer is of the correct type, initialize it, as shown in the following example.</span></span>

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

### <a name="step-4-extend-the-endpointconfiguration-form"></a><span data-ttu-id="d2ca9-298">ステップ 4: EndpointConfiguration フォームを拡張します</span><span class="sxs-lookup"><span data-stu-id="d2ca9-298">Step 4: Extend the EndpointConfiguration form</span></span>

<span data-ttu-id="d2ca9-299">カスタム フィールド入力を保持するには FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ の下に新しいグループ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-299">Add a new group control under FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ to hold your custom field input.</span></span>

![ビジネス イベントのエンドポイント](../media/customendpoint4.png)

<span data-ttu-id="d2ca9-301">カスタム フィールドの入力は、前の手順で作成した新しいテーブルとフィールドにバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-301">The custom field input should be bound to the new table and field that you created in the previous step.</span></span> <span data-ttu-id="d2ca9-302">次の例に示すように、**BusinessEventsEndpointConfiguration** フォームの **getConcreteType** と **showOtherFields** メソッドを拡張するクラス拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-302">Create a class extension to extend the **getConcreteType** and **showOtherFields** methods of **BusinessEventsEndpointConfiguration** form, as shown in the following example.</span></span>

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

## <a name="adding-human-readable-data-fields-to-the-payload"></a><span data-ttu-id="d2ca9-304">ペイロードに人が判読可能なデータ フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-304">Adding human-readable data fields to the payload</span></span>

<span data-ttu-id="d2ca9-305">この機能は、Platform 更新 30 以降でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-305">This feature is available in Platform update 30 and later.</span></span>

<span data-ttu-id="d2ca9-306">ビジネス イベントのシリアル化には、FormJsonSerializer を使用してデータ契約内のオブジェクトをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-306">The serialization of business events uses FormJsonSerializer to serialize objects in the data contract.</span></span> <span data-ttu-id="d2ca9-307">FormJsonSerializer は、**UtcDataTime** の値を ISO 8601 の日時形式にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-307">FormJsonSerializer can format **UtcDataTime** values in the ISO 8601 date and time format.</span></span> <span data-ttu-id="d2ca9-308">ビジネス イベンのペイロードを表示する時、人が判読可能な形式になります。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-308">This format is human-readable when the payload of a business event is viewed.</span></span> <span data-ttu-id="d2ca9-309">たとえば、**UtcDataTime**の値を、**/Date(1196865000000)/** の代わりに、**2007-12-05T14:30Z**の形式にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-309">For example, a **UtcDataTime** value can now be formatted as **"2007-12-05T14:30Z"** instead of **"/Date(1196865000000)/"**.</span></span> <span data-ttu-id="d2ca9-310">「/Date(N)」形式では、N は 1970 年 1 月 1 日 (UTC+0) から経過したミリ秒数です。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-310">In the "/Date(N)" format, N is the number of milliseconds that have passed since January 1, 1970, UTC+0.</span></span> <span data-ttu-id="d2ca9-311">ISO 形式は、JavaScript Object Notation (JSON) を解析するツールで、より頻繁に理解されます。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-311">The ISO format is more often understood by tools that parse JavaScript Object Notation (JSON).</span></span>

<span data-ttu-id="d2ca9-312">人が判読可能な形式にするため、**DateTimeIso8601** という名前の拡張データ型 (EDT) をデータ契約の値の型として使用します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-312">To get the human-readable format, use the extended data type (EDT) that is named **DateTimeIso8601** as the type of the value in the data contract.</span></span> <span data-ttu-id="d2ca9-313">または、**DateTimeIso8601** EDTから派生した EDT を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2ca9-313">Alternatively, use an EDT that is derived from the **DateTimeIso8601** EDT.</span></span>

```X++
[DataMember("TestIsoEdtUtcDateTime")]
public DateTimeIso8601 testIsoEdtUtcDateTime(DateTimeIso8601 _value = this._testIsoDateTime)
{
    if (!prmIsDefault(_value))
    {
        this._testIsoDateTime = _value;
    }
    return this._testIsoDateTime;
}
```