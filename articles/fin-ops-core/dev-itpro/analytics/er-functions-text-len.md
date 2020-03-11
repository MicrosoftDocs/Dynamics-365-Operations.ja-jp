---
title: LEN ER 関数
description: このトピックでは、LEN 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041058"
---
# <span data-ttu-id="25333-103"><a name="LEN">LEN ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="25333-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25333-104">`LEN` 関数は、*整数*値として指定された文字列の文字数を返します。</span><span class="sxs-lookup"><span data-stu-id="25333-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="25333-105">構文</span><span class="sxs-lookup"><span data-stu-id="25333-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="25333-106">引数</span><span class="sxs-lookup"><span data-stu-id="25333-106">Arguments</span></span>

<span data-ttu-id="25333-107">`text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="25333-107">`text`: *String*</span></span>

<span data-ttu-id="25333-108">*文字列*値は、テキストを指定。</span><span class="sxs-lookup"><span data-stu-id="25333-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="25333-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="25333-109">Return values</span></span>

<span data-ttu-id="25333-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="25333-110">*Integer*</span></span>

<span data-ttu-id="25333-111">結果数値。</span><span class="sxs-lookup"><span data-stu-id="25333-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="25333-112">例</span><span class="sxs-lookup"><span data-stu-id="25333-112">Example</span></span>

<span data-ttu-id="25333-113">`LEN ("Sample")` は、**6** を返します。</span><span class="sxs-lookup"><span data-stu-id="25333-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25333-114">追加リソース</span><span class="sxs-lookup"><span data-stu-id="25333-114">Additional resources</span></span>

[<span data-ttu-id="25333-115">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="25333-115">Text functions</span></span>](er-functions-category-text.md)
