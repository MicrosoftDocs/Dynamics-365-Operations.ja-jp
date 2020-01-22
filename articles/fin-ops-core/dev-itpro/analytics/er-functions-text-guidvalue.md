---
title: GUIDVALUE ER 関数
description: このトピックでは、GUIDVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: be5e8e7625d0226c9eb59efd3217fce7b8eba086
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915697"
---
# <span data-ttu-id="0e45b-103"><a name="GUIDVALUE">GUIDVALUE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="0e45b-103"><a name="GUIDVALUE">GUIDVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e45b-104">`GUIDVALUE` 関数は、指定された*文字列*型の入力を *GUID* 型のデータ品目に変換します。</span><span class="sxs-lookup"><span data-stu-id="0e45b-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e45b-105">構文</span><span class="sxs-lookup"><span data-stu-id="0e45b-105">Syntax</span></span>

```
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="0e45b-106">引数</span><span class="sxs-lookup"><span data-stu-id="0e45b-106">Arguments</span></span>

<span data-ttu-id="0e45b-107">`input`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="0e45b-107">`input`: *String*</span></span>

<span data-ttu-id="0e45b-108">*文字列*型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="0e45b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e45b-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="0e45b-109">Return values</span></span>

<span data-ttu-id="0e45b-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0e45b-110">*GUID*</span></span>

<span data-ttu-id="0e45b-111">結果のグローバル一意識別子 (GUID) 値。</span><span class="sxs-lookup"><span data-stu-id="0e45b-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0e45b-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="0e45b-112">Usage notes</span></span>

<span data-ttu-id="0e45b-113">逆方向に変換を行うには (つまり、*GUID* データ型の指定された入力を*文字列*データ型のデータ項目に変換するには)、[TEXT](er-functions-text-text.md) 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="0e45b-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="0e45b-114">例</span><span class="sxs-lookup"><span data-stu-id="0e45b-114">Example</span></span>

<span data-ttu-id="0e45b-115">モデル マッピングでは、次のデータ ソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="0e45b-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0e45b-116">`GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")` 式を含む*計算済フィールド* タイプの **myID** データ ソース</span><span class="sxs-lookup"><span data-stu-id="0e45b-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="0e45b-117">UserInfo テーブルを参照する*テーブル レコード*型の**ユーザー**データ ソース</span><span class="sxs-lookup"><span data-stu-id="0e45b-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="0e45b-118">その後、`FILTER (Users, Users.objectId = myID)` などの式を使用して、*GUID* データ型の **Objectld** フィールドで UserInfo テーブルをフィルタ処理できます。</span><span class="sxs-lookup"><span data-stu-id="0e45b-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e45b-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0e45b-119">Additional resources</span></span>

[<span data-ttu-id="0e45b-120">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="0e45b-120">Text functions</span></span>](er-functions-category-text.md)
