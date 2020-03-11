---
title: GETENUMVALUEBYNAME ER 機能
description: このトピックでは、GETENUMVALUEBYNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 87613978c149b5d41aefc58f9896424229819626
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041183"
---
# <span data-ttu-id="be642-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="be642-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be642-104">`GETENUMVALUEBYNAME` 関数は、*文字列*値して指定された列挙名を使用して、指定された列挙データソースの特定の*列挙*値を検索します。</span><span class="sxs-lookup"><span data-stu-id="be642-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="be642-105">*列挙*値が見つかった場合、関数によって返されます。</span><span class="sxs-lookup"><span data-stu-id="be642-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="be642-106">それ以外の場合、関数は **null** 列挙値を返します。</span><span class="sxs-lookup"><span data-stu-id="be642-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="be642-107">構文</span><span class="sxs-lookup"><span data-stu-id="be642-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="be642-108">引数</span><span class="sxs-lookup"><span data-stu-id="be642-108">Arguments</span></span>

<span data-ttu-id="be642-109">`enumeration data source path`: *列挙型*</span><span class="sxs-lookup"><span data-stu-id="be642-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="be642-110">次のいずれかの列挙型のデータ ソースの有効なパス。</span><span class="sxs-lookup"><span data-stu-id="be642-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="be642-111">電子申告 (ER) モデル 列挙型</span><span class="sxs-lookup"><span data-stu-id="be642-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="be642-112">ER 形式列挙型</span><span class="sxs-lookup"><span data-stu-id="be642-112">ER format enumeration</span></span>
- <span data-ttu-id="be642-113">Microsoft Dynamics 365 Finance 列挙型</span><span class="sxs-lookup"><span data-stu-id="be642-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="be642-114">`enumeration value text`: *文字列*</span><span class="sxs-lookup"><span data-stu-id="be642-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="be642-115">単一の列挙型値の名前を表す文字列値。</span><span class="sxs-lookup"><span data-stu-id="be642-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="be642-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="be642-116">Return values</span></span>

<span data-ttu-id="be642-117">Nullable *列挙*</span><span class="sxs-lookup"><span data-stu-id="be642-117">Nullable *Enum*</span></span>

<span data-ttu-id="be642-118">結果列挙型の値。</span><span class="sxs-lookup"><span data-stu-id="be642-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be642-119">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="be642-119">Usage notes</span></span>

<span data-ttu-id="be642-120">*文字列*値として指定された列挙型値の名前を使用して*列挙*値が見つからない場合は、例外がスローされません。</span><span class="sxs-lookup"><span data-stu-id="be642-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="be642-121">例</span><span class="sxs-lookup"><span data-stu-id="be642-121">Example</span></span>

<span data-ttu-id="be642-122">次の図では、**ReportDirection**の列挙はデータ モデルで導入されます。</span><span class="sxs-lookup"><span data-stu-id="be642-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="be642-123">列挙型値のラベルが定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be642-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="be642-124">次の図は、これらの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="be642-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="be642-125">**$Direction** データソースが、ER レポートで構成されます。</span><span class="sxs-lookup"><span data-stu-id="be642-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="be642-126">このデータ ソースは、**ReportDirection** モデルの列挙型に基づいて構成されます。</span><span class="sxs-lookup"><span data-stu-id="be642-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="be642-127">`$IsArrivals` 式は、この関数のパラメーターとして **$Direction** データ ソースに基づきモデル列挙型を使用するため設計されています。</span><span class="sxs-lookup"><span data-stu-id="be642-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="be642-128">この比較式の値は、**TRUE** です。</span><span class="sxs-lookup"><span data-stu-id="be642-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="be642-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="be642-129">Additional resources</span></span>

[<span data-ttu-id="be642-130">テキスト関数</span><span class="sxs-lookup"><span data-stu-id="be642-130">Text functions</span></span>](er-functions-category-text.md)
