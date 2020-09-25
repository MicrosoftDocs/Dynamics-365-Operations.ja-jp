---
title: ENUMERATE ER 関数
description: このトピックでは、ENUMERATE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: e1871ee41267c2c0e8b35007a47c9601079f05d7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745252"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="da7ee-103">ENUMERATE ER 関数</span><span class="sxs-lookup"><span data-stu-id="da7ee-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da7ee-104">`ENUMERATE` 関数は、指定されたリストの列挙されたレコードで構成される新しい*レコード リスト*値を返します。</span><span class="sxs-lookup"><span data-stu-id="da7ee-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="da7ee-105">構文</span><span class="sxs-lookup"><span data-stu-id="da7ee-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="da7ee-106">引数</span><span class="sxs-lookup"><span data-stu-id="da7ee-106">Arguments</span></span>

<span data-ttu-id="da7ee-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="da7ee-107">`list`: *Record list*</span></span>

<span data-ttu-id="da7ee-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="da7ee-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="da7ee-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="da7ee-109">Return values</span></span>

<span data-ttu-id="da7ee-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="da7ee-110">*Record list*</span></span>

<span data-ttu-id="da7ee-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="da7ee-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="da7ee-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="da7ee-112">Usage notes</span></span>

<span data-ttu-id="da7ee-113">返される列挙されたレコードのリストによって、次の追加の要素が公開されます。</span><span class="sxs-lookup"><span data-stu-id="da7ee-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="da7ee-114">フィールドのレコード (**値**コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="da7ee-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="da7ee-115">現在のレコード インデックス (**番号** コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="da7ee-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="da7ee-116">例</span><span class="sxs-lookup"><span data-stu-id="da7ee-116">Example</span></span>

<span data-ttu-id="da7ee-117">次の図では、**列挙型** データ ソースは、VendTable テーブルを参照する **仕入先** データ ソースの仕入先レコードの列挙型リストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="da7ee-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="da7ee-118">次の図は、電子申告 (ER) 形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="da7ee-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="da7ee-119">この形式では、XML 形式で出力を生成するために、バインディングが作成されます。</span><span class="sxs-lookup"><span data-stu-id="da7ee-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="da7ee-120">この出力では、個々の仕入先が列挙型ノードとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="da7ee-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="da7ee-121">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="da7ee-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="da7ee-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="da7ee-122">Additional resources</span></span>

[<span data-ttu-id="da7ee-123">リスト機能</span><span class="sxs-lookup"><span data-stu-id="da7ee-123">List functions</span></span>](er-functions-category-list.md)
