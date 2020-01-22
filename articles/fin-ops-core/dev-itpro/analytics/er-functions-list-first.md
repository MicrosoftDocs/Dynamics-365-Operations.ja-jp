---
title: FIRST ER 関数
description: このトピックでは、FIRST 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917353"
---
# <span data-ttu-id="ce6a4-103"><a name="FIRST">FIRST ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="ce6a4-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce6a4-104">`FIRST` 関数は、リストが空でない場合に、指定されたリストの最初のレコードを*コンテナー (レコード)* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="ce6a4-105">リストが空の場合、この関数は例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6a4-106">構文</span><span class="sxs-lookup"><span data-stu-id="ce6a4-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="ce6a4-107">引数</span><span class="sxs-lookup"><span data-stu-id="ce6a4-107">Arguments</span></span>

<span data-ttu-id="ce6a4-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="ce6a4-108">`list`: *Record list*</span></span>

<span data-ttu-id="ce6a4-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ce6a4-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="ce6a4-110">Return values</span></span>

<span data-ttu-id="ce6a4-111">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="ce6a4-111">*Container (record)*</span></span>

<span data-ttu-id="ce6a4-112">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ce6a4-113">例 1</span><span class="sxs-lookup"><span data-stu-id="ce6a4-113">Example 1</span></span>

<span data-ttu-id="ce6a4-114">式 `FIRST(SPLIT("ABC",1)).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ce6a4-115">例 2</span><span class="sxs-lookup"><span data-stu-id="ce6a4-115">Example 2</span></span>

<span data-ttu-id="ce6a4-116">式 `FIRST(SPLIT("",1)).Value` は、実行時に例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="ce6a4-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce6a4-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ce6a4-117">Additional resources</span></span>

[<span data-ttu-id="ce6a4-118">リスト機能</span><span class="sxs-lookup"><span data-stu-id="ce6a4-118">List functions</span></span>](er-functions-category-list.md)
