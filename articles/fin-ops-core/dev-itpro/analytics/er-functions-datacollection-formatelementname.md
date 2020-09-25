---
title: FORMATELEMENTNAME ER 関数
description: このトピックでは、FORMATELEMENTNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: e8be55d9a90e841d64288b0c618c0012912ddbab
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745636"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="92c9a-103">FORMATELEMENTNAME ER 関数</span><span class="sxs-lookup"><span data-stu-id="92c9a-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92c9a-104">`FORMATELEMENTNAME` 関数は、現在の電子申告 (ER) 形式要素の名前を表す*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="92c9a-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c9a-105">構文</span><span class="sxs-lookup"><span data-stu-id="92c9a-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="92c9a-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="92c9a-106">Return values</span></span>

<span data-ttu-id="92c9a-107">*文字列*</span><span class="sxs-lookup"><span data-stu-id="92c9a-107">*String*</span></span>

<span data-ttu-id="92c9a-108">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="92c9a-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="92c9a-109">使用上の注意</span><span class="sxs-lookup"><span data-stu-id="92c9a-109">Usage notes</span></span>

<span data-ttu-id="92c9a-110">この関数は、**テキスト** グループからの ER 形式のコンポーネントの**収集したデータ キー名**および**収集したデータ キー値**プロパティに対してコンフィギュレーションされた ER 式で呼び出すことができます。それは**出力の詳細を収集**オプションがオンになっている**共通\\ファイル** コンポーネントの下に存在します。</span><span class="sxs-lookup"><span data-stu-id="92c9a-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="92c9a-111">例</span><span class="sxs-lookup"><span data-stu-id="92c9a-111">Example</span></span>

<span data-ttu-id="92c9a-112">この関数の用途の詳細については、**IT サービス/ソリューション コンポーネントの取得/開発**業務プロセスの一部である [ER 棚卸および集計のために出力された形式の使用](tasks/er-format-counting-summing-1.md) タスク ガイドを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92c9a-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92c9a-113">追加リソース</span><span class="sxs-lookup"><span data-stu-id="92c9a-113">Additional resources</span></span>

[<span data-ttu-id="92c9a-114">データ収集機能</span><span class="sxs-lookup"><span data-stu-id="92c9a-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
