---
title: EMPTYRECORD ER 機能
description: このトピックでは、EMPTYRECORD 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746534"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="3cb2f-103">EMPTYRECORD ER 機能</span><span class="sxs-lookup"><span data-stu-id="3cb2f-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cb2f-104">`EMPTYRECORD`関数は、指定されたリストまたはレコードと同じ構造を持つ *コンテナー (記録)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb2f-105">構文</span><span class="sxs-lookup"><span data-stu-id="3cb2f-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="3cb2f-106">引数</span><span class="sxs-lookup"><span data-stu-id="3cb2f-106">Arguments</span></span>

<span data-ttu-id="3cb2f-107">`list`: *レコード リスト* または *コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="3cb2f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="3cb2f-108">*レコード リスト* または *コンテナー (レコード)* タイプのデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3cb2f-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="3cb2f-109">Return values</span></span>

<span data-ttu-id="3cb2f-110">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="3cb2f-110">*Container (record)*</span></span>

<span data-ttu-id="3cb2f-111">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3cb2f-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="3cb2f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="3cb2f-113">null レコードは、すべてのフィールドが空の値があるレコードです。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="3cb2f-114">空の値が数字の場合は **0** (ゼロ)、文字列の場合、空の文字列などです。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="3cb2f-115">例</span><span class="sxs-lookup"><span data-stu-id="3cb2f-115">Example</span></span>

<span data-ttu-id="3cb2f-116">`EMPTYRECORD (SPLIT ("abc", 1))` は、`SPLIT` 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="3cb2f-117">詳細については、[SPLIT](er-functions-list-split.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3cb2f-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3cb2f-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3cb2f-118">Additional resources</span></span>

[<span data-ttu-id="3cb2f-119">レコード機能</span><span class="sxs-lookup"><span data-stu-id="3cb2f-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]