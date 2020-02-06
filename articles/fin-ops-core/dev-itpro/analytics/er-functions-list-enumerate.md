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
ms.openlocfilehash: f0a1c83ee869810e816b6d32ea890d172d2910e5
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916226"
---
# <span data-ttu-id="3ca53-103"><a name="ENUMERATE">ENUMERATE ER 関数</a></span><span class="sxs-lookup"><span data-stu-id="3ca53-103"><a name="ENUMERATE">ENUMERATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ca53-104">`ENUMERATE` 関数は、指定されたリストの列挙されたレコードで構成される新しい*レコード リスト*値を返します。</span><span class="sxs-lookup"><span data-stu-id="3ca53-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca53-105">構文</span><span class="sxs-lookup"><span data-stu-id="3ca53-105">Syntax</span></span>

```
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="3ca53-106">引数</span><span class="sxs-lookup"><span data-stu-id="3ca53-106">Arguments</span></span>

<span data-ttu-id="3ca53-107">`list`: *レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="3ca53-107">`list`: *Record list*</span></span>

<span data-ttu-id="3ca53-108">*レコード リスト* データ型のデータ ソースの項目の有効なパス。</span><span class="sxs-lookup"><span data-stu-id="3ca53-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ca53-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="3ca53-109">Return values</span></span>

<span data-ttu-id="3ca53-110">*レコード リスト*</span><span class="sxs-lookup"><span data-stu-id="3ca53-110">*Record list*</span></span>

<span data-ttu-id="3ca53-111">レコードの結果リスト。</span><span class="sxs-lookup"><span data-stu-id="3ca53-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3ca53-112">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="3ca53-112">Usage notes</span></span>

<span data-ttu-id="3ca53-113">返される列挙されたレコードのリストによって、次の追加の要素が公開されます。</span><span class="sxs-lookup"><span data-stu-id="3ca53-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="3ca53-114">フィールドのレコード (**値**コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="3ca53-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="3ca53-115">現在のレコード インデックス (\*\*番号 \*\*コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="3ca53-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="3ca53-116">例</span><span class="sxs-lookup"><span data-stu-id="3ca53-116">Example</span></span>

<span data-ttu-id="3ca53-117">次の図では、**列挙型** データ ソースは、VendTable テーブルを参照する **仕入先** データ ソースの仕入先レコードの列挙型リストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="3ca53-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="3ca53-118">次の図は、電子申告 (ER) 形式を示しています。</span><span class="sxs-lookup"><span data-stu-id="3ca53-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="3ca53-119">この形式では、XML 形式で出力を生成するために、バインディングが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3ca53-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="3ca53-120">この出力では、個々の仕入先が列挙型ノードとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ca53-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="3ca53-121">次の図は、設計された形式が実行される際の結果を示します。</span><span class="sxs-lookup"><span data-stu-id="3ca53-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="3ca53-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3ca53-122">Additional resources</span></span>

[<span data-ttu-id="3ca53-123">リスト機能</span><span class="sxs-lookup"><span data-stu-id="3ca53-123">List functions</span></span>](er-functions-category-list.md)