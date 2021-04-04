---
title: TRIM ER 関数
description: このトピックでは、TRIM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560040"
---
# <a name="trim-er-function"></a><span data-ttu-id="f1426-103">TRIM ER 関数</span><span class="sxs-lookup"><span data-stu-id="f1426-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1426-104">`TRIM` 関数は、先頭と末尾のスペースを切り捨ててから *文字列* 値として指定されたテキスト文字列を返し、その後単語間の複数のスペースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="f1426-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1426-105">構文</span><span class="sxs-lookup"><span data-stu-id="f1426-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="f1426-106">引数</span><span class="sxs-lookup"><span data-stu-id="f1426-106">Arguments</span></span>

<span data-ttu-id="f1426-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="f1426-107">`text`: *String*</span></span>

<span data-ttu-id="f1426-108">*文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="f1426-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1426-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="f1426-109">Return values</span></span>

<span data-ttu-id="f1426-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="f1426-110">*String*</span></span>

<span data-ttu-id="f1426-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="f1426-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f1426-112">例</span><span class="sxs-lookup"><span data-stu-id="f1426-112">Example</span></span>

<span data-ttu-id="f1426-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` は、**"Sample text"** を返します。</span><span class="sxs-lookup"><span data-stu-id="f1426-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1426-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f1426-114">Additional resources</span></span>

[<span data-ttu-id="f1426-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="f1426-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]