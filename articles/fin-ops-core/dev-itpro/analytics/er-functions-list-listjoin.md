---
title: LISTJOIN ER 関数
description: このトピックでは、LISTJOIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f78b687865e63e658c1c1c4f148b50595bf063
ms.sourcegitcommit: 54bdcf8e9b6d1b1aae2a244f7a82754879d12053
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2020
ms.locfileid: "3740666"
---
# <a name=""></a><span data-ttu-id="d1457-103"><a name="LISTJOIN">LISTJOIN ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="d1457-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1457-104">この `LISTJOIN` 関数は、指定された引数から作成された新しい結合リストを表す *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="d1457-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1457-105">構文</span><span class="sxs-lookup"><span data-stu-id="d1457-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="d1457-106">引数</span><span class="sxs-lookup"><span data-stu-id="d1457-106">Arguments</span></span>

<span data-ttu-id="d1457-107">`list 1`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="d1457-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="d1457-108">*レコード リスト* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="d1457-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="d1457-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="d1457-109">This argument is mandatory.</span></span>

<span data-ttu-id="d1457-110">`list N`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="d1457-110">`list N`: *Record list*</span></span>

<span data-ttu-id="d1457-111">*レコード リスト* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="d1457-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="d1457-112">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="d1457-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d1457-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="d1457-113">Return values</span></span>

<span data-ttu-id="d1457-114">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="d1457-114">*Record list*</span></span>

<span data-ttu-id="d1457-115">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="d1457-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d1457-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="d1457-116">Usage notes</span></span>

<span data-ttu-id="d1457-117">作成されたリストの構造には、引数で参照されるすべてのレコード リストの構造に存在するフィールドのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1457-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="d1457-118">例</span><span class="sxs-lookup"><span data-stu-id="d1457-118">Example</span></span>

<span data-ttu-id="d1457-119">`Container` タイプのデータ ソース **レコード 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1457-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="d1457-120">このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:</span><span class="sxs-lookup"><span data-stu-id="d1457-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="d1457-121">**コード**: このフィールドには、`String` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1457-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="d1457-122">**量**: このフィールドには、`Real` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1457-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="d1457-123">次に、`Container` タイプのデータ ソース **レコード 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1457-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="d1457-124">このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:</span><span class="sxs-lookup"><span data-stu-id="d1457-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="d1457-125">**量**: このフィールドには、`Real` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1457-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="d1457-126">**IsValid**: このフィールドには、`Boolean` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d1457-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER モデル マッピング デザイナーのページ](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="d1457-128">この場合、式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` は 2 つのレコードを含む新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="d1457-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![ER モデル マッピング デザイナーのページ](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="d1457-130">このフィールドは、呼び出された関数のすべての引数に表示される唯一のフィールドであるため、`Real` タイプの 1 つの **量** フィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d1457-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER モデル マッピング デザイナーのページ](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="d1457-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d1457-132">Additional resources</span></span>

[<span data-ttu-id="d1457-133">リスト関数</span><span class="sxs-lookup"><span data-stu-id="d1457-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="d1457-134">実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する</span><span class="sxs-lookup"><span data-stu-id="d1457-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
