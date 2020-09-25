---
title: VALUEIN ER 関数
description: このトピックでは、VALUEIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4f88c0d71b6fa6980ee8e180ae5be482a463f1c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744674"
---
# <a name="valuein-er-function"></a><span data-ttu-id="94e1a-103">VALUEIN ER 関数</span><span class="sxs-lookup"><span data-stu-id="94e1a-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94e1a-104">`VALUEIN` 関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="94e1a-105">指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="94e1a-106">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e1a-107">構文</span><span class="sxs-lookup"><span data-stu-id="94e1a-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="94e1a-108">引数</span><span class="sxs-lookup"><span data-stu-id="94e1a-108">Arguments</span></span>

<span data-ttu-id="94e1a-109">`input`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="94e1a-109">`input`: *Field*</span></span>

<span data-ttu-id="94e1a-110">*レコード リスト* タイプのデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="94e1a-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="94e1a-111">この項目の値は一致します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-111">The value of this item will be matched.</span></span>

<span data-ttu-id="94e1a-112">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="94e1a-112">`list`: *Record list*</span></span>

<span data-ttu-id="94e1a-113">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="94e1a-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="94e1a-114">`list item expression`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="94e1a-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="94e1a-115">照合に使用される指定されたリストの単一のフィールドを指し示すか、そのフィールドを含む有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="94e1a-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="94e1a-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="94e1a-116">Return values</span></span>

<span data-ttu-id="94e1a-117">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="94e1a-117">*Boolean*</span></span>

<span data-ttu-id="94e1a-118">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="94e1a-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="94e1a-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="94e1a-119">Usage notes</span></span>

<span data-ttu-id="94e1a-120">一般に、`VALUEIN` 関数は一連の **OR** 条件に変換されます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="94e1a-121">**OR** 条件の一覧が大きく、SQL ステートメントの最大長を超える場合は、[`VALUEINLARGE`](er-functions-logical-valueinlarge.md) 機能を使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="94e1a-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="94e1a-122">場合によっては、`EXISTS JOIN` オペレーターを使用してデータベース SQL ステートメントに変換されます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="94e1a-123">例 1</span><span class="sxs-lookup"><span data-stu-id="94e1a-123">Example 1</span></span>

<span data-ttu-id="94e1a-124">モデル マッピングで、*計算済フィールド* タイプの**リスト** データ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="94e1a-125">このデータ ソースには、式 `SPLIT ("a,b,c", ",")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94e1a-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="94e1a-126">データ ソースが呼び出されると、`VALUEIN ("B", List, List.Value)` 式として構成されている場合は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="94e1a-127">この場合、`VALUEIN` 関数は次の一連の条件に変換されます。`("B" = "b")` が **TRUE** と等しい場合、`(("B" = "a") or ("B" = "b") or ("B" = "c"))`。</span><span class="sxs-lookup"><span data-stu-id="94e1a-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="94e1a-128">データ ソースが呼び出されると、`VALUEIN ("B", List, LEFT(List.Value, 0))` 式として構成されている場合は、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="94e1a-129">この場合、`VALUEIN` 関数は次の一連の条件に変換されます。 **TRUE** と等しくない `("B" = "")`。</span><span class="sxs-lookup"><span data-stu-id="94e1a-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="94e1a-130">このような条件のテキストの文字数の上限は 32,768 文字です。</span><span class="sxs-lookup"><span data-stu-id="94e1a-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="94e1a-131">したがって、実行時に制限を超える可能性があるデータ ソースを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="94e1a-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="94e1a-132">制限を超過した場合は、アプリケーションは実行を停止し、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="94e1a-133">たとえば、この状況は、データ ソースが `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` として構成され、**List1** および **List2** リストに大量のレコードが含まれているときに生じます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="94e1a-134">場合によっては、`VALUEIN` 関数は `EXISTS JOIN` オペレーターを使用することでデータベース ステートメントに変換されます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="94e1a-135">この動作は、[`FILTER`](er-functions-list-filter.md) 関数が使用され、次の条件が満たされているときに発生します:</span><span class="sxs-lookup"><span data-stu-id="94e1a-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="94e1a-136">**ASK FOR QUERY** オプションは、レコードのリストを参照する `VALUEIN` 関数のデータ ソースに対してオフになっています。</span><span class="sxs-lookup"><span data-stu-id="94e1a-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="94e1a-137">このデータ ソースには実行時に適用される追加の条件はありません。</span><span class="sxs-lookup"><span data-stu-id="94e1a-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="94e1a-138">入れ子になった式は、レコードのリストを参照する `VALUEIN` 関数のデータ ソース用に構成されません。</span><span class="sxs-lookup"><span data-stu-id="94e1a-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="94e1a-139">`VALUEIN` 関数のリスト項目は、指定されたデータ ソースの式またメソッドではなく、指定されたデータ ソースのフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="94e1a-140">この例の前半で説明した [`WHERE`](er-functions-list-where.md) 関数の代わりにこのオプションを使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="94e1a-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="94e1a-141">例 2</span><span class="sxs-lookup"><span data-stu-id="94e1a-141">Example 2</span></span>

<span data-ttu-id="94e1a-142">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="94e1a-143">*テーブル レコード* タイプの **In** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="94e1a-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="94e1a-144">このデータ ソースは、イントラスタット テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="94e1a-145">*テーブル レコード* タイプの**ポート** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="94e1a-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="94e1a-146">このデータ ソースは、IntrastatPort テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="94e1a-147">`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` 式として構成されたデータ ソースが呼び出されると、次の SQL ステートメントが生成され、イントラスタット テーブルのフィルターされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="94e1a-148">**dataAreaId** フィールドの場合、`IN` 演算子を使用して最終的な SQL ステートメントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="94e1a-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="94e1a-149">例 3</span><span class="sxs-lookup"><span data-stu-id="94e1a-149">Example 3</span></span>

<span data-ttu-id="94e1a-150">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="94e1a-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="94e1a-151">*計算済フィールド* タイプの **Le** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="94e1a-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="94e1a-152">このデータ ソースには、式 `SPLIT ("DEMF,GBSI,USMF", ",")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94e1a-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="94e1a-153">*テーブル レコード* タイプの **In** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="94e1a-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="94e1a-154">このデータ ソースはイントラスタット テーブルを参照し、**会社間**オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="94e1a-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="94e1a-155">`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` 式として構成されたデータ ソースが呼び出されると、最終的な SQL ステートメントには次の条件が含まれています。</span><span class="sxs-lookup"><span data-stu-id="94e1a-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="94e1a-156">追加リソース</span><span class="sxs-lookup"><span data-stu-id="94e1a-156">Additional resources</span></span>

[<span data-ttu-id="94e1a-157">論理関数</span><span class="sxs-lookup"><span data-stu-id="94e1a-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="94e1a-158">VALUEINLARGE 関数</span><span class="sxs-lookup"><span data-stu-id="94e1a-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
