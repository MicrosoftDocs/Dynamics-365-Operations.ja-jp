---
title: TABLENAME2ID ER 関数
description: このトピックでは、TABLENAME2ID 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 77d889f75f38b3c07855a96bf65f1456ac2f42e2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915812"
---
# <span data-ttu-id="eb89c-103"><a name="TABLENAME2ID">TABLENAME2ID ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="eb89c-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb89c-104">`TABLENAME2ID` 関数は、*整数*値として指定されたテーブル名に対応するテーブル ID の数値表現を返します。</span><span class="sxs-lookup"><span data-stu-id="eb89c-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb89c-105">構文</span><span class="sxs-lookup"><span data-stu-id="eb89c-105">Syntax</span></span>

```
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="eb89c-106">引数</span><span class="sxs-lookup"><span data-stu-id="eb89c-106">Arguments</span></span>

<span data-ttu-id="eb89c-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="eb89c-107">`text`: *String*</span></span>

<span data-ttu-id="eb89c-108">有効なテーブル名を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="eb89c-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb89c-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb89c-109">Return values</span></span>

<span data-ttu-id="eb89c-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="eb89c-110">*Integer*</span></span>

<span data-ttu-id="eb89c-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="eb89c-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="eb89c-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="eb89c-112">Usage notes</span></span>

<span data-ttu-id="eb89c-113">この関数を実行すると、同じ会社名が使用されている場合でも、Microsoft Dynamics 365 Finance の異なるインスタンスに結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="eb89c-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="eb89c-114">例</span><span class="sxs-lookup"><span data-stu-id="eb89c-114">Example</span></span>

<span data-ttu-id="eb89c-115">`TABLENAME2ID ("Intrastat")` は、**1510** を返します。</span><span class="sxs-lookup"><span data-stu-id="eb89c-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb89c-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="eb89c-116">Additional resources</span></span>

[<span data-ttu-id="eb89c-117">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="eb89c-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)