---
title: 承認テスト ライブラリのエンティティ
description: このトピックでは、データと関連する動作を表すテスト エンティティ クラスについて説明します。
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
ms.openlocfilehash: 22c7d24d85b28be1ad10787b89b280bd04e20cb0
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537287"
---
# <a name="entities-in-the-acceptance-test-library"></a><span data-ttu-id="7d439-103">承認テスト ライブラリのエンティティ</span><span class="sxs-lookup"><span data-stu-id="7d439-103">Entities in the Acceptance test library</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7d439-104">テスト エンティティ クラスは、単一の概念として認識されるデータと動作を表します。</span><span class="sxs-lookup"><span data-stu-id="7d439-104">A test entity class represents data and behavior that are perceived as a single concept.</span></span> <span data-ttu-id="7d439-105">テスト エンティティ クラスは **販売注文**、**移動オーダー**、そして **リリースされた製品** のようなページに基づいています。</span><span class="sxs-lookup"><span data-stu-id="7d439-105">Test entity classes are based on pages such as **Sales order**, **Transfer order**, and **Released product**.</span></span> <span data-ttu-id="7d439-106">テスト エンティティ クラスは、テスト シナリオで最も頻繁に使用されるプロパティと、テスト データの設定やシナリオ テストの観点から最も重要な動作を公開します。</span><span class="sxs-lookup"><span data-stu-id="7d439-106">The test entity classes expose the properties that are most often used in test scenarios, and the behavior that is most important from the perspective of test data setup and scenario tests.</span></span>

<span data-ttu-id="7d439-107">承認テスト ライブラリ (ATL) のエンティティには、次のメソッドが **必ず** 必要です:</span><span class="sxs-lookup"><span data-stu-id="7d439-107">An entity in the Acceptance test library (ATL) **must** have the following methods:</span></span>

+ <span data-ttu-id="7d439-108">エンティティのプロパティを取得および設定するために使用されるプロパティ メソッド。</span><span class="sxs-lookup"><span data-stu-id="7d439-108">Property methods that are used to get and set entity properties.</span></span>
+ <span data-ttu-id="7d439-109">エンティティ プロパティを Fluent な方法で設定できるように有効化する Fluent セッター メソッド。</span><span class="sxs-lookup"><span data-stu-id="7d439-109">Fluent setter methods that enable entity properties to be set in a fluent manner.</span></span>
+ <span data-ttu-id="7d439-110">エンティティをデータベースに保存するメソッド。</span><span class="sxs-lookup"><span data-stu-id="7d439-110">A method that saves the entity to the database.</span></span>

<span data-ttu-id="7d439-111">ATL のエンティティは、次のメソッドを持つことが *可能* です:</span><span class="sxs-lookup"><span data-stu-id="7d439-111">An entity in ATL *can* have the following methods:</span></span>

+ <span data-ttu-id="7d439-112">エンティティに関連する事業運営を公開するために使用されるアクション メソッド。</span><span class="sxs-lookup"><span data-stu-id="7d439-112">Action methods that are used to expose business operations that are relevant to the entity.</span></span>
+ <span data-ttu-id="7d439-113">コンポーネントおよび関連エンティティに対してナビゲーションを有効にするのに使用されるクエリ メソッド。</span><span class="sxs-lookup"><span data-stu-id="7d439-113">Query methods that are used to enable navigation to components and related entities.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="7d439-114">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-114">Naming convention</span></span>

`[AtlEntity]<ModuleName><EntityName>`

<span data-ttu-id="7d439-115">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="7d439-115">In this naming convention:</span></span>

+ <span data-ttu-id="7d439-116">`<ModuleName>` はメイン メニューのモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="7d439-116">`<ModuleName>` is based on the names of the modules in main menu.</span></span> <span data-ttu-id="7d439-117">短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-117">You should use a short version or an abbreviation to support brevity of test code.</span></span>
+ <span data-ttu-id="7d439-118">`<EntityName>` はテーブル名の代わりにユーザー インターフェイス (UI) 名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="7d439-118">`<EntityName>` is based on the user interface (UI) names instead of the table names.</span></span> <span data-ttu-id="7d439-119">たとえば、`SalesTable` ではなく `SalesOrder` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d439-119">For example, use `SalesOrder`, not `SalesTable`.</span></span>

