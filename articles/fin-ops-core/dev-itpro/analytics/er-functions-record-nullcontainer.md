---
title: NULLCONTAINER ER 関数
description: このトピックでは、NULLCONTAINER 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1932116b67cef79622f0f6152b168b5961a72c7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683041"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="85489-103">NULLCONTAINER ER 関数</span><span class="sxs-lookup"><span data-stu-id="85489-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85489-104">`NULLCONTAINER` 関数は、指定されたリストまたはレコードと同じ構造を持つ *コンテナー (レコード)* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="85489-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="85489-105">構文</span><span class="sxs-lookup"><span data-stu-id="85489-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="85489-106">引数</span><span class="sxs-lookup"><span data-stu-id="85489-106">Arguments</span></span>

<span data-ttu-id="85489-107">`list`: *レコード リスト* または *コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="85489-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="85489-108">*レコード リスト* または *コンテナー (レコード)* タイプのデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="85489-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="85489-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="85489-109">Return values</span></span>

<span data-ttu-id="85489-110">*コンテナー (レコード)*</span><span class="sxs-lookup"><span data-stu-id="85489-110">*Container (record)*</span></span>

<span data-ttu-id="85489-111">結果レコード値。</span><span class="sxs-lookup"><span data-stu-id="85489-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="85489-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="85489-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="85489-113">この関数は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="85489-113">This function is obsolete.</span></span> <span data-ttu-id="85489-114">代わりに `EMPTYRECORD` 関数を使用してください。</span><span class="sxs-lookup"><span data-stu-id="85489-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="85489-115">詳細については、[EMPTYRECORD](er-functions-record-emptyrecord.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="85489-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="85489-116">例</span><span class="sxs-lookup"><span data-stu-id="85489-116">Example</span></span>

<span data-ttu-id="85489-117">`NULLCONTAINER (SPLIT ("abc", 1))` は、`SPLIT` 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="85489-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="85489-118">詳細については、[SPLIT](er-functions-list-split.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="85489-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85489-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="85489-119">Additional resources</span></span>

[<span data-ttu-id="85489-120">レコード機能</span><span class="sxs-lookup"><span data-stu-id="85489-120">Record functions</span></span>](er-functions-category-record.md)
