---
title: ISEMPTY ER 関数
description: このトピックでは、ISEMPTY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916134"
---
# <span data-ttu-id="1cdda-103"><a name="ISEMPTY">ISEMPTY ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="1cdda-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cdda-104">`ISEMPTY` 関数は、指定したリストにレコードが含まれていない場合、**TRUE** の*ブール*値を返します。</span><span class="sxs-lookup"><span data-stu-id="1cdda-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="1cdda-105">それ以外の場合は、**FALSE** の*ブール*値が返されます。</span><span class="sxs-lookup"><span data-stu-id="1cdda-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdda-106">構文</span><span class="sxs-lookup"><span data-stu-id="1cdda-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="1cdda-107">引数</span><span class="sxs-lookup"><span data-stu-id="1cdda-107">Arguments</span></span>

<span data-ttu-id="1cdda-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="1cdda-108">`list`: *Record list*</span></span>

<span data-ttu-id="1cdda-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="1cdda-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1cdda-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="1cdda-110">Return values</span></span>

<span data-ttu-id="1cdda-111">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="1cdda-111">*Boolean*</span></span>

<span data-ttu-id="1cdda-112">結果*ブール*値。</span><span class="sxs-lookup"><span data-stu-id="1cdda-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1cdda-113">例 1</span><span class="sxs-lookup"><span data-stu-id="1cdda-113">Example 1</span></span>

<span data-ttu-id="1cdda-114">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `ISEMPTY(DS)` は **FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="1cdda-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1cdda-115">例 2</span><span class="sxs-lookup"><span data-stu-id="1cdda-115">Example 2</span></span>

<span data-ttu-id="1cdda-116">式 `ISEMPTY (SPLIT ("",1))` は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="1cdda-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1cdda-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1cdda-117">Additional resources</span></span>

[<span data-ttu-id="1cdda-118">リスト機能</span><span class="sxs-lookup"><span data-stu-id="1cdda-118">List functions</span></span>](er-functions-category-list.md)