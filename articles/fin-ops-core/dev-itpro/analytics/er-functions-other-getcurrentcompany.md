---
title: GETCURRENTCOMPANY ER 機能
description: このトピックでは、GETCURRENTCOMPANY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: d91caff1a1b89e060a16833e53f3647208ed3826
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041426"
---
# <span data-ttu-id="65ab2-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER 機能</a></span><span class="sxs-lookup"><span data-stu-id="65ab2-103"><a name="GETCURRENTCOMPANY">GETCURRENTCOMPANY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ab2-104">`GETCURRENTCOMPANY` 機能は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する*文字列*値を返します。</span><span class="sxs-lookup"><span data-stu-id="65ab2-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="65ab2-105">構文</span><span class="sxs-lookup"><span data-stu-id="65ab2-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="65ab2-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="65ab2-106">Return values</span></span>

<span data-ttu-id="65ab2-107">*文字列*</span><span class="sxs-lookup"><span data-stu-id="65ab2-107">*String*</span></span>

<span data-ttu-id="65ab2-108">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="65ab2-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="65ab2-109">例</span><span class="sxs-lookup"><span data-stu-id="65ab2-109">Example</span></span>

<span data-ttu-id="65ab2-110">`GETCURRENTCOMPANY ()` は、**Contoso エンターテインメント システム USA** 会社にサイン インしているユーザーに対して **USMF** を返します。</span><span class="sxs-lookup"><span data-stu-id="65ab2-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65ab2-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="65ab2-111">Additional resources</span></span>

[<span data-ttu-id="65ab2-112">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="65ab2-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
