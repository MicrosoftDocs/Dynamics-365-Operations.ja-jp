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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041978"
---
# <span data-ttu-id="aafab-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="aafab-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aafab-104">`LISTOFFIRSTITEM` 関数は、指定されたリストの最初のレコードのみで構成される*レコード リスト*値を返します。</span><span class="sxs-lookup"><span data-stu-id="aafab-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="aafab-105">構文</span><span class="sxs-lookup"><span data-stu-id="aafab-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="aafab-106">引数</span><span class="sxs-lookup"><span data-stu-id="aafab-106">Arguments</span></span>

<span data-ttu-id="aafab-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="aafab-107">`list`: *Record list*</span></span>

<span data-ttu-id="aafab-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="aafab-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="aafab-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="aafab-109">Return values</span></span>

<span data-ttu-id="aafab-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="aafab-110">*Record list*</span></span>

<span data-ttu-id="aafab-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="aafab-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="aafab-112">例</span><span class="sxs-lookup"><span data-stu-id="aafab-112">Example</span></span>

<span data-ttu-id="aafab-113">式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` はテキスト値 **"A"** を返します。</span><span class="sxs-lookup"><span data-stu-id="aafab-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aafab-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aafab-114">Additional resources</span></span>

[<span data-ttu-id="aafab-115">リスト機能</span><span class="sxs-lookup"><span data-stu-id="aafab-115">List functions</span></span>](er-functions-category-list.md)
