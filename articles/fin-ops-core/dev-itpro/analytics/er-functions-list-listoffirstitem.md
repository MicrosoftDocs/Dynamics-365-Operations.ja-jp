---
title: LISTOFFIRSTITEM ER 関数
description: このトピックでは、LISTOFFIRSTITEM 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: 6dd6c84b43bea36bf922ae9348f95b450e882832
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750183"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="4c00d-103">LISTOFFIRSTITEM ER 関数</span><span class="sxs-lookup"><span data-stu-id="4c00d-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c00d-104">`LISTOFFIRSTITEM` 関数は、指定されたリストの最初のレコードのみで構成される *レコード リスト* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="4c00d-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c00d-105">構文</span><span class="sxs-lookup"><span data-stu-id="4c00d-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="4c00d-106">引数</span><span class="sxs-lookup"><span data-stu-id="4c00d-106">Arguments</span></span>

<span data-ttu-id="4c00d-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="4c00d-107">`list`: *Record list*</span></span>

<span data-ttu-id="4c00d-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="4c00d-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c00d-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="4c00d-109">Return values</span></span>

<span data-ttu-id="4c00d-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="4c00d-110">*Record list*</span></span>

<span data-ttu-id="4c00d-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="4c00d-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="4c00d-112">例</span><span class="sxs-lookup"><span data-stu-id="4c00d-112">Example</span></span>

<span data-ttu-id="4c00d-113">式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="4c00d-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c00d-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4c00d-114">Additional resources</span></span>

[<span data-ttu-id="4c00d-115">リスト機能</span><span class="sxs-lookup"><span data-stu-id="4c00d-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]