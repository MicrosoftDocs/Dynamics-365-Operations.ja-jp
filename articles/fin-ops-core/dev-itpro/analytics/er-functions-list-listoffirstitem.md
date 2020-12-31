---
title: LISTOFFIRSTITEM ER 関数
description: このトピックでは、LISTOFFIRSTITEM 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ea81bce8cd6b922f3ef1d53ec0c4b2574780377
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686491"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="e287f-103">LISTOFFIRSTITEM ER 関数</span><span class="sxs-lookup"><span data-stu-id="e287f-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e287f-104">`LISTOFFIRSTITEM` 関数は、指定されたリストの最初のレコードのみで構成される *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="e287f-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="e287f-105">構文</span><span class="sxs-lookup"><span data-stu-id="e287f-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="e287f-106">引数</span><span class="sxs-lookup"><span data-stu-id="e287f-106">Arguments</span></span>

<span data-ttu-id="e287f-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="e287f-107">`list`: *Record list*</span></span>

<span data-ttu-id="e287f-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="e287f-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e287f-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e287f-109">Return values</span></span>

<span data-ttu-id="e287f-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="e287f-110">*Record list*</span></span>

<span data-ttu-id="e287f-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="e287f-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="e287f-112">例</span><span class="sxs-lookup"><span data-stu-id="e287f-112">Example</span></span>

<span data-ttu-id="e287f-113">式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="e287f-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e287f-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e287f-114">Additional resources</span></span>

[<span data-ttu-id="e287f-115">リスト機能</span><span class="sxs-lookup"><span data-stu-id="e287f-115">List functions</span></span>](er-functions-category-list.md)
