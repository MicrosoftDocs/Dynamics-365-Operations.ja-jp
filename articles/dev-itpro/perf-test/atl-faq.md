---
title: 承認テスト ライブラリに関するよく寄せられる質問
description: このトピックでは、承認テスト ライブラリに関するよくある質問に対する回答を示します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: RobinARH
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 785f6e5af09c46caa88dddfcfb04c3057b350d48
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537281"
---
# <a name="acceptance-test-library-faq"></a><span data-ttu-id="584fc-103">承認テスト ライブラリに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="584fc-103">Acceptance test library FAQ</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="which-fluent-prefix-should-i-use-set-for-or-with"></a><span data-ttu-id="584fc-104">どの Fluent な接頭辞を使用しますか: set、for、with</span><span class="sxs-lookup"><span data-stu-id="584fc-104">Which fluent prefix should I use: set, for, or with?</span></span>

<span data-ttu-id="584fc-105">Fluent メソッドを追加するクラスにより、異なるルールが適用されます:</span><span class="sxs-lookup"><span data-stu-id="584fc-105">Depending on the class that you want to add a fluent method to, different rules might apply:</span></span>

- [<span data-ttu-id="584fc-106">エンティティ</span><span class="sxs-lookup"><span data-stu-id="584fc-106">Entities</span></span>](concepts-entities.md)
- [<span data-ttu-id="584fc-107">作成者</span><span class="sxs-lookup"><span data-stu-id="584fc-107">Creators</span></span>](concepts-creators.md)
- <span data-ttu-id="584fc-108">[[コマンド]](concepts-commands.md)</span><span class="sxs-lookup"><span data-stu-id="584fc-108">[Commands](concepts-commands.md)</span></span>
- [<span data-ttu-id="584fc-109">クエリ</span><span class="sxs-lookup"><span data-stu-id="584fc-109">Queries</span></span>](concepts-queries.md)
- [<span data-ttu-id="584fc-110">詳細</span><span class="sxs-lookup"><span data-stu-id="584fc-110">Specifications</span></span>](concepts-specifications.md)

## <a name="should-i-implement-an-entity-or-a-creator-class"></a><span data-ttu-id="584fc-111">エンティティまたは作成者クラスを実装する必要があるか</span><span class="sxs-lookup"><span data-stu-id="584fc-111">Should I implement an entity or a creator class?</span></span>

<span data-ttu-id="584fc-112">ほとんどのエンティティに対して、エンティティ クラスを作成する作業は作成者クラスを作成する作業と同じです。</span><span class="sxs-lookup"><span data-stu-id="584fc-112">For most entities, the effort of creating an entity class is the same as the effort of creating a creator class.</span></span> <span data-ttu-id="584fc-113">したがって、エンティティ クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="584fc-113">Therefore, the entity class should be created.</span></span> <span data-ttu-id="584fc-114">ただし、場合によっては、エンティティを作成するプロセスは複雑な可能性があります。</span><span class="sxs-lookup"><span data-stu-id="584fc-114">However, in some cases, the process of creating an entity might not be straightforward.</span></span> <span data-ttu-id="584fc-115">良い例は品目エンティティです。</span><span class="sxs-lookup"><span data-stu-id="584fc-115">A good example is the Item entity.</span></span> <span data-ttu-id="584fc-116">品目エンティティを構成する異なるテーブルは 10 以上あるため、エンティティ クラスを作成するのは困難です。</span><span class="sxs-lookup"><span data-stu-id="584fc-116">Because more than ten different tables make up the Item entity, it's hard to create the entity class.</span></span> <span data-ttu-id="584fc-117">テスト ケースでは既存の品目を更新する必要がほとんどないため、作成者クラスがあれば問題ありません。その実装ははるかに簡単です。</span><span class="sxs-lookup"><span data-stu-id="584fc-117">Because you will almost never have to update existing items in your test cases, it's OK if you just have a creator class, which is much easier to implement.</span></span>

## <a name="does-the-order-of-the-chained-fluent-setters-matter"></a><span data-ttu-id="584fc-118">連鎖 Fluent セッターの順番は重要か</span><span class="sxs-lookup"><span data-stu-id="584fc-118">Does the order of the chained fluent setters matter?</span></span>

<span data-ttu-id="584fc-119">ほとんどの場合、連鎖 Fluent セッターの順番は問題になりません。</span><span class="sxs-lookup"><span data-stu-id="584fc-119">In most of the cases, the order of the chained fluent setters doesn't matter.</span></span> <span data-ttu-id="584fc-120">ただし、セッター メソッドの呼び出し時に既定値になることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="584fc-120">However, be aware that defaulting occurs at the time of the call to the setter method.</span></span> <span data-ttu-id="584fc-121">したがって、メソッドの順序を変更すると、異なる結果になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="584fc-121">Therefore, a change in the order of the methods can produce different results.</span></span> <span data-ttu-id="584fc-122">これは販売明細行の例です。</span><span class="sxs-lookup"><span data-stu-id="584fc-122">Here is an example for the sales line.</span></span>

### <a name="option-1"></a><span data-ttu-id="584fc-123">オプション 1</span><span class="sxs-lookup"><span data-stu-id="584fc-123">Option 1</span></span>

```
salesLine.setQuantity(10).setUnitPrice(100).setAmount(2000).save()
```

