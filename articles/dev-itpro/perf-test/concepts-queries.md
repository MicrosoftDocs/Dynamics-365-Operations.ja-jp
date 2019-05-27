---
title: 承認テスト ライブラリのクエリ
description: このトピックでは承認テスト ライブラリでのクエリの使用法に関する情報を提供します。
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
ms.openlocfilehash: 71f5017221b908621cb82bb4865914532d50eee9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506197"
---
# <a name="queries-in-the-acceptance-test-library"></a><span data-ttu-id="40060-103">承認テスト ライブラリのクエリ</span><span class="sxs-lookup"><span data-stu-id="40060-103">Queries in the Acceptance test library</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="40060-104">クエリ クラスはさまざまな条件に基づいて対応するエンティティのインスタンスを見つけるために使用する Fluent アプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="40060-104">A query class provides fluent application programming interfaces (APIs) that are used to find an instance of the corresponding entity, based on various criteria.</span></span> <span data-ttu-id="40060-105">クエリ クラスは検証シナリオでよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="40060-105">Query classes are often used in validation scenarios.</span></span> <span data-ttu-id="40060-106">通常それらは詳細と一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="40060-106">They are usually used together with specifications.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="40060-107">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="40060-107">Naming convention</span></span>

`AtlQuery<ModuleName><EntityNamePlural>`

<span data-ttu-id="40060-108">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="40060-108">In this naming convention:</span></span>

- <span data-ttu-id="40060-109">`<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="40060-109">`<ModuleName>` is optional and is based on the names of the modules on the main menu.</span></span> <span data-ttu-id="40060-110">ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40060-110">However, a short version or an abbreviation should be used to support brevity of test code.</span></span>
- <span data-ttu-id="40060-111">`<EntityNamePlural>` はエンティティ名の複数形です。</span><span class="sxs-lookup"><span data-stu-id="40060-111">`<EntityNamePlural>` is the plural version of the entity name.</span></span>

## <a name="examples"></a><span data-ttu-id="40060-112">例</span><span class="sxs-lookup"><span data-stu-id="40060-112">Examples</span></span>

```
AtlQueryWHSLoadLines

AtlQueryInventTransferOrderLines
```

## <a name="implementation"></a><span data-ttu-id="40060-113">実装</span><span class="sxs-lookup"><span data-stu-id="40060-113">Implementation</span></span>

<span data-ttu-id="40060-114">クエリ クラスは、すべてのクエリに共通の `AtlQuery` クラスから継承します。</span><span class="sxs-lookup"><span data-stu-id="40060-114">Query classes inherit from the `AtlQuery` class that is common to all queries.</span></span>

## <a name="fluent-setters"></a><span data-ttu-id="40060-115">Fluent セッター</span><span class="sxs-lookup"><span data-stu-id="40060-115">Fluent setters</span></span>

<span data-ttu-id="40060-116">クエリ クラスは、クエリの範囲を指定するために Fluent セッター メソッドを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40060-116">Query classes should provide fluent setter methods to specify ranges for the query.</span></span>

### <a name="example"></a><span data-ttu-id="40060-117">例</span><span class="sxs-lookup"><span data-stu-id="40060-117">Example</span></span>

```
loadLine = data.whs().loadLines().query().forSalesOrder(salesOrder).single();
```

<span data-ttu-id="40060-118">クエリは 2 種類の Fluent セッター メソッドを許可します、`for` メソッドと `with` メソッド:</span><span class="sxs-lookup"><span data-stu-id="40060-118">Queries allow for two types of fluent setter methods, `for` methods and `with` methods:</span></span>

- <span data-ttu-id="40060-119">**for** – これらのメソッドは構成または集計関係の親として機能するクエリのフィルターに使用されます。</span><span class="sxs-lookup"><span data-stu-id="40060-119">**for** – These methods are used for filters of the query that act as parents of composition or aggregation relationships.</span></span> <span data-ttu-id="40060-120">たとえば、販売明細行クエリは、特定の販売注文に対して販売明細行をフィルターする `for` メソッドを公開しています。</span><span class="sxs-lookup"><span data-stu-id="40060-120">For example, the sales lines query exposes a `for` method to filter sales lines for a specific sales order.</span></span>
- <span data-ttu-id="40060-121">**with** – これらのメソッドはクエリの他のすべての範囲で使用されます。</span><span class="sxs-lookup"><span data-stu-id="40060-121">**with** – These methods are used for all other ranges of the query.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="40060-122">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="40060-122">Naming convention</span></span>

`for<QueryRangeName>`

`with<QueryRangeName>`

<span data-ttu-id="40060-123">この命名規則では、`<QueryRangeName>` はその範囲が適用されるフィールド名です。</span><span class="sxs-lookup"><span data-stu-id="40060-123">In this naming convention, `<QueryRangeName>` is the name of the field that the range is applied on.</span></span>

### <a name="examples"></a><span data-ttu-id="40060-124">例</span><span class="sxs-lookup"><span data-stu-id="40060-124">Examples</span></span>

```
loadLine = data.whs().loadLines().query().forLoad(load).withInventQty(10).single();

transferLine = data.invent().transferOrderLines().query().forTransferOrder(transferOrder).withInventDims([batch1]).single();
```