<span data-ttu-id="7d439-120">エンティティに 2 つの UI 名がある場合は、短い方の名前を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-120">If an entity has two UI names, it's OK to use the shorter name.</span></span> <span data-ttu-id="7d439-121">たとえば、代替可能な名前であるため `ReleasedProduct` の代わりに `Item` を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-121">For example, you can use `Item` instead of `ReleasedProduct`, because these names are used interchangeably.</span></span>

### <a name="examples"></a><span data-ttu-id="7d439-122">例</span><span class="sxs-lookup"><span data-stu-id="7d439-122">Examples</span></span>

```
AtlEntitySalesOrder

AtlEntityTransferOrderLine
```

## <a name="property-methods"></a><span data-ttu-id="7d439-123">プロパティ メソッド</span><span class="sxs-lookup"><span data-stu-id="7d439-123">Property methods</span></span>

<span data-ttu-id="7d439-124">テスト エンティティの主な目的のひとつは、データを公開することです。</span><span class="sxs-lookup"><span data-stu-id="7d439-124">One of the main purposes of a test entity is to expose data.</span></span> <span data-ttu-id="7d439-125">エンティティのプロパティは `parm` (プロパティ) メソッドを使用して設定または取得できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-125">The properties of the entity can be set or retrieved by using `parm` (property) methods.</span></span>

### <a name="primitive-type-properties"></a><span data-ttu-id="7d439-126">プリミティブ型のプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d439-126">Primitive type properties</span></span>

<span data-ttu-id="7d439-127">プリミティブ型のプロパティを公開するための `parm` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d439-127">Create a `parm` method to expose a primitive type property.</span></span>

#### <a name="example"></a><span data-ttu-id="7d439-128">例</span><span class="sxs-lookup"><span data-stu-id="7d439-128">Example</span></span>

```
public SalesQty parmQuantity(SalesQty _qty = 0)
{
    if (!prmisDefault(_qty))
    { // setter
        salesLine.SalesQty = _qty;
        this.onSalesQtyOrInventDimChange();
    }
    return salesLine.SalesQty;
}
```

### <a name="entity-references"></a><span data-ttu-id="7d439-129">エンティティ参照</span><span class="sxs-lookup"><span data-stu-id="7d439-129">Entity references</span></span>

<span data-ttu-id="7d439-130">たとえば `AtlEntityCustomer` という名前の顧客エンティティがある場合、`AtlEntitySalesOrder` エンティティのプロパティ メソッドとして `customer` への参照を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-130">If there is a customer entity that is named `AtlEntityCustomer`, for example, a reference to `customer` should be exposed as a property method on the `AtlEntitySalesOrder` entity.</span></span>

```
public AtlEntityCustomer parmCustomer(AtlEntityCustomer _custTable = null)
```

<span data-ttu-id="7d439-131">プロパティ メソッドをセッターやゲッターとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-131">The property method can be used as either a setter or a getter.</span></span>

```
salesOrder.parmCustomer(customer); // setter

customer = salesOrder.parmCustomer(); // getter
```

#### <a name="entity-reference-methods-naming-conventions"></a><span data-ttu-id="7d439-132">エンティティ参照メソッドの命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-132">Entity reference methods naming conventions</span></span>

