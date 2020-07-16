---
title: MapiRecipDesc クラス
description: このトピックでは、MapiRecipDesc クラスについて説明します。
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
ms.openlocfilehash: 9ac4acbacaa3a4f82247ab9448e37a8fcc21e07b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502578"
---
# <a name="class-mapirecipdesc"></a><span data-ttu-id="887b4-103">クラス MapiRecipDesc</span><span class="sxs-lookup"><span data-stu-id="887b4-103">Class MapiRecipDesc</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapiRecipDesc extends Object
```

## <a name="remarks"></a><span data-ttu-id="887b4-104">備考</span><span class="sxs-lookup"><span data-stu-id="887b4-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="887b4-105">例</span><span class="sxs-lookup"><span data-stu-id="887b4-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="887b4-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="887b4-106">Methods</span></span>

| <span data-ttu-id="887b4-107">方法</span><span class="sxs-lookup"><span data-stu-id="887b4-107">Method</span></span>                                    | <span data-ttu-id="887b4-108">説明</span><span class="sxs-lookup"><span data-stu-id="887b4-108">Description</span></span>                                                                                                                                   |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887b4-109">public str address(\[str Address\])</span><span class="sxs-lookup"><span data-stu-id="887b4-109">public str address(\[str Address\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="887b4-110">public str name(\[str Name\])</span><span class="sxs-lookup"><span data-stu-id="887b4-110">public str name(\[str Name\])</span></span>             | <span data-ttu-id="887b4-111">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="887b4-111">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="887b4-112">public int recipClass(\[int RecipClass\])</span><span class="sxs-lookup"><span data-stu-id="887b4-112">public int recipClass(\[int RecipClass\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="887b4-113">public void new()</span><span class="sxs-lookup"><span data-stu-id="887b4-113">public void new()</span></span>                         | <span data-ttu-id="887b4-114">MapiRecipDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="887b4-114">Initializes a new instance of the MapiRecipDesc class.</span></span>                                                                                        |
| <span data-ttu-id="887b4-115">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="887b4-115">public void finalize()</span></span>                    |                                                                                                                                               |

## <a name="method-address"></a><span data-ttu-id="887b4-116">メソッド address</span><span class="sxs-lookup"><span data-stu-id="887b4-116">Method address</span></span>

```xpp
public str address([str Address])
```

### <a name="parameters---address"></a><span data-ttu-id="887b4-117">パラメーター - address</span><span class="sxs-lookup"><span data-stu-id="887b4-117">Parameters - address</span></span>

<span data-ttu-id="887b4-118">アドレス</span><span class="sxs-lookup"><span data-stu-id="887b4-118">Address</span></span>  

### <a name="return-value---address"></a><span data-ttu-id="887b4-119">戻り値 - address</span><span class="sxs-lookup"><span data-stu-id="887b4-119">Return Value - address</span></span>

## <a name="method-name"></a><span data-ttu-id="887b4-120">メソッド名</span><span class="sxs-lookup"><span data-stu-id="887b4-120">Method name</span></span>

<span data-ttu-id="887b4-121">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="887b4-121">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str Name])
```

### <a name="parameters---name"></a><span data-ttu-id="887b4-122">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="887b4-122">Parameters - name</span></span>

<span data-ttu-id="887b4-123">氏名</span><span class="sxs-lookup"><span data-stu-id="887b4-123">Name</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="887b4-124">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="887b4-124">Return Value - name</span></span>

<span data-ttu-id="887b4-125">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="887b4-125">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="887b4-126">備考 - name</span><span class="sxs-lookup"><span data-stu-id="887b4-126">Remarks - name</span></span>

<span data-ttu-id="887b4-127">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="887b4-127">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="887b4-128">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="887b4-128">Begins with a letter.</span></span>
-   <span data-ttu-id="887b4-129">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="887b4-129">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="887b4-130">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="887b4-130">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="887b4-131">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="887b4-131">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="887b4-132">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="887b4-132">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-recipclass"></a><span data-ttu-id="887b4-133">メソッド recipClass</span><span class="sxs-lookup"><span data-stu-id="887b4-133">Method recipClass</span></span>

```xpp
public int recipClass([int RecipClass])
```

### <a name="parameters---recipclass"></a><span data-ttu-id="887b4-134">パラメーター - recipClass</span><span class="sxs-lookup"><span data-stu-id="887b4-134">Parameters - recipClass</span></span>

<span data-ttu-id="887b4-135">RecipClass</span><span class="sxs-lookup"><span data-stu-id="887b4-135">RecipClass</span></span>  

### <a name="return-value---recipclass"></a><span data-ttu-id="887b4-136">戻り値 - recipClass</span><span class="sxs-lookup"><span data-stu-id="887b4-136">Return Value - recipClass</span></span>

## <a name="method-new"></a><span data-ttu-id="887b4-137">メソッド new</span><span class="sxs-lookup"><span data-stu-id="887b4-137">Method new</span></span>

<span data-ttu-id="887b4-138">MapiRecipDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="887b4-138">Initializes a new instance of the MapiRecipDesc class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="887b4-139">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="887b4-139">Method finalize</span></span>

```xpp
public void finalize()
```

