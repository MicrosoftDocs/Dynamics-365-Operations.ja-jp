---
title: LISTDISTINCT ER 関数
description: このトピックでは、LISTDISTINCT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 9ab9354b0fdb1c08c192b90e6bab303cb85ea41a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743826"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="7d286-103">LISTDISTINCT ER 関数</span><span class="sxs-lookup"><span data-stu-id="7d286-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7d286-104">この `LISTDISTINCT` 関数は、指定されたリストのすべてのレコードに対して、指定された式をセレクターとして計算します。</span><span class="sxs-lookup"><span data-stu-id="7d286-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="7d286-105">固有のセレクター値ごとに 1 つのレコードを含む、新しい *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="7d286-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d286-106">構文</span><span class="sxs-lookup"><span data-stu-id="7d286-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="7d286-107">引数</span><span class="sxs-lookup"><span data-stu-id="7d286-107">Arguments</span></span>

<span data-ttu-id="7d286-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="7d286-108">`list`: *Record list*</span></span>

<span data-ttu-id="7d286-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="7d286-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7d286-110">`selector`: *プリミティブ データ型*</span><span class="sxs-lookup"><span data-stu-id="7d286-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="7d286-111">指定されたリスト内のすべてのレコードに対してセレクター値を計算するために使用される有効な式。</span><span class="sxs-lookup"><span data-stu-id="7d286-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="7d286-112">このパラメータでは、次のデータ型がサポートされています:</span><span class="sxs-lookup"><span data-stu-id="7d286-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="7d286-113">ブール値</span><span class="sxs-lookup"><span data-stu-id="7d286-113">Boolean</span></span>
- <span data-ttu-id="7d286-114">日</span><span class="sxs-lookup"><span data-stu-id="7d286-114">Date</span></span>
- <span data-ttu-id="7d286-115">DateTime</span><span class="sxs-lookup"><span data-stu-id="7d286-115">DateTime</span></span>
- <span data-ttu-id="7d286-116">GUID</span><span class="sxs-lookup"><span data-stu-id="7d286-116">GUID</span></span>
- <span data-ttu-id="7d286-117">整数</span><span class="sxs-lookup"><span data-stu-id="7d286-117">Integer</span></span>
- <span data-ttu-id="7d286-118">Int64</span><span class="sxs-lookup"><span data-stu-id="7d286-118">Int64</span></span>
- <span data-ttu-id="7d286-119">実績</span><span class="sxs-lookup"><span data-stu-id="7d286-119">Real</span></span>
- <span data-ttu-id="7d286-120">文字列</span><span class="sxs-lookup"><span data-stu-id="7d286-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="7d286-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="7d286-121">Return values</span></span>

<span data-ttu-id="7d286-122">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="7d286-122">*Record list*</span></span>

<span data-ttu-id="7d286-123">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="7d286-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7d286-124">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="7d286-124">Usage notes</span></span>

<span data-ttu-id="7d286-125">作成されたリストの構造は、指定されたリストの構造に一致します。</span><span class="sxs-lookup"><span data-stu-id="7d286-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="7d286-126">指定したリストの複数のレコードに対して同じセレクター値が計算される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7d286-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="7d286-127">この場合、作成されたリスト内の対応するレコードのフィールド値は、セレクター値の計算対象となる指定されたリストの最初のレコードの値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="7d286-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="7d286-128">この関数の実行は、メモリ内に存在する *レコード リスト* タイプの [電子申告 (ER)](general-electronic-reporting.md) データ ソースで実行されます。</span><span class="sxs-lookup"><span data-stu-id="7d286-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="7d286-129">**GROUPBY** データ ソースを使用して、固有の値を持つセレクターが計算されるレコードの一覧を生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="7d286-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="7d286-130">ただし、関数の実行はメモリ内で行われるため、パフォーマンスとメモリの消費の観点から、**GROUPBY** データ ソースより `LISTDISTINCT` 機能を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7d286-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="7d286-131">例</span><span class="sxs-lookup"><span data-stu-id="7d286-131">Example</span></span>

<span data-ttu-id="7d286-132">次の例は、特定の期間中に少なくとも 1 つの売上請求書またはプロジェクト請求書が発行された固有の顧客アカウント番号の一覧を取得する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7d286-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="7d286-133">**CustInvoiceJour** アプリケーション テーブルを参照し、特定期間の売上請求書をフィルター処理する `Record list` タイプの **SalesInvoice** データ ソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="7d286-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="7d286-134">このデータ ソースの `InvoiceAccount` フィールドは、請求済顧客のアカウント番号を返します。</span><span class="sxs-lookup"><span data-stu-id="7d286-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="7d286-135">**ProjInvoiceJour** アプリケーション テーブルを参照し、特定期間のプロジェクト請求書をフィルター処理する `Record list` タイプの **ProjectInvoice** データ ソースを入力します。</span><span class="sxs-lookup"><span data-stu-id="7d286-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="7d286-136">このデータ ソースの `InvoiceAccount` フィールドは、請求済顧客のアカウント番号を返します。</span><span class="sxs-lookup"><span data-stu-id="7d286-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="7d286-137">式 `LISTJOIN(SalesInvoice, ProjectInvoice)` を含む `Calculated field` タイプの **AllInvoices** データ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="7d286-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="7d286-138">このデータ ソースは、売上請求書およびプロジェクト請求書の結合リストを返します。</span><span class="sxs-lookup"><span data-stu-id="7d286-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="7d286-139">式 `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` を含む `Record list` タイプの **InvoicedCustomer** データ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="7d286-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="7d286-140">このデータ ソースは、定義された期間中に請求された固有の顧客ごとに 1 つのレコードを含む新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="7d286-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="7d286-141">このリストの `InvoiceAccount` フィールドには、顧客アカウント番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d286-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d286-142">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7d286-142">Additional resources</span></span>

[<span data-ttu-id="7d286-143">リスト関数</span><span class="sxs-lookup"><span data-stu-id="7d286-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]