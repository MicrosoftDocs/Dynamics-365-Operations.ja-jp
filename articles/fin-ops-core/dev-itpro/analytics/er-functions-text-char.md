---
title: CHAR ER 関数
description: このトピックでは、CHAR 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915743"
---
# <span data-ttu-id="c6471-103"><a name="CHAR">CHAR ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="c6471-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6471-104">`CHAR` 関数は、指定された Unicode 番号で参照される単一の文字を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="c6471-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6471-105">構文</span><span class="sxs-lookup"><span data-stu-id="c6471-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="c6471-106">引数</span><span class="sxs-lookup"><span data-stu-id="c6471-106">Arguments</span></span>

<span data-ttu-id="c6471-107">`number`: *整数*</span><span class="sxs-lookup"><span data-stu-id="c6471-107">`number`: *Integer*</span></span>

<span data-ttu-id="c6471-108">予想される単一文字に対応する番号。</span><span class="sxs-lookup"><span data-stu-id="c6471-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6471-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="c6471-109">Return values</span></span>

<span data-ttu-id="c6471-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="c6471-110">*String*</span></span>

<span data-ttu-id="c6471-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="c6471-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c6471-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="c6471-112">Usage notes</span></span>

<span data-ttu-id="c6471-113">この機能を返す文字列は、親 **FILE** 形式の要素で選択したエンコードによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c6471-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="c6471-114">サポートされているエンコードの一覧については、[エンコーディング クラス](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx) で参照できます。</span><span class="sxs-lookup"><span data-stu-id="c6471-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="c6471-115">例</span><span class="sxs-lookup"><span data-stu-id="c6471-115">Example</span></span>

<span data-ttu-id="c6471-116">`CHAR (255)` は、**"ÿ"** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6471-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6471-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6471-117">Additional resources</span></span>

[<span data-ttu-id="c6471-118">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="c6471-118">Text functions</span></span>](er-functions-category-text.md)
