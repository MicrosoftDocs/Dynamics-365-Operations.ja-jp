---
title: GETCURRENTCOMPANY ER 機能
description: このトピックでは、GETCURRENTCOMPANY 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567547"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="c8de4-103">GETCURRENTCOMPANY ER 機能</span><span class="sxs-lookup"><span data-stu-id="c8de4-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8de4-104">`GETCURRENTCOMPANY` 機能は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="c8de4-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8de4-105">構文</span><span class="sxs-lookup"><span data-stu-id="c8de4-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="c8de4-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8de4-106">Return values</span></span>

<span data-ttu-id="c8de4-107">*文字列*</span><span class="sxs-lookup"><span data-stu-id="c8de4-107">*String*</span></span>

<span data-ttu-id="c8de4-108">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="c8de4-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c8de4-109">例</span><span class="sxs-lookup"><span data-stu-id="c8de4-109">Example</span></span>

<span data-ttu-id="c8de4-110">`GETCURRENTCOMPANY ()` は、**Contoso エンターテインメント システム USA** 会社にサイン インしているユーザーに対して **USMF** を返します。</span><span class="sxs-lookup"><span data-stu-id="c8de4-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8de4-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c8de4-111">Additional resources</span></span>

[<span data-ttu-id="c8de4-112">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="c8de4-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]