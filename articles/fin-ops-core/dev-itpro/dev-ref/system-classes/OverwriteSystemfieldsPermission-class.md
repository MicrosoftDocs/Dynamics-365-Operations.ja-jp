---
title: OverwriteSystemfieldsPermission クラス
description: このトピックでは、OverwriteSystemfieldsPermission クラスについて説明します。
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
ms.openlocfilehash: d6774eb1b5db4356da9c0759fad43078a379f3c6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502877"
---
# <a name="class-overwritesystemfieldspermission"></a><span data-ttu-id="4f63f-103">クラス OverwriteSystemfieldsPermission</span><span class="sxs-lookup"><span data-stu-id="4f63f-103">Class OverwriteSystemfieldsPermission</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class OverwriteSystemfieldsPermission extends CodeAccessPermission
```

## <a name="remarks"></a><span data-ttu-id="4f63f-104">備考</span><span class="sxs-lookup"><span data-stu-id="4f63f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="4f63f-105">例</span><span class="sxs-lookup"><span data-stu-id="4f63f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4f63f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="4f63f-106">Methods</span></span>

| <span data-ttu-id="4f63f-107">方法</span><span class="sxs-lookup"><span data-stu-id="4f63f-107">Method</span></span>                                                 | <span data-ttu-id="4f63f-108">説明</span><span class="sxs-lookup"><span data-stu-id="4f63f-108">Description</span></span>                                                                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f63f-109">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="4f63f-109">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="4f63f-110">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-110">Creates and returns a copy of a permission class object.</span></span>                                                                  |
| <span data-ttu-id="4f63f-111">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="4f63f-111">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="4f63f-112">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-112">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span> |
| <span data-ttu-id="4f63f-113">public void new()</span><span class="sxs-lookup"><span data-stu-id="4f63f-113">public void new()</span></span>                                      | <span data-ttu-id="4f63f-114">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-114">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>                                                  |

## <a name="method-copy"></a><span data-ttu-id="4f63f-115">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="4f63f-115">Method copy</span></span>

<span data-ttu-id="4f63f-116">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-116">Creates and returns a copy of a permission class object.</span></span>

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a><span data-ttu-id="4f63f-117">戻り値 - copy</span><span class="sxs-lookup"><span data-stu-id="4f63f-117">Return Value - copy</span></span>

<span data-ttu-id="4f63f-118">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="4f63f-118">A copy of the derived class object.</span></span>

### <a name="remarks---copy"></a><span data-ttu-id="4f63f-119">備考 - copy</span><span class="sxs-lookup"><span data-stu-id="4f63f-119">Remarks - copy</span></span>

<span data-ttu-id="4f63f-120">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="4f63f-120">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="4f63f-121">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f63f-121">For more information, see �Securing an API that Executes on the Server Tier.�</span></span>

## <a name="method-issubsetof"></a><span data-ttu-id="4f63f-122">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4f63f-122">Method isSubsetOf</span></span>

<span data-ttu-id="4f63f-123">現在のアクセス許可が、派生クラスによって上書きされている場合に、指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-123">Determines whether a current permission is a subset of the specified permission when it is overridden by a derived class.</span></span>

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a><span data-ttu-id="4f63f-124">パラメーター - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4f63f-124">Parameters - isSubsetOf</span></span>

<span data-ttu-id="4f63f-125">target</span><span class="sxs-lookup"><span data-stu-id="4f63f-125">target</span></span>  
<span data-ttu-id="4f63f-126">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="4f63f-126">A CodeAccessPermission class object.</span></span>

### <a name="return-value---issubsetof"></a><span data-ttu-id="4f63f-127">戻り値 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4f63f-127">Return Value - isSubsetOf</span></span>

<span data-ttu-id="4f63f-128">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4f63f-128">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

### <a name="remarks---issubsetof"></a><span data-ttu-id="4f63f-129">備考 - isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="4f63f-129">Remarks - isSubsetOf</span></span>

<span data-ttu-id="4f63f-130">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="4f63f-130">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="4f63f-131">詳細については、「サーバー層で実行する API の保護」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f63f-131">For more information, see �Securing an API that Executes on the Server Tier.�</span></span>

## <a name="method-new"></a><span data-ttu-id="4f63f-132">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4f63f-132">Method new</span></span>

<span data-ttu-id="4f63f-133">OverwriteSystemfieldsPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4f63f-133">Initializes a new instance of the OverwriteSystemfieldsPermission class.</span></span>

```xpp
public void new()
```


