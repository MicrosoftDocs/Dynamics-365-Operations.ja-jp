---
title: SPLIT ER 関数
description: このトピックでは、SPLIT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52a89f744cd37c543294522cc706ae7f47660e75
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070624"
---
# <span data-ttu-id="41ddb-103"><a name="SPLIT">SPLIT ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="41ddb-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41ddb-104">`SPLIT` 関数は、指定された入力文字列をサブ文字列に分割し、結果を新しい*レコード リスト*値として返します。</span><span class="sxs-lookup"><span data-stu-id="41ddb-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="41ddb-105">構文 1</span><span class="sxs-lookup"><span data-stu-id="41ddb-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="41ddb-106">この構文は、指定された入力文字列を指定された長さのサブ文字列に分割するために使用します。</span><span class="sxs-lookup"><span data-stu-id="41ddb-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="41ddb-107">構文 2</span><span class="sxs-lookup"><span data-stu-id="41ddb-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="41ddb-108">この構文は、指定された入力文字列を指定された区切り記号に基づいてサブ文字列に分割するために使用します。</span><span class="sxs-lookup"><span data-stu-id="41ddb-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="41ddb-109">引数</span><span class="sxs-lookup"><span data-stu-id="41ddb-109">Arguments</span></span>

<span data-ttu-id="41ddb-110">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="41ddb-110">`input`: *String*</span></span>

<span data-ttu-id="41ddb-111">分割するテキスト。</span><span class="sxs-lookup"><span data-stu-id="41ddb-111">The text to split.</span></span>

<span data-ttu-id="41ddb-112">`length`: *整数*</span><span class="sxs-lookup"><span data-stu-id="41ddb-112">`length`: *Integer*</span></span>

<span data-ttu-id="41ddb-113">単一のサブ文字列の最大の長さ。</span><span class="sxs-lookup"><span data-stu-id="41ddb-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="41ddb-114">`delimiter`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="41ddb-114">`delimiter`: *String*</span></span>

<span data-ttu-id="41ddb-115">サブ文字列を区切るために使用される区切り記号。</span><span class="sxs-lookup"><span data-stu-id="41ddb-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="41ddb-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="41ddb-116">Return values</span></span>

<span data-ttu-id="41ddb-117">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="41ddb-117">*Record list*</span></span>

<span data-ttu-id="41ddb-118">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="41ddb-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="41ddb-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="41ddb-119">Usage notes</span></span>

<span data-ttu-id="41ddb-120">返されるリストのレコード構造は、*文字列*型の**値**フィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="41ddb-121">返されるリストのすべてのレコードには、このフィールドで生成されたサブ文字列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="41ddb-122">`delimiter` 引数が空の場合、返される新しいリストは、*文字列*型の**値**フィールドを持つ 1 つのレコードで構成されます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="41ddb-123">このフィールドには、入力テキストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41ddb-123">This field contains the input text.</span></span>

<span data-ttu-id="41ddb-124">`input` 引数が空の場合は、新しい空のリストが返されます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="41ddb-125">`input` または `delimiter` 引数のいずれかを指定しない場合 (null)、アプリケーション例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="41ddb-126">例 1</span><span class="sxs-lookup"><span data-stu-id="41ddb-126">Example 1</span></span>

<span data-ttu-id="41ddb-127">`SPLIT ("abcd", 3)` は、*文字列*型の**値**フィールドのある 2 つのレコードで構成される新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="41ddb-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="41ddb-128">最初のレコードの**値**フィールドには、テキスト **"abc"** が、2 つ目のレコードの**値**フィールドには、テキスト **"d"** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="41ddb-129">例 2</span><span class="sxs-lookup"><span data-stu-id="41ddb-129">Example 2</span></span>

<span data-ttu-id="41ddb-130">`SPLIT ("XAb aBy", "aB")` は、*文字列*型の**値**フィールドのある 3 つのレコードで構成される新しいリストを返します。</span><span class="sxs-lookup"><span data-stu-id="41ddb-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="41ddb-131">最初のレコードの**値**フィールドには、テキスト **"X"** が、2 つ目のレコードの**値**フィールドには、テキスト **"&nbsp;"** が、3 つ目のレコードの**値**フィールドにはテキスト **"y"** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="41ddb-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="41ddb-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="41ddb-132">Additional resources</span></span>

[<span data-ttu-id="41ddb-133">リスト機能</span><span class="sxs-lookup"><span data-stu-id="41ddb-133">List functions</span></span>](er-functions-category-list.md)
