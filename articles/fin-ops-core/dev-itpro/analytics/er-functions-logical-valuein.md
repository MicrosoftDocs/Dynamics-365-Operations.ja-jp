---
title: VALUEIN ER 関数
description: このトピックでは、VALUEIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d0df97234df41d11897473dea4e85354e82d36ec
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041702"
---
# <span data-ttu-id="436c7-103"><a name="VALUEIN">VALUEIN ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="436c7-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="436c7-104">`VALUEIN` 関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="436c7-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="436c7-105">指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="436c7-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="436c7-106">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="436c7-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="436c7-107">構文</span><span class="sxs-lookup"><span data-stu-id="436c7-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="436c7-108">引数</span><span class="sxs-lookup"><span data-stu-id="436c7-108">Arguments</span></span>

<span data-ttu-id="436c7-109">`input`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="436c7-109">`input`: *Field*</span></span>

<span data-ttu-id="436c7-110">*レコード リスト* タイプのデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="436c7-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="436c7-111">この項目の値は一致します。</span><span class="sxs-lookup"><span data-stu-id="436c7-111">The value of this item will be matched.</span></span>

<span data-ttu-id="436c7-112">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="436c7-112">`list`: *Record list*</span></span>

<span data-ttu-id="436c7-113">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="436c7-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="436c7-114">`list item expression`: *ブール値*</span><span class="sxs-lookup"><span data-stu-id="436c7-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="436c7-115">照合に使用される指定されたリストの単一のフィールドを指し示すか、そのフィールドを含む有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="436c7-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="436c7-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="436c7-116">Return values</span></span>

<span data-ttu-id="436c7-117">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="436c7-117">*Boolean*</span></span>

<span data-ttu-id="436c7-118">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="436c7-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="436c7-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="436c7-119">Usage notes</span></span>

<span data-ttu-id="436c7-120">一般に、`VALUEIN` 関数は一連の **OR** 条件に変換されます。</span><span class="sxs-lookup"><span data-stu-id="436c7-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="436c7-121">場合によっては、`EXISTS JOIN` オペレーターを使用してデータベース SQL ステートメントに変換されます。</span><span class="sxs-lookup"><span data-stu-id="436c7-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="436c7-122">例 1</span><span class="sxs-lookup"><span data-stu-id="436c7-122">Example 1</span></span>

<span data-ttu-id="436c7-123">モデル マッピングで、*計算済フィールド* タイプの**リスト** データ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="436c7-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="436c7-124">このデータ ソースには、式 `SPLIT ("a,b,c", ",")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="436c7-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="436c7-125">データ ソースが呼び出されると、`VALUEIN ("B", List, List.Value)` 式として構成されている場合は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="436c7-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="436c7-126">この場合、`VALUEIN` 関数は次の一連の条件に変換されます。`("B" = "b")` が **TRUE** と等しい場合、`(("B" = "a") or ("B" = "b") or ("B" = "c"))`。</span><span class="sxs-lookup"><span data-stu-id="436c7-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="436c7-127">データ ソースが呼び出されると、`VALUEIN ("B", List, LEFT(List.Value, 0))` 式として構成されている場合は、**FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="436c7-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="436c7-128">この場合、`VALUEIN` 関数は次の一連の条件に変換されます。 **TRUE** と等しくない `("B" = "")`。</span><span class="sxs-lookup"><span data-stu-id="436c7-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="436c7-129">このような条件のテキストの文字数の上限は 32,768 文字です。</span><span class="sxs-lookup"><span data-stu-id="436c7-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="436c7-130">したがって、実行時に制限を超える可能性があるデータ ソースを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="436c7-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="436c7-131">制限を超過した場合は、アプリケーションは実行を停止し、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="436c7-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="436c7-132">たとえば、この状況は、データ ソースが `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` として構成され、**List1** および **List2** リストに大量のレコードが含まれているときに生じます。</span><span class="sxs-lookup"><span data-stu-id="436c7-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="436c7-133">場合によっては、`VALUEIN` 関数は `EXISTS JOIN` オペレーターを使用することでデータベース ステートメントに変換されます。</span><span class="sxs-lookup"><span data-stu-id="436c7-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="436c7-134">この動作は、[FILTER](er-functions-list-filter.md) 関数が使用され、次の条件が満たされているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="436c7-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="436c7-135">**ASK FOR QUERY** オプションは、レコードのリストを参照する `VALUEIN` 関数のデータ ソースに対してオフになっています。</span><span class="sxs-lookup"><span data-stu-id="436c7-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="436c7-136">このデータ ソースには実行時に適用される追加の条件はありません。</span><span class="sxs-lookup"><span data-stu-id="436c7-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="436c7-137">入れ子になった式は、レコードのリストを参照する `VALUEIN` 関数のデータ ソース用に構成されません。</span><span class="sxs-lookup"><span data-stu-id="436c7-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="436c7-138">`VALUEIN` 関数のリスト項目は、指定されたデータ ソースの式またメソッドではなく、指定されたデータ ソースのフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="436c7-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="436c7-139">この例の前半で説明した [WHERE](er-functions-list-where.md) 関数の代わりにこのオプションを使用することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="436c7-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="436c7-140">例 2</span><span class="sxs-lookup"><span data-stu-id="436c7-140">Example 2</span></span>

<span data-ttu-id="436c7-141">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="436c7-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="436c7-142">*テーブル レコード* タイプの **In** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="436c7-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="436c7-143">このデータ ソースは、イントラスタット テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="436c7-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="436c7-144">*テーブル レコード* タイプの**ポート** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="436c7-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="436c7-145">このデータ ソースは、IntrastatPort テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="436c7-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="436c7-146">`FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` 式として構成されたデータ ソースが呼び出されると、次の SQL ステートメントが生成され、イントラスタット テーブルのフィルターされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="436c7-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="436c7-147">**dataAreaId** フィールドの場合、`IN` 演算子を使用して最終的な SQL ステートメントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="436c7-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="436c7-148">例 3</span><span class="sxs-lookup"><span data-stu-id="436c7-148">Example 3</span></span>

<span data-ttu-id="436c7-149">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="436c7-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="436c7-150">*計算済フィールド* タイプの **Le** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="436c7-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="436c7-151">このデータ ソースには、式 `SPLIT ("DEMF,GBSI,USMF", ",")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="436c7-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="436c7-152">*テーブル レコード* タイプの **In** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="436c7-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="436c7-153">このデータ ソースはイントラスタット テーブルを参照し、**会社間**オプションが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="436c7-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="436c7-154">`FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` 式として構成されたデータ ソースが呼び出されると、最終的な SQL ステートメントには次の条件が含まれています。</span><span class="sxs-lookup"><span data-stu-id="436c7-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="436c7-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="436c7-155">Additional resources</span></span>

[<span data-ttu-id="436c7-156">論理機能</span><span class="sxs-lookup"><span data-stu-id="436c7-156">Logical functions</span></span>](er-functions-category-logical.md)
