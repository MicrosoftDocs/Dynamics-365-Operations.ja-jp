---
title: ALLITEMSQUERY ER 関数
description: このトピックでは、ALLITEMSQUERY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559606"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="acc11-103">ALLITEMSQUERY ER 関数</span><span class="sxs-lookup"><span data-stu-id="acc11-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="acc11-104">`ALLITEMSQUERY` 関数は、結合された SQL クエリとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="acc11-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="acc11-105">これは、指定したパスに一致するすべての品目を表すレコードの一覧を構成する、新しいフラット化された *レコード リスト* の値を返します。</span><span class="sxs-lookup"><span data-stu-id="acc11-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc11-106">構文</span><span class="sxs-lookup"><span data-stu-id="acc11-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="acc11-107">引数</span><span class="sxs-lookup"><span data-stu-id="acc11-107">Arguments</span></span>

<span data-ttu-id="acc11-108">`path`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="acc11-108">`path`: *Record list*</span></span>

<span data-ttu-id="acc11-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="acc11-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="acc11-110">少なくとも 1 つの関係が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acc11-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="acc11-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="acc11-111">Return values</span></span>

<span data-ttu-id="acc11-112">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="acc11-112">*Record list*</span></span>

<span data-ttu-id="acc11-113">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="acc11-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="acc11-114">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="acc11-114">Usage notes</span></span>

<span data-ttu-id="acc11-115">指定されたパスは、*レコード リスト* データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acc11-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="acc11-116">また、少なくとも 1 つの関係が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="acc11-116">It must also contain at least one relation.</span></span> <span data-ttu-id="acc11-117">パス *文字列* や *日付* などのデータ要素は、デザイン時に電子申告 (ER) 式ビルダーでエラーを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acc11-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="acc11-118">この関数は、 SQL を使用して直接呼び出すことができるアプリケーション オブジェクト (テーブル、エンティティ、クエリなど) を参照する *レコード リスト* データ型のデータ ソースに適用されると、結合された SQL クエリとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="acc11-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="acc11-119">それ以外の場合は、[ALLITEMS](er-functions-list-allitems.md) 関数としてメモリ上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="acc11-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="acc11-120">例</span><span class="sxs-lookup"><span data-stu-id="acc11-120">Example</span></span>

<span data-ttu-id="acc11-121">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="acc11-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="acc11-122">CustInvoiceTable テーブルを参照する *テーブル レコード* タイプの **CustInv** データ ソース</span><span class="sxs-lookup"><span data-stu-id="acc11-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="acc11-123">`FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 式を含む *計算済フィールド* タイプの **FilteredInv** データ ソース</span><span class="sxs-lookup"><span data-stu-id="acc11-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="acc11-124">`ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 式を含む *計算済フィールド* タイプの **JourLines**</span><span class="sxs-lookup"><span data-stu-id="acc11-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="acc11-125">**JourLines** データ ソースを呼び出すモデル マッピングを実行すると、次の SQL ステートメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="acc11-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="acc11-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="acc11-126">Additional resources</span></span>

[<span data-ttu-id="acc11-127">リスト機能</span><span class="sxs-lookup"><span data-stu-id="acc11-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]