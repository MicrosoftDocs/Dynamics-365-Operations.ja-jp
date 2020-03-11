---
title: ISVALIDCHARACTERISO7064 ER 関数
description: このトピックでは、ISVALIDCHARACTERISO7064 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c858ad72db7afe63baca8288f312548c4fc37d5c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041403"
---
# <span data-ttu-id="c3482-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="c3482-103"><a name="ISVALIDCHARACTERISO7064">ISVALIDCHARACTERISO7064 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3482-104">`ISVALIDCHARACTERISO7064` 機能は、指定された文字列が有効な国際銀行番号 (IBAN) を表す場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="c3482-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="c3482-105">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c3482-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3482-106">構文</span><span class="sxs-lookup"><span data-stu-id="c3482-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="c3482-107">引数</span><span class="sxs-lookup"><span data-stu-id="c3482-107">Arguments</span></span>

<span data-ttu-id="c3482-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="c3482-108">`text`: *String*</span></span>

<span data-ttu-id="c3482-109">IBAN を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="c3482-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3482-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c3482-110">Return values</span></span>

<span data-ttu-id="c3482-111">*文字列*</span><span class="sxs-lookup"><span data-stu-id="c3482-111">*String*</span></span>

<span data-ttu-id="c3482-112">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="c3482-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3482-113">例</span><span class="sxs-lookup"><span data-stu-id="c3482-113">Example</span></span>

<span data-ttu-id="c3482-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` は、**TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="c3482-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="c3482-115">`ISVALIDCHARACTERISO7064 ("AT61")` は、**FALSE** 返します。</span><span class="sxs-lookup"><span data-stu-id="c3482-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3482-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c3482-116">Additional resources</span></span>

[<span data-ttu-id="c3482-117">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="c3482-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
