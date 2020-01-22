---
title: TRIM ER 関数
description: このトピックでは、TRIM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915536"
---
# <span data-ttu-id="42c90-103"><a name="TRIM">TRIM ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="42c90-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42c90-104">`TRIM` 関数は、先頭と末尾のスペースを切り捨ててから*文字列*値として指定されたテキスト文字列を返し、その後単語間の複数のスペースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="42c90-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c90-105">構文</span><span class="sxs-lookup"><span data-stu-id="42c90-105">Syntax</span></span>

```
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="42c90-106">引数</span><span class="sxs-lookup"><span data-stu-id="42c90-106">Arguments</span></span>

<span data-ttu-id="42c90-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="42c90-107">`text`: *String*</span></span>

<span data-ttu-id="42c90-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="42c90-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="42c90-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="42c90-109">Return values</span></span>

<span data-ttu-id="42c90-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="42c90-110">*String*</span></span>

<span data-ttu-id="42c90-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="42c90-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="42c90-112">例</span><span class="sxs-lookup"><span data-stu-id="42c90-112">Example</span></span>

<span data-ttu-id="42c90-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` は、**"Sample text"** を返します。</span><span class="sxs-lookup"><span data-stu-id="42c90-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42c90-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="42c90-114">Additional resources</span></span>

[<span data-ttu-id="42c90-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="42c90-115">Text functions</span></span>](er-functions-category-text.md)