<span data-ttu-id="7d439-133">プロパティ メソッドを識別するために `parm` プレフィックスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-133">The `parm` prefix should be used to identify property methods.</span></span> <span data-ttu-id="7d439-134">エンティティ参照プロパティを公開するときは、アプリケーション オブジェクト ツリー (AOT) 名の代わりにフィールドの UI 名を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d439-134">When you expose an entity reference property, use the UI name of the field instead of the Application Object Tree (AOT) name.</span></span> <span data-ttu-id="7d439-135">UI 名に `Id`、`Code`、または `Number` 接尾語が含まれている場合は、その接尾語を省略します。</span><span class="sxs-lookup"><span data-stu-id="7d439-135">If the UI name includes the `Id`, `Code`, or `Number` suffix, omit the suffix.</span></span> <span data-ttu-id="7d439-136">たとえば、`parmItemNumber` の代わりに `parmItem` を使用します。</span><span class="sxs-lookup"><span data-stu-id="7d439-136">For example, use `parmItem` instead of `parmItemNumber`.</span></span>

### <a name="record-references"></a><span data-ttu-id="7d439-137">レコード参照</span><span class="sxs-lookup"><span data-stu-id="7d439-137">Record references</span></span>

<span data-ttu-id="7d439-138">顧客エンティティがまだ作成されておらず、近い将来にも作成されない場合、参照プロパティは対応するレコード バッファ (`CustTable`) を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-138">If the customer entity hasn't yet been created and won't be created in the near future, the reference property should expose the corresponding record buffer (`CustTable`).</span></span>

```
public CustTable parmCustomer(CustTable _custTable = null)
```

#### <a name="record-reference-naming-conventions"></a><span data-ttu-id="7d439-139">レコード参照の命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-139">Record reference naming conventions</span></span>

<span data-ttu-id="7d439-140">エンティティ参照に使用されているのと同じ命名規則を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7d439-140">Use the same naming conventions that are used for entity references.</span></span>

### <a name="id-references"></a><span data-ttu-id="7d439-141">ID 参照</span><span class="sxs-lookup"><span data-stu-id="7d439-141">Id references</span></span>

<span data-ttu-id="7d439-142">エンティティやレコード参照を持つことに加えて、`Id` 参照プロパティを導入できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-142">In addition to having an entity or record reference, you can introduce the `Id` reference property.</span></span>

```
public CustAccount customerId(CustAccount _custTable = null)
```

<span data-ttu-id="7d439-143">対応するエンティティまたはバッファー参照も導入しない限り、`Id` 参照を導入しないでください。</span><span class="sxs-lookup"><span data-stu-id="7d439-143">Don't introduce `Id` references unless you also introduce corresponding entity or buffer references.</span></span> <span data-ttu-id="7d439-144">`Id` 参照は、エンティティやバッファー参照メソッドへのショートカットです。</span><span class="sxs-lookup"><span data-stu-id="7d439-144">`Id` references are shortcuts to the entity or buffer reference methods.</span></span> <span data-ttu-id="7d439-145">`Id` 参照の実装は、エンティティやバッファー参照に呼び出しを委任する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-145">The implementation of `Id` references should delegate the call to the entity or buffer reference.</span></span>

#### <a name="id-reference-naming-conventions"></a><span data-ttu-id="7d439-146">ID 参照の命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-146">Id reference naming conventions</span></span>

<span data-ttu-id="7d439-147">`Id`、`Number`、`Account`、`Code`、また `Name` などの語句が含まれる場合は UI 名を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7d439-147">Use the UI name if it includes terms such as `Id`, `Number`, `Account`, `Code`, or `Name`.</span></span> <span data-ttu-id="7d439-148">それ以外の場合、エンティティやレコード参照の名前に適切な接尾語を追加します。</span><span class="sxs-lookup"><span data-stu-id="7d439-148">Otherwise, add an appropriate suffix to the name of the entity or record reference.</span></span>

#### <a name="id-reference-methods-contract"></a><span data-ttu-id="7d439-149">ID 参照メソッドの契約</span><span class="sxs-lookup"><span data-stu-id="7d439-149">Id reference methods contract</span></span>

