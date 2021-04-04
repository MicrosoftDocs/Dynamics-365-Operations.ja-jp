---
title: ISOCREDREF ER 関数
description: このトピックでは、ISOCREDREF 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563416"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="6d5c3-103">ISOCREDREF ER 関数</span><span class="sxs-lookup"><span data-stu-id="6d5c3-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d5c3-104">`ISOCREDREF` 機能は、指定された請求書番号の数字とアルファベット記号に基づいて、国際標準化機構 (ISO) 送金受取人参照情報を表す *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="6d5c3-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d5c3-105">構文</span><span class="sxs-lookup"><span data-stu-id="6d5c3-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="6d5c3-106">引数</span><span class="sxs-lookup"><span data-stu-id="6d5c3-106">Arguments</span></span>

<span data-ttu-id="6d5c3-107">`invoice number digits`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="6d5c3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="6d5c3-108">請求書番号の桁数を表すテキスト値。</span><span class="sxs-lookup"><span data-stu-id="6d5c3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d5c3-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="6d5c3-109">Return values</span></span>

<span data-ttu-id="6d5c3-110">*文字列*</span><span class="sxs-lookup"><span data-stu-id="6d5c3-110">*String*</span></span>

<span data-ttu-id="6d5c3-111">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="6d5c3-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6d5c3-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="6d5c3-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="6d5c3-113">ISO 準拠ではないアルファベットの記号を削除するには、`invoice number digits` 引数はこの関数へ渡す前に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d5c3-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="6d5c3-114">例</span><span class="sxs-lookup"><span data-stu-id="6d5c3-114">Example</span></span>

<span data-ttu-id="6d5c3-115">`ISOCredRef ("VEND-200002")` は、**"RF23VEND-200002"** を返します。</span><span class="sxs-lookup"><span data-stu-id="6d5c3-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d5c3-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6d5c3-116">Additional resources</span></span>

[<span data-ttu-id="6d5c3-117">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="6d5c3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]