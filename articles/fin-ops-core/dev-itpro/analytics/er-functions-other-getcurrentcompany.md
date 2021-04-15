---
title: GETCURRENTCOMPANY ER 機能
description: このトピックでは、GETCURRENTCOMPANY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
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
ms.openlocfilehash: 87bef4aa11c01b42af19f7dc20ca8731b9fb4111
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752836"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="39455-103">GETCURRENTCOMPANY ER 機能</span><span class="sxs-lookup"><span data-stu-id="39455-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39455-104">`GETCURRENTCOMPANY` 機能は、現在ユーザーがサイン インしている法人 (会社) コードのテキスト表現する *文字列* 値を返します。</span><span class="sxs-lookup"><span data-stu-id="39455-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="39455-105">構文</span><span class="sxs-lookup"><span data-stu-id="39455-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="39455-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="39455-106">Return values</span></span>

<span data-ttu-id="39455-107">*文字列*</span><span class="sxs-lookup"><span data-stu-id="39455-107">*String*</span></span>

<span data-ttu-id="39455-108">結果テキスト値。</span><span class="sxs-lookup"><span data-stu-id="39455-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="39455-109">例</span><span class="sxs-lookup"><span data-stu-id="39455-109">Example</span></span>

<span data-ttu-id="39455-110">`GETCURRENTCOMPANY ()` は、**Contoso エンターテインメント システム USA** 会社にサイン インしているユーザーに対して **USMF** を返します。</span><span class="sxs-lookup"><span data-stu-id="39455-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39455-111">追加リソース</span><span class="sxs-lookup"><span data-stu-id="39455-111">Additional resources</span></span>

[<span data-ttu-id="39455-112">その他 (ビジネス ドメインの特定の) 関数</span><span class="sxs-lookup"><span data-stu-id="39455-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]