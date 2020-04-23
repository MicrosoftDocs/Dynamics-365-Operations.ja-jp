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
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249038"
---
# <a name=""></a><span data-ttu-id="8d8e5-103"><a name="LISTJOIN">LISTJOIN ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="8d8e5-103"><a name="LISTJOIN">LISTJOIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d8e5-104">この `LISTJOIN` 関数は、指定された引数から作成された新しい結合リストを表す *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8e5-105">構文</span><span class="sxs-lookup"><span data-stu-id="8d8e5-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="8d8e5-106">引数</span><span class="sxs-lookup"><span data-stu-id="8d8e5-106">Arguments</span></span>

<span data-ttu-id="8d8e5-107">`list 1`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="8d8e5-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="8d8e5-108">*レコード リスト* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8d8e5-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-109">This argument is mandatory.</span></span>

<span data-ttu-id="8d8e5-110">`list N`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="8d8e5-110">`list N`: *Record list*</span></span>

<span data-ttu-id="8d8e5-111">*レコード リスト* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="8d8e5-112">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d8e5-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="8d8e5-113">Return values</span></span>

<span data-ttu-id="8d8e5-114">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="8d8e5-114">*Record list*</span></span>

<span data-ttu-id="8d8e5-115">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d8e5-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="8d8e5-116">Usage notes</span></span>

<span data-ttu-id="8d8e5-117">作成されたリストの構造には、引数で参照されるすべてのレコード リストの構造に存在するフィールドのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="8d8e5-118">例</span><span class="sxs-lookup"><span data-stu-id="8d8e5-118">Example</span></span>

<span data-ttu-id="8d8e5-119">`Container` タイプのデータ ソース **レコード 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="8d8e5-120">このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:</span><span class="sxs-lookup"><span data-stu-id="8d8e5-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8d8e5-121">**コード**: このフィールドには、`String` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="8d8e5-122">**量**: このフィールドには、`Real` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="8d8e5-123">次に、`Container` タイプのデータ ソース **レコード 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="8d8e5-124">このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:</span><span class="sxs-lookup"><span data-stu-id="8d8e5-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="8d8e5-125">**量**: このフィールドには、`Real` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="8d8e5-126">**IsValid**: このフィールドには、`Boolean` タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

<span data-ttu-id="8d8e5-127">この場合、式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` は 2 つのレコードを含む新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-127">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span> <span data-ttu-id="8d8e5-128">このフィールドは、呼び出された関数のすべての引数に表示される唯一のフィールドであるため、`Real` タイプの 1 つの **量** フィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8e5-128">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d8e5-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8d8e5-129">Additional resources</span></span>

[<span data-ttu-id="8d8e5-130">リスト機能</span><span class="sxs-lookup"><span data-stu-id="8d8e5-130">List functions</span></span>](er-functions-category-list.md)
