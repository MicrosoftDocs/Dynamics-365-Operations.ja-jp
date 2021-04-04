---
title: JSONVALUE ER 関数
description: このトピックでは、JSONVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570019"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="480be-103">JSONVALUE ER 関数</span><span class="sxs-lookup"><span data-stu-id="480be-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="480be-104">`JSONVALUE` 関数は指定した ID を持つスカラー値を抽出し、指定したパスでアクセスする JavaScript Object Notation (JSON) 形式で、データを解析します。</span><span class="sxs-lookup"><span data-stu-id="480be-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="480be-105">次に、抽出したスカラー値を *文字列* 値として返します。</span><span class="sxs-lookup"><span data-stu-id="480be-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="480be-106">構文</span><span class="sxs-lookup"><span data-stu-id="480be-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="480be-107">引数</span><span class="sxs-lookup"><span data-stu-id="480be-107">Arguments</span></span>

<span data-ttu-id="480be-108">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="480be-108">`input`: *String*</span></span>

<span data-ttu-id="480be-109">JSON データを含む *文字列* 型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="480be-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="480be-110">`path`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="480be-110">`path`: *String*</span></span>

<span data-ttu-id="480be-111">JSON データのスカラー値の識別子。</span><span class="sxs-lookup"><span data-stu-id="480be-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="480be-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="480be-112">Return values</span></span>

<span data-ttu-id="480be-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="480be-113">*String*</span></span>

<span data-ttu-id="480be-114">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="480be-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="480be-115">例</span><span class="sxs-lookup"><span data-stu-id="480be-115">Example</span></span>

<span data-ttu-id="480be-116">**JsonField** データ ソースは、JSON 形式の次のデータを含みます: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**。</span><span class="sxs-lookup"><span data-stu-id="480be-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="480be-117">この場合、`JSONVALUE (JsonField, "BuildNumber")` 式は *文字列* データ型の次の値を返します: **"7.3.1234.1"**。</span><span class="sxs-lookup"><span data-stu-id="480be-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="480be-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="480be-118">Additional resources</span></span>

[<span data-ttu-id="480be-119">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="480be-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]