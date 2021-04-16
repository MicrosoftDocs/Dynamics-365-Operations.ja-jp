---
title: LEN ER 関数
description: このトピックでは、LEN 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 394e07a7a573cc4462196b17440f8b0547d8dd48
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746318"
---
# <a name="len-er-function"></a><span data-ttu-id="7a16f-103">LEN ER 関数</span><span class="sxs-lookup"><span data-stu-id="7a16f-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a16f-104">`LEN` 関数は、*整数* 値として指定された文字列の文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="7a16f-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a16f-105">構文</span><span class="sxs-lookup"><span data-stu-id="7a16f-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="7a16f-106">引数</span><span class="sxs-lookup"><span data-stu-id="7a16f-106">Arguments</span></span>

<span data-ttu-id="7a16f-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="7a16f-107">`text`: *String*</span></span>

<span data-ttu-id="7a16f-108">*文字列* 値は、テキストを指定。</span><span class="sxs-lookup"><span data-stu-id="7a16f-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a16f-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="7a16f-109">Return values</span></span>

<span data-ttu-id="7a16f-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="7a16f-110">*Integer*</span></span>

<span data-ttu-id="7a16f-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="7a16f-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="7a16f-112">例</span><span class="sxs-lookup"><span data-stu-id="7a16f-112">Example</span></span>

<span data-ttu-id="7a16f-113">`LEN ("Sample")` は、**6** を返します。</span><span class="sxs-lookup"><span data-stu-id="7a16f-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a16f-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7a16f-114">Additional resources</span></span>

[<span data-ttu-id="7a16f-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="7a16f-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]