<span data-ttu-id="7d439-150">`Id` 参照メソッドは参照エンティティを見つけるために常に提供された `Id` を使用し、そしてエンティティやレコード参照メソッドに呼び出しを委任します。</span><span class="sxs-lookup"><span data-stu-id="7d439-150">The `Id` reference method always uses the provided `Id` to find the referenced entity, and it delegates the call to the entity or record reference method.</span></span> <span data-ttu-id="7d439-151">指定された `Id` 値に基づいてエンティティやレコードが見つからない場合は、エラー メッセージがスローされます。</span><span class="sxs-lookup"><span data-stu-id="7d439-151">If no entity or record is found based on the specified `Id` value, an error message is thrown.</span></span>

## <a name="fluent-setter-methods"></a><span data-ttu-id="7d439-152">Fluent セッター メソッド</span><span class="sxs-lookup"><span data-stu-id="7d439-152">Fluent setter methods</span></span>

<span data-ttu-id="7d439-153">Fluent な初期化とエンティティの変更をサポートする Fluent なセッター メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d439-153">Create fluent setter methods to support the fluent initialization and modification of entities.</span></span>

### <a name="declaration-example"></a><span data-ttu-id="7d439-154">宣言の例</span><span class="sxs-lookup"><span data-stu-id="7d439-154">Declaration example</span></span>

```
public AtlEntitySalesLine setQty(SalesQty _qty)
```
    
### <a name="code-example"></a><span data-ttu-id="7d439-155">コードの例</span><span class="sxs-lookup"><span data-stu-id="7d439-155">Code example</span></span>

```
salesLine.setItem(batchItem).setInventDims([warehouse]).setQty(10).save();
```

### <a name="naming-convention"></a><span data-ttu-id="7d439-156">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-156">Naming convention</span></span>

`set<PropertyName>`

<span data-ttu-id="7d439-157">この命名規則では `<PropertyName>` が対応するプロパティ メソッドの名前で使用されているものと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-157">In this naming convention, `<PropertyName>` should match what is used in the name of the corresponding property method.</span></span>

## <a name="action-methods"></a><span data-ttu-id="7d439-158">アクション メソッド</span><span class="sxs-lookup"><span data-stu-id="7d439-158">Action methods</span></span>

<span data-ttu-id="7d439-159">エンティティはデータだけでなく関連するアクションも表します。</span><span class="sxs-lookup"><span data-stu-id="7d439-159">Entities represent not only data but also relevant actions.</span></span> <span data-ttu-id="7d439-160">アクションは単純なアクション メソッドとしても、コマンド オブジェクト初期化子としても実装できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-160">Actions can be implemented either as a simple action method or as a command object initializer.</span></span>

### <a name="simple-action-methods"></a><span data-ttu-id="7d439-161">単純なアクション メソッド</span><span class="sxs-lookup"><span data-stu-id="7d439-161">Simple action methods</span></span>

<span data-ttu-id="7d439-162">単純なアクション メソッドは、完全なアクションを表します。</span><span class="sxs-lookup"><span data-stu-id="7d439-162">Simple action methods represent a complete action.</span></span> <span data-ttu-id="7d439-163">これらを Fluent に連鎖してはいけません。</span><span class="sxs-lookup"><span data-stu-id="7d439-163">They should not be fluently chained.</span></span> <span data-ttu-id="7d439-164">例外は `save` メソッドで、Fluent である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-164">The exception is the `save` method, which should be fluent.</span></span>

#### <a name="naming-convention"></a><span data-ttu-id="7d439-165">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-165">Naming convention</span></span>

`<ExecuteBusinessOperation>`

<span data-ttu-id="7d439-166">この命名規則では `<ExecuteBusinessOperation>` は事業運営を表す動詞です。</span><span class="sxs-lookup"><span data-stu-id="7d439-166">In this naming convention, `<ExecuteBusinessOperation>` is a verb that represents the business operation.</span></span> <span data-ttu-id="7d439-167">それは UI のメニュー項目で使用されているのと同じ用語である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-167">It should be the same term that is used on the menu item in the UI.</span></span>

