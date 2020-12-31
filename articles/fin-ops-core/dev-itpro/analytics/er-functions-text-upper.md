---
title: UPPER ER 関数
description: このトピックでは、UPPER 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688344"
---
# <a name="upper-er-function"></a><span data-ttu-id="d9efd-103">UPPER ER 関数</span><span class="sxs-lookup"><span data-stu-id="d9efd-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9efd-104">`UPPER` 関数は、大文字に変換した後の *文字列* 値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="d9efd-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9efd-105">構文</span><span class="sxs-lookup"><span data-stu-id="d9efd-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="d9efd-106">引数</span><span class="sxs-lookup"><span data-stu-id="d9efd-106">Arguments</span></span>

<span data-ttu-id="d9efd-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="d9efd-107">`text`: *String*</span></span>

<span data-ttu-id="d9efd-108">*文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="d9efd-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9efd-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9efd-109">Return values</span></span>

<span data-ttu-id="d9efd-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="d9efd-110">*String*</span></span>

<span data-ttu-id="d9efd-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="d9efd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d9efd-112">例</span><span class="sxs-lookup"><span data-stu-id="d9efd-112">Example</span></span>

<span data-ttu-id="d9efd-113">`UPPER ("Sample")` は、**"SAMPLE"** を返します。</span><span class="sxs-lookup"><span data-stu-id="d9efd-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9efd-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d9efd-114">Additional resources</span></span>

[<span data-ttu-id="d9efd-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="d9efd-115">Text functions</span></span>](er-functions-category-text.md)