<span data-ttu-id="584fc-124">このオプションにより金額 == 2,000 の販売明細行が生成されます。これは金額が最後に設定されるためです。</span><span class="sxs-lookup"><span data-stu-id="584fc-124">This option produces a sales line where the amount == 2,000, because the amount is set last.</span></span>
    
### <a name="option-2"></a><span data-ttu-id="584fc-125">オプション 2</span><span class="sxs-lookup"><span data-stu-id="584fc-125">Option 2</span></span>

```
salesLine.setAmount(2000).setQuantity(10).setUnitPrice(100).save()
```

<span data-ttu-id="584fc-126">このオプションは 金額 == 1,000 の販売明細行を生成します。これは単価を設定した後、既定で金額は数量 × 価格に設定されるためです。</span><span class="sxs-lookup"><span data-stu-id="584fc-126">This option produces a sales line where the amount == 1,000, because after you set the unit price, the amount is set to quantity × price by default.</span></span>

## <a name="can-i-use-atl-for-tests-that-run-on-the-empty-data-set"></a><span data-ttu-id="584fc-127">空のデータセットで実行するテストに ATL を使用できるか</span><span class="sxs-lookup"><span data-stu-id="584fc-127">Can I use ATL for tests that run on the empty data set?</span></span>

<span data-ttu-id="584fc-128">承認テスト ライブラリ (ATL) は空のデータ セットで問題なく使用できます。</span><span class="sxs-lookup"><span data-stu-id="584fc-128">The Acceptance test library (ATL) can be used on the empty data set without issues.</span></span> <span data-ttu-id="584fc-129">前提条件の自動設定は必要に応じて行われます。</span><span class="sxs-lookup"><span data-stu-id="584fc-129">The automatic setup of prerequisites is done on demand.</span></span> <span data-ttu-id="584fc-130">たとえば、請求書の転記に対する前提条件は、`salesOrder.postInvoice()` への最初の呼び出し時にのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="584fc-130">For example, prerequisites for invoice posting will be set up only during the first call to `salesOrder.postInvoice()`.</span></span> <span data-ttu-id="584fc-131">詳細については [確認](test-data-methods.md#ensure-methods) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="584fc-131">For more information, see [Ensure](test-data-methods.md#ensure-methods).</span></span>

<span data-ttu-id="584fc-132">テスト クラス内のひとつ以上のテストで請求書を転記する必要がある場合は、`setUpTestCase` メソッドで `Ensure` メソッドを呼び出してパフォーマンスを向上させることもできます。</span><span class="sxs-lookup"><span data-stu-id="584fc-132">`Ensure` methods can also be called in the `setUpTestCase` method to improve performance if more than one test in your test class must post invoices.</span></span>

## <a name="can-i-use-atl-for-unit-tests"></a><span data-ttu-id="584fc-133">単体テストで ATL を使用できるか</span><span class="sxs-lookup"><span data-stu-id="584fc-133">Can I use ATL for unit tests?</span></span>

<span data-ttu-id="584fc-134">ATL は主に統合やコンポーネント テストにおけるデータの設定と検証に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="584fc-134">ATL should be used mostly for data setup and validation in integration and component tests.</span></span> <span data-ttu-id="584fc-135">ただし、場合によっては、単体テストにも使用します。</span><span class="sxs-lookup"><span data-stu-id="584fc-135">However, in some cases, it's also used for unit tests.</span></span>

### <a name="why-should-i-be-cautious-about-using-atl-in-unit-and-component-tests"></a><span data-ttu-id="584fc-136">単体テストおよびコンポーネント テストで ATL を使用することに注意が必要な理由</span><span class="sxs-lookup"><span data-stu-id="584fc-136">Why should I be cautious about using ATL in unit and component tests?</span></span>

<span data-ttu-id="584fc-137">販売注文など、より複雑なエンティティでは `modifiedField`、`insert`、`update` の各イベントに関連付けられたすべてのビジネス ロジックが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="584fc-137">In some of the more complex entities, such as Sales order, all the business logic that is associated with the `modifiedField`, `insert`, and `update` events is called.</span></span> <span data-ttu-id="584fc-138">たとえば、請求書トランザクションの作成は、実際の請求書転記ロジックの実行によっても行われます。</span><span class="sxs-lookup"><span data-stu-id="584fc-138">Creation of invoice transactions, for example, is also done by running real invoice posting logic.</span></span> <span data-ttu-id="584fc-139">したがって、いくつかの操作でパフォーマンスが遅くなります。</span><span class="sxs-lookup"><span data-stu-id="584fc-139">Therefore, the performance of some operations will be slow.</span></span> <span data-ttu-id="584fc-140">ただし、これらの問題はマスター データを表すほとんどのエンティティで発生しません。</span><span class="sxs-lookup"><span data-stu-id="584fc-140">However, these issues don't occur for most of the entities that represent master data.</span></span> <span data-ttu-id="584fc-141">したがって、どんな種類のテストでもそれらのエンティティを使える必要があります。</span><span class="sxs-lookup"><span data-stu-id="584fc-141">Therefore, you should be able to use those entities in any type of test.</span></span>

<span data-ttu-id="584fc-142">詳細とクエリを使用して検証を行う場合、重大なオーバーヘッドは発生しません。</span><span class="sxs-lookup"><span data-stu-id="584fc-142">There should not be significant overhead if specifications and queries are used to do validation.</span></span> <span data-ttu-id="584fc-143">これらのコンポーネントは単体テストでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="584fc-143">These artifacts can also be used in unit tests.</span></span>