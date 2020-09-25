---
title: EMPTYLIST ER 関数
description: このトピックでは、EMPTYLIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745324"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="edb25-103">EMPTYLIST ER 関数</span><span class="sxs-lookup"><span data-stu-id="edb25-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edb25-104">`EMPTYLIST` 関数は、指定されたリストをリスト構造のソースとして使用し、空の*レコード リスト*値を返します。</span><span class="sxs-lookup"><span data-stu-id="edb25-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb25-105">構文</span><span class="sxs-lookup"><span data-stu-id="edb25-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="edb25-106">引数</span><span class="sxs-lookup"><span data-stu-id="edb25-106">Arguments</span></span>

<span data-ttu-id="edb25-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="edb25-107">`list`: *Record list*</span></span>

<span data-ttu-id="edb25-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="edb25-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="edb25-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="edb25-109">Return values</span></span>

<span data-ttu-id="edb25-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="edb25-110">*Record list*</span></span>

<span data-ttu-id="edb25-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="edb25-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="edb25-112">例</span><span class="sxs-lookup"><span data-stu-id="edb25-112">Example</span></span>

<span data-ttu-id="edb25-113">`EMPTYLIST (SPLIT ("abc", 1))` は、使用する `SPLIT` 関数によって返されるリストと同じ構造を持つ新しい空のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="edb25-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edb25-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="edb25-114">Additional resources</span></span>

[<span data-ttu-id="edb25-115">リスト機能</span><span class="sxs-lookup"><span data-stu-id="edb25-115">List functions</span></span>](er-functions-category-list.md)
