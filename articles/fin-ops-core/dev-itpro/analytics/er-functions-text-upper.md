---
title: UPPER ER 関数
description: このトピックでは、UPPER 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749144"
---
# <a name="upper-er-function"></a><span data-ttu-id="1716a-103">UPPER ER 関数</span><span class="sxs-lookup"><span data-stu-id="1716a-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1716a-104">`UPPER` 関数は、大文字に変換した後の *文字列* 値として指定されたテキスト返します。</span><span class="sxs-lookup"><span data-stu-id="1716a-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="1716a-105">構文</span><span class="sxs-lookup"><span data-stu-id="1716a-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="1716a-106">引数</span><span class="sxs-lookup"><span data-stu-id="1716a-106">Arguments</span></span>

<span data-ttu-id="1716a-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="1716a-107">`text`: *String*</span></span>

<span data-ttu-id="1716a-108">*文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1716a-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1716a-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="1716a-109">Return values</span></span>

<span data-ttu-id="1716a-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1716a-110">*String*</span></span>

<span data-ttu-id="1716a-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="1716a-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1716a-112">例</span><span class="sxs-lookup"><span data-stu-id="1716a-112">Example</span></span>

<span data-ttu-id="1716a-113">`UPPER ("Sample")` は、**"SAMPLE"** を返します。</span><span class="sxs-lookup"><span data-stu-id="1716a-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1716a-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1716a-114">Additional resources</span></span>

[<span data-ttu-id="1716a-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="1716a-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]