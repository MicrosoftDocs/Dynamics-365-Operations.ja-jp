---
title: LIST ER 関数
description: このトピックでは、LIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683090"
---
# <a name="list-er-function"></a><span data-ttu-id="dece1-103">LIST ER 関数</span><span class="sxs-lookup"><span data-stu-id="dece1-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dece1-104">`LIST` 関数は、指定された引数から作成されたレコードの新しいリストで構成される *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="dece1-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="dece1-105">構文</span><span class="sxs-lookup"><span data-stu-id="dece1-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="dece1-106">引数</span><span class="sxs-lookup"><span data-stu-id="dece1-106">Arguments</span></span>

<span data-ttu-id="dece1-107">`record 1`: *コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="dece1-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="dece1-108">*レコード* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="dece1-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="dece1-109">この引数は必須です。</span><span class="sxs-lookup"><span data-stu-id="dece1-109">This argument is required.</span></span>

<span data-ttu-id="dece1-110">`record N`: *コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="dece1-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="dece1-111">*レコード* データ タイプのデータ ソースの参照。</span><span class="sxs-lookup"><span data-stu-id="dece1-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="dece1-112">これらの追加引数はオプションです。</span><span class="sxs-lookup"><span data-stu-id="dece1-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="dece1-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="dece1-113">Return values</span></span>

<span data-ttu-id="dece1-114">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="dece1-114">*Record list*</span></span>

<span data-ttu-id="dece1-115">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="dece1-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="dece1-116">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="dece1-116">Usage notes</span></span>

<span data-ttu-id="dece1-117">作成されたリストの構造には、引数で指定されているすべてのレコードの構造で表示されるフィールドのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dece1-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="dece1-118">例</span><span class="sxs-lookup"><span data-stu-id="dece1-118">Example</span></span>

<span data-ttu-id="dece1-119">*コンテナー* タイプのデータ ソース **レコード 1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="dece1-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="dece1-120">このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="dece1-121">**コード:** このフィールドには、*文字列* タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="dece1-122">**金額:** このフィールドには、*実数* タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="dece1-123">次に、*コンテナー* タイプのデータ ソース **レコード 2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="dece1-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="dece1-124">このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="dece1-125">**金額:** このフィールドには、*実数* タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="dece1-126">**IsValid:** このフィールドには、*ブール値* タイプの値を返す式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dece1-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="dece1-127">この場合、式 `LIST('Record 1', 'Record 2')` は 2 つのレコードを含む新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="dece1-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="dece1-128">このフィールドは、呼び出された関数のすべての引数に対して表示される唯一のフィールドであるため、このリストの構造は *実数* タイプの 1 つの **金額** フィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="dece1-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dece1-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="dece1-129">Additional resources</span></span>

[<span data-ttu-id="dece1-130">リスト機能</span><span class="sxs-lookup"><span data-stu-id="dece1-130">List functions</span></span>](er-functions-category-list.md)