#### <a name="examples"></a><span data-ttu-id="7d439-168">例</span><span class="sxs-lookup"><span data-stu-id="7d439-168">Examples</span></span>

```
salesOrder.save();

salesOrder.postInvoice();
```

### <a name="command-object-initializers"></a><span data-ttu-id="7d439-169">コマンド オブジェクト初期化子</span><span class="sxs-lookup"><span data-stu-id="7d439-169">Command object initializers</span></span>

<span data-ttu-id="7d439-170">コマンド オブジェクト初期化子は、コマンドのパラメーターを指定し実行できるコマンド オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7d439-170">Command object initializers return a command object that lets you specify parameters of the command and run it.</span></span>

```
transferLine.pick().setQty(10).setWMSLocation(bulkLocation).execute();
```

#### <a name="naming-convention"></a><span data-ttu-id="7d439-171">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-171">Naming convention</span></span>

`<ExecuteBusinessOperation>`

<span data-ttu-id="7d439-172">この命名規則では `<ExecuteBusinessOperation>` は事業運営を表す動詞です。</span><span class="sxs-lookup"><span data-stu-id="7d439-172">In this naming convention, `<ExecuteBusinessOperation>` is a verb that represents the business operation.</span></span> <span data-ttu-id="7d439-173">それは UI のメニュー項目で使用されているのと同じ用語である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-173">It should be the same term that is used on the menu item in the UI.</span></span>

#### <a name="examples"></a><span data-ttu-id="7d439-174">例</span><span class="sxs-lookup"><span data-stu-id="7d439-174">Examples</span></span>

```
salesOrder.pick().execute();

purchaseOrder.register().execute();
```

### <a name="action-entities"></a><span data-ttu-id="7d439-175">アクション エンティティ</span><span class="sxs-lookup"><span data-stu-id="7d439-175">Action entities</span></span>

<span data-ttu-id="7d439-176">エンティティで利用可能ないくつかのアクションは、エンティティそのものと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="7d439-176">Some actions that are available for an entity can be considered entities themselves.</span></span> <span data-ttu-id="7d439-177">仕入先の請求書がひとつの例です。</span><span class="sxs-lookup"><span data-stu-id="7d439-177">Vendor invoices are one example.</span></span> <span data-ttu-id="7d439-178">請求書を転記する前に、請求書のパラメータを設定し、行を編集して、後のために請求書を保存することができます。</span><span class="sxs-lookup"><span data-stu-id="7d439-178">Before you post an invoice, you might want to set up parameters of the invoice, edit lines, and save the invoice for later.</span></span> <span data-ttu-id="7d439-179">これらのコマンドは、個別のエンティティ クラスを導入できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-179">For these commands, you can introduce a separate entity class.</span></span>

#### <a name="naming-convention"></a><span data-ttu-id="7d439-180">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-180">Naming convention</span></span>

`new<ActionName>`

<span data-ttu-id="7d439-181">この命名規則では `<ActionName>` は事業運営を表す名詞です。</span><span class="sxs-lookup"><span data-stu-id="7d439-181">In this naming convention, `<ActionName>` is a noun that represents the business operation.</span></span> <span data-ttu-id="7d439-182">名前は事業運営の UI 名にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-182">The name should be the UI name of the business operation.</span></span>

#### <a name="example"></a><span data-ttu-id="7d439-183">例</span><span class="sxs-lookup"><span data-stu-id="7d439-183">Example</span></span>

```
receipt = transfer.newReceipt().setEditLines(true).setExplodeLines(true);
receipt.lines().withBatch(batch1).single().setReceiptQty(6).setScrapQty(1).save();
receipt.lines().withBatch(batch2).single().setReceiptQty(4).setScrapQty(1).save();
receipt.post();
```

#### <a name="class-naming-convention"></a><span data-ttu-id="7d439-184">クラスの命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-184">Class naming convention</span></span>

`AtlEntity<ModuleName><EntityName><ActionName>`

