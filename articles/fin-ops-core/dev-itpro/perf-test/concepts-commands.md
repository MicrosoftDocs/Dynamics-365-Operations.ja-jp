---
title: 承認テスト ライブラリのコマンド
description: このトピックでは承認テスト ライブラリとコマンドの使用法に関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 06de21bb2a8f842c3fcd397a5c834766e5a91ed5
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866210"
---
# <a name="acceptance-test-library-commands"></a><span data-ttu-id="7fbd2-103">承認テスト ライブラリのコマンド</span><span class="sxs-lookup"><span data-stu-id="7fbd2-103">Acceptance test library commands</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fbd2-104">コマンド クラスは事業運営の実行を処理します。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-104">Command classes are responsible for running business operations.</span></span> <span data-ttu-id="7fbd2-105">Fluent アプリケーション プログラミング インターフェイス (API) を使用して、これらの操作のパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-105">They let you use fluent application programming interfaces (APIs) to set the parameters of these operations.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="7fbd2-106">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7fbd2-106">Naming convention</span></span>

`AtlCommand<ModuleName><EntityName><ExecuteBusinessOperation>`

<span data-ttu-id="7fbd2-107">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="7fbd2-107">In this naming convention:</span></span>

+ <span data-ttu-id="7fbd2-108">`<ModuleName>` はメイン メニュー上のモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-108">`<ModuleName>` is based on the names of the modules on the main menu.</span></span> <span data-ttu-id="7fbd2-109">短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-109">You should use a short version or an abbreviation to support brevity of test code.</span></span>
+ <span data-ttu-id="7fbd2-110">`<EntityName>` はオプションであり、コマンドが異なる種類のエンティティに適用される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-110">`<EntityName>` is optional and is used when the command applies to different types of entities.</span></span>
+ <span data-ttu-id="7fbd2-111">`<ExecuteBusinessOperation>` は事業運営の名前を表す動詞です。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-111">`<ExecuteBusinessOperation>` is a verb that represents the name of the business operation.</span></span>

## <a name="examples"></a><span data-ttu-id="7fbd2-112">例</span><span class="sxs-lookup"><span data-stu-id="7fbd2-112">Examples</span></span>

```xpp
AtlCommandInventMark

AtlCommandSalesReturnOrderLineRegister
```

## <a name="implementation"></a><span data-ttu-id="7fbd2-113">実装</span><span class="sxs-lookup"><span data-stu-id="7fbd2-113">Implementation</span></span>

<span data-ttu-id="7fbd2-114">返されるコマンド オブジェクトは、`AtlICommand` インターフェイスを実装し `AtlCommand` クラスから継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-114">Command objects that are returned should implement the `AtlICommand` interface and should inherit from the `AtlCommand` class.</span></span>

<span data-ttu-id="7fbd2-115">コマンド オブジェクトは、コマンドのパラメータの設定に使用する Fluent セッター メソッドを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-115">Command objects should provide fluent setter methods that are used to set the parameters of the command.</span></span>

### <a name="example"></a><span data-ttu-id="7fbd2-116">例</span><span class="sxs-lookup"><span data-stu-id="7fbd2-116">Example</span></span>

```xpp
salesLine.pick().setInventDims([locationOut]).setQty(pickedQty).execute();
```

## <a name="fluent-setter-methods"></a><span data-ttu-id="7fbd2-117">Fluent セッター メソッド</span><span class="sxs-lookup"><span data-stu-id="7fbd2-117">Fluent setter methods</span></span>

<span data-ttu-id="7fbd2-118">コマンドは 2 種類の Fluent セッター メソッドを許可します、`for` メソッドと `set` メソッド:</span><span class="sxs-lookup"><span data-stu-id="7fbd2-118">Commands allow for two types of fluent setter methods, `for` methods and `set` methods:</span></span>

+ <span data-ttu-id="7fbd2-119">**for** – これらのメソッドはコマンドが適用されるエンティティを表すコマンド パラメータに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-119">**for** – These methods are used for command parameters that represent the entities that the command applies to.</span></span>

    <span data-ttu-id="7fbd2-120">たとえば、請求書コマンドは販売注文に適用できます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-120">For example, the invoice command can apply to sales orders.</span></span> <span data-ttu-id="7fbd2-121">したがって、`for` メソッドは請求書コマンドが適用される販売注文の設定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-121">Therefore, a `for` method is used to set the sales order that the invoice command applies to.</span></span>

+ <span data-ttu-id="7fbd2-122">**set** – これらのメソッドはコマンドの他のすべてのパラメータに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-122">**set** – These methods are used for all other parameters of the command.</span></span> 

    <span data-ttu-id="7fbd2-123">たとえば、販売明細行を予約するときに通常は数量を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-123">For example, when you reserve a sales line, you usually specify a quantity.</span></span> <span data-ttu-id="7fbd2-124">数量はコマンドが適用されるものではありませんが、コマンドの単純なパラメータです。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-124">The quantity isn't something that the command applies to but is instead a simple parameter of the command.</span></span> <span data-ttu-id="7fbd2-125">したがって、`set` メソッドは予約コマンドの数量パラメータの指定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-125">Therefore, a `set` method is used to specify the quantity parameter of the reservation command.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="7fbd2-126">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7fbd2-126">Naming convention</span></span>

`for<CommandParameterName>`

`set<CommandParameterName>`

<span data-ttu-id="7fbd2-127">この命名規則では、`<CommandParameterName>` は Fluent メソッドを使用してコマンドに設定されるパラメーター名です。</span><span class="sxs-lookup"><span data-stu-id="7fbd2-127">In this naming convention, `<CommandParameterName>` is the name of the parameter that is being set for the command by using the fluent method.</span></span>

### <a name="examples"></a><span data-ttu-id="7fbd2-128">例</span><span class="sxs-lookup"><span data-stu-id="7fbd2-128">Examples</span></span>

```xpp
onHandAdjustment.forItem(item).setQuantity(10).execute();
    
picking.forSalesLine(salesLine).setInventDims([warehouse, batch1]).setQuantity(10).execute();
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]