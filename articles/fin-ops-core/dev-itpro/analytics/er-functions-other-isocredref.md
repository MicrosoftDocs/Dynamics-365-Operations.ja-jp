---
title: ISOCREDREF ER 関数
description: このトピックでは、ISOCREDREF 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041380"
---
# <span data-ttu-id="2cde5-103"><a name="ISOCREDREF">ISOCREDREF ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="2cde5-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cde5-104">`ISOCREDREF` 機能は、指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="2cde5-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cde5-105">構文</span><span class="sxs-lookup"><span data-stu-id="2cde5-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="2cde5-106">引数</span><span class="sxs-lookup"><span data-stu-id="2cde5-106">Arguments</span></span>

<span data-ttu-id="2cde5-107">`invoice number digits`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="2cde5-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="2cde5-108">請求書番号の桁数を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="2cde5-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="2cde5-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="2cde5-109">Return values</span></span>

<span data-ttu-id="2cde5-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="2cde5-110">*String*</span></span>

<span data-ttu-id="2cde5-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="2cde5-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2cde5-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="2cde5-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="2cde5-113">ISO 準拠ではないアルファベットの記号を削除するには、`invoice number digits` 引数はこの関数へ渡す前に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2cde5-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="2cde5-114">例</span><span class="sxs-lookup"><span data-stu-id="2cde5-114">Example</span></span>

<span data-ttu-id="2cde5-115">`ISOCredRef ("VEND-200002")` は、**"RF23VEND-200002"** を返します。</span><span class="sxs-lookup"><span data-stu-id="2cde5-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2cde5-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2cde5-116">Additional resources</span></span>

[<span data-ttu-id="2cde5-117">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="2cde5-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
