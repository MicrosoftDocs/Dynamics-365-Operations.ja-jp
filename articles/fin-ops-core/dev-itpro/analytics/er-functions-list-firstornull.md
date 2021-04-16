---
title: FIRSTORNULL ER 関数
description: このトピックでは、FIRSTORNULL 電子申告 (ER) 関数の使用方法について説明します
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753219"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="c43d5-103">FIRSTORNULL ER 関数</span><span class="sxs-lookup"><span data-stu-id="c43d5-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c43d5-104">`FIRSTORNULL` 関数は、レコードが空でない場合に、指定されたリストの最初のレコードを *コンテナー (レコード)* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="c43d5-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="c43d5-105">レコードが空の場合、この関数は null *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="c43d5-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43d5-106">構文</span><span class="sxs-lookup"><span data-stu-id="c43d5-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="c43d5-107">引数</span><span class="sxs-lookup"><span data-stu-id="c43d5-107">Arguments</span></span>

<span data-ttu-id="c43d5-108">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="c43d5-108">`list`: *Record list*</span></span>

<span data-ttu-id="c43d5-109">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="c43d5-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c43d5-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="c43d5-110">Return values</span></span>

<span data-ttu-id="c43d5-111">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="c43d5-111">*Container (record)*</span></span>

<span data-ttu-id="c43d5-112">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="c43d5-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="c43d5-113">例</span><span class="sxs-lookup"><span data-stu-id="c43d5-113">Example</span></span>

<span data-ttu-id="c43d5-114">式 `FIRSTORNULL(SPLIT("",1)).Value` は空の文字列 (**""**) を返します。</span><span class="sxs-lookup"><span data-stu-id="c43d5-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c43d5-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c43d5-115">Additional resources</span></span>

[<span data-ttu-id="c43d5-116">リスト機能</span><span class="sxs-lookup"><span data-stu-id="c43d5-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]