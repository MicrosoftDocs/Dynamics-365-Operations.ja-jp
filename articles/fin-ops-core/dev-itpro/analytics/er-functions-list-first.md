---
title: FIRST ER 関数
description: このトピックでは、FIRST 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564738"
---
# <a name="first-er-function"></a><span data-ttu-id="81121-103">FIRST ER 関数</span><span class="sxs-lookup"><span data-stu-id="81121-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81121-104">`FIRST` 関数は、リストが空でない場合に、指定されたリストの最初のレコードを *コンテナー (レコード)* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="81121-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="81121-105">リストが空の場合、この関数は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="81121-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="81121-106">構文</span><span class="sxs-lookup"><span data-stu-id="81121-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="81121-107">引数</span><span class="sxs-lookup"><span data-stu-id="81121-107">Arguments</span></span>

<span data-ttu-id="81121-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="81121-108">`list`: *Record list*</span></span>

<span data-ttu-id="81121-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="81121-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="81121-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="81121-110">Return values</span></span>

<span data-ttu-id="81121-111">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="81121-111">*Container (record)*</span></span>

<span data-ttu-id="81121-112">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="81121-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="81121-113">例 1</span><span class="sxs-lookup"><span data-stu-id="81121-113">Example 1</span></span>

<span data-ttu-id="81121-114">式 `FIRST(SPLIT("ABC",1)).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="81121-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="81121-115">例 2</span><span class="sxs-lookup"><span data-stu-id="81121-115">Example 2</span></span>

<span data-ttu-id="81121-116">式 `FIRST(SPLIT("",1)).Value` は、実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="81121-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81121-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="81121-117">Additional resources</span></span>

[<span data-ttu-id="81121-118">リスト機能</span><span class="sxs-lookup"><span data-stu-id="81121-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]