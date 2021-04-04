---
title: TABLENAME2ID ER 関数
description: このトピックでは、TABLENAME2ID 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 49370af4ebb7552dd3aff4512890fd93fa67c72d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563273"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="0f808-103">TABLENAME2ID ER 関数</span><span class="sxs-lookup"><span data-stu-id="0f808-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f808-104">`TABLENAME2ID` 関数は、*整数* 値として指定されたテーブル名に対応するテーブル ID の数値表現を返します。</span><span class="sxs-lookup"><span data-stu-id="0f808-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f808-105">構文</span><span class="sxs-lookup"><span data-stu-id="0f808-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="0f808-106">引数</span><span class="sxs-lookup"><span data-stu-id="0f808-106">Arguments</span></span>

<span data-ttu-id="0f808-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0f808-107">`text`: *String*</span></span>

<span data-ttu-id="0f808-108">有効なテーブル名を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="0f808-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="0f808-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0f808-109">Return values</span></span>

<span data-ttu-id="0f808-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="0f808-110">*Integer*</span></span>

<span data-ttu-id="0f808-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="0f808-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0f808-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0f808-112">Usage notes</span></span>

<span data-ttu-id="0f808-113">この関数を実行すると、同じ会社名が使用されている場合でも、Microsoft Dynamics 365 Finance の異なるインスタンスに結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="0f808-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="0f808-114">例</span><span class="sxs-lookup"><span data-stu-id="0f808-114">Example</span></span>

<span data-ttu-id="0f808-115">`TABLENAME2ID ("Intrastat")` は、**1510** を返します。</span><span class="sxs-lookup"><span data-stu-id="0f808-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f808-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0f808-116">Additional resources</span></span>

[<span data-ttu-id="0f808-117">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="0f808-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]