#### <a name="example"></a><span data-ttu-id="7d439-185">例</span><span class="sxs-lookup"><span data-stu-id="7d439-185">Example</span></span>

```
AtlEntityInventTransferOrderReceipt
```

## <a name="adding-components"></a><span data-ttu-id="7d439-186">コンポーネントの追加</span><span class="sxs-lookup"><span data-stu-id="7d439-186">Adding components</span></span>

<span data-ttu-id="7d439-187">コンポジションは複合エンティティがコンポーネント パーツの配置に対して唯一の責任を持つ関係です。</span><span class="sxs-lookup"><span data-stu-id="7d439-187">Composition is a relationship where the composite entity has sole responsibility for the disposition of the component parts.</span></span> <span data-ttu-id="7d439-188">複合オブジェクトがコンポーネントの所有権を持っているため、複合とコンポーネントの関係は強い "持っている" の関係です。</span><span class="sxs-lookup"><span data-stu-id="7d439-188">The relationship between the composite and the component is a strong "has a" relationship, because the composite object takes ownership of the component.</span></span> <span data-ttu-id="7d439-189">したがって、複合はコンポーネント パーツの作成と破棄を担当します。</span><span class="sxs-lookup"><span data-stu-id="7d439-189">Therefore, the composite is responsible for creating and destroying the component parts.</span></span>

<span data-ttu-id="7d439-190">オブジェクト インスタンスのひとつを、ひとつの複合の一部にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7d439-190">An object instance can be part of only one composite.</span></span> <span data-ttu-id="7d439-191">複合オブジェクトが破棄された場合は、すべてのコンポーネント パーツを破棄する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-191">If the composite object is destroyed, all the component parts must be destroyed.</span></span> <span data-ttu-id="7d439-192">コンポーネント パーツは複合オブジェクトの外部に独立した存在を持たず、他のオブジェクトに転送することはできません。</span><span class="sxs-lookup"><span data-stu-id="7d439-192">The component parts have no independent existence outside the composite object, and they can't be transferred to another object.</span></span> <span data-ttu-id="7d439-193">コンポーネント パーツは通常は複合オブジェクトのメンバーであるため、合成はカプセル化を強制します。</span><span class="sxs-lookup"><span data-stu-id="7d439-193">Composition enforces encapsulation, because the component parts are usually members of the composite object.</span></span>

<span data-ttu-id="7d439-194">複合オブジェクトの例は、元伝票行で構成されている元伝票です。</span><span class="sxs-lookup"><span data-stu-id="7d439-194">An example of a composite object is a source document that is made up of source document lines.</span></span>

### <a name="example"></a><span data-ttu-id="7d439-195">例</span><span class="sxs-lookup"><span data-stu-id="7d439-195">Example</span></span>

<span data-ttu-id="7d439-196">元伝票の例では、ドキュメント エンティティは複合ルートとして機能し、ドキュメント行の新しいインスタンスの作成に責任があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-196">In the source document example, the document entity serves as the composition root and is responsible for creating any new instances of document lines.</span></span> <span data-ttu-id="7d439-197">この場合、元伝票エンティティはドキュメントの新しい行を初期化して返す `addLine()` メソッドを持ちます。</span><span class="sxs-lookup"><span data-stu-id="7d439-197">In this case, the source document entity will have an `addLine()` method that initializes and returns a new line for the document.</span></span>


```
public AtlEntitySalesLine addLine()
```

<span data-ttu-id="7d439-198">`addLine()` メソッドは、行オブジェクト (この例では `salesLine`) を行のコレクションに追加して、アプリケーション プログラミング インターフェイス (API) の Fluent を維持するために親エンティティ (この例では `SalesOrder`) を返します。</span><span class="sxs-lookup"><span data-stu-id="7d439-198">The `addLine()` method adds the line object (`salesLine` in this example) to a collection of lines and returns the parent entity (`SalesOrder` in this example) to preserve the fluency of application programming interfaces (APIs).</span></span> <span data-ttu-id="7d439-199">新しい行を作成するには、`newLine()` メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="7d439-199">To create a new line, create a `newLine()` method.</span></span>

