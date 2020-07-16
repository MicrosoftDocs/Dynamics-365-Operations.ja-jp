---
title: CueReference クラス
description: このトピックでは、CueReference クラスについて説明します。
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
ms.openlocfilehash: 6db6fee2a79542fb020d03e856943b4bce379e17
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502699"
---
# <a name="class-cuereference"></a><span data-ttu-id="38091-103">クラス CueReference</span><span class="sxs-lookup"><span data-stu-id="38091-103">Class CueReference</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CueReference extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="38091-104">備考</span><span class="sxs-lookup"><span data-stu-id="38091-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="38091-105">例</span><span class="sxs-lookup"><span data-stu-id="38091-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="38091-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="38091-106">Methods</span></span>

| <span data-ttu-id="38091-107">方法</span><span class="sxs-lookup"><span data-stu-id="38091-107">Method</span></span>                                | <span data-ttu-id="38091-108">説明</span><span class="sxs-lookup"><span data-stu-id="38091-108">Description</span></span>                                                                                                                       |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38091-109">public str cue(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="38091-109">public str cue(\[str value\])</span></span>         |                                                                                                                                   |
| <span data-ttu-id="38091-110">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="38091-110">public str name(\[str value\])</span></span>        | <span data-ttu-id="38091-111">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="38091-111">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="38091-112">public void new(str cueReferenceName)</span><span class="sxs-lookup"><span data-stu-id="38091-112">public void new(str cueReferenceName)</span></span> | <span data-ttu-id="38091-113">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="38091-113">Initializes a new instance of the TreeNode class.</span></span>                                                                                 |

## <a name="method-cue"></a><span data-ttu-id="38091-114">メソッド cue</span><span class="sxs-lookup"><span data-stu-id="38091-114">Method cue</span></span>

```xpp
public str cue([str value])
```

### <a name="parameters---cue"></a><span data-ttu-id="38091-115">パラメーター - cue</span><span class="sxs-lookup"><span data-stu-id="38091-115">Parameters - cue</span></span>

<span data-ttu-id="38091-116">値</span><span class="sxs-lookup"><span data-stu-id="38091-116">value</span></span>  

### <a name="return-value---cue"></a><span data-ttu-id="38091-117">戻り値 - cue</span><span class="sxs-lookup"><span data-stu-id="38091-117">Return Value - cue</span></span>

## <a name="method-name"></a><span data-ttu-id="38091-118">メソッド名</span><span class="sxs-lookup"><span data-stu-id="38091-118">Method name</span></span>

<span data-ttu-id="38091-119">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="38091-119">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="38091-120">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="38091-120">Parameters - name</span></span>

<span data-ttu-id="38091-121">値</span><span class="sxs-lookup"><span data-stu-id="38091-121">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="38091-122">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="38091-122">Return Value - name</span></span>

<span data-ttu-id="38091-123">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="38091-123">The name used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="38091-124">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="38091-124">Remarks - name</span></span>

<span data-ttu-id="38091-125">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="38091-125">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="38091-126">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="38091-126">Begins with a letter.</span></span>
-   <span data-ttu-id="38091-127">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="38091-127">Does not exceed 250 characters.</span></span>
-   <span data-ttu-id="38091-128">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="38091-128">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="38091-129">句読点やスペースを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="38091-129">Does not include punctuation or spaces.</span></span>
-   <span data-ttu-id="38091-130">テーブルは、拡張データ型、基本列挙型、クラス、他のパブリックオブジェクトなど、他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="38091-130">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and other public objects.</span></span>

## <a name="method-new"></a><span data-ttu-id="38091-131">メソッド new</span><span class="sxs-lookup"><span data-stu-id="38091-131">Method new</span></span>

<span data-ttu-id="38091-132">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="38091-132">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str cueReferenceName)
```

### <a name="parameters---new"></a><span data-ttu-id="38091-133">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="38091-133">Parameters - new</span></span>

<span data-ttu-id="38091-134">cueReferenceName</span><span class="sxs-lookup"><span data-stu-id="38091-134">cueReferenceName</span></span>  
<span data-ttu-id="38091-135">このフォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="38091-135">The name to use to identify this form, report, table, query, or other application object.</span></span>



