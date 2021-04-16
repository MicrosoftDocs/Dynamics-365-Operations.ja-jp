---
title: VALUEINLARGE ER 関数
description: このトピックでは、 VALUEINLARGE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 74d6856a0598293d87f79baabed4773d617164d0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743754"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="ebd70-103">VALUEINLARGE ER 関数</span><span class="sxs-lookup"><span data-stu-id="ebd70-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebd70-104">`VALUEINLARGE` 関数は、*Int64* あるいは *整数* タイプの指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="ebd70-105">この関数は、指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="ebd70-106">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="ebd70-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="ebd70-107">`VALUEIN` 関数との違いを理解するには、このトピックで後述する [使用上の注意](#usage_note) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd70-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd70-108">構文</span><span class="sxs-lookup"><span data-stu-id="ebd70-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="ebd70-109">引数</span><span class="sxs-lookup"><span data-stu-id="ebd70-109">Arguments</span></span>

<span data-ttu-id="ebd70-110">`input`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="ebd70-110">`input`: *Field*</span></span>

<span data-ttu-id="ebd70-111">*レコード リスト* タイプのデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="ebd70-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="ebd70-112">この項目の値は一致します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-112">The value of this item will be matched.</span></span>

<span data-ttu-id="ebd70-113">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="ebd70-113">`list`: *Record list*</span></span>

<span data-ttu-id="ebd70-114">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="ebd70-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ebd70-115">`list item expression`: *式*</span><span class="sxs-lookup"><span data-stu-id="ebd70-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="ebd70-116">照合に使用される指定されたリストの単一のフィールドを指し示すか、そのフィールドを含む有効な条件式。</span><span class="sxs-lookup"><span data-stu-id="ebd70-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebd70-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebd70-117">Return values</span></span>

<span data-ttu-id="ebd70-118">*ブール値*</span><span class="sxs-lookup"><span data-stu-id="ebd70-118">*Boolean*</span></span>

<span data-ttu-id="ebd70-119">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="ebd70-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="ebd70-120"><a name="usage_note">使用上の注意</a></span><span class="sxs-lookup"><span data-stu-id="ebd70-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="ebd70-121">指定された入力が、データ ソース項目の *Int64* または *整数* タイプを表す場合、直接 SQL ステートメントに変換可能な呼び出しは、指定されたリストが一時的な SQL テーブルに変換され、単一の `EXISTS JOIN` クエリを実行することによってデータベース内で一致が実行されます。</span><span class="sxs-lookup"><span data-stu-id="ebd70-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="ebd70-122">それ以外の場合、この関数は [`VALUEIN`](er-functions-logical-valuein.md) 関数として機能します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="ebd70-123">指定された入力が、*Int64* および *整数* タイプ以外の項目として設計されたデータ ソース項目を表している場合、設計時にエラーが発生し、`VALUEINLARGE` 関数が設定された ER 式に適用されないことが通知されます。</span><span class="sxs-lookup"><span data-stu-id="ebd70-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="ebd70-124">`VALUEINLARGE` 関数式が実行され、この実行のスコープで複数の一時テーブルが使用される場合、ランタイム エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="ebd70-125">例</span><span class="sxs-lookup"><span data-stu-id="ebd70-125">Example</span></span>

<span data-ttu-id="ebd70-126">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="ebd70-127">*テーブル レコード* タイプの **In** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="ebd70-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="ebd70-128">このデータ ソースは、**イントラスタット** テーブルを参照します。</span><span class="sxs-lookup"><span data-stu-id="ebd70-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="ebd70-129">**会社間** オプションは **いいえ** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="ebd70-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="ebd70-130">*計算フィールド* タイプの **InMemory** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="ebd70-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="ebd70-131">このデータ ソースは、式 `WHERE (In, In.Port <> "")` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebd70-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="ebd70-132">*計算フィールド* タイプの **InFiltered** データ ソース。</span><span class="sxs-lookup"><span data-stu-id="ebd70-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="ebd70-133">このデータ ソースは、式 `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)` が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ebd70-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="ebd70-134">データソース **InFiltered** が、会社 **DEMF** のコンテキストで呼び出されると、アプリケーション データベースに新しい一時テーブルが作成され、レコード ID コードの収集されたメモリ リストがこのテーブルに挿入され、**イントラスタット** テーブルのフィルター処理されたレコードを返す次の SQL ステートメントが生成されます。</span><span class="sxs-lookup"><span data-stu-id="ebd70-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="ebd70-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ebd70-135">Additional resources</span></span>

[<span data-ttu-id="ebd70-136">論理関数</span><span class="sxs-lookup"><span data-stu-id="ebd70-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="ebd70-137">VALUEIN 関数</span><span class="sxs-lookup"><span data-stu-id="ebd70-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]