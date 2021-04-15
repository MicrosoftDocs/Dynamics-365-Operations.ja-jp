---
title: STRINGJOIN ER 関数
description: このトピックでは、STRINGJOIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745524"
---
# <a name="stringjoin-er-function"></a><span data-ttu-id="8a7ba-103">STRINGJOIN ER 関数</span><span class="sxs-lookup"><span data-stu-id="8a7ba-103">STRINGJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a7ba-104">`STRINGJOIN` 関数は、指定されたリストから指定したフィールドの連結された値で構成される *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-104">The `STRINGJOIN` function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="8a7ba-105">値は、指定した区切り記号で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-105">The values can be separated by the specified delimiter.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7ba-106">構文</span><span class="sxs-lookup"><span data-stu-id="8a7ba-106">Syntax</span></span>

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a><span data-ttu-id="8a7ba-107">引数</span><span class="sxs-lookup"><span data-stu-id="8a7ba-107">Arguments</span></span>

<span data-ttu-id="8a7ba-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="8a7ba-108">`list`: *Record list*</span></span>

<span data-ttu-id="8a7ba-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="8a7ba-110">`field`: *フィールド*</span><span class="sxs-lookup"><span data-stu-id="8a7ba-110">`field`: *Field*</span></span>

<span data-ttu-id="8a7ba-111">指定されたリストの *文字列* データ型のフィールドの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-111">The valid path of a field of the *String* data type in the specified list.</span></span>

<span data-ttu-id="8a7ba-112">`delimiter`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="8a7ba-112">`delimiter`: *String*</span></span>

<span data-ttu-id="8a7ba-113">サブ文字列を区切るために使用される区切り記号。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-113">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="8a7ba-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="8a7ba-114">Return values</span></span>

<span data-ttu-id="8a7ba-115">*文字列*</span><span class="sxs-lookup"><span data-stu-id="8a7ba-115">*String*</span></span>

<span data-ttu-id="8a7ba-116">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-116">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8a7ba-117">例</span><span class="sxs-lookup"><span data-stu-id="8a7ba-117">Example</span></span>

<span data-ttu-id="8a7ba-118">データソース **DS** として `SPLIT("abc" , 1)` を入力すると、式 `STRINGJOIN (DS, DS.Value, "-")` は **"a-b-c"** を返します。</span><span class="sxs-lookup"><span data-stu-id="8a7ba-118">If you enter `SPLIT("abc" , 1)` as data source **DS**, the expression `STRINGJOIN (DS, DS.Value, "-")` returns **"a-b-c"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a7ba-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8a7ba-119">Additional resources</span></span>

[<span data-ttu-id="8a7ba-120">リスト機能</span><span class="sxs-lookup"><span data-stu-id="8a7ba-120">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]