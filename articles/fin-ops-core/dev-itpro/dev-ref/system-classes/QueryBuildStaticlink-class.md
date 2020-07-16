---
title: QueryBuildStaticlink クラス
description: このトピックでは、QueryBuildStaticlink クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e175167010565f1e356ab31e6aac689950d14f6e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502863"
---
# <a name="class-querybuildstaticlink"></a><span data-ttu-id="f2851-103">クラス QueryBuildStaticlink</span><span class="sxs-lookup"><span data-stu-id="f2851-103">Class QueryBuildStaticlink</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildStaticlink extends Object
```

<span data-ttu-id="f2851-104">QueryBuildStaticLink クラスは、QueryBuildDataSource クラスで定義されている静的リンクに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f2851-104">The QueryBuildStaticLink class provides the information about the static links that are defined on a QueryBuildDataSource class.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2851-105">備考</span><span class="sxs-lookup"><span data-stu-id="f2851-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="f2851-106">例</span><span class="sxs-lookup"><span data-stu-id="f2851-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f2851-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="f2851-107">Methods</span></span>

| <span data-ttu-id="f2851-108">方法</span><span class="sxs-lookup"><span data-stu-id="f2851-108">Method</span></span>                 | <span data-ttu-id="f2851-109">説明</span><span class="sxs-lookup"><span data-stu-id="f2851-109">Description</span></span>                                                         |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f2851-110">public FieldId field()</span><span class="sxs-lookup"><span data-stu-id="f2851-110">public FieldId field()</span></span> | <span data-ttu-id="f2851-111">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="f2851-111">Provides the field information on which the static link is defined/</span></span> |
| <span data-ttu-id="f2851-112">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="f2851-112">public AnyType value()</span></span> | <span data-ttu-id="f2851-113">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2851-113">Gets the value of the field on which the static link is defined.</span></span>    |
| <span data-ttu-id="f2851-114">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f2851-114">public void finalize()</span></span> |                                                                     |

## <a name="method-field"></a><span data-ttu-id="f2851-115">メソッド field</span><span class="sxs-lookup"><span data-stu-id="f2851-115">Method field</span></span>

<span data-ttu-id="f2851-116">静的リンクが定義されているフィールド情報を提供します/</span><span class="sxs-lookup"><span data-stu-id="f2851-116">Provides the field information on which the static link is defined/</span></span>

```xpp
public FieldId field()
```

### <a name="return-value---field"></a><span data-ttu-id="f2851-117">戻り値 - field</span><span class="sxs-lookup"><span data-stu-id="f2851-117">Return Value - field</span></span>

<span data-ttu-id="f2851-118">静的リンクが定義されているフィールドの FieldId 値。</span><span class="sxs-lookup"><span data-stu-id="f2851-118">The FieldId value of the field on which the static link is defined.</span></span>

## <a name="method-value"></a><span data-ttu-id="f2851-119">メソッド value</span><span class="sxs-lookup"><span data-stu-id="f2851-119">Method value</span></span>

<span data-ttu-id="f2851-120">静的リンクが定義されているフィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2851-120">Gets the value of the field on which the static link is defined.</span></span>

```xpp
public AnyType value()
```

### <a name="return-value---value"></a><span data-ttu-id="f2851-121">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="f2851-121">Return Value - value</span></span>

<span data-ttu-id="f2851-122">静的リンクの値。</span><span class="sxs-lookup"><span data-stu-id="f2851-122">The value of the static link.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="f2851-123">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f2851-123">Method finalize</span></span>

```xpp
public void finalize()
```