### <a name="naming-convention-for-adding-components"></a><span data-ttu-id="7d439-200">コンポーネント追加の命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-200">Naming convention for adding components</span></span>

<span data-ttu-id="7d439-201">コンポーネントを追加するメソッドは、ボタンの UI 名を使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-201">Methods for adding components should use the UI names of the buttons.</span></span>

#### <a name="example"></a><span data-ttu-id="7d439-202">例</span><span class="sxs-lookup"><span data-stu-id="7d439-202">Example</span></span>

```
salesLine = salesOrder.addLine();
```

### <a name="component-collections"></a><span data-ttu-id="7d439-203">コンポーネント コレクション</span><span class="sxs-lookup"><span data-stu-id="7d439-203">Component collections</span></span>

<span data-ttu-id="7d439-204">クエリ メソッドを使用してコンポーネントを検索できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-204">You can search for components by using query methods.</span></span>

#### <a name="naming-convention-for-component-collections"></a><span data-ttu-id="7d439-205">コンポーネント コレクションの命名規則</span><span class="sxs-lookup"><span data-stu-id="7d439-205">Naming convention for component collections</span></span>

<span data-ttu-id="7d439-206">コンポーネント コレクションにアクセスするメソッドは、ホスティング ページのグリッドの UI 名を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d439-206">Methods for accessing component collections should use the UI names of the grid on the hosting page.</span></span>

## <a name="query-methods"></a><span data-ttu-id="7d439-207">クエリ メソッド</span><span class="sxs-lookup"><span data-stu-id="7d439-207">Query methods</span></span>

<span data-ttu-id="7d439-208">エンティティのクエリ メソッドを使用して、コンポーネントと関連エンティティを検索できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-208">Query methods on an entity let you search for components and related entities.</span></span>

### <a name="example"></a><span data-ttu-id="7d439-209">例</span><span class="sxs-lookup"><span data-stu-id="7d439-209">Example</span></span>

```
transferOrderLine = transferOrder.lines().withItem(item).single();
```

<span data-ttu-id="7d439-210">この例では、`lines()` は `AtlQueryTransferOrderLines` クエリを返すクエリ メソッドです。</span><span class="sxs-lookup"><span data-stu-id="7d439-210">In this example, `lines()` is a query method that returns the `AtlQueryTransferOrderLines` query.</span></span> <span data-ttu-id="7d439-211">このクエリは既にフィルターされてるため、`lines()` メソッドが呼び出された移動オーダーの移動オーダー行のみを返します。</span><span class="sxs-lookup"><span data-stu-id="7d439-211">This query is already filtered so that it returns only transfer order lines for the transfer order that the `lines()` method was called on.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="7d439-212">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="7d439-212">Naming convention</span></span>

<span data-ttu-id="7d439-213">可能な限り UI 名を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7d439-213">Use the UI names whenever you can.</span></span> <span data-ttu-id="7d439-214">UI 名がテスト自動化に使用するのに長すぎる場合は、省略形を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d439-214">Abbreviations are acceptable if the UI name is too long to be used in test automation.</span></span>

### <a name="example"></a><span data-ttu-id="7d439-215">例</span><span class="sxs-lookup"><span data-stu-id="7d439-215">Example</span></span>

```
public AtlQueryWHSLoadLines lines()
{
    return new AtlQueryWHSLoadLines().forLoadId(this.parmLoadId());
}
```

## <a name="additional-resources"></a><span data-ttu-id="7d439-216">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7d439-216">Additional resources</span></span>

[<span data-ttu-id="7d439-217">承認テスト ライブラリのクエリ</span><span class="sxs-lookup"><span data-stu-id="7d439-217">Queries in the Acceptance test library</span></span>](concepts-queries.md)
