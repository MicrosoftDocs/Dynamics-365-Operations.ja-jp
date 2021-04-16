---
title: ISEMPTY ER 関数
description: このトピックでは、ISEMPTY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 9c33e8b613bf5bf5bc17a42a7668d4cc4ee58e53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750439"
---
# <a name="isempty-er-function"></a><span data-ttu-id="c6bb8-103">ISEMPTY ER 関数</span><span class="sxs-lookup"><span data-stu-id="c6bb8-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6bb8-104">`ISEMPTY` 関数は、指定したリストにレコードが含まれていない場合、**TRUE** の *ブール* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="c6bb8-105">それ以外の場合は、**FALSE** の *ブール* 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6bb8-106">構文</span><span class="sxs-lookup"><span data-stu-id="c6bb8-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="c6bb8-107">引数</span><span class="sxs-lookup"><span data-stu-id="c6bb8-107">Arguments</span></span>

<span data-ttu-id="c6bb8-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="c6bb8-108">`list`: *Record list*</span></span>

<span data-ttu-id="c6bb8-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c6bb8-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c6bb8-110">Return values</span></span>

<span data-ttu-id="c6bb8-111">*ブール型*</span><span class="sxs-lookup"><span data-stu-id="c6bb8-111">*Boolean*</span></span>

<span data-ttu-id="c6bb8-112">結果 *ブール* 値。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c6bb8-113">例 1</span><span class="sxs-lookup"><span data-stu-id="c6bb8-113">Example 1</span></span>

<span data-ttu-id="c6bb8-114">*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("A|B|C", "|")` が含まれている場合、式 `ISEMPTY(DS)` は **FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c6bb8-115">例 2</span><span class="sxs-lookup"><span data-stu-id="c6bb8-115">Example 2</span></span>

<span data-ttu-id="c6bb8-116">式 `ISEMPTY (SPLIT ("",1))` は **TRUE** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6bb8-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6bb8-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6bb8-117">Additional resources</span></span>

[<span data-ttu-id="c6bb8-118">リスト機能</span><span class="sxs-lookup"><span data-stu-id="c6bb8-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]