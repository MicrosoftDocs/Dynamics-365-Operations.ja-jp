---
title: AOSLoadGen クラス
description: このトピックでは、AOSLoadGen クラスについて説明します。
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
ms.openlocfilehash: b3043abc007e647c58c8cb1d5e92e236c54caf67
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502751"
---
# <a name="class-aosloadgen"></a><span data-ttu-id="e8a52-103">クラス AOSLoadGen</span><span class="sxs-lookup"><span data-stu-id="e8a52-103">Class AOSLoadGen</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AOSLoadGen extends Object
```

## <a name="remarks"></a><span data-ttu-id="e8a52-104">備考</span><span class="sxs-lookup"><span data-stu-id="e8a52-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e8a52-105">例</span><span class="sxs-lookup"><span data-stu-id="e8a52-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e8a52-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8a52-106">Methods</span></span>

| <span data-ttu-id="e8a52-107">方法</span><span class="sxs-lookup"><span data-stu-id="e8a52-107">Method</span></span>                                                     | <span data-ttu-id="e8a52-108">説明</span><span class="sxs-lookup"><span data-stu-id="e8a52-108">Description</span></span>                                  |
|------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="e8a52-109">public boolean spawnClass(ClassId classId, str parm)</span><span class="sxs-lookup"><span data-stu-id="e8a52-109">public boolean spawnClass(ClassId classId, str parm)</span></span>       |                                              |
| <span data-ttu-id="e8a52-110">public boolean spawnJob(UtilElementName jobName, str parm)</span><span class="sxs-lookup"><span data-stu-id="e8a52-110">public boolean spawnJob(UtilElementName jobName, str parm)</span></span> |                                              |
| <span data-ttu-id="e8a52-111">public void new(\[UserId user\], \[ClassId infoClass\])</span><span class="sxs-lookup"><span data-stu-id="e8a52-111">public void new(\[UserId user\], \[ClassId infoClass\])</span></span>    | <span data-ttu-id="e8a52-112">AOSLoadGen クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8a52-112">Creates an instance of the AOSLoadGen class.</span></span> |

## <a name="method-spawnclass"></a><span data-ttu-id="e8a52-113">メソッド spawnClass</span><span class="sxs-lookup"><span data-stu-id="e8a52-113">Method spawnClass</span></span>

```xpp
public boolean spawnClass(ClassId classId, str parm)
```

### <a name="parameters---spawnclass"></a><span data-ttu-id="e8a52-114">パラメーター - spawnClass</span><span class="sxs-lookup"><span data-stu-id="e8a52-114">Parameters - spawnClass</span></span>

<span data-ttu-id="e8a52-115">classId</span><span class="sxs-lookup"><span data-stu-id="e8a52-115">classId</span></span>  

<!-- -->

<span data-ttu-id="e8a52-116">parm</span><span class="sxs-lookup"><span data-stu-id="e8a52-116">parm</span></span>  

### <a name="return-value---spawnclass"></a><span data-ttu-id="e8a52-117">戻り値 - spawnClass</span><span class="sxs-lookup"><span data-stu-id="e8a52-117">Return Value - spawnClass</span></span>

## <a name="method-spawnjob"></a><span data-ttu-id="e8a52-118">メソッド spawnJob</span><span class="sxs-lookup"><span data-stu-id="e8a52-118">Method spawnJob</span></span>

```xpp
public boolean spawnJob(UtilElementName jobName, str parm)
```

### <a name="parameters---spawnjob"></a><span data-ttu-id="e8a52-119">パラメーター - spawnJob</span><span class="sxs-lookup"><span data-stu-id="e8a52-119">Parameters - spawnJob</span></span>

<span data-ttu-id="e8a52-120">jobName</span><span class="sxs-lookup"><span data-stu-id="e8a52-120">jobName</span></span>  

<!-- -->

<span data-ttu-id="e8a52-121">parm</span><span class="sxs-lookup"><span data-stu-id="e8a52-121">parm</span></span>  

### <a name="return-value---spawnjob"></a><span data-ttu-id="e8a52-122">戻り値 - spawnJob</span><span class="sxs-lookup"><span data-stu-id="e8a52-122">Return Value - spawnJob</span></span>

## <a name="method-new"></a><span data-ttu-id="e8a52-123">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e8a52-123">Method new</span></span>

<span data-ttu-id="e8a52-124">AOSLoadGen クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e8a52-124">Creates an instance of the AOSLoadGen class.</span></span>

```xpp
public void new([UserId user], [ClassId infoClass])
```

### <a name="parameters---new"></a><span data-ttu-id="e8a52-125">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e8a52-125">Parameters - new</span></span>

<span data-ttu-id="e8a52-126">ユーザー</span><span class="sxs-lookup"><span data-stu-id="e8a52-126">user</span></span>  
<span data-ttu-id="e8a52-127">AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。</span><span class="sxs-lookup"><span data-stu-id="e8a52-127">The information class that is used to create the instance of the AOSLoadGen class.</span></span> <span data-ttu-id="e8a52-128">既定値は情報です。</span><span class="sxs-lookup"><span data-stu-id="e8a52-128">The default value is info.</span></span>

<!-- -->

<span data-ttu-id="e8a52-129">infoClass</span><span class="sxs-lookup"><span data-stu-id="e8a52-129">infoClass</span></span>  
<span data-ttu-id="e8a52-130">AOSLoadGen クラスのインスタンスを作成するために使用される情報クラス。</span><span class="sxs-lookup"><span data-stu-id="e8a52-130">The information class that is used to create the instance of the AOSLoadGen class.</span></span> <span data-ttu-id="e8a52-131">既定値は情報です。</span><span class="sxs-lookup"><span data-stu-id="e8a52-131">The default value is info.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="e8a52-132">備考 - new</span><span class="sxs-lookup"><span data-stu-id="e8a52-132">Remarks - new</span></span>

<span data-ttu-id="e8a52-133">新しいメソッドへの入力を制御することは、セキュリティ上のリスクとなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e8a52-133">Control of the input to the new method could be a security risk.</span></span> <span data-ttu-id="e8a52-134">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="e8a52-134">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="e8a52-135">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="e8a52-135">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="e8a52-136">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e8a52-136">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>
