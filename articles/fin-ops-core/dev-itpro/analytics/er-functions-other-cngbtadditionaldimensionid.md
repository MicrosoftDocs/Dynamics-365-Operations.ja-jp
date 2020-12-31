---
title: CN_GBT_ADDITIONALDIMENSIONID ER 関数
description: このトピックでは、CN_GBT_ADDITIONALDIMENSIONID 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38908c63c35465747505479bc983ada891f9e2bf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686813"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a><span data-ttu-id="c3cc5-103">CN_GBT_ADDITIONALDIMENSIONID ER 関数</span><span class="sxs-lookup"><span data-stu-id="c3cc5-103">CN_GBT_ADDITIONALDIMENSIONID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3cc5-104">`CN_GBT_ADDITIONALDIMENSIONID` 関数は、指定された文字列から取得された単一の財務分析コード ID を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-104">The `CN_GBT_ADDITIONALDIMENSIONID` function returns a *String* value that represents a single financial dimension ID that is taken from the specified string.</span></span> <span data-ttu-id="c3cc5-105">指定された文字列は、ID のコンマ区切りのリストとしてすべての分析コードを示します。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-105">The specified string presents all dimensions as a comma-separated list of IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cc5-106">構文</span><span class="sxs-lookup"><span data-stu-id="c3cc5-106">Syntax</span></span>

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a><span data-ttu-id="c3cc5-107">引数</span><span class="sxs-lookup"><span data-stu-id="c3cc5-107">Arguments</span></span>

<span data-ttu-id="c3cc5-108">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="c3cc5-108">`text`: *String*</span></span>

<span data-ttu-id="c3cc5-109">ID のコンマ区切りのリストとしてすべての分析コードを示す *文字列* 値。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-109">A *String* value that presents all dimensions as a comma-separated list of IDs.</span></span>

<span data-ttu-id="c3cc5-110">`number`: 整数</span><span class="sxs-lookup"><span data-stu-id="c3cc5-110">`number`: Integer</span></span>

<span data-ttu-id="c3cc5-111">指定された文字列で要求された分析コードの順序コードを定義する *整数* 値。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-111">An *Integer* value that defines the sequence code of the requested dimension in the specified string.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3cc5-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="c3cc5-112">Return values</span></span>

<span data-ttu-id="c3cc5-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="c3cc5-113">*String*</span></span>

<span data-ttu-id="c3cc5-114">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c3cc5-115">例</span><span class="sxs-lookup"><span data-stu-id="c3cc5-115">Example</span></span>

<span data-ttu-id="c3cc5-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` は、**"CC"** を返します。</span><span class="sxs-lookup"><span data-stu-id="c3cc5-116">`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` returns **"CC"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3cc5-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c3cc5-117">Additional resources</span></span>

[<span data-ttu-id="c3cc5-118">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="c3cc5-118">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
